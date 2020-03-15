> This article is converted from Wikipedia: [OpenSSL](https://ko.wikipedia.org/wiki/OpenSSL).


**OpenSSL**은 [네트워크를](https://ko.wikipedia.org/wiki/컴퓨터_네트워크 "wikilink") 통한 데이터 통신에 쓰이는 [프로토콜](https://ko.wikipedia.org/wiki/프로토콜 "wikilink")인 [TLS와](https://ko.wikipedia.org/wiki/트랜스포트_레이어_보안 "wikilink") [SSL](https://ko.wikipedia.org/wiki/SSL "wikilink")의 [오픈 소스](https://ko.wikipedia.org/wiki/오픈_소스 "wikilink") 구현판이다. [C 언어로](https://ko.wikipedia.org/wiki/C_언어 "wikilink") 작성되어 있는 중심 라이브러리 안에는, 기본적인 암호화 기능 및 여러 유틸리티 함수들이 구현되어 있다.

OpenSSL은 Eric A. Young과 Tim Hudson이 만든 SSLeay에 그 근거를 두고 있다. SSLeay의 개발은 Young과 Hudson이 RSA Security로 적을 옮긴 1998년 12월 이래 비공식적으로 중단되어 있다.

거의 모든 버전의 [유닉스 계열](../Page/유닉스_계열.md "wikilink") [운영 체제](https://ko.wikipedia.org/wiki/운영_체제 "wikilink")([솔라리스](https://ko.wikipedia.org/wiki/솔라리스 "wikilink"), [맥 OS X](https://ko.wikipedia.org/wiki/맥_OS_X "wikilink"), [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink"), BSD 포함) 및 OpenVMS, [윈도우에서](https://ko.wikipedia.org/wiki/마이크로소프트_윈도우 "wikilink") OpenSSL을 이용할 수 있다.

## 주요 버전 배포 현황

각 버전의 정식 출시일을 기준으로 작성하였다.\[1\]

  - OpenSSL 1.1.1 - 출시일: 2018-09-11\[2\]
  - OpenSSL 1.1.0 - 출시일: 2016-08-25
  - OpenSSL 1.0.2 - 출시일: 2015-01-22
  - OpenSSL 1.0.1 - 출시일: 2012-03-14
  - OpenSSL 1.0.0 - 출시일: 2010-03-29
  - OpenSSL 0.9.8 - 출시일: 2005-07-05
  - OpenSSL 0.9.7 - 출시일: 2002-12-31
  - OpenSSL 0.9.6 - 출시일: 2000-09-24
  - OpenSSL 0.9.5 - 출시일: 2000-02-28
  - OpenSSL 0.9.4 - 출시일: 1999-08-09
  - OpenSSL 0.9.3 - 출시일: 1999-05-25
  - OpenSSL 0.9.2b - 출시일: 1999-03-22
  - OpenSSL 0.9.1c - 최초 출시일: 1998-12-23

## 알고리즘

OpenSSL은 각기 다른 다양한 암호화 알고리즘을 지원한다:

  - [암호문](https://ko.wikipedia.org/wiki/암호문 "wikilink")(cipher):
    [AES](https://ko.wikipedia.org/wiki/고급_암호_표준 "wikilink"), [블로피시](../Page/블로피시.md "wikilink"), [Camellia](https://ko.wikipedia.org/wiki/Camellia "wikilink"), [CAST-128](https://ko.wikipedia.org/wiki/CAST-128 "wikilink"), [DES](https://ko.wikipedia.org/wiki/데이터_암호화_표준 "wikilink"), [IDEA](../Page/국제_데이터_암호화_알고리즘.md "wikilink"), [RC2](https://ko.wikipedia.org/wiki/RC2 "wikilink"), [RC4](https://ko.wikipedia.org/wiki/RC4 "wikilink"), [RC5](https://ko.wikipedia.org/wiki/RC5 "wikilink"), [트리플 DES](../Page/트리플_DES.md "wikilink"), [GOST 28147-89](https://ko.wikipedia.org/wiki/GOST_28147-89 "wikilink")
  - [암호학의 해시 함수](https://ko.wikipedia.org/wiki/암호학의_해시_함수 "wikilink"):
    [MD5](../Page/MD5.md "wikilink"), [MD2](https://ko.wikipedia.org/wiki/MD2 "wikilink"), [SHA-1](https://ko.wikipedia.org/wiki/SHA-1 "wikilink"), [SHA-2](https://ko.wikipedia.org/wiki/SHA-2 "wikilink"), [MDC-2](https://ko.wikipedia.org/wiki/MDC-2 "wikilink")
  - [공개 키 암호 방식](https://ko.wikipedia.org/wiki/공개_키_암호_방식 "wikilink"):
    [RSA](https://ko.wikipedia.org/wiki/RSA_암호 "wikilink"), [DSA](../Page/디지털_서명_알고리즘.md "wikilink"), [디피-헬만 키 교환](https://ko.wikipedia.org/wiki/디피-헬만_키_교환 "wikilink"), [타원 암호](https://ko.wikipedia.org/wiki/타원곡선_암호 "wikilink"), [GOST R 34.10-2001](https://ko.wikipedia.org/wiki/GOST_R_34.10-2001 "wikilink")

## 취약점

### 하트블리드

## 같이 보기

  - [LibreSSL](../Page/LibreSSL.md "wikilink")

## 각주

## 외부 링크

  -

  - [OpenSSL Manpages](https://www.openssl.org/docs/manpages.html)

  - [OpenSSL Programming Guide](https://web.archive.org/web/20160629195844/http://h71000.www7.hp.com/doc/83final/ba554_90007/ch04s03.html)

  - [The OpenSSL License and the GPL](https://people.gnome.org/~markmc/openssl-and-the-gpl.html) by Mark McLoughlin

  - [OpenSSL programming tutorial](https://www.ibm.com/developerworks/linux/library/l-openssl/index.html)

  - [OpenSSL Community Wiki](https://wiki.openssl.org/index.php/Main_Page)

[분류:암호 소프트웨어](https://ko.wikipedia.org/wiki/분류:암호_소프트웨어 "wikilink") [분류:전송 계층 보안 구현](https://ko.wikipedia.org/wiki/분류:전송_계층_보안_구현 "wikilink") [분류:자유 보안 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_보안_소프트웨어 "wikilink") [분류:1998년 소프트웨어](https://ko.wikipedia.org/wiki/분류:1998년_소프트웨어 "wikilink") [분류:C 라이브러리](https://ko.wikipedia.org/wiki/분류:C_라이브러리 "wikilink")

1.  [OpenSSL - Project Newsflash\!](https://www.openssl.org/news/)
2.  <https://www.openssl.org/blog/blog/2018/09/11/release111/>