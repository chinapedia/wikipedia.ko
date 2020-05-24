> This article is converted from Wikipedia: [D-Bus](https://ko.wikipedia.org/wiki/D-Bus).


[컴퓨팅](../Page/컴퓨팅.md "wikilink")에서 **D-Bus**(데스크톱 버스, "**Desktop Bus**"\[1\])는 같은 머신에서 동시에 실행 중인 여러 [컴퓨터 프로그램](../Page/컴퓨터_프로그램.md "wikilink")(즉, [프로세스](../Page/프로세스.md "wikilink")) 간의 통신을 가능케 하는 [소프트웨어 버스](https://ko.wikipedia.org/wiki/소프트웨어_버스 "wikilink"), [프로세스 간 통신](../Page/프로세스_간_통신.md "wikilink") (IPC), [원격 프로시저 호출](../Page/원격_프로시저_호출.md "wikilink") (RPC) 매커니즘이다. D-Bus는 [레드햇](../Page/레드햇.md "wikilink")의 [하복 페닝튼이](https://ko.wikipedia.org/wiki/하복_페닝튼 "wikilink") [그놈](../Page/그놈.md "wikilink"), [KDE](../Page/KDE.md "wikilink") 등의 [리눅스](../Page/리눅스.md "wikilink") [데스크톱 환경이](../Page/데스크톱_환경.md "wikilink") 제공하는 서비스들을 표준화하기 위해 발의된, [Freedesktop.org](../Page/Freedesktop.org.md "wikilink") 프로젝트의 일부로서 개발되었다.

또, freedesktop.org 프로젝트는 이 사양의 참조 구현체로서 libdbus라는 이름의 [자유-오픈 소스](../Page/자유-오픈_소스_소프트웨어.md "wikilink") [라이브러리를](../Page/라이브러리_\(컴퓨팅\).md "wikilink") 개발하였다. 이 라이브러리는 D-Bus와는 구별된다. 실제로 다른 구현체의 D-Bus 클라이언트 라이브러리도 존재하는데, 이를테면 GDBus (GNOME), QtDBus ([Qt](../Page/Qt_\(프레임워크\).md "wikilink")/KDE), dbus-java, sd-bus ([systemd](https://ko.wikipedia.org/wiki/systemd "wikilink")의 일부) 등이 있다.

## 개요

D-Bus는 원래 [소프트웨어 구성 요소](../Page/컴포넌트_기반_소프트웨어_공학.md "wikilink") 통신 시스템을 대체하기 위해 설계된 IPC 패커니즘으로, [그놈](../Page/그놈.md "wikilink") 및 [KDE](../Page/KDE.md "wikilink") 리눅스 [데스크톱 환경](../Page/데스크톱_환경.md "wikilink")(각각 [CORBA](../Page/공통_객체_요구_매개자_구조.md "wikilink"), [DCOP](https://ko.wikipedia.org/wiki/DCOP "wikilink"))에 의해 사용된다. 이 데스크톱 환경들의 구성 요소들은 일반적으로 수많은 프로세스에 배포되며, 제각기 몇몇의 서비스(보통은 하나의 서비스)를 제공한다. 이러한 서비스들은 자신들의 태스크를 수행하기 위해 일반적인 클라이언트 [애플리케이션에](../Page/응용_소프트웨어.md "wikilink") 의해, 또는 데스크톱 환경의 다른 구성 요소들에 의해 사용될 수 있다.

수반되는 프로세스들의 수가 많은 까닭에 이들 간의 1대1 IPC 통신은 비효율적이고 꽤나 미덥지 못한 접근 방식이 된다. 대신, D-Bus는 [소프트웨어 버스](https://ko.wikipedia.org/wiki/소프트웨어_버스 "wikilink") [추상화를](../Page/추상화_\(컴퓨터_과학\).md "wikilink") 제공하여 단일 공유 가상 채널을 경유하여 일련의 프로세스들 간의 모든 통신을 수집한다. 버스에 연결된 프로세스들은 내부 구현 방식에 대해 알지 못하지만 D-Bus 사양은 버스에 연결된 모든 프로세스들이 이를 통해 서로 통신할 수 있음을 보증한다.

리눅스 데스크톱 환경은 하나의 버스뿐 아니라 수많은 버스들을 열거함으로써 D-Bus 기능을 활용한다:

  - 하나의 단일 **시스템 버스**: 시스템의 모든 사용자와 프로세스에 이용이 가능하며, 시스템 서비스에 대한 접근 권한을 제공한다. (예: [운영 체제와](../Page/운영_체제.md "wikilink") [데몬이](../Page/데몬_\(컴퓨팅\).md "wikilink") 제공하는 서비스들)
  - 각 사용자 로그인 세션별 **세션 버스**: 데스크톱 서비스를 동일 데스크톱 세션의 사용자 애플리케이션에 제공하고 하나의 단위로 데스크톱 세션을 허용한다

프로세스가 버스들에 대한 접근 권한이 있다면 프로세스는 수많은 버스들에 연결할 수 있다. 즉, 어떠한 사용자 프로세스라도 시스템 버스와 현재 소속된 세션 버스에 연결할 수 있으나 다른 사용자의 세션 버스, 심지어는 동일 사용자가 소유한 다른 세션 버스에 연결할 수는 없음을 의미한다. 후자의 제한은 나중에 모든 사용자 세션이 하나의 사용자 버스로 병합되는 경우에는 변경될 수 있다.

D-Bus는 정보 공유, 모듈성, [권한 격리](https://ko.wikipedia.org/wiki/권한_격리 "wikilink") 등 애플리케이션에 대한 기존 기능을 추가하거나 단순화한다. 이를테면, [블루투스](../Page/블루투스.md "wikilink")나 [스카이프](../Page/스카이프.md "wikilink")를 통해 들어온 음성 통화(voice call)의 정보는 현재 실행 중인 음악 플레이어에 의해 전파되고 해석될 수 있으며 통화가 끝날 때까지 음소거하거나 재생을 일시 중지시킴으로써 반응할 수 있다.

또, D-Bus는 각기 다른 사용자 애플리케이션의 구성 요소 연동을 위한 [프레임워크로서](../Page/소프트웨어_프레임워크.md "wikilink") 사용될 수 있다. 이를테면, [오피스 제품군은](https://ko.wikipedia.org/wiki/오피스_제품군 "wikilink") [워드 프로세서와](../Page/워드_프로세서.md "wikilink") [스프레드시트](../Page/스프레드시트.md "wikilink") 간 데이터 공유를 위해 세션 버스를 통해 통신할 수 있다.

## 같이 보기

  - [리눅스](../Page/리눅스.md "wikilink")
  - [공통 언어 기반](../Page/공통_언어_기반.md "wikilink")
  - [공통 객체 요구 매개자 구조](../Page/공통_객체_요구_매개자_구조.md "wikilink")
  - [컴포넌트 오브젝트 모델](../Page/컴포넌트_오브젝트_모델.md "wikilink")
  - [분산 컴포넌트 오브젝트 모델](https://ko.wikipedia.org/wiki/분산_컴포넌트_오브젝트_모델 "wikilink")
  - [외부 함수 인터페이스](../Page/외부_함수_인터페이스.md "wikilink")
  - [자바 원격 함수 호출](../Page/자바_원격_함수_호출.md "wikilink")
  - [원격 프로시저 호출](../Page/원격_프로시저_호출.md "wikilink")
  - [XPCOM](https://ko.wikipedia.org/wiki/XPCOM "wikilink")

## 각주

## 외부 링크

  - [D-Bus](http://www.freedesktop.org/Software/dbus) home page at Freedesktop.org
  - [D-Bus specification](http://dbus.freedesktop.org/doc/dbus-specification.html)
  - [Introduction to D-Bus](http://www.freedesktop.org/wiki/IntroductionToDBus) on the Freedesktop.org wiki
  - [D-Bus Tutorial](http://dbus.freedesktop.org/doc/dbus-tutorial.html)
  - [DBus Overview](https://pythonhosted.org/txdbus/dbus_overview.html)

[분류:응용 계층 프로토콜](https://ko.wikipedia.org/wiki/분류:응용_계층_프로토콜 "wikilink") [분류:C++ 라이브러리](https://ko.wikipedia.org/wiki/분류:C++_라이브러리 "wikilink") [분류:Freedesktop.org](https://ko.wikipedia.org/wiki/분류:Freedesktop.org "wikilink") [분류:프로세스 간 통신](https://ko.wikipedia.org/wiki/분류:프로세스_간_통신 "wikilink") [분류:원격 프로시저 호출](https://ko.wikipedia.org/wiki/분류:원격_프로시저_호출 "wikilink")

1.