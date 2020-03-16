> This article is converted from Wikipedia: [Gettext](https://ko.wikipedia.org/wiki/Gettext).


[컴퓨팅](../Page/컴퓨팅.md "wikilink")에서 **gettext**는 [유닉스 계열](../Page/유닉스_계열.md "wikilink") 컴퓨터 [운영 체제의](../Page/운영_체제.md "wikilink") 다국어 프로그램을 작성할 목적으로 흔히 쓰이는 [국제화와 지역화](../Page/국제화와_지역화.md "wikilink")(i18n, L10n) 시스템이다. 가장 널리 쓰이는 gettext 구현물은 1995년 [GNU 프로젝트가](../Page/GNU_프로젝트.md "wikilink") 공개한 **GNU gettext**이다.

## 역사

gettext는 본래 1990년대 초 [썬 마이크로시스템즈가](../Page/썬_마이크로시스템즈.md "wikilink") 작성하였다. [GNU 프로젝트는](../Page/GNU_프로젝트.md "wikilink") 1995년에 이 시스템의 [자유 소프트웨어](../Page/자유_소프트웨어.md "wikilink") 구현물인 GNU gettext를 공개하였다.\[1\]

## 동작

### 프로그래밍

소스 코드는 GNU gettext 호출을 사용하기 위해 처음 수정되어 있다. 대부분의 [프로그래밍 언어의](../Page/프로그래밍_언어.md "wikilink") 경우 이것은 사용자가 `gettext` 함수 안에서 참조할 [문자열](https://ko.wikipedia.org/wiki/문자열 "wikilink")을 래핑함으로써 처리된다. 입력 시간을 절약하기 위해, 또 코드의 어수선함을 줄이기 위해 이 함수는 `_`로 엘리어스 처리되는데, [C](../Page/C_\(프로그래밍_언어\).md "wikilink") 코드에서 이것은:

``` C
printf(gettext("My name is %s.\n"), my_name);
```

다음과 같이 된다:

``` C
printf(_("My name is %s.\n"), my_name);
```

## 참조

<references />

## 외부 링크

  -

[분류:GNU 프로젝트 소프트웨어](https://ko.wikipedia.org/wiki/분류:GNU_프로젝트_소프트웨어 "wikilink")

1.  <http://compgroups.net/comp.unix.solaris/History-of-gettext-et-al>