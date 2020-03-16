> This article is converted from Wikipedia: [At \(\)](https://ko.wikipedia.org/wiki/At_\(\)).


[유닉스 계열](../Page/유닉스_계열.md "wikilink") 컴퓨터 [운영 체제에서](../Page/운영_체제.md "wikilink") **at**는 미래 어느 특정 시간에 특정 [명령어를](https://ko.wikipedia.org/wiki/명령어_\(컴퓨팅\) "wikilink") 한 차례 실행하기 위해 쓰이는 명령어이다.

## 디자인

at는 [표준 입력으로부터](https://ko.wikipedia.org/wiki/표준_입력 "wikilink") 일련의 명령어들을 읽어들인 다음 미래의 시간에 수행될 하나의 "at-job"으로 모은다. 이 job은 현재의 환경을 상속하는데 이는 동일한 [작업 디렉터리에서](https://ko.wikipedia.org/wiki/작업_디렉터리 "wikilink") 실행되어야 하고 예약을 했을 때와 동일한 [환경 변수를](../Page/환경_변수.md "wikilink") 가지고 실행되어야 하기 때문이다.

한 시간에 한 차례, 매주 화요일, 매년 1월 1일처럼 반복해서 실행하는 [cron](https://ko.wikipedia.org/wiki/cron "wikilink")과는 다르다. cron처럼 수많은 유닉스 운영 체제들은 관리자가 at 명령어에 접근을 제한하도록 할 수 있다.

## 사용법

1월 31일 오전 11시 45분에 [C](../Page/C_\(프로그래밍_언어\).md "wikilink") 프로그램을 컴파일하는 샘플 프로그램이다:

``` bash
 $ echo "cc -o foo foo.c" | at 1145 jan 31
```

또는

``` bash
 $ at 1145 jan 31
 at> cc -o foo foo.c
 at> ^D #(press Control-D while at the beginning of a line)
```

**atq** 프로그램은 현재의 대기열의 job들을 나열하며, **atrm**은 대기열에 있는 job을 제거한다:

``` console
$ atq
1234 2011-08-12 11:45 cc -o foo foo.c user
$ atrm 1234
$ atq
$
```

[윈도우 NT](../Page/윈도우_NT.md "wikilink")/[2000](../Page/윈도우_2000.md "wikilink")/[XP](../Page/윈도우_XP.md "wikilink")/[7에서도](https://ko.wikipedia.org/wiki/윈도우_7 "wikilink") [cron](https://ko.wikipedia.org/wiki/cron "wikilink")과 비슷한 [`at`](https://ko.wikipedia.org/wiki/윈도우_작업_스케줄러 "wikilink") 명령어가 존재하지만 [작업 스케줄러를](https://ko.wikipedia.org/wiki/윈도우_작업_스케줄러 "wikilink") 선호하면서 이용이 권장되지 않는다.

## 같이 보기

  - [cron](https://ko.wikipedia.org/wiki/cron "wikilink")
  - [systemd](https://ko.wikipedia.org/wiki/systemd "wikilink")
  - [유닉스 명령어 목록](../Page/유닉스_명령어_목록.md "wikilink")

## 외부 링크

  -
[분류:표준 유닉스 프로그램](https://ko.wikipedia.org/wiki/분류:표준_유닉스_프로그램 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink") [분류:유닉스 프로세스 및 작업 관리 관련 소프트웨어](https://ko.wikipedia.org/wiki/분류:유닉스_프로세스_및_작업_관리_관련_소프트웨어 "wikilink")