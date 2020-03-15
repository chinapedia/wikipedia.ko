> This article is converted from Wikipedia: [VM](https://ko.wikipedia.org/wiki/VM).


[섬네일](https://ko.wikipedia.org/wiki/파일:ScummVM_Windows_Screenshot.png "wikilink").\]\] **스컴VM**(ScummVM, Script Creation Utility for Maniac Mansion Virtual Machine)은 [게임 엔진 레크리에이션의](https://ko.wikipedia.org/wiki/게임_엔진_레크리에이션 "wikilink") 총집합이다. 원래 [스컴](https://ko.wikipedia.org/wiki/스컴 "wikilink")(SCUMM) 시스템을 이용하는 [루카스아츠 어드벤처 게임을](https://ko.wikipedia.org/wiki/루카스아츠_어드벤처_게임 "wikilink") 즐기기 위해 설계되었으나(여기서 VM은 [가상 머신의](../Page/가상_머신.md "wikilink") 이름에서 따온 것) 이제는 SCUMM 게임이 아니더라도 [레볼루션 소프트웨어와](https://ko.wikipedia.org/wiki/레볼루션_소프트웨어 "wikilink") [어드벤처 소프트와](https://ko.wikipedia.org/wiki/어드벤처_소프트 "wikilink") 같은 기업의 게임도 지원한다. [루드윅 스트라이저스](https://ko.wikipedia.org/wiki/루드윅_스트라이저스 "wikilink")(Ludvig Strigeus)가 처음 개발하였다.\[1\] [GNU 일반 공중 사용 허가서로](https://ko.wikipedia.org/wiki/GNU_일반_공중_사용_허가서 "wikilink") 배포된 스컴VM은 [자유 소프트웨어이다](https://ko.wikipedia.org/wiki/자유_소프트웨어 "wikilink").

스컴VM은 게임이 실행되는 하드웨어를 에뮬레이트하는 대신에 게임에서 게임 세계를 기술하기 위해 사용되는 [스크립트 언어를](../Page/스크립트_언어.md "wikilink") [인터프리트하는데](https://ko.wikipedia.org/wiki/인터프리터 "wikilink") 쓰이는 [소프트웨어](https://ko.wikipedia.org/wiki/소프트웨어 "wikilink") 일부를 재구현한 것이다. 그러므로 스컴VM은 원래 출시된 [플랫폼](../Page/컴퓨팅_플랫폼.md "wikilink") 외의 플랫폼에서도 게임 플레이를 지원할 수 있다.

개발팀은 버그 수정과 번역 등 개선들도 추가하고 있으며\[2\] 재출시와 관련하여 [GOG.com](../Page/GOG.com.md "wikilink") 등 상용 기업과도 작업하고 있다\[3\].

## 기능

스컴VM은 [가상 머신을](../Page/가상_머신.md "wikilink") 통해 수많은 어드벤처 게임 엔진을 지원하는 프로그램이며 사용자는 선택한 플랫폼에서 지원되는 어드벤처 게임을 플레이할 수 있다. 스컴VM은 게임이 지원하는 게임의 오리지널 자산 중 어느 것도 제공하지 않으며 소프트웨어의 합법적 이용을 위해 사용자가 오리지널 게임 매체를 가지고 있다는 전제를 가진다. 공식 프로젝트 웹사이트는 스컴VM과 직접 동작하는 [프리웨어](https://ko.wikipedia.org/wiki/프리웨어 "wikilink") 성격의 게임들을 제공한다. 게임 에뮬레이션 외에 스컴VM을 통해 플레이어는 언제든지 에뮬레이터의 상태를 저장하고 불러오는 것이 가능하며 에뮬레이트되는 게임이 제공하는 것 이상의 세이브 시스템을 실현한다. 터치스크린이 있는 모바일 장치 등 오리지널 게임에서 동작할 수 있도록 더 새로운 장치를 위한 컨트롤을 제공하는 작업이 시작되었다.\[4\]

스컴VM이 [게임 에뮬레이터와](../Page/비디오_게임_콘솔_에뮬레이터.md "wikilink") 동등한 기능을 제공하는 것처럼 보이지만 스컴VM 팀은 그러한 방식을 고려하고 있지 않다. 에뮬레이션에 의존할 수 밖에 없는 오디오 엔진 등 일부 하위 시스템 외에도 스컴VM은 더 오래된 언어의 게임 엔진을 이식성이 더 좋은 [C++](https://ko.wikipedia.org/wiki/C++ "wikilink") 코드로 재창조함으로써 게임 자산의 고급 [명령 코드가](https://ko.wikipedia.org/wiki/명령_코드 "wikilink") 오리지널 릴리스에서와 동일한 방식으로 실행이 가능하게 되었으며 스컴VM을 수많은 플랫폼으로 이식하는데 도움을 주었다. 스컴VM 팀은 단순히 [도스박스](../Page/도스박스.md "wikilink")와 같은 운영 체제 에뮬레이터를 통해 오래된 게임과 실행 파일을 실행하는 것보다 자신들의 이 방식이 더 나은 개선책이라 생각하고 있는데, 스컴VM의 구현체들은 더 가볍고 더 적은 처리 파워와 메모리를 요구하므로 모바일 장치 등 처리에 제약이 있는 환경에서의 이용을 가능케 한다.\[5\]

### 이식

[이식은](https://ko.wikipedia.org/wiki/이식_\(컴퓨팅\) "wikilink") 이 프로젝트의 설계적 목표이다.\[6\] 스컴VM의 포팅은 [마이크로소프트 윈도우](https://ko.wikipedia.org/wiki/마이크로소프트_윈도우 "wikilink"), [macOS](https://ko.wikipedia.org/wiki/macOS "wikilink"), 그리고 다양한 [유닉스 계열](../Page/유닉스_계열.md "wikilink") 시스템(예: RPM/데비안/소스 기반의 [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink"), [FreeBSD](https://ko.wikipedia.org/wiki/FreeBSD "wikilink")/[NetBSD](https://ko.wikipedia.org/wiki/NetBSD "wikilink")/[OpenBSD](https://ko.wikipedia.org/wiki/OpenBSD "wikilink")/[DragonFly BSD](https://ko.wikipedia.org/wiki/DragonFly_BSD "wikilink") 등 [BSD](https://ko.wikipedia.org/wiki/BSD "wikilink") 계열 멤버, [솔라리스](https://ko.wikipedia.org/wiki/솔라리스_\(운영_체제\) "wikilink"))으로 이용이 가능하다. 콘솔 시스템에도 이식되었다. 주류에서 조금 더 먼 개인용 컴퓨터 포팅으로는 [아미가](https://ko.wikipedia.org/wiki/아미가 "wikilink"), Atari-Free[MiNT](https://ko.wikipedia.org/wiki/MiNT "wikilink"), [하이쿠](../Page/하이쿠.md "wikilink")-[BeOS](https://ko.wikipedia.org/wiki/BeOS "wikilink")-[ZETA](https://ko.wikipedia.org/wiki/Magnussoft_ZETA "wikilink"), [RISC OS](https://ko.wikipedia.org/wiki/RISC_OS "wikilink"), [OS/2](https://ko.wikipedia.org/wiki/OS/2 "wikilink")가 포함된다.

다양한 [게임 콘솔에](../Page/비디오_게임_콘솔.md "wikilink") 공식 포트가 있다. 스컴VM은 [플레이스테이션 2](https://ko.wikipedia.org/wiki/플레이스테이션_2 "wikilink"), [드림캐스트](https://ko.wikipedia.org/wiki/드림캐스트 "wikilink"), [닌텐도 64](https://ko.wikipedia.org/wiki/닌텐도_64 "wikilink"), [게임큐브](https://ko.wikipedia.org/wiki/닌텐도_게임큐브 "wikilink"), [Wii](https://ko.wikipedia.org/wiki/Wii "wikilink"),\[7\] 등 게이밍 머신과 [GCW Zero](https://ko.wikipedia.org/wiki/GCW_Zero "wikilink"), [GP2X](https://ko.wikipedia.org/wiki/GP2X "wikilink"), [닌텐도 DS](https://ko.wikipedia.org/wiki/닌텐도_DS "wikilink"), [판도라](https://ko.wikipedia.org/wiki/판도라 "wikilink"), [플레이스테이션 포터블](https://ko.wikipedia.org/wiki/플레이스테이션_포터블 "wikilink"), [플레이스테이션 비타](https://ko.wikipedia.org/wiki/플레이스테이션_비타 "wikilink") 등 [휴대용 게임기에도](../Page/휴대용_게임기.md "wikilink") 이식되었다. 지원되는 [모바일 장치](https://ko.wikipedia.org/wiki/모바일_장치 "wikilink") 플랫폼에는 [팜 OS](https://ko.wikipedia.org/wiki/팜_OS "wikilink") [Tapwave Zodiac](https://ko.wikipedia.org/wiki/Tapwave_Zodiac "wikilink"), [심비안 OS](https://ko.wikipedia.org/wiki/심비안_OS "wikilink") ([UIQ](https://ko.wikipedia.org/wiki/UIQ "wikilink") 플랫폼, 노키아 [60](https://ko.wikipedia.org/wiki/노키아_시리즈_60 "wikilink"), [80](https://ko.wikipedia.org/wiki/노키아_시리즈_80 "wikilink"), [노키아 7710](https://ko.wikipedia.org/wiki/노키아_7710 "wikilink") [90](https://ko.wikipedia.org/wiki/노키아_시리즈_90 "wikilink") 전화 시리즈), 노키아의 [마에모](https://ko.wikipedia.org/wiki/마에모 "wikilink") ([Nokia 770](https://ko.wikipedia.org/wiki/Nokia_770 "wikilink"), [N800](https://ko.wikipedia.org/wiki/N800 "wikilink"), [노키아 N810에](https://ko.wikipedia.org/wiki/노키아_N810 "wikilink") 사용됨), 애플의 [아이폰](../Page/아이폰.md "wikilink"),\[8\] [MotoMAGX](https://ko.wikipedia.org/wiki/MotoMAGX "wikilink"), [MotoEZX](https://ko.wikipedia.org/wiki/MotoEZX "wikilink") 전화, [윈도우 모바일이](../Page/윈도우_모바일.md "wikilink") 포함된다. 비공식 스컴VM 포트 지원 플랫폼으로는 마이크로소프트의 [엑스박스](https://ko.wikipedia.org/wiki/엑스박스 "wikilink") 게이밍 콘솔, [블랙베리 플레이북](../Page/블랙베리_플레이북.md "wikilink"),\[9\] [Zaurus](https://ko.wikipedia.org/wiki/Zaurus "wikilink"), [Gizmondo](https://ko.wikipedia.org/wiki/Gizmondo "wikilink"), [GP32](https://ko.wikipedia.org/wiki/GP32 "wikilink") 포터블 디바이스 플랫폼이 포함된다. [안드로이드](https://ko.wikipedia.org/wiki/안드로이드_\(운영_체제\) "wikilink"),\[10\] [웹OS](https://ko.wikipedia.org/wiki/웹OS "wikilink")\[11\] 또는 비공식 삼성 바다 OS를 포함한 휴대 전화도 지원된다.

## 역사

스컴VM은 2001년 9월 컴퓨터 과학부 학생 루드윅 스트라이저스에 의해 개발되었다.

## 지원 게임

[섬네일](https://ko.wikipedia.org/wiki/파일:ScummVM_Windows_Screenshot.png "wikilink").\]\]

다음 게임은 현재의 스컴 VM 릴리스로의 빌드가 지원된다.\[12\]

### 루카스아츠 스컴 게임

  - [공포의 저택](https://ko.wikipedia.org/wiki/공포의_저택 "wikilink")
  - [Zak McKracken and the Alien Mindbenders](https://ko.wikipedia.org/wiki/Zak_McKracken_and_the_Alien_Mindbenders "wikilink")
  - [Indiana Jones and the Last Crusade: The Graphic Adventure](https://ko.wikipedia.org/wiki/Indiana_Jones_and_the_Last_Crusade:_The_Graphic_Adventure "wikilink")
  - [룸](https://ko.wikipedia.org/wiki/룸_\(비디오_게임\) "wikilink")
  - [원숭이 섬의 비밀](../Page/원숭이_섬의_비밀.md "wikilink")
  - [Monkey Island 2: LeChuck's Revenge](https://ko.wikipedia.org/wiki/Monkey_Island_2:_LeChuck's_Revenge "wikilink")
  - [Indiana Jones and the Fate of Atlantis](https://ko.wikipedia.org/wiki/Indiana_Jones_and_the_Fate_of_Atlantis "wikilink")
  - [텐타클 최후의 날](https://ko.wikipedia.org/wiki/텐타클_최후의_날 "wikilink")
  - [Sam & Max Hit the Road](https://ko.wikipedia.org/wiki/Sam_&_Max_Hit_the_Road "wikilink")
  - [풀 스로틀](https://ko.wikipedia.org/wiki/풀_스로틀_\(1995년_비디오_게임\) "wikilink")
  - [더 디그](https://ko.wikipedia.org/wiki/더_디그_\(비디오_게임\) "wikilink")
  - [원숭이 섬의 저주](https://ko.wikipedia.org/wiki/원숭이_섬의_저주 "wikilink")

### 시에라 온라인 게임

  - [The Beast Within: A Gabriel Knight Mystery](https://ko.wikipedia.org/wiki/The_Beast_Within:_A_Gabriel_Knight_Mystery "wikilink")
  - [The Black Cauldron](https://ko.wikipedia.org/wiki/타란의_대모험 "wikilink")
  - [Castle of Dr. Brain](https://ko.wikipedia.org/wiki/Castle_of_Dr._Brain "wikilink")
  - [Codename: ICEMAN](https://ko.wikipedia.org/wiki/Codename:_ICEMAN "wikilink")
  - [The Colonel's Bequest](https://ko.wikipedia.org/wiki/The_Colonel's_Bequest "wikilink")
  - [Conquests of Camelot: The Search for the Grail](https://ko.wikipedia.org/wiki/Conquests_of_Camelot:_The_Search_for_the_Grail "wikilink")
  - [Conquests of the Longbow: The Legend of Robin Hood](https://ko.wikipedia.org/wiki/Conquests_of_the_Longbow:_The_Legend_of_Robin_Hood "wikilink")
  - [The Dagger of Amon Ra](https://ko.wikipedia.org/wiki/The_Dagger_of_Amon_Ra "wikilink")
  - [EcoQuest: The Search for Cetus](https://ko.wikipedia.org/wiki/EcoQuest_-_The_Search_for_Cetus "wikilink")
  - [EcoQuest II: Lost Secret of the Rainforest](https://ko.wikipedia.org/wiki/EcoQuest2_-_Lost_Secret_of_the_Rainforest "wikilink")
  - [Freddy Pharkas: Frontier Pharmacist](https://ko.wikipedia.org/wiki/Freddy_Pharkas:_Frontier_Pharmacist "wikilink")
  - [Gabriel Knight: Sins of the Fathers](https://ko.wikipedia.org/wiki/Gabriel_Knight:_Sins_of_the_Fathers "wikilink")
  - [Gold Rush\!](https://ko.wikipedia.org/wiki/Gold_Rush! "wikilink")
  - [Hi-Res Adventure \#0: Mission Asteroid](https://ko.wikipedia.org/wiki/Mission_Asteroid "wikilink")
  - [Hi-Res Adventure \#1: Mystery House](https://ko.wikipedia.org/wiki/Mystery_House "wikilink")
  - [Hi-Res Adventure \#2: The Wizard and the Princess](https://ko.wikipedia.org/wiki/Wizard_and_the_Princess "wikilink")
  - [Hi-Res Adventure \#3: Cranston Manor](https://ko.wikipedia.org/wiki/Cranston_Manor "wikilink")
  - [Hi-Res Adventure \#4: Ulysses and the Golden Fleece](https://ko.wikipedia.org/wiki/Ulysses_and_the_Golden_Fleece "wikilink")
  - [Hi-Res Adventure \#5: Time Zone](https://ko.wikipedia.org/wiki/타임_존_\(비디오_게임\) "wikilink")
  - [Hi-Res Adventure \#6: The Dark Crystal](https://ko.wikipedia.org/wiki/다크_크리스탈_\(비디오_게임\) "wikilink")
  - [Hoyle's Official Book of Games](https://ko.wikipedia.org/wiki/Hoyle's_Official_Book_of_Games "wikilink"): Volume 1, Volume 2 and Volume 3
  - [The Island of Dr. Brain](https://ko.wikipedia.org/wiki/The_Island_of_Dr._Brain "wikilink")
  - [Jones in the Fast Lane](https://ko.wikipedia.org/wiki/Jones_in_the_Fast_Lane "wikilink")
  - [King's Quest: Quest for the Crown](https://ko.wikipedia.org/wiki/King's_Quest:_Quest_for_the_Crown "wikilink")
  - [King's Quest II: Romancing the Throne](https://ko.wikipedia.org/wiki/King's_Quest_II:_Romancing_the_Throne "wikilink")
  - [King's Quest III: To Heir Is Human](https://ko.wikipedia.org/wiki/King's_Quest_III:_To_Heir_Is_Human "wikilink")
  - [King's Quest IV: The Perils of Rosella](https://ko.wikipedia.org/wiki/King's_Quest_IV:_The_Perils_of_Rosella "wikilink")
  - [King's Quest V: Absence Makes the Heart Go Yonder\!](https://ko.wikipedia.org/wiki/King's_Quest_V:_Absence_Makes_the_Heart_Go_Yonder! "wikilink")
  - [King's Quest VI: Heir Today, Gone Tomorrow](https://ko.wikipedia.org/wiki/King's_Quest_VI:_Heir_Today,_Gone_Tomorrow "wikilink")
  - [King's Quest VII: The Princeless Bride](https://ko.wikipedia.org/wiki/King's_Quest_VII:_The_Princeless_Bride "wikilink")
  - [King's Questions](https://ko.wikipedia.org/wiki/King's_Questions "wikilink")
  - [Leisure Suit Larry in the Land of the Lounge Lizards](https://ko.wikipedia.org/wiki/Leisure_Suit_Larry_in_the_Land_of_the_Lounge_Lizards "wikilink")
  - [Leisure Suit Larry Goes Looking for Love (in Several Wrong Places)](https://ko.wikipedia.org/wiki/Leisure_Suit_Larry_Goes_Looking_for_Love_\(in_Several_Wrong_Places\) "wikilink")
  - [Leisure Suit Larry III: Passionate Patti in Pursuit of the Pulsating Pectorals](https://ko.wikipedia.org/wiki/Leisure_Suit_Larry_III:_Passionate_Patti_in_Pursuit_of_the_Pulsating_Pectorals "wikilink")
  - [Leisure Suit Larry 5: Passionate Patti Does a Little Undercover Work](https://ko.wikipedia.org/wiki/Leisure_Suit_Larry_5:_Passionate_Patti_Does_a_Little_Undercover_Work "wikilink")
  - [Leisure Suit Larry 6: Shape Up or Slip Out\!](https://ko.wikipedia.org/wiki/Leisure_Suit_Larry_6:_Shape_Up_or_Slip_Out! "wikilink")
  - [Leisure Suit Larry 7: Love for Sail\!](https://ko.wikipedia.org/wiki/Leisure_Suit_Larry:_Love_for_Sail! "wikilink")
  - [Lighthouse: The Dark Being](https://ko.wikipedia.org/wiki/Lighthouse:_The_Dark_Being "wikilink")
  - [Manhunter: New York](https://ko.wikipedia.org/wiki/Manhunter:_New_York "wikilink") ([Evryware](https://ko.wikipedia.org/wiki/Evryware "wikilink") 개발)
  - [Manhunter 2: San Francisco](https://ko.wikipedia.org/wiki/Manhunter_2:_San_Francisco "wikilink") (Evryware 개발)
  - [Mickey's Space Adventure](https://ko.wikipedia.org/wiki/Mickey's_Space_Adventure "wikilink")
  - [Mixed-Up Fairy Tales](https://ko.wikipedia.org/wiki/Mixed-Up_Fairy_Tales "wikilink")
  - [Mixed-Up Mother Goose](https://ko.wikipedia.org/wiki/Mixed-Up_Mother_Goose "wikilink")
  - [Pepper's Adventures in Time](https://ko.wikipedia.org/wiki/Pepper's_Adventures_in_Time "wikilink")
  - [판타스마고리아](https://ko.wikipedia.org/wiki/판타스마고리아_\(비디오_게임\) "wikilink")
  - [Phantasmagoria II: A Puzzle of Flesh](https://ko.wikipedia.org/wiki/Phantasmagoria:_A_Puzzle_of_Flesh "wikilink")
  - [Police Quest: In Pursuit of the Death Angel](https://ko.wikipedia.org/wiki/Police_Quest:_In_Pursuit_of_the_Death_Angel "wikilink")
  - [Police Quest II: The Vengeance](https://ko.wikipedia.org/wiki/Police_Quest_II:_The_Vengeance "wikilink")
  - [Police Quest III: The Kindred](https://ko.wikipedia.org/wiki/Police_Quest_III:_The_Kindred "wikilink")
  - [Police Quest IV: Open Season](https://ko.wikipedia.org/wiki/Police_Quest:_Open_Season "wikilink")
  - [Police Quest: SWAT](https://ko.wikipedia.org/wiki/Daryl_F._Gates'_Police_Quest:_SWAT "wikilink")
  - [Quest for Glory: So You Want to Be a Hero](https://ko.wikipedia.org/wiki/Quest_for_Glory:_So_You_Want_to_Be_a_Hero "wikilink")
  - [Quest for Glory II: Trial by Fire](https://ko.wikipedia.org/wiki/Quest_for_Glory_II:_Trial_by_Fire "wikilink")
  - [Quest for Glory III: Wages of War](https://ko.wikipedia.org/wiki/Quest_for_Glory_III:_Wages_of_War "wikilink")
  - [Quest for Glory IV: Shadows of Darkness](https://ko.wikipedia.org/wiki/Quest_for_Glory:_Shadows_of_Darkness "wikilink")
  - [라마](https://ko.wikipedia.org/wiki/라마_\(비디오_게임\) "wikilink")
  - [시버스](https://ko.wikipedia.org/wiki/시버스 "wikilink")
  - [Slater & Charlie Go Camping](https://ko.wikipedia.org/wiki/Slater_&_Charlie_Go_Camping "wikilink")
  - [Space Quest: The Sarien Encounter](https://ko.wikipedia.org/wiki/Space_Quest:_The_Sarien_Encounter "wikilink")
  - [Space Quest II: Vohaul's Revenge](https://ko.wikipedia.org/wiki/Space_Quest_II:_Vohaul's_Revenge "wikilink")
  - [Space Quest III: The Pirates of Pestulon](https://ko.wikipedia.org/wiki/Space_Quest_III:_The_Pirates_of_Pestulon "wikilink")
  - [Space Quest IV: Roger Wilco and The Time Rippers](https://ko.wikipedia.org/wiki/Space_Quest_IV:_Roger_Wilco_and_The_Time_Rippers "wikilink")
  - [Space Quest V: Roger Wilco – The Next Mutation](https://ko.wikipedia.org/wiki/Space_Quest_V:_Roger_Wilco_–_The_Next_Mutation "wikilink")
  - [Space Quest 6: Roger Wilco in The Spinal Frontier](https://ko.wikipedia.org/wiki/Space_Quest_6:_Roger_Wilco_in_The_Spinal_Frontier "wikilink")
  - [Torin's Passage](https://ko.wikipedia.org/wiki/Torin's_Passage "wikilink")
  - [Troll's Tale](https://ko.wikipedia.org/wiki/Troll's_Tale "wikilink")
  - [Winnie the Pooh in the Hundred Acre Wood](https://ko.wikipedia.org/wiki/Winnie_the_Pooh_in_the_Hundred_Acre_Wood "wikilink")

### Coktel Vision 게임

  - [Bargon Attack](https://ko.wikipedia.org/wiki/Bargon_Attack "wikilink")
  - [The Bizarre Adventures of Woodruff and the Schnibble](https://ko.wikipedia.org/wiki/The_Bizarre_Adventures_of_Woodruff_and_the_Schnibble "wikilink")
  - [패시네이션](https://ko.wikipedia.org/wiki/패시네이션_\(비디오_게임\) "wikilink")
  - [게이샤](https://ko.wikipedia.org/wiki/게이샤_\(비디오_게임\) "wikilink")
  - [Gobliiins](https://ko.wikipedia.org/wiki/Gobliiins "wikilink")
  - [Gobliins 2: The Prince Buffoon](https://ko.wikipedia.org/wiki/Gobliins_2_-_The_Prince_Buffoon "wikilink")
  - [Goblins Quest 3](https://ko.wikipedia.org/wiki/Gobliiins#Goblins_Quest_3 "wikilink")
  - [로스트 인 타임](https://ko.wikipedia.org/wiki/로스트_인_타임_\(비디오_게임\) "wikilink")
  - [Once Upon A Time: Little Red Riding Hood](https://ko.wikipedia.org/wiki/Once_Upon_A_Time:_Little_Red_Riding_Hood "wikilink")
  - [Playtoons: Bambou le Sauveur de la Jungle](https://ko.wikipedia.org/wiki/Playtoons:_Bambou_le_Sauveur_de_la_Jungle "wikilink")
  - [Urban Runner](https://ko.wikipedia.org/wiki/Urban_Runner "wikilink")
  - [Ween: The Prophecy](https://ko.wikipedia.org/wiki/Ween:_The_Prophecy "wikilink")

### 어드벤처소프트-호러소프트 게임

  - [엘비라: 미스트리스 오브 더 다크](https://ko.wikipedia.org/wiki/엘비라:_미스트리스_오브_더_다크 "wikilink")
  - [Elvira II: The Jaws of Cerberus](https://ko.wikipedia.org/wiki/Elvira_II:_The_Jaws_of_Cerberus "wikilink")
  - [The Feeble Files](https://ko.wikipedia.org/wiki/The_Feeble_Files "wikilink")
  - [Personal Nightmare](https://ko.wikipedia.org/wiki/Personal_Nightmare "wikilink")
  - [Simon the Sorcerer](https://ko.wikipedia.org/wiki/Simon_the_Sorcerer "wikilink")
  - [Simon the Sorcerer II: The Lion, the Wizard and the Wardrobe](https://ko.wikipedia.org/wiki/Simon_the_Sorcerer_II:_The_Lion,_the_Wizard_and_the_Wardrobe "wikilink")
  - [Simon the Sorcerer's Puzzle Pack](https://ko.wikipedia.org/wiki/Simon_the_Sorcerer's_Puzzle_Pack "wikilink")
  - [왁스웍스](https://ko.wikipedia.org/wiki/왁스웍스 "wikilink") (엘비라 3)

### Humongous Entertainment 게임

  - [Backyard Baseball](https://ko.wikipedia.org/wiki/Backyard_Baseball "wikilink")
  - [Backyard Baseball 2001](https://ko.wikipedia.org/wiki/Backyard_Baseball_2001 "wikilink")
  - [Backyard Baseball 2003](https://ko.wikipedia.org/wiki/Backyard_Baseball "wikilink")
  - [Backyard Football](https://ko.wikipedia.org/wiki/백야드_풋볼_\(1999년_비디오_게임\) "wikilink")
  - [Backyard Football 2002](https://ko.wikipedia.org/wiki/Backyard_Football_2002 "wikilink")
  - [Big Thinkers\! First Grade](https://ko.wikipedia.org/wiki/빅_싱커즈 "wikilink")
  - [Big Thinkers\! Kindergarten](https://ko.wikipedia.org/wiki/빅_싱커즈 "wikilink")
  - [Blue's 123 Time Activities](https://ko.wikipedia.org/wiki/Blue's_123_Time_Activities "wikilink")
  - [Blue's ABC Time Activities](../Page/블루스_클루스.md "wikilink")
  - [Blue's Art Time Activities](../Page/블루스_클루스.md "wikilink")
  - [Blue's Birthday Adventure](https://ko.wikipedia.org/wiki/Blue's_Birthday_Adventure "wikilink")
  - [Blue's Reading Time Activities](../Page/블루스_클루스.md "wikilink")
  - [Fatty Bear's Birthday Surprise](https://ko.wikipedia.org/wiki/Fatty_Bear's_Birthday_Surprise "wikilink")
  - [Fatty Bear's Fun Pack](https://ko.wikipedia.org/wiki/Fatty_Bear's_Fun_Pack "wikilink")
  - [Freddi Fish and the Case of the Missing Kelp Seeds](https://ko.wikipedia.org/wiki/Freddi_Fish_and_the_Case_of_the_Missing_Kelp_Seeds "wikilink")
  - [Freddi Fish 2: The Case of the Haunted Schoolhouse](https://ko.wikipedia.org/wiki/Freddi_Fish_2:_The_Case_of_the_Haunted_Schoolhouse "wikilink")
  - [Freddi Fish 3: The Case of the Stolen Conch Shell](https://ko.wikipedia.org/wiki/Freddi_Fish_3:_The_Case_of_the_Stolen_Conch_Shell "wikilink")
  - [Freddi Fish 4: The Case of the Hogfish Rustlers of Briny Gulch](https://ko.wikipedia.org/wiki/Freddi_Fish_4:_The_Case_of_the_Hogfish_Rustlers_of_Briny_Gulch "wikilink")
  - [Freddi Fish 5: The Case of the Creature of Coral Cove](https://ko.wikipedia.org/wiki/Freddi_Fish_5:_The_Case_of_the_Creature_of_Coral_Cove "wikilink")
  - [Freddi Fish and Luther's Maze Madness](https://ko.wikipedia.org/wiki/Freddi_Fish_and_Luther's_Maze_Madness "wikilink")
  - [Freddi Fish and Luther's Water Worries](https://ko.wikipedia.org/wiki/Freddi_Fish_and_Luther's_Water_Worries "wikilink")
  - [Let's Explore the Airport with Buzzy](https://ko.wikipedia.org/wiki/Junior_Field_Trips#Let's_Explore_the_Airport "wikilink")
  - [Let's Explore the Farm with Buzzy](https://ko.wikipedia.org/wiki/Junior_Field_Trips#Let's_Explore_the_Farm "wikilink")
  - [Let's Explore the Jungle with Buzzy](https://ko.wikipedia.org/wiki/Junior_Field_Trips#Let's_Explore_the_Jungle "wikilink")
  - [Pajama Sam: No Need to Hide When It's Dark Outside](https://ko.wikipedia.org/wiki/Pajama_Sam:_No_Need_to_Hide_When_It's_Dark_Outside "wikilink")
  - [Pajama Sam 2: Thunder and Lightning Aren't so Frightening](https://ko.wikipedia.org/wiki/Pajama_Sam_2:_Thunder_and_Lightning_Aren't_so_Frightening "wikilink")
  - [Pajama Sam 3: You Are What You Eat from Your Head to Your Feet](https://ko.wikipedia.org/wiki/Pajama_Sam_3:_You_Are_What_You_Eat_from_Your_Head_to_Your_Feet "wikilink")
  - [Pajama Sam's Lost & Found](https://ko.wikipedia.org/wiki/파자마_샘 "wikilink")
  - [Pajama Sam's Sock Works](https://ko.wikipedia.org/wiki/파자마_샘 "wikilink")
  - [Pajama Sam: Games to Play on Any Day](https://ko.wikipedia.org/wiki/파자마_샘 "wikilink")
  - [Putt-Putt & Fatty Bear's Activity Pack](https://ko.wikipedia.org/wiki/풋풋#Other_games "wikilink")
  - [Putt-Putt and Pep's Balloon-O-Rama](https://ko.wikipedia.org/wiki/풋풋#Other_games "wikilink")
  - [Putt-Putt and Pep's Dog on a Stick](https://ko.wikipedia.org/wiki/풋풋#Other_games "wikilink")
  - [Putt-Putt Enters the Race](https://ko.wikipedia.org/wiki/Putt-Putt_Enters_the_Race "wikilink")
  - [Putt-Putt Goes to the Moon](https://ko.wikipedia.org/wiki/Putt-Putt_Goes_to_the_Moon "wikilink")
  - [Putt-Putt Joins the Circus](https://ko.wikipedia.org/wiki/Putt-Putt_Joins_the_Circus "wikilink")
  - [Putt-Putt Joins the Parade](https://ko.wikipedia.org/wiki/Putt-Putt_Joins_the_Parade "wikilink")
  - [Putt-Putt Saves the Zoo](https://ko.wikipedia.org/wiki/Putt-Putt_Saves_the_Zoo "wikilink")
  - [풋풋](https://ko.wikipedia.org/wiki/풋풋 "wikilink")
  - [Putt-Putt's Fun Pack](https://ko.wikipedia.org/wiki/풋풋#Other_games "wikilink")
  - [Spy Fox in "Dry Cereal"](https://ko.wikipedia.org/wiki/Spy_Fox_in_"Dry_Cereal" "wikilink")
  - [Spy Fox 2: "Some Assembly Required"](https://ko.wikipedia.org/wiki/Spy_Fox_2:_"Some_Assembly_Required" "wikilink")
  - [Spy Fox 3: "Operation Ozone"](https://ko.wikipedia.org/wiki/Spy_Fox_3:_"Operation_Ozone" "wikilink")
  - [Spy Fox in Cheese Chase](https://ko.wikipedia.org/wiki/Spy_Fox "wikilink")
  - [Spy Fox in Hold the Mustard](https://ko.wikipedia.org/wiki/Spy_Fox "wikilink")

### [리빙 북스](https://ko.wikipedia.org/wiki/리빙_북스 "wikilink") 시리즈 게임

  - [Aesop's Fables: The Tortoise and the Hare](https://ko.wikipedia.org/wiki/Aesop's_Fables:_The_Tortoise_and_the_Hare "wikilink")
  - [Arthur's Birthday](https://ko.wikipedia.org/wiki/Arthur's_Birthday "wikilink")
  - [Arthur's Teacher Trouble](https://ko.wikipedia.org/wiki/Arthur's_Teacher_Trouble "wikilink")
  - [The Berenstain Bears Get in a Fight](https://ko.wikipedia.org/wiki/The_Berenstain_Bears_Get_in_a_Fight "wikilink")
  - [The Berenstain Bears in the Dark](https://ko.wikipedia.org/wiki/The_Berenstain_Bears_in_the_Dark "wikilink")
  - [Dr. Seuss's ABC](https://ko.wikipedia.org/wiki/Dr._Seuss's_ABC "wikilink")
  - [Green Eggs and Ham](https://ko.wikipedia.org/wiki/Green_Eggs_and_Ham "wikilink")
  - [Harry and the Haunted House](https://ko.wikipedia.org/wiki/Harry_and_the_Haunted_House "wikilink")
  - [Just Grandma and Me](https://ko.wikipedia.org/wiki/Just_Grandma_and_Me "wikilink")
  - [Little Monster at School](https://ko.wikipedia.org/wiki/Little_Monster_at_School "wikilink")
  - [The New Kid on the Block](https://ko.wikipedia.org/wiki/The_New_Kid_on_the_Block "wikilink")
  - [Ruff's Bone](https://ko.wikipedia.org/wiki/Ruff's_Bone "wikilink")
  - [Sheila Rae, the Brave](https://ko.wikipedia.org/wiki/Sheila_Rae,_the_Brave "wikilink")
  - [Stellaluna](https://ko.wikipedia.org/wiki/Stellaluna "wikilink")

### 그 밖의 개발자들의 게임

스컴VM은 SCUMM에 속하지 않은 게임들도 지원한다:

  - [3 Skulls of the Toltecs](https://ko.wikipedia.org/wiki/3_Skulls_of_the_Toltecs "wikilink")
  - [The 7th Guest](https://ko.wikipedia.org/wiki/The_7th_Guest "wikilink")
  - [Amazon: Guardians of Eden](https://ko.wikipedia.org/wiki/Amazon:_Guardians_of_Eden "wikilink")
  - [Beavis and Butt-Head in Virtual Stupidity](https://ko.wikipedia.org/wiki/Beavis_and_Butt-Head_in_Virtual_Stupidity "wikilink")
  - [Beneath a Steel Sky](https://ko.wikipedia.org/wiki/Beneath_a_Steel_Sky "wikilink")
  - [블레이드 러너](https://ko.wikipedia.org/wiki/블레이드_러너_\(1997년_비디오_게임\) "wikilink")
  - [Blue Force](https://ko.wikipedia.org/wiki/Blue_Force "wikilink")
  - [Broken Sword: The Shadow of the Templars](https://ko.wikipedia.org/wiki/Broken_Sword:_The_Shadow_of_the_Templars "wikilink")
  - [Broken Sword II: The Smoking Mirror](https://ko.wikipedia.org/wiki/Broken_Sword_II:_The_Smoking_Mirror "wikilink")
  - [브로큰 소드](https://ko.wikipedia.org/wiki/브로큰_소드 "wikilink")
  - [Bud Tucker in Double Trouble](https://ko.wikipedia.org/wiki/Bud_Tucker_in_Double_Trouble "wikilink")
  - [Chivalry is Not Dead](https://ko.wikipedia.org/wiki/Chivalry_is_Not_Dead "wikilink")
  - [Cruise for a Corpse](https://ko.wikipedia.org/wiki/Cruise_for_a_Corpse "wikilink")
  - [Darby the Dragon](https://ko.wikipedia.org/wiki/Darby_the_Dragon "wikilink")
  - [디스크월드](https://ko.wikipedia.org/wiki/디스크월드_\(비디오_게임\) "wikilink")
  - [Discworld II: Missing Presumed...\!?](https://ko.wikipedia.org/wiki/Discworld_II:_Missing_Presumed...!? "wikilink")
  - [Dragon History](https://ko.wikipedia.org/wiki/Dragon_History "wikilink")
  - [Drascula: The Vampire Strikes Back](https://ko.wikipedia.org/wiki/Drascula:_The_Vampire_Strikes_Back "wikilink")
  - [DreamWeb](https://ko.wikipedia.org/wiki/DreamWeb "wikilink")
  - [Duckman: The Graphic Adventures of a Private Dick](https://ko.wikipedia.org/wiki/Duckman:_The_Graphic_Adventures_of_a_Private_Dick "wikilink")
  - [아이 오브 더 비홀더](https://ko.wikipedia.org/wiki/아이_오브_더_비홀더_\(1991년_비디오_게임\) "wikilink")
  - [Eye of the Beholder II: The Legend of Darkmoon](https://ko.wikipedia.org/wiki/Eye_of_the_Beholder_II:_The_Legend_of_Darkmoon "wikilink")
  - [Flight of the Amazon Queen](https://ko.wikipedia.org/wiki/Flight_of_the_Amazon_Queen "wikilink")
  - [Full Pipe](https://ko.wikipedia.org/wiki/Full_Pipe "wikilink")
  - [Future Wars](https://ko.wikipedia.org/wiki/Future_Wars "wikilink")
  - [Gregory and the Hot Air Balloon](https://ko.wikipedia.org/wiki/Gregory_and_the_Hot_Air_Balloon "wikilink")
  - [Hopkins FBI](https://ko.wikipedia.org/wiki/Hopkins_FBI "wikilink")
  - [Hugo's House of Horrors](https://ko.wikipedia.org/wiki/Hugo's_House_of_Horrors "wikilink")
  - [Hugo II, Whodunit?](https://ko.wikipedia.org/wiki/Hugo_II,_Whodunit? "wikilink")
  - [Hugo III, Jungle of Doom\!](https://ko.wikipedia.org/wiki/Hugo_III,_Jungle_of_Doom! "wikilink")
  - [Hyperspace Delivery Boy\!](https://ko.wikipedia.org/wiki/Hyperspace_Delivery_Boy! "wikilink")
  - [스크림](https://ko.wikipedia.org/wiki/스크림_\(비디오_게임\) "wikilink")
  - [Inherit the Earth: Quest for the Orb](https://ko.wikipedia.org/wiki/Inherit_the_Earth:_Quest_for_the_Orb "wikilink")
  - [The Journeyman Project: Pegasus Prime](https://ko.wikipedia.org/wiki/The_Journeyman_Project:_Pegasus_Prime "wikilink")
  - [The Labyrinth of Time](https://ko.wikipedia.org/wiki/The_Labyrinth_of_Time "wikilink")
  - [Lands of Lore: The Throne of Chaos](https://ko.wikipedia.org/wiki/Lands_of_Lore:_The_Throne_of_Chaos "wikilink")
  - [Leather Goddesses of Phobos 2: Gas Pump Girls Meet the Pulsating Inconvenience from Planet X\!](https://ko.wikipedia.org/wiki/Leather_Goddesses_of_Phobos_2:_Gas_Pump_Girls_Meet_the_Pulsating_Inconvenience_from_Planet_X! "wikilink")
  - [The Legend of Kyrandia: Fables and Fiends](https://ko.wikipedia.org/wiki/The_Legend_of_Kyrandia:_Fables_and_Fiends "wikilink")
  - [The Legend of Kyrandia: Hand of Fate](https://ko.wikipedia.org/wiki/The_Legend_of_Kyrandia:_Hand_of_Fate "wikilink")
  - [The Legend of Kyrandia: Malcolm's Revenge](https://ko.wikipedia.org/wiki/The_Legend_of_Kyrandia:_Malcolm's_Revenge "wikilink")
  - [The Lost Files of Sherlock Holmes: The Case of the Rose Tattoo](https://ko.wikipedia.org/wiki/The_Lost_Files_of_Sherlock_Holmes#The_Case_of_the_Rose_Tattoo "wikilink")
  - [The Lost Files of Sherlock Holmes: The Case of the Serrated Scalpel](https://ko.wikipedia.org/wiki/The_Lost_Files_of_Sherlock_Holmes#The_Case_of_the_Serrated_Scalpel "wikilink")
  - [Lure of the Temptress](https://ko.wikipedia.org/wiki/Lure_of_the_Temptress "wikilink")
  - [Magic Tales: Liam Finds a Story](https://ko.wikipedia.org/wiki/Magic_Tales "wikilink")
  - [Magic Tales: The Princess and the Crab](https://ko.wikipedia.org/wiki/Magic_Tales "wikilink")
  - [Magic Tales: Sleeping Cub's Test of Courage](https://ko.wikipedia.org/wiki/Magic_Tales "wikilink")
  - [The Manhole](https://ko.wikipedia.org/wiki/The_Manhole "wikilink")
  - [Might and Magic IV](https://ko.wikipedia.org/wiki/Might_and_Magic_IV "wikilink")
  - [Might and Magic V](https://ko.wikipedia.org/wiki/Might_and_Magic_V "wikilink")
  - [Might and Magic: Swords of Xeen](https://ko.wikipedia.org/wiki/Might_and_Magic:_Swords_of_Xeen "wikilink")
  - [Might and Magic: World of Xeen](https://ko.wikipedia.org/wiki/Might_and_Magic:_World_of_Xeen "wikilink")
  - [Mission Supernova](https://ko.wikipedia.org/wiki/Mission_Supernova "wikilink") Part 1 and Part 2
  - [Mortville Manor](https://ko.wikipedia.org/wiki/Mortville_Manor "wikilink")
  - [미스트](https://ko.wikipedia.org/wiki/미스트_\(비디오_게임\) "wikilink"), [Myst Masterpiece Edition](https://ko.wikipedia.org/wiki/미스트_\(비디오_게임\) "wikilink")
  - [네버후드](../Page/네버후드.md "wikilink")
  - [Nippon Safes Inc.](https://ko.wikipedia.org/wiki/Nippon_Safes_Inc. "wikilink")
  - [배관공은 넥타이를 매지 않는다](../Page/배관공은_넥타이를_매지_않는다.md "wikilink")
  - [The Prince and the Coward](https://ko.wikipedia.org/wiki/The_Prince_and_the_Coward "wikilink")
  - [Return to Ringworld](https://ko.wikipedia.org/wiki/Return_to_Ringworld "wikilink")
  - [Return to Zork](https://ko.wikipedia.org/wiki/Return_to_Zork "wikilink")
  - [Rex Nebular and the Cosmic Gender Bender](https://ko.wikipedia.org/wiki/Rex_Nebular_and_the_Cosmic_Gender_Bender "wikilink")
  - [Ringworld: Revenge of the Patriarch](https://ko.wikipedia.org/wiki/Ringworld:_Revenge_of_the_Patriarch "wikilink")
  - [리븐](../Page/리븐.md "wikilink")
  - [Rodney's Funscreen](https://ko.wikipedia.org/wiki/Rodney's_Funscreen "wikilink")
  - [스핑크스](https://ko.wikipedia.org/wiki/스핑크스_\(비디오_게임\) "wikilink")
  - [Sołtys](https://ko.wikipedia.org/wiki/Sołtys "wikilink")
  - [Starship Titanic](https://ko.wikipedia.org/wiki/Starship_Titanic "wikilink")
  - [Teenagent](https://ko.wikipedia.org/wiki/Teenagent "wikilink")
  - [Tony Tough and the Night of Roasted Moths](https://ko.wikipedia.org/wiki/Tony_Tough_and_the_Night_of_Roasted_Moths "wikilink")
  - [Toonstruck](https://ko.wikipedia.org/wiki/Toonstruck "wikilink")
  - [Touché: The Adventures of the Fifth Musketeer](https://ko.wikipedia.org/wiki/Touché:_The_Adventures_of_the_Fifth_Musketeer "wikilink")
  - [U.F.O.s](https://ko.wikipedia.org/wiki/U.F.O.s "wikilink")
  - [Versailles 1685](https://ko.wikipedia.org/wiki/Versailles_1685 "wikilink")
  - [보이어](https://ko.wikipedia.org/wiki/보이어_\(비디오_게임\) "wikilink")
  - [Zork: Grand Inquisitor](https://ko.wikipedia.org/wiki/Zork:_Grand_Inquisitor "wikilink")
  - [Zork Nemesis](https://ko.wikipedia.org/wiki/Zork_Nemesis "wikilink")

### 개발 중인 게임

다음 게임들은 스컴VM 공식 버전에서 지원되지 않으나 메인 코드 저장소에서 작업이 진행 중이다.\[13\]

  - [11번째 시간](https://ko.wikipedia.org/wiki/11번째_시간_\(비디오_게임\) "wikilink")
  - [A.J.'s World of Discovery](https://ko.wikipedia.org/wiki/A.J.'s_World_of_Discovery "wikilink")
  - [Backyard Basketball](https://ko.wikipedia.org/wiki/Backyard_Basketball "wikilink")
  - [Backyard Soccer](https://ko.wikipedia.org/wiki/Backyard_Soccer "wikilink")
  - [Backyard Soccer MLS Edition](https://ko.wikipedia.org/wiki/Backyard_Soccer_MLS_Edition "wikilink")
  - [The Big Red Adventure](https://ko.wikipedia.org/wiki/The_Big_Red_Adventure "wikilink")
  - [Blue's Treasure Hunt](https://ko.wikipedia.org/wiki/Blue's_Treasure_Hunt "wikilink")
  - [Dragonsphere](https://ko.wikipedia.org/wiki/Dragonsphere "wikilink")
  - [Freddi Fish's One-Stop Fun Shop](https://ko.wikipedia.org/wiki/Freddi_Fish's_One-Stop_Fun_Shop "wikilink")
  - [디 이모털](https://ko.wikipedia.org/wiki/디_이모털_\(비디오_게임\) "wikilink")
  - [The Last Dynasty](https://ko.wikipedia.org/wiki/The_Last_Dynasty "wikilink")
  - [The Last Express](https://ko.wikipedia.org/wiki/The_Last_Express "wikilink")
  - [Living Books series](https://ko.wikipedia.org/wiki/Living_Books_series "wikilink")
  - [Lord Avalot d'Argent](https://ko.wikipedia.org/wiki/Lord_Avalot_d'Argent "wikilink")
  - [Magic Tales: Baba Yaga and the Magic Geese](https://ko.wikipedia.org/wiki/Magic_Tales "wikilink")
  - [Magic Tales: Imo and the King](https://ko.wikipedia.org/wiki/Magic_Tales "wikilink")
  - [Magic Tales: The Little Samurai](https://ko.wikipedia.org/wiki/Magic_Tales "wikilink")
  - [Martian Memorandum](https://ko.wikipedia.org/wiki/Martian_Memorandum "wikilink")
  - [Moonbase Commander](https://ko.wikipedia.org/wiki/Moonbase_Commander "wikilink")
  - [Noctropolis](https://ko.wikipedia.org/wiki/Noctropolis "wikilink")
  - [Operation Stealth](https://ko.wikipedia.org/wiki/Operation_Stealth "wikilink")
  - [파자마 샘](https://ko.wikipedia.org/wiki/파자마_샘 "wikilink")
  - [The Pink Panther: Hokus Pokus Pink](https://ko.wikipedia.org/wiki/The_Pink_Panther:_Hokus_Pokus_Pink "wikilink")
  - [The Pink Panther: Passport to Peril](https://ko.wikipedia.org/wiki/The_Pink_Panther:_Passport_to_Peril "wikilink")
  - [Playtoons](https://ko.wikipedia.org/wiki/Playtoons "wikilink") series
  - [풋풋](https://ko.wikipedia.org/wiki/풋풋 "wikilink")
  - [Red Comrades](https://ko.wikipedia.org/wiki/Red_Comrades_Save_the_Galaxy "wikilink") series
  - [Return of the Phantom](https://ko.wikipedia.org/wiki/Return_of_the_Phantom "wikilink")
  - [스타트렉 : 25주년 기념](https://ko.wikipedia.org/wiki/스타트렉_:_25주년_기념 "wikilink")
  - [Star Trek: Judgment Rites](https://ko.wikipedia.org/wiki/Star_Trek:_Judgment_Rites "wikilink")
  - [Where in Time is Carmen Sandiego?](https://ko.wikipedia.org/wiki/Where_in_Time_Is_Carmen_Sandiego?_\(1989\) "wikilink")
  - 수많은 [윈터뮤트 엔진](../Page/윈터뮤트_엔진.md "wikilink") 기반 게임
  - 수많은 [월드 빌더](https://ko.wikipedia.org/wiki/월드_빌더 "wikilink") 기반 게임

## 같이 보기

  - [스컴](https://ko.wikipedia.org/wiki/스컴 "wikilink")
  - [도스박스](../Page/도스박스.md "wikilink")

## 각주

## 외부 링크

  -
  -
  -
[분류:솔라리스 소프트웨어](https://ko.wikipedia.org/wiki/분류:솔라리스_소프트웨어 "wikilink") [분류:OS/2 소프트웨어](https://ko.wikipedia.org/wiki/분류:OS/2_소프트웨어 "wikilink") [분류:유닉스 소프트웨어](https://ko.wikipedia.org/wiki/분류:유닉스_소프트웨어 "wikilink") [분류:윈도우 소프트웨어](https://ko.wikipedia.org/wiki/분류:윈도우_소프트웨어 "wikilink") [분류:리눅스 소프트웨어](https://ko.wikipedia.org/wiki/분류:리눅스_소프트웨어 "wikilink") [분류:MacOS 소프트웨어](https://ko.wikipedia.org/wiki/분류:MacOS_소프트웨어 "wikilink") [분류:포켓 PC 소프트웨어](https://ko.wikipedia.org/wiki/분류:포켓_PC_소프트웨어 "wikilink") [분류:BSD 소프트웨어](https://ko.wikipedia.org/wiki/분류:BSD_소프트웨어 "wikilink") [분류:BeOS 소프트웨어](https://ko.wikipedia.org/wiki/분류:BeOS_소프트웨어 "wikilink") [분류:아미가 소프트웨어](https://ko.wikipedia.org/wiki/분류:아미가_소프트웨어 "wikilink") [분류:자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_소프트웨어 "wikilink") [분류:자유 소프트웨어 프로젝트](https://ko.wikipedia.org/wiki/분류:자유_소프트웨어_프로젝트 "wikilink") [분류:팜 OS 소프트웨어](https://ko.wikipedia.org/wiki/분류:팜_OS_소프트웨어 "wikilink") [분류:크로스 플랫폼 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_소프트웨어 "wikilink") [분류:2001년 소프트웨어](https://ko.wikipedia.org/wiki/분류:2001년_소프트웨어 "wikilink") [분류:MacOS 게임](https://ko.wikipedia.org/wiki/분류:MacOS_게임 "wikilink") [분류:윈도우 게임](https://ko.wikipedia.org/wiki/분류:윈도우_게임 "wikilink") [분류:C++로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C++로_작성된_자유_소프트웨어 "wikilink") [분류:자유 가상화 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_가상화_소프트웨어 "wikilink")

1.  [history of ScummVM](http://wiki.scummvm.org/index.php/ScummVM_History) on ScummVM Wiki
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12. [The official ScummVM compatibility chart](http://scummvm.org/compatibility/).
13.