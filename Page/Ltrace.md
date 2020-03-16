> This article is converted from Wikipedia: [Ltrace](https://ko.wikipedia.org/wiki/Ltrace).


**ltrace**는 [사용자 공간](../Page/사용자_공간.md "wikilink") 애플리케이션의 [공유 라이브러리에](https://ko.wikipedia.org/wiki/공유_라이브러리 "wikilink") 대한 호출을 보여주는데 사용되는 [리눅스](../Page/리눅스.md "wikilink")의 [디버깅](https://ko.wikipedia.org/wiki/디버깅 "wikilink") 유틸리티이다. 이것은 [동적 로딩](https://ko.wikipedia.org/wiki/동적_로딩 "wikilink") 시스템을 후킹함으로써 가능해지며, 애플리케이션이 호출 시에 사용하는 [파라미터](https://ko.wikipedia.org/wiki/파라미터 "wikilink")들과 라이브러리 호출이 리포트하는 반환 값을 보여주는 [심](https://ko.wikipedia.org/wiki/심_\(컴퓨팅\) "wikilink")(shim)들을 삽입한다. ltrace는 또한 리눅스 [시스템 호출을](../Page/시스템_호출.md "wikilink") 트레이스할 수 있다. 이것이 동적 라이브러리 후킹 메커니즘을 사용하기 때문에, ltrace는 대상 바이너리에 직접적으로 [정적 링크된](../Page/정적_라이브러리.md "wikilink") 호출들을 트레이스할 수 없다.

## 출력 예시

다음은 xterm 호출의 처음 몇 라인들이다. 이것은 ltrace가 보여주는 다양한 라이브러리들([C 표준 라이브러리](../Page/C_표준_라이브러리.md "wikilink")(malloc, strlen), POSIX 라이브러리(getuid) 등)에 대한 호출들을 보여준다. 호출의 반환 값은 = 기호 뒤에 나오는 값이다.

``` c
[pid 11783] __libc_start_main(0x407420, 1, 0x7fff75b6aad8, 0x443cc0, 0x443d50 <unfinished ...>
[pid 11783] geteuid()                            = 1000
[pid 11783] getegid()                            = 1000
[pid 11783] getuid()                             = 1000
[pid 11783] getgid()                             = 1000
[pid 11783] setuid(1000)                         = 0
[pid 11783] malloc(91)                           = 0x00cf8010
[pid 11783] XtSetLanguageProc(0, 0, 0, 0x7f968c9a3740, 1) = 0x7f968bc16220
[pid 11783] ioctl(0, 21505, 0x7fff75b6a960)      = 0
[pid 11783] XtSetErrorHandler(0x42bbb0, 0x44f99c, 0x669f80, 146, 0x7fff75b6a72c) = 0
[pid 11783] XtOpenApplication(0x670260, 0x44f99c, 0x669f80, 146, 0x7fff75b6a72c) = 0xd219a0
[pid 11783] IceAddConnectionWatch(0x42adc0, 0, 0, 0x7f968c9a3748, 0 <unfinished ...>
[pid 11783] IceConnectionNumber(0xd17ec0, 0, 1, 0xcfb138, 0xd17c00) = 4
[pid 11783] <... IceAddConnectionWatch resumed> ) = 1
[pid 11783] XtSetErrorHandler(0, 0, 1, 0xcfb138, 0xd17c00) = 0
[pid 11783] XtGetApplicationResources(0xd219a0, 0x6701c0, 0x66b220, 34, 0) = 0
[pid 11783] strlen("off")                        = 3
```

## 같이 보기

  - [strace](https://ko.wikipedia.org/wiki/strace "wikilink") - 리눅스의 시스템 호출 트레이서
  - [ktrace](https://ko.wikipedia.org/wiki/ktrace "wikilink") - \*BSD의 시스템 호출 트레이서
  - [truss](https://ko.wikipedia.org/wiki/truss "wikilink") - 고전적인 시스템 호출 트레이서
  - [dtrace](https://ko.wikipedia.org/wiki/dtrace "wikilink") - 솔라리스 / OS X / BSD 커널 트레이싱 툴.
  - [SystemTap](https://ko.wikipedia.org/wiki/SystemTap "wikilink") - 리눅스 커널 트레이싱 툴.

## 외부 링크

  - [홈 페이지](http://www.ltrace.org/)
  - [ltrace man 페이지](http://linux.die.net/man/1/ltrace)
  - Rodrigo Rubira Branco, [*Ltrace Internals*](http://www.kernel.org/doc/ols/2007/ols2007v1-pages-41-52.pdf), [Ottawa Linux Symposium](https://web.archive.org/web/20080913185728/http://www.linuxsymposium.org/) 2007
  - [latrace](http://latrace.sourceforge.net/latrace.html), LD_AUDIT libc 특징을 사용하여 동작하는 동적 라이브러리 호출 트레이서

[분류:유닉스 프로그래밍 도구](https://ko.wikipedia.org/wiki/분류:유닉스_프로그래밍_도구 "wikilink")