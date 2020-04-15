> This article is converted from Wikipedia: [KDE 소프트웨어 모음](https://ko.wikipedia.org/wiki/KDE_소프트웨어_모음).


[대체글=](https://ko.wikipedia.org/wiki/파일:KDE_Mascot_Konqi_by_Tyson_Tan.png "wikilink")\]\] **KDE**(**K** **D**esktop **E**nvironment , K 데스크톱 환경)는 [자유 소프트웨어](../Page/자유_소프트웨어.md "wikilink") 데스크톱 환경으로, [노키아](../Page/노키아.md "wikilink")의 [Qt 툴킷을](../Page/Qt_\(프레임워크\).md "wikilink") 기반으로 하였다. 대부분의 [유닉스 계열](../Page/유닉스_계열.md "wikilink"), [리눅스](../Page/리눅스.md "wikilink"), BSD, AIX 등의 운영 체제에서 작동한다. [OS X의](https://ko.wikipedia.org/wiki/OS_X "wikilink") X11 레이어를 이용한 포팅과 [시그윈](../Page/시그윈.md "wikilink")과 네이티브에서 동작하는 [마이크로소프트 윈도에](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 대한 포팅도 진행 중으로, 현재 kdelibs의 많은 부분과 기타 다른 프로그램들이 [마이크로소프트 윈도에서](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 잘 작동한다.

'K'는 원래 "Kool"의 앞글자에서 유래했지만, 나중에 알파벳 'L'(리눅스의 'L') 앞에 있는 'K'를 의미하는 것으로 바뀌었다.

이 프로젝트의 마스코트는 [콘키](https://ko.wikipedia.org/wiki/콘키 "wikilink")라고 하는 녹색 용으로, KDE 정보 화면에서 이를 만날 수 있다.

## 역사

KDE는 [1996년](../Page/1996년.md "wikilink") 당시 [튀빙엔 대학교](https://ko.wikipedia.org/wiki/튀빙엔_대학교 "wikilink") 학생이었던 [마티아스 에트리히가](https://ko.wikipedia.org/wiki/마티아스_에트리히 "wikilink") 설립하였다. 그는 당시의 유닉스 데스크톱 환경에 불만이 많았다. 그의 지적대로 어떠한 프로그램들도 비슷하게 보이지도, 느껴지지도, 작동하지도 않았다. 또한 그의 불만 가운데 하나는 그 당시의 데스크톱 프로그램들은 그의 여자 친구가 사용할 수 없었다는 것이다. 그 글은 많은 인기를 끌었으며 KDE 프로젝트가 시작되었다.

마티아스는 [Qt를](../Page/Qt_\(프레임워크\).md "wikilink") 사용하기로 했다. 많은 다른 프로그래머들이 KDE/Qt 프로그램을 짜기 시작했고 1997년 초에 많은 프로그램들이 나오기 시작했다. 그 당시에 [Qt는](../Page/Qt_\(프레임워크\).md "wikilink") 자유 소프트웨어 라이선스를 사용하지 않았기 때문에 GNU 프로젝트의 회원들이 걱정하기 시작했다. 그래서 "Harmony"라고 하는 Qt 라이브러리의 자유 소프트웨어 구현과 Qt를 사용하지 않는 데스크톱 환경인 [그놈](../Page/그놈.md "wikilink") 프로젝트가 시작되었다.

[1998년](../Page/1998년.md "wikilink") [11월](../Page/11월.md "wikilink"), Qt 툴킷은 QPL 라이선스로 오픈 소스로 공개되었지만, GPL과의 호환성이 계속 논의되었다. [2000년](../Page/2000년.md "wikilink") [9월](../Page/9월.md "wikilink"), Trolltech은 Qt 라이브러리의 유닉스용은 GPL로 공개하였다. 이것은 자유 소프트웨어 재단의 걱정을 줄여 줄 수 있었다. Qt 4.0부터 유닉스, 맥, 윈도 플랫폼에서도 많은 KDE 프로그램과 라이브러리가 이 플랫폼들로 포팅되고 있다.

Trolltech이 사업 실패를 해서 코드가 사라지는 것을 막기 위해서 Trolltech 쪽에서 코드를 업데이트하지 않거나 망했을 때 코드들이 BSD 라이선스로 유지되도록 하였다. KDE와 그놈 둘 다 Freedesktop.org에 참여해서 상호 호환성을 유지하려고 노력하지만 아직도 많은 선의의 경쟁이 이뤄지고 있다.

## KDE 프로젝트의 조직

많은 오픈 소스/자유 소프트웨어처럼 KDE는 자원 봉사자들의 노력으로 이뤄지고 있으며, Novell, Mandriva, Nokia에서도 많은 지원을 아끼지 않고 있다. 많은 사람들이 KDE에 공여하고 있으므로 프로젝트가 복잡하게 될 수밖에 없다. 대부분 문제들이 많은 메일링 리스트에서 논의되고 있다.

출시 날짜나 새로운 프로그램의 추가 같은 중요한 결정들은 *kde-core-devel* 리스트에서 *core developers*에 의해 결정된다. 이들은 KDE에 오랫동안 중요한 기여를 한 사람들이다. 결정은 메일링 리스트의 토론을 통해서 이뤄진다. 대부분의 경우에 이 시스템은 잘 작동하며, KDE 2에서 3으로 올라가면서 API를 새로 쓰도록 하는 등의 큰 결정은 꽤 드물다.

개발자와 사용자가 전 세계에 퍼져 있기 때문에 프로젝트는 독일에 강력한 기반을 두고 있다. 웹 서버들은 [튀빙엔](https://ko.wikipedia.org/wiki/튀빙엔_대학교 "wikilink") 및 [카이저스라우테른 대학에](https://ko.wikipedia.org/wiki/카이저스라우테른_대학 "wikilink") 있다. 비영리 단체 KDE e.V.에서 KDE의 상표권을 가지며, KDE 회의들이 종종 독일에서 열린다

## 재사용 주기와 버전 번호

프로젝트의 역사처럼, KDE 팀은 새로운 버전을 주기적으로 출시한다. 하나의 공개 버전이 연기되는 일은 거의 없다. 그렇지만 KDE 3.1은 기반 코드에서의 보안 결함 때문에 출시가 한 달 이상 늦어졌다. 두 종류의 공개 버전이 있다.

### 주요 버전

다음 18개의 주요 버전이 있었다: 1.0, 1.1, 2.0, 2.1, 2.2, 3.0, 3.1, 3.2, 3.3, 3.4, 3.5, 4.0, 4.1, 4.2, 4.3, 4.4, 4.5 (현재 4.6)

주요 KDE 버전은 두 가지의 버전 번호가 있다. (예: KDE 1.1) 모든 KDE 릴리즈는 주 버전 번호가 같다면 (예: KDE 1, KDE 2, KDE 3, KDE 4) 이진 파일과 소스가 호환된다. 이것은 KDE 4.x를 염두에 둔 소프트웨어는 모든 KDE 4에서 동작한다는 것이다.

다시 컴파일하거나 포팅을 요구하는 일은 주요 버전이 바뀌는 것 빼곤 없다. 이것은 KDE 프로그램 개발자에게 안정적안 API를 제공한다. KDE의 주 버전 번호는 Qt의 출시 주기를 따른다.

주요 공개 버전이 준비되고 알려지는 즉시, 다음 주 출시를 위한 작업을 시작한다. 주요 공개 버전은 몇 달을 가다듬고 버그들을 수정하면서 안정 버전으로 백포트한다. 현재 주요 공개 버전은 KDE 4 이다.

### 부가 버전

KDE의 부가 버전은 세 가지의 버전 번호가 있다. (예: KDE 1.1.1) 그리고 개발자들은 버그 수정, 잔잔한 일들, 사용 편의성 증가 등에 초점을 맞춘다. 부가 버전의 주기는 상당히 짧다. 부가 버전은 직전 공개 버전에서 갈라져 나오며, HEAD 브랜치에는 영향을 주지 않는다.

> `　　　　　　　기능 추가/버그 수정`
> ` KDE 4.2 릴리즈 ──────────>  KDE 4.3 (HEAD 브랜치로 불림)`
> ` (새 개발 시작)`
> ` 　　　　　　　　버그 수정만`
> ` 　　　　　　　　──────────>  KDE 4.2.x 브랜치 (부가 버전이 됨)`

특별한 버전 번호 "3.0.5a" 등은 버전 번호가 부족할 때 썼다. KDE 3.1 작업이 이미 시작되었고, 출시 계획자는 3.0.5, 3.0.6 버전을 3.1 버전의 스냅샷을 나타내는 것으로 사용했다. 그런데 KDE 3.0.3 이후로도 버그 수정이 계속 필요했고 KDE 3.0.6이 그 당시에 사용 중이었기 때문에 충돌이 생길 수 있었다. 더 최근의 KDE 공개판들은 스냅샷들을 4.3.72과 같은 더 큰 리비전 번호를 사용함 으로써 충돌을 예방하고 있다.

## KDE 4

KDE 4는 현재 KDE의 주요 공개 버전으로, [Qt](../Page/Qt_\(프레임워크\).md "wikilink") 4 를 기반으로 [2008년](../Page/2008년.md "wikilink") 1월 11일 발표되었으며\[1\] 다음의 추가 기능을 지원한다.

  - kdelibs API를 새로 썼고, 인터페이스 지침을 새로 작성.
  - [Oxygen Project에서](https://ko.wikipedia.org/wiki/Oxygen_Project "wikilink") 개발한 [SVG 포맷의](https://ko.wikipedia.org/wiki/SVG "wikilink") 새로운 데스크톱 아이콘과 테마.
  - kdebase중 workspace 패키지를 통한 [Plasma](https://web.archive.org/web/20090315040144/http://plasma.kde.org/)라고 불리는 새로운 데스크톱과 패널과 Kicker, [KDesktop](https://ko.wikipedia.org/wiki/KDesktop "wikilink"), 그리고 [SuperKaramba](https://ko.wikipedia.org/wiki/SuperKaramba "wikilink").
  - [돌핀을](../Page/돌핀_\(파일_관리자\).md "wikilink") 통한 새로운 파일 관리 시스템.
  - [캉커러](../Page/캉커러.md "wikilink")에서 잘 통합된 파일 관리 및 웹 브라우징.
  - [ECMA스크립트](../Page/ECMA스크립트.md "wikilink")를 기반으로 한 새로운 스크립팅 시스템.
  - [Phonon](https://www.webcitation.org/67lLj6qv4?url=http://phonon.kde.org/)이라고 하는 새로운 멀티미디어 인터페이스.
  - 네트워크 및 휴대용 장치를 다루는 [Solid](https://web.archive.org/web/20080525085511/http://solid.kde.org/) [API](../Page/API.md "wikilink").
  - Tenor라고 불리는 [메타데이터](../Page/메타데이터.md "wikilink") 및 검색 프레임워크.
  - [KWin](https://ko.wikipedia.org/wiki/KWin "wikilink")의 새로운 화면 효과 플러그인.
  - [마이크로소프트 윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 및 [OS X으로의](https://ko.wikipedia.org/wiki/OS_X "wikilink") 포팅.

### KDE 4.4

KDE 4.4는 다음 KDE의 주 버전 릴리즈이며 다음의 기능을 지원할 예정이다.

  - KDE 4.4부터 [넷북](../Page/넷북.md "wikilink")을 위한 새로운 Plasma-netbook 지원.
  - [ssh](../Page/시큐어_셸.md "wikilink") 등을 통한 [Plasma](https://web.archive.org/web/20090315040144/http://plasma.kde.org/) 위젯의 원격 사용 지원.
  - 더욱 화려하고 간결해진 새로운 위젯 추가 선택 창 지원.

## KDE를 사용하는 소프트웨어

  - [Amarok](https://ko.wikipedia.org/wiki/아마록 "wikilink") - 오디오 플레이어
  - [Dolphin](../Page/돌핀_\(파일_관리자\).md "wikilink") - [파일 관리자](https://ko.wikipedia.org/wiki/파일_관리자 "wikilink")
  - [K3b](../Page/K3b.md "wikilink") - 디스크 굽기 및 편집 프로그램
  - [Kate](https://ko.wikipedia.org/wiki/Kate "wikilink") - [텍스트 에디터](https://ko.wikipedia.org/wiki/텍스트_에디터 "wikilink")
  - [Kdenlive](../Page/Kdenlive.md "wikilink") - 비선형 비디오 편집 프로그램
  - [KDevelop](../Page/KDevelop.md "wikilink") - 개발 환경
  - [Konsole](https://ko.wikipedia.org/wiki/Konsole "wikilink") - 터미널 구동기
  - [Kontact](https://ko.wikipedia.org/wiki/Kontact "wikilink") - 개인 일정 관리자 및 메일, 피드 리더.
  - [Kopete](https://ko.wikipedia.org/wiki/Kopete "wikilink") - 인스턴트 메신저
  - [Konqueror](https://ko.wikipedia.org/wiki/Konqueror "wikilink") - [웹 브라우저](../Page/웹_브라우저.md "wikilink") 및 [파일 관리자](https://ko.wikipedia.org/wiki/파일_관리자 "wikilink")
  - [KOffice](../Page/KOffice.md "wikilink") - [오피스 제품군](https://ko.wikipedia.org/wiki/오피스_제품군 "wikilink")
  - [KTorrent](https://ko.wikipedia.org/wiki/KTorrent "wikilink") - BitTorrent 클라이언트

## KDE Plasma 5 의 스크린샷

|KDE Plasma 5.16

## 참조

## 외부 링크

  - [KDE 공식 웹사이트](http://www.kde.org/)
  - [KDE UserBase](https://web.archive.org/web/20100405075523/http://userbase.kde.org/Welcome_to_KDE_UserBase_\(ko\))
  - [KDE TechBase](https://web.archive.org/web/20091009130930/http://techbase.kde.org/Welcome_to_KDE_TechBase_\(ko\))
  - [KDE Community Forums](http://forum.kde.org/)

[분류:자유 데스크톱 환경](https://ko.wikipedia.org/wiki/분류:자유_데스크톱_환경 "wikilink") [분류:KDE 소프트웨어](https://ko.wikipedia.org/wiki/분류:KDE_소프트웨어 "wikilink") [분류:X 윈도 시스템](https://ko.wikipedia.org/wiki/분류:X_윈도_시스템 "wikilink") [분류:리눅스용 유틸리티](https://ko.wikipedia.org/wiki/분류:리눅스용_유틸리티 "wikilink") [분류:macOS용 유틸리티](https://ko.wikipedia.org/wiki/분류:macOS용_유틸리티 "wikilink") [분류:윈도우용 유틸리티](https://ko.wikipedia.org/wiki/분류:윈도우용_유틸리티 "wikilink") [분류:1998년 소프트웨어](https://ko.wikipedia.org/wiki/분류:1998년_소프트웨어 "wikilink")

1.  [KDE 4 Release Schedule](http://techbase.kde.org/Schedules/KDE4/4.0_Release_Schedule)