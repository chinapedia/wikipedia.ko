> This article is converted from Wikipedia: [Lspci](https://ko.wikipedia.org/wiki/Lspci).


**lspci**는 시스템 내 [PCI](../Page/PCI_버스.md "wikilink") 버스와 [장치의](../Page/컴퓨터_하드웨어.md "wikilink") 상세 정보를 출력(나열)하는 [유닉스 계열](../Page/유닉스_계열.md "wikilink") 운영 체제의 명령어이다. 다양한 운영 체제의 PCI 구성 공간에 대한 접근 권한을 제공하는 포터블 라이브러리 libpci에 기반을 둔다.

{{-}}

## 사용 예

[리눅스](../Page/리눅스.md "wikilink") 시스템에서의 사용 예이다:

``` console
# lspci
00:00.0 Host bridge: Intel Corporation 82815 815 Chipset Host Bridge and Memory Controller Hub (rev 11)
00:02.0 VGA compatible controller: Intel Corporation 82815 Chipset Graphics Controller (CGC) (rev 11)
00:1e.0 PCI bridge: Intel Corporation 82801 Mobile PCI Bridge (rev 03)
00:1f.0 ISA bridge: Intel Corporation 82801BAM ISA Bridge (LPC) (rev 03)
00:1f.1 IDE interface: Intel Corporation 82801BAM IDE U100 Controller (rev 03)
00:1f.2 USB Controller: Intel Corporation 82801BA/BAM USB Controller #1 (rev 03)
00:1f.3 SMBus: Intel Corporation 82801BA/BAM SMBus Controller (rev 03)
00:1f.4 USB Controller: Intel Corporation 82801BA/BAM USB Controller #2 (rev 03)
00:1f.5 Multimedia audio controller: Intel Corporation 82801BA/BAM AC'97 Audio Controller (rev 03)
01:03.0 CardBus bridge: O2 Micro, Inc. OZ6933/711E1 CardBus/SmartCardBus Controller (rev 01)
01:03.1 CardBus bridge: O2 Micro, Inc. OZ6933/711E1 CardBus/SmartCardBus Controller (rev 01)
01:0b.0 PCI bridge: Actiontec Electronics Inc Mini-PCI bridge (rev 11)
02:04.0 Ethernet controller: Intel Corporation 82557/8/9/0/1 Ethernet Pro 100 (rev 08)
02:08.0 Communication controller: Agere Systems WinModem 56k (rev 01)
```

수많은 장치가 알 수 없음(예: "Unknown device 2830 (rev 02))으로 표시되는 경우 보통은 'update-pciids' 명령을 실행하여 이 문제를 해결할 수 있다.

## lsusb

`lsusb`\[1\]은 USB 버스와 장치를 위한 유사 명령어이다. 이 프로그램의 모든 기능을 이용하려면 [/proc/bus/usb](http://www.linux-usb.org/USB-guide/x173.html) 인터페이스를 지원하는 리눅스 커널이 필요하다. (예: [리눅스 커널](../Page/리눅스_커널.md "wikilink") 2.3.15 이상).

## hwinfo

`hwinfo`는 하드웨어 전반을 위한 것이다.\[2\] `lshw`는 hwinfo 프리셋의 하위 집합이다.\[3\]\[4\]

## 기타 플랫폼

FreeBSD의 동등한 명령어는 `pciconf -l`이다. pciconf는PCI 레지스터의 읽기, 쓰기와 같은 기타 명령을 수행할 수도 있다. 자세한 정보는 [man page](http://www.freebsd.org/cgi/man.cgi?query=pciconf&apropos=0&sektion=0&manpath=FreeBSD+7.1-RELEASE&format=html)를 참고할 것.

위에 언급된 hwinfo 도구와는 관련이 없는 [HWiNFO](http://www.hwinfo.com/)라는 이름의 도구는 무료로 바이너리 형태로 다운로드가 가능하다.

## 비슷한 명령어

  - [Dmesg](../Page/Dmesg.md "wikilink"): 커널의 [메시지 버퍼](https://ko.wikipedia.org/wiki/메시지_버퍼 "wikilink") 출력
  - [Uname](../Page/Uname.md "wikilink"): 현재 머신과 운영 체제의 이름, 버전, 기타 세부 정보 출력
  - [Util-linux](../Page/Util-linux.md "wikilink")

## 같이 보기

  - [idProduct](https://ko.wikipedia.org/wiki/idProduct "wikilink")
  - [Uname](../Page/Uname.md "wikilink")
  - [Util-linux](../Page/Util-linux.md "wikilink")
  - [파일 시스템](../Page/파일_시스템.md "wikilink")

## 각주

## 외부 링크

  -
  - [The PCI utilities home](http://mj.ucw.cz/pciutils.shtml).

  - [The home of the pci.ids](http://pciids.sourceforge.net/) file, with its [Online list of ID's](http://pci-ids.ucw.cz/read/PC/).

  - [Online device driver check page that maps PCI Ids to Linux drivers](http://kmuto.jp/debian/hcl/).

  - [8 commands to check hardware information on Linux](http://www.binarytides.com/linux-cpu-information/)

[분류:유닉스 소프트웨어](https://ko.wikipedia.org/wiki/분류:유닉스_소프트웨어 "wikilink")

1.
2.  [Discover your hardware](https://h-node.org/wiki/page/en/Discover-your-hardware) in Linux, H-node.org
3.  [16 commands to check hardware information on Linux](http://www.binarytides.com/linux-commands-hardware-info/) on BinaryTides.com, April 2014
4.  [How to interpret lshw output](http://www.ezix.org/project/wiki/HardwareLiSter#Howtointerpretlshwsoutput) on Ezix.org; retrieved in October 2016