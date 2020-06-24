> This article is converted from Wikipedia: [FreeBSD](https://ko.wikipedia.org/wiki/FreeBSD).


**FreeBSD**는 [BSD](../Page/BSD.md "wikilink") 계열의 [오픈 소스](../Page/오픈_소스.md "wikilink") [운영 체제로서](../Page/운영_체제.md "wikilink"), [캘리포니아 대학교 버클리](../Page/캘리포니아_대학교_버클리.md "wikilink")(UC Berkeley) CSRG(Computer Systems Research Group)의 4.4BSD 라이트를 바탕으로 개발되었다. 2016년 4월 기준 FreeBSD 10.3을 배포하고 있으며, 기본적으로는 [x86](https://ko.wikipedia.org/wiki/x86 "wikilink") 및 [x86-64](https://ko.wikipedia.org/wiki/x86-64 "wikilink") 기종을 중심으로 개발되고, 다른 주요 기종에도 이식되고 있다.

## 개요

FreeBSD는 BSD 유닉스로 알려진 [캘리포니아 대학교 버클리](../Page/캘리포니아_대학교_버클리.md "wikilink") CSRG(Computer Systems Research Group)의 4.4BSD-Lite를 이어받아 개발된 [오픈 소스](../Page/오픈_소스.md "wikilink") [운영 체제이다](../Page/운영_체제.md "wikilink"). [리눅스](../Page/리눅스.md "wikilink")와 달리 전통적인 [유닉스](../Page/유닉스.md "wikilink") 방식에 따라 온전한 운영 체제의 개발을 목표로 하여, [커널을](../Page/커널_\(컴퓨팅\).md "wikilink") 비롯한 기본적인 [운영 체제](../Page/운영_체제.md "wikilink") 구성 요소는 하나의 [CVS](../Page/CVS.md "wikilink") 트리로 관리되어 통합적으로 개발되며 그밖에 외부 개발 요소를 포함하여 단일한 배포본으로 구성된다.

기본적으로 32비트 [x86](https://ko.wikipedia.org/wiki/x86 "wikilink") 프로세서(IA-32) 기반 i386 플랫폼을 중심으로 개발되고 있으며 현재 64비트 확장판 [AMD64](https://ko.wikipedia.org/wiki/AMD64 "wikilink")(x86-64)을 비롯하여 [NEC PC-98](https://ko.wikipedia.org/wiki/NEC_PC-98 "wikilink"), 64비트 프로세서 [인텔](../Page/인텔.md "wikilink") [아이테니엄](../Page/아이테니엄.md "wikilink")(IA-64), [SPARC](../Page/SPARC.md "wikilink"), [파워PC](../Page/파워PC.md "wikilink"), [DEC 알파](../Page/DEC_알파.md "wikilink") [아키텍처](https://ko.wikipedia.org/wiki/아키텍처 "wikilink")를 지원하며(단, FreeBSD 7부터 [DEC Alpha](../Page/DEC_알파.md "wikilink") 프로세서 제외), 아울러 [ARM](../Page/ARM_아키텍처.md "wikilink"), [MIPS](https://ko.wikipedia.org/wiki/MIPS_아키텍처 "wikilink") 프로세서와 [MS](../Page/마이크로소프트.md "wikilink") [Xbox](https://ko.wikipedia.org/wiki/Xbox "wikilink") 기종에 대한 개발이 진행되고 있다.

FreeBSD 자체는 상용화되지는 않았으나, 안정적이고 튼튼한 운영 체제로 인정받으며 Walnut Creek CDROM(cdrom.com), [야후\!](../Page/야후!.md "wikilink"), [핫메일](../Page/핫메일.md "wikilink")(Hotmail)\[1\]\[2\] 등의 대형 인터넷 서비스에 사용되어 왔으며, 대한민국에서도 포털사이트 [드림위즈](https://ko.wikipedia.org/wiki/드림위즈 "wikilink")(www.dreamwiz.com), [세이클럽](https://ko.wikipedia.org/wiki/세이클럽 "wikilink")(www.sayclub.com) 등에 채용되었다.\[3\] 또한, 상용 제품인 [애플](https://ko.wikipedia.org/wiki/애플_\(기업\) "wikilink") Mac OS X의 코어 Darwin의 토대\[4\]이며, 마이크로소프트의 C\# 및 CLI 소스공유(Shared Source Initiative) 대상이다.\[5\]\[6\]

## 역사

FreeBSD는 당시 약 20년의 개발 역사를 가진 BSD를 바탕으로 개발되었다. 이후 BSD의 원래 개발자들이 설립한 BSDi의 BSD/OS와도 교류하며 꾸준히 개발되어 왔으며, 현재 BSD 계열의 가장 대표적인 운영 체제이다.

### BSD 역사

처음 BSD 개발은 유닉스 제6판의 [추가 기능](https://ko.wikipedia.org/wiki/추가_기능 "wikilink")(add-on)이라는 개념으로 시작되었다. [1977년](../Page/1977년.md "wikilink") [캘리포니아 대학교 버클리의](../Page/캘리포니아_대학교_버클리.md "wikilink") 대학원생이었던 빌 조이(Bill Joy)는 미니컴퓨터 PDP-11에 설치된 유닉스에 사용할 파스칼(Pascal) [컴파일러](../Page/컴파일러.md "wikilink")와 라인에디터 Ex를 작성하고, 이것을 중심으로 패키지를 만들어 “Berkeley Software Distribution”이라는 이름으로 배포하였다. 그 이듬해 [1978년](../Page/1978년.md "wikilink")에는 vi 에디터와 [C 셸을](../Page/C_셸.md "wikilink") 작성하고 이것을 포함한 두 번째 배포본 “Second Berkeley Software Distribution”을 만들었는데, 이것이 2BSD라는 약칭으로 불렸다. 이후 개량이 지속되어 [1983년](../Page/1983년.md "wikilink")에는 유닉스 버전 7을 기반으로 한 온전한 운영 체제 배포본으로서 2.9BSD로 완성되었다.

한편, [1979년](../Page/1979년.md "wikilink") 말에는 새로 도입된 VAX 기종에서 3BSD가 탄생한다. 3BSD는 VAX용 유닉스인 UNIX/32V를 개량하여 가상메모리를 구현한 새로운 커널을 만들고 2BSD를 흡수하여 새로운 운영 체제로 만들어졌다. 이어 1980년에는 3BSD를 개량하여 4BSD가 만들어지고 그 성능을 개선한 4.1BSD가 1981년에 나왔으며, 1983년에는 TCP/IP 구현과 새로운 파일시스템 FFS를 포함한 4.2BSD가 개발되었다. 1986년에 발표된 4.3BSD는 기능 개선보다는 4.2BSD의 성능 향상이 주요 목표였는데, 4.3BSD 배포 후에 기존 VAX 시스템으로부터 Power 6/32로 이전하여 1988년 4.3BSD-Tahoe가 나오면서 코드를 시스템 의존적인 부분과 비의존적인 부분으로 나누는 한편, AT\&T의 원본 유닉스 코드와 완전히 결합된 형태가 되었다. 이에 따라, BSD의 사용에서도 AT\&T의 라이선스가 필요하게 되는데, AT\&T 코드와 분리된 배포 요구에 따라 [1989년](../Page/1989년.md "wikilink") AT\&T의 유닉스 코드를 제외한 “Networking Release 1 (Net/1)”이 만들어지고 자유롭게 재배포할 수 있는 BSD 라이선스를 적용하였다. 1990년 초에는 4.3BSD-Reno가 나오며 CMU 마크(Mach)의 가상메모리 시스템과 Sun의 NFS이 구현되었다.

마침내 [1991년](../Page/1991년.md "wikilink")에는 대부분의 AT\&T 코드를 BSD 코드로 대체한 “Networking Release 2 (Net/2)”가 나왔는데, 이것은 PC로 옮겨져 386BSD와 BSD/386의 기반이 되었다. 1992년에 발생한 저작권 및 상표권을 둘러싼 USL과 BSD의 법정 공방 끝에, [1994년](../Page/1994년.md "wikilink") 4.3BSD-Net/2는 AT\&T 라이선스가 필요한 4.4BSD-Encumbered와 완전히 자유로운 4.4BSD-Lite로 나뉘어 다시 배포되었다. [1995년](../Page/1995년.md "wikilink")에는 BSD의 최종판인 4.4BSD-Lite Release 2가 나오며, CSRG는 그동안의 모든 연구와 개발을 마무리하고 해산하였다. 이즈음 386BSD는 FreeBSD와 NetBSD로 이어졌고 BSD/386은 BSD/OS이 되어 4.4BSD를 계승한다.

### FreeBSD의 태동과 변천

FreeBSD의 개발은 [1993년](../Page/1993년.md "wikilink")부터 4.3BSD Net/2에 기반한 [386BSD](../Page/386BSD.md "wikilink")의 소스 코드를 이용하여 시작되었다. 처음은 [1992년](../Page/1992년.md "wikilink") Jordan K. Hubbard, Nate Williams, Rod Grimes 세 사람이 시작한 “Unofficial 386BSD Patchkit”로\[7\] 원래는 [386BSD](../Page/386BSD.md "wikilink")를 보완하는 개념이었으나 [386BSD](../Page/386BSD.md "wikilink")의 개발이 줄곧 늦어지고 작업 결과가 반영되지 않으면서,\[8\] 이 작업은 결국 별도의 BSD 운영 체제 개발로 전환되어 David Greenman의 명명에 따라 ‘FreeBSD’라는 이름으로 독자적인 작업이 되었고, [1993년 11월](https://ko.wikipedia.org/wiki/1993년_11월 "wikilink") FreeBSD 1.0이 발표되었다. Walnut Creek사의 후원으로 CD-ROM으로 배포된 최초의 FreeBSD는 4.3BSD를 바탕으로 386BSD의 작업과 GNU 결과물을 포함하여 구성되었는데, 곧이어 [1994년 5월에](https://ko.wikipedia.org/wiki/1994년_5월 "wikilink") 버전 1.1이 발표되었고 [1994년 7월](https://ko.wikipedia.org/wiki/1994년_7월 "wikilink") 버전 1.1.5.1로 완료된다. 그런데 이 무렵 4.3BSD Net/2를 둘러싸고 AT\&T Unix의 소유자였던 USL과 BSD Unix의 개발자 [캘리포니아 대학교 버클리](../Page/캘리포니아_대학교_버클리.md "wikilink") 사이에 발생한 저작권 분쟁의 여파로 4.3BSD Net/2에 기반한 기존의 [386BSD](../Page/386BSD.md "wikilink") 소스 코드는 사용을 중단해야 했고, 이에 따라 FreeBSD 2.0은 자유로운 배포를 보장받은 4.4BSD-Lite를 바탕으로 다시 작성되었다.\[9\]\[10\]

[1995년 1월에](https://ko.wikipedia.org/wiki/1995년_1월 "wikilink") 발표된 FreeBSD 2.0은 4.4BSD를 기반으로 전면 재작성되어 [1995년 6월](https://ko.wikipedia.org/wiki/1995년_6월 "wikilink") 버전 2.0.5을 거쳐 [1998년 11월](https://ko.wikipedia.org/wiki/1998년_11월 "wikilink") 버전 2.1.7.1과 버전 2.2.8로 완료되었다. 가장 큰 향상은 [CMU의](https://ko.wikipedia.org/wiki/카네기_멜론_대학교 "wikilink") [Mach](https://ko.wikipedia.org/wiki/Mach "wikilink") 가상 메모리 시스템을 개선하여 과부하 상태에서도 안정적인 성능을 유지하도록 최적화되었고, 포트(port) 시스템이 도입되어 서드파티 소프트웨어의 설치 및 관리의 편의를 제공한다.

FreeBSD 3.0은 [1998년 10월에](https://ko.wikipedia.org/wiki/1998년_10월 "wikilink") 발표되어 [2000년 7월](https://ko.wikipedia.org/wiki/2000년_7월 "wikilink") 버전 3.5.1로 마무리되었는데, [ELF 바이너리 포맷으로](https://ko.wikipedia.org/wiki/ELF_바이너리_포맷 "wikilink") 전환, [대칭형 다중 프로세서](https://ko.wikipedia.org/wiki/대칭형_다중_프로세서 "wikilink")(SMP) 시스템 지원, 새로운 64비트 플랫폼 [DEC Alpha](https://ko.wikipedia.org/wiki/DEC_Alpha "wikilink") 지원 등의 변화가 있었다. 비록 확실한 기능상의 이점도 성능 향상도 가져오지 못했다는 비판도 있었으나, [1995년 6월에](https://ko.wikipedia.org/wiki/1995년_6월 "wikilink") 완성된 BSD Unix의 최종 결과물 4.4BSD-Lite2까지 흡수\[11\]하며 이전의 여러 개발 성과들을 총괄하여, 향후 FreeBSD 4에서의 도약을 위한 토대가 되었다.

[2000년 3월에는](https://ko.wikipedia.org/wiki/2000년_3월 "wikilink") FreeBSD를 후원하던 Walnut Creek CDROM과 BSD/OS의 개발사 BSDi가 합병하였다.\[12\]\[13\] 이 결과, 원래 CSRG의 BSD 개발자들이었던 BSDi의 개발진이 FreeBSD에 합류하여 BSD/OS와 FreeBSD의 코드를 통합한 오픈 소스 FreeBSD 개발을 지속하고, BSD/OS는 이를 바탕으로 비공개 드라이버 등 상업용 구성 요소를 추가하고 상업적 기술 지원을 제공하는 상용 제품으로 추진하는 방안이 모색되었다.\[14\]\[15\]

### FreeBSD 4

FreeBSD 4.0은 2000년 3월에 발표되어 2005년 1월 최종판 4.11로 완료되었다. FreeBSD 4에서는 가상메모리 성능이 향상되고, SVR4 계열 유닉스에 대한 에뮬레이션이 추가되었으며, ATA/ATAPI 통합 드라이버가 도입되었다. 4.1판부터는 기존의 i386 배포본과 더불어 alpha 플랫폼 배포본이 공식 배포되었다.

  - 업데이트 연혁

<!-- end list -->

  - FreeBSD 4.0 2000-05-14
  - FreeBSD 4.1 2000-07-27
  - FreeBSD 4.1.1 2000-09-27
  - FreeBSD 4.2 2000-11-21
  - FreeBSD 4.3 2001-04-20
  - FreeBSD 4.4 2001-09-20
  - FreeBSD 4.5 2002-01-29
  - FreeBSD 4.6 2002-06-15
  - FreeBSD 4.6.2 2002-08-15
  - FreeBSD 4.7 2002-10-10
  - FreeBSD 4.8 2003-04-03
  - FreeBSD 4.9 2003-10-28
  - FreeBSD 4.10 2004-05-27
  - FreeBSD 4.11 2005-01-25

### FreeBSD 5

당초 FreeBSD 5와 관련해서 BSD/OS와 완전한 소스 코드 통합이 간혹 언급되기도 하였으나\[16\] 실제 실현되지는 않았다. 다만 일부 코드의 공유가 있었고, 특히 BSD/OS의 SMPng이 도입되었다.\[17\]\[18\] FreeBSD 5에서는 많은 구조적 변화와 함께 안정성과 성능이 크게 향상되고 새로운 기능이 추가되었으며,\[19\] 보다 많은 플랫폼에 이식되었다.

  - 업데이트 연혁

<!-- end list -->

  - FreeBSD 5.0 2003-01-17
  - FreeBSD 5.1 2003-06-09
  - FreeBSD 5.2 2004-01-12
  - FreeBSD 5.2.1 2004-02-22
  - FreeBSD 5.3 2004-11-06
  - FreeBSD 5.4 2005-05-09
  - FreeBSD 5.5 2006-05-25

### FreeBSD 6

FreeBSD 6은 2005년 6.0을 시작으로 2008년 1월 18일 6.3판까지 발표되었다. 이 시기에는 SMP와 스레드 최적화에 관한 작업이 진행되었고, 802.11의 추가적인 기능 개선, 보안 이벤트 감사(TrustedBSD 프로젝트에 의해 작성), 네트워크 스택 성능의 현저한 개선, 완전한 선점형 커널 그리고 하드웨어 성능 카운터(HWPMC)의 지원 등도 진행되었다. FreeBSD 6에서 일차적인 개선점으로는 가상파일시스템(Virtual File System)에서 Giant lock의 제거, 1:1 스레딩을 통한 libthr의 부가적인 성능 개선 그리고 OpenBSM이라고 불리는 기초 보안 모듈(BSM, Basic Security Module)의 구현이다. OpenBSM은 애플의 오픈 소스 [다윈의](../Page/다윈_\(운영_체제\).md "wikilink") 구현을 기반으로 하였으며 TrustedBSD 프로젝트에 의해 작성되어 BSD 라이선스로 배포되었다.

  - 업데이트 연혁

<!-- end list -->

  - FreeBSD 6.0 2005-11-01
  - FreeBSD 6.1 2006-05-08
  - FreeBSD 6.2 2007-01-15
  - FreeBSD 6.3 2008-01-18
  - FreeBSD 6.4 2008-11-28

### FreeBSD 7

FreeBSD 7은 2008년 2월 27일에 7.0이 발표되었으며 특징은 다음과 같다.\[20\]

  - SMP 성능 향상
  - ULE 스케줄러 개선 (7.1부터 기본 설정으로 전환 예정)
  - XFS 파일 시스템 지원 (읽기 전용)
  - ZFS 파일 시스템 지원 (실험적)
  - SCTP 지원 (실험적)
  - [UFS](../Page/유닉스_파일_시스템.md "wikilink")(FreeBSD의 파일 시스템)의 저널링
  - GCC 4.2.1, X.Org 7.3, KDE 3.5.8, GNOME 2.20.2. BIND 9.4.2.

<!-- end list -->

  - 업데이트 연혁

<!-- end list -->

  - FreeBSD 7.0 2008-02-27
  - FreeBSD 7.1 2009-01-05
  - FreeBSD 7.2 2009-05-04
  - FreeBSD 7.3 2010-03-23
  - FreeBSD 7.4 2011-02-24

### FreeBSD 8

  - 업데이트 연혁

<!-- end list -->

  - FreeBSD 8.0 2009-11-26
  - FreeBSD 8.1 2010-07-23
  - FreeBSD 8.2 2011-02-24

### FreeBSD 9

  - 업데이트 연혁

<!-- end list -->

  - FreeBSD 9.0 2012-01-12
  - FreeBSD 9.1 2012-12-30
  - FreeBSD 9.2 2013-09-26
  - FreeBSD 9.3 2014-07-08

### FreeBSD 10

  - 업데이트 연혁

<!-- end list -->

  - FreeBSD 10.0 2014-01-20
  - FreeBSD 10.1 2014-11-05
  - FreeBSD 10.2 2015-08-06
  - FreeBSD 10.3 2016-04-04

### FreeBSD 11

  - 업데이트 연혁

<!-- end list -->

  - FreeBSD 11.0 2016-10-10

### 안정판(stable)과 개발판(current)

FreeBSD는 실용을 위한 안정판(stable)과 함께 개발 과정을 반영한 개발판(current)를 병렬적으로 운용하고 있다. 안정판은 현재의 배포본을 바탕으로 업데이트가 진행되고 있는 것이며, 어느 정도 개선 작업이 축적되면 소규모 업그레이드가 적용된 새로운 배포본을 만든다. 개발판은 이와 별도로 보다 근본적인 설계 변경 등의 대규모 작업이 장기적으로 진행되고 있는 것으로 이 결과는 대규모 업그레이드가 된 차기판으로 나오게 된다.

## 특징

FreeBSD는 [UC 버클리](https://ko.wikipedia.org/wiki/UC_버클리 "wikilink") CSRG의 4.4BSD를 계승하여 개발되어 왔으며, BSD 전통에 따라 어떠한 제약 조건없이 누구든지 어느 목적으로도 사용할 수 있는 소프트웨어를 만드는 것을 목표로 한다. 기본적으로 널리 보급되어 있는 x86 PC 기종에서 동작하는 고성능 운영 체제를 추구하고 있으며, 수많은 자원 봉사자의 노력과 여러 공헌자의 협조로 개발되고 있다. FreeBSD는 다른 운영 체제와 직접 경쟁하거나 또는 대체하는 것을 목표로 하지 않으며,\[21\] 다만 가장 널리 사용되어 보다 많은 경우에 폭넓은 유용성을 제공하는 것을 추구한다.\[22\]

### 지원 플랫폼

FreeBSD는 기본적으로 PC 호환 기종을 중심으로 개발되어 왔으며, 아울러 다른 플랫폼으로 포팅도 진행되어 있다. 2015년 12월 현재까지 배포본의 공식 지원 플랫폼은 다음과 같다.

<table>
<thead>
<tr class="header">
<th><p>FreeBSD 11</p></th>
<th><p>FreeBSD 10</p></th>
<th><p>FreeBSD 9</p></th>
<th><p>FreeBSD 8</p></th>
<th><p>FreeBSD 7</p></th>
<th><p>FreeBSD 6</p></th>
<th><p>FreeBSD 5</p></th>
<th><p>FreeBSD 4</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>i386</li>
<li>amd64</li>
<li>ia64</li>
<li>sparc64</li>
<li>aarch64</li>
<li>powerpc</li>
<li>powerpc64</li>
</ul></td>
<td><ul>
<li>i386</li>
<li>amd64</li>
<li>ia64</li>
<li>sparc64</li>
<li>powerpc</li>
<li>powerpc64</li>
<li>armv6</li>
</ul></td>
<td><ul>
<li>i386</li>
<li>amd64</li>
<li>ia64</li>
<li>sparc64</li>
<li>powerpc</li>
<li>powerpc64</li>
</ul></td>
<td><ul>
<li>i386</li>
<li>pc98</li>
<li>amd64</li>
<li>ia64</li>
<li>sparc64</li>
<li>powerpc</li>
</ul></td>
<td><ul>
<li>i386</li>
<li>pc98</li>
<li>amd64</li>
<li>ia64</li>
<li>sparc64</li>
<li>powerpc</li>
</ul></td>
<td><ul>
<li>i386</li>
<li>pc98</li>
<li>amd64</li>
<li>ia64</li>
<li>sparc64</li>
<li>powerpc</li>
<li>alpha</li>
</ul></td>
<td><ul>
<li>i386</li>
<li>pc98</li>
<li>amd64</li>
<li>ia64</li>
<li>sparc64</li>
<li>alpha</li>
</ul></td>
<td><ul>
<li>i386</li>
<li>alpha</li>
</ul></td>
</tr>
</tbody>
</table>

#### i386 아키텍처

일반적인 32비트 PC 기종이며 FreeBSD의 주개발 목표였다. 본래 386 CPU를 지원했으나 버전 5.2에서 16비트 데이터 버스인 386SX가 제외되었고, FreeBSD 6부터는 FPU를 갖춘 486 이상의 CPU만 지원한다. 따라서 현재 FreeBSD/i386은 32비트 데이터 버스, 32비트 어드레스, 수치연산보조프로세서(FPU)를 갖춘 [IA-32](../Page/IA-32.md "wikilink") 아키텍처를 지원하며, 명령어 세트에 따라 I486, I586, I686의 3종류 클래스로 CPU를 분류한다. FreeBSD는 부팅 단계에서 하드웨어를 감지하여 CPU 클래스를 출력한다.

|                                         |                                                                                                                                                  |
| --------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| Intel                                   | i486/i486DX, i486SL, i486DX2, i486DX4, ODP486SX, ODP486DX, ODPR486DX, DX2ODP, DX2ODPR, DX4ODP, DX4ODPR, RapidCAD, { i486SX, i486SX2, i486SL-NM } |
| AMD                                     | Am486DX, Am486DX2, Am486DX2, Am486DX4, Am486DX5/X5/Am5x86, Élan SC520, { Am486SX, Am486SX2 }                                                     |
| Cyrix                                   | Cx486DX, Cx486DX2, Cx486DX4, { Cx486DLC, Cx486DLC2, Cx486DRx, Cx486DRx2, Cx486DRu, Cx486DRu2 }, { Cx486D, Cx486S, Cx486S2 }                      |
| Texas Instruments                       | TI486DX, TI486DX2, TI486DX4, { TX486DLC, TI486SXL }                                                                                              |
| SGS-Thomson                             | ST486DX, ST486DX2, ST486DX4                                                                                                                      |
| IBM                                     | 486DX, 486DX2, 486DX4, BL486DX2, { 486DLC2, 486DLC3 }, { 486SX }                                                                                 |
| UMC                                     | U5SD, U486DX2, { U5S, U5SX 486, U486SX2 }                                                                                                        |
| VMT/ASCII                               | { VM486DLC2 }                                                                                                                                    |
| ※ { }의 CPU들은 내장 FPU가 없으므로, 보조프로세서 장착 필요 |                                                                                                                                                  |

**I486 class**

|             |                                                                                |
| ----------- | ------------------------------------------------------------------------------ |
| Intel       | Pentium, Pentium MMX, Pentium OverDrive MMX (PODPMT), Pentium OverDrive (P24T) |
| AMD         | 5k86/K5, K6, K6-2, K6-2-P, K6-2+, K6-III, K6-III-P, K6-III+                    |
| Cyrix       | 5x86                                                                           |
| SGS-Thomson | ST5x86                                                                         |
| IBM         | 5x86C                                                                          |
| RiSE        | mP6                                                                            |
| NexGen      | Nx586-PF, Nx586 + Nx587                                                        |
| CenTaur/idt | C6/WinChip, WinChip2                                                           |
| Transmeta   | Crusoe                                                                         |

**I586 class**

|             |                                                                                                                                                                                                                                        |
| ----------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Intel       | Pentium Pro, Pentium II OverDrive, Pentium II, Pentium III, Pentium 4, Celeron, Pentium II Xeon, Pentium III Xeon, Xeon, Xeon MP, Dual-Core Xeon LV, Pentium 4-M, Pentium M, Celeron M, Core Duo, Core Solo, Pentium Dual-Core (Yonah) |
| AMD         | Athlon, Athlon XP, Sempron, Duron, Athlon MP                                                                                                                                                                                           |
| Cyrix       | 6x86, 6x86L, 6x86MX, M II                                                                                                                                                                                                              |
| SGS-Thomson | ST6x86                                                                                                                                                                                                                                 |
| IBM         | 6X86, 6X86L, 6X86MX                                                                                                                                                                                                                    |
| VIA         | CyrixIII/C3, C3-M, C7                                                                                                                                                                                                                  |
|             |                                                                                                                                                                                                                                        |

**I686 class**

대체로 인텔의 CPU를 기준으로 호환 CPU도 그것을 따르게 되는데, FreeBSD에서의 인식은 커널 최적화 목적이므로, CPU 설계에 따른 엄밀한 분류나 동작 성능에 따른 실용 등급과 일치하지 않는 경우도 있다. 현재 386 기종은 제외된 상태이지만, 386DX 시스템에 장착된 몇몇 특수한 CPU는 486 호환이므로 FPU만 지원되면 i486 클래스로 설치할 수 있다.\[23\] 커널을 컴파일할 때 CPU 옵션을 지정하여 최적화된 실행 코드를 생성하는데, 실제 시스템보다 상위 클래스로 컴파일하면 제대로 동작되지 못한다.

그밖에 설치를 위한 최소 요구사양은 RAM 24MB, HDD 150MB이다. 디스켓 부팅에 의한 네트워크 설치도 지원되므로, CD-ROM 드라이브는 필수적인 것은 아니다.

#### AMD64 아키텍처

FreeBSD/amd64는 AMD64와 인텔 EM64T를 지원하는 64비트 [x86-64](https://ko.wikipedia.org/wiki/x86-64 "wikilink") 환경이다. FreeBSD 5.2부터 지원하며, 지원되는 CPU는 다음과 같다.

  - AMD : Athlon 64, Athlon 64 X2, Athlon 64 FX, Turion 64, Turion 64 X2, Opteron, Sempron (일부)
  - Intel : Pentium 4 (일부), Pentium D, Celeron D, Pentium XE, Core 2, Celeron (일부), Xeon (일부)

CPU를 제외하면 대부분 i386 플랫폼과 같다.

#### NEC PC-98 아키텍처

FreeBSD/pc98은 1990년대 중반까지 주로 일본을 중심으로 보급되었던 NEC PC-98 플랫폼으로, CPU는 [x86](https://ko.wikipedia.org/wiki/x86 "wikilink") 기반이지만 I/O 버스 등에서 PC 호환 기종과는 다소 차이가 있다. FreeBSD 5 \~ FreeBSD 8까지만 지원된다.

FreeBSD 5 기준에서 지원하는 시스템은 다음과 같다. 단, 486급 이상의 CPU가 장착된 모델이 요구된다.

  - NEC : PC-9801, PC-9821, FC-9801, FC-9801, SV-98
  - EPSON : PC-486/586

NEC PC-98XA/XL/RL/XL2, PC-H98 계열의 고해상도 모드는 아직 지원되지 않는다.

그밖에, 설치를 위한 최소 요구 사양은 i386과 동일하게 RAM 24MB, HDD 150MB이다.

#### IA-64 아키텍처

FreeBSD/ia64는 인텔 아이태니엄(Itanium) [IA-64](https://ko.wikipedia.org/wiki/IA-64 "wikilink")을 지원한다. FreeBSD 5에서 지원이 시작되었다. 인텔 Itanium, Itanium 2 CPU와 HP zx1, Intel 460GX, Intel E8870 칩셋이 지원된다.

#### DEC 알파 아키텍처

FreeBSD/alpah는 DEC 알파 프로세서 기반 시스템을 지원한다. FreeBSD 3.3\[24\] 및 FreeBSD 4.1\[25\]부터 지원되었으나 알파 기종의 단종에 따라 FreeBSD 7부터는 개발이 중단되었다.\[26\]

#### SUN UltraSparc 아키텍처

FreeBSD/sparc64는 SUN의 UltraSparc 시스템들을 지원하며, FreeBSD 5부터 지원된다.

  - Blade 100, Blade 150
  - Enterprise 220R, Enterprise 250, Enterprise 420R, Enterprise 450
  - Fire V100, Fire V120
  - Netra t1 105, Netra T1 AC200/DC200, Netra t 1100, Netra t 1120, Netra t 1125, Netra t 1400/1405, Netra 120, Netra X1
  - SPARCEngine Ultra AXi, SPARCEngine Ultra AXmp
  - Ultra 1, Ultra 1E, Ultra 2, Ultra 5, Ultra 10, Ultra 30, Ultra 60, Ultra 80

Enterprise 3500, Enterprise 4500 시스템은 부분적으로 지원되며, UltraSPARC III 기종은 지원하지 않는다.

#### PowerPC 아키텍처

FreeBSD/powerpc는 PowerPC 기반 시스템을 지원한다. FreeBSD 6부터 지원된다.

#### ARMv6

FreeBSD/ARMv6은 ARM 기반 시스템들을 지원하며, FreeBSD 10.1부터 지원한다 괄호 안의 버전은 지원 중 혹은 잠시 지원이 됐었던 것들이다.

  - BEAGLEBONE(10.1R\~)
  - RPI-B(10.1R\~)
  - PANDABOARD(10.1R\~)
  - ZEDBOARD(10.1R)
  - GUMSTIX(10.2R\~)
  - CUBOX-HUMMINGBOARD(10.2\~)
  - WANDBOARD(10.2\~)

### 포트 및 패키지

기본 [시스템 소프트웨어](../Page/시스템_소프트웨어.md "wikilink") 이외에 [응용 프로그램들은](https://ko.wikipedia.org/wiki/응용_프로그램 "wikilink") 운영 체제 설치와 별도로 설치 작업이 필요한데, FreeBSD는 이 과정에 대하여 포트(port) 및 패키지(package)라는 관리 방법을 사용한다.

시스템에 설치된 응용 프로그램은 각각 패키지라는 개념으로 관리된다. 하나의 응용 프로그램이라도 여러 가지 요소로 구성되며 또한 여러 응용 프로그램에서 공통적으로 사용되는 요소도 존재하는데, 각각 개별 단위로 구분될 수 있는 구성 요소가 “패키지”가 된다. 이때 프로그램의 올바른 설치 및 동작을 위해 필요한 패키지 상호간의 관계를 “의존성”이라고 하는데, FreeBSD의 패키지 관리에서는 이러한 의존성까지 점검하고 있다.

한편, 패키지는 바이너리 파일로 직접 설치될 수도 있지만 프로그램 소스를 직접 컴파일하여 설치할 수도 있는데, 이 경우에는 우선 배포되는 프로그램 소스를 수집하고, 운영 체제 및 하드웨어에 적합하도록 소스 코드의 일부 수정이 필요하게 된다. 이때 FreeBSD는 “포트”를 사용하여 소스 코드의 수집, 수정과 컴파일 및 설치 과정 모두를 자동화한다. 즉, “포트”는 소스 코드를 통한 응용 프로그램 설치를 위하여, 소스 코드의 배포 위치, 수정해야 할 부분, 컴파일 작업, 설치 과정 등 모든 단계의 정보를 담아 놓은 자동화 파일의 집합이다. 이것을 통하여 FreeBSD는 직접 관리·배포하는 기본 [시스템 소프트웨어](../Page/시스템_소프트웨어.md "wikilink") 이외에도 사용 가능한 모든 오픈 소스 프로그램에 대하여 일관된 유지 보수가 가능하게 된다.

### 호환성

FreeBSD는 다른 유닉스 계열 및 리눅스 운영 체제와 바이너리 호환성을 제공하고 있는데, FreeBSD 7에서는 리눅스 커널 2.6과 바이너리 호환성이 제공된다.

이처럼 호환 계층을 이용하여 바이너리만 배포되는 리눅스 전용 프로그램도 FreeBSD에서 실행할 수 있는데, 그 대표적인 것으로는 [오라클](https://ko.wikipedia.org/wiki/오라클_DBMS "wikilink"), [VMware](https://ko.wikipedia.org/wiki/VMware "wikilink"), 매스매티카(Mathematica), 매트랩(Matlab), Sun 스타오피스(StarSuite), [워드퍼펙트](../Page/워드퍼펙트.md "wikilink"), [모질라 파이어폭스](https://ko.wikipedia.org/wiki/파이어폭스 "wikilink"), 어도비 아크로뱃, 리얼플레이어, 스카이프(Skype), [둠 3](https://ko.wikipedia.org/wiki/둠_3 "wikilink"), 퀘이크 4 등이 있다. 리눅스용 프로그램을 실행할 때에도 FreeBSD용 프로그램에 비해 두드러진 성능 저하는 없으며, 심지어 같은 프로그램을 리눅스에서 실행시키는 것보다 더 빠른 경우도 있다고 한다.\[27\] 다만, 일부 프로그램은 리눅스 호환 계층에서 실행에 문제가 있을 수 있다.

### 파생된 운영 체제 및 배포본

FreeBSD에서 파생된 운영 체제 및 배포본은 다음과 같다.

  - [TrueOS](../Page/TrueOS.md "wikilink") - [iXsystems](https://ko.wikipedia.org/wiki/iXsystems "wikilink")에서 개발하였다. 가정 사용자와 [워크스테이션](../Page/워크스테이션.md "wikilink")을 주요 대상으로 한다. 예전에는 [PC-BSD](https://ko.wikipedia.org/wiki/PC-BSD "wikilink")라는 이름이었다.
  - [GhostBSD](https://ko.wikipedia.org/wiki/GhostBSD "wikilink") - [그놈](../Page/그놈.md "wikilink") 기반 배포판이며 [LXDE](../Page/LXDE.md "wikilink") [GUI](https://ko.wikipedia.org/wiki/GUI "wikilink")도 지원한다.
  - [MidnightBSD](https://ko.wikipedia.org/wiki/MidnightBSD "wikilink") - [데스크탑](https://ko.wikipedia.org/wiki/데스크탑 "wikilink") 사용자를 대상으로 한다.
  - [DesktopBSD](https://ko.wikipedia.org/wiki/DesktopBSD "wikilink") - 가정 사용자와 [워크스테이션](../Page/워크스테이션.md "wikilink")을 주요 대상으로 한다.
  - [DragonFly BSD](../Page/DragonFly_BSD.md "wikilink")
  - [TrustedBSD](http://www.trustedbsd.org/), The TrustedBSD Project.
  - [FreeNAS](http://www.freenas.org/)
  - [FreeSBIE](http://www.freesbie.org/)
  - [Arch BSD](https://ko.wikipedia.org/wiki/Arch_BSD "wikilink")

FreeBSD를 참조한 운영 체제는 다음과 같다.

  - [애플 다윈](https://ko.wikipedia.org/wiki/애플_다윈 "wikilink") - [Apple Darwin (Mac OS X core)](http://developer.apple.com/darwin/), Apple, Inc.

### 다른 주요 BSD 운영 체제

  - [NetBSD](../Page/NetBSD.md "wikilink") : FreeBSD와 비슷한 시기에 출발했으며, 이식성에 중점을 두고 개발되어\[28\] 가장 다양한 플랫폼을 지원하고 있다. 최신 버전은 6.1.3이며, 현재 54개 플랫폼을 지원하고 있다.\[29\]
  - [OpenBSD](../Page/OpenBSD.md "wikilink") : NetBSD의 초기에 갈라졌으며, 보안에 역점을 두며\[30\] 최상의 개발 플랫폼을 제공하려 한다.\[31\] 최신 버전은 4.2이다.\[32\]
  - [BSD/OS](https://ko.wikipedia.org/wiki/BSD/OS "wikilink") : 현재 단종. 상용 제품으로 본래의 BSD 개발진들이 BSD, Inc.를 설립하여 개발해왔다.
  - [Mac OS X](https://ko.wikipedia.org/wiki/Mac_OS_X "wikilink") : 애플의 GUI 운영 체제로 상용 제품이다. 기존 4.3BSD + Mach 2.5 기반이었던 NEXTSTEP/OPENSTEP을 바탕으로 옛 Mac OS를 흡수하는 방식으로 만들어졌는데, 골격을 FreeBSD 5 + Mach 3.0으로 갱신한 다윈을 토대로 기존 매킨토시 API 지원을 위한 Carbon, OpenStep API 지원을 위한 코코아, 자바 플랫폼 지원 등을 포함하며, 그래픽 환경은 전통적인 유닉스의 X 윈도 시스템 대신에 Quartz 엔진 중심의 Aqua를 사용한다.

## 개발 방식과 조직

### 개발 조직

FreeBSD는 전통적인 BSD 라이선스에 따라 오픈 소스 모델로 개발되고 있다. 개발진은 소스 코드를 직접 수정할 수 있는 커미터(Committer)들과 그 가운데 주요 사안에 대한 최종 의결권이 부여된 코어 팀(Core Team)이 구성되며, 이들을 중심으로 그 밖의 공헌자(Contributor)들이 참여하는 형태로 되어 있다. FreeBSD의 개발진에는 과거 BSD 시절부터의 개발자들도 참여하고 있으며, 리눅스 프로젝트에 비해 연령대가 높은 편이다.

이 가운데 한국인 커미터는 2008년 3월 현재 5명이다.

  - 최준호: ports
  - 편용헌: src
  - 장혜식: ports
  - 김정욱: src
  - 정원교: src

### FreeBSD 재단

FreeBSD 프로젝트를 후원하기 위한 비영리 단체로 FreeBSD 재단([The FreeBSD Foundation](http://www.freebsdfoundation.org/))이 설립되어 있다. 2000년 말에 설립된 이 단체는 FreeBSD를 위한 각종 모금 활동 등 후원 조직인 동시에 법률 관계, 라이선스, 계약 체결 등에서 FreeBSD 프로젝트의 법적 실체로 활동한다.\[33\] 재단 설립 이전에는 프로젝트의 초기 멤버인 조다단 허버드와 데이비드 그린맨이 1995년 초에 설립한 ‘FreeBSD, Inc.’가 이러한 역할을 대행하였다.\[34\]

### 라이선스

FreeBSD는 다른 BSD계열 운영 체제와 마찬가지로 기본적으로 BSD 라이선스를 따르고 있으나, 최종 배포본 구성에서는 외부 개발 코드도 사용되므로 전체적으로는 다양한 [라이선스](https://ko.wikipedia.org/wiki/라이선스 "wikilink")가 적용되어 있다.

거의 대부분을 차지하는 비교적 새로 짜인 기본 코드는 FreeBSD 라이선스\[35\]가 적용되는데, 이것은 두 조항으로 구성된 BSD 사용 허가서로서 저작권 명시와 보증 부인 및 면책 선언을 유지하는 조건으로 자유로운 수정 및 재배포가 허락된다.

그 밖에 외부 코드는 대부분 BSD 계열 라이선스나 [GPL](https://ko.wikipedia.org/wiki/GPL "wikilink") 또는 [LGPL](https://ko.wikipedia.org/wiki/LGPL "wikilink")을 따르고 있다.

### 로고와 마스코트

초기 FreeBSD 로고는 ‘Beastie’라는 애칭의 BSD 데몬(BSD Daemon)을 그대로 사용했다. 4.2BSD부터 사용된 BSD의 로고 BSD 데몬은 다른 이름은 갖지 않는다. 현재 BSD 데몬의 저작권은 4.4BSD의 개발자였던 마셜 커크(Marshall Kirk McKusick)가 소유하고 있다.\[36\] 여기에는 여러 가지 도안이 존재하는데 가장 널리 알려진 것은 애니메이션 “토이 스토리(Toy Story)”의 작가 존 라세터(John Alan Lasseter)의 작품이다. FreeBSD에 특화된 도안으로는 [호소카와 타츠미의 도안](http://fromto.cc/hosokawa/gallery/)이 사용되다가,\[37\] 2005년에 새로운 로고를 공모하여 2005년 10월 8일 Anton K. Gural의 디자인이 채택되었고,\[38\] 예전의 [BSD 데몬은](../Page/BSD_데몬.md "wikilink") FreeBSD의 마스코트로 남게 되었다.

FreeBSD의 슬로건은 ‘The Power to Serve’이다.

## 관련 도서

### 한글 출판본

2008년 3월 현재까지 대한민국에서 출간된 FreeBSD 관련 서적은 모두 3권이 확인된다.

  - [《About FreeBSD》. 최준호, 김승영, 오준선, 편용헌. (주)영진닷컴, 2000.](https://web.archive.org/web/20100704213117/http://www.kr.freebsd.org/doc/aboutfreebsd/) (절판)
  - [《클릭하세요 FreeBSD》. 최성, 이영옥. 도서출판 대림, 2005.](https://web.archive.org/web/20120111072055/http://www.drbook.co.kr/new_20050605/books/view.asp?ISBN=8972807184)
  - [《오픈 소스 BSD 돌아온 전설》. Michael W. Lucas 저. 이정문, 신승현 역. 에이콘출판사, 2003.](http://www.acornpub.co.kr/book/open-bsd/) (번역판: 원제 *Absolute BSD*. 2002.)

### 영문 출판본

영문판 서적은 상당수 존재하는데, 그 가운데 대표적인 것들은 다음과 같다.

  - [*The Design and Implementation of the FreeBSD Operating System*. Marshall K. McKusick, George V. Neville-Neil. Addison Wesley, 2004.](https://web.archive.org/web/20050307020853/http://www.aw-bc.com/catalog/academic/product/0,1144,0201702452,00.html)
  - [*The Design and Implementation of the 4.4BSD Operating System*. Marshall K. McKusick, Keith Bostic, Michael J. Karels, John S. Quartermain. Addison Wesley, 1996.](https://web.archive.org/web/20050114092826/http://www.aw-bc.com/catalog/academic/product/0,1144,0201549794,00.html)
  - [*The Complete FreeBSD*. Greg Lehey. O'Reilly Media, 2003.](http://oreilly.com/catalog/cfreebsd/)
  - [*Absolute FreeBSD, 2nd Edition*. Michael W. Lucas. No Starch Press, 2007.](https://web.archive.org/web/20071127144640/http://www.nostarch.com/abs_bsd2.htm)
  - [*Absolute BSD*. Michael W. Lucas. No Starch Press, 2002.](https://web.archive.org/web/20080107140544/http://www.nostarch.com/abs_bsd.htm)

### 한글 전자책

  - [《한글 FreeBSD 핸드북》. The FreeBSD Documentation Project 저, 이영옥 역, 김승영 편. KFUG, 2005.](https://web.archive.org/web/20071112120256/http://www.kr.freebsd.org/doc/KoreanFreeBSDHandbook/) (번역본: *FreeBSD Handbook*. 2004.)

### 영문 전자책

  - [*FreeBSD Handbook*. The FreeBSD Documentation Project. 2008.](http://www.freebsd.org/doc/en_US.ISO8859-1/books/handbook/)
  - [*FreeBSD Developers' Handbook*. The FreeBSD Documentation Project. 2006.](http://www.freebsd.org/doc/en_US.ISO8859-1/books/developers-handbook/)
  - [*FreeBSD Architecture Handbook*. The FreeBSD Documentation Project. 2006.](http://www.freebsd.org/doc/en_US.ISO8859-1/books/arch-handbook/)
  - [*The Complete FreeBSD*. Greg Lehey. 2006.](http://www.lemis.com/grog/Documentation/CFBSD/)

## 참고문헌

  - 《about FreeBSD》. 최준호, 김승영, 오준선, 편용헌. (주)영진닷컴, 2000.
  - 《오픈 소스》. 송창훈, 이기동, 이만용, 최준호. 한빛미디어(주), 2000. [1](http://www.hanb.co.kr/look.php?isbn=89-7914-069-X)
  - 《한글 FreeBSD 핸드북》. 이영옥 역, 김승영 편. KFUG, 2005. [2](https://web.archive.org/web/20071112120256/http://www.kr.freebsd.org/doc/KoreanFreeBSDHandbook/)
  - *FreeBSD 6 UNLEASHED*. Brian Tiemann. SAMS Publishing, 2006.
  - *FreeBSD Handbook*. The FreeBSD Documentation Project. 2008. [3](http://www.freebsd.org/doc/en_US.ISO8859-1/books/handbook/)
  - *FreeBSD Handbook*. The FreeBSD Documentation Project. 2000.
  - *Mac OS X Technology Overview*. Apple, Inc., 2007. [4](http://developer.apple.com/documentation/MacOSX/Conceptual/OSX_Technology_Overview/)
  - ["FreeBSD 7.0-RELEASE Hardware Notes"](http://www.freebsd.org/releases/7.0R/hardware.html). The FreeBSD Documentation Project, 2008.
  - [〈버클리 유닉스의 20년〉, Marshall Kirk McKusick, 최준호 역. 《오픈 소스》(PDF판). 한빛미디어, 2000.](http://www.hanb.co.kr/download/opensource/opensource02.pdf)
  - [〈왜 FreeBSD인가?〉, Frank Pohlmann. 《IBM developerWorks》(한국판). IBM, 2005.](http://www.ibm.com/developerworks/kr/library/os-freebsd/)
  - [〈Yahoo\!와 FreeBSD〉, David Filo, 김승영 역. 1999.](https://web.archive.org/web/20080511180603/http://www.kr.freebsd.org/doc/yahoo_and_freebsd/)
  - [〈전 세계 역사상 가장 위대한 소프트웨어〉, 《컴퓨터월드》, 2006년 11월호.](http://www.itdaily.kr/news/articleView.html?idxno=5415)

<!-- end list -->

  - ["Twenty Years of Berkeley Unix", Marshall Kirk McKusick. *Open Sources*. O'Reilly Media, 1999.](http://www.oreilly.com/catalog/opensources/book/kirkmck.html)
  - ["The FreeBSD System", *Operating Systems Concepts* (6th edn.). Abraham Silberschatz, Peter Baer Galvin. Greg Gagne. John Wiley & Sons, 2001.](http://www.wiley.com/college/silberschatz6e/0471417432/pdf/bsd.pdf)
  - ["Why FreeBSD", Frank Pohlmann. *IBM developerWorks*. IBM, 2005.](http://www-128.ibm.com/developerworks/opensource/library/os-freebsd/)
  - ["What's The Greatest Software Ever Written?", Charles Babcock. *InformationWeek*, 2006-09-14.](http://www.informationweek.com/research/showArticle.jhtml?articleID=191901844)

## 각주

<references />

## 외부 링크

  - [The FreeBSD Project](https://www.freebsd.org) : FreeBSD 공식 홈페이지
  - [The FreeBSD Mall](http://www.freebsdmall.com) (FreeBSD Mall, Inc.) : FreeBSD 관련 상품의 주요 공급처
  - [The FreeBSD Ports Archive](http://www.freebsdsoftware.org) : FreeBSD 포트 모음
  - [Korea FreeBSD Users Group](ftp://ftp.kr.freebsd.org/pub/FreeBSD-kr/doc/www/htdocs/index.shtml)

<!-- end list -->

  - [대한민국](../Page/대한민국.md "wikilink")의 [미러](https://ko.wikipedia.org/wiki/미러_\(컴퓨팅\) "wikilink") 사이트

<!-- end list -->

  - [네오위즈게임즈의 FreeBSD 포트 미러](https://web.archive.org/web/20140811071745/http://ftp.neowiz.com/)
  - [카이스트의 FreeBSD 포트 미러](https://web.archive.org/web/20140423105852/http://ftp.kaist.ac.kr/)
  - [FreeBSD 한국 미러](https://web.archive.org/web/20151118124053/http://ftp4.kr.freebsd.org/pub/FreeBSD/)
  - [FreeBSD 한국 미러](https://web.archive.org/web/20151118100827/http://ftp5.kr.freebsd.org/pub/FreeBSD/)
  - [FreeBSD 한국 미러](https://web.archive.org/web/20151118122123/http://ftp6.kr.freebsd.org/pub/FreeBSD/)

[FreeBSD](https://ko.wikipedia.org/wiki/분류:FreeBSD "wikilink") [분류:BSD](https://ko.wikipedia.org/wiki/분류:BSD "wikilink") [분류:1993년 소프트웨어](https://ko.wikipedia.org/wiki/분류:1993년_소프트웨어 "wikilink") [분류:ARM 운영 체제](https://ko.wikipedia.org/wiki/분류:ARM_운영_체제 "wikilink") [분류:파워PC 운영 체제](https://ko.wikipedia.org/wiki/분류:파워PC_운영_체제 "wikilink") [분류:자유 소프트웨어 운영 체제](https://ko.wikipedia.org/wiki/분류:자유_소프트웨어_운영_체제 "wikilink") [분류:BSD 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:BSD_라이선스_소프트웨어 "wikilink")

1.  [MS, 핫메일 W2K로 이전 「유닉스 따라잡기」](http://www.zdnet.co.kr/news/enterprise/0,39031021,10006965,00.htm). ZDNet Korea, 2000-08-03.
2.  [Microsoft Hotmail still runs on U\*\*x](http://www.theregister.co.uk/2001/12/12/microsoft_hotmail_still_runs/). The Register, 2001-12-12.
3.  이영옥, 〈FreeBSD 소개〉, 《한글 FreeBSD 핸드북》. 2005.
4.  “Mac OS X System Overview,” *Mac OS X Technology Overview*. Apple, Inc., 2007-10-31.
5.  [MS, FreeBSD와 C\#, CLI의 소스 공유키로 결정](http://www.zdnet.co.kr/news/enterprise/0,39031021,10039391,00.htm). ZDNet Korea, 2001-07-04.
6.  [MS, FreeBSD와 윈도용 표준화 소스코드 공유](http://www.zdnet.co.kr/news/enterprise/0,39031021,10047587,00.htm). ZDNet Korea, 2002-03-31.
7.  이에 따라 FreeBSD는 이때의 공헌자들을 FreeBSD 공헌자로 인정하고 있다. [386BSD Patch Kit Patch Contributors](http://www.freebsd.org/doc/en_US.ISO8859-1/articles/contributors/contrib-386bsd.html), *Contributors to FreeBSD*. The FreeBSD Project, 2006-09-11.
8.  386BSD의 개발자인 William Jolitz는 처음에는 이 작업을 386BSD의 개발 과정으로 승인했으나, 나중에 취소하였다.
9.  [A Brief History of FreeBSD](http://www.freebsd.org/doc/en_US.ISO8859-1/books/handbook/history.html), Jordan K. Hubbard.
10. ["Not Just Another Free Unix", Jordan Hubbard. *BYTE* (December 1995). CMP Media](http://www.byte.com/art/9512/sec14/art1.htm) .
11. "The code from 4.4BSD-Lite2 has been (finally) merged." ([FreeBSD 3.0 Release Notes](http://www.freebsd.org/releases/3.0R/notes.html). The FreeBSD Project, 1998-10-16.)
12. [BSD SUPPLIERS UNITE TO DELIVER THE WORLD'S MOST POPULAR INTERNET OPERATING SYSTEMS](http://www.freebsd.org/news/press-rel-4.html). FreeBSD Press Release: March 9, 2000.
13. [Changes are a' comin'\!](http://ezine.daemonnews.org/200003/merger.html) , Gregory Sutter. Dæmon News.
14. [Bob Bruce on the BSDI/Walnut Creek Merger](http://bsd.slashdot.org/article.pl?sid=00/03/09/0711253), Slashdot.
15. [Merger Interview](http://ezine.daemonnews.org/200004/interview.html) , Chris Coleman, Dæmon News.
16. 〈FreeBSD에 대해서〉, 최준호, 《about FreeBSD》. (주)영진닷컴, 2000.
17.
18.
19. [Early Adopter's Guide to FreeBSD 5.0-RELEASE](http://www.freebsd.org/releases/5.0R/early-adopter.html). The FreeBSD Release Engineering Team, 2003.
20. [FreeBSD 7.0-RELEASE Announcement](http://www.freebsd.org/releases/7.0R/announce.html). The FreeBSD Project, 2008-02-27.
21. [Faster Performance, Fewer Machines For FreeBSD?](http://www.internetnews.com/dev-news/article.php/3731386/Faster+Performance+Fewer+Machines+For+FreeBSD.htm). Sean Michael Kerner. *InternetNews.com*, 2008-02-29.
22. [FreeBSD Project Goals](http://www.freebsd.org/doc/en_US.ISO8859-1/books/handbook/history.html), Jordan K. Hubbard.
23. Intel RapidCAD, Cyrix Cx486DLC, Cx486DLC2, Cx486DRx, Cx486DRx2, Cx486DRu, Cx486DRu2 등이 여기에 해당한다.
24. [FreeBSD 3.3 Announcement](http://www.freebsd.org/releases/3.3R/announce.html). 1999-09-17.
25. [FreeBSD 4.1 Announcement](http://www.freebsd.org/releases/4.1R/announce.html). 2000-07-27.
26. [FreeBSD/alpha Project](http://www.freebsd.org/platforms/alpha.html). The FreeBSD Project
27. Brian Tiemann. "How FreeBSD Compares to Other Operating Systems", *FreeBSD 6 UNLEASHED*. SAMS, 2006.
28. “One of the primary focuses of the NetBSD project has been to make the base OS highly portable.”([About the NetBSD Project](http://www.netbsd.org/about/). The NetBSD Foundation, Inc.)
29. [Announcing NetBSD 4.0](http://www.netbsd.org/releases/formal-4/NetBSD-4.0.html). The NetBSD Foundation, Inc., 2007-12-19.
30. “Try to be the \#1 most secure operating system”([Project Goals](http://www.openbsd.org/goals.html). OpenBSD.)
31. “Provide the best development platform possible.”([Project Goals](http://www.openbsd.org/goals.html). OpenBSD.)
32. [The OpenBSD 4.2 Release](http://www.openbsd.org/42.html). OpenBSD, 2007-11-01.
33. [About the FreeBSD Foundation](http://www.freebsdfoundation.org/about.shtml) , The FreeBSD Foundation.
34. “FreeBSD, Inc. was founded in early 1995 by Jordan K. Hubbard and David Greenman with the goal of furthering the aims of the FreeBSD Project and giving it a minimal corporate presence.”("Contributing to FreeBSD", *FreeBSD Handbook*. The FreeBSD Documentation Project, 2000.)
35. [The FreeBSD Copyright](http://www.freebsd.org/copyright/freebsd-license.html), The FreeBSD Project.
36. [History of the BSD Daemon](http://www.mckusick.com/beastie/), Marshall Kirk McKusick. The official home of the BSD Daemon.
37. [The BSD Daemon](http://www.freebsd.org/copyright/daemon.html), The FreeBSD project.
38. [Final result for the FreeBSD logo design competition](http://logo-contest.freebsd.org/result/) , The FreeBSD project.