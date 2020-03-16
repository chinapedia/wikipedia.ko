> This article is converted from Wikipedia: [Modprobe](https://ko.wikipedia.org/wiki/Modprobe).


**`modprobe`** 는 [리눅스](../Page/리눅스.md "wikilink") 프로그램으로서 [적재 가능 커널 모듈](../Page/적재_가능_커널_모듈.md "wikilink")(LKM)을 [리눅스 커널에](../Page/리눅스_커널.md "wikilink") 추가하거나 커널로부터 제거하는데 사용된다. 이것은 일반적으로 간접적으로 사용된다: udev는 자동적으로 탐지된 하드웨어를 위한 드라이버를 로드하기 위해 modprobe에 의존한다.

2014년 부터 modprobe는 소프트웨어 패키지 "kmod"의 한 부분으로 배포된다.\[1\] 이것은 이전에 다음과 같이 개발되었다:

  - 리눅스 커널 버전 2.6과 그 이후를 위한 "module-init-tools"\[2\]
  - 리눅스 버전 2.2.x와 2.4.x에서 사용되는 "modutils"\[3\]

## 동작

`modprobe` 프로그램은 다음과 같은 이점들을 통해서 더 기본적인 유틸리티들인 **insmod**와 **rmmod** 보다 더 완전한 다용도 적인 특징을 갖는다:

  - 어떤 모듈이 로드되어야 할지에 관한 직관적인 결정을 제공하는 능력
  - 모듈을 로드하기 위해 언제 요청되어야 할지와 어떤 먼저 요구되는 모듈을 추가할지 같은 모듈 의존성에 대한 인식
  - 요구되는 재귀적 모듈 의존성의 해법

기본적으로 modprobe는 모듈을 커널에 추가/삽입/설치한다. 이 변경을 위해서 일반적으로 루트 권한이 요구된다.

모듈 이름 뒤에 나오는 모든 인자는 커널에 전달된다(설정 파일에 열거된 옵션들 뿐만 아니라).

몇몇 버전의 modprobe에서 설정 파일은 modprobe.conf이며 다른 버전에서는 /etc/modprobe.d 디렉토리에서 <modulename>으로 불리는 파일들의 집합이기도 하다.

## 특징

*modprobe* 프로그램은 또한 다른 비슷한 유틸리티들 보다 더 많은 설정 특징들을 갖는다. 모듈들의 자동 로딩을 위해 모듈 aliases를 정의할 수 있다. 커널이 모듈을 요구할 때 이것은 실제로 요청하기 위해 modprobe를 실행한다; 그러나 커널은 단지 몇몇 모듈 속성들의 설명만 갖고 modprobe가 aliases를 통해 실제 모듈 이름으로 변환하는 작업을 수행한다.

이 프로그램은 또한 주어진 모듈을 로딩 또는 언로딩하기 전이나 후에 프로그램을 실행할 수 있는 능력을 갖는다; 예를 들면 사운드 카드 모듈을 로딩한 후에 믹서를 설정하는 것. 비록 이러한 행동들은 반드시 외부 프로그램들에 의해서 구현되어야 하지만 modprobe는 그들의 실행을 모듈의 로딩/언로딩을 통해 동기화할 수 있다.

## 블랙리스트

두개 또는 그 이상의 모듈들이 같은 장치를 지원하는 경우가 있을 수 있다; 블랙리스트 키워드는 특정한 모듈의 내부 aliases 모두가 무시되게 지정할 수 있다.\[4\]

Modeprobe를 사용해서 모듈을 블랙리스트에 넣는 두 가지 방식이 존재하는데 첫번째는 /etc/modprobe.d/blacklist에 존재하는 블랙리스팅 시스템을 사용하는 것이다.

`cat /etc/modprobe.d/blacklist`
`blacklist ieee1394`
`blacklist ohci1394`
`blacklist eth1394`
`blacklist sbp2`

install은 설정 파일에서 가장 높은 우선순위를 가지며 위의 blacklist 대신 사용된다.

`cat /etc/modprobe.d/ieee1394`
`install ieee1394 /bin/true`
`install ohci1394 /bin/true`
`install eth1394 /bin/true`
`install sbp2 /bin/true`

그 대신에 /etc/modprobe.conf를 변경할 수도 있다:

`alias sub_module /dev/null`
`alias module_main /dev/null`
`options module_main needed_option=0`

## 같이 보기

  - [lsmod](https://ko.wikipedia.org/wiki/lsmod "wikilink")

## 각주

## 외부 링크

  - [modprobe man page](http://linux.die.net/man/8/modprobe).
  - [modprobe.conf](http://linux.die.net/man/5/modprobe.conf)
  - [modules.dep](http://linux.die.net/man/5/modules.dep)

[분류:리눅스 커널 관련 소프트웨어](https://ko.wikipedia.org/wiki/분류:리눅스_커널_관련_소프트웨어 "wikilink")

1.  <http://git.kernel.org/cgit/utils/kernel/kmod/kmod.git>
2.
3.
4.  [modprobe.conf(5) - Linux man page](http://linux.die.net/man/5/modprobe.conf)