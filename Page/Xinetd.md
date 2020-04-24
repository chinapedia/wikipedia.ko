> This article is converted from Wikipedia: [Xinetd](https://ko.wikipedia.org/wiki/Xinetd).


**xinetd**(*extended Internet daemon*)는 [오픈 소스](../Page/오픈_소스.md "wikilink") [슈퍼 서버](https://ko.wikipedia.org/wiki/슈퍼_서버 "wikilink") [데몬으로서](../Page/데몬_\(컴퓨팅\).md "wikilink") 많은 [유닉스 계열](../Page/유닉스_계열.md "wikilink") 시스템에서 돌아가며 인터넷 기반 연결을 관리한다.

이것은 오래된 [inetd](https://ko.wikipedia.org/wiki/inetd "wikilink")의 대체로서 더 강력한 보안을 제공하며, 대부분의 현대 [리눅스 배포판에서는](../Page/리눅스_배포판.md "wikilink") 이것을 사용한다.\[1\]

## 개요

xinetd는 네트워크에 들어오는 요청을 듣고, 거기에 맞는 적절한 서비스를 실행시킨다.\[2\] 요청들은 식별자로서 [포트 번호를](https://ko.wikipedia.org/wiki/TCP_및_UDP_포트 "wikilink") 사용하여 만들어지며, 보통 요청을 다루는 다른 데몬을 실행시킨다. 이것은 특권 서비스 또는 아닌것들 둘 다를 시작시킬 때 사용될 수 있다.

xinetd는 [TCP 래퍼](../Page/TCP_래퍼.md "wikilink") [ACLs](../Page/접근_제어_목록.md "wikilink") 같은 [접근 제어](../Page/접근_제어.md "wikilink") 매커니즘과 확장된 로깅 역량 그리고 시간에 기반한 서비스 활성화 능력 등을 특징으로 갖는다. 이것은 시스템이 시작할 수 있는 서버들의 수를 제한할 수 있고, [포트 스캐너](../Page/포트_스캔.md "wikilink") 같은 것들로 부터 보호할 수 있는 매커니즘을 갖는다.

## 설정

xinetd의 기본 설정 파일은/etc/xinetd.conf 이며, 이것이 제공하는 서비스들의 설정은 /etc/xinetd.d 디렉터리에 저장된다. 각 서비스들의 설정은 보통 xinetd가 서비스를 활성화할지 안할지에 대한 제어 변경을 포함한다.

RFC 868 time server의 설정 파일 예시:

`# default: off`
`# description: An RFC 868 time server. This protocol provides a`
`# site-independent, machine readable date and time. The Time service sends back`
`# to the originating source the time in seconds since midnight on January first`
`# 1900.`
`# This is the tcp version.`
`service time`
`{`
`        disable         = yes`
`        type            = INTERNAL`
`        id              = time-stream`
`        socket_type     = stream`
`        protocol        = tcp`
`        user            = root`
`        wait            = no`
`}`

`# This is the udp version.`
`service time`
`{`
`        disable         = yes`
`        type            = INTERNAL`
`        id              = time-dgram`
`        socket_type     = dgram`
`        protocol        = udp`
`        user            = root`
`        wait            = yes`
`}`

"\#"으로 시작하는 줄은 주석문으로서 서비스에 영향을 미치지 않는다. 두 가지 서비스 버전이 있으며, 하나는 [전송 제어 프로토콜](../Page/전송_제어_프로토콜.md "wikilink") (TCP)이고 다른 하나는 [사용자 데이터그램 프로토콜](../Page/사용자_데이터그램_프로토콜.md "wikilink") (UDP)이다. 서비스의 종류와 예정된 사용법은 필요한 핵심 프로토콜을 결정한다. 간단하게, UDP는 패키지를 특정한 순서로 재정렬하거나 무결성을 보장하는 능력의 부족으로 큰 데이터 전송을 다룰 수 없지만 TCP 보다는 빠르다. TCP는 이러한 기능들을 갖지만 더 느리다.

*disable* 옵션은 서비스를 실행할 것인가 아닌가를 바꾼다. 대부분의 경우에 기본 상태는 *yes*이다. 서비스를 활성화하기 위해서는 *no*로 바꾼다.

서비스들의 *type*이 있다. 타입은 서비스가 xinetd에 의해 제공되는 경우에는 *INTERNAL,* [원격 프로시저 호출](../Page/원격_프로시저_호출.md "wikilink") (RPC)에 기반한다면 *RPC*이고 일반적으로 /etc/rpc 파일에 목록화되어 있으며, 서비스가 /etc/services나 /etc/rpc 파일에 모두 없는 경우에는 *UNLISTED*이다.

*id*는 서비스의 고유한 식별자이다.|

*socket_type*은 서비스를 통한 데이터 전송 방식을 결정한다. 3 종류가 있는데 *stream*, *dgram* 그리고 *raw*가 그것이다. 표준 프로토콜을 기반으로 하지 않는 서비스를 설정할 때는 마지막이 유용하다.

*user* 옵션을 통해 실행중인 서비스의 소유자인 사용자를 고르는게 가능해 진다. 보안 관련한 이유 때문에 [root를](https://ko.wikipedia.org/wiki/슈퍼_유저 "wikilink") 고르지 않는게 강력하게 추천된다.

*wait*가 *yes*라면 xinetd는 연결이 된 경우에 서비스를 위한 요청을 받지 않는다. 그래서 연결의 숫자는 하나가 된다. 이것은 우리가 한번에 단지 한 연결만 설정하길 원할 때 유용하다.

xinetd에는 많은 옵션들이 있다. 대부분의 리눅스 배포판에서 가능한 전체 옵션 리스트와 설명이 "man xinetd.conf" 명령어를 통해 접근 가능하다.

새로운 설정을 적용하기 위해서는 SIGHUP 신호가 반드시 xinetd 프로세스에게 전해져야 하는데, 이후 설정 파일을 다시 읽게 되기 때문이다. 이것은 다음과 같은 명령어를 통해 달성할 수 있다. `kill -SIGHUP "`[`PID`](../Page/프로세스_식별자.md "wikilink")`"`. PID는 xinetd의 실제 프로세스 식별자이다. 이것은 `pgrep xinetd` 명령어를 통해 알 수 있다.\[3\]\[4\]

## 각주

## 외부 링크

  -
  - [Source code](http://github.com/xinetd-org/xinetd)

[분류:MacOS](https://ko.wikipedia.org/wiki/분류:MacOS "wikilink") [분류:유닉스](https://ko.wikipedia.org/wiki/분류:유닉스 "wikilink") [분류:리눅스 보안 소프트웨어](https://ko.wikipedia.org/wiki/분류:리눅스_보안_소프트웨어 "wikilink")

1.
2.
3.  [리눅스 man 페이지: xinetd.conf(5)](http://linux.die.net/man/5/xinetd.conf)
4.