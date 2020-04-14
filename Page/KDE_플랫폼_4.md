> This article is converted from Wikipedia: [KDE 플랫폼 4](https://ko.wikipedia.org/wiki/KDE_플랫폼_4).


[섬네일](https://ko.wikipedia.org/wiki/파일:KDE_brand_map.svg "wikilink") **KDE 플랫폼 4**(KDE Platform 4)는 [KDE](../Page/KDE.md "wikilink")의 라이브러리와 [소프트웨어 프레임워크의](../Page/소프트웨어_프레임워크.md "wikilink") 모음으로, [GNU LGPL](https://ko.wikipedia.org/wiki/GNU_LGPL "wikilink") 하에서 배포되는 [KDE 소프트웨어 컴파일레이션 4의](https://ko.wikipedia.org/wiki/KDE_소프트웨어_컴파일레이션_4 "wikilink") 기술 토대를 제공한다.

## 기술

  - 사용자 인터페이스
      - [플라스마](https://ko.wikipedia.org/wiki/KDE_플라스마_워크스페이스 "wikilink") - 데스크톱 및 패널 위젯 엔진
      - [KHTML](../Page/KHTML.md "wikilink") – [HTML 렌더링 엔진](https://ko.wikipedia.org/wiki/웹_브라우저_엔진 "wikilink")
      - [KIO](../Page/KIO.md "wikilink") – 외부 네트워크-투명 파일 접근
      - [KParts](https://ko.wikipedia.org/wiki/KParts "wikilink") – 가벼운 프로세스 내 그래픽 컴포넌트 프레임워크
      - [소넷](https://ko.wikipedia.org/wiki/소넷 "wikilink") – 철자 검사기
      - [XMLGUI](https://ko.wikipedia.org/wiki/XMLGUI "wikilink") – UI 요소 정의 ([XML](../Page/XML.md "wikilink") 파일을 통한 메뉴, 도구 모음 등)
      - [고야](https://ko.wikipedia.org/wiki/고야_\(KDE\) "wikilink")
  - 하드웨어 및 멀티미디어
      - [Phonon](https://ko.wikipedia.org/wiki/:en:Phonon_\(KDE\) "wikilink") – 멀티미디어 프레임워크
      - [Solid](https://ko.wikipedia.org/wiki/:en:Solid_\(KDE\) "wikilink") – 장치 연동 프레임워크
  - 서비스
      - [NEPOMUK](https://ko.wikipedia.org/wiki/NEPOMUK "wikilink")
      - [KNewStuff](https://ko.wikipedia.org/wiki/KNewStuff "wikilink") – KDE의 "Hot New Stuff" 클래스
      - [Policykit-KDE](https://ko.wikipedia.org/wiki/Policykit-KDE "wikilink")
  - 통신
      - [Akonadi](https://ko.wikipedia.org/wiki/Akonadi "wikilink")
  - 게임
      - [Gluon](https://ko.wikipedia.org/wiki/:en:Gluon_\(KDE\) "wikilink")
      - [KGGZ](https://ko.wikipedia.org/wiki/KGGZ "wikilink")
  - 기타
      - [스레드위버](https://ko.wikipedia.org/wiki/스레드위버 "wikilink") – 멀티프로세서 시스템을 더 효율적으로 사용하기 위한 라이브러리
      - [키오스크](https://ko.wikipedia.org/wiki/키오스크_\(KDE\) "wikilink") – KDE의 기능을 비활성화하여 더 통제된 환경을 만들 수 있게 함
      - [크로스](https://ko.wikipedia.org/wiki/크로스_\(KDE\) "wikilink")
      - [KConfig XT](https://ko.wikipedia.org/wiki/KConfig_XT "wikilink")
      - [ownCloud](https://ko.wikipedia.org/wiki/ownCloud "wikilink")\[1\]

### KDE 플랫폼 4로 대체된 기술

  - [aRts](https://ko.wikipedia.org/wiki/aRts "wikilink") – [사운드 드라이버](https://ko.wikipedia.org/wiki/사운드_드라이버 "wikilink")
  - [DCOP](https://ko.wikipedia.org/wiki/DCOP "wikilink") – [프로세스 간 통신](../Page/프로세스_간_통신.md "wikilink") 시스템 ([D-Bus](https://ko.wikipedia.org/wiki/D-Bus "wikilink") 대체)

## KParts

**KParts**는 [KDE 플라스마](https://ko.wikipedia.org/wiki/KDE_플라스마 "wikilink") [데스크톱 환경을](../Page/데스크톱_환경.md "wikilink") 위한 [컴포넌트](https://ko.wikipedia.org/wiki/소프트웨어_컴포넌트 "wikilink") 프레임워크이다. 개개의 컴포넌트는 **KPart**라고 한다.

## 스레드위버

## Hello World 예제

``` cpp-qt
#include <KApplication>
#include <KAboutData>
#include <KCmdLineArgs>
#include <KMessageBox>
#include <KLocale>

int main (int argc, char *argv[])
{
    KAboutData aboutData(
                         // The program name used internally.
                         "tutorial1",
                         // The message catalog name
                         // If null, program name is used instead.
                         0,
                         // A displayable program name string.
                         ki18n("Tutorial 1"),
                         // The program version string.
                         "1.0",
                         // Short description of what the app does.
                         ki18n("Displays a KMessageBox popup"),
                         // The license this code is released under
                         KAboutData::License_GPL,
                         // Copyright Statement
                         ki18n("Copyright (c) 2007"),
                         // Optional text shown in the About box.
                         // Can contain any information desired.
                         ki18n("Some text..."),
                         // The program homepage string.
                         "http://example.com/",
                         // The bug report email address
                         "submit@bugs.kde.org");

    KCmdLineArgs::init( argc, argv, &aboutData );
    KApplication app;
    KGuiItem yesButton( i18n( "Hello" ), QString(),
                        i18n( "This is a tooltip" ),
                        i18n( "This is a WhatsThis help text." ) );
    KMessageBox::questionYesNo( 0, i18n( "Hello World" ),
                                i18n( "Hello" ), yesButton );
    return 0;
}
```

## 각주

## 외부 링크

  - [TechBase](http://techbase.kde.org/), documentation for KDE developers
  - [KDE Projects](https://projects.kde.org/), overview of all projects within git.kde.org
  - [KDE quick Git source code browser](http://quickgit.kde.org/)
  - [KDE Bug Tracking System](http://arquivo.pt/wayback/19990430062327/http://bugs.kde.org/)
  - [KDE tutorial first program](http://techbase.kde.org/Development/Tutorials/First_program)

[KDE_플랫폼](https://ko.wikipedia.org/wiki/분류:KDE_플랫폼 "wikilink") [분류:API](https://ko.wikipedia.org/wiki/분류:API "wikilink") [분류:컴퓨팅 플랫폼](https://ko.wikipedia.org/wiki/분류:컴퓨팅_플랫폼 "wikilink") [분류:KDE 소프트웨어](https://ko.wikipedia.org/wiki/분류:KDE_소프트웨어 "wikilink") [분류:자유 라이브러리](https://ko.wikipedia.org/wiki/분류:자유_라이브러리 "wikilink")

1.  <http://owncloud.org/>