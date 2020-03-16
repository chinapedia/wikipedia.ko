> This article is converted from Wikipedia: [XSPF](https://ko.wikipedia.org/wiki/XSPF).


**XML 셰어러블 플레이리스트 포맷**(, **XSPF**)는 [XML](../Page/XML.md "wikilink") 기반의 [디지털 미디어를](../Page/디지털_미디어.md "wikilink") 위한 [플레이리스트](../Page/플레이리스트.md "wikilink") 포맷이다. 흔히, 사람들은 XSPF를 **스피프**()라고 발음한다. [Xpih.Org 재단이](https://ko.wikipedia.org/wiki/Xpih.Org_재단 "wikilink") 후원하고 있다. 2004년 Yahoo.com/Webjay.org 출신의 루카스 건즈()가 이 포맷을 개발하였다.

XSPF는 개인용 PC나 휴대용 기기 사이에 [플레이리스트](../Page/플레이리스트.md "wikilink")를 공유하기 위해서 사용하는 포맷이다. 사람들이 어느 PC에서나 무슨 웹 페이지든 열어 볼 수 있는 것과 마찬가지로, 플레이리스트 사이의 포터빌리티를 제공하는 데 쓰이기 위해 XSPF가 개발되었다.

## 기능 및 특징

  - [M3U](../Page/M3U.md "wikilink") 혹은 [ASX](https://ko.wikipedia.org/wiki/ASX "wikilink")와 같은 플레이리스트 기능
  - `application/xspf+xml` [MIME](../Page/MIME.md "wikilink") 콘텐트 타입
  - 특허 문제에 있어서 자유로움 (Patent-free) (저작자가 특허를 걸어 놓지 않음.)
  - [크레이티브 코몬즈 애트리뷰션-노데리브스 2.5 라이선스](https://ko.wikipedia.org/wiki/크레이티브_코몬즈_라이선스 "wikilink")
  - XML, [애텀과](https://ko.wikipedia.org/wiki/atom "wikilink") 마찬가지.
  - [유니코드](../Page/유니코드.md "wikilink") 지원.
  - [크로스 플랫폼](https://ko.wikipedia.org/wiki/크로스_플랫폼 "wikilink") 지원.
  - 메타데이터 풍부성(metadata-rich).

## 역사

XSPF는 애드 혹 워킹 그룹에 의해 개발되었다. 2004년 2월에 출범한 애드 혹 워킹 그룹이었다. 2004년 4월 버전 0에 대하 대략적인 콘센서스에 이르렀다. 예제 구현을 해봤으며, 2004년 여름과 가을에 미세한 튜닝을 하였다. 2005년 1월 버전 1을 끝내 발표하였다.

XSPF는 아직 인터넷 표준은 아니다. 또한 Xiph.Org 재단 이외의 곳에서는 표준이나 권고안이 아니다.

## 스펙

자세한 문서는 [XSPF Version 1 specification](http://xspf.org/xspf-v1.html)를 참고하라.

## XSPF 1.0 플레이리스트의 예제

``` xml
<?xml version="1.0" encoding="UTF-8"?>
<playlist version="1" ns="http://xspf.org/ns/0/">
  <trackList>
    <track>
      <title>Internal Example</title>
      <location>file:///C:/music/foo.mp3</location>
    </track>
    <track>
      <title>External Example</title>
      <location>http://www.example.com/music/bar.ogg</location>
    </track>
  </trackList>
</playlist>
```

## 콘텐트 레졸루션

전통적으로 플레이리스트에는 각각의 음악 타이틀에 대한 파일 경로가 들어가 있었다. 이러한 플레이리스트는 한 컴퓨터에서는 잘 동작했으나, 다른 컴퓨터에 가져가서는 동작하지 않았다. XSPF는 콘텐트 레졸루션())이라는 개념을 가지고 플레이리스트 공유 기능을 구현하고 있다.

간단히 말해, 콘텐트 레졸루션이란 콘텐트 레졸루션이란 메타데이터에 기반한 지역적(local) 재생성이다. 콘텐트 리졸버()가 XSPF 플레이리스트를 열고 카탈로그 내에서 <creator>, <album>,

<title>

태그와 일치하는 멀티 미디어 타이틀을 찾는다. 찾아낸 타이틀을 가지고 플레이리스트를 새로 하나 만든다. 여기서 카탈로그란 로컬 디스트에 있는 모든 미디어 파일들의 콜렉션이 될 수도 있고, Yahoo\! 뮤직 언리미티드()나 다른 검색 가능한 아카이브의 음악 구독(subscription) 서비스가 될 수도 있다. 결과적으로 공유되는 플레이리스트는 특정 콜렉션이나 서비스에 종속되지 않게 된다.

## 소프트웨어

  - [아마록](https://ko.wikipedia.org/wiki/아마록 "wikilink")
  - [오데이셔스](https://ko.wikipedia.org/wiki/오데이셔스 "wikilink")
  - [헤리](https://ko.wikipedia.org/wiki/헤리 "wikilink") - XSPF 읽기/쓰기 가능. XSPF는 셧다운 시 자동 저장 플레이리스트 포맷으로도 쓰인다.
  - [서펀타인 (소프트웨어)](https://ko.wikipedia.org/wiki/서펀타인_\(소프트웨어\) "wikilink") - 오디오 CD 구이용 [그놈](../Page/그놈.md "wikilink") 애플리케이션.
  - [VLC 미디어 플레이어](../Page/VLC_미디어_플레이어.md "wikilink")
  - [Visonair.tv Stream Directory](https://web.archive.org/web/20080919091517/http://dir.visonair.tv/) (XSPF를 서버 리스트 다운로드에 쓴다.)
  - [libSpiff](http://libspiff.sourceforge.net/) (C++ XSPF 라이브러리)
  - [Visonair.tv Player](https://web.archive.org/web/20080810053957/http://www.visonair.tv/player.php) (XSPF 지원)
  - [Clipland Playlists](https://web.archive.org/web/20071212082531/http://www.clipland.com/PRO/playHome) (주문형 비디오 플레이리스트. XSPF.)
  - [PHP4XSPF](https://web.archive.org/web/20080915092903/http://php4xspf.berlios.de/) - PHP 클래스 모음. PHP를 가지고 XSPF 파일 생성 가능케 함.
  - [XSPF for Ruby](https://web.archive.org/web/20080708192636/http://xspf.rubyforge.org/) - 순수 루비(Ruby) 파서 및 제네레이터 라이브러리
  - [JointRadio](http://www.jointradio.com/) - MP3 파일들의 피드를 받아 XSPF 파일을 생성한다.
  - [XSPF Web Music Player](http://musicplayer.sourceforge.net/) - 오픈 소스 XSPF 플레이어 (웹 브라우저 내에서 플레이)

상기 언급된 소프트웨어 말고도 더 많은 소프트웨어가 XSPF를 지원한다. 외부 링크 절의 XSPF 홈페이지 고리에 들어가면 더 자세히 언급되어 있다.

## 외부 링크

  - [XSPF 홈페이지](http://xspf.org/)
  - [온라인 XSPF 발리데이터](http://validator.xspf.org/)
  - [XSPF discussion interface](https://web.archive.org/web/20080620135420/http://www.nabble.com/MusicBrainz---Playlist-f10925.html)
  - [MyPlayList](https://web.archive.org/web/20190321202902/http://myplaylist.biz/) First XSPF picture / music playlist compiler

[분류:플레이리스트 파일 포맷](https://ko.wikipedia.org/wiki/분류:플레이리스트_파일_포맷 "wikilink") [분류:XML 기반 표준](https://ko.wikipedia.org/wiki/분류:XML_기반_표준 "wikilink") [분류:오픈 포맷](https://ko.wikipedia.org/wiki/분류:오픈_포맷 "wikilink")