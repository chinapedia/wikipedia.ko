> This article is converted from Wikipedia: [SSF \(에뮬레이터\)](https://ko.wikipedia.org/wiki/SSF_\(에뮬레이터\)).


**SSF**는 [DirectX](../Page/DirectX.md "wikilink") 9.0c를 사용하는 [윈도용](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") [세가 새턴](../Page/세가_새턴.md "wikilink") [에뮬레이터](../Page/에뮬레이터.md "wikilink")이다. 이 프로그램의 최신 버전은 세가 새턴 하드웨어를 거의 완벽히 구현했다고 알려져 있으며 새턴 기반의 [세가 타이탄 비디오](../Page/ST-V.md "wikilink") 업소용 게임기 또한 에뮬레이션할 수 있다. 대부분의 에뮬레이터처럼 게임 CD나 [디스크 이미지는](../Page/디스크_이미지.md "wikilink") 포함되어 있지 않으며, 별도로 보유하고 있어야 한다. [바이오스](../Page/바이오스.md "wikilink")도 포함되어 있지 않다. 그러나 0.07 Beta R3 버전부터는 바이오스 없이도 게임을 구동할 수 있다. 바이오스 파일의 사용은 선택 사항이지만 호환성을 높여주기 때문에 사용을 권장하며, 세가 새턴의 내장 메모리의 내용 관리나 시스템 시간 설정 같은 작업을 위해서 필요하다.

## 개요

이 에뮬레이터는 [스캔라인](https://ko.wikipedia.org/wiki/스캔라인 "wikilink")을 적용하거나 하지 않은 채 전체화면으로 실행될 수 있다. [화면 해상도는](https://ko.wikipedia.org/wiki/화면_해상도 "wikilink") 전체화면이든 아니든 간에 새턴의 일반적인 해상도인 320x240의 두 배인 640x480으로 고정되는데, 두 배 크기의 픽셀로 랜더링되기 때문에 기술적으로 해상도는 똑같다. 마찬가지로 352x240 해상도를 사용하는 게임의 경우 704x480으로 잡아늘려진다. 전체화면 상태에서 에뮬레이터는 가용한 해상도 중에서 에뮬레이션할 화면과 가장 가까운 해상도를 사용하게 되며, 따라서 704x480 해상도를 사용하는 게임은 주로 PC에서 DVD를 볼 때 사용하는 720x480 해상도를 사용하게 되며 좌우에 작은 테두리가 생기게 된다.

물론 비디오카드 드라이버나 다른 유틸리티를 사용해 사용자 설정 해상도를 추가함으로써 전체화면 출력이 704x480 해상도로 이루어지도록 만들 수는 있다. 사용자는 또한 [Vsync를](https://ko.wikipedia.org/wiki/수직_동기화 "wikilink") 켜고 끄거나 더 나은 성능을 얻기 위해 [DirectDraw](https://ko.wikipedia.org/wiki/DirectDraw "wikilink") 디스플레이를 켜고 끌 수 있다. 이미지 랜더링은 소프트웨어로 이루어지기 때문에 고성능 3D 기능을 가진 비디오 카드를 사용하여도 성능 향상을 기대하기는 힘들다.

SSF를 실행하기 위해서는 [DirectX](../Page/DirectX.md "wikilink") 8 호환 [그래픽 카드와](../Page/그래픽_카드.md "wikilink") 최소 256MB의 [RAM](https://ko.wikipedia.org/wiki/RAM "wikilink")이 필요하며, 제 속도를 내려면 3GHz 이상의 속도를 가진 CPU가 필요하다. 이보다 느린 CPU를 가진 컴퓨터에서 게임은 느리게 실행된다. 에뮬레이터는 이 문제를 제 속도를 내기 위해 프레임을 건너뛰거나, 게임이 느려지는 걸 감수하고라도 모든 프레임을 다 보여주는 두 가지 방식으로 해결할 수 있으며, 어느 쪽이든 옵션을 조절해 선택할 수 있다. 또한 SSF는 복수의 스레드를 사용해 새턴의 각 하드웨어 부분을 에뮬레이션할 수 있기 때문에, 인텔의 [코어 듀오나](https://ko.wikipedia.org/wiki/코어_듀오 "wikilink") AMD의 [애슬론 64 X2](../Page/애슬론_64_X2.md "wikilink") 같은 멀티코어 CPU를 사용할 경우 효과를 볼 수 있다.

**SSF는 [SSE2](../Page/SSE2.md "wikilink") 명령어 집합을 사용하기 때문에, [펜티엄 4](../Page/펜티엄_4.md "wikilink"), [펜티엄 M](../Page/펜티엄_M.md "wikilink"), [옵테론](../Page/옵테론.md "wikilink"), [애슬론 64](../Page/애슬론_64.md "wikilink"), [셈프론](../Page/셈프론.md "wikilink") (64비트), [튜리온 64](https://ko.wikipedia.org/wiki/튜리온_64 "wikilink") 이후에 나온 프로세서에서만 실행된다.**

### 주요 키 할당

#### 조작키(기본값)

<table>
<tbody>
<tr class="odd">
<td><p>상하좌우 방향키</p></td>
<td><p>커서키</p></td>
</tr>
<tr class="even">
<td><p>A, B, C 버튼</p></td>
<td><p>, ,  키</p></td>
</tr>
<tr class="odd">
<td><p>X, Y, Z 버튼</p></td>
<td><p>, ,  키</p></td>
</tr>
<tr class="even">
<td><p>L, R 버튼</p></td>
<td><p>,  키</p></td>
</tr>
<tr class="odd">
<td><p>START</p></td>
<td><p>키</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
</tr>
</tbody>
</table>

#### 기능키(변경불가)

<table>
<tbody>
<tr class="odd">
<td><p>CD 열기 / 닫기</p></td>
<td><p>/  키</p></td>
</tr>
<tr class="even">
<td><p>하드 리셋</p></td>
<td><p>{{키눌림|F4} 키</p></td>
</tr>
<tr class="odd">
<td><p>Scanline의 ON/OFF</p></td>
<td><p>키</p></td>
</tr>
<tr class="even">
<td><p>Sound의 ON/OFF</p></td>
<td><p>키</p></td>
</tr>
<tr class="odd">
<td><p>상태 로드</p></td>
<td><p>키</p></td>
</tr>
<tr class="even">
<td><p>상태 저장</p></td>
<td><p>+  키</p></td>
</tr>
<tr class="odd">
<td><p>화면 저장(BMP)</p></td>
<td><p>키</p></td>
</tr>
<tr class="even">
<td><p>사운드 녹음</p></td>
<td><p>키</p></td>
</tr>
<tr class="odd">
<td><p>창/전체화면 전환</p></td>
<td><p>+  키</p></td>
</tr>
<tr class="even">
<td><p>종료</p></td>
<td><p>키</p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
</tr>
</tbody>
</table>

## 최소 시스템 요구사항

|          |                                                                                                                                                                                     |
| -------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **프로세서** | [SSE2](../Page/SSE2.md "wikilink")를 지원하는 x86 호환 CPU                                                                                                                                 |
| **RAM**  | 256 [MB](../Page/메가바이트.md "wikilink") [RAM](https://ko.wikipedia.org/wiki/RAM "wikilink")                                                                                           |
| **비디오**  | [다이렉트X](../Page/DirectX.md "wikilink") 9c 호환                                                                                                                                        |
| **사운드**  | 다이렉트X 9c 호환                                                                                                                                                                         |
| **운영체제** | [윈도 XP](https://ko.wikipedia.org/wiki/윈도_XP "wikilink"), [윈도 비스타](https://ko.wikipedia.org/wiki/윈도_비스타 "wikilink"), [윈도 7](https://ko.wikipedia.org/wiki/윈도_7 "wikilink") 각 32/64비트 |
|          |                                                                                                                                                                                     |

## 권장 시스템 사양

|          |                                                                                                                                                                                     |
| -------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **프로세서** | [인텔 코어 2 듀오](https://ko.wikipedia.org/wiki/인텔_코어_2_듀오 "wikilink") 또는 [애슬론 64 X2](../Page/애슬론_64_X2.md "wikilink") 4800+                                                             |
| **RAM**  | 512 [MB](../Page/메가바이트.md "wikilink") [듀얼 채널](https://ko.wikipedia.org/wiki/듀얼_채널 "wikilink") [RAM](https://ko.wikipedia.org/wiki/RAM "wikilink")                                   |
| **비디오**  | 다이렉트X 9c 호환                                                                                                                                                                         |
| **사운드**  | 다이렉트X 9c 호환                                                                                                                                                                         |
| **운영체제** | [윈도 XP](https://ko.wikipedia.org/wiki/윈도_XP "wikilink"), [윈도 비스타](https://ko.wikipedia.org/wiki/윈도_비스타 "wikilink"), [윈도 7](https://ko.wikipedia.org/wiki/윈도_7 "wikilink") 각 32/64비트 |
|          |                                                                                                                                                                                     |

## 외부 링크

  - [Official SSF homepage](https://web.archive.org/web/20140712083202/http://www.geocities.jp/mj3kj8o5/ssf/index.html)

  - [SSF Tribute Neo, Translations, Screenshots, Compatibility list & Archive](http://evilboris.sonic-cult.net/SSF/)

  - [호환 소프트웨어 목록](http://www.segasaturn.org/)

[분류:세가 새턴 에뮬레이터](https://ko.wikipedia.org/wiki/분류:세가_새턴_에뮬레이터 "wikilink") [분류:윈도우 에뮬레이션 소프트웨어](https://ko.wikipedia.org/wiki/분류:윈도우_에뮬레이션_소프트웨어 "wikilink") [분류:에뮬레이션 소프트웨어](https://ko.wikipedia.org/wiki/분류:에뮬레이션_소프트웨어 "wikilink")