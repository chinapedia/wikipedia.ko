> This article is converted from Wikipedia: [Fuser \(유닉스\)](https://ko.wikipedia.org/wiki/Fuser_\(유닉스\)).


[유닉스](../Page/유닉스.md "wikilink") [명령어](../Page/명령어_\(컴퓨팅\).md "wikilink") **fuser**는 어느 [프로세스](../Page/프로세스.md "wikilink")가 특정 [컴퓨터 파일](../Page/컴퓨터_파일.md "wikilink"), [파일 시스템](../Page/파일_시스템.md "wikilink"), [유닉스 도메인 소켓을](https://ko.wikipedia.org/wiki/유닉스_도메인_소켓 "wikilink") 사용하는지를 표시하기 위해 사용된다.

## 예제

이를테면 USB 드라이브에 접근하는 프로세스 ID와 사용자를 확인하려면:

``` console
$ fuser -m -u /mnt/usb1
/mnt/usb1:   1347c(root)  1348c(guido)  1349c(guido)
```

이 명령어는 특정 파일 또는 파일 시스템을 사용하는 프로세스의 [프로세스 식별자를](../Page/프로세스_식별자.md "wikilink") 표시한다. 기본 디스플레이 모드에서 개별 파일 이름에는 접근 유형을 의미하는 문자가 뒷따른다:

  - c : 현재 디렉터리.
    e : 실행 중인 실행 파일.
    f : 열려있는 파일.
    F : 쓰기를 위해 열려있는 파일.
    r : 루트 디렉터리.
    m : mmap된 파일 또는 공유 디렉터리

이 명령어는 어느 프로세스가 네트워크 포트를 사용하는지 검사하기 위해서도 사용할 수 있다:

``` console
$ fuser -v -n tcp 80
                     USER        PID ACCESS COMMAND
80/tcp:              root       3067 F.... (root)httpd
                     apache     3096 F.... (apache)httpd
                     apache     3097 F.... (apache)httpd
```

이 명령어는 접근 중인 파일이 없거나 치명적인 오류가 발생할 경우 0이 아닌 코드를 반환한다. 적어도 하나의 접근이 성공하여야 fuser는 0을 반환한다. fuser의 출력은 파일 시스템의 [언마운트를](../Page/Mount_\(유닉스\).md "wikilink") 시도할 때 리소스 비지(resource busy) 메시지를 진단하는데 유용할 수 있다.

## 옵션

  - \-k : 파일에 접근 중인 모든 프로세스를 kill한다. 예: `fuser -k /path/to/your/filename`는 확인 과정 없이 이 디렉터리에 접근 중인 모든 프로세스를 죽인다. 확인 처리를 위해서는 -i를 사용할 것.
    \-i : 상호작용 모드. 프로세스를 kill하기 전에 확인 과정을 거친다
    \-v : 버보스(verbose) 모드
    \-u : 사용자 이름 추가
    \-a : 모든 파일 표시
    \-m : `name`는 마운트되어 있는 블록 장치 또는 마운트된 파일 시스템의 파일을 지정한다. 해당 파일 시스템의 파일들에 접근하는 모든 프로세스가 나열된다.

\-k는 SIGKILL을 모든 프로세스에 보낸다. -signal을 사용하여 다른 신호를 보낼 수 있다. 지원되는 신호 목록의 경우 fuser -l을 입력하여 확인할 수 있다.

## 관련 명령어

  - [lsof](https://ko.wikipedia.org/wiki/lsof "wikilink")
  - [BSD](../Page/BSD.md "wikilink") 운영 체제의 fuser 버전: `fstat(1)`

## 외부 링크

[분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink") [분류:유닉스 프로세스 및 작업 관리 관련 소프트웨어](https://ko.wikipedia.org/wiki/분류:유닉스_프로세스_및_작업_관리_관련_소프트웨어 "wikilink")