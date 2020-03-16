> This article is converted from Wikipedia: [Pkill](https://ko.wikipedia.org/wiki/Pkill).


**`pkill`**은 초기에 [솔라리스 7에서](../Page/솔라리스_\(운영_체제\).md "wikilink") 사용될 목적으로 만들어진 [커맨드 라인](../Page/명령_줄_인터페이스.md "wikilink") 유틸리티이다. 이것은 [리눅스](../Page/리눅스.md "wikilink")와 몇몇 [BSD](../Page/BSD.md "wikilink")들에서 재구현되었다.

[`kill`](https://ko.wikipedia.org/wiki/kill "wikilink")과 [`killall`](https://ko.wikipedia.org/wiki/killall "wikilink") 명령어 처럼, **`pkill`**은 [프로세스](../Page/프로세스.md "wikilink")에게 [시그널을](../Page/유닉스_신호.md "wikilink") 보내는데 사용된다. **`pkill`** 명령어는 확장된 [정규 표현식](https://ko.wikipedia.org/wiki/정규_표현식 "wikilink") 패턴들의 사용을 허용한다.

## 사용 예시

가장 최근에 생성된 `acroread` 프로세스 kill하기:

``` bash
pkill -n acroread
```

`acroread` 프로세스에 [USR1](../Page/유닉스_신호.md "wikilink") 시그널 보내기:

``` bash
pkill -USR1 acroread
```

## 같이 보기

  - [유닉스 명령어 목록](../Page/유닉스_명령어_목록.md "wikilink")
  - [`kill`](https://ko.wikipedia.org/wiki/kill "wikilink")`(1)`
  - [`nice`](https://ko.wikipedia.org/wiki/nice_\(유닉스\) "wikilink")`(1)`
  - [`skill`](https://ko.wikipedia.org/wiki/skill "wikilink")`(1)`, 시그널을 보내거나 프로세스 상태를 보고하는 커맨드 라인 유틸리티이지만, `pkill`이 더 자주 사용된다.
  - [`top`](https://ko.wikipedia.org/wiki/top_\(소프트웨어\) "wikilink")`(1)`
  - [`htop`](https://ko.wikipedia.org/wiki/htop "wikilink")`(1)`

## 각주

  -
  -
## 외부 링크

  - [Oracle: Man pages pgrep, pkill](http://docs.oracle.com/cd/E19253-01/816-5165/pkill-1/index.html)
  - [Oracle: How to terminate a process (pkill)](http://docs.oracle.com/cd/E19120-01/open.solaris/819-2380/spprocess-95930/index.html)

[분류:유닉스 프로세스 및 작업 관리 관련 소프트웨어](https://ko.wikipedia.org/wiki/분류:유닉스_프로세스_및_작업_관리_관련_소프트웨어 "wikilink")