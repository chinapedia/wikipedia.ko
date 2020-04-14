> This article is converted from Wikipedia: [ICC 프로파일](https://ko.wikipedia.org/wiki/ICC_프로파일).


[색 관리에서](../Page/색_관리.md "wikilink") **ICC 프로파일**(ICC profile)은 색 입력 장치나 색 출력 장치의 특성을 구현하는 데이터의 집합으로 [국제 컬러 협회](../Page/국제_컬러_협회.md "wikilink")(ICC)가 공표한 표준을 따른다. 프로파일들은 특정한 장치의 색 특성을 정의하거나 [색 공간](../Page/색_공간.md "wikilink"), PCS(프로파일 연결 공간)의 매핑 정의에 필요한 요구 사항을 보여 준다. 이 PCS는 [CIELAB](https://ko.wikipedia.org/wiki/랩_색_공간 "wikilink")(L\*a\*b\*) 또는 [CIEXYZ로](https://ko.wikipedia.org/wiki/CIE_1931_색공간 "wikilink") 되어 있다. 매핑은 [보간](https://ko.wikipedia.org/wiki/보간 "wikilink")이 적용된 테이블을 사용하거나 변환을 위한 일련의 변수를 통해 지정할 수 있다.

색을 사용하거나 보여 주는 모든 장치는 저마다 프로파일을 가지고 있다. 일부 제조업체들은 자사 제품에 맞는 프로파일을 제공하며 최종 사용자가 저만의 색 프로파일을 만들 수 있게 하는 제품들도 몇몇 존재한다. ([컬러리미터](https://ko.wikipedia.org/wiki/컬러리미터 "wikilink") 사용)

ICC는 이 포맷을 정확하게 정의하지만 알고리즘이나 처리에 대한 자세한 부분까지 정의하지는 않는다. 다시 말해 ICC 프로파일과 호환되는 응용 프로그램과 시스템 사이에 차이가 있을 수 있다. 특히 버전에 따른 호환성 문제가 크게 대두 되는데, 높은 버전의 프로파일을 지원하지 않을 경우에 이미지가 깨져서 출력될 수 있다.\[1\] 현재의 규격은 4.2이다.\[2\]

## 색교정에 대한 이해

색교정은 디자이너가 자신이 추구하는 방향으로 색을 조정하는 색보정과는 다른의미이다. 정확한 색보정을 하기 위해서는 정확한 색의 기준을 잡아주는 색교정 과정을 거친 후에야 비로소 실현될 수 있다.

현실적으로 이것이 어떻게 작동하는지 간략하게 살펴보면, 특정한 [RGB와](../Page/RGB_가산혼합.md "wikilink") [CMYK](https://ko.wikipedia.org/wiki/CMYK_감산혼합 "wikilink") [색 공간이](../Page/색_공간.md "wikilink") 있고 RGB에서 CMYK로 변환하려고 한다고 하자. 첫 단계는 두 개의 색상 체계가 독립적인 색상 체계를 기준으로 각각의 ICC 프로파일들을 얻는 것이다. 그리고 두 번째 단계로 RGB값이 독립된 색상 체계로 변환을 하게 되는데, 먼저 RGB 각각의 값(빨강, 녹색, 파랑)이 RGB 프로파일을 사용하여 PCS로 변환한다. PCS는 L\*a\*b\*와 CIE XYZ 등이 사용된다. 세 번째 단계는 변환된 PCS를 CMYK 프로파일을 사용하여 요구되는 C, M, Y, K 네 개의 값으로 변환하는 것이다. 이렇듯 프로파일은 특정한 색상을 물리적인 색상으로 변환할 때에 한 번, 그것을 또다시 특정한 색상으로 변환할 때에 두 번이 필요하다. 즉 파이프라인이 성립되기 위해서는 특정한 색상체계 사이를 오고갈 수 있는 교량역할의 프로파일이 두 개가 필요하다. 필요하다면 파이프라인을 여러번 반복할 수 있다.

색상 프로파일이 필요한 가장 큰 이유는 전혀 다른 색상 체계, 또는 같은 색상 체계라도 전혀 다른 장비에 의해서 표현될 때에 어떻게 하면 정확한 물리적 색상을 재현할 수 있는가이다. 예를 들면 두 개의 디스플레이에서 같은 값의 RGB 정보를 나타낸다고 하더라도, 그 디스플레이가 속한 방의 밝기와 조명의 색상 등 환경적인 변수에 따라서 실제 눈으로 들어오는 물리적인 색상은 달라질 수 있다. 또한 같은 RGB 색상 체계의 센서를 사용하는 카메라라도, 그 기종이나 촬영 조건에 따라 입력되는 RGB 색상은 현저히 달라질 수 있다. 특히 디스플레이와 프린터 같은 전혀 다른 방식의 색 체계, 표현방식에서는 더더욱 물리적인 색상이 달라지는데, 이것들은 물리적인 변수에 따른 실제 물리색상이 달라지는 연유와 전혀 다른 색 체계 상의 변환 문제 등이 함께 거론되는 부분이다.

이러한 이유등으로 각각의 색상 체계나 장비에 따른 색상에 차이를 기술하고 교정해주는 역할이 필요한데, 그것이 프로파일의 존재 이유이다. 그러기 위해서는 L\*a\*b\*나 CIE XYZ 같은 프로파일이 필요 없는 실제의 물리적인 색상을 기술하기 위한 색 체계가 필요하다. 프로파일을 만들고 변환하기 위해서는 이러한 물리적 색 체계를 기준으로 작동하는데, 디스플레이에 경우 암실에서 L\*a\*b\*나 CIE XYZ 같은 물리색상 체계를 기술할 수 있는 센서장비를 이용하여 디스플레이에 표현되고 있는 값과 실제 물리 색상을 비교해서, 그 교정값을 프로파일로 작성한다. 이렇게 만들어진 RGB 프로파일은 운영 체제에서 표현하고자 하는 본래의 RGB 값을 다시 L\*a\*b\*나 CIE XYZ 같은 물리 색상 체계에서의 값으로 변환하고, 그 값을 다시 RGB 값으로 가지고 와서 디스플레이에 표현할 때에 사용된다. 또한 어도비 같은 그래픽 소프트웨어에서도 내부적으로 사용되는데, 일례로 포토샵에서 불러오는 문서는 각기 할당(assign)된 프로파일이 있으며, 그것을 적용하기 이전에 사용자가 미리 설정해 둔 작업(working)프로파일 설정과 비교를 한 뒤에 사용한다.

그래픽 소스의 경우 프로파일이 없을 경우 매우 치명적인데, 도큐멘트가 RGB 값만을 가지고 있을 때에 그것을 디스플레이에 표현하거나 편집할 경우, 그래픽카드에서 렌더링 하지 못 할 수도 있다. 실제로 운영체제에서는 프로파일이 없을 경우 강제로 프로파일을 할당하기도 하며, 맥 오에스 텐의 경우 시스템에 필요한 sRGB 같은 기본 프로파일을 시스템 라이브러리에서 강제로 삭제하면은 로그인에 필요한 그래픽 소스가 아예 표시되지 않을 수도 있다. 이렇듯이 단순히 RGB 값이나, CMYK 값만을 가지고는 아무런 의미가 없으며, 색상 값과 함께 그에 맞는 프로파일을 가지고 있을 때에만 비로소 정확한 색을 재현해낼 수 있다.

프로파일은 [렌더링 인텐트에](https://ko.wikipedia.org/wiki/렌더링_인텐트 "wikilink") 따라 몇 가지 매핑을 정의할 수도 있다. 이러한 매핑들은 가장 잘 맞는 색의 매핑을 선택할 수 있게 허용하며 다른 [색역](../Page/색역.md "wikilink")을 허용하는 전반적인 색 범위를 다시 매핑한다.

## 표준 참조

현재 국제 표준 ISO 15076-1:2005로 진행 중인 ICC 프로파일 규격\[3\]\[4\]은 다른 표준들에 널리 참조되고 있다. 아래의 국제 표준들과 [de facto 표준들은](https://ko.wikipedia.org/wiki/de_facto "wikilink") ICC 프로파일에 대해 참조하고 있다.

### 국제 표준

<small>

  - ISO/IEC 10918-1: 정적 사진의 부호화 - [JPEG](../Page/JPEG.md "wikilink")
  - ISO 12234-4: 사진 - 전자적 정적 사진 이미징 – Part 4: Exchangeable image file format ([Exif](https://ko.wikipedia.org/wiki/Exif "wikilink") 2.2) (ISO TC42)
  - ISO 12639:2004 그래픽 기술 — 디지털 데이터 교환 추진 — Tag image file format for image technology ([TIFF](https://ko.wikipedia.org/wiki/TIFF "wikilink")/IT) (ISO TC130)
  - ISO/DIS 12647-1: 그래픽 기술 - 반색조(하프톤) 색 분리, 시험 인화, 생산용 인쇄물의 생산 처리 제어 – part 1: Parameters and measurement methods (Revision under way in ISO TC130)
  - ISO/DIS 12647-2: 그래픽 기술 – 반색조(하프톤) 색 분리, 시험 인화, 생산용 인쇄물의 생산 처리 제어 – part 2: Offset processes (Revision under way in ISO TC130)
  - ISO/CD 12647-3: 그래픽 기술 - 반색조(하프톤) 색 분리, 시험 인화, 생산용 인쇄물의 생산 처리 제어 - Part 3: Coldset offset lithography on newsprint
  - ISO/CD 12647-3: 그래픽 기술 — 반색조(하프톤) 색 분리, 시험 인화, 생산용 인쇄물의 생산 처리 제어 — Part 4: Publication gravure printing
  - ISO/CD 12647-6: 그래픽 기술 – 반색조(하프톤) 색 분리, 시험 인화, 생산용 인쇄물의 생산 처리 제어 – Part 6: Flexographic printing
  - ISO/IEC 15948: [PNG](../Page/PNG.md "wikilink") 파일 포맷 (W3C와 함께 정의됨 – [이 곳](https://web.archive.org/web/20080925122412/http://www.libpng.org/pub/png/spec/iso/) 참고)
  - ISO/IEC15444: 정적 사진의 부호화 - [JPEG2000](https://ko.wikipedia.org/wiki/JPEG2000 "wikilink") (ISO JTC 1/SC 2)
  - ISO 15930-1:2001 그래픽 기술 — 디지털 데이터 교환 추진: PDF 사용 - Part 1: Complete exchange using CMYK data ([PDF](../Page/PDF.md "wikilink")/X-1 and PDF/X-1a) (ISO TC130)
  - ISO 15930-3:2002 그래픽 기술 — 디지털 데이터 교환 추진: PDF 사용 - Part 3: Complete exchange suitable for color managed workflows (PDF/X-3) (ISO TC130)
  - ISO 15930-4:2003 그래픽 기술 - 디지털 데이터 교환 추진: PDF 사용 - Part 4: Complete exchange of CMYK and spot color printing data using PDF 1.4 (PDF/X-1a)
  - ISO 15930-5:2003 그래픽 기술 - 디지털 데이터 교환 추진: PDF 사용 - Part 5: Partial exchange of printing data using PDF 1.4 (PDF/X-2)
  - ISO 15930-6:2003 그래픽 기술 - 디지털 데이터 교환 추진: PDF 사용 - Part 6: PDF 1.4 (PDF/X-3)를 사용한 색 관리 워크플로에 맞는 인쇄 데이터 교환 완성
  - ISO 22028-1:2004 사진 및 그래픽 기술 – 디지털 이미지 저장, 조작, 교환의 확장된 색 인코딩 – Part 1: Architecture and requirements (ISO TC42)
  - ISO 12052 / NEMA PS3 [의료용 디지털 영상 및 통신 표준](../Page/의료용_디지털_영상_및_통신_표준.md "wikilink") ([DICOM](https://ko.wikipedia.org/wiki/DICOM "wikilink"))

</small>

### 사실 상의 표준

  - [PICT](https://ko.wikipedia.org/wiki/PICT "wikilink") 표준 규격 (애플이 출시한 파일 포맷)
  - [포스트스크립트](../Page/포스트스크립트.md "wikilink") 언어 (애플이 출시한 EPS 파일 포맷)
  - [PDF](../Page/PDF.md "wikilink") 포터블 도큐먼트 포맷 (애플이 출시한 EPS 파일 포맷)
  - [JDF](https://ko.wikipedia.org/wiki/JDF "wikilink") v1.1 개정 A (CIP4 컨소시엄이 출판한 JDF [참고](http://www.cip4.org))
  - [SVG](https://ko.wikipedia.org/wiki/SVG "wikilink") 버전 1.1 (W3C가 정의한 파일 포맷 [참고](https://web.archive.org/web/20080923061609/http://www.w3.org/TR/SVG/))
  - [CSS3](https://ko.wikipedia.org/wiki/CSS3 "wikilink") (W3C가 정의한 파일 포맷 [참고](http://www.w3.org/Style/CSS/current-work))

## 각주

<references />

## 외부 링크

  - [ICC 프로파일 규격](https://web.archive.org/web/20080516025645/http://www.color.org/icc_specs2.html)
  - [어도비 포토샵의 ICC 프로파일](https://web.archive.org/web/20090220094202/http://kb.adobe.com/selfservice/viewContent.do?externalId=321382&sliceId=1)

[분류:색 공간](https://ko.wikipedia.org/wiki/분류:색_공간 "wikilink")

1.
2.
3.
4.  ISO 15076-1:2005. [Image technology colour management–Architecture, profile format and data structure–Part 1: Based on ICC.1:2004-10](http://www.iso.org/iso/iso_catalogue/catalogue_tc/catalogue_detail.htm?csnumber=40317)