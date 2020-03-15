> This article is converted from Wikipedia: [EFTP](https://ko.wikipedia.org/wiki/EFTP).


**EFTP**(이 줄임말에 대한 본디말로서는 여러 가지가 언급되고 있다. **Easy File Transfer Protocol**, **Ether File Transfer Protocol**, 혹은 **Experimental File Transfer Protocol**이라고도 한다.)는 매우 간단한 [컴퓨터 파일](https://ko.wikipedia.org/wiki/컴퓨터_파일 "wikilink") 전송 [프로토콜이다](https://ko.wikipedia.org/wiki/통신_프로토콜 "wikilink"). [1970년대](https://ko.wikipedia.org/wiki/1970년대 "wikilink") 후반, [제록스 파크가](https://ko.wikipedia.org/wiki/팰러앨토_연구소 "wikilink") [파크 유니버설 패킷](https://ko.wikipedia.org/wiki/파크_유니버설_패킷 "wikilink")(PUP) [프로토콜 모음을](https://ko.wikipedia.org/wiki/프로토콜_모음 "wikilink") 개발하였는데, EFTP는 그중 일부로 들어가 있다. [TCP/IP](https://ko.wikipedia.org/wiki/인터넷_프로토콜_스위트 "wikilink") 프로토콜 모음의 [TFTP](https://ko.wikipedia.org/wiki/TFTP "wikilink")에 많은 영향을 주었다.

후속 프로토콜인 TFTP와 마찬가지로, EFTP는 [신뢰성 있는 바이트 스트림](https://ko.wikipedia.org/wiki/신뢰성_있는_바이트_스트림 "wikilink") 프로토콜에 기반하고 있지 않다. 여기서 PUP의 경우에는 신뢰성 있는 바이트 스트림 프로토콜은 [바이트 스트림 프로토콜이](https://ko.wikipedia.org/wiki/바이트_스트림_프로토콜 "wikilink") 된다.) 그러한 프로토콜에 기반하는 것이 아니라 EFTP는 기본적인 [인터네트워크](https://ko.wikipedia.org/wiki/인터네트워크 "wikilink") 레이어 위에 바로 올라간다. EFTP의 초기 버전은 [이더넷](https://ko.wikipedia.org/wiki/이더넷 "wikilink") [패킷](https://ko.wikipedia.org/wiki/패킷 "wikilink") 상 위에 바로 구현되기도 하였다. TFTP와 마찬가지로 EFTP는 간단한 락-스텝(lock-step) 프로토콜이다. 어느 시점에서 관찰하면 돌아다니는 패킷은 오직 한 개뿐이며, 그 패킷이 관찰된다. 파일 전송이 끝날 때까지 계속, 어느 한 쪽 편은 다른 쪽 편으로부터 받은 패킷에 대해 각각마다 응답 패킷을 만들어 응답(reply)을 한다.

EFTP라는 프로토콜이 꽤 간단하기 때문에, 매우 작은 용량의 [컴퓨터 메모리만](https://ko.wikipedia.org/wiki/컴퓨터_메모리 "wikilink") 가지고도 구현이 가능하다. 당시에는 메모리를 적게 쓰는 것이 관건이었다. EFTP는 [제록스 알토를](https://ko.wikipedia.org/wiki/제록스_알토 "wikilink") 이더넷 상에서 네트워크 [시동](https://ko.wikipedia.org/wiki/시동 "wikilink")(부팅)을 하도록 시키는 데 이용되었다. 또한 [프린터 스풀러](https://ko.wikipedia.org/wiki/스풀 "wikilink") 혹은 [레이저 프린터](../Page/레이저_프린터.md "wikilink") 등으로 파일을 전송하는 데 이용되었다.

TFTP와는 달리, EFTP는 파일 전송 전에 파일 이름을 보내는 절차를 가지고 있지 않았다. 그러한 이유로, EFTP는 파일 이름이 필요하지 않은 곳에 쓰인다거나(프린터 [스풀](https://ko.wikipedia.org/wiki/스풀 "wikilink")링이 그 예이다.) 혹은 파일 이름을 제공하는 다른 프로토콜과 함께 쓰이곤 하였다. (부팅이 그 예이다.)

## 참고 문헌

  - John Shoch, *EFTP: A PUP-based Ether File Transfer Protocol* (Xerox PARC, Palo Alto, June 1976)
  - Ed Taft, *Spruce Protocols* (Xerox PARC, Palo Alto, June 1979)
  - Ed Taft, David Boggs, *Alto Boot Protocol* (Xerox PARC, Palo Alto, February 1979)

[분류:네트워크 파일 전송 프로토콜](https://ko.wikipedia.org/wiki/분류:네트워크_파일_전송_프로토콜 "wikilink")