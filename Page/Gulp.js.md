> This article is converted from Wikipedia: [Gulp.js](https://ko.wikipedia.org/wiki/Gulp.js).


**gulp**(걸프)는 Fractal Innovations과\[1\] [깃허브](../Page/깃허브.md "wikilink") 오픈 소스 커뮤니티의 [오픈 소스](../Page/오픈_소스_소프트웨어.md "wikilink") [자바스크립트](../Page/자바스크립트.md "wikilink") 툴킷으로, [프론트엔드 웹 개발의](https://ko.wikipedia.org/wiki/프론트엔드_웹_개발 "wikilink") 스트리밍 [빌드 시스템로](https://ko.wikipedia.org/wiki/빌드_자동화 "wikilink") 사용된다.

[Node.js](../Page/Node.js.md "wikilink")와 [npm](https://ko.wikipedia.org/wiki/npm "wikilink") 기반의 태스크 러너이며, [소형화](https://ko.wikipedia.org/wiki/소형화 "wikilink"), 연결(concatenation), 캐시 버스팅(cache busting), [유닛 테스트](../Page/유닛_테스트.md "wikilink"), [린팅](../Page/린트_\(소프트웨어\).md "wikilink"), 최적화 등 웹 개발에 수반되는 시간 소모적이고 반복되는 태스크들을 자동화하기 위해 사용된다.\[2\]

gulp는 구성보다 코드(code-over-configuration) 접근 방식을 사용하여 태스크를 정의하며 이것들을 수행하기 위해 크기가 작은 단일 목적의 플러그인에 의존한다. gup 생태계는 300개 이상의 플러그인이 포함되어 있다.\[3\]

## gulpfile의 해부

gulpfile은 모든 동작이 gulp에 정의되는 장소이다. gulpfile는 최상위에 필요 플러그인이 포함되어 있으며, 끝부분에는 태스크의 정의와 기본 태스크가 위치한다.\[4\]

### 플러그인

``` javascript
//Adding dependencies
var gulp = require ('gulp');
var gutil = require ('util-gulp');
```

### 태스크

``` javascript
//Defining tasks
gulp.task ( 'taskName', function () {
//do something
});
```

``` javascript
function fn1 () {
// do something
}

function fn2 () {
// Do something else
}

// Task with array of function names
gulp.task ( 'taskName', ['fn1','fn2']);
```

### 기본 태스크

``` javascript
// Gulp default task
gulp.task ( 'default', [ '']);
```

## 각주

## 참고문헌

  -
  -
  -
## 외부 링크

  -
  -
[분류:자바스크립트 프로그래밍 도구](https://ko.wikipedia.org/wiki/분류:자바스크립트_프로그래밍_도구 "wikilink")

1.
2.
3.
4.