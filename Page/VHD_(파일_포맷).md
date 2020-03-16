> This article is converted from Wikipedia: [VHD \( \)](https://ko.wikipedia.org/wiki/VHD_\(_\)).


**가상 하드 디스크**(Virtual Hard Disk, VHD)는 [버추얼 PC](https://ko.wikipedia.org/wiki/버추얼_PC "wikilink") 2004 ([커넥틱스](https://ko.wikipedia.org/wiki/커넥틱스 "wikilink")사가 개발)와 마이크로소프트사의 [버추얼 서버](https://ko.wikipedia.org/wiki/버추얼_서버 "wikilink") 2005 R2에 쓰이는 기술이다. 2005년 6월 이후로 마이크로소프트사는 VHD 이미지 포맷 규격을 만들어 [마이크로소프트 오픈 규격 약정](https://ko.wikipedia.org/wiki/마이크로소프트_오픈_규격_약정 "wikilink") 하에 서드파티에게 제공하고 있다.

VHD 포맷은 완전한 [가상 머신](../Page/가상_머신.md "wikilink") [운영 체제와](../Page/운영_체제.md "wikilink") 응용 프로그램 스택을 하나의 파일에 캡처한다.\[1\]

VHD 포맷은 [하이퍼 V라](https://ko.wikipedia.org/wiki/하이퍼_V "wikilink") 불리는 [하이퍼바이저](../Page/하이퍼바이저.md "wikilink") 기반의 가상화 기술을 포함하고 있는 [윈도 서버 2008에도](https://ko.wikipedia.org/wiki/윈도_서버_2008 "wikilink") 사용된다. 하이퍼-V는 오프라인으로 VHD를 이용함으로써 가상 머신을 증명하지 않고도 관리자에게 VHD 안의 파일을 안전하게 접근할 수 있는 기능을 제공한다. 그뿐 아니라 일부 오프라인 관리 작업을 수행할 수 있는 기능도 제공한다.\[2\]

## 지원 포맷

VHD는 네이티브 호스트 파일 시스템에 상주하는 파일로 추가된다. 다음의 VHD 포맷은 마이크로소프트 버추얼 PC와 버추얼 서버가 지원한다.

  - 고정 하드 디스크 이미지
  - 동적 하드 디스크 이미지
  - 차별화된 하드 디스크 이미지

## VFD

가상 플로피 디스크(Virtual Floppy Disk, VFD)는 Microsoft Virtual PC, Microsoft Automated Deployment Services, Microsoft Virtual Server 2005에 쓰이는 관련 파일 포맷이다.\[3\]\[4\]\[5\]

## VHDX

가상 하드 디스크 v2(VHDX)는 VHD의 뒤를 잇는 포맷이다. VHD이 2048 GB라는 용량 제한이 있는 반면, VHDX는 64 TB의 용량 제한이 있다. 이 새로운 포맷의 디스크 이미지의 경우 파일 확장자는 `vhd` 대신 `vhdx`를 사용한다. VHDX는 전원 실패를 보호하며 [하이퍼V](https://ko.wikipedia.org/wiki/하이퍼V "wikilink")에 사용된다.\[6\] VHDX는 VHD처럼 마운트가 가능하다.

## 잠재적인 목적

  - VHD와 호스트 파일 시스템 사이의 파일 이동
  - 백업 및 복구
  - 바이러스 진단 및 보안
  - 이미지 관리 및 패치
  - 디스크 변환 (물리 디스크의 내용을 가상 디스크로, 등)
  - 수명 관리

## 같이 보기

  - [섬유 채널](https://ko.wikipedia.org/wiki/섬유_채널 "wikilink")
  - [iSCSI](https://ko.wikipedia.org/wiki/iSCSI "wikilink")

## 참조

[분류:디스크 이미지](https://ko.wikipedia.org/wiki/분류:디스크_이미지 "wikilink")

1.  [Microsoft Virtual Hard Disk Overview](http://technet.microsoft.com/en-us/bb738373.aspx)
2.  [Microsoft Windows Server 2008 Reviewer's Guide](http://technet.microsoft.com/en-us/windowsserver/2008/bb414776.aspx)
3.
4.
5.
6.  <https://technet.microsoft.com/en-us/library/hh831446(v=ws.11>).aspx