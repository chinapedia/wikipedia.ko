> This article is converted from Wikipedia: [Env](https://ko.wikipedia.org/wiki/Env).


**env**는 [유닉스](https://ko.wikipedia.org/wiki/유닉스 "wikilink") 및 [유닉스 계열](https://ko.wikipedia.org/wiki/유닉스_계열 "wikilink") [운영 체제용](https://ko.wikipedia.org/wiki/운영_체제 "wikilink") [셸](https://ko.wikipedia.org/wiki/유닉스_셸 "wikilink") [명령어](https://ko.wikipedia.org/wiki/명령어 "wikilink")이다. [환경 변수의](https://ko.wikipedia.org/wiki/환경_변수 "wikilink") 목록을 출력하거나, 현존하는 환경을 수정하지 않고도 변경된 환경 내에서 다른 유틸리티를 실행하는데 사용할 수 있다. env를 사용함으로써 변수를 추가하거나 제거할 수 있으며, 기존 변수는 새로운 값을 이들에 할당함으로써 변경할 수 있다.

실제로 env는 다른 용도로 사용되기도 한다. 올바른 [인터프리터](https://ko.wikipedia.org/wiki/인터프리터 "wikilink")를 실행하기 위해 [셸 스크립트에](https://ko.wikipedia.org/wiki/셸_스크립트 "wikilink") 자주 쓰인다. 이렇게 사용할 경우 환경은 일반적으로 변경되지 않는다.

## 예

새로운 셸을 위해 환경을 지우는 방법은 다음과 같다(기존의 환경 변수가 없는 새로운 환경 만들기):

``` bash
env -i /bin/sh
```

[X](https://ko.wikipedia.org/wiki/X_윈도_시스템 "wikilink") 응용 프로그램인 [xcalc](https://ko.wikipedia.org/wiki/xcalc "wikilink")를 실행하고 이를 다른 디스플레이에 표시하는 방법은 다음과 같다:

``` bash
env DISPLAY=foo.bar:1.0 xcalc
```

매우 단순한 [파이썬](https://ko.wikipedia.org/wiki/파이썬 "wikilink") 스크립트 코드는 다음과 같다:

``` bash
#!/usr/bin/env python2
print "Hello World."
```

이 예에서 `/usr/bin/env`는 `env` 명령의 완전한 [경로](https://ko.wikipedia.org/wiki/경로 "wikilink")이다. 환경은 변경되지 않는다.

## 같이 보기

  - [set](https://ko.wikipedia.org/wiki/set "wikilink")

## 외부 링크

  -
  - [env](http://www.gnu.org/software/coreutils/manual/html_node/env-invocation.html) -- manual page ([GNU](https://ko.wikipedia.org/wiki/GNU "wikilink") [coreutils](https://ko.wikipedia.org/wiki/coreutils "wikilink")).

  -
[분류:표준 유닉스 프로그램](https://ko.wikipedia.org/wiki/분류:표준_유닉스_프로그램 "wikilink") [분류:환경 변수](https://ko.wikipedia.org/wiki/분류:환경_변수 "wikilink")