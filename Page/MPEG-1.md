> This article is converted from Wikipedia: [MPEG-1](https://ko.wikipedia.org/wiki/MPEG-1).


**MPEG-1**(Moving Picture Experts Group Phase 1, 엠펙 원)은 [ISO/IEC JTC 1의](https://ko.wikipedia.org/wiki/ISO/IEC_JTC_1 "wikilink") [MPEG](https://ko.wikipedia.org/wiki/MPEG "wikilink") 그룹이 만든 표준 동영상 및 멀티미디어 규격 가운데 하나이다.

오디오/비디오 규격으로 세계적으로 가장 널리 쓰이는 형식 중 하나이며, [비디오 CD](https://ko.wikipedia.org/wiki/비디오_CD "wikilink"), [케이블](https://ko.wikipedia.org/wiki/케이블_텔레비전 "wikilink")/[위성](https://ko.wikipedia.org/wiki/위성_텔레비전 "wikilink") TV, [DAB](https://ko.wikipedia.org/wiki/디지털_오디오_방송 "wikilink") 등에서 이용되고 있다. 단지 MPEG 동영상이라고 하면, MPEG-1으로 압축된 것을 가리키는 경우가 많다. MPEG-1 규격 중 가장 알려진 것은 MP3 오디오 형식일 것이다.

[비디오](https://ko.wikipedia.org/wiki/비디오 "wikilink")와 [오디오](https://ko.wikipedia.org/wiki/소리 "wikilink") 두 가지를 합친 시스템에 대해 규격화되고 있다. 오디오의 규격에는 레이어 1, 레이어 2, 레이어 3이 있고, 각각 MP1, MP2, MP3 로 불리고 있다. 레이어 2와 호환되는 기기는 레이어 1도 재생할 수 있다. 이와 같이 레이어 3도 하위 1, 2 또한 모두 재생할 수 있다. 다시 말해, [상위 호환성을](https://ko.wikipedia.org/wiki/상위_호환성 "wikilink") 가진다. 비디오 CD의 경우, 레이어 2를 사용한다.

MPEG-1 표준은 ISO/IEC-11172로 등재되어 있다.

## 특허

MPEG-1 비디오와 레이어 I/II 오디오는 라이선스 비용을 지불하지 않고 사용될 수 있다.\[1\]\[2\]\[3\]\[4\]\[5\] ISO 특허 데이터베이스는 2003년에 만료된 ISO 11172, US 4,472,747 특허를 담고 있다.\[6\] MPEG-1 표준의 거의 완성된 초안은 1991년 2012년 12월 6일 즈음부터 ISO CD 11172로서 공개적으로 사용할 수 있었다. 시간적인 이유로 기술 특허권 대부분은 만료되었다.\[7\]

## 파트 1:시스템

MPEG-1 표준의 파트 1은 시스템에 대해서 다루며, **ISO/IEC-11172-1**에 정의되어 있다.

MPEG-1 시스템은 오디오, 비디오, 다른 다양한 데이터를 표준 비트스트림으로 인코딩하여 저장하고, 다양한 컨텐츠 사이의 동기화 상태를 유지하기 위하여 사용하는 논리적 레이아웃과 방법을 규정한다. 이 [파일 포맷은](https://ko.wikipedia.org/wiki/파일_형식 "wikilink") 미디어의 저장, [데이터 채널을](https://ko.wikipedia.org/wiki/데이터_채널 "wikilink") 통한 전송에 맞춰 설계되었다. 소수의 오류 보호만이 표준에 규정되어있고, 비트스트림의 작은 오류들은 상당한 결점을 유발할 수도 있다.

이 구조는 나중에 [MPEG 프로그램 스트림이라는](https://ko.wikipedia.org/wiki/MPEG_프로그램_스트림 "wikilink") 이름을 갖게 된다.(MPEG-1 시스템 디자인은 본질적으로 MPEG-2 프로그램 스트림과 동일하다.) 이 용어는 더 유명하고 정확하며([MPEG 트랜스포트 스트림과는](https://ko.wikipedia.org/wiki/MPEG_트랜스포트_스트림 "wikilink") 구별된다.) 여기에 쓰인다.

**기초 스트림**(**ES**)은 MPEG-1 오디오와 영상의 인코딩된) 데이터의 원본 비트스트림이다. 이 파일은 MP3 파일처럼 그 자체로 배포할 수 있다.

**패킷화 기초 스트림**(**PES**)은 가변 길이의 패킷으로 패킷화된 기초 스트림이다. 이것은 기초 스트림을 [순환 중복성 검사](https://ko.wikipedia.org/wiki/순환_중복성_검사 "wikilink")(CRC) [체크섬](https://ko.wikipedia.org/wiki/체크섬 "wikilink")이 오류 감지를 위해 각각의 패킷에 추가된 독립적인 덩어리로 나눈 것이다.

**시스템 클럭 참조값**(SCR)는 27MHz의 정확도로 추가적인 시간 데이터를 저장하는 9비트 확장과, 90kHz의 주파수/정확도로 각각의 패킷의 33비트 헤더 속에 저장된 시간 값이다. 이것들은 인코더가 삽입하며, 시스템 시간 클럭(STC)에서 얻어진다. 그러나 버퍼링, 인코딩,지터, 다른 지연 시간 때문에 동시에 인코딩된 오디오와 비디오 스트림은 동일한 SCR 값을 갖지 않는다.

## 파트 2: 영상

MPEG-1 표준의 파트 2는 영상에 대해서 다루며, **ISO/IEC-11172-2**에 정의되어 있다.

  - 색 공간
  - 해상도/비트레이트: 최대 4095×4095 (12비트), 비트레이트 최대 100 Mbit/초\[8\]

## 파트 3: 오디오

MPEG-1 표준의 파트 3는 오디오에 대해서 다루며, **ISO/IEC-11172-3**에 정의되어 있다.

  - 레이어 1
  - 레이어 2
  - 레이어 3

## 파트 4: 적합성 평가

MPEG-1 표준의 파트 4는 적합성 평가(Conformance test)에 대해서 다루며, **ISO/IEC-11172-4**에 정의되어 있다.

적합성: 적합성을 평가하기 위한 과정

인코더가 생성한 비트스트림과 마찬가지로 MPEG-1 오디오, 비디오 디코더의 적합성을 평가하기 위한 두 가지의 가이드라인과 참조 비트스트림을 제공한다.

## 파트 5: 참조 소프트웨어

MPEG-1 표준의 파트 5는 참조 소프트웨어에 대해서 다루며, **ISO/IEC-11172-5**에 정의되어 있다.

시뮬레이션: 참조 소프트웨어

다중화와 역다중화와 마찬가지로, 오디오와 비디오의 인코딩과 디코딩을 위한 [C](https://ko.wikipedia.org/wiki/C_\(프로그래밍_언어\) "wikilink") 참조 구현을 제공한다.

## 파일 확장자

.mpg는 MPEG-1과 MPEG-2 오디오, 비디오 압축을 위한 여러 가지 확장자 중 하나이다. MPEG-1 파트 2 비디오는 요즘에는 보기 힘들며, 이 확장자는 보통 [MPEG 프로그램 스트림](https://ko.wikipedia.org/wiki/MPEG_프로그램_스트림 "wikilink")(MPEG-1과 MPEG-2에서 정의하는) 또는 [MPEG 트랜스포트 스트림](https://ko.wikipedia.org/wiki/MPEG_트랜스포트_스트림 "wikilink")(MPEG-2에서 정의)을 가리킨다. .m2ts 같은 다른 확장자 또한 존재한다.

## 같이 보기

  - [MPEG](https://ko.wikipedia.org/wiki/MPEG "wikilink")
  - [MP3](https://ko.wikipedia.org/wiki/MP3 "wikilink")
  - [MPEG-2](https://ko.wikipedia.org/wiki/MPEG-2 "wikilink")
  - [JPEG](https://ko.wikipedia.org/wiki/JPEG "wikilink")
  - [JBIG](https://ko.wikipedia.org/wiki/JBIG "wikilink")
  - [AAC](https://ko.wikipedia.org/wiki/고급_오디오_부호화 "wikilink")

## 각주

<references />

## 외부 링크

  - [MPEG-1에 들어가는 소스 코드](http://standards.iso.org/ittf/PubliclyAvailableStandards/c025029_ISO_IEC_TR_11172-5_1998\(E\)_Software_Simulation.zip)

[1](https://ko.wikipedia.org/wiki/분류:MPEG "wikilink") [분류:영상 코덱](https://ko.wikipedia.org/wiki/분류:영상_코덱 "wikilink") [분류:오디오 코덱](https://ko.wikipedia.org/wiki/분류:오디오_코덱 "wikilink") [분류:ISO/IEC 표준](https://ko.wikipedia.org/wiki/분류:ISO/IEC_표준 "wikilink")

1.
2.
3.
4.  [\[homework](http://lists.w3.org/Archives/Public/public-html/2007Nov/0153.html) summary of the video (and audio) codec discussion from Dave Singer on 2007-11-09 (public-html@w3.org from November 2007)\]
5.  [MPEG-1 Video Coding (H.261)](http://www.digitalpreservation.gov/formats/fdd/fdd000035.shtml)
6.  [ISO Patent Database](http://www.iso.org/patents)[ISO JTC1 Patent Database](http://isotc.iso.org/livelink/livelink/3777806/JTC1_Patents_database.html?func=doc.Fetch&nodeid=3777806) Search for 11172 in page
7.  [Performance of a Software MPEG Video Decoder](http://bmrc.berkeley.edu/research/mpeg/software/Old/Mpeg93.ps.gz)
8.