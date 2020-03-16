> This article is converted from Wikipedia: [Util-linux](https://ko.wikipedia.org/wiki/Util-linux).


**util-linux**는 [리눅스](../Page/리눅스.md "wikilink") [운영 체제의](../Page/운영_체제.md "wikilink") 표준 패키지이다. 차세대를 뜻하는 ng라는 용어가 포함된 util-linux-ng라는 [포크는](../Page/포크_\(소프트웨어_개발\).md "wikilink") 개발이 중단되었을 때 만들어졌으나\[1\] 2011년 1월에 util-linux로 이름이 바뀌었고 현재는 패키지의 공식 버전이다.\[2\]

## 내용물

다음의 유틸리티를 포함한다:

  - addpart
  - [agetty](https://ko.wikipedia.org/wiki/getty_\(유닉스\) "wikilink")
  - [blkdiscard](http://man7.org/linux/man-pages/man8/blkdiscard.8.html)
  - blkid
  - blockdev
  - [cal](https://ko.wikipedia.org/wiki/cal "wikilink")
  - [cfdisk](https://ko.wikipedia.org/wiki/cfdisk "wikilink")
  - chcpu
  - chfn
  - chrt
  - [chsh](https://ko.wikipedia.org/wiki/chsh "wikilink")
  - col (레거시)\[3\]
  - colcrt
  - colrm
  - column
  - ctrlaltdel
  - delpart
  - [dmesg](https://ko.wikipedia.org/wiki/dmesg "wikilink")
  - eject
  - fallocate
  - [fdformat](https://ko.wikipedia.org/wiki/fdformat "wikilink")
  - [fdisk](https://ko.wikipedia.org/wiki/fdisk "wikilink")
  - findfs
  - findmnt
  - [flock](https://ko.wikipedia.org/wiki/File_locking "wikilink")
  - [fsck](https://ko.wikipedia.org/wiki/fsck "wikilink")
  - [fsck](https://ko.wikipedia.org/wiki/fsck "wikilink").[cramfs](https://ko.wikipedia.org/wiki/cramfs "wikilink")
  - [fsck](https://ko.wikipedia.org/wiki/fsck "wikilink").[minix](https://ko.wikipedia.org/wiki/MINIX_file_system "wikilink")
  - fsfreeze
  - [fstab](https://ko.wikipedia.org/wiki/fstab "wikilink")
  - fstrim
  - [getopt](https://ko.wikipedia.org/wiki/getopt "wikilink")
  - [hexdump](https://ko.wikipedia.org/wiki/Hex_dump#od_and_hexdump "wikilink")
  - hwclock (하드웨어 클럭 (RTC) 조회 및 설정)
  - [ionice](https://ko.wikipedia.org/wiki/ionice "wikilink")
  - ipcmk
  - [ipcrm](https://ko.wikipedia.org/wiki/ipcrm "wikilink")
  - [ipcs](https://ko.wikipedia.org/wiki/ipcs "wikilink")
  - isosize
  - [kill](https://ko.wikipedia.org/wiki/kill "wikilink")
  - last
  - ldattach
  - line (레거시)\[4\]
  - logger
  - login
  - look
  - [losetup](https://ko.wikipedia.org/wiki/losetup "wikilink")
  - lsblk
  - lscpu\[5\]
  - lslocks
  - lslogins
  - mcookie
  - [mesg](https://ko.wikipedia.org/wiki/mesg "wikilink")
  - [mkfs](https://ko.wikipedia.org/wiki/mkfs "wikilink") (레거시)\[6\]
  - [mkfs](https://ko.wikipedia.org/wiki/mkfs "wikilink").[bfs](https://ko.wikipedia.org/wiki/Boot_File_System "wikilink")
  - [mkfs](https://ko.wikipedia.org/wiki/mkfs "wikilink").[cramfs](https://ko.wikipedia.org/wiki/cramfs "wikilink")
  - [mkfs](https://ko.wikipedia.org/wiki/mkfs "wikilink").[minix](https://ko.wikipedia.org/wiki/MINIX "wikilink")
  - mkswap
  - [more](https://ko.wikipedia.org/wiki/more "wikilink")
  - [mount](https://ko.wikipedia.org/wiki/mount_\(유닉스\) "wikilink")
  - mountpoint
  - namei
  - newgrp
  - nologin
  - nsenter
  - partx
  - pg (레거시)\[7\]
  - pivot_root
  - prlimit<ref>

</ref>

  - raw
  - readprofile
  - rename
  - [renice](https://ko.wikipedia.org/wiki/nice "wikilink")
  - reset (레거시)\[8\]
  - resizepart
  - rev
  - rtcwake
  - runuser
  - [script](https://ko.wikipedia.org/wiki/script "wikilink")
  - scriptreplay
  - setarch (i386, linux32, linux64, x86_64 등의 아키텍처 심볼릭 링크 포함)
  - setpriv
  - setsid
  - setterm
  - sfdisk
  - su
  - sulogin
  - swaplabel
  - swapoff
  - swapon
  - switch_root
  - tailf (레거시)\[9\]
  - taskset
  - tunelp (deprecated)\[10\]
  - ul
  - umount
  - unshare
  - utmpdump
  - uuidd
  - uuidgen
  - [vipw](https://ko.wikipedia.org/wiki/vipw "wikilink") (vigr의 심볼릭 링크 포함)
  - wall
  - wdctl
  - [whereis](https://ko.wikipedia.org/wiki/whereis "wikilink")
  - wipefs
  - [write](https://ko.wikipedia.org/wiki/write "wikilink")
  - zramctl

아래의 유틸리티들은 과거에 포함되었으나 2015년 7월 1일 기준으로 제거되어 있다:

  - arch\[11\]
  - chkdupexe\[12\]
  - clock\[13\]
  - cytune\[14\]
  - [ddate](https://ko.wikipedia.org/wiki/ddate "wikilink") (기본 빌드에서 먼저 제거됨.\[15\] - 함께 제거되기 이전에\[16\])
  - elvtune\[17\]
  - fastboot\[18\]
  - fasthalt\[19\]
  - halt\[20\]
  - initctl\[21\]
  - ramsize (과거에는 rdev의 심볼릭 링크였음)\[22\]
  - rdev\[23\]
  - reboot\[24\]
  - rootflags (과거에는 rdev의 심볼릭 링크였음)\[25\]
  - shutdown\[26\]
  - simpleinit\[27\]
  - vidmode (과거에는 rdev의 심볼릭 링크였음)\[28\]

## 각주

<references />

## 외부 링크

  - [The util-linux code repository.](https://git.kernel.org/cgit/utils/util-linux/util-linux.git/)

  - [pub/linux/utils/util-linux](https://www.kernel.org/pub/linux/utils/util-linux/) - [Kernel.org](https://ko.wikipedia.org/wiki/Kernel.org "wikilink")

  - [util-linux development discussion and bug reporting mailing list](http://vger.kernel.org/vger-lists.html#util-linux)

  - [Karel Zak's blog](http://karelzak.blogspot.com/), the current maintainer.

[분류:리눅스](https://ko.wikipedia.org/wiki/분류:리눅스 "wikilink") [분류:C로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C로_작성된_자유_소프트웨어 "wikilink")

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
11.
12.
13.
14.
15.
16.
17.
18.
19.
20.
21.
22.
23.
24.
25.
26.
27.
28.