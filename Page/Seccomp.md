> This article is converted from Wikipedia: [Seccomp](https://ko.wikipedia.org/wiki/Seccomp).


**seccomp** (**secure computing mode**의 약자)는 [리눅스 커널에서](https://ko.wikipedia.org/wiki/리눅스_커널 "wikilink") 애플리케이션 [샌드박싱](https://ko.wikipedia.org/wiki/샌드박스_\(컴퓨터_보안\) "wikilink") 메커니즘을 제공하는 [컴퓨터 보안](https://ko.wikipedia.org/wiki/컴퓨터_보안 "wikilink") 기능이다; 이것은 리눅스 커널 2.6.12부터 통합되었다(2005년 5월 8일에 배포되었다).\[1\] seccomp은 프로세스가 `exit()`, `sigreturn()`, 그리고 이미 열린 [파일 디스크립터에](https://ko.wikipedia.org/wiki/파일_서술자 "wikilink") 대한 `read(),`  `write()` 를 제외한 어떠한 [시스템 호출도](https://ko.wikipedia.org/wiki/시스템_호출 "wikilink") 일으킬 수 없는 안전한 상태로 일방향 변환을 할 수 있게 한다. 만약 다른 시스템 호출을 시도한다면, 커널이 [SIGKILL로](../Page/유닉스_신호.md "wikilink") 프로세스를 종료시킨다. 이러한 의미에서 이것은 시스템의 자원을 가상화하는 것이 아니라 프로세스를 고립시키는 것이라고 할 수 있다.

seccomp 모드는 `PR_SET_SECCOMP` 인자를 사용하는 시스템 호출 또는 리눅스 커널 3.17\[2\] 이후로는 시스템 호출을 통해 활성화 된다.\[3\] 전에는 seccomp 모드가 파일 `/proc/self/seccomp` 에 씀으로써 활성화되었지만 이 메소드는 prctl()을 위해 제거되었다.\[4\] 몇몇 커널 버전에서 seccomp은 RDTSC [x86](https://ko.wikipedia.org/wiki/x86 "wikilink") 명령어를 비활성화시킨다.\[5\]

**seccomp-bpf**는 seccomp의 확장이며\[6\] 설정 정책을 통한 시스템 호출 필터링을 허용한다. 이것은 [오픈SSH](https://ko.wikipedia.org/wiki/오픈SSH "wikilink")와 vsftpd 그리고 [크롬 OS와](https://ko.wikipedia.org/wiki/크롬_OS "wikilink") [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink")의 [구글 크롬](https://ko.wikipedia.org/wiki/구글_크롬 "wikilink") 웹 브라우저에서 사용된다.\[7\]

## 각주

## 외부 링크

  -
  - [Google's Chromium sandbox](http://lwn.net/Articles/347547/), [LWN.net](../Page/LWN.net.md "wikilink"), August 2009, by Jake Edge

  - [seccomp-nurse](https://web.archive.org/web/20110106145629/http://chdir.org/~nico/seccomp-nurse/), a sandboxing framework based on seccomp

  - [Documentation/prctl/seccomp_filter.txt](https://www.kernel.org/doc/Documentation/prctl/seccomp_filter.txt), part of the [Linux kernel](https://ko.wikipedia.org/wiki/리눅스_커널 "wikilink") documentation

  - [Security In-Depth for Linux Software: Preventing and Mitigating Security Bugs](https://www.cr0.org/paper/jt-ce-sid_linux.pdf)

[분류:컴퓨터 보안](https://ko.wikipedia.org/wiki/분류:컴퓨터_보안 "wikilink") [분류:리눅스 커널 특징](https://ko.wikipedia.org/wiki/분류:리눅스_커널_특징 "wikilink")

1.
2.
3.
4.
5.
6.
7.