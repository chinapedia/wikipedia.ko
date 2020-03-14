> This article is converted from Wikipedia: [Kernfs](https://ko.wikipedia.org/wiki/Kernfs).


[리눅스 커널에서](https://ko.wikipedia.org/wiki/리눅스_커널 "wikilink"), **kernfs**는 내부적으로 다양한 커널 서브시스템에서 사용되는 가상 파일 시스템을 생성하기 위해 요청되는 기능들을 포함하는 함수들의 집합이다. Kernfs의 생성은 sysfs에 의해 사용되는 내부 로직의 한 부분에 의한 것으로서, 하드웨어 장치들과 커널의 디바이스 모델에서 부터 사용자 공간 까지 관련된 [장치 드라이버들에](https://ko.wikipedia.org/wiki/장치_드라이버 "wikilink") 대한 정보를 독립적이고 재사용 가능한 기능에 익스포팅함으로써 가상 파일들의 집합을 제공한다. 그럼으로써 다른 커널 서브시스템들이 자신의 가상 파일 시스템을 더 쉽고 일관적으로 구현할 수 있다.\[1\]\[2\]\[3\]

관련된 패치는 리눅스 커널 버전 3.14에서 합병되었다.\[4\]\[5\] Kernfs의 주요 사용자 중 하나는 cgroups에 의해 내부적으로 사용되는 가상 파일 시스템으로서 이것의 재설계는 리눅스 커널 버전 3.15에서 계속되었다.\[6\]

## 같이 보기

  - [procfs](https://ko.wikipedia.org/wiki/procfs "wikilink") - 유닉스 계열 운영 체제에서 특별한 파일 시스템으로써 프로세스들과 다른 시스템 정보에 대한 정보를 보여준다.
  - [tmpfs](https://ko.wikipedia.org/wiki/tmpfs "wikilink") - 많은 유닉스 계열 운영 체제들에서 임시 파일 저장 시설을 위한 일반적인 이름.

## 각주

## 외부 링크

  - [Source code](https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/tree/fs/kernfs), fs/kernfs within the Linux kernel source tree

[분류:리눅스 커널의 인터페이스](https://ko.wikipedia.org/wiki/분류:리눅스_커널의_인터페이스 "wikilink")

1.
2.
3.
4.
5.
6.