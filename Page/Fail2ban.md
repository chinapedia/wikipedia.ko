> This article is converted from Wikipedia: [Fail2ban](https://ko.wikipedia.org/wiki/Fail2ban).


**Fail2ban**은 [침입 차단 소프트웨어](https://ko.wikipedia.org/wiki/침입_차단_시스템 "wikilink") 프레임워크로서 컴퓨터 서버를 [무차별 대입 공격으로부터](https://ko.wikipedia.org/wiki/무차별_대입_공격 "wikilink") 보호한다.\[1\] [파이썬](https://ko.wikipedia.org/wiki/파이썬 "wikilink") 프로그래밍 언어로 쓰여졌으며, 패킷 제어 시스템이나 로컬에 설치된 방화벽([iptables](https://ko.wikipedia.org/wiki/iptables "wikilink") 또는 [TCP 래퍼](../Page/TCP_래퍼.md "wikilink"))과의 인터페이스를 갖는 [POSIX](https://ko.wikipedia.org/wiki/POSIX "wikilink") 시스템에서 돌아갈 수 있다.

## 기능

Fail2ban은 로그 파일들(예를 들면 `/var/log/auth.log`, `/var/log/apache/access.log` 등)의 선택된 엔트리들과 이것에 기반한 스크립트들을 모니터링함으로써 동작한다. 일반적으로 이것은 선택된 [IP 주소들](https://ko.wikipedia.org/wiki/IP_주소 "wikilink")(시스템의 보안을 위반하려는 시도를 하는)을 막는데 사용된다. 이것은 너무 많은 로그인 시도를 하거나 의도되지 않은 행동을 수행하는 어떤 호스트 IP 주소도 막을 수 있다. Fail2ban은 일반적으로 특정한 기간 이내에 차단된 호스트에 대한 차단을 풀어서 임시로 잘못 설정된 진짜 연결이 접속할 수 있게 한다. 하지만 이것을 푸는 몇 분의 시간이 보통 악의적인 접속들로 인한 플루딩을 막거나 성공적인 [사전 공격의](https://ko.wikipedia.org/wiki/사전_공격 "wikilink") 가능성을 줄이는데에는 충분하다.

Fail2ban은 문제가 되는 IP 주소가 탐지될 때마다 다중적인 행동을 취할 수 있다:\[2\] 위반자의 IP 주소를 거부하기 위한 [넷필터](../Page/넷필터.md "wikilink") 또는 PF 방화벽 규칙, [TCP 래퍼의](../Page/TCP_래퍼.md "wikilink") `hosts.deny` 테이블의 업데이트; 이메일 알림; 또는 파이썬 스크립트에 의해 수행되는 사용자 정의 행위.

표준 설정은 [아파치](https://ko.wikipedia.org/wiki/아파치_HTTP_서버 "wikilink"), [Lighttpd](https://ko.wikipedia.org/wiki/Lighttpd "wikilink"), [sshd](https://ko.wikipedia.org/wiki/시큐어_셸 "wikilink"), vsftpd, qmail, Postfix 그리고 Courier 메일 서버를 위한 필터들과 함께 제공된다.\[3\] 필터들은 파이썬 [정규표현식](https://ko.wikipedia.org/wiki/정규표현식 "wikilink")에 정의되며 관리자가 익숙한 정규 표현식으로 커스터마이즈될 수 있다. 필터와 행위의 조합은 "jail"로 알려져 있으며 악의적인 호스트들이 특정한 네트워크 서비스에 접근하는 것을 막는다. 소프트웨어와 함께 배포되는 예시들 뿐 아니라 "jail"은 로그 파일이나 접근을 생성하는 어떠한 네트워크를 위해서도 생성될 수 있다.

## 단점

  - Fail2ban는 분산 무차별 대입 공격을 방어할 수 없다.
  - [IPv6](https://ko.wikipedia.org/wiki/IPv6 "wikilink")에 대한 지원이 없다. 제공자가 자동으로 이것을 설치하면 Fail2ban은 동작하지 않을 것이다.\[4\]
  - 애플리케이션 전용 API/AGI들과 상호 작용이 없다.

## 같이 보기

  - [DenyHosts](https://ko.wikipedia.org/wiki/DenyHosts "wikilink"), 로그 기반 침입 차단 보안 툴.
  - [Stockade](https://ko.wikipedia.org/wiki/Stockade "wikilink"), 스팸에 대한 비율 제한적인 접근.
  - [OSSEC](https://ko.wikipedia.org/wiki/OSSEC "wikilink"), 오픈 소스 호스트 기반 침입 탐지 시스템.

## 각주

## 외부 링크

  - <span class="official-website" contenteditable="false"><span class="url">[공식 웹사이트](http://fail2ban.sourceforge.net/)</span></span><span class="official-website" contenteditable="false"></span>
  - [Debian popularity contest results for fail2ban](http://qa.debian.org/developer.php?popcon=fail2ban)

[분류:네트워크 보안](https://ko.wikipedia.org/wiki/분류:네트워크_보안 "wikilink") [분류:보안 소프트웨어](https://ko.wikipedia.org/wiki/분류:보안_소프트웨어 "wikilink") [분류:자유 보안 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_보안_소프트웨어 "wikilink") [분류:인터넷 프로토콜 기반 네트워크 소프트웨어](https://ko.wikipedia.org/wiki/분류:인터넷_프로토콜_기반_네트워크_소프트웨어 "wikilink") [분류:리눅스 보안 소프트웨어](https://ko.wikipedia.org/wiki/분류:리눅스_보안_소프트웨어 "wikilink") [분류:파이썬으로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:파이썬으로_작성된_자유_소프트웨어 "wikilink")

1.
2.
3.
4.