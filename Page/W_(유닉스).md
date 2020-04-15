> This article is converted from Wikipedia: [W \(유닉스\)](https://ko.wikipedia.org/wiki/W_\(유닉스\)).


명령어 **w**는 [유닉스 계열의](../Page/유닉스_계열.md "wikilink") 많은 [운영체제](https://ko.wikipedia.org/wiki/운영체제 "wikilink")들에서 컴퓨터에 로그인 한 모든 유저와 작업 목록을 제공한다. 예를 들면, 현재 로그인 한 유저가 하고 있는 일과 로그인 한 시간, 컴퓨터가 수행하는 모든 활동의 부하 정도 등. 이 명령어는 여러 유닉스 명령어들, [`who`](../Page/Who_\(유닉스\).md "wikilink"), [`uptime`](https://ko.wikipedia.org/wiki/uptime "wikilink"), [`ps`](../Page/Ps_\(유닉스\).md "wikilink") 의 결합된 형태이다.

## 출력 예

다음의 명령어 `w`의 출력 예제이다. 시스템마다 출력 형식이 조금씩 다르다.

``` text
$ w
 11:12am up 608 day(s), 19:56,  6 users,  load average: 0.36, 0.36, 0.37
User     tty       login@  idle  what
smithj   pts/5      8:52am       w
jonesm   pts/23    20Apr06    28 -bash
harry    pts/18     9:01am     9 pine
peterb   pts/19    21Apr06       emacs -nw html/index.html
janetmcq pts/8     10:12am 3days -csh
singh    pts/12    16Apr06  5:29 /usr/bin/perl -w perl/test/program.pl
```

## 외부 링크

  -

[분류:유닉스 사용자 관리 및 지원 관련 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_사용자_관리_및_지원_관련_유틸리티 "wikilink")