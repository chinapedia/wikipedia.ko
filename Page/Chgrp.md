> This article is converted from Wikipedia: [Chgrp](https://ko.wikipedia.org/wiki/Chgrp).


**chgrp** 명령어는 [유닉스 계열](https://ko.wikipedia.org/wiki/유닉스_계열 "wikilink") 운영 체제의 일반 사용자들이 파일 시스템 오브젝트에 연결된 그룹을 변경하는 명령이다. 파일 시스템 오브젝트에는 3가지 집합의 접근 권한이 있는데, 그 중 하나가 소유자를 위한 것이고, 다른 하나가 그룹을 위한 것이며, 나머지 하나가 기타 사용자를 위한 것이다.

## 문법

` chgrp [options]  `*`group`*`   `*`FSO`*

### 일반적으로 구현된 옵션

`-R`: 하위 디렉터리에도 적용한다.

`-v`: 변경되는 오브젝트의 이름을 출력한다.

`-f`: 오류가 발생하더라도 다른 오브젝트에 적용을 계속한다.

## 예

``` console
$ ls -l *.conf
-rw-rw-r--   1 gbeeker  wheel          3545 Nov 04 2011  prog.conf
-rw-rw-r--   1 gbeeker  wheel          3545 Nov 04 2011  prox.conf
$ chgrp staff *.conf
$ ls -l *.conf
-rw-rw-r--   1 gbeeker  staff          3545 Nov 04 2011  prog.conf
-rw-rw-r--   1 gbeeker  staff          3545 Nov 04 2011  prox.conf
```

위의 명령은 prog.conf라는 파일에 연결된 그룹을 wheel에서 staff로 변경한 것이다.

## 같이 보기

  - [chmod](https://ko.wikipedia.org/wiki/chmod "wikilink")
  - [chown](https://ko.wikipedia.org/wiki/chown "wikilink")
  - [유닉스 명령어 목록](../Page/유닉스_명령어_목록.md "wikilink")

## 외부 링크

  -
[분류:운영 체제 보안](https://ko.wikipedia.org/wiki/분류:운영_체제_보안 "wikilink") [분류:표준 유닉스 프로그램](https://ko.wikipedia.org/wiki/분류:표준_유닉스_프로그램 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink")