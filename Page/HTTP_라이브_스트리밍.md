> This article is converted from Wikipedia: [HTTP 라이브 스트리밍](https://ko.wikipedia.org/wiki/HTTP_라이브_스트리밍).


**HTTP 라이브 스트리밍**(HTTP Live Streaming, **HLS**)은 [애플](../Page/애플.md "wikilink")이 개발하여 2009년 출시한 [HTTP](../Page/HTTP.md "wikilink") 기반 [적응 비트레이트 스트리밍](https://ko.wikipedia.org/wiki/적응_비트레이트_스트리밍 "wikilink") 통신 프로토콜이다. 이 프로토콜은 여러 미디어 플레이어, 웹 브라우저, 모바일 기기, 스트리밍 미디어 서버에서 지원되고 있다. 연간 비디오 산업 조사에 따르면 가장 대중적인 스트리밍 포맷으로 간주된다.\[1\]

HLS는 전반적인 스트림을 크기가 작은 일련의 HTTP 기반 파일 다운로드로 분리시켜 개개의 다운로드를 통해 잠재적으로 무한한 전송 스트림의 작은 덩어리를 적재시킴으로써 동작한다는 면에서 [MPEG-DASH와](../Page/HTTP_동적_적응_스트리밍.md "wikilink") 유사하다. 각기 다른 비트레이트로 인코딩되는, 이용 가능한 스트림 목록은 [확장 M3U 플레이리스트를](../Page/M3U.md "wikilink") 사용하여 클라이언트에 전송된다.\[2\]

표준 HTTP 트랜잭션에 기반한 HTTP 라이브 스트리밍은 [RTP](../Page/실시간_전송_프로토콜.md "wikilink") 등 UDP 기반 프로토콜과 달리 표준 HTTP 트래픽을 통해 [방화벽이나](../Page/방화벽_\(네트워킹\).md "wikilink") [프록시 서버를](../Page/프록시_서버.md "wikilink") 경유할 수 있다. 또, 널리 이용되는 HTTP 기반 [콘텐츠 전송 네트워크를](../Page/콘텐츠_전송_네트워크.md "wikilink") 통해 콘텐츠를 전통적인 HTTP 서버로부터 제공받을 수 있다.\[3\] 이 표준은 또한 표준 암호화 매커니즘\[4\]과 [HTTPS](../Page/HTTPS.md "wikilink")를 이용한 보안 키 배포를 사용하며 이 둘은 단순한 [DRM](../Page/디지털_권리_관리.md "wikilink") 시스템을 제공하게 된다. 이 프로토콜의 후반 버전은 [트릭 모드](https://ko.wikipedia.org/wiki/트릭_모드 "wikilink") 빨리감기와 되감기, 자막 연동을 제공한다.

애플은 HTTP 라이브 스트리밍을 [인터넷 초안](https://ko.wikipedia.org/wiki/인터넷_초안 "wikilink")(개별 제출)으로 문서화하였으며 이는 [RFC](../Page/RFC.md "wikilink")로서의 출판 과정의 첫 단계이다. 2015년 12월 기준으로 해당 문서의 저자들은 [IETF](../Page/국제_인터넷_표준화_기구.md "wikilink") 총의 과정이 아닌 외부에서 문서를 정보성(비표준) RFC로 출판하기 위해 RFC ISE(Independent Stream Editor)를 요청하였다.\[5\] 2017년 8월, RFC8216는 프로토콜 버전 7을 기술하기 위해 출판되었다.\[6\]

## 같이 보기

  - [HTTP 동적 적응 스트리밍](../Page/HTTP_동적_적응_스트리밍.md "wikilink")

## 각주

[분류:HTTP](https://ko.wikipedia.org/wiki/분류:HTTP "wikilink") [분류:멀티미디어](https://ko.wikipedia.org/wiki/분류:멀티미디어 "wikilink") [분류:네트워크 프로토콜](https://ko.wikipedia.org/wiki/분류:네트워크_프로토콜 "wikilink")

1.
2.
3.
4.
5.
6.