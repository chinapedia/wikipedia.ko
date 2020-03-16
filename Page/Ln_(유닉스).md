> This article is converted from Wikipedia: [Ln \(\)](https://ko.wikipedia.org/wiki/Ln_\(\)).


**`ln`** 명령어는 기존 파일에 대한 [하드 링크나](../Page/하드_링크.md "wikilink") [심볼릭 링크를](../Page/심볼릭_링크.md "wikilink") 생성하기 위해 사용되는 표준 [유닉스 명령](../Page/유닉스_명령어_목록.md "wikilink") 유틸리티이다.\[1\] 하드 링크를 사용하면 여러 개의 [파일 이름을](../Page/파일_이름.md "wikilink") 동일한 [파일에](../Page/컴퓨터_파일.md "wikilink") 연결할 수 있으며, 하드 링크는 지정된 파일의 [아이노드](../Page/아이노드.md "wikilink")를 가리키게 되며 데이터는 [디스크에](../Page/하드_디스크_드라이브.md "wikilink") 저장된다. 한편, 심볼릭 링크는 [이름을](../Page/파일_이름.md "wikilink") 통해 다른 파일들을 가리키는 특수한 파일들이다.\[2\]

`ln` 명령어는 기본적으로 하드 링크를 생성하며 [명령 줄](../Page/명령_줄_인터페이스.md "wikilink") [변수](../Page/명령_줄_인터페이스.md "wikilink") `ln '-s'`로 호출할 때 심볼릭 링크를 생성한다.\[3\] 대부분의 [운영 체제는](../Page/운영_체제.md "wikilink") [디렉터리](https://ko.wikipedia.org/wiki/디렉터리 "wikilink")에 대한 하드 링크 생성을 금지하는데, 이러한 기능은 [파일 시스템의](../Page/파일_시스템.md "wikilink") 구조를 파괴하여 다른 유틸리티의 동작에 간섭을 줄 수 있기 때문이다.\[4\] 그러나 `ln` 명령어는 기존에 존재하지 않는 파일에 대한 심볼릭 링크를 생성하기 위해 사용할 수 있다.\[5\]

## 사양

[단일 유닉스 규격을](../Page/단일_유닉스_규격.md "wikilink") 준수하는 시스템 상의 `ln` 유틸리티는 SUS의 일부를 형성하는 셸과 유틸리티(XCU) 문서에 명시되어 있다.\[6\]\[7\]

이 사양은 `ln` 유틸리티를 호출하는 2가지 방법을 기술한다.\[8\] 더 구체적으로 말해,

::하나의 파일을 호출할 때 `ln` 유틸리티는 `target_file` 연산자에 의해 지정된 목적 경로에서 `source_file` 연산자에 의해 지정된 소스 파일에 대한 새로운 하드 링크(디렉터리 엔트리)를 생성한다. 그러나 `-s` 옵션이 지정되면 심볼릭 링크를 생성한다.

::

``` bash
ln [-fs] [-L|-P] source_file target_file
```

::여러 개의 파일을 호출할 때 `ln` 유틸리티는 새로운 하드 링크를 만들지만([Directory entry](http://pubs.opengroup.org/onlinepubs/9699919799/basedefs/V1_chap03.html#tag_03_130)) `-s` 옵션을 지정하면 심볼릭 링크를 생성한다. 이는 `target_dir` 연산자에 의해 명명된 기존의 디렉터리의 목적 경로에서 `source_file` 연산자에 의해 지정된 각 파일을 대상으로 한다.

::

``` bash
ln [-fs] [-L|-P] source_file_1 source_file_2 ... target_dir
```

## 같이 보기

  - [유닉스 명령어 목록](../Page/유닉스_명령어_목록.md "wikilink")

## 각주

## 외부 링크

  -
  -
  -
  -
  -
[분류:표준 유닉스 프로그램](https://ko.wikipedia.org/wiki/분류:표준_유닉스_프로그램 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.