> This article is converted from Wikipedia: [SFML](https://ko.wikipedia.org/wiki/SFML).


**SFML**(Simple and Fast Multimedia Library)은 컴퓨터의 다양한 멀티미디어 구성 요소에 단순한 [API](https://ko.wikipedia.org/wiki/API "wikilink")를 제공하기 위해 설계된 [크로스 플랫폼](https://ko.wikipedia.org/wiki/크로스_플랫폼 "wikilink") 소프트웨어 개발 [라이브러리이다](https://ko.wikipedia.org/wiki/라이브러리_\(컴퓨팅\) "wikilink"). [C](https://ko.wikipedia.org/wiki/C_\(프로그래밍_언어\) "wikilink"), [크리스탈](https://ko.wikipedia.org/wiki/크리스탈_\(프로그래밍_언어\) "wikilink"), [D](https://ko.wikipedia.org/wiki/D_\(프로그래밍_언어\) "wikilink"), [유포리아](https://ko.wikipedia.org/wiki/유포리아 "wikilink"), [Go](https://ko.wikipedia.org/wiki/Go_\(프로그래밍_언어\) "wikilink"), [Java](https://ko.wikipedia.org/wiki/자바_\(프로그래밍_언어\) "wikilink"), [Julia](../Page/줄리아_\(프로그래밍_언어\).md "wikilink"), [.NET](https://ko.wikipedia.org/wiki/닷넷_프레임워크 "wikilink"), [Nim](https://ko.wikipedia.org/wiki/:en:Nim_\(programming_language\) "wikilink"), [OCaml](https://ko.wikipedia.org/wiki/OCaml "wikilink"), [Python](https://ko.wikipedia.org/wiki/파이썬 "wikilink"), [Ruby](https://ko.wikipedia.org/wiki/루비_\(프로그래밍_언어\) "wikilink"), and [Rust용으로](../Page/러스트_\(프로그래밍_언어\).md "wikilink") 이용 가능한 [바인딩과](https://ko.wikipedia.org/wiki/언어_바인딩 "wikilink") 함께 [C++](https://ko.wikipedia.org/wiki/C++ "wikilink")로 작성되어 있다.\[1\] 실험적인 모바일 포트들은 SFML 2.2의 출시와 함께 [안드로이드](https://ko.wikipedia.org/wiki/안드로이드_\(운영_체제\) "wikilink"), [iOS](https://ko.wikipedia.org/wiki/iOS "wikilink")용으로 이용 가능하게 되었다.\[2\]

SFML은 [창에](https://ko.wikipedia.org/wiki/창_\(컴퓨팅\) "wikilink") 대한 만들기 및 입력, 그리고 [OpenGL](https://ko.wikipedia.org/wiki/OpenGL "wikilink") 컨텍스트의 만들기 및 관리를 관리한다. [프리타입](https://ko.wikipedia.org/wiki/프리타입 "wikilink")을 이용한 텍스트 렌더링, [OpenAL](https://ko.wikipedia.org/wiki/OpenAL "wikilink")을 사용하는 오디오 모듈, 기본적인 [전송 제어 프로토콜](https://ko.wikipedia.org/wiki/전송_제어_프로토콜 "wikilink")(TCP)과 [사용자 데이터그램 프로토콜](https://ko.wikipedia.org/wiki/사용자_데이터그램_프로토콜 "wikilink")(UDP) 통신을 위한 네트워크 모듈을 포함하여 [2차원 컴퓨터 그래픽스의](https://ko.wikipedia.org/wiki/2차원_컴퓨터_그래픽스 "wikilink") 단순한 [하드웨어 가속을](https://ko.wikipedia.org/wiki/하드웨어_가속 "wikilink") 위한 그래픽 모듈도 제공한다.

SFML은 [zlib/png 라이선스](../Page/Zlib_라이선스.md "wikilink") 조항으로 제공되는 [자유-오픈 소스 소프트웨어이다](https://ko.wikipedia.org/wiki/자유-오픈_소스_소프트웨어 "wikilink"). [윈도우](https://ko.wikipedia.org/wiki/마이크로소프트_윈도우 "wikilink"), [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink"), [macOS](https://ko.wikipedia.org/wiki/macOS "wikilink"), [FreeBSD](https://ko.wikipedia.org/wiki/FreeBSD "wikilink")에서 이용할 수 있다.\[3\]\[4\]</ref> 최초 버전 1.0은 2007년 8월 9일 출시되었으며 최신 버전 v2.5.0은 2018년 5월 9일 출시되었다.

## 소프트웨어 구조

### 모듈

SFML은 다양한 모듈로 구성되어 있다:

  - 시스템 – [벡터](https://ko.wikipedia.org/wiki/벡터_\(물리\) "wikilink"), [유니코드](https://ko.wikipedia.org/wiki/유니코드 "wikilink") [문자열](https://ko.wikipedia.org/wiki/문자열 "wikilink") 클래스, 포터블 [스레드](https://ko.wikipedia.org/wiki/스레드 "wikilink") 및 타이머 기능
  - 창 – [창](https://ko.wikipedia.org/wiki/창_\(컴퓨팅\) "wikilink") 및 [입력 장치](https://ko.wikipedia.org/wiki/컴퓨터_입력_장치 "wikilink") 관리 ([조이스틱](https://ko.wikipedia.org/wiki/조이스틱 "wikilink"), [OpenGL](https://ko.wikipedia.org/wiki/OpenGL "wikilink") 컨텍스트 관리 지원 포함)
  - 그래픽스 – [스프라이트](https://ko.wikipedia.org/wiki/스프라이트_\(컴퓨터_그래픽스\) "wikilink"), [다각형](https://ko.wikipedia.org/wiki/다각형 "wikilink"), 텍스트 렌더링을 포함한 2차원 그래픽스의 [하드웨어 가속](https://ko.wikipedia.org/wiki/하드웨어_가속 "wikilink")
  - 오디오 – 하드웨어 가속 [스페셜](https://ko.wikipedia.org/wiki/스페셜_뮤직 "wikilink") 오디오 재생 및 녹음
  - 네트워크 – TCP 및 UDP [네트워크 소켓](https://ko.wikipedia.org/wiki/네트워크_소켓 "wikilink"), 데이터 캡슐화 기능, [HTTP](https://ko.wikipedia.org/wiki/HTTP "wikilink") 및 [파일 전송 프로토콜](https://ko.wikipedia.org/wiki/파일_전송_프로토콜 "wikilink") 클래스

### 언어 바인딩

SFML은 C++로 작성되어 있으며 C++ 인터페이스를 제공한다. 다른 프로그래밍 언어로 SFML을 사용할 수 있게 해주는 여러 [언어 바인딩이](https://ko.wikipedia.org/wiki/언어_바인딩 "wikilink") 존재한다.\[5\]

이 표는 2017년 기준으로 SFML을 위해 지원되는 바인딩을 나열한다.

| 이름                                                                            | 언어                                                                                         | 지원 버전 |
| ----------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ | ----- |
| [CSFML](http://www.sfml-dev.org/download/csfml)<sup>1</sup>                   | [C](https://ko.wikipedia.org/wiki/C_\(프로그래밍_언어\) "wikilink")                               | 2.3   |
| [SFML.Net](http://www.sfml-dev.org/download/sfml.net)<sup>1</sup>             | [.NET](https://ko.wikipedia.org/wiki/닷넷_프레임워크 "wikilink")                                  | 2.2   |
| [CrSFML](https://github.com/oprypin/crsfml)                                   | [Crystal](https://crystal-lang.org)                                                        | 2.4.1 |
| [DerelictSFML2](https://github.com/DerelictOrg/DerelictSFML2)                 | [D](https://ko.wikipedia.org/wiki/D_\(프로그래밍_언어\) "wikilink")                               | 2.3   |
| [DSFML](https://github.com/Jebbs/DSFML)                                       | [D](https://ko.wikipedia.org/wiki/D_\(프로그래밍_언어\) "wikilink")                               | 2.1   |
| [EuSFML2](https://github.com/gAndy50/EuSFML2)                                 | [Euphoria](https://ko.wikipedia.org/wiki/:en:Euphoria_\(programming_language\) "wikilink") | 2.3.2 |
| [csfml-fpc](https://github.com/DJMaster/csfml-fpc)                            | [프리 파스칼](https://ko.wikipedia.org/wiki/프리_파스칼 "wikilink")                                  | 2.4.0 |
| [GoSFML2](https://bitbucket.org/krepa098/gosfml2/wiki/Home)                   | [Go](https://ko.wikipedia.org/wiki/Go_\(프로그래밍_언어\) "wikilink")                             | 2.2   |
| [Hackage](https://hackage.haskell.org/package/SFML)                           | [Haskell](https://ko.wikipedia.org/wiki/하스켈 "wikilink")                                    | 2.3.2 |
| [JSFML](https://jsfml.sfmlprojects.org/)                                      | [Java](https://ko.wikipedia.org/wiki/자바_\(프로그래밍_언어\) "wikilink")                           | 2.2   |
| [SFML.jl](https://github.com/zyedidia/SFML.jl)                                | [Julia](../Page/줄리아_\(프로그래밍_언어\).md "wikilink")                                            | 2.2   |
| [nim-csfml](https://github.com/oprypin/nim-csfml)                             | [Nim](https://ko.wikipedia.org/wiki/:en:Nim_\(programming_language\) "wikilink")           | 2.3   |
| [Ocsfml](https://github.com/JoeDralliam/Ocsfml)                               | [OCaml](https://ko.wikipedia.org/wiki/OCaml "wikilink")                                    | 2.3   |
| [OCaml-SFML](http://ocaml-sfml.forge.ocamlcore.org/)                          | [OCaml](https://ko.wikipedia.org/wiki/OCaml "wikilink")                                    | 2.0   |
| [PasSFML](https://github.com/CWBudde/PasSFML)                                 | [Pascal](https://ko.wikipedia.org/wiki/파스칼_\(프로그래밍_언어\) "wikilink")                        | 2.3   |
| [pySFML](https://web.archive.org/web/20180527201512/https://python-sfml.org/) | [Python](https://ko.wikipedia.org/wiki/파이썬 "wikilink")                                     | 2.3.2 |
| [rbSFML](https://groogy.se/mainsite/rbsfml/)                                  | [Ruby](https://ko.wikipedia.org/wiki/루비_\(프로그래밍_언어\) "wikilink")                           | 2.3.2 |
| [rust-sfml](https://github.com/jeremyletang/rust-sfml)                        | [Rust](../Page/러스트_\(프로그래밍_언어\).md "wikilink")                                             | 2.3   |

<sup>1</sup> 공식 바인딩

## 같이 보기

  - [CreateJS](https://ko.wikipedia.org/wiki/CreateJS "wikilink")
  - [OpenGL](https://ko.wikipedia.org/wiki/OpenGL "wikilink")
  - [OpenGL 유틸리티 툴킷](https://ko.wikipedia.org/wiki/OpenGL_유틸리티_툴킷 "wikilink") (GLUT)
  - [심플 다이렉트미디어 레이어](https://ko.wikipedia.org/wiki/심플_다이렉트미디어_레이어 "wikilink") (SDL)

## 추가 문헌

  - Jan Haller, Henrik Vogelius Hansson, Artur Moreira: *SFML Game Development*, Packt Publishing,
  - <http://www.lifehacker.com.au/2013/02/xna-is-dead-3-alternatives-that-let-you-use-your-c-and-net-skills/>
  - <https://web.archive.org/web/20180417194130/http://www.binpress.com/tutorial/creating-a-city-building-game-with-sfml/137>
  - <http://www.gamefromscratch.com/page/Game-From-Scratch-CPP-Edition-The-Introduction.aspx>

## 각주

## 외부 링크

  -
  -
[분류:API](https://ko.wikipedia.org/wiki/분류:API "wikilink") [분류:오디오 라이브러리](https://ko.wikipedia.org/wiki/분류:오디오_라이브러리 "wikilink") [분류:C++ 라이브러리](https://ko.wikipedia.org/wiki/분류:C++_라이브러리 "wikilink") [분류:크로스 플랫폼 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_소프트웨어 "wikilink") [분류:자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_소프트웨어 "wikilink") [분류:그래픽 라이브러리](https://ko.wikipedia.org/wiki/분류:그래픽_라이브러리 "wikilink") [분류:리눅스 API](https://ko.wikipedia.org/wiki/분류:리눅스_API "wikilink") [분류:MacOS API](https://ko.wikipedia.org/wiki/분류:MacOS_API "wikilink") [분류:비디오 게임 개발](https://ko.wikipedia.org/wiki/분류:비디오_게임_개발 "wikilink") [분류:윈도우 API](https://ko.wikipedia.org/wiki/분류:윈도우_API "wikilink") [분류:Zlib 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:Zlib_라이선스_소프트웨어 "wikilink")

1.
2.
3.
4.
5.