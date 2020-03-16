> This article is converted from Wikipedia: [EPROM](https://ko.wikipedia.org/wiki/EPROM).


[섬네일](https://ko.wikipedia.org/wiki/파일:Eprom.jpg "wikilink") **EPROM**(Erasable PROM, 삭제 가능한 롬)은 필요할 때 기억된 내용을 지우고 다른 내용을 기록할 수 있는 롬이다. 지우는 방법에 따라 [자외선](../Page/자외선.md "wikilink")으로 지울 수 있는 **UVEPROM**(Ultra-Violet Erasable Programmable Read Only Memory)과 높은 전압으로 지울 수 있는 **EEPROM**(Electrically Erasable Programmable Read-Only Memory)로 나뉜다. 하지만 일반적으로 UVEPROM을 가리킨다.

UVEPROM은 1971년 인텔의 엔지니어인 Dov Frohman이 발명했으며 최초의 제품은 인텔 1702A이다.

기록은 [플로팅 게이트](https://ko.wikipedia.org/wiki/플로팅_게이트 "wikilink")(floating-gate) 트랜지스터에 고전압(보통 12V 전후)으로 전자를 주입하여 기록하며 플로팅 게이트는 절연되어 있어서 전원을 꺼도 전자는 보존되어 롬으로 사용할 수 있다. 그러나 여기에 강한 자외선(234nm)을 쬐게 되면 전자는 게이트의 절연막을 통과해 기록이 지워지게 된다. 보통 UVEPROM에는 석영유리창이 있어 다른 롬들과는 확연히 구분한다. 기록횟수는 고전압이 실리콘에 영향을 주기 때문에 20회 전후이며 차광 씰을 잘 부착하여 최적으로 보관한다면 약 10년 데이터 보관이 가능하다.

UVEPROM은 과거 [메인보드](../Page/메인보드.md "wikilink"), [그래픽카드](https://ko.wikipedia.org/wiki/그래픽카드 "wikilink")의 [바이오스](../Page/바이오스.md "wikilink") 칩이나 게임기의 롬으로 많이 사용되었다.

그리고 칩 패키지에서 창을 없앤 UVEPROM을 **OTP**(one-time programmable)라고 하는데 소거창이 없기 때문에 한번 기록 후 지울 수 없으며 주로 [마이크로컨트롤러](../Page/마이크로컨트롤러.md "wikilink")에서 볼 수 있다.

| EPROM 모델명      | 용량 ([비트](../Page/비트_\(단위\).md "wikilink"))              | 용량 ([바이트](../Page/바이트.md "wikilink")) | 길이([hex](https://ko.wikipedia.org/wiki/16진수 "wikilink")) | 주소(hex) | 공정         |
| -------------- | ------------------------------------------------------- | ------------------------------------- | -------------------------------------------------------- | ------- | ---------- |
| 1702, 1702A    | 2 [Kbit](https://ko.wikipedia.org/wiki/Kbit "wikilink") | 256                                   | 100                                                      | 000FF   | PMOS       |
| 2704           | 4 Kbit                                                  | 512                                   | 200                                                      | 001FF   | NMOS       |
| 2708           | 8 Kbit                                                  | 1 [KB](../Page/킬로바이트.md "wikilink")   | 400                                                      | 003FF   | NMOS       |
| 2716, 27C16    | 16 Kbit                                                 | 2 KB                                  | 800                                                      | 007FF   | NMOS, CMOS |
| 2732, 27C32    | 32 Kbit                                                 | 4 KB                                  | 1000                                                     | 00FFF   | NMOS, CMOS |
| 2764, 27C64    | 64 Kbit                                                 | 8 KB                                  | 2000                                                     | 01FFF   | NMOS, CMOS |
| 27128, 27C128  | 128 Kbit                                                | 16 KB                                 | 4000                                                     | 03FFF   | NMOS, CMOS |
| 27256, 27C256  | 256 Kbit                                                | 32 KB                                 | 8000                                                     | 07FFF   | NMOS, CMOS |
| 27512, 27C512  | 512 Kbit                                                | 64 KB                                 | 10000                                                    | 0FFFF   | NMOS, CMOS |
| 27C010, 27C100 | 1 [Mbit](https://ko.wikipedia.org/wiki/메가비트 "wikilink") | 128 KB                                | 20000                                                    | 1FFFF   | CMOS       |
| 27C020         | 2 Mbit                                                  | 256 KB                                | 40000                                                    | 3FFFF   | CMOS       |
| 27C040         | 4 Mbit                                                  | 512 KB                                | 80000                                                    | 7FFFF   | CMOS       |
| 27C080         | 8 Mbit                                                  | 1 [MB](../Page/메가바이트.md "wikilink")   | 100000                                                   | FFFFF   | CMOS       |

## 같이 보기

  - [ROM](../Page/고정_기억_장치.md "wikilink")
  - [PROM](https://ko.wikipedia.org/wiki/PROM "wikilink")

## 외부 링크

}}

  - [Detailed information about EPROM types and EPROM programming](http://www.progshop.com/shop/electronic/eprom-programming.html)

  - [Video of the Intel 1702 EPROM](https://www.youtube.com/watch?v=uKk7fVIZPE4)

[분류:기억 장치](https://ko.wikipedia.org/wiki/분류:기억_장치 "wikilink") [분류:비휘발성 메모리](https://ko.wikipedia.org/wiki/분류:비휘발성_메모리 "wikilink")