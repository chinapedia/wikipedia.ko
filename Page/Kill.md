> This article is converted from Wikipedia: [Kill](https://ko.wikipedia.org/wiki/Kill).


**kill**은 [유닉스 계열](../Page/유닉스_계열.md "wikilink") [운영 체제에서](../Page/운영_체제.md "wikilink") 시스템상에서 동작하고 있는 [프로세스](../Page/프로세스.md "wikilink")에 간단한 메시지(시그널)를 보내는 명령어이다. 기본적으로 보내는 메시지는 종료 메시지이고 프로세스에 종료하는 것을 요구한다. 하지만 kill은 그 명칭과는 조금 다르게 종료와 무관한 메시지를 보낼 때도 사용한다. kill 명령어는 내부적으로 kill()이란 [시스템 콜을](https://ko.wikipedia.org/wiki/시스템_콜 "wikilink") 사용하여 구현하고, [프로세스 식별자](../Page/프로세스_식별자.md "wikilink")(PID)로 지시한 프로세스와 [프로세스 그룹 식별자](https://ko.wikipedia.org/wiki/프로세스_그룹_식별자 "wikilink")(PGID)로 지시한 프로세스 그룹에 시그널을 보낸다. kill은 예전부터 독립적인 유틸리티로 제공되었으나 많은 프로그램은 약간 다른 형태의 kill 명령어를 가지고 있다.

사용자가 일반적으로 가장 많이 사용하는 시그널은 SIGTERM과 SIGKILL인데, kill은 이 외에도 서로 다른 다양한 종류의 시그널을 보내는 것이 가능하다. 기본적으로 보내지는 시그널은 SIGTERM이다. 이 시그널을 받은 프로세스는 프로그램을 종료하기 전에 프로그램을 종료하는 처리(환경설정을 파일에 기록한다던지...)를 수행하는 것이 가능하다.

프로세스는 SIGKILL과 SIGSTOP을 제외한 모든 시그널에 대해서 시그널에 대한 처리를 하는 별도의 루틴을 만들 수 있다. 이것은 프로세스가 시그널을 받았을 때 어떤 특별한 처리를 하기 위함이다. 예외적으로, 프로세스는 SIGKILL과 SIGSTOP에 대한 처리를 할 수 없도록 되어있다. SIGKILL은 프로세스를 강제 종료하는 명령이고 SIGSTOP은 SIGCONT 시그널을 받을 때까지 프로그램 실행을 정지시키는 명령이다.

유닉스는 권한없는 사용자가 프로세스를 종료하는 것을 방지하기 위해 보안 기능을 제공하고 있다. 기본적으로는 어떤 프로세스가 다른 프로세스로 시그널을 보낼 때, 시그널을 보내는 프로세스의 소유자가 시그널을 받는 프로세스의 소유자와 같은지, 최고 관리자인지 확인하게 된다.

사용 가능한 시그널은 고유한 명칭이 있고 특정한 숫자와 대응되어 있다. 유닉스의 설계에 따라서 시그널과 숫자의 대응이 다른 것은 주의할 필요가 있다. SIGTERM은 많은 경우 15이고, SIGKILL은 많은 경우 9이다.

일반적으로 해당 Process에 문제가 있어서 다시 시작하고자 할 때에는 SIGHUP, SIGTERM, SIGKILL의 순서로 각각 시도하길 바란다.

아래 명령어로 전체 시그널의 리스트를 볼 수 있다.

``` bash
$ kill -l
 1) SIGHUP   2) SIGINT   3) SIGQUIT  4) SIGILL   5) SIGTRAP
 6) SIGABRT  7) SIGBUS   8) SIGFPE   9) SIGKILL 10) SIGUSR1
11) SIGSEGV 12) SIGUSR2 13) SIGPIPE 14) SIGALRM 15) SIGTERM
16) SIGSTKFLT   17) SIGCHLD 18) SIGCONT 19) SIGSTOP 20) SIGTSTP
21) SIGTTIN 22) SIGTTOU 23) SIGURG  24) SIGXCPU 25) SIGXFSZ
26) SIGVTALRM   27) SIGPROF 28) SIGWINCH    29) SIGIO   30) SIGPWR
31) SIGSYS  34) SIGRTMIN    35) SIGRTMIN+1  36) SIGRTMIN+2  37) SIGRTMIN+3
38) SIGRTMIN+4  39) SIGRTMIN+5  40) SIGRTMIN+6  41) SIGRTMIN+7  42) SIGRTMIN+8
43) SIGRTMIN+9  44) SIGRTMIN+10 45) SIGRTMIN+11 46) SIGRTMIN+12 47) SIGRTMIN+13
48) SIGRTMIN+14 49) SIGRTMIN+15 50) SIGRTMAX-14 51) SIGRTMAX-13 52) SIGRTMAX-12
53) SIGRTMAX-11 54) SIGRTMAX-10 55) SIGRTMAX-9  56) SIGRTMAX-8  57) SIGRTMAX-7
58) SIGRTMAX-6  59) SIGRTMAX-5  60) SIGRTMAX-4  61) SIGRTMAX-3  62) SIGRTMAX-2
63) SIGRTMAX-1  64) SIGRTMAX
```

사용 중인 셸에 kill 명령을 내장하고 있을 수 있으며, /bin/kill과는 조금 다를 수 있다.

## 마이크로소프트 윈도우

마이크로소프트의 [윈도우 파워셸의](https://ko.wikipedia.org/wiki/윈도우_파워셸 "wikilink") 명령 줄 인터프리터에서 kill은 Stop-Process라는 cmdlet의 미리 정의된 명령 별칭이다.

[마이크로소프트 윈도우 XP](../Page/윈도우_XP.md "wikilink"), [비스타](../Page/윈도우_비스타.md "wikilink"), [7](https://ko.wikipedia.org/wiki/윈도우_7 "wikilink") 이상의 운영 체제에서는 taskkill이라는 명령을 사용하여 프로세스를 종료할 수 있다.

## 외부 링크

  - 명령어:
  - 시스템 호출:

[분류:윈도우 명령어](https://ko.wikipedia.org/wiki/분류:윈도우_명령어 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink") [분류:유닉스 프로세스 및 작업 관리 관련 소프트웨어](https://ko.wikipedia.org/wiki/분류:유닉스_프로세스_및_작업_관리_관련_소프트웨어 "wikilink") [분류:프로세스](https://ko.wikipedia.org/wiki/분류:프로세스 "wikilink") [분류:윈도우 관리](https://ko.wikipedia.org/wiki/분류:윈도우_관리 "wikilink")