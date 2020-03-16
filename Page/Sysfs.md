> This article is converted from Wikipedia: [Sysfs](https://ko.wikipedia.org/wiki/Sysfs).


**sysfs**는 [리눅스 커널이](../Page/리눅스_커널.md "wikilink") 제공하는 [가상 파일 시스템의](https://ko.wikipedia.org/wiki/가상_파일_시스템 "wikilink") 하나로서, [가상 파일을](https://ko.wikipedia.org/wiki/가상_파일 "wikilink") 통해 다양한 커널 하위 시스템, 하드웨어 장치, 또 커널 장치 모델에서 [사용자 공간에](../Page/사용자_공간.md "wikilink") 이르는 관련 [장치 드라이버에](../Page/장치_드라이버.md "wikilink") 대한 정보를 내보낸다. 다양한 장치와 커널 하위 시스템의 정보를 제공하는 일뿐 아니라, 내보낸 가상 파일들은 이들의 구성에도 사용된다.

sysfs는 [BSD](../Page/BSD.md "wikilink") [운영 체제에서](../Page/운영_체제.md "wikilink") 볼 수 있는 [sysctl](https://ko.wikipedia.org/wiki/sysctl "wikilink") 구조와 비슷한 기능을 제공하며, 차이점으로는 sysfs가 목적에 따라 만들어진 커널 매커니즘이 아닌 가상 파일 시스템으로 구현되어 있다는 것이다.

## 역사

버전 2.5 개발 중 리눅스 드라이버 모델이 도입되면서 버전 2.4의 단점 몇 가지를 수정하였다:

  - 통일된 방식으로 표현되는 드라이버 장치 관계가 존재하지 않았다.
  - 포괄적인 [핫플러그](https://ko.wikipedia.org/wiki/핫_스와핑 "wikilink") 구조가 없었다.
  - [procfs](https://ko.wikipedia.org/wiki/procfs "wikilink")에 프로세스와 무관한 너무 많은 정보가 포함되어 있었다.

sysfs는 [장치 트리에](https://ko.wikipedia.org/wiki/장치_트리 "wikilink") 표현되는 정보를 내보낼 목적으로 설계되었으며 더 이상 procfs에 과도한 정보를 포함하지 않는다. 패트릭 모첼(Patrick Mochel)이 작성하였다.\[1\]\[2\] 나중에 마니시 소니(Maneesh Soni)가 대형 시스템에서 메모리 사용량을 줄이기 위해 sysfs 보조 기억 패치를 작성하였다.

버전 2.5 개발의 이듬해에 드라이버 모델과, 과거에는 ddfs로 불리던 driverfs의 하부 구조적 기능들이 다른 하위 시스템에도 유용하다는 것이 입증되기 시작하였다.\[3\]\[4\] 중점적인 오브젝트 구조를 제공하기 위해 [kobjects](https://ko.wikipedia.org/wiki/kobjects "wikilink")가 개발되었으며 하위 시스템의 본질을 다 이해하는 것은 불가능하다는 것을 표현하기 위해 driverfs는 sysfs로 이름이 바뀌었다.

sysfs는 `/sys`라는 마운트 지점 아래에 마운트된다.

## 지원 버스

  - PCI
    [PCI](../Page/PCI_버스.md "wikilink") 장치의 정보를 내보낸다.
  - USB
    [USB](../Page/USB.md "wikilink") 장치와 USB 호스트를 둘 다 포함한다.
  - S/390 버스
    [S/390](https://ko.wikipedia.org/wiki/S/390 "wikilink") 구조는 어느 곳에서도 볼 수 없는 장치를 포함하고 있어서 특수 버스가 만들어졌다:
      - *css*: 하위 채널들을 포함한다. (현재 제공되는 유일한 드라이버는 입출력 하위 채널을 위해 존재함)
      - *ccw*: 채널 부착 장치들을 포함한다. ([CCW](https://ko.wikipedia.org/wiki/채널_커맨드_워드 "wikilink"))로 구동)
      - *ccwgroup*: 사용자가 만들어 ccw 장치를 이루는 인공 장치들. 2.4 chandev 기능 일부를 대체한다.
      - *iucv*: VM의 [IUCV](https://ko.wikipedia.org/wiki/IUCV "wikilink") 인터페이스를 사용하는 netiucv 장치와 같은 인공 장치들.

## sysfs와 사용자 공간

sysfs는 여러 유틸리티들이 하드웨어 및 이에 연결되는 드라이버([커널 모듈](../Page/적재_가능_커널_모듈.md "wikilink"), 예를 들어 [udev](https://ko.wikipedia.org/wiki/udev "wikilink")나 [HAL](https://ko.wikipedia.org/wiki/HAL_\(소프트웨어\) "wikilink"))의 정보에 접근하는데 쓰인다. 과거에 [procfs](https://ko.wikipedia.org/wiki/procfs "wikilink")를 통해 수집된 정보에 접근하기 위해 스크립트가 작성되며 일부 스크립트들은 장치 드라이버와 장치를 이들의 속성을 통해 구성한다.

## 같이 보기

  - [tmpfs](https://ko.wikipedia.org/wiki/tmpfs "wikilink")

## 각주

<references />

## 외부 링크

  - [Driver model overview from the LWN porting to 2.6 series](http://lwn.net/Articles/31185/)

  - [kobjects and sysfs from the LWN porting to 2.6 series](http://lwn.net/Articles/54651/)

  - [Ramfs](http://wiki.debian.org/ramfs)

  - [The sysfs Filesystem, OLS'05](http://www.kernel.org/pub/linux/kernel/people/mochel/doc/papers/ols-2005/mochel.pdf)

  - [Documentation/filesystems/sysfs.txt](http://kernel.org/doc/Documentation/filesystems/sysfs.txt) Linux kernel documentation for sysfs

[분류:리눅스 커널 특징](https://ko.wikipedia.org/wiki/분류:리눅스_커널_특징 "wikilink") [분류:리눅스 커널의 인터페이스](https://ko.wikipedia.org/wiki/분류:리눅스_커널의_인터페이스 "wikilink") [분류:파일 시스템](https://ko.wikipedia.org/wiki/분류:파일_시스템 "wikilink")

1.
2.
3.
4.