> This article is converted from Wikipedia: [OCR-A](https://ko.wikipedia.org/wiki/OCR-A).


[오른쪽](https://ko.wikipedia.org/wiki/파일:OCR-A_SP.svg "wikilink") **OCR-A**는 1968년 컴퓨터 광학 문자 인식의 초기에 등장한 [글꼴로](https://ko.wikipedia.org/wiki/컴퓨터_글꼴 "wikilink"), 최초로 컴퓨터뿐만 아니라 동시에 사람도 인식 할 수있는 글꼴이 필요할 때 사용되었었다. \[1\]

OCR-A는 간단하고 두터운 획을 사용하여 인식 가능한 문자를 제공했다.\[2\]

예를 들어, OCR-A의 글자는 \(0.254cm\) 의 공간을 확보하고, \(0.2286cm\)의 공백을 인쇄시 기술적으로 허용하는 프린터의 경우, \(0.4572cm(0.2286cm \times 0.2286cm)\) 의 간격에서 글꼴이 고정 폭이다.

## 표준

OCR-A 글꼴은 [ANSI](https://ko.wikipedia.org/wiki/ANSI "wikilink")( American National Standards Institute )에서 ANSI X3.17-1981로 표준화했다. X3.4이후 INCITS(International Committee for Information Technology Standards)가 작업했으며, OCR-A 표준은 현재 ISO 1073-1 : 1976 이라고 불린다. OCR-A의 DIN 66008이라는 독일 표준도 있다.\[3\]

## 구현

[섬네일](https://ko.wikipedia.org/wiki/파일:Matt-OCR-A-B.png "wikilink") 1968년 ATF(American Type Founders)는 미국 표준 국(US Bureau of Standards)에서 정한 기준을 충족하는 최초의 광학 문자 인식 글꼴 중 하나 인 OCR-A를 제작했다. 디자인은 간단하여 기계로 쉽게 읽을 수 있지만 육안으로 읽기는 더 어려워졌다.\[4\]

금속 유형의 인쇄에서 컴퓨터 기반의 출력 조판 방식으로 바뀜에 따라 Tor Lillqvist는 메타폰트(MetaFont)를 사용하여 OCR-A 글꼴을 고안했다. 그 정의는 리처드 B. 웨일즈(Richard B. Wales)에 의해 이후에 개선되었다. 그들의 작업은 [CTAN](https://ko.wikipedia.org/wiki/CTAN "wikilink") 에서 확인 가능하다.\[5\]

무료 버전의 글꼴을 사용자가 쉽게 이용할 수 있도록하기 위해 존 사우터(John Sauter)는 2004 년 [포트레이스](https://ko.wikipedia.org/wiki/포트레이스 "wikilink")(potrace) 및 [폰트포지](../Page/폰트포지.md "wikilink")(FontForge) 를 사용하여 MetaFont 정의를 [윈도우상에서](https://ko.wikipedia.org/wiki/마이크로소프트_윈도우 "wikilink") 작동하는 [트루타입](https://ko.wikipedia.org/wiki/트루타입 "wikilink")(TrueType)으로 변환했다.\[6\] 2007 년 거칸 셍건(Gürkan Sengün)은 이 구현에서 [데비안](https://ko.wikipedia.org/wiki/데비안 "wikilink") 패키지를 만들어냈다.\[7\] 2008 년, 뤽 데브로이(Luc Devroye)는 존 사우터(John Sauter)의 구현에서 수직 위치를 수정하고 소문자 z에대한 작업을 완료했다.\[8\]

독립적으로 매튜 스칼라(Matthew Skala)는\[9\] mftrace\[10\] 를 사용하여 2006 년 메타폰트(Metafont) 정의를 [트루타입](https://ko.wikipedia.org/wiki/트루타입 "wikilink") 형식으로 변환했다. 2011 년에는 메타폰트(Metafont) 정의를 다시 작성하여 중간 버전 추적없이 직접 개요를 생성하는 새 버전을 릴리스했다. 2012 년 9 월 27 일에 그는 구현을 버전 0.2로 업데이트했다.\[11\]

매튜 스칼라(Matthew Skala)는 [퍼블릭도메인](https://ko.wikipedia.org/wiki/퍼블릭도메인 "wikilink")으로 OCR-A, [OCR-B](../Page/OCR-B.md "wikilink") 폰트와 소스 모두를 공개했다.\[12\]

OCR-A의 이러한 무료 구현 외에도 상용 공급 업체가 판매하는 여러 구현도 있다.

광학 문자 인식 기술이 단순한 글꼴이 더 이상 필요하지 않은 시점까지 발전했지만 OCR-A 글꼴은 계속 사용되어왔다. 그것의 사용은 세계 수표의 암호화에 널리 남아 있다. 여전히 일부 지로청구 같은 전문 회사는 청구서 양식에 주요 기재사항과 관련된 문자 및 번호와 금액에대해 철자와 숫자들을 OCR-A로 인쇄해야한다고 주장하고 있다.\[13\] 또한, 간혹 본연의 기계적인 이미지 때문에, 광고 및 디스플레이 그래픽에 사용되기도 한다.

## 유니코드

[ASCII](https://ko.wikipedia.org/wiki/ASCII "wikilink")의 현재 계열은 ISO 10646 으로도 알려진 [유니 코드이다](https://ko.wikipedia.org/wiki/유니_코드 "wikilink"). 유니 코드는 ASCII를 포함하고 있으며 OCR 문자에 대한 특수 규정이 있으므로 OCR-A의 일부 구현은 문자 코드 할당에 대한 지침으로 유니 코드를 고려해야한다.

## 같이 보기

  - [고정폭 글꼴](../Page/고정폭_글꼴.md "wikilink")
  - [OCR-B](../Page/OCR-B.md "wikilink")
  - [오픈소스 유니코드 서체](https://ko.wikipedia.org/wiki/오픈소스_유니코드_서체 "wikilink")

## 각주

## 참고

  - (CTAN)[ctan.org의 OCR-A 무료배포 메타폰트](http://www.ctan.org/tex-archive/fonts/ocr-a)
  - (Matthew Skala의 Tsukurimashou프로젝트)http://Tsukurimashou.sourceforge.jp [퍼블릭도메인](https://ko.wikipedia.org/wiki/퍼블릭도메인 "wikilink") OCR-A
  - (Matthew Skala 비공식[미러링](https://ko.wikipedia.org/wiki/미러링 "wikilink")사이트)https://github.com/opensourcedesign/fonts/tree/master/OCRA (opensourcedesign.net)

[분류:산세리프 글꼴](https://ko.wikipedia.org/wiki/분류:산세리프_글꼴 "wikilink") [분류:마이크로소프트 글꼴](https://ko.wikipedia.org/wiki/분류:마이크로소프트_글꼴 "wikilink") [분류:ISO 표준](https://ko.wikipedia.org/wiki/분류:ISO_표준 "wikilink") [분류:광학 문자 인식](https://ko.wikipedia.org/wiki/분류:광학_문자_인식 "wikilink") [분류:고정폭 글꼴](https://ko.wikipedia.org/wiki/분류:고정폭_글꼴 "wikilink") [분류:오픈 소스 글꼴](https://ko.wikipedia.org/wiki/분류:오픈_소스_글꼴 "wikilink")

1.  [Motivation for OCR-A from Microscan](http://www.microscan.com/en-us/technology/opticalcharacterrecognition.aspx)
2.
3.  [DIN 66008-1 Font A For Optical Character Recognition; Characters And Nominal Dimensions](http://infostore.saiglobal.com/store/Details.aspx?productID=668602)
4.  [Background on OCR-A from Adobe](http://www.myfonts.com/fonts/adobe/ocra/)
5.
6.  [John Sauter's 2004 OCR-A font from those MetaFont sources](http://sourceforge.net/project/showfiles.php?group_id=121297)
7.  [The fonts-ocr-a Debian package, based on John Sauter's SourceForge project](https://packages.debian.org/wheezy/fonts-ocr-a)
8.  [Luc Devroye's account of his changes to John Sauter's implementation of OCR-A](http://luc.devroye.org/fonts-48501.html)
9.  [Matthew Skala's home page](http://ansuz.sooke.bc.ca/page/about)
10. [The mftrace Debian package](http://packages.debian.org/mftrace)
11. [Matthew Skala's 2012 OCR-A font from the MetaFont sources](http://ansuz.sooke.bc.ca/page/fonts#ocra)
12. <http://tsukurimashou.osdn.jp/ocr.pdf>
13. [Description of a lockbox service, note “The bill contains an invoice and a statement with patient information contained in a scannable Optical Character Recognition (OCR) line. The OCR line is similar in appearance to that found on a credit card statement or telephone bill.”](https://www.pnc.com/content/dam/pnc-com/pdf/corporateandinstitutional/Treasury%20Management/Healthcare/078_Patient_Pay_Lockbox_3-13.pdf)