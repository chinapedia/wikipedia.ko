> This article is converted from Wikipedia: [BeOS](https://ko.wikipedia.org/wiki/BeOS).


**BeOS**는 [Be 사에서](https://ko.wikipedia.org/wiki/Be_사 "wikilink") 개발한 개인용 컴퓨터용 [운영 체제이다](../Page/운영_체제.md "wikilink").

## 역사

[1991년](../Page/1991년.md "wikilink")에 [BeBox](https://ko.wikipedia.org/wiki/BeBox "wikilink")라는 [하드웨어](https://ko.wikipedia.org/wiki/하드웨어 "wikilink")에서 동작하도록 만들어졌다. 당시의 운영 체제와 달리, 처음부터 [GUI에](../Page/그래픽_사용자_인터페이스.md "wikilink") 기반한 운영 체제로 설계되었다. 디지털 미디어 작업을 위해서 다중 프로세서 지원 및 다중 스레드, 선점형 멀티태스킹 및 64비트 저널링 파일 시스템을 지원했다. 개발의 편의를 위해 API는 [C++](https://ko.wikipedia.org/wiki/C++ "wikilink")로 만들었다. [POSIX](../Page/POSIX.md "wikilink") 호환성을 가지고 있고 배시 셸을 통한 명령행 접근도 가능했다. 이는 비-유닉스 기반 운영 체제에서는 찾아보기 힘들다.

[AT\&T 호빗](https://ko.wikipedia.org/wiki/AT&T_호빗 "wikilink") 기반 하드웨어에서 동작하도록 설계되었지만 추후 [PowerPC](https://ko.wikipedia.org/wiki/PowerPC "wikilink") 프로세서에서도 실행할 수 있도록 수정되었다. Be 사는 애플 사가 맥 오에스의 대체품으로 자신들의 운영 체제를 지원해 줄 것을 기대했지만, 애플은 [넥스트스텝](https://ko.wikipedia.org/wiki/넥스트스텝 "wikilink")이 더 나은 선택이라고 판단하고 넥스트 사를 1996년에 인수해서 애플의 공동 창업자 [스티브 잡스를](../Page/스티브_잡스.md "wikilink") 다시 영입했다. Be 사에 치명적인 타격이겠지만 애플은 [PowerPC G3의](https://ko.wikipedia.org/wiki/PowerPC_G3 "wikilink") 내부 구조를 공개하지 않아서 BeOS가 애플 하드웨어에서 동작하지 않도록 만들었다.

애플의 이러한 움직임 때문에 Be 사는 [x86](https://ko.wikipedia.org/wiki/x86 "wikilink") 플랫폼으로 이식하기 시작했다. 1990년대 말에 BeOS는 인기를 끌었지만 회사 자체가 안정화되지는 못했다. 이것 때문에 Be 사는 [BeOS R5를](https://ko.wikipedia.org/wiki/BeOS_R5 "wikilink") 내놓았다. 이것은 BeOS의 기능을 잘라내었지만 무료로 사용할 수 있는 버전이었고 BeOS Personal Edition으로 알려졌다. BeOS PE는 [마이크로소프트 윈도나](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") [리눅스](../Page/리눅스.md "wikilink")에서 바로 실행될 수 있었고, 최종 사용자들은 더 쉽게 다가갈 수 있었다.

Be 사는 BeOS의 또 다른 버전인 BeOS for Internet Appliances ([BeIA](../Page/BeIA.md "wikilink"))를 내놓았다. 하지만 BeOS PE와 BEIA는 오래 가지 못했고, 2001년 Be 사가 팜 사에 인수되기에 이르렀다. 하지만 팜 사에 인수되기 전에 개발되고 있었고 Beos Network Environment 네트워크 스택을 내장했던 BeOS R5.1 "Dano" 버전이 회사가 인수된 후 유출되었다.

Be 사가 망했지만 BeOS를 쓰는 사람은 아직도 있다. BeOS 커뮤니티는 아직도 자유 소프트웨어를 만들고 패치도 만들고 있으며, 드라이버 및 기타 업데이트를 제작하고 있다. BeOS에 관계된 소프트웨어는 [BeBits](https://ko.wikipedia.org/wiki/BeBits "wikilink") \[[http://www.bebits.com\]에서](http://www.bebits.com%5D에서) 찾을 수 있다.

BeOS 사용자 인터페이스는 테마를 적용시킬 수 없다. 노란색 BeOS 기본 테마 및 창 위의 가변 길이 탭 및 회색 인터페이스 위젯만 사용해야 했다. 이 인터페이스는 1995년까지도 바뀌지 않았지만 유출된 Dano 릴리즈에서 바뀌었다. 운영 체제 내부의 이스터에그를 사용하면 제목 표시줄과 외향을 바꿀 수 있다. 하지만 다른 인터페이스 위젯을 바꿀 수 없다.

순수 BeOS R5 인터페이스는 완벽하게 다른 운영 체제로 포팅되었다. 대표적인 사례로는 TriangleOS라는 운영 체제에서 BeOS테마는 주 UI로 사용하며, [그놈](../Page/그놈.md "wikilink")에서는 설치시 제공되는 몇 가지 테마중의 하나로 제공된다.

### 버전 역사

<table>
<thead>
<tr class="header">
<th><p>릴리스</p></th>
<th><p>날짜</p></th>
<th><p>하드웨어</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>DR1–DR5</p></td>
<td><p>1995년 10월</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/AT&amp;T_호빗" title="wikilink">AT&amp;T 호빗</a></p></td>
</tr>
<tr class="even">
<td><p>DR6 (개발자 릴리스)</p></td>
<td><p>1996년 1월</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/PowerPC" title="wikilink">PowerPC</a></p></td>
</tr>
<tr class="odd">
<td><p>DR7</p></td>
<td><p>1996년 4월</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>DR8</p></td>
<td><p>1996년 9월</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>어드밴스트 액세스 프리뷰 릴리스<br />
Advanced Access Preview Release</p></td>
<td><p>1997년 5월</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>PR1 (프리뷰 릴리스)</p></td>
<td><p>1997년 6월</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>PR2</p></td>
<td><p>1997년 10월</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>R3</p></td>
<td><p>1998년 3월</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/PowerPC" title="wikilink">PowerPC</a>, <a href="https://ko.wikipedia.org/wiki/인텔_x86" title="wikilink">인텔 x86</a></p></td>
</tr>
<tr class="odd">
<td><p>R3.1</p></td>
<td><p>1998년 6월</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>R3.2</p></td>
<td><p>1998년 7월</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>R4</p></td>
<td><p>1998년 11월 4일</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>R4.5 ("Genki")</p></td>
<td><p>1999년 6월</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/BeOS_R5" title="wikilink">R5 PE/Pro ("Maui")</a></p></td>
<td><p>2000년 3월</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/Dano" title="wikilink">R5.1 ("Dano")</a></p></td>
<td><p>2001년 11월</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/인텔_x86" title="wikilink">인텔 x86</a></p></td>
</tr>
</tbody>
</table>

## BeOS를 다시 만드려는 프로젝트

BeOS는 작지만 활발한 커뮤니티의 지원을 받고 있었다. 하지만 Be 사는 그 운영 체제에 대한 지원을 해 줄 수 없었다. 2002년에 서로 다른 방법으로 BeOS를 만들려는 많은 프로젝트가 생겼다. 운영 체제를 커뮤니티에서 훔쳐 가는 것을 막고 자원 봉사자 프로그래머를 끌기 위해서 모든 프로젝트는 자유 소프트웨어이며 공개 소프트웨어이다. 원본 BeOS의 구조를 유지하면서 새로운 운영 체제를 유지하기 위해서 호환성 테스트가 이루어졌다. BeOS의 거의 모든 부분을 자유 소프트웨어로 대체할 수 있다.

  - [하이쿠 (운영 체제)](https://ko.wikipedia.org/wiki/하이쿠_\(운영_체제\) "wikilink")
  - [Blue Eyed OS](https://ko.wikipedia.org/wiki/Blue_Eyed_OS "wikilink") (개발이 중지됨)
  - [Cosmoe](https://ko.wikipedia.org/wiki/Cosmoe "wikilink")

## BeOS를 계승하려는 프로젝트

  - [YellowTAB](https://ko.wikipedia.org/wiki/YellowTAB "wikilink") 사는 미완성인 BeOS R5.1의 코드를 사용할 수 있는 권리가 있다. 하지만 BeOS 상표를 사용할 권리는 없기 때문에 [ZETA라는](https://ko.wikipedia.org/wiki/YellowTAB_ZETA "wikilink") 이름으로 배포하고 있다. YellowTAB 사는 그들과 BeOS 코드와의 법적인 관계를 아직 정리하지 않았기 때문에 Be 커뮤니티에서 많은 논쟁을 유발하였다.

## 외부 링크

  - [대한민국 BeOS 사용자 그룹(사이트 사라짐)](https://web.archive.org/web/20051122205241/http://www.bekrage.net/)
  - [BeOS News](http://www.beosnews.com)

[BeOS](https://ko.wikipedia.org/wiki/분류:BeOS "wikilink") [분류:X86 운영 체제](https://ko.wikipedia.org/wiki/분류:X86_운영_체제 "wikilink") [분류:파워PC 운영 체제](https://ko.wikipedia.org/wiki/분류:파워PC_운영_체제 "wikilink")