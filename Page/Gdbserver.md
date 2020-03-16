> This article is converted from Wikipedia: [Gdbserver](https://ko.wikipedia.org/wiki/Gdbserver).


**gdbserver**는 다른 프로그램들을 원격으로 [디버깅](https://ko.wikipedia.org/wiki/디버깅 "wikilink")할 수 있게 해주는 컴퓨터 프로그램이다.\[1\] 이것은 디버깅되는 프로그램과 같은 시스템에서 동작하며, [GNU 디버거를](../Page/GNU_디버거.md "wikilink") 다른 시스템에서 연결할 수 있게 한다; 즉 소스 코드와 바이너리 파일의 복사본 등은 개발자의 로컬 컴퓨터(호스트)에 두고, 대상 시스템에는 단지 디버그되는 실행 파일만 둘 수 있다. 이 연결은 [TCP](https://ko.wikipedia.org/wiki/TCP "wikilink") 또는 시리얼 라인을 통해 가능해 진다.

## 동작 원리

1.  `gdbserver`는 다음의 인자들과 함께 대상 시스템에서 시작된다:
      - 디바이스 이름(시리얼 라인을 사용할 때) 또는 TCP 호스트 이름과 포트 이름, 그리고
      - 디버깅되는 실행 파일의 경로와 파일이름
    <!-- end list -->
      -
        이후 호스트 gdb가 통신할 때 까지 수동적으로 기다린다.
2.  `gdb`는 다음의 인자들과 함께 호스트에서 실행된다:
      - 호스트에서 실행 파일의 경로와 파일 이름
      - 디바이스 이름(시리얼 라인을 사용할 때) 또는 대상 시스템으로의 연결을 위해 필요한 IP 주소와 포트 번호.

원격 대상에 있는 `hello_world`로 불리는 프로그램을 TCP ("2159"는 [원격 GDB를 위해 등록된 TCP 포트 번호이다](https://ko.wikipedia.org/wiki/TCP/UDP의_포트_목록 "wikilink"))를 사용해 디버깅하는 예제:

``` console
remote@~$ gdbserver :2159 hello_world
Process hello_world created; pid = 2509
Listening on port 2159
```

``` console
local@~$ gdb -q hello_world
Reading symbols from /home/user/hello_world...done.
(gdb) target remote 192.168.0.11:2159
Remote debugging using 192.168.0.11:2159
0x002f3850 in ?? () from /lib/ld-linux.so.2
(gdb) continue
Continuing.

Program received signal SIGSEGV, Segmentation fault.
0x08048414 in main () at hello_world.c:10
10          printf("x[%d] = %g\n", i, x[i]);
(gdb)
```

## 대안

프로그램을 원격으로 디버깅하는 또 다른 기법은 *remote stub*을 사용하는 것이다.\[2\] 이 경우 디버깅되는 프로그램은 GDB 원격 시리얼 프로토콜을 구현하는 특별한 목적의 서브루틴들과 링크된다. 이러한 서브루틴들을 포함하는 파일은 "디버깅 스텁"이라고 불린다.

## 같이 보기

  - [GNU 디버거](../Page/GNU_디버거.md "wikilink")
  - [KGDB](https://ko.wikipedia.org/wiki/KGDB "wikilink")

## 노트

## 각주

  - Andreas Zeller: <cite>Why Programs Fail: A Guide to Systematic Debugging</cite>, Morgan Kaufmann, 2005.

## 외부 링크

  - [GDB 홈페이지](https://www.gnu.org/software/gdb/)
  - [GDB로 디버깅하기](http://davis.lbl.gov/Manuals/GDB/gdb_17.html)

[분류:디버거](https://ko.wikipedia.org/wiki/분류:디버거 "wikilink") [분류:디버깅](https://ko.wikipedia.org/wiki/분류:디버깅 "wikilink") [분류:GNU 프로젝트 소프트웨어](https://ko.wikipedia.org/wiki/분류:GNU_프로젝트_소프트웨어 "wikilink") [분류:유닉스 프로그래밍 도구](https://ko.wikipedia.org/wiki/분류:유닉스_프로그래밍_도구 "wikilink")

1.  [GDB Manual](http://ftp.gnu.org/old-gnu/Manuals/gdb-5.1.1/html_node/gdb_130.html)
2.  [Debugging with GDB](http://davis.lbl.gov/Manuals/GDB/gdb_17.html#SEC140)