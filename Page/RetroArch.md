> This article is converted from Wikipedia: [RetroArch](https://ko.wikipedia.org/wiki/RetroArch).


**RetroArch**는 [libretro](https://ko.wikipedia.org/wiki/libretro "wikilink") [API](../Page/API.md "wikilink")의 참조 구현체이다.\[1\]\[2\] 자유 [오픈 소스](../Page/오픈_소스.md "wikilink"), [크로스 플랫폼](https://ko.wikipedia.org/wiki/크로스_플랫폼 "wikilink") 소프트웨어이며 [GNU 일반 공중 사용 허가서](../Page/GNU_일반_공중_사용_허가서.md "wikilink")(GPL)로 라이선스된다.

[에뮬레이터](../Page/에뮬레이터.md "wikilink"), [게임 엔진](../Page/게임_엔진.md "wikilink"), [비디오 게임](../Page/비디오_게임.md "wikilink"), [미디어 플레이어를](https://ko.wikipedia.org/wiki/디지털_미디어_플레이어 "wikilink") 위한 빠르고 가볍고 포팅 가능하고 의존성 없도록 설계된 [프런트엔드로](../Page/프런트엔드와_백엔드.md "wikilink") 기술된다.\[3\]

## 역사

원래 이름은 SSNES였으며, 처음에는 [byuu의](https://ko.wikipedia.org/wiki/higan "wikilink") libretro의 전신 libsnes에 기반을 두었으며\[4\] 2010년에 Hans-Kristian "themaister" Arntzen이 [깃허브](../Page/깃허브.md "wikilink")에 첫 변경사항을 커밋하면서 개발이 시작되었다.\[5\] [bsnes의](../Page/Higan.md "wikilink") [Qt](../Page/Qt_\(프레임워크\).md "wikilink") 기반 인터페이스를 대체하기 위해 개발되었으나\[6\] 더 많은 에뮬레이션 코어를 지원하는 수준으로 성장하였다. 2012년 4월 21일, SSNES는 공식적으로 명칭을\[7\] RetroArch로 변경하면서 이러한 방향 변화를 반영하였다.

## 지원 시스템

RetroArch는 어떠한 libretro 코어라도 구동할 수 있다. RetroArch가 여러 플랫폼을 지원하지만 특정 코어를 사용할 수 있는지의 여부는 플랫폼마다 다르다.

아래는 RetroArch에 사용할 수 있는 시스템 및 기반 코어에 대한 표이다:

<table>
<thead>
<tr class="header">
<th><p>시스템</p></th>
<th><p>기반</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="../Page/3DO_인터랙티브_멀티플레이어.md" title="wikilink">3DO</a></p></td>
<td><p>4DO</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/아케이드_게임.md" title="wikilink">Arcade</a></p></td>
<td><p><a href="../Page/MAME.md" title="wikilink">MAME</a> <a href="https://ko.wikipedia.org/wiki/MESS" title="wikilink">MESS</a></p>
<p>FinalBurnAlpha</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/아타리_2600.md" title="wikilink">아타리 2600</a></p></td>
<td><p>Stella</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/아타리_5200.md" title="wikilink">아타리 5200</a></p></td>
<td><p>Atari800</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/아타리_7800.md" title="wikilink">아타리 7800</a></p></td>
<td><p>ProSystem</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/아타리_재규어.md" title="wikilink">아타리 재규어</a></p></td>
<td><p>Virtual Jaguar</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/아타리_링크스.md" title="wikilink">아타리 링크스</a></p></td>
<td><p>Mednafen</p>
<p>Handy</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/아타리_팰컨" title="wikilink">아타리 팰컨</a></p></td>
<td><p>Hatari</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/동굴_이야기.md" title="wikilink">동굴 이야기</a></p></td>
<td><p>NXEngine</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/봄버맨" title="wikilink">봄버맨</a></p></td>
<td><p>Mr. Boom</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/CHIP-8" title="wikilink">CHIP-8</a></p></td>
<td><p>Emux</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/콜레코비전.md" title="wikilink">콜레코비전</a></p></td>
<td><p>blueMSX</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/둠_(1993년_비디오_게임).md" title="wikilink">코모도어 64</a></p></td>
<td><p>VICE</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/둠_(1993년_비디오_게임).md" title="wikilink">둠</a></p></td>
<td><p>PrBoom</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/드림캐스트.md" title="wikilink">드림캐스트</a></p></td>
<td><p>Redream Reicast</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/패미컴_디스크_시스템.md" title="wikilink">패미컴 디스크 시스템</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/Nestopia" title="wikilink">Nestopia</a></p>
<p><a href="../Page/Higan.md" title="wikilink">Higan</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/FFmpeg.md" title="wikilink">FFmpeg</a></p></td>
<td><p>FFmpeg</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/게임보이.md" title="wikilink">게임보이</a> / <a href="../Page/게임보이_컬러.md" title="wikilink">컬러</a></p></td>
<td><p>Emux Gambatte</p>
<p>SameBoy</p>
<p>TGB Dual</p>
<p><a href="../Page/Higan.md" title="wikilink">Higan</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/게임보이_어드밴스.md" title="wikilink">게임보이 어드밴스</a></p></td>
<td><p>Mednafen gpSP</p>
<p>Meteor</p>
<p>mGBA</p>
<p><a href="../Page/비주얼보이어드밴스.md" title="wikilink">비주얼보이어드밴스</a></p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/닌텐도_게임큐브.md" title="wikilink">닌텐도 게임큐브</a></p></td>
<td><p><a href="../Page/돌핀_(에뮬레이터).md" title="wikilink">돌핀</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/게임_기어.md" title="wikilink">게임 기어</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/제네시스_플러스" title="wikilink">제네시스 플러스 GX</a></p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/MSX.md" title="wikilink">MSX</a></p></td>
<td><p>fMSX blueMSX</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/네오지오_포켓.md" title="wikilink">네오지오 포켓</a> / <a href="../Page/네오지오_포켓_컬러.md" title="wikilink">컬러</a></p></td>
<td><p>Mednafen</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/NEC_PC-98" title="wikilink">NEC PC-98</a></p></td>
<td><p>Neko Project II</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/닌텐도_64.md" title="wikilink">닌텐도 64</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/Mupen64Plus" title="wikilink">Mupen64Plus</a></p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/패밀리_컴퓨터.md" title="wikilink">패밀리 컴퓨터</a></p></td>
<td><p>higan <a href="https://ko.wikipedia.org/wiki/FCEUX" title="wikilink">Emux</a></p>
<p>FCEUmm</p>
<p><a href="https://ko.wikipedia.org/wiki/Nestopia" title="wikilink">Nestopia</a> UE</p>
<p>QuickNES</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/닌텐도_DS.md" title="wikilink">닌텐도 DS</a></p></td>
<td><p><a href="../Page/DeSmuME.md" title="wikilink">DeSmuME</a></p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/닌텐도_3DS.md" title="wikilink">닌텐도 3DS</a></p></td>
<td><p><a href="../Page/Citra.md" title="wikilink">Citra</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/마그나복스_오디세이².md" title="wikilink">마그나복스 오디세이²</a></p></td>
<td><p><a href="../Page/마그나복스_오디세이².md" title="wikilink">마그나복스 오디세이²</a></p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/PC-FX.md" title="wikilink">PC-FX</a></p></td>
<td><p>Mednafen</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/슈퍼_32X.md" title="wikilink">슈퍼 32X</a></p></td>
<td><p>Picodrive</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/메가_CD.md" title="wikilink">메가 CD/세가 CD</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/제네시스_플러스" title="wikilink">제네시스 플러스 GX</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/메가_드라이브.md" title="wikilink">메가 드라이브/제네시스</a></p></td>
<td><p>제네시스 플러스 GX</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/세가_마스터_시스템.md" title="wikilink">세가 마스터 시스템</a></p></td>
<td><p>PicoDrive</p>
<p>Genesis Plus GX</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/플레이스테이션_포터블.md" title="wikilink">플레이스테이션 포터블</a></p></td>
<td><p><a href="../Page/PPSSPP.md" title="wikilink">PPSSPP</a></p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/플레이스테이션" title="wikilink">플레이스테이션</a></p></td>
<td><p>Mednafen PCSX ReARMed</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/포켓몬_미니" title="wikilink">포켓몬 미니</a></p></td>
<td><p>PokeMini</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/퀘이크_(비디오_게임).md" title="wikilink">퀘이크 1</a></p></td>
<td><p>TyrQuake</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/세가_새턴.md" title="wikilink">세가 새턴</a></p></td>
<td><p>Mednafen</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/슈퍼_패미컴.md" title="wikilink">슈퍼 NES</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/Bsnes" title="wikilink">Bsnes</a></p>
<p><a href="../Page/Higan.md" title="wikilink">Higan</a></p>
<p><a href="https://ko.wikipedia.org/wiki/Snes9x" title="wikilink">Snes9x</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/툼레이더_(1996년_비디오_게임).md" title="wikilink">툼 레이더</a></p></td>
<td><p>OpenLara</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/PC_엔진" title="wikilink">PC 엔진</a> / <a href="https://ko.wikipedia.org/wiki/PC_엔진_슈퍼그래픽스" title="wikilink">PC 엔진 슈퍼그래픽스</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/Mednafen" title="wikilink">Mednafen</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/PC_엔진" title="wikilink">PC 엔진</a></p></td>
<td><p>Mednafen</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/벡트렉스.md" title="wikilink">벡트렉스</a></p></td>
<td><p>VecXGL</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/버추얼_보이" title="wikilink">버추얼 보이</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/Mednafen" title="wikilink">Mednafen</a></p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/원더스완.md" title="wikilink">원더스완</a></p></td>
<td><p>Mednafen</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/ZX_스펙트럼.md" title="wikilink">ZX 스펙트럼</a></p></td>
<td><p>Fuse</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/ZX81.md" title="wikilink">ZX81</a></p></td>
<td><p>EightyOne</p></td>
</tr>
</tbody>
</table>

## 같이 보기

  - [비디오 게임 에뮬레이터 목록](../Page/비디오_게임_에뮬레이터_목록.md "wikilink")

## 각주

[분류:안드로이드 에뮬레이션 소프트웨어](https://ko.wikipedia.org/wiki/분류:안드로이드_에뮬레이션_소프트웨어 "wikilink") [분류:아케이드 에뮬레이터](https://ko.wikipedia.org/wiki/분류:아케이드_에뮬레이터 "wikilink") [분류:게임보이 어드밴스 에뮬레이터](https://ko.wikipedia.org/wiki/분류:게임보이_어드밴스_에뮬레이터 "wikilink") [분류:게임보이 에뮬레이터](https://ko.wikipedia.org/wiki/분류:게임보이_에뮬레이터 "wikilink") [분류:플레이스테이션 에뮬레이터](https://ko.wikipedia.org/wiki/분류:플레이스테이션_에뮬레이터 "wikilink")

1.  <https://github.com/libretro/RetroArch/blob/master/libretro-common/include/libretro.h>
2.  <https://github.com/libretro/libretro-samples>
3.
4.
5.
6.
7.