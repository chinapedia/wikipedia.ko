> This article is converted from Wikipedia: [Ogg](https://ko.wikipedia.org/wiki/Ogg).


**Ogg**(오그)는 [멀티미디어](../Page/멀티미디어.md "wikilink") [컨테이너 포맷이다](https://ko.wikipedia.org/wiki/컨테이너_포맷 "wikilink"). [특허권으로](https://ko.wikipedia.org/wiki/소프트웨어_특허권 "wikilink") 보호되지 않는 [오픈 표준](https://ko.wikipedia.org/wiki/오픈_표준 "wikilink") 파일 형식으로 [멀티미디어](../Page/멀티미디어.md "wikilink") [비트스트림을](https://ko.wikipedia.org/wiki/비트스트림_형식 "wikilink") 효율적으로 [전송하고](https://ko.wikipedia.org/wiki/스트리밍_미디어 "wikilink") 처리할 수 있게 하기 위해 [Xiph.Org 재단에서](../Page/Xiph.Org_재단.md "wikilink") 개발한 것이다. 보통 Ogg 스트림에는 Ogg [보비스](https://ko.wikipedia.org/wiki/보비스 "wikilink") [소리 파일 형식을](https://ko.wikipedia.org/wiki/소리_파일_형식 "wikilink") 사용한 [오디오가](../Page/소리.md "wikilink") 많이 담기긴 하지만, 이외에도 Ogg [테오라](../Page/테오라.md "wikilink")와 같은 다른 형식도 들어 갈 수 있다.

Ogg 형식 파일에는 오디오와 [비디오](../Page/비디오.md "wikilink"), 문자열 (예: 자막) 용의 몇 가지의 서로 다른 오픈 소스 [코덱](../Page/코덱.md "wikilink")으로 저장된 정보를 담을 수 있다. .ogg라는 확장자의 파일은 앞서 언급한 몇 가지의 Ogg 미디어 파일 형식들 중 하나에 해당할 수 있다. 또한 무료로 사용할 수 있는 파일 형식이기 때문에, 여러 무료 및 상용 [미디어 플레이어는](../Page/미디어_플레이어.md "wikilink") 물론 다양한 [포터블 미디어 플레이어에](../Page/포터블_미디어_플레이어.md "wikilink") Ogg의 여러 코덱을 내장해 사용될 수 있다.

현재 Ogg를 기본적으로 사용하는 프로젝트로는 [보비스](https://ko.wikipedia.org/wiki/보비스 "wikilink"), 스픽스, 테오라등이 있고, FLAC 프로젝트도 디랙 프로젝트의 하부 프로젝트인 슈뢰딩거 프로젝트도 Ogg 포맷의 사용을 지원한다.

2007년 이후부터 Xiph.org 재단은 .ogg 확장자를 Ogg 보비스 오디오 파일에만 사용할 것을 권고하고 있다. 그리고 Xiph 재단은 .oga, .ogv, .ogx와 같은 새로운 파일 확장자를 만들기로 하였다. .oga는 오디오만 담고 있는 파일, .ogv는 소리를 포함하지 않는 비디오, .ogx는 멀티플렉싱 기술이 적용된 Ogg에 사용된다.\[1\]

## 오그 코덱

Ogg는 [컨테이너 파일에](https://ko.wikipedia.org/wiki/컨테이너_파일 "wikilink") 불과하다. 코덱으로 인코딩된 실제 오디오 데이터 또는 비디오 데이터는 Ogg 컨테이너 안에 저장되어 있다.

오그는 컨테이너 포맷이므로 다양한 포맷으로 오디오와 비디오를 담을 수 있다. 그러나 오그는 의도적으로 또는 보통 다음과 같은 [Xiph.org](https://ko.wikipedia.org/wiki/Xiph.org "wikilink") 무료 코덱을 이용한다.

  - [오디오 코덱](../Page/오디오_코덱.md "wikilink")
      - [손실 압축](../Page/손실_압축.md "wikilink") 방식
          - [Speex](https://ko.wikipedia.org/wiki/Speex "wikilink"): 녹음에 최적화된 코덱이다. (\~8-32 kbit/s/channel)
          - [Vorbis](../Page/Vorbis.md "wikilink"): 기본으로 VBR (Variable Bitrates) 방식을 취하는 일반적인 오디오 코덱이다. (채널 당 16-500kb까지 가능)
      - [무손실 압축](https://ko.wikipedia.org/wiki/무손실_압축 "wikilink") 방식
          - [FLAC](../Page/FLAC.md "wikilink"): 무손실 압축 코덱이며 압축률을 조정할 수 있다.

<!-- end list -->

  - [영상 코덱](../Page/영상_코덱.md "wikilink")
      - [손실 압축](../Page/손실_압축.md "wikilink") 방식
          - [Theora](https://ko.wikipedia.org/wiki/Theora "wikilink"): [On2](https://ko.wikipedia.org/wiki/On2 "wikilink")의 [VP3](https://ko.wikipedia.org/wiki/VP3 "wikilink")가 바탕이며 [MPEG-4](../Page/MPEG-4.md "wikilink") 비디오, [리얼 비디오](https://ko.wikipedia.org/wiki/리얼_비디오 "wikilink"), [윈도 미디어 비디오를](https://ko.wikipedia.org/wiki/윈도_미디어_비디오 "wikilink") 겨냥해서 나왔다.
          - 탈킨(Tarkin):2000년, 2001년, 2002년에 실험적으로 개발된 영상 코덱
      - [무손실 압축](https://ko.wikipedia.org/wiki/무손실_압축 "wikilink") 방식
          - [디랙](https://ko.wikipedia.org/wiki/디랙_\(코덱\) "wikilink")(Dirac)
      - 비압축 방식
          - [OggUVS](https://ko.wikipedia.org/wiki/OggUVS "wikilink")

## 각주

<references/>

## 외부 링크

  - [Xiph.Org 재단 공식 웹페이지 — Ogg](http://www.xiph.org/ogg/)
  - [RFC 3533 — Ogg 요약 포맷 버전 0](https://web.archive.org/web/20041010002923/http://www.ietf.org/rfc/rfc3533.txt)
  - [RFC 5334 — Ogg 미디어 타입](http://tools.ietf.org/html/rfc5334)
  - [RFC 3534 — application/ogg 미디어 타입](https://web.archive.org/web/20041010004613/http://www.ietf.org/rfc/rfc3534.txt) - obsoleted by RFC 5334
  - [Ogg 컨테이너에 크레이티브 커먼즈 메타데이터 사용](http://wiki.creativecommons.org/OGG)
  - [Xiph.Org's official Ogg QuickTime Components for iTunes and iMovie (윈도, OS X)](http://xiph.org/quicktime/)
  - [Vorbis, Speex, Theora, FLAC용 윈도 미디어 플레이어 코덱](http://www.xiph.org/dshow/)
  - [Ogg 파일 변환 온라인 툴, 다운로드 필요없음.](https://web.archive.org/web/20130101114454/http://www.oggconvert.com/)
  - [마이크로 비디오 컨버터](http://www.mirovideoconverter.com/)

[분류:자유 멀티미디어 코덱](https://ko.wikipedia.org/wiki/분류:자유_멀티미디어_코덱 "wikilink") [분류:자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_소프트웨어 "wikilink") [분류:오디오 파일 포맷](https://ko.wikipedia.org/wiki/분류:오디오_파일_포맷 "wikilink") [분류:오픈 포맷](https://ko.wikipedia.org/wiki/분류:오픈_포맷 "wikilink")

1.  [종류와 확장자".](http://wiki.xiph.org/index.php/MIME_Types_and_File_Extensions%22MIME) XiphWiki. 2007년 09월 07일. 2007년 09월 10일에 확인.