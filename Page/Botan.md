> This article is converted from Wikipedia: [Botan](https://ko.wikipedia.org/wiki/Botan).


**Botan**은 [BSD 사용 허가서로](https://ko.wikipedia.org/wiki/BSD_사용_허가서 "wikilink") 라이선스된 [암호화](https://ko.wikipedia.org/wiki/암호화 "wikilink") 라이브러리이다.

Botan은 여러 다양한 암호화 알고리즘을 제공한다. 또한 암호와 관련한 포맷, 프로토콜 지원 기능도 제공한다.

Botan 프로젝트의 원 이름은 [OpenCL](https://ko.wikipedia.org/wiki/OpenCL "wikilink")이었다. 2002년 OpenCL에서 Botan으로 이름을 바꾸었다. 2008년 현재 OpenCL이라는 이름은, 전혀 다른 곳인, [애플 (기업)의](https://ko.wikipedia.org/wiki/애플_\(기업\) "wikilink") 그래픽스 카드 프로그래밍 언어에 쓰이는 이름이 되어 있다.\[1\].

2007년, 독일의 연방정보보안국()이 전자여권(ePassports)을 위한 Card Verifiable Certificates 를 Botan에 추가하여 구현한다는 내용의 계약을 플렉스시큐어 사(FlexSecure GmbH)와 맺었다. 수정된 Botan은 InSiTo라는 이름 하에 발매되었다.\[2\].

Botan은 [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink"), FreeBSD, NetBSD, [솔라리스](https://ko.wikipedia.org/wiki/솔라리스_\(운영_체제\) "wikilink"), Mac OS X, 마이크로소프트 윈도 용으로 나와 있다. 1.10 버전까지는 [C++98](https://ko.wikipedia.org/wiki/C++98 "wikilink") 스탠다드에 맞춰 구현되어 있으며, 이후버전은 [C++11](https://ko.wikipedia.org/wiki/C++11 "wikilink") 스탠다드 컴파일러가 필요하다. STL 및 ISO 표준 라이브러리 외에 다른 디펜던시가 없다.

## 사용처

Botan은 분산 리비전 콘트롤 프로그램인 모노톤(Monotone)에 쓰이고 있다.

## 지원하는 알고리즘

지원하는 알고리즘 중 주요한 것은 다음과 같다.

  - RSA, ElGamal, DLIES 공개키 암호화.
  - RSA, DSA, ECDSA, Nyberg-Rueppel, Rabin-Williams 공개키 서명.
  - Diffie-Hellman, ECKAEG 키교환.
  - ECB, CBC, CBC/CTS, CFB, OFB, CTR 블록 사이퍼. EAX 사이퍼 모드.
  - AES (Rijndael)
  - AES 후보였던 Serpent, Twofish, MARS, CAST-256, RC6
  - DES, DES 변종 3DES와 DESX
  - ARC4, Salsa20, Turing, WiderWake4+1 스트림 사이퍼
  - SEED, KASUMI, MISTY1, GOST, Skipjack
  - Blowfish, CAST-128, IDEA, Noekeon, TEA, XTEA, RC2, RC5, SAFER-SK, Square 기타 블록 사이퍼
  - SHA-224, SHA-256, SHA-384, SHA-512, Whirlpool, SHA-1, Tiger, RIPEMD-160, RIPEMD-128, HAS-160, FORK-256 등의 해시

## 각주

## 외부 링크

  -

[분류:C++ 라이브러리](https://ko.wikipedia.org/wiki/분류:C++_라이브러리 "wikilink") [분류:BSD 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:BSD_라이선스_소프트웨어 "wikilink") [분류:전송 계층 보안 구현](https://ko.wikipedia.org/wiki/분류:전송_계층_보안_구현 "wikilink") [분류:암호 소프트웨어](https://ko.wikipedia.org/wiki/분류:암호_소프트웨어 "wikilink")

1.
2.