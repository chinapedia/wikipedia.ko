> This article is converted from Wikipedia: [메탈 \(API\)](https://ko.wikipedia.org/wiki/메탈_\(API\)).


**메탈**(Metal)은 부하가 적은 하드웨어 가속 그래픽 및 연산 [API](../Page/API.md "wikilink")로, [iOS 8에](https://ko.wikipedia.org/wiki/iOS_8 "wikilink") 처음 등장했다. 한 API에 [OpenGL](../Page/OpenGL.md "wikilink"), [OpenCL](../Page/OpenCL.md "wikilink")과 비슷한 기능을 병합하고 있다. 크로노스 그룹의 크로스 플랫폼 [벌컨](../Page/벌컨_\(API\).md "wikilink"), 마이크로소프트의 윈도우용 [Direct3D 12처럼](../Page/Direct3D.md "wikilink") 다른 플랫폼의 유사 API의 성능 이점 일부를 iOS에 가져오도록 설계되어 있다. 2015년 6월 8일 이후 메탈은 [애플 A7](../Page/애플_A7.md "wikilink") 이상을 이용하는 iOS 기기 및 [OS X 엘카피탠를](../Page/OS_X_엘카피탠.md "wikilink") 구동하는 2012년 이후 모델의 맥에서 이용이 가능하다. 또, 메탈은 연산 셰이더를 도입함으로써 [GPGPU](https://ko.wikipedia.org/wiki/GPGPU "wikilink") 프로그래밍 기능을 더 개선하였다.

메탈은 [C++11](../Page/C++11.md "wikilink") 기반의 [셰이딩 언어를](https://ko.wikipedia.org/wiki/셰이딩_언어 "wikilink") 이용하며, [클랭](../Page/클랭.md "wikilink")과 [LLVM](../Page/LLVM.md "wikilink")을 이용하여 구현되어 있다.\[1\]

OS X의 메탈 지원은 WWDC 2015에서 발표되었다.

## 성능

메탈은 몇 가지 이유로 [OpenGL](../Page/OpenGL.md "wikilink") 보다 더 나은 성능을 보여준다:

  - 미리 컴파일된 [셰이더](../Page/셰이더.md "wikilink")와 선행 상태 확인
  - [GPU](https://ko.wikipedia.org/wiki/GPU "wikilink")와 [CPU](https://ko.wikipedia.org/wiki/CPU "wikilink") 사이의 명확한 동기화
  - GPU와 CPU 간 공유 메모리 공간
  - 더 낮은 드라이버 부하\[2\]

이 요점들 중 일부는 CPU가 GPU 명령을 성공적으로 수행하는데 필요한 업무량을 제거해준다. 그 뒤 CPU가 다른 작업을 연산하는데 사용될 수 있으므로 전반적인 성능 향상을 가져다준다.

## 도입

애플에 따르면 2017년 6월 기준으로 148,000개 이상의 애플리케이션이 메탈을 직접 사용하며 1,700,000개가 하이레벨 [프레임워크를](../Page/애플리케이션_프레임워크.md "wikilink") 통해 이를 사용한다.\[3\]

<table>
<thead>
<tr class="header">
<th><p>타이틀</p></th>
<th><p>개발사 (macOS 버전)</p></th>
<th><p>게임 엔진</p></th>
<th><p>출시일 (macOS)</p></th>
<th><p>참고</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="../Page/도타_2.md" title="wikilink">도타 2</a></p></td>
<td><p><a href="../Page/밸브_코퍼레이션.md" title="wikilink">밸브 코퍼레이션</a></p></td>
<td><p><a href="../Page/소스_(게임_엔진).md" title="wikilink">소스 2</a></p></td>
<td><p>2013년 07월 18일</p></td>
<td><p>2018년 기준으로 Molten VK를 사용하여 메탈 위에 <a href="../Page/벌컨_(API).md" title="wikilink">벌컨</a> 지원을 제공한다[4]</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/F1_2016" title="wikilink">F1 2016</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/페럴_인터랙티브" title="wikilink">페럴 인터랙티브</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/EGO" title="wikilink">EGO Engine 4.0</a></p></td>
<td><p>2017년 04월 06일</p></td>
<td><p>시작 때부터 메탈을 지원</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/Total_War:_Warhammer" title="wikilink">Total War: Warhammer</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/페럴_인터랙티브" title="wikilink">페럴 인터랙티브</a></p></td>
<td><p>Total War Engine 3</p></td>
<td><p>2017년 4월 19일</p></td>
<td><p>시작 때부터 메탈을 지원</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/Warhammer_40,000:_Dawn_of_War_III" title="wikilink">Warhammer 40,000: Dawn of War III</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/페럴_인터랙티브" title="wikilink">페럴 인터랙티브</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/Essence_Engine" title="wikilink">Essence Engine 4</a></p></td>
<td><p>2017년 6월 9일</p></td>
<td><p>시작 때부터 메탈을 지원</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/Hitman" title="wikilink">Hitman</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/페럴_인터랙티브" title="wikilink">페럴 인터랙티브</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/IO_인터랙티브" title="wikilink">IO 인터랙티브</a></p></td>
<td><p>2017년 6월 20일</p></td>
<td><p>시작 때부터 메탈을 지원</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/BioShock:_The_Collection" title="wikilink">Bioshock Remastered</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/페럴_인터랙티브" title="wikilink">페럴 인터랙티브</a></p></td>
<td><p><a href="../Page/언리얼_엔진.md" title="wikilink">Unreal Engine 2.5</a></p></td>
<td><p>2017년 8월 22일</p></td>
<td><p>시작 때부터 메탈을 지원</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/F1_2017" title="wikilink">F1 2017</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/페럴_인터랙티브" title="wikilink">페럴 인터랙티브</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/EGO" title="wikilink">EGO Engine 4.0</a></p></td>
<td><p>2017년 8월 25일</p></td>
<td><p>시작 때부터 메탈을 지원</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/Deus_Ex:_Mankind_Divided" title="wikilink">Deus Ex: Mankind Divided</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/페럴_인터랙티브" title="wikilink">페럴 인터랙티브</a></p></td>
<td><p>Dawn Engine</p></td>
<td><p>2017년 12월 12일</p></td>
<td><p>시작 때부터 메탈을 지원</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/DiRT_Rally" title="wikilink">DiRT Rally</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/페럴_인터랙티브" title="wikilink">페럴 인터랙티브</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/EGO" title="wikilink">EGO Engine 2.5</a></p></td>
<td><p>2017년 11월 16일</p></td>
<td><p>시작 때부터 메탈을 지원</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/Ballistic_Overkill" title="wikilink">Ballistic Overkill</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/Aquiris_Game_Studio" title="wikilink">Aquiris Game Studio</a></p></td>
<td><p><a href="../Page/유니티_(게임_엔진).md" title="wikilink">Unity Engine 5</a></p></td>
<td><p>2017년 3월 28일</p></td>
<td><p>시작 때부터 메탈을 지원</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/마피아_III.md" title="wikilink">마피아 III</a></p></td>
<td><p><a href="../Page/Aspyr.md" title="wikilink">Aspyr</a></p></td>
<td><p>Illusion Engine</p></td>
<td><p>2017년 5월 11일</p></td>
<td><p>시작 때부터 메탈을 지원</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/월드_오브_워크래프트.md" title="wikilink">월드 오브 워크래프트</a></p></td>
<td><p><a href="../Page/블리자드_엔터테인먼트.md" title="wikilink">블리자드 엔터테인먼트</a></p></td>
<td><p>WoW Engine</p></td>
<td><p>2004년 11월 23일</p></td>
<td><p>메탈 지원 시점: 2016년 8월</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/스타크래프트_II:_자유의_날개.md" title="wikilink">스타크래프트 II: 자유의 날개</a></p></td>
<td><p><a href="../Page/블리자드_엔터테인먼트.md" title="wikilink">블리자드 엔터테인먼트</a></p></td>
<td><p>SC2 Engine</p></td>
<td><p>2010년 7월 27일</p></td>
<td><p>메탈 베타 지원 시점: 2017년 1월 24일</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/히어로즈_오브_더_스톰.md" title="wikilink">히어로즈 오브 더 스톰</a></p></td>
<td><p><a href="../Page/블리자드_엔터테인먼트.md" title="wikilink">블리자드 엔터테인먼트</a></p></td>
<td><p>SC2 Engine</p></td>
<td><p>2015년 6월 2일</p></td>
<td><p>메탈 베타 지원 시점: 2017년 1월 24일. 2017년 9월 29일 블리자드는 <a href="http://us.battle.net/heroes/en/blog/21273597/heroes-of-the-storm-balance-patch-notes-november-29-2017-11-29-2017">일시적으로</a> 메타 지원을 제거함.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/Fortnite" title="wikilink">Fortnite</a></p></td>
<td><p><a href="../Page/에픽게임즈.md" title="wikilink">에픽게임즈</a></p></td>
<td><p><a href="../Page/언리얼_엔진.md" title="wikilink">Unreal Engine 4</a></p></td>
<td><p>2017년 7월 25일</p></td>
<td><p>시작 때부터 메탈을 지원</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/Obduction" title="wikilink">Obduction</a></p></td>
<td><p><a href="../Page/사이언_월드.md" title="wikilink">사이언 월드</a></p></td>
<td><p><a href="../Page/언리얼_엔진.md" title="wikilink">Unreal Engine 4</a></p></td>
<td><p>2017년 3월 29일</p></td>
<td><p>시작 때부터 메탈을 지원</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/Everspace" title="wikilink">Everspace</a></p></td>
<td><p>Rockfish</p></td>
<td><p><a href="../Page/언리얼_엔진.md" title="wikilink">Unreal Engine 4</a></p></td>
<td><p>2017년 5월 26일</p></td>
<td><p>시작 때부터 메탈을 지원</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/아크_서바이벌_이볼브드.md" title="wikilink">아크 서바이벌 이볼브드</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/Studio_Wildcard" title="wikilink">Studio Wildcard</a></p></td>
<td><p><a href="../Page/언리얼_엔진.md" title="wikilink">Unreal Engine 4</a></p></td>
<td><p>2017년 8월 29일</p></td>
<td><p>시작 때부터 메탈을 지원</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/Observer" title="wikilink">Observer</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/Bloober_Team" title="wikilink">Bloober Team</a></p></td>
<td><p><a href="../Page/언리얼_엔진.md" title="wikilink">Unreal Engine 4</a></p></td>
<td><p>2017년 10월 24일</p></td>
<td><p>시작 때부터 메탈을 지원</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/언리얼_토너먼트.md" title="wikilink">언리얼 토너먼트</a></p></td>
<td><p><a href="../Page/에픽게임즈.md" title="wikilink">에픽게임즈</a></p></td>
<td><p><a href="../Page/언리얼_엔진.md" title="wikilink">Unreal Engine 4</a></p></td>
<td></td>
<td><p>메탈 지원 시점: 2017년 1월</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/Refunct" title="wikilink">Refunct</a></p></td>
<td><p>Dominique Grieshofer</p></td>
<td><p><a href="../Page/언리얼_엔진.md" title="wikilink">Unreal Engine 4</a></p></td>
<td><p>2016년 9월 5일</p></td>
<td><p>시작 때부터 메탈을 지원</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/시티즈:_스카이라인.md" title="wikilink">시티즈: 스카이라인</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/패러독스_인터랙티브" title="wikilink">패러독스 인터랙티브</a></p></td>
<td><p><a href="../Page/유니티_(게임_엔진).md" title="wikilink">Unity Engine 5</a></p></td>
<td><p>2015년 3월 10일</p></td>
<td><p>메탈 지원 시점: 2017년 5월 18일</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/유니버스_샌드박스.md" title="wikilink">유니버스 샌드박스</a></p></td>
<td><p>Giant Army</p></td>
<td><p><a href="../Page/유니티_(게임_엔진).md" title="wikilink">Unity Engine 5</a></p></td>
<td></td>
<td><p>메탈 베타 지원 시점: 2017년 6월</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/워_썬더.md" title="wikilink">워 썬더</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/가이진_엔터테인먼트" title="wikilink">가이진 엔터테인먼트</a></p></td>
<td><p>Dagor Engine 4</p></td>
<td><p>2012년 11월 1일</p></td>
<td><p>메탈 지원 시점: 2017년 5월 24일</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/The_Witness_(2016_video_game)" title="wikilink">The Witness</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/Thekla,_Inc" title="wikilink">Thekla, Inc</a></p></td>
<td><p>Thekla Engine</p></td>
<td><p>2017년 3월 8일</p></td>
<td><p>시작 때부터 메탈을 지원</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/Micro_Machines_World_Series" title="wikilink">Micro Machines World Series</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/Virtual_Programming_(company)" title="wikilink">Virtual Programming</a></p></td>
<td><p><a href="../Page/유니티_(게임_엔진).md" title="wikilink">Unity Engine 5</a></p></td>
<td><p>2017년 6월 30일</p></td>
<td><p>시작 때부터 메탈을 지원</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/Guardians_of_the_Galaxy:_The_Telltale_Series" title="wikilink">Guardians of the Galaxy: The Telltale Series</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/텔테일_게임즈" title="wikilink">텔테일 게임즈</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/텔테일_게임즈" title="wikilink">텔테일 게임즈</a></p></td>
<td><p>2017년 4월 18일</p></td>
<td><p>시작 때부터 메탈을 지원</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/Batman:_The_Enemy_Within" title="wikilink">Batman: The Enemy Within</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/텔테일_게임즈" title="wikilink">텔테일 게임즈</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/텔테일_게임즈" title="wikilink">텔테일 게임즈</a></p></td>
<td><p>2017년 08월 08일</p></td>
<td><p>시작 때부터 메탈을 지원</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/마인크래프트:_스토리_모드.md" title="wikilink">마인크래프트: 스토리 모드</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/텔테일_게임즈" title="wikilink">텔테일 게임즈</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/텔테일_게임즈" title="wikilink">텔테일 게임즈</a></p></td>
<td><p>2017년 7월 11일</p></td>
<td><p>시작 때부터 메탈을 지원</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/ARMA_3" title="wikilink">ARMA 3</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/버추얼_프로그래밍" title="wikilink">버추얼 프로그래밍</a></p></td>
<td><p>Real Virtuality</p></td>
<td></td>
<td><p>메탈 베타 지원 시점: 2017년 9월 17일</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/X-Plane_(simulator)" title="wikilink">X-Plane 11</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/Laminar_Research" title="wikilink">Laminar Research</a></p></td>
<td><p>Custom engine</p></td>
<td><p>2017년 5월 30일</p></td>
<td><p>메탈 지원 예정</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/Headlander" title="wikilink">Headlander</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/Double_Fine_Productions" title="wikilink">Double Fine Productions</a></p></td>
<td><p>Buddha Engine</p></td>
<td><p>2016년 11월 18일</p></td>
<td><p>시작 때부터 메탈을 지원</p></td>
</tr>
</tbody>
</table>

## 같이 보기

  - [Direct3D](../Page/Direct3D.md "wikilink") – [DirectX 12는](https://ko.wikipedia.org/wiki/DirectX#DirectX_12 "wikilink") 저급(로우 레벨) API를 도입하고 있다.
  - [글라이드](../Page/글라이드.md "wikilink") – 지금은 파산한 [3dfx](../Page/3dfx.md "wikilink")의 다른 로우레벨 API
  - [맨틀](../Page/맨틀_\(API\).md "wikilink") – [AMD](https://ko.wikipedia.org/wiki/AMD "wikilink")의 로우레벨 API
  - [벌컨](../Page/벌컨_\(API\).md "wikilink") – 부하가 적은 API로서 OpenGL을 계승한다.

## 참고문헌

## 외부 링크

  - [메탈 프로그래밍 가이드](https://developer.apple.com/library/prerelease/ios/documentation/Miscellaneous/Conceptual/MetalProgrammingGuide/Introduction/Introduction.html#//apple_ref/doc/uid/TP40014221) (예비)

  - [WWDC14 데모](https://www.youtube.com/watch?v=NRoGwuSDh3E); [확장판](https://www.youtube.com/watch?v=Br7qVnzxzv8#t=1013)

[분류:2014년 출시](https://ko.wikipedia.org/wiki/분류:2014년_출시 "wikilink") [분류:그래픽 라이브러리](https://ko.wikipedia.org/wiki/분류:그래픽_라이브러리 "wikilink") [분류:iOS](https://ko.wikipedia.org/wiki/분류:iOS "wikilink")

1.
2.  <http://blogs.unity3d.com/2014/07/03/metal-a-new-graphics-api-for-ios-8/>
3.
4.