> This article is converted from Wikipedia: [DMARC](https://ko.wikipedia.org/wiki/DMARC).


**DMARC**(**Domain-based Message Authentication, Reporting and Conformance**)는 [이메일](https://ko.wikipedia.org/wiki/이메일 "wikilink") 인증 프로토콜이다. 이메일 도메인 소유자가 이메일 스푸핑으로 알려진 무단 사용에서 도메인을 보호할 수 있도록 설계되었다. DMARC의 구현 목적은 비즈니스 이메일 공격, [피싱](../Page/피싱.md "wikilink") 이메일, 이메일 사기 등 사이버 위협 행위에 도메인이 이용되지 않게 보호한다.

DMARC [DNS](../Page/도메인_네임_시스템.md "wikilink") 레코드가 게시되면 수신 이메일 서버는 도메인 소유자가 게시한 정책에 따라 수신 이메일을 검사한다. 이메일이 인증을 통과하면 전송되고 신뢰할 수 있다. 이메일이 검사에 통과하지 못하면 DMARC 레코드에 포함된 지침에 따라 이메일을 전송, 격리 또는 거부할 수 있다.

DMARC는 Sender Policy Framework(SPF)와 DomainKeys Identified Mail(DKIM) 두 가지 기존 메커니즘을 확장한다. 도메인의 관리자는 [DNS](../Page/도메인_네임_시스템.md "wikilink") 레코드에 정책을 게시하여 해당 도메인에서 전자 메일을 보낼 때 어떤 메커니즘(DKIM, SPF 또는 둘 다)을 사용하는지 지정할 수 있다. 최종 사용자에게 표시된 `From:` 필드를 확인하는 방법과 수신자가 실패를 처리하는 방법, 일일 보고서 전달 방식을 지정한다.

DMARC는 "Informational" 상태로 2015년 3월 12일자 RFC 7489 표준으로 정의한다.\[1\]

## 개요

DMARC 정책을 사용하면 보낸 사람의 도메인에서 이메일이 SPF 및/또는 DKIM으로 보호됨을 표시하고, 인증을 통과하지 못하는 경우 메시지를 거부하거나 격리하는 등 수신자에게 수행할 작업을 지정할 수 있다. 이 정책은 전자 메일 수신자가 인증에 성공/실패한 메시지를 보낸 사람의 도메인에 보고하는 방법도 지정할 수 있다.\[2\]

DMARC 정책은 공개 [도메인 네임 시스템](../Page/도메인_네임_시스템.md "wikilink")(DNS)에 TXT 레코드로 게시한다.

DMARC는 이메일이 스팸인지 또는 사기성인지 직접 정의하지 않고, 대신 메시지가 DKIM 또는 SPF 유효성 검사를 통과하는 것 뿐 아니라 연관성 검사를 통과할 것을 필수로 요구한다. DMARC 표준에서는 SPF나 DKIM을 통과해도 연관성이 없으면 인증이 실패할 수 있다.\[3\]

DMARC를 설정하면 적절한 발신자의 전송 성공 비율에 긍정적인 영향을 줄 수 있다.\[4\]

## 연관성

DMARC는 메일의 보낸 사람 `From:` 필드의 도메인이 다른 인증 도메인과 연관되는지 확인하는 방식으로 동작한다. SPF 또는 DKIM 연관 검사가 통과하면 DMARC 테스트가 통과한다.

연관성은 엄격하거나 느슨하게 지정할 수 있다. 엄격한 정책을 사용하면 도메인 이름이 일치해야 한다. 느슨한 정책을 사용하면, 최상위 "조직 도메인"이 일치해야 한다. 조직 도메인(Organizational Domain)은 공개 DNS 접미사 목록을 확인한 다음 DNS 레이블을 추가해서 찾는다. 예를 들어, ".com.au" 도메인 등록 기관이 존재하므로, "abcdexample.com.au"와 "example.com.au"는 동일한 조직 도메인을 가진다. 조직 도메인은 Public Suffix List에서만 파생할 수 있다.

SPF과 DKIM처럼 DMARC는 도메인 소유자, 특정 DNS 도메인을 변경할 수 있는 권한을 가진 주체라는 개념을 사용한다.

SPF는 보내는 메일 서버의 IP 주소가 SMTP `MAIL FROM` 명령에 나타나는 도메인 소유자의 승인을 받았는지 확인한다. (MAIL FROM의 전자 메일 주소는 envelope-from 또는 5321.MailFrom으로 지칭한다) DMARC는 SPF 검사 통과 외에도 5321.MailFrom 값과 5322.MailFrom 값이 연관되는지 확인한다.

DKIM을 사용하면 전자 메일 메시지의 일부를 암호로 서명할 수 있으며 서명에는 보낸 사람 필드가 반드시 포함되어야한다. DKIM-Signature 메일 헤더 내에서 `d=` (domain) 및 `s=` (selector) 태그는 DNS에서 서명의 공개 키를 조회할 주소를 지정한다. 유효한 서명은 서명자가 도메인 소유자이고 서명한 후 보낸 사람 필드가 수정되지 않았음을 보장한다. 이메일 메시지에는 여러 개의 DKIM 서명이 있을 수 있다. DMARC는 `d=` 태그의 도메인이 `From:` 헤더 필드에 명시된 발신자의 도메인과 연관되는 유효한 서명을 요구한다.

## DNS 레코드

DMARC 레코드는 `_dmarc.example.com`처럼 하위 도메인 레이블 `_dmarc`로 DNS에 게시된다.

TXT 레코드의 내용은 SPF와 DKIM 레코드와 유사한 `name=value` 태그로 구성되며 세미콜론으로 구분한다.

예시:

`"v=DMARC1;p=none;sp=quarantine;pct=100;rua=mailto:dmarcreports@example.com;"`

`v`는 버전, `p`는 정책, `sp`는 하위 도메인 정책, `pct`는 정책을 적용할 '부적합' 이메일의 비율, `rua`는 일일 보고서를 보낼 URI이다. 하위 도메인은 자체 DMARC 레코드를 게시할 수 있으므로, 수신자는 조직 도메인 레코드로 폴백하기 전에 먼저 확인해야한다.

## 보고서

DMARC는 두 가지 유형의 보고서를 생성할 수 있다. 종합 보고서는 `rua` 태그로 지정된 주소로 전송된다. 포렌식 보고서는 `ruf` 태그로 지정된 주소로 전송된다. 이 주소는 반드시 [URI](../Page/통합_자원_식별자.md "wikilink") [mailto](https://ko.wikipedia.org/wiki/mailto "wikilink") 포맷으로 지정해야한다.(예: worker@example.net) 여러 개의 보고 주소를 사용할 수 있으며 개별 주소는 콤마로 구분된 완전한 URI 형식이어야 한다.

보고서를 수신할 메일 주소는 외부 도메인에 속할 수 있다. 이 경우 보고서를 수신할 도메인은 수신 동의 의사를 나타내는 DMARC 레코드를 설정해야한다. 예를 들어, 수신 메일 시스템에서 `From: someone@sender.example` 로 표시된 메시지를 받아 보고서를 보낼 때 `ruf=mailto:some-id@thirdparty.example` 항목이 있다면, 수신 대상이 관리하는 네임 스페이스에 아래와 같은 DNS 레코드가 있는지 확인한다.

`sender.example._report._dmarc.thirdparty.example IN TXT "v=DMARC1;"`

### 종합 보고서

종합 보고서는 일반적으로 하루에 한 번 [XML](../Page/XML.md "wikilink") 파일로 전송된다. 제목에는 보고 대상 메일 메시지의 정책 게시자인 "Report Domain"과 보고서를 발행하는 주체인 "Submitter"를 포함한다. 페이로드는 보고서 발급 수신자, 보고 기간의 시작과 종료 시점(유닉스 타임 스탬프), 고유 식별자(선택)를 \! 구분자로 조합하고 압축 방식별 확장자로 구성된 긴 이름의 첨부 파일이다.\[5\]

예: `example.com!example.org!1475712000!1475798400.xml.gz`

XML 내용은 보고서의 기반이되는 정책을 포함하는 머리글과 보고서 메타 데이터로 구성되며 복수의 레코드로 이어진다. XML 스키마는 표준\[6\]의 부록 C에 정의되어 있다. DMARC 레코드는 [XSL 스타일 시트를](https://ko.wikipedia.org/wiki/XSL "wikilink") 적용하여 HTML로 직접 변환할 수 있다.

## 각주

## 외부 링크

  -
[분류:스팸 필터](https://ko.wikipedia.org/wiki/분류:스팸_필터 "wikilink")

1.
2.
3.
4.
5.
6.