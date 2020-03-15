> This article is converted from Wikipedia: [MathML](https://ko.wikipedia.org/wiki/MathML).


**MathML**(Mathematical Markup Language)은 [XML](https://ko.wikipedia.org/wiki/XML "wikilink") 응용 중 하나로 [수학](https://ko.wikipedia.org/wiki/수학 "wikilink") 수식을 표현하고, 그 구조와 내용을 파악하기 위한 [마크업 언어이다](https://ko.wikipedia.org/wiki/마크업_언어 "wikilink"). [월드 와이드 웹](../Page/월드_와이드_웹.md "wikilink") 페이지 및 다른 문서들에 수식을 통합하는 것을 목적으로 한다. [W3C](https://ko.wikipedia.org/wiki/W3C "wikilink") 매스(math) [워킹 그룹의](https://ko.wikipedia.org/wiki/워킹_그룹 "wikilink") 권고이며 [HTML5](https://ko.wikipedia.org/wiki/HTML5 "wikilink")의 일부이다.

## 표현과 의미

MathML은 *표현*만을 다루지 않으며 수식의 *의미* 요소도 다룬다(후자를 "내용Content MathML”이라 한다). 수식의 의미는 표현과는 별개로 보존되므로, 내용이 어떻게 소통되는지는 사용자에게 맡겨진다. 예를 들어 MathML 내장 웹 페이지는 많은 브라우저들에서 정상 웹 페이지로 보이지만, 시각장애인 사용자는 [스크린 리더](https://ko.wikipedia.org/wiki/스크린_리더 "wikilink") ([인터넷 익스플로러용](https://ko.wikipedia.org/wiki/인터넷_익스플로러 "wikilink") [매스플레이어](https://ko.wikipedia.org/wiki/매스플레이어 "wikilink") [플러그인](../Page/플러그인.md "wikilink"), [오페라](https://ko.wikipedia.org/wiki/오페라_\(웹_브라우저\) "wikilink") 9.50 빌드 9656 이상, 파이어폭스용 [파이어 복스](https://ko.wikipedia.org/wiki/파이어_복스 "wikilink") 확장 등)를 이용하여 MathML 읽기를 제공받을 수 있다.

### 표현 MathML

표현 MathML은 수식의 화면 표시에 집중하며, 30여 가지의 엘리먼트들이 있다. 이들 엘리먼트의 이름은 모두 `m`으로 시작한다. 표현 MathML 식은 *토큰*들이 모여 구성되며, 레이아웃을 조절하는 고수준 엘리먼트에 의해 조합된다. (50여 종의 애트리뷰트 또한 존재하는데, 이들은 주로 미세 조정에 쓰인다.).

토큰 엘리먼트들은 일반적으로 문자만을 포함한다(즉 다른 엘리먼트를 포함하지 않는다). 다음을 포함한다:

  - <mi>`x`</mi> – 식별자;
  - <mo>`+`</mo> – 연산자;
  - <mn>`2`</mn> – 숫자.
  - <mtext>`non zero`</mtext> – 텍스트.

이들 토큰 엘리먼트들은 호스트 언어에서 마크업을 허용하는 확장점으로 쓰일 수도 있다는 것에 주의하라. [HTML5](https://ko.wikipedia.org/wiki/HTML5 "wikilink")에서의 MathML은 mtext에서 대부분의 HTML 마크업을 허용한다. 즉,

  - <mtext><b>`non`</b>`  zero `</mtext>

와 같이, HTML 마크업을 MathML 내에 내장된 텍스트를 꾸미는 데 쓸 수도 있다(이 예제에서는 첫 번째 단어를 굵게 처리한다).

이들은 레이아웃 엘리먼트를 이용하여 조합된다:

  - <mrow> – 항목들로 이루어진 가로 행;
  - <msup>, <munderover> 등 – 위첨자, limits over and under operators like sums, etc.;
  - <mfrac> – 분수;
  - <msqrt> and <mroot> – 근호;
  - <mfenced> - 내용을 괄호(예를 들어 소괄호)로 감싼다.

HTML이나 XML에서처럼, 특별한 기호나 이름을 나타내는 데 쓸 수 있는 많은 엔티티([entities](https://ko.wikipedia.org/wiki/entities "wikilink"))가 있다. 예를 들어 π, → 등이다. 한 가지 흥미로운 MathML의 기능은, 일반적으로 보이지 않는 연산자를 표현하기 위한 엔티티도 존재한다는 것이다. 암묵적인 곱셈연산자(implicit multiplication) `⁢` 가 그 예이다. 그 외에 다음과 같은 것들이 있다: U+2061 FUNCTION APPLICATION; U+2062 INVISIBLE TIMES; U+2063 INVISIBLE SEPARATOR; U+2064 INVISIBLE PLUS. 완전한 MathML 엔티티 명세는 \[[http://www.w3.org/TR/MathML3/chapter7.html\]에](http://www.w3.org/TR/MathML3/chapter7.html%5D에) 있으며, HTML 및 XML에서의 일반적인 사용을 위한 연관 명세([1](http://www.w3.org/TR/xml-entity-names/))와 밀접히 연관되어 있다.

따라서, 수식 \(a x^2+b x+c\)는 두 개의 레이아웃 엘리먼트를 필요로 한다: 하나는 전체적인 수평 행을, 다른 하나는 지수 표현을 위한 위첨자 행을 생성한다. 레이아웃 엘리먼트와 토큰만을 포함시키면, 구조는 다음과 같이 될 것이다:

``` xml
    <mrow>
      a &InvisibleTimes; <msup>x 2</msup>
      + b &InvisibleTimes; x
      + c
    </mrow>

```

그러나 개별 토큰들은 식별자(mi), 연산자(mo), 숫자(mn)로 구별되어야 한다. 토큰 마크업을 추가하면, 완성된 양식은 아래와 같다:

``` xml
    <mrow>
      <mi>a</mi> <mo>&InvisibleTimes;</mo> <msup><mi>x</mi><mn>2</mn></msup>
      <mo>+</mo><mi>b</mi><mo>&InvisibleTimes;</mo><mi>x</mi>
      <mo>+</mo><mi>c</mi>
    </mrow>

```

유효한 MathML 문서는 전형적으로 XML 선언, DOCTYPE 선언, document 엘리먼트로 이루어진다. 그리고 document body는 \(엘리먼트 속에 나타나는 MathML 표현식을 포함한다. MathML이 [[HTML|HTML]], [[DocBook|DocBook]], 다른 [[XML|XML]] 스키마 같은 더 일반적인 문서에 포함되는 일도 흔하다. 위의 MathML 예제만으로 이루어진 완전한 문서는 아래와 같다:

<source lang="xml">
 <?xml version="1.0" encoding="UTF-8"?>
  <!DOCTYPE math PUBLIC "-//W3C//DTD MathML 2.0//EN"
           "http://www.w3.org/Math/DTD/mathml2/mathml2.dtd">
  <math ns="http://www.w3.org/1998/Math/MathML">
    <mrow>
      <mi>a</mi>
      <mo>&InvisibleTimes;</mo>
      <msup>
        <mi>x</mi>
        <mn>2</mn>
      </msup>
      <mo>+</mo>
      <mi>b</mi>
      <mo>&InvisibleTimes; </mo>
      <mi>x</mi>
      <mo>+</mo>
      <mi>c</mi>
    </mrow>\)

</source>

### 내용 MathML

내용 MathML은 수식의 모양보다는 내용에 집중한다. 내용 MathML의 중심은 함수 적용을 나타내는 <apply> 엘리먼트이다. 적용하는 함수는 <apply> 아래의 첫 번째 자식 엘리먼트(child element)이고, 나머지 자식 엘리먼트들은 피연산자(형식인수)이다. 내용 MathML은 적은 수의 애트리뷰트만을 사용한다.

식별자나 숫자 같은 토큰들은 표현 MathML에서처럼 개별적으로 마크업된다. 다만 `ci`나 `cn` 같은 엘리먼트로 표현된다. 연산자들은 단순히 다른 종류의 토큰이 되는 게 아니라, 특수 엘리먼트로 표현되는데, 이들의 수학적 의미는 MathML에 의해 인지된다. `times`, `power` 등이 그 예이다. 100개가 넘는 함수 및 연산자에 대응되는 엘리먼트가 있다(\[[http://www.w3.org/TR/MathML3/chapter4.html\#contm.opel\]를](http://www.w3.org/TR/MathML3/chapter4.html#contm.opel%5D를) 보라.).

예를 들어, <apply><sin/><ci>`x`</ci></apply>는 \(\sin(x)\)를 나타내며, <apply><plus/><ci>`x`</ci><cn>`5`</cn></apply>는 \(x+5\)를 나타낸다. 연산자와 함수를 표현하는 엘리먼트들은 빈 엘리먼트(empty element)인데, 그 이유는 그들의 피연산자들이 <apply>를 포함하는 다른 엘리먼트이기 때문이다.

수식 \(a x^2+b x+c\)는 아래와 같이 표현할 수 있다.

``` xml
<math>
    <apply>
        <plus/>
        <apply>
            <times/>
            <ci>a</ci>
            <apply>
                <power/>
                <ci>x</ci>
                <cn>2</cn>
            </apply>
        </apply>
        <apply>
            <times/>
            <ci>b</ci>
            <ci>x</ci>
        </apply>
        <ci>c</ci>
    </apply>
</math>
```

내용 MathML은 [Scheme](https://ko.wikipedia.org/wiki/스킴_\(프로그래밍_언어\) "wikilink") 같은 [functional language의](https://ko.wikipedia.org/wiki/Functional_programming "wikilink") [expressions와](https://ko.wikipedia.org/wiki/Binary_expression_tree "wikilink") 거의 같은 구조이다. <apply>`...`</apply>는 Scheme의 `(...)`에 해당하고, 많은 연산자 및 함수들이 Scheme 함수에 대응된다. 이런 간단한 문자 변환과 개별 토큰의 태그 제거만으로, 위 예제를 아래와 같이 변환할 수 있다:

` (plus`
`   (times a (power x 2))`
`   (times b x)`
`   c)`

이는 널리 알려진 XML 엘리먼트 구조와 LISP 또는 Scheme의 [S-expressions](https://ko.wikipedia.org/wiki/S-expressions "wikilink") 사이의 가까운 관계를 반영한다.\[1\]\[2\]

## 예제 및 다른 형식과의 비교

[이차 방정식의](https://ko.wikipedia.org/wiki/이차_방정식 "wikilink") 근의 공식

\[x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}\] 은 [LaTeX](https://ko.wikipedia.org/wiki/LaTeX "wikilink") 문법으로는 다음처럼 나타낸다.

``` latex
x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
```

또다른 문서 마크업 언어인 [troff](https://ko.wikipedia.org/wiki/troff "wikilink")/[eqn](https://ko.wikipedia.org/wiki/eqn "wikilink")에서는 다음처럼 나타낸다.

`x={-b +- sqrt{b sup 2 - 4ac}} over 2a`

[오픈오피스](https://ko.wikipedia.org/wiki/오픈오피스 "wikilink") 수식편집에서는 다음 두 가지 방법으로 나타낸다.

`x={-b plusminus sqrt {b^2 - 4 ac}} over {2 a}`
`x={-b +- sqrt {b^2 - 4ac}} over 2a`

이 수식을 표현 MathML로는 다음처럼 나타낼 수 있다.

``` xml
<math ns="http://www.w3.org/1998/Math/MathML">
 <mi>x</mi>
 <mo>=</mo>
 <mfrac>
  <mrow>
   <mrow>
    <mo>-</mo>
    <mi>b</mi>
   </mrow>
   <mo>&PlusMinus;</mo>
   <msqrt>
    <msup>
     <mi>b</mi>
     <mn>2</mn>
    </msup>
    <mo>-</mo>
    <mrow>
     <mn>4</mn>
     <mo>&InvisibleTimes;</mo>
     <mi>a</mi>
     <mo>&InvisibleTimes;</mo>
     <mi>c</mi>
    </mrow>
   </msqrt>
  </mrow>
  <mrow>
   <mn>2</mn>
   <mo>&InvisibleTimes;</mo>
   <mi>a</mi>
  </mrow>
 </mfrac>
</math>
```

내용 MathML로는 다음과 같다.

``` xml
<apply>
  <eq/>
  <ci>x</ci>
  <apply>
    <divide/>
    <apply>
      <csymbol>&PlusMinus;</csymbol>
      <apply>
        <minus/>
        <ci>b</ci>
      </apply>
      <apply>
        <root/>
        <degree><cn>2</cn></degree>
        <apply>
          <minus/>
          <apply>
            <power/>
            <ci>b</ci>
            <cn>2</cn>
          </apply>
          <apply>
            <times/>
            <cn>4</cn>
            <ci>a</ci>
            <ci>c</ci>
          </apply>
        </apply>
      </apply>
    </apply>
    <apply>
      <times/>
      <cn>2</cn>
      <ci>a</ci>
    </apply>
  </apply>
</apply>
```

## MathML을 HTML/XHTML 파일에 포함시키기

MathML은 XML이므로 다른 XML 파일에 삽입될 수 있다. Firefox 3+나 Opera 9.6+(불완전하게 지원) 같은 최신 브라우저들은 XHTML에 포함된 표현 MathML을 화면에 표시할 수 있다.

``` xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.1 plus MathML 2.0//EN" "http://www.w3.org/Math/DTD/mathml2/xhtml-math11-f.dtd">
<html ns="http://www.w3.org/1999/xhtml" xml:lang="en">
  <head>
    <title>Example of MathML embedded in an XHTML file</title>
    <meta name="description" content="Example of MathML embedded in an XHTML file"/>
  </head>
  <body>
    <h1>Example of MathML embedded in an XHTML file</h1>
    <p>
      The area of a circle is
      <math ns="http://www.w3.org/1998/Math/MathML">
        <mi>π<!-- π --></mi>
        <mo>⁢<!-- &InvisibleTimes; --></mo>
        <msup>
          <mi>r</mi>
          <mn>2</mn>
        </msup>
      </math>.
    </p>
  </body>
</html>
```

  -
    [435px](https://ko.wikipedia.org/wiki/파일:MathMLxhtml.png "wikilink")
    <small>A rending of the formula for a circle in mathml+xhtml using firefox 22 on Mac OSX</small>

인라인 MathML 또한 [HTML5](https://ko.wikipedia.org/wiki/HTML5 "wikilink") 파일에서 지원된다. [WebKit](https://ko.wikipedia.org/wiki/WebKit "wikilink") ([Safari](https://ko.wikipedia.org/wiki/사파리_\(웹_브라우저\) "wikilink"), [Chrome](https://ko.wikipedia.org/wiki/Google_Chrome "wikilink")), [Gecko](../Page/게코_\(레이아웃_엔진\).md "wikilink") ([Firefox](https://ko.wikipedia.org/wiki/Firefox "wikilink")). xhtml에서처럼 네임스페이스를 지정할 필요가 없다.

``` html5
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>Example of MathML embedded in an HTML5 file</title>
  </head>
  <body>
    <h1>Example of MathML embedded in an HTML5 file</h1>
    <p>
      The area of a circle is
      <math>
        <mi>π<!-- π π --></mi>
        <mo>⁢<!-- &InvisibleTimes; --></mo>
        <msup>
          <mi>r</mi>
          <mn>2</mn>
        </msup>
      </math>.
    </p>
  </body>
</html>
```

## 지원 소프트웨어

### 편집기

최근에 발표된 [마이크로소프트 워드](https://ko.wikipedia.org/wiki/마이크로소프트_워드 "wikilink"), [오픈오피스](https://ko.wikipedia.org/wiki/오픈오피스 "wikilink") 워드프로세서, 아래한글 [HWP](https://ko.wikipedia.org/wiki/HWP "wikilink") 등의 여러 문서 편집기에서 MathML을 지원하고 있다.

수식 입력 및 편집 전문 소프트웨어인 [매스매직](https://ko.wikipedia.org/wiki/매스매직 "wikilink"), MathType, [매스매티카](https://ko.wikipedia.org/wiki/매스매티카 "wikilink"), [메이플](https://ko.wikipedia.org/wiki/메이플_\(소프트웨어\) "wikilink") 등에서도 입력된 수식을 MathML 포맷으로 저장하거나, MathML 수식을 읽어들여 편집할 수 있도록 지원한다.

### 변환

[W3.org](https://ko.wikipedia.org/wiki/W3.org "wikilink")는 MathML 관련 소프트웨어의 다운로드를 위한 목록을 유지하고 있다.\[3\]

수식은 일종의 세계 표준 언어이기도 하지만, 수학이나 물리 분야 뿐만 아니라 이공계 각 분야는 물론 통계와 인문 분야 등 그 사용 분야가 폭넓고, 그 다양한 수식 형태와 심볼 등으로 구성된 복잡성으로 인해 키보드와 마우스를 기본으로 하는 컴퓨터 인터페이스 상에서 입력과 편집은 쉬운 일이 아니다.

따라서 [수식 편집기](https://ko.wikipedia.org/wiki/수식_편집기 "wikilink") 소프트웨어마다 저마다의 장점을 앞세운 인터페이스와 다양한 입력 방식이 제시되었고, 프로그램에 따라 다양한 파일 포맷이 만들어지게 되었다.

많은 수식 편집기가 내부적인 수식 저장 포맷으로 [TeX](https://ko.wikipedia.org/wiki/TeX "wikilink")과 [LaTeX](https://ko.wikipedia.org/wiki/LaTeX "wikilink") 표현을 차용하거나 이를 응용하여 사용하고 있기는 하지만, 용도에 따라 수식을 화면에 표시하기 위한 그림 포맷([GIF](https://ko.wikipedia.org/wiki/GIF "wikilink"), [JPEG](https://ko.wikipedia.org/wiki/JPEG "wikilink"), [PNG](https://ko.wikipedia.org/wiki/PNG "wikilink") 등), 다른 응용 프로그램과 호환하기 위한 포맷([LaTeX](https://ko.wikipedia.org/wiki/LaTeX "wikilink"), [TeX](https://ko.wikipedia.org/wiki/TeX "wikilink"), MathML, WMF, PICT 등), 고품질 출력을 위한 포맷([EPS](https://ko.wikipedia.org/wiki/EPS "wikilink"), [PDF](https://ko.wikipedia.org/wiki/PDF "wikilink"), [SVG](https://ko.wikipedia.org/wiki/SVG "wikilink"), [DVI](https://ko.wikipedia.org/wiki/DVI "wikilink")) 등 다양한 포맷으로 사용되고 있다.

대부분의 수식편집기 소프트웨어는 자체 파일 포맷 외에, 이러한 파일 포맷 중 한두가지 포맷으로의 저장이나 변환은 지원하지만, 다양한 파일 포맷 간의 손쉬운 변환을 제공하는 것은 많지 않으며, 수식의 복잡성과 원래 사용되었던 심볼 서체의 의존성 등으로 인해 완벽한 변환을 기대하기는 어려운 경우가 많다.

현재로서는 수식 편집 전문 프로그램인 [MathMagic](https://ko.wikipedia.org/wiki/MathMagic "wikilink")이 가장 다양한 파일 포맷을 읽고 쓸 수도록 지원하고 있으며, Plain TeX, LaTeX, AMS LaTeX, MathML, GIF, JPEG, PNG, BMP, PICT, WMF, EPS, PDF, Wiki 수식(MediaWiki TeXvc), ASCIIMath, ASCIIMathML 등의 포맷을 지원하고 있으며(버전에 따라 다소 차이가 있을 수 있음), MathType, MS Word 수식, Google Docs 수식, Zoho Writer 등에서 작성된 수식도 지원한다. MathMagic은 또한 일괄변환(Batch conversion) 기능을 지원하고 있어, 동시에 여러가지 파일 포맷으로 된 복수의 파일이나 폴더를 다른 포맷으로 변환할 수도 있다.

### 웹 변환

[ASCIIMathML](https://ko.wikipedia.org/wiki/ASCIIMathML "wikilink")\[4\] provides a [JavaScript](https://ko.wikipedia.org/wiki/JavaScript "wikilink") library to rewrite a convenient Wiki-like text syntax used inline in web pages into MathML on the fly; it works in [Gecko-based](../Page/게코_\(레이아웃_엔진\).md "wikilink") browsers, and [Internet Explorer](https://ko.wikipedia.org/wiki/Internet_Explorer "wikilink") with [MathPlayer](https://ko.wikipedia.org/wiki/MathPlayer "wikilink"). LaTeXMathML\[5\] does the same for (a subset of) the standard [LaTeX](https://ko.wikipedia.org/wiki/LaTeX "wikilink") mathematical syntax. [ASCIIMathML](https://ko.wikipedia.org/wiki/ASCIIMathML "wikilink") syntax would also be quite familiar to anyone used to electronic scientific calculators.

[MathJax](https://ko.wikipedia.org/wiki/MathJax "wikilink"): 자바스크립트 라이브러리로서 인라인 렌더링이 가능하다. LaTeX을 MathML로 변환하여 브라우저가 해석하게 할 수도 있다.\[6\]

[Blahtex](https://ko.wikipedia.org/wiki/Blahtex "wikilink"): TeX-to-MathML 변환기로 [MediaWiki](https://ko.wikipedia.org/wiki/MediaWiki "wikilink")에서 쓸 목적으로 만들어졌다.

[jqMath](https://ko.wikipedia.org/wiki/jqMath "wikilink"):\[7\] TeX과 비슷한 간단한 문법을, 브라우저가 MathML을 지원하면 MathML로, 그렇지 않으면 단순 HTML과 CSS로, 동적으로 변환하는 자바스크립트 모듈이다.

[LaTeXML](https://ko.wikipedia.org/wiki/LaTeXML "wikilink"): 펄 유틸리티로, LaTeX 문서를 HTML로 변환한다. 수식 변환에 MathML 또는 비트맵 이미지를 선택할 수 있다.

## 웹 브라우저

주요 [웹 브라우저](https://ko.wikipedia.org/wiki/웹_브라우저 "wikilink") 중에서 최신 버전의 [게코](../Page/게코_\(레이아웃_엔진\).md "wikilink") 엔진을 사용하는 브라우저([파이어폭스](https://ko.wikipedia.org/wiki/파이어폭스 "wikilink")나 [카미노](https://ko.wikipedia.org/wiki/카미노 "wikilink") 등)와 [오페라](https://ko.wikipedia.org/wiki/오페라_\(웹_브라우저\) "wikilink") 9.5 이상에서 지원하고 있다.

게코 엔진을 쓰는 브라우저에서 현재 제대로 기능을 지원받으려면 특별한 글꼴을 따로 다운로드받아야 한다.

오페라 브라우저에서는 MathML for CSS profile 기능을 지원하고 있다.

## 같이 보기

  - [TeX](https://ko.wikipedia.org/wiki/TeX "wikilink")
  - [LaTeX](https://ko.wikipedia.org/wiki/LaTeX "wikilink")
  - [수식 편집기](https://ko.wikipedia.org/wiki/수식_편집기 "wikilink")

## 각주

## 외부 링크

  -
  - [MathML 지원 소프트웨어 목록](http://www.w3.org/Math/Software/)

  -
[분류:XML 마크업 언어](https://ko.wikipedia.org/wiki/분류:XML_마크업_언어 "wikilink") [분류:W3C 표준](https://ko.wikipedia.org/wiki/분류:W3C_표준 "wikilink") [분류:XML 기반 표준](https://ko.wikipedia.org/wiki/분류:XML_기반_표준 "wikilink")

1.  Steven DeRose. The SGML FAQ Book: Understanding the Relationship of SGML and XML, Kluwer Academic Publishers, 1997. .
2.  [Canonical S-expressions\#cite note-0](https://ko.wikipedia.org/wiki/Canonical_S-expressions#cite_note-0 "wikilink")
3.  [MathML Implementations](http://www.w3.org/Math/Software/)
4.  [ASCIIMathML: Math on the web for everyone](http://www1.chapman.edu/~jipsen/mathml/asciimath.html). .chapman.edu. Retrieved on 9 May 2012.
5.  [LaTeXMathML: a dynamic LaTeX mathematics to MathML converter](http://www.maths.nottingham.ac.uk/personal/drw/lm.html). Maths.nottingham.ac.uk. Retrieved on 9 May 2012.
6.  [MathJax MathML Support](http://www.mathjax.org/resources/docs/?mathml.html) . Mathjax.org. Retrieved on 9 May 2012.
7.  [jqMath – Put Math on the Web](http://mathscribe.com/author/jqmath.html). Mathscribe.com. Retrieved on 9 May 2012.