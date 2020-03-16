> This article is converted from Wikipedia: [ PDF](https://ko.wikipedia.org/wiki/_PDF).


**수마트라 PDF**(Sumatra PDF)는 무료 [오픈소스](https://ko.wikipedia.org/wiki/오픈소스 "wikilink") [전자책](../Page/전자책.md "wikilink") [뷰어로](../Page/파일_뷰어.md "wikilink") , PDF(Portable Document Format), Microsoft HTML 도움말([CHM](https://ko.wikipedia.org/wiki/CHM "wikilink")), [DjVu](https://ko.wikipedia.org/wiki/DjVu "wikilink") , [EPUB](../Page/EPUB.md "wikilink") , FictionBook (FB2), [Mobi](https://ko.wikipedia.org/wiki/Mobi "wikilink") , [PRC](https://ko.wikipedia.org/wiki/PRC_\(파일_포맷\) "wikilink") , [Open XML Paper](https://ko.wikipedia.org/wiki/Open_XML_Paper "wikilink") 등 다양한 문서 형식 포맷(OpenXPS, OXPS, XPS), 만화 아카이브 파일 (CB7, CBR, CBT, CBZ)을 지원한다.\[1\] MS[윈도우즈](https://ko.wikipedia.org/wiki/윈도우즈 "wikilink")(Microsoft Windows) 전용으로 개발되었지만 [WINE을](../Page/와인_\(소프트웨어\).md "wikilink") 사용하여 [Linux](https://ko.wikipedia.org/wiki/Linux "wikilink")에서 실행할 수 있다.

## 특징

수마트라PDF(이하, 수마트라)는 [미니멀리즘](../Page/미니멀리즘.md "wikilink") [디자인](../Page/디자인.md "wikilink")을 가지고 있으며, 심플함은 광범위한 기능을 희생시키면서 얻을 수 있다. PDF 렌더링을 위해 MuPDF 라이브러리를 사용한다.\[2\] 수마트라는 외장형 의존성이없는 하나의 파일로 구성되어 있으므로 외장형 [USB](../Page/USB.md "wikilink") 드라이브에서 사용할 수있어 설치가 필요하지않는 휴대형으로 설계되었다.\[3\] PDF, XPS, DjVu, CHM, 전자 책 ([ePub](../Page/EPUB.md "wikilink") 및 [Mobi](https://ko.wikipedia.org/wiki/Mobi "wikilink")) 및 만화 (CBZ 및 CBR) 형식을 읽을 수있는 광범위한 이식 가능한 응용 프로그램으로 분류된다.\[4\]

수마트라는 많은 휴대용 응용 프로그램의 특성상 거의 디스크 공간을 사용하지 않다.\[5\] 2009년 Sumatra 1.0은 [어도비 애크러뱃 리더(Reader)](../Page/어도비_애크러뱃.md "wikilink") 9.5의 32MB에 비해 1.21MB의 설치 파일을 가지고있었다.\[6\]\[7\] 2017 년 1 월, 실제 버전 수마트라PDF(SumatraPDF) 3.1.2에는 하나의 6.1 Mb 실행 파일이었다. 한편, 어도비리더(Adobe Reader) XI는 320MB의 디스크 공간을 사용한다.\[8\]

수마트라 0.6에서는 PDF 형식의 사용 제한이 구현되어\[9\] 사용자가 문서 작성자가 제한하는 문서에서 인쇄하거나 복사 할 수 없게하는 형식인 [디지털 권리 관리](../Page/디지털_권리_관리.md "wikilink")(Digital Rights Management,DRM)형식이 사용되었다. 크쥐시토프 코월직(Kowalczyk)은 "나는 수마트라가 PDF 제작자들의 희망을 존중할 것이라고 결정했다. [아큘러](../Page/아큘러.md "wikilink")(Okular) 와 [에빈스](../Page/에빈스.md "wikilink")(Evince) 와 같은 다른 오픈소스 개발자들은 이 옵션을 선택하게되며,\[10\]\[11\]\[12\]그러나, [데비안](../Page/데비안.md "wikilink")은 상호 호환성과 재사용이라는 오픈소스 원칙에 따라 이러한 제한을 없애기 위해 소프트웨어를 패치한다.\[13\]

수마트라 1.1까지 각 PDF 페이지를 [비트맵](https://ko.wikipedia.org/wiki/비트맵 "wikilink") 이미지로 변환하여 인쇄가 이루어졌다. 이로 인해 매우 큰 스풀 파일이 만들어지고 인쇄 속도가 느려질 수 있다.\[14\]\[15\]

수마트라 0.9.1 이후, PDF 문서에 내장된 하이퍼 링크가 지원되었다.\[16\]

수마트라는 다국어를 지원하며 69개국의 언어에서 번역되었다.\[17\]

수마트라는 [pdfTeX](https://ko.wikipedia.org/wiki/pdfTeX "wikilink") 또는 XeTeX로 만든 [TeX](../Page/TeX.md "wikilink") 소스와 PDF 출력을 동기화하는 양방향 방식인 SyncTeX를 지원한다.\[18\]

버전 0.9.4 이후, 수마트라는 JPEG 2000 형식을 지원한다.

## 개발

수마트라의 PDF는 크쥐시토프 코월직(Krzysztof Kowalczyk)와 사이먼 번츨리(Simon Bünzli)의 두 기여자가 주로 작성한다.\[19\] 소스 코드 는 주로 C ++의 두 가지 프로그래밍 언어로 개발되었으며 C 언어의 일부 구성 요소가 포함되어 있다. 소스 코드는 Microsoft Visual Studio에 대한 지원과 함께 제공된다.\[20\]

Windows XP 가 Windows 의 최신 버전이었을 때 처음 설계 되었기 때문에 수마트라는 처음에는 이전 버전의 Windows와 호환되지 않다. Windows 95 , 98 및 Me에 대한 지원이 제거되었다.\[21\]

초기에 코월직(Kowalczyk)은 64 비트 버전의 수마트라를 공개하지 않았으므로 속도와 사용 가능한 메모리가 약간 더 많을 수도 있지만 그 당시에는 사용자의 혼란을 크게 가중시키고 잠재적 비용을 능가하지는 않을 것이라고 믿었다 .\[22\]그러나 일부 사용자는 수마트라의 64 비트 빌드를 요청했으며 다른 개발자들은 비공식 64 비트 빌드를 컴파일하여 32 비트 빌드보다 빠르게 문서를 로드했다.\[23\] 그러나 공식 빌드 개발자는 비공식 빌드가'수마트라' 이름을 사용하지 않도록 요청했다.\[24\] 2015 년 10 월 수마트라의 공식 64 비트 버전이 발표되었다.\[25\]

수마트라 소스 코드는 원래 [Google](../Page/구글.md "wikilink") 코드에서 호스팅되었다. 미국의 수출에대한 법적 규제로 인해 " 쿠바,이란, 북한, 수단, 시리아를 포함한 외국자산관리국 제재목록에있는 국가에서는 "이용할 수 없다 .\[26\]\[27\] 현재 소스 코드가 [GitHub](https://ko.wikipedia.org/wiki/GitHub "wikilink")에 호스팅되어있다.\[28\]

## 역사

버전 0.1로 지정된 수마트라 PDF의 첫 번째 버전은 Xpdf 0.2를 기반으로했으며 2006 년 6 월 1 일에 릴리스되었다. 버전 0.2에서 Poppler 로 전환되었다. 버전 0.4에서는 더 빠른 속도와 더 나은 Windows 플랫폼 지원을 위해 MuPDF 로 변경되었다.\[29\] Poppler는 한동안 대안 엔진으로 남아 있었고 버전 0.6에서 0.8까지 MuPDF가 로드하지 못한 페이지를 렌더링하는 데 자동으로 사용되었다. Poppler는 2008 년 8 월 10 일에 릴리스 된 버전 0.9에서 제거되었다.

2009 년 7 월, 수마트라 PDF는 MuPDF에서의 동일한 라이센스 변경과 일치하도록 라이센스를 GNU GPLv2 에서 GNU GPLv3 으로 변경했다.\[30\]

버전 1.0은 누적 개발 기간이 3 년 이상인 2009 년 11 월 17 일에 릴리스되었다. 버전 2.0은 2012 년 4 월 2 일에 릴리스되었다. 버전 1.0이 출시 된 후 2 년이 지났다.\[31\]

2007 년 수마트라의 PDF가 공식 다국어 지원을 받기전에 Lars Wohlfahrt\[32\] before Sumatra PDF got official multi-language support.

In October 2015, version 3.1 introduced a 64-bit version, in addition to their original 32-bit version.\[33\]\[34\]에 의해 최초의 비공식 번역본이 발표되었다.

2015 년 10 월 버전 3.1은 원래 32 비트 버전 외에도 64 비트 버전을 도입했다.\[35\]\[36\]

## 이름과 커버표지

[섬네일에](https://ko.wikipedia.org/wiki/파일:Sumatra_PDF_Logo.png "wikilink") 영감을 받은 수마트라 PDF의 초기 로고 \]\] 저자는 "수마트라"라는 이름의 선택은 [수마트라 섬이나](https://ko.wikipedia.org/wiki/수마트라_섬 "wikilink") [커피](../Page/커피.md "wikilink")에 대한 찬사가 아니며 그 이름에 특별한 추론이 없다고 지적했다.\[37\]

수마트라의 그래픽 디자인은 [앨런 무어와](../Page/앨런_무어.md "wikilink") [데이브 기번스](https://ko.wikipedia.org/wiki/데이브_기번스 "wikilink") 의 [왓치맨](../Page/왓치맨.md "wikilink") 그래픽 소설 표지에 대한 찬사([오마쥬](https://ko.wikipedia.org/wiki/오마쥬 "wikilink"))이다.\[38\]

## 중요 리셉션

수마트라는 이동성 , 키보드 단축키 및 오픈소스 개발이라는 면에서 속도와 단순성으로 인해 높은 평가를 받았다.\[39\]\[40\]\[41\]

한때 [FSF](https://ko.wikipedia.org/wiki/FSF "wikilink")유럽 재단(Free Software Foundation Europe)은 수마트라(Sumatra)PDF를 권장했지만 수마트라에 자유 라이센스가 부여된 비공개 코드가 존재하기 때문에 2014 년 2 월에 권고안을 삭제했다. 재단 대표 Heiki Ojasild는 " 그들이 비 자유 라이브러리를 계속 사용하는 동안 수마트라 PDF는 [자유 소프트웨어로](../Page/자유_소프트웨어.md "wikilink") 인정 될 수 없다 "고 설명했다.\[42\]\[43\]\[44\]\[45\] [Unrar](https://ko.wikipedia.org/wiki/Unrar "wikilink")라이브러리는 궁극적으로 3.0 버전에서부터 무료 대안으로 대체되어 100 % 무료 [오픈소스](https://ko.wikipedia.org/wiki/오픈소스 "wikilink") 소프트웨어로 만들어지게 됐다.\[46\]

## 같이 보기

  - [PDF 소프트웨어 목록](https://ko.wikipedia.org/wiki/PDF#지원_소프트웨어 "wikilink")
  - [EPUB](../Page/EPUB.md "wikilink")

## 각주

[분류:C++로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C++로_작성된_자유_소프트웨어 "wikilink") [분류:포터블 소프트웨어](https://ko.wikipedia.org/wiki/분류:포터블_소프트웨어 "wikilink") [분류:전자책](https://ko.wikipedia.org/wiki/분류:전자책 "wikilink") [분류:GPL 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:GPL_라이선스_소프트웨어 "wikilink")

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
13. [Okular, Debian, and copy restrictions](https://lwn.net/Articles/335415/)
14.
15.
16.
17.
18.
19.
20.
21.
22.
23.
24.
25.
26.
27.
28.
29.
30. [update the license to GPLv3, to match mupdf's license change](https://github.com/sumatrapdfreader/sumatrapdf/commit/04d7b0dcf8bc78c4926b1719203e861b2d11bc7b) on github.com on 3 Jul 2009
31.
32.
33.
34. [Sumatra PDF version history](http://www.sumatrapdfreader.org/news.html)
35.
36. [Sumatra PDF version history](http://www.sumatrapdfreader.org/news.html)
37.
38.
39.
40. [This Amazing PDF Reader Is Portable And Tiny](http://www.techsupportalert.com/content/amazing-pdf-reader-portable-and-tiny.htm) Submitted by Rob Schifreen on 21 July 2013
41.
42.
43.
44.
45.
46.