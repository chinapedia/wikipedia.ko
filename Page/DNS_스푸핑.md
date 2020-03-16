> This article is converted from Wikipedia: [DNS ](https://ko.wikipedia.org/wiki/DNS_).


**DNS 스푸핑**() 또는 **DNS 캐시 포지셔닝**()은 컴퓨터 보안 [해킹의](https://ko.wikipedia.org/wiki/보안_해커 "wikilink") 일종이며, 변질된 [도메인 네임 시스템](../Page/도메인_네임_시스템.md "wikilink") 데이터가 [DNS 리졸버](../Page/도메인_네임_시스템.md "wikilink")(DNS resolver)의 [캐시에](https://ko.wikipedia.org/wiki/네임_서버 "wikilink") 유입되어 [네임 서버가](https://ko.wikipedia.org/wiki/네임_서버 "wikilink") 유효하지 않은 결과 레코드(예: [IP 주소](../Page/IP_주소.md "wikilink"))를 반환한다. 이를 통해 공격자의 컴퓨터(또는 다른 컴퓨터)로 [공격 우회를](../Page/중간자_공격.md "wikilink") 할 수 있다.

## 도메인 네임 시스템 개요

[도메인 네임 시스템 서버가](https://ko.wikipedia.org/wiki/네임_서버 "wikilink") 사람이 읽을 수 있는 [도메인 네임](../Page/도메인_네임.md "wikilink")(예: [`Example.com`](../Page/Example.com.md "wikilink"))을 노드 간 통신 라우팅에 사용되는 숫자 [IP 주소로](../Page/IP_주소.md "wikilink") 변환한다. 일반적으로는 서버가 요청 변환을 인지하지 못하는 경우 다른 서버에 질의하여 프로세스를 [재귀](https://ko.wikipedia.org/wiki/재귀 "wikilink")적으로 계속한다. 성능 개선을 위해 서버는 일반적으로 특정 시간 동안 이러한 변환을 캐시 처리한다. 즉, 같은 변환을 위한 다른 요청을 받으면 캐시 만기가 도래하기 전까지는 다른 모든 서버에 일일이 질의할 필요 없이 응답할 수 있다.

DNS 서버가 성능 최적화를 위해 잘못된 변환과 캐시를 받으면 이는 중독(poisoned)된 것으로 간주되며 유효하지 않은 데이터를 클라이언트에 제공된다. DNS 서버가 중독된 경우 유효하지 않은 IP 주소를 반환할 수 있으며 트래픽을 다른 컴퓨터(종종 공격자의 컴퓨터)로 우회시킬 수 있다.\[1\]

## 공격 원리

사용자의 컴퓨터는 보통 컴퓨터가 사용하는 [IP 주소대신](../Page/IP_주소.md "wikilink") 사람들이 쓰기 편한 문자로 구성되어 있는 URL주소를 사용한다. 하지만 컴퓨터는 URL주소를 바로 인식할 수 없기 때문에, 사용자로부터 URL주소를 입력을 받으면 등록된 [도메인 네임 시스템의](../Page/도메인_네임_시스템.md "wikilink") 주소로 [UDP](https://ko.wikipedia.org/wiki/UDP "wikilink")프로토콜을 이용하여 질의를 보낸다.

### [중간자 공격을](../Page/중간자_공격.md "wikilink") 이용한 공격

이때 [중간자 공격을](../Page/중간자_공격.md "wikilink") 받고 있는 경우에는 사용자의 컴퓨터가 보내는 질의의 내용을 수정하여 [도메인 네임 시스템서버에](../Page/도메인_네임_시스템.md "wikilink") 전송하고, [도메인 네임 시스템서버는](../Page/도메인_네임_시스템.md "wikilink") 변경된 질의에 대한 답을 사용자의 컴퓨터로 보내고, 사용자의 컴퓨터는 질의에 나와 있는 [IP 주소를](../Page/IP_주소.md "wikilink") 이용하여 접속을 하게 된다. 이때 이미 질의가 [중간자 공격으로](../Page/중간자_공격.md "wikilink") 인해 원래의 값이 아니기 때문에 의도치 않은 곳으로 접속될 수 있다.

### 사용자의 컴퓨터에 저장된 [도메인 네임 시스템주소가](../Page/도메인_네임_시스템.md "wikilink") 변조되어있을 경우의 공격

만약 사용자의 컴퓨터에 등록되어 있는 [도메인 네임 시스템의](../Page/도메인_네임_시스템.md "wikilink") [IP 주소가](../Page/IP_주소.md "wikilink") 다른 요인으로 인해 이미 변경되어 있을 경우, 사용자의 컴퓨터가 제대로 된 질의를 보내도 이미 공격자가 지정한 서버에 질의를 보내게 되므로 의도치 않은 곳으로 접속될 가능성이 있다.

## 방어 방법

### [중간자 공격의](../Page/중간자_공격.md "wikilink") 경우

### [도메인 네임 시스템](../Page/도메인_네임_시스템.md "wikilink") 주소 변조의 경우

변조되어 있는 주소를 신뢰할 수 있는 [도메인 네임 시스템의](../Page/도메인_네임_시스템.md "wikilink") 주소로 바꿔준다.

## 같이 보기

  - [DNS 하이재킹](https://ko.wikipedia.org/wiki/DNS_하이재킹 "wikilink")
  - [파밍](https://ko.wikipedia.org/wiki/파밍 "wikilink")

## 각주

[분류:취약점 공격](https://ko.wikipedia.org/wiki/분류:취약점_공격 "wikilink") [분류:도메인 네임 시스템](https://ko.wikipedia.org/wiki/분류:도메인_네임_시스템 "wikilink") [분류:인터넷 보안](https://ko.wikipedia.org/wiki/분류:인터넷_보안 "wikilink") [분류:인터넷 도덕](https://ko.wikipedia.org/wiki/분류:인터넷_도덕 "wikilink") [분류:인터넷 서비스 제공자](https://ko.wikipedia.org/wiki/분류:인터넷_서비스_제공자 "wikilink")

1.