> This article is converted from Wikipedia: [ABC 기보법](https://ko.wikipedia.org/wiki/ABC_기보법).


**ABC 기보법**은 [기보법](../Page/기보법.md "wikilink")의 축약된 형태이다.

ABC 표기법(ABC notation,ABC 기보법)은 음악 표기법의 일종으로 중요해진 형식이다. 기본형에서는 A부터 G까지의 문자를 사용하여 주어진 음을 나타낸다. 다른 요소는 음영, 길이, 장식의 길이와 같이 다양한 옵션이 추가됐다. 이후에 컴퓨터가 주요 의사 소통 수단으로 등장하면서 사용자들은 온라인 음악 공유를 용이하게하고 소프트웨어 개발자를위한 새로운 언어를 추가하는 ASCII 코드로 이 형식의 표기법을 사용할 수있는 가능성을 보았다. 이 경우 ASCII 문자 세트를 미리 정의된 용도로 사용한다. ABC 표기법은 ASCII 기반이며 모든 텍스트 편집기를 사용하여 음악을 편집할 수 있다. 이러한 소프트웨어는 [Microsoft Windows](https://ko.wikipedia.org/wiki/Microsoft_Windows "wikilink") , [Unix](https://ko.wikipedia.org/wiki/Unix "wikilink") / [Linux](https://ko.wikipedia.org/wiki/Linux "wikilink") , [Macintosh](https://ko.wikipedia.org/wiki/Macintosh "wikilink") , [Palm OS](https://ko.wikipedia.org/wiki/Palm_OS "wikilink") 및 [웹](https://ko.wikipedia.org/wiki/웹 "wikilink") 기반을 포함하여 널리 사용 가능하게 되었다.\[1\]\[2\]

최신 [써드 파티](../Page/서드_파티_개발자.md "wikilink")(third-party) 소프트웨어 패키지는 TeX 타입 세터를 우회하여 직접 출력을 제공하고,\[3\] 다중 음성 및 다중 스태프 표기법,\[4\] 태블러쳐 ,\[5\]및 [MIDI](../Page/MIDI.md "wikilink")와 일치하는 가사 를 지원하는 구문을 확장했다.\[6\]

## 표준화

초기의 ABC 표기법은 [크리스 월쇼](https://ko.wikipedia.org/wiki/크리스_월쇼 "wikilink")(Chris Walshaw)가 설정한 ASCII 문자 세트이며 여러 사람들의 기여와 의견이 함께 반영되어 표준화되고 여러 요구사항을위해 변경되었다. 이러한 다양한 반영으로 다시 작성되었지만, 이후에도 여전히 초기의 ABC 표기형태와 호환 및 공유가 가능하며 편집이 간단하고 쉽게 접근할 수있는 형식을 유지하는 음악 표기법이 되었다. 원래 영어와 아일랜드어, 스코틀랜드와 같은 민속 음악 및 전통 음악과 함께 [태블러처](https://ko.wikipedia.org/wiki/태블러처 "wikilink") 및 [솔페지오](https://ko.wikipedia.org/wiki/솔페지오 "wikilink")로도 사용할수있도록 설계되었으며, 일반적으로 크리스 월쇼(Chris Walshaw)의 작업 이외에도 다른 사람들의 작업이 시작되어 현저히 발전하였다. 추가된 최신 문자 및 헤더 목록은 각 곡의 메타 데이터도 지원할 수 있게되었다.\[7\]

이러한 ABC표기법의 표준화는 단순히 음악을 작곡하는 방법의 제공뿐만아니라 이러한 작곡된 음악 데이터는 다른 환경에서 들려줄수있게 서로 공유가 가능하고 호환성을 유지해주는 광범위한 협업이 가능하다는 점에서 중요한 의미가 있다.

## 프로그램간 협업이 가능한 ABC표기법

최근 ABC표기법은 협업 환경에서 음악을 작곡하고 편집하며 보여주고 들려주는 방법으로까지 구현되어있다. ABC표기법을 사용할수있도록 협업화된 [Wiki](https://ko.wikipedia.org/wiki/미디어_위키 "wikilink") 환경은 다음과 같다.

\-협업 및 대규모 악보 편집을위한 ABC 기반 플랫폼-

  - [MediaWiki](https://ko.wikipedia.org/wiki/MediaWiki "wikilink") 용 악보 플러그인 : 이것은 기본 렌더링 엔진으로 [GNU LilyPond](../Page/릴리폰드.md "wikilink")(릴리폰드) 를 사용한다. 릴리폰드(LilyPond)에는 ABC 표기법을 릴리폰드로 변환하는 스크립트인 abc2ly가 함께 제공된다. 확장 프로그램은 abc2ly와 LilyPond를 호출한다.
  - [MusicWiki](https://ko.wikipedia.org/wiki/MusicWiki "wikilink") : [MoinMoin](https://ko.wikipedia.org/wiki/모인모인 "wikilink") 위키 용 [파이썬](../Page/파이썬.md "wikilink") [플러그인](../Page/플러그인.md "wikilink")
  - [PmWiki](https://ko.wikipedia.org/wiki/PmWiki "wikilink")에 ABC 표기법을 표시하기위한 AbcMusic
  - 몬트리올 세션 튠북(Montreal Session Tunebook) : AbcMusic 플러그인의 맞춤형 버전을 사용하여 전통 음악을위한 협업 소스
  - [그레고리오 프로젝트](https://ko.wikipedia.org/wiki/그레고리오_프로젝트 "wikilink") (Gregorio Project) 에서 그레고리오 성가(Gregorian chant) 악보를 기록하기 위해 개발한 gabc 표기법
  - [DokuWiki](../Page/도쿠위키.md "wikilink") 에서 ABC 표기법을 표시하기위한 ABC 플러그인. 이 플러그인은 제프 모인(Jef Moine)의 abcm2ps 패키지를 렌더링 엔진으로 사용한다. ABC Plus Project를 사용하여 MIDI 오디오 출력을 생성한다.
  - EasyABC는 MIDI 내보내기 및 SVG 렌더링을 지원하는 ABC 편집기이다.
  - 웹 페이지에 ABC 표기법을 표시하기위한 abc.js 플러그인: 서버에서 클라이언트 측을 지원한다.

<!-- end list -->

  - Zap's ABC는 abcm2ps, abc2midi 및 abc4j의 비트를 손에넣는 도구를 결합한 Android 앱
  - 멀티 플레이어 게임 [The Lord of the Rings Online은](../Page/반지의_제왕_온라인:_어둠의_제국_앙그마르.md "wikilink") 이제 ABC 표기법을 사용하여 플레이어가 게임 내 모든 MIDI 음악 파일을 변환하고 재생할 수있게한다. 플레이어는 캐릭터가 해당 악기를 연주하도록하여 음악을 재생한다.
  - PC 게임 [스타바운드](https://ko.wikipedia.org/wiki/스타바운드 "wikilink")(Starbound)를 통해 플레이어는 자신의 악기를 사용하여 사용자 지정 음악을 재생할 수 있다.
  - [musicXML](https://ko.wikipedia.org/wiki/musicXML "wikilink")에 특화되어 제작된 전용 [자바스크립트](../Page/자바스크립트.md "wikilink")파일은 [JQuery](../Page/JQuery.md "wikilink")와 함께 스탠드얼론상태인 [PC환경에서도](../Page/개인용_컴퓨터.md "wikilink") ABC표기법에 기반해서 웹 브라우저 상에서 편집과 재생이 가능토록한다.\[8\]

## 예(Lilypond)

**단순한 경우**

    <score>
    {c' d' e' f' f' fes' eis' e'}
    </score>

<score> {c' d' e' f' f' fes' eis' e'} </score>


**좀더 복잡한 경우**

``` latex
<score>
  \transpose c g \relative c' {
  \key c \minor
  \time 4/4
    c4 e8 e g4 g          % (text after the % is just a comment)
    <c es g>2 <c es g>    % angle brackets create chords
    es4 d( ces b)         % parentheses create slurs
    a4. r8 r8 a8 ~ a4     % r creates rests; ~ creates ties
    e-- e-> e-. g\fermata % accents and other signs
    \bar "|."
  }
</score>
```

<score>

` \transpose c g \relative c'{`
` \key c \minor`
` \time 4/4`
`   c4 e8 e g4 g          % (text after the % is just a comment)`
`   `<c es g>`2 `<c es g>`    % angle brackets create chords`
`   es4 d( ces b)         % parentheses create slurs`
`   a4. r8 r8 a8 ~ a4     % r creates rests; ~ creates ties`
`   e-- e-> e-. g\fermata % accents and other signs`
`   \bar "|."`
` }`

% This is just a comment line. </score>

## 같이 보기

  - [musicXML](https://ko.wikipedia.org/wiki/musicXML "wikilink")

## 각주

## 외부 링크

  - [ABC notation 참고 사이트](http://abcnotation.com/)

[분류:파일 포맷](https://ko.wikipedia.org/wiki/분류:파일_포맷 "wikilink") [분류:기보법](https://ko.wikipedia.org/wiki/분류:기보법 "wikilink")

1.
2.  ([W3C](../Page/W3C.md "wikilink") 공식웹사이트)https://www.w3.org/community/music-notation/
3.
4.
5.
6.
7.
8.  <https://wim.vree.org/js/xml2abc-js_index.html>