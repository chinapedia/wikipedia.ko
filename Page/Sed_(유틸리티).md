> This article is converted from Wikipedia: [Sed \(유틸리티\)](https://ko.wikipedia.org/wiki/Sed_\(유틸리티\)).


**sed**(*stream editor*)는 [유닉스](../Page/유닉스.md "wikilink")에서 텍스트를 분해하거나 변환하기 위한 프로그램이다. sed는 [벨 연구소의](../Page/벨_연구소.md "wikilink") [리 E. 맥마흔이](https://ko.wikipedia.org/wiki/리_E._맥마흔 "wikilink") 1973년부터 1974년까지 개발하였고, 현재 유닉스 등의 여러가지 운영 체제에서 사용 가능하다.

## 역사

[버전 7 유닉스에서](https://ko.wikipedia.org/wiki/버전_7_유닉스 "wikilink") 처음 등장한 sed는 데이터 파일의 명령 줄 처리를 위해 개발된 초기 유닉스 명령어들 가운데 하나이다. 대중적인 [grep](https://ko.wikipedia.org/wiki/grep "wikilink") 명령어의 뒤를 자연스럽게 이을 정도로 발전하였다.\[1\] 원래는 치환을 목적으로 한 grep(g/re/p)의 상이형인 "g/re/s"이었다.\[2\] 개별 명령어를 위해 추가적인 특수 목적의 프로그램들이 등장할 것으로 예견하면서 맥마흔은 범용 목적의 라인 지향 스트림 편집기를 작성하였으며, 이것이 sed로 되었다.\[3\]

## 사용법

### 치환 명령어

다음의 예는 sed의 가장 일반적인 치환의 예이다. 이 사용법은 실제로 sed의 원래 동기와 부합한다:\[4\]

``` bash
sed 's/regexp/replacement/g' inputFileName > outputFileName
```

### 기타 sed 명령어

치환 외에도 25개의 sed 명령을 사용하여 다른 형태의 단순한 처리가 가능하다. 이를테면, 다음의 경우 d 명령어를 사용하여 비어있거나 공백만 포함하는 줄을 삭제한다:

``` bash
sed '/^ *$/d' inputFileName
```

### 필터로서의 사용

유닉스에서 sed는 [파이프](../Page/파이프_\(유닉스\).md "wikilink") 안에 [필터로](https://ko.wikipedia.org/wiki/필터_\(소프트웨어\) "wikilink") 종종 사용된다:

``` bash
generateData | sed 's/x/y/g'
```

즉, "generateData"와 같은 프로그램은 데이터를 만든 다음 x를 y로 대체하는 사소한 변경을 취한다.

  - 예 :

<!-- end list -->

``` console
$ echo xyz xyz | sed 's/x/y/g'
yyz yyz
```

### 파일 기반 sed 스크립트

한 줄에 하나의 명령으로 여러 sed 명령을 `subst.sed`와 같은 스크립트 파일 안에 넣으면 유용할 수 있으며 `-f` 옵션을 사용하면 파일로부터 `s/x/y/g`와 같은 명령을 실행할 수 있다.

``` bash
sed -f subst.sed inputFileName > outputFileName
```

### 수정 편집

GNU sed에 도입된 `-i` 옵션을 사용하면 파일의 직접 수정을 가능케 한다. 이를테면 다음과 같다:

``` bash
sed -i 's/abc/def/' fileName
```

## 같이 보기

  - [AWK](../Page/AWK.md "wikilink")

## 각주

## 외부 링크

  -
[분류:스크립트 언어](https://ko.wikipedia.org/wiki/분류:스크립트_언어 "wikilink")

1.
2.
3.
4.