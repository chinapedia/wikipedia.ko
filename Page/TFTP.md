> This article is converted from Wikipedia: [TFTP](https://ko.wikipedia.org/wiki/TFTP).


**TFTP** (Trivial File Transfer Protocol)는 [FTP와](../Page/파일_전송_프로토콜.md "wikilink") 마찬가지로 파일을 전송하기 위한 프로토콜이지만, FTP보다 더 단순한 방식으로 파일을 전송한다. 따라서 데이터 전송 과정에서 데이터가 손실될 수 있는 등 불안정하다는 단점을 가지고 있다. 하지만 [FTP처럼](../Page/파일_전송_프로토콜.md "wikilink") 복잡한 [프로토콜을](https://ko.wikipedia.org/wiki/통신_프로토콜 "wikilink") 사용하지 않기 때문에 구현이 간단하다. [임베디드 시스템에서](../Page/임베디드_시스템.md "wikilink") [운영 체제](../Page/운영_체제.md "wikilink") 업로드로 주로 사용된다.

1981년에 처음 표준화되었다.\[1\]

## 사용 예제

    user@host:~$ tftp 192.168.1.1

    tftp> get file.txt

## 역사

TFTP는 [1980년](../Page/1980년.md "wikilink")에 처음 등장하였다.

TFTP가 매우 간단했으므로, 매우 작은 양의 [컴퓨터 메모리만을](https://ko.wikipedia.org/wiki/컴퓨터_메모리 "wikilink") 가지고도 TFTP를 구현할 수 있었다.\[2\] 따라서, TFTP는 [라우터](../Page/라우터.md "wikilink")와 같이 [자료 저장 장치가](https://ko.wikipedia.org/wiki/자료_저장_장치 "wikilink") 달려 있지 않은 컴퓨터 장치를 [시동](https://ko.wikipedia.org/wiki/시동 "wikilink")(부팅)하는 데 많이 쓰였다. TFTP는 오늘날까지도 [컴퓨터 네트워크로](https://ko.wikipedia.org/wiki/컴퓨터_네트워크 "wikilink") 물린 호스트 간에 작은 크기의 파일을 주고 받는 데 쓰인다. 네트워크 호스트나 [서버](../Page/서버.md "wikilink")를 이용한 네트워크 시동 절차를 밟는 원격 [X 윈도 시스템](../Page/X_윈도_시스템.md "wikilink") [컴퓨터 터미널이나](https://ko.wikipedia.org/wiki/컴퓨터_터미널 "wikilink") 다른 [신 클라이언트](../Page/신_클라이언트.md "wikilink") 등이 네트워크 시동을 할 경우에 널리 쓰인다.

TFTP는 더 예전에 나온 프로토콜인 [EFTP](../Page/EFTP.md "wikilink")에 기반을 두고 있다. [EFTP](../Page/EFTP.md "wikilink")는 [PARC 유니버설 패킷](https://ko.wikipedia.org/wiki/PARC_유니버설_패킷 "wikilink") [프로토콜 모음의](https://ko.wikipedia.org/wiki/프로토콜_모음 "wikilink") 일부였다. [TCP/IP](https://ko.wikipedia.org/wiki/TCP/IP "wikilink") 프로토콜 모음을 한창 개발하고 있을 때, 새로운 호스트 타입에서 가장 먼저 구현되곤 하였던 프로토콜이었다. TFTP가 매우 단순했기 때문에 구현하기가 쉬웠기 때문이었다.

RFC 1350이 나오기 이전까지의 초창기 TFTP 버전에는 매우 심각한 프로토콜 결함이 존재한다. 이 결함의 이름은 [마법사의 견습생 신드롬이라](https://ko.wikipedia.org/wiki/마법사의_견습생_신드롬 "wikilink") 었는데, 이것은 [판타지아라는](https://ko.wikipedia.org/wiki/판타지아_\(영화\) "wikilink") 영화의 [마법사의 견습생](https://ko.wikipedia.org/wiki/마법사의_견습생 "wikilink") 세그먼트의 이름을 따 이름이 붙은 것이었다.

TFTP는 4.3 BSD에서 처음으로 4.3 BSD에 포함되어 등장하였다. [맥 오에스 X](https://ko.wikipedia.org/wiki/맥_오에스_X "wikilink") 10.5 버전 이후로 [맥 오에스 X에](https://ko.wikipedia.org/wiki/맥_오에스_X "wikilink") 들어가 있다.

최근 TFTP는 [웜 (컴퓨터)에](https://ko.wikipedia.org/wiki/웜_\(컴퓨터\) "wikilink") 의해 악용되고는 한다. [블래스터 (컴퓨터 웜)](../Page/블래스터_\(컴퓨터_웜\).md "wikilink") 같은 웜들이 TFTP를 악용한다. 웜을 퍼뜨려 새로운 호스트를 감염시키는 데 TFTP를 이용한다.

## IETF 표준 문서

| RFC 번호   | 제목                                              | 게시일        | 저자             | Obsolete / Update 정보                                                            |
| -------- | ----------------------------------------------- | ---------- | -------------- | ------------------------------------------------------------------------------- |
| RFC 783  | The TFTP Protocol (Revision 1)                  | June 1981  | K. Sollins     | Obsoleted by - RFC 1350                                                         |
| RFC 906  | Bootstrap Loading using TFTP                    | June 1984  | Ross Finlayson | \-                                                                              |
| RFC 951  | Bootstrap Protocol                              | Sep.1985   | Bill Croft     | Updated by RFC 1395, RFC 1497, RFC 1532, RFC 1542, RFC 5494                     |
| RFC 1350 | The TFTP Protocol (Revision 2)                  | July 1992  | K. Sollins     | Updated by RFC 1782, RFC 1783, RFC 1784, RFC 1785, RFC 2347, RFC 2348, RFC 2349 |
| RFC 1782 | TFTP Option Extension                           | March 1995 | G. Malkin      | Obsoleted by - RFC 2347                                                         |
| RFC 2131 | Dynamic Host Configuration Protocol             | March 1997 | R. Droms       | Updated by RFC 3396, RFC 4361, RFC 5494, RFC 6842                               |
| RFC 2347 | TFTP Option Extension                           | May 1998   | G. Malkin      | \-                                                                              |
| RFC 2348 | TFTP Blocksize Option                           | May 1998   | G. Malkin      | \-                                                                              |
| RFC 2349 | TFTP Timeout Interval and Transfer Size Options | May 1998   | G. Malkin      | \-                                                                              |
| RFC 5505 | Principles of Internet Host Configuration       | May 2009   | B. Aboba       | \-                                                                              |
| RFC 7440 | TFTP Windowsize Option                          | Jan 2015   | P. Masotta     | \-                                                                              |
|          |                                                 |            |                |                                                                                 |

## 각주

<references />

[분류:인터넷 프로토콜](https://ko.wikipedia.org/wiki/분류:인터넷_프로토콜 "wikilink") [분류:인터넷 표준](https://ko.wikipedia.org/wiki/분류:인터넷_표준 "wikilink") [분류:파일 전송 프로토콜](https://ko.wikipedia.org/wiki/분류:파일_전송_프로토콜 "wikilink")

1.  RFC 783
2.  당시 사람들은 컴퓨터 메모리를 적게 쓰는 일에 큰 관심이 있었다.