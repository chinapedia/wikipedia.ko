> This article is converted from Wikipedia: [DTrace](https://ko.wikipedia.org/wiki/DTrace).


**DTrace**는 운영 시스템의 [커널과](../Page/커널_\(컴퓨팅\).md "wikilink") 응용 프로그램 문제를 실시간으로 [해결하기](https://ko.wikipedia.org/wiki/트러블슈팅 "wikilink") 위해 [썬 마이크로시스템즈가](../Page/썬_마이크로시스템즈.md "wikilink") 개발한 동적 [트레이싱](../Page/트레이싱.md "wikilink") 프레임워크이다. 원래 [솔라리스용으로](../Page/솔라리스_\(운영_체제\).md "wikilink") 개발되었다가, 그 이후로 자유 [공동 개발 및 배포 허가서](../Page/공동_개발_및_배포_허가서.md "wikilink")(CDDL)로 출시되면서 다른 여러 [유닉스 계열](../Page/유닉스_계열.md "wikilink") 운영 체제로 이식되었다.

DTrace는 메모리의 양, CPU 시간, 또 실행 중인 프로세스들이 사용하는 파일 시스템 및 네트워크 자원 등, 실행 중인 시스템의 전반적인 개요를 가져오는데 사용할 수 있다. 특정 함수가 호출된 인수의 로그라든지 특정 파일에 접근하는 프로세스의 목록과 같은 훨씬 더 자세한 정보를 제공할 수 있다.

2011년 10월 기준으로, 오라클은 DTrace를 [리눅스](../Page/리눅스.md "wikilink")로 [이식하는](../Page/이식_\(컴퓨팅\).md "wikilink") 것을 발표하였으나 2014년 10월 13일 기준으로 공식적으로 이용이 불가능한 상황이다.\[1\] DTrace의 비공식 리눅스 포트는 이용할 수 있으나, 라이선스 조항에 대한 변경사항은 없다 .\[2\]

## 명령 줄 예

하나 이상의 프로브(probe)와 액션(action)을 인수로 지정하여 DTrace 스크립트를 명령 줄에서 직접 호출할 수 있다. 일부 예는 다음과 같다:

``` bash
# New processes with arguments
dtrace -n 'proc:::exec-success { trace(curpsinfo->pr_psargs); }'

# Files opened by process
dtrace -n 'syscall::open*:entry { printf("%s %s",execname,copyinstr(arg0)); }'

# Syscall count by program
dtrace -n 'syscall:::entry { @num[execname] = count(); }'

# Syscall count by syscall
dtrace -n 'syscall:::entry { @num[probefunc] = count(); }'

# Syscall count by process
dtrace -n 'syscall:::entry { @num[pid,execname] = count(); }'

# Disk size by process
dtrace -n 'io:::start { printf("%d %s %d",pid,execname,args[0]->b_bcount); }'

# Pages paged in by process
dtrace -n 'vminfo:::pgpgin { @pg[execname] = sum(arg0); }'
```

수백 줄의 길이로 스크립트의 작성이 가능하지만 일반적으로 고급 문제 해결 및 분석에는 수십 줄이 필요하다. 200개 이상의 오픈 소스 DTrace 스크립트의 예제를 DTraceToolkit에서 볼 수 있으며,\[3\] 이는 DTrace 책의 저자 Brendan Gregg가 만든 것으로\[4\]), 문서와 각각의 증명 결과도 제공한다.

## 같이 보기

  - [ftrace](https://ko.wikipedia.org/wiki/ftrace "wikilink")
  - [ktrace](https://ko.wikipedia.org/wiki/ktrace "wikilink")
  - [Ltrace](../Page/Ltrace.md "wikilink")
  - [Strace](../Page/Strace.md "wikilink")
  - [SystemTap](https://ko.wikipedia.org/wiki/SystemTap "wikilink")
  - [Sysdig](https://ko.wikipedia.org/wiki/Sysdig "wikilink")
  - [LTTng](https://ko.wikipedia.org/wiki/LTTng "wikilink")
  - IBM [ProbeVue](https://ko.wikipedia.org/wiki/ProbeVue "wikilink")

## 각주

  -
  -
### 내용주

## 외부 링크

  - [DTrace Tools](http://www.brendangregg.com/dtrace.html) Brendan Gregg's DTrace examples (2004)
  - [FreeBSD DTrace page](https://wiki.freebsd.org/DTrace) FreeBSD DTrace homepage, includes a tutorial and one-liners
  - [DTrace book](http://www.dtracebook.com/index.php/Main_Page) includes hundreds of example scripts
  - [Dynamic Tracing with DTrace & SystemTap](http://myaut.github.io/dtrace-stap-book) free book with examples and exercises
  - [DTrace book scripts](https://github.com/brendangregg/DTrace-book-scripts) DTrace book scripts on GitHub
  - [DTraceToolkit](http://www.brendangregg.com/dtracetoolkit.html) a collection of DTrace scripts
  - [DTrace Hands On Lab](http://dtracehol.com/) a step-by-step course to learn DTrace
  - [DLight Tutorial](http://developers.sun.com/sunstudio/documentation/tutorials/dlight/) an interactive GUI utility for C/C++ developers based on DTrace technology from the [Oracle Solaris Studio](https://ko.wikipedia.org/wiki/:en:Sun_Studio_\(software\) "wikilink")
  - [Exploring Leopard with DTrace](https://web.archive.org/web/20170903114855/http://www.mactech.com/articles/mactech/Vol.23/23.11/ExploringLeopardwithDTrace/index.html) DTrace for debugging and exploration
  - [Tech Talk on DTrace given by Bryan Cantrill](https://www.youtube.com/watch?v=TgmA48fILq8%7CGoogle)
  - [Hidden in Plain Sight](http://queue.acm.org/detail.cfm?id=1117401), Sun Microsystems, by Bryan Cantrill

[분류:자유 시스템 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_시스템_소프트웨어 "wikilink") [분류:디버거](https://ko.wikipedia.org/wiki/분류:디버거 "wikilink") [분류:관점 지향 프로그래밍](https://ko.wikipedia.org/wiki/분류:관점_지향_프로그래밍 "wikilink") [분류:리눅스 커널 특징](https://ko.wikipedia.org/wiki/분류:리눅스_커널_특징 "wikilink") [분류:썬 마이크로시스템즈 소프트웨어](https://ko.wikipedia.org/wiki/분류:썬_마이크로시스템즈_소프트웨어 "wikilink")

1.  <http://www.slideshare.net/brendangregg/from-dtrace-to-linux> Published on Oct 13, 2014 (slide 28)
2.  <https://github.com/dtrace4linux/linux>
3.
4.