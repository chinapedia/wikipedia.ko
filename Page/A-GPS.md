> This article is converted from Wikipedia: [A-GPS](https://ko.wikipedia.org/wiki/A-GPS).


**Assisted GPS**(줄여서 **A-GPS**)는 특정 조건에서(주로 [서버](https://ko.wikipedia.org/wiki/서버 "wikilink")와 데이터 연결이 성립되었을 때) [GPS](https://ko.wikipedia.org/wiki/GPS "wikilink") 시작 속도를 향상시키고, TTFF(Time To First Fix, 처음 [인공위성](../Page/인공위성.md "wikilink")과 [데이터 링크가](https://ko.wikipedia.org/wiki/데이터_링크 "wikilink") 고정되기까지 소요된 [시간](https://ko.wikipedia.org/wiki/시간 "wikilink"))를 줄이기 위한 위성 기반 위치 획득 체계이다. A-GPS는 GPS가 내장된 [휴대 전화](https://ko.wikipedia.org/wiki/휴대_전화 "wikilink") 혹은 [스마트폰](https://ko.wikipedia.org/wiki/스마트폰 "wikilink")에서 주로 사용되며, [미](https://ko.wikipedia.org/wiki/미국 "wikilink") [연방 통신 위원회에](../Page/연방_통신_위원회.md "wikilink") 의해 911 응급 통화시 위치를 빠르게 전달하기 위한 목적으로 개발되었다.\[1\]

## 동작 원리

Standalone GPS(줄여서 [S-GPS](https://ko.wikipedia.org/wiki/:en:S-GPS "wikilink"))는 [GPS 위성의](https://ko.wikipedia.org/wiki/:en:GPS_satellite "wikilink") 무선 신호를 이용하여 독립적으로 동작한다. A-GPS는 위치를 획득하기 위해 추가적으로 무선네트워크(3G/4G/WIFI) 자원을 활용하여 위성 신호를 보다 빨리 활용하고, 수신 환경이 열악한 경우에도 보다 향상된 결과를 제공한다. 위성 신호의 품질이 현저히 떨어지는 상황, 예를 들어 도시 환경에서, 위성 신호는 건물들에 의해 반사되어 발생하는 [다중 경로 전파](https://ko.wikipedia.org/wiki/다중_경로_전파 "wikilink")([multipath propagation](https://ko.wikipedia.org/wiki/:en:multipath_propagation "wikilink")) 현상과 대기, 벽, 나무 등을 통과하면서 발생하는 [전파의 감쇄와](https://ko.wikipedia.org/wiki/전파_감쇄 "wikilink") 같은 현상들에 의해 약화된다. GPS 기기가 이런 환경에서 처음 작동하게 되면, 일부 S-GPS 제품들은 신호를 제대로 수신하지 못하거나 부정확한 위치를 획득하게 된다. S-GPS는 최대 12분 30초동안 지속적으로 양호한 품질의 위성 신호가 수신되지 않을 경우 GPS 불능으로 표시한다. (12분 30초는 [GPS를 통한 달력/천체력](https://ko.wikipedia.org/wiki/:en:GPS_signals#Navigation_message "wikilink") 데이터 다운로드에 필요한 시간이다).\[2\] 12분 30초는 다음과 같이 계산된다. 필요한 데이터는 50bps 속도로 위성에서 수신기로 데이터를 전송한다. 1개의 서브프레임은 300bit로 구성되고 5개의 서브프레임이 모여 한개의 프레임을 구성한다(1,500bit frame가 필요, 50bps로 30초간 전송). 각각의 위성은 총25개의 프레임으로 구성된 롱프레임 형태로 구현된다(롱프레임의 모든 데이터를 수신하기 위해서 12분 30초가 필요하다).

A-GPS는 다음의 수단을 이용하여 S-GPS의 문제점을 해결한다.

GPS 보조의 수단은 두 가지로 분류된다.

1.  위성의 위치를 보다 빨리 획득하기 위한 정보(A-GPS, MS(이동국)-Based)
      - 이 정보를 이용하여 GPS의 [궤도](https://ko.wikipedia.org/wiki/궤도 "wikilink") 정보(Almanac)와 [천체력](../Page/천체력.md "wikilink") 데이터(Ephemeris)를 GPS [수신기](https://ko.wikipedia.org/wiki/수신기 "wikilink")에 제공할 수 있으며, 어떤 경우에는 GPS 수신기가 보다 빨리 위성과의 데이터 링크를 고정하도록 해준다.
      - 무선네트워크를 통해 정확한 시간을 얻을 수 있다.
2.  GPS 수신기에 수신된 정보를 보조 서버에 전송하여 위치 계산을 수행(A-GPS, MS(이동국)-Assisted)
      - 차후 위치 정보 처리를 위해 대략적인 시간의 정보와 함께 GPS 신호의 스냅샷을 서버에 보관해 둘 수 있다.
      - 보조 서버는 양호한 위성 신호 수신이 가능하며, 많은 양의 계산을 수행할 수 있다. 따라서 GPS 수신기가 수신한 약한 신호들도 비교하여 분석 가능하다.
      - [기지국](../Page/기지국.md "wikilink")을 통한 정확하고, 이미 확정되어 있는 좌표를 이용함으로써 해당 지역 [전리층](https://ko.wikipedia.org/wiki/전리층 "wikilink")의 상황과 같은 GPS 신호에 영향을 주는 정보를 GPS 수신기 단독으로 사용할 때보다 쉽게 획득할 수 있다. 이를 통해 보다 정확한 위치 계산이 가능하다.

추가적으로, 일부 "MS-Assisted"가 구현된 A-GPS 기기들은 대부분의 신호 계산을 보조 서버에 맡겨둠으로써 신호 처리에 필요한 [중앙 처리 장치와](https://ko.wikipedia.org/wiki/중앙_처리_장치 "wikilink") [프로그램](https://ko.wikipedia.org/wiki/프로그램 "wikilink") [로직](https://ko.wikipedia.org/wiki/로직 "wikilink") 부담을 줄일 수 있다는 장점이 있다. 반면 서버와의 [레이턴시](../Page/레이턴시.md "wikilink")에 영향을 받으므로 지속적인 추적에는 적당하지 않다.

이와 달리 "MS-Based"가 구현된 A-GPS 기기들은 구동 초기에 위성 정보를 얻기 위한 용도로 데이터 연결을 사용하며, 이후에는 S-GPS 처럼 동작하므로 내비게이션과 같이 빠른 위치 획득 응답을 요구하는 경우에 적당하다.

일반적으로 A-GPS 수신기들은 보조 서버의 A-GPS 정보를 이용하기 위해 데이터 연결을 시도한다. ([인터넷](../Page/인터넷.md "wikilink")이나 다른 수단을 통해) S-GPS로도 동작이 가능한 경우, S-GPS를 사용하게 되며 이 경우 [위성과의 데이터 링크가 고정되기까지의 시간이](https://ko.wikipedia.org/wiki/:en:Time_to_first_fix "wikilink") 보다 더 오래 걸릴 수 있다. 하지만 네트워크 의존적이지 않으므로, 통신망의 범위를 벗어난 지역에서도 사용이 가능하며 데이터 이용료가 부과되지도 않는다.\[3\] 일부 A-GPS 기기들은 S-GPS동작 옵션을 제공하지 않기도 한다.

많은 휴대 전화들이 A-GPS 뿐만 아니라 AP를 통한 [와이파이 위치 획득 체계](https://ko.wikipedia.org/wiki/와이파이_위치_획득_체계 "wikilink"), 이동 전화 기지국을 통한 [위치 획득과](https://ko.wikipedia.org/wiki/위치_획득 "wikilink") 같은 다른 위치 획득 서비스를 조합하여 사용하며, [애플](https://ko.wikipedia.org/wiki/애플_\(기업\) "wikilink") [아이폰](../Page/아이폰.md "wikilink")의 경우 [하이브리드 위치 획득 시스템을](https://ko.wikipedia.org/wiki/:en:hybrid_positioning_system "wikilink") 사용하기도 한다.\[4\]

[고감도 GPS는](https://ko.wikipedia.org/wiki/:en:High_Sensitivity_GPS "wikilink") 추가적인 [인프라](https://ko.wikipedia.org/wiki/인프라 "wikilink")를 필요로 하지 않도록 GPS의 수신 문제 해결을 위한 기술이다. 그러나 A-GPS와 달리, 고감도 GPS 역시 GPS가 오랜 기간동안 동작하지 않은 경우 즉각적인 위치 정보를 제공하지 못하는 단점을 가지고 있다.

## 기본 개념

S-GPS의 시스템은 현재 위치를 계산하기 위해서 위성의 궤도 정보가 필요하다. 위성 신호의 데이터 속도는 50bps로 매우 느려 일반적으로 시간이 오래 걸린다. S-GPS는 직접 위성에서 이페머리스와 알마낙 등의 궤도 정보를 50bps로 다운로드한다. S-GPS는 대략 30-40초 뒤에 첫 번째 위치를 잡을 수 있다. 모든 데이터를 받기 위해서는 12.5분이 걸린다. 그리고 위성 신호는 이 정보의 취득 중에 에러가 발생하는 경우 사용할 수 없다. 이 경우 S-GPS 시스템은 처음부터 다시 시작해야 한다. A-GPS에서 네트워크 운영자는 A-GPS 서버를 이용한다 . 이러한 A-GPS 서버는 위성의 궤도 정보를 다운로드하여 데이터베이스에 저장한다. A-GPS 기능이 있는 기기는 해당 보조서버에 연결하여 GSM , CDMA , WCDMA , LTE 또는 다른 전송장치인 Wi-Fi와 같은 모바일 네트워크를 사용하여 이 정보를 다운로드 할 수 있다. 보통 이러한 전송장치의 데이터 속도는 빠르다. 따라서 궤도 정보를 다운로드하는 것은 매우 적은 시간이 걸린다.

## 운영 모드

AGPS의 작동 모드는 두 가지가 있다.

1.  MSA(Mobile Station-Assisted:이동국 지원받음) - MSA 모드에서 A-GPS의 작동, A-GPS 이용이 가능한 기기는 A-GPS 보조서버에서 취득 지원, 기준 시간 및 다른 옵션 보조 데이터를 받는다. 이러한 데이터의 도움으로 A-GPS 기기는 보이는 위성에서 신호를 받고 A-GPS 서버로 데이터를 보냅니다. A-GPS 서버는 위치를​​ 계산하고 다시 A-GPS 장치로 보낸다.
2.  MSB(Mobile Station-Based:이동국 기반) - MSB 모드에서 A-GPS의 작동, A-GPS 기기는 A-GPS 보조서버에서 이페머리스, 기준위치, 기준시간 다른 기타 보조 데이터를 받는다. 이러한 데이터의 도움으로 A-GPS 기기는 보이는 위성에서 직접 신호를 받아 위치를 계산한다.

## 표준

AGPS 프로토콜은 3GPP와 OMA라는 두 개의 서로 다른 표준화기구에 의해 정의된 위치 프로토콜의 일부이다.

1.  3GPP 제어 평면 프로토콜 - 이것은 휴대 전화 시스템의 여러 세대에 걸쳐 3GPP에 의해 정의된다. 이 프로토콜은 Circuit Switched Networks에 정의되어 있다 . 다음과 같은 위치 프로토콜이 정의되어있다.
      - RRLP - 3GPP GSM 네트워크에 위치 프로토콜을 지원하는 RRLP 또는 라디오 자원 위치 프로토콜을 정의.
      - TIA 801 - CDMA2000 계열은 CDMA 2000 네트워크에 이 프로토콜을 정의.
      - RRC 위치 프로토콜 - 3GPP는 이 프로토콜을 RRC 에 대한 표준 UMTS 네트워크의 일환으로 정의.
      - LPP - 3GPP는 LPP 또는 LTE의 네트워크를 위한 LTE 위치 프로토콜을 정의.
2.  Open Mobile Alliance\[오픈 모바일 얼라이언스 (OMA)\] 사용자 평면 프로토콜 - 이것은 Packet Switched Networks의 위치 프로토콜을 지원하는 OMA에 의해 정의된다. 사용자 평면 프로토콜은 세 가지로 분류된다.
      - SUPL V1.0
      - SUPL V2.0
      - SUPL V3.0

## 각주

[분류:GPS](https://ko.wikipedia.org/wiki/분류:GPS "wikilink")

1.
2.  [1](http://www.navcen.uscg.gov/pubs/gps/gpsuser/gpsuser.pdf) NavCen GPS User. 3.5.3 Almanac Collection
3.  [Watch out for data charges on your GPS phone](http://www.cnet.com.au/mobilephones/phones/0,239025953,339281483,00.htm). CNET, August 2007
4.  [Networking iPhone A-GPS](http://www.edepot.com/iphone.html#iPhone) Hybrid system