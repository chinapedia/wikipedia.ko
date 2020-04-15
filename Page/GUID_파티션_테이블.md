> This article is converted from Wikipedia: [GUID 파티션 테이블](https://ko.wikipedia.org/wiki/GUID_파티션_테이블).


[섬네일](https://ko.wikipedia.org/wiki/파일:GUID_Partition_Table_Scheme.svg "wikilink") [컴퓨터 하드웨어에서](../Page/컴퓨터_하드웨어.md "wikilink") **[GUID](../Page/전역_고유_식별자.md "wikilink") 파티션 테이블**(GPT, GUID Partition Table)은 물리적인 [하드 디스크에](https://ko.wikipedia.org/wiki/하드_디스크 "wikilink") 대한 [파티션 테이블](https://ko.wikipedia.org/wiki/파티션_테이블 "wikilink") 레이아웃 표준이다. [확장 펌웨어 인터페이스](https://ko.wikipedia.org/wiki/확장_펌웨어_인터페이스 "wikilink") (EFI) 표준([인텔](../Page/인텔.md "wikilink")이 [PC](../Page/개인용_컴퓨터.md "wikilink") [바이오스](../Page/바이오스.md "wikilink")를 대체하기 위하여 제안한 것)의 일부로 형성되어 있기는 하지만 [MBR](../Page/마스터_부트_레코드.md "wikilink") 파티션 테이블의 제한 때문에 일부 [바이오스](../Page/바이오스.md "wikilink") 시스템에 사용되기도 한다. MBR 파티션 테이블의 경우 하나의 디스크 파티션 크기를 최대 2.2 [TB](https://ko.wikipedia.org/wiki/테라바이트 "wikilink") (2.2 × 10<sup>12</sup> [바이트](../Page/바이트.md "wikilink"))).\[1\] 로 제한한다. GPT는 최대 디스크 및 파티션 크기를 9.4 [ZB](https://ko.wikipedia.org/wiki/제타바이트 "wikilink")(9.4 × 10<sup>21</sup> 바이트)까지 허용한다.\[2\]\[3\]

2010년을 기준으로 일반적인 시스템 간의 GPT에 대한 지원은 제한을 받는다.

## GPT의 운영 체제 지원

하이브리드 MBR은 표준이 아니며 운영 체제에 따라 다른 방식으로 해석한다. 아래에 아무런 언급이 없으면 운영 체제는 하이브리드 MBR 구성을 이용할 때 GPT 데이터에 우선 순위를 제공한다.

"이 아키텍처 및 버전에 대한 순수한 지원은 제공하지 않는다."는 다음과 같이 이해하여야 한다:

  -
    데이터 디스크로 지원하지 않는다\[4\], 보호 MBR에서 볼 수 있는 알려진 레거시 파티션만 운영 체제를 통해 접근할 수 있다. 탈착 가능한 디스크: MBR 파티션만 지원 안 함; 최종 사용자 응용으로 접근 권한이 없음. GPT가 포함된 순수 데이터는 낮은 수준의 디스크 접근을 위하여 서드 파티 관리자 도구를 통해 접근할 수 있다. 읽기 또는 읽기-쓰기 형태의 진정한 파일 시스템 수준 지원은 서드 파티 제조업체가 제공하는 소프트웨어에 종속된다.

### [유닉스 계열](../Page/유닉스_계열.md "wikilink") 운영 체제

<table>
<thead>
<tr class="header">
<th><p>운영 체제</p></th>
<th><p>버전/<br />
에디션</p></th>
<th><p>플랫폼</p></th>
<th><p>PC/BIOS 상의 GPT로부터 시동</p></th>
<th><p>EFI 상의 GPT로부터 시동</p></th>
<th><p>참고</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="../Page/FreeBSD.md" title="wikilink">FreeBSD</a></p></td>
<td><p>7.0 이후</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/x86" title="wikilink">x86</a>, <a href="https://ko.wikipedia.org/wiki/x86-64" title="wikilink">x86-64</a></p></td>
<td></td>
<td></td>
<td><p>하이브리드 구성에서 GPT와 MBR 파티션 식별자 모두 사용할 수 있다.</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/리눅스.md" title="wikilink">리눅스</a></p></td>
<td><p>대부분의 x86 리눅스 배포판<br />
<a href="https://ko.wikipedia.org/wiki/페도라_(운영_체제)" title="wikilink">페도라</a> 8 이상 및 <a href="../Page/우분투_(운영_체제).md" title="wikilink">우분투</a> 8.04 이상[5]</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/x86" title="wikilink">x86</a>, <a href="https://ko.wikipedia.org/wiki/x86-64" title="wikilink">x86-64</a>, <a href="https://ko.wikipedia.org/wiki/IA-64" title="wikilink">IA-64</a></p></td>
<td></td>
<td></td>
<td><p>fdisk와 같은 일부 배포 도구들은 GPT와 함께 동작하지 않는다. gdisk와 같은 새로운 도구[6], <a href="https://ko.wikipedia.org/wiki/Syslinux" title="wikilink">Syslinux</a>, <a href="https://ko.wikipedia.org/wiki/GNU_GRUB" title="wikilink">grub .96+ 패치</a>, <a href="https://ko.wikipedia.org/wiki/grub2" title="wikilink">grub2</a>은 GPT를 이용할 수 있다.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/Mac_OS_X" title="wikilink">Mac OS X</a></p></td>
<td><p>10.4.0 이후 (10.4.6 이후의 일부 기능)[7]</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/x86" title="wikilink">x86</a>, <a href="https://ko.wikipedia.org/wiki/x86-64" title="wikilink">x86-64</a></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/솔라리스_(운영_체제).md" title="wikilink">솔라리스</a></p></td>
<td><p>솔라리스 10 이후</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/x86" title="wikilink">x86</a>, <a href="https://ko.wikipedia.org/wiki/x86-64" title="wikilink">x86-64</a>, <a href="../Page/SPARC.md" title="wikilink">SPARC</a></p></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

### 32비트 윈도 버전

마이크로소프트는 32비트 플랫폼에서 EFI를 지원하지 않으며 더 나아가 GPT 파티션으로부터의 시동 또한 지원하지 않는다.

<table>
<thead>
<tr class="header">
<th><p>운영 체제</p></th>
<th><p>버전/<br />
에디션</p></th>
<th><p>플랫폼</p></th>
<th><p>PC/BIOS 상의 GPT로부터 시동</p></th>
<th><p>EFI 상의 GPT로부터 시동</p></th>
<th><p>참고</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/윈도_XP" title="wikilink">윈도 XP</a></p></td>
<td><p>(2001-10-25)</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/x86" title="wikilink">x86</a></p></td>
<td></td>
<td></td>
<td><p>이 아키텍처 및 버전에 대한 순수한 지원은 제공하지 않는다.</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/윈도_서버_2003" title="wikilink">윈도 서버 2003</a></p></td>
<td><p>(2003-04-24)</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/x86" title="wikilink">x86</a></p></td>
<td></td>
<td></td>
<td><p>이 아키텍처 및 버전에 대한 순수한 지원은 제공하지 않는다.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/윈도_서버_2003" title="wikilink">윈도 서버 2003</a></p></td>
<td><p>서비스 팩 1 (2005-03-30)</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/x86" title="wikilink">x86</a></p></td>
<td></td>
<td></td>
<td><p>데이터 디스크에만 지원.[8] MBR은 하이브리드 구성에서 우선 순위를 가진다.</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/윈도_비스타" title="wikilink">윈도 비스타</a></p></td>
<td><p>(2005-07-22)</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/x86" title="wikilink">x86</a></p></td>
<td></td>
<td></td>
<td><p>MBR은 하이브리드 구성에서 우선 순위를 가진다.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/윈도_서버_2008" title="wikilink">윈도 서버 2008</a></p></td>
<td><p>(2008-02-27)</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/x86" title="wikilink">x86</a></p></td>
<td></td>
<td></td>
<td><p>MBR은 하이브리드 구성에서 우선 순위를 가진다.</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/윈도_7" title="wikilink">윈도 7</a></p></td>
<td><p>(2009-10-22)</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/x86" title="wikilink">x86</a></p></td>
<td></td>
<td></td>
<td><p>MBR은 하이브리드 구성에서 우선 순위를 가진다.[9]</p></td>
</tr>
</tbody>
</table>

### 64비트 윈도 버전

다음의 표는 GPT를 지원하는 64비트 윈도 버전만을 나열한다.

<table>
<tbody>
<tr class="odd">
<td><p>운영 체제</p></td>
<td><p>버전/<br />
에디션</p></td>
<td><p>플랫폼</p></td>
<td><p>PC/BIOS 상의 GPT로부터 시동</p></td>
<td><p>EFI 상의 GPT로부터 시동</p></td>
<td><p>참고</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/윈도_XP" title="wikilink">윈도 XP</a></p></td>
<td><p>64비트 (2001-10-25)</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/IA-64" title="wikilink">IA-64</a></p></td>
<td></td>
<td></td>
<td><p>MBR은 하이브리드 구성에서 우선 순위를 가진다. 탈착 가능한 디스크: MBR 파티션만 지원.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/윈도_XP" title="wikilink">윈도 XP</a></p></td>
<td><p>64비트, 버전 2003 (2003-03-28)<br />
(윈도 서버 2003 64비트의 워크스테이션 제품)</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/IA-64" title="wikilink">IA-64</a></p></td>
<td></td>
<td></td>
<td><p>MBR은 하이브리드 구성에서 우선 순위를 가진다. 탈착 가능한 디스크: MBR 파티션만 지원.</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/윈도_서버_2003" title="wikilink">윈도 서버 2003</a></p></td>
<td><p>64비트 (2003-04-24)</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/IA-64" title="wikilink">IA-64</a></p></td>
<td></td>
<td></td>
<td><p>MBR은 하이브리드 구성에서 우선 순위를 가진다. 기본 파티션 동작은 GPT이다. "IA-64 시스템의 시동 디스크는 GPT 디스크여야 한다. IA-64 시스템에서 다른 디스크를 사용할 때에는 MBR이나 GPT를 사용할 수 있다.''[10]</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/윈도_서버_2003" title="wikilink">윈도 서버 2003</a></p></td>
<td><p>x64, 서비스 팩 1 (2005-03-30)</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/x86-64" title="wikilink">x86-64</a></p></td>
<td></td>
<td></td>
<td><p>데이터 디스크만 지원[11] MBR은 하이브리드 MBR 구성에서 우선 순위를 가진다.</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/윈도_XP" title="wikilink">윈도 XP</a></p></td>
<td><p>프로페셔널 x64 (2005-04-25)<br />
(윈도 서버 2003 x64의 워크스테이션 제품)</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/x86-64" title="wikilink">x86-64</a></p></td>
<td></td>
<td></td>
<td><p>데이터 디스크만 지원[12] MBR은 하이브리드 구성에서 우선 순위를 가진다. 탈착 가능한 디스크: MBR 파티션만 지원.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/윈도_비스타" title="wikilink">윈도 비스타</a></p></td>
<td><p>(2005-07-22)</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/x86-64" title="wikilink">x86-64</a></p></td>
<td></td>
<td></td>
<td><p>MBR은 하이브리드 구성에서 우선 순위를 가진다.</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/윈도_서버_2008" title="wikilink">윈도 서버 2008</a></p></td>
<td><p>(2008-02-27)</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/x86-64" title="wikilink">x86-64</a>, <a href="https://ko.wikipedia.org/wiki/IA-64" title="wikilink">IA-64</a></p></td>
<td></td>
<td></td>
<td><p>MBR은 하이브리드 구성에서 우선 순위를 가진다.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/윈도_7" title="wikilink">윈도 7</a></p></td>
<td><p>(2009-10-22)</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/x86-64" title="wikilink">x86-64</a></p></td>
<td></td>
<td></td>
<td><p>MBR은 하이브리드 구성에서 우선 순위를 가진다.[13]</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/윈도_서버_2008_R2" title="wikilink">윈도 서버 2008 R2</a></p></td>
<td><p>(2009-10-22)<br />
(윈도 7의 서버 제품)</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/x86-64" title="wikilink">x86-64</a>, <a href="https://ko.wikipedia.org/wiki/IA-64" title="wikilink">IA-64</a></p></td>
<td></td>
<td></td>
<td><p>MBR은 하이브리드 구성에서 우선 순위를 가진다.</p></td>
</tr>
</tbody>
</table>

## 파티션 유형 GUID

| 관련 운영 체제                                                                                                                  | 파티션 유형                                     | 전역 고유 식별자 (GUID)                                              |
| ------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------ | ------------------------------------------------------------- |
| *(없음)*                                                                                                                    | 사용하지 않는 항목                                 | `00000000-0000-0000-0000-000000000000`                        |
| MBR 파티션 구조                                                                                                                | `024DEE41-33E7-11D3-9D69-0008C781F39F`     |                                                               |
| [EFI 시스템 파티션](https://ko.wikipedia.org/wiki/EFI_시스템_파티션 "wikilink")                                                       | `C12A7328-F81F-11D2-BA4B-00A0C93EC93B`     |                                                               |
| [BIOS 시동 파티션](https://ko.wikipedia.org/wiki/BIOS_시동_파티션 "wikilink")                                                       | `21686148-6449-6E6F-744E-656564454649` |-  | [윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink")     |
| [기본 데이터 파티션](https://ko.wikipedia.org/wiki/기본_데이터_파티션 "wikilink")                                                         | `EBD0A0A2-B9E5-4433-87C0-68B6B72699C7`     |                                                               |
| [논리 디스크 관리자](https://ko.wikipedia.org/wiki/논리_디스크_관리자 "wikilink") 메타데이터 파티션                                               | `5808C8AA-7E8F-42E0-85D2-E1E90434CFB3`     |                                                               |
| [논리 디스크 관리자](https://ko.wikipedia.org/wiki/논리_디스크_관리자 "wikilink") 데이터 파티션                                                 | `AF9B60A0-1431-4F62-BC68-3311714A69AD`     |                                                               |
| [윈도 복구 환경](https://ko.wikipedia.org/wiki/윈도_복구_환경 "wikilink")                                                             | `DE94BBA4-06D1-4D40-A16A-BFD50179D6AC`     |                                                               |
| [IBM 일반 병렬 파일 시스템](https://ko.wikipedia.org/wiki/IBM_일반_병렬_파일_시스템 "wikilink") (GPFS) 파티션                                  | `37AFFC90-EF7D-4E96-91C3-2D7AE055B174`     |                                                               |
| [HP-UX](../Page/HP-UX.md "wikilink")                                                                                      | 데이터 파티션                                    | `75894C1E-3AEB-11D3-B7C1-7B03A0000000`                        |
| 서비스 파티션                                                                                                                   | `E2A1E728-32E3-11D6-A682-7B03A0000000` |-  | [리눅스](../Page/리눅스.md "wikilink")                              |
| RAID 파티션                                                                                                                  | `A19D880F-05FC-4D3B-A006-743F0F84911E`     |                                                               |
| 스왑 파티션                                                                                                                    | `0657FD6D-A4AB-43C4-84E5-0933C84B4F4F`     |                                                               |
| [논리 디스크 관리자](https://ko.wikipedia.org/wiki/논리_디스크_관리자_\(리눅스\) "wikilink") (LVM) 파티션                                       | `E6D6D379-F507-44C2-A23C-238F2A3DF928`     |                                                               |
| 예비                                                                                                                        | `8DA63339-0007-60C0-C436-083AC8230908` |-  | [FreeBSD](../Page/FreeBSD.md "wikilink")                      |
| 데이터 파티션                                                                                                                   | `516E7CB4-6ECF-11D6-8FF8-00022D09712B`     |                                                               |
| 스왑 파티션                                                                                                                    | `516E7CB5-6ECF-11D6-8FF8-00022D09712B`     |                                                               |
| [유닉스 파일 시스템](../Page/유닉스_파일_시스템.md "wikilink") (UFS) 파티션                                                                  | `516E7CB6-6ECF-11D6-8FF8-00022D09712B`     |                                                               |
| [바이넘 볼륨 관리자](https://ko.wikipedia.org/wiki/바이넘_볼륨_관리자 "wikilink") 파티션                                                     | `516E7CB8-6ECF-11D6-8FF8-00022D09712B`     |                                                               |
| [ZFS](../Page/ZFS.md "wikilink") 파티션                                                                                      | `516E7CBA-6ECF-11D6-8FF8-00022D09712B` |-  | [Mac OS X](https://ko.wikipedia.org/wiki/Mac_OS_X "wikilink") |
| [애플](https://ko.wikipedia.org/wiki/애플_\(기업\) "wikilink") [UFS](https://ko.wikipedia.org/wiki/Unix_File_System "wikilink") | `55465300-0000-11AA-AA11-00306543ECAC`     |                                                               |
| [애플](https://ko.wikipedia.org/wiki/애플_\(기업\) "wikilink") [APFS](../Page/애플_파일_시스템.md "wikilink")                          | `7C3457EF-0000-11AA-AA11-00306543ECAC`     |                                                               |
| [ZFS](../Page/ZFS.md "wikilink")                                                                                          | `6A898CC3-1DD2-11B2-99A6-080020736631`     |                                                               |
| 애플 RAID 파티션                                                                                                               | `52414944-0000-11AA-AA11-00306543ECAC`     |                                                               |
| 애플 RAID 파티션, 오프라인                                                                                                         | `52414944-5F4F-11AA-AA11-00306543ECAC`     |                                                               |
| 애플 시동 파티션                                                                                                                 | `426F6F74-0000-11AA-AA11-00306543ECAC`     |                                                               |
| 애플 레이블                                                                                                                    | `4C616265-6C00-11AA-AA11-00306543ECAC`     |                                                               |
| 애플 TV 복구 파티션                                                                                                              | `5265636F-7665-11AA-AA11-00306543ECAC` |-  | [솔라리스](../Page/솔라리스_\(운영_체제\).md "wikilink")                  |
| 루트 파티션                                                                                                                    | `6A85CF4D-1DD2-11B2-99A6-080020736631`     |                                                               |
| 스왑 파티션                                                                                                                    | `6A87C46F-1DD2-11B2-99A6-080020736631`     |                                                               |
| 백업 파티션                                                                                                                    | `6A8B642B-1DD2-11B2-99A6-080020736631`     |                                                               |
| /usr 파티션                                                                                                                  | `6A898CC3-1DD2-11B2-99A6-080020736631`     |                                                               |
| /var 파티션                                                                                                                  | `6A8EF2E9-1DD2-11B2-99A6-080020736631`     |                                                               |
| /home 파티션                                                                                                                 | `6A90BA39-1DD2-11B2-99A6-080020736631`     |                                                               |
| 대체 섹터                                                                                                                     | `6A9283A5-1DD2-11B2-99A6-080020736631`     |                                                               |
| 예비 파티션                                                                                                                    | `6A945A3B-1DD2-11B2-99A6-080020736631`     |                                                               |
| `6A9630D1-1DD2-11B2-99A6-080020736631`                                                                                    |                                            |                                                               |
| `6A980767-1DD2-11B2-99A6-080020736631`                                                                                    |                                            |                                                               |
| `6A96237F-1DD2-11B2-99A6-080020736631`                                                                                    |                                            |                                                               |
| `6A8D2AC7-1DD2-11B2-99A6-080020736631` |-                                                                                 | [NetBSD](../Page/NetBSD.md "wikilink")     | 스왑 파티션                                                        |
| [FFS](../Page/유닉스_파일_시스템.md "wikilink") 파티션                                                                               | <code>49F48D5A-B10E-11DC-B99B-0019D1879648 |                                                               |
| [LFS](https://ko.wikipedia.org/wiki/로그_구조_파일_시스템_\(BSD\) "wikilink") 파티션                                                  | <code>49F48D82-B10E-11DC-B99B-0019D1879648 |                                                               |
| RAID 파티션                                                                                                                  | <code>49F48DAA-B10E-11DC-B99B-0019D1879648 |                                                               |
| 중첩 파티션                                                                                                                    | <code>2DB519C4-B10F-11DC-B99B-0019D1879648 |                                                               |
| 암호화된 파티션                                                                                                                  | <code>2DB519EC-B10F-11DC-B99B-0019D1879648 |                                                               |

## 각주

<references />

## 같이 보기

  - [마스터 부트 레코드](../Page/마스터_부트_레코드.md "wikilink")
  - [전역 고유 식별자](../Page/전역_고유_식별자.md "wikilink") (GUID)
  - [확장 펌웨어 인터페이스](https://ko.wikipedia.org/wiki/확장_펌웨어_인터페이스 "wikilink") (EFI)
  - [디스크 파티션](https://ko.wikipedia.org/wiki/디스크_파티션 "wikilink")

## 외부 링크

  - Microsoft TechNet: [Disk Sectors on GPT Disks](https://web.archive.org/web/20080321063028/http://technet2.microsoft.com/windowsserver/en/library/bdeda920-1f08-4683-9ffb-7b4b50df0b5a1033.mspx?mfr=true)
  - Microsoft TechNet: [Using GPT Drives on x86-64 Systems](http://www.microsoft.com/whdc/device/storage/GPT-on-x64.mspx)
  - Apple Developer Connection: [Secrets of the GPT](http://developer.apple.com/technotes/tn2006/tn2166.html)
  - [Make the most of large drives with GPT and Linux](http://www.ibm.com/developerworks/linux/library/l-gpt/)
  - GPT fdisk : [Information on Hybrid GPT-MBR, Converting MBR and BSD disklabels to GPT and Booting from GPT disks](http://rodsbooks.com/gdisk/)
  - Microsoft : [FAQs on Using GPT disks in Windows](http://www.microsoft.com/whdc/device/storage/GPT_FAQ.mspx)
  - [A forum post describing steps to modify existing Windows x64 BIOS-MBR based installations to boot from UEFI-GPT](https://web.archive.org/web/20091120100508/http://www.insanelymac.com/forum/lofiversion/index.php/t186440.html)

[분류:바이오스](https://ko.wikipedia.org/wiki/분류:바이오스 "wikilink") [분류:부팅](https://ko.wikipedia.org/wiki/분류:부팅 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10. <http://codeidol.com/windows/inside-windows-server-2003/Configuring-Data-Storage/Working-with-GPT-Disks/>  Working with GPT Disks
11.
12.
13.