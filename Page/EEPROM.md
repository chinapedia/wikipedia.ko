> This article is converted from Wikipedia: [EEPROM](https://ko.wikipedia.org/wiki/EEPROM).


**EEPROM** (Electrically Erasable Programmable Read-Only Memory, E<sup>2</sup>PROM, )는 [비휘발성 메모리](../Page/비휘발성_메모리.md "wikilink")(NVM)의 하나이다.

## 역사

Hughes Aircraft의 엘리 하라이(Eli Harari)는 1977년 얇은 부동 게이트를 통한 파울러 노드하임 터널링을 이용하여 EEPROM을 발명했다.\[1\]\[2\] 그는 그 뒤 최초의 EEPROM 장치 개발에 착수하였고, 1983년 인텔의 George Perlegos가 인텔 2816이라는 제품을 처음 개발하였다.

## 개요

[UVEPROM](https://ko.wikipedia.org/wiki/UVEPROM "wikilink")이 자외선을 쏘며 내용을 지우는 반면 EEPROM은 전기적으로만 지울 수 있는 [PROM](https://ko.wikipedia.org/wiki/PROM "wikilink")으로 칩의 한 핀에 전기적 신호를 가해줌으로써 내부 데이터가 지워지게 되어 있는 롬이다. 데이터를 삭제하기 위한 전용 이레이저가 따로 필요하지 않으며 하나의 [롬 라이터를](https://ko.wikipedia.org/wiki/롬_라이터 "wikilink") 사용해서 쓰고 지울 수 있다. 그러나 EEPROM은 전기를 노출시킴으로써 한 번에 1 바이트씩만 지울 수 있기 때문에 [플래시 메모리와](../Page/플래시_메모리.md "wikilink") 비교하면 매우 느리며 반복 기록 횟수에 제한이 있는데 약 10만 번 정도이다.

EEPROM은 인터페이스에 따라 직렬 버스와 병렬 버스로 나뉜다.

  - 직렬 버스
      - 보통 [SPI](https://ko.wikipedia.org/wiki/SPI "wikilink")나 [I²C](../Page/I²C.md "wikilink"), [1-Wire](https://ko.wikipedia.org/wiki/1-Wire "wikilink") [인터페이스로](https://ko.wikipedia.org/wiki/물리_인터페이스 "wikilink") 8핀 패키지로 구성된다.
      - 동작에 [OP-Code](https://ko.wikipedia.org/wiki/OP-Code "wikilink"), [주소](../Page/주소.md "wikilink"), [데이터](https://ko.wikipedia.org/wiki/데이터 "wikilink")의 3 단계가 필요하다.
  - 병렬 버스
      - 보통 8비트 데이터 버스로 칩 셀렉트와 쓰기 방지 핀을 가지고 있다.
      - 단순하고 빠르게 작동되지만 크기가 크고 핀 수(32개 이상)가 많다.

EEPROM은 [모뎀](../Page/모뎀.md "wikilink")이나 [비디오 카드](https://ko.wikipedia.org/wiki/비디오_카드 "wikilink"), [메인보드](../Page/메인보드.md "wikilink"), [SCSI](../Page/SCSI.md "wikilink") 컨트롤러 등에서 사용된다. 모뎀의 경우에는 내부에 사용자가 AT명령을 통해서 설정한 상태가 전원을 껐다 켠 후에도 그대로 유지되는데. 이것은 EEPROM에서 그 상태를 저장해 놓기 때문이다. 대부분의 비디오카드, 메인보드, SCSI 컨트롤러 등에서 EEPROM을 사용해 [점퍼없이](https://ko.wikipedia.org/wiki/점퍼_\(컴퓨팅\) "wikilink") 설정상태를 저장한다.

## 각주

[분류:기억 장치](https://ko.wikipedia.org/wiki/분류:기억_장치 "wikilink") [분류:비휘발성 메모리](https://ko.wikipedia.org/wiki/분류:비휘발성_메모리 "wikilink")

1.  <http://www.freepatentsonline.com/4115914.pdf>
2.