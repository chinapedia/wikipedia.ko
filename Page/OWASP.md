> This article is converted from Wikipedia: [OWASP](https://ko.wikipedia.org/wiki/OWASP).


**OWASP**(The Open Web Application Security Project)는 오픈소스 웹 애플리케이션 보안 프로젝트이다. 주로 웹에 관한 정보노출, 악성 파일 및 스크립트, 보안 취약점 등을 연구하며, 10대 웹 애플리케이션의 취약점 ([OWASP TOP 10](https://ko.wikipedia.org/wiki/OWASP_TOP_10 "wikilink"))을 발표했다.

[OWASP TOP 10은](https://ko.wikipedia.org/wiki/OWASP_TOP_10 "wikilink") 웹 애플리케이션 취약점 중에서 빈도가 많이 발생하고, 보안상 영향을 크게 줄 수 있는 것들 10가지를 선정하여 2004년, 2007년, 2010년, 2013년, 2017년을 기준으로 발표되었고, 문서가 공개되었다.

<https://web.archive.org/web/20191201191321/https://www.owasp.org/index.php/Category:OWASP_Top_Ten_Project>

## Top Ten Overview (2017)

  - A1: Injection (인젝션)
    [SQL](../Page/SQL.md "wikilink"), [OS](https://ko.wikipedia.org/wiki/OS "wikilink"), XXE(Xml eXternal Entity), [LDAP](../Page/LDAP.md "wikilink") 인젝션 취약점은 신뢰할 수 없는 데이터가 명령어나 쿼리문의 일부분으로써, 인터프리터로 보내질 때 발생한다. 공격자의 악의적인 데이터는 예상하지 못하는 명령을 실행하거나 적절한 권한 없이 데이터에 접근하도록 인터프리터를 속일 수 있다.

<!-- end list -->

  - A2: Broken Authentication (취약한 인증)
    인증과 세션 관리와 관련된 애플리케이션 기능은 정확하게 구현되어 있지 않아서, 공격자가 패스워드, 키 또는 세션 토큰을 해킹하거나 다른 구현 취약점을 공격하여 다른 사용자 계정을 일시적 또는 영구적으로 탈취하는 것을 허용한다

<!-- end list -->

  - A3: Sensitive Data Exposure (민감한 데이터 노출)
    많은 웹 애플리케이션들이 신용카드, 개인 식별 정보 및 인증 정보와 같은 중요한 데이터를 제대로 보호하지 않는다. 공격자는 신용카드 사기, 신분 도용 또는 다른 범죄를 수행하는 등 약하게 보호된 데이터를 훔치거나 변경할 수 있다. 중요 데이터가 저장 또는 전송 중이거나 브라우저와 교환하는 경우 특별히 주의하여야 하며, 암호화와 같은 보호조치를 취해야 한다.

<!-- end list -->

  - A4: XML External Entities (XXE) (XML 외부 개체 (XXE))
    오래되고 설정이 엉망인 많은 XML 프로세서들은 XML 문서 내에서 외부 개체 참조를 평가한다. 외부 개체는 파일 URI 처리기, 내부 파일 공유, 내부 포트 스캔, 원격 코드 실행과 서비스 거부공격을 사용하여 내부 파일을 공개하는데 사용할 수 있다.

<!-- end list -->

  - A5: Broken Access Control (취약한 접근 통제)
    취약한 접근 제어는 인증된 사용자가 수행할 수 있는 것에 대한 제한이 제대로 적용되지 않는 것을 의미한다. 공격자는 이러한 취약점을 악용하여 사용자의 계정 액세스, 중요한 파일 보기, 사용자의 데이터 수정, 액세스 권한 변경 등과 같은 권한 없는 기능, 또는 데이터에 액세스할 수 있다.

<!-- end list -->

  - A6: Security Misconfiguration (잘못된 보안 구성)
    훌륭한 보안은 애플리케이션, 프레임워크, 애플리케이션 서버, 웹 서버, 데이터베이스 서버 및 플랫폼에 대해 보안 설정이 정의되고 적용되어 있다. 기본으로 제공되는 값은 종종 안전하지 않기 때문에 보안 설정은 정의, 구현 및 유지되어야 한다. 또한 소프트웨어는 최신의 상태로 유지해야 한다.

<!-- end list -->

  - A7: Cross-Site Scripting ([XSS](https://ko.wikipedia.org/wiki/XSS "wikilink")) (크로스 사이트 스크립팅 (XSS))
    [XSS](https://ko.wikipedia.org/wiki/XSS "wikilink") 취약점은 애플리케이션이 신뢰할 수 없는 데이터를 가져와 적절한 검증이나 제한 없이 웹 브라우저로 보낼 때 발생한다. [XSS](https://ko.wikipedia.org/wiki/XSS "wikilink")는 공격자가 피해자의 브라우저에 스크립트를 실행하여 사용자 세션 탈취, 웹 사이트 변조, 악의적인 사이트로 이동할 수 있다.

<!-- end list -->

  - A8: Insecure Deserialization(안전하지 않은 역직렬화)
    안전하지 않은 역직렬화는 종종 원격 코드 실행으로 이어집니다. 역직렬화 취약점이 원격 코드실행 결과를 가져오지 않더라도 이는 권한 상승 공격, 주입 공격과 재생 공격을 포함한 다양한 공격 수행에 사용될 수 있다.

<!-- end list -->

  - A9: Using Components with Known Vulnerabilities (알려진 취약점이 있는 구성요소 사용)
    컴포넌트, 라이브러리, 프레임워크 및 다른 소프트웨어 모듈은 대부분 항상 전체 권한으로 실행된다. 이러한 취약한 컴포넌트를 악용하여 공격하는 경우 심각한 데이터 손실이 발생하거나 서버가 장악된다. 알려진 취약점이 있는 컴포넌트를 사용하는 애플리케이션은 애플리케이션 방어 체계를 손상하거나, 공격 가능한 범위를 활성화하는 등의 영향을 미친다.

<!-- end list -->

  - A10: Insufficient Logging & Monitoring(불충분한 로깅 및 모니터링)
    불충분한 로깅과 모니터링은 사고 대응의 비효율적인 통합 또는 누락과 함께 공격자들이 시스템을 더 공격하고, 지속성을 유지하며, 더 많은 시스템을 중심으로 공격할 수 있도록 만들고, 데이터를 변조, 추출 또는 파괴할 수 있다. 대부분의 침해 사례에서 침해를 탐지하는 시간이 200일이 넘게 걸리는 것을 보여주고, 이는 일반적으로 내부 프로세스와 모니터링보다 외부기관이 탐지한다.

## Top Ten Overview (2013)

  - A1: Injection (인젝션)
    [SQL](../Page/SQL.md "wikilink"), [OS](https://ko.wikipedia.org/wiki/OS "wikilink"), [LDAP](../Page/LDAP.md "wikilink") 인젝션 취약점은 신뢰할 수 없는 데이터가 명령어나 질의문의 일부분으로서 인터프리터로 보내질 때 발생한다. 공격자의 악의적인 데이터는 예상하지 못하는 명령을 실행하거나 적절한 권한 없이 데이터에 접근하도록 인터프리터를 속일 수 있다.

<!-- end list -->

  - A2: Broken Authentication and Session Management (인증 및 세션 관리 취약점)
    인증과 세션 관리와 관련된 애플리케이션 기능은 정확하게 구현되어 있지 않아서, 공격자가 패스워드, 키 또는 세션 토큰을 해킹하거나 다른 구현 취약점을 공격하여 다른 사용자 ID로 가장할 수 있다.

<!-- end list -->

  - A3: Cross-Site Scripting ([XSS](https://ko.wikipedia.org/wiki/XSS "wikilink")) (크로스 사이트 스크립팅)
    [XSS](https://ko.wikipedia.org/wiki/XSS "wikilink") 취약점은 애플리케이션이 신뢰할 수 없는 데이터를 가져와 적절한 검증이나 제한 없이 웹 브라우저로 보낼 때 발생한다. [XSS](https://ko.wikipedia.org/wiki/XSS "wikilink")는 공격자가 피해자의 브라우저에 스크립트를 실행하여 사용자 세션 탈취, 웹 사이트 변조, 악의적인 사이트로 이동할 수 있다.

<!-- end list -->

  - A4: Insecure Direct Object References (취약한 직접 객체 참조)
    직접 객체 참조는 개발자가 파일, 디렉토리, 데이터베이스 키와 같은 내부 구현 객체를 참조하는 것을 노출시킬 때 발생한다. 접근 통제를 통한 확인이나 다른 보호수단이 없다면, 공격자는 노출된 참조를 조작하여 허가 받지 않은 데이터에 접근할 수 있다.

<!-- end list -->

  - A5: Security Misconfiguration (보안 설정 오류)
    훌륭한 보안은 애플리케이션, 프레임워크, 애플리케이션 서버, 웹 서버, 데이터베이스 서버 및 플랫폼에 대해 보안 설정이 정의되고 적용되어 있다. 기본으로 제공되는 값은 종종 안전하지 않기 때문에 보안 설정은 정의, 구현 및 유지되어야 한다. 또한 소프트웨어는 최신의 상태로 유지해야 한다.

<!-- end list -->

  - A6: Sensitive Data Exposure (민감 데이터 노출)
    많은 웹 애플리케이션들이 신용카드, 개인 식별 정보 및 인증 정보와 같은 중요한 데이터를 제대로 보호하지 않는다. 공격자는 신용카드 사기, 신분 도용 또는 다른 범죄를 수행하는 등 약하게 보호된 데이터를 훔치거나 변경할 수 있다. 중요 데이터가 저장 또는 전송 중이거나 브라우저와 교환하는 경우 특별히 주의하여야 하며, 암호화와 같은 보호조치를 취해야 한다.

<!-- end list -->

  - A7: Missing Function Level Access Control (기능 수준의 접근 통제 누락)
    대부분의 웹 애플리케이션은 UI에 해당 기능을 보이게 하기 전에 기능 수준의 접근권한을 확인한다. 그러나, 애플리케이션은 각 기능에 접근하는 서버에 동일한 접근통제 검사를 수행한다. 요청에 대해 적절히 확인하지 않을 경우 공격자는 적절한 권한 없이 기능에 접근하기 위한 요청을 위조할 수 있다.

<!-- end list -->

  - A8: Cross-Site Request Forgery ([CSRF](https://ko.wikipedia.org/wiki/CSRF "wikilink")) (크로스 사이트 요청 변조)
    [CSRF](https://ko.wikipedia.org/wiki/CSRF "wikilink") 공격은 로그온 된 피해자의 취약한 웹 애플리케이션에 피해자의 세션 쿠키와 기타 다른 인증정보를 자동으로 포함하여 위조된 HTTP 요청을 강제로 보내도록 하는 것이다. 이것은 공격자가 취약한 애플리케이션이 피해자로부터의 정당한 요청이라고 오해할 수 있는 요청들을 강제로 만들 수 있다.

<!-- end list -->

  - A9: Using Components with Known Vulnerabilities (알려진 취약점이 있는 컴포넌트 사용)
    컴포넌트, 라이브러리, 프레임워크 및 다른 소프트웨어 모듈은 대부분 항상 전체 권한으로 실행된다. 이러한 취약한 컴포넌트를 악용하여 공격하는 경우 심각한 데이터 손실이 발생하거나 서버가 장악된다. 알려진 취약점이 있는 컴포넌트를 사용하는 애플리케이션은 애플리케이션 방어 체계를 손상하거나, 공격 가능한 범위를 활성화하는 등의 영향을 미친다.

<!-- end list -->

  - A10: Unvalidated Redirects and Forwards (검증되지 않은 리다이렉트 및 포워드)
    웹 애플리케이션은 종종 사용자들을 다른 페이지로 리다이렉트 하거나 포워드하고, 대상 페이지를 결정하기 위해 신뢰할 수 없는 데이터를 사용한다. 적절한 검증 절차가 없으면 공격자는 피해자를 피싱 또는 악성코드 사이트로 리다이렉트 하거나 승인되지 않은 페이지에 접근하도록 전달할 수 있다.

## Top Ten Overview (2010)

  - A1: Injection
    [SQL](../Page/SQL.md "wikilink"), [OS](https://ko.wikipedia.org/wiki/OS "wikilink"), [LDAP](../Page/LDAP.md "wikilink") 인젝션과 같은 인젝션 결함은 신뢰할 수 없는 데이터가 명령어나 질의어의 일부분으로써 [인터프리터](../Page/인터프리터.md "wikilink")에 보내질 때 발생한다. 공격자의 악의적인 데이터는 예기치않은 명령 실행이나 권한없는 데이터에 접근하도록 [인터프리터](../Page/인터프리터.md "wikilink")를 속일 수 있다.

<!-- end list -->

  - A2: Cross-Site Scripting ([XSS](https://ko.wikipedia.org/wiki/XSS "wikilink"))
    [XSS](https://ko.wikipedia.org/wiki/XSS "wikilink") 결함은 적절한 확인이나 제한없이 애플리케이션이 신뢰할 수 없는 데이터를 갖고, 그것을 [웹브라우저](https://ko.wikipedia.org/wiki/웹브라우저 "wikilink")에 보낼 때 발생한다. [XSS](https://ko.wikipedia.org/wiki/XSS "wikilink")는 공격자가 피해자의 브라우저 내에서 [스크립트](https://ko.wikipedia.org/wiki/스크립트 "wikilink")의 실행을 허용함으로써, 사용자의 세션을 탈취하거나, 웹사이트를 변조하거나, 악의적인 사이트로 사용자를 리다이렉트할 수 있다.

<!-- end list -->

  - A3: Broken Authentication and Session Management
    인증과 세션 관리와 연관된 애플리케이션 기능은 종종 올바로 구현되지 않는다. 그 결과, 공격자로 하여금 다른 사용자의 아이덴터티로 가장 할 수 있도록 패스워드, 키, 세션 토큰 체계를 위태롭게하거나, 구현된 다른 결함들을 악용할 수 있도록 허용한다.

<!-- end list -->

  - A4: Insecure Direct Object References
    직접 [객체](https://ko.wikipedia.org/wiki/객체 "wikilink") 참조는 파일, 디렉토리, 데이터베이스 키와 같이 내부적으로 구현된 객체에 대해 개발자가 참조를 노출할 때 발생한다. 접근통제에 의한 확인이나 다른 보호가 없다면, 공격자는 이 참조를 권한 없는 데이터에 접근하기 위해 조작할 수 있다.

<!-- end list -->

  - A5: Cross-Site Request Forgery ([CSRF](https://ko.wikipedia.org/wiki/CSRF "wikilink"))
    [CSRF](https://ko.wikipedia.org/wiki/CSRF "wikilink") 공격은 로그온 된 피해자의 브라우저가 취약한 웹애플리케이션에 피해자의 세션 쿠키와 어떤 다른 자동으로 포함된 인증 정보를 갖고 변조된 [HTTP](../Page/HTTP.md "wikilink") 요청을 보내도록 강제한다. 이것은 공격자가 피해자의 브라우저로 하여금 취약한 애플리케이션이 피해자로부터의 정당한 요청이라고 착각하게 만드는 요청들을 생성하도록 강제하는 것을 허용한다.

<!-- end list -->

  - A6: Security Misconfiguration
    훌륭한 보안은 애플리케이션, 프레임워크, 애플리케이션서버, 웹서버, 데이터베이스 서버와 플랫폼에 대해 보안 구성이 정의되고 적용하기를 요구한다. 대부분이 보안을 기본적으로 탑재되지 않기 때문에 이 모든 설정은 정의되고, 구현되고, 유지되어야만 한다. 이것은 애플리케이션에서 사용되는 모든 코드 라이브러리를 포함하여 모든 소프트웨어가 최신의 상태를 유지하는 것을 포함한다.

<!-- end list -->

  - A7: Insecure Cryptographic Storage
    많은 웹애플리케이션들이 적절한 암호나 해쉬를 갖고 신용카드번호, 주민등록번호, 그리고 인증 신뢰 정보와 같은 민감한 데이터를 적절히 보호하지 않는다. 공격자는 아이덴티티 도난, 신용카드사기, 또는 다른 범죄를 저지르기 위해 그렇게 약하게 보호된 데이터를 훔치거나 조작할 지 모른다.

<!-- end list -->

  - A8: Failure to Restrict URL Access
    많은 웹애플리케이션들이 보호된 링크나 버튼을 표현하기 전에 URL 접근 권한을 확인한다. 그러나, 애플리케이션은 이 페이지들이 접근될 때마다 매번 유사한 접근 통제 확인이 필요하다. 공격자는 이 감춰진 페이지에 접근하기 위해 URL을 변조시킬 수 있다.

<!-- end list -->

  - A9: Insufficient Transport Layer Protection
    애플리케이션은 종종 민감한 네트워크 트래픽의 인증, 암호화, 그리고 비밀성과 무결성을 보호하는데 실패한다. 실패할 때에는 대체로 약한 알고리즘을 사용하거나, 만료되거나 유효하지 않은 인증서를 사용하거나 또는 그것들을 올바로 사용하지 않을 때이다.

<!-- end list -->

  - A10: Unvalidated Redirects and Forwards
    웹애플리케이션은 종종 사용자들을 다른 페이지로 리다이렉트하거나 포워드한다. 그러나, 목적 페이지를 결정하기 위해 신뢰되지 않는 데이터를 사용한다.적절한 확인이 없다면, 공격자는 피해자를 피싱 사이트나 악의적인 사이트로 리다이렉트 할 수 있고, 포워드를 권한 없는 페이지의 접근을 위해 사용할 수 있다.

## Top Ten Overview (2007)

A1 - Cross Site Scripting (XSS)

A2 - Injection Flaws

A3 - Malicious File Execution

A4 - Insecure Direct Object Reference

A5 - Cross Site Request Forgery (CSRF)

A6 - Information Leakage and Improper Error Handling

A7 - Broken Authentication and Session Management

A8 - Insecure Cryptographic Storage

A9 - Insecure Communications

A10 - Failure to Restrict URL Access

## Top Ten Overview (2004)

A1 2004 Unvalidated Input

A2 2004 Broken Access Control

A3 2004 Broken Authentication and Session Management

A4 2004 Cross Site Scripting

A5 2004 Buffer Overflow

A6 2004 Injection Flaws

A7 2004 Improper Error Handling

A8 2004 Insecure Storage

A9 2004 Application Denial of Service

A10 2004 Insecure Configuration Management

## 외부 링크

  - [OWASP 프로젝트](http://www.owasp.org)

[분류:네트워크 보안](https://ko.wikipedia.org/wiki/분류:네트워크_보안 "wikilink") [분류:웹 취약점 공격](https://ko.wikipedia.org/wiki/분류:웹_취약점_공격 "wikilink")