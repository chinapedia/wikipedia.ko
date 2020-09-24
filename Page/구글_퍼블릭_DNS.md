> This article is converted from Wikipedia: [구글 퍼블릭 DNS](https://ko.wikipedia.org/wiki/구글_퍼블릭_DNS).


**구글 퍼블릭 DNS**()는 2009년 12월 3일에 발표되어, [구글](../Page/구글.md "wikilink")에서 무료로 제공하는 [DNS](../Page/도메인_네임_시스템.md "wikilink") 서비스로서\[1\], 웹 환경을 빠르고 보다 안전하게 하기 위한 노력의 일부이다.\[2\]\[3\] 구글에 따르면 2013년 기준으로 구글 퍼블릭 DNS는 하루 평균 1,300,000,000,000건 이상의 요청을 처리할 수 있는, 세계에서 가장 큰 공용 DNS 서비스이다.\[4\]

## 서비스

구글 퍼블릭 DNS는 다음과 같은 리커시브 네임 서버 주소를 공용으로 제공하며\[5\], [애니캐스트](../Page/애니캐스트.md "wikilink") 라우팅을 통해 가장 가까운 운영 서버 위치로 매핑해 준다:\[6\]

<table>
<tbody>
<tr class="odd">
<td><p><strong><a href="https://ko.wikipedia.org/wiki/DNS_오버_HTTPS" title="wikilink">DoH</a> 주소</strong></p></td>
<td><p><a href="https://dns.google/dns-query">https://dns.google/dns-query</a><br />
<a href="https://dns.google/resolve">https://dns.google/resolve</a>?</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="../Page/IPv4.md" title="wikilink">IPv4</a> 주소</strong></p></td>
<td><p>8.8.8.8<br />
8.8.4.4</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="../Page/IPv6.md" title="wikilink">IPv6</a> 주소</strong>[7]</p></td>
<td><p>2001:4860:4860::8888<br />
2001:4860:4860::8844</p></td>
</tr>
</tbody>
</table>

## DNS64

구글 퍼블릭 DNS64 서비스는 [NAT64](https://ko.wikipedia.org/wiki/NAT64 "wikilink")와의 이용을 위해 다음 2개의 IP 주소에서 공적은 용도로 반복(recursive) 네임 서버를 운영한다.\[8\] 이 서버들은 DNS 오버 HTTPS와 호환된다.

<table>
<tbody>
<tr class="odd">
<td><p><strong><a href="https://ko.wikipedia.org/wiki/DNS_오버_HTTPS" title="wikilink">DoH</a> 주소</strong></p></td>
<td><p><a href="https://dns64.dns.google/dns-query">https://dns64.dns.google/dns-query</a>{?dns}<br />
<a href="https://dns64.dns.google/resolve?name=ipv4only.arpa&amp;type=AAAA">https://dns64.dns.google/resolve?name=ipv4only.arpa&amp;type=AAAA</a></p></td>
</tr>
<tr class="even">
<td><p><strong><a href="../Page/IPv6.md" title="wikilink">IPv6</a> 주소</strong></p></td>
<td><p>2001:4860:4860::6464<br />
2001:4860:4860::64</p></td>
</tr>
</tbody>
</table>

## 역사

2009년 12월, 구글 퍼블릭 DNS가 제품 관리자 Prem Ramaswami에 의해 [구글 코드](https://ko.wikipedia.org/wiki/구글_코드 "wikilink") 블로그의 추가 게시물과 더불어 공식 구글 블로그를 통해 런칭이 발표되었다.\[9\]\[10\]

2019년 1월, 구글 DNS는 [DNS 오버 TLS](https://ko.wikipedia.org/wiki/DNS_오버_TLS "wikilink") 프로토콜을 채택하였다.\[11\]

## 참조

<references/>

## 외부 링크

  -
[분류:구글의 서비스](https://ko.wikipedia.org/wiki/분류:구글의_서비스 "wikilink") [분류:인터넷 프라이버시](https://ko.wikipedia.org/wiki/분류:인터넷_프라이버시 "wikilink")

1.  [Geez, Google Wants to Take Over DNS, Too](http://www.wired.com/threatlevel/2009/12/geez-google-wants-to-take-over-dns-too/) Wired, 3 December 2009
2.  [Introducing Google Public DNS](http://googleblog.blogspot.com/2009/12/introducing-google-public-dns.html), Official Google Blog
3.  [Pondering Google's Move Into the D.N.S. Business](http://bits.blogs.nytimes.com/2009/12/03/pondering-googles-move-into-the-dns-business/) New York Times, 4 December 2009
4.
5.  [Google DNS](http://code.google.com/speed/public-dns/) Speed
6.  [Google DNS FAQ](http://code.google.com/speed/public-dns/faq.html#countries) Countries
7.
8.
9.  [Introducing Google Public DNS](http://googleblog.blogspot.com/2009/12/introducing-google-public-dns.html) Official Google Blog, 3 December 2009
10.
11.