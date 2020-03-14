> This article is converted from Wikipedia: [WebRTC](https://ko.wikipedia.org/wiki/WebRTC).


**WebRTC** (Web Real-Time Communication)는 [웹 브라우저](https://ko.wikipedia.org/wiki/웹_브라우저 "wikilink") 간에 [플러그인](https://ko.wikipedia.org/wiki/플러그인 "wikilink")의 도움 없이 서로 통신할 수 있도록 설계된 [API](https://ko.wikipedia.org/wiki/API "wikilink")이다. [W3C](https://ko.wikipedia.org/wiki/W3C "wikilink")에서 제시된 초안이며, 음성 통화, 영상 통화, P2P 파일 공유 등으로 활용될 수 있다.

## 역사

[웹 브라우저](https://ko.wikipedia.org/wiki/웹_브라우저 "wikilink") 기반의 통신 방식인 WebRTC는 [구글](https://ko.wikipedia.org/wiki/구글 "wikilink")이 [오픈 소스화한](https://ko.wikipedia.org/wiki/오픈_소스 "wikilink") 프로젝트에서 기원하였다.\[1\] 그 뒤로 [국제 인터넷 표준화 기구](https://ko.wikipedia.org/wiki/국제_인터넷_표준화_기구 "wikilink")\[2\]가 [프로토콜](https://ko.wikipedia.org/wiki/프로토콜 "wikilink") 표준화 작업을, [W3C](https://ko.wikipedia.org/wiki/W3C "wikilink")가 API 정의를 진행하였다.\[3\]

WebRTC의 W3C 초안\[4\] 작업은 진행 중이며 [크롬과](https://ko.wikipedia.org/wiki/구글_크롬 "wikilink") [파이어폭스](https://ko.wikipedia.org/wiki/파이어폭스 "wikilink") 브라우저에서 먼저 구현되고 있다. API는 [WHATWG](https://ko.wikipedia.org/wiki/WHATWG "wikilink")\[5\]과 [에릭슨](https://ko.wikipedia.org/wiki/에릭슨 "wikilink").\[6\]의 작업에 기반하여 정의되었다.

## 개요

### 설계

WebRTC의 주요 구성 요소는 여러 [자바스크립트](https://ko.wikipedia.org/wiki/자바스크립트 "wikilink") [API](https://ko.wikipedia.org/wiki/API "wikilink")를 포함하고 있다:

  - `getUserMedia`: 오디오와 비디오 미디어를 가져온다. (예: 장치의 카메라와 마이크로폰에 접근하여)\[7\]
  - `RTCPeerConnection`: 피어 간 오디오, 비디오 통신을 활성화한다. [신호 처리](https://ko.wikipedia.org/wiki/신호_처리 "wikilink"), [코덱](https://ko.wikipedia.org/wiki/코덱 "wikilink") 관리, P2P 통신, 보안, [대역폭](https://ko.wikipedia.org/wiki/대역폭 "wikilink") 관리를 수행한다.\[8\]
  - `RTCDataChannel`: 피어 간 양방향 임의 데이터 통신을 허용한다. [웹소켓](https://ko.wikipedia.org/wiki/웹소켓 "wikilink")과 동일한 API를 사용하며 매우 낮은 [레이턴시를](https://ko.wikipedia.org/wiki/네트워크_레이턴시 "wikilink") 보인다.\[9\]

또, WebRTC API는 통계 함수를 포함한다:

  - `getStats`: 웹 애플리케이션에 WebRTC 세션에 관한 통계 집합의 검색을 허용한다. 이 통계 데이터는 별도의 W3C 문서에 기술되어 있다.\[10\]

### 지원

WebRTC는 다음의 브라우저에서 지원된다:

  - 데스크톱 PC
      - [마이크로소프트 엣지](https://ko.wikipedia.org/wiki/마이크로소프트_엣지 "wikilink") 12+\[11\]
      - [구글 크롬](https://ko.wikipedia.org/wiki/구글_크롬 "wikilink") 28+
      - [모질라 파이어폭스](https://ko.wikipedia.org/wiki/모질라_파이어폭스 "wikilink") 22+\[12\]
      - [Safari](https://ko.wikipedia.org/wiki/사파리_\(웹_브라우저\) "wikilink") 11+\[13\]
      - [Opera](https://ko.wikipedia.org/wiki/오페라_\(웹_브라우저\) "wikilink") 18+\[14\]
      - [Vivaldi](https://ko.wikipedia.org/wiki/비발디_\(웹_브라우저\) "wikilink") 1.9+
  - [Android](https://ko.wikipedia.org/wiki/안드로이드_\(운영_체제\) "wikilink")
      - Google Chrome 28+ (버전 29부터 기본으로 활성화됨)
      - Mozilla Firefox 24+\[15\]
      - Opera Mobile 12+
  - [크롬 OS](https://ko.wikipedia.org/wiki/크롬_OS "wikilink")
  - [파이어폭스 OS](https://ko.wikipedia.org/wiki/파이어폭스_OS "wikilink")
  - [블랙베리 10](https://ko.wikipedia.org/wiki/블랙베리_10 "wikilink")
  - [IOS 11](https://ko.wikipedia.org/wiki/IOS_11 "wikilink")
      - MobileSafari/WebKit
  - [타이젠](https://ko.wikipedia.org/wiki/타이젠 "wikilink") 3.0

2013년 10월 마지막 기능 릴리스 이전의 [인터넷 익스플로러에서는](https://ko.wikipedia.org/wiki/인터넷_익스플로러 "wikilink") 지원되지 않으나,\[16\] 서드파티 플러그인을 사용하여 인터넷 익스플로러와 macOS용 사파리에서 WebRTC 지원을 추가할 수 있다.\[17\]\[18\] [WWDC](https://ko.wikipedia.org/wiki/애플_세계_개발자_회의 "wikilink") 2017에서, 애플은 사파리 11에서 WebRTC를 지원할 것이라고 발표했으며,\[19\] 사파리 테크놀로지 프리뷰 릴리스 32에서 사용 가능하게 되었다.\[20\]

## 참조

## 외부 링크

  -

  - [W3C Web Real-Time Communications Working Group](http://www.w3.org/2011/04/webrtc/)

  - [IETF Real-Time Communication in WEB-browsers (rtcweb) Working Group](http://tools.ietf.org/wg/rtcweb/)

[분류:웹 개발](https://ko.wikipedia.org/wiki/분류:웹_개발 "wikilink") [분류:BSD 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:BSD_라이선스_소프트웨어 "wikilink") [분류:P2P](https://ko.wikipedia.org/wiki/분류:P2P "wikilink")

1.
2.  <http://tools.ietf.org/wg/rtcweb/charters?item=charter-rtcweb-2011-05-03.txt>
3.
4.
5.
6.
7.
8.
9.
10.
11.
12. [Firefox Notes - Desktop](https://www.mozilla.org/en-US/firefox/22.0/releasenotes/). Mozilla.org (2013-06-25). Retrieved on 2014-04-11.
13.
14. [Opera News](http://blogs.opera.com/news/2013/11/opera-18/). blogs.opera.com (2013-11-19). Retrieved on 2015-09-17.
15. [Firefox Notes - Desktop](https://www.mozilla.org/en-US/mobile/24.0/releasenotes/). Mozilla.org (2013-09-17). Retrieved on 2014-08-04.
16.
17.
18.
19.
20.