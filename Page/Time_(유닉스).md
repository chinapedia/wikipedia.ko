> This article is converted from Wikipedia: [Time \(유닉스\)](https://ko.wikipedia.org/wiki/Time_\(유닉스\)).


[컴퓨팅](../Page/컴퓨팅.md "wikilink")에서 **`time`**은 [유닉스](../Page/유닉스.md "wikilink"), [유닉스 계열](../Page/유닉스_계열.md "wikilink") 운영 체제의 명령어이다. 특정 [명령어의](../Page/명령어_\(컴퓨팅\).md "wikilink") 실행 시간을 확인하는데 사용한다.

## 개요

time(1)은 [GNU](../Page/GNU.md "wikilink") time와 같이 독립 프로그램으로 존재할 수 있고, 대부분의 경우(예: [sh](../Page/유닉스_셸.md "wikilink"), [bash](../Page/배시_\(유닉스_셸\).md "wikilink"), [Tcsh](../Page/Tcsh.md "wikilink") 또는 [Z 셸](../Page/Z_셸.md "wikilink")) [셸](../Page/유닉스_셸.md "wikilink") 내장으로 존재할 수 있다.

### 사용자 시간 vs 시스템 시간

총 CPU 시간은 CPU가 일부 프로그램의 동작을 수행하기 위해 소요된 시간의 양, 그리고 프로그램 대신 [커널의](../Page/커널_\(컴퓨팅\).md "wikilink") [시스템 호출을](../Page/시스템_호출.md "wikilink") 수행하는데 소요된 시간을 합친 것이다. 프로그램이 배열을 통해 루프를 돌 때 사용자 CPU 시간이 축적된다. 이와 반대로, 프로그램이 `exec` 또는 `fork`와 같은 [시스템 호출을](../Page/시스템_호출.md "wikilink") 실행할 때 시스템 CPU 타임을 축적한다.

### 실시간 vs CPU 타임

이 문맥에서 "실시간"이라는 용어는 스톱 워치를 사용하는 것처럼 경과된 [벽시계 시간을](https://ko.wikipedia.org/wiki/벽시계_시간 "wikilink") 가리킨다. 총 CPU 타임(사용자 시간 + 시스템 시간)은 어느 정도 해당 값과 비슷할 수 있다. 프로그램이 온전히 실행이 아닌 대기로만 어느 정도 시간을 소요할 수 있기 때문에(사용자 모드냐 시스템 모드냐에 따라) 실시간은 총 CPU 시간보다 더 클 수 있다. CPU 시간(사용자, 시스템 둘 다)이 `time` 명령에 의해 보고된 값에 추가된 칠드런을 프로그램이 포크할 수 있으므로(멀티코어 시스템에서 태스크들은 병렬로 수행됨) 총 CPU 시간은 실시간보다 더 클 수 있다.

## 사용법

명령어를 사용하려면 다음과 같이 단순히 `time` 단어를 우선하여 명령어를 지정하면 된다:

``` bash
$ time ls
```

명령어가 실행될 때 `time`는 사용자 [CPU 타임](../Page/CPU_타임.md "wikilink"), 시스템 CPU 타임, 실시간 측면에서 얼마나 오랫동안 [`ls`](../Page/Ls_\(유닉스\).md "wikilink") 명령어의 실행이 소요되었는지를 보고한다. 출력 포맷은 명령어의 버전에 따라 다양하며 일부는 다음과 같은 추가적인 통계를 제공하기도 한다:

``` console
$ time host wikipedia.org
wikipedia.org has address 103.102.166.224
wikipedia.org mail is handled by 50 mx2001.wikimedia.org.
wikipedia.org mail is handled by 10 mx1001.wikimedia.org.
host wikipedia.org  0.04s user 0.02s system 7% cpu 0.780 total
$
```

time(독립 프로그램이든, 또는 POSIX 모드로 Bash 셸이 실행 중이면서 time이 `time -p`로 호출 시)은 표준 오류 출력에 보고한다.

### time -p

포터블 스크립트는 다른 출력 포맷을 사용하지만 다양한 출력 포맷을 사용하는 `time -p`를 사용하는 것이 좋으며, 여러 구현체에서 다음과 같이 일정한 형태를 지닌다:

``` console
$ time -p sha256sum /bin/ls
12477deb0e25209768cbd79328f943a7ea8533ece70256cdea96fae0ae34d1cc  /bin/ls
real 0.00
user 0.00
sys 0.00
$
```

## 구현체

### GNU time

현재 버전의 GNU time은 기본적으로 시간 외에 더 많은 정보를 보고한다:

``` console
$ /usr/bin/time sha256sum /bin/ls
12477deb0e25209768cbd79328f943a7ea8533ece70256cdea96fae0ae34d1cc  /bin/ls
0.00user 0.00system 0:00.00elapsed 100%CPU (0avgtext+0avgdata 2156maxresident)k
0inputs+0outputs (0major+96minor)pagefaults 0swaps
$
```

[GNU](../Page/GNU.md "wikilink") time의 출력 포맷은 **`TIME`** 환경 변수를 사용하여 조정할 수 있으며 실행 시간 외의 정보(예: 메모리 사용률)를 포함할 수 있다. 이러한 동작은 일반 [POSIX](../Page/POSIX.md "wikilink") 호환 time에서, 또 `time -p`로 실행 중에는 사용할 수 없다.

이 time의 설명 문서는 보통 `man 1 time`를 사용하여 접근할 수 있다.

#### 운용 방식

GNU의 `time` 구현체의 소스 코드에 따르면 `time`로 표시되는 더 많은 정보는 `wait3` 시스템 호출에서 가져온 것이다. 상태 정보를 반환하는 `wait3` 호출이 없는 시스템에서는 `times` 시스템 호출을 대신 사용한다.

### Bash

유명한 유닉스 셸 [Bash에서](../Page/배시_\(유닉스_셸\).md "wikilink"), **`time`**은 특수 키워드로서, [파이프라인](https://ko.wikipedia.org/wiki/파이프라인 "wikilink")(또는 단일 명령) 이전에 둘 수 있으며 하나의(처음) 명령어만이 아닌 파이프라인 전반의 시간을 측정하며 다른 기본 포맷을 사용하며 시간을 보고하기 전에 빈 줄을 추가한다:

``` console
$ time seq 10000000 | wc -l
10000000

real    0m0.078s
user    0m0.116s
sys 0m0.029s
$
```

보고되는 시간은 **`seq`**와 **`wc``   ``-l`**를 함께 사용한 시간이다. 출력 포맷은 **`TIMEFORMAT`** 변수를 사용하여 조정할 수 있다.

시간은 내장형이 아닌, 특수 키워드이며 함수나 명령으로 처리될 수 없다. 또, 파이프라인 리다이렉이션은 무시한다.("POSIX 모드"로 Bash를 실행하지 않은 경우 `time -p`으로 실행할 때에도)

이 time의 설명 문서는 `man 1 bash`를 사용하여, 또는 bash 그 자체에서 `help time`를 사용하여 접근할 수 있다.

## 같이 보기

  - [시스템 시간](../Page/시스템_시간.md "wikilink")
  - [Cron](../Page/Cron.md "wikilink")
  - [TIME (명령어)](https://ko.wikipedia.org/wiki/TIME_\(명령어\) "wikilink")

## 참고 문헌

  -
  -
[분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink") [분류:유닉스 프로세스 및 작업 관리 관련 소프트웨어](https://ko.wikipedia.org/wiki/분류:유닉스_프로세스_및_작업_관리_관련_소프트웨어 "wikilink")