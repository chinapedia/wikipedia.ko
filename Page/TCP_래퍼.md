> This article is converted from Wikipedia: [TCP ](https://ko.wikipedia.org/wiki/TCP_).


**TCP 래퍼**(TCP Wrapper)는 호스트 기반 네트워킹 [ACL](https://ko.wikipedia.org/wiki/접근_제어_목록 "wikilink") 시스템으로서, [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink") 또는 [BSD](https://ko.wikipedia.org/wiki/BSD "wikilink") 같은 [운영 체제의](https://ko.wikipedia.org/wiki/운영_체제 "wikilink") 인터넷 프로토콜 서버에서 네트워크 접근을 필터링하기 위해 사용된다. 이것은 [접근 제어](https://ko.wikipedia.org/wiki/접근_제어 "wikilink") 목적을 위한 필터 역할을 하는 토큰으로서 사용되며, [호스트](https://ko.wikipedia.org/wiki/호스트 "wikilink")나 [부분망](https://ko.wikipedia.org/wiki/부분망 "wikilink") [IP 주소](https://ko.wikipedia.org/wiki/IP_주소 "wikilink"), [호스트명](https://ko.wikipedia.org/wiki/호스트명 "wikilink") 쿼리 응답을 허용한다.

타볼([tarball](https://ko.wikipedia.org/wiki/Tar_\(파일_포맷\) "wikilink"))은 **libwrap**라는 이름의 라이브러리를 포함하는데, 이것은 실제 기능을 구현한다. 초기에는 '''tcpd '''프로그램을 사용하여, 단지 각 연결이 [inetd](https://ko.wikipedia.org/wiki/inetd "wikilink") 같은 [슈퍼 서버에서](https://ko.wikipedia.org/wiki/슈퍼_서버 "wikilink") 생성된 서비스들만 *래핑* 되었다. 그러나 초기와 달리 대부분의 현재 네트워크 서비스 데몬들은 직접적으로 libwrap과 연결될 수 있다. 이것은 슈퍼 서버에서 생성될 필요 없이 동작하거나 단일 프로세스가 여러 연결들을 다루는, [데몬에](https://ko.wikipedia.org/wiki/데몬_\(컴퓨팅\) "wikilink") 의해 사용된다. 한편 오직 첫 번째 연결 시도만 이것의 ACL들에 의해 체크된다.

종종 데몬의 설정 파일에서 발견되는 호스트 접근 제어 지시자와 비교했을 때, TCP 래퍼는 [런타임](https://ko.wikipedia.org/wiki/런타임 "wikilink") ACL 재설정과(다시 로드하거나 시작할 필요가 없다) 일반적인 네트워크 관리에 대한 장점이 존재한다.

원래 [TCP](https://ko.wikipedia.org/wiki/TCP "wikilink")와 [UDP](https://ko.wikipedia.org/wiki/UDP "wikilink") 관련 서비스를 보호하기 위해 만들어졌지만, 특정한 [ICMP](https://ko.wikipedia.org/wiki/ICMP "wikilink") 패킷들에 대한 필터도 사용할 수 있다. 예를 들면 'pingd' ([사용자 공간](https://ko.wikipedia.org/wiki/사용자_공간 "wikilink") [핑](https://ko.wikipedia.org/wiki/핑 "wikilink") 요청 응답자)가 있다.

## 같이 보기

  - [도메인 이름 서비스 기반 블랙홀 목록](https://ko.wikipedia.org/wiki/도메인_이름_서비스_기반_블랙홀_목록 "wikilink")
  - [방화벽](https://ko.wikipedia.org/wiki/방화벽_\(네트워킹\) "wikilink")

## 외부 링크

  - [Softpanorama TCP Wrappers Information](http://www.softpanorama.org/Net/Network_security/TCP_wrappers/index.shtml)
  - [Howto on tcp wrapper](http://generationip.com/documentation/mini-howto/116-howto-on-tcp-wrapper)

[분류:인터넷 프로토콜 기반 네트워크 소프트웨어](https://ko.wikipedia.org/wiki/분류:인터넷_프로토콜_기반_네트워크_소프트웨어 "wikilink") [분류:자유 보안 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_보안_소프트웨어 "wikilink") [분류:BSD 소프트웨어](https://ko.wikipedia.org/wiki/분류:BSD_소프트웨어 "wikilink")