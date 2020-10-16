> This article is converted from Wikipedia: [Hosts](https://ko.wikipedia.org/wiki/Hosts).


**hosts** 파일은 [운영 체제가](../Page/운영_체제.md "wikilink") [호스트 이름을](https://ko.wikipedia.org/wiki/호스트_이름 "wikilink") [IP 주소에](../Page/IP_주소.md "wikilink") 매핑할 때 사용하는 [컴퓨터 파일이다](../Page/컴퓨터_파일.md "wikilink"). 이 hosts 파일은 [플레인 텍스트](../Page/플레인_텍스트.md "wikilink") 파일이며 전통적으로 *hosts*라는 이름을 사용한다.

## 파일 내용

이 hosts 파일에는 여러 줄이 올 수 있으며, 이 줄의 첫 문자 필드에는 IP 주소가, 그 다음에는 하나 이상의 호스트 이름이 위치한다. 각 필드는 흰 공백 탭으로 구별되는데, 역사적인 이유로 탭이 선호되지만 공백도 사용된다. 주석 줄을 포함할 수도 있는데 해시 문자(\#)를 줄의 처음 위치에 놓으면 된다. 파일 내의 완전히 비어있는 줄들은 무시된다. 이를테면 일반적인 hosts 파일은 다음과 같다:

    127.0.0.1  localhost loopback
    ::1        localhost

이 예는 오직 시스템과 시스템 호스트 이름의 루프백 주소를 위한 엔트리만 포함하고 있으며, 이것이 일반적인 기본 hosts 파일의 내용이다. 이 예는 IP 주소가 여러 개의 호스트 이름을 가질 수 있음을 나타내며(localhost, loopback) 호스트 이름은 [IPv4](../Page/IPv4.md "wikilink")와 [IPv6](../Page/IPv6.md "wikilink") 주소에 매핑할 수 있다.

## 파일 시스템에서의 위치

[파일 시스템](../Page/파일_시스템.md "wikilink") 계층에서의 hosts 파일의 위치는 운영 체제에 따라 다양하다. 파일 이름은 일반적으로 확장자가 없는 *hosts*로 되어 있다.

<table>
<thead>
<tr class="header">
<th><p>운영 체제</p></th>
<th><p>버전</p></th>
<th><p>위치</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="../Page/유닉스.md" title="wikilink">유닉스</a>, <a href="../Page/유닉스_계열.md" title="wikilink">유닉스 계열</a>, <a href="../Page/POSIX.md" title="wikilink">POSIX</a></p></td>
<td></td>
<td><p>/etc/hosts[1]</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/마이크로소프트_윈도우.md" title="wikilink">마이크로소프트 윈도우</a></p></td>
<td><p><a href="../Page/윈도우_3.1x.md" title="wikilink">3.1</a></p></td>
<td><p><a href="../Page/환경_변수.md" title="wikilink">%WinDir%</a>\HOSTS</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/윈도우_95.md" title="wikilink">95</a>, <a href="../Page/윈도우_98.md" title="wikilink">98</a>, <a href="https://ko.wikipedia.org/wiki/윈도우_Me" title="wikilink">ME</a></p></td>
<td><p><a href="../Page/환경_변수.md" title="wikilink">%WinDir%</a>\hosts[2]</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/윈도우_NT.md" title="wikilink">NT</a>, <a href="../Page/윈도우_2000.md" title="wikilink">2000</a>, <a href="../Page/윈도우_XP.md" title="wikilink">XP</a>,[3] <a href="../Page/윈도우_서버_2003.md" title="wikilink">2003</a>, <a href="../Page/윈도우_비스타.md" title="wikilink">비스타</a>,<br />
<a href="../Page/윈도우_서버_2008.md" title="wikilink">2008</a>, <a href="https://ko.wikipedia.org/wiki/윈도우_7" title="wikilink">7</a>, <a href="../Page/윈도우_서버_2012.md" title="wikilink">2012</a>, <a href="../Page/윈도우_8.md" title="wikilink">8</a>, <a href="../Page/윈도우_10.md" title="wikilink">10</a></p></td>
<td><p><a href="../Page/환경_변수.md" title="wikilink">%SystemRoot%</a>\System32\drivers\etc\hosts [4]</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/윈도우_모바일.md" title="wikilink">윈도우 모바일</a>, <a href="../Page/윈도우_폰.md" title="wikilink">윈도우 폰</a></p></td>
<td></td>
<td><p>HKEY_LOCAL_MACHINE\Comm\Tcpip\Hosts 아래의 <a href="../Page/윈도우_레지스트리.md" title="wikilink">레지스트리</a> 키</p></td>
</tr>
<tr class="even">
<td><p>애플 <a href="../Page/매킨토시.md" title="wikilink">매킨토시</a></p></td>
<td><p>9 이상</p></td>
<td><p>환경설정 또는 시스템 폴더</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/OS_X" title="wikilink">맥 OS X</a> 10.0 – 10.1.5[5]</p></td>
<td><p>(NetInfo나 niload를 통해 추가)</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/OS_X" title="wikilink">맥 OS X</a> 10.2 이상</p></td>
<td><p>/etc/hosts (/private/etc/hosts의 <a href="../Page/심볼릭_링크.md" title="wikilink">심볼릭 링크</a>)[6]</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/넷웨어.md" title="wikilink">노벨 넷웨어</a></p></td>
<td></td>
<td><p>SYS:etc\hosts</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/OS/2" title="wikilink">OS/2</a> &amp; <a href="https://ko.wikipedia.org/wiki/eComStation" title="wikilink">eComStation</a></p></td>
<td></td>
<td><p>"시동 드라이브":\mptn\etc\</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/심비안OS" title="wikilink">심비안</a></p></td>
<td><p>심비안 OS 6.1–9.0</p></td>
<td><p>C:\system\data\hosts</p></td>
</tr>
<tr class="even">
<td><p>심비안 OS <a href="https://ko.wikipedia.org/wiki/심비안" title="wikilink">9.1+</a></p></td>
<td><p>C:\private\10000882\hosts</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/MorphOS" title="wikilink">MorphOS</a></p></td>
<td><p>넷스택</p></td>
<td><p>ENVARC:sys/net/hosts</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/아미가OS.md" title="wikilink">아미가OS</a></p></td>
<td><p>4</p></td>
<td><p>DEVS:Internet/hosts</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/AROS" title="wikilink">AROS</a></p></td>
<td></td>
<td><p>ENVARC:AROSTCP/db/hosts</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/안드로이드_(운영_체제).md" title="wikilink">안드로이드</a></p></td>
<td></td>
<td><p>/etc/hosts (/system/etc/hosts의 심볼릭 링크)</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/iOS" title="wikilink">iOS</a></p></td>
<td><p>iOS 2.0 이상</p></td>
<td><p>/etc/hosts (/private/etc/hosts의 심볼릭 링크)</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/TOPS-20" title="wikilink">TOPS-20</a></p></td>
<td></td>
<td><p><SYSTEM>HOSTS.TXT</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/플랜_9" title="wikilink">플랜 9</a></p></td>
<td></td>
<td><p>/lib/ndb/hosts</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/BeOS.md" title="wikilink">BeOS</a></p></td>
<td></td>
<td><p>/boot/beos/etc/hosts[7]</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/하이쿠_(운영_체제)" title="wikilink">하이쿠</a></p></td>
<td></td>
<td><p>/boot/common/settings/network/hosts[8]</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/OpenVMS.md" title="wikilink">OpenVMS</a></p></td>
<td><p>UCX</p></td>
<td><p>UCX$HOST</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/TCPware" title="wikilink">TCPware</a></p></td>
<td><p>TCPIP$HOST</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/RISC_OS.md" title="wikilink">RISC OS</a></p></td>
<td></td>
<td><p>!Boot.Resources.!Internet.files.Hosts</p></td>
</tr>
<tr class="odd">
<td><p>나중에 나온 시동 시퀀스</p></td>
<td><p>!Boot.Choices.Hardware.Disabled.Internet.Files.Hosts[9]</p></td>
<td></td>
</tr>
</tbody>
</table>

## 보안 문제

hosts 파일은 악성 소프트웨어의 공격 벡터로 악용될 수 있다. 이 파일은 이를테면 [애드웨어](../Page/애드웨어.md "wikilink")나 [컴퓨터 바이러스](../Page/컴퓨터_바이러스.md "wikilink"), [트로이 목마](../Page/트로이_목마_\(컴퓨팅\).md "wikilink") 소프트웨어를 통해 수정됨으로써 의도한 곳으로 가야할 트래픽을 원치 않거나 악의적인 콘텐츠를 호스팅하는 사이트로 우회시킬 수 있다.\[10\]

## 각주

<references />

[분류:도메인 네임 시스템](https://ko.wikipedia.org/wiki/분류:도메인_네임_시스템 "wikilink") [분류:설정 파일](https://ko.wikipedia.org/wiki/분류:설정_파일 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.  RISC OS 6.14
10.