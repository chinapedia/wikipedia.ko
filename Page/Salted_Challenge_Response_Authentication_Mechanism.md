> This article is converted from Wikipedia: [Salted Challenge Response Authentication Mechanism](https://ko.wikipedia.org/wiki/Salted_Challenge_Response_Authentication_Mechanism).


암호화에서, **Salted Challenge Response Authentication Mechanism** (**SCRAM**) 은 서버에 사용자 인증을 제공하는 현대적인 암호 기반 시도 응답 인증 방법의 제품군이다. [Simple Authentication and Security Layer](../Page/SASL.md "wikilink") (SASL) 에 명시된 대로, [SMTP](https://ko.wikipedia.org/wiki/SMTP "wikilink") 와 [IMAP](https://ko.wikipedia.org/wiki/IMAP "wikilink") ([e-mail](https://ko.wikipedia.org/wiki/e-mail "wikilink")), 또는 [XMPP](../Page/XMPP.md "wikilink") (chat) 와 같은 서비스에 대한 비밀번호 기반의 로그인에 사용할 수 있다. XMPP 에서는 의무적으로 지원해야한다.\[1\]

## 동기유발

[Alice는](https://ko.wikipedia.org/wiki/Alice_and_Bob "wikilink") Bob의 서버에 접속하고 싶어한다. 그녀는 그녀임을 증명해야 한다. 이 인증 문제를 해결하기 위하여, Alice와 Bob은 Alice가 알고 있고 Bob은 검증하는 방법을 알고 있는 암호 사용에 동의한다.

이제 Alice는 Bob이 검증하기 위하여 암호화되지 않은 연결로 그녀의 평문 암호를 전송한다. 그러나 그것은 도청하고 있는 Mallory가 암호에 접근할 수 있게 해준다. Alice와 Bob은 암호화된 연결을 사용하여 이것을 우회할 수 있다. 그러나, Alice는 암호화 설정을 [중간자 공격](../Page/중간자_공격.md "wikilink") 에 의해 Mallory가 한게 아니라 Bob이 한 것인지 알 수 없다. 그러므로, Alice는 [CRAM-MD5](https://ko.wikipedia.org/wiki/CRAM-MD5 "wikilink") 또는 [DIGEST-MD5](https://ko.wikipedia.org/wiki/DIGEST-MD5 "wikilink") 처럼 그녀의 암호의 해시코드를 대신 전송한다. 해시일 경우, Mallory는 그것만으로 암호를 얻을 수 없다. 그리고 해시값은 시도값에 의해 변형(salted)되어 있기 때문에 Mallory는 그 해시값을 한번의 로그인 과정에서만 사용할 수 있다. 그러나, Alice는 몇가지 비밀 정보를 Bob에게 보내고 싶고, 그것이 Mallory가 아닌 Bob임을 확인하고 싶어한다.

이 문제를 해결하기 위해서, Bob은 자신을 [인증 기관](../Page/인증_기관.md "wikilink") (Certificate Authority, CA)에 등록해서 자격증명(certificate)을 발급받는다. Alice는 단독으로 그 서명 시스템에 의존할 수 있지만, 그것에 약점이 있다는 것을 알고 있다. 중간자 공격이 없다는 것을 보장하기 위해, Bob은 비밀번호(혹은 비밀번호의 변형된 해시값)을 알고 있다는 증거를 만들고, 이것을 그의 자격증명에 포함시킨다. 이러한 포함 작업을 channel binding이라 부르는데, 저수준의 암호 채널이 고수준의 애플리케이션 채널에 '바인드'되는 것이다.

Alice는 이제 Bob을 인증할 수 있고, Bob도 Alice를 인증할 수 있다. 서로를 인증하는 것이 [상호 인증](https://ko.wikipedia.org/wiki/상호_인증 "wikilink") (mutual authentication)이다. DIGEST-MD5에서는 이미 상호 인증이 가능했다. 하지만 그것은 정확하지 않게 구현되었다.

Mallory가 중간자 공격을 하면서 CA 서명을 위조했을 때, 그녀는 비밀번호의 해시값을 얻을 수 있다. 그러나 그녀는 한번의 로그인 세션에서 조차 Alice를 가장할 수 없는데, Alice는 Mallory의 암호화 키를 그녀의 해시값에 포함시키므로 결국 Bob으로의 로그인이 실패하기 때문이다. 완전히 명백한 공격을 만들기 위해, Mallory는 Alice에 의해 사용되는 비밀번호를 알아야 하거나 Bob의 비밀 암호화 키를 알아야만 한다.

Bob은 서버 데이터베이스의 데이터 보안에 허점이 있다는 사실을 들었다. 그래서 그는 유저의 비밀번호를 평문으로 저장하지 않기로 결정했다. 그는 CRAM-MD5와 DIGEST-MD5 로그인 계획을 들었지만, 이런 로그인 계획을 자신의 유저들에게 제공하기 위해서는, 약하게 해시되는 변형되지 않은 비밀번호를 저장해야만 한다. 그는 이런 계획이 맘에 안들어서 비밀번호를 평문으로 요구하는 것을 선택한다. 그런다음 그는 [bcrypt](https://ko.wikipedia.org/wiki/bcrypt "wikilink"), [scrypt](https://ko.wikipedia.org/wiki/scrypt "wikilink") 혹은 [PBKDF2](https://ko.wikipedia.org/wiki/PBKDF2 "wikilink")와 같은 안전한 해시로 그 비밀번호를 해싱할 수 있고 그가 원하는 대로 그들을 변형시킬 수 있다. 하지만 그 다음에는 Bob과 Alice는 여전히 이전에 설명한 문제에 부딪히게 된다. 이 문제를 해결하기 위해서, 그들은 SCRAM을 사용하는데, Bob은 비밀번호를 변형된 형식으로 PBKDF2를 사용하여 저장할 수 있다. 로그인 동안, Bob은 Alice에게 그의 salt와 PBKDF2 알고리즘의 반복 횟수를 전송한다. 그러면 Alice는 이 값들을 사용하여 Bob이 그의 데이터베이스에 가지고 있는 해시된 비밀번호를 계산한다. SCRAM에서의 모든 계산은 그들 모두가 알고 있는 이 값들에 근거한다.

## 프로토콜 개요

모든 클라리언트와 서버는 [SHA-1](https://ko.wikipedia.org/wiki/SHA-1 "wikilink") 해시 알고리즘을 지원해야하지만, SCRAM 은 [CRAM-MD5](https://ko.wikipedia.org/wiki/CRAM-MD5 "wikilink") 또는 [DIGEST-MD5](https://ko.wikipedia.org/wiki/DIGEST-MD5 "wikilink") 와 다르게 기본이 되는 해시 함수로부터 독립적이다.\[2\] [IANA](http://www.iana.org/assignments/hash-function-text-names/hash-function-text-names.xhtml) 에 정의된 모든 해시 함수를 대신 사용할 수 있다. 동기유발 절에서 언급한 바와 같이, SCRAM 은 [PBKDF2](https://ko.wikipedia.org/wiki/PBKDF2 "wikilink") 방법을 사용하여, 서버상의 데이터 유출시의 [무차별 대입 공격에](https://ko.wikipedia.org/wiki/Password_cracking "wikilink") 대한 견고성을 증가시킨다. 서버가 광고하고 클라이언트가 선택한 알고리즘의 이름에 의해 주어진 선택된 해시 함수를 \(H\) 라고 하자. 'SCRAM-SHA1' 을 예로 들면, 해시 함수로 SHA1 을 사용한다.

### 메시지

RFC 5802 은 서버/클라이언트간 4개의 연속적인 메시지를 명명한다:

  - *client-first*: *client-first* 메시지는 *gs2-cbind-flag*, 원하는 \(\mathrm{username}\), 그리고 무작위로 생성된 클라이언트 임시값 \(\mathrm{nonce}_c\) 로 구성되어있다.
    *server-first*: 서버는 이 클라이언트 임시값에 자신의 임시값 \(\mathrm{nonce}_s\) 를 덧붙이고, 그것을 *server-first* 메시지에 추가한다, 그것은 또한 사용자의 암호 해시를 위한 salting 에 사용된 \(\mathrm{salt}\)t 와 반복 카운트 표시 \(\mathrm{it}\) 를 포함한다.
    *client-final*: After that the client sends the *client-final* message, which contains *c-bind-input*, the concatenation of the client and the server nonce, and a proof \(\mathrm{proof}_c\) of all the messages sent, and the contents of *client-final* up to the proof.
    *server-final* : 통신은 서버 증명 \(\mathrm{proof_s}\) 을 포함한 *server-final* 메시지와 함께 종료된다.

### 저장된 암호

저장된 암호 \(\mathrm{password}_s\) 는 다음과 같이 계산된다:

\[\mathrm{password}_s = H_i(\mathrm{password}, \mathrm{salt}, \mathrm{it})\], \(H_i(p,s,i)\) 는 [PBKDF2](https://ko.wikipedia.org/wiki/PBKDF2 "wikilink") ([HMAC](https://ko.wikipedia.org/wiki/HMAC "wikilink"), \(p\), \(s\), \(i\), \(H\) 의 결과값 길이) 로 정의한다.

모든 사용자에 대하여, 서버는 username 과 [평문 암호가](https://ko.wikipedia.org/wiki/#장점 "wikilink") 아닌 \(\mathrm{salt}\) 와 \(\mathrm{it}\) 으로 계산된 \(\mathrm{password}_s\)

### 증명

client 와 server 는 다음과 같이 구성된 같은 \(\mathrm{Auth}\) 변수로 서로를 증명한다:

\[\mathrm{Auth} = \text{client-first} , \text{server-first} , \text{client-final-without-proof}\]

proof 는 다음과 같이 계산된다:

\[\mathrm{key}_c = HMAC(\mathrm{password}_s,  \text{``Client Key''})\]

\[\mathrm{key}_s = HMAC(\mathrm{password}_s,  \text{``Server Key''})\]

\[\mathrm{proof}_c = \mathrm{key}_c \oplus HMAC(H(\mathrm{key}_c), \mathrm{Auth})\]

\[\mathrm{proof}_s = HMAC(H(\mathrm{key}_s), \mathrm{Auth})\]

\(\oplus\) 는 [XOR](https://ko.wikipedia.org/wiki/XOR "wikilink") 연산을 정의한다. \(\text{``Client Key''}\) 와 \(\text{``Server Key''}\) 는 말 그대로의 문자열이다.

### 채널 바인딩

채널 바인딩 용어는 애플리케이션 계층을 'bind' 하는 중간자 공격 방지 전략을 묘사하는데, 이는 하위 (대부분 암호화 된) 계층에 상호 인증을 제공하여 연결의 양측 종단점이 동일하다고 보장한다. 채널 바인딩에는 두가지 일반적인 방향이 있습니다: *unique* 와 *endpoint* 채널 바인딩. 첫째는 특정한 연결이 사용되는것이고, 두번째는 종단점이 같다는 것이다.

여러 채널 바인딩 유형이 있는데, 모든 단일 유형은 *channel binding unique prefix*\[3\] 를 가지고 있습니다.. 모든 채널 바인딩 타입은 채널과 종단점을 통해 고유 정보를 제공하는 *channel binding data* 의 내용을 명시합니다. 예를 들어, *tls-server-end-point* 채널 바인딩은 서버의 TLS 자격 입니다.\[4\] 애플리케이션 계층의 SCRAM 채널 바인딩의 예시적인 사용 사례는 하위 계층의 [Transport Layer Security](https://ko.wikipedia.org/wiki/Transport_Layer_Security "wikilink") (TLS) 가 될 수 있다. TLS 는 도청은 보호하지만, 중간자 공격은 막지 않습니다. 이를 위해, 종단점은 서로 식별성을 보장해야하는데, 이는 SCRAM 에 의해 제공된다.

The *gs2-cbind-flag* SCRAM variable specifies whether the client supports channel binding or not, or thinks the server doesn't support channel binding, and *c-bind-input* contains the *gs2-cbind-flag* together with the *channel binding unique prefix* and the *channel binding data* themselves.

SCRAM 에서 채널 바인딩은 선택이고, *gs2-cbind-flag* 변수는 [다운그레이드 공격](https://ko.wikipedia.org/wiki/다운그레이드_공격 "wikilink") 을 방지한다.

서버에서 채널 바인딩을 지원하면 광고하는 SCRAM 알고리즘 이름에 '-PLUS' 문자열을 붙여야 한다.

## 장점

  - 강력한 암호 저장: 올바른 방법으로 구현되는 경우, 서버는 반복된 해시로 [salted](https://ko.wikipedia.org/wiki/Salt_\(cryptography\) "wikilink") 된 암호를 저장하고, [오프라인 공격을](https://ko.wikipedia.org/wiki/Password_cracking "wikilink") 어렵게 하고, 데이터베이스 위반의 영향을 감소시킨다.\[5\]
  - 간단하다: SCRAM 은 DIGEST-MD5 보다 구현하기 쉽다\[6\].\[7\]
  - 국제 상호 운용성: RFC 는 CRAM-MD5 와 달리 usernames 와 passwords 사용에 [UTF-8](../Page/UTF-8.md "wikilink") 을 필요로한다.\[8\]\[9\]
  - salted 해시된 암호가 전체 로그인 절차에서 사용되고, 서버상의 salt 가 변하지 않기 때문에 클라이언트가 암호 저장에 해시된 암호를 사용할 수 있고 평문 암호를 공격자에게 드러내지 않습니다. 이러한 해시 된 암호는 암호 재사용이 편리하게 한 서버에 바인딩되어 있습니다.\[10\]

## 참고자료

## 외부 링크

  - RFC 5802, SCRAM for SASL and GSS-API
  - \[//datatracker.ietf.org/doc/draft-melnikov-httpbis-scram-auth/ SCRAM in HTTP\] (현재 초안 상태)
  - [GNU Network Security Labyrinth](http://josefsson.org/talks/gnu-network-security-labyrinth.pdf) ([동기유발](https://ko.wikipedia.org/wiki/#동기유발 "wikilink") 절과 유사)

[분류:암호 프로토콜](https://ko.wikipedia.org/wiki/분류:암호_프로토콜 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.  [CRAM-MD5 to Historic](http://tools.ietf.org/html/draft-ietf-sasl-crammd5-to-historic-00)
10.