> This article is converted from Wikipedia: [Rxvt](https://ko.wikipedia.org/wiki/Rxvt).


**rxvt**는 [X 윈도 시스템](../Page/X_윈도_시스템.md "wikilink")([윈도용의](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 경우 [시그윈](../Page/시그윈.md "wikilink") 포팅의 형태로 배포됨)용 [단말 에뮬레이터이다](../Page/단말_에뮬레이터.md "wikilink"). 롭 네이션(Rob Nation)이 처음 작성한 뒤, 나중에 마크(Mark Olesen)가 수년에 걸쳐 유지 보수를 통해 대폭 수정하였다. [xterm](https://ko.wikipedia.org/wiki/xterm "wikilink")에서 [테크트로닉스 4014](https://ko.wikipedia.org/wiki/테크트로닉스_4010 "wikilink") 에뮬레이션과 [툴킷](https://ko.wikipedia.org/wiki/X_툴킷_인트린식스 "wikilink") 스타일의 구성과 같은, 잘 쓰이지 않는 기능을 제거하여 가볍게 만들기 위해 고안되었다. 후자의 경우 바인딩 키와 같은 Xt 리소스 구조를 가리킨다. rxvt는 [켄트 대학교의](https://ko.wikipedia.org/wiki/켄트_대학교 "wikilink") 존 보비의 구 xvt 단말 에뮬레이터의 확장 버전이다. 이 이름은 원래 Robert's xvt를 대표하는 말이었으나 나중에 "our xvt"를 대표하는 말로 바뀌었다. (문자 r-x-v-t와 같은 발음)

리소스 파일의 제어를 받는 것들과 같은 기능들을 제쳐두고, rxvt의 단말 에뮬레이션은 두 가지 측면에서 [xterm](https://ko.wikipedia.org/wiki/xterm "wikilink")와 중요한 차이가 있다.

  - [VT220](https://ko.wikipedia.org/wiki/VT220 "wikilink")이 아닌 [VT102를](https://ko.wikipedia.org/wiki/VT100 "wikilink") 가상으로 구현한다. 이는 8비트 데이터를 다르게 관리하며 xterm이 처리할 수 있는 [C1](https://ko.wikipedia.org/wiki/C0_및_C1_제어_코드 "wikilink") 컨트롤이 추가되어 있지 않는다는 것을 뜻한다. xterm은 해당 기능을 비활성화하는 "-k8"\[1\] 스위치가 없다. rxvt는 VT220을 가상으로 구현하는 옵션을 제공하지 않는다.
  - 명령 키를 위해 보내는 문자열이 다르다. xterm은 [ANSI/ISO](https://ko.wikipedia.org/wiki/ANSI_이스케이프_코드 "wikilink") 이스케이프 시퀀스와 동일한 규칙을 이용하여 인코딩되는 문자열을 내보낸다. rxvt는 이와 맞먹는 호환성 유연성을 제공하지만 이를 직접 내보내지는 않는다.

새로운 버전의 rxvt는 [모조 투명성](https://ko.wikipedia.org/wiki/모조_투명성 "wikilink")(pseudo-transparency)을 순수하게 지원한다.

또, rxvt 배포판에는 rclock이라는 아날로그 시계 프로그램을 포함하고 있다. 매우 오래된 배포판에는 [vttest](https://ko.wikipedia.org/wiki/vttest "wikilink")의 사본을 포함하였으나 1996년 2.18 버전부터 이를 제공하지 않고 있다.

## 파생 프로그램

  - [aterm](https://ko.wikipedia.org/wiki/aterm "wikilink") (rxvt 2.4.8부터)
  - [Eterm](https://ko.wikipedia.org/wiki/인라이튼먼트 "wikilink") (rxvt 2.21부터)
  - [mrxvt](https://ko.wikipedia.org/wiki/mrxvt "wikilink") (rxvt 2.7.11부터)
  - [rxvt-unicode](https://ko.wikipedia.org/wiki/rxvt-unicode "wikilink") (rxvt 2.7.11부터)

## 같이 보기

  - [단말 에뮬레이터의 목록](https://ko.wikipedia.org/wiki/단말_에뮬레이터의_목록 "wikilink")

## 각주

<references />

## 외부 링크

  - [소스포지 닷넷](http://sourceforge.net/projects/rxvt/)

  - [프리코드](http://freecode.com/projects/rxvt/)

[분류:자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_소프트웨어 "wikilink") [분류:X 윈도 프로그램](https://ko.wikipedia.org/wiki/분류:X_윈도_프로그램 "wikilink") [분류:자유 터미널 에뮬레이터](https://ko.wikipedia.org/wiki/분류:자유_터미널_에뮬레이터 "wikilink")

1.