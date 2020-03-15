> This article is converted from Wikipedia: [Xftp](https://ko.wikipedia.org/wiki/Xftp).


**Xftp**는 [넷사랑컴퓨터](https://ko.wikipedia.org/wiki/넷사랑컴퓨터 "wikilink")에서 개발한 [FTP](https://ko.wikipedia.org/wiki/FTP "wikilink"), [SFTP](../Page/SSH_파일_전송_프로토콜.md "wikilink") 클라이언트 프로그램이다.

## 역사

Xftp는 GUI 기반의 [FTP](https://ko.wikipedia.org/wiki/FTP "wikilink"), [SFTP](../Page/SSH_파일_전송_프로토콜.md "wikilink") 클라이언트로 2004년에 정식으로 출시되었다.

  - 2004년 10월 : Xftp 1.2 정식 버전을 출시하였다.
  - 2008년 6월 : Xftp 3 정식 버전을 출시하였다. 가정 및 학교 사용자를 대상으로 Xftp 무료 라이선스를 제공하기 시작했다.
  - 2010년 5월 : Xftp 4 정식 버전을 출시하였다.
  - 2014년 11월 : Xftp 5 정식 버전을 출시하였다.
  - 2018년 4월 24일 : Xftp 6 정식 버전을 출시하였다.

## 기능

최신 버전을 기준으로 Xftp의 기능은 다음과 같다.

  - 광범위한 프로토콜 지원 ([FTP](https://ko.wikipedia.org/wiki/FTP "wikilink"), [SFTP](../Page/SSH_파일_전송_프로토콜.md "wikilink"))
  - 탭과 커맨더 환경으로 구성 및 폴더 트리 지원
  - 사용자가 정의 가능한 인터페이스 (전송 대기열, 링크 모음, 빠른 연결 표시줄 등)
  - [IPv6](https://ko.wikipedia.org/wiki/IPv6 "wikilink") 지원
  - SSH [ZLIB](https://ko.wikipedia.org/wiki/Zlib "wikilink") 압축 지원
  - 명령줄 인터페이스 지원
  - 호스트 키/사용자 키 관리
  - 폴더 동기화 지원
  - Windows Shell 메뉴 지원
  - 폴더 경로 북마크 지원
  - FTP 로깅 및 세션 로깅

## 호환성

Xftp는 [Windows XP](https://ko.wikipedia.org/wiki/Windows_XP "wikilink"), [Windows Vista와](https://ko.wikipedia.org/wiki/Windows_Vista "wikilink") [Windows 7](https://ko.wikipedia.org/wiki/Windows_7 "wikilink"), [Windows 8](https://ko.wikipedia.org/wiki/Windows_8 "wikilink"), [Windows 8.1](https://ko.wikipedia.org/wiki/Windows_8.1 "wikilink"), [Windows 10](https://ko.wikipedia.org/wiki/Windows_10 "wikilink"), [Windows Server에서](https://ko.wikipedia.org/wiki/Windows_Server "wikilink") 실행이 가능하다. 버전 6 부터는 [Windows XP를](https://ko.wikipedia.org/wiki/Windows_XP "wikilink") 지원하지 않는다.

## 라이선스

Xftp는 가정 및 학교에서 무료 라이선스 사용이 가능하다.\[1\] 무료 버전은 국제적으로 학교 및 대학에서 활용되고 있다. 기업 사용자는 라이선스 구매가 필요하다.

## 시스템 사양

버전 6 기준 시스템 최소 사양은 다음과 같다.\[2\]

|           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| --------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **운영체제**  | [Windows 10](https://ko.wikipedia.org/wiki/Windows_10 "wikilink"), [Windows 8.1](https://ko.wikipedia.org/wiki/Windows_8.1 "wikilink"), [Windows 7](https://ko.wikipedia.org/wiki/Windows_7 "wikilink"), [Windows Server 2019](https://ko.wikipedia.org/wiki/Windows_Server_2019 "wikilink"), [Windows Server 2016](https://ko.wikipedia.org/wiki/Windows_Server_2016 "wikilink"), [Windows Server 2012](https://ko.wikipedia.org/wiki/Windows_Server_2012 "wikilink"), Windows Server 2008 SP 1, Windows Vista SP 1, Citrix MetaFrame for Windows |
| **CPU**   | Intel® Pentium 이상                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **메모리**   | 512 MB 이상                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **하드디스크** | 50 MB 이상                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |

## 보안

  - [공개 키 암호 방식](https://ko.wikipedia.org/wiki/공개_키_암호_방식 "wikilink")
  - [대칭 키 암호](https://ko.wikipedia.org/wiki/대칭_키_암호 "wikilink")
  - [PKCS\#11](https://ko.wikipedia.org/wiki/PKCS#11 "wikilink") 인증 지원
  - SSH 에이전트 지원
  - 추가적인 보안 기능

| 암호화 알고리즘                      | MAC                           | 키 교환 알고리즘                            |
| ----------------------------- | ----------------------------- | ------------------------------------ |
| 3des-cbc                      | hmac-md5\[3\]                 | curve25519-sha256@libssh.org         |
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

  - [파일질라](https://ko.wikipedia.org/wiki/파일질라 "wikilink")
  - [토탈 커맨더](https://ko.wikipedia.org/wiki/토탈_커맨더 "wikilink")
  - [WinSCP](../Page/WinSCP.md "wikilink")

## 각주

[분류:윈도우 전용 소프트웨어](https://ko.wikipedia.org/wiki/분류:윈도우_전용_소프트웨어 "wikilink")

1.
2.
3.  해시 기반 메세지 인증 코드