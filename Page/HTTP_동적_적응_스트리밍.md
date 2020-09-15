> This article is converted from Wikipedia: [HTTP 동적 적응 스트리밍](https://ko.wikipedia.org/wiki/HTTP_동적_적응_스트리밍).


**HTTP 동적 적응 스트리밍**(Dynamic Adaptive Streaming over HTTP, **DASH** 또는 **MPEG-DASH**)은 전통적인 [HTTP](../Page/HTTP.md "wikilink") 웹 서버로부터 전달되는, 인터넷을 경유하는 미디어의 고품질 [스트리밍](../Page/스트리밍.md "wikilink")을 가능케 하는 [적응 비트레이트 스트리밍](https://ko.wikipedia.org/wiki/적응_비트레이트_스트리밍 "wikilink") 기술의 하나이다. 애플의 [HTTP 라이브 스트리밍](https://ko.wikipedia.org/wiki/HTTP_라이브_스트리밍 "wikilink")(HLS) 솔루션과 비슷하게 MPEG-DASH는 내용을 일련의 작은 크기의 HTTP 기반 파일 세그먼트들로 분리시킴으로써 동작하며, 각 세그먼트는 영화나 스포츠 이벤트 생방송 등 잠재적으로 수시간에 걸친 내용물의 재생 시간의 짧은 간격(interval)을 포함하고 있다. 이 콘텐츠는 다양한 비트레이트로 이용이 가능하다. 콘텐츠가 MPEG-DASH 클라리언트에 의해 재생되면 클라이언트는 비트레이트 적응(ABR) 알고리즘을 사용하여\[1\] 재생 시 멈춤이나 재버퍼링을 일으키지 않고 다운로드할 수 있도록 가능한 최고 비트레이트의 세그먼트를 자동으로 선별한다.\[2\] 현재의 MPEG-DASH 참조 클라이언트 [dash.js](https://reference.dashif.org/dash.js)는 버퍼 기반(BOLA\[3\])과 하이브리드(DYNAMIC\[4\]) 비트레이트 적응 알고리즘을 모두 제공한다. 그러므로 MPEG-DASH 클라이언트는 변화하는 네트워크 상황에 순응하고 멈춤이나 재버퍼링을 거의 일으키지 않으면서 고품질의 재생을 제공할 수 있게 된다.

MPEG-DASH는 국제 표준화된 최초의 적응 비트레이트 HTTP 기반 스트리밍 솔루션이다.\[5\] MPEG-DASH는 전송 프로토콜과 혼동해서는 안 되는데, MPEG-DASH가 사용하는 전송 프로토콜은 [TCP이다](../Page/전송_제어_프로토콜.md "wikilink"). MPEG-DASH는 필연적으로 모든 월드 와이드 웹 콘텐츠의 전송에 사용되는 기존 HTTP 웹 서버 하부 구조를 사용한다. 인터넷에 연결된 텔레비전, TV 셋톱박스, 데스크톱 컴퓨터, 스마트폰, 태블릿 등과 같은 장치들이 인터넷을 경유하여 전달되는 멀티미디어 콘텐츠(동영상, TV, 라디오 등)을 소비할 수 있게 해 주며 다양한 인터넷 수신 상황에 대처한다. 적응 스트리밍 솔루션의 표준화는 해당 솔루션이 범용적인 상황에 채택될 수 있음을 시장에 보증하는 것을 의미하며, 이는 마치 이와 유사하지만 사유 솔루션인 마이크로소프트의 [스무스 스트리밍이라든지](https://ko.wikipedia.org/wiki/스무스_스트리밍 "wikilink"), 어도비의 [HDS와](https://ko.wikipedia.org/wiki/HTTP_동적_스트리밍 "wikilink") 비견될 수 있다. HDS, 스무스 스트리밍과 달리 DASH는 [코덱](../Page/코덱.md "wikilink")에 의존적이지 않으므로 [H.265](../Page/고효율_비디오_코딩.md "wikilink"), [H.264](https://ko.wikipedia.org/wiki/H.264/MPEG-4_AVC "wikilink"), [VP9](https://ko.wikipedia.org/wiki/VP9 "wikilink") 등 어떠한 [코딩 포맷으로](https://ko.wikipedia.org/wiki/비디오_코딩_포맷 "wikilink") 인코딩된 콘텐츠라도 사용이 가능하다.\[6\]

## 표준화

MPEG-DASH 기술은 [MPEG](../Page/MPEG.md "wikilink")를 통해 개발되었다. DASH의 작업은 2010년 시작되었으며 2011년 1월 초안 국제 표준이 되었고 2011년 11월 국제 표준이 되었다.\[7\]\[8\] MPEG-DASH 표준은 2012년 4월 출판되었으나 2019년 [MPEG-DASH ISO/IEC 23009-1:2019](https://standards.iso.org/ittf/PubliclyAvailableStandards/c075485_ISO_IEC_23009-1_2019.zip)으로 개정되었다.

## 각주

## 외부 링크

  - [MPEG-DASH Standard](http://standards.iso.org/ittf/PubliclyAvailableStandards/c065274_ISO_IEC_23009-1_2014.zip)
  - [DASH subscription mailing list](http://lists.uni-klu.ac.at/mailman/listinfo/dash)
  - [DASH research at Alpen-Adria Universität Klagenfurt](http://dash.itec.aau.at/)
  - [Mailing list of the open-source DASH client library libdash](https://web.archive.org/web/20130624105147/http://vicky.bitmovin.net/mailman/listinfo/libdash-dev)

[분류:MPEG](https://ko.wikipedia.org/wiki/분류:MPEG "wikilink") [분류:HTTP](https://ko.wikipedia.org/wiki/분류:HTTP "wikilink") [분류:멀티미디어](https://ko.wikipedia.org/wiki/분류:멀티미디어 "wikilink") [분류:네트워크 프로토콜](https://ko.wikipedia.org/wiki/분류:네트워크_프로토콜 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.  [ISO/IEC DIS 23009-1.2 Dynamic adaptive streaming over HTTP (DASH)](http://www.iso.org/iso/iso_catalogue/catalogue_tc/catalogue_detail.htm?csnumber=57623)