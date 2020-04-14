> This article is converted from Wikipedia: [MIME](https://ko.wikipedia.org/wiki/MIME).


**MIME**()는 [전자 우편을](https://ko.wikipedia.org/wiki/전자_우편 "wikilink") 위한 인터넷 표준 포맷이다. 전자우편은 7비트 [ASCII](https://ko.wikipedia.org/wiki/ASCII "wikilink") 문자를 사용하여 전송되기 때문에, 8비트 이상의 코드를 사용하는 문자나 [이진 파일들은](../Page/이진_파일.md "wikilink") MIME 포맷으로 변환되어 [SMTP](https://ko.wikipedia.org/wiki/SMTP "wikilink")로 전송된다. 실질적으로 [SMTP](https://ko.wikipedia.org/wiki/SMTP "wikilink")로 전송되는 대부분의 [전자 우편은](https://ko.wikipedia.org/wiki/전자_우편 "wikilink") MIME 형식이다. MIME 표준에 정의된 content types은 [HTTP](../Page/HTTP.md "wikilink")와 같은 통신 프로토콜에서 사용되며, 점차 그 중요성이 커지고 있다.

## 개요

기본적으로 인터넷 [전자 우편](https://ko.wikipedia.org/wiki/전자_우편 "wikilink") 전송 프로토콜인 [SMTP](https://ko.wikipedia.org/wiki/SMTP "wikilink")는 7비트 [ASCII](https://ko.wikipedia.org/wiki/ASCII "wikilink") 문자만을 지원한다. 이것은 7비트 ASCII 문자로 표현할 수 없는 영어 이외의 언어로 쓰인 [전자 우편은](https://ko.wikipedia.org/wiki/전자_우편 "wikilink") 제대로 전송될 수 없다는 것을 의미한다. MIME은 [ASCII](https://ko.wikipedia.org/wiki/ASCII "wikilink")가 아닌 [문자 인코딩을](../Page/문자_인코딩.md "wikilink") 이용해 영어가 아닌 다른 언어로 된 [전자 우편을](https://ko.wikipedia.org/wiki/전자_우편 "wikilink") 보낼 수 있는 방식을 정의한다. 또한 그림, 음악, 영화, 컴퓨터 프로그램과 같은 8비트짜리 이진 파일을 [전자 우편으로](https://ko.wikipedia.org/wiki/전자_우편 "wikilink") 보낼 수 있도록 한다. MIME은 또한 [전자우편](../Page/전자우편.md "wikilink")과 비슷한 형식의 메시지를 사용하는 [HTTP](../Page/HTTP.md "wikilink")와 같은 통신 프로토콜의 기본 구성 요소이다. 메시지를 MIME 형식으로 변환하는 것은 [전자 우편](https://ko.wikipedia.org/wiki/전자_우편 "wikilink") 프로그램이나 서버 상에서 자동으로 이루어진다.

[전자 우편의](https://ko.wikipedia.org/wiki/전자_우편 "wikilink") 기본적인 형식은 RFC 2821에서 정의하고 있다. 이 문서는 RFC 822를 대체한다. 이 문서는 텍스트 [전자 우편의](https://ko.wikipedia.org/wiki/전자_우편 "wikilink") 헤더와 본문의 형식을 명시하고 있으며, 그중에는 우리에게 익숙한 "To:", "Subject:", "From:", "Date:" 등의 헤더가 포함되어 있다. MIME은 메시지의 종류를 나타내는 *content-type*, 메시지 인코딩 방식을 나타내는 *content-transfer-encoding*과 같은 추가적인 [전자 우편](https://ko.wikipedia.org/wiki/전자_우편 "wikilink") 헤더를 정의하고 있다. MIME은 또한 [ASCII](https://ko.wikipedia.org/wiki/ASCII "wikilink")가 아닌 문자를 [전자 우편](https://ko.wikipedia.org/wiki/전자_우편 "wikilink") 헤더로 사용할 수 있도록 규정하고 있다.

MIME은 확장 가능하다. MIME 표준은 새로운 *content-type*과 또 다른 MIME 속성 값을 등록할 수 있는 방법을 정의하고 있다.

MIME의 명시적인 목표 중 하나는 기존 [전자 우편](https://ko.wikipedia.org/wiki/전자_우편 "wikilink") 시스템과의 호환성이다. MIME을 지원하는 클라이언트에서 비 MIME가 제대로 표시될 수 있고, 반대로 MIME을 지원하지 않는 클라이언트에서 간단한 MIME 메시지가 표시될 수 있다.

## MIME 헤더

### MIME-Version

이 헤더는 해당 메시지가 MIME 형식임을 나타낸다. 현재 사용되는 값은 "1.0"이므로 아래와 같이 사용할 수 있다.

`MIME-Version: 1.0`

### Content-Type

이 헤더는 메시지의 타입과 서브타입을 나타낸다. 예를 들면

`Content-Type: text/plain`

타입과 서브타입을 합쳐 MIME 타입이라 부른다. *Internet media type* 이라고도 부른다. 다양한 파일 포맷이 MIME 타입으로 등록되어 있다. *text* 타입은 *charset* 인자를 가질 수 있으며 이 인자는 [문자 인코딩을](../Page/문자_인코딩.md "wikilink") 지정한다.

*content-type* 헤더와 MIME 타입은 [전자 우편을](https://ko.wikipedia.org/wiki/전자_우편 "wikilink") 위해 정의된 것이지만, 이제는 [HTTP](../Page/HTTP.md "wikilink"), [SIP](https://ko.wikipedia.org/wiki/SIP "wikilink")와 같은 인터넷 프로토콜에서 함께 사용하고 있다. MIME 타입 등록은 [IANA](https://ko.wikipedia.org/wiki/IANA "wikilink")에서 관리하고 있다.

*multipart* 메시지 타입을 통해 MIME은 트리 구조의 메시지 형식을 정의할 수 있다. 이 방식은 다음을 지원한다.

  - *text/plain*을 통한 단순 텍스트 메시지 ("Content-type:"의 기본값")
  - 첨부가 포함된 텍스트 (*text/plain* 파트와 텍스트가 아닌 파트로 구성된 *multipart/mixed*). 파일을 첨부한 MIME 메시지는 "Content-disposition:" 헤더를 통해 파일의 본래 이름을 지정한다. 파일의 종류는 MIME의 content-type 헤더와 파일 확장자를 통해 알 수 있다.
  - 원본 메시지가 첨부된 답장 메시지 (*text/plain* 파트와 원본 메시지를 나타내는 *message/rfc822* 파트로 구성된 *multipart/mixed*)
  - 평문 텍스트와 [HTML](../Page/HTML.md "wikilink")과 같이 다른 포맷을 함께 보낸 메시지 (*multipart/alternative*)
  - 그 외 다양한 메시지 구조들

### Content-Transfer-Encoding

MIME (RFC 2045)는 바이너리 데이터를 [ASCII](https://ko.wikipedia.org/wiki/ASCII "wikilink") 텍스트 형식으로 변환하기 위한 몇가지 방법을 정의하고 있다. *content-transfer-encoding* MIME 헤더를 통해 변환 방식을 지정한다. RFC 문서와 전송 인코딩에 대한 [IANA 목록](http://www.iana.org/assignments/transfer-encodings)은 다음을 정의하고 있다.

  - 일반 SMTP에 사용 가능
      - **7bit** - \[1..127\]의 [ASCII](https://ko.wikipedia.org/wiki/ASCII "wikilink") 코드로 이루어진 데이터로 줄 단위로 표현하며 각 줄을 CR, LF로 끝난다. 한 줄의 최대 길이는 CR (ASCII 코드 13), LF (ASCII 코드 10)를 제외하고 998자이다.
      - **[quoted-printable](https://ko.wikipedia.org/wiki/quoted-printable "wikilink")** - 약간의 바이너리 데이터가 포함된 US-ASCII로 이루어진 텍스트 데이터를 표현할 때 효과적이다. US-ASCII는 특별한 변환을 거치지 않고 그대로 표시되기에 효율적이며 인코딩한 데이터를 사람이 이해할 수 있다.
      - **[base64](https://ko.wikipedia.org/wiki/base64 "wikilink")** - 임의의 바이너리 데이터를 7비트 데이터로 변환한다. 고정된 오버헤드가 발생하고 비 텍스트 데이터의 변환 시 사용한다.
  - [8BITMIME](https://ko.wikipedia.org/wiki/8BITMIME "wikilink") 지원하는 SMTP 서버에 사용 가능
      - **8bit** - 8비트로 표현된 데이터로 한 줄 당 998자로 표현하며 CR, LF로 끝난다.
      - **binary** - 일련의 octets. SMTP에서는 사용할 수 없다.

## Encoded-Word

RFC 2822의 정의에 따르면, 메시지 헤더와 그 값은 항상 ASCII 문자를 사용해야 한다. ASCII가 아닌 헤더 값은 MIME의 **encoded-word** 문법(RFC 2047)에 따라 인코딩해야 한다. 이 문법은 원본 문자 인코딩("문자셋")과 원본 데이터를 ASCII 문자로 변환하는 데 사용한 인코딩 방식을 포함한다.

encoded-word의 형식: "`=?`문자셋`?`인코딩 방식`?`인코드된 데이터`?=`".

  - 문자셋은 보통 [utf-8을](../Page/UTF-8.md "wikilink") 사용한다. 하지만 [IANA에](https://ko.wikipedia.org/wiki/Internet_Assigned_Numbers_Authority "wikilink") 등록된 어떤 문자셋도 사용 가능하다.
  - 인코딩 방식은 [quoted-printable](https://ko.wikipedia.org/wiki/quoted-printable "wikilink") 인코딩 방식과 비슷한 Q-encoding 방식을 나타내는 "`Q`"나 [base64](https://ko.wikipedia.org/wiki/base64 "wikilink") 인코딩을 나타내는 "`B`" 중 하나를 사용할 수 있다.
  - 인코드된 데이터는 인코딩 방식에 의해 변환된 데이터이다.

*Q-encoding과 quoted-printable의 차이*

RFC 2047에 따르면, encoded-word는 공백 문자(white space)를 포함해서는 안 된다. 따라서 ASCII 코드로 20h(iso-8859-1에서의 스페이스)인 문자는 인코딩을 거쳐야 한다. ASCII 20h(20h가 공백이 아닐지라도)인 문자는 보통 "_" 문자(ASCII 5Fh)로 변환한다. 공백을 "=20"으로 인코딩한 것보다 이 방식이 인코드된 데이터의 가독성을 높여준다.

예를 들어,

`Subject: =?utf-8?Q?=C2=A1Hola,_se=C3=B1or!?=`

위 문장은 "Subject: ¡Hola, señor\!"를 인코딩한 데이터이다.

encoded-word 형식은 헤더 이름에는 사용할 수 없다. 헤더 이름은 항상 US-ASCII로 표현해야 한다.

## Multipart 메시지

MIME multipart 메시지는 "Content-type:" 헤더에 boundary 파라미터를 포함한다. 이 boundary는 다음과 같이 각 메시지 파트를 구분하는 역할을 하며, 메시지의 시작과 끝부분에도 나타난다.

``` email
MIME-Version: 1.0
Content-Type: multipart/mixed; boundary=frontier

This is a message with multiple parts in MIME format.
--frontier
Content-Type: text/plain

This is the body of the message.
--frontier
Content-Type: application/octet-stream
Content-Transfer-Encoding: base64

PGh0bWw+CiAgPGhlYWQ+CiAgPC9oZWFkPgogIDxib2R5PgogICAgPHA+VGhpcyBpcyB0aGUg
Ym9keSBvZiB0aGUgbWVzc2FnZS48L3A+CiAgPC9ib2R5Pgo8L2h0bWw+Cg==
--frontier--
```

각 파트는 *Content-*로 시작하는 자신만의 헤더와 본문을 갖는다. 그리고 multipart 메시지는 중첩 가능하다. 각 파트는 자신만의 문자셋과 인코딩 방식(Content-Transfer-Encoding)을 파트 헤더에서 정의하고 있다. Multipart 메시지에는 아래와 같은 종류가 있다.

Notes:

  - 첫 번째 boundary 전에 나오는 내용은 MIME을 지원하지 않는 클라이언트를 위해 제공된다. MIME 호환 클라이언트는 이 내용을 무시한다.
  - Boundary를 선택하는 것은 전자 우편을 전송하는 클라이언트의 몫이다. 보통 무작위의 문자를 선택함으로써 메시지의 본문과 충돌을 피한다.

### Mixed

Multipart/mixed는 다른 "Content-type" 헤더를 갖는 파일을 전송하는 데 사용한다. 그림이나 쉽게 읽을 수 있는 파일을 전송할 때, 대부분의 전자 우편 클라이언트는 이를 직접 화면에 표시할 것이다. 그렇지 않을 경우 해당 데이터는 첨부 파일의 형태로 표시된다. "Content-disposition" 헤더는 첨부 파일의 이름을 표시하는 데 사용한다.

### Digest

RFC 2049에 명시되어 있듯이 multipart/mixed와 multipart/digest는 최소한 지원해야 할 MIME 타입이다. mixed 파트의 기본 content-type은 text/plain이며, digest의 경우 message/rfc822이다. Multipart/digest는 하나 이상의 메시지를 포워딩 하기 위한 간편한 방법이다.

### Alternative

Multipart/alternative 메시지는 동일한 내용을 다른 형식으로 표현할 때 사용된다. 각각의 파트는 서로 다른 "Content-type" 헤더를 가지며, MIME을 지원하지 않는 클라이언트에서 처리를 쉽게 하고자 표현하기 쉬운 형식에서 복잡한 형식 순으로 메시지에 나타난다. 따라서 메일 클라이언트는 각 파트를 순서대로 검색하여 자신이 표현할 수 있는 마지막 파트를 선택하게 된다. 일부 클라이언트는 이런 순서를 무시한 채 자신이 선호하는 형식을 표시하기도 한다. 일반적으로 오래된 클라이언트를 위해 text/plain 타입의 파트가 먼저 나오고 최신 클라이언트를 위해 text/html 타입의 파트가 나온다.

예전 [스팸 방지 필터는](https://ko.wikipedia.org/wiki/스팸_방지_필터 "wikilink") text/html 파트보다 파싱이 쉽다는 이유로 메시지의 text/plain 파트 만을 검사했다. [스패머](https://ko.wikipedia.org/wiki/스패머 "wikilink")들은 이러한 점을 악용해 메시지의 text/plain 파트에는 평범한 내용을 넣고 대신 text/html에는 광고를 포함하였다. 이런 방식을 막기 위해 anti-spam 소프트웨어는 multipart/alternative 메시지 중 각 파트가 매우 상이한 내용을 가질 경우 이를 스팸 메시지로 처리하는 식으로 해당 메시지를 걸러낸다.

### Related

Multipart/related는 상호 연관된 여러 개의 파트들로 구성된 메시지이다. 각각의 파트들은 root 타입을 중심으로 내부적으로 연결되며, 각 파트를 참조하기 위해서 일반적으로 파트의 content-ID를 사용한다. Multipart/related의 type 파라미터는 root 파트의 content-type을 지정하며 필수 파라미터이다. Start 파라미터는 root 파트의 content-ID를 지정하며 start 파라미터가 없을 경우에는 가장 먼저 나오는 파트가 root 파트가 된다.

Multipart/related의 사용 예로 이미지가 포함된 [HTML](../Page/HTML.md "wikilink") 문서를 들 수 있다. 이 경우 root 파트는 HTML 문서가 되며 HTML에 포함된 이미지들은 뒷따르는 파트로 구성하고 HTML 내부에서 이를 참조하는 식으로 표현할 수 있다.

### Report

Multipart/report 메시지는 메일 서버를 위한 형식화된 데이터를 포함한다. 이 메시지 타입은 text/plain과 message/delivery-status로 나뉜다.

### Signed

Multipart/signed 메시지는 본문과 서명 파트를 갖는다. MIME 헤드를 포함하는 본문 파트는 서명을 생성하기 위해 사용된다. Application/pgp-signature, application/x-pkcs7-signature 등의 서명이 사용된다.

### Encrypted

Multipart/encrypted 메시지 타입은 암호화된 application/octet-stream과 이를 풀기 위한 정보를 갖는 제어 파트로 구분된다.

## 참조

  - RFC 1847 : Security Multiparts for MIME: Multipart/Signed and Multipart/Encrypted.
    RFC 2045 : MIME Part One: Format of Internet Message Bodies.
    RFC 2046 : MIME Part Two: Media Types. N. Freed, [Nathaniel Borenstein](https://ko.wikipedia.org/wiki/Nathaniel_Borenstein "wikilink"). November 1996.
    RFC 2047 : MIME Part Three: Message Header Extensions for Non-ASCII Text. [Keith Moore](https://ko.wikipedia.org/wiki/Keith_Moore "wikilink"). November 1996.
    RFC 4288 : MIME Part Four: Media Type Specifications and Registration Procedures.
    RFC 4289 : MIME Part Four: Registration Procedures. N. Freed, J. Klensin. December 2005.
    RFC 2049 : MIME Part Five: Conformance Criteria and Examples. N. Freed, N. Borenstein. November 1996.
    RFC 2231 : MIME Parameter Value and Encoded Word Extensions: Character Sets, Languages, and Continuations. N. Freed, K. Moore. November 1997.
    RFC 2387 : The MIME Multipart/Related Content-type

## 외부 링크

  - [Blog tracking Internet mail related drafts and standards](https://web.archive.org/web/20061004071705/http://db.org/)
  - [List of IANA registered MIME Media Types](http://www.iana.org/assignments/media-types/)
  - [List of Character Sets](http://www.iana.org/assignments/character-sets)
  - [MIME at the Debian Wiki](http://wiki.debian.org/MIME)
  - [A more detailed overview of MIME](https://web.archive.org/web/20060623063612/http://mgrand.home.mindspring.com/mime.html) (1993)

[분류:인터넷 표준](https://ko.wikipedia.org/wiki/분류:인터넷_표준 "wikilink") [분류:표현 계층 프로토콜](https://ko.wikipedia.org/wiki/분류:표현_계층_프로토콜 "wikilink")