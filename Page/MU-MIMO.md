> This article is converted from Wikipedia: [MU-MIMO](https://ko.wikipedia.org/wiki/MU-MIMO).


**MU-MIMO**(, 다중 사용자 MIMO)는 제각기 하나 이상의 안테나를 갖춘 사용자나 무선 터미널들이 서로 통신하는, [무선 통신을](../Page/무선_통신.md "wikilink") 위한 [MIMO](../Page/MIMO.md "wikilink") 기술들의 집합이다.\[1\] 이와 대조적으로 단일 사용자 MIMO(single-user MIMO)는 하나의 멀티 안테나 송신기가 하나의 멀티 안테나 수신기와 통신하는 방식이다. [OFDMA](https://ko.wikipedia.org/wiki/OFDMA "wikilink")가 다중 접속(다중 사용자) 기능을 [OFDM에](../Page/직교_주파수_분할_다중_방식.md "wikilink") 추가하는 방식과 비슷하게, MU-MIMO는 다중 접속(다중 사용자) 기능을 MIMO에 추가한다. MU-MIMO는 멀티 안테나 통신에 대한 연구가 시작될 때부터 탐구되어 왔으며 여기에는 MU-MIMO 업링크 기능에 대한 Telatar의 업적이 포함된다.\[2\]

SDMA,\[3\]\[4\]\[5\] 대용량 MIMO(massive MIMO),\[6\]\[7\] CoMP(coordinated multipoint),\[8\] 애드혹 MIMO는 모두 MU-MIMO와 관련되어 있다. 해당 기술들은 개별 사용자에게 여유 공간을 조율한다.

## 기술

MU-MIMO는 더 값비싼 신호 처리 대신 여러 사용자들을 공간적으로 분산된 전송 자원으로 활용할 수 있다. 이와 비교해, 전통적인 단일 사용자 [MIMO](../Page/MIMO.md "wikilink")는 오직 하나의 로컬 장치 멀티 안테나 규모만 고려한다. MU-MIMO 알고리즘은 사용자나 연결 수가 하나보다 더 클 때 MIMO 시스템을 강화하도록 발전되었다. MU-MIMO는 두 가지 분류로 일반화할 수 있다: 다운링크 상황을 위한 MIMO 브로드캐스트 채널(MIMO broadcast channels, MIMO BC), 업링크 상황을 위한 MIMO 다중 접속 채널(MIMO multiple access channels, MIMO MAC). 단일 사용자 MIMO는 점대점(P2P) 쌍방향 MIMO로 이야기할 수 있다.

"수신기"와 "송신기"라는 단어의 모호성을 제거하기 위해 "액세스 포인트"(AP 또는 베이스 스테이션)와 "사용자"라는 용어를 채택할 수 있다. AP는 송신기라면 사용자는 다운링크 환경을 위한 수신자인 반면, AP가 수신기라면 사용자는 업링크 환경을 위한 송신자이다.

## MIMO 브로드캐스트 (MIMO BC)

[섬네일](https://ko.wikipedia.org/wiki/파일:BD-CSI.png "wikilink")

MIMO 브로드캐스트는 다중 수신기 무선 네트워크에 대한 단일 송신기의 MIMO 다운링크 케이스를 보여준다. MIMO BC의 고급 전송 처리의 예는 간섭을 인지하는 [프리코딩](https://ko.wikipedia.org/wiki/프리코딩 "wikilink") 및 SDMA 기반 다운링크 사용자 스케줄링이다. 고급 전송 처리의 경우 [채널 상태 정보는](https://ko.wikipedia.org/wiki/채널_상태_정보 "wikilink") 전송기(CSIT) 측에서 인식되어야 한다. 즉, CSIT가 인식하는 정보를 통해 스루풋 개선을 허용하며 CSIT를 취득하는 방식들은 상당히 중요해진다. MIMO BC 시스템들은 P2P MIMO 시스템 대비 뛰어난 이점이 있는데, 특히 송신기 또는 AP 측의 전송 안테나 수가 개별 수신기(사용자)의 수신기 안테나의 수보다 더 많을 때 그러하다. MIMO BC의 2가지 코딩 기법에는 [더티 페이퍼 코딩](https://ko.wikipedia.org/wiki/더티_페이퍼_코딩 "wikilink")(DPC)을 사용하는 것과 선형(linear) 기법을 사용하는 방식이 있다.\[9\] 게다가 하이브리드(아날로그, 디지털) 방식 또한 주목을 받고 있다\[10\].

## 같이 보기

  - [메시 네트워크](../Page/메시_네트워크.md "wikilink")
  - [모바일 애드혹 네트워크](../Page/모바일_애드혹_네트워크.md "wikilink")

## 각주

## 외부 링크

  - [MU-MIMO Beamforming by Constructive Interference](http://demonstrations.wolfram.com/MUMIMOBeamformingByConstructiveInterference/), Wolfram Demonstrations Project

[분류:정보 이론](https://ko.wikipedia.org/wiki/분류:정보_이론 "wikilink")

1.
2.
3.  N. Jindal, [MIMO Broadcast Channels with Finite Rate Feedback](https://dx.doi.org/10.1109/TIT.2006.883550), IEEE Transactions on Information Theory, vol. 52, no. 11, pp. 5045–5059, 2006.
4.  D. Gesbert, M. Kountouris, R.W. Heath Jr., C.-B. Chae, and T. Sälzer, [Shifting the MIMO Paradigm](https://dx.doi.org/10.1109/MSP.2007.904815), IEEE Signal Processing Magazine, vol. 24, no. 5, pp. 36-46, 2007.
5.  R. Tweg, R. Alpert, H. Leizerovich, A. Steiner, E. Levitan, E. Offir-Arad, A.B. Guy, B. Zickel, A. Aviram, A. Frieman, M. Wax, [ASIC Implementation of Beamforming and SDMA for WiFi Metropolitan-Area Deployment](http://ieeexplore.ieee.org/xpl/articleDetails.jsp?arnumber=4151533), Global Telecommunications Conference, 2006. GLOBECOM '06. IEEE.
6.  T. L. Marzetta, [Noncooperative Cellular Wireless with Unlimited Numbers of Base Station Antennas](https://dx.doi.org/10.1109/TWC.2010.092810.091092) IEEE Transactions on Wireless Communications, vol. 9, no. 11, pp. 56-61, 3590-3600, Nov. 2010.
7.  J. Hoydis, S. ten Brink, M. Debbah, [Massive MIMO in the UL/DL of Cellular Networks: How Many Antennas Do We Need?](https://dx.doi.org/10.1109/JSAC.2013.130205) IEEE Journal on Selected Areas in Communications, vol. 31, no. 2, pp. 160-171, Feb. 2013.
8.  E. Björnson and E. Jorswieck, [Optimal Resource Allocation in Coordinated Multi-Cell Systems](http://kth.diva-portal.org/smash/get/diva2:608533/FULLTEXT01), Foundations and Trends in Communications and Information Theory, vol. 9, no. 2-3, pp. 113-381, 2013.
9.
10. [Vizziello, A., Savazzi, P., & Chowdhury, K. R. (2018). A Kalman Based Hybrid Precoding for Multi-User Millimeter Wave MIMO Systems. IEEE Access, 6, 55712-55722.](https://www.researchgate.net/publication/327946873_A_Kalman_based_Hybrid_Precoding_for_Multi-User_Millimeter_Wave_MIMO_Systems)