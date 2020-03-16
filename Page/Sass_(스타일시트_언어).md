> This article is converted from Wikipedia: [Sass \( \)](https://ko.wikipedia.org/wiki/Sass_\(_\)).


[섬네일](https://ko.wikipedia.org/wiki/파일:Sass_Logo_Color.svg "wikilink") **Sass**(syntactically awesome stylesheets, 사스)는 [햄튼 캐틀린이](https://ko.wikipedia.org/wiki/햄튼_캐틀린 "wikilink") 설계하고 [나탈리 바이첸바움이](https://ko.wikipedia.org/wiki/나탈리_바이첸바움 "wikilink") 개발한 [스타일시트 언어이다](https://ko.wikipedia.org/wiki/스타일시트_언어 "wikilink").\[1\]\[2\] 초기 버전들 이후에 바이첸바움과 [크리스 엡스타인은](https://ko.wikipedia.org/wiki/크리스_엡스타인 "wikilink") Sass 파일에 쓰이는 단순 스크립팅 언어인 SassScript로 Sass의 확장을 계속하였다.

Sass는 [종속형 시트](../Page/종속형_시트.md "wikilink")(CSS)로 [해석](https://ko.wikipedia.org/wiki/인터프리트_언어 "wikilink") 및 [컴파일되는](../Page/컴파일_언어.md "wikilink") [스크립트 언어이다](../Page/스크립트_언어.md "wikilink"). SassScript는 그 자체로 스크립트 언어이다. Sass는 2가지 신택스로 구성되어 있다. 인덴티드 신택스(indented syntax)라는 이름의 원래의 신택스는 [Haml](https://ko.wikipedia.org/wiki/Haml "wikilink")과 비슷한 신택스를 사용한다.\[3\] 규칙 분리를 위해 [들여쓰기를](../Page/들여쓰기_방식.md "wikilink") 사용하여 코드 블록과 [새줄 문자를](../Page/새줄_문자.md "wikilink") 구분한다. 새로운 신택스 "SCSS"는 CSS의 것과 비슷한 블록 형식을 사용한다. 블록 안의 줄을 구분하기 위해 괄호를 사용하여 코드 블록과 세미콜론을 인지한다. 인덴티드 신택스와 SCSS 파일들은 전통적으로 각각 .sass, .scss [확장자를](../Page/파일_확장자.md "wikilink") 가진다.

[CSS3는](../Page/종속형_시트.md "wikilink") 이들에 적용할 규칙을 묶는 일련의 셀렉터와 의사 셀렉터(pseudo-selector)들로 구성된다. Sass\[4\](두 신택스에 해당)는 특히 [객체 지향 언어와](../Page/객체_지향_프로그래밍.md "wikilink") 같은 더 전통적인 [프로그래밍 언어에서](../Page/프로그래밍_언어.md "wikilink") 사용 가능하면서도 CSS3 자체적으로는 이용이 불가능한 여러 매커니즘을 제공함으로써 CSS를 확장한다. SassScript이 해석될 때 Sass 파일에 정의된 여러 셀렉터를 위한 CSS 규칙 블록을 만들어낸다. Sass 인터프리터는 SassScript를 CSS로 변환한다. 아니면 Sass는 .sass나 .scss 파일을 모니터링하다가 .sass 또는 .scss 파일이 저장될 때마다 .css 파일로 변환, 출력할 수 있다.\[5\] Sass는 CSS를 위한 [신택틱 슈거라](https://ko.wikipedia.org/wiki/신택틱_슈거 "wikilink") 할 수 있다.

Sass 공식 구현체는 [오픈 소스이며](../Page/오픈_소스_소프트웨어.md "wikilink") [루비로](../Page/루비_\(프로그래밍_언어\).md "wikilink") 코딩되어 있다. 그러나 [다트](https://ko.wikipedia.org/wiki/다트_\(프로그래밍_언어\) "wikilink"), [PHP](../Page/PHP.md "wikilink"), 또 libSass라는 이름의 [C의](../Page/C_\(프로그래밍_언어\).md "wikilink") 고성능 구현체를 포함하여 다른 구현체들도 존재한다.\[6\]\[7\] 또, JSass라는 이름의 [자바](../Page/자바_\(프로그래밍_언어\).md "wikilink") 구현체도 있다.\[8\] 게다가 [Vaadin](https://ko.wikipedia.org/wiki/Vaadin "wikilink")은 Sass의 자바 구현체를 포함하고 있다.\[9\] 인덴티드 신택스는 메타 언어이다. SCSS는 [네스티드 메타 언어인데](../Page/메타_언어.md "wikilink"), 유효한 CSS가 동일한 시맨틱스를 포함하고 있는 유효한 SCSS이다. Sass는 [모질라 파이어폭스](../Page/모질라_파이어폭스.md "wikilink") 확장 기능 [파이어버그](https://ko.wikipedia.org/wiki/파이어버그 "wikilink")와의 통합을 지원한다.\[10\]

SassScript는 다음의 매커니즘을 제공한다: 변수, 네스팅, [mixin](https://ko.wikipedia.org/wiki/mixin "wikilink"), 셀렉터 상속.\[11\]

## 변수

Sass는 변수 정의를 허용한다. 변수는 [$](https://ko.wikipedia.org/wiki/$ "wikilink") (`$`)로 시작할 수 있다. 변수 할당은 [콜론](https://ko.wikipedia.org/wiki/콜론 "wikilink")(`:`)으로 마무리한다.\[12\]

SassScript는 4가지 자료형을 지원한다:\[13\]

  - [수](../Page/수_\(수학\).md "wikilink") (단위 포함)
  - [문자열](https://ko.wikipedia.org/wiki/문자열 "wikilink") (인용 부호가 있거나 없이)
  - 컬러 (하나 이상의 이름)
  - [불리언](../Page/불리언_자료형.md "wikilink")

변수는 사용 가능한 여러 [함수들](../Page/함수_\(프로그래밍\).md "wikilink") 가운데 하나에 대해 [매개변수로](../Page/매개변수_\(컴퓨터_프로그래밍\).md "wikilink") 사용하거나 결과물이 될 수 있다.\[14\] 변환 과정 중에 변수의 값들은 출력 CSS 문서에 삽입된다.\[15\]

SCSS 스타일:

``` scss
$primary-color: #3bbfce;
$margin: 16px;

.content-navigation {
  border-color: $primary-color;
  color: darken($primary-color, 10%);
}

.border {
  padding: $margin / 2;
  margin: $margin / 2;
  border-color: $primary-color;
}
```

Sass 스타일:

``` sass
$primary-color: #3bbfce
$margin: 16px

.content-navigation
  border-color: $primary-color
  color: darken($primary-color, 10%)

.border
  padding: $margin/2
  margin:  $margin/2
  border-color: $primary-color
```

컴파일 결과:

``` css
.content-navigation {
  border-color: #3bbfce;
  color: #2b9eab;
}

.border {
  padding: 8px;
  margin: 8px;
  border-color: #3bbfce;
}
```

## 네스팅

CSS는 논리적인 네스팅을 지원하지만 코드 블록 자체는 네스팅되지 않는다. Sass는 서로 간에 네스팅된 코드를 삽입할 수 있게 한다.\[16\]

Sass 스타일:

``` sass
table.hl
  margin: 2em 0
  td.ln
    text-align: right

li
  font:
    family: serif
    weight: bold
    size: 1.3em
```

SCSS 스타일:

``` scss
table.hl {
  margin: 2em 0;
  td.ln {
    text-align: right;
  }
}

li {
  font: {
    family: serif;
    weight: bold;
    size: 1.3em;
  }
}
```

컴파일 결과:

``` css
table.hl {
  margin: 2em 0;
}
table.hl td.ln {
  text-align: right;
}

li {
  font-family: serif;
  font-weight: bold;
  font-size: 1.3em;
}
```

[이름공간](../Page/이름공간.md "wikilink") 네스팅 및 부모 참조를 포함한 더 복잡한 유형의 네스팅은 Sass 문서에서 논하고 있다.\[17\]

``` scss
@mixin table-base {
  th {
    text-align: center;
    font-weight: bold;
  }
  td, th {
    padding: 2px;
  }
}

#data {
  @include table-base;
}
```

Sass 스타일:

``` sass
=table-base
  th
    text-align: center
    font-weight: bold
  td, th
    padding: 2px

#data
  +table-base
```

컴파일 결과:

``` css
#data th {
  text-align: center;
  font-weight: bold;
}
#data td, #data th {
  padding: 2px;
}
```

### 루프

Sass는 , , 를 사용하여 변수에 대한 루프를 지원하며, 비슷한 클래스나 id를 가진 요소들에 각기 다른 스타일을 적용하기 위해 사용할 수 있다.

``` sass
$squareCount: 3
@for $i from 1 through $squareCount
  #square-#{$i}
   background-color: red
   width: 50px * $i
   height: 120px / $i
```

위의 예의 컴파일 결과:

``` css
#square-1 {
  background-color: red;
  width: 50px;
  height: 120px;
}

#square-2 {
  background-color: red;
  width: 100px;
  height: 60px;
}

#square-3 {
  background-color: red;
  width: 150px;
  height: 40px;
}
```

### 인수

Mixins은 또한 인수를 지원한다.\[18\]

``` sass
=left($dist)
  float: left
  margin-left: $dist

#data
  +left(10px)
```

컴파일 결과:

``` css
#data {
  float: left;
  margin-left: 10px;
}
```

### 혼합

``` sass
=table-base
  th
    text-align: center
    font-weight: bold
  td, th
    padding: 2px

=left($dist)
  float: left
  margin-left: $dist

#data
  +left(10px)
  +table-base
```

컴파일 결과:

``` css
#data {
  float: left;
  margin-left: 10px;
}
#data th {
  text-align: center;
  font-weight: bold;
}
#data td, #data th {
  padding: 2px;
}
```

## 셀렉터 상속

CSS3는 [문서 객체 모델](../Page/문서_객체_모델.md "wikilink")(DOM) 계층을 지원하지만 셀렉터 상속을 허용하지 않는다. Sass에서 상속은 @extend 키워드를 사용하고 다른 셀렉터를 참조하는 코드 블록 내 줄을 삽입함으로써 수행된다. 이 확장된 셀렉터의 속성은 호출을 하는 셀렉터에 적용된다.\[19\]

``` sass
.error
  border: 1px #f00
  background: #fdd

.error.intrusion
  font-size: 1.3em
  font-weight: bold

.badError
  @extend .error
  border-width: 3px
```

컴파일 결과:

``` css
.error, .badError {
  border: 1px #f00;
  background: #fdd;
}

.error.intrusion,
.badError.intrusion {
  font-size: 1.3em;
  font-weight: bold;
}

.badError {
  border-width: 3px;
}
```

Sass는 [다중 상속을](https://ko.wikipedia.org/wiki/다중_상속 "wikilink") 지원한다.\[20\]

## libSass

2012년에 HTML5 개발자 콘퍼런스에서 Sass의 개발자 햄튼 캐틀린은 [무브웹](https://ko.wikipedia.org/wiki/무브웹 "wikilink")의 엔지니어링 팀, 캐틀린, Aaron Leung이 개발한 Sass의 오픈 소스 C++ 구현체 libSass의 버전 1.0을 발표하였다.\[21\]\[22\] 현재의 Sass 유지보수자 크리스 엡스타인 또한 기여할 의도가 있음을 내비쳤다.\[23\]

캐틀린에 따르면 "libSass는 아무 곳에나 던져 넣으면 Sass가 들어간다... 오늘날에는 파이어폭스에 바로 넣어서 파이어폭스를 빌드하고 컴파일된다. 가능한 처음부터 우리만의 파서를 썼다."\[24\]

libSass의 설계 목적은 다음과 같다:

  - 성능 - 개발자들은 Sass의 루비 구현체 대비 10배 속도가 더 빠르다고 보고하였다.\[25\]
  - 더 쉬운 통합 - libSass는 Sass를 더 많은 소프트웨어에 더 쉽게 통합할 수 있게 한다. libSass 이전까지는 Sass를 특정 언어나 소프트웨어 제품에 밀접하게 통합하기 위해 루비 인터프리터를 번들해야 했다. 이와 대조적으로 libSass는 외부 의존성이나 C 계열 인터페이스 없이 정적 링크가 가능한 라이브러리이므로 다른 프로그래밍 언어와 도구에 직접 Sass를 래핑하는 것이 용이하다.

이를테면, 오픈 소스 libSass 바인딩은 현재 [Node](../Page/Node.js.md "wikilink"), [Go](../Page/Go_\(프로그래밍_언어\).md "wikilink"), [Ruby용으로](../Page/루비_\(프로그래밍_언어\).md "wikilink") 존재한다.\[26\]

  - 호환성 - libSass의 목적은 공식 루비 구현체의 Sass와의 완전한 호환성이다. 그러나 이 목표는 아직까지 완전히 충족되지 않고 있다.\[27\]

## IDE 통합

| IDE                                                                       | 소프트웨어       | 웹사이트                                                                                          |
| ------------------------------------------------------------------------- | ----------- | --------------------------------------------------------------------------------------------- |
| [어도비 드림위버](../Page/어도비_드림위버.md "wikilink") CC 2017                        |             | <https://blogs.adobe.com/creativecloud/getting-started-with-css-preprocessors-less-and-sass/> |
| [이클립스](../Page/이클립스_\(소프트웨어\).md "wikilink")                              |             |                                                                                               |
| [이맥스](../Page/이맥스.md "wikilink")                                          | SCSS Mode   | <https://github.com/antonj/scss-mode/>                                                        |
| [JetBrains IntelliJ IDEA (얼티밋 에디션)](../Page/IntelliJ_IDEA.md "wikilink")  |             | <https://www.jetbrains.com/idea/>                                                             |
| [JetBrains PhpStorm](https://ko.wikipedia.org/wiki/PhpStorm "wikilink")   |             | <http://www.jetbrains.com/phpstorm/>                                                          |
| [JetBrains RubyMine](https://ko.wikipedia.org/wiki/루비마인 "wikilink")       |             | <http://www.jetbrains.com/ruby/>                                                              |
| [마이크로소프트 비주얼 스튜디오](../Page/마이크로소프트_비주얼_스튜디오.md "wikilink")                | Mindscape   | <http://www.mindscapehq.com/products/web-workbench>                                           |
| [마이크로소프트 비주얼 스튜디오](../Page/마이크로소프트_비주얼_스튜디오.md "wikilink")                | SassyStudio | <http://visualstudiogallery.msdn.microsoft.com/85fa99a6-e4c6-4a1c-9f00-e6a8129b6f4d>          |
| [마이크로소프트 웹 매트릭스](https://ko.wikipedia.org/wiki/마이크로소프트_웹_매트릭스 "wikilink") |             | <https://web.archive.org/web/20150512042040/http://www.microsoft.com/web/>                    |
| [넷빈즈](../Page/넷빈즈.md "wikilink")                                          |             | <http://plugins.netbeans.org/plugin/34929/scss-support>                                       |
| [Vim](../Page/Vim.md "wikilink")                                          | haml.zip    | <http://www.vim.org/scripts/script.php?script_id=1433>                                        |
| [아톰](../Page/아톰_\(문서_편집기\).md "wikilink")                                 |             | <https://github.com/atom/language-sass>                                                       |
| [비주얼 스튜디오 코드](../Page/비주얼_스튜디오_코드.md "wikilink")                          |             | <https://code.visualstudio.com/Docs/languages/css>                                            |

## 각주

## 외부 링크

  -
  - [Haml/Sass Google Group](https://groups.google.com/group/haml)

  - [pyScss, a Python Scss library and client](https://github.com/Kronuz/pyScss)

  - [Sai the mixins extension and CSS authoring framework for Less & Sass/Scss (Git)](https://github.com/hapztron/sai)

  - [Sass tools and resources](https://web.archive.org/web/20150323061242/http://www.logogulf.ae/blog/sass-tools-and-resources/)

[분류:2006년 개발된 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:2006년_개발된_프로그래밍_언어 "wikilink") [분류:MIT 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:MIT_라이선스_소프트웨어 "wikilink") [분류:루비 (프로그래밍 언어)](https://ko.wikipedia.org/wiki/분류:루비_\(프로그래밍_언어\) "wikilink") [분류:스타일시트 언어](https://ko.wikipedia.org/wiki/분류:스타일시트_언어 "wikilink") [분류:자유 라이브러리](https://ko.wikipedia.org/wiki/분류:자유_라이브러리 "wikilink")

1.
2.
3.
4.
5.  [Sass - Syntactically Awesome Stylesheets](http://sass-lang.com/tutorial.html) Tutorial
6.
7.
8.
9.
10. [Sass (Syntactically Awesome StyleSheets)](http://sass-lang.com/docs/yardoc/file.SASS_REFERENCE.html) SASS_REFERENCE
11.
12.
13.
14. [Module: Sass::Script::Functions](http://sass-lang.com/docs/yardoc/Sass/Script/Functions.html) Sass Functions
15.
16.
17.
18.
19.
20.
21.
22.
23.
24.
25.
26.
27.