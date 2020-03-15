> This article is converted from Wikipedia: [IPv4](https://ko.wikipedia.org/wiki/IPv4).


**IPv4**는 [인터넷 프로토콜의](../Page/인터넷_프로토콜.md "wikilink") 4번째 판이며, 전 세계적으로 사용된 첫 번째 인터넷 프로토콜이다. 과거에 인터넷에서 사용되는 유일한 프로토콜이였으나 [오늘날에는 IPv6이 대중화되었다.](../Page/IPv6.md "wikilink") [IETF](https://ko.wikipedia.org/wiki/IETF "wikilink") RFC 791(1981년 9월)에 기술되어 있다.

IPv4는 [패킷 교환](https://ko.wikipedia.org/wiki/패킷_교환 "wikilink") [네트워크](https://ko.wikipedia.org/wiki/네트워크 "wikilink") 상에서 데이터를 교환하기 위한 [프로토콜](https://ko.wikipedia.org/wiki/프로토콜 "wikilink")이다. 데이터가 정확하게 전달될 것을 보장하지 않고, 중복된 패킷을 전달하거나 패킷의 순서를 잘못 전달할 가능성도 있다. 데이터의 정확하고 순차적인 전달은 그보다 상위 프로토콜인 [TCP에서](../Page/전송_제어_프로토콜.md "wikilink")(그리고 [UDP에서도](../Page/사용자_데이터그램_프로토콜.md "wikilink") 일부) 보장한다.

IPv4의 주소체계는 총 12자리이며 네 부분으로 나뉜다. 각 부분은 0\~255까지 3자리의 수로 표현된다. IPv4 주소는 32비트로 구성되어 있으며, 현재 인터넷 사용자의 증가로 인해 주소공간의 고갈에 대한 우려가 높아지고 있다. 이에 따라 대안으로 128비트 주소체계를 갖는 [IPv6](../Page/IPv6.md "wikilink")가 등장하였다. 중국의 경우 주소공간 고갈을 우려하여 일부에서 독자적으로 [IPv9](https://ko.wikipedia.org/wiki/IPv9 "wikilink")(십진제 인터넷 주소체계)과 숫자도메인(Digital Domain Name System, DDNS)이 결합된 개념인 IP 주소와 도메인 이름이 동일한 네트워크 체제인 All-Digital-Domain-Address (ADDA)를 사용하기도 한다.

[2011년](../Page/2011년.md "wikilink") 2월 4일부터 모든 IPv4 주소가 소진되어 IPv4의 할당이 중지되었다.

## 구성 단위

| CLASS | 구성                  | 범위                           | 예                  |
| ----- | ------------------- | ---------------------------- | ------------------ |
| A 클래스 | **xxx**.xxx.xxx.xxx | 1.0.0.1 \~ 126.255.255.254   | **61**.211.123.22  |
| B 클래스 | **xxx.xxx.**xxx.xxx | 128.0.0.1 \~ 191.255.255.254 | **181.123.**211.33 |
| C 클래스 | **xxx.xxx.xxx.**xxx | 192.0.0.1 \~ 223.255.255.254 | **221.23.222.**222 |
| D 클래스 |                     | 224.0.0.0 \~ 239.255.255.255 |                    |
| E 클래스 |                     | 240.0.0.0 \~ 254.255.255.254 |                    |

### A 클래스

  - A Class는 최고위의 Class로서, 1\~126 (0, 127 예약됨)범위의 IP주소를 가진다. 두 번째, 세 번째 그리고 네 번째 단위의 세 숫자는 A Class가 자유롭게 네트워크 사용자에게 부여가 가능한 아이피이다.

### B 클래스

  - **B Class**는 두 번째로 높은 단위의 Class로써, 아이피 구성에서 첫 번째 단위의 세 숫자는 128 - 191 가운데 하나를 가지며 (위의 예에서 181), 두 번째 단위의 세 숫자는 B Class가 접속할 수 있는 네트워크를 지시한다.

### C 클래스

  - **C Class**는 최하위의 Class로서, 아이피 구성에서 첫 번째 단위의 세 숫자는 192 -223 가운데 하나를 가지며 (위의 예에서 221), 두 번째와 세 번째 단위의 세 숫자는 C Class가 접속할 수 있는 네트워크를 지시한다. C Class가 자유로이 부여할 수 있는 아이피는 마지막 네 번째 단위의 254 개이다.(2개는 예약)手机号这时候

## 패킷 구조

### 헤더

| 오프셋                                                 | [옥텟](https://ko.wikipedia.org/wiki/옥텟 "wikilink") | 0                 | 1    | 2         | 3   |
| --------------------------------------------------- | ------------------------------------------------- | ----------------- | ---- | --------- | --- |
| | [옥텟](https://ko.wikipedia.org/wiki/옥텟 "wikilink") | [비트](../Page/비트_\(단위\).md "wikilink")             | 0                 | 1    | 2         | 3   |
| 0                                                   | 0                                                 | 버전                | IHL  | DSCP      | ECN |
| 4                                                   | 32                                                | 식별 정보             | 플래그  | 프래그먼트 오프셋 |     |
| 8                                                   | 64                                                | TTL(생존 시간)        | 프로토콜 | 헤더 체크섬    |     |
| 12                                                  | 96                                                | 출발지 IP 주소         |      |           |     |
| 16                                                  | 128                                               | 목적지 IP 주소         |      |           |     |
| 20                                                  | 160                                               | 옵션 (IHL \> 5인 경우) |      |           |     |
| 24                                                  | 192                                               |                   |      |           |     |
| 28                                                  | 224                                               |                   |      |           |     |
| 32                                                  | 256                                               |                   |      |           |     |

IPv4 헤더 포맷

## 특수 용도 주소

| 주소 대역          | 용도                    |
| -------------- | --------------------- |
| 0.0.0.0/8      | 자체 네트워크               |
| 10.0.0.0/8     | 사설 네트워크               |
| 127.0.0.0/8    | 루프백(loopback) 즉, 자기자신 |
| 169.254.0.0/16 | 링크 로컬(link local)     |
| 172.16.0.0/12  | 사설 네트워크               |
| 192.0.2.0/24   | 예제 등 문서에서 사용          |
| 192.88.99.0/24 | 6to4 릴레이 애니캐스트        |
| 192.168.0.0/16 | 사설 네트워크               |
| 198.18.0.0/15  | 네트워크 장비 벤치마킹 테스트      |
| 224.0.0.0/4    | 멀티캐스트                 |
| 240.0.0.0/4    | 미래 사용 용도로 예약          |

## 나라별 할당 현황

### 대한민국

[2013년](../Page/2013년.md "wikilink") [8월 19일](../Page/8월_19일.md "wikilink") 현재 IPv4의 4,294,967,296개의 주소 가운데 [대한민국](../Page/대한민국.md "wikilink")에 약 2.61%인 112,268,800개가 할당되어 있으며 이 중 약 99.97%인 112,235,264개가 사용되고 있다. 이는 전 세계에서 [미국](../Page/미국.md "wikilink"), [중국](../Page/중화인민공화국.md "wikilink"), [일본](../Page/일본.md "wikilink"), [영국](../Page/영국.md "wikilink"), [독일](https://ko.wikipedia.org/wiki/독일 "wikilink") 다음으로 6위를 차지하고 있으며 [아시아](../Page/아시아.md "wikilink")권에서는 [중국](../Page/중화인민공화국.md "wikilink"), [일본](../Page/일본.md "wikilink") 다음으로 3위를 차지하고 있다.

## WHOIS 검색 서비스

IP 주소 및 도메인은 다음의 검색 기관의 WHOIS 검색 서비스 통해 쉽게 검색할 수 있다.

## 참고

  - [IPv4 주소 할당량에 따른 나라 목록](../Page/IPv4_주소_할당량에_따른_나라_목록.md "wikilink")
  - [IPv6](../Page/IPv6.md "wikilink")

## 외부 링크

### 대한민국

  - [KISA](http://whois.kisa.or.kr/): Korea Internet & Security Agency, [한국인터넷진흥원](https://ko.wikipedia.org/wiki/한국인터넷진흥원 "wikilink")

### 아시아 지역

  - [APNIC](http://wq.apnic.net/apnic-bin/whois.pl): Asia Pacific Network Information Center

### 북미 지역

  - [ARIN](https://web.archive.org/web/20090928094938/http://ws.arin.net/whois/index.html): American Registry for Internet Numbers

### 중남미 지역

  - [LACNIC](http://lacnic.net/cgi-bin/lacnic/whois): Latin American and Caribbean Internet Addresses Registry

### 유럽 지역

  - [RIPE](https://web.archive.org/web/20080507161609/http://www.db.ripe.net/whois): Réseaux IP Européens

[분류:인터넷 표준](https://ko.wikipedia.org/wiki/분류:인터넷_표준 "wikilink") [분류:인터넷 프로토콜](https://ko.wikipedia.org/wiki/분류:인터넷_프로토콜 "wikilink") [분류:네트워크 계층 프로토콜](https://ko.wikipedia.org/wiki/분류:네트워크_계층_프로토콜 "wikilink") [분류:인터넷 계층 프로토콜](https://ko.wikipedia.org/wiki/분류:인터넷_계층_프로토콜 "wikilink")