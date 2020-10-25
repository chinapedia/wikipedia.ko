> This article is converted from Wikipedia: [MX 레코드](https://ko.wikipedia.org/wiki/MX_레코드).


**메일 익스체인저 레코드**(, MX 레코드, MX record)는 인증되고 유효성이 확인된 [도메인 네임 시스템의](../Page/도메인_네임_시스템.md "wikilink") [리소스 레코드의](https://ko.wikipedia.org/wiki/리소스_레코드 "wikilink") 일종으로, 수신자의 도메인 중간에 [이메일](https://ko.wikipedia.org/wiki/이메일 "wikilink") 메시지 수용을 책임지는 [메일 서버](https://ko.wikipedia.org/wiki/메일_서버 "wikilink"), 또 여러 메일 서버를 이용할 수 있을 경우 메일 전달 우선순위 제어에 사용되는 선호 값을 규정한다. 도메인 네임의 MX 레코드 집합은 이메일이 어떻게 [간이 우편 전송 프로토콜](../Page/간이_우편_전송_프로토콜.md "wikilink")(SMTP)로 라우팅되는 것이 좋을지를 규정한다.

## 개요

리소스 레코드는 도메인 네임 시스템(DNS)의 기초적인 정보 요소이다. MX 레코드는 그것들 가운데 하나이며 도메인 하나는 아래와 같이 하나 이상의 것들을 포함할 수 있다:

    Domain          TTL   Class    Type  Priority      Host
    example.com.        1936    IN  MX  10         onemail.example.com.
    example.com.        1936    IN  MX  10         twomail.example.com.

MX 레코드의 특징적인 페이로드 정보는 위 "Priority"라는 레이블에 보이는 선호값, 그리고 메일서버의 도메인 이름("Host")의 도메인 이름이다.

## 표준 문서

  - RFC 1035 (1987), *Domain Names - Implementation and Specification*
  - RFC 1912 (1996), *Common DNS Operational and Configuration Errors*
  - RFC 5321 (2008), *Simple Mail Transfer Protocol*
  - RFC 7505 (2015), *A "Null MX" No Service Resource Record for Domains That Accept No Mail*

구식:

  - RFC 2821 (2001), *Simple Mail Transfer Protocol* (obsoleted by *RFC-5321*)
  - RFC 974 (1986), *Mail Routing and the Domain System* (obsoleted by RFC-5321)

## 같이 보기

  - [SRV 레코드](https://ko.wikipedia.org/wiki/SRV_레코드 "wikilink")

[분류:DNS 레코드 유형](https://ko.wikipedia.org/wiki/분류:DNS_레코드_유형 "wikilink") [분류:전자 우편](https://ko.wikipedia.org/wiki/분류:전자_우편 "wikilink")