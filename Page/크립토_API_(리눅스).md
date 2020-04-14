> This article is converted from Wikipedia: [크립토 API \(리눅스\)](https://ko.wikipedia.org/wiki/크립토_API_\(리눅스\)).


**크립토 API**(Crypto API)는 [리눅스 커널에서](../Page/리눅스_커널.md "wikilink") 사용하는 암호 프레임워크이며, [IPsec](https://ko.wikipedia.org/wiki/IPsec "wikilink")과 dm-crypt와 같은 암호화된 데이터를 다루는 부분에서 사용한다. 리눅스 커널 버전 2.5.45에서 최초로 도입되었으며\[1\] 자주 사용되는 [블록 암호와](https://ko.wikipedia.org/wiki/블록_암호 "wikilink") [해시 함수를](../Page/해시_함수.md "wikilink") 포함하기 위해 확장되고 있다.

## 사용자 공간 인터페이스

암호화 함수 및 해시 함수를 제공하는 플랫폼은 크게 두 가지 방식으로 나눌 수 있다. [명령어 집합 구조](https://ko.wikipedia.org/wiki/명령어_집합_구조 "wikilink") 자체에 암호화 및 해시 함수를 포함시켜서 [커널 공간이나](https://ko.wikipedia.org/wiki/커널_공간 "wikilink") [사용자 공간에](../Page/사용자_공간.md "wikilink") 있는 모든 프로그램에서 사용할 수 있도록 한 방식과, 프로세서 내부의 장치를 통해서 접근하며 OpenSSL, GnuTLS 등 사용자 공간에서는 커널 드라이버를 통해 접근해야 하는 방식이다. 명령어 집합 자체에 암호화 및 해시 함수가 포함되어 있는 프로세서는 인텔과 AMD의 [AES-NI](../Page/AES-NI.md "wikilink")이며, 커널 드라이버를 사용하는 프로세서는 마벨 Kirkwood 및 [AMD 지오드](../Page/지오드.md "wikilink") 프로세서이다.

크립토 API에서 제공하는 사용자 공간 인터페이스는 다음과 같다.

  - AF_ALG
    네트워크 소켓과 유사한 인터페이스로 접근할 수 있으며, 커널 내부 암호화 엔진에 접근하기 위한 `AF_ALG` 주소 형식을 지원한다.\[2\] 리눅스 커널 버전 2.6.38에 통합되었다.\[3\]<ref>[03c8efc](http://git.kernel.org/?p=linux/kernel/git/torvalds/linux-2.6.git;a=commitdiff;h=03c8efc1ffeb6b82a22c1af8dd908af349563314)

[fe869cd](http://git.kernel.org/?p=linux/kernel/git/torvalds/linux-2.6.git;a=commitdiff;h=fe869cdb89c95d060c77eea20204d6c91f233b53) [8ff5909](http://git.kernel.org/?p=linux/kernel/git/torvalds/linux-2.6.git;a=commitdiff;h=8ff590903d5fc7f5a0a988c38267a3d08e6393a2)</ref> OpenSSL에서 AF_ALG를 지원하기 위한 플러그인이 존재하며, OpenSSL에 통합되기 위해서 버그 트래커에 올라왔으나 2016년에 거절되었다.\[4\]

  - cryptodev
    OpenBSD 암호화 프레임워크 인터페이스인 /dev/crypto를 리눅스로 이식한 코드가 있지만\[5\]\[6\]\[7\] 리눅스 커널에 통합되지는 않았다.

## 같이 보기

  - [마이크로소프트 크립토API](https://ko.wikipedia.org/wiki/마이크로소프트_크립토API "wikilink")

## 각주

[분류:API](https://ko.wikipedia.org/wiki/분류:API "wikilink") [분류:암호 소프트웨어](https://ko.wikipedia.org/wiki/분류:암호_소프트웨어 "wikilink") [분류:리눅스 커널 특징](https://ko.wikipedia.org/wiki/분류:리눅스_커널_특징 "wikilink") [분류:리눅스 보안 소프트웨어](https://ko.wikipedia.org/wiki/분류:리눅스_보안_소프트웨어 "wikilink")

1.
2.
3.  [Linux_2_6_38 changes](http://kernelnewbies.org/Linux_2_6_38#head-6bd372b9e646453417be976d4ff1f31086429b7a)
4.
5.
6.
7.