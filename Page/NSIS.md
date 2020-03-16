> This article is converted from Wikipedia: [NSIS](https://ko.wikipedia.org/wiki/NSIS).


**NSIS**(Nullsoft Scriptable Install System, 널소프트 스크립터블 인스톨 시스템)는 스크립트 기반으로 동작하는 [윈도용](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") [설치 시스템으로](https://ko.wikipedia.org/wiki/설치_프로그램 "wikilink"), [윈앰프](../Page/윈앰프.md "wikilink")를 만든 것으로 알려져 있는 [널소프트](https://ko.wikipedia.org/wiki/널소프트 "wikilink")가 지원하는 가벼운 설치 시스템이다. NSIS는 [인스톨실드](https://ko.wikipedia.org/wiki/인스톨실드 "wikilink")와 같은 상용 [사유](https://ko.wikipedia.org/wiki/사유_소프트웨어 "wikilink") 제품들을 널리 대체하면서 인기를 끌고 있다.

NSIS는 주로 [zlib 라이선스인](https://ko.wikipedia.org/wiki/zlib_라이선스 "wikilink") [자유 소프트웨어 라이선스와](https://ko.wikipedia.org/wiki/자유_소프트웨어_라이선스 "wikilink") 결합한 [자유 소프트웨어이다](../Page/자유_소프트웨어.md "wikilink").\[1\]

## 역사

NSIS는 [윈앰프](../Page/윈앰프.md "wikilink")를 배포할 목적으로 만들어졌다. 이 시스템은 이전 [널소프트](https://ko.wikipedia.org/wiki/널소프트 "wikilink") 제품인 PiMP (플러그인 미니 패키저)에 기반을 두고 있으며 슈퍼PiMP(SuperPiMP)라고도 부른다. [버전](https://ko.wikipedia.org/wiki/소프트웨어_버전 "wikilink") 2.0a0 이후로 제품은 [소스포지](../Page/소스포지.md "wikilink")로 이동되면서 [널소프트](https://ko.wikipedia.org/wiki/널소프트 "wikilink") 외부 개발자들까지도 작업에 참가할 수 있게 되었다. 그러다가 약 2년 뒤에 NSIS 2.0이 출시되었다.

NSIS 버전 1은 여러 방면에서 [윈도 인스톨러의](https://ko.wikipedia.org/wiki/윈도_인스톨러 "wikilink") 기본 형태와 비슷하다. 그러나 스크립트를 작성하기 더 쉽고 더 많은 압축 포맷을 지원한다는 점에서 차이가 있다. NSIS 버전 2부터는 새로운 스트림라인 [GUI를](../Page/그래픽_사용자_인터페이스.md "wikilink") 제공하며 [LZMA](../Page/LZMA.md "wikilink") 압축, 다국어를 지원하며 플러그인 시스템을 쉽게 이용할 수 있게 되었다.

## 개념

### 스크립트

NSIS 컴파일러 시스템 *makensis*는 다음과 같은 예제의 스크립트를 컴파일하여 실행 가능한 설치 프로그램을 만든다. 이 스크립트의 각 줄은 하나의 명령어를 담고 있다.

``` nsis
# 스크립트 예제
Name "예제1"
OutFile "예제1.exe"
InstallDir "$PROGRAMFILES\예제1"
Page Directory
Page InstFiles
Section
  SetOutPath $INSTDIR
  File ..\makensis.exe
SectionEnd
```

### 현대의 사용자 인터페이스

[섬네일](https://ko.wikipedia.org/wiki/파일:NSIS_menu.png "wikilink") [오른쪽](https://ko.wikipedia.org/wiki/파일:Nsis1.png "wikilink") 버전 2.0부터 선택 가능한 스트림라인 [GUI](../Page/그래픽_사용자_인터페이스.md "wikilink") "모던 UI"(MUI)가 새롭게 도입되었다. 이 MUI는 [마법사같은](../Page/마법사_\(소프트웨어\).md "wikilink") 인터페이스를 갖추고 있다. 환경 페이지, 마침 페이지, 언어 선택 대화 상자, 구성 요소 기술 영역, 또 이전 사용자 인터페이스에 견주어 더 나은 사용자 지정 옵션을 지원한다.

``` nsis
# 모던 UI 스크립트 예제
!include MUI.nsh
Name "예제 2"
OutFile "예제2.exe"
!insertmacro MUI_PAGE_WELCOME
!insertmacro MUI_PAGE_LICENSE "license.rtf"
!insertmacro MUI_PAGE_DIRECTORY
!insertmacro MUI_PAGE_COMPONENTS
!insertmacro MUI_PAGE_INSTFILES
!insertmacro MUI_PAGE_FINISH
!insertmacro MUI_LANGUAGE "영어 (English)"
!insertmacro MUI_LANGUAGE "독일어 (German)"
!insertmacro MUI_LANGUAGE "프랑스어 (French)"
Section "Extract makensis"
  SetOutPath $INSTDIR
  File ..\makensis.exe
SectionEnd
```

NSIS 버전 2.30 (2007년 8월 25일 출시)부터는 이 사용자 인터페이스의 새로운 (베타) 버전을 이용할 수 있다. 이를 **모던 UI 2**(MUI2)라고 하며 기존의 모던 UI에 있던 기능들이 강화된 것이다. 오래된 MUI와 달리 이 버전은 오래된 방식의 InstallOptions .ini 파일이 아닌 nsDialogs에 기반을 둔다.

버전 2.34 (2007년 12월 24일)부터 MUI2는 이 시스템의 많은 이용에 대비하여 모든 NSIS 패키지에 포함되었다. 모든 예제가 it.[Modern UI 2](http://nsis.sourceforge.net/Docs/Modern%20UI%202/Readme.html) 문서로 전환되었다.

### 플러그인

NSIS는 설치 프로그램과 통신할 수 있는 [플러그인](../Page/플러그인.md "wikilink")으로 확장할 수 있다. 플러그인은 [C](../Page/C_\(프로그래밍_언어\).md "wikilink"), [C++](https://ko.wikipedia.org/wiki/C++ "wikilink"), [델파이로](https://ko.wikipedia.org/wiki/델파이_프로그래밍_언어 "wikilink") 작성할 수 있으며 설치 작업을 수행하거나 설치 프로그램 인터페이스를 확장하는 데 사용할 수도 있다. NSIS 코드에서 줄 하나만 추가하면 플러그인을 호출할 수 있다.

여러 플러그인들이 NSIS 패키지에 포함되어 있으며 이들을 이용하면 설치 프로그램이 스플래시 화면, 사용자 지정 페이지, 배경 위의 그림을 보여줄 수 있고 웹사이트로부터 파일을 내려받거나 연산 기능을 수행하거나 파일을 패치하는 등의 일도 할 수 있다.

그 밖의 플러그인들은 [ZipDLL](http://nsis.sourceforge.net/ZipDLL), [파이썬](../Page/파이썬.md "wikilink") [플러그인](http://nsis.sourceforge.net/Python_Interpreter)을 비롯하여 온라인에서 내려받을 수 있다.

## 기능

  - 매우 작은 [오버헤드](https://ko.wikipedia.org/wiki/오버헤드 "wikilink") (34 KB\[2\])
  - [zlib](https://ko.wikipedia.org/wiki/zlib "wikilink"), [bzip2](https://ko.wikipedia.org/wiki/bzip2 "wikilink"), [LZMA](../Page/LZMA.md "wikilink") 압축
  - 스크립트 기반
  - 다국어
  - [플러그인](../Page/플러그인.md "wikilink") 지원
  - 스크립트 [전처리](https://ko.wikipedia.org/wiki/전처리 "wikilink")
  - [그 밖의 기능...](http://nsis.sourceforge.net/Features)

## NSIS를 이용하는 제품

<table>
<tbody>
<tr class="odd">
<td><ul>
<li><a href="../Page/7-Zip.md" title="wikilink">7-Zip</a></li>
<li><a href="https://ko.wikipedia.org/wiki/아시아_온라인" title="wikilink">아시아 온라인 언어 스튜디오</a></li>
<li><a href="https://ko.wikipedia.org/wiki/ATI" title="wikilink">ATI</a> 디스플레이 드라이버</li>
<li><a href="https://ko.wikipedia.org/wiki/비트토렌트" title="wikilink">비트토렌트</a></li>
<li><a href="https://ko.wikipedia.org/wiki/CDex" title="wikilink">CDex</a></li>
<li><a href="../Page/DivX.md" title="wikilink">DivX</a></li>
<li><a href="../Page/이뮬.md" title="wikilink">이뮬</a></li>
<li><a href="../Page/파일질라.md" title="wikilink">파일질라</a></li>
<li><a href="../Page/FL_스튜디오.md" title="wikilink">FL 스튜디오</a></li>
<li><a href="https://ko.wikipedia.org/wiki/푸바2000" title="wikilink">푸바2000</a></li>
<li><a href="https://ko.wikipedia.org/wiki/FreeOTFE" title="wikilink">FreeOTFE</a></li>
<li><a href="https://ko.wikipedia.org/wiki/지오서버" title="wikilink">지오서버</a></li>
<li><a href="../Page/구글.md" title="wikilink">구글</a> (<a href="../Page/피카사.md" title="wikilink">피카사</a>, <a href="../Page/구글_토크.md" title="wikilink">토크</a>)</li>
<li><a href="../Page/인텔.md" title="wikilink">인텔</a> <a href="https://ko.wikipedia.org/wiki/인텔_C_컴파일러" title="wikilink">C 컴파일러</a></li>
<li><a href="../Page/IrfanView.md" title="wikilink">IrfanView</a></li>
<li>WireShark</li>
</ul></td>
<td><ul>
<li><a href="https://ko.wikipedia.org/wiki/카스퍼스키" title="wikilink">카스퍼스키</a> <a href="../Page/카스퍼스키_안티바이러스.md" title="wikilink">안티바이러스</a></li>
<li><a href="https://ko.wikipedia.org/wiki/LEGO_디지털_디자이너" title="wikilink">LEGO 디지털 디자이너</a></li>
<li><a href="https://ko.wikipedia.org/wiki/라임와이어" title="wikilink">라임와이어</a></li>
<li><a href="https://ko.wikipedia.org/wiki/라인_6" title="wikilink">라인 6</a> 팟 팜 / 기어박스 (Pod Farm / Gearbox)</li>
<li><a href="https://ko.wikipedia.org/wiki/LyX" title="wikilink">LyX</a></li>
<li><a href="https://ko.wikipedia.org/wiki/미란다_IM" title="wikilink">미란다 IM</a></li>
<li><a href="../Page/모질라_파이어폭스.md" title="wikilink">모질라 파이어폭스</a></li>
<li><a href="https://ko.wikipedia.org/wiki/NASA_World_Wind" title="wikilink">NASA World Wind</a></li>
<li><a href="https://ko.wikipedia.org/wiki/OpenOffice.org" title="wikilink">OpenOffice.org</a> (윈도)</li>
<li><a href="https://ko.wikipedia.org/wiki/PortableApps.com" title="wikilink">PortableApps.com</a></li>
<li><a href="../Page/피진_(소프트웨어).md" title="wikilink">피진</a></li>
<li><a href="https://ko.wikipedia.org/wiki/TASpring" title="wikilink">Spring</a></li>
<li><a href="../Page/VLC_미디어_플레이어.md" title="wikilink">VLC 미디어 플레이어</a></li>
<li><a href="../Page/윈앰프.md" title="wikilink">윈앰프</a></li>
<li><a href="https://ko.wikipedia.org/wiki/Warhammer_Online" title="wikilink">Warhammer Online</a></li>
</ul></td>
</tr>
</tbody>
</table>

그 밖의 항목은 [NSIS WWW 사이트](http://nsis.sourceforge.net/Users)에 나열되어 있다.

## 그래픽 인터페이스

NSIS 프로젝트는 (.nsi 확장자의) 간단히 문서 파일을 편집하여 구성할 수 있다. 그러나 다음과 같은 외부 소프트웨어를 이용하여 편집할 수도 있다:

  - [EclipseNSIS](http://eclipsensis.sourceforge.net/)은 [이클립스](https://ko.wikipedia.org/wiki/이클립스 "wikilink") 플랫폼을 위한 모듈이다. NSIS 스크립트의 편집, 컴파일, 검증을 도와준다.
  - [HM NIS Edit](http://hmne.sourceforge.net/)는 사용자 지정 [C++](https://ko.wikipedia.org/wiki/C++ "wikilink")/[델파이](../Page/델파이.md "wikilink") 플러그인을 지원하는 프리웨어 NSIS 편집기이다.
  - [Venis](http://nsis.sourceforge.net/Venis_IX)는 수많은 기능을 제공하는 프리웨어 편집기이다.

## 설치 프로그램 인터페이스

모던 UI를 대체하거나 확장하는 일부 프로젝트들은 지난 몇 년에 걸쳐 시작되고 있다. [ExperienceUI](https://web.archive.org/web/20060127085803/http://xpui.sourceforge.net/), [UltraModernUI](http://ultramodernui.sourceforge.net/)와 같은 인터페이스들은 [인스톨실드](https://ko.wikipedia.org/wiki/인스톨실드 "wikilink") 인터페이스와 비슷한 스킨을 입혀서 완전히 설치 프로그램의 스타일을 변경한다. [InstallSpiderUI](http://nsis.sourceforge.net/InstallSpiderUI)와 같은 그 밖의 인터페이스들은 모던 UI와 같은 수준의 기능을 유지하면서도 시각적인 측면에 더 최소화된 접근을 제공하는 것이 목적이다.

모던 UI 2 인터페이스에 기반한 프로젝트도 몇 가지 있는데, 기능이 더 강화되었으며 설치 프로그램의 스킨을 완전히 다시 입힐 수도 있다: [그래피컬 인스톨러 (Graphical Installer)](http://www.unsigned-softworks.sk/installer/) (상용 목적으로 판매되지만 개인은 무료로 이용할 수 있다). 주가 되는 장점은 설치 프로그램에 기반한 표준 MUI와 MUI2를 사용자가 지정한 그래픽(배경, 버튼, 체크 상자)의 스킨을 입힌 설치 프로그램으로 쉽게 변환할 수 있다는 것이다. 더 새로운 버전에는 단지 몇 초만에 완전한 스크립트를 만들 수 있는 마법사를 제공하는 HM NIS 편집을 위한 플러그인을 포함하기도 한다. 모든 기능을 보려면 [NSIS의 그래피컬 인스톨러 페이지](http://nsis.sourceforge.net/Graphical_Installer)를 참고하라.

## 제공 목적을 위한 설치 프로그램

제공 목적을 위한 설치 프로그램은 [PE 포맷으로](../Page/PE_포맷.md "wikilink") 되어 있으며 설치 파일들이 포함된 설치 프로그램을 가리킨다. 이는 NSIS 설치 프로그램에 34 KB 정도의 오버헤드가 있다.\[3\] 또, 설치 스크립트가 실행 코드로 컴파일된다. 설치 스크립트가 컴파일되면 스크립트는 이진 파일을 [역공학](https://ko.wikipedia.org/wiki/역공학 "wikilink")하지 않는 한 살펴보지 못한다.

이 압축 형태의 파일은 [7-Zip](../Page/7-Zip.md "wikilink")이나 [토탈 커맨더](../Page/토탈_커맨더.md "wikilink") 플러그인[InstallExplorer](http://www.totalcmd.net/plugring/InstallExplorer.html), [전처리기](https://web.archive.org/web/20050309212710/http://plugring.farmanager.com/cgi-bin/downld.cgi?Lang=Eng)를 이용하여 압축을 풀 수 있다.

이 압축 파일은 다음과 같은 폴더를 포함하고 있다:

  - **$PLUGINSDIR** : 설치 루틴 플러그인
  - **$INSTDIR** : 설치하는 동안에 쓰이는 파일
  - **$_OUTDIR** : 설치할 파일.

## 유니코드 지원

NSIS의 공식판은 3.0버전부터 유니코드를 정식 지원하고, 이전 버전의 경우에는 유니코드 지원을 포함하지 않지만 플러그인을 이용하면 일부 파일을 다른 인코딩으로 변환할 수 있다.\[4\]

2.xx버전대의 경우 [짐 파크](http://www.scratchpaper.com/)(Jim Park)는 완전한 유니코드 지원을 포함하는 NSIS의 변종을 만들어 유지, 제공하고 있다.\[5\]

짐 파크의 유니코드 변종을 이용하고 있는 프로젝트들은 다음과 같다\[6\]:

  - [구글](../Page/구글.md "wikilink") ([피카사](../Page/피카사.md "wikilink"))
  - [OpenOffice.org](https://ko.wikipedia.org/wiki/OpenOffice.org "wikilink") (윈도)
  - [모질라](../Page/모질라.md "wikilink") ([파이어폭스](https://ko.wikipedia.org/wiki/파이어폭스 "wikilink"), [모질라 선더버드](../Page/모질라_선더버드.md "wikilink"))
  - [파일질라](../Page/파일질라.md "wikilink")
  - [윈앰프](../Page/윈앰프.md "wikilink")
  - [flickr](../Page/플리커.md "wikilink")
  - [PortableApps.com](https://ko.wikipedia.org/wiki/PortableApps.com "wikilink")

## 같이 보기

  - [소프트웨어 설치 프로그램 목록](https://ko.wikipedia.org/wiki/:en:List_of_installation_software "wikilink")

## 참조

## 외부 링크

  - [NSIS 홈페이지](https://web.archive.org/web/20080516065536/http://nsis.sourceforge.net/)

  - [NSIS 소스포지 프로젝트 페이지](http://sourceforge.net/projects/nsis)

  - [이 달의 SourceForge.net 프로젝트](https://web.archive.org/web/20070227162451/http://sourceforge.net/potm/potm-2006-01.php) - 2006년 1월

[분류:자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_소프트웨어 "wikilink") [분류:윈도우 소프트웨어](https://ko.wikipedia.org/wiki/분류:윈도우_소프트웨어 "wikilink") [분류:C로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C로_작성된_자유_소프트웨어 "wikilink") [분류:C++로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C++로_작성된_자유_소프트웨어 "wikilink") [분류:Zlib 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:Zlib_라이선스_소프트웨어 "wikilink")

1.
2.  [Features - NSIS](http://nsis.sourceforge.net/Features)
3.  [Features](http://nsis.sourceforge.net/Features), NSIS
4.  [Unicode plug-in](http://nsis.sourceforge.net/Unicode_plug-in) - NSIS
5.  [Unicode NSIS 프로젝트 페이지](http://www.scratchpaper.com)
6.  [Unicode NSIS Project Users](http://www.scratchpaper.com/home/shameless-promotion)