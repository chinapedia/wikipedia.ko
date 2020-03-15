> This article is converted from Wikipedia: [Raw ](https://ko.wikipedia.org/wiki/Raw_).


**raw 소켓**은 어느 특정한 프로토콜 용의 [전송 계층](https://ko.wikipedia.org/wiki/전송_계층 "wikilink") 포매팅 없이 [인터넷 프로토콜](https://ko.wikipedia.org/wiki/인터넷_프로토콜 "wikilink") [패킷](https://ko.wikipedia.org/wiki/패킷 "wikilink")을 직접적으로 주고 받게 해주는 [인터넷 소켓이다](https://ko.wikipedia.org/wiki/인터넷_소켓 "wikilink").

## 개요

*standard sockets*에서 [페이로드](https://ko.wikipedia.org/wiki/페이로드 "wikilink")는 선택된 전송 계층 프로토콜에 따라 자동으로 캡슐화되며 소켓 사용자는 페이로드와 함께 브로드캐스트되는 프로토콜 헤더의 존재를 알지 못한다. raw 소켓을 읽는 경우 보통 헤더들도 포함된다. raw 소켓에서 패킷을 전달할 때 헤더를 자동으로 추가할지 여부는 필수적이지 않다.

Raw 소켓들은 [nmap](https://ko.wikipedia.org/wiki/nmap "wikilink") 같은 보안 관련 애플리케이션에서 사용된다. raw 소켓을 사용한 다른 가능한 방식으로 [사용자 공간에서](https://ko.wikipedia.org/wiki/사용자_공간 "wikilink") 새로운 전송 계층 프로토콜을 구현하는 것이 있다.\[1\] Raw 소켓들은 일반적으로 네트워크 장비에서 사용 가능하며 [인터넷 그룹 관리 프로토콜](https://ko.wikipedia.org/wiki/인터넷_그룹_관리_프로토콜 "wikilink") (IGMPv4)과 [최단 경로 우선 프로토콜](../Page/최단_경로_우선_프로토콜.md "wikilink")(OSPF), 그리고 [ICMP](https://ko.wikipedia.org/wiki/인터넷_제어_메시지_프로토콜 "wikilink") 같은 라우팅 프로토콜에서 ICMP echo request를 보내고 ICMP echo replie를 받을 때 사용된다.\[2\]

## 구현

대부분의 소켓 API들은 raw 소켓을 지원한다. [윈도우 XP는](https://ko.wikipedia.org/wiki/윈도우_XP "wikilink") 2001년 Winsock 인터페이스에 구현된 raw 소켓을 지원하였지만 3년 후 마이크로소프트는 Winsock의 raw 소켓 지원을 보안을 이유로 제한하였다.\[3\]

## 같이 보기

  - [인터넷 프로토콜](https://ko.wikipedia.org/wiki/인터넷_프로토콜 "wikilink")
  - [인터넷 프로토콜 스위트](https://ko.wikipedia.org/wiki/인터넷_프로토콜_스위트 "wikilink")
  - [IPv4 패킷 포맷](https://ko.wikipedia.org/wiki/IPv4 "wikilink")
  - [IPv6 패킷 포맷](https://ko.wikipedia.org/wiki/IPv6 "wikilink")

## 각주

## 외부 링크

  - \[<http://metacpan.org/module/Net>::RawIP Net::RawIP; module for Perl applications.\] Created by [Sergey Kolychev](https://web.archive.org/web/20050623074557/http://www.ic.al.lg.ua/~ksv/).
  - Network Programming for Microsoft Windows ()
  - [A little more info on raw sockets and Windows XP SP2 - Michael Howard's Web Log](https://web.archive.org/web/20100106225718/http://blogs.msdn.com/michael_howard/archive/2004/08/12/213611.aspx) an indication of what's actually allowed on Windows.
  - [SOCK_RAW Demystified: article describing inner workings of Raw Sockets](http://sock-raw.org/papers/sock_raw)
  - [C language examples of Linux raw sockets for IPv4 and IPv6](http://www.pdbuchan.com/rawsock/rawsock.html) - David Buchan's C language examples of IPv4 and IPv6 raw sockets for Linux.

[분류:취약점 공격](https://ko.wikipedia.org/wiki/분류:취약점_공격 "wikilink")

1.
2.
3.  Ian Griffiths for IanG on Tap. 12 August, 2004.