> This article is converted from Wikipedia: [URL](https://ko.wikipedia.org/wiki/URL).


**URL**(Uniform Resource Locator 또는 web address, )은 네트워크 상에서 자원이 어디 있는지를 알려주기 위한 규약이다. 즉, [컴퓨터 네트워크와](../Page/컴퓨터_네트워크.md "wikilink") 검색 [메커니즘](https://ko.wikipedia.org/wiki/메커니즘 "wikilink")에서의 위치를 지정하는, [웹 리소스에](https://ko.wikipedia.org/wiki/리소스_\(웹\) "wikilink") 대한 참조이다. 흔히 웹 사이트 주소로 알고 있지만, URL은 웹 사이트 주소뿐만 아니라 컴퓨터 네트워크상의 자원을 모두 나타낼 수 있다. 그 주소에 접속하려면 해당 URL에 맞는 [프로토콜을](../Page/통신_프로토콜.md "wikilink") 알아야 하고, 그와 동일한 프로토콜로 접속해야 한다.

[FTP](https://ko.wikipedia.org/wiki/FTP "wikilink") 프로토콜인 경우에는 FTP [클라이언트](https://ko.wikipedia.org/wiki/클라이언트 "wikilink")를 이용해야 하고, [HTTP](../Page/HTTP.md "wikilink")인 경우에는 [웹 브라우저를](../Page/웹_브라우저.md "wikilink") 이용해야 한다. [텔넷](../Page/텔넷.md "wikilink")의 경우에는 텔넷 프로그램을 이용해서 접속해야 한다.

## 역사

URL은 1994년 [월드 와이드 웹의](../Page/월드_와이드_웹.md "wikilink") 창시자 [팀 버너스 리와](https://ko.wikipedia.org/wiki/팀_버너스_리 "wikilink") [IETF](https://ko.wikipedia.org/wiki/IETF "wikilink")의 URI 워킹 그룹에 의해 1992년 IETF Live Documents [Birds of a feather에서](https://ko.wikipedia.org/wiki/Birds_of_a_feather "wikilink") 시작한 협업의 산물로서 [RFC](../Page/RFC.md "wikilink") 1738에 정의되었다.

## 문법

```
 scheme:[//[user:password@]host[:port]][/]path[?query][#fragment]
```

  - URL은 제일 앞에 자원에 접근할 방법을 정의해 둔 프로토콜 이름을 적는다. [gopher](../Page/고퍼_\(프로토콜\).md "wikilink"), [telnet](../Page/텔넷.md "wikilink"), [ftp](../Page/파일_전송_프로토콜.md "wikilink"), [http](../Page/HTTP.md "wikilink"), [usenet](../Page/유즈넷.md "wikilink") 등이다.
  - 프로토콜 이름 다음에는 프로토콜 이름을 구분하는 구분자인 ":"을 적는다.
  - 만약 IP 혹은 Domain name 정보가 필요한 프로토콜이라면 ":" 다음에 "//"를 적는다.\[1\]
  - 프로토콜명 구분자인 ":" 혹은 "//" 다음에는 프로토콜 마다 특화된 정보를 넣는다.
      - 예1) <http://www.somehost.com/a.gif> - IP 혹은 Domain name 정보가 필요한 형태 ( www.somehost.com에 있는 a.gif를 가리키고 있음 )
      - 예2) <ftp://id:pass@192.168.1.234/a.gif> - IP 혹은 Domain name 정보가 필요한 형태 ( 192.168.1.234에 있는 a.gif를 가리키고 있음 )
      - 예3) [`mailto:somebody@mail.somehost.com`](mailto:somebody@mail.somehost.com) - IP정보가 필요없는 프로토콜 ( mailto 프로토콜은 단지 메일을 받는 사람의 주소를 나타냄 )

## 같이 보기

  - [웹 사이트](https://ko.wikipedia.org/wiki/웹_사이트 "wikilink")
  - [TinyURL](https://ko.wikipedia.org/wiki/TinyURL "wikilink")
  - [통합 자원 식별자](../Page/통합_자원_식별자.md "wikilink")(URI)

## 각주

[URL](https://ko.wikipedia.org/wiki/분류:URL "wikilink") [분류:식별자](https://ko.wikipedia.org/wiki/분류:식별자 "wikilink")

1.  URL Spec - 5. BNF for specific URL schemes <http://tools.ietf.org/html/rfc1738#section-5>