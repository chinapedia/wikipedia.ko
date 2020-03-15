> This article is converted from Wikipedia: [Tcpdump](https://ko.wikipedia.org/wiki/Tcpdump).


**tcpdump**는 [명령 줄에서](../Page/명령_줄_인터페이스.md "wikilink") 실행하는 일반적인 [패킷 가로채기](https://ko.wikipedia.org/wiki/패킷_가로채기 "wikilink") 소프트웨어이다. 사용자가 [TCP/IP뿐](https://ko.wikipedia.org/wiki/인터넷_프로토콜_스위트 "wikilink") 아니라, 컴퓨터에 부착된 [네트워크를](https://ko.wikipedia.org/wiki/컴퓨터_네트워크 "wikilink") 통해 송수신되는 기타 패킷을 가로채고 표시할 수 있게 도와 준다. [BSD 허가서를](https://ko.wikipedia.org/wiki/BSD_허가서 "wikilink") 통해 배포되는\[1\] tcpdump는 [자유 소프트웨어이다](https://ko.wikipedia.org/wiki/자유_소프트웨어 "wikilink").

tcpdump는 [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink"), [솔라리스](https://ko.wikipedia.org/wiki/솔라리스_\(운영_체제\) "wikilink"), [BSD](https://ko.wikipedia.org/wiki/BSD "wikilink"), [맥 OS X](https://ko.wikipedia.org/wiki/맥_OS_X "wikilink"), [HP-UX](../Page/HP-UX.md "wikilink"), [AIX](https://ko.wikipedia.org/wiki/AIX_\(운영_체제\) "wikilink") 따위의 대부분의 [유닉스 계열](../Page/유닉스_계열.md "wikilink") [운영 체제에서](https://ko.wikipedia.org/wiki/운영_체제 "wikilink") 동작하며 여기서 [libpcap](https://ko.wikipedia.org/wiki/libpcap "wikilink") 라이브러리를 사용하여 패킷을 포획한다. [윈도용](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") tcpdump 이식판으로는 WinDump가 있으며, 이는 libpcap의 윈도 이식판인 [WinPcap을](../Page/Pcap.md "wikilink") 이용한다.

## 매개변수

`tcpdump [ -AdDefIKlLnNOpqRStuUvxX ][ -B buffer_size ][ -c count ][ -C file_size ][ -G rotate_seconds ][ -F file ][ -i interface ][ -m module ][ -M secret ][ -r file ][ -s snaplen ][ -T type ][ -w file ][ -W filecount ][ -E spi@ipaddr algo:secret,... ][ -y datalinktype ][ -z postrotate-command ][ -Z user ]`

  - `-A`: 패킷의 내용을 화면에 [ASCII로](https://ko.wikipedia.org/wiki/미국_정보_교환_표준_부호 "wikilink") 보여준다
    `-B`: 운영 체제가 캡처하는 버퍼 크기를 buffer_size로 바꾼다.
    `-c`: 주어진 수의 패킷을 받은 후 종료한다.
    `-C`: 방금 받은 패킷을 저장파일로 만들기 전에 파일이 file_size보다 큰지 체크한다. 만약 그렇다면, 현재 저장파일을 닫고 새로 하나를 연다. 저장된 파일의 이름은 -w 기호를 이용해 1부터 시작해 하나씩 늘어난다.(1,048,576 바이트가 아니라 1,000,000바이트이다)
    `-d`: 컴파일된 packet-matching code를 사람이 읽을 수 있는 표준형으로 바꾼후 멈춘다.
    `-dd`: packet-matching 코드를 C 프로그램의 일부로 표현한다.
    `-ddd`: packet-matching 코드를 십진수로 표현한다.
    `-D`: tcpdump가 패킷을 잡을 수 있는 시스템 상에 가능한 네트워크 인터페이스 목록을 출력한다. 각각의 네트워크 인터페이스에는 번호와 인터페이스 이름이 매겨져 있어야 하고 그에 해당하는 설명이 덧붙여져 있어야 한다. 이 기능은 tcpdump가 오래된 버전일 경우에 지원되지 않을 수 있다.
    `-e`: 링크 레벨 헤더를 각각 덤프라인에 출력한다.
    `-f`: 외부 IPv4 주소를 되도록 심볼(상징적)이 아닌 숫자로서 표현한다.
    `-F`: 파일을 필터식(filter expression)으로 입력한다. 추가적으로 명령창에 입력된 식은 무시된다.
    `-G`: 이 옵션을 지정하면 덤프 파일을 `-w` 옵션으로 매 초마다 회전해 회전된 덤프파일을 저장한다. 저장된 파일은 -w 옵션으로 strftime으로 시간 정보가 정의 되어 이름에 포함되어야 한다. 만약 시간 형식이 저장되지 않으면 매번 새로운 파일은 원래 있던 파일에 덮어 씌워 진다. 만약 -C 옵션과 함께 쓰인다면 이름은 'file<count>'형식으로 저장된다.
    `-i`: 인터페이스를 정한다. 정해지지 않았으면 tcpdump는 시스템 인터페이스 목록에서 가장 낮은 숫자를 고른다.
    `-I`: 인터페이스를 "monitor mode"로 놓는다. 이는 IEEE 802.11 와이파이 인터페이스에서만 작동되고 몇몇 운영 체제에서만 지원된다.

## 같이 보기

  - [pcap](https://ko.wikipedia.org/wiki/pcap "wikilink") (libpcap)

## 각주

<references />

## 외부 링크

  - (lipbcap 포함)

  -
[분류:윈도우 소프트웨어](https://ko.wikipedia.org/wiki/분류:윈도우_소프트웨어 "wikilink") [분류:크로스 플랫폼 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_소프트웨어 "wikilink") [분류:네트워크 분석기](https://ko.wikipedia.org/wiki/분류:네트워크_분석기 "wikilink") [분류:C로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C로_작성된_자유_소프트웨어 "wikilink") [분류:크로스 플랫폼 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_자유_소프트웨어 "wikilink")

1.