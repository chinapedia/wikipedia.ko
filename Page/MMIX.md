> This article is converted from Wikipedia: [MMIX](https://ko.wikipedia.org/wiki/MMIX).


[섬네일](https://ko.wikipedia.org/wiki/파일:Mmix.png "wikilink") **MMIX**는 [도널드 커누스가](https://ko.wikipedia.org/wiki/도널드_커누스 "wikilink") 만든 [64비트](../Page/64비트.md "wikilink") [RISC](https://ko.wikipedia.org/wiki/RISC "wikilink") [가상기계](https://ko.wikipedia.org/wiki/가상기계 "wikilink")이다. [MIPS](https://ko.wikipedia.org/wiki/MIPS_아키텍처 "wikilink") 칩을 만든 [존 L. 헤네시와](https://ko.wikipedia.org/wiki/존_L._헤네시 "wikilink") [DEC 알파](../Page/DEC_알파.md "wikilink") 칩을 설계한 [딕 사이츠도](https://ko.wikipedia.org/wiki/딕_사이츠 "wikilink") MMIX의 설계에 많은 기여를 했다. 카누스에 따르면 앞으로 그가 쓰는 *[The Art of Computer Programming](https://ko.wikipedia.org/wiki/The_Art_of_Computer_Programming "wikilink")* (TAoCP)에서는 MMIX를 이용하여 [컴퓨터 프로그래밍의](../Page/컴퓨터_프로그래밍.md "wikilink") 기계 수준 알고리즘 분석을 할 것이라고 한다. MMIX는 '엠믹스'라고 읽는다.

MMIX의 이전 버전인 [MIX](https://ko.wikipedia.org/wiki/MIX "wikilink")는 *The Art of Computer Programming*의 현재판까지만 사용된다. MMIX는 컴퓨터 설계에 대한 현대적인 접근방법을 모두 채택하여 처음부터 새로 만들어졌으며 기존의 MIX를 완전히 대체할 것이다.

## 구조

MMIX는 64 비트의 [가상주소공간](https://ko.wikipedia.org/wiki/가상주소공간 "wikilink")을 가진 [빅 엔디안](https://ko.wikipedia.org/wiki/빅_엔디안 "wikilink") 형태의 [이진](../Page/이진법.md "wikilink") [컴퓨터](../Page/컴퓨터.md "wikilink")이다. 명령어는 32비트이다.

### 명령어

모든 명령어는 관련된 약어를 가지고 있다. 예를 들어 명령어 32는 'ADD'와 연결된다. 대부분의 명령은 "OP, X, Y, Z"과 같은 형태를 따른다. 여기서 OP는 명령어에 해당하고, X는 결과값을 저장할 레지스터이다. 나머지는 명령어에 인자로 사용할 값들을 저장한다. 여기서 명령어의 각 부분은 모두 8비트이다. 예를 들어 "ADD $0, $1, 3"라는 명령은 1번 레지스터의 값에 3을 더해서 그 결과값을 0번 레지스터에 저장한다." 라는 의미이다. MMIX 프로그램은 보통 [MMIXAL](https://ko.wikipedia.org/wiki/MMIXAL_프로그래밍_언어 "wikilink") 어셈블리 언어로 구성된다.

#### [Hello world 프로그램](https://ko.wikipedia.org/wiki/Hello_world_프로그램 "wikilink")

MMIXAL로 Hello, world를 출력하는 프로그램이다.

``` mmix
Main GETA $255,string ; Get the address of the string
                                        ; in register 255.

        TRAP  0,Fputs,StdOut            ; Put the string pointed to
                                        ; by register 255 to file StdOut.

        TRAP  0,Halt,0                  ; End process.

string BYTE "Hello, world!",#a,0 ; String to be printed.
                                        ; #a is newline,
                                        ; 0 terminates the string.
```

### 레지스터

MMIX 칩에는 $0부터 $255까지 256개의 범용 레지스터와 32개의 특수 레지스터가 있다.

#### 지역 레지스터 스택

#### 특수 레지스터

## 참고 문헌

  - Donald E. Knuth (1999). *MMIXware: A RISC Computer for the Third Millennium*. Heidelberg: Springer-Verlag. [(errata)](http://www-cs-faculty.stanford.edu/~knuth/mmixware.html)

## 외부 링크

  - [Donald Knuth's MMIX page](http://www-cs-faculty.stanford.edu/~knuth/mmix.html) — MMIX에 대한 간략한 소개와 왜 'The Art of Computer Programming'에 가상의 [어셈블리어](../Page/어셈블리어.md "wikilink")를 이용할 수밖에 없었는지에 대한 설명.
  - [Donald Knuth's MMIX news page](http://www-cs-faculty.stanford.edu/~knuth/mmix-news.html) — [CWEB](https://ko.wikipedia.org/wiki/CWEB "wikilink")으로 만든 MMIX의 [오픈 소스](../Page/오픈_소스.md "wikilink") 시뮬레이터와 프로그래머 매뉴얼, 예제 프로그램.
  - [MMIXmasters web site](https://web.archive.org/web/20070516201842/http://mmixmasters.sourceforge.net/) TAOCP 1권 \~ 3권에서 예전 MIX로 만든 예제 프로그램을 새로운 MMIX로 바꾸려는 사람(MMIXmasters)들의 모임.

[분류:컴퓨터 프로그래밍](https://ko.wikipedia.org/wiki/분류:컴퓨터_프로그래밍 "wikilink") [분류:추상기계](https://ko.wikipedia.org/wiki/분류:추상기계 "wikilink") [분류:도널드 커누스](https://ko.wikipedia.org/wiki/분류:도널드_커누스 "wikilink") [분류:명령어 집합 구조](https://ko.wikipedia.org/wiki/분류:명령어_집합_구조 "wikilink")