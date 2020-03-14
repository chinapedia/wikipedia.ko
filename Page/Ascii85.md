> This article is converted from Wikipedia: [Ascii85](https://ko.wikipedia.org/wiki/Ascii85).


**Ascii85** 또는 **Base85** 불리는 이것은 Paul E. Rutter가 유틸리티 [:en:btoa](https://ko.wikipedia.org/wiki/:en:btoa "wikilink")를 위해 만든 [:en:binary-to-text encoding](https://ko.wikipedia.org/wiki/:en:binary-to-text_encoding "wikilink") 방법으로 5개의 [ASCII](https://ko.wikipedia.org/wiki/ASCII "wikilink") 문자로 4 바이트의 [이진 데이터를](https://ko.wikipedia.org/wiki/이진_데이터 "wikilink") 표현한다. ASCII 한 문자가 8비트라면 이 방법으로 하면 원본이 ¹⁄₄만큼 더 커진다. 이것은 4개의 문자로 3 바이트를 표현해서 ¹⁄₃만큼 더 커지는 [:en:uuencode](https://ko.wikipedia.org/wiki/:en:uuencode "wikilink")나 [베이스64](https://ko.wikipedia.org/wiki/베이스64 "wikilink")보다 효율적이다.

이것은 [Adobe의](https://ko.wikipedia.org/wiki/어도비_시스템즈 "wikilink") [포스트스크립트](https://ko.wikipedia.org/wiki/포스트스크립트 "wikilink")와 [PDF](https://ko.wikipedia.org/wiki/PDF "wikilink") 파일 형식에 사용된다.

## 기본 구상

binary-to-text encoding은 사람이 읽을 수 있는([:en:human-readable](https://ko.wikipedia.org/wiki/:en:human-readable "wikilink")) 문자만을 전송할 수 있는 기존 통신 프로토콜 위에서 [이진 데이터를](https://ko.wikipedia.org/wiki/이진_데이터 "wikilink") 다루기 위해서 필요했다. 이런 환경에서 문자는 7 비트만을 사용하고 그 마저도 일부 제어 문자를 빼야하므로 데이터의 전송에 사용할 수 있는 문자는 95개 뿐이다.

4 바이트는 2<sup>32</sup> = 4,294,967,296 가지의 값을 가지고, 5자리 85 진수([:en:radix](https://ko.wikipedia.org/wiki/:en:radix "wikilink"))는 85<sup>5</sup> = 4,437,053,125 가지의 값이 가능하므로 이걸로 32비트 값을 충분히 표현할 수 있다. 5자리의 84 진수는 84<sup>5</sup> = 4,182,119,424 가지 값만을 가지기 때문에 85가 5자리로 4바이트를 표현해 낼 수 있는 최소값이라 이것이 선택되었다.

인코딩은 4바이트를 [big-endian으로](https://ko.wikipedia.org/wiki/엔디언 "wikilink") 묶어 32비트 수를 얻는 것에서 시작한다. 이것을 85진수로 바꾼다. 85를 연속해서 나누면서 나머지들을 얻는 과정이다. 그렇게 5자리의 85진수가 얻어지면, 각 자리에 33를 더해서 33 ("\!")에서 117 ("u")까지의 ASCII 문자로 바꾸는 것이다.

데이터가 모두 0인 경우는 상당히 흔하기 때문에 예외적으로 데이터 압축을 위해서 "`z`" 한 문자로 인코딩한다. "`!!!!!`"가 아니다.

디코딩했을 때 (인코딩 했을 때 "`s8W-!`")보다 큰 수는 에러다. as will "`z`" characters in the middle of a group. White space between the characters is ignored and may occur anywhere to accommodate line-length limitations.

Ascii85의 한 가지 단점은 인코딩 데이터가 backslash나 quote 같은 [:en:escape character를](https://ko.wikipedia.org/wiki/:en:escape_character "wikilink") 포함할 수 있다는 것인데, 이것들은 많은 프로그래밍 언어나 일부 문자 기반의 프로토콜에서 특별한 의미를 가지므로 문제가 될 수 있다. Z85는 소스 코드에서도 안전하도록 설계된 것이다.\[1\]

## 같이 보기

  - [Base32](https://ko.wikipedia.org/wiki/Base32 "wikilink")
  - [Base36](https://ko.wikipedia.org/wiki/Base36 "wikilink")
  - [Base64](https://ko.wikipedia.org/wiki/Base64 "wikilink")
  - [Binary-to-text encoding](https://ko.wikipedia.org/wiki/Binary-to-text_encoding "wikilink") for a comparison of various encoding algorithms

## 각주

<references />

## 외부 링크

  - [BasE91](http://base91.sourceforge.net/)
  - [btoa](http://www.ibiblio.org/pub/packages/ccic/software/unix/utils/btoa.c) and [atob](http://www.ibiblio.org/pub/packages/ccic/software/unix/utils/atob.c) source code from 1990
  - [PostScript Language Reference](http://www.adobe.com/products/postscript/pdfs/PLRM.pdf) (Adobe) - see ASCII85Encode Filter
  - Encoder/Decoder implementations in several languages:
      - [awk](http://sites.google.com/site/dannychouinard/Home/unix-linux-trinkets/little-utilities/base64-and-base85-encoding-awk-scripts)
      - [C\#](http://blog.codinghorror.com/c-implementation-of-ascii85/)
      - [F\#](http://blog.wezeku.com/2010/07/01/f-ascii85-module/)
      - [Java](https://web.archive.org/web/20151229122850/http://java.freehep.org/) [(documentation)](https://web.archive.org/web/20160304035222/http://java.freehep.org/freehep-io/apidocs/org/freehep/util/io/ASCII85.html)
      - [Perl](http://b2d-f9r.blogspot.com/2010/05/ascii85-encoder-in-perl-take-2.html)
      - [ASCII85-Tools, Perl command-line utilities](http://sourceforge.net/projects/ascii85-tools/) - C version also available.
      - [MPPerl::Convert::ASCII85::XS, a Perl module with time-critical code written in C](http://sourceforge.net/projects/mpperl-convert-ascii85-xs/)
      - [Python](https://ko.wikipedia.org/wiki/:sourceforge:projects/pyascii85 "wikilink")
      - [Yet another RFC1924/ASCII85/IPv6 Base85 Python implementation (APLv2)](http://code.google.com/p/python-mom/source/browse/mom/codec/base85.py)
      - RFC1924/ASCII85 [C library and command line tool](https://github.com/woolstar/test/tree/master/encode)
      - [JavaScript](http://github.com/noseglid/base85/)

[분류:문자 인코딩](https://ko.wikipedia.org/wiki/분류:문자_인코딩 "wikilink")

1.  ["Z85 - ZeroMQ Base-85 Encoding Algorithm"](http://rfc.zeromq.org/spec:32)