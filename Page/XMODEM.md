> This article is converted from Wikipedia: [XMODEM](https://ko.wikipedia.org/wiki/XMODEM).


**XMODEM**은 [워드 크리스텐슨](https://ko.wikipedia.org/wiki/워드_크리스텐슨 "wikilink")(Ward Christensen)이 1977년 자신의 **MODEM.ASM** [단말 에뮬레이터에](https://ko.wikipedia.org/wiki/단말_에뮬레이터 "wikilink") 사용할 목적으로 빠른 [해킹으로](https://ko.wikipedia.org/wiki/해커 "wikilink") 개발된 단순 [파일 전송](https://ko.wikipedia.org/wiki/파일_전송 "wikilink") 프로토콜이다. 사용자들은 양측이 MODEM을 사용하는 경우 컴퓨터 간 파일을 전송할 수 있게 허용하였다. 케이스 피터슨(Keith Petersen)은 "조용한 모드"(quiet mode)를 무조건 활성화시키는 사소한 업데이트를 진행하였는데 그 결과 XMODEM이 탄생하게 되었다.\[1\]

XMODEM은 초기 [전자 게시판](https://ko.wikipedia.org/wiki/전자_게시판 "wikilink")(BBS) 시장에서 큰 인기를 끌었는데, 이는 대체적으로 구현이 매우 단순하였기 때문이었다. 한편으로는 상당히 비효율적이어서 모뎀 속도가 증가될 때 이러한 문제로 인해 성능을 개선하거나 프로토콜의 다른 문제를 해결하기 위해 수많은 XMODEM 수정판이 개발되었다. 크리스텐슨은 자신의 오리지널 XMODEM이 "컴퓨터 역사상 가장 많이 수정된 하나의 프로그램"이 될 것이라 생각하였다.\[2\] Chuck Forsberg는 자신의 [YMODEM](https://ko.wikipedia.org/wiki/YMODEM "wikilink") 프로토콜에 수많은 수정사항을 집약했지만 구현을 잘 하지 못하여 나중에 나올 자신의 [Z모뎀](https://ko.wikipedia.org/wiki/Z모뎀 "wikilink") 프로토콜에 재병합되기 전까지는 추가적인 균열이 발생되었다.

대부분의 파일 전송 프로토콜과 같이 XMODEM은 원래의 데이터를 일련의 [패킷](https://ko.wikipedia.org/wiki/패킷 "wikilink")으로 쪼개어 수신자에게 보내며 여기에 추가 정보를 담고 있어서 수신자가 어느 패킷을 올바르게 받았는지를 결정할 수 있게 한다.

## 패킷 구조

오리지널 XMODEM은 128바이트 데이터 패킷을 사용하였으며, 이는 [CP/M](https://ko.wikipedia.org/wiki/CP/M "wikilink") [플로피 디스크에](https://ko.wikipedia.org/wiki/플로피_디스크 "wikilink") 사용된 기본 블록 크기와 동일하다.

## XMODEM-CRC

오리지널 프로토콜에 사용된 체크섬은 극히 단순했으며 패킷 내 오류는 눈치채지 못할 수 있었다. 이로 인해 John Byrns는 **XMODEM-CRC**를 도입하게 되었고,\[3\]\[4\] 이는 8비트 체크섬 대신 16비트 [CRC를](https://ko.wikipedia.org/wiki/순환_중복_검사 "wikilink") 사용한다. CRC는 패킷 내 데이터뿐 아니라 위치까지 인코딩하므로 체크섬이 놓칠 수 있는 비트 치환 오류를 감지할 수 있다.

## 더 높은 스루풋

송신자가 <ACK> 또는 <NAK> 메시지를 수신자로부터 받아야할 것을 XMODEM 프로토콜이 요구하기 때문에 매우 속도가 느린 경향이 있다.

이러한 문제를 해결하기 위해 수많은 새로운 버전의 XMODEM이 도입되었다.

### WXModem

**WXmodem**("Windowed Xmodem"의 준말)은 피터 보스웰(Peter Boswell)이 개발한 높은 [레이턴시](https://ko.wikipedia.org/wiki/랙 "wikilink") 데이터 링크에 최적화된 Xmodem [파일 전송](https://ko.wikipedia.org/wiki/파일_전송 "wikilink") 프로토콜의 한 종류이다.\[5\] 최대 512 [바이트](https://ko.wikipedia.org/wiki/바이트 "wikilink")의 블록 크기를 지원한다. Xmodem은 정지 및 대기 프로토콜을 사용하는 반면 WXmodem은 슬라이딩 윈도 프로토콜을 사용한다.

## 각주

## 외부 링크

  - [XMODEM / YMODEM Protocol Reference by Chuck Forsberg](http://textfiles.com/programming/ymodem.txt), October 10, 1985
  - [XMODEM / YMODEM Protocol Reference by Chuck Forsberg](http://pauillac.inria.fr/~doligez/zmodem/ymodem.txt), June 18, 1988 (document reformatted October 14, 1988) [(HTML version with text issues)](https://web.archive.org/web/20121110151951/http://www.techfest.com/hardware/modem/xymodem.htm)
  - [XMODEM / XMODEM-CRC / WXMODEM File Transfer Protocols](http://wiki.synchro.net/ref:xmodem), synchro.net
  - [Adontec XMODEM/32k and XMODEM/64k extensions](http://www.adontec.com/xmodem_e.htm), adontec.com

[분류:네트워크 프로토콜](https://ko.wikipedia.org/wiki/분류:네트워크_프로토콜 "wikilink")

1.  Ward Christensen, ["Memories"](http://www.bbsdocumentary.com/software/AAA/AAA/CBBS/memories.txt), 25 November 1992
2.
3.
4.
5.  [WXmodem 4 program and source code](https://github.com/cpeterso/wxmodem)