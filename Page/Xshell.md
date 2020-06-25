> This article is converted from Wikipedia: [Xshell](https://ko.wikipedia.org/wiki/Xshell).


**Xshell**은 [(주)넷사랑컴퓨터의](../Page/넷사랑컴퓨터.md "wikilink") [SSH](https://ko.wikipedia.org/wiki/SSH "wikilink"), [텔넷](../Page/텔넷.md "wikilink"), [Rlogin](../Page/Rlogin.md "wikilink")을 위한 [단말 에뮬레이터](../Page/단말_에뮬레이터.md "wikilink") [클라이언트](https://ko.wikipedia.org/wiki/클라이언트 "wikilink")이다.\[1\]\[2\] 호스트별로 개별 세션 파일을 만들 수 있으며 세션별 보기 방식을 탭 형식으로 제공하여 동시간의 호스트 운영 및 관리에 용이한 특성이 있다.

## 역사

  - Xshell은 2002년에 처음 출시되었다.
  - 2005년 5월에는 버전 2가, 2008년 6월에는 버전 3이 출시되었다.
  - 2010년 5월에는 버전 4가 출시되고 이 때부터 엔터프라이즈용 에디션이 제공되기 시작했다.
  - 2014년 11월에는 버전 5가 출시되었다.
  - 2018년 4월 24일에는 버전 6가 출시되었다.

## 라이선스

Xshell은 사유 소프트웨어로서 개인 사용자에 한해 무료이며 기업은 유료 라이선스가 필요하다. Xshell 단일 라이선스 및 Xmanager, [Xftp](../Page/Xftp.md "wikilink"), Xlpd가 포함된 기업용 엔터프라이즈 라이선스가 있다.\[3\]

## 시스템 사양

버전 6 기준 시스템 최소 사양은 다음과 같다.\[4\]

|           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| --------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **운영체제**  | [Windows 10](https://ko.wikipedia.org/wiki/Windows_10 "wikilink"), [Windows 8.1](https://ko.wikipedia.org/wiki/Windows_8.1 "wikilink"), [Windows 7](https://ko.wikipedia.org/wiki/Windows_7 "wikilink"), [Windows Server 2019](https://ko.wikipedia.org/wiki/Windows_Server_2019 "wikilink"), [Windows Server 2016](https://ko.wikipedia.org/wiki/Windows_Server_2016 "wikilink"), [Windows Server 2012](https://ko.wikipedia.org/wiki/Windows_Server_2012 "wikilink"), Windows Server 2008 SP 1, Windows Vista SP 1, Citrix MetaFrame for Windows |
| **CPU**   | Intel® Pentium 이상                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **메모리**   | 512 MB 이상                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **하드디스크** | 50 MB 이상                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |

## 기능

기능은 다음과 같다.\[5\]

  - SSH1, SSH2, [Telnet](https://ko.wikipedia.org/wiki/Telnet "wikilink"), [rlogin](https://ko.wikipedia.org/wiki/rlogin "wikilink"), [Serial](https://ko.wikipedia.org/wiki/Serial "wikilink"), [SFTP](https://ko.wikipedia.org/wiki/SFTP "wikilink"), [FTP](https://ko.wikipedia.org/wiki/FTP "wikilink") 프로토콜 지원
  - 사용자 지정 유저 인터페이스 (분리가 가능한 탭 그룹 관리, 레이아웃 관리, 사용자 지정 테마)
  - 커스텀 마우스 및 키보드 매핑
  - [IPv6](../Page/IPv6.md "wikilink") 지원
  - 터미널 다중 세션 동시 키 입력
  - 스크립트 지원 ([비주얼 베이직](../Page/비주얼_베이직.md "wikilink"), [자바스크립트](../Page/자바스크립트.md "wikilink"), [파이썬](../Page/파이썬.md "wikilink"))
  - 사용자 키 및 호스트 키 관리
  - [Zmodem](https://ko.wikipedia.org/wiki/ZMODEM "wikilink"), [Xmodem](../Page/XMODEM.md "wikilink"), [Ymodem](https://ko.wikipedia.org/wiki/YMODEM "wikilink"), [SFTP](https://ko.wikipedia.org/wiki/SFTP "wikilink") 등의 파일 전송 유틸리티
  - Xftp 및 Xmanager 와의 연동
  - [X11](../Page/X_윈도_시스템.md "wikilink") 포워딩
  - SOCKS 4/5 프록시
  - SSH 터널링
  - 터미널 하이라이트 편집
  - 작성 창, 빠른 명령 창
  - 웹 검색 기능
  - [ASCII](https://ko.wikipedia.org/wiki/ASCII "wikilink") 및 NonASCII 문자열에 대한 글꼴 지정

## 보안

  - [공개 키 암호 방식](../Page/공개_키_암호_방식.md "wikilink")
  - [대칭 키 암호](../Page/대칭_키_암호.md "wikilink")
  - GSSAPI ([MIT Kerberos](../Page/커베로스.md "wikilink"), Microsoft SSPI)
  - SSH PKCS 11 인증
  - 마스터 패스워드 인증, 화면 잠금 기능, 키보드 인터렉티브 인증 지원

| 암호화 알고리즘                      | MAC                           | 키 교환 알고리즘                            |
| ----------------------------- | ----------------------------- | ------------------------------------ |
| 3des-cbc                      | hmac-md5\[6\]                 | curve25519-sha256@libssh.org         |
| aes128-cbc                    | hmac-md5-96                   | ecdh-sha2-nistp256                   |
| aes128-ctr                    | hmac-md5-96-etm@openssh.com   | ecdh-sha2-nistp384                   |
| aes128-gcm@openssh.com        | hmac-md5-etm@openshh.com      | ecdh-sha2-nistp521                   |
| aes192_cbc                   | hmac-ripemd160                | diffie-hellman-group14-sha1          |
| aes192-ctr                    | hmac-ripemd160@openssh.com    | diffie-hellman-group1-sha1           |
| aes256-cbc                    | hmac-sha1                     | diffie-hellman-group-exchange-sha1   |
| aes256-ctr                    | hmac-sha1-96                  | diffie-hellman-group-exchange-sha256 |
| aes258-gcm@openssh.com        | hmac-sha1-96-etm@openssh.com  |                                      |
| arcfour                       | hmac-sha1-etm@openssh.com     |                                      |
| arcfour 128                   | hmac-sha2-256                 |                                      |
| arcfour 256                   | hmac-sha2-256-etm@openssh.com |                                      |
| blowfish-cbc                  | hmac-sha2-512                 |                                      |
| cast128-cbc                   | hmac-sha-512-etm@openssh.com  |                                      |
| chacha20-poly1305@openssh.com |                               |                                      |
| rijndael128-cbc               |                               |                                      |
| rijndael192-cbc               |                               |                                      |
| rijndael256-cbc               |                               |                                      |
| rijndael-cbc@lysator.liu.se   |                               |                                      |

## 같이 보기

  - [단말 에뮬레이터 목록](../Page/단말_에뮬레이터_목록.md "wikilink")
  - [PuTTY](../Page/PuTTY.md "wikilink")

## 각주

[분류:암호 소프트웨어](https://ko.wikipedia.org/wiki/분류:암호_소프트웨어 "wikilink") [분류:터미널 에뮬레이터](https://ko.wikipedia.org/wiki/분류:터미널_에뮬레이터 "wikilink") [분류:윈도우 전용 소프트웨어](https://ko.wikipedia.org/wiki/분류:윈도우_전용_소프트웨어 "wikilink")

1.  <https://betanews.com/2014/11/27/xshell-is-a-one-stop-ssh-sftp-terminal-emulator/>, Mike Williams, Betanews, November 27, 2014
2.  <http://www.filecluster.com/reviews/042014/xshell-a-telnet-and-rlogin-emulator/>, Adam Jones, Filecluster, April 20, 2014
3.  <https://www.netsarang.com/ko/all-downloads/>
4.  [시스템 요구 사항](https://www.netsarang.com/ko/xshell-all-features)
5.  <https://www.vladan.fr/putty-alternative-called-xshell-5-free-for-home-users-and-schools/>, Vladan SEGET, July 13, 2016
6.  해시 기반 메세지 인증 코드