> This article is converted from Wikipedia: [NTFS](https://ko.wikipedia.org/wiki/NTFS).


**NTFS**(New Technology File System\[1\])는 [윈도우 NT](../Page/윈도우_NT.md "wikilink") 계열 운영체제의 [파일 시스템으로](../Page/파일_시스템.md "wikilink") [윈도우 2000](../Page/윈도우_2000.md "wikilink"), [윈도우 XP](../Page/윈도우_XP.md "wikilink"), [윈도우 서버 2003](../Page/윈도우_서버_2003.md "wikilink"), [윈도우 서버 2008](../Page/윈도우_서버_2008.md "wikilink"), [윈도우 비스타](../Page/윈도우_비스타.md "wikilink"), [윈도우 7](https://ko.wikipedia.org/wiki/윈도우_7 "wikilink"), [윈도우 서버 2008 R2](../Page/윈도우_서버_2008_R2.md "wikilink") , [윈도우 8](../Page/윈도우_8.md "wikilink"), [윈도우 서버 2012](../Page/윈도우_서버_2012.md "wikilink"), [윈도우 8.1](../Page/윈도우_8.1.md "wikilink"), [윈도우 서버 2012 R2](https://ko.wikipedia.org/wiki/윈도우_서버_2012_R2 "wikilink") 등에도 포함되어 있다. NTFS의 NT는 윈도우 NT와 비슷하게 새로운 기술이라는 뜻의 New Technology의 준말이다. [MS-DOS](../Page/MS-DOS.md "wikilink")와 이전 버전의 윈도우에서 쓰였던 [마이크로소프트](../Page/마이크로소프트.md "wikilink")의 이전 [FAT](../Page/파일_할당_테이블.md "wikilink") 파일 시스템을 대체하였다. NTFS는 FAT와 HPFS([고성능 파일 시스템](https://ko.wikipedia.org/wiki/고성능_파일_시스템 "wikilink"))을 거쳐 몇 가지 개선이 있다. 이를테면, [메타데이터](../Page/메타데이터.md "wikilink")의 지원, 고급 데이터 구조의 사용으로 인한 성능 개선, 신뢰성, 추가 확장 기능을 더한 디스크 공간 활용을 들 수 있다.

## 역사

1980년대 중순, 마이크로소프트와 [IBM](../Page/IBM.md "wikilink")은 차세대 그래픽 [운영 체제를](../Page/운영_체제.md "wikilink") 만들기 위해 조인트 프로젝트를 개설하였다. 프로젝트의 결과물은 [OS/2](https://ko.wikipedia.org/wiki/OS/2 "wikilink")였으나 마이크로소프트와 IBM은 수많은 중요 문제에 대해 합의에 이르지 못했고 마침내 분리되었다: OS/2는 IBM의 프로젝트로 남았고 마이크로소프트는 윈도우 NT를 작업하게 되었다.

OS/2 파일 시스템 [HPFS](../Page/HPFS.md "wikilink")는 여러 중요한 신기능을 포함하였다. 마이크로소프트가 새로운 운영 체제를 만들었을 때 이러한 개념들 중 다수를 NTFS로 가져왔다.\[2\] 혈통이 동일했던 덕분인지 HPFS와 NTFS는 동일한 [디스크 파티션](https://ko.wikipedia.org/wiki/디스크_파티션 "wikilink") 식별 유형 코드 (07)을 사용한다.

사용할 수 있는 수많은 코드가 있고, 기타 주요 파일 시스템들이 자체 코드를 갖고 있기 때문에 동일한 파티션 ID 레코드 번호를 사용하는 것은 흔치 않다. FAT는 9개 이상을 갖고 있다. ([FAT12](https://ko.wikipedia.org/wiki/FAT12 "wikilink"), [FAT16](https://ko.wikipedia.org/wiki/FAT16 "wikilink"), [FAT32](https://ko.wikipedia.org/wiki/FAT32 "wikilink") 등 각각) 파티션 유형 07의 파일 시스템을 식별하는 알고리즘들은 추가적인 검사를 수행해야 한다. NTFS 개발자들은 다음을 포함한다: [톰 밀러](https://ko.wikipedia.org/wiki/톰_밀러 "wikilink"), [게리 키무라](https://ko.wikipedia.org/wiki/게리_키무라 "wikilink"), 브라이언 앤드루, 데이빗 고벨.\[3\]

## 버전

NTFS는 다음의 5 가지 버전을 가지고 있다:

  - **v1.0**: 1993년 [윈도우 NT 3.1과](../Page/윈도우_NT_3.1.md "wikilink") 함께 출시되었다. v1.0은 1.1 이상과 호환되지 않는다: 윈도우 NT 3.5x가 만든 볼륨은 업데이트 설치 없이 윈도우 NT 3.1에서 읽을 수 없다. (NT 3.5x 설치 미디어에서 이용 가능)\[4\]
  - **v1.1**: 1995년 [윈도우 NT 3.51과](../Page/윈도우_NT_3.51.md "wikilink") 함께 출시되었다. 압축 파일, 명명 스트림, [접근 제어 목록을](../Page/접근_제어_목록.md "wikilink") 지원한다.\[5\]
  - **v1.2**: 1996년 [윈도우 NT 4.0과](../Page/윈도우_NT_4.0.md "wikilink") 함께 출시되었다. [보안 서술자를](https://ko.wikipedia.org/wiki/보안_서술자 "wikilink") 지원한다. OS 출시 이후 NTFS 4.0으로 흔히 부른다.
  - **v3.0**: [윈도우 2000과](../Page/윈도우_2000.md "wikilink") 함께 출시되었다.\[6\] 디스크 쿼터, [암호화 파일 시스템](../Page/암호화_파일_시스템.md "wikilink"), [희소 파일](https://ko.wikipedia.org/wiki/희소_파일 "wikilink"), [리파스 포인트](https://ko.wikipedia.org/wiki/NTFS_리파스_포인트 "wikilink"), [업데이트 시퀀스 번호 (USN) 저널링](https://ko.wikipedia.org/wiki/USN_저널 "wikilink"), $Extend 폴더 및 파일을 지원한다. [보안 서술자를](https://ko.wikipedia.org/wiki/보안_서술자 "wikilink") 재정비하여 같은 보안 설정을 사용하는 여러 파일들이 같은 서술자를 공유할 수 있다.\[7\] OS 출시 이후 NTFS 5.0으로 흔히 부른다.
  - **v3.1**: 2001년 가을 [윈도우 XP와](../Page/윈도우_XP.md "wikilink") 함께 출시되었다. (윈도우 비스타, 윈도우 7에도 연이어 사용됨) 추가 MFT 레코드 번호(손상된 MFT 파일 복구에 유용)와 더불어 마스터 파일 테이블 (MFT) 엔트리를 확장하였다. OS 출시 이후로 NTFS 5.1로 흔히 부른다.

## 특징

  - **복구성** : 시스템 고장과 디스크 손상을 복구하는 능력이 있다. 손상이 발생하면 NTFS는 디스크 볼륨을 재구성하여 일관성 있는 상태로 복구한다. 파일 시스템을 변경하기 위해 [트랜잭션](https://ko.wikipedia.org/wiki/트랜잭션 "wikilink") 처리 모델이 적용되어, 각 진행 단계들은 [원자적 행위](https://ko.wikipedia.org/wiki/원자적_행위 "wikilink")(atomic action)로 처리된다. 손상된 시점에서 처리중이었던 각 트랜잭션은 차후에 실행이 완료되거나 파기된다. 다른 한편으로는 중요한 파일 시스템 데이터를 보존하기 위해 중복 저장장치를 사용한다. 그렇게 함으로써 디스크 섹터의 일부가 파손되더라도 파일 시스템의 구조에 관한 데이터 상실을 방지한다.

<!-- end list -->

  - **보안성** : 보안을 위해 [윈도우 NT](../Page/윈도우_NT.md "wikilink") 객체 모델이 적용되었다. 어떤 파일을 열면, 해당 파일은 파일의 보안 속성을 관장하는 보안 서술자를 가진 파일 객체로 구현된다.

## 내부 구조

### 파티션 부트 섹터

<table>
<caption>NTFS 부트 섹터 내용</caption>
<thead>
<tr class="header">
<th><p>바이트 오프셋</p></th>
<th><p>필드 길이</p></th>
<th><p>일반 수치</p></th>
<th><p>필드 이름</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>0x00</p></td>
<td><p>3 바이트</p></td>
<td><p>0xEB5290</p></td>
<td><p>JMP 명령</p></td>
</tr>
<tr class="even">
<td><p>0x03</p></td>
<td><p>8 바이트</p></td>
<td><p>"<code>NTFS    </code>"<br />
<small>워드 "NTFS" 뒤에 4개의 공백(0x20)이 존재</small></p></td>
<td><p>OEM ID</p></td>
</tr>
<tr class="odd">
<td><p>0x0B</p></td>
<td><p>2 바이트</p></td>
<td><p>0x0200</p></td>
<td><p>섹터 당 바이트</p></td>
</tr>
<tr class="even">
<td><p>0x0D</p></td>
<td><p>1 바이트</p></td>
<td><p>0x08</p></td>
<td><p>클러스터 당 섹터</p></td>
</tr>
<tr class="odd">
<td><p>0x0E</p></td>
<td><p>2 바이트</p></td>
<td><p>0x0000</p></td>
<td><p>예약된 섹터</p></td>
</tr>
<tr class="even">
<td><p>0x10</p></td>
<td><p>3 바이트</p></td>
<td><p>0x000000</p></td>
<td><p>미사용</p></td>
</tr>
<tr class="odd">
<td><p>0x13</p></td>
<td><p>2 바이트</p></td>
<td><p>0x0000</p></td>
<td><p>NTFS가 사용하지 않음</p></td>
</tr>
<tr class="even">
<td><p>0x15</p></td>
<td><p>1 바이트</p></td>
<td><p>0xF8</p></td>
<td><p>미디어 서술자</p></td>
</tr>
<tr class="odd">
<td><p>0x16</p></td>
<td><p>2 바이트</p></td>
<td><p>0x0000</p></td>
<td><p>미사용</p></td>
</tr>
<tr class="even">
<td><p>0x18</p></td>
<td><p>2 바이트</p></td>
<td><p>0x003F</p></td>
<td><p>트랙 당 섹터</p></td>
</tr>
<tr class="odd">
<td><p>0x1A</p></td>
<td><p>2 바이트</p></td>
<td><p>0x00FF</p></td>
<td><p>헤드 수</p></td>
</tr>
<tr class="even">
<td><p>0x1C</p></td>
<td><p>4 바이트</p></td>
<td><p>0x0000003F</p></td>
<td><p>숨겨진 섹터</p></td>
</tr>
<tr class="odd">
<td><p>0x20</p></td>
<td><p>4 바이트</p></td>
<td><p>0x00000000</p></td>
<td><p>미사용</p></td>
</tr>
<tr class="even">
<td><p>0x24</p></td>
<td><p>4 바이트</p></td>
<td><p>0x80008000</p></td>
<td><p>미사용</p></td>
</tr>
<tr class="odd">
<td><p>0x28</p></td>
<td><p>8 바이트</p></td>
<td><p>0x00000000007FF54A</p></td>
<td><p>총 섹터</p></td>
</tr>
<tr class="even">
<td><p>0x30</p></td>
<td><p>8 바이트</p></td>
<td><p>0x0000000000000004</p></td>
<td><p>$MFT 클러스터 번호</p></td>
</tr>
<tr class="odd">
<td><p>0x38</p></td>
<td><p>8 바이트</p></td>
<td><p>0x000000000007FF54</p></td>
<td><p>$MFTMirr 클러스터 번호</p></td>
</tr>
<tr class="even">
<td><p>0x40</p></td>
<td><p>1 바이트</p></td>
<td><p>0xF6</p></td>
<td><p>파일 레코드 세그먼트 당 바이트</p></td>
</tr>
<tr class="odd">
<td><p>0x41</p></td>
<td><p>3 바이트</p></td>
<td><p>0x000000</p></td>
<td><p>미사용</p></td>
</tr>
<tr class="even">
<td><p>0x44</p></td>
<td><p>1 바이트</p></td>
<td><p>0x01</p></td>
<td><p>인덱스 버퍼 당 클러스터</p></td>
</tr>
<tr class="odd">
<td><p>0x45</p></td>
<td><p>3 바이트</p></td>
<td><p>0x000000</p></td>
<td><p>미사용</p></td>
</tr>
<tr class="even">
<td><p>0x48</p></td>
<td><p>8 바이트</p></td>
<td><p>0x1C741BC9741BA514</p></td>
<td><p>볼륨 일련 번호</p></td>
</tr>
<tr class="odd">
<td><p>0x50</p></td>
<td><p>4 바이트</p></td>
<td><p>0x00000000</p></td>
<td><p>체크섬</p></td>
</tr>
<tr class="even">
<td><p>0x54</p></td>
<td><p>426 바이트</p></td>
<td></td>
<td><p>부트스트랩 코드</p></td>
</tr>
<tr class="odd">
<td><p>0x01FE</p></td>
<td><p>2 바이트</p></td>
<td><p>0xAA55</p></td>
<td><p>섹터 끝 마커</p></td>
</tr>
</tbody>
</table>

\[8\]

### 메타 파일

| 세그먼트 번호 | 파일 이름                                                                                                                                              |
| ------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| 0       | `$MFT`                                                                                                                                             |
| 1       | `$MFTMirr`                                                                                                                                         |
| 2       | `$LogFile`                                                                                                                                         |
| 3       | `$Volume`                                                                                                                                          |
| 4       | `$AttrDef`                                                                                                                                         |
| 5       | `.`                                                                                                                                                |
| 6       | `$Bitmap`                                                                                                                                          |
| 7       | `$Boot`                                                                                                                                            |
| 8       | `$BadClus`                                                                                                                                         |
| 9       | `$Secure`                                                                                                                                          |
| 10      | `$UpCase`                                                                                                                                          |
| 11      | `$Extend`                                                                                                                                          |
| 12–23   | $MFT 확장 엔트리를 위해 예약되어 있다. 확장 엔트리들은 프라이머리 레코드에 맞지 않는 추가 특성을 포함하는 추가적인 MFT 레코드들이다. 파일이 충분히 단편화되어 있고, 스트림이 많으며, 긴 파일 이름, 복잡한 보안 및 기타 드문 환경에 처할 때 발생한다. |
| 24      | `$Extend\$Quota`                                                                                                                                   |
| 25      | `$Extend\$ObjId`                                                                                                                                   |
| 26      | `$Extend\$Reparse`                                                                                                                                 |
| 27—     | 정규 파일 엔트리의 시작.                                                                                                                                     |

NTFS 메타파일의 목록

## 제한

NTFS에는 다음과 같은 몇 가지 제한이 있다.

  - 파일 이름: 파일 이름은 255 [UTF-16](../Page/UTF-16.md "wikilink") 코드 워드로 그 수가 제한된다. 특정한 이름은 볼륨 루트 디렉터리에 남아 있으므로 파일에 사용하지 못한다. 이를테면 $MFT, $MFTMirr, $LogFile, $Volume, $AttrDef, . (점), $Bitmap, $Boot, $BadClus, $Secure, $Upcase, $Extend가 있다.\[9\] 점 (.)과 $Extend는 둘 다 디렉터리이며 그 밖의 것들은 파일들이다. NT 커널은 완전한 경로를 32,767 utf-16 코드 워드로 그 수를 제한한다.

<!-- end list -->

  - 최대 볼륨 크기: 이론적으로 최대 NTFS 볼륨 크기는 2<sup>64</sup>−1 클러스터이다. 그러나 윈도우 XP 프로페셔널에 제공되는 최대 NTFS 볼륨 크기는 2<sup>32</sup>−1 클러스터이다. 이를테면 최대 윈도우 XP NTFS 볼륨 크기인 64 KB () 클러스터는 256 TB () - 64 KB이다. 기본 클러스터 크기 (4 KB)를 사용하면 최대 NTFS 볼륨 크기는 16 16 TB - 4 KB로 된다. 둘 다 윈도우 XP 서비스팩 1에서 제한되었던 128 GB ()보다는 높은 수치이다. 마스터 부트 레코드 (MBR) 디스크 상의 파티션 테이블이 최대 2 TB의 파티션 크기를 지원하기 때문에 다이내믹 또는 [GPT](../Page/GUID_파티션_테이블.md "wikilink") 볼륨은 2 TB 이상의 NTFS 볼륨을 만드는 데 사용하여야 한다. GPT 볼륨에서 윈도우 환경으로 시동하는 경우 [EFI를](https://ko.wikipedia.org/wiki/확장_펌웨어_인터페이스 "wikilink") 채용한 시스템과 64비트 지원을 요구한다.\[10\]

<!-- end list -->

  - 최대 파일 크기: 앞서 언급한 대로 이론적인 최대 NTFS 파일 크기는 16 EB () - 1 KB (), 곧 18,446,744,073,709,550,592 바이트이다. 하지만 실제 최대 NTFS 파일 크기는 16 TB () - 64 KB (), 곧 17,592,185,978,880 바이트이다.

<!-- end list -->

  - 대체 데이터 스트림: 윈도우 시스템 호출은 대체 데이터 스트림을 관리할 수 있다.\[11\] 운영 체제에 따라 유틸리티 및 원격 파일 시스템, 파일 전송은 데이터 스트림을 조용히 스트리핑(strip)할 수 있다.\[12\] 파일을 안전하게 복사하고 이동하는 방법은 BackupRead, BackupWrite 호출을 사용하는 것이며 이로써 프로그램이 스트림을 열거하고 각 스트림이 목적 볼륨에 제대로 기록하는지 유효성을 확인하며 위반 스트림을 무시하는 것을 알게 된다.\[13\]

<!-- end list -->

  - 운영 체제 호환성: [윈도우 NT](../Page/윈도우_NT.md "wikilink") 기반 운영 체제는 이 파일 시스템을 이용한다. 사용자는 다른 운영 체제의 컴퓨터와의 전송을 위하여 [플래시 드라이브나](https://ko.wikipedia.org/wiki/플래시_드라이브 "wikilink") 외장 [하드 드라이브를](https://ko.wikipedia.org/wiki/하드_드라이브 "wikilink") [FAT32](https://ko.wikipedia.org/wiki/FAT32 "wikilink")로 포맷할 것을 권고 받는다.

## 같이 보기

  - [FAT](../Page/파일_할당_테이블.md "wikilink")
  - [HPFS](../Page/HPFS.md "wikilink")
  - [UFS](../Page/유닉스_파일_시스템.md "wikilink")
  - [파일 시스템](../Page/파일_시스템.md "wikilink")

## 각주

<references />

[분류:윈도우 구성 요소](https://ko.wikipedia.org/wiki/분류:윈도우_구성_요소 "wikilink") [분류:파일 시스템](https://ko.wikipedia.org/wiki/분류:파일_시스템 "wikilink") [분류:1993년 소프트웨어](https://ko.wikipedia.org/wiki/분류:1993년_소프트웨어 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.  [NTFS Partition Boot Sector](http://www.ntfs.com/ntfs-partition-boot-sector.htm) Information on structure of the boot sector.
9.
10. <http://www.rodsbooks.com/gdisk/booting.html>
11.
12.
13.