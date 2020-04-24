> This article is converted from Wikipedia: [TLS 구현의 비교](https://ko.wikipedia.org/wiki/TLS_구현의_비교).


[전송 계층 보안](../Page/전송_계층_보안.md "wikilink") 프로토콜은 네트워크 간의 통신을 보호하는 기능을 제공한다. 이 **TLS 구현의 비교**에서는 가장 알려진 라이브러리를 비교한다.

모든 비교 범주에서 설명 섹션에 나열되어있는 각 구현의 안정 버전을 사용하며 이 비교는 TLS 프로토콜에 직접 관련된 기능에 한정한다.

## 개요

<table>
<thead>
<tr class="header">
<th><p><strong>구현</strong></p></th>
<th><p><strong>개발자</strong></p></th>
<th><p><strong>오픈 소스</strong></p></th>
<th><p><strong>소프트웨어 라이센스</strong></p></th>
<th><p><strong>저작권 소유자</strong></p></th>
<th><p><strong>언어</strong></p></th>
<th><p><strong>최신 안정 버전 릴리스 날짜</strong></p></th>
<th><p><strong>출처</strong></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/:en:GnuTLS" title="wikilink">GnuTLS</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/:en:GnuTLS" title="wikilink">GnuTLS project</a></p></td>
<td><p>Yes</p></td>
<td><p><a href="../Page/GNU_약소_일반_공중_사용_허가서.md" title="wikilink">GNU LGPLv2.1 +</a></p></td>
<td><p><a href="../Page/자유_소프트웨어_재단.md" title="wikilink">자유 소프트웨어 재단</a></p></td>
<td><p><a href="../Page/C_(프로그래밍_언어).md" title="wikilink">C</a></p></td>
<td><table>
<tbody>
<tr class="odd">
<td><p><strong>stable</strong></p></td>
<td><p>3.5.18 / 2018년 2월 16일 (4 개월 전) <small></small>[1]</p></td>
</tr>
<tr class="even">
<td><p><strong>stable-next</strong></p></td>
<td><p>3.6.2 / 2018년 2월 16일 (4 개월 전) <small></small>[2]</p></td>
</tr>
</tbody>
</table></td>
<td><p>EU (Greece and Sweden)</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/OpenSSL.md" title="wikilink">OpenSSL</a></p></td>
<td><p><a href="../Page/OpenSSL.md" title="wikilink">OpenSSL project</a></p></td>
<td><p>Yes</p></td>
<td><p><a href="../Page/OpenSSL.md" title="wikilink">OpenSSL 듀얼 라이센스</a>-SSLeay</p></td>
<td><p>Eric Young, Tim Hudson, Sun OpenSSL project 등</p></td>
<td><p><a href="../Page/C_(프로그래밍_언어).md" title="wikilink">C</a> , <a href="../Page/어셈블리어.md" title="wikilink">어셈블리어</a></p></td>
<td><p>1.1.0h - 2018년 3월 27일 (2 개월 전) <small></small>[3] 1.0.2o - 2018년 3월 27일 (2 개월 전)[4]</p></td>
<td><p>Australia / EU</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/wolfSSL" title="wikilink">wolfSSL</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/wolfSSL" title="wikilink">wolfSSL</a></p></td>
<td><p>Yes</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/GNU_일반_공중_사용권" title="wikilink">GNU GPLv2 + 상용 라이센스</a></p></td>
<td><p>wolfSSL Inc.</p></td>
<td><p><a href="../Page/C_(프로그래밍_언어).md" title="wikilink">C</a></p></td>
<td><p>3.13.0 - 2017년 12월 21일 (5 개월 전) <small></small>[5]</p></td>
<td><p>US</p></td>
</tr>
<tr class="even">
<td><p><strong>구현</strong></p></td>
<td><p><strong>개발자</strong></p></td>
<td><p><strong>오픈 소스</strong></p></td>
<td><p><strong>소프트웨어 라이센스</strong></p></td>
<td><p><strong>저작권 소유자</strong></p></td>
<td><p><strong>언어</strong></p></td>
<td><p><strong>최신 안정 버전 릴리스 날짜</strong></p></td>
<td><p><strong>출처</strong></p></td>
</tr>
</tbody>
</table>

## 프로토콜 지원

TLS 프로토콜에는 여러 버전이 존재한다. SSL 2.0은 심각한 약점을 가지고 폐지 예정이다. SSL 3.0 (1996)과 TLS 1.0 (1999)는 2001년에 Serge Vaudenay 의해 설명된 CBC 패딩 두 가지 약점을 그대로 뒤따르고 있다. TLS 1.1 (2006)는 CBC 블록 암호에 임의의 초기화 벡터 (IV)를 사용하도록 전환하여 여러 문제 중 하나만 해결했던 반면, 안전한 pad-mac-encrypt 대신해 mac-pad-encrypt 문제있는 사용은 RFC7366로 처리되었다. TLS 1.1 랜덤 IV에 상당하는 SSL 3.0 및 TLS 1.0의 해결 방법은 2011년 후반 많은 구현에서 널리 채용되고 있었다. 보안 관점에서는 TLS 1.0, 1.1, 1.2의 모든 기존 버전이 기본 프로토콜에서 동등한 강도를 가지고 NIST SP800-57에 따라서 적어도 2030년까지는 128 비트 보안에 적합하다. 2014년에는 SSL 3.0 POODLE의 취약점이 발견되었는데, 이것은 CBC의 알려진 취약점을 이용하여 브라우저에서 사용되는 안전하지 않은 TLS 버전의 폴백 협상을 할 것이다.

TLS 1.2 (2008)는 기본 프로토콜의 최신 버전이며, 디지털 서명에 사용되는 해시를 식별하는 수단을 도입했다. SSL 3.0 의 보수적인 선택 (rsa, sha1 + md5)에서 미래의 디지털 서명 (rsa, sha256 / sha384 / sha512)에 대해 강력한 해쉬 함수를 사용할 수 있도록 하는 한편, TLS 1.2 프로토콜 변경은 기본 디지털 서명을 고의적으로 상당히 많이 약화시키면서 (rsa, sha1)는 물론 심지어 (rsa, md5)까지 제공한다.

데이터 그램 전송 계층 보안 (DTLS 혹은 Datagram TLS) 1.0은 패킷 손실과 패킷의 정렬을 허용해야 하는 패킷 기반 전송 계층의 TLS 1.1을 변경 한 것이다. TLS 1.2를 기반으로 한 DTLS 1.2 개정판은 2012 년 1월에 공개되었다.

SSL 2.0과 SSL 3.0에는 알려진 취약점이 존재한다. 예측 가능한 IV (간단한 해결 방법이 존재함)을 제외하고 현재 알려진 모든 취약점은 TLS 1.0 / 1.1 / 1.2 와 같은 모든 버전에 영향을 미친다.

| **구현**                                                        | **[SSL 2.0](../Page/전송_계층_보안.md "wikilink") (안전하지 않음)**<small></small><small>\[6\]</small>   | **[SSL 3.0](../Page/전송_계층_보안.md "wikilink") (안전하지 않음)** <small></small><small>\[7\]</small>  | **[TLS 1.0](../Page/전송_계층_보안.md "wikilink")** <small></small><small>\[8\]</small>  | **[TLS 1.1](../Page/전송_계층_보안.md "wikilink")** <small></small><small>\[9\]</small>  | **[TLS 1.2](../Page/전송_계층_보안.md "wikilink")** <small></small><small>\[10\]</small> | **[TLS 1.3](../Page/전송_계층_보안.md "wikilink")** **(초안)**<small>\[11\]</small> <small>\[12\]</small> | **DTLS 1.0** <small></small><small>\[13\]</small> | **DTLS 1.2** <small></small><small>\[14\]</small> |
| ------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------- | ------------------------------------------------- |
| [GnuTLS](https://ko.wikipedia.org/wiki/:en:GnuTLS "wikilink") | No                                                                                           | 기본적으로 비활성화 <small></small><small>\[15\]</small>                                              | Yes                                                                                | Yes                                                                                | Yes                                                                                |                                                                                                   | Yes                                               | Yes                                               |
| [OpenSSL](../Page/OpenSSL.md "wikilink")                      | No <small></small><small>\[16\]</small>                                                      | 기본적으로 활성화                                                                                    | Yes                                                                                | Yes <small></small><small>\[17\]</small>                                           | Yes <small></small><small>\[18\]</small>                                           | Yes                                                                                               | Yes                                               | Yes <small></small><small>\[19\]</small>          |
| [wolfSSL](https://ko.wikipedia.org/wiki/wolfSSL "wikilink")   | No                                                                                           | 기본적으로 비활성화 <small></small><small>\[20\]</small>                                              | Yes                                                                                | Yes                                                                                | Yes                                                                                | Yes <small></small><small>\[21\]</small>                                                          | Yes                                               | Yes                                               |
| **구현**                                                        | **[SSL 2.0](../Page/전송_계층_보안.md "wikilink") (안전하지 않음)** <small></small><small>\[22\]</small> | **[SSL 3.0](../Page/전송_계층_보안.md "wikilink") (안전하지 않음)** <small></small><small>\[23\]</small> | **[TLS 1.0](../Page/전송_계층_보안.md "wikilink")** <small></small><small>\[24\]</small> | **[TLS 1.1](../Page/전송_계층_보안.md "wikilink")** <small></small><small>\[25\]</small> | **[TLS 1.2](../Page/전송_계층_보안.md "wikilink")** <small></small><small>\[26\]</small> | **[TLS 1.3](../Page/전송_계층_보안.md "wikilink")** **(초안)** <small>\[27\]\[28\]</small>                | **DTLS 1.0** <small></small><small>\[29\]</small> | **DTLS 1.2** <small></small><small>\[30\]</small> |

## 미국 국가 안보국 (NSA) Suite B 암호화

[NSA Suite B 암호화](https://ko.wikipedia.org/wiki/:en:NSA_Suite_B_Cryptography "wikilink") ( RFC 6460 )에 필요한 구성 요소 :

·        키 크기가 128 및 256 비트 [Advanced Encryption Standard (AES)](../Page/고급_암호화_표준.md "wikilink"). 트래픽 범위에 대해서는, AES는 대역폭이 낮은 경우엔 카운터 모드 (CTR)에서 사용하고 높은 대역폭의 경우 Galois / Counter Mode (GCM)에서 사용 할 필요가있다 ([블록 암호화 / 암호 사용 모드](../Page/블록_암호_운용_방식.md "wikilink") 참조) - [대칭 키 암호화](../Page/대칭_키_암호.md "wikilink")

·        [타원 곡선 전자 서명 알고리즘 (ECDSA)](https://ko.wikipedia.org/wiki/:en:Elliptic_Curve_Digital_Signature_Algorithm "wikilink")- [전자 서명](../Page/전자서명.md "wikilink")

·        [디피 헬만 곡선 (ECDH)](../Page/디피-헬먼_키_교환.md "wikilink") - [키 합의](https://ko.wikipedia.org/wiki/:en:Key_agreement "wikilink")

·        [SHA-2](../Page/SHA-2.md "wikilink") (SHA-256 및 SHA-384) - [메시지 다이제스트](../Page/암호화_해시_함수.md "wikilink")

각각의 CNSSP-15에 대하여 256 비트의 타원 곡선(FIPS 186-2로 지정), SHA-256 및 128 비트 AES 는 '[기밀 (Secret)](https://ko.wikipedia.org/wiki/:en:Security_clearance#Secret "wikilink")'수준으로 분류되는 정보를 보호하기 위한 것임에 반해 '[최고 기밀 (Top Secret)](https://ko.wikipedia.org/wiki/:en:Security_clearance#Top_Secret "wikilink")' 의 정보를 보호하기 위해서는 384 비트의 타원 곡선 (FIPS 186-2로 지정), SHA-384 및 256 비트 잠금 장치 AES가 필요하다.

| **구현**                                                        | **[TLS 1.2](../Page/전송_계층_보안.md "wikilink") Suite B** |
| ------------------------------------------------------------- | ----------------------------------------------------- |
| [GnuTLS](https://ko.wikipedia.org/wiki/:en:GnuTLS "wikilink") | Yes                                                   |
| [OpenSSL](../Page/OpenSSL.md "wikilink")                      | Yes <small></small>\[31\]                             |
| [wolfSSL](https://ko.wikipedia.org/wiki/wolfSSL "wikilink")   | Yes                                                   |
| **구현**                                                        | **TLS 1.2 Suite B**                                   |

## 인증

| **구현**                                                                                             | **FIPS 140-1 , FIPS 140-2** <small></small><small>\[32\]</small>                                                                                                                              | **임베디드 FIPS 솔루션** |
| -------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------- |
| [GnuTLS](https://ko.wikipedia.org/wiki/:en:GnuTLS "wikilink") <small></small><small>\[33\]</small> | Red Hat Enterprise Linux GnuTLS Cryptographic Module (\# 2780)                                                                                                                                |                   |
| [OpenSSL](../Page/OpenSSL.md "wikilink") <small>\[34\]</small>                                     | OpenSSL FIPS Object Module : 1.0 (\# 624), 1.1.1 (\# 733), 1.1.2 (\# 918), 1.2, 1.2.1, 1.2.2, 1.2.3 or 1.2.4 (\# 1051) 2.0 2.0.1, 2.0.2, 2.0.3, 2.0.4, 2.0.5, 2.0.6, 2.0.7 or 2.0.8 (\# 1747) |                   |
| [wolfSSL](https://ko.wikipedia.org/wiki/wolfSSL "wikilink") <small></small><small>\[35\]</small>   | wolfCrypt FIPS Module : 3.6.0 (\# 2425) See details on NIST certificate for validated Operating Environments                                                                                  | Yes               |
| **구현**                                                                                             | **FIPS 140-1 , FIPS 140-2**                                                                                                                                                                   | **임베디드 FIPS 솔루션** |

## 키 교환 알고리즘 (인증서 만)

이 섹션에서는 다양한 구현에서 사용 가능한 인증서 검증 기능을 나타낸다.

| **구현**                                                        | **[RSA](../Page/RSA_암호.md "wikilink")** <small></small><small>\[36\]</small> | **[RSA](../Page/RSA_암호.md "wikilink") -EXPORT (안전하지 않음)**<small></small><small>\[37\]</small>  | **[디피 - 헬만 키 교환](../Page/디피-헬먼_키_교환.md "wikilink") -RSA ( Forward secrecy )** <small></small><small>\[38\]</small> | **[디피 - 헬만 키 교환](../Page/디피-헬먼_키_교환.md "wikilink") -DSS ( Forward secrecy )** <small></small><small>\[39\]</small> | **ECDH -ECDSA** <small></small><small>\[40\]</small> | **ECDHE - ECDSA (forward secrecy )**<small></small> <small>\[41\]</small> | **ECDH- RSA** <small></small><small>\[42\]</small> | **ECDHE - RSA (forward secrecy)**<small></small> <small>\[43\]</small>  | **GOST 표준 R 34.10-94, 34.10-2001** <small></small><small>\[44\]</small> |
| ------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------- | ------------------------------------------------------------------------- | -------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| [GnuTLS](https://ko.wikipedia.org/wiki/:en:GnuTLS "wikilink") | Yes                                                                          | No                                                                                             | Yes                                                                                                                | 기본적으로 비활성화 <small></small><small>\[45\]</small>                                                                    | No                                                   | Yes                                                                       | No                                                 | Yes                                                                     | No                                                                      |
| [OpenSSL](../Page/OpenSSL.md "wikilink")                      | Yes                                                                          | No <small></small><small>\[46\]</small>                                                        | Yes                                                                                                                | 기본적으로 비활성화 <small></small><small>\[47\]</small>                                                                    | Yes                                                  | Yes                                                                       | Yes                                                | Yes                                                                     | Yes <small></small><small>\[48\]</small>                                |
| [wolfSSL](https://ko.wikipedia.org/wiki/wolfSSL "wikilink")   | Yes                                                                          | No                                                                                             | Yes                                                                                                                | No                                                                                                                 | Yes                                                  | Yes                                                                       | Yes                                                | Yes                                                                     | No                                                                      |
| **구현**                                                        | **[RSA](../Page/RSA_암호.md "wikilink")** <small></small><small>\[49\]</small> | **[RSA](../Page/RSA_암호.md "wikilink") -EXPORT (안전하지 않음)** <small></small><small>\[50\]</small> | **디피 - 헬만 키 교환 - RSA( Forward secrecy )** <small></small><small>\[51\]</small>                                     | **디피 - 헬만 키 교환 - DSS( Forward secrecy )** <small></small><small>\[52\]</small>                                     | **ECDH -ECDSA** <small></small><small>\[53\]</small> | **ECDHE - ECDSA (forward secrecy )** <small></small><small>\[54\]</small> | **ECDH -RSA** <small></small><small>\[55\]</small> | **ECDHE - RSA (forward secrecy )**<small></small> <small>\[56\]</small> | **GOST 표준 R 34.10-94, 34.10-2001** <small></small><small>\[57\]</small> |

## 키 교환 알고리즘 (대체 키 교환)

| **구현**                                                        | **SRP** <small></small><small>\[58\]</small> | **SRP -[DSS](../Page/디지털_서명_알고리즘.md "wikilink")** <small></small><small>\[59\]</small> | **SRP -RSA** <small></small><small>\[60\]</small> | **PSK -RSA** <small></small><small>\[61\]</small> | **PSK** <small></small><small>\[62\]</small> | **DHE - PSK ( [forward secrecy](https://ko.wikipedia.org/wiki/:en:Forward_secrecy "wikilink") )** <small></small><small>\[63\]</small> | **ECDHE - PSK ( [forward secrecy](https://ko.wikipedia.org/wiki/:en:Forward_secrecy "wikilink") )** <small></small><small>\[64\]</small> | **KRB5** <small></small><small>\[65\]</small> | **DH -ANON** <small></small><small>\[66\]</small> **(안전하지 않음)** | **ECDH -ANON** <small></small><small>\[67\]</small> **(안전하지 않음)** |
| ------------------------------------------------------------- | -------------------------------------------- | -------------------------------------------------------------------------------------- | ------------------------------------------------- | ------------------------------------------------- | -------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------- | --------------------------------------------------------------- | ----------------------------------------------------------------- |
| [GnuTLS](https://ko.wikipedia.org/wiki/:en:GnuTLS "wikilink") | Yes                                          | Yes                                                                                    | Yes                                               | Yes                                               | Yes                                          | Yes                                                                                                                                    | Yes                                                                                                                                      | No                                            | 기본적으로 비활성화                                                      | 기본적으로 비활성화                                                        |
| [OpenSSL](../Page/OpenSSL.md "wikilink")                      | Yes                                          | Yes                                                                                    | Yes                                               | Yes                                               | Yes                                          | Yes                                                                                                                                    | Yes                                                                                                                                      | Yes <small></small><small>\[68\]</small>      | 기본적으로 비활성화<small></small> <small>\[69\]</small>                 | 기본적으로 비활성화 <small>\[70\]</small>                                  |
| [wolfSSL](https://ko.wikipedia.org/wiki/wolfSSL "wikilink")   | No                                           | No                                                                                     | No                                                | No                                                | Yes                                          | No                                                                                                                                     | Yes <small></small><small>\[71\]</small>                                                                                                 | No                                            | No                                                              | No                                                                |
| **구현**                                                        | **SRP**<small></small>\[72\]                 | **SRP - [DSS](../Page/디지털_서명_알고리즘.md "wikilink")** <small></small>\[73\]               | **SRP - RSA** <small></small>\[74\]               | **PSK - RSA** <small></small>\[75\]               | **PSK** <small></small>\[76\]                | **DHE - PSK ( [forward secrecy](https://ko.wikipedia.org/wiki/:en:Forward_secrecy "wikilink") )** <small></small>\[77\]                | **ECDHE - PSK ( [forward secrecy](https://ko.wikipedia.org/wiki/:en:Forward_secrecy "wikilink") )** <small></small>\[78\]                | **KRB5** <small></small>\[79\]                | **DH -ANON** <small></small>\[80\] **(안전하지 않음)**                | **ECDH -ANON** <small></small>\[81\] **(안전하지 않음)**                |

## 인증서 검증 방법

| **구현**                                                        | **응용 프로그램 정의** | **PKIX 경로 확인** <small></small><small>\[82\]</small> | **CRL** <small></small><small>\[83\]</small> | **OCSP** <small></small><small>\[84\]</small> | **DANE (DNSSEC)** <small></small><small>\[85\]</small> | **Trust on First Use (TOFU)** |
| ------------------------------------------------------------- | -------------- | --------------------------------------------------- | -------------------------------------------- | --------------------------------------------- | ------------------------------------------------------ | ----------------------------- |
| [GnuTLS](https://ko.wikipedia.org/wiki/:en:GnuTLS "wikilink") | Yes            | Yes                                                 | Yes                                          | Yes                                           | Yes                                                    | Yes                           |
| [OpenSSL](../Page/OpenSSL.md "wikilink")                      | Yes            | Yes                                                 | Yes                                          | Yes                                           | Yes                                                    | No                            |
| [wolfSSL](https://ko.wikipedia.org/wiki/wolfSSL "wikilink")   | Yes            | Yes                                                 | Yes                                          | Yes                                           | No                                                     | No                            |
| **구현**                                                        | **응용 프로그램 정의** | **PKIX 경로 확인** <small></small>\[86\]                | **CRL** <small></small>\[87\]                | **OCSP** <small></small>\[88\]                | **DANE (DNSSEC)** <small></small>\[89\]                | **Trust on First Use (TOFU)** |

## 암호화 알고리즘

| **구현**                                                              | **[블록 암호화](https://ko.wikipedia.org/wiki/블록_암호 "wikilink") / [암호 사용 모드](../Page/블록_암호_운용_방식.md "wikilink")** | **[스트림 암호](../Page/스트림_암호.md "wikilink")**                                          | **없음**                                |
| ------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------- | ------------------------------------- |
| **[AES](../Page/고급_암호화_표준.md "wikilink") GCM**<small>\[90\]</small> | **[AES](../Page/고급_암호화_표준.md "wikilink") CCM**<small>\[91\]</small>                                          | **[AES](../Page/고급_암호화_표준.md "wikilink") [CBC](../Page/블록_암호_운용_방식.md "wikilink")** | **Camellia GCM**<small>\[92\]</small> |
| [GnuTLS](https://ko.wikipedia.org/wiki/:en:GnuTLS "wikilink")       | Yes                                                                                                          | Yes <small></small>                                                                 | Yes                                   |
| [OpenSSL](../Page/OpenSSL.md "wikilink")                            | Yes <small></small><small>\[93\]</small>                                                                     | 기본적으로 비활성화 <small></small><small>\[94\]</small>                                     | Yes                                   |
| [wolfSSL](https://ko.wikipedia.org/wiki/wolfSSL "wikilink")         | Yes                                                                                                          | Yes                                                                                 | Yes                                   |
| **구현**                                                              | **[블록 암호화](https://ko.wikipedia.org/wiki/블록_암호 "wikilink") / [암호 사용 모드](../Page/블록_암호_운용_방식.md "wikilink")** | **스트림 암호**                                                                          | **없음**                                |
| **[AES](../Page/고급_암호화_표준.md "wikilink") GCM**                      | **[AES](../Page/고급_암호화_표준.md "wikilink") CCM**                                                               | **[AES](../Page/고급_암호화_표준.md "wikilink") [CBC](../Page/블록_암호_운용_방식.md "wikilink")** | **Camellia GCM**                      |

**Notes**

1\.    ^ ***<sup>a b</sup>*** 이 알고리즘은 초안에서 제안된 단계에서 RFC의 TLS 암호 수트로 아직 정의되어 있지 않다.

2\.    ^ ***<sup>a b</sup>*** 인증만 암호화 없음

## 폐지된 알고리즘

<table>
<thead>
<tr class="header">
<th><p><strong>구현</strong></p></th>
<th><p><strong><a href="https://ko.wikipedia.org/wiki/블록_암호" title="wikilink">블록 암호화</a> / <a href="../Page/블록_암호_운용_방식.md" title="wikilink">암호 사용 모드</a></strong></p></th>
<th><p><strong><a href="../Page/스트림_암호.md" title="wikilink">스트림 암호</a></strong></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="../Page/국제_데이터_암호화_알고리즘.md" title="wikilink">IDEA</a> <a href="../Page/블록_암호_운용_방식.md" title="wikilink">CBC</a></strong> <sup>[n 1]</sup> <strong>(안전하지 않음)</strong><small>[95]</small></p></td>
<td><p><strong><a href="../Page/데이터_암호화_표준.md" title="wikilink">DES</a> <a href="../Page/블록_암호_운용_방식.md" title="wikilink">CBC</a></strong> <strong>(안전하지 않음)</strong></p>
<p><sup>[n 1]</sup></p></td>
<td><p><strong><a href="../Page/데이터_암호화_표준.md" title="wikilink">DES</a> -40 <a href="../Page/블록_암호_운용_방식.md" title="wikilink">CBC</a></strong> <strong>(EXPORT 안전하지 않음)</strong></p>
<p><sup>[n 2]</sup></p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/:en:GnuTLS" title="wikilink">GnuTLS</a></p></td>
<td><p>No</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/OpenSSL.md" title="wikilink">OpenSSL</a></p></td>
<td><p>기본적으로 비활성화 <small></small><small>[96]</small></p></td>
<td><p>기본적으로 비활성화</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/wolfSSL" title="wikilink">wolfSSL</a></p></td>
<td><p>기본적으로 비활성화 <small></small><small>[97]</small></p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p><strong>구현</strong></p></td>
<td><p><strong><a href="https://ko.wikipedia.org/wiki/블록_암호" title="wikilink">블록 암호화</a> / <a href="../Page/블록_암호_운용_방식.md" title="wikilink">암호 사용 모드</a></strong></p></td>
<td><p><strong><a href="../Page/스트림_암호.md" title="wikilink">스트림 암호</a></strong></p></td>
</tr>
<tr class="even">
<td><p><strong><a href="../Page/국제_데이터_암호화_알고리즘.md" title="wikilink">IDEA</a> <a href="../Page/블록_암호_운용_방식.md" title="wikilink">CBC</a></strong> <sup>[n 1]</sup> <strong>(안전하지 않음)</strong></p></td>
<td><p><strong><a href="../Page/데이터_암호화_표준.md" title="wikilink">DES</a> <a href="../Page/블록_암호_운용_방식.md" title="wikilink">CBC</a></strong> <strong>(안전하지 않음)</strong></p>
<p><sup>[n 1]</sup></p></td>
<td><p><strong><a href="../Page/데이터_암호화_표준.md" title="wikilink">DES</a> -40 <a href="../Page/블록_암호_운용_방식.md" title="wikilink">CBC</a></strong> <strong>(EXPORT 안전하지 않음</strong></p>
<p><sup>[n 2]</sup></p></td>
</tr>
</tbody>
</table>

**Notes**

1\.    ^ ***<sup>a b c d</sup>*** IDEA와 DES는 TLS 1.2에서 제거<small>\[98\]</small>

2\.    ^ ***<sup>a b c d e f</sup>*** 특정 강력한 암호화 알고리즘 지닌 암호화 소프트웨어의 수출에 대한 미국의 규제를 준수하기 위해 40 비트 강도 암호화 제품군이 단축 된 키 길이에서 작동하도록 설계되었다. 이러한 약한 스위트는 TLS 1.1 및 그 이후에서는 금지됨.

3\.    ^ ***<sup>a b</sup>*** [RC4 공격은](../Page/전송_계층_보안.md "wikilink") SSL / TLS에서 사용되는 RC4를 안전하지 않게 함. (RC4의 사용은 RFC 7465에서 금지됨)

4\.    ^ ***<sup>a b</sup>*** [RC4 공격은](../Page/전송_계층_보안.md "wikilink") SSL / TLS에서 사용되는 RC4는 안전하지 않게 함.

## 지원되는 타원 곡선

이 섹션에서는 각 구현에서 지원되는 타원 곡선을 목록으로 만든다.

<table>
<thead>
<tr class="header">
<th><p><strong>구현</strong></p></th>
<th><p><strong>sect163k1</strong> <strong>NIST K-163</strong></p>
<p><strong>(1)</strong>[99]</p></th>
<th><p><strong>sect163r1</strong> <strong>(2)</strong>[100]</p></th>
<th><p><strong>sect163r2</strong> <strong>NIST B-163</strong>[101]</p>
<p><strong>(3)</strong></p></th>
<th><p><strong>sect193r1</strong> <strong>(4)</strong>[102]</p></th>
<th><p><strong>sect193r2</strong> <strong>(5)</strong>[103]</p></th>
<th><p><strong>sect233k1</strong> <strong>NIST K-233</strong></p>
<p><strong>(6)</strong>[104]</p></th>
<th><p><strong>sect233r1</strong> <strong>NIST B-233</strong></p>
<p><strong>(7)</strong>[105]</p></th>
<th><p><strong>sect239k1</strong> <strong>(8)</strong>[106]</p></th>
<th><p><strong>sect283k1</strong> <strong>NIST K-283</strong></p>
<p><strong>(9)</strong>[107]</p></th>
<th><p><strong>sect283r1</strong> <strong>NIST B-283</strong></p>
<p><strong>(10)</strong>[108]</p></th>
<th><p><strong>sect409k1</strong> <strong>NIST K-409</strong></p>
<p><strong>(11)</strong>[109]</p></th>
<th><p><strong>sect409r1</strong> <strong>NIST B-409</strong></p>
<p><strong>(12)</strong>[110]</p></th>
<th><p><strong>sect571k1</strong> <strong>NIST K-571</strong></p>
<p><strong>(13)</strong>[111]</p></th>
<th><p><strong>sect571r1</strong> <strong>NIST B-571</strong></p>
<p><strong>(14)</strong>[112]</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/:en:GnuTLS" title="wikilink">GnuTLS</a></p></td>
<td><p>No</p></td>
<td><p>No</p></td>
<td><p>No</p></td>
<td><p>No</p></td>
<td><p>No</p></td>
<td><p>No</p></td>
<td><p>No</p></td>
<td><p>No</p></td>
<td><p>No</p></td>
<td><p>No</p></td>
<td><p>No</p></td>
<td><p>No</p></td>
<td><p>No</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/OpenSSL.md" title="wikilink">OpenSSL</a></p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/wolfSSL" title="wikilink">wolfSSL</a></p></td>
<td><p>No</p></td>
<td><p>No</p></td>
<td><p>No</p></td>
<td><p>No</p></td>
<td><p>No</p></td>
<td><p>No</p></td>
<td><p>No</p></td>
<td><p>No</p></td>
<td><p>No</p></td>
<td><p>No</p></td>
<td><p>No</p></td>
<td><p>No</p></td>
<td><p>No</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p><strong>구현</strong></p></td>
<td><p><strong>sect163k1</strong> <strong>NIST K-163</strong></p>
<p><strong>(1)</strong></p></td>
<td><p><strong>sect163r1</strong> <strong>(2)</strong></p></td>
<td><p><strong>sect163r2</strong> <strong>NIST B-163</strong></p>
<p><strong>(3)</strong></p></td>
<td><p><strong>sect193r1</strong> <strong>(4)</strong></p></td>
<td><p><strong>sect193r2</strong> <strong>(5)</strong></p></td>
<td><p><strong>sect233k1</strong> <strong>NIST K-233</strong></p>
<p><strong>(6)</strong></p></td>
<td><p><strong>sect233r1</strong> <strong>NIST B-233</strong></p>
<p><strong>(7)</strong></p></td>
<td><p><strong>sect239k1</strong> <strong>(8)</strong></p></td>
<td><p><strong>sect283k1</strong> <strong>NIST K-283</strong></p>
<p><strong>(9)</strong></p></td>
<td><p><strong>sect283r1</strong> <strong>NIST B-283</strong></p>
<p><strong>(10)</strong></p></td>
<td><p><strong>sect409k1</strong> <strong>NIST K-409</strong></p>
<p><strong>(11)</strong></p></td>
<td><p><strong>sect409r1</strong> <strong>NIST B-409</strong></p>
<p><strong>(12)</strong></p></td>
<td><p><strong>sect571k1</strong> <strong>NIST K-571</strong></p>
<p><strong>(13)</strong></p></td>
<td><p><strong>sect571r1</strong> <strong>NIST B-571</strong></p>
<p><strong>(14)</strong></p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr class="header">
<th><p><strong>구현</strong></p></th>
<th><p><strong>secp160k1</strong> <strong>(15)</strong>[113]</p></th>
<th><p><strong>secp160r1</strong> <strong>(16)</strong>[114]</p></th>
<th><p><strong>secp160r2</strong> <strong>(17)</strong>[115]</p></th>
<th><p><strong>secp192k1</strong> <strong>(18)</strong>[116]</p></th>
<th><p><strong>secp192r1</strong> <strong>prime192v1</strong></p>
<p><strong>NIST P-192</strong></p>
<p><strong>(19)</strong>[117]</p></th>
<th><p><strong>secp224k1</strong> <strong>(20)</strong>[118]</p></th>
<th><p><strong>secp224r1</strong> <strong>NIST P-244</strong></p>
<p><strong>(21)</strong>[119]</p></th>
<th><p><strong>secp256k1</strong> <strong>(22)</strong>[120]</p></th>
<th><p><strong>secp256r1</strong> <strong>prime256v1</strong></p>
<p><strong>NIST P-256</strong></p>
<p><strong>(23)</strong>[121]</p></th>
<th><p><strong>secp384r1</strong> <strong>NIST P-384</strong></p>
<p><strong>(24)</strong>[122]</p></th>
<th><p><strong>secp521r1</strong> <strong>NIST P-521</strong></p>
<p><strong>(25)</strong>[123]</p></th>
<th><p><strong>arbitrary prime curves</strong> <strong>(0xFF01)</strong>[124][125]</p></th>
<th><p><strong>arbitrary char2 curves</strong> <strong>(0xFF02)</strong>[126][127]</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/:en:GnuTLS" title="wikilink">GnuTLS</a></p></td>
<td><p>No</p></td>
<td><p>No</p></td>
<td><p>No</p></td>
<td><p>No</p></td>
<td><p>Yes</p></td>
<td><p>No</p></td>
<td><p>Yes</p></td>
<td><p>No</p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>No</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/OpenSSL.md" title="wikilink">OpenSSL</a></p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>No</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/wolfSSL" title="wikilink">wolfSSL</a></p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>Yes</p></td>
<td><p>No</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p><strong>구현</strong></p></td>
<td><p><strong>secp160k1</strong> <strong>(15)</strong></p></td>
<td><p><strong>secp160r1</strong> <strong>(16)</strong></p></td>
<td><p><strong>secp160r2</strong> <strong>(17)</strong></p></td>
<td><p><strong>secp192k1</strong> <strong>(18)</strong></p></td>
<td><p><strong>secp192r1</strong> <strong>prime192v1</strong></p>
<p><strong>NIST P-192</strong></p>
<p><strong>(19)</strong></p></td>
<td><p><strong>secp224k1</strong> <strong>(20)</strong></p></td>
<td><p><strong>secp224r1</strong> <strong>NIST P-244</strong></p>
<p><strong>(21)</strong></p></td>
<td><p><strong>secp256k1</strong> <strong>(22)</strong></p></td>
<td><p><strong>secp256r1</strong> <strong>prime256v1</strong></p>
<p><strong>NIST P-256</strong></p>
<p><strong>(23)</strong></p></td>
<td><p><strong>secp384r1</strong> <strong>NIST P-384</strong></p>
<p><strong>(24)</strong></p></td>
<td><p><strong>secp521r1</strong> <strong>NIST P-521</strong></p>
<p><strong>(25)</strong></p></td>
<td><p><strong>arbitrary prime curves</strong> <strong>(0xFF01)</strong></p></td>
<td><p><strong>arbitrary char2 curves</strong> <strong>(0xFF02)</strong></p></td>
</tr>
</tbody>
</table>

| **구현**                                                        | **brainpoolP256r1** **(26)**\[128\] | **brainpoolP384r1** **(27)**\[129\] | **brainpoolP512r1** **(28)**\[130\] | **X25519**\[131\]                                 | **Curve448** **Ed448-Goldilocks**\[132\] | **M221** **Curve2213**\[133\] | **E222**\[134\] | **Curve1174**\[135\] | **E382**\[136\] | **M383**\[137\] | **Curve383187**\[138\] | **Curve41417** **Curve3617**\[139\] | **M511** **Curve511187**\[140\] | **E521**\[141\] |
| ------------------------------------------------------------- | ----------------------------------- | ----------------------------------- | ----------------------------------- | ------------------------------------------------- | ---------------------------------------- | ----------------------------- | --------------- | -------------------- | --------------- | --------------- | ---------------------- | ----------------------------------- | ------------------------------- | --------------- |
| [GnuTLS](https://ko.wikipedia.org/wiki/:en:GnuTLS "wikilink") | No                                  | No                                  | No                                  | Yes <small></small>\[142\]                        | No                                       | No                            | No              | No                   | No              | No              | No                     | No                                  | No                              | No              |
| [OpenSSL](../Page/OpenSSL.md "wikilink")                      | Yes <small></small>\[143\]          | Yes <small></small>\[144\]          | Yes <small></small>\[145\]          | Yes <small></small> <small></small>\[146\]\[147\] | Yes <small></small>\[148\]\[149\]        | No                            | No              | No                   | No              | No              | No                     | No                                  | No                              | No              |
| [wolfSSL](https://ko.wikipedia.org/wiki/wolfSSL "wikilink")   | Yes                                 | Yes                                 | Yes                                 | Yes <small></small>\[150\]                        | No                                       | No                            | No              | No                   | No              | No              | No                     | No                                  | No                              | No              |
| **구현**                                                        | **brainpoolP256r1** **(26)**        | **brainpoolP384r1** **(27)**        | **brainpoolP512r1** **(28)**        | **Curve25519**                                    | **Curve448** **Ed448-Goldilocks**        | **M221** **Curve2213**        | **E222**        | **Curve1174**        | **E382**        | **M383**        | **Curve383187**        | **Curve41417** **Curve3617**        | **M511** **Curve511187**        | **E521**        |

## 데이터 무결성

| **구현**                                                        | **HMAC - [MD5](../Page/MD5.md "wikilink")** | **HMAC - [SHA](../Page/SHA.md "wikilink")1** | **HMAC - [SHA256 / 384](../Page/SHA-2.md "wikilink")** | **AEAD** | **GOST 28147-89 IMIT** <small></small>\[151\] | **GOST R 34.11-94** <small></small>\[152\] |
| ------------------------------------------------------------- | ------------------------------------------- | -------------------------------------------- | ------------------------------------------------------ | -------- | --------------------------------------------- | ------------------------------------------ |
| [GnuTLS](https://ko.wikipedia.org/wiki/:en:GnuTLS "wikilink") | Yes                                         | Yes                                          | Yes                                                    | Yes      | No                                            | No                                         |
| [OpenSSL](../Page/OpenSSL.md "wikilink")                      | Yes                                         | Yes                                          | Yes                                                    | Yes      | Yes <small></small>\[153\]                    | Yes <small></small>\[154\]                 |
| [wolfSSL](https://ko.wikipedia.org/wiki/wolfSSL "wikilink")   | Yes                                         | Yes                                          | Yes                                                    | Yes      | No                                            | No                                         |
| **구현**                                                        | **HMAC-MD5**                                | **HMAC-SHA1**                                | **HMAC-SHA256 / 384**                                  | **AEAD** | **GOST 28147-89 IMIT**                        | **GOST R 34.11-94**                        |

## 압축

CRIME 공격은 TLS 압축을 이용하기 때문에, 신중한 구현에서는 TLS 레벨에서의 압축은 사용하지 않는다. 또한 HTTP 압축 무관이 공격의 영향을 받지 않지만, 관련 BREACH 공격에 의해 악용되는 점에 주의가 필요하다.

| **구현**                                                        | **DEFLATE** <small></small>\[155\] **(안전하지 않음)** |
| ------------------------------------------------------------- | ------------------------------------------------ |
| [GnuTLS](https://ko.wikipedia.org/wiki/:en:GnuTLS "wikilink") | 기본적으로 비활성화                                       |
| [OpenSSL](../Page/OpenSSL.md "wikilink")                      | 기본적으로 비활성화                                       |
| [wolfSSL](https://ko.wikipedia.org/wiki/wolfSSL "wikilink")   | 기본적으로 비활성화                                       |
| **구현**                                                        | **DEFLATE**                                      |

## 확장 기능

이 섹션에서는 각 구현이 지원하는 확장 기능을 나열한다. 안전한 재협상 확장 (Secure Renegotiation extension)은 HTTPS 클라이언트 보안에 중요한 의미를 갖는다. 클라이언트가 TLS 재협상 (TLS renegotiation)을 구현하고 있는지 여부에 관계없이 이 확장을 구현하지 않은 TLS 클라이언트는 공격에 취약하다.

| **구현**                                                        | **재협상**\[156\] | **Server Name Indication**\[157\] | **ALPN**\[158\]            | **Certificate Status Request** \[159\] | **OpenPGP**\[160\]          | **Supplemental Data**\[161\] | **Session Ticket**\[162\] | **Keying Material Exporter**\[163\] | **Maximum Fragment Length**\[164\] | **TruncatedHMAC**\[165\] | **Encrypt-then-MAC**\[166\] | **TLS Fallback SCSV**\[167\] | **Extended Master Secret**\[168\] | **ClientHello Padding**\[169\] | **Raw Public Keys**\[170\] |
| ------------------------------------------------------------- | -------------- | --------------------------------- | -------------------------- | -------------------------------------- | --------------------------- | ---------------------------- | ------------------------- | ----------------------------------- | ---------------------------------- | ------------------------ | --------------------------- | ---------------------------- | --------------------------------- | ------------------------------ | -------------------------- |
| [GnuTLS](https://ko.wikipedia.org/wiki/:en:GnuTLS "wikilink") | Yes            | Yes                               | Yes <small></small>\[171\] | Yes                                    | 폐지 예정<small></small>\[172\] | Yes                          | Yes                       | Yes                                 | Yes                                | No                       | Yes\[173\]                  | Yes <small></small>\[174\]   | Yes <small></small>               | Yes <small></small>\[175\]     | No                         |
| [OpenSSL](../Page/OpenSSL.md "wikilink")                      | Yes            | Yes                               | Yes <small></small>\[176\] | Yes                                    | No                          | No?                          | Yes                       | Yes?                                | No                                 | No                       | No                          | Yes <small></small>\[177\]   | Yes <small></small>\[178\]        | Yes <small></small>\[179\]     | 알수없음                       |
| [wolfSSL](https://ko.wikipedia.org/wiki/wolfSSL "wikilink")   | Yes            | Yes                               | Yes <small></small>\[180\] | Yes                                    | No                          | No                           | Yes                       | No                                  | Yes                                | Yes                      | No                          | No                           | Yes                               | No                             | 알수없음                       |
| **구현**                                                        | **재협상**        | **Server Name Indication**        | **ALPN**                   | **Certificate Status Request**         | **OpenPGP**                 | **Supplemental Data**        | **Session Ticket**        | **Keying Material Exporter**        | **Maximum Fragment Length**        | **Truncated HMAC**       | **Encrypt-then-MAC**        | **TLS Fallback SCSV**        | **Extended Master Secret**        | **ClientHello Padding**        | **Raw Public Keys**        |

## 어시스트 암호화

이 섹션에서는 암호화를 최적화 하는 CPU 명령어 세트의 장점을 살린 구현의 알려진 기능이나 하드웨어 암호화 및 데이터 분리의 접근을 허용하는 디바이스의 사용 시스템에 대해 나열한다.

| **구현**                                                        | **[PKCS \# 11 device](https://ko.wikipedia.org/wiki/PKCS_#_11_device "wikilink")** | **[Intel AES-NI](https://ko.wikipedia.org/wiki/AES_알고리즘 "wikilink")** | **VIA PadLock** | **[ARMv8-A](../Page/ARM_홀딩스.md "wikilink")** | **Intel SGX** | **Intel QAT**              |
| ------------------------------------------------------------- | ---------------------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------- | -------------------------------------------- | ------------- | -------------------------- |
| [GnuTLS](https://ko.wikipedia.org/wiki/:en:GnuTLS "wikilink") | Yes                                                                                | Yes                                                                   | Yes             | Yes <small></small>\[181\]                   | No            | No                         |
| [OpenSSL](../Page/OpenSSL.md "wikilink")                      | Yes <small></small>\[182\]                                                         | Yes                                                                   | Yes             | Yes <small></small>\[183\]                   |               | No                         |
| [wolfSSL](https://ko.wikipedia.org/wiki/wolfSSL "wikilink")   | No                                                                                 | Yes                                                                   | No              | Yes                                          | Yes           | Yes <small></small>\[184\] |
| **구현**                                                        | **PKCS \# 11 device**                                                              | **Intel AES-NI**                                                      | **VIA PadLock** | **ARMv8-A**                                  | **Intel SGX** | **Intel QAT**              |

## 시스템 고유의 백엔드

이 섹션에서는 사용 가능한 운영 체제 고유의 백엔드 또는 다른 구현에서 제공하는 백엔드를 사용하는 구현의 기능을 나타낸다.

| **구현**                                                        | **/ dev / crypto** | **Windows CSP** | **CommonCrypto** | **[OpenSSL engine](../Page/OpenSSL.md "wikilink")** |
| ------------------------------------------------------------- | ------------------ | --------------- | ---------------- | --------------------------------------------------- |
| [GnuTLS](https://ko.wikipedia.org/wiki/:en:GnuTLS "wikilink") | Yes                | No              | No               | No                                                  |
| [OpenSSL](../Page/OpenSSL.md "wikilink")                      | Yes                | No              | No               | Yes                                                 |
| [wolfSSL](https://ko.wikipedia.org/wiki/wolfSSL "wikilink")   | No                 | 부분적             | No               | No                                                  |
| **구현**                                                        | **/ dev / crypto** | **Windows CSP** | **CommonCrypto** | **OpenSSL engine**                                  |

## 암호화 모듈 / 토큰 지원

| **구현**                                                        | **TPM support** | **Hardware token support** | **Objects identified via**                     |
| ------------------------------------------------------------- | --------------- | -------------------------- | ---------------------------------------------- |
| [GnuTLS](https://ko.wikipedia.org/wiki/:en:GnuTLS "wikilink") | Yes             | PKCS11                     | RFC7512 PKCS \# 11 URLs <small></small>\[185\] |
| [OpenSSL](../Page/OpenSSL.md "wikilink")                      | Yes             | PKCS11 (타사 모듈을 통해)\[186\]  | RFC7512 PKCS \# 11 URLs <small></small>\[187\] |
| [wolfSSL](https://ko.wikipedia.org/wiki/wolfSSL "wikilink")   | No              | No                         |                                                |
| **구현**                                                        | **TPM support** | **Hardware token support** | **Objects identified via**                     |

## 코드의 종속성

<table>
<thead>
<tr class="header">
<th><p><strong>구현</strong></p></th>
<th><p><strong>따의존</strong></p></th>
<th><p><strong>옵션</strong> <strong>의존</strong></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/:en:GnuTLS" title="wikilink">GnuTLS</a></p></td>
<td><p>libc nettle</p>
<p>gmp</p></td>
<td><p>zlib (compression) p11-kit (PKCS # 11)</p>
<p>trousers (TPM)</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/OpenSSL.md" title="wikilink">OpenSSL</a></p></td>
<td><p>libc</p></td>
<td><p>zlib (compression)</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/wolfSSL" title="wikilink">wolfSSL</a></p></td>
<td><p>None</p></td>
<td><p>libc, zlib (compression)</p></td>
</tr>
<tr class="even">
<td><p><strong>구현</strong></p></td>
<td><p><strong>따의존</strong></p></td>
<td><p><strong>옵션</strong> <strong>의존</strong></p></td>
</tr>
</tbody>
</table>

## 개발 환경

<table>
<thead>
<tr class="header">
<th><p><strong>구현</strong></p></th>
<th><p><strong>Namespace</strong></p></th>
<th><p><strong>빌드 도구</strong></p></th>
<th><p><strong>API 문서</strong></p></th>
<th><p><strong>백 엔드 암호화</strong></p></th>
<th><p><strong>Template  : OpenSSL 호환 레이어</strong></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/:en:GnuTLS" title="wikilink">GnuTLS</a></p></td>
<td><p>gnutls_ *</p></td>
<td><p>Autoconf, automake, libtool</p></td>
<td><p>가이드 및 API 참조 (HTML, PDF)</p></td>
<td><p>외부 libnettle</p></td>
<td><p>Yes (limited)</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/OpenSSL.md" title="wikilink">OpenSSL</a></p></td>
<td><p>SSL_ * SHA1_ *</p>
<p>MD5_ *</p>
<p>EVP_ *</p>
<p>...</p></td>
<td><p>Makefile</p></td>
<td><p>Man pages</p></td>
<td><p>포함됨 (monolithic)</p></td>
<td><p>N / A</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/wolfSSL" title="wikilink">wolfSSL</a></p></td>
<td><p>CyaSSL_ * SSL_ *</p></td>
<td><p>Autoconf, automake, libtool, MSVC project workspaces, XCode projects, CodeWarrior projects, MPLAB X projects, Keil, IAR, Clang, GCC</p></td>
<td><p>가이드 및 API 참조 (HTML, PDF)</p></td>
<td><p>포함됨 (monolithic)</p></td>
<td><p>Yes (약 10 %의 API)</p></td>
</tr>
<tr class="even">
<td><p><strong>구현</strong></p></td>
<td><p><strong>Namespace</strong></p></td>
<td><p><strong>빌드 도구</strong></p></td>
<td><p><strong>API 문서</strong></p></td>
<td><p><strong>백 엔드 암호화</strong></p></td>
<td><p><strong>OpenSSL 호환 레이어</strong></p></td>
</tr>
</tbody>
</table>

## 이식성에 대한 우려

| **구현**                                                        | **플랫폼 요구 사항** | **네트워크 요구 사항**                                              | **스레드 안전**                                                   | **랜덤 배정**         | **크로스 컴파일** | **No OS (베어 메탈)** | **지원 OS**                                                                                                                                                                                                                                                                                                                               |
| ------------------------------------------------------------- | ------------- | ----------------------------------------------------------- | ------------------------------------------------------------ | ----------------- | ----------- | ----------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [GnuTLS](https://ko.wikipedia.org/wiki/:en:GnuTLS "wikilink") | C89           | POSIX send ()와 recv (). API to supply your own replacement. | 스레드 안전, POSIX 또는 Windows 스레드 둘다 불가능 할 경우 사용자 mutex 후크 필요     | 플랫폼에 의존           | Yes         | No                | POSIX 플랫폼, Windows GNU / Linux, Win32 / 64, OS X, Solaris OpenWRT FreeBSD, NetBSD, OpenBSD 등 일반적으로 테스트 된 플랫폼                                                                                                                                                                                                                            |
| [OpenSSL](../Page/OpenSSL.md "wikilink")                      | C89?          | ?                                                           | mutex 콜백이 필요                                                 | 네이티브 API를 통해서 됨   | Yes         | No                | Unix, DOS (with djgpp), Windows OpenVMS, MacOS, NetWare eCos                                                                                                                                                                                                                                                                            |
| [wolfSSL](https://ko.wikipedia.org/wiki/wolfSSL "wikilink")   | C89           | POSIX send ()와 recv (). API to supply your own replacement. | 스레드 안전, PThreads 또는 WinThreads이 불가능하면 mutex 후크 필요. 오프로 설정 가능 | wolfCrypt에서 랜덤 배정 | Yes         | Yes               | Win32 / 64, Linux OS X, Solaris ThreadX, VxWorks FreeBSD, NetBSD, OpenBSD, embedded Linux, Haiku, OpenWRT, iPhone (iOS), Android Nintendo Wii and Gamecube through DevKitPro, QNX, MontaVista, OpenCL, NonStop, TRON / ITRON / μITRON, Micrium 's μC OS, FreeRTOS, SafeRTOS, Freescale MQX, Nucleus, TinyOS, HP / UX, Keil RTX, TI-RTOS |
| **구현**                                                        | **플랫폼 요구 사항** | **네트워크 요구 사항**                                              | **스레드 안전**                                                   | **랜덤 배정**         | **크로스 컴파일** | **No OS (베어 메탈)** | **지원 OS**                                                                                                                                                                                                                                                                                                                               |

## 관련 항목

  - SCTP - DTLS 지원
  - DCCP - DTLS 지원
  - SRTP - DTLS 지원 및 SRTCP (DTLS-SRTP)

## 참조

[분류:암호 소프트웨어](https://ko.wikipedia.org/wiki/분류:암호_소프트웨어 "wikilink") [TLS 구현](https://ko.wikipedia.org/wiki/분류:보안_소프트웨어_비교 "wikilink") [전송_계층_보안_구현](https://ko.wikipedia.org/wiki/분류:전송_계층_보안_구현 "wikilink")

1.
2.
3.
4.
5.   wolfSSL Embedded SSL/TLS Library Documentation|뉴스=wolfSSL|언어=en-US|확인날짜=2018-06-26}}
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
17.
18.
19.
20.
21.
22.
23.
24.
25.
26.
27.
28.
29.
30.
31.
32.  CSRC|확인날짜=2018-06-26|보존url=[https://web.archive.org/web/20141226152243/http://csrc.nist.gov/groups/STM/cmvp/documents/140-1/140val-all.htm|보존날짜=2014-12-26|url-status=dead](https://web.archive.org/web/20141226152243/http://csrc.nist.gov/groups/STM/cmvp/documents/140-1/140val-all.htm%7C보존날짜=2014-12-26%7Curl-status=dead)}}
33.
34.
35.  wolfSSL Embedded SSL/TLS Library|뉴스=wolfSSL|언어=en-US|확인날짜=2018-06-26}}
36.
37.
38.
39.
40.
41.
42.
43.
44.
45.
46.
47.
48.
49.
50.
51.
52.
53.
54.
55.
56.
57.
58.
59.
60.
61.
62.
63.
64.
65.
66.
67.
68.
69.
70.
71.  wolfSSL Embedded SSL/TLS Library Documentation|뉴스=wolfSSL|언어=en-US|확인날짜=2018-06-26}}
72.
73.
74.
75.
76.
77.
78.
79.
80.
81.
82.
83.
84.
85.
86.
87.
88.
89.
90.
91.
92.
93.
94.
95.
96.
97.  wolfSSL Embedded SSL/TLS Library Documentation|뉴스=wolfSSL|언어=en-US|확인날짜=2018-06-26}}
98.
99.
100.
101.
102.
103.
104.
105.
106.
107.
108.
109.
110.
111.
112.
113.
114.
115.
116.
117.
118.
119.
120.
121.
122.
123.
124.
125.
126.
127.
128.
129.
130.
131.
132.
133.
134.
135.
136.
137.
138.
139.
140.
141.
142.
143.
144.
145.
146.
147.
148.
149.
150.  wolfSSL Embedded SSL/TLS Library Documentation|뉴스=wolfSSL|언어=en-US|확인날짜=2018-06-26}}
151.
152.
153.
154.
155.
156.
157.
158.
159.
160.
161.
162.
163.
164.
165.
166.
167.
168.
169.
170.
171.
172.
173.
174.
175.
176.
177.
178.
179.
180.
181.
182.
183.
184.
185.
186.
187.