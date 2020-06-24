> This article is converted from Wikipedia: [X.509](https://ko.wikipedia.org/wiki/X.509).


**X.509**는 암호학에서 공개키 인증서와 인증알고리즘의 표준 가운데에서 공개 키 기반([PKI](https://ko.wikipedia.org/wiki/PKI "wikilink"))의 [ITU-T](../Page/ITU-T.md "wikilink") 표준이다.

## 역사와 활용

X.509는 1988년 7월 3일 X.500 표준안의 일환으로 시작되었다. 1993년 인증기관 고유 식별자와 주체고유 식별자가 추가된 v2가 발표되었으며, 1996년에 확장 기능(Extension)을 이용해 데이터를 추가할 수 있는 v3가 발표되어 현재 쓰이고 있다. PGP처럼 상호 신뢰를 기반으로 하는 웹 모델과 달리, X.509는 매우 엄격한 수직적 구조를 채택하였다. 따라서 하나의 인증 기관을 정점으로하는 트리 구조를 갖게 된다. 이러한 형태의 불편함을 해소하기 위해, v3는 보다 유연한 구조를 채택하여 몇 개의 신용할만한 Root CA끼리는 상호 인증, 혹은 자가 인증을 허용하고 있다.

## 인증서

X.509 시스템에서 CA는 X.500 규약에 따라 서로 구별되는 공개키를 가진 인증서를 발행한다.

한 조직의 인증된 루트 인증서는 그 PKI 시스템을 사용하는 모든 직원들에 분배될 수 있다. [인터넷 익스플로러나](../Page/인터넷_익스플로러.md "wikilink") [모질라](../Page/모질라.md "wikilink"), [오페라와](../Page/오페라_\(웹_브라우저\).md "wikilink") 같은 브라우저는 SSL 인증서라 불리는 미리 설치된 루트 인증서가있다. 사용자가 이 루트 인증서를 제거하거나 사용중지할 수도 있기는 하지만, 거의 그러지는 않는다.

X.509는 또한 CRL (certificate revocation list) 구현을 위한 표준도 포함한다. IETF에서 승인된 인증서 유효성 점검 방법은 [OCSP](https://ko.wikipedia.org/wiki/OCSP "wikilink")(Online Certificate Status Protocol)이다.

### 인증서의 구조

X.509 v3의 디지털 인증서의 구조는 아래와 같다.

  - Certificate
      - Version 인증서의 버전을 나타냄
      - Serial Number CA가 할당한 정수로 된 고유 번호
      - Signature 서명 알고리즘 식별자
      - Issuer 발행자
      - Validity 유효기간
          - Not Before 유효기간 시작 날짜
          - Not After 유효기간 끝나는 날짜
      - Subject 소유자
      - Subject Public Key Info 소유자 공개 키 정보
          - Public Key Algorithm 공개 키 알고리즘
          - Subject Public Key
      - Issuer Unique Identifier (Optional) 발행자 고유 식별자
      - Subject Unique Identifier (Optional) 소유자 고유 식별자
      - Extensions (Optional) 확장
          - ...
  - Certificate Signature Algorithm
  - Certificate Signature

### 인증서 파일 확장자

X.509 인증서의 확장자는 다음과 같다:

  - `.CER` - [CER](https://ko.wikipedia.org/wiki/Canonical_Encoding_Rules "wikilink") 암호화 된 인증서. 복수의 인증서도 가능.
  - `.DER` - [DER](https://ko.wikipedia.org/wiki/Distinguished_Encoding_Rules "wikilink") 암호화 된 인증서.
  - `.PEM` - ([Privacy Enhanced Mail](https://ko.wikipedia.org/wiki/Privacy_Enhanced_Mail "wikilink")) [Base64](https://ko.wikipedia.org/wiki/Base64 "wikilink")로 인코딩 된 인증서. "-----BEGIN CERTIFICATE-----"와 "-----END CERTIFICATE-----" 가운데에 들어간다.
  - `.P7B` - `.p7c` 참조.
  - `.P7C` - [PKCS\#7](https://ko.wikipedia.org/wiki/PKCS7 "wikilink") `서명 자료 구조`(자료는 제외), 인증서이거나 CRL(복수도 가능).
  - `.PFX` - `.p12` 참조.
  - `.P12` - [PKCS\#12](https://ko.wikipedia.org/wiki/PKCS12 "wikilink"), 공개 인증서와 암호로 보호되는 개인 키를 가질 수 있다(복수도 가능).

[PKCS\#7는](https://ko.wikipedia.org/wiki/PKCS7 "wikilink") 데이터를 서명하거나 암호화 할 때 쓰이는(enveloping) 표준이다. 서명된 데이터를 검증할 때는 인증서가 필요하기 때문에 `서명 자료 구조`에 인증서를 포함하기도 한다. `.P7C` 파일은 데이터가 아니라 `서명 자료 구조`일 뿐이다.

[PKCS\#12는](https://ko.wikipedia.org/wiki/PKCS12 "wikilink") PFX(개인 정보 교환:Personal inFormation eXchange)이 발전된 형태이며, 하나의 파일에서 공개 / 개인 자료들을 교환할 때 쓰인다.

A `.PEM` 파일은 단수, 혹은 복수의 인증서와 개인 키를 가질 수 있으며 적절한 시작/종료 라인 사이에 위치한다(CERTIFICATE or RSA PRIVATE KEY).

## 외부 링크

  - [ITU-T Recommendation X.509 : Information technology - Open Systems Interconnection - The Directory: Public-key and attribute certificate frameworks](http://www.itu.int/rec/T-REC-X.509/en)

  - Peter Gutmann's articles, an overview of PKI [1](https://web.archive.org/web/20110607040159/http://www.cs.auckland.ac.nz/~pgut001/pubs/pkitutorial.pdf), X.509 implementation notes [X.509 Style Guide](http://www.cs.auckland.ac.nz/~pgut001/pubs/x509guide.txt)

[분류:암호 프로토콜](https://ko.wikipedia.org/wiki/분류:암호_프로토콜 "wikilink") [분류:ITU-T 권고](https://ko.wikipedia.org/wiki/분류:ITU-T_권고 "wikilink")