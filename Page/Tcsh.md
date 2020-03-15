> This article is converted from Wikipedia: [Tcsh](https://ko.wikipedia.org/wiki/Tcsh).


**tcsh** ("티시셸, tee-see-shell" 또는 "티셸 tee-shell" 또는 "티시에스에이치")는 [C 셸](https://ko.wikipedia.org/wiki/C_셸 "wikilink")(csh) 기반이면서 C 셸과 [호환되는](https://ko.wikipedia.org/wiki/하위_호환성 "wikilink") [유닉스 셸이다](https://ko.wikipedia.org/wiki/유닉스_셸 "wikilink"). [명령 줄 완성](https://ko.wikipedia.org/wiki/명령_줄_완성 "wikilink"), [명령 줄](https://ko.wikipedia.org/wiki/명령_줄_인터페이스 "wikilink") 편집 등의 기능이 포함된 C 셸이다. 다른 셸들과 달리 tcsh 스크립트 안에 함수를 정의할 수 없으며 사용자는 csh에서처럼 별칭(alias)을 대신 사용해야 한다. [FreeBSD](https://ko.wikipedia.org/wiki/FreeBSD "wikilink") 등의 BSD 기반 시스템을 위한 네이티브 루트 셸이다.

## 역사

`tcsh`의 t는 명령 완성 기능과 더불어 [카네기 멜런 대학교의](https://ko.wikipedia.org/wiki/카네기_멜런_대학교 "wikilink") tcsh의 개발자 켄 그리어(Ken Greer)에 영감을 준 [운영 체제](https://ko.wikipedia.org/wiki/운영_체제 "wikilink") [TENEX의](https://ko.wikipedia.org/wiki/TOPS-20 "wikilink") T에서 비롯되었다.\[1\] 그리어는 1975년 9월 자신의 코드에 Tenex 스타일의 파일 이름 완성을 구현하는 작업을 시작했으며 1981년 12월에 C 셸로의 통합을 마쳤다.\[2\] 페어차일드 A.I. 연구소의 마이크 엘리스는 1983년 9월 명령어 완성을 추가하였다.\[3\] 1983년 10월 3일 그리어는 net.sources 뉴스그룹에 소스를 게시하였다.\[4\]

## 배치

초기 버전의 맥 OS X은 tcsh를 기본 셸로 포함하고 있으나 새로운 계정의 기본 셸은 [10.3](https://ko.wikipedia.org/wiki/맥_OS_X_팬더 "wikilink") 기준으로 [배시이다](https://ko.wikipedia.org/wiki/배시_\(유닉스_셸\) "wikilink"). (tcsh는 여전히 제공되며 운영 체제를 업그레이드한다고 하여도 기존의 모든 계정의 셸을 변경하지는 않는다) tcsh는 [FreeBSD](https://ko.wikipedia.org/wiki/FreeBSD "wikilink") 및 파생([드래곤플라이 BSD와](https://ko.wikipedia.org/wiki/드래곤플라이_BSD "wikilink") [데스크톱BSD](https://ko.wikipedia.org/wiki/데스크톱BSD "wikilink"))의 기본 루트 셸(기본 사용자 셸은 [POSIX](https://ko.wikipedia.org/wiki/POSIX "wikilink") 기반)이다.\[5\]\[6\]

## 각주

## 외부 링크

  -
  - [tcsh manual page](https://web.archive.org/web/20051029095645/http://www.tcsh.org/tcsh.html/top.html)

  - [Archive for the O'Reilly book "Using csh and tcsh"](http://www.kitebird.com/csh-tcsh-book/)

[분류:셸](https://ko.wikipedia.org/wiki/분류:셸 "wikilink") [분류:크로스 플랫폼 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_자유_소프트웨어 "wikilink") [분류:C로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C로_작성된_자유_소프트웨어 "wikilink") [분류:스크립트 언어](https://ko.wikipedia.org/wiki/분류:스크립트_언어 "wikilink") [분류:유닉스 셸](https://ko.wikipedia.org/wiki/분류:유닉스_셸 "wikilink") [분류:BSD 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:BSD_라이선스_소프트웨어 "wikilink")

1.
2.
3.
4.
5.
6.  [POSIX 2008 Shell Command Language](http://pubs.opengroup.org/onlinepubs/9699919799/xrat/V4_xcu_chap02.html)  "The System V shell was selected as the starting point for the Shell and Utilities volume of POSIX.1-2008. The BSD C shell was excluded from consideration"