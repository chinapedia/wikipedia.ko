> This article is converted from Wikipedia: [ReFS](https://ko.wikipedia.org/wiki/ReFS).


**ReFS**\[1\](Resilient File System, 코드명: Protogon\[2\])는 [NTFS](../Page/NTFS.md "wikilink")(New technology File System)의 차세대 [파일 시스템으로](../Page/파일_시스템.md "wikilink") 염두에 두고 [윈도우 서버 2012에](../Page/윈도우_서버_2012.md "wikilink") 도입된 [마이크로소프트](../Page/마이크로소프트.md "wikilink")의 [사유](https://ko.wikipedia.org/wiki/사유_포맷 "wikilink") [파일 시스템이다](../Page/파일_시스템.md "wikilink").

ReFS는 NTFS 도입 이후 중요하게 부각되었던 문제들을 극복하기 위해 설계되었으며, 여기에는 어떻게 데이터 기억 장치의 요구 사항들이 변화했는지와 관련된다. ReFS의 주요 설계 상 이점에는 자동 [무결성 검사](https://ko.wikipedia.org/wiki/파일_무결성_감시 "wikilink"), [데이터 스크러빙](https://ko.wikipedia.org/wiki/데이터_스크러빙 "wikilink"), [CHKDSK](../Page/CHKDSK.md "wikilink") 실행의 필요성 제거, [데이터 마모에](https://ko.wikipedia.org/wiki/데이터_마모 "wikilink") 대한 보호, [하드 디스크 드라이브 실패](https://ko.wikipedia.org/wiki/하드_디스크_드라이브_실패 "wikilink") 및 [다중화의](https://ko.wikipedia.org/wiki/다중화_\(시스템\) "wikilink") 내부 관리, [RAID](../Page/RAID.md "wikilink") 기능 통합, 데이터 및 메타데이터 업데이트를 위한 [카피/얼로케이트 온 라이트로의](https://ko.wikipedia.org/wiki/카피_온_라이트 "wikilink") 전환, [매우 긴 경로와 파일 이름의](../Page/긴_파일_이름.md "wikilink") 관리, 임의 크기의 [논리 볼륨을](../Page/논리_볼륨_관리자.md "wikilink") 포함(사용 중인 드라이브의 물리 크기와는 무관)한 [스토리지 가상화](https://ko.wikipedia.org/wiki/스토리지_가상화 "wikilink") 및 풀링이 포함된다.

2012\~2013년 초기 버전에서 ReFS는 대부분의 테스트에서 NTFS와 비슷하거나 조금 더 빨랐으나\[3\] ReFS의 새로운 기능인 완전 무결성 검사 기능을 사용 중일 때에는 훨씬 속도가 느렸다.\[4\]\[5\]

## 같이 보기

  - [WinFS](../Page/WinFS.md "wikilink")

## 각주

<references />

## 외부 링크

  - [Analysis of detailed differences between NTFS and ReFS in Server 2012, and reasons for choosing one or the other](http://kx.cloudingenium.com/microsoft/servers/windows-servers/windows-server-2012/windows-server-2012-file-system-resiliency-refs-data-deduplication-ntfs/)

[분류:2012년 소프트웨어](https://ko.wikipedia.org/wiki/분류:2012년_소프트웨어 "wikilink") [분류:윈도우 디스크 파일 시스템](https://ko.wikipedia.org/wiki/분류:윈도우_디스크_파일_시스템 "wikilink")

1.
2.
3.
4.
5.