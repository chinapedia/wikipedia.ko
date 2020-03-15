> This article is converted from Wikipedia: [G.726](https://ko.wikipedia.org/wiki/G.726).


**G.726**은 16, 24, 32, 40 kbit/s의 속도의 음성 전송의 대역을 갖는 [ITU-T](../Page/ITU-T.md "wikilink") [ADPCM](https://ko.wikipedia.org/wiki/ADPCM "wikilink")이다.

## 기능

  - 샘플링 주파수 8 kHz
  - 16 kbit/s 24 kbit/s, 32 kbit/s, 40 kbit/s 비트레이트 사용 가능.
  - 비트레이트를 발생시키므로 패킷화로 프레임 길이를 결정한다.(보통 10 ms 프레임 크기에 80 샘플링 수)
  - 형식적 알고리즘 지연시간은 0.125 ms이다. look-ahead 지연 없음.
  - G.726은 [ADPCM](https://ko.wikipedia.org/wiki/ADPCM "wikilink")을 사용하는 파형 음성 코더이다.
  - 이상적인 조건에서의 PSQM 테스트에서 G.726 (32 kbit/s)의 평균 평가점(Mean Opinion Scores, MOS)이 4.30인데, 이는 G.711(뮤 법칙)의 4.45와 비교된다.
  - 네트워크 스트레트 조건에서의 PSQM 테스트에서 G.726 (32 kbit/s)의 평균 평가점은 3.79인데, 이는 G,711(뮤 법칙)의 4.13과 비교된다.
  - 40 kbit/초 G.726은 초당 12000비트 이하의 모뎀 신호를 전달할 수 있으나, 32 kbit/초 G.726는 초당 2400 비트 이하의 모뎀 신호와, 분명한 채널 코덱 기준에서 일부 단계적 역행을 통한 초당 4800비트의 신호를 전달할 수 있다.

## 외부 링크

  - [ITU-T G.726 페이지](http://www.itu.int/rec/recommendation.asp?type=folders&lang=e&parent=T-REC-G.726)
  - [ITU-T G.191 software tools for speech and audio coding, including G.726 C code](http://www.itu.int/rec/T-REC-G.191/en)
  - [RFC 3551 - RTP Profile for Audio and Video Conferences with Minimal Control, G726-40, G726-32, G726-24, and G726-16](http://tools.ietf.org/html/rfc3551#page-18)

[분류:음성 코덱](https://ko.wikipedia.org/wiki/분류:음성_코덱 "wikilink") [분류:오디오 코덱](https://ko.wikipedia.org/wiki/분류:오디오_코덱 "wikilink") [분류:ITU-T 권고](https://ko.wikipedia.org/wiki/분류:ITU-T_권고 "wikilink")