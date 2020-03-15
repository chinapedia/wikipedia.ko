> This article is converted from Wikipedia: [PostCSS](https://ko.wikipedia.org/wiki/PostCSS).


**PostCSS**는 일상적인 [CSS](https://ko.wikipedia.org/wiki/종속형_시트 "wikilink") 동작을 자동화하기 위해 [자바스크립트](https://ko.wikipedia.org/wiki/자바스크립트 "wikilink") 기반 [플러그인](https://ko.wikipedia.org/wiki/플러그인 "wikilink")을 사용하는 [소프트웨어 개발 도구이다](https://ko.wikipedia.org/wiki/프로그래밍_도구 "wikilink").\[1\] 이 도구는 [위키백과](https://ko.wikipedia.org/wiki/위키백과 "wikilink"),\[2\]\[3\] [페이스북](https://ko.wikipedia.org/wiki/페이스북 "wikilink"),\[4\], [깃허브](https://ko.wikipedia.org/wiki/깃허브 "wikilink")의 코드를 개발하기 위해 사용되어 왔다.\[5\]\[6\] PostCSS는 [npm](../Page/Npm_\(소프트웨어\).md "wikilink") 사용자들 간에 가장 선호되는 CSS 도구이다.\[7\] Evil Martians의 프론트엔드 작업에서 아이디어를 가져와 Andrey Sitnik에 의해 설계되었다.\[8\]

## 동작 원리

### 구조

[섬네일](https://ko.wikipedia.org/wiki/파일:PostCSS_scheme.svg "wikilink")

[Sass와](../Page/Sass_\(스타일시트_언어\).md "wikilink") [Less](https://ko.wikipedia.org/wiki/Less "wikilink")와 달리 PostCSS는 CSS 컴파일 틀 언어가 아닌 CSS 도구 개발을 위한 [프레임워크이다](https://ko.wikipedia.org/wiki/소프트웨어_프레임워크 "wikilink").\[9\] 그러나 Saas와 LESS와 같은 틀 언어를 개발하기 위해 사용할 수 있다.\[10\]

PostCSS 코어는 다음으로 구성된다:\[11\]

  - **CSS [파서](https://ko.wikipedia.org/wiki/파서 "wikilink")**: CSS 코드의 줄을 위한 객체 트리([AST](https://ko.wikipedia.org/wiki/추상_구문_트리 "wikilink"))를 생성한다.
  - **[클래스의](https://ko.wikipedia.org/wiki/객체_지향_프로그래밍 "wikilink") 집합**: 트리를 구성한다.
  - **CSS 생성기**: 객체 트리를 위한 CSS 줄을 생성한다.
  - **코드 맵 생성기**: CSS 변경을 위해 사용된다.

유용한 모든 기능은 플러그인을 통해 사용할 수 있다. 이 플러그인들은 [객체 트리와](https://ko.wikipedia.org/wiki/추상_구문_트리 "wikilink") 함께 동작하는 작은 프로그램들이다. 코어가 CSS 문자열을 객체 트리로 변환한 뒤 플러그인은 이 트리를 분석하고 변경한다. 이 때 PostCSS 코어는 플러그인 변경 트리를 위한 새로운 CSS 문자열을 생성한다.

### 사용법

PostCSS와 플러그인 모두 [자바스크립트](https://ko.wikipedia.org/wiki/자바스크립트 "wikilink")로 작성되어 있으며 [npm을](../Page/Npm_\(소프트웨어\).md "wikilink") 통해 배포된다.

PostCSS는 저급 자바스크립트 조작을 위한 [API](https://ko.wikipedia.org/wiki/API "wikilink")를 제공한다:

``` js
// Load the core and plugins from npm
const postcss = require('postcss')
const autoprefixer = require('autoprefixer')
const precss = require('precss')

// Indicate the plugins to use
const processor = postcss([autoprefixer, precss])

// Indicate the CSS code and the names of the input/output file
processor.process('a {}', { from: './app.css', to: './app.build.css' })
  // Use Promise API in case there are asynchronous plugins
  .then(result => {
    // Get the post-processed CSS code displayed
    console.log(result.css)
    // Get the warning messages displayed
    for ( let message of result.warnings() ) {
      console.warn(message.toString())
    }
  })
```

## 각주

## 외부 링크

  - [Official website](http://postcss.org/)

  -
  - [Plugin list](http://postcss.parts/)

[분류:종속형 시트](https://ko.wikipedia.org/wiki/분류:종속형_시트 "wikilink") [분류:구문 분석](https://ko.wikipedia.org/wiki/분류:구문_분석 "wikilink") [분류:자바스크립트로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:자바스크립트로_작성된_자유_소프트웨어 "wikilink") [분류:MIT 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:MIT_라이선스_소프트웨어 "wikilink") [분류:자유 컴파일러와 인터프리터](https://ko.wikipedia.org/wiki/분류:자유_컴파일러와_인터프리터 "wikilink")

1.  [First article about PostCSS in Tuts+ course](http://webdesign.tutsplus.com/tutorials/postcss-deep-dive-what-you-need-to-know--cms-24535)
2.  [Adding PostCSS commit in Wikipedia repo](https://github.com/wikimedia/portals/commit/998d7ce74c1f68397a52434ce9b85064de7d0008)
3.  [Wikimedia Stylelint Config](https://github.com/wikimedia/stylelint-config-wikimedia)
4.  [Improving CSS quality at Facebook and beyond](https://code.facebook.com/posts/879890885467584/improving-css-quality-at-facebook-and-beyond/)
5.  [PostCSS settings GitHub build tool](https://archive.is/20160823060733/https://github.com/primer/primer/blob/master/.postcss.json)
6.  [Primer Stylelint Config](https://github.com/primer/stylelint-config-primer)
7.  [CSS preprocessors downloads from npm](http://www.npmtrends.com/postcss-vs-less-vs-node-sass-vs-stylus)
8.  [Evil Martians commit in PostCSS repo](https://github.com/postcss/postcss/commit/513f9c1b46a7085ac215e4de9bac5c617d5b2f26)
9.  [What is PostCSS discussion](https://github.com/postcss/postcss/issues/861)
10. [PostCSS Deep Dive: Preprocessing with “PreCSS”](http://webdesign.tutsplus.com/tutorials/postcss-deep-dive-preprocessing-with-precss--cms-24583)
11. [Andrey Sitnik - PostCSS: The Future After Sass and LESS](https://www.youtube.com/watch?v=1yUFTrAxTzg)