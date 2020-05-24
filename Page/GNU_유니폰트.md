> This article is converted from Wikipedia: [GNU 유니폰트](https://ko.wikipedia.org/wiki/GNU_유니폰트).


[오른쪽](https://ko.wikipedia.org/wiki/파일:GNUUnifontDemonstration.png "wikilink") 로만 치보라(Roman Czyborra)\[1\]가 디자인한 GNU 유니폰트(GNU Unifont)는 중간 비트맵 글꼴 형식을 사용하여 전체 [유니코드](../Page/유니코드.md "wikilink") BMP ( Basic Multilingual Plane)을 다루는 무료 [비트맵](https://ko.wikipedia.org/wiki/비트맵 "wikilink") 글꼴이다.

[Linux](https://ko.wikipedia.org/wiki/Linux "wikilink") , [XFree86](../Page/XFree86.md "wikilink") 또는 X.org Server 와 같은 대부분의 공개 무료 운영 체제 및 윈도우 시스템 및 RockBox 와 같은 일부 내장 [펌웨어](../Page/펌웨어.md "wikilink")에 있다. 글꼴은 [GNU](../Page/GNU.md "wikilink") [GPL](https://ko.wikipedia.org/wiki/GPL "wikilink")(General Public License) 버전 2+에서 글꼴 포함 예외 (문서에 글꼴 포함시 동일한 라이센스하에 문서를 배치할 필요가 없음)와 함께 릴리스된다.

2013년 10월에 [GNU](../Page/GNU.md "wikilink") 패키지가 되었다.

## .hex 글꼴 형식

GNU 유니폰트(GNU Unifont) .hex 형식은 폭이 8 또는 16 픽셀, 높이가 16 픽셀인 [글리프를](../Page/자체.md "wikilink") 정의한다. 대부분의 서구권 스크립트 글리프는 8 픽셀 너비로 정의 할 수 있지만 다른 글리프 (특히 중국어 - 일본어 - 한국어 또는 [CJK](../Page/CJK.md "wikilink") 세트라고 잘 알려진)는 일반적으로 16 픽셀 너비로 정의된다.

GNU 유니폰트 파일(unifont.hex)에는 각 글리프에 대해 한 줄씩 표시된다. 각 행은 4 자리의 유니 코드 16 진수 코드 포인트, 콜론 및 [비트맵](https://ko.wikipedia.org/wiki/비트맵 "wikilink") 문자열로 구성된다. 비트 문자열은 8 픽셀 폭 글리프의 32 자리 16 진수 또는 16 픽셀 폭 글리프의 64 자리 16 진수이다.

비트 열의 '1'비트는 'on'픽셀에 해당한다. 픽셀 비트는 왼쪽에서 오른쪽으로 위에서 아래로 저장된다.

글꼴은 [X11](../Page/X_윈도_시스템.md "wikilink") 에서 사용하기 위해 BDF 파일로 변환된다.

## 예

[ASCII](https://ko.wikipedia.org/wiki/ASCII "wikilink") 대문자 'A'에 대해 하나의 글리프가 포함 된 예제 글꼴

    <nowiki>
    0041:0000000018242442427E424242420000
    </nowiki>

첫 번째 숫자는 0000에서 FFFF 범위의 16 진수 유니코드 코드포인트이다. [16진수](https://ko.wikipedia.org/wiki/16진수 "wikilink")(Hexadecimal) 0041은 문자 'A'의 코드 포인트인 [10진수](https://ko.wikipedia.org/wiki/10진수 "wikilink") 65이다. 콜론은 코드 포인트와 [비트맵](https://ko.wikipedia.org/wiki/비트맵 "wikilink")을 구분하는 역할을 한다. 이 예에서 글리프는 8 픽셀 너비이므로 비트 문자열은 32 자리의 16 진수이다.

비트 문자열은 8 개의 0으로 시작하므로 상위 4 개 행은 비어 있다 (8 비트, 바이트 당 2 개의 16 진수, 8 픽셀 전체 글리프의 경우 행 당 8 비트). 비트 문자열도 4 개의 0으로 끝나기 때문에 하단 2 개의 행은 비어있게된다. 기본 글꼴 디센더가 기준선보다 2 줄 아래에 있고 높이가 기준선보다 10 행 높다는 것은 암묵적인 사실이다. 이것은 라틴 글리프가있는 GNU 유니폰트의 경우이다.

hexdraw [Perl](https://ko.wikipedia.org/wiki/Perl "wikilink") 스크립트는 위의 한 줄 문자 모양 정의에서 다음 출력을 생성한다 (더 나은 시각화를 위해 같은 출력으로 오른쪽에 배치)

`0041:`
`   ––––––––`
`   ––––––––`
`   ––––––––`
`   ––––––––`
`   –––##–––`
`   ––#––#––`
`   ––#––#––`
`   –#––––#–`
`   –#––––#–`
`   –######–`
`   –#––––#–`
`   –#––––#–`
`   –#––––#–`
`   –#––––#–`
`   ––––––––`
`   ––––––––`

`0041:`
`   – – – – – – – –`
`   – – – – – – – –`
`   – – – – – – – –`
`   – – – – – – – –`
`   – – – # # – – –`
`   – – # – – # – –`
`   – – # – – # – –`
`   – # – – – – # –`
`   – # – – – – # –`
`   – # # # # # # –`
`   – # – – – – # –`
`   – # – – – – # –`
`   – # – – – – # –`
`   – # – – – – # –`
`   – – – – – – – –`
`   – – – – – – – –`

텍스트 편집기에서 편집 한 다음 동일한 유틸리티를 사용하여 16 진수 문자열로 다시 변환 할 수 있다. 목표는 새로운 글립 문자를 쉽게 추가 할 수있는 중간 형식을 만드는 것이었다.

## 역사

로만 치보라(Roman Czyborra)는 1994 년에 초기의 노력 끝에 1998 년에 유니폰트(Unifont) 포맷을 만들었다.\[2\]

2008 년 Luis Alejandro González Miranda는이 글꼴을 TrueType 글꼴로 변환하는 프로그램을 작성했다. Paul Hardy는 나중에 [트루타입](../Page/트루타입.md "wikilink")(TrueType) 버전의 문자 조합을 지원하도록 수정했다.

마지막으로 [리차드 스톨만Richard](https://ko.wikipedia.org/wiki/리차드_스톨만 "wikilink") Stallman 은 2013년 10월 유니폰트(Unifont)라는 GNU 패키지를 폴 하디(Paul Hardy)의 메인 테이너로 지칭했다.

## 벡터화 프로젝트

루이스 알레한드로 곤살레스 미란다(Luis Alejandro González Miranda)는 [폰트포지](../Page/폰트포지.md "wikilink")(FontForge)를 사용하여 [글리프 비트 맵 분포 형식의](../Page/BDF_\(파일_포맷\).md "wikilink") 유니폰트(unifont.bdf)글꼴을 벡터화하고 트루 타입 형식으로 변환하는 스크립트를 작성했다.\[3\] 폴 하디 (Paul Hardy)는 최신 트루 타입 버전의 문자 조합 (악센트 등)을 처리하기 위해 이 스크립트를 조정했다.\[4\]

## 같이 보기

  - [BDF](../Page/BDF_\(파일_포맷\).md "wikilink")

## 각주

## 외부 링크

  - [GNU Project Archives](https://ftp.gnu.org/gnu/unifont/)
  - [Unifoundry.com GNU Unifont page](http://unifoundry.com/unifont.html)

[유니폰트](https://ko.wikipedia.org/wiki/분류:GNU_프로젝트_소프트웨어 "wikilink") [분류:1998년 도입](https://ko.wikipedia.org/wiki/분류:1998년_도입 "wikilink") [분류:유니코드](https://ko.wikipedia.org/wiki/분류:유니코드 "wikilink") [분류:디지털 타이포그래피](https://ko.wikipedia.org/wiki/분류:디지털_타이포그래피 "wikilink") [분류:글꼴](https://ko.wikipedia.org/wiki/분류:글꼴 "wikilink") [분류:유니코드 글꼴](https://ko.wikipedia.org/wiki/분류:유니코드_글꼴 "wikilink") [분류:오픈 소스 글꼴](https://ko.wikipedia.org/wiki/분류:오픈_소스_글꼴 "wikilink")

1.  <http://czyborra.com/>
2.  [Roman Czyborra's GNU Unifont page](http://czyborra.com/unifont/)
3.
4.