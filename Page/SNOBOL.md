> This article is converted from Wikipedia: [SNOBOL](https://ko.wikipedia.org/wiki/SNOBOL).


**SNOBOL**(StriNg Oriented and symBOlic Language)은 1962년부터 1967년까지 [AT\&T](../Page/AT&T.md "wikilink") [벨 연구소에서](../Page/벨_연구소.md "wikilink") [David J. Farber](https://ko.wikipedia.org/wiki/David_J._Farber "wikilink"), [Ralph Griswold](https://ko.wikipedia.org/wiki/Ralph_Griswold "wikilink"), Ivan P. Polonsky가 개발한 컴퓨터 [프로그래밍 언어](../Page/프로그래밍_언어.md "wikilink") 시리즈이며, SNOBOL4까지 개발되었다. 1950년대와 1960년대 동안 개발된 수많은 텍스트 문자열 지향 언어들 가운데 하나였으며, SNOBOL 외에도 [COMIT](https://ko.wikipedia.org/wiki/COMIT "wikilink")과 [TRAC](https://ko.wikipedia.org/wiki/TRAC "wikilink")이 있다.

## 개발

초기의 SNOBOL 언어는 개발자가 다항식을 기호적으로 조작하기 위해 사용되는 도구로 제작되었다. [IBM 7090용](https://ko.wikipedia.org/wiki/IBM_7090 "wikilink") 어셈블리어로 작성되었다. 단순한 문법, 오직 하나의 자료형, 문자열, 함수의 부재, 선언의 부재, 그리고 오류 제어가 거의 없음을 특징으로 한다. 그러나 이러한 단숨함에도 불구하고 이 언어의 사용은 다른 그룹으로까지 퍼져나가기 시작했다. 그 결과 개발자들은 이를 확장하기로 결정하였다. 이들은 언어를 재작성하고 함수들을 더 추가했는데, 여기에는 표준 함수와 사용자 지정 함수를 아우르며, SNOBOL3가 탄생하기에 이른다. SNOBOL2는 존재하였으나 사용자 지정 함수 없는 중간 개발 버전으로 단명하였으며 출시되지 않았다. SNOBOL3는 매우 대중화되었으며 다른 프로그래머들에 의해 IBM 7090 이외의 다른 컴퓨터로 재작성되기도 했다. 그 결과 여러 비호환이 발생하기도 했다.

SNOBOL3가 대중화되면서 개발자들은 언어에 대한 더 많은 확장 요청을 받게 되었다. 또, 개발자들이 작성한 적이 없는 버전에 대한 버그와 비호환성에 대한 불평을 받기 시작했다. 이를 해결하고 1960년대 말에 도입된 새로운 컴퓨터를 최대한 활용하고자 수많은 자료형과 기능을 갖추면서 [가상 머신을](../Page/가상_머신.md "wikilink") 이용하여 컴퓨터 간 이식성을 개선한 SNOBOL4의 개발에 착수하였다.\[1\] SNOBOL4 언어 번역기는 여전히 어셈블리어로 작성되었다. 그러나 어셈블러의 매크로 기능들은 SNOBOL 구현 언어(SIL)의 가상 기계어를 정의하는데 사용되었다.

## 기능

SNOBOL4는 [정수](../Page/정수.md "wikilink"), 제한된 정밀 [실수](https://ko.wikipedia.org/wiki/실수 "wikilink"), [문자열](https://ko.wikipedia.org/wiki/문자열 "wikilink"), [패턴](https://ko.wikipedia.org/wiki/패턴 "wikilink"), [배열](../Page/배열.md "wikilink"), [테이블](https://ko.wikipedia.org/wiki/테이블 "wikilink")(연관 배열)과 같은 수많은 내장 [자료형](../Page/자료형.md "wikilink")을 지원하며 프로그래머가 추가적인 자료형과 새로운 [함수](../Page/함수.md "wikilink")를 정의할 수 있게 하고 있다. SNOBOL4의 프로그래머 정의 자료형 기능은 당시 진보된 것이며, 초기 [코볼](../Page/코볼.md "wikilink") 및 이후 [파스칼](../Page/파스칼.md "wikilink")의 레코드와 비슷하다.

모든 SNOBOL 명령 줄은 다음과 같은 형식을 취하고 있다.

  -
    *label subject pattern* **=** *object* **:** *transfer*

## 프로그램의 예

헬로 월드 프로그램은 아래와 같다.

``` snobol
          OUTPUT = "Hello world"
END
```

사용자 이름을 물어본 다음 출력 문장에 사용하는 단순한 프로그램은 다음과 같다.

``` snobol
          OUTPUT = "What is your name?"
          Username = INPUT
          OUTPUT = "Thank you, " Username
END
```

3개의 가능한 출력 중 하나를 선택하는 것은 다음과 같다.

``` snobol
          OUTPUT = "What is your name?"
          Username = INPUT
          Username "J"                                             :S(LOVE)
          Username "K"                                             :S(HATE)
MEH       OUTPUT = "Hi, " Username                                 :(END)
LOVE      OUTPUT = "How nice to meet you, " Username               :(END)
HATE      OUTPUT = "Oh. It's you, " Username
END
```

더 나올 것이 없을 때까지 요청 중인 입력을 계속하려면...

``` snobol
          OUTPUT = "This program will ask you for personal names"
          OUTPUT = "until you press return without giving it one"
          NameCount = 0                                            :(GETINPUT)
AGAIN     NameCount = NameCount + 1
          OUTPUT = "Name " NameCount ": " PersonalName
GETINPUT  OUTPUT = "Please give me name " NameCount + 1
          PersonalName = INPUT
          PersonalName LEN(1)                                      :S(AGAIN)
          OUTPUT = "Finished. " NameCount " names requested."
END
```

## 같이 보기

  - [아이콘 (프로그래밍 언어)](../Page/아이콘_\(프로그래밍_언어\).md "wikilink")

## 참고문헌

  - Griswold, Ralph E. *The Macro Implementation of SNOBOL4*. San Francisco, CA: W. H. Freeman and Company, 1972 ().

## 각주

## 외부 링크

  -
[분류:프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:프로그래밍_언어 "wikilink") [분류:1962년 개발된 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:1962년_개발된_프로그래밍_언어 "wikilink")

1.  See Chapter 1 of *The Macro Implementation of SNOBOL4*