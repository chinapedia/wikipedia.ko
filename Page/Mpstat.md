> This article is converted from Wikipedia: [Mpstat](https://ko.wikipedia.org/wiki/Mpstat).


**mpstat**는 [유닉스](https://ko.wikipedia.org/wiki/유닉스 "wikilink") 방식의 [운영 체제에](https://ko.wikipedia.org/wiki/운영_체제 "wikilink") 쓰이는 [컴퓨터](https://ko.wikipedia.org/wiki/컴퓨터 "wikilink") 명령 줄 [소프트웨어](https://ko.wikipedia.org/wiki/소프트웨어 "wikilink")의 하나로, [프로세서](https://ko.wikipedia.org/wiki/중앙_처리_장치 "wikilink") 관련 통계를 화면에 보고한다. [CPU](https://ko.wikipedia.org/wiki/중앙_처리_장치 "wikilink") [사용률에](https://ko.wikipedia.org/wiki/CPU_타임 "wikilink") 대한 통계를 작성하거나 문제를 진단할 목적으로 컴퓨터 감시에 사용된다.

## 설명

**mpstat** 명령어는 이용 가능한 각각의 [프로세서에](https://ko.wikipedia.org/wiki/중앙_처리_장치 "wikilink") 대한 활동을 표준 출력에 기록한다.

mpstat는 [SMP](https://ko.wikipedia.org/wiki/대칭형_다중_처리 "wikilink") 및 UP 머신에 둘 다 사용할 수 있으나 후자의 경우 전역 평균 활동만 출력된다.

## 사용법

    $ mpstat <주기> <횟수>

주기는 통계 줄이 출력되는 시간의 간격을 뜻한다. 횟수는 출력하고자 하는 줄의 수를 가리킨다.

[iostat](https://ko.wikipedia.org/wiki/iostat "wikilink"), [vmstat](https://ko.wikipedia.org/wiki/vmstat "wikilink")과 같이 mpstat의 출력 첫 줄은 시스템 시동 이후의 평균치를 포함한다. 최종 줄은 현재의 값을 나타낸다.

## 예

리눅스에서의 출력의 예는 다음과 같다:

    $ mpstat
    Linux 2.4.21-32.ELsmp (linux00)        07/04/07

    10:26:54     CPU   %user   %nice %system %iowait    %irq   %soft   %idle    intr/s
    10:26:54     all    0.07    0.00    0.16    8.48    0.00    0.09   91.18    165.49

솔라리스 11에서의 예:

    $ mpstat
    CPU minf mjf xcal  intr ithr  csw icsw migr smtx  srw syscl  usr sys  wt idl
      0    0   0    0   329  121  169    6    0    0    0   406    0   1   0  98

AIX 6에서의 예:

    $ mpstat 1 1

    System configuration: lcpu=8 ent=1.0 mode=Uncapped

    cpu  min  maj  mpc  int   cs  ics   rq  mig lpa sysc us sy wa id   pc  %ec  lcs
      0    8    0    0  182  336  102    0    0 100 1434 38 51  0 12 0.02  1.8  185
      1    0    0    0   11    5    5    0    0   -    0  0 19  0 81 0.00  0.1   12
      2    0    0    0    1    0    0    0    0   -    0  0 42  0 58 0.00  0.0    0
      3    0    0    0    1    0    0    0    0   -    0  0 43  0 57 0.00  0.0    0
      4    0    0    0    1    0    0    0    0   -    0  0 45  0 55 0.00  0.0    0
      5    0    0    0    1    0    0    0    0   -    0  0 44  0 56 0.00  0.0    0
      6    0    0    0    1    0    0    0    0   -    0  0  2  0 98 0.00  0.0    0
      7    0    0    0   53    5    5    0    0   -    0  0 66  0 34 0.00  0.2   54
      U    -    -    -    -    -    -    -    -   -    -  -  -  0 99 0.99 99.0    -
    ALL    8    0    0  251  346  112    0    0 100 1434  0  0  0 99 0.02  2.0  251

## 같이 보기

  - [유닉스 명령어 목록](../Page/유닉스_명령어_목록.md "wikilink")

## 참고문헌

  - [Linux mpstat man page](https://web.archive.org/web/20160403064806/http://linuxcommand.org/man_pages/mpstat1.html)
  - [AIX mpstat manual page](https://archive.is/20130103041138/http://publib.boulder.ibm.com/infocenter/aix/v6r1/index.jsp?topic=/com.ibm.aix.cmds/doc/aixcmds3/mpstat.htm)

## 외부 링크

  - [sysstat](http://perso.orange.fr/sebastien.godard/) - includes mpstat

[분류:유닉스 소프트웨어](https://ko.wikipedia.org/wiki/분류:유닉스_소프트웨어 "wikilink")