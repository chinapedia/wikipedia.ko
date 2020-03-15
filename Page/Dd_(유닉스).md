> This article is converted from Wikipedia: [Dd \(\)](https://ko.wikipedia.org/wiki/Dd_\(\)).


**dd**는 파일을 변환하고 복사하는 것이 주 목적인 [유닉스](https://ko.wikipedia.org/wiki/유닉스 "wikilink") 및 [유닉스 계열](https://ko.wikipedia.org/wiki/유닉스_계열 "wikilink") [운영 체제용](https://ko.wikipedia.org/wiki/운영_체제 "wikilink") 명령 줄 유틸리티이다.\[1\]

유닉스에서 하드웨어와 특수 [장치 파일용](https://ko.wikipedia.org/wiki/장치_파일 "wikilink") 장치 드라이버는 파일 시스템에서 마치 일반 파일처럼 나타난다. dd는 기능이 개별 드라이버에서 구현되어 있는 경우 이러한 파일들을 읽거나 기록하는 것이 가능하다. 그러므로 dd는 하드 드라이브의 [부팅 섹터를](https://ko.wikipedia.org/wiki/부팅_섹터 "wikilink") 백업하는 등의 일과 고정된 크기의 랜덤 데이터를 취득하기 위해 사용할 수 있다. dd 프로그램은 복사 시 데이터에 변환을 수행할 수도 있는데, 여기에는 [바이트 순서](https://ko.wikipedia.org/wiki/엔디언 "wikilink") 스와핑, [ASCII](https://ko.wikipedia.org/wiki/ASCII "wikilink")↔[EBCDIC](https://ko.wikipedia.org/wiki/EBCDIC "wikilink") 텍스트 인코딩 변환을 포함할 수 있다.\[2\]

dd라는 이름은 [IBM](https://ko.wikipedia.org/wiki/IBM "wikilink")의 [작업 제어 언어](https://ko.wikipedia.org/wiki/작업_제어_언어 "wikilink")(JCL)에서 발견되는 [DD 문과](https://ko.wikipedia.org/wiki/작업_제어_언어#인스트림_입력 "wikilink") 관련되며\[3\]\[4\] 여기에서 DD는 "Data Description"을 가리킨다.\[5\] 이 명령의 문법은 다른 유닉스 명령보다 JCL 문과 유사하다.\[6\]

원래 [ASCII](https://ko.wikipedia.org/wiki/ASCII "wikilink")와 [EBCDIC](https://ko.wikipedia.org/wiki/EBCDIC "wikilink") 간의 변환을 위해 고안된 dd는 [버전 5 유닉스에](https://ko.wikipedia.org/wiki/버전_5_유닉스 "wikilink") 처음 등장하였다.\[7\] dd 명령어는 [SUS의](https://ko.wikipedia.org/wiki/단일_유닉스_규격 "wikilink") 일부인 [IEEE](https://ko.wikipedia.org/wiki/IEEE "wikilink") 표준 1003.1-2008에 규정되어 있다.

## 용도

dd 명령은 다양한 목적을 위해 쓰일 수 있다.

### 데이터 전송

<table>
<caption>dd의 데이터 전송 형태</caption>
<tbody>
<tr class="odd">
<td><div class="sourceCode" id="cb1"><pre class="sourceCode bash"><code class="sourceCode bash"><span id="cb1-1"><a href="#cb1-1"></a><span class="fu">dd</span> if=/dev/sr0 of=myCD.iso bs=2048 conv=noerror,sync</span></code></pre></div></td>
<td><p>CD-ROM으로부터 <a href="https://ko.wikipedia.org/wiki/ISO_이미지" title="wikilink">ISO</a> <a href="https://ko.wikipedia.org/wiki/디스크_이미지" title="wikilink">디스크 이미지를</a> 생성한다. 일부의 경우 작성된 ISO 이미지는 CD-ROM 기록에 사용되는 것과 동일하지 않을 수도 있다.<ref>{{서적 인용</p></td>
<td><p>url = <a href="http://books.google.com/books?id=ZBKsMYz1Q4kC&amp;pg=PA174&amp;lpg=PA174&amp;dq=iso+image+2048+block&amp;source=bl&amp;ots=fKnHYFhTYV&amp;sig=yxcSn_WWaIm7uYrXyPaL4bW01Js&amp;hl=en&amp;sa=X&amp;ei=zXD5U7O_CcbdaMbWgegE&amp;redir_esc=y#v=onepage&amp;q&amp;f=false">http://books.google.com/books?id=ZBKsMYz1Q4kC&amp;pg=PA174&amp;lpg=PA174&amp;dq=iso+image+2048+block&amp;source=bl&amp;ots=fKnHYFhTYV&amp;sig=yxcSn_WWaIm7uYrXyPaL4bW01Js&amp;hl=en&amp;sa=X&amp;ei=zXD5U7O_CcbdaMbWgegE&amp;redir_esc=y#v=onepage&amp;q&amp;f=false</a></p></td>
<td><p>제목 = The Linux Command Line, A Complete Introduction</p></td>
<td><p>chapter = 15. Storage Media</p></td>
<td><p>year = 2012 | accessdate = 2014-08-24</p></td>
<td><p>author = William E. Shotts, Jr. | publisher = <a href="https://ko.wikipedia.org/wiki/No_Starch_Press" title="wikilink">No Starch Press</a></p></td>
<td><p>page = 174 }}</ref></p></td>
</tr>
<tr class="even">
<td><div class="sourceCode" id="cb2"><pre class="sourceCode bash"><code class="sourceCode bash"><span id="cb2-1"><a href="#cb2-1"></a><span class="fu">dd</span> if=system.img of=/dev/sdc bs=4096 conv=noerror</span></code></pre></div></td>
<td><p>이전에 만든 이미지로부터 하드 디스크 드라이브(또는 SD 카드)를 복원한다.</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><div class="sourceCode" id="cb3"><pre class="sourceCode bash"><code class="sourceCode bash"><span id="cb3-1"><a href="#cb3-1"></a><span class="fu">dd</span> if=/dev/sda2 of=/dev/sdb2 bs=4096 conv=noerror</span></code></pre></div></td>
<td><p>하나의 <a href="https://ko.wikipedia.org/wiki/하드_디스크_파티션" title="wikilink">파티션을</a> 다른 파티션으로 <a href="https://ko.wikipedia.org/wiki/디스크_복제" title="wikilink">복제한다</a>.</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><div class="sourceCode" id="cb4"><pre class="sourceCode bash"><code class="sourceCode bash"><span id="cb4-1"><a href="#cb4-1"></a><span class="fu">dd</span> if=/dev/ad0 of=/dev/ad1 bs=1M conv=noerror</span></code></pre></div></td>
<td><p>하드 디스크 드라이브 "ad0"을 "ad1"으로 복제한다.</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

### 마스터 부트 레코드 백업 및 복원

마스터 부트 레코드를 복구할 수 있다. 복구 파일로부터 전송받거나 복구 파일로 전송할 수 있다.

플로피 드라이브의 처음 두 개의 섹터를 복제:

``` bash
dd if=/dev/fd0 of=MBRboot.img bs=512 count=2
```

완전한 x86 [마스터 부트 레코드의](https://ko.wikipedia.org/wiki/마스터_부트_레코드 "wikilink") 이미지 만들기 (MS-DOS [파티션](https://ko.wikipedia.org/wiki/파티션 "wikilink"), MBR 매직 바이트 포함):

``` bash
dd if=/dev/sda of=MBR.img bs=512 count=1
```

[마스터 부트 레코드의](https://ko.wikipedia.org/wiki/마스터_부트_레코드 "wikilink") 부트 코드만의 이미지 만들기 ([파티션 테이블](https://ko.wikipedia.org/wiki/파티션_테이블 "wikilink") 없이, 또 부팅 시 필요한 매직 바이트 없이):

``` bash
dd if=/dev/sda of=MBR_boot.img bs=446 count=1
```

### 데이터 수정

dd는 특정 자리의 데이터를 수정할 수 있다. 이를테면 아래의 명령을 통해 파일의 최초 512바이트를 널(null) 바이트로 채울 수 있다:

``` bash
dd if=/dev/zero of=path/to/file bs=512 count=1 conv=notrunc
```

notrunc 변환 옵션은 출력 파일을 잘라내지 않는다는 것을 뜻한다. 즉, 출력 파일이 이미 존재하면 지정된 바이트를 대체하되 출력 파일의 나머지 부분만은 남겨둔다. 이 옵션을 사용하지 않으면 dd는 512바이트 길이의 출력 파일을 생성한다.

디스크 이미지 파일로서 특정 디스크 파티션을 다른 파티션에 복제하려면 다음과 같이 실행한다:

``` bash
dd if=/dev/sdb2 of=partition.image bs=4096 conv=noerror
```

### 디스크 완전 소거

보안 목적으로 이따금은 버림 받은 장치의 [디스크 완전 소거를](https://ko.wikipedia.org/wiki/데이터_완전_소거 "wikilink") 할 필요가 있다.

dd를 이용하여 디스크를 0으로 채워 소거하는 방법은 아래와 같다:

``` bash
dd if=/dev/zero of=/dev/sda bs=4k
```

다른 방법으로 랜덤 데이터를 채워 소거할 수도 있다:

``` bash
dd if=/dev/urandom of=/dev/sda bs=4k
```

### 데이터 복구

파일, 드라이브, 파티션의 [데이터 복구](https://ko.wikipedia.org/wiki/데이터_복구 "wikilink") 및 복원에 대한 [오픈 소스 소프트웨어의](https://ko.wikipedia.org/wiki/오픈_소스_소프트웨어 "wikilink") 초기 역사에는 GNU dd가 포함되어 있으며, 저작권 고지는 1985년에 시작된다.\[8\] dd 프로세스 당 하나의 블록 크기를 가지며 특정한 형태의 dd를 실행 중인 사용자의 상호작용 세션까지만 한정하여 복구 알고리즘을 제공하였다. 그 뒤 dd_rescue\[9\]라는 C 프로그램이 1999년 10월에 작성되어 해당 알고리즘 안에 두 개의 블록 크기를 가질 수 있었다. 그러나 2003년 dd_rescue의 데이터 복구 알고리즘을 강화한 셸 스크립트 dd_rhelp의 저자는 2004년에 처음 출시된 dd와는 무관한 데이터 복구 프로그램인 GNU [ddrescue](https://ko.wikipedia.org/wiki/ddrescue "wikilink")\[10\]\[11\]의 사용을 권장하였다.

더 새로운 GNU 프로그램을 더 오래된 스크립트와 구별하기 위해 GNU의 ddrescue와는 다른 이름이 쓰이기도 하는데 여기에는 addrescue (freecode.com, freshmeat.net에서의 이름), gddrescue ([데비안](https://ko.wikipedia.org/wiki/데비안 "wikilink") 패키지 이름), gnu_ddrescue([오픈수세](https://ko.wikipedia.org/wiki/오픈수세 "wikilink") 패키지 이름)가 포함된다. savehd7이라는 다른 오픈 소스 프로그램은 복잡한 알고리즘을 사용하지만 사용을 위해 자체 프로그래밍 언어 인터프리터의 설치가 필요하다.

### 드라이브 성능 벤치마크

드라이브 벤치마크를 테스트하고, 1024바이트 블록에 대한 순차 시스템 읽기/쓰기 성능을 분석하려면 다음과 같이 진행한다:

``` bash
dd if=/dev/zero bs=1024 count=1000000 of=file_1GB
dd if=file_1GB of=/dev/null bs=1024
```

### 랜덤 데이터로 파일 생성

커널 랜덤 드라이버를 이용하여 랜덤 데이터로 이루어진 100바이트의 파일을 채우려면 다음과 같이 진행한다:

``` bash
dd if=/dev/urandom of=myrandom bs=100 count=1
```

### 파일을 대문자로 변환

파일을 대문자로 변경하려면 다음과 같이 진행한다:

``` bash
dd if=filename of=filename1 conv=ucase
```

## 같이 보기

  - [백업](https://ko.wikipedia.org/wiki/백업 "wikilink")
  - [디스크 복제](https://ko.wikipedia.org/wiki/디스크_복제 "wikilink")
  - [유닉스 명령어 목록](../Page/유닉스_명령어_목록.md "wikilink")

## 각주

<references />

## 외부 링크

  -
  - [dd](http://www.gnu.org/software/coreutils/manual/html_node/dd-invocation.html): manual page from the [GNU Core Utilities](../Page/GNU_코어_유틸리티.md "wikilink").

  - [dd for Windows](http://www.chrysocome.net/dd).

[분류:디스크 복제](https://ko.wikipedia.org/wiki/분류:디스크_복제 "wikilink")

1.
2.
3.
4.
5.  See this old discussion
6.
7.
8.
9.
10.
11.