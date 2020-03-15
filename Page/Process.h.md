> This article is converted from Wikipedia: [Process.h](https://ko.wikipedia.org/wiki/Process.h).


**process.h**는 스레드와 프로세스 작업에 쓰이는 함수 정의와 매크로가 포함된 C 언어의 [헤더 파일이다](../Page/헤더_파일.md "wikilink"). [ANSI/ISO C나](../Page/ANSI_C.md "wikilink") [POSIX](https://ko.wikipedia.org/wiki/POSIX "wikilink") 표준에서는 헤더 파일 또는 함수가 구현되어 있지 않다. 수많은 C 컴파일러는 [도스](https://ko.wikipedia.org/wiki/도스 "wikilink"), [윈도 3.1x](https://ko.wikipedia.org/wiki/윈도_3.1x "wikilink"), [Win32](https://ko.wikipedia.org/wiki/윈도_API "wikilink"), [OS/2](https://ko.wikipedia.org/wiki/OS/2 "wikilink"), [넷웨어](../Page/넷웨어.md "wikilink"), [도스 익스텐더에](https://ko.wikipedia.org/wiki/도스_익스텐더 "wikilink") 적용할 자신의 라이브러리의 헤더 파일과 라이브러리 함수에 타겟이 맞춰져 있다.

## 역사

첫 파일 참조는 1986년 10월 26일에 돌아간 Net.Micro.PC 유즈넷의 포스트에 있다.\[1\] 컴파일러는 마이크로소프트 C 컴파일러 3.0 버전에 사용되었다. Lattice C 컴파일러 3.30 (1988년 8월 24일)은 헤더 파일을 갖지 않고, 유사한 함수가 제공된다. 볼랜드에서는 헤더 파일이 [터보 C](https://ko.wikipedia.org/wiki/터보_C "wikilink") 컴파일러 2.01 버전에서 제공된다. C 웨어-퍼스널 C 컴파일러 1.2c 버전 (6월 1989)는 ANSI 헤더 파일만을 갖는다.

## 멤버 함수

| 이름                                                                                                               | 내용                                                                                                                           | 적용 운영 체제           |
| ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | ------------------ |
| [`execl,``   ``execle,``   ``execlp,``   ``execlpe`](https://ko.wikipedia.org/wiki/exec_\(운영_체제\) "wikilink")    | 부모 프로세스가 이전에 할당받은 메모리에 위치한 자식 프로세스를 로드하고 [실행한다](https://ko.wikipedia.org/wiki/실행_\(컴퓨팅\) "wikilink"). 개별적으로 매개변수를 들어간다.      | DOS,Win,OS/2,POSIX |
| [`execv,``   ``execve,``   ``execvp,``   ``execvpe`](https://ko.wikipedia.org/wiki/exec_\(운영_체제\) "wikilink")    | 부모 프로세스가 이전에 할당받은 메모리에 위치한 새 자식 프로세스를 로드하고 [실행한다](https://ko.wikipedia.org/wiki/실행_\(컴퓨팅\) "wikilink"). 매개변수는 포인터의 배열로 들어간다. | DOS,Win,OS/2,POSIX |
| [`spawnl,``   ``spawnle,``   ``spawnlp,``   ``spawnlpe`](https://ko.wikipedia.org/wiki/spawn_\(컴퓨팅\) "wikilink") | 자식 프로세스를 로드하고 실행한다. 개별적으로 매개변수를 들어간다.                                                                                        | DOS,Win,OS/2       |
| [`spawnv,``   ``spawnve,``   ``spawnvp,``   ``spawnvpe`](https://ko.wikipedia.org/wiki/spawn_\(컴퓨팅\) "wikilink") | 새 자식 프로세스를 로드하고 실행한다. 매개변수는 포인터의 배열로 들어간다.                                                                                   | DOS,Win,OS/2       |
| [`beginthread``   ``beginthreadNT`](https://ko.wikipedia.org/wiki/beginthread "wikilink"),                       | 현재 프로세스 동안 실행에 관한 새 스레드를 만든다.                                                                                                | Win,OS/2           |
| [`endthread`](https://ko.wikipedia.org/wiki/endthread "wikilink")                                                | `beginthread`로 만들어진 프로세스를 종료한다.                                                                                              | Win,OS/2           |
| [`getpid`](https://ko.wikipedia.org/wiki/getpid "wikilink")                                                      | [프로세스 식별자를](../Page/프로세스_식별자.md "wikilink") 반환한다.                                                                            | DOS,Win,OS/2       |
| [`cexit`](https://ko.wikipedia.org/wiki/cexit "wikilink")                                                        | 시작 코드에 의해 변경된 인터럽트 벡터를 원래대로 되돌린다.                                                                                            | DOS,Win,OS/2       |
|                                                                                                                  |                                                                                                                              |                    |

## 멤버 상수

| 이름                      | 내용                                             | 비고                                       | 운영 체제             |
| ----------------------- | ---------------------------------------------- | ---------------------------------------- | ----------------- |
| `_P_WAIT`               | 자식 프로세스가 실행이 끝날 때까지 부모 프로세스를 차단한다.             | 동기 스폰.                                   | MS-DOS,Win32,OS/2 |
| `_P_NOWAIT, _P_NOWAITO` | 동시에 호출된 프로세스를 새 프로세스에 실행 하는 것을 계속한다.           | 비동기 스폰                                   | Win32,OS/2        |
| `_P_OVERLAY`            | 부모 프로세스가 자식 프로세스에 덮어쓰기 할 경우, 부모 프로세스를 강제 종료한다. | `exec*` 함수와 같은 효과를 가진다.                  | MS-DOS,Win32,OS/2 |
| `_P_DETACH`             | 콘솔이나 키보드로 액세스하지 않고 자식이 백그라운드에서 실행된다.           | 새 프로세스가 실패하는 동시에 `_cwait`를 호출한다. 비동기 스폰. | Win32,OS/2        |
| `_WAIT_CHILD`           | `cwait` 동작에 사용된다.                              | Win32에는 쓰이지 않는다.                         | MS-DOS,OS/2       |
| `_WAIT_GRANDCHILD`      | `cwait` 동작에 사용된다.                              | Win32에는 쓰이지 않는다.                         | MS-DOS,OS/2       |
|                         |                                                |                                          |                   |

## 구현

어떤 표준도 없이 구현된 것을 감안하여 각 컴파일러의 헤더 파일에 따라 사용해야 한다. 아래는 process.h을 지원하는 컴파일러 목록이다.

  - DJGPP\[2\]\[3\]
  - 오픈왓컴(OpenWatCom)\[4\]\[5\]
  - 디지털 마르스\[6\]\[7\]
  - MinGW\[8\]
  - [마이크로소프트 비주얼 C++](https://ko.wikipedia.org/wiki/비주얼_C++ "wikilink")\[9\]
  - [볼랜드 터보 C](https://ko.wikipedia.org/wiki/터보_C "wikilink"), 2.0 이후 버전\[10\]\[11\]
  - Lcc32\[12\]
  - QNX Neutrino QCC 6.x\[13\]

## 차이점

한편 exec\*와 spawn\* 매개변수의 혼합 길이가 변경될 수도 있다.

  - Delorie DJGPP : 제한을 가지지 않는다.\[14\]
  - 디지털 마르스 : 최댓값이 128바이트이며 '\\0' 문자로 끝내야 될 필요는 없다.
  - 마이크로소프트 비주얼 C++ : 새 프로세스의 매개변수는 반드시 1024 바이트를 넘지 않아야 된다.\[15\]

## 참조

<references />

## 외부 링크

  - [Digital Mars _exec reference](http://www.digitalmars.com/rtl/process.html#_exec)

[분류:C 라이브러리](https://ko.wikipedia.org/wiki/분류:C_라이브러리 "wikilink")

1.  [First reference to process.h](http://groups-beta.google.com/group/net.micro.pc/browse_frm/thread/b85ef1946a4915e6/1154bb52be4d5854?lnk=st&q=%22process%5C.h%22&rnum=23#1154bb52be4d5854), groups-beta.google.com
2.  [Delorie.com](http://www.delorie.com/djgpp/)
3.  [DJGPP process.h](http://www.delorie.com/djgpp/doc/incs/process.h), delorie.com
4.
5.  [OpenWatcom clib](http://www.openwatcom.org/ftp/manuals/clib.pdf) , openwatcom.org
6.  [DigitalMars.com](http://www.digitalmars.com/)
7.  [Digital Mars process.h](http://www.digitalmars.com/rtl/process.html), digitalmars.com
8.  [MinGW.org](http://www.mingw.org/)
9.
10.
11. [C version 2.01](http://dn.codegear.com/article/20841Turbo), dn.codegear.com
12. [CS.Virginia.edu](http://www.cs.virginia.edu/~lcc-win32/)
13. [QNX.com](http://www.qnx.com/products/neutrino_rtos/)
14. [DJGPP spawn\*](http://www.delorie.com/djgpp/doc/libc/libc_736.html), delorie.com
15. [Microsoft MSDN](http://msdn.microsoft.com/library/default.asp?url=/library/en-us/vccore98/HTML/_crt_system.2c_._wsystem.asp), msdn.microsoft.com