> This article is converted from Wikipedia: [IP 주소 스푸핑](https://ko.wikipedia.org/wiki/IP_주소_스푸핑).


[섬네일](https://ko.wikipedia.org/wiki/파일:IP_spoofing_en.svg "wikilink") [컴퓨터 네트워크에서](../Page/컴퓨터_네트워크.md "wikilink") **IP 주소 스푸핑**(IP address spoofing) 또는 **IP 스푸핑**(IP spoofing)은 다른 컴퓨팅 시스템인 것처럼 가장하기 위해 거짓 소스 [IP 주소로](../Page/IP_주소.md "wikilink") [인터넷 프로토콜](../Page/인터넷_프로토콜.md "wikilink")(IP) [패킷을](../Page/네트워크_패킷.md "wikilink") 만드는 일이다.\[1\]

## 배경

인터넷 네트워크와 기타 수많은 컴퓨터 네트워크를 통해 데이터를 보내기 위한 기본 프로토콜은 [인터넷 프로토콜](../Page/인터넷_프로토콜.md "wikilink")(IP)이다. 이 프로토콜은 각 IP 패킷이 반드시 패킷을 보낸이의 IP 주소를 포함하는 [헤더를](https://ko.wikipedia.org/wiki/헤더_\(컴퓨팅\) "wikilink") 포함할 것을 명시하고 있다. 근원이 되는 IP 주소는 일반적으로 패킷을 송신한 주소이지만 헤더 내의 보낸이의 주소는 변조가 가능하므로 받는이 측면에서는 다른 근원으로부터 들어온 패킷으로 보일 수 있다.

프로토콜은 컴퓨터가 소스 IP 주소의 응답을 회신할 것을 요구하며, 스푸핑은 주로 보낸이가 네트워크 응답을 받을 것을 예측하거나 응답에 신경쓰지 않는 상황일 때 이용된다.

소스 IP 주소는 보낸이의 제한된 정보만을 제공한다. 패킷 전송 시 지역, 도시의 일반적인 정보를 제공할 수 있다. 보낸이의 신상 정보나 사용된 컴퓨터에 관한 정보를 제공하지는 않는다.

## IP 스푸핑에 취약한 서비스

IP 스푸핑에 취약한 구성과 서비스는 다음과 같다:

  - RPC ([원격 프로시저 호출](../Page/원격_프로시저_호출.md "wikilink") 서비스)
  - IP 주소 인증을 사용하는 모든 서비스
  - [X 윈도 시스템](../Page/X_윈도_시스템.md "wikilink")
  - R 서비스 스위트 ([Rlogin](../Page/Rlogin.md "wikilink"), [rsh](../Page/리모트_셸.md "wikilink") 등)

## 같이 보기

  - [출구 필터링](../Page/출구_필터링.md "wikilink")
  - [입구 필터링](../Page/입구_필터링.md "wikilink")
  - [네트워크 주소 변환](../Page/네트워크_주소_변환.md "wikilink")
  - RFC 1948, Defending Against Sequence Number Attacks, May 1996
  - [라우터](../Page/라우터.md "wikilink")
  - [MAC 스푸핑](https://ko.wikipedia.org/wiki/MAC_스푸핑 "wikilink")

## 각주

## 외부 링크

  - [ANA Spoofer Project: State of IP Spoofing and Client Test](https://web.archive.org/web/20160305150334/http://spoofer.csail.mit.edu/summary.php)

[분류:인터넷 보안](https://ko.wikipedia.org/wiki/분류:인터넷_보안 "wikilink") [분류:기만](https://ko.wikipedia.org/wiki/분류:기만 "wikilink") [스푸핑](https://ko.wikipedia.org/wiki/분류:IP_주소 "wikilink")

1.