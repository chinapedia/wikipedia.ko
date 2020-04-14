> This article is converted from Wikipedia: [Tail \(유닉스\)](https://ko.wikipedia.org/wiki/Tail_\(유닉스\)).


**tail**(테일)은 문서 파일이나 지정된 데이터의 마지막 몇 줄을 보여주는 데 사용하는 유닉스 및 [유닉스 계열](../Page/유닉스_계열.md "wikilink") 시스템에서의 프로그램이다.

## 구문

tail의 명령 구문은 다음과 같다.:

`tail [옵션] `<파일 이름>

`tail`은 입력된 파일 및 데이터의 마지막 10줄을 [stdout](https://ko.wikipedia.org/wiki/stdout "wikilink")(표준 출력)으로 출력하게 초기화되어 있다. 명령행에 옵션을 사용함으로써 출력될 줄의 수, 출력 단위(줄, 블록 또는 바이트) 등을 바꿀 수 있다. 다음 예는 입력된 파일의 마지막 20줄을 출력한다. :

`tail -n 20 "파일 이름"`

다음 예는 *foo*로 시작되는 모든 파일의 마지막 15바이트를 출력한다.:

`tail -c 15 `*`foo*`*

다음 예는 입력된 파일의 두 번째 줄부터 모든 줄을 보여준다. :

`tail -n +2 "파일 이름"`

(-n 옵션이 지원되지 않기에 썬 솔라리스에서는 여전히 사용되는) 예전 구문을 사용함으로써 다음 명령 구문으로 입력된 파일의 마지막 20줄과 마지막 50바이트를 볼 수 있다. :

`tail -20 "파일 이름"`
`tail -50c "파일 이름"`

그러나 이 구문은 현재 쓰이지 않고 POSIX 1003.1-2001 표준을 따르지도 않는다. 비록 현재 버전에서는 여전히 지원된다 해도 -f와 같은 다른 옵션들과 함께 사용될 때는 적용할 수 없다.

## 파일 감시

`tail`은 실시간으로 파일의 변화를 감지할 수 있게 해주는 `-f` 옵션이라는 특별한 명령행 옵션을 가지고 있다. 마지막 몇 줄을 출력하고 끝내는 것에 그치지 않고, `tail`은 그 줄들을 표시하고 파일을 감시한다. 새 줄들이 다른 프로세스에 의해 그 파일에 추가될 때, `tail`의 `-f` 옵션은 그 표시 또한 실시간으로 업데이트한다. 이 옵션은 특히 로그 파일(입출력 정보 파일)들을 감시할때 유용하다. 다음의 명령 구문은 messages라는 파일의 마지막 열줄을 보여주고 새 줄들이 추가되면 그 줄들을 추가하여 보여준다. :

`tail -f /var/adm/messages`

파일 감시를 끝내고자 한다면 Ctrl+C를 눌러 빠져나올 수 있다. 참고로 만약 어떤 명령 구문을 정기적으로 실행하여 그 결과가 변하는지 확인하고 싶을때는 [watch명령어를](https://ko.wikipedia.org/wiki/watch_\(Unix\) "wikilink") 사용하면 된다. `tail`의 `-f` 옵션은 실시간 감시라면 watch 명령어는 정기적 감시라 할 수 있다.

## 옵션

  - \-c수: 끝에서부터 지정된 수만큼의 바이트에 해당하는 정보를 보여준다.
    \-f: 파일의 크기가 바뀔 때마다 추가된 정보를 출력한다.
    \-F: 위 -f 옵션의 경우 파일 크기가 변하여 5 메가바이트 정도 되면 확장자에 숫자를 붙여 백업 파일을 생성하고, 다시 본 파일은 0 바이트부터 저장된다. 그래서 tail -f 파일 이름으로 실행 중인 명령이 멈춰버린다는 문제가 생겨 다시 실행시켜 주어야 하는 번거로움이 있다.

\-F 옵션을 사용하면 이런 다시 실행 문제 및 용량 변화로 인한 문제를 걱정하지 않아도 된다. -f 옵션때와 마찬가지로 +로 빠져나올 수 있다.

  - \-n수: 끝에서부터 지정된 수만큼의 줄을 보여준다.
    \-q: 출력 결과에서 맨 윗줄에 입력 파일 이름을 표시하지 않게 설정한다.
    \-v: -q와 반대로 출력 결과에서 맨 윗줄에 입력 파일 이름을 항상 표시해준다.
    \--help: 도움말을 보여준다.
    \--version: 버전 정보를 보여준다.

## 변형

  - [CCZE](http://freshmeat.net/redir/ccze/33590/url_homepage/ccze.html)는 출력 결과를 색으로 보여준다.
  - [pctail](http://sourceforge.net/projects/pctail/)은 Python Colorized tail의 준말로 CCZE처럼 출력 결과를 색으로 만들어준다.
  - [root-tail](https://web.archive.org/web/20080608183755/http://www.goof.com/pcg/marc/root-tail.html) [X-server](https://ko.wikipedia.org/wiki/X-server "wikilink") 기반 윈도에서 출력 결과를 보여준다.
  - [Inotail](http://distanz.ch/inotail/): 정규 tail 프로그램은 -f 옵션 사용시 새 정보가 표시될 수 있다면 1초에 한 번씩 폴링한다. Inotail은 [리눅스 커널의](../Page/리눅스_커널.md "wikilink") [inotify](https://ko.wikipedia.org/wiki/inotify "wikilink")라는 시스템하에서 파일들을 감시하는 속도를 더욱 높여준다.
  - [MultiTail](http://www.vanheusden.com/multitail/)은 로그 파일들을 색으로 표시해 줄뿐만 아니라 subwindows에 있는 terminal window를 통합, filter, scrollback, 분할도 할 수 있다. 이것은 tail, [sed](https://ko.wikipedia.org/wiki/sed "wikilink"), [watch](https://ko.wikipedia.org/wiki/watch "wikilink"), CCZE/pctail, [grep](https://ko.wikipedia.org/wiki/grep "wikilink"), [diff](https://ko.wikipedia.org/wiki/diff "wikilink"), [Beeper](http://cosoleto.free.fr/beeper/)등의 조합과 비슷하다.

## 같이 보기

  - [head](https://ko.wikipedia.org/wiki/head "wikilink")

## 외부 링크

  - [GNU Project documentation for tail](http://www.gnu.org/software/coreutils/manual/html_node/tail-invocation.html)
  - [FreeBSD documentation for tail](http://www.freebsd.org/cgi/man.cgi?query=tail&apropos=0&sektion=0&manpath=FreeBSD+5.3-RELEASE+and+Ports&format=html)
  - [tail man page](https://web.archive.org/web/20090523233558/http://www.thelinuxblog.com/linux-man-pages/1/tail)

[분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink") [분류:유닉스 텍스트 처리 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_텍스트_처리_유틸리티 "wikilink")