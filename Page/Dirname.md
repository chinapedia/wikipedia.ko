> This article is converted from Wikipedia: [Dirname](https://ko.wikipedia.org/wiki/Dirname).


**dirname**은 표준 [유닉스](../Page/유닉스.md "wikilink") [컴퓨터 프로그램이다](../Page/컴퓨터_프로그램.md "wikilink"). dirname에 [경로 이름을](../Page/경로.md "wikilink") 지정하면 마지막 슬래시(`'/'`) 문자로 시작되는 모든 글자들을 지우고 결과를 반환한다. dirname은 [SUS에](../Page/단일_유닉스_규격.md "wikilink") 기술되어 있으며 주로 [셸 스크립트에](../Page/셸_스크립트.md "wikilink") 쓰인다.

## 사용법

dirname에 대한 [SUS의](../Page/단일_유닉스_규격.md "wikilink") 용법은 다음과 같다.

    dirname 문자열

  -
    `문자열`
      -
        [경로 이름](../Page/경로.md "wikilink")

## 예

dirname은 슬래시 뒤의 부분은 모두 무시하고 경로 이름으로부터 디렉터리 경로 이름만은 반환한다.

``` console

$ dirname /home/martin/docs/base.wiki
/home/martin/docs

$ dirname /home/martin/docs/
/home/martin

$ dirname base.wiki
.

$ dirname /
/
```

## 성능

`dirname`이 오직 하나의 피연산자만을 받기 때문에 셸 스크립트의 [내부 루프](https://ko.wikipedia.org/wiki/내부_루프 "wikilink") 안에 사용하면 성능에 악영향을 미칠 수 있다. 다음과 같은 경우

``` bash
 while read file; do
     dirname "$file"
 done < some-input
```

입력의 각 줄마다 별개의 프로세스 호출을 일으킨다. 이러한 까닭에 다음과 같이 대체할 수 있고

``` bash
 echo "${file%/*}";
```

상대 경로 이름도 다루어야 한다면 다음과 같이 변경할 수 있다.

``` bash
 if [ -n "${file##*/*}" ]; then
     echo "."
 else
     echo "${file%/*}";
 fi
```

참고로, 위의 방식들은 dirname과는 다르게 슬래시를 처리한다.

## 같이 보기

  - [유닉스 명령어 목록](../Page/유닉스_명령어_목록.md "wikilink")
  - [basename](https://ko.wikipedia.org/wiki/basename "wikilink")
  - [경로](../Page/경로.md "wikilink")

## 외부 링크

  -
[분류:표준 유닉스 프로그램](https://ko.wikipedia.org/wiki/분류:표준_유닉스_프로그램 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink")