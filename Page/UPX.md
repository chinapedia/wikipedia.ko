> This article is converted from Wikipedia: [UPX](https://ko.wikipedia.org/wiki/UPX).


**UPX**(**U**ltimate **P**acker for e**X**ecutables)는 여러 운영체제에서 수많은 파일 포맷을 지원하는 [오픈 소스](../Page/오픈_소스.md "wikilink") [실행 파일 압축](../Page/실행_파일_압축.md "wikilink") 프로그램이다. [GNU 일반 공중 사용 허가서를](../Page/GNU_일반_공중_사용_허가서.md "wikilink") 통해 공개된 [자유 소프트웨어이다](../Page/자유_소프트웨어.md "wikilink"). 압축, 압축 해제의 기능을 모두 담당한다.

## 압축

UPX는 UCL이라는 이름의 [데이터 압축 알고리즘을](../Page/데이터_압축.md "wikilink") 사용하며\[1\], 이 구현은 사유 NRV(*Not Really Vanished*\[2\]) 알고리즘의 일부인 [오픈 소스로](../Page/오픈_소스.md "wikilink") 되어 있다.\[3\]

2.90 베타 이후부터 UPX는 대부분의 플랫폼을 대상으로 [LZMA](../Page/LZMA.md "wikilink")를 사용할 수 있으나 16비트의 오래된 컴퓨터에서 압축 해제 속도 저하 현상이 일어나기 때문에 기본값으로는 비활성화되어 있다. (강제로 사용하려면 --lzma 사용)

## 압축 해제

UPX는 압축 해제를 위해 두 개의 메커니즘을 지원한다.

1.  인 플레이스(in-place) 테크닉
2.  [임시 파일로의](https://ko.wikipedia.org/wiki/임시_파일 "wikilink") 해제

실행 파일을 메모리로 해제하는 인 플레이스 테크닉은 모든 플랫폼에서 이용이 가능한 것은 아니다. 나머지 플랫폼에서는 임시 파일로의 압축 해제를 사용한다. 이 과정에는 추가적인 오버헤드와 기타 단점들이 동반되지만, 어떠한 실행 파일 포맷도 압축이 가능하게 한다.

임시 파일로 해제는 방식은 몇 가지 단점이 존재한다:

  - [suid와](https://ko.wikipedia.org/wiki/setuid "wikilink") 같은 특수 권한이 무시된다.
  - `argv[0]`의 의미가 없어진다.
  - 여러 인스턴스로 실행 중인 실행 프로그램들은 공통된 세그먼트를 공유할 수 없다.

수정되지 않은 UPX 압축이 자주 발견되며 [바이러스 검사 소프트웨어](../Page/바이러스_검사_소프트웨어.md "wikilink") 스캐너를 통해 압축이 해제된다. UPX 또한 이미 압축된 미수정 실행 파일들의 압축을 해제할 수 있는 기능이 자체 내장되어 있다.

## 지원 포맷

  - [ARM](../Page/ARM_아키텍처.md "wikilink")/[pe](../Page/PE_포맷.md "wikilink")
  - [atari](https://ko.wikipedia.org/wiki/atari "wikilink")/tos
  - \*[BSD](../Page/BSD.md "wikilink")/[i386](https://ko.wikipedia.org/wiki/i386 "wikilink")
  - [djgpp2](https://ko.wikipedia.org/wiki/DJGPP "wikilink")/[coff](https://ko.wikipedia.org/wiki/COFF "wikilink")
  - dos/[com](../Page/COM_파일.md "wikilink")
  - dos/[exe](../Page/EXE.md "wikilink")
  - dos/sys
  - [리눅스](../Page/리눅스.md "wikilink")/[i386](https://ko.wikipedia.org/wiki/i386 "wikilink") [a.out](https://ko.wikipedia.org/wiki/a.out "wikilink")
  - [리눅스](../Page/리눅스.md "wikilink")/[ELF](https://ko.wikipedia.org/wiki/ELF "wikilink"): [i386](https://ko.wikipedia.org/wiki/i386 "wikilink"), [x86-64](https://ko.wikipedia.org/wiki/x86-64 "wikilink"), [ARM](../Page/ARM_아키텍처.md "wikilink"), [파워PC](../Page/파워PC.md "wikilink")
  - [리눅스](../Page/리눅스.md "wikilink")/커널: [i386](https://ko.wikipedia.org/wiki/i386 "wikilink"), [x86-64](https://ko.wikipedia.org/wiki/x86-64 "wikilink"), [ARM](../Page/ARM_아키텍처.md "wikilink")
  - mach/ppc32, mach/i386
  - rtm32/[pe](../Page/PE_포맷.md "wikilink")
  - tmt/adam
  - [ps1](https://ko.wikipedia.org/wiki/플레이스테이션 "wikilink")/exe
  - [watcom](https://ko.wikipedia.org/wiki/watcom "wikilink")/le
  - [win32](https://ko.wikipedia.org/wiki/win32 "wikilink")/[pe](../Page/PE_포맷.md "wikilink") ([닷넷 프레임워크를](../Page/닷넷_프레임워크.md "wikilink") 사용하여 만든 파일은 제외)

## 각주

<references />

## 외부 링크

  - [UPX 웹사이트](http://upx.sourceforge.net/)
  - [UPX 소스포지](http://sourceforge.net/projects/upx/)

[분류:압축 소프트웨어](https://ko.wikipedia.org/wiki/분류:압축_소프트웨어 "wikilink") [분류:1998년 소프트웨어](https://ko.wikipedia.org/wiki/분류:1998년_소프트웨어 "wikilink") [분류:C++로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C++로_작성된_자유_소프트웨어 "wikilink") [분류:자유 압축 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_압축_소프트웨어 "wikilink")

1.  <http://www.oberhumer.com/opensource/ucl/>
2.  <http://www.oberhumer.com/products/nrv/>
3.  <http://upx.hg.sourceforge.net/hgweb/upx/upx/file/5d434f4a3fe7/README.SRC>