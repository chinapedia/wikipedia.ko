> This article is converted from Wikipedia: [ECos](https://ko.wikipedia.org/wiki/ECos).


[thumb](https://ko.wikipedia.org/wiki/파일:ECos_logo.png "wikilink")

**eCos**(Embedded Configurable Operating System)는 [자유-오픈 소스](../Page/자유-오픈_소스_소프트웨어.md "wikilink") [실시간 운영 체제의](../Page/실시간_운영_체제.md "wikilink") 하나로, 오직 하나의 [프로세스](../Page/프로세스.md "wikilink")에 [다중 스레드만](https://ko.wikipedia.org/wiki/스레드 "wikilink") 필요한 [임베디드 시스템과](../Page/임베디드_시스템.md "wikilink") 애플리케이션을 위해 고안되었다. 런타임 성능과 하드웨어 요구에 대한 애플리케이션 요건을 세밀히 조정할 수 있도록 설계되었다. [C](../Page/C_\(프로그래밍_언어\).md "wikilink")/[C++](https://ko.wikipedia.org/wiki/C++ "wikilink")로 구현되어 있으며 [POSIX](../Page/POSIX.md "wikilink")와 [µITRON용](https://ko.wikipedia.org/wiki/ITRON_프로젝트 "wikilink") [호환성 계층과](https://ko.wikipedia.org/wiki/호환성_계층 "wikilink") [API](../Page/API.md "wikilink")로 구현되어 있다. eCos는 [WolfSSL](../Page/WolfSSL.md "wikilink") 등의 유명한 [SSL/TLS](../Page/전송_계층_보안.md "wikilink") 라이브러리들을 통해 지원되므로 임베디드 보안의 모든 표준을 충족한다.\[1\]

## 설계

eCos는 수10\~수100 [킬로바이트](../Page/킬로바이트.md "wikilink")의 메모리 규모를 갖춘 장치용으로,\[2\] 또는 실시간 요건이 필요한 응용 프로그램을 위해 설계되었다.

eCos는 다양한 하드웨어 플랫폼에서 실행되는데, 여기에는 [ARM](../Page/ARM_아키텍처.md "wikilink"), [CalmRISC](https://ko.wikipedia.org/wiki/CalmRISC "wikilink"), [FR-V](https://ko.wikipedia.org/wiki/FR-V "wikilink"), [히타치 H8](https://ko.wikipedia.org/wiki/히타치_H8 "wikilink"), [IA-32](../Page/IA-32.md "wikilink"), [모토로라 68000](../Page/모토로라_68000.md "wikilink"), [마츠시타 AM3x](https://ko.wikipedia.org/wiki/마츠시타_AM3x "wikilink"), [MIPS](https://ko.wikipedia.org/wiki/MIPS_아키텍처 "wikilink"), [NEC V8xx](https://ko.wikipedia.org/wiki/NEC_V8xx "wikilink"), [Nios II](https://ko.wikipedia.org/wiki/Nios_II "wikilink"), [파워PC](../Page/파워PC.md "wikilink"), [SPARC](../Page/SPARC.md "wikilink"), [슈퍼H](https://ko.wikipedia.org/wiki/슈퍼H "wikilink")가 포함된다.

eCos 배포판으로는 [임베디드 시스템을](../Page/임베디드_시스템.md "wikilink") 위해 [부트스트랩](../Page/부팅.md "wikilink") [펌웨어](../Page/펌웨어.md "wikilink")를 제공하기 위해 eCos [하드웨어 추상화를](https://ko.wikipedia.org/wiki/하드웨어_추상화 "wikilink") 사용하는 [오픈 소스](../Page/오픈_소스_소프트웨어.md "wikilink") [애플리케이션인](../Page/응용_소프트웨어.md "wikilink") [레드부트](https://ko.wikipedia.org/wiki/레드부트 "wikilink")(RedBoot)가 있다.

## 역사

eCos는 1997년 처음 개발되었으며\[3\] 개발사는 [레드햇](../Page/레드햇.md "wikilink")에 의해 인수된 [시그너스 솔루션이다](https://ko.wikipedia.org/wiki/시그너스_솔루션 "wikilink"). 2002년 초에 레드햇은 eCos의 개발을 중단하였고 프로젝트의 직원을 해고하였다.\[4\] 해고된 직원 중 다수는 eCos의 작업을 계속해나갔고 일부는 소프트웨어의 서비스들을 제공하는 자신들만의 기업을 설립하였다. 2004년 1월, eCos 개발자들의 요청에 따라 레드햇은 eCos의 저작권을 [자유 소프트웨어 재단에](../Page/자유_소프트웨어_재단.md "wikilink") 2005년 10월 인계할 것에 동의했으며\[5\] 2008년 5월 해당 프로세스는 완료되었다.

## 각주

## 외부 링크

  - [eCos Homepage](http://ecos.sourceware.org/)
  - ["eCos Porting Guide"](https://web.archive.org/web/20020611012907/http://www.embedded.com/story/OEG20011220S0059) article by Anthony J. Massa 2001-12-28
  - ["Embedded Software Development with eCos"](http://www.informit.com/content/images/0130354732/downloads/0130354732.pdf) book by Anthony J. Massa 2002-11-25,
  - [eCosCentric web site](http://www.ecoscentric.com/ecos/ecospro.shtml)

[분류:ARM 운영 체제](https://ko.wikipedia.org/wiki/분류:ARM_운영_체제 "wikilink") [분류:임베디드 운영 체제](https://ko.wikipedia.org/wiki/분류:임베디드_운영_체제 "wikilink") [분류:자유 소프트웨어 운영 체제](https://ko.wikipedia.org/wiki/분류:자유_소프트웨어_운영_체제 "wikilink") [분류:MIPS 운영 체제](https://ko.wikipedia.org/wiki/분류:MIPS_운영_체제 "wikilink") [분류:실시간 운영 체제](https://ko.wikipedia.org/wiki/분류:실시간_운영_체제 "wikilink")

1.
2.
3.
4.
5.