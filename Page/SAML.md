> This article is converted from Wikipedia: [SAML](https://ko.wikipedia.org/wiki/SAML).


**SAML**(Security Assertion Markup Language, 샘엘\[1\])은 [인증 정보 제공자](https://ko.wikipedia.org/wiki/인증_정보_제공자 "wikilink")(identity provider)와 [서비스 제공자](https://ko.wikipedia.org/wiki/서비스_제공자 "wikilink")(service provider) 간의 [인증](../Page/인증.md "wikilink") 및 [인가](../Page/인가.md "wikilink") 데이터를 교환하기 위한 XML 기반의 [개방형 표준](../Page/개방형_표준.md "wikilink") 데이터 포맷이다. **보안 어서션 마크업 언어**\[2\], **보안 추가 마크업 언어**\[3\]라고도 한다. SAML은 [OASIS](https://ko.wikipedia.org/wiki/OASIS "wikilink") 보안 서비스 기술 위원회의 산물이다. SAML은 2001년으로 거슬러 올라가며, 최근의 주요 SAML 업데이트는 2005년에 게시되었다. 그러나 프로토콜 개선은 선택적, 추가 표준들을 통해 꾸준히 추가되어오고 있다.

SAML이 기술하는 가장 중요한 요구사항은 [웹 브라우저](../Page/웹_브라우저.md "wikilink") [통합 인증](../Page/통합_인증.md "wikilink")(SSO)이다. 통합 인증은 [인트라넷](../Page/인트라넷.md "wikilink") 수준에서 일반적이지만(이를테면 [쿠키를](../Page/HTTP_쿠키.md "wikilink") 사용하여) 인트라넷 밖으로 확장하는 것은 문제가 있으며 상호 운용 사유 기술들이 범람하게 되었다. (이 밖에 브라우저 SSO 문제를 해결하기 위한 최근의 접근은 [오픈ID 커넥트](https://ko.wikipedia.org/wiki/오픈ID_커넥트 "wikilink") 프로토콜이 있다)\[4\]

## 원리

SAML 사양은 3개의 역할을 정의한다:

1.  주체(일반적으로 사용자)
2.  [인증 정보 제공자](https://ko.wikipedia.org/wiki/인증_정보_제공자 "wikilink")(identity provider, IdP)
3.  서비스 제공자(service provider, SP)

SAML 사용 예에서 주체는 서비스를 서비스 제공자로부터 요청한다. 이 서비스 제공자는 식별 어서션(assertion)을 인증 정보 제공자로부터 요청하여 가져온다. 이 어서션(assertion)에 기초하여, 서비스 제공자는 [접근 제어](../Page/접근_제어.md "wikilink") 결정을 할 수 있다. 즉, 연결된 주체에 대해 일부 서비스를 수행할지의 여부를 결정할 수 있다.

## 버전

SAML은 V1.0 이후로 마이너 버전과 메이저 버전이 있다.

  - SAML 1.0은 2002년 11월 OASIS 표준으로 채택되었다
  - [SAML 1.1은](https://ko.wikipedia.org/wiki/SAML_1.1 "wikilink") 2003년 9월 OASIS 표준으로 승인되었다
  - [SAML 2.0은](https://ko.wikipedia.org/wiki/SAML_2.0 "wikilink") 2005년 3월 OASIS 표준으로 되었다

리버티 얼라이언스는 ID-FF(Identity Federation Framework)를 2003년 OASIS SSTC에 기여하였다:

  - ID-FF 1.1은 2003년 4월에 출시되었다
  - ID-FF 1.2는 2003년 11월에 완성되었다

## 같이 보기

  - [OAuth](../Page/OAuth.md "wikilink")

## 각주

## 외부 링크

  - [OASIS Security Services Technical Committee](http://www.oasis-open.org/committees/tc_home.php?wg_abbrev=security)
  - [The Basics of SAML](https://web.archive.org/web/20160304032626/http://www.gigya.com/blog/the-basics-of-saml/)

[분류:XML 기반 표준](https://ko.wikipedia.org/wiki/분류:XML_기반_표준 "wikilink") [분류:컴퓨터 접근 제어](https://ko.wikipedia.org/wiki/분류:컴퓨터_접근_제어 "wikilink") [분류:계정 관리](https://ko.wikipedia.org/wiki/분류:계정_관리 "wikilink")

1.
2.
3.
4.