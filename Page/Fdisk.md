> This article is converted from Wikipedia: [Fdisk](https://ko.wikipedia.org/wiki/Fdisk).


컴퓨터 [파일 시스템에서](https://ko.wikipedia.org/wiki/파일_시스템 "wikilink") **fdisk**는 [디스크 파티션](https://ko.wikipedia.org/wiki/디스크_파티션 "wikilink") 기능을 제공하는 [명령 줄 인터페이스](https://ko.wikipedia.org/wiki/명령_줄_인터페이스 "wikilink") 유틸리티이다. [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink") 및 [유닉스 계열에서는](https://ko.wikipedia.org/wiki/유닉스_계열 "wikilink") 시스템용으로 존재하며 [윈도우 2000](https://ko.wikipedia.org/wiki/윈도우_2000 "wikilink") 이상의 [윈도우 NT](https://ko.wikipedia.org/wiki/윈도우_NT "wikilink") 운영 체제 계열 버전에서 fdisk는 [diskpart](https://ko.wikipedia.org/wiki/diskpart "wikilink")라는 이름의 더 진보된 도구로 대체되었다. [리눅스환경에서의 fdisk 실행화면](https://ko.wikipedia.org/wiki/파일:Fdisk_supports_maximum_60_partitions_in_Linux_at_2018.jpg "wikilink")

## 구현

### DOS 및 윈도우

[IBM](https://ko.wikipedia.org/wiki/IBM "wikilink")은 [하드 디스크 드라이브에](https://ko.wikipedia.org/wiki/하드_디스크_드라이브 "wikilink") 데이터를 저장한 최초의 PC인 [IBM PC XT의](../Page/IBM_PC_XT.md "wikilink") 1983년 3월 릴리스, 그리고 [IBM PC-DOS](https://ko.wikipedia.org/wiki/PC-DOS "wikilink") 버전 2.0과 더불어 fdisk, 즉 Fixed Disk Setup Program 버전 1.00을 선보였다. 버전 1은 하나의 [FAT](https://ko.wikipedia.org/wiki/파일_할당_테이블 "wikilink") 도스 파티션을 만들고 삭제하고 [활성화 파티션을](https://ko.wikipedia.org/wiki/활성화_파티션 "wikilink") 변경하고 파티션 데이터를 표시할 수만 있었다. fdisk는 [마스터 부트 레코드](https://ko.wikipedia.org/wiki/마스터_부트_레코드 "wikilink")(MBR)을 기록하며 최대 4개의 파티션을 지원했다. 다른 3개는 [CP/M-86](https://ko.wikipedia.org/wiki/CP/M-86 "wikilink"), [제닉스](https://ko.wikipedia.org/wiki/제닉스 "wikilink")와 같은 다른 운영 체제용으로 고안되었으며 fdisk가 지원하지 않았던 자체만의 파티셔닝 유틸리티를 가지고 있는 것으로 예측되었다.

1984년 8월, PC DOS 3.0은 [파일 할당 테이블](https://ko.wikipedia.org/wiki/파일_할당_테이블 "wikilink") 파티션을 추가하여 더 큰 용량의 하드 디스크를 더 효율적으로 지원한다.

1987년 4월, PC DOS/fdisk 3.30은 [확장 파티션의](https://ko.wikipedia.org/wiki/디스크_파티션 "wikilink") 지우너을 추가하였으며 최대 23개의 논리 드라이브나 [볼륨을](../Page/볼륨_\(컴퓨팅\).md "wikilink") 보유할 수 있었다.

[파일 할당 테이블](https://ko.wikipedia.org/wiki/파일_할당_테이블 "wikilink") 지원은 컴팩 MS-DOS 3.31과 함께 추가되었으며 나중에 [MS-DOS](https://ko.wikipedia.org/wiki/MS-DOS "wikilink")/PC DOS 4.0과 함께 이용이 가능해졌다.

오리지널 [윈도우 95과](https://ko.wikipedia.org/wiki/윈도우_95 "wikilink") 함께 출시된 fdisk 프로그램을 포함하는 대부분의 [도스](https://ko.wikipedia.org/wiki/도스 "wikilink") fdisk 프로그램들은 오직 FAT12, FAT16, FAT16B [FAT](https://ko.wikipedia.org/wiki/파일_할당_테이블 "wikilink") 파티션을 생성할 수만 있다.

[MS-DOS](https://ko.wikipedia.org/wiki/MS-DOS "wikilink") fdisk 파생판들은 윈도우 95, [윈도우 98](https://ko.wikipedia.org/wiki/윈도우_98 "wikilink"), 나중에는 [윈도우 미와](https://ko.wikipedia.org/wiki/윈도우_미 "wikilink") 함께 제공되었다. 윈도우 95B 이상에 포함된 fdisk 버전만이 [FAT](https://ko.wikipedia.org/wiki/파일_할당_테이블 "wikilink") 파티션을 조작할 수 있다.\[1\] [윈도우 2000](https://ko.wikipedia.org/wiki/윈도우_2000 "wikilink") 이상은 fdisk를 사용하지 않으며 [DiskPart](https://ko.wikipedia.org/wiki/DiskPart "wikilink") 외에 [논리 디스크 관리자](https://ko.wikipedia.org/wiki/논리_디스크_관리자 "wikilink") 기능이 포함되어 있다.

윈도우 95에 제공되는 fdisk는 64 GB 이상의 하드 디스크에 대해 정확한 크기를 보고하지 않는다. 이를 수정한 업데이트된 fdisk는 마이크로소프트로부터 이용이 가능하다..\[2\]

### 프리도스

[프리도스](https://ko.wikipedia.org/wiki/프리도스 "wikilink")의 fdisk 구현체는 [자유 소프트웨어이다](https://ko.wikipedia.org/wiki/자유_소프트웨어 "wikilink").

### OS/2

[OS/2](https://ko.wikipedia.org/wiki/OS/2 "wikilink")는 버전 4.0까지 2개의 파티션 테이블 매니저가 포함되었다. 이들은 [텍스트 모드](https://ko.wikipedia.org/wiki/텍스트_모드 "wikilink") fdisk, [GUI](https://ko.wikipedia.org/wiki/그래픽_사용자_인터페이스 "wikilink") 기반 fdiskpm이었다. 이 둘은 기능상 동일하며 FAT 파티션과 더 진보된 [HPFS](../Page/HPFS.md "wikilink") 파티션을 조작할 수 있다.

OS/2 버전 4.5 이상([eComStation](https://ko.wikipedia.org/wiki/eComStation "wikilink") 포함)은 JFS 파일 시스템 및 FAT, HPFS를 사용할 수 있으며 fdisk는 [논리 볼륨 관리자](../Page/논리_볼륨_관리자.md "wikilink")(LVM)로 대체된다.

### PC DOS 7.10

[IBM PC DOS 7.10은](https://ko.wikipedia.org/wiki/PC-DOS "wikilink") FDISK32, FORMAT32 유틸리티를 포함했다.

## LVM 및 리눅스

리눅스에서 사용되는 fdisk 명령어는 디스크 파티션을 기본적인 설정에서부터 세밀하고 부가적인 기능을 설정할수있게 도와주는 명령어이다. [LVM에](../Page/논리_볼륨_관리자.md "wikilink") 대한 설정도 지원하고있으며 따라서 여러 하드디스크및 저장장치를 단일 혹은 원하는 갯수에서 논리적으로 통합 및 분할할수있다.

`> fdisk --help`

명령 프롬프트

`> Command(m for help):`

한편 설정과는 무관하게 파티션의 현황을 살펴보는 뷰어 기능도 제공하고 있다.\[3\] 2018년 기준 버전은 util-linux 2.31.1 에 포함되있다.

## 같이 보기

  - [Format (명령어)](https://ko.wikipedia.org/wiki/Format_\(명령어\) "wikilink")
  - [cfdisk](https://ko.wikipedia.org/wiki/cfdisk "wikilink")

## 각주

## 외부 링크

  - [Linux Partition HOWTO. Partitioning with fdisk](http://tldp.org/HOWTO/Partition/fdisk_partitioning.html)
  - [Linux Programmer's Manual, fdisk(8)](https://www.die.net/doc/linux/man/man8/fdisk.8.html)
  - [fdisk from utils-linux-ng](https://git.kernel.org/cgit/utils/util-linux/util-linux.git/)
  - [blkid - command-line utility to locate/print block device attributes](http://linux.die.net/man/8/blkid)
  - [Using the blkid Command](http://docs.fedoraproject.org/en-US/Fedora/17/html/System_Administrators_Guide/s2-sysinfo-filesystems-blkid.html) .
  - [FreeBSD System Manager's Manual, FDISK(8)](http://www.freebsd.org/cgi/man.cgi?fdisk)

[분류:외부 도스 명령어](https://ko.wikipedia.org/wiki/분류:외부_도스_명령어 "wikilink") [분류:OS/2](https://ko.wikipedia.org/wiki/분류:OS/2 "wikilink") [분류:유닉스 파일 시스템 관련 소프트웨어](https://ko.wikipedia.org/wiki/분류:유닉스_파일_시스템_관련_소프트웨어 "wikilink") [분류:윈도우 관리](https://ko.wikipedia.org/wiki/분류:윈도우_관리 "wikilink")

1.
2.
3.  (리눅스 우분투18LTS) 파티션 현황 p, 도움말 m , 설정 중단 q, 저장후 실행 w