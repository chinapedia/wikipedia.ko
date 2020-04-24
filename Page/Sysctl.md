> This article is converted from Wikipedia: [Sysctl](https://ko.wikipedia.org/wiki/Sysctl).


**sysctl**은 버전 번호나 보안 설정 같은 시스템 [커널의](../Page/커널_\(컴퓨팅\).md "wikilink") 속성들을 읽고 수정하는 몇몇 [유닉스 계열](../Page/유닉스_계열.md "wikilink") 운영 체제의 기능이다. 이것은 컴파일된 프로그램에서 [시스템 호출로서](../Page/시스템_호출.md "wikilink") 그리고 스크립트로도 사용될 수 있는 관리 명령어로서도 사용 가능하다. [리눅스](../Page/리눅스.md "wikilink")는 추가적으로 sysctl을 가상 파일 시스템로서 사용 가능하게 한다.

## BSD

BSD에서 이러한 매개변수들은 일반적으로 공유 메모리 세그먼트의 크기, 운영 체제가 [NFS](../Page/네트워크_파일_시스템.md "wikilink") 클라이언트로서 사용할 스레드의 수, 시스템에서의 최대 프로세스의 개수 같은 조정 가능한 제한을 명시하거나 IP 포워딩이나 보안 제한 또는 디버깅 출력 등을 명시하는 [관리 정보 베이스](https://ko.wikipedia.org/wiki/관리_정보_베이스 "wikilink")(MIB)의 객체들이다.

BSD에서 [시스템 호출](../Page/시스템_호출.md "wikilink") 또는 시스템 호출 래퍼는 일반적으로 프로그램에서 사용 가능하며 또한 관리 프로그램과 설정 파일에서도 사용할 수 있게 제공된다.

## 리눅스

리눅스에서 sysctl 인터페이스 메커니즘은 또한 `/proc/sys` 디렉토리 아래에서 [procfs](https://ko.wikipedia.org/wiki/procfs "wikilink")의 한 부분으로서 사용될 수 있다([`/sys` 디렉토리와](../Page/Sysfs.md "wikilink") 헷갈리면 안된다). 이 차이는 어떤 매개변수의 값을 검사하려면 [가상 파일 시스템에서](https://ko.wikipedia.org/wiki/가상_파일_시스템 "wikilink") 파일을 오픈하고 내용을 읽고 파싱한 후에 파일을 닫을 필요가 있다는 것이다. sysctl 시스템 호출은 리눅스에서 존재하지만 [glibc에서](../Page/GNU_C_라이브러리.md "wikilink") 래핑 함수로 존재하지 않으며 사용하는 것이 추천되지는 않는다.\[1\]

## 예시

IP 포워딩이 활성화되면 운영 체제는 [라우터](../Page/라우터.md "wikilink")처럼 행동할 것이다. [FreeBSD](../Page/FreeBSD.md "wikilink"), [NetBSD](../Page/NetBSD.md "wikilink"), [OpenBSD](../Page/OpenBSD.md "wikilink"), [DragonFly BSD](../Page/DragonFly_BSD.md "wikilink"), 그리고 [Darwin](../Page/다윈_\(운영_체제\).md "wikilink")/[Mac OS X에서](https://ko.wikipedia.org/wiki/MacOS "wikilink") 매개변수 `net.inet.ip.forwarding` 는 이 행위를 활성화하기 위해 `1`로 설정될 수 있다. 리눅스의 sysctl 에뮬레이션에서 매개변수는 `net.ipv4.ip_forward` 로 불린다.

대부분의 시스템에서 명령어 ` sysctl -w  `*`parameter`*`=1` 은 특정한 행위를 활성화할 것이다. 이것은 리부팅될 때까지 유지된다. 만약 특정 행위가 시스템 부팅 시마다 활성화되어야 한다면 *`parameter`*`=1` 이 파일 `/etc/sysctl.conf`에 추가될 수 있다. 추가적으로 어떤 sysctl 변수들은 시스템이 부팅된 이후에는 수정되지 않는다. 이러한 변수들은 커널 컴파일 시간에 정적으로 설정되거나 `/boot/loader.conf`에서 설정한다.

## 각주

## 외부 링크

  -
  -
  - [EnderUNIX sysctl](http://sysctl.enderunix.org)

  - [Sysctl.conf example for BSD](http://klaver.it/bsd/sysctl.conf)

  - [Sysctl.conf example for Linux](http://klaver.it/linux/sysctl.conf)

[분류:BSD](https://ko.wikipedia.org/wiki/분류:BSD "wikilink") [분류:리눅스](https://ko.wikipedia.org/wiki/분류:리눅스 "wikilink") [분류:유닉스](https://ko.wikipedia.org/wiki/분류:유닉스 "wikilink") [분류:OpenBSD](https://ko.wikipedia.org/wiki/분류:OpenBSD "wikilink") [분류:FreeBSD](https://ko.wikipedia.org/wiki/분류:FreeBSD "wikilink")

1.