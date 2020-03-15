> This article is converted from Wikipedia: [Bochs](https://ko.wikipedia.org/wiki/Bochs).


**박스**(Bochs)는 대부분이 [C++](https://ko.wikipedia.org/wiki/C++ "wikilink")로 작성되고 [GNU LGPL의](https://ko.wikipedia.org/wiki/GNU_LGPL "wikilink") [자유 소프트웨어로](https://ko.wikipedia.org/wiki/자유_소프트웨어 "wikilink") 배포된 포터블 [IA-32](https://ko.wikipedia.org/wiki/IA-32 "wikilink")와 [X86-64](../Page/X86-64.md "wikilink") [IBM PC 호환](https://ko.wikipedia.org/wiki/IBM_PC_호환 "wikilink") [에뮬레이터](../Page/에뮬레이터.md "wikilink")이자 [디버거](../Page/디버거.md "wikilink")이다. 프로세서([보호 모드](../Page/보호_모드.md "wikilink") 포함), 메모리, 디스크, 디스플레이, [이더넷](https://ko.wikipedia.org/wiki/이더넷 "wikilink"), [바이오스](https://ko.wikipedia.org/wiki/바이오스 "wikilink"), [PC의](https://ko.wikipedia.org/wiki/IBM_PC_호환_기종 "wikilink") 일반적인 하드웨어 주변기기를 에뮬레이트하는 것을 지원한다.

수많은 게스트 [운영 체제는](https://ko.wikipedia.org/wiki/운영_체제 "wikilink") [도스](https://ko.wikipedia.org/wiki/도스 "wikilink"), 여러 버전의 [마이크로소프트 윈도우](https://ko.wikipedia.org/wiki/마이크로소프트_윈도우 "wikilink"), [BSD](https://ko.wikipedia.org/wiki/BSD "wikilink"), [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink"), [Xenix](https://ko.wikipedia.org/wiki/Xenix "wikilink"), [랩소디](../Page/랩소디_\(운영_체제\).md "wikilink")(맥 OS X의 전신)을 포함하여 에뮬레이터를 사용하여 실행할 수 있다. Bochs는 [안드로이드](https://ko.wikipedia.org/wiki/안드로이드_\(운영_체제\) "wikilink"), [iOS](https://ko.wikipedia.org/wiki/iOS "wikilink"), [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink"), [macOS](https://ko.wikipedia.org/wiki/macOS "wikilink"), [플레이스테이션 2](https://ko.wikipedia.org/wiki/플레이스테이션_2 "wikilink"), [윈도우](https://ko.wikipedia.org/wiki/마이크로소프트_윈도우 "wikilink"), [윈도우 모바일을](../Page/윈도우_모바일.md "wikilink") 포함한 수많은 호스트 운영 체제에서 구동할 수 있다.

Bochs는 운영 체제 개발에 대부분 사용되며(에뮬레이트되는 운영 체제가 충돌이 발생하면 호스트 운영 체제의 충돌로 이어지지 않으므로 에뮬레이트되는 운영 체제는 [디버깅](https://ko.wikipedia.org/wiki/디버깅 "wikilink")이 가능하다), 그 외에도 이미 실행 중인 호스트 운영 체제 안에서 다른 게스트 운영 체제를 구동하기 위해 사용할 수도 있다. 또, 컴퓨터 속도가 너무 빠르다는 이유로, 아니면 호환되지 않는 컴퓨터라는 이유로 구동이 되지 않는 PC 게임과 같은 오래된 소프트웨어를 구동하기 위해 사용할 수 있다.

## 역사

Bochs는 사용을 위해 [US$](../Page/미국_달러.md "wikilink")25의 가격으로 상용 라이선스의 프로그램으로 시작되었다. 사용자가 Bochs를 다른 소프트웨어와 연동해야 하는 경우 특별한 라이선스를 협상할 필요가 있다. 이 부분은 Mandrakesoft(현재의 [맨드리바](../Page/맨드리바.md "wikilink"))가 선임 개발자 케빈 로튼(Kevin Lawton)으로부터 Bochs를 사들인 2000년 3월 22일에 변경되었으며 [GNU LGPL로](https://ko.wikipedia.org/wiki/GNU_LGPL "wikilink") [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink")용으로 출시되었다.\[1\]

## 이용

Bochs는 하드 드라이브, CD 드라이브, 플로피 드라이브를 포함하여 PC 운영 체제에 필요한 하드웨어를 에뮬레이트한다. 어떠한 CPU [가상화](https://ko.wikipedia.org/wiki/하드웨어_지원_가상화 "wikilink") 기능을 활용하지 않으므로 대부분의 가상화 보다 더 느린 편이다. 게스트 운영 체제를 하드웨어와 완전하게 분리시킴으로써 추가적인 보안을 제공한다. Bochs는 또한 광활한 디버깅 기능을 제공한다. 코드 테스트를 위해 시스템 재시작을 할 필요가 줄어드므로 운영 체제 개발에 널리 사용된다.

"Graphical Debugger Interface for the Bochs PC Emulator"로 기술되는 BFE는 Bochs PC 에뮬레이터 내의 디버거를 위한 그래픽 인터페이스로서, 명령 단위, 레지스터 레벨로 단계별로 소프트웨어를 디버그할 수 있게 해주며 이는 마치 볼랜드의 [터보 디버거와](https://ko.wikipedia.org/wiki/볼랜드_터보_디버거 "wikilink") 유사하다.\[2\]

## 에뮬레이트하는 하드웨어

<table>
<thead>
<tr class="header">
<th><p>유형</p></th>
<th><p>장치</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="../Page/그래픽_카드.md" title="wikilink">그래픽 카드</a></p></td>
<td><p>시러스 로직 CL-GD5430 <a href="../Page/ISA_버스.md" title="wikilink">ISA</a></p></td>
</tr>
<tr class="even">
<td><p>시러스 로직 <a href="../Page/시러스_로직.md" title="wikilink">CL-GD5446</a> <a href="../Page/PCI_버스.md" title="wikilink">PCI</a></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/사운드_카드.md" title="wikilink">사운드 카드</a></p></td>
<td><p><a href="../Page/사운드_블라스터_16.md" title="wikilink">사운드 블라스터 16</a> 카드 (ISA, <a href="https://ko.wikipedia.org/wiki/플러그_앤드_플레이" title="wikilink">플러그 앤드 플레이</a> 지원 안 함)</p></td>
</tr>
<tr class="even">
<td></td>
<td><p><a href="https://ko.wikipedia.org/wiki/NE2000" title="wikilink">NE2000</a> <a href="https://ko.wikipedia.org/wiki/이더넷" title="wikilink">이더넷</a>[3]</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/칩셋" title="wikilink">칩셋</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/인텔_440FX" title="wikilink">인텔 440FX</a> PCI. 호스트 투 PCI 브리지 (PMC/DBX), PCI 투 ISA 브리지, PCI IDE 컨트롤러 (PIIX3) 이용 가능. PCI 카드의 경우 5개의 PCI 슬롯이 있음.</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/USB" title="wikilink">USB</a></p></td>
<td><p>루트 허브 및 장치 마우스, 태블릿, 키패드, 디스크.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/대칭형_다중_처리" title="wikilink">SMP</a></p></td>
<td><p>최대 8개의 CPU 시뮬레이트 가능.</p></td>
</tr>
<tr class="even">
<td><p>강화된 BIOS</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/El_Torito" title="wikilink">ElTorito</a>, <a href="https://ko.wikipedia.org/wiki/INT_13" title="wikilink">EDD</a> v3.0, 기본 <a href="https://ko.wikipedia.org/wiki/고급_전원_관리" title="wikilink">APM</a>, PCIBIOS 기능, <a href="../Page/PCI_버스.md" title="wikilink">PCI</a> 인터럽트 루팅 테이블. <a href="../Page/ACPI.md" title="wikilink">ACPI</a>, <a href="https://ko.wikipedia.org/wiki/시스템_관리_모드" title="wikilink">SMM</a>, <a href="https://ko.wikipedia.org/wiki/대칭형_다중_처리" title="wikilink">SMP를</a> 위한 32비트 초기화.</p></td>
</tr>
</tbody>
</table>

## 플레이스테이션 2 포트

PS2 버전이 KarasQ에 의해 포팅되었다. (psx-scene 포럼)

## 각주

## 외부 링크

  -
[분류:에뮬레이션 소프트웨어](https://ko.wikipedia.org/wiki/분류:에뮬레이션_소프트웨어 "wikilink") [분류:C++로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C++로_작성된_자유_소프트웨어 "wikilink") [분류:자유 에뮬레이션 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_에뮬레이션_소프트웨어 "wikilink") [분류:x86 에뮬레이터](https://ko.wikipedia.org/wiki/분류:x86_에뮬레이터 "wikilink")

1.
2.
3.   090427 bochs.sourceforge.net