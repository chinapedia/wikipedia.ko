> This article is converted from Wikipedia: [Mkdir](https://ko.wikipedia.org/wiki/Mkdir).


[유닉스](https://ko.wikipedia.org/wiki/유닉스 "wikilink"), [도스](https://ko.wikipedia.org/wiki/도스 "wikilink"), [마이크로소프트 윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") [운영 체제의](https://ko.wikipedia.org/wiki/운영_체제 "wikilink") **`mkdir`** 명령어는 [디렉터리](https://ko.wikipedia.org/wiki/디렉터리 "wikilink")를 새로 만드는 데 쓰인다. 일반적으로 다음과 같이 직접 만들 수 있다.

`mkdir 디렉터리의 이름`

"디렉터리의 이름"이 실제로 사용자가 만들 디렉터리의 이름이 된다. 위와 같이 입력하면 현재의 디렉터리 안에 새로운 디렉터리가 만들어진다. 다만, 새로 만들려는 디렉터리가 이미 존재하는 경우, 디렉터리가 이미 존재한다는 오류 문구가 나타난다.

도스와 윈도 운영체제에서 이 명령어는 대개 `md`로 줄여 쓴다.

## 역사

초기 버전의 유닉스([4.1BSD](https://ko.wikipedia.org/wiki/BSD "wikilink"), 초기 버전의 [시스템 V](https://ko.wikipedia.org/wiki/시스템_V "wikilink"))에서 이 명령어가 [`setuid`](https://ko.wikipedia.org/wiki/setuid "wikilink") [루트여야](https://ko.wikipedia.org/wiki/슈퍼_사용자 "wikilink") 했다. 왜냐하면 [커널이](https://ko.wikipedia.org/wiki/커널_\(컴퓨팅\) "wikilink") `mkdir()` [syscall을](../Page/시스템_호출.md "wikilink") 가지고 있지 않았기 때문이다. 그 대신, `mknod()`로 디렉터리를 만들어 .과 .. 디렉터리 항목을 수동으로 링크하였다.

## 같이 보기

  - [`find`](https://ko.wikipedia.org/wiki/find "wikilink") 명령어

## 외부 링크

  -

  -

  - [`mkdir`의 맨페이지](http://www.linuxmanpages.com/man1/mkdir.1.php)

[분류:윈도우 명령어](https://ko.wikipedia.org/wiki/분류:윈도우_명령어 "wikilink") [분류:내부 도스 명령어](https://ko.wikipedia.org/wiki/분류:내부_도스_명령어 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink") [분류:윈도우 관리](https://ko.wikipedia.org/wiki/분류:윈도우_관리 "wikilink")