> This article is converted from Wikipedia: [EPUB](https://ko.wikipedia.org/wiki/EPUB).


**EPUB**(electronic publication)은 [국제 디지털 출판 포럼](https://ko.wikipedia.org/wiki/국제_디지털_출판_포럼 "wikilink")([IDPF](https://ko.wikipedia.org/wiki/IDPF "wikilink"), International Digital Publishing Forum)에서 제정한 개방형 자유 전자서적 표준이다. EPUB은 자동공간조정(reflowable)이 가능하게 끔 디자인 되었다. 이는 EPUB으로 만들어진 내용을 볼 때 디스플레이하는 기계의 형식, 크기에 자동으로 최적화되어 보여줄 수 있다는 뜻이다. EPUB는 2007년 9월 이전에 있던 오픈 eBook 표준을 대체하기 위해 국제 디지털 출판 포럼에서 공식 표준으로 채택되었다.

## 기능

  - 자유 소프트웨어 개발이 가능한 개방형 표준
  - 자동공간조정과 글자크기 변환
  - 내부에 래스터나 백터 이미지를 담을 수 있음
  - [메타데이터](../Page/메타데이터.md "wikilink") 포함
  - [DRM](https://ko.wikipedia.org/wiki/DRM "wikilink") 지원
  - [CSS](https://ko.wikipedia.org/wiki/CSS "wikilink") 지원
  - 같은 파일에 대해 대체적인 렌더링 지원
  - 기능 확장을 위한 내외부적 [XML](../Page/XML.md "wikilink")기능 지원

## 파일 형식

EPUB은 세 가지 정의로 이루어져 있다.

  - Open Publication Structure 2.0, 이는 내용의 형태를 정의한다.
  - Open Packaging Format (OPF) 2.0, 이는 XML로 구성된 .epub의 파일 구조를 정의한다.
  - OEBPS Container Format(OCF) 1.0, 모든 파일들을 ZIP으로 압축 저장한다.

기본적으로, EPUB은 내부적으로 XHTML이나 DTBook(DAISY 컨소시엄에서 만든 XML 표준.)를 이용하여 내부의 글과 문서 구조를 만들고, CSS의 일부를 이용해 문서의 틀과 형식을 만든다. 목록이나 표 양식, EPUB 메타데이터를 위해 XML을 사용한다. zip 파일을 통해 상기된 다양한 파일들을 하나로 묶어 배포한다.

### 개방형 출판 형식(Open Publication Structure) 2.0

EPUB은 내용을 구성하기위해 이전 버전에서는 XHTML에서 파생된 OEBPS 1.2를 사용했었으나 2.0버전에서는 XHTML 1.1(이나 DTBook)을 사용한다. 그러나 XHTML 구성요소(element)에 대한 제한이 좀 있다. EPUB의 XHTML에서 사용하는 mimetype은 application/xhtml+xml이다. XHTML 모듈과 제한에 대한 자세한 설명은 2.2\[1\]를 참고 하면 된다.

스타일과 레이아웃은 "OPS 스타일 시트"라 불리는 CSS 2.0의 일부를 사용한다. 이 특별한 구문들은 CSS 중 읽기시스템과 몇가지 특수한 부분만을 사용한다. 특수한 부분이란 `oeb-page-head, oeb-page-foot,`나, `oeb-column-number`등과 같은 것들이다. 폰트는 `@font-face`항목이나 OPF 메니페스트 속에 폰트를 포함시켜 설정할 수 있다. [mimetype을](https://ko.wikipedia.org/wiki/internet_media_type "wikilink") 위한 EPUB의 CSS 문서형식은 `text/css` 이다.\[2\] 지원항목과 그에 대한 세부정보는 [Section 3.0](https://web.archive.org/web/20080827131750/http://www.idpf.org/2007/ops/OPS_2.0_final_spec.html#Section3.0)에서 찾아볼 수 있다.

EPUB에서 이미지는 [PNG](../Page/PNG.md "wikilink"), [JPEG](../Page/JPEG.md "wikilink"), [GIF](../Page/GIF.md "wikilink"), [SVG](https://ko.wikipedia.org/wiki/SVG "wikilink") 형식을 지원한다. 이들은 각각 [mimetype의](https://ko.wikipedia.org/wiki/인터넷_미디어_타입 "wikilink") `image/png, image/jpeg, image/gif, image/svg+xml`를 사용한다. 다른 미디어 형식도 허용되나, 제작자가 지원 형식으로 된 대체물을 지정해 두어야 한다.\[3\] mimetypes을 위한 표는 Section 1.3.7의 세부사항\[4\]을 참고하면 된다.

국제적이며 다중언어 서적을 위해 [Unicode](https://ko.wikipedia.org/wiki/Unicode "wikilink") 가 사용되며, 제작자는 [UTF-8](../Page/UTF-8.md "wikilink") or [UTF-16](../Page/UTF-16.md "wikilink") 인코딩을 사용해야 한다. 하지만, 읽기 시스템에서 유니코드의 모든 유니코드 문자를 위한 폰트를 제공해야 하는 것은 아니지만, 표시할 수 없는 문자를 위한 표시는 해주어야 한다.\[5\]

EPUB을 위한 XHTML의 기본 골격은 아래와 같다.

``` html4strict
<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.1//EN" "http://www.w3.org/TR/xhtml11/DTD/xhtml11.dtd">
<html ns="http://www.w3.org/1999/xhtml" xml:lang="en">
  <head>
    <meta http-equiv="Content-Type" content="application/xhtml+xml; charset=utf-8" />
    <title>Pride and Prejudice</title>
    <link rel="stylesheet" href="css/main.css" type="text/css" />
  </head>
  <body>
    ...
  </body>
</html>
```

## 소프트웨어

### 읽기 지원

EPUB를 읽는 것을 지원하는 장치는 OPS 출판을 지원하는 하드웨어와 소프트웨어의 조합이다.

| 소프트웨어                                                                               | 플랫폼                                                                                                                                                               | DRM 지원                                                            | 비고                                                                            |
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| [어도비 디지털 에디션](https://ko.wikipedia.org/wiki/어도비_디지털_에디션 "wikilink")                 | [윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink"), [OS X](https://ko.wikipedia.org/wiki/OS_X "wikilink")                                                  | [어도비 콘텐트 서버](https://ko.wikipedia.org/wiki/어도비_콘텐트_서버 "wikilink") | 온라인으로 정품인증이 필요                                                                |
| [Aldiko](https://ko.wikipedia.org/wiki/Aldiko "wikilink")                           | [안드로이드](../Page/안드로이드_\(운영_체제\).md "wikilink")                                                                                                                    |                                                                   | 안드로이드 기기 EPUB 지원                                                              |
| [FBReaderJ](https://ko.wikipedia.org/wiki/FBReaderJ "wikilink")                     | 안드로이드                                                                                                                                                             |                                                                   | 오픈 소스                                                                         |
| [BookGlutton](https://ko.wikipedia.org/wiki/BookGlutton "wikilink")                 | [웹](https://ko.wikipedia.org/wiki/웹 "wikilink")                                                                                                                   |                                                                   | 자유 소프트웨어 온라인 읽기 지원                                                            |
| [Bookworm](https://ko.wikipedia.org/wiki/Bookworm_\(software\) "wikilink")          | [웹](../Page/월드_와이드_웹.md "wikilink")                                                                                                                               |                                                                   | 자유 소프트웨어 온라인 읽기 지원                                                            |
| [캘리버](../Page/캘리버.md "wikilink")(Calibre)                                           | [윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink"), [OS X](https://ko.wikipedia.org/wiki/OS_X "wikilink"), [리눅스](../Page/리눅스.md "wikilink")                |                                                                   | 도서관 관리, 변환, 전자책 연결에 주로 사용,[GPL](https://ko.wikipedia.org/wiki/GPL "wikilink") |
| [EPUBReader](https://ko.wikipedia.org/wiki/EPUBReader "wikilink")                   | Firefox add-on [윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink"), [OS X](https://ko.wikipedia.org/wiki/OS_X "wikilink"), [리눅스](../Page/리눅스.md "wikilink") |                                                                   | [파이어폭스](https://ko.wikipedia.org/wiki/파이어폭스 "wikilink") 추가 기능                 |
| [FBReader](https://ko.wikipedia.org/wiki/FBReader "wikilink")                       | 윈도, 리눅스, [PDA](https://ko.wikipedia.org/wiki/PDA "wikilink")                                                                                                      |                                                                   | 완전히 지원하지 않음                                                                   |
| [Freda](https://ko.wikipedia.org/wiki/Freda "wikilink")                             | [윈도 모바일](https://ko.wikipedia.org/wiki/윈도_모바일 "wikilink")                                                                                                         |                                                                   | DRM 없는 파일만 지원                                                                 |
| [Gitden Reader](https://ko.wikipedia.org/wiki/Gitden_Reader "wikilink")             | [안드로이드](../Page/안드로이드_\(운영_체제\).md "wikilink"), [iOS](https://ko.wikipedia.org/wiki/iOS "wikilink")                                                               | DRM 지원                                                            | EPUB 2와 EPUB 3 지원 및 Audio, Video, Reflow, Fixed-Layout, SMIL, SVG, MathML 기능  |
| [iBooks](https://ko.wikipedia.org/wiki/iBooks "wikilink")                           | [iOS](https://ko.wikipedia.org/wiki/iOS "wikilink")                                                                                                               | Apple iBooks                                                      |                                                                               |
| [i2Reader](https://ko.wikipedia.org/wiki/i2Reader "wikilink")                       | [아이폰](../Page/아이폰.md "wikilink")                                                                                                                                  |                                                                   |                                                                               |
| [Lexcycle Stanza](https://ko.wikipedia.org/wiki/Lexcycle_Stanza "wikilink")         | 윈도, [OS X](https://ko.wikipedia.org/wiki/OS_X "wikilink"), [아이폰](../Page/아이폰.md "wikilink")                                                                       |                                                                   |                                                                               |
| [Lucidor (software)](https://ko.wikipedia.org/wiki/Lucidor_\(software\) "wikilink") | 윈도, [OS X](https://ko.wikipedia.org/wiki/OS_X "wikilink"), [리눅스](../Page/리눅스.md "wikilink")                                                                       |                                                                   |                                                                               |
| [Mobipocket](https://ko.wikipedia.org/wiki/Mobipocket "wikilink")                   | 윈도, [블랙베리](../Page/블랙베리_\(스마트폰\).md "wikilink"), [심비안](https://ko.wikipedia.org/wiki/심비안 "wikilink"), [윈도 모바일](https://ko.wikipedia.org/wiki/윈도_모바일 "wikilink")   |                                                                   |                                                                               |
| [Okular](https://ko.wikipedia.org/wiki/Okular "wikilink")                           | [리눅스](../Page/리눅스.md "wikilink"), 윈도, [Maemo](https://ko.wikipedia.org/wiki/Maemo "wikilink"), [OS X](https://ko.wikipedia.org/wiki/OS_X "wikilink")              |                                                                   |                                                                               |
| [Openberg Lector](https://ko.wikipedia.org/wiki/Openberg_Lector "wikilink")         |                                                                                                                                                                   |                                                                   |                                                                               |
| [수마트라 PDF](../Page/수마트라_PDF.md "wikilink")                                          |                                                                                                                                                                   |                                                                   | EPUB 기본 지원,[GPL](https://ko.wikipedia.org/wiki/GPL "wikilink")                |
| [IkuReader](https://ko.wikipedia.org/wiki/IkuReader "wikilink")                     | [닌텐도 DS](../Page/닌텐도_DS.md "wikilink")                                                                                                                            |                                                                   |                                                                               |
|                                                                                     |                                                                                                                                                                   |                                                                   |                                                                               |

Reading Systems and Software

### 편집 시스템

| 소프트웨어                                                                                               | 플랫폼                                                                                                                                                | 비고                                                                                                                         |
| --------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| wink2.0(윙크)                                                                                         | 윈도                                                                                                                                                 | Adobe AIR기반의 프로그램, CSS를 간단한 설정으로 생성할 수 있고, 폰트와 표지페이지 생성을 자동으로 만들어 준다. 안드로이드 앱과 pc용 앱으로 패키징을 지원한다.                          |
| [어도비 인디자인](../Page/어도비_인디자인.md "wikilink")                                                          | [윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink"), [OS X](https://ko.wikipedia.org/wiki/OS_X "wikilink")                                   |                                                                                                                            |
| [Atlantis Word Processor](https://ko.wikipedia.org/wiki/Atlantis_Word_Processor "wikilink")         | [윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink")                                                                                          | 어떤 문서든 변환, 글꼴 내장 제공                                                                                                        |
| [Autopub](https://ko.wikipedia.org/wiki/Autopub "wikilink")                                         | [웹](../Page/월드_와이드_웹.md "wikilink")                                                                                                                | 변환도구, 변환된 전자책 오픈마켓                                                                                                         |
| [biscuitMaker (application)](https://ko.wikipedia.org/wiki/biscuitMaker_\(application\) "wikilink") | [윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink"),[HWP](https://ko.wikipedia.org/wiki/HWP "wikilink")                                      | 한글워드파일을 편집하고 EPUB으로 변환 저장하는 EPUB 제작 도구                                                                                     |
| [BookGlutton Converter](https://ko.wikipedia.org/wiki/BookGlutton_Converter "wikilink")             | [웹](../Page/월드_와이드_웹.md "wikilink")                                                                                                                | 변환도구                                                                                                                       |
| [eBookStylist (application)](https://ko.wikipedia.org/wiki/eBookStylist_\(application\) "wikilink") | [윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink"), [리눅스](../Page/리눅스.md "wikilink"), [OS X](https://ko.wikipedia.org/wiki/OS_X "wikilink") | Adobe AIR기반의 프로그램, CSS를 간단한 설정으로 생성할 수 있는 스타일 EPUB 제작 도구                                                                   |
| [eBooksWriter](https://ko.wikipedia.org/wiki/eBooksWriter "wikilink")                               | [윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink")                                                                                          | 모비포켓 파일도 지원                                                                                                                |
| [eCub](https://ko.wikipedia.org/wiki/eCub "wikilink")                                               | [윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink"), [OS X](https://ko.wikipedia.org/wiki/OS_X "wikilink"), [리눅스](../Page/리눅스.md "wikilink") | 암호화 불가능                                                                                                                    |
| [Feedbooks](https://ko.wikipedia.org/wiki/Feedbooks "wikilink")                                     | [웹](../Page/월드_와이드_웹.md "wikilink")                                                                                                                | 무료 가상화 서비스 지원                                                                                                              |
| [iStudio Publisher](https://ko.wikipedia.org/wiki/iStudio_Publisher "wikilink")                     | [OS X](https://ko.wikipedia.org/wiki/OS_X "wikilink")                                                                                              | 전자 출판 소프트웨어                                                                                                                |
| [페이지](../Page/페이지_\(소프트웨어\).md "wikilink")                                                          | [OS X](https://ko.wikipedia.org/wiki/OS_X "wikilink")                                                                                              | 워드프로세서                                                                                                                     |
| [Sigil](https://ko.wikipedia.org/wiki/Sigil_\(application\) "wikilink")                             | [윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink"), [리눅스](../Page/리눅스.md "wikilink"), [OS X](https://ko.wikipedia.org/wiki/OS_X "wikilink") | GPLv3하의 자유 소프트웨어                                                                                                           |
| [펍트리 에디터](https://web.archive.org/web/20090413140708/http://www.namo.co.kr/)                        | [윈도](https://ko.wikipedia.org/wiki/윈도 "wikilink")                                                                                                  | 애플의 iBooks Author 처럼 소스없이 작업하면서 인터렉티브한 EPUB 3 제작 가능                                                                        |
| [뷰포터 에디터](http://viewporter.com/)                                                                   | [윈도](https://ko.wikipedia.org/wiki/윈도 "wikilink"), [Mac](https://ko.wikipedia.org/wiki/Mac "wikilink")                                             | 애플의 iBooks Author 처럼 코딩없이 작업하면서(실제로 코딩도 가능) 인터렉티브한 EPUB 3 제작 가능(앱북도 제작가능), 아이콘, 이미지, 오디오 및 비디오도 연결된 스토어에서 바로 다운로드 후 사용이 가능 |
| [genebook](http://genebook.de)                                                                      | [월드 와이드 웹](../Page/월드_와이드_웹.md "wikilink")                                                                                                         | 전자 책 편집 및 게시                                                                                                               |
| [wepubl author](https://www.wepubl.com)                                                             | 윈도                                                                                                                                                 | 전자 책 편집 및 게시                                                                                                               |
|                                                                                                     |                                                                                                                                                    |                                                                                                                            |

editing Systems and Software

## 각주

<references/>

## 외부 링크

  - [Open Publication Structure (OPS) 2.0 사양 정보](https://web.archive.org/web/20080827131750/http://www.idpf.org/2007/ops/OPS_2.0_final_spec.html)
  - [Open Packaging Format (OPF) 2.0 사양 정보](https://web.archive.org/web/20090604120716/http://www.idpf.org/2007/opf/OPF_2.0_final_spec.html)
  - [OEBPS Container Format (OCF) 1.0 사양 정보](https://web.archive.org/web/20091005005258/http://www.idpf.org/ocf/ocf1.0/download/ocf10.htm)
  - [International Digital Publishing Forum (IDPF) 홈페이지](https://web.archive.org/web/20100704034714/http://www.idpf.org/)
  - [샘플 전자책 라이브러리](https://web.archive.org/web/20090601063632/http://www.infogridpacific.com/igp/AZARDI/ePub%20Books%20and%20Resources/)
  - [팀 오라일리가 말하는 EPUB의 중요성, 포브스 기사](http://www.forbes.com/2009/02/22/kindle-oreilly-ebooks-technology-breakthroughs_oreilly.html)

[분류:전자 출판](https://ko.wikipedia.org/wiki/분류:전자_출판 "wikilink") [분류:페이지 기술 언어](https://ko.wikipedia.org/wiki/분류:페이지_기술_언어 "wikilink") [분류:XML 기반 표준](https://ko.wikipedia.org/wiki/분류:XML_기반_표준 "wikilink") [분류:오픈 포맷](https://ko.wikipedia.org/wiki/분류:오픈_포맷 "wikilink")

1.
2.
3.
4.
5.