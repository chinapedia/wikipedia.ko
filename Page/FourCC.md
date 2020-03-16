> This article is converted from Wikipedia: [FourCC](https://ko.wikipedia.org/wiki/FourCC).


**FourCC(Four Character Code)**는 말 그대로 "4글자 코드"라는 뜻이며, 4 [바이트](../Page/바이트.md "wikilink")로 된 문자열은 데이터 형식을 구분하는 고유 글자가 된다. 그리고 **FourCC** 개념은 [매킨토시](../Page/매킨토시.md "wikilink") 시스템 소프트웨어의 [OSType](https://ko.wikipedia.org/wiki/OSType "wikilink")에서 가져왔다. 이 개념은 나중에 [퀵타임](../Page/퀵타임.md "wikilink")과 [다이렉트쇼](../Page/다이렉트쇼.md "wikilink")의 데이터 형식을 구분하는데 사용되기도 한다.

영문 알파벳 네 글자로 데이터를 구분하므로 사람이 읽기 쉽고, 외우기도 쉽다. 4 [바이트](../Page/바이트.md "wikilink")로 구성되어, 아직까지는 32비트 시스템에 적합하다. 하지만 [엔디안](https://ko.wikipedia.org/wiki/엔디안 "wikilink") 문제 때문에 읽기가 힘든 경우도 있다. 예를 들면, **FourCC**가 'abcd'인 경우에 리틀 엔디안 시스템에서는 "0x64636261"로 표현한다.

**FourCC**는 주로 [AVI](../Page/오디오_비디오_인터리브.md "wikilink") 파일의 영상 코덱을 구분할 때 사용된다. [AVI](https://ko.wikipedia.org/wiki/AVI "wikilink") 확장자 파일에서 사용 가능한 코덱은 [Divx](https://ko.wikipedia.org/wiki/Divx "wikilink"), [Xvid](https://ko.wikipedia.org/wiki/Xvid "wikilink"), [H.264](https://ko.wikipedia.org/wiki/H.264 "wikilink")가 있다. 또, AVI나 [WAV](https://ko.wikipedia.org/wiki/웨이브 "wikilink") 파일의 음성 코덱 구분에는 2 바이트가 사용된다. 대개 16진수로 쓰인다. (예: [MP3](https://ko.wikipedia.org/wiki/MP3 "wikilink")는 0x0055) 물론, 영상 코덱이나 음성 코덱 이외의 파일 형식 구분에도 사용된다.

## 외부 링크

  - [FourCC.org](http://www.fourcc.org) - 영상 코덱과 화소에 대한 정보
  - [FourCC in VideoCodec](http://www.fourcc.org/codecs.php) - Video Codec에 사용되는 FourCC
  - [등록된 FOURCC 목록](https://web.archive.org/web/20080408170521/http://msdn2.microsoft.com/en-us/library/ms867195.aspx) - 2003년까지 등록된 것
  - [Standard for Interchange Format Files](https://web.archive.org/web/20080720173848/http://www.szonye.com/bradd/iff.html) - FourCC에 대한 소개

[분류:파일 포맷](https://ko.wikipedia.org/wiki/분류:파일_포맷 "wikilink") [분류:명수 4](https://ko.wikipedia.org/wiki/분류:명수_4 "wikilink")