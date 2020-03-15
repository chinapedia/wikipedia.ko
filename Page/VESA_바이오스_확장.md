> This article is converted from Wikipedia: [VESA  ](https://ko.wikipedia.org/wiki/VESA__).


**VESA 확장 BIOS**는 높은 해상도 및 많은 색상을 표현할 때 호환 비디오 보드에 접근하는 소프트웨어에서 사용 가능한 인터페이스인 [VESA](https://ko.wikipedia.org/wiki/VESA "wikilink") 표준이다. 최신 버전은 3이다. 이것은 640\*480(4bit) 또는 이 이하의 그래픽을 제공하는 바이오스 기능 호출 int 10h와 반대이다.VBE는 비디오 어댑터를 통해 시스템 시작시 [바이오스](https://ko.wikipedia.org/wiki/바이오스 "wikilink")를 가리키는 인터럽트를 설치 하게 한다. 하지만, 오래된 VBE는 [윈도 95와](https://ko.wikipedia.org/wiki/윈도_95 "wikilink") [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink") 같은 [보호 모드](../Page/보호_모드.md "wikilink") [운영체제](https://ko.wikipedia.org/wiki/운영체제 "wikilink")에서 성능이 저하되는 [실제 모드](https://ko.wikipedia.org/wiki/실제_모드 "wikilink") 인터페이스의 VBE만 제공한다. 이것은 VESA 바이오스 확장은 비디오 드라이버를 사용하는데 거의 사용되지 않았다는 것을 의미한다. 또한, 각각의 비디오 카드 제작사들은 비디오 카드와 통신하기위한 [독점 프로토콜을](https://ko.wikipedia.org/wiki/독점_프로토콜 "wikilink") 만들었다. 그럼에도 불구하고, 이 [비디오 카드를](https://ko.wikipedia.org/wiki/비디오_카드 "wikilink") 위한 많은 기존의 드라이버가 사용하지 않으면 카드와 카드 사이에서 수백의 포트가 필요해서 화면 모드를 초기화하기 위해 리얼 모드 인터럽트를 호출하고 카드 선형 [프레임 버퍼에](https://ko.wikipedia.org/wiki/프레임_버퍼 "wikilink") 직접 액세스할 [인터럽트](../Page/인터럽트.md "wikilink")로 사용되었다. 새로운 [그래픽 카드](../Page/그래픽_카드.md "wikilink") 대부분은 더 뛰어난 VBE 3.0 표준을 구현한다.

## VESA에 의해 규정된 모드

| 그래픽 모드         | 320x200     | 640x400     | 640x480     | 800x600                | 1024x768    | 1280x1024   |
| -------------- | ----------- | ----------- | ----------- | ---------------------- | ----------- | ----------- |
| 16 색 팔레트       |             |             |             | 258 (0102h), 106 (6Ah) | 260 (0104h) | 262 (0106h) |
| 256 색 팔레트      |             | 256 (0100h) | 257 (0101h) | 259 (0103h)            | 261 (0105h) | 263 (0107h) |
| 15-bit (5:5:5) | 269 (010Dh) |             | 272 (0110h) | 275 (0113h)            | 278 (0116h) | 281 (0119h) |
| 16-bit (5:6:5) | 270 (010Eh) |             | 273 (0111h) | 276 (0114h)            | 279 (0117h) | 282 (011Ah) |
| 24-bit (8:8:8) | 271 (010Fh) |             | 274 (0112h) | 277 (0115h)            | 280 (0118h) | 283 (011Bh) |
|                |             |             |             |                        |             |             |

| 텍스트 모드 | 열    |
| ------ | ---- |
| 줄      | 80   |
| 25     |      |
| 43     |      |
| 50     |      |
| 60     | 108h |
|        |      |

## 참고

  - [VESA BIOS 확장 1.2](https://web.archive.org/web/20090114055246/http://docs.ruudkoot.nl/vesasp12.txt)
  - [VESA BIOS 확장 2.0](https://web.archive.org/web/20081211174813/http://docs.ruudkoot.nl/vbe20.txt)
  - [VESA BIOS 확장 3.0](http://www.petesqbsite.com/sections/tutorials/tuts/vbe3.pdf)

## 추가 링크

  - [Dr. Dobb's Examining the VESA VBE 2.0 Specification](http://www.ddj.com/architect/184409592)

  - [Scitech Software](https://web.archive.org/web/20090207093803/http://scitechsoft.com/){{ Creators of the useful [UniVBE](https://ko.wikipedia.org/wiki/UniVBE "wikilink") and [Scitech Display Doctor](https://web.archive.org/web/20080725050445/http://www.scitechsoft.com/sdd_win.html){{ VESA VBE enhancement software. Made freely available in recent years.

  - [SuperVGA/VESA programmer's notes](http://www.faqs.org/faqs/pc-hardware-faq/supervga-programming/)

  - [List of VESA VBE 2.0/3.0 implementing chipsets](https://web.archive.org/web/20090112210259/http://www.xerxys.info/index.php?title=VESA)

  - [Capture VBE mode info vbespy source package](https://web.archive.org/web/20110722052548/http://www.phoronix.net/downloads/vbespy.tar.bz2)

  - [How to use vbespy source package](http://www.phoronix.com/scan.php?page=article&item=803&num=1)

  - [vbetool](http://www.codon.org.uk/~mjg59/vbetool/) - an application for executing video card BIOS code

  -
  -
[분류:바이오스](https://ko.wikipedia.org/wiki/분류:바이오스 "wikilink") [바이오스](https://ko.wikipedia.org/wiki/분류:VESA "wikilink")