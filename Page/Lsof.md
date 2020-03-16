> This article is converted from Wikipedia: [Lsof](https://ko.wikipedia.org/wiki/Lsof).


**lsof**는 list open files(열려있는 파일 나열)을 뜻하는 명령으로, 수많은 [유닉스 계열](../Page/유닉스_계열.md "wikilink") 운영 체제에서 열려있는 모든 파일과, 그 파일들을 열고 있는 프로세스들의 목록을 출력한다. 이 [오픈 소스](../Page/오픈_소스.md "wikilink") 유틸리티는 [퍼듀 대학교](../Page/퍼듀_대학교.md "wikilink") 컴퓨팅 센터의 부소장으로 은퇴한 빅터 A. 아벨이 개발·지원하였다. 일부 유닉스 계열에서 동작하며 지원한다.\[1\]

## 예

시스템에 열려 있는 파일들로는 모든 프로세스가 열고 있는 디스크 파일, [지명 파이프](https://ko.wikipedia.org/wiki/지명_파이프 "wikilink"), [네트워크 소켓](https://ko.wikipedia.org/wiki/네트워크_소켓 "wikilink"), 장치를 포함한다. 지정되지 않은 파일들이 사용 중이라는 이유로 디스크를 마운트할 수 없을 때 이용하면 유용하다. 열려있는 파일들을 사용하고 있는 프로세스를 식별하기 위해 (필요 시 적절히 필터링도 가능) 사용할 수 있다.

``` bash
# lsof /var
COMMAND     PID     USER   FD   TYPE DEVICE SIZE/OFF   NODE NAME
syslogd     350     root    5w  VREG  222,5        0 440818 /var/adm/messages
syslogd     350     root    6w  VREG  222,5   339098   6248 /var/log/syslog
cron        353     root  cwd   VDIR  222,5      512 254550 /var -- atjobs
```

데몬과 관련된 포트를 보는 방법은 다음과 같다:

``` bash
# lsof -i -n -P | grep sendmail
sendmail  31649    root    4u  IPv4 521738       TCP *:25 (LISTEN)
```

위에서 "sendmail"을 보면 표준 포트 25를 대기하고 있는 것을 확인할 수 있다.

  - `-i` IP 소켓을 나열한다.
  - `-n` 호스트 이름을 결정하지 않는다 (DNS 없음).
  - `-P` 포트 이름을 결정하지 않는다 (이름 대신 포트 번호 나열).

`lsof -U`를 이용하면 유닉스 소켓을 나열할 수 있다.

## 같이 보기

  - [fuser](https://ko.wikipedia.org/wiki/fuser "wikilink")
  - [netstat](https://ko.wikipedia.org/wiki/netstat "wikilink")
  - [strace](https://ko.wikipedia.org/wiki/strace "wikilink")

## 각주

<references />

## 외부 링크

  -

  -
  -
  - [Using lsof](http://danielmiessler.com/study/lsof)

  - [Troubleshooting Runnings Systems with lsof](https://web.archive.org/web/20110809005534/http://www.digitalprognosis.com/linuxtips/troubleshooting-running-systems-with-lsof/)

  - [Lsof FAQ](https://web.archive.org/web/20150822095342/http://gd.tuwien.ac.at/utils/admin-tools/lsof/FAQ)

  - Sam Nelson's [PCP](https://web.archive.org/web/20070509052951/http://www.unix.ms/pcp/) script, an alternative to "lsof -i" for Solaris.

  - [Glsof](http://glsof.sourceforge.net/) is two separate utilities (Queries and Filemonitor) based on lsof.

[분류:유닉스 파일 시스템 관련 소프트웨어](https://ko.wikipedia.org/wiki/분류:유닉스_파일_시스템_관련_소프트웨어 "wikilink")

1.