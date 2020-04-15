> This article is converted from Wikipedia: [FTP 명령어 목록](https://ko.wikipedia.org/wiki/FTP_명령어_목록).


아래는 **FTP 명령어 목록**이다.

| 명령어  | [RFC](../Page/RFC.md "wikilink") | 설명                                                                                                      |
| ---- | -------------------------------- | ------------------------------------------------------------------------------------------------------- |
| ABOR |                                  | 현재의 파일 전송 중단.                                                                                           |
| ACCT |                                  | 계정 정보.                                                                                                  |
| ADAT | RFC 2228                         | 인증/보안 데이터                                                                                               |
| ALLO |                                  | 파일을 받기 위해 충분한 디스크 공간 할당.                                                                                |
| APPE |                                  | 이어서 추가.                                                                                                 |
| AUTH | RFC 2228                         | 인증/보안 구조                                                                                                |
| CCC  | RFC 2228                         | 명령 채널 지우기                                                                                               |
| CDUP |                                  | 부모 디렉터리로 변경.                                                                                            |
| CONF | RFC 2228                         | 기밀 보호 명령                                                                                                |
| CWD  |                                  | 작업 디렉터리 변경                                                                                              |
| DELE |                                  | 파일 삭제                                                                                                   |
| ENC  | RFC 2228                         | 개인 정보 보호 채널                                                                                             |
| EPRT | RFC 2428                         | 서버 접속에 필요한 확장 주소 및 포트 지정.                                                                               |
| EPSV | RFC 2428                         | 확장 수동 모드 들어가기.                                                                                          |
| FEAT | RFC 2389                         | 서버가 추가한 기능 목록 보기                                                                                        |
| LANG | RFC 2640                         | 언어 탐색                                                                                                   |
| LIST |                                  | 지정한 경우 파일이나 디렉터리 정보를 반환. 지정하지 않은 경우 현재 작업 디렉터리 정보 반환.                                                   |
| LPRT | RFC 1639                         | 서버 접속에 필요한 긴 주소 및 목록 지정.                                                                                |
| LPSV | RFC 1639                         | 긴 수동 모드 들어가기                                                                                            |
| MDTM | RFC 3659                         | 지정한 파일의 마지막으로 수정한 시간 반환                                                                                 |
| MIC  | RFC 2228                         | 무결성 보호 명령                                                                                               |
| MKD  |                                  | 디렉터리 만들기                                                                                                |
| MLSD | RFC 3659                         | 디렉터리의 이름이 지정되면 디렉터리의 내용을 보여줌                                                                            |
| MLST | RFC 3659                         | 명령 줄에 입력한 데이터만 제공.                                                                                      |
| MODE |                                  | 전송 모드 설정 (스트림, 블록, 압축)                                                                                  |
| NLST |                                  | 지정한 디렉터리의 파일 이름 목록 반환.                                                                                  |
| NOOP |                                  | 동작 안 함 (더미 패킷: 대개 회선이 살아있는지를 살피기 위해 쓰임)                                                                 |
| OPTS | RFC 2389                         | 기능 옵션 선택.                                                                                               |
| PASS |                                  | 암호.                                                                                                     |
| PASV |                                  | 수동 모드 들어가기.                                                                                             |
| PBSZ | RFC 2228                         | 보호 버퍼 크기                                                                                                |
| PORT |                                  | 서버 접속에 필요한 주소 및 포트 지정.                                                                                  |
| PROT | RFC 2228                         | 데이터 채널 보호 수준.                                                                                           |
| PWD  |                                  | 작업 디렉터리 인쇄. 호스트 컴퓨터의 현재 디렉터리 반환.                                                                        |
| QUIT |                                  | 연결 끊기.                                                                                                  |
| REIN |                                  | 연결 다시 초기화.                                                                                              |
| REST |                                  | 지정한 지점에서 전송 다시 시작.                                                                                      |
| RETR |                                  | 파일 복사본 전송                                                                                               |
| RMD  |                                  | 디렉터리 제거                                                                                                 |
| RNFR |                                  | 이름 변경 원본 이름                                                                                             |
| RNTO |                                  | 이름 변경 대상 이름                                                                                             |
| SITE |                                  | 지정한 명령어를 원격 서버로 송신.                                                                                     |
| SIZE | RFC 3659                         | 파일 크기 반환                                                                                                |
| SMNT |                                  | 파일 구조 마운트.                                                                                              |
| STAT |                                  | 현재 상태 반환.                                                                                               |
| STOR |                                  | 데이터 입력 및 서버 쪽 파일로 저장.                                                                                   |
| STOU |                                  | 파일을 저만의 방식으로 저장.                                                                                        |
| STRU |                                  | 전송 구조 설정.                                                                                               |
| SYST |                                  | 시스템 유형 반환.                                                                                              |
| TYPE |                                  | 전송 모드 설정 ([ASCII](https://ko.wikipedia.org/wiki/ASCII "wikilink")/[바이너리](../Page/이진_파일.md "wikilink")). |
| USER |                                  | 인증 사용자 이름.                                                                                              |

## 같이 보기

  - [FTP 서버 반환 코드 목록](https://ko.wikipedia.org/wiki/FTP_서버_반환_코드_목록 "wikilink")

## 외부 링크

  - RFC 697 - CWD Command of FTP

  - RFC 959 - File Transfer Protocol (FTP)

  - RFC 1639 - FTP Operation Over Big Address Records (FOOBAR)

  - RFC 2228 - FTP Security Extensions

  - RFC 2389 - Feature negotiation mechanism for the File Transfer Protocol

  - RFC 2428 - FTP Extensions for IPv6 and NATs

  - RFC 2640 - Internationalization of the File Transfer Protocol

  - RFC 3659 - Extensions to FTP

  - RFC 5797 - FTP Command and Extension Registry

  - RFC 7151 - File Transfer Protocol HOST Command for Virtual Hosts

  - [IANA FTP Commands and Extensions registry](http://www.iana.org/assignments/ftp-commands-extensions/ftp-commands-extensions.xhtml) - The official registry of FTP Commands and Extensions

  - [Raw FTP command list](http://www.nsftools.com/tips/RawFTP.htm)

[분류:파일 전송 프로토콜](https://ko.wikipedia.org/wiki/분류:파일_전송_프로토콜 "wikilink")