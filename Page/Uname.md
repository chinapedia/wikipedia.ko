> This article is converted from Wikipedia: [Uname](https://ko.wikipedia.org/wiki/Uname).


**uname**(*unix name*의 준말)은 [유닉스](../Page/유닉스.md "wikilink") 및 [유닉스 계열](../Page/유닉스_계열.md "wikilink") 컴퓨터 [운영 체제의](../Page/운영_체제.md "wikilink") [컴퓨터 프로그램의](../Page/컴퓨터_프로그램.md "wikilink") 하나로, 현재의 머신, 또 그 머신 위에 실행 중인 운영 체제에 대한 이름, 버전, 기타 자세한 정보를 출력해준다. `uname` 시스템 호출과 명령은 [PWB/UNIX](https://ko.wikipedia.org/wiki/PWB/UNIX "wikilink")에 처음 등장하였다. 둘 다 [POSIX](../Page/POSIX.md "wikilink")에 의해 정의되어 있다.\[1\]\[2\]

[AT\&T](../Page/AT&T.md "wikilink") [유닉스 시스템 V](https://ko.wikipedia.org/wiki/유닉스_시스템_V "wikilink") 릴리스 3.0과 같은 일부 유닉스 계열은 관련 `setname` 프로그램을 포함하고 있어서 uname이 보고하는 값을 변경할 수 있다.

[GNU](../Page/GNU.md "wikilink") 버전의 uname은 "sh-utils" 또는 "coreutils" 패키지에 포함되어 있다. uname 그 자체는 독립적인 프로그램으로 사용이 불가능하다.

## 예

[다윈을](../Page/다윈_\(운영_체제\).md "wikilink") 실행 중인 시스템에서 `-a` [명령 줄 인터페이스에](../Page/명령_줄_인터페이스.md "wikilink") `uname`을 실행한 결과의 출력물은 아래의 텍스트과 같이 표시된다:

``` console
$ uname -a
Darwin Roadrunner.local 10.3.0 Darwin Kernel Version 10.3.0: Fri Feb 26 11:58:09 PST 2010; root:xnu-1504.3.12~1/RELEASE_I386 i386
```

아래의 표는 다양한 플랫폼에서 다양한 버전의 `uname`을 실행한 예를 포함하고 있다.\[3\] [bash](../Page/배시_\(유닉스_셸\).md "wikilink") 셸 내에서 **OSTYPE** [환경 변수에는](../Page/환경_변수.md "wikilink") 의 값과 비슷한(동일하지는 않은) 값을 포함하고 있다.

<table>
<thead>
<tr class="header">
<th><p>배포판</p></th>
<th><p>시스템 또는 커널 ()<br />
POSIX</p></th>
<th><p>운영 체제 또는 배포판 ()</p></th>
<th><p>머신 ()<br />
POSIX</p></th>
<th><p>프로세서 ()</p></th>
<th><p>하드웨어 플랫폼 ()</p></th>
<th><p>OS (커널) 버전 ()<br />
POSIX</p></th>
<th><p>OS (커널) 릴리스 ()<br />
POSIX</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="../Page/안드로이드_(운영_체제).md" title="wikilink">안드로이드</a> 4.2.1 on <a href="../Page/넥서스_4.md" title="wikilink">넥서스 4</a></p></td>
<td><p>Linux</p></td>
<td><p>GNU/Linux</p></td>
<td><p>armv7l</p></td>
<td></td>
<td></td>
<td><p>#1 SMP PREEMPT Thu Nov 8 15:42:02 PST 2012</p></td>
<td><p>3.4.0-perf-ge039dcb</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/안드로이드_(운영_체제).md" title="wikilink">안드로이드</a> 2.3 on Meteorit netbook</p></td>
<td><p>Linux</p></td>
<td><p>GNU/Linux</p></td>
<td><p>armv6l</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>any, coreutils 7.1</p></td>
<td><p><a href="../Page/리눅스.md" title="wikilink">리눅스</a></p></td>
<td><p>GNU/Linux</p></td>
<td><p>sparc64</p></td>
<td><p>sparc64</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/UltraSPARC_T1" title="wikilink">UltraSPARC T1</a> (Niagara)</p></td>
<td><p>(all)</p></td>
<td><p>(all)</p></td>
</tr>
<tr class="even">
<td><p>any, coreutils 7.1-8.4</p></td>
<td><p><a href="../Page/리눅스.md" title="wikilink">리눅스</a></p></td>
<td><p>GNU/Linux</p></td>
<td><p>ppc64</p></td>
<td><p>ppc64</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/PowerPC_970" title="wikilink">PPC 970FX</a> (<a href="https://ko.wikipedia.org/wiki/XServe#Xserve_G5" title="wikilink">XServe G5</a>)</p></td>
<td><p>(all)</p></td>
<td><p>(all)</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/비지박스.md" title="wikilink">busybox-w32</a> 1.27 (32-bit) on Windows 10</p></td>
<td><p>Windows_NT</p></td>
<td><p>MS/Windows</p></td>
<td><p>i686</p></td>
<td></td>
<td></td>
<td><p>9200</p></td>
<td><p>6.2</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/비지박스.md" title="wikilink">busybox-w32</a> 1.27 (64-bit) on Wine 2.0</p></td>
<td><p>Windows_NT</p></td>
<td><p>MS/Windows</p></td>
<td><p>x86_64</p></td>
<td></td>
<td></td>
<td><p>3790</p></td>
<td><p>5.2</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/CentOS.md" title="wikilink">CentOS</a> 6.5, Pentium SU4100</p></td>
<td><p><a href="../Page/리눅스.md" title="wikilink">리눅스</a></p></td>
<td><p>GNU/Linux</p></td>
<td><p>i686</p></td>
<td><p>i686</p></td>
<td><p>i386</p></td>
<td><p>#1 SMP Fri Nov 22 00:26:36 UTC 2013</p></td>
<td><p>2.6.32-431.el6.i686</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/Cray" title="wikilink">Cray</a> <a href="https://ko.wikipedia.org/wiki/UNICOS" title="wikilink">UNICOS</a> 9.0.2.2</p>
</td></td>
<td><p>sn5176</p>
</td></td>
<td></td></td>
<td><p>CRAY Y-MP</p>
</td></td>
<td></td></td>
<td></td></td>
<td><p>sin.0</p>
</td></td>
<td><p>9.0.2.2</p>
</td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/시그윈.md" title="wikilink">시그윈</a> (Windows XP), Pentium 4</p></td>
<td><p>CYGWIN_NT-5.1</p></td>
<td><p>Cygwin</p></td>
<td><p>i686</p></td>
<td><p>unknown</p></td>
<td><p>unknown</p></td>
<td><p>2006-01-20 13:28</p></td>
<td><p>1.5.19(0.150/4/2)</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/시그윈.md" title="wikilink">시그윈</a> 1.7 (Windows 7 32-bit), Core i7</p></td>
<td><p>CYGWIN_NT-6.1</p></td>
<td><p>Cygwin</p></td>
<td><p>i686</p></td>
<td><p>unknown</p></td>
<td><p>unknown</p></td>
<td><p>2012-07-20 22:55</p></td>
<td><p>1.7.16(0.262/5/3)</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/시그윈.md" title="wikilink">시그윈</a> 1.7 (Windows 7 64-bit), Core i7</p></td>
<td><p>CYGWIN_NT-6.1-WOW64</p></td>
<td><p>Cygwin</p></td>
<td><p>i686</p></td>
<td><p>unknown</p></td>
<td><p>unknown</p></td>
<td><p>2012-05-09 10:25</p></td>
<td><p>1.7.15(0.260/5/3)</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/시그윈.md" title="wikilink">시그윈</a> 1.7 64 bit (Windows 7 64-bit)</p></td>
<td><p>CYGWIN_NT-6.1</p></td>
<td><p>Cygwin</p></td>
<td><p>x86_64</p></td>
<td><p>unknown</p></td>
<td><p>unknown</p></td>
<td><p>2014-02-09 21:06</p></td>
<td><p>1.7.28(0.271/5/3)</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/시그윈.md" title="wikilink">시그윈</a> 2.2 64 bit (Windows 10 64-bit)</p></td>
<td><p>CYGWIN_NT-10.0</p></td>
<td><p>Cygwin</p></td>
<td><p>x86_64</p></td>
<td><p>unknown</p></td>
<td><p>unknown</p></td>
<td><p>2015-08-20 11:42</p></td>
<td><p>2.2.1(0.289/5/3)</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/DJGPP" title="wikilink">DJGPP</a> v2 32 bit (Windows Server 2008)</p></td>
<td><p>MS-DOS</p></td>
<td></td></td>
<td><p>i686</p></td>
<td></td></td>
<td></td></td>
<td><p>50</p></td>
<td><p>5</p></td>
</tr>
<tr class="odd">
<td><p>Debian 6.0.5 on <a href="../Page/라즈베리_파이.md" title="wikilink">라즈베리 파이</a> B</p></td>
<td><p>Linux</p></td>
<td><p>GNU/Linux</p></td>
<td><p>armv6l</p></td>
<td></td>
<td><p>(-i) / invalid (-M)</p></td>
<td><p>#90 Wed Apr 18 18:23:05 BST 2012 / #538 PREEMPT Fri Aug 30 20:42:08 BST 2013</p></td>
<td><p>3.1.9+ / 3.6.11+</p></td>
</tr>
<tr class="even">
<td><p>Debian on <a href="https://ko.wikipedia.org/wiki/Western_Digital_My_Book#My_Book_Live" title="wikilink">WD MyBookLive</a></p></td>
<td><p>Linux</p></td>
<td><p>GNU/Linux</p></td>
<td><p>ppc</p></td>
<td></td>
<td><p>(-i) / invalid (-M)</p></td>
<td><p>#1 Fri Oct 15 17:13:23 PDT 2010</p></td>
<td><p>2.6.32.11-svn21605</p></td>
</tr>
<tr class="odd">
<td><p>Debian GNU/<a href="../Page/GNU_허드.md" title="wikilink">Hurd</a></p></td>
<td><p>GNU</p></td>
<td><p>GNU</p></td>
<td><p>i686-AT386</p></td>
<td><p>unknown</p></td>
<td><p>unknown (-i) / 유효하지 않은 옵션 (-M)</p></td>
<td><p>GNU-Mach 1.3.99-486/Hurd-0.3</p></td>
<td><p>0.3</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/Debian_GNU/kFreeBSD" title="wikilink">Debian GNU/kFreeBSD</a> 6.0, AMD</p></td>
<td><p>GNU/kFreeBSD</p></td>
<td><p>GNU/kFreeBSD</p></td>
<td><p>x86_64</p></td>
<td><p>amd64</p></td>
<td><p>AMD Sempron(tm) Processor 3000+</p></td>
<td><p>#0 Thu Nov 26 04:22:59 CET 2009</p></td>
<td><p>8.0-1-amd64</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/DragonFly_BSD.md" title="wikilink">DragonFly BSD</a></p></td>
<td><p>DragonFly</p></td>
<td></td>
<td><p>i386</p></td>
<td><p>i386</p></td>
<td><p>GENERIC</p></td>
<td><p>DragonFly v2.13.0.749.g93fef-DEVELOPMENT #0: …</p></td>
<td><p>2.13-DEVELOPMENT</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/DragonFly_BSD.md" title="wikilink">DragonFly BSD</a> 2.7, AMD64</p></td>
<td><p>DragonFly</p></td>
<td></td>
<td><p>x86_64</p></td>
<td><p>x86_64</p></td>
<td><p>[filename of kernel conf file]</p></td>
<td><p>DragonFly v2.7.3.122.g0ba92-DEVELOPMENT #0: Tue June 8 16:50:35 CEST 2010</p></td>
<td><p>2.7-DEVELOPMENT root@Chance.: /usr/obj/usr/src/sys/X86_64_GENERIC</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/페도라_(운영_체제)" title="wikilink">Fedora</a> 19</p></td>
<td><p>Linux</p></td>
<td><p>GNU/Linux</p></td>
<td><p>i686</p></td>
<td><p>i686</p></td>
<td><p>i386</p></td>
<td><p>#1 SMP Fri Mar 7 17:22:54 UTC 2014</p></td>
<td><p>3.13.6-100.fc19.i686</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/FreeBSD.md" title="wikilink">FreeBSD</a> 6.1, Intel</p></td>
<td><p>FreeBSD</p></td>
<td></td>
<td><p>i386</p></td>
<td><p>i386</p></td>
<td><p>[kernel name from kernel conf file. i.e.: GENERIC]</p></td>
<td><p>FreeBSD 6.1-RELEASE-p15 #1: Sun Apr 15 18:04:51 EDT 2007</p></td>
<td><p>6.1-RELEASE-p15</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/FreeBSD.md" title="wikilink">FreeBSD</a> 9.0, Intel</p></td>
<td><p>FreeBSD</p></td>
<td><p>FreeBSD</p></td>
<td><p>amd64</p></td>
<td><p>amd64</p></td>
<td><p>[kernel name from kernel conf file. i.e.: GENERIC]</p></td>
<td><p>FreeBSD 9.0-RELEASE #0: Tue Jan 3 07:46:30 UTC 2012 root@farrell.cse.buffalo.edu:/usr/obj/usr/src/sys/GENERIC</p></td>
<td><p>9.0-RELEASE</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/젠투_리눅스.md" title="wikilink">Gentoo</a>, <a href="https://ko.wikipedia.org/wiki/UltraSPARC_II#UltraSPARC_IIe" title="wikilink">UltraSparc IIe</a></p></td>
<td><p><a href="../Page/리눅스.md" title="wikilink">리눅스</a></p></td>
<td><p>GNU/Linux</p></td>
<td><p>sparc64</p></td>
<td><p>sun4u</p></td>
<td><p>TI UltraSparc IIe (Hummingbird)</p></td>
<td><p>#1 SMP Wed Nov 10 02:04:26 CET 2010</p></td>
<td><p>2.6.34-gentoo-r12</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/하이쿠_(운영_체제)" title="wikilink">Haiku</a> R1/Alpha 1, QEMU</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/하이쿠_(운영_체제)" title="wikilink">Haiku</a></p></td>
<td><p>Haiku</p></td>
<td><p>BePC</p></td>
<td></td>
<td></td>
<td><p>r33109 Sep 12 2009 17:45:45</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/HP-UX.md" title="wikilink">HP-UX</a></p></td>
<td><p>HP-UX</p></td>
<td></td>
<td><p>9000/712</p></td>
<td></td>
<td><p>[Unique machine ID number or node name if cannot be determined.]</p></td>
<td><p>U</p></td>
<td><p>B.11.11</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/HP-UX.md" title="wikilink">HP-UX</a> 11i v3</p></td>
<td><p>HP-UX</p></td>
<td></td>
<td><p>ia64</p></td>
<td></td>
<td><p>[Unique machine ID number or node name if cannot be determined.]</p></td>
<td><p>U</p></td>
<td><p>B.11.31</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/IBM_AIX.md" title="wikilink">IBM AIX</a> 5.3</p></td>
<td><p>AIX</p></td>
<td><p>AIX</p></td>
<td><p>00C57D4D4C00</p></td>
<td><p>powerpc</p></td>
<td><p>IBM,8205-E6B</p></td>
<td><p>5</p></td>
<td><p>3</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/IBM_AIX.md" title="wikilink">IBM AIX</a> 7.1</p></td>
<td><p>AIX</p></td>
<td></td>
<td><p>uniqe serial number</p></td>
<td><p>powerpc</p></td>
<td><p>IBM,7891-73X</p></td>
<td><p>7</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/IBM_i" title="wikilink">IBM i</a> 5.3 with QSH</p></td>
<td><p>OS400</p></td>
<td><p><em>(hostname)</em></p></td>
<td><p><em>(serial number of machine)</em></p></td>
<td></td>
<td></td>
<td><p>5</p></td>
<td><p>3</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/IBM_i" title="wikilink">IBM i</a> 6.1 with QSH</p></td>
<td><p>OS400</p></td>
<td><p><em>(hostname)</em></p></td>
<td><p><em>(serial number of machine)</em></p></td>
<td></td>
<td></td>
<td><p>6</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/IBM_i" title="wikilink">IBM i</a> 7.1 with QSH</p></td>
<td><p>OS400</p></td>
<td><p><em>(hostname)</em></p></td>
<td><p><em>(serial number of machine)</em></p></td>
<td></td>
<td></td>
<td><p>7</p></td>
<td><p>1</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/Interix" title="wikilink">Interix</a> (<a href="https://ko.wikipedia.org/wiki/Windows_Services_for_UNIX" title="wikilink">Windows Services for UNIX</a>) 3.5</p></td>
<td><p>Interix</p></td>
<td></td>
<td><p>x86</p></td>
<td><p>Intel_x86_Family6_Model28_Stepping10</p></td>
<td></td>
<td><p>10.0.7063.0</p></td>
<td><p>6.1</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/IRIX.md" title="wikilink">IRIX</a></p></td>
<td><p>IRIX</p></td>
<td></td>
<td><p>IP22</p></td>
<td><p>mips</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/IRIX.md" title="wikilink">IRIX</a> 6.5.30, Origin 2000</p></td>
<td><p>IRIX64</p></td>
<td></td>
<td><p>IP30 IP35</p></td>
<td><p>mips</p></td>
<td></td>
<td><p>07202013</p></td>
<td><p>6.5</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/리눅스_민트.md" title="wikilink">리눅스 민트</a> 10 "Julia" 64-bit</p></td>
<td><p><a href="../Page/리눅스.md" title="wikilink">리눅스</a></p></td>
<td><p>GNU/Linux</p></td>
<td><p>x86_64</p></td>
<td></td>
<td></td>
<td><p>#33-Ubuntu SMP Sun Sep 19 20:32:27 UTC 2010</p></td>
<td><p>2.6.35-22-generic</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/리눅스.md" title="wikilink">리눅스</a> on <a href="../Page/제온_파이.md" title="wikilink">Xeon Phi</a></p></td>
<td><p>Linux</p></td>
<td><p>GNU/Linux</p></td>
<td><p>k1om</p></td>
<td><p>k1om</p></td>
<td><p>k1om</p></td>
<td><p>#2 SMP Fri Jun 21 13:43:31 EDT 2013</p></td>
<td><p>2.6.38.8-g2593b11</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/맥_OS_X_팬더.md" title="wikilink">맥 OS X 팬더</a> 10.3, PowerBook G4 (2004)</p></td>
<td><p><a href="../Page/다윈_(운영_체제).md" title="wikilink">Darwin</a></p></td>
<td></td>
<td><p>Power Macintosh</p></td>
<td><p>powerpc</p></td>
<td></td>
<td><p>Darwin Kernel Version 7.8.0: Wed Dec 22 14:26:17 PST 2004; root:xnu/xnu-517.11.1.obj~1/RELEASE_PPC</p></td>
<td><p>7.8.0</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/맥_OS_X_10.6" title="wikilink">맥 OS X 10.6</a> 10.6, MacBook3,1 (Late 2007)</p></td>
<td><p><a href="../Page/다윈_(운영_체제).md" title="wikilink">Darwin</a></p></td>
<td></td>
<td><p>i386</p></td>
<td><p>i386</p></td>
<td></td>
<td><p>Darwin Kernel Version 10.0.0: Fri Jul 31 22:47:34 PDT 2009; root:xnu-1456.1.25~1/RELEASE_I386</p></td>
<td><p>10.0.0</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/맥_OS_X_라이언.md" title="wikilink">맥 OS X 라이언</a> 10.7.3 build 11D50, MacbookPro7,1 (Late 2010)</p></td>
<td><p><a href="../Page/다윈_(운영_체제).md" title="wikilink">Darwin</a></p></td>
<td></td>
<td><p>x86_64</p></td>
<td><p>i386</p></td>
<td></td>
<td><p>Darwin Kernel Version 11.3.0: Thu Jan 12 18:47:41 PST 2012; root:xnu-1699.24.23~1/RELEASE_X86_64</p></td>
<td><p>11.3.0</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/OS_X_마운틴_라이언.md" title="wikilink">OS X 마운틴 라이언</a> 10.8.3 build 12D78, MacbookPro10,1 (Mid 2012)</p></td>
<td><p><a href="../Page/다윈_(운영_체제).md" title="wikilink">Darwin</a></p></td>
<td></td>
<td><p>x86_64</p></td>
<td><p>i386</p></td>
<td></td>
<td><p>Darwin Kernel Version 12.3.0: Sun Jan 6 22:37:10 PST 2013; root:xnu-2050.22.13~1/RELEASE_X86_64</p></td>
<td><p>12.3.0</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/OS_X_매버릭스.md" title="wikilink">OS X 매버릭스</a> 10.9 build 13A598, MacbookPro5,1 (Mid 2009)</p></td>
<td><p><a href="../Page/다윈_(운영_체제).md" title="wikilink">Darwin</a></p></td>
<td></td>
<td><p>x86_64</p></td>
<td><p>i386</p></td>
<td></td>
<td><p>Darwin Kernel Version 13.0.0: Thu Sep 19 22:22:27 PDT 2013; root:xnu-2422.1.72~6/RELEASE_X86_64</p></td>
<td><p>13.0.0</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/OS_X_요세미티.md" title="wikilink">OS X 요세미티</a> 10.10 build 14A298i, MacbookPro6,2 (Mid 2010)</p></td>
<td><p><a href="../Page/다윈_(운영_체제).md" title="wikilink">Darwin</a></p></td>
<td></td>
<td><p>x86_64</p></td>
<td><p>i386</p></td>
<td></td>
<td><p>Darwin Kernel Version 14.0.0: Tue Jul 15 23:56:31 PDT 2014; root:xnu-2782.1.43.0.2~1/RELEASE_X86_64</p></td>
<td><p>14.0.0</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/OS_X_엘카피탠.md" title="wikilink">OS X 엘카피탠</a> 10.11 build 15A284, MacBookPro10,1 (Mid 2012)</p></td>
<td><p><a href="../Page/다윈_(운영_체제).md" title="wikilink">Darwin</a></p></td>
<td></td>
<td><p>x86_64</p></td>
<td><p>i386</p></td>
<td></td>
<td><p>Darwin Kernel Version 15.0.0: Sat Sep 19 15:53:46 PDT 2015; root:xnu-3247.10.11~1/RELEASE_X86_64</p></td>
<td><p>15.0.0</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/MacOS_시에라.md" title="wikilink">MacOS 시에라</a> 10.12 build 16E195, MacBookPro12,1 (Early 2015)</p></td>
<td><p><a href="../Page/다윈_(운영_체제).md" title="wikilink">Darwin</a></p></td>
<td></td>
<td><p>x86_64</p></td>
<td><p>i386</p></td>
<td></td>
<td><p>Darwin Kernel Version 16.5.0: Fri Mar 3 16:52:33 PST 2017; root:xnu-3789.51.2~3/RELEASE_X86_64</p></td>
<td><p>16.5.0</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/만자로_리눅스.md" title="wikilink">만자로 리눅스</a> 0.8.11 64 bit</p></td>
<td><p><a href="../Page/리눅스.md" title="wikilink">리눅스</a></p></td>
<td><p>GNU/Linux</p></td>
<td><p>x86_64</p></td>
<td></td>
<td></td>
<td><p>#1 SMP PREEMPT Sat Nov 15 10:54:42 UTC 2014</p></td>
<td><p>3.17.3-1-MANJARO</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/MINIX_3" title="wikilink">MINIX</a> 3.1.7, x86</p></td>
<td><p>Minix</p></td>
<td></td>
<td><p>i686</p></td>
<td><p>i386</p></td>
<td></td>
<td><p>1.7</p></td>
<td><p>3</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/MinGW.md" title="wikilink">MinGW</a></p></td>
<td><p>MINGW32_NT-6.1</p></td>
<td><p>Msys</p></td>
<td><p>i686</p></td>
<td></td>
<td></td>
<td><p>2012-11-21 22:34</p></td>
<td><p>1.0.18(0.48/3/2)</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/MinGW.md" title="wikilink">MinGW</a></p></td>
<td><p>MSYS_NT-6.1</p></td>
<td><p>Msys</p></td>
<td><p>i686</p></td>
<td></td>
<td></td>
<td><p>2012-11-21 22:34</p></td>
<td><p>1.0.18(0.48/3/2)</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/NetBSD.md" title="wikilink">NetBSD</a></p></td>
<td><p>NetBSD</p></td>
<td></td>
<td><p>i386</p></td>
<td><p>i386</p></td>
<td></td>
<td><p>NetBSD 6.0.1 (GENERIC)</p></td>
<td><p>6.0.1</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/NonStop" title="wikilink">NonStop</a> H06 25</p></td>
<td><p>NONSTOP_KERNEL</p></td>
<td></td>
<td><p>NSE-T</p></td>
<td></td>
<td><p>H06</p></td>
<td><p>25</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/NonStop" title="wikilink">NonStop</a> J06 14</p></td>
<td><p>NONSTOP_KERNEL</p></td>
<td></td>
<td><p>NSE-AB</p></td>
<td></td>
<td><p>J06</p></td>
<td><p>14</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/OpenBSD.md" title="wikilink">OpenBSD</a> 5.4</p></td>
<td><p><a href="../Page/OpenBSD.md" title="wikilink">OpenBSD</a></p></td>
<td></td>
<td><p>amd64</p></td>
<td><p>amd64</p></td>
<td></td>
<td><p>GENERIC.MP#1</p></td>
<td><p>5.4</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/오픈수세.md" title="wikilink">오픈수세</a> 10.3, Core2-duo 64-bit</p></td>
<td><p><a href="../Page/리눅스.md" title="wikilink">리눅스</a></p></td>
<td><p>GNU/Linux</p></td>
<td><p>x86_64</p></td>
<td><p>x86_64</p></td>
<td><p>x86_64</p></td>
<td><p>#1 SMP 2007/09/21 22:29:00 UTC</p></td>
<td><p>2.6.22.5-31-default</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/OpenWrt.md" title="wikilink">OpenWrt</a> Barrier Breaker r40420 on TL-WR1043ND</p></td>
<td><p><a href="../Page/리눅스.md" title="wikilink">리눅스</a></p></td>
<td><p>GNU/Linux</p></td>
<td><p>mips</p></td>
<td></td>
<td><p>(-i) / invalid (-M)</p></td>
<td><p>#1 Tue Apr 8 06:30:07 UTC 2014</p></td>
<td><p>3.10.34</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/QNX.md" title="wikilink">QNX</a></p></td>
<td><p>QNX</p></td>
<td><p>-</p></td>
<td><p>x86pc</p></td>
<td><p>x86</p></td>
<td><p>-</p></td>
<td><p>2010/07/09-14:44:03EDT</p></td>
<td><p>6.5.0</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/레드햇.md" title="wikilink">레드햇</a> Linux, Fedora Core 6, AMD Turion64 mobile</p></td>
<td><p>Linux</p></td>
<td><p>GNU/Linux</p></td>
<td><p>i686</p></td>
<td><p>athlon</p></td>
<td><p>i386</p></td>
<td><p>#1 SMP Wed Jan 10 19:28:18 EST 2007</p></td>
<td><p>2.6.19-1.2895.fc6</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/SINIX" title="wikilink">ReliantUNIX</a></p></td>
<td><p>ReliantUNIX-Y</p></td>
<td></td>
<td><p>RM600</p></td>
<td><p>R4000</p></td>
<td></td>
<td><p>B2005</p></td>
<td><p>5.45</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/SINIX" title="wikilink">SINIX</a></p></td>
<td><p>SINIX-Y</p></td>
<td></td>
<td><p>RM600</p></td>
<td><p>R4000</p></td>
<td></td>
<td></td>
<td><p>5.43</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/솔라리스_(운영_체제).md" title="wikilink">Solaris</a> 8</p></td>
<td><p><a href="../Page/썬OS.md" title="wikilink">썬OS</a></p></td>
<td></td>
<td><p>sun4u</p></td>
<td><p>sparc</p></td>
<td><p>SUNW,UltraAX-i2</p></td>
<td><p>Generic_117350-50</p></td>
<td><p>5.8</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/솔라리스_(운영_체제).md" title="wikilink">Solaris</a> 9, Sun Fire 280R</p></td>
<td><p><a href="../Page/썬OS.md" title="wikilink">썬OS</a></p></td>
<td></td>
<td><p>sun4u</p></td>
<td><p>sparc</p></td>
<td><p>SUNW,Sun-Fire-280R</p></td>
<td><p>Generic_112233-08</p></td>
<td><p>5.9</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/솔라리스_(운영_체제).md" title="wikilink">Solaris</a> 10, Sun Fire V490</p></td>
<td><p><a href="../Page/썬OS.md" title="wikilink">썬OS</a></p></td>
<td></td>
<td><p>sun4u</p></td>
<td><p>sparc</p></td>
<td><p>SUNW,Sun-Fire-V490</p></td>
<td><p>Generic_142900-13</p></td>
<td><p>5.10</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/솔라리스_(운영_체제).md" title="wikilink">Solaris</a> 11.1, Sun Fire X4540</p></td>
<td><p><a href="../Page/썬OS.md" title="wikilink">썬OS</a></p></td>
<td></td>
<td><p>i86pc</p></td>
<td><p>i386</p></td>
<td><p>i86pc</p></td>
<td><p>11.1</p></td>
<td><p>5.11</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/OpenIndiana" title="wikilink">OpenIndiana</a></p></td>
<td><p><a href="../Page/썬OS.md" title="wikilink">썬OS</a></p></td>
<td></td>
<td><p>i86pc</p></td>
<td><p>i386</p></td>
<td><p>i86pc</p></td>
<td><p>oi_151a8</p></td>
<td><p>5.11</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/스마트OS.md" title="wikilink">스마트OS</a></p></td>
<td><p><a href="../Page/썬OS.md" title="wikilink">썬OS</a></p></td>
<td></td>
<td><p>i86pc</p></td>
<td><p>i386</p></td>
<td><p>i86pc</p></td>
<td><p>joyent_20150403T203811Z</p></td>
<td><p>5.11</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/OmniOS" title="wikilink">OmniOS</a></p></td>
<td><p><a href="../Page/썬OS.md" title="wikilink">썬OS</a></p></td>
<td></td>
<td><p>i86pc</p></td>
<td><p>i386</p></td>
<td><p>i86pc</p></td>
<td><p>omnios-a708424</p></td>
<td><p>5.11</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/Tru64" title="wikilink">Tru64</a></p></td>
<td><p>OSF1</p></td>
<td><p>invalid</p></td>
<td><p>alpha</p></td>
<td><p>alpha</p></td>
<td><p>invalid</p></td>
<td><p>2650</p></td>
<td><p>V5.1</p></td>
</tr>
<tr class="even">
<td><p><a href="../Page/우분투_(운영_체제).md" title="wikilink">Ubuntu</a> 11.04</p></td>
<td><p>Linux</p></td>
<td><p>GNU/Linux</p></td>
<td><p>x86_64</p></td>
<td><p>x86_64</p></td>
<td><p>x86_64</p></td>
<td><p>#46-Ubuntu SMP Tue Jun 28 15:07:17 UTC 2011</p></td>
<td><p>2.6.38-10-generic</p></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/우분투_(운영_체제).md" title="wikilink">Ubuntu</a> 12.0.4 on <a href="https://ko.wikipedia.org/wiki/PandaBoard" title="wikilink">Pandaboard ES</a></p></td>
<td><p>Linux</p></td>
<td><p>GNU/Linux</p></td>
<td><p>armv7l</p></td>
<td><p>armv7l</p></td>
<td><p>armv7l</p></td>
<td><p>#33-Ubuntu SMP PREEMPT Sat Jan 26 00:46:04 UTC 2013</p></td>
<td><p>3.2.0-1425-omap4</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/Ultrix" title="wikilink">Ultrix</a></p></td>
<td><p>ULTRIX</p></td>
<td><p>-</p></td>
<td><p>VAX</p></td>
<td><p>-</p></td>
<td><p>-</p></td>
<td><p>0</p></td>
<td><p>4.5</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/Unity_Linux" title="wikilink">Unity Linux</a></p></td>
<td><p>Linux</p></td>
<td><p>GNU/Linux</p></td>
<td><p>i686</p></td>
<td><p>Intel(R) Core(TM) i5-2520M CPU @ 2.50 GHz</p></td>
<td><p>(-i) / invalid (-M)</p></td>
<td><p>#1 SMP Fri Oct 1 16:46:58 UTC 2010</p></td>
<td><p>2.6.35.7-unity1</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/UnxUtils" title="wikilink">UnxUtils</a> 2007 32 bit (Windows Server 2008)</p></td>
<td><p>WindowsNT</p></td>
<td></td></td>
<td><p>x86</p></td>
<td></td></td>
<td></td></td>
<td><p>6</p></td>
<td><p>0</p></td>
</tr>
<tr class="odd">
<td><p>(SCO) <a href="https://ko.wikipedia.org/wiki/OpenServer" title="wikilink">OpenServer</a> 5.0.6</p></td>
<td><p>SCO_SV</p></td>
<td><p><em>(hostname)</em></p></td>
<td><p>i386</p></td>
<td><p>i386</p></td>
<td></td>
<td><p>5.0.6</p></td>
<td><p>3.2</p></td>
</tr>
<tr class="even">
<td><p>(SCO) <a href="https://ko.wikipedia.org/wiki/유닉스_시스템_V" title="wikilink">유닉스 시스템 V</a></p></td>
<td><p>SCO_SV</p></td>
<td></td>
<td><p>i386</p></td>
<td><p>i386</p></td>
<td></td>
<td><p>6.0.0</p></td>
<td><p>5</p></td>
</tr>
<tr class="odd">
<td><p>(SCO) <a href="../Page/유닉스웨어.md" title="wikilink">유닉스웨어</a> 7.1.4</p></td>
<td><p>UnixWare</p></td>
<td></td>
<td><p>i386</p></td>
<td><p>x86at</p></td>
<td><p>-i hardware serial/license number, .e.g. 1AB000123 or NUL000000; -M is 유효하지 않은 옵션</p></td>
<td><p>7.1.4</p></td>
<td><p>5</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/UWIN" title="wikilink">UWIN</a> (64 bit Windows 7), Intel Core i5</p></td>
<td><p>UWIN-W7</p></td>
<td><p>UWIN</p></td>
<td><p>i686-64</p></td>
<td><p>x64</p></td>
<td><p>64/64</p></td>
<td><p>2012-06-26</p></td>
<td><p>5.0/6.1</p></td>
</tr>
<tr class="odd">
<td><p>SYS$UNIX:SH on <a href="../Page/OpenVMS.md" title="wikilink">OpenVMS</a> on VAX emulator</p></td>
<td><p>IS/WB</p></td>
<td></td>
<td><p>vax-6340</p></td>
<td></td>
<td></td>
<td><p>std</p></td>
<td><p>5.0</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/Z/OS" title="wikilink">Z/OS</a> <a href="https://ko.wikipedia.org/wiki/UNIX_System_Services" title="wikilink">USS</a></p></td>
<td><p>OS/390</p></td>
<td></td>
<td><p>2097</p></td>
<td></td>
<td><p>-i/-M: unknown option; -I: z/OS</p></td>
<td><p>03</p></td>
<td><p>22.00</p></td>
</tr>
</tbody>
</table>

## 같이 보기

  - [유닉스 명령어 목록](../Page/유닉스_명령어_목록.md "wikilink")
  - [ver (명령어)](https://ko.wikipedia.org/wiki/ver_\(명령어\) "wikilink")

## 각주

## 외부 링크

  -
  -
  -
  -
  -
[분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink")

1.  [uname](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/uname.html). The Open Group Base Specifications Issue 7/IEEE Std 1003.1, 2013 Edition. Specifies the command.
2.  [uname](http://pubs.opengroup.org/onlinepubs/9699919799/functions/uname.html). The Open Group Base Specifications Issue 7/IEEE Std 1003.1, 2013 Edition. Specifies the function/system call.
3.  These are merely meant to broadly represent common systems; actual output may vary depending on hardware type, OS version, and which software patches have been installed.