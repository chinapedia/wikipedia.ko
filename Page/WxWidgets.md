> This article is converted from Wikipedia: [WxWidgets](https://ko.wikipedia.org/wiki/WxWidgets).


**wxWidgets** (이전 이름: wxWindows)는 [크로스 플랫폼](https://ko.wikipedia.org/wiki/크로스_플랫폼 "wikilink") 응용 프로그램을 위한 [그래픽 사용자 인터페이스를](https://ko.wikipedia.org/wiki/그래픽_사용자_인터페이스 "wikilink") 만들어 주는 [위젯 툴킷이다](https://ko.wikipedia.org/wiki/위젯_툴킷 "wikilink"). wxWidgets는 특별한 코드 변경 없이도 프로그램의 GUI 코드를 여러 컴퓨터의 운영 체제에서 컴파일하고 동작할 수 있게 도와 준다. [마이크로소프트 윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink"), [OS X](https://ko.wikipedia.org/wiki/OS_X "wikilink"), [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink")/[유닉스](https://ko.wikipedia.org/wiki/유닉스 "wikilink") ([X11](https://ko.wikipedia.org/wiki/X11 "wikilink"), [모티프](https://ko.wikipedia.org/wiki/모티프_\(위젯_툴킷\) "wikilink"), [GTK+](https://ko.wikipedia.org/wiki/GTK+ "wikilink")), [오픈VMS](https://ko.wikipedia.org/wiki/오픈VMS "wikilink"), [OS/2](https://ko.wikipedia.org/wiki/OS/2 "wikilink"), [아미가OS](https://ko.wikipedia.org/wiki/아미가OS "wikilink")와 같은 운영 체제를 지원한다. [임베디드 시스템을](https://ko.wikipedia.org/wiki/임베디드_시스템 "wikilink") 위한 버전은 현재 개발 중이다.\[1\]

## 역사

wxWidgets(원래는 wxWindows)는 1992년에 [에든버러 대학교의](https://ko.wikipedia.org/wiki/에든버러_대학교 "wikilink") 줄리안 스마트(Julian Smart)가 시작하였다.\[2\] 그는 1986년에 [세인트앤드루스 대학교로부터](https://ko.wikipedia.org/wiki/세인트앤드루스_대학교 "wikilink") [계산과학](../Page/계산과학.md "wikilink") 대학 우등 코스 졸업 학위를 받았고 지금도 핵심 개발자이다.\[3\]\[4\]

2004년 2월 20일에 wxWindows의 개발자들은 프로젝트 이름을 wxWidgets로 바꾸고 있다고 언급하였다. 그 까닭은 [마이크로소프트](https://ko.wikipedia.org/wiki/마이크로소프트 "wikilink")사가 줄리안 스마트에게 "Windows"라는 마이크로소프트의 [영국](https://ko.wikipedia.org/wiki/영국 "wikilink") 상표를 존중해 달라는 요청을 하였기 때문이었다.\[5\] 2003년 6월 9일에 주된 공개 버전이 2.4이었으며 2005년 4월 23일에는 2.6, 2006년 12월 14일에는 2.80이었다.

## 라이선스

wxWidgets는 [GNU 약소 일반 공중 사용 허가서와](../Page/GNU_약소_일반_공중_사용_허가서.md "wikilink") 비슷한 맞춤식 라이선스로 배포된다. 이를테면 일반적인 GNU 허가서에서 명시된 바와 달리 wxWidgets를 통해 만든 이진 형태의 작품은 사용자가 소스를 공개해도 되고 공개하지 않아도 된다. 이 라이선스는 [자유 소프트웨어 라이선스이므로](https://ko.wikipedia.org/wiki/자유_소프트웨어_라이선스 "wikilink") wxWidgets는 [자유 소프트웨어가](https://ko.wikipedia.org/wiki/자유_소프트웨어 "wikilink") 된다.\[6\]

## 기능

wxWidgets 라이브러리는 흔히 쓰이는 수많은 [프로그래밍 언어에](https://ko.wikipedia.org/wiki/프로그래밍_언어 "wikilink") 이용할 수 있는 [언어 결합과](https://ko.wikipedia.org/wiki/언어_결합 "wikilink") 더불어 [C++](https://ko.wikipedia.org/wiki/C++ "wikilink")로 추가되었다. 지원하는 프로그래밍 언어로는 이를테면 [파이썬](https://ko.wikipedia.org/wiki/파이썬 "wikilink") ([wxPython](https://ko.wikipedia.org/wiki/wxPython "wikilink")), [얼랭](https://ko.wikipedia.org/wiki/얼랭 "wikilink") ([wxErlang](https://web.archive.org/web/20100819232924/http://sourceforge.net/apps/mediawiki/wxerlang/index.php?title=Main_Page)), [하스켈](https://ko.wikipedia.org/wiki/하스켈 "wikilink") ([wxHaskell](https://ko.wikipedia.org/wiki/wxHaskell "wikilink")), [Tcl](../Page/Tcl.md "wikilink") ([wxTCL](https://web.archive.org/web/20080211101523/http://membres.lycos.fr/awaken/)), [루아](https://ko.wikipedia.org/wiki/루아_\(프로그래밍_언어\) "wikilink") ([wxLua](https://web.archive.org/web/20100817175822/http://wxlua.sourceforge.net/)), [펄](https://ko.wikipedia.org/wiki/펄 "wikilink") ([wxPerl](https://ko.wikipedia.org/wiki/wxPerl "wikilink")), [루비](https://ko.wikipedia.org/wiki/루비_\(프로그래밍_언어\) "wikilink") ([wxRuby](http://webarchive.loc.gov/all/20090306104458/http://wxruby.rubyforge.org/wiki/wiki.pl)), [스몰토크](https://ko.wikipedia.org/wiki/스몰토크 "wikilink") ([wxSqueak](https://web.archive.org/web/20100913031514/http://www.wxsqueak.org/)), [커먼 리스프](https://ko.wikipedia.org/wiki/커먼_리스프 "wikilink") ([wxCL](https://web.archive.org/web/20090430131620/http://www.wxcl-project.org/language/en/)), [베이직](https://ko.wikipedia.org/wiki/베이직 "wikilink") ([wxBasic](http://wxbasic.sourceforge.net/)), [C](https://ko.wikipedia.org/wiki/C_\(프로그래밍_언어\) "wikilink") ([wxC](http://wxc.sourceforge.net/)), [D](https://ko.wikipedia.org/wiki/D_\(프로그래밍_언어\) "wikilink") ([wxD](https://web.archive.org/web/20100820021606/http://wxd.sourceforge.net/)), [유포리아](https://ko.wikipedia.org/wiki/유포리아_\(프로그래밍_언어\) "wikilink") ([wxEuphoria](http://wxeuphoria.sourceforge.net/)), [닷넷 프레임워크](../Page/닷넷_프레임워크.md "wikilink") ([wx.NET](https://web.archive.org/web/20100825110129/http://wxnet.sourceforge.net/)), [자바](https://ko.wikipedia.org/wiki/자바_\(프로그래밍_언어\) "wikilink") ([wx4j](http://wx4j.sourceforge.net/)), [자바스크립트](https://ko.wikipedia.org/wiki/자바스크립트 "wikilink") ([wxJavaScript](http://www.wxjavascript.net/) / [GLUEScript](http://gluescript.sourceforge.net/)) 등이 있다. 완전한 목록을 보려면, 이 문서 끝에 보이는 외부 링크 참조를 통하여 각 프로젝트 사이트의 링크로 들어가면 된다. 1995년에 만든 wxWindows (버전 1)의 비호환 분기를 이용하는 [라켓도](https://ko.wikipedia.org/wiki/라켓_\(프로그래밍_언어\) "wikilink") 있다. 이 툴킷은 단순히 라이브러리 바인딩을 제공하는 다른 언어와는 달리 언어 런타임 (쓰레기 수집, 자원 관리)에 통합되어 있다.

wxWidgets는 [네이티브 모드](https://ko.wikipedia.org/wiki/네이티브_모드 "wikilink") 툴킷으로 잘 알려져 있는데 이는 원시 그래픽을 이용하여 위젯 표현을 따라하지 않고 얇은 추상화(thin abstraction)를 플랫폼의 네이티브 위젯에 제공하기 때문이다. 대상 플랫폼에 이러한 네이티브 위젯을 이용하면 [스윙](https://ko.wikipedia.org/wiki/스윙_\(자바\) "wikilink") (자바의 경우)과 같은 도구킷보다 더 네이티브하게 보이는 인터페이스뿐 아니라 성능 향상과 다른 이점도 제공한다.\[7\]

이 도구킷은 GUI 개발에만 국한되지 않으며 [프로세스 간 통신](../Page/프로세스_간_통신.md "wikilink") 계층, [소켓](https://ko.wikipedia.org/wiki/인터넷_소켓 "wikilink") 네트워킹 기능 등도 내장하고 있다.

## 공식 지원

### 지원 플랫폼

wxWidgets는 다음 플랫폼을 지원한다\[8\]

  - **윈도** - wxMSW (윈도 95/98/ME, NT, 2000, XP, 비스타)
  - **리눅스/유닉스** wxGTK+, wxX11, wxMotif
  - **OS X** - wxMac (10.3, 카본을 이용)
  - **OS/2** - wxOS2, wxPM, wxWidgets for GTK+, Motif는 OS/2에서 컴파일 가능
  - **임베디드 플랫폼** - wxEmbedded\[9\]

#### 외부 포팅

  - **아미가** - wxWidgets-AOS: AmigaOS port\[10\]

### 지원 컴파일러

wxWidgets는 공식적으로 다음 컴파일러와 정상 동작함이 확인되었다.\[11\]

<table>
<thead>
<tr class="header">
<th><p>wxMSW</p></th>
<th><p>wxGTK</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>컴파일러</p></td>
<td><p>버전</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/마이크로소프트_비주얼_스튜디오" title="wikilink">마이크로소프트 비주얼 스튜디오</a> - <a href="https://ko.wikipedia.org/wiki/비주얼_C++" title="wikilink">비주얼 C++</a><br />
<a href="https://ko.wikipedia.org/wiki/볼랜드_C++" title="wikilink">볼랜드 C++</a><br />
<a href="https://ko.wikipedia.org/wiki/볼랜드_C++_빌더" title="wikilink">볼랜드 C++ 빌더</a><br />
<a href="https://ko.wikipedia.org/wiki/왓콤_C/C++_컴파일러" title="wikilink">왓콤 C++</a>, <a href="https://ko.wikipedia.org/wiki/오픈왓콤" title="wikilink">오픈왓콤</a><br />
<a href="https://ko.wikipedia.org/wiki/코드워리어" title="wikilink">코드워리어</a><br />
<a href="../Page/시그윈.md" title="wikilink">시그윈</a><br />
<a href="../Page/MinGW.md" title="wikilink">MinGW</a><br />
<a href="https://ko.wikipedia.org/wiki/디지털_마스" title="wikilink">디지털 마스</a> C/C++ 컴파일러</p></td>
<td><p>5.0 +<br />
5.5 +<br />
2006 +<br />
10.6 +<br />
7 +<br />
1.5 +<br />
2.0 +<br />
8.40 +</p></td>
</tr>
</tbody>
</table>

## wxWidgets을 위한 RAD 도구 및 IDE

  - [wxDev-C++](https://ko.wikipedia.org/wiki/wxDev-C++ "wikilink")
  - [Code::Blocks](https://ko.wikipedia.org/wiki/Code::Blocks "wikilink")
  - [코드라이트](https://ko.wikipedia.org/wiki/코드라이트 "wikilink")
  - [wxGlade](https://ko.wikipedia.org/wiki/wxGlade "wikilink")
  - 보아 컨스트럭터 ([파이썬](https://ko.wikipedia.org/wiki/파이썬 "wikilink"))

## 같이 보기

  - [위젯 툴킷](https://ko.wikipedia.org/wiki/위젯_툴킷 "wikilink")
  - [Qt (프레임워크)](https://ko.wikipedia.org/wiki/Qt_\(프레임워크\) "wikilink")
  - [GTK+](https://ko.wikipedia.org/wiki/GTK+ "wikilink")

## 각주

<references />

## 외부 링크

  - [공식 웹사이트](http://wxwidgets.org/)
  - [wxWidgets 포럼](https://web.archive.org/web/20170116151401/http://wxforum.shadonet.com/)
  - [wxCode](http://wxcode.sourceforge.net/)
  - [wxPack](http://wxpack.sourceforge.net/)

[분류:위젯 툴킷](https://ko.wikipedia.org/wiki/분류:위젯_툴킷 "wikilink") [분류:C++ 라이브러리](https://ko.wikipedia.org/wiki/분류:C++_라이브러리 "wikilink") [분류:1992년 소프트웨어](https://ko.wikipedia.org/wiki/분류:1992년_소프트웨어 "wikilink") [분류:C++로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C++로_작성된_자유_소프트웨어 "wikilink") [분류:자유 라이브러리](https://ko.wikipedia.org/wiki/분류:자유_라이브러리 "wikilink")

1.
2.  <http://wxwidgets.org/about/>
3.  [About Julian Smart](http://www.anthemion.co.uk/julian.htm)
4.
5.  <http://wxwidgets.org/about/name.htm>
6.
7.
8.
9.
10.
11.