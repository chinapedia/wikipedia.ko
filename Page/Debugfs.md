> This article is converted from Wikipedia: [Debugfs](https://ko.wikipedia.org/wiki/Debugfs).


**debugfs**는 버전 2.6.10-rc 부터 [리눅스 커널에서](../Page/리눅스_커널.md "wikilink") 사용되는 특별한 파일 시스템이다.\[1\] 이것은 Greg Kroah-Hartman에 의해 만들어졌다.\[2\]

debugfs는 디버깅 목적으로 특별히 설계된 쉽게 사용 가능한 램 기반 파일 시스템이다. 이것은 커널 개발자들이 사용자 공간에서 정보를 활용 가능하게 해주는 것을 편하게 하기 위해 존재한다.\[3\] 단지 프로세스에 대한 정보를 제공하는 목적을 가진 /proc이나, 파일 당 엄격한 한 값을 규칙으로 갖는 [sysfs](https://ko.wikipedia.org/wiki/sysfs "wikilink")와 달리 이것은 규칙이 존재하지 않는다. 개발자들은 자신이 원하는 아무 정보를 여기에 넣을 수 있다.\[4\]

## 사용

debugfs 기능을 사용해서 리눅스 커널을 컴파일하기 위해서는, CONFIG_DEBUG_FS 옵션이 yes로 설정되어야 한다. 이것은 일반적으로 /sys/kernel/debug 에 다음과 같은 명령어로 마운트된다:\[5\]

```
```

이것은 다음을 포함하는 C 헤더 파일 linux/debugfs.h의 여러 호출들을 사용함으로써 조작 가능하다:

  - debugfs_create_file - 디버그 파일 시스템에서 파일을 생성하기 위한.
  - debugfs_create_dir - 디버그 파일 시스템에서 디렉토리를 생성하기 위한.
  - debugfs_create_symlink - 디버그 파일 시스템에서 심볼릭 링크를 생성하기 위한.
  - debugfs_remove - 디버그 파일 시스템에서 debugfs 엔트리를 제거하기 위한.

## 각주

## 외부 링크

  - [A basic introduction to debugfs](https://web.archive.org/web/20160105144119/http://people.ee.ethz.ch/~arkeller/linux/kernel_user_space_howto.html#ss2.5)
  - [An updated guide to debugfs at](http://lwn.net/Articles/334546/) [LWN](../Page/LWN.net.md "wikilink")

[분류:리눅스 커널](https://ko.wikipedia.org/wiki/분류:리눅스_커널 "wikilink") [분류:리눅스 커널 특징](https://ko.wikipedia.org/wiki/분류:리눅스_커널_특징 "wikilink")

1.  [Linux: DebugFS](http://kerneltrap.org/node/4394) , by Jeremy, December 11, 2004, KernelTrap.
2.
3.  [Linux Kernel Documentation :: filesystems : debugfs.txt](http://www.mjmwired.net/kernel/Documentation/filesystems/debugfs.txt) documentation from the source code (Based on kernel version 2.6.35.4.
4.  [An updated guide to debugfs](http://lwn.net/Articles/334546/), By Jonathan Corbet, May 25, 2009, LWN
5.  [2.5 Debugfs](http://people.ee.ethz.ch/~arkeller/linux/kernel_user_space_howto.html#ss2.5)  A guide to using debugfs, Ariane Keller, Version 0.8, July 2008, Kernel Space - User Space Interfaces