> This article is converted from Wikipedia: [Netstat](https://ko.wikipedia.org/wiki/Netstat).


**netstat**(***net**work **stat**istics*)는 [전송 제어 프로토콜](../Page/전송_제어_프로토콜.md "wikilink"), [라우팅 테이블](../Page/라우팅_테이블.md "wikilink"), 수많은 네트워크 인터페이스([네트워크 인터페이스 컨트롤러](../Page/네트워크_인터페이스_컨트롤러.md "wikilink") 또는 [소프트웨어 정의 네트워크 인터페이스](https://ko.wikipedia.org/wiki/가상_네트워크_인터페이스 "wikilink")), 네트워크 프로토콜 통계를 위한 네트워크 연결을 보여주는 명령 줄 도구이다. [OS X](https://ko.wikipedia.org/wiki/OS_X "wikilink"), [리눅스](../Page/리눅스.md "wikilink"), [솔라리스](../Page/솔라리스_\(운영_체제\).md "wikilink"), [BSD](../Page/BSD.md "wikilink")를 포함한 [유닉스 계열](../Page/유닉스_계열.md "wikilink") [운영 체제와](../Page/운영_체제.md "wikilink") [윈도우 XP](../Page/윈도우_XP.md "wikilink"), [윈도우 비스타](../Page/윈도우_비스타.md "wikilink"), [윈도우 7](https://ko.wikipedia.org/wiki/윈도우_7 "wikilink"), [윈도우 8](../Page/윈도우_8.md "wikilink"), [윈도우 10을](../Page/윈도우_10.md "wikilink") 포함한 [윈도우 NT](../Page/윈도우_NT.md "wikilink") 기반 운영 체제에서 이용이 가능하다.

네트워크의 문제를 찾아내고 성능 측정으로서 네트워크 상의 트래픽의 양을 결정하기 위해 사용된다.\[1\]

리눅스에서 net-tools의 일부인 netstat은 시대에 뒤쳐진 것으로 간주되며, [iproute2](https://ko.wikipedia.org/wiki/iproute2 "wikilink")의 일부인 ss를 대신 사용하여야 한다.\[2\]\[3\]\[4\]\[5\]

## 예

TCP나 UDP 프로토콜에 대한 통계만 확인하려면 다음의 명령 중 하나를 입력한다:

> `netstat -sp tcp`

> `netstat -sp udp`

마이크로소프트 윈도우:

  -
    활성화된 TCP 연결과 프로세스 ID를 5초마다 확인려면 다음의 명령을 입력한다. (XP, 2003 전용. 윈도우 2000의 경우 핫픽스 사용 시 이용 가능):

> `netstat -o 5`

  -
    숫자 형태로 활성화된 TCP 연결과 프로세스 ID를 확인하려면 다음의 명령을 입력한다. (XP, 2003 전용. 윈도우 2000의 경우 핫픽스 사용 시 이용 가능):

> `netstat -no`

  -
    id *pid*와 함께 프로세스가 열고 있는 모든 포트를 확인하려면:

> `netstat -aop | grep "pid"`

  -
    열려 있는 TCP 및 UDP 연결을 숫자로 확인하고 어느 프로그램이 리눅스에서 이들을 이용하는지 계속 확인하려면:

> `sudo netstat -nutpacw`

## 각주

<references />

## 외부 링크

  - [net-tools](http://sourceforge.net/projects/net-tools/) project page on Sourceforge

  - [Ports & Services Database](http://www.iana.org/assignments/port-numbers)

  - [Microsoft TechNet Netstat article](http://technet.microsoft.com/en-us/library/bb490947.aspx) – documentation for the netstat.exe command-line program.

  - [The netstat Command (Linux)](http://www.faqs.org/docs/linux_network/x-087-2-iface.netstat.html) – a guide to using the netstat command in Linux.

  - [Security Now \#49 - The NETSTAT Command](http://www.grc.com/SecurityNow.htm#49) – podcast guide to netstat from [Security Now\!](https://ko.wikipedia.org/wiki/Security_Now! "wikilink").

  - [From linux-ip.net](http://linux-ip.net/html/tools-netstat.html) More complete description of some aspects of the output.

[분류:윈도우 명령어](https://ko.wikipedia.org/wiki/분류:윈도우_명령어 "wikilink") [분류:유닉스 네트워크 관련 소프트웨어](https://ko.wikipedia.org/wiki/분류:유닉스_네트워크_관련_소프트웨어 "wikilink") [분류:윈도우 관리](https://ko.wikipedia.org/wiki/분류:윈도우_관리 "wikilink")

1.
2.
3.
4.
5.