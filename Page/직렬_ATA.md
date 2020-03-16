> This article is converted from Wikipedia: [ ATA](https://ko.wikipedia.org/wiki/_ATA).


**직렬 ATA**(, **SATA**)는 [하드 디스크](https://ko.wikipedia.org/wiki/하드_디스크 "wikilink") 혹은 [광학 드라이브와](https://ko.wikipedia.org/wiki/광학_드라이브 "wikilink") 데이터 전송을 주요 목적으로 만든 [컴퓨터 버스의](https://ko.wikipedia.org/wiki/컴퓨터_버스 "wikilink") 한 가지이다. 약자를 철자대로 읽어서 **사타**(영어식으로는 **새터**, **세이터**)라고도 한다. 직렬 ATA는 예전의 [ATA](../Page/병렬_ATA.md "wikilink") 표준을 계승하여, ‘[병렬 ATA](../Page/병렬_ATA.md "wikilink")(, 기존의 ATA)’를 대체하기 위해 고안되었다. 직렬 ATA 어댑터와 장치들은 비교적 속도가 빠른 [직렬 연결을](../Page/직렬_통신.md "wikilink") 이용하여 연결된다.

## 구조

직렬 ATA의 구조에서 [물리 계층을](../Page/물리_계층.md "wikilink") 보면, 데이터 연결은 두 쌍의 한 방향의 신호 선들로 이루어진다. 이 선 위에서, 직렬 ATA는 [낮은 전압 차분 신호](../Page/낮은_전압_차분_신호.md "wikilink")(LVDS) 방식을 사용한다. LVDS는 병렬 ATA에 비해 더 빠른 전송을 가능케 한다. 바이트 데이터는 8B/10B 인코딩을 이용하여 인코딩되고 전송된다. 8B/10B 인코딩은 [이더넷](../Page/이더넷.md "wikilink"), [파이버 채널](../Page/파이버_채널.md "wikilink"), [PCI 익스프레스](../Page/PCI_익스프레스.md "wikilink") 등에서 이용되는 방식이다. 일반적으로 병렬에서 직렬로 인코딩을 하면 효율이 80%정도 나온다. 다만, 이 인코딩 방식은 비트와 문자열 경계를 구분하는 정보를 함께 가지고 있으므로, 클럭 신호가 따로 필요 없다. 병렬 방식이 아닌 직렬 방식을 사용하면, 미래에 성능이 개선된 하드 디스크가 나오면 속도를 뒷받침할 수 있다. 또한, 고속의 병렬 인터페이스에 견주어 가격을 낮출 수 있다.

SATA [물리 계층](../Page/물리_계층.md "wikilink") 위에는 링크 계층 및 트랜스포트 계층이 존재한다. 이 상위 계층들은 설정 및 데이터 오퍼레이션들 순차적인 패킷으로 변환한다. 이 패킷은 SATA이 연결되면 전송된다. 응용 계층에서는 SATA는 ATA의 동작 모델을 그대로 이용하였다. 작업 레지스터 파일(읽기/쓰기 PIO 및 DMA를 요청하기 위해 쓰임)도 같은데, 모든 SATA 호스트 구현은 이것을 반드시 구현해야 한다. 각 제조사별로는 옵션으로 사용할 수 있게 해 두었다. (이를테면, 시뮬레이티드 [RAID](../Page/RAID.md "wikilink")), 하지만 이러한 기능들을 이용하려면 특별한 장치 드라이버를 써야 한다.

사용자의 관점에서 주요한 SATA와 PATA의 차이점이 한 가지 더 있다. 호스트와 드라이브 사이가 1:1로 연결된다는 것이다. 각 SATA 장치는 SATA 호스트 포트와 1:1로 연결된다. 다른 장치들과 케이블이나 대역을 같이 쓰지 않으며 별도의점퍼설정이 필요없으며 저장장치는 노트북과 데스크탑과 단자가 같고 odd는 단자의 크기에서 차이나지만 호환이가능하다.

많은 제조사들은 직렬 ATA를 [직렬 부착 SCSI](https://ko.wikipedia.org/wiki/직렬_부착_SCSI "wikilink")(Serial Attached SCSI)와 결합하여 구현한 바 있다. 이 프로토콜은 커넥터를 같이 쓴다. 입문 수준의 초보 사용자들은 SATA 저장 장치를 쓰고, 나중에 높은 성능을 바라는 사용자들은 SAS로 업그레이드하는 길이 열려 있다.

## SATA 1.5 Gbit/s(SATA1)

SATA 1.5 Gbit/s는 1세대 SATA 인터페이스다. **사타 원**(SATA I), 혹은 **SATA/150**이라고 말하기도 한다. 1 초에 약 1.5 기가비트의 속도로 통신할 수 있다. 8B10B 코딩의 오버헤드를 감안하면, 부호화가 되지 않은 상태의 전송률은 1 초에 1.2 기가비트(초당 150 메가바이트)다. 실제로는 SATA/150이나 PATA/133이나 이론적인 버스트-스루풋(burst throughput)은 비슷비슷하다. 하지만, 최근의 SATA 장치들은 [NCQ](../Page/NCQ.md "wikilink") 같은 기능을 제공하여 다중 작업 환경에서 SATA의 성능을 조금 더 높여주고 있다.

## SATA 3.0 Gbit/s(SATA2)

SATA/150이 업계에 도입된 바로 다음, SATA/150에서 문제점이 몇 가지 부각되었다. 먼저, 응용 프로그램 수준에서 SATA의 구동 모델은 PATA의 구동 모델을 가상으로 구현하는 방식이었기 때문에, 디스크가 한번에 한가지 요청(읽기/쓰기 등의 동작)만 처리할 수 있었다. 이에 반해, SCSI 디스크는 여러 요청을 받아서 큐(queue)에 넣은 후, 디스크 드라이브가 응답 시간을 최적화하기 위해 요청을 다시 배열할 수 있었다. NCQ에 의해 SATA에도 이러한 기능이 도입되었다. NCQ는 부가 기능으로 SATA 1.5 Gbit/s 와 SATA 3.0 Gbit/s 두 군데에서 쓸 수 있다.

1세대 직렬 ATA 장치들은 이전의 병렬 ATA/133 장치에 비해 조금 더 빠를 뿐이었다. 그리하여 데이터 [스루풋](https://ko.wikipedia.org/wiki/스루풋 "wikilink")을 150 MB/s 에서 300 MB/s 로 늘린, 3 Gbit/s 신호 속도의 물리 계층이 도입되었다. 현재 데스크톱에서 쓸 수 있는 가장 빠른 하드 디스크만이 단지 SATA/150 링크를 간신히 꽉 채워서 사용하지만, 앞으로는 SATA/300 링크를 꽉 채워서 쓸 수 있는 디스크 드라이브 [스루풋](https://ko.wikipedia.org/wiki/스루풋 "wikilink")이 필요할 것이고, SATA/300이 그것을 만족시켜 줄 것으로 예상한다. 이것은 1.5 Gbits/s용 SATA 데이터 케이블이, 현재 3.0 Gbit/s 드라이브에 연결되어 지속/버스트 데이터 전송에 대해 속도 저하 없이 쓰이고 있는 까닭이기도 하다.

SATA/300과 SATA/150 사이의 하위 호환성은 중요했다. 그래서 SATA/300의 자동 협상 절차(autonegotiation sequence)가 SATA/300의 설계에 들어갔다. SATA/300은 SATA/150 장치(콘트롤러)와 연결될 때에는 SATA/150의 속도(1.5 Gbit/s)로 자동으로 떨어지게 된다. 몇몇의 옛 SATA 콘트롤러는 SATA 자동 속도 협상을 잘 처리하지 못한다. 해당 시스템에서는 3.0 Gbit/s 장치를 1.5 Gbit/s 장치로 설정하기 위해 사용자가 직접 점퍼를 바꿔서 꽂아야 했다. [1](http://www.seagate.com/support/disc/sata/st3160812as.html) 오류가 있는 칩셋으로는 VIA VT8237, VT8237R 사우스 브리지와, VIA VT6420, VT6421L 독립형 SATA 콘트롤러를 꼽을 수 있다.[2](http://wdc.custhelp.com/cgi-bin/wdc.cfg/php/enduser/std_adp.php?p_faqid=1337)

3.0 Gbit/s 규격은 흔히 **시리얼 ATA II**, 또는 **사타 투**()라고도 불린다. 사실 직렬 ATA 표준화 단체에서는 그런 이름을 바라지 않았다. [공식 사이트](http://www.sata-io.org) 에서는 SATA II는 당시 조직 이름이었을 뿐이라고 언급하고 있다. 그리고 SATA 3.0 Gbit/s 규격은 예전에 정의되었던 SATA II 가운데 하나였을 뿐이었다고 하며, SATA II가 아니라 **SATA 3.0 Gbit/s**로 불러줄 것을 요청하고 있다. (직렬 ATA 표준화 단체는 그 뒤에 이름을 바꾸었다. 지금의 이름은 이다. SATA-IO라고 줄여 쓴다.) 대부분의 SATA 드라이브와 콘트롤러 제조 업체에서는 SATA II”라는 용어를 피하고 있다.

SATA 3.0 Gbit/초는 다른 말로 **SATA 3.0**, **SATA/300**이라고도 불린다. ATA/100, ATA/133, SATA/150라고 불리던 관례를 따랐다.

## SATA 6.0 Gbit/s(SATA3)

SATA의 로드맵은 SATA 6.0 Gbit/s 규격을 포함하고 있다. 현재의 PC에서 SATA 3.0 Gbit/s는 벌써 하드 디스크의 최고 전송 속도(버스트 전송을 제외한)를 훨씬 뛰어 넘었기 때문에 6.0 Gbit/s 규격은 하나의 SATA 포트에 여러 개의 드라이브를 연결하는 포트 멀티플라이어에 쓸모 있을 것으로 보인다. 램 드라이브와 같은 [솔리드 스테이트 디스크](https://ko.wikipedia.org/wiki/솔리드_스테이트_디스크 "wikilink")(SSD) 또한 머지 않아 이러한 전송 속도를 개선하는 이득을 볼 것으로 예상된다. 하드 디스크 제조 업체에서 이론적인 버스트 전송 속도를 잘 밝히지 않기 때문에 실생활에서 SATA를 사용하면서 얻는 이득은 더 적은 전력 소모와 케이블, 그리고 [핫 플러그](https://ko.wikipedia.org/wiki/핫_플러그 "wikilink") 정도다. 지금 몇몇 보드에서 지원하고 있다.인텔의 P67,H67,Z68에서 지원하고 AMD는 SB850,A75 사우스브리지가 탑재된 메인보드에서 네이티브로 지원된다 그 외 메인보드는 별도의 컨트롤러에 의한 지원이다.

## SATA에서 달라진 점

SATA는 단지 4 가닥의 신호선을 이용한다. PATA에 비해 작고, 저렴한 케이블을 쓸 수 있게 한다. 또, [핫 스왑이나](https://ko.wikipedia.org/wiki/핫_스왑 "wikilink") [네이티브 커맨드 큐잉](https://ko.wikipedia.org/wiki/네이티브_커맨드_큐잉 "wikilink") 같은 기능을 제공한다.

SATA 드라이브들은 부가적으로 [직렬 부착 SCSI](https://ko.wikipedia.org/wiki/직렬_부착_SCSI "wikilink")(Serial Attached SCSI, SAS) 콘트롤러에 붙일 수 있다. 네이티브 SAS 디스크와 동일한 물리적 케이블을 이용하여 통신한다. 하지만 SAS 디스크들은 SATA 콘트롤러에 붙일 수 없다.

### 케이블과 단자

가장 눈에 띄는 변화는 PATA에 비해 SATA 방식의 전원 케이블과 데이터 케이블이 많이 달라졌다는 것이다. PATA와 달리, 노트북 디스크(2.5인치)든지 데스크톱용 디스크(3.5인치)든지 똑같은 모양의 SATA 커넥터를 쓸 수 있다. 노트북용 하드 디스크를 데스크톱에 연결해도 SATA를 쓰면 따로 어댑터를 사용하지 않아도 된다.

SATA 표준에서는 데이터 케이블을 7 가닥으로 정의한다. (3개는 그라운드이고 4개는 2쌍의 액티브 데이터 선이다.) 양 끝에는 8 밀리미터 너비의 웨이퍼 커넥터가 달린다. SATA 케이블은 약 1 미터 길이까지 허용된다; PATA [리본 케이블은](https://ko.wikipedia.org/wiki/리본_케이블 "wikilink") 대개 40개 혹은 80개의 도선 가닥을 가지고 있고, 46 센티미터 길이까지 허용한다. SATA 커넥터는 밀폐된 공간에 잘 들어맞고, [공기 냉각에](https://ko.wikipedia.org/wiki/공기_냉각 "wikilink") 장애물이 되지 않아 깔끔하다. 하지만 SATA 커넥터는 때때로 의도하지 않게 빠지거나 하드디스크 커넥터 지지대가 부러질수도 있다.

[섬네일](https://ko.wikipedia.org/wiki/파일:SATA_Data_Cable.jpg "wikilink")

  -
    {| class="wikitable"

|- \! 핀 \# \!\! 기능 |- | 1 | 그라운드 |- | 2 | A+ |- | 3 | A- |- | 4 | 그라운드 |- | 5 | B- |- | 6 | B+ |- | 7 | 그라운드 |}

[섬네일](https://ko.wikipedia.org/wiki/파일:SATA_power_cable.jpg "wikilink") SATA 표준에서는, 데이터 케이블 외에도 새로운 [전원 커넥터를](https://ko.wikipedia.org/wiki/전원_커넥터 "wikilink") 규정하고 있다. 데이터 케이블과 마찬가지로 웨이퍼를 기반으로 한다. 15핀이다. 서로 헷갈리지 않게 하였다. 일부 SATA 장치에는 4핀 커넥터\[5V,GND,GND,12V\]를 연결할 수도 있지만 네이티브 SATA 장치에는 PATA에 쓰이던 예전의 4핀 커넥터보다는 SATA 파워 커넥터를 쓰는 것이 낫다. SATA 파워 커넥터는 강도 면에서 문제를 보이기도 한다.(수직이 아닌 방향으로 억지로 빼면, 상단의 플라스틱 덮개가 부러질 수도 있다. 오른쪽 그림 참고) 개수가 많아 보이는 핀들은 세 개의 각각 다른 3.3V, 5V, 12V [전압](../Page/전압.md "wikilink")을 공급할 때 쓰인다. 각 전압은 각각 3개 핀을 합쳐 공급 받는다. 나머지 핀 가운데 5개는 그라운드다. 마지막 11번 핀은 새로 붙는 드라이브를 위한 [스태거드 스핀업에](https://ko.wikipedia.org/wiki/스태거드_스핀업 "wikilink") 사용된다. 전압 공급 핀들은 하나만으로는 충분한 전류를 공급하지 못하므로 다른 두 개 핀과 함께 전력을 공급한다. 3개의 전압 각각에 대한 핀들 가운데 한 개는 컴퓨터가 켜져 있는 동안 장착하고 제거할 수 있는 [핫 플러그](https://ko.wikipedia.org/wiki/핫_플러그 "wikilink") 용도로도 쓰인다.

  -
    {| class="wikitable"

|- \!colspan="2"| 핀 \# \!\! 기능 |- | style="background-color: orange;" | | 1-3 | 3.3 볼트 |- | style="background-color: black;" | | 4-6 | 그라운드 |- | style="background-color: red;" | | 7-9 | 5 볼트 |- | style="background-color: black;" | | 10 | 그라운드 |- | style="background-color: gray;" | | 11 | 스태거드 스핀-업 (지원 드라이브에 한함) |- | style="background-color: black;" | | 12 | 그라운드 |- | style="background-color: yellow;" | | 13-15 | 12 볼트 |}

PATA에서 쓰던 4 핀 커넥터를 SATA 파워 커넥터로 변환해 주는 어댑터가 시중에 나와 있다. 하지만 4 핀짜리 커넥터는 3.3 볼트 전압을 공급해 주지 못하므로, 이를 이용하는 경우 3.3 볼트 전압선은 연결되지 않는다. 따라서 3.3 V 전압이 필요한 드라이브에서는 이러한 어댑터를 쓰지 못한다. 이러한 사정을 감안하여, 하드 디스크 드라이브 제조사들은 3.3 볼트를 잘 안 쓰고 있다. 하지만, 3.3V 전압이 없으면, 앞서 말한 [핫 플러깅을](https://ko.wikipedia.org/wiki/핫_플러깅 "wikilink") 구현하지 못할 가능성이 있다.

## mSATA

[섬네일](https://ko.wikipedia.org/wiki/파일:Hitachi_2.5"_HDD_and_ADATA_XM13_20120402.jpg "wikilink").\]\] 미니 SATA는 2009년 9월 21일 Serial ATA International Organization이 발표한 SATA 방식이다.\[1\] 더 작은 [솔리드 스테이트 드라이브를](../Page/솔리드_스테이트_드라이브.md "wikilink") 요구하는 [노트북](https://ko.wikipedia.org/wiki/노트북 "wikilink") 등의 장치에 어울린다. 단자는 [PCI 익스프레스 미니 카드](../Page/PCI_익스프레스.md "wikilink") 인터페이스와 모양이 비슷하지만, 전자적으로 호환되지 않는다. 그러나 데이터 신호(TX±/RX± SATA, PETn0 PETp0 PERn0 PERp0 PCI-express)는 PCI 익스프레스 호스트 컨트롤러가 아닌 SATA 호스트 컨트롤러의 연결이 필요하다. miniSATA 방식과 microSATA 방식으로 나뉜다.

## 외장 SATA

2004년 중반, **외장 SATA**(, **eSATA**)가 표준이 되었다. 다른 종류의 케이블과 커넥터를 사용하도록 규정하였고, 전기적 요구 사양도 외장 용도에 맞게 개정하였다:

  - 최소 송신 전압이 늘어났다: 범위가 400-600 mV 에서 500–600 m[볼트](../Page/볼트_\(단위\).md "wikilink") 로 조정되었다.
  - 최소 수신 전압이 줄었다: 범위가 325-600 mV 에서 240–600 mV 로 조정되었다.
  - 프로토콜과 논리 시그널링은 SATA와 같다. (링크-트랜스포트 계층과 그 이상의 계층을 말한다.) 네이티브 SATA 장치가 최소한의 변경만으로 외장 인클로저에 담겨 쓰일 수 있도록 해 준다.
  - 케이블 길이는 최대 2 미터다. ([USB](../Page/USB.md "wikilink")와 [파이어와이어](https://ko.wikipedia.org/wiki/파이어와이어 "wikilink")가 더 길다.)

## 같이 보기

  - [AHCI](https://ko.wikipedia.org/wiki/AHCI "wikilink")
  - [ATA](../Page/병렬_ATA.md "wikilink")
  - [VTL](https://ko.wikipedia.org/wiki/가상_테이프_라이브러리 "wikilink")

## 각주

## 외부 링크

  - [Serial ATA 국제 기구 ( SATA-IO )](http://www.sata-io.org/)

  - [Dispelling the Confusion: SATA II does not mean 3Gb/s](https://web.archive.org/web/20070707031303/http://www.sata-io.org/namingguidelines.asp)

  - [SATA-IO White Paper - External SATA (eSATA)](https://web.archive.org/web/20070421211342/http://www.sata-io.org/docs/External%20SATA%20WP%2011-09.pdf)

  - [SATA motherboard connector pinout](http://pinouts.ru/HD/serialATA_pinout.shtml)

  - [SATA on Linux](http://linuxmafia.com/faq/Hardware/sata.html)

  - [SATA Linux status report](https://web.archive.org/web/20070312010549/http://linux-ata.org/driver-status.html)

[분류:직렬 버스](https://ko.wikipedia.org/wiki/분류:직렬_버스 "wikilink") [분류:컴퓨터 버스](https://ko.wikipedia.org/wiki/분류:컴퓨터_버스 "wikilink") [분류:컴퓨터 통신](https://ko.wikipedia.org/wiki/분류:컴퓨터_통신 "wikilink")

1.