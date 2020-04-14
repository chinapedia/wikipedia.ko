> This article is converted from Wikipedia: [SSH 파일 전송 프로토콜](https://ko.wikipedia.org/wiki/SSH_파일_전송_프로토콜).


[컴퓨팅](../Page/컴퓨팅.md "wikilink")에서 **SSH 파일 전송 프로토콜**(SSH File Transfer Protocol) 또는 **보안 파일 전송 프로토콜**(Secure File Transfer Protocol, **SFTP**)은 신뢰할 수 있는 [데이터 스트림을](https://ko.wikipedia.org/wiki/데이터_스트림 "wikilink") 통해 [파일 접근](https://ko.wikipedia.org/wiki/파일_접근 "wikilink"), [파일 전송](https://ko.wikipedia.org/wiki/파일_전송 "wikilink"), [파일 관리를](https://ko.wikipedia.org/wiki/파일_관리 "wikilink") 제공하는 [네트워크 프로토콜이다](https://ko.wikipedia.org/wiki/네트워크_프로토콜 "wikilink"). [국제 인터넷 표준화 기구](../Page/국제_인터넷_표준화_기구.md "wikilink")(IETF)가 보안 파일 전송 기능을 제공할 목적으로 [시큐어 셸](../Page/시큐어_셸.md "wikilink") 프로토콜 (SSH) 버전 2.0의 확장으로 설계하였다. IETF [인터넷 초안에](https://ko.wikipedia.org/wiki/인터넷_초안 "wikilink") 따르면 이 프로토콜이 SSH-2 프로토콜의 문맥 안에 기술되어 있지만 [전송 계층 보안](../Page/전송_계층_보안.md "wikilink")(TLS)를 통하는 보안 파일 전송 프로그램이나 [VPN](https://ko.wikipedia.org/wiki/VPN "wikilink") 응용 프로그램의 관리 정보 전송과 같은 다른 수많은 응용 프로그램들에도 사용할 수 있다고 언급되어 있다.

이 프로토콜은 SSH와 같은 [보안 채널을](https://ko.wikipedia.org/wiki/보안_채널 "wikilink") 통해 수행되는데, 이 말은 서버가 이미 클라이언트와 인증이 되어 있으면서, 클라이언트 사용자 증명을 프로토콜에 이용할 수 있는 상태여야 한다는 것을 뜻한다.

## 기능

파일 전송만을 다루는 [SCP](https://ko.wikipedia.org/wiki/시큐어_카피 "wikilink") 프로토콜과 비교하면, SFTP 프로토콜은 원격 [파일 시스템](../Page/파일_시스템.md "wikilink") 프로토콜과 같이 원격 파일에 어느 정도의 조작을 허용한다. SFTP [클라이언트](https://ko.wikipedia.org/wiki/클라이언트 "wikilink")의 추가 기능에는 중단된 전송 재개, 디렉터리 나열, 원격 파일 제거를 포함한다. \[1\]

SFTP는 SCP 보다 더 플랫폼 독립적인 경향이 강하다. 이를테면 SCP를 이용하면 클라이언트에서 규정한 [와일드카드의](https://ko.wikipedia.org/wiki/와일드카드_문자 "wikilink") 확장은 서버에 달려있지만, SFTP의 설계는 이러한 문제를 회피한다. SCP가 [유닉스](../Page/유닉스.md "wikilink") 플랫폼에 주로 구현되어 있는 반면, SFTP 서버들은 대부분의 플랫폼에서 흔히 이용이 가능하다.

SFTP는 [SSH](../Page/시큐어_셸.md "wikilink") 기반으로 동작하는 [FTP이](../Page/파일_전송_프로토콜.md "wikilink") 아니며 [국제 인터넷 표준화 기구](../Page/국제_인터넷_표준화_기구.md "wikilink")(IETF) SECSH [워킹 그룹에](https://ko.wikipedia.org/wiki/워킹_그룹 "wikilink") 의해 처음부터 설계된 새로운 프로토콜이다. [단순 파일 전송 프로토콜과](https://ko.wikipedia.org/wiki/단순_파일_전송_프로토콜 "wikilink") 혼동되기도 한다. \[2\]

이 프로토콜 그 자체는 인증과 보안을 제공하지 않는다. 기반 프로토콜이 이를 보안해 줄 것으로 예측할 뿐이다. SFTP는 [SSH](../Page/시큐어_셸.md "wikilink") 프로토콜 버전 2 구현체의 하위 시스템으로 자주 사용되며, 이는 같은 워킹 그룹에 의해 설계되고 있다. 그러나 SSH-1 및 이를 지원하는 구현체들, 또는 다른 데이터 스트림을 통해서도 수행이 가능하다. SSH-1을 통해 SFTP 서버를 구동하는 일은 플랫폼 독립적이지 않은데, 그 까닭은 SSH-1은 하위 시스템의 개념을 지원하지 않기 때문이다. SFTP 클라이언트가 SSH-1 서버에 접속하려 한다면 그 클라이언트는 서버 측 SFTP 서버 바이너리의 경로를 인지하고 있어야 한다.

업로드된 파일들은 타임스탬프처럼 자신들의 기본 특성과 연결될 수 있다. 이는 일반적인 [FTP](../Page/파일_전송_프로토콜.md "wikilink") 프로토콜 이상의 이점이 있는데, 이는 별도의 도움 없이 원래의 날짜/타임스탬프 특성을 포함하기 위해 업로드를 제공할 필요가 없음을 뜻한다.

## 역사 및 개발

[시큐어 셸](../Page/시큐어_셸.md "wikilink") 버전 2 프로토콜 (RFC 4251)의 개발을 맡았던 국제 인터넷 표준화 기구 (IETF) 워킹 그룹 "Secsh"는 안전한 파일 전송 기능의 표준 확장에 대한 초안 작성을 시도하였다. [인터넷 초안들이](https://ko.wikipedia.org/wiki/인터넷_초안 "wikilink") 만들어지면서 새로운 버전들로 이 프로토콜을 연이어 개정하였다.\[3\] 아직 초안이 표준화되기 전이었지만 소프트웨어 산업은 이 프로토콜의 다양한 버전들을 구현하기 시작하였다. 개발이 진척됨에 따라 Secsh 파일 전송 프로젝트의 범위는 [파일 접근과](https://ko.wikipedia.org/wiki/파일_접근 "wikilink") [파일 관리를](https://ko.wikipedia.org/wiki/파일_관리 "wikilink") 포함하는 데까지 확장되었다. 마침내 일부 위원회 구성원들이 SFTP를 단순히 [파일 접근이나](https://ko.wikipedia.org/wiki/파일_접근 "wikilink") [파일 전송](https://ko.wikipedia.org/wiki/파일_전송 "wikilink") 프로토콜이 아닌 [파일 시스템](../Page/파일_시스템.md "wikilink") 프로토콜로 보기 시작하자 개발은 중단되었는데, 이는 워킹 그룹의 범위를 넘어섰기 때문이다.\[4\] 7년의 중단 기간이 있었지만, 2013년 버전 3 초안을 기본으로 하는 SFTP의 작업을 다시 시작하고자 하는 시도가 있었다.\[5\]

### 버전 0 - 2

IETF의 참여 이전에, SFTP는 [SSH 커뮤니케이션스 보안의](https://ko.wikipedia.org/wiki/SSH_커뮤니케이션스_보안 "wikilink") 사유 프로토콜이었으며 이 프로토콜은 1997년 Sami Lehtinen의 도움으로 Tatu Ylönen가 설계한 것이다.\[6\] 버전 0 - 2와 버전 3 간의 차이점은 [section 10 of draft-ietf-secsh-filexfer-02](http://tools.ietf.org/html/draft-ietf-secsh-filexfer-02#section-10) 안에 나열되어 있다.

### 버전 3

IETF 시큐어 셸 파일 전송 프로젝트의 시작으로, Secsh 그룹은 SSH 파일 전송 프로토콜의 목적이 신뢰할 수 있는 데이터 스트림에 안전한 파일 전송 기능을 제공하는 것이며 SSH-2 프로토콜을 사용한 표준 파일 전송 프로토콜이 되고자 함임을 언급하였다.

IETF 인터넷 초안 00 - 02는 SFTP 프로토콜 버전 3의 개정판들을 정의한다.

  - [SSH File Transfer Protocol, Draft 00, January 2001](http://tools.ietf.org/html/draft-ietf-secsh-filexfer-00)
  - [SSH File Transfer Protocol, Draft 01, March 2001](http://tools.ietf.org/html/draft-ietf-secsh-filexfer-01)
  - [SSH File Transfer Protocol, Draft 02, October 2001](http://tools.ietf.org/html/draft-ietf-secsh-filexfer-02)

### 버전 4

IETF 인터넷 초안 03 - 04는 이 프로토콜의 버전 4의 개정판들을 정의한다.

  - [SSH File Transfer Protocol, Draft 03, October 2002](http://tools.ietf.org/html/draft-ietf-secsh-filexfer-03)
  - [SSH File Transfer Protocol, Draft 04, December 2002](http://tools.ietf.org/html/draft-ietf-secsh-filexfer-04)

### 버전 5

IETF 인터넷 초안 05는 이 프로토콜의 버전 5를 정의한다.

  - [SSH File Transfer Protocol, Draft 05, January 2004](http://tools.ietf.org/html/draft-ietf-secsh-filexfer-05)

### 버전 6

IETF 인터넷 초안 06 - 13은 이 프로토콜의 버전 6의 개정판들을 정의한다.

  - [SSH File Transfer Protocol, Draft 06, October 2004](http://tools.ietf.org/html/draft-ietf-secsh-filexfer-06)
  - [SSH File Transfer Protocol, Draft 07, March 2005](http://tools.ietf.org/html/draft-ietf-secsh-filexfer-07)
  - [SSH File Transfer Protocol, Draft 08, April 2005](http://tools.ietf.org/html/draft-ietf-secsh-filexfer-08)
  - [SSH File Transfer Protocol, Draft 09, June 2005](http://tools.ietf.org/html/draft-ietf-secsh-filexfer-09)
  - [SSH File Transfer Protocol, Draft 10, June 2005](http://tools.ietf.org/html/draft-ietf-secsh-filexfer-10)
  - [SSH File Transfer Protocol, Draft 11, January 2006](http://tools.ietf.org/html/draft-ietf-secsh-filexfer-11)
  - [SSH File Transfer Protocol, Draft 12, January 2006](http://tools.ietf.org/html/draft-ietf-secsh-filexfer-12)
  - [SSH File Transfer Protocol, Draft 13, July 2006](http://tools.ietf.org/html/draft-ietf-secsh-filexfer-13)

## 같이 보기

  - [FTPS](../Page/FTPS.md "wikilink")
  - [파일 전송 프로토콜 목록](https://ko.wikipedia.org/wiki/파일_전송_프로토콜_목록 "wikilink")
  - [Lsh](https://ko.wikipedia.org/wiki/Lsh "wikilink")
  - [SSHFS](https://ko.wikipedia.org/wiki/SSHFS "wikilink")

## 각주

## 외부 링크

  - [Chrooted SFTP with Public Key Authentication](https://archive.is/20130103130850/http://www.ipsure.com/blog/2010/chrooted-sftp-with-public-key-authentication) – Integrating SFTP into FreeBSD production servers using the public key cryptography approach

[분류:암호 프로토콜](https://ko.wikipedia.org/wiki/분류:암호_프로토콜 "wikilink") [분류:네트워크 파일 전송 프로토콜](https://ko.wikipedia.org/wiki/분류:네트워크_파일_전송_프로토콜 "wikilink") [분류:시큐어 셸](https://ko.wikipedia.org/wiki/분류:시큐어_셸 "wikilink")

1.
2.
3.
4.
5.
6.  <ftp://ftp.ietf.org/ietf-mail-archive/secsh/2012-09.mail>