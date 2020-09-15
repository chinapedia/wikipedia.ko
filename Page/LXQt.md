> This article is converted from Wikipedia: [LXQt](https://ko.wikipedia.org/wiki/LXQt).


**LXQt**는 완전한 [데스크톱 환경을](../Page/데스크톱_환경.md "wikilink") 제공하는 것을 목표로 하는, 개발 중인 소프트웨어 패키지의 번들이다. [LXDE](../Page/LXDE.md "wikilink")과 [Razor-qt](https://ko.wikipedia.org/wiki/Razor-qt "wikilink") 프로젝트의 병합을 통해 만들어졌다.

## 역사

[GTK+](../Page/GTK+.md "wikilink") 3에 만족하지 못한\[1\] [LXDE](../Page/LXDE.md "wikilink")의 유지보수자 Hong Jen Yee는 2013년 초에 [Qt를](../Page/Qt_\(프레임워크\).md "wikilink") 실험하였으며\[2\] 2013년 3월 26일 최초 버전의 Qt 기반 [PCManFM](https://ko.wikipedia.org/wiki/PCManFM "wikilink")을 출시하였다.\[3\] 그러나 그는 "Gtk+와 Qt 버전은 공존할 것이다"라고 못박았다. 나중에 그는 LXDE의 [Xrandr](https://ko.wikipedia.org/wiki/Xrandr "wikilink") 프론트엔드를 Qt로 [이식하였다](../Page/이식_\(컴퓨팅\).md "wikilink").\[4\]

2013년 7월 3일에 Hong Jen Yee는 완전한 LXDE 스위트의 Qt 포팅 버전을 발표하였으며,\[5\] 2013년 7월 21일, [Razor-qt](https://ko.wikipedia.org/wiki/Razor-qt "wikilink")와 LXDE는 두 프로젝트의 병합을 결정했다고 발표하였다.\[6\]\[7\] 이 병합은 GTK+와 Qt 버전이 처음에 공존할 것이지만 최종적으로는 GTK+ 버전을 중단하고 Qt 포팅 노력에 초점을 두겠다는 의미가 된다.\[8\] LXDE-Qt와 Razor-qt의 병합으로 말미암아 LXQt로 이름이 바뀌었으며,\[9\] 최초 릴리스 버전 0.7.0은 2014년 5월 7일에 이용이 가능하게 되었다.\[10\]

## 소프트웨어 구성 요소

LXQt는 수많은 모듈 방식의 구성 요소로 이루어져 있으며 그 중 일부는 Qt와 KDE 프레임워크 5에 의존한다.\[11\]

| 이름                                                                    | 의존 (Qt 외)                                                                 |
| --------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| [qterminal](https://ko.wikipedia.org/wiki/qterminal "wikilink")       |                                                                           |
| [:en:QupZilla](https://ko.wikipedia.org/wiki/:en:QupZilla "wikilink") |                                                                           |
| [sddm](https://ko.wikipedia.org/wiki/sddm "wikilink")                 |                                                                           |
| lximage-qt                                                            |                                                                           |
| lxmenu-data                                                           |                                                                           |
| lxqt-about                                                            |                                                                           |
| lxqt-admin                                                            |                                                                           |
| lxqt-common                                                           |                                                                           |
| lxqt-config                                                           | KScreen ([:en:RandR](https://ko.wikipedia.org/wiki/:en:RandR "wikilink")) |
| lxqt-globalkeys                                                       | KGlobalAccel                                                              |
| lxqt-notificationd                                                    |                                                                           |
| lxqt-openssh-askpass                                                  |                                                                           |
| lxqt-panel                                                            | [Solid](../Page/KDE_플랫폼_4.md "wikilink")                                  |
| lxqt-policykit                                                        |                                                                           |
| lxqt-powermanagement                                                  | Solid                                                                     |
| lxqt-qtplugin                                                         |                                                                           |
| lxqt-runner                                                           |                                                                           |
| lxqt-session                                                          |                                                                           |
| lxqt-sudo                                                             |                                                                           |
| menu-cache                                                            |                                                                           |
| obconf-qt                                                             |                                                                           |
| compton-conf                                                          |                                                                           |
| pcmanfm-qt                                                            |                                                                           |
| qt-gtk-engine                                                         |                                                                           |

### 로드맵

  - [LXQt 로드맵](https://github.com/lxde/lxqt/wiki/Roadmap)

## 버전 역사

| 버전    | 날짜               | 설명                                                                                                                                                                           |
| ----- | ---------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 0.7.0 | 2014-05-07\[12\] |                                                                                                                                                                              |
| 0.8.0 | 2014-10-13\[13\] | 완전한 [Qt 5](../Page/Qt_\(프레임워크\).md "wikilink") [호환성](https://ko.wikipedia.org/wiki/컴퓨터_호환성 "wikilink")                                                                       |
| 0.9   | 2015-02-08       | 상당한 내부 정리 및 [리팩터링](../Page/리팩터링.md "wikilink") 처리. Qt 4 호환 지원이 중단되어 Qt 5 및 [KDE 프레임워크](https://ko.wikipedia.org/wiki/KDE_프레임워크 "wikilink") 5 필요. Qt 5.3이 현재 최소 요구 버전임.\[14\] |
| 0.10  | 2015-11-02\[15\] |                                                                                                                                                                              |
| 0.11  | 2016-09-24\[16\] |                                                                                                                                                                              |
| 0.12  | 2017-10-21\[17\] | 최소 Qt 버전 5.6.1\[18\]                                                                                                                                                         |

## 같이 보기

  - [Razor-qt](https://ko.wikipedia.org/wiki/Razor-qt "wikilink")

## 각주

## 외부 링크

  -
[LXDE](https://ko.wikipedia.org/wiki/분류:LXDE "wikilink") [분류:2013년 소프트웨어](https://ko.wikipedia.org/wiki/분류:2013년_소프트웨어 "wikilink") [분류:자유 데스크톱 환경](https://ko.wikipedia.org/wiki/분류:자유_데스크톱_환경 "wikilink")

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
11. <https://github.com/lxde/lxqt/wiki/KF5-usage-in-LXQt>
12.
13.
14.
15.
16.
17.
18.