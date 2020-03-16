> This article is converted from Wikipedia: [GRUB](https://ko.wikipedia.org/wiki/GRUB).


[섬네일로](https://ko.wikipedia.org/wiki/파일:GNU_GRUB_on_MBR_partitioned_hard_disk_drives.svg "wikilink") 파티션된 하드 디스크 드라이브의 GNU GRUB\]\] [섬네일로](https://ko.wikipedia.org/wiki/파일:GNU_GRUB_on_GPT_partitioned_hard_disk_drives.svg "wikilink") 파티션된 하드 디스크 드라이브의 GNU GRUB\]\] [섬네일](https://ko.wikipedia.org/wiki/파일:GNU_GRUB_components.svg "wikilink") (섹터 0)에 기록된다. `core.img`는 가능하면 MBR과 첫 파티션 사이의 빈 섹터들에 기록된다. (전통적인 이유로 첫 파티션은 섹터 1이 아닌, 섹터 63에서 시작하지만 필수 사항은 아니다). `/boot/grub`-directory는 별도의 파티션이나 /-partition에 위치할 수 있다.\]\]

[섬네일](https://ko.wikipedia.org/wiki/파일:StartUp-Manager.png "wikilink")\]\] **GNU GRUB**(대개 GRUB)은 [GNU](../Page/GNU.md "wikilink") 프로젝트의 [부트로더](https://ko.wikipedia.org/wiki/부트로더 "wikilink")이다. 대부분 운영 체제의 커널을 불러올 수 있으며, 인자를 넘겨 줄 수도 있다. GNU GRUB의 이전 이름은 **GRand Unified Bootloader**이었고 이는 [대통일 이론의](../Page/대통일_이론.md "wikilink") 영문 이름의 패러디이다. 대부분 [리눅스 배포판에서](../Page/리눅스_배포판.md "wikilink") 부트로더로 사용한다.

대부분 사용되는 GRUB은 "GRUB Legacy"로 분류된다. 현재의 버전은 기능 추가 대신 버그 수정이 이뤄지고 있다. 현재는 [GRUB 2](https://ko.wikipedia.org/wiki/GRUB_2 "wikilink") 개발에 집중하고 있으며 이는 [PUPA](https://ko.wikipedia.org/wiki/PUPA "wikilink") 프로젝트의 코드를 기반으로 한다.

## 기능

  - 동적으로 설정 가능하다. 심지어 부팅 시간에도 커널의 인자를 조정할 수 있다.
  - [Bash](https://ko.wikipedia.org/wiki/Bash "wikilink")와 같은 명령줄 인터페이스가 있다.
  - 사용자 정의 부팅 기능
  - [파일 시스템](../Page/파일_시스템.md "wikilink") 직접 접근 기능
  - 다양한 실행 [파일 형식](https://ko.wikipedia.org/wiki/파일_형식 "wikilink") 지원
  - 비 [멀티부팅](https://ko.wikipedia.org/wiki/멀티부팅 "wikilink") 운영 체제 지원
  - 사람이 읽을 수 있는 설정 파일 제공
  - 메뉴 인터페이스
      - 그래픽 메뉴 및 배경 그림도 사용할 수 있다.
      - 비 [GUI](https://ko.wikipedia.org/wiki/GUI "wikilink") 인터페이스도 쓸 수 있다.
  - 다양한 파일 시스템 지원
  - 자동으로 압축 해제 지원
  - 지오메트리 정보 독립
  - 모든 [RAM을](../Page/랜덤_액세스_메모리.md "wikilink") [바이오스](../Page/바이오스.md "wikilink")와 관계없이 인식
  - [LBA](../Page/논리_블록_주소_지정.md "wikilink") 및 [네트워크](https://ko.wikipedia.org/wiki/통신_네트워크 "wikilink") 지원
  - 디스크 없는 시스템 지원

## 설치

GRUB은 [LILO](../Page/LILO.md "wikilink")와 달리 설정 변경 후에 재설치가 필요 없다. GRUB은 스테이지 단위로 부팅 과정이 구성되어 있으며, GRUB의 스테이지 1은 MBR에 존재한다. GRUB 설정 파일은 대개 스테이지 2에서 불리며 이들은 GRUB이 읽을 수 있는 파티션에 존재한다. 만약 설정 파일이 없으면 명령줄로 간다. 이들 설정 파일은 /boot/grub에 있으며 배포판마다 파일 이름이 다르다. 이러한 구조 때문에 GRUB 설정 파일이 있던 파티션만 지웠다면 평소 보던 메뉴가 사라지므로, 초보자들은 부팅이 되지 않는다는 것으로 착각할 수 있다.

[CD](../Page/콤팩트_디스크.md "wikilink"), [DVD](../Page/DVD.md "wikilink") 같은 다양한 장치에서의 부팅도 지원한다.

## 지원하는 파일 시스템

이 자료는 2005년 현재 자료이다.

  - [ext2](https://ko.wikipedia.org/wiki/ext2 "wikilink")/[ext3](https://ko.wikipedia.org/wiki/ext3 "wikilink")/[ext4](https://ko.wikipedia.org/wiki/ext4 "wikilink")
  - [IBM](../Page/IBM.md "wikilink") [JFS](https://ko.wikipedia.org/wiki/JFS "wikilink")
  - [ISO 9660](../Page/ISO_9660.md "wikilink")
  - [미닉스 파일 시스템](https://ko.wikipedia.org/wiki/미닉스_파일_시스템 "wikilink")
  - [ReiserFS](../Page/ReiserFS.md "wikilink")
  - [SGI](https://ko.wikipedia.org/wiki/실리콘_그래픽스_사 "wikilink") [XFS](../Page/XFS.md "wikilink")
  - [UFS](../Page/유닉스_파일_시스템.md "wikilink")/[UFS2](https://ko.wikipedia.org/wiki/UFS2 "wikilink")
  - [FAT](../Page/파일_할당_테이블.md "wikilink") 계열 파일시스템
  - [NTFS](../Page/NTFS.md "wikilink")

## 지원하는 운영 체제

[300px나](https://ko.wikipedia.org/wiki/파일:Gnu_grub_config_file.png "wikilink") [우분투를](../Page/우분투_\(운영_체제\).md "wikilink") 불러올 수 있게 한다.\]\]

  - 임의의 멀티부팅 가능한 커널
  - [FreeBSD](../Page/FreeBSD.md "wikilink")
  - [NetBSD](../Page/NetBSD.md "wikilink")
  - [OpenBSD](../Page/OpenBSD.md "wikilink")
  - [리눅스](../Page/리눅스.md "wikilink")

[체인 로딩](https://ko.wikipedia.org/wiki/체인_로딩 "wikilink") 기능을 쓰면 [마이크로소프트 윈도같은](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 상용 운영 체제도 불러올 수 있다.

## 같이 보기

  - [Loadlin](../Page/Loadlin.md "wikilink")
  - [RAID](../Page/RAID.md "wikilink")
  - [LVM](../Page/논리_볼륨_관리자.md "wikilink")

## 각주

## 외부 링크

  - [GNU GRUB 웹사이트](http://www.gnu.org/software/grub/)
  - [GRUB 설명서](http://www.gnu.org/software/grub/manual/html_node/)
  - [An introductory tutorial](http://www.linuxjournal.com/article/4622)
  - [GRUB development wiki](https://web.archive.org/web/20060828195659/http://grub.enbug.org/)
  - [Booting with GRUB](https://web.archive.org/web/20070210091856/http://www.osdcom.info/content/view/33/39/)
  - [Linux+Win9x+Grub HowTo](http://tldp.org/HOWTO/Linux+Win9x+Grub-HOWTO/index.html)
  - [Win32 GRUB](https://web.archive.org/web/20060820164047/http://www.skyjammer.com/files/knoppix/)
  - [WinGRUB](http://grub4dos.sourceforge.net/)
  - [GRUB Installer for Windows](https://web.archive.org/web/20050414003836/http://www.geocities.com/lode_leroy/grubinstall/)
  - [GRUB for DOS](https://web.archive.org/web/20070928090753/http://grub.linuxeden.com/) - Bridging DOS/Windows to Unix/Linux
  - [Grub from the Ground Up](http://www.troubleshooters.com/linux/grub/grub.htm) - gathering required information, configuring, troubleshooting
  - [Freshmeat project page](http://freshmeat.net/projects/gnugrub/)

[분류:시스템 소프트웨어](https://ko.wikipedia.org/wiki/분류:시스템_소프트웨어 "wikilink") [분류:부트 로더](https://ko.wikipedia.org/wiki/분류:부트_로더 "wikilink") [GRUB](https://ko.wikipedia.org/wiki/분류:GNU_프로젝트_소프트웨어 "wikilink") [분류:C로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C로_작성된_자유_소프트웨어 "wikilink")