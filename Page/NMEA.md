> This article is converted from Wikipedia: [NMEA](https://ko.wikipedia.org/wiki/NMEA).


**NMEA** 라고 주로 불리는 **NMEA 0183**은 시간, 위치, 방위 등의 정보를 전송하기 위한 규격이다. NMEA 0183은 미국의 [NMEA](https://ko.wikipedia.org/wiki/해양_전자_협회 "wikilink")(The National Marine Electronics Association)에서 정의해 놓았다. 이 데이터들은 주로 [자이로컴퍼스](https://ko.wikipedia.org/wiki/자이로컴퍼스 "wikilink"), [GPS](../Page/GPS.md "wikilink"), [나침반](../Page/나침반.md "wikilink"), [관성항법장치](https://ko.wikipedia.org/wiki/관성항법장치 "wikilink")(INS)에 사용된다. NMEA 0183은 [ASCII](https://ko.wikipedia.org/wiki/ASCII "wikilink")코드로 직렬 방식의 통신을 사용한다.

## 레이어

**NMEA 0183**은 3가지 레이어로 구성되어 있으며, 이것은 각각 물리 계층, 데이터링크 계층, 애플리케이션 계층이다. 물리 계층은 [RS-232](../Page/RS-232.md "wikilink"), [RS-422](../Page/RS-422.md "wikilink") 등의 전기적인 전송 규격을 뜻한다. 데이터링크 계층은 Baud rate, Data bit, Parity bit, Stop bit 등을 정해 놓는다. Application Layer는 데이터를 전송하는 Sentence에 대한 규약이이며 GPS등에서 표준프로토콜이다.\[1\]

## 애플리케이션 레이어

애플리케이션 레이어에서의 문장 구조의 형식 및 특징은 다음과 같다.

  - '$'로 시작한다.
  - 첫 두 자리는 제품의 종류를 나타낸다. GPS 제품일 경우 GP, 수심 측정 장비인 Depth Sounder 제품일 경우 SD 를 사용한다.
  - 다음 세 자리는 해당 프로토콜이 가지고 있는 데이터의 종류를 나타낸다.
  - 데이터의 구분은 ','로 하며 '\*'로 끝난다.
  - '$'와 '\*'사이의 모든 데이터를 [XOR](https://ko.wikipedia.org/wiki/XOR "wikilink")(exclusive or) 연산을 하여 체크섬 값을 만들어 추가한다.
  - <CR><LF>를 붙인다.

주로 사용되는 문장에 대한 예시와 설명은 다음과 같다.

  - Elextech사에서 만든 G1800s라는 GPS모듈이다.
  - Baud Rate는 9600bps이다.

### GPGGA

*GPGGA* *Global Positioning System Fix Data*라고 한다. 여기에서 주로 알 수 있는 것은 시간, 위도, 경도, 고도 등이다.

  - 114455.532는 시간으로서 Zulu time (그리니치 표준시) 기준으로 11시 44분 55.532초를 뜻한다.
  - 3735.0079는 위도로서 37도 35.0079분을 뜻한다. 도(degree) 단위로 환산시, 35.0079/60 = 0.5 대략 37.5도가 된다.
  - 뒤의 N은 북위를 뜻한다. 적도 남쪽에 있다면 S가 된다.
  - 12701.6446은 경도로서 127도 1.6446분을 뜻한다. 도(degree) 단위로 환산시, 1.6446/60 = 0.027 대략 127.0도가 된다.
  - 뒤의 E는 동경을 뜻한다. W가 되면 서경이 된다.
  - '1'은 Fix의 종류를 뜻한다. 이 자리의 숫자에 따른 뜻은 다음과 같다.
      - 0 : Invalid 잘못된 데이터. 주로 위성이 안 잡힐 경우.
      - 1 : GPS에서 제공하는 기본 위성을 가지고만 계산할 경우.
      - 2 : DGPS를 이용하여 보정하여 계산할 경우
      - DGPS를 이용할 경우 더욱 정확한 측정이 가능해진다. DGPS는 지구의 지표의 위치가 명확히 알려진 곳에 기지국을 설치하거나 또 다른 위성(NAVSTAR GPS위성이 아닌 타 위성)이 GPS송출 신호를 내보내어 보정하도록 하는 방법이다. 보통 15M정도의 오차를 가지는 GPS가 DGPS로 보정할 경우 5M로 오차가 줄어들게 된다.
  - '03'은 계산에 사용한 위성을 개수를 나타낸다. 위치를 알기 위해서 최소3개 이상의 신호를 받아야 한다.
  - '7.9'는 horizontal dilution of Precision으로 2차원적 오차결정(수평방향)을 뜻한다.
  - '48.8M'는 해수면 기준 고도이다.
  - '19.6M'는 WGS-84에서 정해놓은 타원체로서 모델링한 지구와 구체로서 모델링된 지구의 고도차이를 뜻한다.
  - '0.0'과 '0000'은 DGPS 사용시 마지막으로 update한 시간과 DGPS 기지국의 ID이다.
  - '48'은 Check Sum이다.

### GPGSV

*GPGSV* *GPS Satellites in View*는 현재 GPS Module이 수신할 수 있는 모든 위성의 정보이다. 모든 위성을 계산에 사용하지는 않는다.

  - '3'은 앞으로 나올 GPGSV가 총 몇 개의 Sentence일지 알려준다. 여기에서는 총 3개의 Sentence이다.
  - '1'은 GPGSV Sentence중 몇 번째의 Sentence인지 알려준다. 여기에서는 1번째 Sentence이다.
  - '10'은 현재 수신할 수 있는 모든 위성의 개수를 나타낸다.
  - '03,86,244,00'는
      - 3번 위성이고,
      - 현재 자신의 위치에서 86도 (degree) elevation
      - 244도 (degree)의 Azimuth
      - 신호대잡음비 (SNR)은 0 이다.
  - '77'은 Checksum이다.

최대 4개의 위성이 하나의 Sentence에 들어갈 수 있다.

### GPRMC

*GPRMC* *Recommended Minimum data*는 추천되는 최소한의 데이터들이다.

  - 114455.532는 시간으로서 Zulu time (그리니치 표준시) 기준으로 11시 44분 55.532초를 뜻한다.
  - A는 GPS 신호의 신뢰성을 뜻한다. (A = 신뢰할 수 있음, V = 신뢰할 수 없음)
  - 3735.0079는 위도로서 37도 35.0079분을 뜻한다. 도(degree) 단위로 환산시, 35.0079/60 = 0.5 대략 37.5도가 된다.
  - 뒤의 N은 북위를 뜻한다. 적도 남쪽에 있다면 S가 된다.
  - 12701.6446은 경도로서 127도 1.6446분을 뜻한다. 도(degree) 단위로 환산시, 1.6446/60 = 0.027 대략 127.0도가 된다.
  - 뒤의 E는 동경을 뜻한다. W가 되면 서경이 된다.
  - '0.000000'은 Speed over ground로서 knots 단위의 속도계이다. 비행기에서는 KIAS라는 속도 단위를 사용하고, 배에서는 Knots를 사용한다. KIAS는 Knots indicator air speed의 약자이다. km/h로 변환시 대략 1.8을 곱한다.
  - '121.61'은 Track Angle in degree true로서, 진행 방향을 정북을 0도부터 359도 까지 표현한 것이다. 121.61은 대략 동남쪽이다.
  - '110706'은 Date를 뜻한다. 여기에서는 11th, July, 2006이며 2006년 7월 11일이다.
  - ' '는 Magnetic Variation으로서 나침반이다. 예시의 GPS Module은 나침반이 내장되어 있지 않다.
  - '\*0A'는 체크섬이다.

### GPGSA

GSA는 "GNSS DOP and Active Satellite"를 의미한다. 데이타를 제공하는 위성을 나열하는 GSA 레코드에는 위성 번호에 대한 12개의 필드가 포함되어 있지만 8개의 위성 만 고려되므로 4개의 필드는 비어 있다.GSA는 단독으로 쓰이기 보다는 GSV와 상호참조로 위성상태를 확인하거나 시각적 분석을 위한 GLONASS 인공위성 및 이들의 자료등을 활용할수있다. 이 GSA 문장의 각각에는 대화자 ID GN가 있어야한다. 인공위성은 조합된 솔루션에 사용되며 각각의 위치 데이타에 사용된 결합 위성은 PDOP(축위오차), HDOP(수평오차) 및 VDOP(수직오차)를가지고있다. \[2\]

  -
    $--GSA : 문장 ID
    a : 모드1 - A = 2D/3D 자동변환 ,M =수동 전환
    x : 모드2 - 2 = 2D , 3=3D
    xx :사용된 위성번호 1\~12개
    VDOP, HDOP, PDOP : 오차값
    hh : [체크섬](../Page/체크섬.md "wikilink")

## 체크섬 코드

[자바](../Page/자바_\(프로그래밍_언어\).md "wikilink") 버전\[3\]

```
 char checkSum(String nmeaStr) {
  char check = 0; // iterate over the string, XOR each byte with the total sum;
  for (int c = 0; c < theseChars.length(); c++) {
  check = char(check ^ theseChars.charAt(c));
 } // return the result return check;
}
```

## 같이 보기

  - [GPS](../Page/GPS.md "wikilink")
  - [UTC](https://ko.wikipedia.org/wiki/UTC "wikilink")

## 외부 링크

  - [NMEA 홈페이지](http://www.nmea.org/)

  - [NMEA 0183](https://web.archive.org/web/20100915131506/http://www.nmea.org/content/nmea_standards/nmea_083_v_400.asp), NMEA

  - [NMEA에 대한 질문과 대답](https://web.archive.org/web/20140215150802/http://www.kh-gps.de/nmea.faq)

  - [NMS 프로토콜의 생성과 분석에 관한 자유 C 라이브러리](http://nmea.sourceforge.net)

  - [NMEA 자료 정보](http://www.gpsinformation.org/dale/nmea.htm)

## 참고

  - [NMEA](https://web.archive.org/web/20190121232511/https://www.nmea.org/content/nmea_standards/erratanmea.asp)
  - [NMEA 0183 Developers Information - NMEA 0183 Developers Information](https://www.nmea.org/Assets/20160217%200183%20manufacturer%20codes.pdf)
  - [NMEA 0183 SENTENCES](http://linux.geodatapub.com/shipwebpages/manuals/apos/hpr%20400%20nmea%200183%20sentences.pdf)

[분류:GPS](https://ko.wikipedia.org/wiki/분류:GPS "wikilink") [분류:네트워크 프로토콜](https://ko.wikipedia.org/wiki/분류:네트워크_프로토콜 "wikilink")

1.  [GPS 센서](https://www.u-blox.com/sites/default/files/products/documents/NEO-6_DataSheet_%28GPS.G6-HW-09005%29.pdf)
2.  [NMEA](https://www.nmea.org/content/nmea_standards/erratanmea.asp)
3.  ([CCL3](https://ko.wikipedia.org/wiki/크리에이티브_커먼즈_라이선스 "wikilink"))출처: <http://techlog.gurucat.net/305> \[하얀쿠아의 이것저것 만들기 Blog\]