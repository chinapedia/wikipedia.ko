> This article is converted from Wikipedia: [Ifconfig](https://ko.wikipedia.org/wiki/Ifconfig).


**ifconfig**는 [네트워크 인터페이스](https://ko.wikipedia.org/wiki/네트워크_카드 "wikilink") 구성을 위한 [유닉스 계열](https://ko.wikipedia.org/wiki/유닉스_계열 "wikilink") 운영체제의 시스템 관리 유틸리티이다.

이 유틸리티는 [명령 줄 인터페이스](https://ko.wikipedia.org/wiki/명령_줄_인터페이스 "wikilink") 도구의 하나이며, 수많은 운영 체제의 시스템 시작 스크립트에도 사용된다. [TCP/IP](https://ko.wikipedia.org/wiki/TCP/IP "wikilink") 네트워크 인터페이스 변수의 구성, 제어, 조회를 위한 기능을 갖추고 있다. ifconfig는 [BSD](https://ko.wikipedia.org/wiki/BSD "wikilink") TCP/IP 제품군의 일부로서 4.2BSD에 처음 등장하였다.

ifconfig 는 네트워크 인터페이스 구성(interface configuration)의 약자이다.\[1\]

## 용도

`ifconfig`는 일반적으로 네트워크 인터페이스의 [IP 주소와](https://ko.wikipedia.org/wiki/IP_주소 "wikilink") [넷마스크](https://ko.wikipedia.org/wiki/넷마스크 "wikilink")의 설정 및 인터페이스의 활성화/비활성화 등을 위해 사용된다.\[2\] 시동 시에 유닉스 계열 운영 체제는 ifconfig를 호출하는 셸 스크립트를 통해 네트워크 인터페이스를 초기화한다. 시스템 관리자들은 상호작용 도구의 하나인 이 유틸리티를 사용하여 네트워크 인터페이스 변수를 표시하고 분석할 수 있다. 다음의 두 예제는 도구의 출력을 표시하며 각각 [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink") 기반 호스트(인터페이스 [eth](https://ko.wikipedia.org/wiki/이더넷 "wikilink")0)와 [OpenBSD](https://ko.wikipedia.org/wiki/OpenBSD "wikilink") 설치본의 [ural](https://ko.wikipedia.org/wiki/Ralink "wikilink")0 인터페이스가 있는 하나의 활성화된 인터페이스를 조회하는 모습을 보여주고 있다.

```
 eth0      Link encap:Ethernet  HWaddr 00:0F:20:CF:8B:42
           inet addr:217.149.127.10  Bcast:217.149.127.63  Mask:255.255.255.192
           UP BROADCAST RUNNING MULTICAST  MTU:1500  Metric:1
           RX packets:2472694671 errors:1 dropped:0 overruns:0 frame:0
           TX packets:44641779 errors:0 dropped:0 overruns:0 carrier:0
           collisions:0 txqueuelen:1000
           RX bytes:1761467179 (1679.7 Mb)  TX bytes:2870928587 (2737.9 Mb)
           Interrupt:28
```

```
 ural0: flags=8843<UP,BROADCAST,RUNNING,SIMPLEX,MULTICAST> mtu 1500
         lladdr 00:0d:0b:ed:84:fb
         media: IEEE802.11 DS2 mode 11b hostap (autoselect mode 11b hostap)
         status: active
         ieee80211: nwid ARK chan 11 bssid 00:0d:0b:ed:84:fb  100dBm
         inet 172.30.50.1 netmask 0xffffff00 broadcast 172.30.50.255
         inet6 fe80::20d:bff:feed:84fb%ural0 prefixlen 64 scopeid 0xa
```

  - HWaddr은 하드웨어 주소(hardware address), 즉 [MAC 주소를](https://ko.wikipedia.org/wiki/MAC_주소 "wikilink") 가리킨다.
  - txqueuelen 변수는 [이더넷 프레임의](https://ko.wikipedia.org/wiki/이더넷_프레임 "wikilink") 수, 그리고 [네트워크 스케줄러에](https://ko.wikipedia.org/wiki/네트워크_스케줄러 "wikilink") 의해 관리되는 버퍼의 크기를 통해 측정된다.

### 매체 접근 제어 기능

`ifconfig`는 또한 인터페이스의 [매체 접근 제어](https://ko.wikipedia.org/wiki/매체_접근_제어 "wikilink")(MAC) 주소를 변경하는데 사용할 수 있다. 이 과정에서 네트워크 인터페이스는 `iconfig`를 이용하여 먼저 비활성화하고(down) 그 뒤 MAC을 변경한다:

`ifconfig wlan0 down`
`ifconfig wlan0 hw ether 00:11:22:33:44:55`
`ifconfig wlan0 up`

## 참고

  - [ip (명령어)](https://ko.wikipedia.org/wiki/ip_\(명령어\) "wikilink")
  - [netstat](https://ko.wikipedia.org/wiki/netstat "wikilink")

## 각주

## 외부 링크

  - [`ifconfig(8)`](http://net-tools.sourceforge.net/man/ifconfig.8.html), official [manpage](https://ko.wikipedia.org/wiki/manpage "wikilink") for Linux net-tools ifconfig
  - [`ifconfig(8)`](http://www.freebsd.org/cgi/man.cgi?query=ifconfig), manpage for the FreeBSD ifconfig
  - [`ifconfig(8)`](http://www.openbsd.org/cgi-bin/man.cgi?query=ifconfig), manpage for the OpenBSD ifconfig

[분류:라우팅](https://ko.wikipedia.org/wiki/분류:라우팅 "wikilink") [분류:유닉스 네트워크 관련 소프트웨어](https://ko.wikipedia.org/wiki/분류:유닉스_네트워크_관련_소프트웨어 "wikilink")

1.  [제목 : 리눅스 네트워크관리 2편](https://www.linux.co.kr/home/lecture/?leccode=10878)
2.  *Linux Network Administrators Guide* [Section 5.7. Interface Configuration for IP](http://www.faqs.org/docs/linux_network/x-087-2-iface.interface.html)