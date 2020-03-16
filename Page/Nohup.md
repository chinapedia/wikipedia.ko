> This article is converted from Wikipedia: [Nohup](https://ko.wikipedia.org/wiki/Nohup).


**nohup**은 [HUP](https://ko.wikipedia.org/wiki/SIGHUP "wikilink")(hangup) 신호를 무시하도록 만드는 [POSIX](../Page/POSIX.md "wikilink") 명령어이다. HUP 신호는 전통적으로 터미널이 의존 프로세스들에게 로그아웃을 알리는 방식이다.

일반적으로 터미널로 향하는 출력은 별도로 넘겨주기 처리를 하지 않았을 경우 `nohup.out`이라는 이름의 파일로 출력된다.

## 사용

아래의 명령 중 첫 번째 항목은 백그라운드에 `abcd`라는 프로그램을 시작한다. 그 뒤 로그아웃을 하더라도 이 프로그램의 프로세스를 중단하지는 않는다.

`$ nohup abcd &`
`$ exit`

위 방법을 사용하면 로그아웃을 할 때 프로세스가 정지(stop) 신호를 내보내는 것을 막을 수 있지만 표준 입출력 파일(stdin, stdout, stderr)에 대해 입출력을 수신하면 터미널에 행(hang)이 걸리게 된다.\[1\]

nohup은 프로세스의 우선 순위를 낮추기 위해 [nice](https://ko.wikipedia.org/wiki/nice "wikilink") 명령어와 결합해서 사용할 수 있다.

`$ nohup nice abcd &`

## 행의 극복

nohup으로 백그라운드 처리된 작업들은 원격 [SSH](../Page/시큐어_셸.md "wikilink") [세션을](https://ko.wikipedia.org/wiki/로그인_세션 "wikilink") 로그오프할 때 일반적으로 이들의 종료를 막기 위해 사용된다. 이 상황에서 발생할 수 있는 또 다른 문제는 ssh가 로그오프(행)을 거부하는 것인데, 그 이유는 백그라운드 작업들에 대한 데이터 손실을 거부하기 때문이다.\[2\]\[3\] 이 문제는 3개의 모든 입출력 스트림을 [리다이렉션](../Page/리다이렉션.md "wikilink") 처리함으로써 극복할 수 있다.

`$ nohup ./myprogram > foo.out 2> foo.err < /dev/null &`

SSH 세션을 닫으면 무조건 의존 프로세스들에 HUP 신호를 보내지 않게 된다. 이는 [의사 터미널의](https://ko.wikipedia.org/wiki/의사_터미널 "wikilink") 할당 여부에 따라 달라진다.\[4\]

## 각주

## 외부 링크

  - [nohup from Solaris's man pages](https://web.archive.org/web/20061028142027/http://bama.ua.edu/cgi-bin/man-cgi?nohup+1)

[분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink")

1.
2.
3.
4.