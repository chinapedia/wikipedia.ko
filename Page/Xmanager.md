> This article is converted from Wikipedia: [Xmanager](https://ko.wikipedia.org/wiki/Xmanager).


**Xmanager**는 [(주)넷사랑컴퓨터에서](../Page/넷사랑컴퓨터.md "wikilink") 개발한 윈도우 응용프로그램이다. X 응용프로그램을 윈도우 환경에서 사용할 수 있도록 하는 PC X 서버 소프트웨어로 원격 유닉스/리눅스에 설치된 X 응용프로그램을 로컬의 윈도우 응용프로그램들처럼 사용할 수 있다.

## 역사

  - Xmanager는 1997년에 처음 출시되었다. 정보통신부 신소프트웨어상품상을 수상하였다.\[1\]
  - 2010년 5월에는 버전 4가 출시되었으며 통합 제품군인 엔터프라이즈 패키지가 판매되기 시작했다.
  - 2014년 11월에는 버전 5가 출시되었다.
  - 2018년 4월 24일에는 버전 6가 출시되었다.\[2\]

## 시스템 사양

버전 6 기준 시스템 최소 사양은 다음과 같다.\[3\]

|           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| --------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **운영체제**  | [Windows 10](https://ko.wikipedia.org/wiki/Windows_10 "wikilink"), [Windows 8.1](https://ko.wikipedia.org/wiki/Windows_8.1 "wikilink"), [Windows 7](https://ko.wikipedia.org/wiki/Windows_7 "wikilink"), [Windows Server 2019](https://ko.wikipedia.org/wiki/Windows_Server_2019 "wikilink"), [Windows Server 2016](https://ko.wikipedia.org/wiki/Windows_Server_2016 "wikilink"), [Windows Server 2012](https://ko.wikipedia.org/wiki/Windows_Server_2012 "wikilink"), Windows Server 2008 SP 1, Windows Vista SP 1, Citrix MetaFrame for Windows |
| **CPU**   | Intel® Pentium 이상                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **메모리**   | 512 MB 이상                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **하드디스크** | 200 MB 이상                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |

## 라이선스

Xmanager는 사유 소프트웨어로서 개인 및 기업 사용자의 경우 유료 라이선스가 필요하다. 라이선스는 상업용과 교육용이 존재하며 Xmanager 단일 라이선스와 [Xshell](../Page/Xshell.md "wikilink"), [Xftp](../Page/Xftp.md "wikilink"), Xlpd가 포함된 엔터프라이즈 라이선스로 구분되어 있다. \[4\]

## 기능

Xmanager 최신 버전 기준 주요 기능은 다음과 같다.\[5\]

  - [XDMCP](https://ko.wikipedia.org/wiki/XDMCP "wikilink") 및 [Secure XDMCP](https://ko.wikipedia.org/wiki/Secure_XDMCP "wikilink") 연결 지원
  - Passive Mode, Broadcast Session
  - GLX 1.3, OpenGL 1.2 확장
  - XRANDR, XKEYBOARD, RENDER 등의 X 확장 기능
  - 단일 윈도우 및 다중 윈도우 선택
  - [Xshell](../Page/Xshell.md "wikilink")과 [Xftp](../Page/Xftp.md "wikilink")와의 상호 연동
  - 호스트 키 및 사용자 키 관리
  - [IPv6](../Page/IPv6.md "wikilink") 지원
  - 호스트 액세스 제어
  - GUI 키보드 편집기
  - 주소 창을 이용한 즉석 연결

## 보안

  - [공개 키 암호 방식](../Page/공개_키_암호_방식.md "wikilink")
  - 호스트별 액세스 제어
  - SSH 보안 터널을 이용한 [XDMCP](https://ko.wikipedia.org/wiki/XDMCP "wikilink") 접속
  - SSH [PKCS\#11](https://ko.wikipedia.org/wiki/PKCS#11 "wikilink") 인증
  - 마스터 패스워드 인증

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

## 각주

[분류:윈도우 전용 소프트웨어](https://ko.wikipedia.org/wiki/분류:윈도우_전용_소프트웨어 "wikilink")

1.  <https://news.v.daum.net/v/19970204114200129?f=o>
2.  <https://blog.netsarang.com/ko/1765/introducing-version-6/>
3.  [시스템 요구 사항](https://www.netsarang.com/ko/xmanager-all-features)
4.
5.  [Xmanager 제품 기능](https://www.netsarang.com/ko/xmanager-all-features)
6.  해시 기반 메세지 인증 코드