> This article is converted from Wikipedia: [Sort \(\)](https://ko.wikipedia.org/wiki/Sort_\(\)).


**sort**는 표준 [유닉스](../Page/유닉스.md "wikilink") [명령어](https://ko.wikipedia.org/wiki/명령어 "wikilink") 프로그램으로서 입력어들이나 인수 목록들에 기입된 모든 파일들의 연속어들을 정렬된 순서로 출력한다. 정렬하기는 입력어 각각으로부터 도출된 하나 혹은 그 이상의 정렬 키들에 바탕을 두어 시행된다. 디폴트에 의해서 전체 입력어는 정렬 키로 처리된다. 빈 공백은 디폴트 필드 구분자로서 처리되어 사용된다. **-r** 플래그는 정렬 명령을 반대로 시행한다.

## 옵션

### 정렬 옵션

\-b: 선행 공백 무시한다.

\-f: 영어 소문자를 대문자로 처리한다. 즉, 대소문자 구별안한다.

\-n: 비교 대상을 텍스트내의 숫자로 한정하여 정렬한다.

\-R: 해시의 키값 기준으로 랜덤하게 정렬한다.

\-r: 비교 결과를 역순(내림차순)으로 정렬한다.

### 확장 옵션

\-c: 파일이 정렬되어 있는지 검사한다.

\-k n: n번째 필드를 기준으로 정렬한다.

\-m: 이미 정렬된 파일들을 병합한다. (정렬은 하지 않는다.)

\-o: 표준 출력 대신 저장할 파일명을 명시한다.

\-t: 필드 구분자를 지정해준다. (기본 구분자는 공백이다.)

\-u: 정렬 후 중복된 내용을 제거한다.

## 예

### 현재 디렉터리를 파일 크기에 따라 정렬하기

`$ `[`ls`](https://ko.wikipedia.org/wiki/ls_\(유닉스\) "wikilink")` -s | `**`sort`**` -n`
`  96 Nov1.txt`
` 128 _arch_backup.lst`
` 128 _arch_backup.lst.tmp`
`1708 NMON`

### 알파벳 순서로 파일 정렬하기

`$ `[`cat`](https://ko.wikipedia.org/wiki/cat_\(유닉스\) "wikilink")` phonebook`
`Smith, Brett     555-4321`
`Doe, John        555-1234`
`Doe, Jane        555-3214`
`Avery, Cory      555-4321`
`Fogarty, Suzie   555-2314`

`$ `**`sort`**` phonebook`
`Avery, Cory      555-4321`
`Doe, Jane        555-3214`
`Doe, John        555-1234`
`Fogarty, Suzie   555-2314`
`Smith, Brett     555-4321`

### 숫자로 정렬하기

\-n 옵션은 프로그램이 숫자값에 따라 정렬되도록 만든다:

`$ `[`du`](https://ko.wikipedia.org/wiki/du_\(유닉스\) "wikilink")` /bin/* | `**`sort`**` -n`
`4       /bin/domainname`
`24      /bin/ls`
`102     /bin/sh`
`304     /bin/csh`

sort의 과거 버전에서는, +1 옵션은 프로그램 데이터의 두 번째 열을 ( +2은 세 번째 열을 정렬하고 나머지도 이와 같은 식으로) 정렬되도록 한다. 이것이 더 이상 지속되지 않는 경우, 대신 -k 옵션을 사용하여 같은 일을 한다. (주의 : "-k2"는 두 번째 열에 대한 것이다):

`$ `[`cat`](https://ko.wikipedia.org/wiki/cat_\(유닉스\) "wikilink")` zipcode`
`Adam  12345`
`Bob   34567`
`Joe   56789`
`Sam   45678`
`Wendy 23456`

`$ `**`sort`**` -nk 2 zipcode`
`Adam  12345`
`Wendy 23456`
`Bob   34567`
`Sam   45678`
`Joe   56789`

### 파이프로 한정된 파일 정렬하기

`$ `**`sort`**` -t':' -k2 zipcode`
`Adam|12345`
`Wendy|23456`
`Bob|34567`
`Sam|45678`
`Joe|56789`

### 반대로 정렬하기

\-r 옵션은 단순히 정렬하기 순서를 반대로 뒤집는다:

`$ `**`sort`**` -nrk 2 zipcode`
`Joe   56789`
`Sam   45678`
`Bob   34567`
`Wendy 23456`
`Adam  12345`

## 같이 보기

  - [원문 페이지 대조](https://ko.wikipedia.org/wiki/원문_페이지_대조 "wikilink")
  - [유닉스 명령어](https://ko.wikipedia.org/wiki/유닉스_명령어 "wikilink")

## 외부 링크

  -
  - [Softpanorama Unix sort page](http://softpanorama.org/Tools/sort.shtml)

  - [Online interface to the *sort* program](https://web.archive.org/web/20081205030217/http://www.iconv.com/sort.htm)

[분류:유닉스 텍스트 처리 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_텍스트_처리_유틸리티 "wikilink") [분류:정렬 알고리즘](https://ko.wikipedia.org/wiki/분류:정렬_알고리즘 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink")