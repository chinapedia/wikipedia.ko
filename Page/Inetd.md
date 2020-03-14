> This article is converted from Wikipedia: [Inetd](https://ko.wikipedia.org/wiki/Inetd).


**inetd** (**i**nter**net** service **d**aemon)는 [유닉스](https://ko.wikipedia.org/wiki/유닉스 "wikilink") 시스템에서 돌아가는 [슈퍼 서버](https://ko.wikipedia.org/wiki/슈퍼_서버 "wikilink") [데몬으로서](https://ko.wikipedia.org/wiki/데몬_\(컴퓨팅\) "wikilink") [인터넷](https://ko.wikipedia.org/wiki/인터넷 "wikilink") 서비스들을 제공한다. 각 설정된 서비스들을 위해서, 이것은 연결된 클라이언트들로부터 요청을 리슨한다. 요청들은 적절한 실행 파일을 실행시키는 과정을 통해 서비스되지만, *echo* 같은 간단한 것들은 inetd 스스로 처리한다. 요청에 따라 실행되는 외부 실행 파일들은 단일 또는 다중 스레드일 수 있다. 처음 [4.3BSD에서](https://ko.wikipedia.org/wiki/BSD "wikilink") 공개되었으며, 일반적으로 `/usr/sbin/inetd`에 위치한다.

## 기능

종종 [슈퍼 서버로](https://ko.wikipedia.org/wiki/슈퍼_서버 "wikilink") 불리는 inetd는 [FTP](https://ko.wikipedia.org/wiki/FTP "wikilink"), [POP3](https://ko.wikipedia.org/wiki/POP3 "wikilink") 그리고 [텔넷](https://ko.wikipedia.org/wiki/텔넷 "wikilink") 등의 서비스들에서 사용하는 포트들을 리슨한다. [TCP](https://ko.wikipedia.org/wiki/TCP "wikilink") 패킷 또는 [UDP](https://ko.wikipedia.org/wiki/UDP "wikilink") 패킷이 특정한 목적 포트 번호로 도착하면, inetd는 적절한 서버 프로그램을 실행해서 연결을 처리하게 한다. 고하중으로 실행되도록 설계되지 않은 서비스들의 경우에 이 방식이 매우 효율적인게, 특정한 서버를 오직 필요할 때만 실행시킬 수 있기 때문이다. 게다가 inetd가 생성한 프로세스의 stdin, stdout 그리고 stderr을 직접 후킹하므로 서비스 프로그램들에서 네트워크 코드가 필요치 않다. 빈번한 트래픽이 발생하는 [HTTP](https://ko.wikipedia.org/wiki/HTTP "wikilink")나 POP3 서버의 경우에는 트래픽을 직접 받는것이 더 선호된다.

## 설치

서비스되는 서비스들의 목록은 보통 `/etc/inetd.conf` 설정 파일에 기록된다. 데몬은 설정을 다시 읽기 위해 신호를 필요로 할 수 있다. 아래는 텔넷의 설정이다.

`telnet  stream  tcp6    nowait  root    /usr/sbin/telnetd      telnetd -a`

`telnet`은 서비스의 공식 이름이다. `/etc/services`에서 확인할 수 있다.

`telnet          23/tcp`

두번째와 세번째는 각각 소켓의 종류와 프로토콜이다. `/etc/protocols` 데이터베이스에서 확인할 수 있다.

네번째는 wait/nowait 스위치이다. 단일 스레드 서버는 inetd가 자신이 모든 데이터를 읽을 때까지 기다려줄 것으로 예상한다. 그외에는 inetd는 서버가 새로운 요청에 대한 새로 생성한 프로세스를 실행하도록 한다.

다섯번째는 사용자 이름으로서 `/etc/passwd`에서 확인한다. 이것은 서비스 프로그램이 실행되는 이름이다.

마지막으로 외부 프로그램에 주어진 경로와 인자이다. 일반적으로 첫 번째 인자는 프로그램 이름이다. 예를 들면 inetd는 프로그램 `/usr/sbin/telnetd`를 명령 줄 인자 `telnetd -a`로 실행한다. inetd는 서버 프로그램의 stdin, stdout 그리고 stderr에 대한 소켓을 자동으로 후킹한다.

일반적으로 TCP 소켓들은 각 연결을 동시에 다루기 위해 분리된 서버를 생성하는 형식으로 다뤄진다. UDP 소켓들은 일반적으로 단일 서버가 포트의 모든 패킷을 다룬다.

echo 같은 간단한 서비스들은 inetd에 의해 직접적으로 다뤄지며, 외부 서버를 생성하지 않는다.

## inetd 서비스 생성

이것은 [C로](https://ko.wikipedia.org/wiki/C_\(프로그래밍_언어\) "wikilink") 쓰여진 간단한 inetd 서비스이다. 이것은 로그 파일을 위한 파일 이름이 포함된 명령 줄 인자를 기대한다. 그리고 소켓을 통해 보내진 모든 문자열들을 이 로그 파일에 기록한다. 

``` c
#include <stdio.h>
#include <stdlib.h>

int main(int argc, char **argv)
{
  const char *fn = argv[1];
  FILE *fp = fopen(fn, "a+");

  if(fp == NULL)
    exit(EXIT_FAILURE);

  char str[4096];
  //inetd passes its information to us in stdin.
  while(fgets(str, sizeof(str), stdin)) {
    fputs(str, fp);
    fflush(fp);
  }
  fclose(fp);
  return 0;
}
```

이 예제는 stdio 함수를 사용하며 stdin으로 들어오는 네트워크 트래픽에 반응한다. 이 경우에 우리는 요청된 서비스에 대해서 한 서비스만 돌아가고, 모든 메시지들이 단일 파일에 기록되기를 원한다. 이것은 UDP를 사용하는게 좋다는 것이다. 첫째로, 사용되지 않는 포트 번호가 선택되어야 한다. 여기서는 9999가 사용되었다.  `/etc/services` 엔트리는 다음과 같다.

`errorLogger 9999/udp`

그리고 `/etc/inetd.conf`에서의 엔트리는 다음과 같다.

`errorLogger dgram udp wait root /usr/local/bin/errlogd errlogd /tmp/logfile.txt`

이것은 inetd에게 `/usr/local/bin/errlogd` 프로그램을 실행하도록  `errlogd /tmp/logfile.txt`와 같이 말한다. 파일 이름을 포함한 첫 번째 인자는 로그 파일로 사용된다. (`/tmp/logfile.txt`) inetd는 필요할 때 서비스를 실행시키고, 포트 9999를 입출력 스트림에 붙일 것이다. 그리고 포트에 보내진 모든 문자열들은 이 파일에 저장된다. **wait**를 명시하면서, 이것은 inetd에게 모든 요청을 다룰 때 오직 서버의 한 인스턴스만 사용하도록 한다.

## inetd 대체

최근에 원래 버전의 보안 한계 때문에 [xinetd](https://ko.wikipedia.org/wiki/xinetd "wikilink"), rlinetd, ucspi-tcp, 그리고 다른 많은 시스템들로 대체되었다. [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink")와 [Mac OS X는](https://ko.wikipedia.org/wiki/OS_X "wikilink") [xinetd](https://ko.wikipedia.org/wiki/xinetd "wikilink")를 사용한다.

inetd에 의해 제공되는 서비스들은 전체적으로 생략되었다. 이것은 기계들이 점점 단일 기능에 전념하게 되었기 때문이다. 예를 들면 HTTP 서버는 단지 [httpd](https://ko.wikipedia.org/wiki/httpd "wikilink")를 돌리기 위해 설정되었고, 다른 포트를 열어놓지 않는다. [방화벽도](https://ko.wikipedia.org/wiki/방화벽_\(네트워킹\) "wikilink") 전용 기계로서 다른 서비스들을 사용하지 않는다.

## 보안 문제

inetd의 서비스 디스패처로서의 개념이 본질적으로 불안정하지는 않지만, inetd가 제공하는 서비스들의 긴 목록은 컴퓨터 보안 전문가들이 사용을 그만두게 만들었다. 익스플로잇 가능한 결함이나 서비스의 남용에 대한 가능성을 고려해야 하기 때문이다. 현재의 리눅스 배포판에서는 거의 쓰이지 않고 있다.

## 같이 보기

  - [TCP 래퍼](../Page/TCP_래퍼.md "wikilink")
  - [xinetd](https://ko.wikipedia.org/wiki/xinetd "wikilink")
  - [TCP/UDP의 포트 목록](https://ko.wikipedia.org/wiki/TCP/UDP의_포트_목록 "wikilink")
  - [Svchost.exe](https://ko.wikipedia.org/wiki/Svchost.exe "wikilink")

## 외부 링크

  -
[분류:유닉스 네트워크 관련 소프트웨어](https://ko.wikipedia.org/wiki/분류:유닉스_네트워크_관련_소프트웨어 "wikilink")