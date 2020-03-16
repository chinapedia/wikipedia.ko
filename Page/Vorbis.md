> This article is converted from Wikipedia: [Vorbis](https://ko.wikipedia.org/wiki/Vorbis).


**Vorbis**는 [Xiph.org](https://ko.wikipedia.org/wiki/Xiph.org "wikilink")에서 개발한 오디오 코덱이다. [오픈 소스며](../Page/오픈_소스.md "wikilink") 누구나 무료로 사용할 수 있는 [손실 압축](../Page/손실_압축.md "wikilink") 오디오 코덱이다. 확장자는 보통 .ogg를 사용하지만, [테오라](../Page/테오라.md "wikilink") 파일로 혼동하는 것을 막기 위해 .oga 확장자를 사용하기도 한다.

## 이름

'Vorbis'라는 이름은 [테리 프래쳇의](../Page/테리_프래쳇.md "wikilink") 소설, [디스크월드](https://ko.wikipedia.org/wiki/디스크월드 "wikilink")의 등장인물인 Exquisitor Vorbis의 이름에서 따왔다.\[1\]

## 요약

  - [VBR과](../Page/가변_비트레이트.md "wikilink") [ABR를](https://ko.wikipedia.org/wiki/평균_비트레이트 "wikilink") 지원한다.
  - [오픈 소스이므로](../Page/오픈_소스.md "wikilink") 별도의 사용료가 없다.
  - 확장성이 높다.

## 사양

  - 알고리즘 : MDCT ([수정 이산 코사인 변환](https://ko.wikipedia.org/wiki/수정_이산_코사인_변환 "wikilink"))
    샘플링 레이트 : 8kHz - 192kHz (일반적인 레이트)
    채널수: 1채널(모노), 2채널(스테레오), 4채널, 5.1채널, 6.1채널（최대 255 채널)
    비트레이트 : 평균 32kbps([aoTuV](https://ko.wikipedia.org/wiki/#aoTuV "wikilink") Q-2 mode), 평균 45kbps(Q-1) \~ 평균 500kbps(Q10) (44.1kHz 스테레오에서)
    채널 커플링 : 스테레오 모드에서만 작동
    비트레이트 제한 : 인코더에 의존
    MIME Type : application/ogg, application/x-ogg, application/x-vorbis
    스트리밍 : 가능 (플레이어에서 스트리밍을 가능하게 하면)
    체크 섬 : 가능 (기본적으로 켜짐)
    복제 방지 : 없음
    태그 정보 : Vorbis Comment (UTF-8) (일반적인 [ID3](../Page/ID3.md "wikilink") 태그는 사용할 수 없음)

## 역사

Vorbis는 [1998년](../Page/1998년.md "wikilink") 9월에 처음으로 연구가 진행되었다. 이때 [MP3](https://ko.wikipedia.org/wiki/MP3 "wikilink") 포맷은 라이선스가 등록되어 있어서 일정한 금액을 지불해야 했다. 이에 Vorbis 개발자는 완전 무료의 차세대 오디오 코덱을 개발하기로 결심한다. 약 2년 동안 다른 개발자와 함께 협업하여 [2001년](../Page/2001년.md "wikilink") [6월 15일](../Page/6월_15일.md "wikilink"), RC1 버전을 내놓는다. [2001년](../Page/2001년.md "wikilink") [8월 30일에는](../Page/8월_30일.md "wikilink") RC2 버전을 선보이는데, 이 버전은 최고 [비트레이트](../Page/비트레이트.md "wikilink")가 350kbps로 확장했다. 당시에 Vorbis는 MP3를 뛰어넘을 획기적인 압축 기술로 주목받았다. [2002년](../Page/2002년.md "wikilink") [7월 17일](../Page/7월_17일.md "wikilink") 공식판 1.0이 발표되었다. 공식판의 미비한 점을 보완하고자 개발자 aoTuV는 [2004년](../Page/2004년.md "wikilink")부터 공식판을 토대로 미비한 부분을 겹겹이 튜닝한 버전을 내놓는다.

## 특징

### 메타데이터

Ogg Vorbis에도 MP3의 ID3에 비견되는 메타데이터 표준이 있으며, 이를 [Vorbis 코멘트라고](../Page/보비스_코멘트.md "wikilink") 부른다. 메타데이터는 키 값과 커멘트 내용의 짝으로 저장이 되며, 키와 커멘트의 길이는 2<sup>32</sup>-1 바이트까지 가능하다. 이 정보는 Vorbis 비트 스트림의 처음 부분에 있는 시간 값이 담긴 헤더에 저장된다.

키 값은 대소문자 구분이 없는 7 bit ASCII 값으로 저장되며, 일부 문자는 허용되지 않는다. 커멘트 내용은 [UTF-8](../Page/UTF-8.md "wikilink")로 저장된다. 음악 태그는 일반적으로 "\[태그 키\]=\[커멘트 내용\]"과 같은 형식으로 저장된다.

`"ARTIST=Various Artist"`

ID3도 마찬가지로 태그를 입력하는 데 자유로운 편이다. 또한 Replaygain과 Discnumber 등의 2차적 태그를 지원한다.

### 장점

Vorbis는 모든 비트레이트를 자유롭게 지정할 수 있고 기존 코덱(MP3)의 한계를 넘을 수 있도록 설계되어 있다. Vorbis는 같은 비트레이트의 [MP3](https://ko.wikipedia.org/wiki/MP3 "wikilink")보다 음질이 좋고, [AAC와는](../Page/고급_오디오_부호화.md "wikilink") 음질이 비슷하거나 그 이상의 음질을 보장한다.단,CBR의 경우 MP3보다 안좋은 결과를 내놓기도 한다.

압축률의 지정은 일반적으로 퀄리티 레벨로 불리는 수치로 지정한다. 범위는 -1에서 10까지 있다. 44.1kHz Stereo (2ch)의 소스의 경우에 표준 퀄리티 레벨은 Q3(112kbps)가 된다. 최고 퀄리티 레벨은 Q10(500kbps), 최저 퀄리티 레벨은 Q-1(48kbps)가 된다. ([aoTuV](https://ko.wikipedia.org/wiki/#aoTuV "wikilink") 인코더에서는 최저 퀄리티 레벨인 Q-1의 하위인 Q-2를 지정할 수 있어 32kbps로 인코딩 할 수 있다).

이전에는 인코더 속도가 느리다는 지적이 있었지만, Blacksword에 의한 Ogg Vorbis 고속화 프로젝트에 의해 크게 개선되고 있다. 음질은 확장성의 높이를 살려 겹겹이 튜닝을 한 aoTuV가 긴 세월에 걸쳐 높은 평가를 거두고 있어 공식판의 최신 버전에 aoTuV 튜닝 기술이 들어갔다.

Vorbis는 프로그램에서는 샘플 단위로 위치를 지정해 정확하게 디코드할 수 있고, 별도의 소스 사용 금액이 없어서, PC 게임 등에서 많이 사용하고 있다.\[2\]

### 단점

  - Vorbis는 가변 비트레이트가 기본이므로 AVI 같은 VBR 음성 코덱을 따로 지원하지 않는 곳에 사용하면 문제가 생길 수 있다.
  - Vorbis는 MP3보다 더 많은 인코더 시간을 요구한다.
      - Ogg Vorbis 고속화 프로젝트로 인코더 시간을 줄일 수 있다.\[3\]
  - 재생할 수 있는 플레이어가 적다.
  - MP3에 비해 디코더 메모리가 많이 필요하다. 현대의 개인용 컴퓨터에서는 아무런 문제가 되지 않지만 MP3 플레이어 같은 휴대 매체에서는 전지를 빨리 소비하는 단점이 있다.
  - [대한민국](../Page/대한민국.md "wikilink") 대부분의 음원 제공 사이트는 MP3 형식의 음원만을 제공한다. Vorbis 형식의 음원은 구하기 힘들다.
  - MP3와 달리 앨범아트 기능을 지원하지 않는다
  - 무손실을 지원하지 않는다

## 종류

### 공식판

Xiph.Org 재단에서 개발하고 관리하고 있으며 [BSD](../Page/BSD.md "wikilink") 라이선스와 [GNU](../Page/GNU.md "wikilink") 라이선스를 따른다. 2007년 6월 22일 1.2.0 버전이 올라와있다.

### aoTuV

aoTuV는 공식판 버전을 새로 튜닝한 버전으로 공식판 버전에 비해 괜찮은 음질을 얻을 수 있다. 대체적으로 공식판 버전이 판올림될 때 같이 판올림되는 특징을 보인다. 현재 최신 버전은 [2009년](../Page/2009년.md "wikilink") [3월 3일에](../Page/3월_3일.md "wikilink") 나온 베타 5.7 버전이다. 고속화 프로젝트 팀은 aoTuV를 바탕으로 최적화된 고속화 버전으로 개량하는데, aoTuV로 인코딩하는 속도보다 고속화 버전으로 개량한 버전이 인코딩 속도가 더 빠르다.

## 지원

### 하드웨어

  - [코원시스템](../Page/코원시스템.md "wikilink") iAudio
  - [삼성](https://ko.wikipedia.org/wiki/삼성 "wikilink") 옙 MP3 플레이어
  - [아이리버](../Page/아이리버.md "wikilink")

[애플의](https://ko.wikipedia.org/wiki/애플_\(기업\) "wikilink") [아이팟](../Page/아이팟.md "wikilink")은 아직 정식으로 Vorbis를 지원하지 않지만, [락박스](../Page/락박스.md "wikilink")를 이용하여 Vorbis 파일을 재생할 수 있다. Xiph.org 재단 위키에서 vorbis를 지원하는 하드웨어 목록을 올리고 있다.\[4\]

### 소프트웨어

애플의 [아이튠즈](../Page/아이튠즈.md "wikilink")는 Vorbis를 지원하지 않지만, Xiph.org 재단에서 개발한 컴포넌트로 Vorbis를 재생할 수 있다. 컴포넌트는 [윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 버전과 [매킨토시](../Page/매킨토시.md "wikilink") 버전 둘 다 나와있다. [윈도 미디어 플레이어도](https://ko.wikipedia.org/wiki/윈도_미디어_플레이어 "wikilink") 애플처럼 Vorbis를 지원하지 않지만, 다이렉트 쇼 필터로 Vorbis를 재생할 수 있다. [리눅스](../Page/리눅스.md "wikilink")에서는 리눅스 기반 프로그램인 XMMS나 xine 등으로 Vorbis 재생을 지원한다. 더 많은 정보는 재단 홈페이지에 있다.\[5\] 윈도 버전에서는 [윈앰프](../Page/윈앰프.md "wikilink")와 [푸바2000](https://ko.wikipedia.org/wiki/푸바2000 "wikilink"), [제트오디오](../Page/제트오디오.md "wikilink"), [VLC 미디어 플레이어](../Page/VLC_미디어_플레이어.md "wikilink") 등이 vorbis 재생을 지원한다.

## 관련항목

  - [MP3](https://ko.wikipedia.org/wiki/MP3 "wikilink")
  - [Ogg](../Page/Ogg.md "wikilink")

## 각주

<references />

## 외부 링크

  - [Ogg Vorbis 공식 사이트](http://www.vorbis.com/)
  - [Xiph 재단 홈페이지](http://www.xiph.org/)
  - [aoTuV 개발자 홈페이지](https://web.archive.org/web/20100522210924/http://www.geocities.jp/aoyoume/aotuv/)
  - [Ogg Vorbis 고속화 프로젝트 사이트](https://web.archive.org/web/20051229033435/http://homepage3.nifty.com/blacksword/)

[분류:자유 멀티미디어 코덱](https://ko.wikipedia.org/wiki/분류:자유_멀티미디어_코덱 "wikilink") [분류:오디오 코덱](https://ko.wikipedia.org/wiki/분류:오디오_코덱 "wikilink") [분류:손실 압축 알고리즘](https://ko.wikipedia.org/wiki/분류:손실_압축_알고리즘 "wikilink") [분류:오디오 파일 포맷](https://ko.wikipedia.org/wiki/분류:오디오_파일_포맷 "wikilink") [분류:오픈 포맷](https://ko.wikipedia.org/wiki/분류:오픈_포맷 "wikilink") [분류:BSD 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:BSD_라이선스_소프트웨어 "wikilink")

1.
2.  [게임에 사용된 Ogg Vorbis](http://wiki.xiph.org/index.php/Games_that_use_Vorbis)
3.
4.  [Vorbis Hardware - XiphWiki](http://wiki.xiph.org/VorbisHardware)
5.  [Vorbis Software Players - XiphWiki](http://wiki.xiph.org/index.php/VorbisSoftwarePlayers)