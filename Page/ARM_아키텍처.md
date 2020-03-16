> This article is converted from Wikipedia: [ARM ](https://ko.wikipedia.org/wiki/ARM_).


**ARM 아키텍처**(ARM architecture, 과거 명칭: Advanced RISC Machine, 최초 명칭: Acorn RISC Machine)는 임베디드 기기에 많이 사용되는 [RISC](https://ko.wikipedia.org/wiki/RISC "wikilink") 프로세서이다. 저전력을 사용하도록 설계하여 ARM CPU는 모바일 시장 및 [싱글 보드 컴퓨터로](https://ko.wikipedia.org/wiki/싱글_보드_컴퓨터 "wikilink") 불리는 [개인용 컴퓨터에서](../Page/개인용_컴퓨터.md "wikilink") 뚜렷한 강세를 보인다.

  - 1985년 4월 26일 영국의 캠브리지에 있는 에이콘 컴퓨터(Acorn Computers)에 의해서 탄생.
  - 1990년 11월에 [애플과](https://ko.wikipedia.org/wiki/애플_\(기업\) "wikilink") [VLSI](https://ko.wikipedia.org/wiki/VLSI "wikilink")의 조인트 벤처 형식으로 ARM(Advanced RISC Machines Ltd.)가 생김.

## 계보

  - ARMv4 아키텍처는 32비트 주소 영역에서 32비트 ISA(Instruction Set Architecture) 동작이 가능하다. 16비트 Thumb 명령어 셋을 탑재한 ARMv4T 아키텍처는 32비트 코드의 이점을 그대로 살리고, 메모리 공간을 35% 이상 절약할 수 있도록 해주었다.

<!-- end list -->

  - ARMv5TE(1999년) 아키텍처는 개선된 thumb 아키텍처와 ‘Enhanced’ DSP 명령어 셋을 ARM ISA에 추가하였다. 이러한 Thumb의 변화에는 소수의 명령어 추가와 함께 ARM/Thumb 인터워킹(interworking)의 개선, 컴파일 성능의 대폭적인 향상, ARM/Thumb 루틴의 혼합 사용, 코드 크기와 성능에 대한 균형도 포함되어 있다. 또한 ‘Enhanced’ DSP 명령어들은 복잡한 수치연산에서 70%의 성능 개선을 보여주었다.

<!-- end list -->

  - ARMv5TEJ(2000년) 아키텍처에는 Jazelle(자바 하드웨어 가속기) 확장명령어가 추가되었으며, 이로써 자바 가속 기술을 탑재한 아키텍처가 탄생하게 된다. ARMv5TJE 아키텍처는 Jazelle의 탄생함에 따라 가속 기술을 사용하지 않은 JVM(Java Virtual Machine)보다 속도 면에서 8배가 향상되었으며, 소비전력의 측면에서도 80%를 줄일 수 있게 된다.

<!-- end list -->

  - ARMv6(2001년) 아키텍처가 발표되면서 여러 방면에서 기능 개선이 이루어졌다. 특히 메모리 시스템, 예외 처리의 개선, 멀티프로세싱 환경을 위한 더 많은 지원 등이 이에 해당한다. 이것 이외도 ARMv6 아키텍처에는 SIMD(Single Instruction Multiple Data) 소프트웨어 실행을 지원하는 미디어 명령이 포함되어 있으며, SIMD 명령들은 오디오 및 비디오 코덱을 포함하는 응용 프로그램들의 사용 확대를 위해 최적화되었다.

<!-- end list -->

  - ARM1136J(2002년) (F)-8 코어. 스트롱암 CPU는 DEC(Digital Equipment Corporation)에 의해서 ARM과 함께 개발되었다. 이것이 최초의 modified-Harvard 아키텍처(명령어 캐시와 데이터 캐시를 분리해서 사용)를 채용한 제품이며, modified-Harvard 아키텍처로 ARM의 쓰기 처리 능력의 고속화가 가능하게 되었다. 스트롱암의 주요 특징 중에는 5단 파이프라인의 채용, 64비트 곱셈 및 일부 곱셈 기능을 제외한 모든 일반 명령어들의 싱글 사이클 처리 등이 포함되어 있다.

## ARM 코어

<table>
<thead>
<tr class="header">
<th><p>계열</p></th>
<th><p>아키텍처 버전</p></th>
<th><p>코어</p></th>
<th><p>기능</p></th>
<th><p>캐시 (명령어/데이터)/<a href="../Page/메모리_관리_장치.md" title="wikilink">MMU</a></p></th>
<th><p>일반적인 <a href="https://ko.wikipedia.org/wiki/MIPS" title="wikilink">MIPS</a> @ MHz</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ARM1</p></td>
<td><p>ARMv1</p></td>
<td><p>ARM1</p></td>
<td></td>
<td><p>없음</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>ARM2</p></td>
<td><p>ARMv2</p></td>
<td><p>ARM2</p></td>
<td><p>곱하기 명령 (MUL) 추가</p></td>
<td><p>없음</p></td>
<td><p>4 MIPS @ 8 MHz<br />
0.33 DMIPS/MHz</p></td>
</tr>
<tr class="odd">
<td><p>ARMv2a</p></td>
<td><p>ARM250</p></td>
<td><p>MEMC (MMU) 구현, 그래픽과 IO 프로세스. 아키텍처 2a:SWP와 SWPB 등의 스왑 명령추가.</p></td>
<td><p>없음, MEMC1a</p></td>
<td><p>7 MIPS @ 12 MHz</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>ARM3</p></td>
<td><p>ARMv2a</p></td>
<td><p>ARM2a</p></td>
<td><p>ARM에 프로세스 캐시 최초 사용</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/4K" title="wikilink">4K</a> 통합</p></td>
<td><p>12 MIPS @ 25 MHz<br />
0.50 DMIPS/MHz</p></td>
</tr>
<tr class="odd">
<td><p>ARM6</p></td>
<td><p>ARMv3</p></td>
<td><p>ARM60</p></td>
<td><p>v3 아키텍처, 최초로 32 비트 메모리 지원(26 비트에 반대된)</p></td>
<td><p>없음</p></td>
<td><p>10 MIPS @ 12 MHz</p></td>
</tr>
<tr class="even">
<td><p>ARM600</p></td>
<td><p>캐시와 코프로세스 버스(FPA10 <a href="../Page/부동소수점.md" title="wikilink">부동소수점</a> 모듈).</p></td>
<td><p>4K 통합</p></td>
<td><p>28 MIPS @ 33 MHz</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>ARM610</p></td>
<td><p>캐시, 코프로세서 버스 없음.</p></td>
<td><p>4K 통합</p></td>
<td><p>17 MIPS @ 20 MHz<br />
0.65 DMIPS/MHz</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>ARM7</p></td>
<td><p>ARMv3</p></td>
<td><p>ARM700</p></td>
<td></td>
<td><p>8 <a href="../Page/킬로바이트.md" title="wikilink">KB</a> 통합</p></td>
<td><p>40 MHz</p></td>
</tr>
<tr class="odd">
<td><p>ARM710</p></td>
<td></td>
<td><p>8KB 통합</p></td>
<td><p>40 MHz</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>ARM710a</p></td>
<td></td>
<td><p>8 KB 통합</p></td>
<td><p>40 MHz<br />
0.68 DMIPS/MHz</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>ARM7100</p></td>
<td><p>SoC.</p></td>
<td><p>8 KB 통합</p></td>
<td><p>18 MHz</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>ARM7500</p></td>
<td><p>SoC.</p></td>
<td><p>4 KB 통합</p></td>
<td><p>40 MHz</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>ARM7500FE</p></td>
<td><p>SoC. "FE" FPA와 EDO 메모리 컨트롤러 추가</p></td>
<td><p>4 KB 통합</p></td>
<td><p>56 MHz<br />
0.73 DMIPS/MHz</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>ARM7TDMI</p></td>
<td><p>ARMv4T</p></td>
<td><p>ARM7TDMI(-S)</p></td>
<td><p>3-단계 파이프라인, Thumb</p></td>
<td><p>없음</p></td>
<td><p>15 MIPS @ 16.8 MHz</br>63 DMIPS @ 70 MHz</p></td>
</tr>
<tr class="odd">
<td><p>ARM710T</p></td>
<td></td>
<td><p>8 KB 통합, MMU</p></td>
<td><p>36 MIPS @ 40 MHz</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>ARM720T</p></td>
<td></td>
<td><p>8 KB 통합, MMU</p></td>
<td><p>60 MIPS @ 59.8 MHz</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>ARM740T</p></td>
<td></td>
<td><p>MPU</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>ARMv5TEJ</p></td>
<td><p>ARM7EJ-S</p></td>
<td><p>Jazelle DBX, 향상된 DSP 명령, 5-단계 파이프라인</p></td>
<td><p>없음</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>StrongARM</p></td>
<td><p>ARMv4</p></td>
<td><p>SA-110</p></td>
<td></td>
<td><p>16 KB/16 KB, MMU</p></td>
<td><p>203 MHz<br />
1.0 DMIPS/MHz</p></td>
</tr>
<tr class="even">
<td><p>SA-1110</p></td>
<td></td>
<td><p>16 KB/16 KB, MMU</p></td>
<td><p>233 MHz</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>ARM8</p></td>
<td><p>ARMv4</p></td>
<td><p>ARM810[1]</p></td>
<td><p>5-단계 파이프라인, 고정된 예측 분기, 이중 대역폭 메모리</p></td>
<td><p>8 KB 통합, MMU</p></td>
<td><p>84 MIPS @ 72 MHz<br />
1.16 DMIPS/MHz</p></td>
</tr>
<tr class="even">
<td><p>ARM9TDMI</p></td>
<td><p>ARMv4T</p></td>
<td><p>ARM9TDMI</p></td>
<td><p>5-단계 파이프라인</p></td>
<td><p>없음</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>ARM920T</p></td>
<td></td>
<td><p>16 KB/16 KB, MMU</p></td>
<td><p>200 MIPS @ 180 MHz</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>ARM922T</p></td>
<td></td>
<td><p>8 KB/8 KB, MMU</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>ARM940T</p></td>
<td></td>
<td><p>4 KB/4 KB, MPU</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>ARM9E</p></td>
<td><p>ARMv5TE</p></td>
<td><p>ARM946E-S</p></td>
<td><p>향상된 DSP 명령</p></td>
<td><p>가변적, 메모리 밀착형 MPU</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>ARM966E-S</p></td>
<td></td>
<td><p>캐시없음, TCMs</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>ARM968E-S</p></td>
<td></td>
<td><p>캐시없음, TCMs</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>ARMv5TEJ</p></td>
<td><p>ARM926EJ-S</p></td>
<td><p>Jazelle DBX, 향상된 DSP 명령</p></td>
<td><p>가변적, TCMs, MMU</p></td>
<td><p>220 MIPS @ 200 MHz,</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>ARMv5TE</p></td>
<td><p>ARM996HS</p></td>
<td><p>Clockless 프로세서, 향상된 DSP 명령</p></td>
<td><p>캐시없음, TCMs, MPU</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>ARM10E</p></td>
<td><p>ARMv5TE</p></td>
<td><p>ARM1020E</p></td>
<td><p>VFP, 6-단계 파이프라인, 향상된 DSP 명령</p></td>
<td><p>32 KB/32 KB, MMU</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>ARM1022E</p></td>
<td><p>VFP</p></td>
<td><p>16 KB/16 KB, MMU</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>ARMv5TEJ</p></td>
<td><p>ARM1026EJ-S</p></td>
<td><p>Jazelle DBX, 향상된 DSP 명령</p></td>
<td><p>가변적, MMU or MPU</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>XScale</p></td>
<td><p>ARMv5TE</p></td>
<td><p>80200/IOP310/IOP315</p></td>
<td><p>I/O 프로세서, 향상된 DSP 명령</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>80219</p></td>
<td></td>
<td></td>
<td><p>400/600 MHz</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>IOP321</p></td>
<td></td>
<td></td>
<td><p>600 BogoMips @ 600 MHz</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>IOP33x</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>IOP34x</p></td>
<td><p>1-2 core, RAID Acceleration</p></td>
<td><p>32K/32K L1, 512K L2, MMU</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>PXA210/PXA250</p></td>
<td><p>응용분야 프로세서, 7-단계 파이프라인</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>PXA255</p></td>
<td></td>
<td><p>32KB/32KB, MMU</p></td>
<td><p>400 BogoMips @ 400 MHz</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>PXA26x</p></td>
<td></td>
<td></td>
<td><p>default 400 MHz, up to 624 MHz</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>PXA27x</p></td>
<td><p>응용분야 프로세서</p></td>
<td><p>32 <a href="https://ko.wikipedia.org/wiki/KiB" title="wikilink">KiB</a>/32 Kb, MMU</p></td>
<td><p>800 MIPS @ 624 MHz</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>PXA800(E)F</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Monahans</p></td>
<td></td>
<td></td>
<td><p>1000 MIPS @ 1.25 GHz</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>PXA900</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>IXC1100</p></td>
<td><p>Control Plane 프로세서</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>IXP2400/IXP2800</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>IXP2850</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>IXP2325/IXP2350</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>IXP42x</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>IXP460/IXP465</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>ARM11</p></td>
<td><p>ARMv6</p></td>
<td><p>ARM1136J(F)-S</p></td>
<td><p>SIMD, Jazelle DBX, VFP, 8-단계 파이프라인</p></td>
<td><p>가변적, MMU</p></td>
<td><p>740 @ 532-665 MHz (i.MX31 SoC), 400-528 MHz</p></td>
</tr>
<tr class="odd">
<td><p>ARMv6T2</p></td>
<td><p>ARM1156T2(F)-S</p></td>
<td><p>SIMD, Thumb-2, VFP, 9-단계 파이프라인</p></td>
<td><p>가변적, MPU</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>ARMv6KZ</p></td>
<td><p>ARM1176JZ(F)-S</p></td>
<td><p>SIMD, Jazelle DBX, VFP</p></td>
<td><p>가변적, MMU+TrustZone</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>ARMv6K</p></td>
<td><p>ARM11 MPCore</p></td>
<td><p>1-4 코어 SMP, SIMD, Jazelle DBX, VFP</p></td>
<td><p>가변적, MMU</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Cortex</p></td>
<td><p>ARMv7-A</p></td>
<td><p>Cortex-A8</p></td>
<td><p>응용분야 형상, VFP, NEON, Jazelle RCT, Thumb-2, 13-단계 <a href="../Page/슈퍼스칼라.md" title="wikilink">슈퍼스칼라</a> 파이프라인</p></td>
<td><p>가변적 (L1+L2), MMU+TrustZone</p></td>
<td><p>2000 (2.0 DMIPS/MHz, 600 MHz부터 1 GHz) 까지</p></td>
</tr>
<tr class="odd">
<td><p>Cortex-A9</p></td>
<td><p>응용분야 형상, VFP, (NEON), Jazelle RCT and DBX, Thumb-2</p></td>
<td><p>MMU+TrustZone</p></td>
<td><p>2.5 DMIPS/MHz</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Cortex-A9 MPCore</p></td>
<td><p>As Cortex-A9, 1-4 코어 SMP</p></td>
<td><p>MMU+TrustZone</p></td>
<td><p>2.0 DMIPS/MHz</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Cortex-A12</p></td>
<td></td>
<td></td>
<td><p>2.96 DMIPS/MHz</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Cortex-A15</p></td>
<td></td>
<td></td>
<td><p>3.5 DMIPS/MHz</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>ARMv7-R</p></td>
<td><p>Cortex-R4(F)</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/임베디드" title="wikilink">임베디드</a> 형상, (FPU)</p></td>
<td><p>가변적 캐시, MPU optional</p></td>
<td><p>600 DMIPS</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>ARMv6-M</p></td>
<td><p>Cortex-M1</p></td>
<td><p>FPGA와 연동, <a href="../Page/마이크로컨트롤러.md" title="wikilink">마이크로컨트롤러</a> 형상, Thumb-2 (BL, MRS, MSR, ISB, DSB, and DMB).</p></td>
<td><p>없음, 선택적 메모리 밀착형.</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>ARMv7-M</p></td>
<td><p>Cortex-M3</p></td>
<td><p><a href="../Page/마이크로컨트롤러.md" title="wikilink">마이크로컨트롤러</a> 형상, Thumb-2 only.</p></td>
<td><p>캐시없음, (MPU)</p></td>
<td><p>125 DMIPS @ 100 MHz</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>ARMv7E-M</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/Cortex-M4" title="wikilink">Cortex-M4</a></p></td>
<td><p><a href="../Page/마이크로컨트롤러.md" title="wikilink">마이크로컨트롤러</a> 형상</p></td>
<td></td>
<td><p>125 DMIPS</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>ARMv8-A</p></td>
<td><p>Cortex-A53</p></td>
<td><p>64비트 명령어 지원</p></td>
<td><p>MMU, TrustZone, 64bit 가상 주소</p></td>
<td><p>2.3 DMIPS/MHz</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Cortex-A57</p></td>
<td><p>64비트 명령어 지원</p></td>
<td><p>MMU, TrustZone, 64bit 가상 주소</p></td>
<td><p>4.1 DMIPS/MHz</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Cortex-A72</p></td>
<td><p>64비트 명령어 지원</p></td>
<td><p>MMU, TrustZone, 64bit 가상 주소</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## 32비트 아키텍처

### 보안 확장

#### 트러스트존 (Cortex-A 프로파일)

트러스트존 테크놀로지(TrustZone Technology)라는 이름으로 마케팅된 보안 확장 기능은 ARMv6KZ 이상의 애플리케이션 프로파일 아키텍처에 포함된다. 하드웨어 기반 접근 제어의 지원을 받는 2개의 가상 프로세서를 제공함으로써 SoC의 다른 전용 보안 코어를 추가하지 않으므로 비용을 낮출 수 있다.

#### ARMv8-M용 트러스트존 (Cortex-M 프로파일)

TrustZone for ARMv8-M Technology로 마케팅되는 보안 확장 기능은 ARMv8-M 아키텍처에 도입되었다.

## 어셈블리어 예제

[C 언어로](https://ko.wikipedia.org/wiki/C_언어 "wikilink") 다음과 같은 코드를,

``` c
    while (i != j) {
       if (i > j)
           i -= j;
       else
           j -= i;
    }
```

ARM 어셈블리어로는 다음과 같이 작성할 수 있다.

``` arm
loop:   CMP  Ri, Rj         ; set condition "NE" if (i != j),
                            ;               "GT" if (i > j),
                            ;            or "LT" if (i < j)
        SUBGT  Ri, Ri, Rj   ; if "GT" (Greater Than), i = i-j;
        SUBLT  Rj, Rj, Ri   ; if "LT" (Less Than), j = j-i;
        BNE  loop           ; if "NE" (Not Equal), then loop
```

## 크로스 컴파일

현재 [이클립스나](../Page/이클립스_\(소프트웨어\).md "wikilink") [WAF등을](https://ko.wikipedia.org/wiki/waf "wikilink") 통해서 운영체제와 상관없이 일정수준을 만족하는 기준에서 작성된 소스코드를 원하는 운영체제에 맞는 실행파일로 빌드를 지원하고있다. 한편 ARM社 역시 이러한 오픈소스와 작동하는 [GNU Compiler](../Page/GNU_컴파일러_모음.md "wikilink") (GCC) 툴체인 프로그램을 제공하고있다.\[2\]\[3\]

이에따라 특히 기존 [인텔](../Page/인텔.md "wikilink")이나 [AMD](https://ko.wikipedia.org/wiki/AMD "wikilink") [x86](https://ko.wikipedia.org/wiki/x86 "wikilink")계열의 리눅스 프로그램들은 자유로이 [싱글보드 컴퓨터에](../Page/단일_보드_컴퓨터.md "wikilink") 포팅되어 사용할 수 있는 생태계가 형성되었다.

## 마이크로컨트롤러 타입

일부 [마이크로컨트롤러](../Page/마이크로컨트롤러.md "wikilink")유닛인 MCU타입 보드는 [아두이노 IDE에서의](../Page/아두이노_IDE.md "wikilink") 개발환경을 공식적으로 지원한다.\[4\]\[5\]

## 아두이노 보드

MCU타입 보드인 cortex-M4칩을 장착한 [ST社의](../Page/ST마이크로일렉트로닉스.md "wikilink") [STM32](../Page/STM32.md "wikilink") NUCLEO-F303K8는 오픈 소스 하드웨어인 [아두이노](../Page/아두이노.md "wikilink") 나노 보드와 헤더배치에서 호환되도록 설계되었다.\[6\]\[7\] 한편 cortex-M4칩은 [FPU](https://ko.wikipedia.org/wiki/FPU "wikilink")를 포함한 32비트 [CPU](https://ko.wikipedia.org/wiki/CPU "wikilink")이다.

## 싱글보드컴퓨터

Cortex-A8을 채택한 10cm X6cm 전후의 초소형 크기에 5V 전력을 사용하는 단일보드컴퓨터는 본격적으로 [스마트폰](../Page/스마트폰.md "wikilink")이나 [싱글보드컴퓨터등에](../Page/단일_보드_컴퓨터.md "wikilink") 특화되어 사용되기 시작했다.\[8\]\[9\]

운영체제로는 우분투계열의 [우분투 메이트나](https://ko.wikipedia.org/wiki/우분투_메이트 "wikilink") [아크 리눅스등이](../Page/아크_리눅스.md "wikilink") [리눅스 OS로서](../Page/리눅스.md "wikilink") 지원되며 리눅스 운영체제를 기반으로하는 [안드로이드가](../Page/안드로이드_\(운영_체제\).md "wikilink") 스마트폰등에서 그리고 다양한 임베디드 기기를 위해 [웹OS](../Page/웹OS.md "wikilink")나 [타이젠](../Page/타이젠.md "wikilink")등이 사용되고있다.

## 각주

  - \[참고\] [ARM Cortex-M4-based STM32F4 MCU Series](https://www.st.com/en/microcontrollers/stm32f4-series.html?querycriteria=productId=SS1577)
  - \[참고\] [STM32F4 MCU - nucleo-f303k8](https://www.st.com/en/evaluation-tools/nucleo-f303k8.html)

## 외부 링크

  - , ARM Ltd.

[ARM_아키텍처](https://ko.wikipedia.org/wiki/분류:ARM_아키텍처 "wikilink") [분류:마이크로프로세서](https://ko.wikipedia.org/wiki/분류:마이크로프로세서 "wikilink") [분류:임베디드 시스템](https://ko.wikipedia.org/wiki/분류:임베디드_시스템 "wikilink") [분류:임베디드 마이크로프로세서](https://ko.wikipedia.org/wiki/분류:임베디드_마이크로프로세서 "wikilink") [분류:마이크로컨트롤러](https://ko.wikipedia.org/wiki/분류:마이크로컨트롤러 "wikilink")

1.  ["ARM810 - Dancing to the Beat of a Different Drum"](http://www.hotchips.org/archives/hc8/2_Mon/HC8.S4/HC8.4.1.pdf)  ARM Limited presentation at Hot Chips 8, 1996
2.  Eclipse CDT for C/C++ , Cross GNU , Cross ARM GNU
3.  [ARM](https://ko.wikipedia.org/wiki/ARM "wikilink") - [The GNU Embedded Toolchain for Arm](https://developer.arm.com/open-source/gnu-toolchain/gnu-rm/downloads)
4.  [STM32 Nucleo 보드 - multiple IDE support](https://www.st.com/content/ccc/resource/sales_and_marketing/promotional_material/flyer/d2/06/5c/20/25/28/42/ff/flstm32nucleo.pdf/files/flstm32nucleo.pdf/jcr:content/translations/en.flstm32nucleo.pdf)
5.  [Quick Start to STM Nucleo on Arduino IDE By sriksh9 in WorkshopTools](https://www.instructables.com/id/Quick-Start-to-STM-Nucleo-on-Arduino-IDE/)
6.  [STM32 NUCLEO-F303K8 , Arduino-Nano-compatible headers](https://os.mbed.com/platforms/ST-Nucleo-F303K8/)
7.  [STM32 Nucleo-32 development board with STM32F303K8 MCU, supports Arduino connectivity](https://www.st.com/content/st_com/en/products/evaluation-tools/product-evaluation-tools/mcu-eval-tools/stm32-mcu-eval-tools/stm32-mcu-nucleo/nucleo-f303k8.html#samplebuy-scroll)
8.  [오드로이드](https://www.hardkernel.com/shop/odroid-c2/)
9.  [삼성 캘럭시S](https://www.samsung.com/sec/support/model/SHW-M110SHKSC/)