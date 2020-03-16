> This article is converted from Wikipedia: [Xargs](https://ko.wikipedia.org/wiki/Xargs).


**xargs**는 [유닉스](../Page/유닉스.md "wikilink") 및 [유닉스 계열](../Page/유닉스_계열.md "wikilink") [운영 체제의](../Page/운영_체제.md "wikilink") 명령어로 [표준 입력을](https://ko.wikipedia.org/wiki/표준_입력 "wikilink") 통해 명령 줄을 만들고 실행하는 데 사용한다. 버전 2.6.23 이전의 [리눅스 커널에서는](../Page/리눅스_커널.md "wikilink") 긴 목록의 매개변수가 명령어를 통해 이용하지 못하는 경우도 간혹 있으므로\[1\] xargs는 변수 목록을 여러 하부 목록으로 잘게 나누어서 받아들일 수 있게 한다.

예를 들면, 다음 명령어들은 /path 아래에 파일들이 너무 많이 있을 경우 "Argument list too long"이란 메시지를 내며 실행되지 않는다.

``` bash
 rm /path/*
```

또는

``` bash
 rm `find /path -type f`
```

그러나, (같은 역할을 하는) 다음 명령어는 파일 개수와 상관없이 실행된다.

``` bash
 find /path -type f -print0 | xargs -0 rm
```

이 예제에서, `find`는 파일이름의 리스트를 갖는 `xargs`를 입력으로 받는다. `xargs`는 이 리스트를 세부리스트로 나누면서 각각의 리스트에대해서 `rm`을 호출한다. 이 방법은 같은 역할을 하는 다음의 명령어 보다 더 효율적이다.

``` bash
 find /path -type f -exec rm '{}' \;
```

위 명령어에서는 각각의 파일에 대해 `rm`이 호출된다.<ref> 참고로, 근래의 `find` 명령어에서는, `xargs`의 기능을 다음과 같이 대체 시킬 수 있다.

``` bash
 find /path -type f -exec rm '{}' +
```

</ref>

## 같이 보기

  - [find](https://ko.wikipedia.org/wiki/find "wikilink")

## 각주

<references />

## 외부 링크

  -
  -
  -
[분류:유닉스 텍스트 처리 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_텍스트_처리_유틸리티 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink")

1.  <http://www.gnu.org/software/coreutils/faq/coreutils-faq.html#Argument-list-too-long>