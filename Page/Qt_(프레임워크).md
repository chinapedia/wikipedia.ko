> This article is converted from Wikipedia: [Qt \(\)](https://ko.wikipedia.org/wiki/Qt_\(\)).


**Qt**는 컴퓨터 프로그래밍에서 [GUI](../Page/그래픽_사용자_인터페이스.md "wikilink") 프로그램 개발에 널리 쓰이는 크로스 플랫폼 프레임워크이다. 서버용 콘솔과 명령 줄 도구와 같은 비GUI 프로그램 개발에도 사용된다. 그래픽 사용자 인터페이스를 사용하는 경우에는 Qt를 [위젯 툴킷으로](https://ko.wikipedia.org/wiki/위젯_툴킷 "wikilink") 분류한다. 회사 내부에서는 Qt를 "cute"로 발음하고 있으며 비공식적으로는 "큐티"로 발음한다. Qt는 [KDE](../Page/KDE.md "wikilink"), [Qtopia](https://ko.wikipedia.org/wiki/Qtopia "wikilink"), [OPIE](https://ko.wikipedia.org/wiki/OPIE "wikilink")에 이용되고 있다,

노르웨이 회사 [트롤텍](https://ko.wikipedia.org/wiki/트롤텍 "wikilink")에 의해서 개발되었다. 2008년 1월에는 [노키아](../Page/노키아.md "wikilink")에 인수되었다.\[1\] 이후, 2012년 8월에 핀란드 회사 [Digia](https://ko.wikipedia.org/wiki/Digia "wikilink")에 인수되었다.\[2\]

Qt는 [C++](https://ko.wikipedia.org/wiki/C++ "wikilink")를 주로 사용하지만, [파이썬](../Page/파이썬.md "wikilink"), [루비](../Page/루비_\(프로그래밍_언어\).md "wikilink"), [C](../Page/C_\(프로그래밍_언어\).md "wikilink"), [펄](../Page/펄.md "wikilink"), [파스칼과도](../Page/파스칼_\(프로그래밍_언어\).md "wikilink") 연동된다. 수많은 플랫폼에서 동작하며, 상당히 좋은 국제화를 지원한다. [SQL](../Page/SQL.md "wikilink") 데이터베이스 접근, [XML](../Page/XML.md "wikilink") 처리, [스레드](https://ko.wikipedia.org/wiki/스레드 "wikilink") 관리, 단일 크로스 플랫폼 파일 관리 [API](../Page/API.md "wikilink")를 제공한다.

## 종류

Qt는 다음 플랫폼으로 개발된다.

  - 리눅스/X11 — [X 윈도 시스템](../Page/X_윈도_시스템.md "wikilink")([유닉스](../Page/유닉스.md "wikilink") / [리눅스](../Page/리눅스.md "wikilink"))을 위한 Qt
  - 맥 OS X — [OS X을](https://ko.wikipedia.org/wiki/OS_X "wikilink") 위한 Qt
  - 윈도 — [마이크로소프트 윈도를](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 위한 Qt
  - 임베디드 리눅스 — [PDA](https://ko.wikipedia.org/wiki/PDA "wikilink"), [스마트폰](../Page/스마트폰.md "wikilink") 등의 임베디드 플랫폼을 위한 Qt
  - 윈도 CE — [윈도 CE](https://ko.wikipedia.org/wiki/윈도_CE "wikilink") 등을 위한 Qt
  - 심비안 - [심비안](https://ko.wikipedia.org/wiki/심비안 "wikilink")을 위한 Qt
  - 마에모- [Maemo](https://ko.wikipedia.org/wiki/Maemo "wikilink")를 위한 Qt

각각 플랫폼에는 세 종류의 에디션이 있다.

  - GUI 프레임워크 — 네트워크와 데이터베이스를 제외한 순수 GUI 개발 에디션.(데스크톱 라이트-Desktop Light-라고도 불린다.)
  - 풀 프레임워크 — 상업용 개발을 위한 완전한 에디션.
  - 오픈 소스 — 오픈 소스 개발을 위한 완전한 에디션.

### 비주얼 스튜디오 및 볼랜드 C++ 빌더 지원

[Q../Free](http://sourceforge.net/projects/qtwin/) 프로젝트는 몇몇 패치 [1](http://sourceforge.net/project/showfiles.php?group_id=49109) 를 내어 놓았다. 이 패치는 비주얼 스튜디오 및 볼랜드 C++ 빌더 지원을 Qt/Windows 오픈 소스 에디션에 추가한다.

## 현재

트롤텍은 Qt 4를 [2005년](../Page/2005년.md "wikilink") [6월 28일에](../Page/6월_28일.md "wikilink") 내 놓았으며 다섯 가지의 중요한 새 기술을 추가하였다.

  - 튤립(Tulip) - 템플릿 컨테이너 클래스 모음.
  - 인터뷰(Interview) - 항목 보기를 위한 모델/뷰 아키텍처.
  - 아서(Arthur) - 2차원 그리기 프레임워크.
  - 스크라이브(Scribe) - 낮은 수준의 텍스트 레이아웃을 지원하는 유니코드 텍스트 렌더러.
  - 메인윈도(MainWindow) - 액션 기반의 메인 윈도, 도구 모음, 메뉴, 도킹 아키텍처.

Qt 4는 모든 플랫폼에서 GPL, LGPL과 상용 라이선스 세 종류로 제공된다. 하지만 Qt/Windows 3.3 이하는 상용 라이선스만으로 제공된다.

[2005년](../Page/2005년.md "wikilink") [12월 19일에](../Page/12월_19일.md "wikilink") 출시된 Qt 4.1은 [SVG](https://ko.wikipedia.org/wiki/SVG "wikilink") Tiny 지원을 추가하였고, Qt 인쇄 시스템에 [PDF](../Page/PDF.md "wikilink") 백엔드를 추가했다. 또한 [이 곳](https://web.archive.org/web/20060315161449/http://www.trolltech.com/newsroom/announcements/00000229.html) 에서 추가적인 기능을 확인할 수 있다.

## 역사

하버드 노드(Haavard Nord)와 에이릭(Eirik Chambe-Eng, Qt의 원 개발자이자 현재 트롤텍의 CEO) 둘은 [1991년](../Page/1991년.md "wikilink") Qt의 개발을 시작했다. 이 회사의 이름은 퀘이사 테크놀로지스(Quasar Technologies)로 시작해서, 트롤 테크(Troll Tech), 트롤테크(Trolltech)로 바뀌어 갔다. 하버드의 [이맥스](../Page/이맥스.md "wikilink") 글꼴 중 Q라는 글자가 예뻐 보였고, t는 X 툴킷 [Xt에서](https://ko.wikipedia.org/wiki/Intrinsics "wikilink") 따 와서 Qt라는 이름을 붙였다.

[1998년](../Page/1998년.md "wikilink") KDE가 [리눅스](../Page/리눅스.md "wikilink") 데스크톱 환경으로 많이 사용되면서 논쟁이 시작되었다. KDE는 Qt를 사용하고, 많은 오픈 소스나 자유 소프트웨어에 연관된 사람들이 그들의 운영체계의 주된 부분이 상용 소프트웨어라는 것에 우려를 표했다. 이것은 두 결과를 가지고 왔다. 하나는 [하모니 툴킷이라고](https://ko.wikipedia.org/wiki/하모니_툴킷 "wikilink") 하는 자유 소프트웨어로 된 Qt의 복제품이었고, 또 다른 하나는 KDE를 대체할 수 있는 [그놈](../Page/그놈.md "wikilink") 데스크톱이었다. 그놈은 [김프](../Page/김프.md "wikilink")를 위해서 작성된 [GTK+를](https://ko.wikipedia.org/wiki/김프_툴킷 "wikilink") 사용했고, 그것은 자유롭게 사용 가능했기 때문이다.

버전 1.45까지 Qt의 원본 코드는 FreeQt 라이선스로 공개되었다. 하지만 자유 소프트웨어 재단은 수정된 버전을 재배포할 수 없었기 때문에 이것이 오픈 소스의 정신에 부합된다고 생각하지 않았다. Qt 2.0이 나오면서 [Q 퍼블릭 라이선스로](https://ko.wikipedia.org/wiki/Q_퍼블릭_라이선스 "wikilink") 공개되었다. 이것은 자유 소프트웨어 라이선스이지만 자유 소프트웨어 재단에서는 [GPL과](../Page/GNU_일반_공중_사용_허가서.md "wikilink") 호환될 수 없다고 하였다. KDE와 트롤텍 사이에서 트롤텍이 파산을 해도 Qt가 QPL보다 더 제약 사항이 많은 라이선스로 바뀌는 것을 막기 위해서 [KDE 자유 Qt 재단](https://web.archive.org/web/20070127134848/http://www.kde.org/whatiskde/kdefreeqtfoundation.php) 을 만들었다. 이 재단에서는 Qt의 오픈 소스 버전이 12개월 동안 공개되지 않는 경우 Qt가 자동으로 BSD 라이선스로 전환하도록 한다.

Qt의 초기 버전은 유닉스용 Qt/X11, 윈도용 Qt/Windows 두 가지 플랫폼만 지원했다. 윈도용은 상업적 라이선스로만 사용할 수 있었다. 2001년 말 Qt 3.0이 나오면서 [맥 OS X](https://ko.wikipedia.org/wiki/맥_OS_X "wikilink") 지원이 추가되었다. Mac OS X 지원은 2003년 6월 Qt 3.2의 GPL 버전이 OS X을 지원하기 전까지는 상용으로만 사용할 수 있었다.

2002년 KDE on Cygwin 프로젝트의 회원들이 GPL로 공개된 Qt/X11 코드를 윈도에서 사용할 수 있도록 포팅 작업을 하고 있었다. [2](http://qtwin.sourceforge.net/qt3-win32/history.php) 이것은 윈도가 오픈소스 환경이 아니기 때문에 트롤텍이 Qt/Windows를 GPL로 공개하지 않았기 때문에 시작되었다. [3](http://lists.kde.org/?l=kde-cygwin&m=104431728920022&w=2)[4](https://web.archive.org/web/20031005175911/http://www.trolltech.com/developer/faqs/noncomm.html) 이 프로젝트는 상용화 단계에 들어갈 수 없었지만 많은 성공을 거두었다. Qt/Windows 4가 2005년 6월 GPL로 공개되면서 존재할 필요가 없어졌다. Qt 4부터는 상용 에디션과 오픈소스 에디션 간의 플랫폼 차이가 없다.

## 디자인

### 클래스 디자인

Qt 4.0 기준으로 다음과 같은 클래스로 나뉘어 있다.

  - QtCore – 핵심 클래스
  - QtGui – 그래픽 사용자 인터페이스 구성요소
  - QtNetwork – 네트워크 구성요소
  - QtOpenGL – OpenGL 구성요소
  - QtSql – SQL 데이터베이스 구성요소
  - QtSvg – SVG 그림 구성요소
  - QtXml – XML 파서 구성요소
  - QtDesigner – Qt 디자이너를 위한 클래스
  - QtUiTools – Qt 디자이너 폼을 다루는 클래스
  - QtAssistant – 온라인 도움말을 위한 클래스
  - Qt3Support – Qt 3 호환성 클래스
  - QtTest – 프로그램 테스트를 위한 클래스

Qt 라이브러리를 사용하는 데 도움을 주는 도구는 다음과 같다.

  - Qt-Creator - IDE 툴로 개발 및 디버깅 문법검사를 지원한다.
  - Qt-Designer – Qt 프로그램의 폼을 작성해 준다.
  - Qt-Assistant – 온라인 문서를 제공한다.
  - Qt-Linguist, lupdate und lrelease – 프로그램의 지역화를 도와 준다.
  - qmake – ([qmake](https://ko.wikipedia.org/wiki/qmake "wikilink") 참고)
  - moc – Qt 메타 정보 컴파일러
  - uic – Qt 폼 컴파일러 (.ui -\> .h)
  - rcc – Qt 리소스 컴파일러<sup>1</sup>

<small>1. 현재 Qt는 리소스를 자체적으로 지원하는 윈도나 OS X에서 그 기능을 사용하지 않는다.</small>

Qt가 처음 나왔을 때의 디자인적인 혁명은 다음과 같다.

### GUI의 완전한 추상화

Qt는 자체 페인팅 엔진과 컨트롤을 사용하며, 실행되는 플랫폼의 모습을 최대한 따라한다. 따라서 Qt는 플랫폼에 의존적인 코드를 거의 사용하지 않았으므로 서로 다른 플랫폼으로 이식하는 것이 쉬웠다. 하지만 이 방법은 서로 다른 플랫폼의 모습을 정교하게 따라하도록 해야 하는 것이다. 최근 버전의 Qt는 서로 다른 플랫폼의 자체 API를 사용해서 Qt 컨트롤을 그리므로 최근의 Qt에는 적용되지 않는다. [wxWidgets](https://ko.wikipedia.org/wiki/wxWidgets "wikilink") 같은 다른 플랫폼에 의존하는 함수를 사용하는 그래픽 툴킷들은 그 나름대로의 디자인을 가지고 있다.

### 메타 오브젝트 컴파일러

약칭 "moc" 로 알려져 있는 이 프로그램은 Qt에서 사용되고 있는 비표준적인 메타데이터들을 처리하기 위한 도구이다. 일례로 Qt에서 사용하고 있는 이벤트 처리방식인 시그널-슬롯 방식은 표준 C++ 처리방식이 아니다.

이러한 비표준적인 방식을 사용하는 것에 대해 기존의 C++ 사용자들의 비판이 일었다. 또한, 매크로를 기반으로 한 구현은 타입 안전성과 네임스페이스 오염을 유발할 수 있다고 한다.

하지만 이러한 비판에 트롤텍은 Qt의 첫 출시될 당시에는 템플릿 구현에 있어서 컴파일러 간에 차이가 있었을 뿐 아니라 시그널-슬롯의 동적생성 및 RTTI에 있어서 이러한 구조를 사용할 필요가 있다고 주장했다.

## 사용하는 곳

Qt는 다음 프로그램 및 환경에서 사용된다.

### Qt

  - [다음 클라우드](https://ko.wikipedia.org/wiki/다음_클라우드 "wikilink")(Daum Cloud)
  - [KDE](../Page/KDE.md "wikilink")

### Qtopia

  - 샤프 [자우루스](https://ko.wikipedia.org/wiki/자우루스 "wikilink")
  - i-Station T43 PMP
  - 모토로라 E680/A780 휴대폰

그 밖의 정보는 [5](https://web.archive.org/web/20060615034114/http://www.trolltech.com/customers/casestories) 를 참고하기 바란다.

## [Hello World 프로그램](https://ko.wikipedia.org/wiki/Hello_World_프로그램 "wikilink")

``` cpp
#include <QtGui>
#include <QLabel>

int main(int argc, char *argv[])
{
    QApplication app(argc, argv);
    QLabel label("Hello, world!");
    label.show();
    return app.exec();
}
```

## 같이 보기

  - [GTK](https://ko.wikipedia.org/wiki/GTK "wikilink")

## 각주

## 외부 링크

  - [Qt 홈페이지](http://www.qt.io/)

  - [Qt Wiki홈페이지](https://wiki.qt.io/Main/ko)

  - [Qt 홈페이지](http://www.qtsoftware.com/title-ko?set_language=ko&cl=ko)

[분류:KDE](https://ko.wikipedia.org/wiki/분류:KDE "wikilink") [분류:X 윈도 시스템](https://ko.wikipedia.org/wiki/분류:X_윈도_시스템 "wikilink") [분류:위젯 툴킷](https://ko.wikipedia.org/wiki/분류:위젯_툴킷 "wikilink") [분류:1992년 소프트웨어](https://ko.wikipedia.org/wiki/분류:1992년_소프트웨어 "wikilink") [분류:C++로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C++로_작성된_자유_소프트웨어 "wikilink") [분류:LGPL 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:LGPL_라이선스_소프트웨어 "wikilink") [분류:자유 라이브러리](https://ko.wikipedia.org/wiki/분류:자유_라이브러리 "wikilink")

1.  <http://techcrunch.com/2008/01/28/nokia-acquires-trolltech-for-153-million/>
2.