> This article is converted from Wikipedia: [CoAP](https://ko.wikipedia.org/wiki/CoAP).


**CoAP**(, 코앱)은 제약이 있는(constrained) 장치들을 위한 특수한 인터넷 애플리케이션 프로토콜로서 RFC 7252에 정의되었다. "노드"(node)로 불리는 해당 제약 장치들이 비슷한 프로토콜을 사용하는 더 넓은 인터넷과 통신할 수 있게 한다. COAP은 제약이 있는 동일한 네트워크(예: 저전력, 손실 네트워크)의 장치들 간에, 장치와 인터넷 상의 일반 노드 간에, 또 인터넷을 통해 참여한, 제약이 있는 각기 다른 네트워크 상의 장치 간에 사용하기 위해 설계되었다. 또, CoAP은 모바일 통신망의 SMS와 같은 다른 구조를 통해 사용되기도 한다.

CoAP은 [무선 센서 네트워크](https://ko.wikipedia.org/wiki/무선_센서_네트워크 "wikilink") 노드처럼 자원에 제약이 있는 장치들에서 사용할 목적으로 고안된 [서비스 계층](https://ko.wikipedia.org/wiki/서비스_계층 "wikilink") 프로토콜이다. CoAP은 단순한 웹 연동을 위해 [HTTP](https://ko.wikipedia.org/wiki/HTTP "wikilink")로 쉽게 변환되도록 설계되어 있으며 [멀티캐스트](../Page/멀티캐스트.md "wikilink") 지원과 같은 특수한 요건을 충족하면서도 부하가 매우 낮으며 단순한 편이다.\[1\]\[2\] 멀티캐스트, 낮은 부하, 단순성은 심도있게 [임베디드되는](https://ko.wikipedia.org/wiki/임베디드_시스템 "wikilink") 경향이 있고 전통적인 인터넷 장치보다 훨씬 더 적은 메모리와 전력 공급을 지니는 경향이 있는 [사물인터넷](../Page/사물인터넷.md "wikilink")(IoT) 및 [사물통신](https://ko.wikipedia.org/wiki/사물통신 "wikilink")(M2M) 장치에 매우 중요하다. 즉, 효율성이 매우 중요하다. CoAP은 [UDP](https://ko.wikipedia.org/wiki/사용자_데이터그램_프로토콜 "wikilink") 또는 UDP 유사 프로토콜을 지원하는 대부분의 장치에서 구동할 수 있다.

## 메시지 포맷

### CoAP 요청/응답 코드

요청 코드는 다음의 형태를 취한다:

| 바이트   |
| ----- |
| 0     |
| CLASS |

문서 상에서는 보통 \`<class>\`.\`\<code\>\`와 같은 형태로 표현된다.

#### CoAP 등록 코드

\[[https://www.iana.org/assignments/core-parameters/core-parameters.xhtml\#codes\]에서](https://www.iana.org/assignments/core-parameters/core-parameters.xhtml#codes%5D에서) CoAP의 최신 등록 코드를 볼 수 있다.

### CoAP 메시지 구조

| 바이트                    | 바이트  | 바이트                       | 바이트           |
| ---------------------- | ---- | ------------------------- | ------------- |
| 0                      | 1    | 2                         | 3             |
| VER                    | TYPE | TKL (토큰 길이: Token Length) | CoAP 요청/응답 코드 |
| 토큰 (TKL 바이트) (8바이트 최대) |      |                           |               |
| 옵션 (사용 가능한 경우)\[3\]    |      |                           |               |
| 1                      | 1    | 1                         | 1             |

CoAP 메시지 구조

CoAP 고정 헤더는 처음 4바이트이다. 이로써 토큰, 옵션, 페이로드를 생략할 경우 가장 작은 CoAP 메시지의 길이를 4바이트로 유지할 수 있게 한다.

이 매크로를 통해 C에서 고정 헤더의 정보를 쉽게 추출할 수 있다:

``` c
#define COAP_HEADER_VERSION(data)  ( (0xC0 & data[0])>>6    )
#define COAP_HEADER_TYPE(data)     ( (0x30 & data[0])>>4    )
#define COAP_HEADER_TKL(data)      ( (0x0F & data[0])>>0    )
#define COAP_HEADER_CLASS(data)    ( ((data[1]>>5)&0x07)    )
#define COAP_HEADER_CODE(data)     ( ((data[1]>>0)&0x1F)    )
#define COAP_HEADER_MID(data)      ( (data[2]<<8)|(data[3]) )
```

## 구현체

<table>
<thead>
<tr class="header">
<th><p>이름</p></th>
<th><p>프로그래밍 언어</p></th>
<th><p>구현된 CoAP 버전</p></th>
<th><p>클라이언트/서버</p></th>
<th><p>구현된 CoAP 기능</p></th>
<th><p>라이선스</p></th>
<th><p>링크</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>aiocoap</p></td>
<td><p>Python 3</p></td>
<td><p>RFC 7252</p></td>
<td><p>Client + Server</p></td>
<td><p>Blockwise Transfers, Observe (부분적)</p></td>
<td><p>MIT</p></td>
<td><p><a href="https://pypi.python.org/pypi/aiocoap">https://pypi.python.org/pypi/aiocoap</a></p></td>
</tr>
<tr class="even">
<td><p>Californium</p></td>
<td><p>Java</p></td>
<td><p>RFC 7252</p></td>
<td><p>Client + Server</p></td>
<td><p>Observe, Blockwise Transfers, DTLS</p></td>
<td><p>EPL+EDL</p></td>
<td><p><a href="https://web.archive.org/web/20181207034534/http://www.eclipse.org/californium/">https://web.archive.org/web/20181207034534/http://www.eclipse.org/californium/</a></p></td>
</tr>
<tr class="odd">
<td><p>cantcoap</p></td>
<td><p>C++/C</p></td>
<td><p>RFC 7252</p></td>
<td><p>Client + Server</p></td>
<td></td>
<td><p>BSD</p></td>
<td><p><a href="https://github.com/staropram/cantcoap">https://github.com/staropram/cantcoap</a></p></td>
</tr>
<tr class="even">
<td><p>Canopus</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/Go_(프로그래밍_언어)" title="wikilink">Go</a></p></td>
<td><p>RFC 7252</p></td>
<td><p>Client + Server</p></td>
<td><p>Core</p></td>
<td><p>Apache License 2.0</p></td>
<td><p><a href="https://github.com/zubairhamed/canopus">https://github.com/zubairhamed/canopus</a></p></td>
</tr>
<tr class="odd">
<td><p>CoAP implementation for Go</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/Go_(프로그래밍_언어)" title="wikilink">Go</a></p></td>
<td><p>RFC 7252</p></td>
<td><p>Client + Server</p></td>
<td><p>Core + Draft Subscribe</p></td>
<td><p>MIT</p></td>
<td><p><a href="https://github.com/dustin/go-coap">https://github.com/dustin/go-coap</a></p></td>
</tr>
<tr class="even">
<td><p>CoAP.NET</p></td>
<td><p>C#</p></td>
<td><p>RFC 7252, coap-13, coap-08, coap-03</p></td>
<td><p>Client + Server</p></td>
<td><p>Core, Observe, Blockwise Transfers</p></td>
<td><p>3-clause BSD</p></td>
<td><p><a href="https://github.com/smeshlink/CoAP.NET">https://github.com/smeshlink/CoAP.NET</a></p></td>
</tr>
<tr class="odd">
<td><p>CoAPSharp</p></td>
<td><p>C#, .NET</p></td>
<td><p>RFC 7252</p></td>
<td><p>Client + Server</p></td>
<td><p>Core, Observe, Block, RD</p></td>
<td><p>LGPL</p></td>
<td><p><a href="http://www.coapsharp.com">http://www.coapsharp.com</a></p></td>
</tr>
<tr class="even">
<td><p>CoAPthon</p></td>
<td><p>Python</p></td>
<td><p>RFC 7252</p></td>
<td><p>Client + Server + Forward Proxy + Reverse Proxy</p></td>
<td><p>Observe, Multicast server discovery, CoRE Link Format parsing, Block-wise</p></td>
<td><p>MIT</p></td>
<td><p><a href="https://github.com/Tanganelli/CoAPthon">https://github.com/Tanganelli/CoAPthon</a></p></td>
</tr>
<tr class="odd">
<td><p>CoAP Shell</p></td>
<td><p>Java</p></td>
<td><p>RFC 7252</p></td>
<td><p>Client</p></td>
<td><p>Observe, Blockwise Transfers, DTLS</p></td>
<td><p>Apache License 2.0</p></td>
<td><p><a href="https://github.com/tzolov/coap-shell">https://github.com/tzolov/coap-shell</a></p></td>
</tr>
<tr class="even">
<td><p>Copper</p></td>
<td><p>JavaScript (Browser Plugin)</p></td>
<td><p>RFC 7252</p></td>
<td><p>Client</p></td>
<td><p>Observe, Blockwise Transfers</p></td>
<td><p>3-clause BSD</p></td>
<td><p><a href="https://github.com/mkovatsc/Copper">https://github.com/mkovatsc/Copper</a> <a href="https://addons.mozilla.org/firefox/addon/copper-270430/">https://addons.mozilla.org/firefox/addon/copper-270430/</a></p></td>
</tr>
<tr class="odd">
<td><p>eCoAP</p></td>
<td><p>C</p></td>
<td><p>RFC 7252</p></td>
<td><p>Client + Server</p></td>
<td><p>Core</p></td>
<td><p>MIT</p></td>
<td><p><a href="https://gitlab.com/jobol/ecoap">https://gitlab.com/jobol/ecoap</a></p></td>
</tr>
<tr class="even">
<td><p>Erbium for Contiki</p></td>
<td><p>C</p></td>
<td><p>RFC 7252</p></td>
<td><p>Client + Server</p></td>
<td><p>Observe, Blockwise Transfers</p></td>
<td><p>3-clause BSD</p></td>
<td><p><a href="http://www.contiki-os.org/">http://www.contiki-os.org/</a> (er-rest-example)</p></td>
</tr>
<tr class="odd">
<td><p>iCoAP</p></td>
<td><p>Objective-C</p></td>
<td><p>RFC 7252</p></td>
<td><p>Client</p></td>
<td><p>Core, Observe, Blockwise Transfers</p></td>
<td><p>MIT</p></td>
<td><p><a href="https://github.com/stuffrabbit/iCoAP">https://github.com/stuffrabbit/iCoAP</a></p></td>
</tr>
<tr class="even">
<td><p>jCoAP</p></td>
<td><p>Java</p></td>
<td><p>RFC 7252</p></td>
<td><p>Client + Server</p></td>
<td><p>Observe, Blockwise Transfers</p></td>
<td><p>Apache License 2.0</p></td>
<td><p><a href="https://code.google.com/p/jcoap/">https://code.google.com/p/jcoap/</a></p></td>
</tr>
<tr class="odd">
<td><p>libcoap</p></td>
<td><p>C</p></td>
<td><p>RFC 7252</p></td>
<td><p>Client + Server</p></td>
<td><p>Observe, Blockwise Transfers, DTLS</p></td>
<td><p>BSD/GPL</p></td>
<td><p><a href="https://github.com/obgm/libcoap">https://github.com/obgm/libcoap</a></p></td>
</tr>
<tr class="even">
<td><p>LibNyoci</p></td>
<td><p>C</p></td>
<td><p>RFC 7252</p></td>
<td><p>Client + Server</p></td>
<td><p>Core, Observe, Block, DTLS</p></td>
<td><p>MIT</p></td>
<td><p><a href="https://github.com/darconeous/libnyoci">https://github.com/darconeous/libnyoci</a></p></td>
</tr>
<tr class="odd">
<td><p>lobaro-coap</p></td>
<td><p>C</p></td>
<td><p>RFC 7252</p></td>
<td><p>Client + Server</p></td>
<td><p>Observe, Blockwise Transfers</p></td>
<td><p>MIT</p></td>
<td><p><a href="http://www.lobaro.com/lobaro-coap">http://www.lobaro.com/lobaro-coap</a></p></td>
</tr>
<tr class="even">
<td><p>microcoap</p></td>
<td><p>C</p></td>
<td><p>RFC 7252</p></td>
<td><p>Client + Server</p></td>
<td></td>
<td><p>MIT</p></td>
<td><p><a href="https://github.com/1248/microcoap">https://github.com/1248/microcoap</a></p></td>
</tr>
<tr class="odd">
<td><p>nCoap</p></td>
<td><p>Java</p></td>
<td><p>RFC 7252</p></td>
<td><p>Client + Server</p></td>
<td><p>Observe, Blockwise Transfers, CoRE Link Format, <a href="https://tools.ietf.org/html/draft-kleine-core-coap-endpoint-id-01">Endpoint-ID-Draft</a></p></td>
<td><p>BSD</p></td>
<td><p><a href="https://github.com/okleine/nCoAP">https://github.com/okleine/nCoAP</a></p></td>
</tr>
<tr class="even">
<td><p>node-coap</p></td>
<td><p>Javascript</p></td>
<td><p>RFC 7252</p></td>
<td><p>Client + Server</p></td>
<td><p>Core, Observe, Block</p></td>
<td><p>MIT</p></td>
<td><p><a href="https://github.com/mcollina/node-coap">https://github.com/mcollina/node-coap</a></p></td>
</tr>
<tr class="odd">
<td><p>Ruby coap</p></td>
<td><p>Ruby</p></td>
<td><p>RFC 7252</p></td>
<td><p>Client + Server (david)</p></td>
<td><p>Core, Observe, Block, RD</p></td>
<td><p>MIT, GPL</p></td>
<td><p><a href="https://github.com/nning/coap">https://github.com/nning/coap</a><br />
<a href="https://web.archive.org/web/20180611002224/https://github.com/nning/david">https://web.archive.org/web/20180611002224/https://github.com/nning/david</a></p></td>
</tr>
<tr class="even">
<td><p>Sensinode C Device Library</p></td>
<td><p>C</p></td>
<td><p>RFC 7252</p></td>
<td><p>Client + Server</p></td>
<td><p>Core, Observe, Block, RD</p></td>
<td><p>Commercial</p></td>
<td><p><a href="https://silver.arm.com/browse/SEN00">https://silver.arm.com/browse/SEN00</a></p></td>
</tr>
<tr class="odd">
<td><p>Sensinode Java Device Library</p></td>
<td><p>Java SE</p></td>
<td><p>RFC 7252</p></td>
<td><p>Client + Server</p></td>
<td><p>Core, Observe, Block, RD</p></td>
<td><p>Commercial</p></td>
<td><p><a href="https://silver.arm.com/browse/SEN00">https://silver.arm.com/browse/SEN00</a></p></td>
</tr>
<tr class="even">
<td><p>Sensinode NanoService Platform</p></td>
<td><p>Java SE</p></td>
<td><p>RFC 7252</p></td>
<td><p>Cloud Server</p></td>
<td><p>Core, Observe, Block, RD</p></td>
<td><p>Commercial</p></td>
<td><p><a href="https://silver.arm.com/browse/SEN00">https://silver.arm.com/browse/SEN00</a></p></td>
</tr>
<tr class="odd">
<td><p>SwiftCoAP</p></td>
<td><p>Swift</p></td>
<td><p>RFC 7252</p></td>
<td><p>Client + Server</p></td>
<td><p>Core, Observe, Blockwise Transfers</p></td>
<td><p>MIT</p></td>
<td><p><a href="https://github.com/stuffrabbit/SwiftCoAP">https://github.com/stuffrabbit/SwiftCoAP</a></p></td>
</tr>
<tr class="even">
<td><p>TinyOS CoapBlip</p></td>
<td><p>nesC/C</p></td>
<td><p>coap-13</p></td>
<td><p>Client + Server</p></td>
<td><p>Observe, Blockwise Transfers</p></td>
<td><p>BSD</p></td>
<td><p><a href="https://web.archive.org/web/20130312140509/http://docs.tinyos.net/tinywiki/index.php/CoAP">https://web.archive.org/web/20130312140509/http://docs.tinyos.net/tinywiki/index.php/CoAP</a></p></td>
</tr>
<tr class="odd">
<td><p>txThings</p></td>
<td><p>Python (Twisted)</p></td>
<td><p>RFC 7252</p></td>
<td><p>Client + Server</p></td>
<td><p>Blockwise Transfers, Observe (partial)</p></td>
<td><p>MIT</p></td>
<td><p><a href="https://github.com/mwasilak/txThings/">https://github.com/mwasilak/txThings/</a></p></td>
</tr>
<tr class="even">
<td><p>FreeCoAP</p></td>
<td><p>C</p></td>
<td><p>RFC 7252</p></td>
<td><p>Client + Server + HTTP/CoAP Proxy</p></td>
<td><p>Core, DTLS, Blockwise Transfers</p></td>
<td><p>BSD</p></td>
<td><p><a href="https://github.com/keith-cullen/FreeCoAP">https://github.com/keith-cullen/FreeCoAP</a></p></td>
</tr>
<tr class="odd">
<td><p>coap-rs</p></td>
<td><p>Rust</p></td>
<td><p>RFC 7252</p></td>
<td><p>Client + Server</p></td>
<td></td>
<td><p>MIT</p></td>
<td><p><a href="https://github.com/Covertness/coap-rs">https://github.com/Covertness/coap-rs</a></p></td>
</tr>
<tr class="even">
<td><p>YaCoAP</p></td>
<td><p>C</p></td>
<td></td>
<td></td>
<td></td>
<td><p>MIT</p></td>
<td><p><a href="https://github.com/RIOT-Makers/YaCoAP">https://github.com/RIOT-Makers/YaCoAP</a></p></td>
</tr>
</tbody>
</table>

## 프록시 구현

  - [Squid 3.1.9 with transparent HTTP-CoAP mapping module](http://telecom.dei.unipd.it/pages/read/90/)
  - [jcoap Proxy](https://code.google.com/p/jcoap/)
  - [Californium cf-proxy](https://github.com/mkovatsc/Californium)
  - [CoAPthon](https://github.com/Tanganelli/CoAPthon)
  - [FreeCoAP](https://github.com/keith-cullen/FreeCoAP)

## 보안 문제

프로토콜 표준이 [DDoS](https://ko.wikipedia.org/wiki/DDoS "wikilink") 증폭 공격의 위협을 완화하기 위한 대비책이 있지만\[4\], 이 대비책들은 실제로 구현되어 있지 않으므로\[5\], 주로 중국에 위치한 580,000개 이상이 표적이 되어 최대 320Gbps의 공격을 받고 있다\[6\].

## 같이 보기

  - [사물인터넷](../Page/사물인터넷.md "wikilink")
  - [OMA Lightweight M2M](https://ko.wikipedia.org/wiki/OMA_LWM2M "wikilink")
  - [사물 웹](https://ko.wikipedia.org/wiki/사물_웹 "wikilink")

## 각주

[분류:HTTP](https://ko.wikipedia.org/wiki/분류:HTTP "wikilink") [분류:응용 계층 프로토콜](https://ko.wikipedia.org/wiki/분류:응용_계층_프로토콜 "wikilink") [분류:사물인터넷](https://ko.wikipedia.org/wiki/분류:사물인터넷 "wikilink")

1.  [RFC 7252, Constrained Application Protocol (CoAP)](https://tools.ietf.org/html/rfc7252)
2.  "[Integrating Wireless Sensor Networks with the Web](http://hinrg.cs.jhu.edu/joomla/images/stories/IPSN_2011_koliti.pdf)" , Walter, Colitti 2011
3.  [Options Numbers](https://www.iana.org/assignments/core-parameters/core-parameters.xhtml#option-numbers)
4.  ["TLS 1.3 is going to save us all, and other reasons why IoT is still insecure", Dani Grant, 2017-12-24](https://blog.cloudflare.com/why-iot-is-insecure/)
5.  ["When Machines Can't Talk: Security and Privacy Issues of Machine-to-Machine Data Protocols", Federico Maggi and Rainer Vosseler, 2018-12-06](https://i.blackhat.com/eu-18/Thu-Dec-6/eu-18-Maggi-When-Machines-Cant-Talk-wp.pdf)
6.  ["The CoAP protocol is the next big thing for DDoS attacks", Catalin Cimpanu, 2018-12-05](https://www.zdnet.com/article/the-coap-protocol-is-the-next-big-thing-for-ddos-attacks/)