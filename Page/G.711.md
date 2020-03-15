> This article is converted from Wikipedia: [G.711](https://ko.wikipedia.org/wiki/G.711).


**G.711**은 [ITU-T](../Page/ITU-T.md "wikilink")의 오디오 [컴팬딩](https://ko.wikipedia.org/wiki/컴팬딩 "wikilink")을 위한 표준이다. 주로 전화에서 많이 쓰인다. 공식적인 명칭은 '음성 주파수의 펄스 부호 변조([PCM](https://ko.wikipedia.org/wiki/PCM "wikilink"))'이다. G.711은 또한 IP 네트워크 상의 [팩스](https://ko.wikipedia.org/wiki/팩스 "wikilink") 통신에도 사용된다. 펄스 부호 변조(PCM)으로도 알려져 있는 G.711은 파형 코덱으로 자주 사용된다. G.711은 64 kbit/s에서 시외 전화 정도의 품질을 제공하는 [협대역](https://ko.wikipedia.org/wiki/협대역 "wikilink") 오디오 코덱이다. G.711은 300-3400 Hz 범위의 오디오 신호를 통과시키며 초당 8000샘플링의 레이트로 샘플링한다.

G.711에는 두가지 강화 버전이 있는데 G.711.0과 G.711.1이다. G.711.0은 대역폭 사용을 줄이기 위해 [무손실](https://ko.wikipedia.org/wiki/무손실_압축 "wikilink") [데이터 압축을](https://ko.wikipedia.org/wiki/데이터_압축 "wikilink") 활용한다. G.711.1은 대역폭을 크게 하여 오디오 품질을 증가시킨다.

## 기능

  - 샘플링 주파수 8 kHz
  - 64 kbit/s 비트레이트(8kHz 샘플링 주파수 x 8 비트/샘플 수)
  - 형식적 알고리즘 지연 시간은 0.125 ms이며 look-ahead 지연은 없음.
  - G.711은 [파형](https://ko.wikipedia.org/wiki/파형 "wikilink") [음성 코더](https://ko.wikipedia.org/wiki/음성_부호화 "wikilink")
  - G.711 부록 I은 패킷화된 네트워크에서 전송 손실을 숨기는 것을 도와주는 [패킷 손실 은폐](https://ko.wikipedia.org/wiki/패킷_손실_은폐 "wikilink")(PLC) 알고리즘을 정의한다.
  - G.711 부록 II는 무음 상태일 때 대역폭 사용을 줄이기 위해 [음성 활동 감지](https://ko.wikipedia.org/wiki/음성_활동_감지 "wikilink")(VAD)와 [안정 소음 발생](https://ko.wikipedia.org/wiki/안정_소음_발생 "wikilink")(CNG)를 사용하는 [불연속 전송](https://ko.wikipedia.org/wiki/불연속_전송 "wikilink")(DTX) 알고리즘을 정의한다.
  - 이상적인 조건 하에서 테스트 했을 때 [PSQM](https://ko.wikipedia.org/wiki/PSQM "wikilink")은 G.711 μ-law가 4.45점, G.711 A-law가 4.45점의 [평균 오피니언 평점을](https://ko.wikipedia.org/wiki/평균_오피니언_평점 "wikilink") 도출해냈다.
  - 네트워크 부하 상태에서 테스트 했을 때 [PSQM](https://ko.wikipedia.org/wiki/PSQM "wikilink")은 G.711 μ-law가 4.13점, G.711 A-law가 4.11점의 [평균 오피니언 평점을](https://ko.wikipedia.org/wiki/평균_오피니언_평점 "wikilink") 도출해냈다.

## 라이선스

G.711이 1972년에 발표됐기 때문에 특허는 이미 사라진지 오래되었다. 그러므로 자유롭게 사용가능하다.\[1\]

## 각주

<references/>

## 외부 링크

  - \[<http://www.itu.int/rec/dologin_pub.asp?lang=e&id=T-REC-G.711-198811-I>\!\!PDF-E\&type=items ITU-T 권고 G.711\] - (STD.ITU-T RECMN G.711-ENGL 1989)
  - [ITU-T G.711 페이지](http://www.itu.int/rec/recommendation.asp?type=folders&lang=e&parent=T-REC-G.711)
  - [ITU-T G.711 C 코드를 위한 음성 및 오디오 부호화를 위한 G.191 소프트웨어 툴](http://www.itu.int/rec/T-REC-G.191/en)
  - [Code Project C\# implementation of G.711 with source code](https://web.archive.org/web/20060720180425/http://www.codeproject.com/csharp/g711audio.asp)
  - [RFC 3551 - RTP Profile for Audio and Video Conferences with Minimal Control](http://tools.ietf.org/html/rfc3551#page-28) - G.711 - PCMA와 PCMU 정의.
  - [RFC 4856 - 미디어 타입 audio/PCMA and audio/PCMU의 등록](http://tools.ietf.org/html/rfc4856#page-21)
  - RFC 5391 - ITU-T 권고 G.711.1를 위한 RTP Payload Format (PCMA-WB and PCMU-WB)

[분류:오디오 코덱](https://ko.wikipedia.org/wiki/분류:오디오_코덱 "wikilink") [분류:음성 코덱](https://ko.wikipedia.org/wiki/분류:음성_코덱 "wikilink") [분류:ITU-T 권고](https://ko.wikipedia.org/wiki/분류:ITU-T_권고 "wikilink")

1.