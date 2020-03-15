> This article is converted from Wikipedia: [JMicron](https://ko.wikipedia.org/wiki/JMicron).


**JMicron Technology Corporation**(제이마이크론)은 [중화민국](https://ko.wikipedia.org/wiki/중화민국 "wikilink")의 반도체 기업으로 주로 [SATA](https://ko.wikipedia.org/wiki/시리얼_ATA "wikilink") 관련 컨트롤러를 제조, 판매하고 있다.\[1\] JMicron의 칩은 [에이수스](../Page/에이수스.md "wikilink")\[2\], [기가바이트](https://ko.wikipedia.org/wiki/기가바이트 "wikilink"), [MSI](https://ko.wikipedia.org/wiki/마이크로-스타_인터내셔널 "wikilink")\[3\] 등 다수의 PC 메인보드 제조업체에서 사용하고 있다. 하지만 최근 MSI의 새로운 제품들은 마벨 컨트롤러를 사용하는 추세이다.\[4\]

## SSD 컨트롤러

JMicron의 JMF601, JMF602 SATA 플래시 컨트롤러는 쓰기 지연으로 인해 성능이 떨어지는 문제가 보고되고 있는데\[5\]\[6\] 그 원인은 컨트롤러에 내장된 캐시 크기가 너무 작기 때문이다.\[7\] 몇몇 제조 업체에서는 컨트롤러를 2개 사용하고 캐시 메모리를 추가해 이 문제를 해결하고자 하였으나 제조 비용이 증가할 뿐만 아니라 여전히 성능 향상에도 실패하였다.\[8\] 2008년 6월, JMicron은 이러한 문제를 해결하기 위해 캐시를 2배 늘려 쓰기 지연을 줄인 JMF602B 컨트롤러를 출시하였다.\[9\] 하지만 아난드텍(Anandtech)의 테스트 결과 [웨스턴 디지털의](../Page/웨스턴_디지털.md "wikilink") 벨로시랩터 300GB 하드디스크에 비해 4KB 랜덤 쓰기 지연 시간은 74배 더 걸리며 쓰기 속도는 2%에 불과한 것으로 밝혀졌다.\[10\]

JMicron의 SSD 컨트롤러는 에이수스 Eee PC, [커세어](https://ko.wikipedia.org/wiki/커세어 "wikilink")\[11\], [OCZ](../Page/OCZ.md "wikilink"), [트랜센드](../Page/트랜센드.md "wikilink") 등 많은 SSD 제조사에서 채용하고 있다. JMicron은 이들 제조 회사에 SSD 컨트롤러를 처음 납품한 회사로 MLC SSD 가격을 낮추는 데 공헌하였다. JMicron은 2009년 3/4분기에 DRAM 캐시를 사용하는 새로운 SSD 컨트롤러 JMF612를 출시하였다.\[12\]

## 리눅스 호환성

JMicron SATA/IDE 컨트롤러는 몇몇 [부트 로더와](https://ko.wikipedia.org/wiki/부트_로더 "wikilink") 호환성이 떨어진다. 특히, [우분투](https://ko.wikipedia.org/wiki/우분투_\(운영_체제\) "wikilink") 리눅스에서 [GRUB](../Page/GRUB.md "wikilink")을 사용할 경우 [시동](https://ko.wikipedia.org/wiki/시동 "wikilink")할 수 없는 경우가 있다.(2006년 8월, 2.6.17 커널 기준)\[13\] [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink") 2.6.18 커널과 JMicron 컨트롤러 1.06.53 바이오스\[14\]에서 이 호환성 문제가 해결되었지만 메인보드 바이오스를 업그레이드해야 한다는 단점이 있다. [윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 부트 로더나 [EXTLINUX](https://ko.wikipedia.org/wiki/EXTLINUX "wikilink") 같은 다른 부트 로더에서는 제대로 작동한다.

## 대표적인 제품

  - PATA-SATA 변환 브리지
  - USB-ATA 브리지
  - 1394+USB-SATA 브리지
  - PCI-Express-ATA 브리지
  - PCI Express-1394 브리지
  - RAID용 SATA 포트 멀티플라이어/셀렉터
  - PCI Express-이더넷 브리지
  - USB+SATA 플래시 컨트롤러

## 참고 자료

## 외부 링크

  - [JMicron 공식 웹사이트](http://www.jmicron.com/)

[분류:타이완의 전자 기업](https://ko.wikipedia.org/wiki/분류:타이완의_전자_기업 "wikilink")

1.
2.
3.
4.
5.  <http://www.dailytech.com/OCZ+Once+Again+Slashes+the+Price+of+Core+Series+SSDs/article12993.htm>  OCZ Once Again Slashes the Price of Core Series SSDs\]
6.  [G.Skill, Intel & Patriot SSD group test](http://www.bit-tech.net/hardware/2008/12/03/g-skill-patriot-and-intel-ssd-test/10)
7.  [Avoid SSDs with Jmicron's JMF602 Controller](http://www.tomshardware.com/news/ssd-jmicron-jmf602,7057.html)
8.  [Super Talent Claims Its SSDs Can Rock Intel's](http://www.tomshardware.com/news/super-talent-intel-ssd,7978.html)
9.
10. [The SSD Anthology: Understanding SSDs and New Drives from OCZ](http://anandtech.com/storage/showdoc.aspx?i=3531)
11. [New SSD Series from Corsair | Hardware Secrets](http://www.hardwaresecrets.com/news/4585)
12.
13. [Bug \#57502: JMicron PATA/SATA Controller does not work](https://bugs.launchpad.net/bugs/57502)
14. [JMicron FAQ](http://www.jmicron.com/Support_FAQ.html)  - broken link