> This article is converted from Wikipedia: [DASH7](https://ko.wikipedia.org/wiki/DASH7).


**DASH7**은 초저전력 무선 데이터 기술로서 433MHz 대역에서 air interface 통신을 정의하는 국제 표준인 [ISO/IEC 18000-7이](https://ko.wikipedia.org/wiki/ISO/IEC_18000-7 "wikilink") 지니고 있는 상호운영성의 한계점을 극복하기 위해 새롭게 등장한 무선 데이터 기술이다. DASH7은 433MHz 주파수 대역에서 운영되는 개방형 표준으로서 UWB나 [WiFi](https://ko.wikipedia.org/wiki/WiFi "wikilink") 보다 낮은 저전력으로 방출이 되며 27.77kbps(최대 250kbps)까지 데이터를 전송할 수 있다. 또한 전자 기기간에 간결하면서도 가볍고 안정성 있는 통신을 제공하며 시간 단위가 아닌 연 단위의 배터리 수명으로 확장 시킬 수 있는 전원관리 기술을 도입하여 기존에 개발되었던 태그보다 훨씬 더 경제적인 태그 개발을 가능하게 한다.

## 등장

RFID 시장은 정부 주도의 사업으로 꾸준한 성장세를 보여왔으나 active RFID 시장은 passive RFID 시장에 비하여 아직까지 시장성이 미약한 실정이다. 이는 active RFID 장비의 높은 가격 및 기대 이하의 활용성과 실제 적용 사례의 미흡이 낳은 결과이기도 하다. 그러나 특히 433MHz 장비의 통신 규격을 제시하고 있는 ISO/IEC 18000-7의 명확하지 않은 해석(Grey Area)과 이로 인한 RFID 구조 및 ISO/IEC 18000-7 표준의 임의 해석으로 같은 표준에 따라서 개발된 장비임에도 불구하고 완성된 RFID 장비들 간의 상호운영성이 보장되지 않아 최종 사용자에게 통합된 active RFID 시스템을 제공하지 못한다는 큰 문제점을 내포하고 있다. 이에 2009년 2월 active RFID 시장의 성장을 촉진하고 장비간 상호운영성을 확보하기 위해 RFID 업체와 관련 연구 기관 및 고객사들이 모여 새로운 무선 데이터 기술인 DASH7을 명명하고 이를 운영하기 위한 [DASH7 Alliance](https://web.archive.org/web/20090321090926/http://www.dash7.org/)를 설립하였다.

## 특징

DASH7은 DASH7 Alliance에서 상호운영성 확보를 위해 제시하는 기술을 의미하며 현재 active RFID 통신 규격을 규정하고 있는 ISO/IEC 18000-7이 지니고 있는 문제점들을 해결할 수 있다. 여러 분야에서 비교해 볼 때 기존의 무선 데이터 기술인 WiFi를 비롯하여 ZigBee, passive RFID 그리고 GPRS 보다 탁월한 스펙과 성능을 보유하고 있다고 할 수 있다. DASH7은 전력 효율성과 배터리 수명, 글로벌 주파수 유효성(글로벌 로밍), 802.11n(2.45GHz) 주파수의 간섭과 위치 및 센싱 애플리케이션 활용면에서 WiFi나 ZigBee, passive RFID, 그리고 GPRS 보다 높은 이점을 가지고 있으며 저가의 장비를 공급할 수 있다는 장점 또한 갖고 있다. 한편 국제 표준 준수 및 RTLS로의 활용,, 태그간의 통신과 센서 지원 및 보안의 측면에서도 기타 무선 기술 표준에 뒤지지 않는 강점을 보이고 있다. 대부분의 기본 센싱 기능에서 RFID는 저전력 [RF](https://ko.wikipedia.org/wiki/RF "wikilink") 기술들과 제품 라인들을 포함하여 active RFID로 간주되어 왔었는데 DASH7에 기반한 active RFID 태그는 passive RFID 와 비교했을 때 매우 낮은 전력 특징을 지니고 있다.

| Technology | 국제표준            | 주파수대역                     | 글로벌사용                                     | 액체투과 | 콘크리트투과 | 범위      | 평균 power draw | 평균 latency                      | 장비가격 | 멀티홉 | 센서지원 | 보안지원 | 최대비트속도      |
| ---------- | --------------- | ------------------------- | ----------------------------------------- | ---- | ------ | ------- | ------------- | ------------------------------- | ---- | --- | ---- | ---- | ----------- |
| DASH7      | ISO/IEC 18000-7 | 433 MHz                   | Yes                                       | Yes  | Yes    | 1,000 m | 30–60 mw      | 2.5–5 seconds                   | $10+ | Yes | Yes  | Yes  | 28 kbps     |
| ZigBee     | IEEE 802.15.4   | 2.4 GHz, 915 MHz, 868 MHz | 2.4 GHz – yes; 915 MHz – no; 868 MHz – no | No   | No     | 10–75 m | 300–600 mw    | typ \<100ms potentially minutes | $10+ | Yes | Yes  | Yes  | 20–240 kbps |

## BLAST 기술

DASH7을 기반으로 하는 네트워크는 기존의 무선 네트워크와는 다르다. 기존의 무선 네트워크 기술에서는 전력 제한과 네트워크 속도를 가장 중요한 특징으로 삼고 있지만 DASH7 네트워크는 저전력 애플리케이션을 지원하고 데이터 전송이 산발적으로 이루어진다. 이와 같은 DASH7 기술 특징을 BLAST라는 개념으로 설명할 수 있다.\[1\]

*B*ursty: 데이터 전송은 산발적으로 이루어지며 비디오나 오디오와 같은 형태의 데이터 컨텐츠는 포함하지 않는다.

*L*ight: 일반적인 애플리케이션에서 패킷 사이즈는 256 바이트로 제한된다. 대용량으로 전달되는 연속적인 패킷이 발생할 수도 있으나 가급적 256 바이트로 제한한다.

*AS*ynchronous: DASH7의 주요 통신 방법은 명령-응답 형식으로 구성된다.

*T*ransitive: DASH7 장비 시스템은 본래 이동적이며 다른 무선 기술과는 다르게 메인으로 업로드는 되지만 다운로드는 되지 않는 특성을 가지고 있다. 따라서 장비는 기지국과 같은 고정된 인프라에 의해 관리될 필요가 없다.

개념적으로 BLAST는 DASH7 애플리케이션 모델에 적합하며 저전력 RF에도 매우 잘 적응한다. DASH7 시스템들은 상하 수직적인 구조인 기존의 전통적인 네트워크로 이해되어서는 안되며 이전에는 접근할 수 없었던 데이터의 비구조풀(Structureless pool)로서 이해되어야 한다.

## [DASH7 Alliance](https://web.archive.org/web/20090321090926/http://www.dash7.org/)

DASH7의 어원은 433MHz 대역의 air interface 통신을 정의하는 국제 표준인 ISO/IEC 18000-7의 '-7(dash seven)'에서 따온 것이다. DASH7 Alliance는 국제 표준인 ISO/IEC 18000-7을 기반으로 한다는 점에서 IEEE 802.11 Wi-Fi Alliance와 비슷한 성격을 지니고 있다. ISO/IEC 18000-7은 Savi Technology의 IP로써 active RFID 솔루션의 대표적인 표준으로 사용이 되고 있으며 ISO/IEC 18000-7 제품을 개발 및 생산하는 업체들에게 국제 표준을 제시하여 왔다. 그러나 ISO/IEC 18000-7 표준의 명확하지 않은 해석과 이를 기반으로 만들어진 장비들 간의 상호운영성을 확보하지 못한다는 문제점이 드러나게 되자 이를 해결하기 위하여 관련 업체들과 함께 DASH7 Alliance를 형성 하였다. DASH7 Alliance의 주요 목적은 RFID 태그와 리더를 개발하는 업체들의 제품 간 상호운영성 및 안정성을 보장하고 현재 몇몇 분야에만 제한되어 있는 RFID 사업 영역을 확장하여 전체 RFID 시장 확장에 기여하는 데에 있다. DASH7 Alliance에서 제시하는 ISO 18000-7 표준 기반의 상호운영성에는 일반 상호운영성, 저주파 wake-up 상호운영성, 센서 상호운영성, 그리고 화물보안 상호운영성이 있다. 4개 분야의 상호운영성을 확보하기 위하여 DASH7 Alliance는 Business Working Group과 Technical Working Group, 그리고 Test and Certification Working Group의 세 개의 WG 분야로 구분하여 활발히 활동을 하고 있으며 내년에는 WG의 분야를 확산하여 적극적인 RFID 적용 분야를 넓혀갈 예정이다.

DASH7 Alliance에 현재 20여개의 RFID 하드웨어 업체와 관련 연구기관이 참여하고 있으며 DASH7 Alliance를 설립한 Founding Member로는 한국의 [KPC(케이피씨)](http://www.kpcnet.com), 미국의 [Savi Technology](http://www.savi.com), [RFind](https://web.archive.org/web/20180808003022/http://rfind.com/), [evigia](http://www.evigia.com), [IDENTEC Solutions](http://www.identecsolutions.com), [Hi-G-Tek](http://www.higtek.com)이 있다.

## 상호운영성 테스트

DASH7 기술의 상호운영성 테스트는 DASH7 Alliance의 기술 고문을 맡고 있는 피츠버그 대학교(University of Pittsburgh)의 RFID Center of Excellence 연구소에서 시행된다. RFID Center of Excellence 연구소는 ISO/IEC 18000-7 기반 제품들의 상호운영성 테스트를 위한 시설 및 장비를 갖추고 있으며 DASH7 Alliance에 가입된 업체들을 대상으로 제품 테스트를 시행하고 있다. IOS/IEC 18000-7 표준에 기반한 제품이 본 연구소에서 실시하는 상호운영성 테스트를 통과하면 해당 제품에 대해서 ISO/IEC 18000-7 상호운영성이 보장된다는 증명의 로고를 부착할 수 있도록 해준다.

## 각주

<references/>

[분류:무선 네트워크](https://ko.wikipedia.org/wiki/분류:무선_네트워크 "wikilink") [분류:무선 센서 네트워크](https://ko.wikipedia.org/wiki/분류:무선_센서_네트워크 "wikilink")

1.  Norair, JP (March 16, 2009). "Introduction to DASH7 Technologies, 1st Edition" (PDF). DASH7 Alliance. <http://www.dash7.org/DASH7%20WP%20ed1.pdf> . Retrieved 2009-09-04.