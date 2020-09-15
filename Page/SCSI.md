> This article is converted from Wikipedia: [SCSI](https://ko.wikipedia.org/wiki/SCSI).


[섬네일](https://ko.wikipedia.org/wiki/파일:Scsi_logo.svg "wikilink")

**SCSI** (스커지/스카시, **S**mall **C**omputer **S**ystem **I**nterface, )는 [컴퓨터](../Page/컴퓨터.md "wikilink")에 [주변기기](../Page/주변기기.md "wikilink")를 연결할 때 직렬 방식으로 연결하기 위한 표준을 일컫는다. 다시 말해, 컴퓨터에서 주변기기를 연결하기 위한 병렬 표준 인터페이스로 입출력 버스를 접속하는 데에 필요한 기계적, 전기적인 요구 사항과 모든 주변 기기 장치를 중심으로 명령어 집합에 대한 규격을 말한다.

SCSI는 IBM 호환기종을 제외한 [애플](../Page/애플.md "wikilink"), [썬 마이크로시스템즈](../Page/썬_마이크로시스템즈.md "wikilink") 등에 널리 쓰이고 있다. SCSI는 주변 기기의 번호만 각각 지정해 주면 자료 충돌 없이 주변 기기를 제어할 수 있다.

또한 SCSI 어댑터를 통해 자체적으로 버스를 구성하기도 하지만 주변기기 자체가 사용하는 프로토콜이 조금이라도 다르면 사용할 수 없다. SCSI는 주변장치를 제어하는 기능이 호스트에 있는 것이 아니라 주변장치 자체에 들어 있어서 SCSI를 사용하는 주변장치들은 모두 호스트 어댑터를 통해 직접 통신할 수 있다.

SCSI가 발전된 것으로 SCSI-2가 있는데 이는 초기 SCSI 방식의 단점을 보완하고자 발표된 2차 표준안으로, 이 규격은 표준 디스크와 테이프 장치 이외에 광자기 디스크, 매체 교환 장치, 통신 장치 등에도 적용하였다. 비용이 비싼 것이 단점이라 일반 [개인용 컴퓨터에는](../Page/개인용_컴퓨터.md "wikilink") 잘 도입하지 않았다.

## 역사

SCSI는 본래 1978년에 개발되어 1981년에 공개된 [슈거트 어소시에이츠](https://ko.wikipedia.org/wiki/슈거트_어소시에이츠 "wikilink") 시스템 인터페이스(Shugart Associates System Interface)의 약자인 "SASI"에서 비롯하였다.\[1\]

## SCSI 인터페이스

[섬네일](https://ko.wikipedia.org/wiki/파일:Scsi-1_gehaeuse.jpg "wikilink")

SCSI는 다양한 인터페이스로 사용할 수 있다. 가장 흔히 쓰이는 첫 번째 것이 [병렬 SCSI](https://ko.wikipedia.org/wiki/병렬_SCSI "wikilink") (SPI로도 불림)이며 [병렬](https://ko.wikipedia.org/wiki/병렬_통신 "wikilink") 버스 디자인을 사용한다. 2008년에 SPI는 [시리얼 결합 SCSI](https://ko.wikipedia.org/wiki/시리얼_결합_SCSI "wikilink") (SAS)로 대체되어 [직렬 통신](../Page/직렬_통신.md "wikilink") 디자인을 사용하며 다른 기술들을 포함하고 있다. [iSCSI](https://ko.wikipedia.org/wiki/iSCSI "wikilink")는 물리적인 기능을 완전히 제거하고 그 대신 [TCP/IP](https://ko.wikipedia.org/wiki/TCP/IP "wikilink")를 전달 구조로 사용한다. 완전한 SCSI 표준을 따르지 않는 다른 수많은 인터페이스는 SCSI 명령 프로토콜을 사용한다.

SCSI 인터페이스는 [마이크로소프트 윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink"), [맥 OS](../Page/맥_OS.md "wikilink"), [유닉스](../Page/유닉스.md "wikilink"), [리눅스](../Page/리눅스.md "wikilink") 운영 체제용으로 다양한 제조업체의 컴퓨터에 포함되기도 하고 [메인보드](../Page/메인보드.md "wikilink")에 달리거나 플러그인 어댑터를 통하여 제공되기도 한다. [시리얼 결합 SCSI와](https://ko.wikipedia.org/wiki/시리얼_결합_SCSI "wikilink") [SATA](https://ko.wikipedia.org/wiki/시리얼_ATA "wikilink") 드라이브가 등장하면서 메인보드에 SCSI 기능은 더 이상 제공되지 않고 있다. 그러나 일부 회사는 PCIe와 PCI-X를 지원하는 메인보드에 SCSI 인터페이스를 제공하고 있다.

## 같이 보기

  - [버스 (컴퓨팅)](../Page/버스_\(컴퓨팅\).md "wikilink")
  - [하드 디스크](https://ko.wikipedia.org/wiki/하드_디스크 "wikilink")
  - [병렬 ATA](../Page/병렬_ATA.md "wikilink")

## 각주

[분류:컴퓨터 버스](https://ko.wikipedia.org/wiki/분류:컴퓨터_버스 "wikilink")

1.  ANSI Draft SASI Standard, Rev D, February 17, 1982, pg. ii states, "9/1 5/81 first presentation to ANSI committee X3T9-3 (2 weeks following announcement in Electronic Design)."