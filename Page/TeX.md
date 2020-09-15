> This article is converted from Wikipedia: [TeX](https://ko.wikipedia.org/wiki/TeX).


**TeX**(, , )\[1\]은 [도널드 커누스가](https://ko.wikipedia.org/wiki/도널드_커누스 "wikilink") 만든 조판 프로그램이다.\[2\]

TeX 개발의 두 가지 목적은, 최소한의 노력으로 미려한 문서를 얻을 수 있도록 하는 것과, 컴퓨터 기종과 상관없이 똑같은 결과물을 얻도록 하는 것이다. 따라서 TeX으로 컴파일하여 만든 문서의 확장자는 device independent format을 뜻하는 .dvi이다. 이를 변환하여 PDF, [포스트스크립트](../Page/포스트스크립트.md "wikilink") 등의 문서파일을 얻는다. (.dvi를 만드는 것이 TeX의 가장 큰 특징 중 하나였으나, 요즘은 사실상 문서 표준으로 자리잡은 [PDF](../Page/PDF.md "wikilink")를 [dvi](https://ko.wikipedia.org/wiki/dvi "wikilink")를 거치지 않고 바로 만드는 방법도 많이 쓰인다.)

수학, 물리학, 컴퓨터 과학, 경제학 등 많은 분야에서 논문, 책자, 발표 슬라이드 등 다양한 문서 작성을 위해 사용된다. 그리고 무엇보다도 수식을 표현하는 데 있어 강력하다. 현재 나와 있는 명령어 기반 수식 편집이 가능한 워드프로세서 등(한글, 위키백과)의 명령어는 이 TeX을 기반으로 한 것이다. 수식에 강점을 갖고 있지만, 목차, 표목차, 그림목차, 각주, 미주, 장절명령등이 자동화되므로, 내용에 집중한 구조적 문서를 만드는 것을 강제하는 장점이 있다. 반면, 조판언어로서의 특징을 갖고 있어, 사용자들이 명령어를 익혀야 하는 등 초기 사용에 다소 진입장벽이 있다는 단점도 있다.

## 구조

텍과 주변 패키지들의 구조를 이해할 필요가 있다. 구조의 밑에서부터 엔진-포맷(또는 포맷의 집합인 패키지)-클래스 순으로 생각하면 쉽다. 우선, 커누스 교수가 개발한 TeX 엔진은 그 자체로 사용하기에는 TeX은 단순한 명령어들을 자주 사용해야 한다는 번거로움이 있었다. 이에 이를 보완하여 [레슬리 램포트가](../Page/레슬리_램포트.md "wikilink") TeX 위에서 구동하는 매크로방식의 포맷(자주 쓰이는 일련의 명령어를 하나의 명령어나 틀로 통합하여 간단하게 문서를 만들 수 있는 체계) LaTeX을 만들었다('레이텍'으로 읽는다).

이러한 포맷 중 수식편집에 강력한 기능을 가진 것에는 American Mathematical Society가 수학 논문 조판에 필요한 기능을 담아 만든 AMSTeX이 있다.\[3\] AMSTeX과 LaTeX 등을 합쳐 같이 배포하는 형태를 "패키지"라고 한다(이 패키지의 이름은 AMS-LaTex으로 부름). 또한, 한글 등 다국어 문서 편집을 용이하게 할 수 있는 포맷으로 LuaTeX, ConTeXt, XeTeX가 있다.\[4\]

이런 포맷을 사용하여 텍 문서를 작성할 경우 각 포맷마다 요구하는 형식이나 조건들을 선언해 주어야 하는데, 이를 간편하게 도와주는 것이 바로 "클래스"이다. 이중 한글사용자들에게 도움이 되는 것 중 하나가 Memoir 클래스, 그리고 Memoir 위에서 구동하며 이를 더 편하게 쓸 수 있게 해주는 클래스 위의 클래스로서 Oblivoir 클래스가 있다. 또한, 프리젠테이션 파일을 쉽게 만들어 주는 beamer 클래스도 널리 사용된다.

이러한 것들을 이용해 문서를 만들려면 먼저 텍스트 파일 에디터를 이용, 텍스트 문서에다 위에 열거한 포맷과 클래스를 선언하여 이를 쓸 것이라고 지정해 주고, 그의 규칙에 맞게 텍 코드에 따라 문서를 작성해서(HTML을 생각하면 쉽다) 컴파일 하면 pdf 등 최종출력본 문서를 얻게 된다.

그리고 이런 도구들과 이런 도구의 추가 설치 및 업데이트 한데 묶어서 배포하는 것이 ko.TeX 패키지 들이다. 이를 사용하기 위해서 2012년까지는 한글 TeX 사용자그룹\[5\]에 접속하여 ko.TeXlive를 다운받아야 했었는데, 2013년부터는 ko.TeX 관련 패키지가 [CTAN](../Page/CTAN.md "wikilink")에 대거 등재되면서\[6\] 단순히 TeXlive를 다운받아 사용하더라도 한글 텍을 사용할 수 있게 되었다.

## 한국어판 TeX

  - HLaTeX. 일명 한글 LaTeX: 개발자 은광희. ko.TeX 이전의 사실상 표준 한글 [LaTeX](../Page/LaTeX.md "wikilink")이었다.
  - hLaTeXp, hTeXp, 한글 TeX : 개발자 차재춘, HLaTeX과 동시기에 사용된 한글 TeX 시스템이다. 이와 같은 뿌리를 갖는 시스템은 [윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 기반에서 운용되는 hLaTeXn, hTeXn, 한TeX등
  - 한TeX: [KAIST](https://ko.wikipedia.org/wiki/KAIST "wikilink") 고기형 교수와 연구실이 [한글과컴퓨터](../Page/한글과컴퓨터.md "wikilink") 사의 의뢰로 만들었다. [트루타입](../Page/트루타입.md "wikilink") 글꼴을 이용하고, 자체 [DVI](https://ko.wikipedia.org/wiki/DVI "wikilink") 뷰어를 갖는 등, 현재 기준으로 보아도 뒤떨어지지 않는 사용 편의성을 가지고 있었다.
  - ko.TeX: 주 개발자 김도현 교수, 김강수, 은광희. dhucs의 저자들과 HLaTeX의 저자가 힘을 모아 새롭게 조성한 한글 TeX 구현 모음이다. dhucs의 [유니코드](../Page/유니코드.md "wikilink")기반의 한글 TeX 환경을 중심으로 [EUC-KR](https://ko.wikipedia.org/wiki/EUC-KR "wikilink")로 인코딩한 한글 문서 중심의 HLaTeX의 코드를 이어 받아, option에 따라 [유니코드](../Page/유니코드.md "wikilink")로 인코딩된 문서와 [EUC-KR](https://ko.wikipedia.org/wiki/EUC-KR "wikilink")로 인코딩된 예전 문서에 대한 호환성을 유지하고 있다. [2018년](../Page/2018년.md "wikilink") 현재 기준으로 TeX에서 [한글](https://ko.wikipedia.org/wiki/한글 "wikilink")을 사용하기 위한 시스템중 가장 안정화되어 있으며, 사실상 TeX에서 한글 구현의 표준이다.

## 수식 예제

| 코드                           | 표시                    |
| ---------------------------- | --------------------- |
| `e^{\pi i} + 1 = 0`          | \(e^{\pi i} + 1 = 0\) |
| `\frac 3 2` 또는 `{3 \over 2}` | \(\frac 3 2\)         |

## 각주

## 관련 문서

  - [LaTeX](../Page/LaTeX.md "wikilink")
  - [위키백과:TeX 문법](https://ko.wikipedia.org/wiki/위키백과:TeX_문법 "wikilink")

## 외부 링크

  - [한글 TeX 사용자 그룹 (KTUG)](https://web.archive.org/web/20130604184548/http://ktug.org/)

  - [hTeXp, hLaTeXp 홈페이지](https://web.archive.org/web/20090321062301/http://knot.kaist.ac.kr/htex/)

  - [플레인 TeX 퀵 레퍼런스 (PDF)](https://web.archive.org/web/20090206100110/http://refcards.com/docs/silvermanj/tex/tex-refcard-letter.pdf)

[TeX](https://ko.wikipedia.org/wiki/분류:TeX "wikilink") [분류:자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_소프트웨어 "wikilink") [분류:페이지 기술 언어](https://ko.wikipedia.org/wiki/분류:페이지_기술_언어 "wikilink") [분류:디지털 타이포그래피](https://ko.wikipedia.org/wiki/분류:디지털_타이포그래피 "wikilink") [분류:1978년 소프트웨어](https://ko.wikipedia.org/wiki/분류:1978년_소프트웨어 "wikilink") [분류:도널드 커누스](https://ko.wikipedia.org/wiki/분류:도널드_커누스 "wikilink") [분류:매크로 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:매크로_프로그래밍_언어 "wikilink")

1.  TeX은 ‘기술’이라는 뜻의 낱말이며 ‘테크닉’이라는 말의 어원이기도 한 그리스어 ‘(고전 발음: , 현대 발음: )’의 약어이다. X는 로마자 [X](https://ko.wikipedia.org/wiki/X "wikilink")(엑스)가 아닌 그리스 문자 [Χ](../Page/Χ.md "wikilink")(키, 카이)의 대문자를 가리키는 글자이다.
2.  버전 3 이후로는 3.14부터 시작하여 발전할 수록 버전 번호가 3.141592...로 이어지면서 [원주율](https://ko.wikipedia.org/wiki/원주율 "wikilink")에 수렴한다. TeX의 개발과 병행하여 커누스는 WEB라는 중간 언어를 만들어 같이 발전시킬 수 있다. 공식적인 지침서로 커누스가 지은 The TeXbook과 The Metafontbook이 있다. 이들은 단행본으로 출간되었으며 나중에 Computer and Typesetting이라는 전집물의 1, 2권이다.
3.  더 많은 기호와 수식을 사용할 수 있어 사실상 표준 패키지가 되었다. usepackage문으로 간단하게 사용할 수 있다
4.  AMSTeX 외에도, TeX의 기능을 첨가한 확장 변형과, 각 잡지 등의 특정한 포맷에 특화시킨 변형 등이 있다( KPSTeX: 한국 물리학회 포맷, ReVTeX: 미국 물리학회 포맷)
5.
6.