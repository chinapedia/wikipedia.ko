> This article is converted from Wikipedia: [Ps \(\)](https://ko.wikipedia.org/wiki/Ps_\(\)).


대부분의 [유닉스 계통](https://ko.wikipedia.org/wiki/유닉스_계통 "wikilink") 운영 체제에서 **ps** 프로그램은 현재 실행되고 있는 [프로세스](../Page/프로세스.md "wikilink")들을 표시한다. [top라는](../Page/Top_\(소프트웨어\).md "wikilink") 이름의 관련 유닉스 유틸리티는 실행 중인 프로세스들의 실시간 보기를 제공한다.

## 예제들

``` console
tux:~$ ps
  PID TTY          TIME CMD
 7431 pts/0    00:00:00 su
 7434 pts/0    00:00:00 bash
18585 pts/0    00:00:00 ps
```

[grep](https://ko.wikipedia.org/wiki/grep "wikilink")명령어와 함께 사용하여, 특정 프로세스의 프로세스 id 같은 정보를 알아볼 수 있다.

``` console
tux:~$ ps -A | grep firefox-bin
11778 ?        02:40:08 firefox-bin
11779 ?        00:00:00 firefox-bin
```

## 옵션

ps는 다양한 옵션이 있다. [단일 유닉스 규격](../Page/단일_유닉스_규격.md "wikilink") 표준을 지원하는 [운영 체제에서](https://ko.wikipedia.org/wiki/운영_체제 "wikilink") ps는 일반적으로 **-ef** 옵션과 함께 시행된다. **-ef**에서 "-e"는 모든(**e**very) 프로세스를 선별하고 "-f"는 완전한("**f**ull") 출력 포맷을 선택한다. 이 외 자주 사용하는 옵션으로 **-l**이 있으며, 이는 긴("**l**ong") 출력 포맷을 지정한다.

[BSD](https://ko.wikipedia.org/wiki/BSD "wikilink")로부터 유래된 대부분의 시스템들은 역사상의 갈등들 때문에 POSIX와 UNIX 표준 옵션을 사용하지 않는다. (예를 들어 "e"나 "-e" 옵션은 [환경 변수들을](../Page/환경_변수.md "wikilink") 표시한다). 이러한 시스템들에서 ps는 일반적으로 비표준 옵션 **aux**로 실행한다. **aux**에서 "a"는 모든 프로세스를 열거하며, 이것은 다른 사용자들의 프로세스도 포함된다. "x"는 통제하는 터미널 없이 모든 프로세스들을 열거하고 "u"는 각각의 프로세스에 대하여 통제하는 사용자를 추가한다. 이러한 신택스를 사용하는 경우 최대 호환성을 위하여 "aux" 앞에 "-"가 없음을 주의하라. 또한 모든 변수들을 포함하여 프로세스에 대한 완벽한 정보를 위한 "ps auxwww"와 같이 aux 뒤에 'www'를 추가할 수 있다.

## 함께 보기

  - [`tasklist`](https://ko.wikipedia.org/wiki/tasklist_\(윈도\) "wikilink")
  - [`top`](https://ko.wikipedia.org/wiki/top_\(소프트웨어\) "wikilink")
  - [procps](https://ko.wikipedia.org/wiki/procps "wikilink")
  - [`pstree`](https://ko.wikipedia.org/wiki/pstree "wikilink")
  - [`pgrep`](https://ko.wikipedia.org/wiki/pgrep "wikilink")

## 외부 링크

  -

  -

  -
  - [The ps Command](http://www.linfo.org/ps.html) - by The Linux Information Project (LINFO)

[분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink") [분류:유닉스 프로세스 및 작업 관리 관련 소프트웨어](https://ko.wikipedia.org/wiki/분류:유닉스_프로세스_및_작업_관리_관련_소프트웨어 "wikilink")