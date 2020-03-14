> This article is converted from Wikipedia: [SQRL](https://ko.wikipedia.org/wiki/SQRL).


**안전하고, 빠르고, 신뢰있는 로그인**(Secure, Quick, Reliable Login)의 약자인 **SQRL**(안전한 QR 로그인이라는 의미에서 Secure QR Login 으로 쓰기도 한다) 은 웹사이트 등에서 안전하게 로그인하고 인증받기 위한 공개표준이다. SQRL은 일반적으로 [QR code를](https://ko.wikipedia.org/wiki/QR_code "wikilink") 사용하는데, 이를 통해 사용자가 ID와 비밀번호를 사용하지 않고서도 익명으로 자신을 인증할 수 있다. 이러한 방법은 무차별 암호대입 공격이나 의도치 않은 정보노출 등의 위협으로부터 현재까지는 안전하다고 여겨지고 있다. 또한 사용자뿐만 아니라 인증을 요구하는 부분에서 이루어지는 중요한 보안상의 부담을 덜어준다. SQRL은 2013년 10월 Gibson Research Corporation에서 근무하는 [Steve Gibson에](https://ko.wikipedia.org/wiki/Steve_Gibson "wikilink") 의해 제3자에게 정보의 노출 없이 인증 프로토콜 과정을 단순화하는 방법으로 처음 제안되었다.

## 개발동기

이 프로토콜은 identity fragmentation 문제에 대한 해결책으로서 제안되었다. 이 기술은 기존의 [OAuth](https://ko.wikipedia.org/wiki/OAuth "wikilink")와 [OpenID](https://ko.wikipedia.org/wiki/OpenID "wikilink") 방식보다 향상된 기능을 제공하는데, 이를 통해 제3자에게 정보를 노출하지 않고도 인증이 가능하다. 더불어 SQRL은 로그인 과정을 단순화하는 과정을 사용하는데, 이것은 [LastPass](https://ko.wikipedia.org/wiki/LastPass "wikilink")와 같은 비밀번호 관리자 [password manager에서도](https://ko.wikipedia.org/wiki/password_manager "wikilink") 사용할 수 있는 방법이다.

## 사용방법

웹사이트에서 이 프로토콜을 사용하기 위해서는 두 가지 요소가 필요하다. 하나는 구현과정인데 이는 웹서비스의 일종으로서 [QR code](https://ko.wikipedia.org/wiki/QR_code "wikilink") 또는 이 프로토콜의 내용에 따라 생성된 특정 URL을 표시해주어 인증한다. 다른 하나는 브라우저 플러그인 또는 모바일 애플리케이션인데 이를 통해 안전하게 인증할 수 있도록 [QR code를](https://ko.wikipedia.org/wiki/QR_code "wikilink") 읽는다.

SQRL 사용자는 단방향 함수를 사용한다. 쉽게 말해 비밀번호를 암호화 할 수는 있되 암호화된 내용을 다시 원래의 비밀번호로 되돌릴 수 없게 함으로써 무차별 암호대입 공격이나 다른 방법들을 무력화시킨다.

## 피싱 방어

SQRL은 그 포로토몰 자체가 피싱으로부터 방호받을 수 있는 속성을 갖고있으나, 완벽하게 보호되는 것은 아닌 것으로 알려져 있다.\[1\]

## 각주

<references />

[분류:인증 방법](https://ko.wikipedia.org/wiki/분류:인증_방법 "wikilink")

1.  "Details about phishing defenses and limitations". grc.com. 2013-12-06. Retrieved 2013-12-06.