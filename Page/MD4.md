> This article is converted from Wikipedia: [MD4](https://ko.wikipedia.org/wiki/MD4).


**MD4 메시지-다이제스트 알고리즘**(MD4 Message-Digest Algorithm)은 1990년 [로널드 라이베스트가](https://ko.wikipedia.org/wiki/로널드_라이베스트 "wikilink") 개발한 [암호화 해시 함수이다](https://ko.wikipedia.org/wiki/암호화_해시_함수 "wikilink").\[1\] 다이제스트 길이는 128비트이다. 이 알고리즘은 [MD5](https://ko.wikipedia.org/wiki/MD5 "wikilink"), [SHA-1](https://ko.wikipedia.org/wiki/SHA-1 "wikilink"), [RIPEMD](https://ko.wikipedia.org/wiki/RIPEMD "wikilink") 알고리즘과 같은 이후의 디자인에 영향을 주었다. "MD"는 "메시지 다이제스트"(Message Digest)의 준말이다.

MD4는 마이크로소프트 윈도우 NT, XP, 비스타, 7, 8, 10에서 [NTLM](https://ko.wikipedia.org/wiki/NT_LAN_매니저 "wikilink") 암호 파생 키 다이제스트를 연산하기 위해 사용된다.\[2\]

## MD4 해시

128비트(16바이트) MD4 해시(메시지 다이제스트)는 일반적으로 32자리 [십육진수로](https://ko.wikipedia.org/wiki/십육진법 "wikilink") 표현한다. 다음은 43바이트 [아스키](https://ko.wikipedia.org/wiki/아스키 "wikilink") 입력 및 그와 일치하는 MD4 해시를 나타낸 것이다:

`MD4("The quick brown fox jumps over the lazy ``og")`
`= 1bee69a46ba811185c194762abaeae90`

이 메시지의 사소한 변경도 완전히 다른 해시를 만들어내는데, 이를테면 d가 c로 바뀌는 점이다:

`MD4("The quick brown fox jumps over the lazy ``og")`
`= b86e130ce7028da59e672d56ad0113df`

길이가 0인 문자열의 해시는 다음과 같다:

`MD4("") = 31d6cfe0d16ae931b73c59d7e0c089c0`

## MD4 테스트 벡터

다음의 테스트 벡터는 RFC 1320 (MD4 메시지 다이제스트 알고리즘)에 정의되어 있다.

`MD4 ("") = 31d6cfe0d16ae931b73c59d7e0c089c0`
`MD4 ("a") = bde52cb31de33e46245e05fbdbd6fb24`
`MD4 ("abc") = a448017aaf21d8525fc10ae87aa6729d`
`MD4 ("message digest") = d9130a8164549fe818874806e1c7014b`
`MD4 ("abcdefghijklmnopqrstuvwxyz") = d79e1c308aa5bbcdeea8ed63df412da9`
`MD4 ("ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789") = 043f8582f241db351ce627e153e7f0e4`
`MD4 ("12345678901234567890123456789012345678901234567890123456789012345678901234567890") = e33b4ddc9c38f2199c3e7b164fcc0536`

## MD4 충돌 예제

다음이 있다고 가정하면:

` k1 = 839c7a4d7a92cb`****`678a5d5`****`9eea5a7573c8a74deb366c3dc20a083b69f5d2a3bb3719dc69891e9f95e809fd7e8b23ba6318ed`****`45e51fe39708bf9427e9c3e8b9`
` k2 = 839c7a4d7a92cb`****`678a5d5`****`9eea5a7573c8a74deb366c3dc20a083b69f5d2a3bb3719dc69891e9f95e809fd7e8b23ba6318ed`****`45e51fe39708bf9427e9c3e8b9`

k1 ≠ k2이지만, MD4(k1) = MD4(k2) = 4d7e6a1defa93d2dde05b45d864c429b이다. k1과 k2의 16진 자리가 입력 문자열의 한 바이트를 정의하며, 여기서 길이는 64바이트로 된다.

## 같이 보기

  - [MD2](https://ko.wikipedia.org/wiki/MD2 "wikilink")
  - [MD5](https://ko.wikipedia.org/wiki/MD5 "wikilink")
  - [MD6](https://ko.wikipedia.org/wiki/MD6 "wikilink")

## 각주

## 외부 링크

  - RFC 1320 - Description of MD4 by Ron Rivest

  - RFC 6150 - MD4 to Historic Status

  -
[분류:암호화 해시 함수](https://ko.wikipedia.org/wiki/분류:암호화_해시_함수 "wikilink")

1.
2.