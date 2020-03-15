> This article is converted from Wikipedia: [DPMI](https://ko.wikipedia.org/wiki/DPMI).


**도스 보호 모드 인터페이스**(DOS Protected Mode Interface), 곧 **DPMI**는 [도스](https://ko.wikipedia.org/wiki/도스 "wikilink") 프로그램이 [리얼 모드에서](https://ko.wikipedia.org/wiki/리얼_모드 "wikilink") 사용할 수 없는 수많은 프로세서 기능들에 접근할 수 있게 해 주며 [보호 모드에서](https://ko.wikipedia.org/wiki/보호_모드 "wikilink") 돌아가도록 도와 주는 인터페이스이다. 거의 모든 도스 확장자들은 DPMI에 바탕을 두며 DOS 프로그램들이, [개인용 컴퓨터](https://ko.wikipedia.org/wiki/개인용_컴퓨터 "wikilink") 안에서 사용할 수 있는 모든 메모리의 기억 장치에 번지를 넣게 하여 보호 모드에서 돌아가도록 도와준다. 처음에 윈도 3.0을 위해 [마이크로소프트](https://ko.wikipedia.org/wiki/마이크로소프트 "wikilink")사에서 고안된 것이다.

이러한 서비스는 16비트나 32비트, 유니버설(universal)이 될 수 있으며, 'DPMI 커널', 'DPMI 호스트', 아니면 'DPMI 서버'라고도 한다. 호스트 운영체제 (가상 DPMI 호스트) 또는 도스 확장자(리얼 DPMI 호스트)가 이를 제공한다. DPMI 커널은 "보통 내장할 수 있는" DOS4GW, DOS32A, PMODEW, 아니면 별개로 떼어 쓸 수 있는 CWSDPMI 또는 HPDMI와 같이, 도스 확장자의 일부가 될 수 있다.

DPMI의 첫 규격 도안은 1989년에 출간되었다. 버전 0.9는 DPMI 위원회에서 1990년에 제정했으며 1991년에 버전 1.0으로 연장하였다. 부가 기능으로 "True DPMI", 즉 "도스 [API](../Page/API.md "wikilink") 해석"이 있는데 0.9 버전의 도안에 선언되었지만 공식 규격의 일부가 되지 못했다. 그럼에도 불구하고 몇몇 제품은 이 기능을 지원한다. DPMI 규격은 [인텔](https://ko.wikipedia.org/wiki/인텔 "wikilink") 리터러쳐 세일즈(Literature Sales) 및 온라인에서 읽어 볼 수 있다. 버전 1.0이 [윈도에](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 도입되지 않았기 때문에 많은 프로그램들과 도스 확장자들은 버전 0.9 기반으로만 만들어야 했다. 가장 잘 알려져 있는 DPMI의 별개 커널은 아마 [CWSDPMI](https://ko.wikipedia.org/wiki/CWSDPMI "wikilink")겠지만 DPMI 0.9만 지원하고 "도스 API 변화"를 지원하지 않는다. 더 새로운 제품으로 [HDPMI](https://ko.wikipedia.org/wiki/HDPMI "wikilink")가 있는데 이것은 "도스 API 변화"와 대부분의 DPMI 1.0 기능들을 지원한다. 현재 [DPMIONE](https://ko.wikipedia.org/wiki/DPMIONE "wikilink")은 독립식 DPMI 호스트이며 DPMI 1.0을 완전히 지원한다.

## VCPI

**VCPI**(가상 제어 프로그램 인터페이스:Virtual Control Program Interface)는 DPMI와 똑같은 일을 하기 위한 더 이전에 나온 비호환 방식이었으며 32비트 모드에 제한을 받았다. VCPI는 도스의 [확장 메모리](https://ko.wikipedia.org/wiki/중첩_확장_메모리_규격 "wikilink") 관리자(보기: [CEMM](https://ko.wikipedia.org/wiki/CEMM "wikilink"), [QEMM](https://ko.wikipedia.org/wiki/QEMM "wikilink"), 나중에는 [EMM386](https://ko.wikipedia.org/wiki/EMM386 "wikilink"))가 제공하였다. DPMI의 등장으로 VCPI는 가려지기 시작했는데, 주된 원인은 첫째, 윈도 3.0의 네이티브 [보호 모드](https://ko.wikipedia.org/wiki/보호_모드 "wikilink"), 곧 386 확장 모드에서 실행되는 도스 프로그램에 대한 지원이 없었다는 것이고, 둘째로는 VCPI가 Ring 0에서 프로그램들을 실행하여 x86 보호의 목적을 무효하게 하기 때문이다. 이것은 [OS/2](https://ko.wikipedia.org/wiki/OS/2 "wikilink") 2.0 이후에서도 동작하지 않았다. 윈도 3.x만 VCPI를 표준/리얼 모드에서 지원하였다. 초기의 윈도/386 2.1은 도스 확장들과 전혀 호환성이 없었다.

VCPI는 또한 공간 제약이 있었다. 보호 모드 도스 프로그램이 [가상 8086 모드](https://ko.wikipedia.org/wiki/가상_8086_모드 "wikilink") 작업 안에서 이미 실행되고 있는 도스에서 프로그램이 시작했을 때에만 실행을 허용했다. (이것은 보통 프로세서를 위한 *가상 모드 제어 프로그램*로서의 [메모리 관리자](https://ko.wikipedia.org/wiki/메모리_관리자 "wikilink") 운영을 통해 이루어졌다.) 가상 8086 모드는 프로그램과 하드웨어를 떨어트려 놓기 때문에, 프로그램이 제어 프로그램으로부터의 몇 가지 지원 없이 보호 모드로 전환하도록 만들 수 없다.

1980년대 말에 규격 확장 버전 **XVCPI**가 이러한 문제 가운데 일부를 서술하였으며, [인터렉티브 유닉스와](https://ko.wikipedia.org/wiki/인터렉티브_유닉스 "wikilink") [디지털 리서치](../Page/디지털_리서치.md "wikilink") 운영 체제를 포함한 수많은 제품에 쓰였다.

## 외부 링크

  - [*가상 제어 프로그램 인터페이스* 버전 1.0](http://docs.ruudkoot.nl/vcpi.doc)
  - [DPMI 규격 버전 0.9](https://web.archive.org/web/20080915135044/http://clio.rice.edu/cwsdpmi/dpmispec.txt) (C.W.Sandman 제공)
  - [DPMI 규격 버전 1.0](https://web.archive.org/web/20080705112555/http://clio.rice.edu/cwsdpmi/dpmispec1.pdf) (C.W.Sandman 제공)
  - [DPMI 규격](http://www.delorie.com/djgpp/doc/dpmi/) (Delorie software 제공)
  - [DPMI 규격](https://web.archive.org/web/20160521221856/http://www.tenberry.com/dpmi/index.html) (Tenberry 제공)
  - [CWSDPMI 내려받기](https://web.archive.org/web/20080921112746/http://clio.rice.edu/cwsdpmi/)
  - [HX DOS 확장자](http://www.japheth.de/HX.htm) (HDMPI 포함, HXRT.ZIP 꾸러미)
  - [DPMIONE 문서 파일](http://www.sudleyplace.com/dpmione/)

[분류:도스 기술](https://ko.wikipedia.org/wiki/분류:도스_기술 "wikilink") [분류:도스 확장자](https://ko.wikipedia.org/wiki/분류:도스_확장자 "wikilink")