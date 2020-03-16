> This article is converted from Wikipedia: [ATcommand](https://ko.wikipedia.org/wiki/ATcommand).


**ATcommand** 또는 **헤이즈 커맨드 세트**(Hayes command set) 또는 줄여서 AT는 1981년 Hayes Smartmodem 300 보오 모뎀을 위해 [데니스 헤이즈](https://ko.wikipedia.org/wiki/데니스_헤이즈 "wikilink")(Dennis Hayes)가 처음 개발 한 특정 명령 언어이다.\[1\] 이후 [마이크로컨트롤러](../Page/마이크로컨트롤러.md "wikilink")(MCU),블루투스등 이들과의 확장성이 용이한 통신 프로토콜로 사용되고있다.

명령 세트는 전화 걸기, 전화 끊기 및 연결 매개 변수 변경과 같은 작업에 대한 명령을 생성하기 위해 결합될 수있는 일련의 짧은 텍스트 문자열로 구성된다. 대다수의 전화 접속 모뎀은 다양한 변형에서 Hayes 명령인 AT command를 사용하고있다.

명령 집합은 가장 오래된 300 비트 / s 모뎀에서 지원하는 작업만 포함한다. 고속 모뎀의 추가 기능을 제어하기 위해 새로운 명령이 필요할 때 주요 공급 업체 각각에서 다양한 일회성 표준이 나왔다. 이들은 계속해서 기본 명령 구조와 구문을 공유했지만 Hayes와 USR에서는 '&', Microcom에서는 '\\'와 같은 몇 가지 프리픽스(prefix) 문자를 사용하여 새로운 명령을 추가했다. 이 중 많은 부분이 SupraFAXModem 14400이 도입 된 후 AT는 확장과 그 이후의 시장에서의 표준을 위한 통합에 대한 재 표준화가 이루어졌다.

## 사용예

[블루투스](../Page/블루투스.md "wikilink") 및 [BLE에서의](../Page/Bluetooth_Low_Energy.md "wikilink") 사용 예

| 명령어                | 기능           | 비고                                   |
| ------------------ | ------------ | ------------------------------------ |
| AT                 | AT 통신상태확인    | 응답 OK                                |
| AT+TYPE 또는 AT+MODE | TYPE 또는 MODE | 보안모드: 0(전송모드 -초기값),1(PIO용),2(원격 페어링) |
| AT+PIN 또는 AT+PASS  | PIN 또는 PASS  | 핀번호 또는 패스워드                          |

  - 명령어 구문

AT(+명령어)(파라미터)

  - 질의응답 구문

AT(+명령어?)

## 전송속도

일반적으로 9600b 또는 115200b등을 사용한다.

## 함께보기

  - [통신 프로토콜](../Page/통신_프로토콜.md "wikilink")

## 참고

  - [conexant-Commands for HostProcessed and HostControlled Modems Reference Manual](https://web.archive.org/web/20151028101531/http://www.zoomtel.com/documentation/dial_up/100498D.pdf)
  - [SIM tech-SIM com, AT Command Set ,SIM5320 _ATC_V1.23](http://www.mt-system.ru/sites/default/files/simcom_sim5320_atc_en_v1.23.pdf)
  - [SIM com -BLE 4.0 modules(HM-10;HM-11)DataSheet](http://www.jnhuamao.cn/index_en.asp?ID=1)

[분류:네트워크 프로토콜](https://ko.wikipedia.org/wiki/분류:네트워크_프로토콜 "wikilink")

1.