> This article is converted from Wikipedia: [NVM ](https://ko.wikipedia.org/wiki/NVM_).


**NVM 익스프레스**(NVM Express, NVMe) 또는 **비휘발성 메모리 호스트 컨트롤러 인터페이스 사양**(Non-Volatile Memory Host Controller Interface Specification, NVMHCI)은 [PCI 익스프레스](../Page/PCI_익스프레스.md "wikilink")(PCIe) 버스에 부착된 비휘발성 기억 매체 접근을 위한 논리 장치 인터페이스 사양이다. "NVM"은 "비휘발성 메모리"(non-volatile memory)를 뜻하며, 보통 [솔리드 스테이트 드라이브](../Page/솔리드_스테이트_드라이브.md "wikilink")(SSD) 형태로 출시되는 플래시 메모리를 가리킨다.

설계 상, NVM 익스프레스는 현대의 SSD에서 볼 수 있는 여러 수준의 병렬화를 허용하며 이로써 호스트 하드웨어와 소프트웨어에 의해 완전히 이용될 수 있다. 그 결과, NVM 익스프레스는 [입출력](../Page/입출력.md "wikilink") 부하를 줄이고 길이가 긴 다중 명령 큐, 감소된 레이턴시를 포함하여 이전 논리 장치 인터페이스에 비해 다양한 성능 개선을 이루게 된다.

NVM 익스프레스 장치는 표준 크기의 PCI 익스프레스 [확장 카드와](../Page/확장_카드.md "wikilink")\[1\], U.2 단자(이전 이름: SFF-8639)를 통해 4 레인의 PCI 익스프레스 인터페이스를 제공하는 2.5인치 폼 팩터 장치로 존재한다.\[2\]\[3\] 내부적으로 마운트된 컴퓨터 확장 카드를 위한 [SATA 익스프레스](../Page/SATA_익스프레스.md "wikilink") 스토리지 장치와 M.2 사양 또한 NVM 익스프레스를 논리 장치 인터페이스로서 지원한다.\[4\]\[5\]

## 역사

비휘발성 메모리를 접근하는 새로운 표준에 대한 상세 내용은 [인텔 개발자 포럼](../Page/인텔_개발자_포럼.md "wikilink") 2007에서 처음 등장하였고, 이 때 NVMHCI가 메모리 (플래시) 칩 사이드의 ONFI(Open NAND Flash Interface Working Group)가 포함된 제안 형태의 아키텍처 디자인의 호스트 사이드 프로토콜로 모습을 드러냈다.\[6\] 인텔이 주도한 NVMHCI 워킹 그룹은 그 해에 창설되었다. NVMHCI 1.0 사양은 2008년 4월 완료되었고 인텔의 웹 사이트에 공개되었다.\[7\]\[8\]\[9\]

NVMe에 대한 기술적인 작업은 2009년 후반에 시작되었다.\[10\] NVMe 사양은 NVM 익스프레스 워크그룹에 의해 개발되었고, 90곳이 넘는 회사로 구성되었다. [인텔](../Page/인텔.md "wikilink")의 Amber Huffman는 그룹의 의장이었다. 버전 1.0의 사양은 2011년 3월 1일에 공개되었고\[11\], 버전 1.1의 사양은 2012년 10월 11일에 공개되었다.\[12\] 버전 1.1에 추가된 주요 기능으로는 멀티패스 입출력 (이름공간 공유 포함)과 임의 길이 [scatter-gather 입출력이다](https://ko.wikipedia.org/wiki/벡터_입출력 "wikilink"). 차기 버전은 이름공간 관리가 상당히 개선될 것이다. 기능에 초점을 두었기 때문에 NVMe 1.1은 처음에 "엔터프라이즈 NVMHCI"로 불렸다.\[13\] 버전 1.0e의 기반 NVMe 사양의 업데이트는 2013년 1월에 공개되었다.\[14\] 2011년 6월에 7개 회사가 주도하는 프로모터 그룹은 형성되었다.

최초로 상용화된 NVMe 칩셋은 2012년 8월 [Integrated Device Technology](https://ko.wikipedia.org/wiki/Integrated_Device_Technology "wikilink")(IDT, 89HF16P04AG3 및 89HF32P08AG)가 출시하였다.\[15\]\[16\] 최초의 NVMe 드라이브인 삼성의 XS1715 엔터프라이즈 드라이브는 2013년 7월에 발표되었고, 삼성에 따르면 이 드라이브는 과거 기업에 제공되었던 것 보다 6배 더 빠른 3 GB/초의 읽기 속도를 지원하였다.\[17\] 2013년 11월에 출시된 LSI [샌드포스](https://ko.wikipedia.org/wiki/샌드포스 "wikilink") SF3700 컨트롤러 계열도 NVMe를 지원한다.\[18\]

## AHCI와의 비교

[고급 호스트 컨트롤러 인터페이스](../Page/고급_호스트_컨트롤러_인터페이스.md "wikilink")(AHCI) 인터페이스는 폭넓은 소프트웨어 호환성의 이점이 있지만, 단점으로는 [PCI 익스프레스](../Page/PCI_익스프레스.md "wikilink") 버스를 통해 연결된 [SSD와](../Page/솔리드_스테이트_드라이브.md "wikilink") 함께 사용할 때 최적의 성능을 전달하지 않는다는 것이다. 논리 인터페이스로서 AHCI는 시스템의 [호스트 버스 어댑터](https://ko.wikipedia.org/wiki/호스트_버스_어댑터 "wikilink")(HBA)의 목적이 CPU/메모리 하위 시스템을 회전하는 [자기 매체](https://ko.wikipedia.org/wiki/자기_디스크 "wikilink") 기반의 훨씬 더 느린 스토리지 하위 시스템과 연결하는 것이었던 시기에 개발되었다. 그 결과, AHCI는 회전하는 매체 보다 [DRAM](https://ko.wikipedia.org/wiki/DRAM "wikilink")의 동작에 더 가까운 SSD 장치와 함께 사용할 때 특정한 비효율성이 유입되었다.\[19\]

NVMe 장치 인터페이스는 밑바닥부터 다시 설계하여, PCI 익스프레스 SSD의 낮은 레이턴시와 [병렬화를](../Page/병렬_컴퓨팅.md "wikilink") 이용하고 동시대 CPU, 플랫폼, 응용 프로그램의 병렬화를 보완한다.

높은 수준에서 AHCI 대비 NVMe의 기본적인 이점은 호스트 하드웨어와 소프트웨어의 병렬화를 이용할 수 있다는 것과 관련되며, 이는 [명령 큐의](https://ko.wikipedia.org/wiki/명령_큐 "wikilink") 깊이의 차이, [인터럽트](../Page/인터럽트.md "wikilink") 처리의 효율성, 캐시 불가능한 [레지스터](../Page/프로세서_레지스터.md "wikilink") 접근의 수 등의 차이에서 분명하게 볼 수 있으며, 그 결과 다양한 성능 개선을 이루었다.\[20\]\[21\]

아래의 표는 NVMe와 AHCI의 논리 장치 인터페이스 간 차이를 요약한 것이다.

<table>
<caption>AHCI와 NVMe의 비교[22]</caption>
<thead>
<tr class="header">
<th><p> </p></th>
<th><p><a href="../Page/고급_호스트_컨트롤러_인터페이스.md" title="wikilink">AHCI</a></p></th>
<th><p>NVMe</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>최대 큐 깊이</p></td>
<td><p>하나의 명령 큐<br />
큐 하나 당 32개의 명령</p></td>
<td><p>65535개의 큐[23]<br />
큐 하나 당 65536개의 명령</p></td>
</tr>
<tr class="even">
<td><p>캐시 불가능한 레지스터 접근 수<br />
(각각 2000 사이클)</p></td>
<td><p>큐에 없는 명령마다 6개<br />
큐가 있는 명령마다 9개</p></td>
<td><p>명령 당 2개</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/메시지_신호_인터럽트" title="wikilink">MSI-X</a><br />
와 인터럽트 스티어링</p></td>
<td><p>단일 인터럽트<br />
스티어링 없음</p></td>
<td><p>2048개의 MSI-X 인터럽트</p></td>
</tr>
<tr class="even">
<td><p>병렬화<br />
및 다중 스레드</p></td>
<td><p>명령 발행을 위해<br />
동기화 락이 필요</p></td>
<td><p>락 없음</p></td>
</tr>
<tr class="odd">
<td><p>4 KB 명령의<br />
효율성</p></td>
<td><p>명령 매개변수는<br />
2개의 직렬화된 호스트 DRAM 페치 필요</p></td>
<td><p>하나의 64바이트 페치의<br />
명령 매개변수를 가져옴</p></td>
</tr>
</tbody>
</table>

## 운영 체제 지원

[섬네일의](https://ko.wikipedia.org/wiki/파일:IO_stack_of_the_Linux_kernel.svg "wikilink") 스토리지 스택의 다양한 계층 안에 있는 NVMe 데이터 경로와 다중 내부 큐의 위치.\[24\]\]\]

  - 크롬 OS
    2015년 2월 24일, NVM 익스프레스 장치의 부팅 지원이 [크롬 OS에](../Page/크롬_OS.md "wikilink") 추가되었다.\[25\]\[26\]
  - FreeBSD
    인텔은 [FreeBSD](../Page/FreeBSD.md "wikilink")의 head 및 stable/9 브랜치용 NVM 익스프레스 드라이버를 지원하였다.\[27\]\[28\] nvd(4)와 nvme(4) 드라이버가 FreeBSD 버전 10.2 이후로 GENERIC 커널 구성에 기본으로 포함되어 있다.\[29\]
  - 하이쿠
    NVMe의 [하이쿠](https://ko.wikipedia.org/wiki/하이쿠_\(운영_체제\) "wikilink") 지원은 예정되어 있으나 아직 완료되지 않았다.\[30\]
  - illumos
    [illumos](https://ko.wikipedia.org/wiki/illumos "wikilink")는 2014년 10월 15일 NVMe의 지원을 받았다.\[31\]
  - [iOS](https://ko.wikipedia.org/wiki/iOS "wikilink")
    [아이폰 6S](https://ko.wikipedia.org/wiki/아이폰_6S "wikilink"), [6S 플러스의](https://ko.wikipedia.org/wiki/아이폰_6S_플러스 "wikilink") 출시와 함께 [애플은](https://ko.wikipedia.org/wiki/애플_\(기업\) "wikilink") \[스마트폰에 [PCIe를](../Page/PCI_익스프레스.md "wikilink") 통한 NVMe의 첫 모바일 기능을 도입하였다.\[32\]
  - 리눅스
    인텔은 리눅스용 NVM 익스프레스 드라이버\[33\]\[34\]\[35\]를 출시하였고 2012년 3월 19일 리눅스 커널 버전 3.3 출시와 함께 [리눅스 커널](../Page/리눅스_커널.md "wikilink") 주류에 통합되었다.\[36\]
  - OpenBSD
    OpenBSD의 NVMe 지원에 필요한 개발 작업이 과거 [USB 2.0](https://ko.wikipedia.org/wiki/USB_2.0 "wikilink"), AHCI 지원을 맡았던 개발자에 의해 2014년 4월 시작되었다.\[37\] NVMe의 지원은 OpenBSD 6.0 릴리스에서 활성화되었다.\[38\]
  - [OS X](https://ko.wikipedia.org/wiki/OS_X "wikilink")
    [OS X 요세미티의](../Page/OS_X_요세미티.md "wikilink") 10.10.3 업데이트에서 애플은 NVM 익스프레스의 지원을 도입하였다. 레티나 맥북은 논리 장치 인터페이스로서 PCIe를 통한 NVMe를 사용한다.\[39\]
  - 솔라리스
    [솔라리스는](../Page/솔라리스_\(운영_체제\).md "wikilink") 오라클 솔라리스 11.2에서 NVMe의 지원을 받았다.\[40\]
  - VMware
    인텔은 [VMware](https://ko.wikipedia.org/wiki/VMware "wikilink")용 NVMe 드라이버를 제공하였으며\[41\], vSphere 6.0 이상 빌드에 포함되어 있고 다양한 NVMe 장치를 지원한다.\[42\]
  - 윈도우
    마이크로소프트는 [윈도우 8.1과](../Page/윈도우_8.1.md "wikilink") [윈도우 서버 2012 R2에](https://ko.wikipedia.org/wiki/윈도우_서버_2012_R2 "wikilink") NVMe의 네이티브 지원을 추가하였다.\[43\]\[44\] [윈도우 7과](https://ko.wikipedia.org/wiki/윈도우_7 "wikilink") [윈도우 서버 2008 R2의](../Page/윈도우_서버_2008_R2.md "wikilink") 네이티브 드라이버는 업데이트에 추가되었다.\[45\]

## 소프트웨어 지원

  - QEMU
    NVMe는 2013년 8월 15일 출시된 버전 1.6부터 [QEMU](../Page/QEMU.md "wikilink")에 의해 지원된다.\[46\]

<!-- end list -->

  - UEFI
    [UEFI](https://ko.wikipedia.org/wiki/UEFI "wikilink")용 오픈 소스 NVMe 드라이버는 소스포지를 통해 이용 가능하다.\[47\]

## 각주

## 외부 링크

  -

  - [LFCS: Preparing Linux for nonvolatile memory devices](https://lwn.net/Articles/547903/), [LWN.net](../Page/LWN.net.md "wikilink"), April 19, 2013, by Jonathan Corbet

  - [Multipathing PCI Express Storage](https://web.archive.org/web/20161118033839/http://events.linuxfoundation.org/sites/events/files/slides/LinuxVault2015_KeithBusch_PCIeMPath.pdf), [Linux Foundation](../Page/리눅스_재단.md "wikilink"), March 12, 2015, by Keith Busch

[분류:컴퓨터 버스](https://ko.wikipedia.org/wiki/분류:컴퓨터_버스 "wikilink")

1.
2.
3.
4.
5.
6.
7.  <http://www.bswd.com/FMS09/FMS09-T2A-Huffman.pdf>
8.
9.  <http://www.flashmemorysummit.com/English/Collaterals/Proceedings/2008/20080813_T2A_Huffman.pdf>
10. <http://www.flashmemorysummit.com/English/Collaterals/Proceedings/2013/20130813_A12_Onufryk.pdf>
11.
12.
13.
14.
15.
16.
17.
18.
19.
20.
21.
22.
23.
24.
25.
26.
27.
28.
29.
30.
31.
32.
33.
34.
35.
36.
37.
38.
39.
40.
41.
42.
43.
44.
45.
46.
47.