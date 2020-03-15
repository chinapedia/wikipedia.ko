> This article is converted from Wikipedia: [True false](https://ko.wikipedia.org/wiki/True_false).


[유닉스 계열](https://ko.wikipedia.org/wiki/유닉스_계열 "wikilink") [운영 체제에서](https://ko.wikipedia.org/wiki/운영_체제 "wikilink") **true**와 **false**는 미리 정의된 [종료 상태로](../Page/종료_상태.md "wikilink") 반환하는 기능만 하는 명령어이다. 프로그래머와 스크립트들은 종종 명령의 종료 상태를 사용하여 명령의 성공(종료 상태 0)이나 실패(0이 아님)를 평가한다. true와 false 명령어들이 명령 성공의 [논리값을](https://ko.wikipedia.org/wiki/진릿값 "wikilink") 대표하는데, 그 이유는 true는 0을 반환하고 false는 1을 반환하기 때문이다.

## 사용법

명령들은 일반적으로 [셸 스크립트의](https://ko.wikipedia.org/wiki/셸_스크립트 "wikilink") [조건문](https://ko.wikipedia.org/wiki/조건문 "wikilink")과 [루프에](https://ko.wikipedia.org/wiki/제어_흐름 "wikilink") 사용된다. 이를테면, 다음의 셸 스크립트는 중단시킬 때까지 *echo hello* 루프를 반복한다:

``` bash
while true
do
  echo hello
done
```

이 명령들은 예시에서처럼 다른 일련의 명령들의 성공 또는 실패를 무시하는데 사용할 수 있다:

``` bash
make … && false
```

[/etc/passwd에서](https://ko.wikipedia.org/wiki/passwd "wikilink") 사용자의 [로그인 셸을](https://ko.wikipedia.org/wiki/유닉스_셸 "wikilink") **`false`**로 설정하면 상호작용 셸로의 접근을 효율적으로 거부할 수 있지만 [FTP](https://ko.wikipedia.org/wiki/파일_전송_프로토콜 "wikilink") 등의 다른 서비스들에 대해서는 계정이 여전히 유효하다. (사용 가능한 경우 `/sbin/nologin`가 이 목적에 더 부합할 수 있지만, 세션을 끝내기 전에 알림을 출력한다.)

이 프로그램들은 실제 매개변수를 취하지 않는다. 대부분의 리눅스 버전에서 표준 매개변수 `--help`는 사용법 요약을 보여주며 `--version`은 프로그램 버전을 보여준다.

## 같이 보기

  - [IEFBR14](../Page/IEFBR14.md "wikilink")

## 외부 링크

  -
  -
### 매뉴얼 페이지

  - [true(1)](https://www.gnu.org/software/coreutils/manual/html_node/true-invocation.html): Do nothing, successfully – [GNU](https://ko.wikipedia.org/wiki/GNU "wikilink") [Coreutils](https://ko.wikipedia.org/wiki/Coreutils "wikilink") reference
  - [false(1)](https://www.gnu.org/software/coreutils/manual/html_node/false-invocation.html): Do nothing, unsuccessfully – [GNU](https://ko.wikipedia.org/wiki/GNU "wikilink") [Coreutils](https://ko.wikipedia.org/wiki/Coreutils "wikilink") reference
  - [true(1)](http://man.freebsd.org/true): Return true value – [FreeBSD](https://ko.wikipedia.org/wiki/FreeBSD "wikilink") manual page
  - [false(1)](http://man.freebsd.org/false): Return false value – [FreeBSD](https://ko.wikipedia.org/wiki/FreeBSD "wikilink") manual page

[분류:표준 유닉스 프로그램](https://ko.wikipedia.org/wiki/분류:표준_유닉스_프로그램 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink")