> This article is converted from Wikipedia: [IOMMU](https://ko.wikipedia.org/wiki/IOMMU).


[섬네일](https://ko.wikipedia.org/wiki/파일:MMU_and_IOMMU.svg "wikilink") (**MMU**)\]\] **IOMMU** (Input/Output Memory Management Unit, 입출력 메모리 관리 장치, **IOMMU**)는 [DMA](../Page/직접_메모리_접근.md "wikilink") 가능한 입출력 [버스와](../Page/버스_\(컴퓨팅\).md "wikilink") [주기억장치](../Page/주기억장치.md "wikilink")를 접속하는 [메모리 관리 장치](../Page/메모리_관리_장치.md "wikilink")(MMU)이다. MMU가 [CPU에](../Page/중앙_처리_장치.md "wikilink") 보이는 [가상 주소를](../Page/가상_메모리.md "wikilink") [물리 주소로](../Page/메모리_주소.md "wikilink") 변환하듯이, IOMMU는 주변기기에서 보이는 가상 주소(장치 주소 또는 입출력 주소라고 부름)을 물리 주소로 변환한다. 주변기기의 오동작에서 메모리를 지키기 위해 [메모리 보호](../Page/메모리_보호.md "wikilink") 기능도 제공한다.

## 실제 예시와 호칭

IOMMU의 예로, [AGP나](../Page/가속_그래픽_포트.md "wikilink") [PCI 익스프레스의](../Page/PCI_익스프레스.md "wikilink") 그래픽 카드에서 사용되고 있는 GART(Graphics Address Remapping Table)가 있다.

[AMD는](../Page/어드밴스트_마이크로_디바이시스.md "wikilink") [하이퍼트랜스포트](../Page/하이퍼트랜스포트.md "wikilink") 아키텍처에서의 IOMMU 기술의 방법을 공표하고 있다.\[1\] [인텔](../Page/인텔.md "wikilink")은 IOMMU의 방법을 VT-d (Virtualization Technology for Directed I/O)로 공표하고 있다.\[2\] [썬 마이크로 시스템즈의](https://ko.wikipedia.org/wiki/썬_마이크로_시스템즈 "wikilink") IOMMU는 Solaris Developer Connection의 DVMA(Device Virtual Memory Access)로 공표하고 있다.\[3\] [IBM](../Page/IBM.md "wikilink")의 IOMMU 는 TCE(Translation Control Entry)라는 이름의 문서가 있다.\[4\] PCI-SIG 에서는 관련되는 부분을 I/O 가상화 (IOV)\[5\]와 Address Translation Services (ATS) 라고 부르고 있다.

x86의 IOMMU에 대해서는 [x86 가상화도](https://ko.wikipedia.org/wiki/x86_가상화 "wikilink") 참고할 것.

## 이점

물리 주소를 직접 사용할 때와 비교한 IOMMU의 이점은 아래와 같다.

  - 큰 버퍼를 확보할 때에 물리적으로 연속이란 것을(실제로 나뉘었지만) 보증할 필요가 없다. IOMMU가 이어져 있게끔 가상 주소와 나뉜 물리 주소의 매핑을 실행한다.

<!-- end list -->

  - 주기억 메모리 전체에 지정할 수 있을 만큼의 주소 폭을 가지지 않는 주변기기(버스)일 때에는 IOMMU를 사용하면 메모리 위에 어디든 버퍼가 있어도 액세스가 가능하게 된다. 이것에 의해 주변기기가 액세스 가능한 범위에 있는 버퍼와 실제 버퍼 간에 메모리 복사를 할 필요가 없어진다.
      - 예를 들면 최신 x86계열 프로세서는 [PAE](../Page/물리_주소_확장.md "wikilink") 기능에 의해 4GB 이상의 메모리 공간을 관리한다. 하지만 32비트의 PCI 장치는 4GB를 넘는 주소에 있는 메모리에는 단순히 액세스할 수 없다. IOMMU가 없을 때에 [운영 체제는](../Page/운영_체제.md "wikilink") 더블 버퍼링(윈도)이나 바운스 버퍼(리눅스)로 불리는 시간이 걸리는 처리를 필요로 한다.

<!-- end list -->

  - [메모리 보호](../Page/메모리_보호.md "wikilink") 기능에 의해 명시적으로 액세스 권한이 없다면 장치에서 메모리에 액세스할 수 없다. 이것에 의해 장치의 오동작이나 악성 장치로부터 메모리를 보호한다. IOMMU의 설정은 CPU 상에서 동작하는 OS가 실행하기에 장치에서 설정할 수는 없다.
      - [가상화](../Page/가상화.md "wikilink")에서는 게스트 OS가 IOMMU를 직접 제어하게 해서는 안 된다.
      - 아키텍처에 따라 IOMMU가 [인터럽트](../Page/인터럽트.md "wikilink")의 재매핑을 실행한다.

IOMMU는 CPU가 장치와 (DMA가 아닌) [보드 맵 입출력으로](../Page/메모리_맵_입출력.md "wikilink") 통신할 때에는 사용되지 않는다.

## 결점

IOMMU를 사용할 때에 결점으로써 다음의 사항이 지적되고 있다.\[6\]

  - IOMMU에 의한 변환과 관리에 의해 성능 저하가 나타난다.
  - I/O용의 [페이지 테이블을](../Page/페이지_테이블.md "wikilink") 작성할 필요가 있기에 물리 메모리가 그만큼 소비된다 [멀티 프로세서](https://ko.wikipedia.org/wiki/멀티_프로세서 "wikilink") 기기에서 프로세서 간의 I/O용 페이지 테이블을 공유 가능할 때에 문제는 조금 완화된다.

## IOMMU 와 가상화의 관계

운영 체제가 [Xen](https://ko.wikipedia.org/wiki/Xen "wikilink") 등의 [가상화 소프트웨어](../Page/가상_머신.md "wikilink") 상에 동작하는 경우 각 운영 체제는 액세스하고 있는 물리 주소를 모른다. 그렇기에 주변기기에 DMA를 지시하도록 하여도 직접적으로 물리 주소를 지정하는 것은 불가능하다. 실제로는 가상 머신이 입출력 조작에 대하여 변환을 하고 있어 입출력 조작지연이 발생하는 원인이 되고 있다.

IOMMU는 게스트 OS와 주변기기의 액세스하는 주소의 매핑을 하기에, 이것을 해결할 수 있다.\[7\]

## 같이 보기

  - [가상 메모리](../Page/가상_메모리.md "wikilink")
  - [메모리 맵 입출력](../Page/메모리_맵_입출력.md "wikilink")
  - [직접 메모리 접근](../Page/직접_메모리_접근.md "wikilink")

## 각주

## 참고 문헌

  -
[분류:기억 장치](https://ko.wikipedia.org/wiki/분류:기억_장치 "wikilink")

1.
2.
3.
4.
5.
6.
7.