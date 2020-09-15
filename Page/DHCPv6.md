> This article is converted from Wikipedia: [DHCPv6](https://ko.wikipedia.org/wiki/DHCPv6).


**DHCPv6**(Dynamic Host Configuration Protocol 버전 6)은 IPv6 네트워크에서 작동하는 데 필요한 IP 주소, IP 접두사 및 기타 구성 데이터를 사용하여 IPv6 (Internet Protocol version 6) 호스트를 구성하기 하는데 이용가능한 네트워크 프로토콜이다. IPv4 용 동적 호스트 구성 프로토콜 (DHCP) 과 동일한 기능을 하는 IPv6 에서 사용가능한 프로토클이다. 관련 표준은 RFC 3315 에 명시되어 있다. \[1\]

## 기능

IPv6 호스트는 SLAAC (Stateless Address Autoconfiguration)을 사용하여 내부적으로 IP 주소를 자동 생성하거나 DHCPv6을 사용하여 구성 데이터를 할당받을 수 있는 두가지 방법이 있다.

기존의 IPv4 와 다르게 상태 비 저장 자동 구성을 사용하는 IPv6 호스트에는 IP 주소 또는 경로 이외의 정보가 필요할 수 있다. DHCPv6은 IP 주소를 구성하는 데 사용되지 않더라도 해당 정보를 수집하는 데 사용할 수 있다. DHCPv6은 DNS (Domain Name System) 서버의 주소로 호스트를 구성하는 데 필요하지 않다. 이유는 해당되는 호스트는 Stateless Autoconfiguration의 자체적인 메커니즘 인 Neighbor Discovery Protocol을 사용하여 구성 할 수 있기 때문이다.

## 활용

주거 네트워크 용 라우터와 같은 많은 IPv6 라우터는 운영자의 개입없이 자동으로 구성되어야 한다. 이러한 라우터는 단말에서 사용하는 업스트림 라우터와의 통신에 사용할 IPv6 주소뿐만 아니라 라우터의 다운 스트림 측에서 장치를 구성하는 데 사용하기위한 IPv6 접두어도 필요로 한다. DHCPv6 네트워크를 구성하는 접두사 위임또는 할당을 받는것은 이러한 라우터를 구성하는 메커니즘을 제공 한다.

## IETF 표준

  - RFC 3315, "Dynamic Host Configuration Protocol for IPv6 (DHCPv6)" - Updated by RFC 6221, RFC 4361
  - [RFC 3315bis draft](https://tools.ietf.org/html/draft-ietf-dhc-rfc3315bis), "Dynamic Host Configuration Protocol for IPv6 (DHCPv6) bis"
  - RFC 3319, "Dynamic Host Configuration Protocol (DHCPv6) Options for Session Initiation Protocol (SIP) Servers"
  - RFC 3633, "IPv6 Prefix Options for Dynamic Host Configuration Protocol (DHCP) version 6"
  - RFC 3646, "DNS Configuration options for Dynamic Host Configuration Protocol for IPv6 (DHCPv6)"
  - RFC 3736, "Stateless Dynamic Host Configuration Protocol (DHCP) Service for IPv6"
  - RFC 4704, "The Dynamic Host Configuration Protocol for IPv6 (DHCPv6) Client Fully Qualified Domain Name (FQDN) Option"
  - RFC 5007, "DHCPv6 Leasequery"
  - RFC 6221, "Lightweight DHCPv6 Relay Agent" (LDRA) - Updates RFC 3315, Errata
  - RFC 6355, "Definition of the UUID-Based DHCPv6 Unique Identifier (DUID-UUID)"
  - RFC 6939, "Client Link-Layer Address Option in DHCPv6"

## 같이 보기

  - [DHCP](https://ko.wikipedia.org/wiki/DHCP "wikilink")

## 각주

[분류:IPv6](https://ko.wikipedia.org/wiki/분류:IPv6 "wikilink") [분류:응용 계층 프로토콜](https://ko.wikipedia.org/wiki/분류:응용_계층_프로토콜 "wikilink")

1.  <https://tools.ietf.org/html/rfc3315>