> This article is converted from Wikipedia: [DOSEMU](https://ko.wikipedia.org/wiki/DOSEMU).


**DOSEMU**는 [MS-DOS](../Page/MS-DOS.md "wikilink") 시스템을 사용할 수 있는 [호환성 계층의](https://ko.wikipedia.org/wiki/호환성_계층 "wikilink") [소프트웨어](../Page/소프트웨어.md "wikilink") 꾸러미다. [x86](https://ko.wikipedia.org/wiki/x86 "wikilink") 기반의 [개인용 컴퓨터](../Page/개인용_컴퓨터.md "wikilink")(IBM PC 호환 컴퓨터)에서 리눅스를 쓴다 해도 [도스](../Page/도스.md "wikilink")용 소프트웨어를 구동할 수 있다.

[하드웨어](https://ko.wikipedia.org/wiki/하드웨어 "wikilink") [가상화 기술과](https://ko.wikipedia.org/wiki/가상화_기술 "wikilink") 전략적인 [에뮬레이션](https://ko.wikipedia.org/wiki/에뮬레이션 "wikilink")을 함께 사용한다. 8086 호환 도스 운영 체제와 x86 호환 프로세서의 응용 프로그램의 속도와 x86-64 프로세서와 더불어 x86 호환 프로세서 위의 32비트 [DPMI](../Page/DPMI.md "wikilink") 응용 프로그램들의 속도가 거의 네이티브에 근접했다. 가상 8086 모드는 [x86-64](https://ko.wikipedia.org/wiki/x86-64 "wikilink") 롱 모드에서 사용할 수 없기 때문에 DOSEMU는 8086 프로세서 에뮬레이터를 포함하여 16비트 응용 프로그램의 사용을 지원하고 있다.

현재는 x86 [리눅스](../Page/리눅스.md "wikilink") 시스템에서만 사용할 수 있다.

## 기능

DOSEMU는 오래된 도스용 소프트웨어를 계속 쓰고자 하는 사람들을 위한 선택 사항이다. 매뉴얼에서 DOSEMU는 리눅스 커널과 80386 프로세서의 특별한 기능을 사용하여 MS-DOS/프리도스/DR-DOS를 실행하는 사용자 수준의 프로그램이라고 적혀 있다. 사람들은 이를 도스 상자라고 부르며 다음과 같은 기능이 있다[1](http://dosemu.sourceforge.net/docs/HOWTO/):

  - 모든 입출력, 프로세서 제어 기능을 가상화한다.
  - 완전한 보호 모드 환경에서 실행되는 동안 iAPX86 프로세서 계열의 리얼 모드의 워드 크기와 주소 모드를 지원한다.
  - 모든 도스와 바이오스 시스템 호출을 간섭하고 적절한 동작과 성능을 위해 이러한 호출을 가상으로 구현한다.
  - 도스 프로그램이 제어에 익숙할 수 있도록 하드웨어 환경을 시뮬레이트한다.
  - 네이티브 리눅스 서비스를 통해 도스 서비스를 제공한다. 이를테면 DOSEmu는 리눅스 디렉터리 계급인 가상 하드 디스크 드라이브를 제공한다.

## 같이 보기

  - [가상 도스 머신](../Page/가상_도스_머신.md "wikilink")
  - [도스박스](../Page/도스박스.md "wikilink")

## 각주

## 외부 링크

  - [DOSEMU 웹사이트](http://www.dosemu.org/)

[분류:도스 에뮬레이터](https://ko.wikipedia.org/wiki/분류:도스_에뮬레이터 "wikilink") [분류:호환성 계층](https://ko.wikipedia.org/wiki/분류:호환성_계층 "wikilink")