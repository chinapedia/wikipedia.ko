> This article is converted from Wikipedia: [Udev](https://ko.wikipedia.org/wiki/Udev).


[섬네일에](https://ko.wikipedia.org/wiki/파일:Free_and_open-source-software_display_servers_and_UI_toolkits.svg "wikilink") 통합되었다.\]\] **udev**는 [리눅스 커널을](../Page/리눅스_커널.md "wikilink") 위한 장치 관리자이다. [devfsd](https://ko.wikipedia.org/wiki/devfsd "wikilink")와 hotplug를 계승하는 udev는 주로 [/dev](https://ko.wikipedia.org/wiki/Devfs "wikilink") 디렉터리의 [장치 노드를](../Page/장치_파일.md "wikilink") 관리한다. 동시에 udev는 특정 장치에 필요한 [펌웨어](../Page/펌웨어.md "wikilink") 적재를 포함하여 하드웨어 장치가 시스템에 추가되거나 제거되는 동안 발생한 모든 사용자 공간 이벤트들을 관리한다.

## 개요

/dev 디렉터리의 [장치 노드들에](https://ko.wikipedia.org/wiki/장치_노드 "wikilink") 정적인 파일들을 모아두는 전통적인 [유닉스](../Page/유닉스.md "wikilink") 시스템과는 달리, 리눅스의 udev 장치 관리자는 시스템에 실제로 존재하는 장치들의 노드들만 동적으로 제공한다. [devfs가](../Page/장치_파일.md "wikilink") 비슷한 기능을 제공하는데 사용되지만, [그레그 크로아 하트먼은](https://ko.wikipedia.org/wiki/그레그_크로아_하트먼 "wikilink") devfs 보다 udev를 선호하는 이유\[1\]를 다수 언급하였다.

  - udev는 영속적인 장치 명명 기능을 지원하는데, 예를 들어 장치가 시스템에 장착된 순서에 의존하지 않는다. 기본 udev의 설정은 장치 이름의 영구적인 이름을 제공한다. 어떠한 하드 디스크라도 고유한 파일 시스템 ID, 디스크의 이름, 하드웨어가 장착된 물리적 위치에 의해 인식된다.
  - devfs의 [커널 공간과는](https://ko.wikipedia.org/wiki/커널_공간 "wikilink") 달리 udev는 완전히 [사용자 이름](https://ko.wikipedia.org/wiki/사용자_이름 "wikilink") 안에서 실행된다. 명명 정책을 커널 밖으로 끄집어내었고, 노드를 만들기 전에 임의의 프로그램들을 실행하여 장치의 속성들로부터 장치의 이름을 구성할 수 있게 하였다. 즉, 모든 과정은 중단이 가능하며 더 낮은 우선에서 동작한다.

udev를 크게 보면 세 가지로 나뉜다:

  - [라이브러리](../Page/라이브러리_\(컴퓨팅\).md "wikilink") libudev는 장치 정보의 접근을 허용한다. [systemd](https://ko.wikipedia.org/wiki/systemd "wikilink") 소프트웨어 번들에 통합되었다.
  - 가상 /dev를 관리하는 사용자 공간 [데몬](../Page/데몬_\(컴퓨팅\).md "wikilink") udevd.
  - 진단을 위한 관리 [명령 줄](https://ko.wikipedia.org/wiki/명령_줄 "wikilink") 유틸리티 udevadm.

시스템은 [넷링크](https://ko.wikipedia.org/wiki/넷링크 "wikilink") 소켓을 통해 커널로부터 호출들을 가져온다. 초기 버전들은 이러한 목적을 위해 hotplug를 사용하여 /etc/hotplug.d/default에서 자기 자신들에 대한 링크를 추가한다.

## 역사

udev는 리눅스 2.5에 도입되었다.

리눅스 커널 버전 2.6.13은 새로운 버전의 uevent 인터페이스를 도입하였다. 새로운 버전의 udev를 사용하는 시스템은 udev를 비활성화하고 전통적인 /dev 디렉터리를 장치 접근에 사용하지 않는 한 2.6.14 미만의 커널에서 부팅되지 않는다.

## 각주

## 외부 링크

  - [udev source code](http://cgit.freedesktop.org/systemd/systemd/tree/src/udev)

  - [mdev documentation](http://git.busybox.net/busybox/plain/docs/mdev.txt)

  - [eudev project](https://wiki.gentoo.org/wiki/Project:Eudev)

[분류:컴퓨터 설정](https://ko.wikipedia.org/wiki/분류:컴퓨터_설정 "wikilink") [분류:리눅스 커널의 인터페이스](https://ko.wikipedia.org/wiki/분류:리눅스_커널의_인터페이스 "wikilink") [분류:리눅스 커널 특징](https://ko.wikipedia.org/wiki/분류:리눅스_커널_특징 "wikilink") [분류:유닉스 파일 시스템 관련 소프트웨어](https://ko.wikipedia.org/wiki/분류:유닉스_파일_시스템_관련_소프트웨어 "wikilink")

1.