> This article is converted from Wikipedia: [Cmp \(유닉스\)](https://ko.wikipedia.org/wiki/Cmp_\(유닉스\)).


**cmp**는 [유닉스 계열](../Page/유닉스_계열.md "wikilink") [운영 체제를](../Page/운영_체제.md "wikilink") 사용하는 [컴퓨터](../Page/컴퓨터.md "wikilink") 시스템에 대한 [명령 줄](https://ko.wikipedia.org/wiki/명령_줄 "wikilink") 유틸리티이다. 이는 모든 종류의 두 개의 파일을 비교하고 그 결과물을 [표준 출력에](https://ko.wikipedia.org/wiki/표준_출력 "wikilink") 쓴다. 기본값으로 만약 파일들이 같다면 cmp은 실행되지 않는다. 파일들이 서로 다르다면, 다른 점이 발견된 최초 지점의 [바이트](../Page/바이트.md "wikilink")와 문자열 숫자를 알려준다.

## 전환

cmp은 다음과 같은 전환들의 사용으로 인해 권한이 지정된다. (긴 버전들은 괄호 안에 있다):

  - \-b (--print-bytes) - 다른 바이트들을 출력한다.
  - \-i SKIP (--ignore-initial=SKIP) - 입력어의 최초 SKIP 바이트들을 건너뛴다.
  - \-i SKIP1:SKIP2 (--ignore-initial=SKIP1:SKIP2) - FILE1의 최초 SKIP1 바이트와 FILE2의 최초 SKIP2 바이트를 건너뛴다.
  - \-l (--verbose) - 모든 다른 바이트들의 바이트 숫자들과 가치들을 출력한다.
  - \-n LIMIT (--bytes=LIMIT) - 기껏해야 LIMIT 바이트에서 비교한다.
  - \-s (--quiet --silent) - 아무것도 출력하지 않는다; 출구 상태만을 산출한다.
  - \-v (--version) - 출력 버전 정보
  - \--help - help 파일을 출력한다.

## 반환값

  - 0 - 파일들이 동일하다
  - 1 - 파일들이 다르다
  - 2 - 접근할 수 없거나 없어진 인수

## 함께 보기

  - [파일 비교 도구의 비교](https://ko.wikipedia.org/wiki/파일_비교_도구의_비교 "wikilink") ([en](https://ko.wikipedia.org/wiki/:en:Comparison_of_file_comparison_tools "wikilink"))
  - [유닉스 명령어 목록](../Page/유닉스_명령어_목록.md "wikilink")

## 외부 링크

  -

  -

  - [*Comparing and Merging Files*: Invoking cmp](http://www.gnu.org/software/diffutils/manual/html_node/Invoking-cmp.html) The section of the manual of GNU cmp in the [diffutils](https://ko.wikipedia.org/wiki/diffutils "wikilink") [free manual](https://ko.wikipedia.org/wiki/free_manual "wikilink").

[분류:파일 비교 도구](https://ko.wikipedia.org/wiki/분류:파일_비교_도구 "wikilink") [분류:표준 유닉스 프로그램](https://ko.wikipedia.org/wiki/분류:표준_유닉스_프로그램 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink")