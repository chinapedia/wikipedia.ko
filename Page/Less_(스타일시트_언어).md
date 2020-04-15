> This article is converted from Wikipedia: [Less \(스타일시트 언어\)](https://ko.wikipedia.org/wiki/Less_\(스타일시트_언어\)).


**Less**(Leaner Style Sheets, **LESS**, 레스)는 [종속형 시트](../Page/종속형_시트.md "wikilink")(CSS)로 컴파일한 다음 클라이언트 사이드나 서버 사이드에서 실행할 수 있는 동적 [전처리기](https://ko.wikipedia.org/wiki/전처리기 "wikilink") [스타일시트 언어이다](https://ko.wikipedia.org/wiki/스타일시트_언어 "wikilink").\[1\] Alexis Sellier가 설계한 Less는 [Sass의](../Page/Sass_\(스타일시트_언어\).md "wikilink") 영향을 받았으며 CSS와 같은 블록 서식 문법을 채택한 Sass의 더 새로운 "SCSS" 문법에 영향을 주었다.\[2\] Less는 [오픈 소스이다](../Page/오픈_소스_소프트웨어.md "wikilink"). 최초 버전은 [루비로](../Page/루비_\(프로그래밍_언어\).md "wikilink") 작성되었다. 그러나 이후 버전에서 루비 사용이 구식 처리되어 [자바스크립트](../Page/자바스크립트.md "wikilink")로 변경되었다. Less의 들여쓰기 문법은 [네스티드(nested)된 메타언어이며](../Page/메타_언어.md "wikilink") 유효한 CSS는 동일한 시맨틱스를 갖는 유효한 Less 코드이다. Less는 다음의 매커니즘을 제공한다: [변수](https://ko.wikipedia.org/wiki/변수 "wikilink"), 네스팅(nesting), [mixin](https://ko.wikipedia.org/wiki/mixin "wikilink"), [연산자](https://ko.wikipedia.org/wiki/연산자 "wikilink"), [함수](../Page/함수.md "wikilink"). Less와 그 밖의 CSS 전처리기와의 주된 차이점의 경우 Less는 브라우저에 의해 less.js를 통해 실시간 컴파일을 허용한다는 것이다.\[3\]\[4\]

## 변수

**Less**는 변수 정의를 허용한다. Less의 변수는 [골뱅이표](../Page/골뱅이표.md "wikilink")(@)로 정의된다. 변수 할당은 [콜론](https://ko.wikipedia.org/wiki/콜론 "wikilink")(:)을 통해 이루어진다.

변환 중에 변수의 값들은 출력 CSS 문서에 삽입된다.\[5\]

``` less
@pale-green-color: #4D926F;

#header {
  color: @pale-green-color;
}
h2 {
  color: @pale-green-color;
}
```

상기의 Less 코드는 다음의 CSS 코드로 컴파일된다.

``` css
#header {
  color: #4D926F;
}
h2 {
  color: #4D926F;
}
```

## 믹스인

믹스인(mixin)은 클래스 이름을 속성 중 하나로 포함시킴으로써 클래스의 모든 속성을 다른 클래스 안으로 임베드하는 것을 허용하며, 이로써 일종의 상수나 변수처럼 동작한다. 이들은 마치 함수처럼 동작하며 인수를 취한다. CSS 자체는 믹스인을 지원하지 않는다. 즉, 반복되는 코드는 각 위치에 반복되어야 한다. 믹스인은 더 효율적이고 깨끗한 코드 반복을 허용하며 쉬운 코드 변경 또한 가능케 한다.\[6\]

``` less
.rounded-corners (@radius: 5px 10px 8px 2px) {
  -webkit-border-radius: @radius;
  -moz-border-radius: @radius;
  border-radius: @radius;
}

#header {
  .rounded-corners;
}
#footer {
  .rounded-corners(10px 25px 35px 0px);
}
```

위의 Less 코드는 다음의 CSS 코드로 컴파일된다:

``` css
#header {
  -webkit-border-radius: 5px 10px 8px 2px;
  -moz-border-radius: 5px 10px 8px 2px;
  border-radius: 5px 10px 8px 2px;
}
#footer {
  -webkit-border-radius: 10px 25px 35px 0px;
  -moz-border-radius: 10px 25px 35px 0px;
  border-radius: 10px 25px 35px 0px;
}
```

Less는 파라메트릭 믹스인(parametric mixin)이라는 특별한 타입의 룰셋(ruleset)이 있어서 클래스처럼 믹스가 가능하지만 파라미터를 수락한다.

``` less
#header {
  h1 {
    font-size: 26px;
    font-weight: bold;
  }
  p {
    font-size: 16px;
    a {
      text-decoration: none;
      color: red;
      &:hover {
        border-width: 1px;
        color: #fff;
      }
    }
  }
}
```

위의 Less 코드는 다음의 CSS 코드로 컴파일된다:

``` css
#header h1 {
  font-size: 26px;
  font-weight: bold;
}
#header p {
  font-size: 16px;
}
#header p a {
  text-decoration: none;
  color: red;
}
#header p a:hover {
  border-width: 1px;
  color: #fff;
}
```

## 같이 보기

  - [Sass (스타일시트 언어)](../Page/Sass_\(스타일시트_언어\).md "wikilink")

## 각주

## 외부 링크

  -
  - [Less source code repository (Git)](https://github.com/less/less.js)

  - [LESS Hat mixins library](https://github.com/csshat/lesshat)

  - [Sai the mixins extension and CSS authoring framework for LESS & SASS/SCSS (Git)](https://github.com/hapztron/sai)

[분류:자바스크립트 라이브러리](https://ko.wikipedia.org/wiki/분류:자바스크립트_라이브러리 "wikilink") [분류:아파치 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:아파치_라이선스_소프트웨어 "wikilink") [분류:스타일시트 언어](https://ko.wikipedia.org/wiki/분류:스타일시트_언어 "wikilink") [분류:자유 라이브러리](https://ko.wikipedia.org/wiki/분류:자유_라이브러리 "wikilink")

1.  [Official Less website](http://lesscss.org/) Official Less website
2.  [Sass and Less](http://nex-3.com/posts/83-sass-and-less)  Sass and Less
3.
4.
5.
6.