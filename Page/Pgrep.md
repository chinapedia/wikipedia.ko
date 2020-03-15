> This article is converted from Wikipedia: [Pgrep](https://ko.wikipedia.org/wiki/Pgrep).


**pgrep**은 처음에 [마이크 샤피로가](https://ko.wikipedia.org/wiki/마이크_샤피로 "wikilink") [솔라리스 7](https://ko.wikipedia.org/wiki/솔라리스_\(운영_체제\) "wikilink") 운영 체제에 사용할 목적으로 개발된 [명령 줄](https://ko.wikipedia.org/wiki/명령_줄_인터페이스 "wikilink") 유틸리티이다. 그 뒤로 [일루모스](../Page/일루모스.md "wikilink")에서 이용이 가능하게 되었으며, [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink"), [BSD](https://ko.wikipedia.org/wiki/BSD "wikilink")([DragonFly BSD](https://ko.wikipedia.org/wiki/DragonFly_BSD "wikilink"), [FreeBSD](https://ko.wikipedia.org/wiki/FreeBSD "wikilink"), [NetBSD](https://ko.wikipedia.org/wiki/NetBSD "wikilink"), [OpenBSD](https://ko.wikipedia.org/wiki/OpenBSD "wikilink"))로 재구현되었다. 확장 [정규 표현식](https://ko.wikipedia.org/wiki/정규_표현식 "wikilink") 패턴으로 모든 [프로세스](https://ko.wikipedia.org/wiki/프로세스 "wikilink")의 이름을 검색할 수 있으며 기본적으로 프로세스 ID를 반환한다.

대안으로 `pidof`(프로그램 이름으로 프로세스 ID를 찾는다)와 [`ps`](https://ko.wikipedia.org/wiki/ps_\(유닉스\) "wikilink")가 있다.

## 예

pgrep의 기본 동작(명명 태스크의 [프로세스 식별자를](../Page/프로세스_식별자.md "wikilink") 반환)은 복잡한 태스크를 단순화한다.

이는 마치 다음과 동일하다:

pgrep의 추가 기능은 그룹 alice에 속한 모든 프로세스의 프로세스 이름과 PID를 나열하는 것이다. (-l은 프로세스 ID와 프로세스 이름을 나열한다. -G는 실제 그룹 ID가 나열된 프로세스만 일치시키며 숫자나 심볼 값을 사용할 수 있다.):

``` bash
$ pgrep -l -G alice
```

매칭을 반전시킴으로써 (-v는 매칭을 반전시킨다) [root](https://ko.wikipedia.org/wiki/슈퍼유저 "wikilink") 사용자에 속하지 않은 모든 프로세스를 표시한다. (`-u euid`는 유효한 사용자 ID가 나열된 프로세스만 일치시킨다):

``` bash
$ pgrep -v -u root
```

가장 최근에 시작한 프로세스만 일치시킨다 (-n은 최근의 프로세스만 선택한다):

``` bash
$ pgrep -n                # The most recent process started
$ pgrep -n -u alice emacs # The most recent `emacs` process started by user `alice`
```

## 같이 보기

  - [유닉스 명령어 목록](../Page/유닉스_명령어_목록.md "wikilink")
  - [`pidof`](https://ko.wikipedia.org/wiki/pidof "wikilink")
  - [`Pkill`](../Page/Pkill.md "wikilink")
  - [`ps`](https://ko.wikipedia.org/wiki/Ps_\(유닉스\) "wikilink")
  - [`Grep`](https://ko.wikipedia.org/wiki/Grep "wikilink")

## 각주

  -
  -
[분류:유닉스 프로세스 및 작업 관리 관련 소프트웨어](https://ko.wikipedia.org/wiki/분류:유닉스_프로세스_및_작업_관리_관련_소프트웨어 "wikilink")