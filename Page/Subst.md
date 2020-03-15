> This article is converted from Wikipedia: [Subst](https://ko.wikipedia.org/wiki/Subst).


**`subst`**는 논리, 물리 드라이브의 경로를 [가상 드라이브로](https://ko.wikipedia.org/wiki/가상_드라이브 "wikilink") 대체하는 [도스](https://ko.wikipedia.org/wiki/도스 "wikilink") [운영 체제](https://ko.wikipedia.org/wiki/운영_체제 "wikilink") 명령어이다. 옛날에는 보안에 민감한 [PC의](https://ko.wikipedia.org/wiki/개인용_컴퓨터 "wikilink") 숨겨진 드라이브를 드러내는 데 사용하였다. `subst`명령어는 [윈도 2000](https://ko.wikipedia.org/wiki/윈도_2000 "wikilink") 이후의 [명령 줄 인터프리터에서도](https://ko.wikipedia.org/wiki/명령_줄_인터프리터 "wikilink") 사용할 수 있다.\[1\]

## 사용법

아래에는 [윈도 비스타의](https://ko.wikipedia.org/wiki/윈도_비스타 "wikilink") 명령 프롬프트에서 실행한 SUBST 도움말의 출력문이다:

    Microsoft Windows [Version 6.0.6000]
    (C) Copyright 1985-2005 Microsoft Corp.

    C:\>subst /?
    경로를 드라이브 문자로 지정합니다.

    SUBST [드라이브1: [드라이브2:]경로]
    SUBST 드라이브1: /D

      드라이브1:        경로에 지정할 가상 드라이브를 지정합니다.
      [드라이브2:]경로  가상 드라이브에 지정할 실제 드라이브와 경로를
                        지정합니다.
      /D                가상 드라이브를 지웁니다.

    매개 변수를 지정하지 않고 SUBST를 사용하면, 현재의 가상 드라이브를 표시합니다.

    C:\>

이를테면 C:의 루트를 X: 드라이브로 마운트하려면 명령 줄에 `subst X: C:\`라고 입력하면 된다. 이렇게 되면 탐색기에 X:라는 새로운 드라이브가 나타날 것이다.

## 제한

모든 [윈도 프로세스가](https://ko.wikipedia.org/wiki/윈도_프로세스 "wikilink") 이러한 방법으로 드라이브 문자열을 사용할 수 있는 것은 아니다.

## 같이 보기

  - [가상 드라이브](https://ko.wikipedia.org/wiki/가상_드라이브 "wikilink")

## 참조

<references />

## 외부 링크

  - [마이크로소프트 테크넷의 Subst 문건](http://technet.microsoft.com/en-us/library/bb491006.aspx)

[분류:외부 도스 명령어](https://ko.wikipedia.org/wiki/분류:외부_도스_명령어 "wikilink") [분류:윈도우 명령어](https://ko.wikipedia.org/wiki/분류:윈도우_명령어 "wikilink")

1.  [마이크로소프트 문건](http://technet.microsoft.com/en-us/library/bb491006.aspx)