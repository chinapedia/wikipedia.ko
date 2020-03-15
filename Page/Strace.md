> This article is converted from Wikipedia: [Strace](https://ko.wikipedia.org/wiki/Strace).


**strace**는 진단, [디버그](https://ko.wikipedia.org/wiki/디버그 "wikilink"), 지시적 [사용자 공간](https://ko.wikipedia.org/wiki/사용자_공간 "wikilink") 유틸리티이다. [시스템 호출](https://ko.wikipedia.org/wiki/시스템_호출 "wikilink"), [신호](../Page/유닉스_신호.md "wikilink") 전달자, 프로세스 상태의 변화를 포함하는 [프로세스](https://ko.wikipedia.org/wiki/프로세스 "wikilink")와 [리눅스 커널](https://ko.wikipedia.org/wiki/리눅스_커널 "wikilink") 간 상호 작용을 감시하는데 사용된다. strace는 [ptrace](https://ko.wikipedia.org/wiki/ptrace "wikilink")라는 커널 기능을 통해 사용될 수 있다.

일부 [유닉스 계열](https://ko.wikipedia.org/wiki/유닉스_계열 "wikilink") 운영 체제는 [truss](https://ko.wikipedia.org/wiki/truss "wikilink")와 같은 strace 유사 진단 도구를 제공한다.

## 역사

strace는 본래 1991년에 [썬OS](https://ko.wikipedia.org/wiki/썬OS "wikilink")가 작성한 것으로, 저작권 고지에 따르면 1992년 일찍이 comp.sources.sun 제3권에 출판되었다. 초기 [README](https://ko.wikipedia.org/wiki/README "wikilink") 파일은 다음을 포함하였다:\[1\]

    strace(1)는 썬이 제공했던 프로그램 trace(1)과 매우 비슷한 썬(tm) 시스템용
    시스템 호출 트레이서이다. strace(1)은 디버그 프로그램을 정렬하는데 유용한
    유틸리티로서 안타깝게도 썬이 제공했던 시스템 소프트웨어 거의 대부분이
    그러하듯 소스는 제공되지 않는다.

나중에 Branko Lankester는 이 버전을 [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink")로 포팅하였으며, 그의 버전은 1992년 11월 공개되었고 1993년에 제2판이 공개되었다.\[2\]\[3\] Richard Sladkey는 이 각각의 strace 버전을 병합하였고 1994년에 이 프로그램을 [SVR4](https://ko.wikipedia.org/wiki/SVR4 "wikilink")와 [솔라리스에](https://ko.wikipedia.org/wiki/솔라리스_\(운영_체제\) "wikilink") 이식하였으며\[4\] 그 결과 1994년 중순에 comp.source.misc에 strace 3.0을 발표하기에 이르렀다.\[5\]

비 [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink") 운영 체제용 일부(죽은\[6\]) 코드가 포함된 strace의 마지막 버전은 2011년 3월에 공개된 4.6이다.\[7\] 2012년 5월 공개된 strace 버전 4.7에서는\[8\] 리눅스와 관련 없는 모든 코드가 제거되었다.\[9\]

## 사용

가장 일반적인 사용은 strace를 사용하여 프로그램을 시작하고 이것이 프로그램에 의해 만들어진 시스템 호출들의 리스트를 보여주는 것이다. 이것은 만약 프로그램이 지속적으로 충돌되거나 예상대로 행동하지 않는 경우에 유용하다; 예를 들면 strace를 사용하는 것이 프로그램이 존재하지 않거나 읽을 수 없는 파일에 대한 접근을 시도하는지를 밝힐 수 있다. 대체 애플리케이션은 -p 플래그를 사용해서 실행 중인 프로세스를 어태치하는 것이다. 이것은 프로세스가 반응이 중단되었을 때 유용할 수 있으며, 예를 들면 프로세스가 네트워크 연결을 시도하는 동안 블록된 것을 밝힐 수 있다. strace가 단지 시스템 호출들을 보여주기 때문에, [GNU 디버거](https://ko.wikipedia.org/wiki/GNU_디버거 "wikilink") 같은 코드 디버거만큼의 많은 문제들을 탐지할 수는 없다. 그러나 코드 디버거를 사용하는 것보다 쉬운 방법이며, 시스템 관리자들에게 극단적으로 유용한 도구이다. 이것은 또한 연구자들이 이후 시스템 호출 재개를 추적하기 위한 용도로 시스템 호출 트레이스를 생성하는데 사용될 수 있다.\[10\]\[11\]\[12\]

## 예시

다음은 strace 명령어의 일반적인 예시를 보여준다.

    open(".", O_RDONLY|O_NONBLOCK|O_LARGEFILE|O_DIRECTORY|O_CLOEXEC) = 3
    fstat64(3, {st_mode=S_IFDIR|0755, st_size=4096, ...}) = 0
    fcntl64(3, F_GETFD)                     = 0x1 (flags FD_CLOEXEC)
    getdents64(3, /* 18 entries */, 4096)   = 496
    getdents64(3, /* 0 entries */, 4096)    = 0
    close(3)                                = 0
    fstat64(1, {st_mode=S_IFIFO|0600, st_size=0, ...}) = 0
    mmap2(NULL, 4096, PROT_READ|PROT_WRITE, MAP_PRIVATE|MAP_ANONYMOUS, -1, 0) = 0xb7f2c000
    write(1, "autofs\nbackups\ncache\nflexlm\ngames"..., 86autofsA

위의 내용들은 'ls' 명령어를 실행했을 때의 출력의 단지 작은 부분만을 보여준다. 이것은 현재 워킹 디렉토리가 열려있으며, 조사되고 있고 내용이 검색된다는 것을 보여준다. 파일 이름들의 결과 리스트는 표준 출력으로 쓰여졌다.

## 비슷한 도구

다른 운영 체제들에서 비슷한 역할을 하는 도구들이 존재한다.

  - [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink")는 라이브러리와 시스템 호출들을 트레이스할 수 있는 [ltrace](https://ko.wikipedia.org/wiki/ltrace "wikilink")가 있으며, X 윈도우 프로그램들을 트레이스할 수 있는 xtrace\[13\], [SystemTap](https://ko.wikipedia.org/wiki/SystemTap "wikilink") 등이 있다.
  - [마이크로소프트 윈도우는](https://ko.wikipedia.org/wiki/마이크로소프트_윈도우 "wikilink") StraceNT\[14\]라고 불리는 비슷한 유틸리티가 있으며 [프로세스 모니터라고](../Page/프로세스_모니터.md "wikilink") 불리는 비슷한 GUI 기반 유틸리티도 존재한다.

## 같이 보기

  - [gdb](https://ko.wikipedia.org/wiki/gdb "wikilink")
  - [lsof](https://ko.wikipedia.org/wiki/lsof "wikilink")

## 각주

## 외부 링크

  - [Project page](http://sourceforge.net/projects/strace/)
  - [Manual page](http://man7.org/linux/man-pages/man1/strace.1.html)
  - [OS Reviews article on strace](http://www.osreviews.net/reviews/admin/strace)

[분류:유닉스 프로그래밍 도구](https://ko.wikipedia.org/wiki/분류:유닉스_프로그래밍_도구 "wikilink") [분류:C로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C로_작성된_자유_소프트웨어 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.