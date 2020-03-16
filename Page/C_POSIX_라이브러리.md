> This article is converted from Wikipedia: [C POSIX ](https://ko.wikipedia.org/wiki/C_POSIX_).


**C POSIX 라이브러리**는 [C 표준 라이브러리](../Page/C_표준_라이브러리.md "wikilink") [POSIX](../Page/POSIX.md "wikilink")에 대한 시스템 사양이다. 이것은 [ANSI C의](../Page/ANSI_C.md "wikilink") 표준으로 동시에 개발되었다. POSIX는 추가적인 기능을 표준 C를 사용하는 사람들에게 소개를 했고, 이러한 노력으로 POSIX와 [표준 C를](https://ko.wikipedia.org/wiki/표준_C "wikilink") 호환되도록 만들 수 있었다.

## C POSIX 라이브러리 헤더 파일

| 헤더 파일                                                                            | 설명                                                                                                                                                |
| -------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| *' \<cpio.h\>*'                                                                  | [특별한 숫자의](https://ko.wikipedia.org/wiki/파일_형식 "wikilink") [cpio](https://ko.wikipedia.org/wiki/cpio "wikilink") 아카이브 형식임.                         |
| *' \<dirent.h\>*'                                                                | [디렉터리](https://ko.wikipedia.org/wiki/디렉터리 "wikilink")의 개방과 목록 확인을 허용함.                                                                            |
| *' \<[fcntl.h](https://ko.wikipedia.org/wiki/fcntl.h "wikilink")\>*'             | 파일을 열고, [잠금](../Page/파일_잠금.md "wikilink") 및 다른 작업을 할 수 있음.                                                                                        |
| *' \<grp.h\>*'                                                                   | 사용자 [그룹](https://ko.wikipedia.org/wiki/그룹_식별자_\(유닉스\) "wikilink") 정보를 제어함.                                                                        |
| *' \<[pthread.h](https://ko.wikipedia.org/wiki/pthread.h "wikilink")\>*'         | [POSIX](../Page/POSIX.md "wikilink") 스레드를 생성하고 조작하기 위한 API를 정의함.                                                                                  |
| *' \<[pwd.h](https://ko.wikipedia.org/wiki/pwd.h "wikilink")\>*'                 | [패스워드](https://ko.wikipedia.org/wiki/패스워드_\(파일\) "wikilink") (사용자 정보)를 접근하고 제어할 수 있음.                                                             |
| *' \<[sys/ipc.h](https://ko.wikipedia.org/wiki/sys/ipc.h "wikilink")\>*'         | [프로세스 간 통신](../Page/프로세스_간_통신.md "wikilink") IPC.                                                                                                 |
| *' \<[sys/msg.h](https://ko.wikipedia.org/wiki/sys/msg.h "wikilink")\>*'         | POSIX [메시지 큐](https://ko.wikipedia.org/wiki/메시지_큐 "wikilink").                                                                                    |
| *' \<[sys/sem.h](https://ko.wikipedia.org/wiki/sys/sem.h "wikilink")\>*'         | POSIX [세마포어](https://ko.wikipedia.org/wiki/세마포어_\(프로그래밍\) "wikilink").                                                                            |
| *' \<[sys/stat.h](https://ko.wikipedia.org/wiki/sys/stat.h "wikilink")\>*'       | 파일 정보 ([통계분석](https://ko.wikipedia.org/wiki/통계분석_\(유닉스\) "wikilink")) 등.                                                                          |
| *' \<sys/time.h\>*'                                                              | 시간과 날짜 기능과 구조.                                                                                                                                    |
| *' \<[sys/types.h](https://ko.wikipedia.org/wiki/sys/types.h "wikilink")\>*'     | 어떤 곳에서든지 사용되는 다양한 데이터 유형.                                                                                                                         |
| *' \<[sys/utsname.h](https://ko.wikipedia.org/wiki/sys/utsname.h "wikilink")\>*' | [uname](https://ko.wikipedia.org/wiki/uname "wikilink") 에 관련된 구조들.                                                                                |
| *' \<[sys/wait.h](https://ko.wikipedia.org/wiki/sys/wait.h "wikilink")\>*'       | 종료된 자식 프로세스의 상태 ([대기](https://ko.wikipedia.org/wiki/대기_\(운영_체제\) "wikilink") 참조).                                                                 |
| *' \<[tar.h](https://ko.wikipedia.org/wiki/tar.h "wikilink")\>*'                 | [압축(tar)된](https://ko.wikipedia.org/wiki/tar_\(파일_포맷\) "wikilink") 아카이브 형식의 [특별한 숫자](https://ko.wikipedia.org/wiki/파일형식#Magic_number "wikilink"). |
| *' \<[termios.h](https://ko.wikipedia.org/wiki/termios.h "wikilink")\>*'         | [터미널 입출력(I/O)](../Page/직렬_포트.md "wikilink") 인트페이스를 허용함.                                                                                           |
| *' \<[unistd.h](https://ko.wikipedia.org/wiki/unistd.h "wikilink")\>*'           | 다양한 필수 POSIX 함수와 상수.                                                                                                                              |
| *' \<[utime.h](https://ko.wikipedia.org/wiki/utime.h "wikilink")\>*'             | [아이노드](../Page/아이노드.md "wikilink")(inode) 접근과 수정시간.                                                                                               |

## 참조

  - [Official List of headers in the POSIX library on opengroup.org](http://www.opengroup.org/onlinepubs/9699919799/idx/head.html)
  - [Lists headers in the POSIX library](http://web.archive.org/web/*/http://www.space.unibe.ch/comp_doc/c_manual/C/FUNCTIONS/funcref.htm)
  - [Description of the posix library from the Flux OSKit](http://www.cs.utah.edu/flux/oskit/html/oskit-wwwch20.html)

## 더 읽어보기

  -
[C_POSIX_라이브러리](https://ko.wikipedia.org/wiki/분류:C_POSIX_라이브러리 "wikilink") [분류:POSIX](https://ko.wikipedia.org/wiki/분류:POSIX "wikilink")