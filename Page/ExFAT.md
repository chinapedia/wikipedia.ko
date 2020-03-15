> This article is converted from Wikipedia: [ExFAT](https://ko.wikipedia.org/wiki/ExFAT).


**exFAT** (확장 파일 할당 테이블, Extended File Allocation Table, 줄여서 FAT64)는 [특허 출원](../Page/특허.md "wikilink") 중인\[1\][사유](https://ko.wikipedia.org/wiki/사유_소프트웨어 "wikilink") [파일 시스템으로](https://ko.wikipedia.org/wiki/파일_시스템 "wikilink"), [마이크로소프트](https://ko.wikipedia.org/wiki/마이크로소프트 "wikilink")사가 [윈도우 CE 6.0](https://ko.wikipedia.org/wiki/윈도우_CE_6.0 "wikilink") 장치와 데스크톱 운영 체제 [윈도우 비스타 서비스 팩 1](../Page/윈도우_비스타.md "wikilink")\[2\] 및 [윈도우 7](https://ko.wikipedia.org/wiki/윈도우_7 "wikilink"), 그리고 자사의 서버 운영 체제인 [윈도우 서버 2008에](../Page/윈도우_서버_2008.md "wikilink") 도입하기 위해 만든 것이다.\[3\]

exFAT는 [NTFS](../Page/NTFS.md "wikilink") 파일 시스템이 자료 구조 오버헤드 등의 문제로 적절치 못할 경우, 또는 이전 버전인 [FAT](../Page/파일_할당_테이블.md "wikilink") 파일 시스템의 파일 크기/디렉터리 제약이 문제가 되는 경우에 사용될 수 있다.

[윈도우 XP와](../Page/윈도우_XP.md "wikilink") [윈도우 서버 2003](../Page/윈도우_서버_2003.md "wikilink") (둘다 x86, x64) 사용자들은 마이크로소프트사로부터 업데이트 KB955704를 내려받아 설치하면 exFAT 지원을 사용할 수 있다.\[4\] exFAT 파일 읽기를 지원하는 실험적인 오픈 소스 리눅스 커널 모듈은 현재 개발 중이다\[5\]. 마이크로소프트 exFAT 드라이버로부터 라이선스 받아 전달된 클로즈드 소스의 읽기/쓰기 리눅스 드라이버는 Tuxera를 통해 구매하여 사용할 수 있다\[6\].

## 이점

이전 [파일 할당 테이블](../Page/파일_할당_테이블.md "wikilink") (FAT) 파일 시스템 버전과 견주어 나아진 점은 다음과 같다:

  - 대용량으로 크기를 넓힐 수 있음: 이론 상 최대 64 [ZiB](https://ko.wikipedia.org/wiki/제비바이트 "wikilink"), 권장 최대 512 [TiB](https://ko.wikipedia.org/wiki/테비바이트 "wikilink") 지원 - 이는 기존 [FAT32](https://ko.wikipedia.org/wiki/FAT32 "wikilink") 파티션의 2 TiB의 제한에서 상승한 것임. 다만 [윈도우 XP에](../Page/윈도우_XP.md "wikilink") 내장된 포맷 유틸리티는 새로운 FAT32 파티션을 32 [GiB로까지](https://ko.wikipedia.org/wiki/기가바이트 "wikilink") 제한한다.\[7\]
  - 2<sup>9</sup> (512)와 2<sup>12</sup> (4,096) 바이트의 [섹터](../Page/디스크_섹터.md "wikilink") 크기
  - 최대 32 [MiB의](../Page/메비바이트.md "wikilink") [클러스터](https://ko.wikipedia.org/wiki/클러스터 "wikilink")\[8\]
  - 파일 한 개 당 최대 64 [ZiB](https://ko.wikipedia.org/wiki/제비바이트 "wikilink") (512 [TiB](https://ko.wikipedia.org/wiki/테비바이트 "wikilink") 권장 최대) 지원 - 이는 [FAT32](https://ko.wikipedia.org/wiki/FAT32 "wikilink")에서 4 [GiB에서](https://ko.wikipedia.org/wiki/기가바이트 "wikilink") 상승한 것임.\[9\]
  - [자유 공간 비트맵의](https://ko.wikipedia.org/wiki/자유_공간_비트맵 "wikilink") 도입으로 자유 공간 할당 및 삭제 성능 개선
  - 한 [디렉터리](https://ko.wikipedia.org/wiki/디렉터리 "wikilink")에 최대 2,796,202개의 파일을 담을 수 있음\[10\] - 이는 기존의 65,536개에서 상승한 것임.
  - [접근 제어 목록](../Page/접근_제어_목록.md "wikilink") 지원 (윈도우 비스타 SP1에서는 아직 지원 안 함)\[11\]
  - [TFAT](https://ko.wikipedia.org/wiki/TFAT "wikilink") 지원 - 트랜잭션 파일 시스템 표준 ([WinCE](https://ko.wikipedia.org/wiki/윈도우_CE "wikilink") 활성 기능은 선택 사항)
  - OEM 정의 가능 변수 예비로 특정 드라이브 특성을 위한 파일 시스템의 사용자 지정 가능
  - [UTC](https://ko.wikipedia.org/wiki/협정_세계시 "wikilink") 시간표 지원 ([비스타 SP2부터](../Page/윈도우_비스타.md "wikilink") 지원)\[12\]
  - 시간표 정밀도 10 [ms](https://ko.wikipedia.org/wiki/밀리초 "wikilink") (기존의 FAT 버전의 2 [초보다](https://ko.wikipedia.org/wiki/초_\(시간\) "wikilink") 좋지만 NTFS의 100 [ns보다는](https://ko.wikipedia.org/wiki/나노초 "wikilink") 나쁨)\[13\]

## 단점

이전 FAT 버전과 견주어 나빠진 점은 다음과 같다:

  - [윈도우 XP](../Page/윈도우_XP.md "wikilink"), [윈도우 서버 2003](../Page/윈도우_서버_2003.md "wikilink") 사용자들은 exFAT 지원을 위하여 서비스 팩 2 이상 또는 별도의 업데이트를 설치하여야 함
  - [윈도우 비스타](../Page/윈도우_비스타.md "wikilink") 사용자들은 exFAT 지원을 위하여 [서비스 팩 1](../Page/윈도우_비스타.md "wikilink") 이상을 설치하여야 함
  - exFAT를 사용하여 포맷한 장치는 [윈도우 XP](../Page/윈도우_XP.md "wikilink") 이전의 버전, 도스, OS/2에 읽히지 않음
  - exFAT를 사용하는 장치는 [윈도우 비스타의](../Page/윈도우_비스타.md "wikilink") [레디부스트](../Page/레디부스트.md "wikilink") 기능을 사용할 수 없음 ([윈도우 7은](https://ko.wikipedia.org/wiki/윈도우_7 "wikilink") exFAT로 포맷한 드라이브에 대한 [레디부스트](../Page/레디부스트.md "wikilink") 기능을 지원하며 기존 [FAT32](https://ko.wikipedia.org/wiki/FAT32 "wikilink")의 4GB 크기 제한이 없어짐으로써 더 넓은 레디부스트 캐시를 사용할 수 있음)\[14\]
  - 마이크로소프트사는 exFAT 파일 규격을 공개하지 않고 있고 exFAT 기능을 만들어 배포하려면 마이크로소프트로부터의 라이선스가 필요하다\[15\]
  - 현재 PC 환경 밖에서는 제한되거나 지원되지 않고 있음 — 텔레비전 및 A/V 수신기와 같은 대부분의 전자 기기는 이전의 FAT 버전만 다룰 수 있음 (이는 새로운 exFAT를 요구하는 [SDXC 카드](https://ko.wikipedia.org/wiki/시큐어_디지털_카드 "wikilink") 및 [메모리 스틱 XC와](../Page/메모리_스틱.md "wikilink") 함께 쓸 경우 달라질 수 있음)

## 라이선스

회사들은 exFAT를 사진기, 캠코더, 디지털 사진틀 등의 특정 그룹의 전자 기기에 통합할 수 있다. 다만 휴대 전화, 개인용 컴퓨터, 네트워크는 다른 가격 모델을 가진다.\[16\]

## 같이 보기

  - [파일 시스템의 목록](https://ko.wikipedia.org/wiki/파일_시스템의_목록 "wikilink")

## 각주

## 외부 링크

  - [Personal Storage: Opportunities and challenges for pocket-sized storage devices in the Windows world](http://download.microsoft.com/download/5/b/9/5b97017b-e28a-4bae-ba48-174cf47d23cd/STO072_WH06.ppt) ([마이크로소프트 파워포인트](https://ko.wikipedia.org/wiki/마이크로소프트_파워포인트 "wikilink") 프레젠테이션)
  - [TFAT 개요](http://msdn2.microsoft.com/en-us/library/aa915463.aspx)
  - [exFAT 파일 시스템](http://msdn2.microsoft.com/en-us/library/aa914353.aspx)
  - [exFAT 파일 시스템 드라이버 업데이트 패키지 설명](http://support.microsoft.com/Default.aspx?kbid=955704)
  - [윈도우 XP용 업데이트 (KB955704)](https://web.archive.org/web/20100723072011/http://www.microsoft.com/downloads/details.aspx?FamilyID=1cbe3906-ddd1-4ca2-b727-c2dff5e30f61&displaylang=en)
  - [윈도우 XP x64 에디션용 업데이트 (KB955704)](http://www.microsoft.com/downloads/details.aspx?FamilyID=6f69637b-41e6-4346-aa99-fcf802bd8bbd&DisplayLang=en)
  - [윈도우 서버 2003용 업데이트 (KB955704)](http://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=94fad746-22de-4d89-aa9d-b54751261fab)
  - [윈도우 서버 2003 x64 에디션용 업데이트 (KB955704)](http://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=026d782d-a3ff-4c40-a1fa-f1e4f5ae01d3)

[분류:윈도우 CE](https://ko.wikipedia.org/wiki/분류:윈도우_CE "wikilink") [분류:파일 시스템](https://ko.wikipedia.org/wiki/분류:파일_시스템 "wikilink") [분류:2006년 소프트웨어](https://ko.wikipedia.org/wiki/분류:2006년_소프트웨어 "wikilink")

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
11. [Anandtech - Second Shot: Windows Vista SP1](http://www.anandtech.com/systems/showdoc.aspx?i=3233&p=4)
12.
13. [미국 특허 20090164440](http://appft1.uspto.gov/netacgi/nph-Parser?Sect1=PTO2&Sect2=HITOFF&p=1&u=/netahtml/PTO/search-bool.html&r=1&f=G&l=50&co1=AND&d=PG01&s1=20090164440&OS=20090164440&RS=20090164440)는 마이크로소프트 exFAT 규격 (리비전 1.00)을 포함하고 있다
14.
15.
16.