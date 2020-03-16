> This article is converted from Wikipedia: [OAuth](https://ko.wikipedia.org/wiki/OAuth).


[right가](https://ko.wikipedia.org/wiki/파일:Oauth_logo.svg "wikilink") 설계함.\]\] **OAuth**는 인터넷 사용자들이 비밀번호를 제공하지 않고 다른 웹사이트 상의 자신들의 정보에 대해 웹사이트나 애플리케이션의 접근 권한을 부여할 수 있는 공통적인 수단으로서 사용되는, 접근 위임을 위한 [개방형 표준이다](../Page/개방형_표준.md "wikilink").\[1\] 이 매커니즘은 여러 기업들에 의해 사용되는데, 이를테면 아마존,\[2\] 구글, 페이스북, 마이크로소프트, 트위터가 있으며 사용자들이 타사 애플리케이션이나 웹사이트의 계정에 관한 정보를 공유할 수 있게 허용한다.

## 개요

OAuth가 사용되기 전에는 인증방식의 표준이 없었기 때문에 기존의 기본인증인 아이디와 비밀번호를 사용하였는데, 이는 보안상 취약한 구조이다.

기본인증이 아닐 경우는 각 애플리케이션들이 각자의 개발한 회사의 방법대로 사용자를 확인하였다. 예를 들면 [구글](../Page/구글.md "wikilink")의 AuthSub, AOL의 OpenAuth, 야후의 BBAuth, 아마존의 웹서비스 API 등이 있다.

OAuth는 이렇게 제각각인 인증방식을 표준화한 인증방식이다. OAuth를 이용하면 이 인증을 공유하는 애플리케이션끼리는 별도의 인증이 필요없다. 따라서 여러 애플리케이션을 통합하여 사용하는 것이 가능하게 된다.

## 역사

2006년 11월 [브래인 쿡은](https://ko.wikipedia.org/wiki/브래인_쿡 "wikilink") [트위터](../Page/트위터.md "wikilink")에 OpenID를 탑재하는 작업을 하고 있었다. 같은 시기, 소셜 북마크 사이트인 Ma.gnolia는, 회원이 OpenID를 사용하여 대시보드 위젯으로 서비스에 접속할 수 있는 인증 방법을 필요로 하고 있었다. 이에 쿡, 크리스 메시나, 래리 하프(Ma.gnolia)는 데이비드 리코던(당시 베리사인)과 만나 OpenID를 활용해 트위터나 Ma.gnolia의 API로 인증을 위임하는 방법을 논의했다. 그 결과, API 접근 위임에 대한 공개 표준이 아직 존재하지 않는다는 결론에 이르렀다.

OAuth의 인터넷 커뮤니티는 2007년 4월에 탄생하여, 소수 인원으로 새로운 공개 프로토콜의 초안을 썼다. OAuth 프로젝트를 알게 된 구글의 드위트 클린턴은 지원을 표명했다. 2007년 7월, 팀은 사양 초안을 완성시켰다. 에런 해머래해브가 가세하여 많은 협력자들의 조정을 실시하여, 보다 정식적인 사양을 작성해나갔다. 2007년 10월 3일, OAuth 코어 1.0의 최종 초안이 발표되었다.\[3\]

2008년 11월, 미네아폴리스에서 열린 제73회의 IETF 회합에서 OAuth의 비공식 회합도 열려 새로운 표준화를 향해 IETF에 OAuth 프로토콜을 제안할지를 논의했다. 회합은 성황을 이루었고 IETF에서 정식으로 OAuth 작업모임을 발족시키는 일에 폭넓은 지지를 얻을 수 있었다.

## 용어

OAuth에 관련된 용어들을 간략히 설명한다.

  - 사용자(user): 서비스 제공자와 소비자를 사용하는 계정을 가지고 있는 개인
  - 소비자(consumer): Open API를 이용하여 개발된 OAuth를 사용하여 서비스 제공자에게 접근하는 웹사이트 또는 애플리케이션
  - 서비스 제공자(service provider): OAuth를 통해 접근을 지원하는 웹 애플리케이션(Open API를 제공하는 서비스)
  - 소비자 비밀번호(consumer secret) : 서비스 제공자에서 소비자가 자신임을 인증하기 위한 키
  - 요청 토큰(request token) : 소비자가 사용자에게 접근권한을 인증받기 위해 필요한 정보가 담겨있으며 후에 접근 토큰으로 변환된다.
  - 접근 토큰(access token) : 인증 후에 사용자가 서비스 제공자가 아닌 소비자를 통해서 보호된 자원에 접근하기 위한 키를 포함한 값.

## 인증방식

OAuth인증은 소비자와 서비스 제공자 사이에서 일어나는데 이 인증 과정은 다음과 같다.\[4\]

1.  소비자가 서비스제공자에게 요청토큰을 요청한다.
2.  서비스제공자가 소비자에게 요청토큰을 발급해준다.
3.  소비자가 사용자를 서비스제공자로 이동시킨다. 여기서 사용자 인증이 수행된다.
4.  서비스제공자가 사용자를 소비자로 이동시킨다.
5.  소비자가 접근토큰을 요청한다.
6.  서비스제공자가 접근토큰을 발급한다.
7.  발급된 접근토큰을 이용하여 소비자에서 사용자 정보에 접근한다.

## OAuth와 다른 표준

### OAuth를 사용 시의 OpenID와 의사 인증

OAuth는 인증 프로토콜이 아닌, 인가 프로토콜이다.

[OpenID vs. pseudo-authentication using OAuth](https://ko.wikipedia.org/wiki/파일:OpenIDvs.Pseudo-AuthenticationusingOAuth.svg "wikilink")

## 같이 보기

  - [오픈아이디](../Page/오픈아이디.md "wikilink")

## 각주

## 외부 링크

  - The OAuth 1.0 Protocol (RFC 5849)

  - The OAuth 2.0 Authorization Framework (RFC 6749)

  - The OAuth 2.0 Authorization Framework: Bearer Token Usage (RFC 6750)

  -
[분류:인터넷 프로토콜](https://ko.wikipedia.org/wiki/분류:인터넷_프로토콜 "wikilink") [분류:컴퓨터 접근 제어](https://ko.wikipedia.org/wiki/분류:컴퓨터_접근_제어 "wikilink")

1.
2.  [Amazon & OAuth 2.0](https://login.amazon.com/)
3.
4.  <http://oauth.net/core/diagram.png>