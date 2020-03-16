> This article is converted from Wikipedia: [Netsh](https://ko.wikipedia.org/wiki/Netsh).


[소프트웨어](../Page/소프트웨어.md "wikilink")로서, 또는 [네트워크](../Page/컴퓨터_네트워크.md "wikilink") [셸](../Page/셸.md "wikilink")에서의 **netsh**는 [마이크로소프트](../Page/마이크로소프트.md "wikilink")의 [윈도우 NT](../Page/윈도우_NT.md "wikilink") [운영체제](https://ko.wikipedia.org/wiki/운영체제 "wikilink") 계열의 [윈도우 2000에서부터](../Page/윈도우_2000.md "wikilink") 유틸리티로 포함되기 시작하였다. 이 명령어는 로컬 또는 원격 구성의 네트워크 설정을 변경 할 수 있게 해준다.

**netsh**의 일반적인 사용방법은 [TCP/IP](https://ko.wikipedia.org/wiki/TCP/IP "wikilink") 스택을 기본 값으로 되돌려주는 것이다. 잘 알려진 매개변수로는, [윈도우 98에서](../Page/윈도우_98.md "wikilink") [TCP/IP](https://ko.wikipedia.org/wiki/TCP/IP "wikilink") 어댑터의 재설치 작업이다.. 그 모드에서는 당신은 반드시 [로그 파일을](https://ko.wikipedia.org/wiki/로그_파일 "wikilink") 제공하거나 **netsh** 영향을 받은 가치와 함께 보존해야 한다.

Netsh의 많은 다른 기능으로는, 사용자 컴퓨터의 [IP 주소를](../Page/IP_주소.md "wikilink") 변경하는 기능도 있다.

윈도우 비스타부터는 netsh를 사용해서 무선 네트워크 설정(예: SSID) 편집이 가능하다.

## 사용 예제

사용 예제:

    netsh interface ip reset C:\resetlog.txt

정적 IP 주소:

    netsh interface ip set address local static 123.123.123.123 255.255.255.0

복수 정적 IP 주소:

    netsh interface ip set address local static 123.123.123.123 255.255.255.0
    netsh interface ip add address local 234.234.234.234 255.255.255.0

동적 IP 주소:

    netsh interface ip set address name="Local Area Connection" source=dhcp

## NETSH 및 IPv6

netsh는 [IPv6](../Page/IPv6.md "wikilink") 스택에서 정보를 읽을 수 있을 뿐만 아니라, IPv4.exe 유틸리티보다 좀 더 사용자 친화적이고 좀 더 많은 같은 등급의 정보를 제공한다.

IPv6 주소가 NETSH에 사용되는 것을 보는 방법:

    netsh interface ipv6 show address

## 외부 링크

  - [Netsh 사용](http://technet.microsoft.com/en-us/library/bb490939.aspx)
  - [Ipv6 in .NET](https://web.archive.org/web/20080919123647/http://network.programming-in.net/articles/book-network-programming-art6-13.asp)
  - [주소 빌드 및 명령 바인딩 온라인 도구](https://web.archive.org/web/20080219233637/http://platformlabs.com/bag/net.htm)
  - [netsh commands](http://www.colorconsole.de/cmd/kr/Windows_XP/netsh.htm)

[분류:윈도우 구성 요소](https://ko.wikipedia.org/wiki/분류:윈도우_구성_요소 "wikilink") [분류:윈도우 관리](https://ko.wikipedia.org/wiki/분류:윈도우_관리 "wikilink")