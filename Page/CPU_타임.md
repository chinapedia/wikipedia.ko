> This article is converted from Wikipedia: [CPU ](https://ko.wikipedia.org/wiki/CPU_).


[섬네일](https://ko.wikipedia.org/wiki/파일:CpuTimeonSingleCpuMultiTaskingSystem.svg "wikilink") [섬네일](https://ko.wikipedia.org/wiki/파일:CPU_Time.png "wikilink") 시스템([GNU](https://ko.wikipedia.org/wiki/GNU "wikilink")/[리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink"))에서 [top](https://ko.wikipedia.org/wiki/top_\(소프트웨어\) "wikilink") 프로그램을 이용하여 CPU 타임을 보고 있다. (TIME+ 컬럼.) \]\]

**CPU 타임**() 또는 **CPU 사용률**()은 한 컴퓨터 [프로그램이](https://ko.wikipedia.org/wiki/컴퓨터_프로그램 "wikilink") [CPU를](https://ko.wikipedia.org/wiki/중앙_처리_장치 "wikilink") 차지하여 일을 한 [시간](https://ko.wikipedia.org/wiki/시간 "wikilink")의 양을 뜻한다. 보통 [클럭 틱](https://ko.wikipedia.org/wiki/클럭_틱 "wikilink") 단위로 측정된다. 프로그램들 사이의 CPU 사용률을 비교하기 위해 사용된다.

## 하위 구분

CPU 시간 또는 CPU 사용률은 전체 시스템을 기준으로 각 스레드별로나 각 프로세스별로 보고할 수 있다. 게다가 CPU가 무엇을 하고 있는지에 따라 보고되는 값은 다음과 같이 분류할 수 있다:

  - 사용자 시간(user time): CPU가 [사용자 공간에서](https://ko.wikipedia.org/wiki/사용자_공간 "wikilink") 코드를 실행할 때 바쁜 시간의 양.
  - 시스템 시간(system time): CPU가 [커널 공간에서](https://ko.wikipedia.org/wiki/커널_공간 "wikilink") 코드를 실행할 때 바쁜 시간의 양.
  - 유휴 시간(idle time, 전체 시스템에만 적용): CPU가 바쁘지 않은 시간의 양. [시스템 유휴 프로세스의](../Page/시스템_유휴_프로세스.md "wikilink") 시간.
  - 스틸 타임(steal time, 전체 시스템에만 적용): [가상화](../Page/가상화.md "wikilink") 하드웨어에서 [운영 체제가](https://ko.wikipedia.org/wiki/운영_체제 "wikilink") 실행을 원하지만 [하이퍼바이저](https://ko.wikipedia.org/wiki/하이퍼바이저 "wikilink")에 의해 허용되지 않은 시간의 양.\[1\]

## 같이 보기

  - [CPU](https://ko.wikipedia.org/wiki/중앙_처리_장치 "wikilink")
  - [프로세스](../Page/프로세스.md "wikilink")
  - [시스템 타임](https://ko.wikipedia.org/wiki/시스템_타임 "wikilink")
  - [어도비 플래시](../Page/어도비_플래시.md "wikilink")(주로 저사양 컴퓨터에서 높은 CPU 사용률을 일으킴)

## 참고 자료

  -
## 각주

## 외부 링크

  - [GNU glibc manual: clock and times functions](http://www.gnu.org/software/libc/manual/html_node/Processor-And-CPU-Time.html#Processor-And-CPU-Time)

[분류:컴퓨터 성능](https://ko.wikipedia.org/wiki/분류:컴퓨터_성능 "wikilink")

1.