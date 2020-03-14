> This article is converted from Wikipedia: [ATTRIB](https://ko.wikipedia.org/wiki/ATTRIB).


**attrib**는 [도스](https://ko.wikipedia.org/wiki/도스 "wikilink"), [OS/2](https://ko.wikipedia.org/wiki/OS/2 "wikilink"), [마이크로소프트 윈도의](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 명령 가운데 하나이다. attrib의 기능은 [파일 특성](https://ko.wikipedia.org/wiki/파일_특성 "wikilink") (읽기 전용/r, 보관/a, 시스템/s, 숨김/h)을 설정하고 제거하는 것이다. 이러한 특성들은 파일을 보호하고 분류할 목적으로 다양한 소프트웨어에 사용된다.\[1\]

수많은 사용자들은 일반적으로 읽기 전용 특성을 마주치면서 소프트웨어 사용 시 사용자가 파일을 덮어쓰거나 추가하지 못하게 한다. 그러나 사용자에게 확인을 받은 뒤에는 소프트웨어가 이 옵션을 무효화할 수 있다. 보관 특성은 어느 파일을 백업할 필요가 있는지를 알려주기 위해 다양한 백업 및 파일 복사 프로그램에 사용된다.\[2\] 숨김 특성은 영향을 받는 파일들이 수많은 프로그램들에 보이지 않게 하지만 다양한 소프트웨어, 특히 파일 나열, 표시, 검색을 목적으로 설계된 소프트웨어는 숨김 파일을 보이게 만들 수 있으며 숨김 처리되어 있음을 표시해준다. 시스템 특성은 특정한 운영 체제 파일들을 가리키며 다른 특성들에 비해 대부분의 소프트웨어의 작동에 덜 영향을 미친다.

## attrib 명령어의 정의

윈도 파일에는 4가지 특성이 있다.

  - (r) 읽기 전용 파일 특성
  - (a) 보관 파일 특성
  - (s) 시스템 파일 특성
  - (h) 숨김 파일 특성

하나 이상의 파일을 +와 -를 사용하여 설정하거나 설정을 해제할 수 있다. 3가지 옵션 스위치가 있지만 아래의 스위치들이 모든 버전의 윈도에서 인식하는 것은 아니다.:

  - /S: 현재 폴더와 모든 하위 폴더에서 일치하는 파일을 처리한다.
  - /D: 폴더를 처리한다. ([윈도 2000](https://ko.wikipedia.org/wiki/윈도_2000 "wikilink"), [윈도 XP에만](https://ko.wikipedia.org/wiki/윈도_XP "wikilink") 적용됨)
  - /L: 기호화된 링크의 대상과 기호화된 링크의 특성에 대해 작업한다. ([윈도 비스타](https://ko.wikipedia.org/wiki/윈도_비스타 "wikilink"), [윈도 서버 2008에](https://ko.wikipedia.org/wiki/윈도_서버_2008 "wikilink") 도입됨)

일반적인 attrib 명령어의 문법은 다음과 같다:

  -

      -
        attrib \[+r|-r\] \[+a|-a\] \[+h|-h\] \[+s|-s\] \[d:\]\[path\]filename \[/s\] \[/d\] \[/l\]

예를 들어, 읽기 전용과 숨김 특성을 현재 디렉터리의 모든 파일에서 제거하려면 다음과 같이 입력한다:

  -

      -
        attrib -r -h \*.\* /s /d

\-s 변수는 파일에 대한 시스템 특성을 제거하며 주의 있게 사용해야 한다. 일반 시스템 파일에는 사용할 수 없다.

## 예

`C:\DOS>attrib +S +H example.jpg`

## 같이 보기

  - [cacls](https://ko.wikipedia.org/wiki/cacls "wikilink") - MS 윈도 NT 파일 시스템 ACL 제어 유틸리티
  - [chattr](https://ko.wikipedia.org/wiki/chattr "wikilink") - 유닉스/리눅스에 쓰이는 특성 관리 명령어

## 참조

<references />

## 외부 링크

  - [Microsoft TechNet Attrib article](http://technet.microsoft.com/en-us/library/bb490868)

  - [Microsoft DOS attrib command](http://www.computerhope.com/attribhl.htm)

[분류:외부 도스 명령어](https://ko.wikipedia.org/wiki/분류:외부_도스_명령어 "wikilink") [분류:윈도우 명령어](https://ko.wikipedia.org/wiki/분류:윈도우_명령어 "wikilink")

1.
2.