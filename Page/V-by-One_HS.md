> This article is converted from Wikipedia: [V-by-One HS](https://ko.wikipedia.org/wiki/V-by-One_HS).


**V-by-One HS**는 전기신호를 전송하는 인터페이스의 하나로, 특히 디지털 평판TV향으로 THine Electronics사에 의해 개발 되었다. 현재는 복합기 등의 사무기기, 차량용 인포테인먼트 시스템, 로보트, 시큐리티등 폭 넓은 분야에 적용되고 있다.

종래 디지털 평판TV의 내부배선은 , 영상신호 전송에 [LVDS](https://ko.wikipedia.org/wiki/LVDS "wikilink")가 표준적으로 사용되어 왔으나, 고해상도 Color depth 확장으로 인해 보다 빠른 전송속도 요구와 케이블간의 타이밍문제 (Skew) 가 대두되었다 V-by-One HS는 SerDes이면서 Clock Data Recovery등의 기술을 가미해 1Pair당 3.75Gbps의 고속전송을 실현 하면서, Skew문제를 해결함과 동시에 EMI, 소비전력을 줄이고 있다. 또한 전송 Pair수의 감소로 케이블, 커넥터등의 종합적인 원가절감도 가능해졌다.

## 개요

  - 대형액정디스플레이의 영상입력신호 VESA표준사양인 LVDS를 대체 할 목적으로 개발되었다.
  - 이퀄라이저기능의 도입으로 기존 [LVDS](https://ko.wikipedia.org/wiki/LVDS "wikilink") 대비 전송품질을 향상시켰다.
  - 클럭 Data Recovery 기술의 채용으로 기존 LVDS가 갖고 있던케이블 Skew 문제가 해결 되었다.
  - 종래 [LVDS](https://ko.wikipedia.org/wiki/LVDS "wikilink")가 필요로 했던 클럭전송 케이블 (고정주파수의 전송)이 없어 EMI, Noise가 감소된다
  - 최대 3.75Gbps전송이 가능하여 케이블 수, 커넥터 수가 줄어들고 종합적인 원가절감, 공간절약이 실현가능
  - 전송속도가 고정이 아니므로, 고정주파수를 채택하는 타 인터페이스의 전송사양과 비교시 소비전력이 감소 가능하다. Serial전송속도: 600Mbps～3.75Gbps
  - 종래 [LVDS](https://ko.wikipedia.org/wiki/LVDS "wikilink")설계에서 큰 변경이 없이 [V-by-One HS의](https://ko.wikipedia.org/wiki/V-by-One_HS "wikilink") 설계가 가능하다.
  - 개발사인 THine Electronics사로 부터 사양이 공개되어 Open Standard화 되어 있다.

## 개발까지의 경위

액정 디스플레이는 브라운관 디스플레이와 달라, 개별 픽셀을 표시하는 신호는 반드시 디지털 신호이어야만 한다.

액정 디스플레이가 Notebook PC에 응용되었던 당시 영상신호는 Parallel신호로 전송되었으나 18bit Color의 Color Depth에서도 RGB 6개씩과 제어신호 3개의 클럭을 포함하여 22개의 신호선이 필요하게 되어, 배선공간과 Skew조정에 어려운 문제가 있었다.

이러한 문제를 해결하기 위하여, 액정 디스플레이의 인터페이스로서 [LVDS](https://ko.wikipedia.org/wiki/LVDS "wikilink")의 응용이 고안되었다. [LVDS](https://ko.wikipedia.org/wiki/LVDS "wikilink")는 TIA/EIA-644에서 규격화 된 차동전송방식으로 고속화가 가능하기에 액정 디스플레이에서는 영상신호를 Serial화 해서 전송한다. 도입 당시는 18bit Color가 주류였기에 RGB 각각 6bit와 제어신호 3bit, 합계 21bit를 3ch의 차동신호 Pair에 7bit씩 나눠서, 클럭 1ch와 같이 4pair의 배선으로 Serial 전송 하는 사양으로 제안 되었다. 결국, Parallel통신에서는 22개나 필요했던 배선이 8개 Serial통신으로 가능하게 되었다. 이 방식이 비디오 주변기기관련 업계 표준화 단체인 [VESA](https://ko.wikipedia.org/wiki/VESA "wikilink")에 표준사양으로 채용되어 액정 디스플레이향 인터페이스로서 [LVDS](https://ko.wikipedia.org/wiki/LVDS "wikilink")가 널리 보급되게 되었다.

그 후 액정 디스플레이의 고해상도와 Color Depth확장이 진행되었고, 또한 액정 디스플레이의 결점이었던 응답속도의 향상을 위하여 2배속 또는 4배속구동 기술이 도입되어 액정 디스플레이에 입력해야 할 영상신호의 데이터양은 늘어나기만 했다. 그 결과 예를 들어 Full HD (1920×1080)에서 10bit Color Depth의 120Hz Panel에서는 [LVDS](https://ko.wikipedia.org/wiki/LVDS "wikilink")라도 24Pair, 48개의 배선이 필요하게 되었다. 전송 클럭도 고속화 되어 수백ps 정도의 Skew조정이 필요하게 되었다. 또한 기존 [LVDS](https://ko.wikipedia.org/wiki/LVDS "wikilink")의 사양에서는 고정주파수의 클럭전송이 필요하고 스펙트럼이 집중되기 때문에 무선 LAN등에 영향을 주지 않도록 EMI의 제거가 필요하다.

또한 [LVDS](https://ko.wikipedia.org/wiki/LVDS "wikilink")는 규격상 GND에서 1.2V의 전압을 중심으로 변화하는 전기신호를 전송 해야만 한다. LSI의 미세화가 진행되면서 이 전압의 규격이 [LSI](https://ko.wikipedia.org/wiki/LSI "wikilink") 설계상의 큰 제한을 가져오게 되었다. 이러한 상황에서 [DVI](https://ko.wikipedia.org/wiki/DVI "wikilink")와 [HDMI](https://ko.wikipedia.org/wiki/HDMI "wikilink"), [DisplayPort](https://ko.wikipedia.org/wiki/DisplayPort "wikilink")라 불리는 여러가지 인터페이스사양이 제안되어 실용화 되어왔다.

DVI와 [HDMI](https://ko.wikipedia.org/wiki/HDMI "wikilink")는 Skew조정 기능이 있고, [HDMI](https://ko.wikipedia.org/wiki/HDMI "wikilink")에는 컨텐츠보호기능으로 HDCP가 내장되어 있기 때문에 기기간의 영상신호 전송에는 최적으로 널리 보급 되었으나, 내장 하는데 라이센스 비용이 필요하고, 기기내부의 영상신호 전송으로는 기능이 과도하고, 소비전력도 커서 채용된 사례는 없었다.

[DisplayPort](https://ko.wikipedia.org/wiki/DisplayPort "wikilink")는 VESA에서 [LVDS](https://ko.wikipedia.org/wiki/LVDS "wikilink")를 대체할 수 있는 사양으로 규격화 된 것으로 향후 보급에 기대를 하고 있다. 전송방식의 사양은 PCI Express에 유사한 Bias로 되어 있어 LSI설계상 장벽이 낮아졌다. 그러나 [HDMI](https://ko.wikipedia.org/wiki/HDMI "wikilink")와 마찬가지로 외부기기 간 전송을 고려하여 HDCP가 내장되어 있기에 기기내부의 영상신호 전송으로는 기능이 과도하며 소비전력이 증대가 우려되고 있다. 또한 [DisplayPort](https://ko.wikipedia.org/wiki/DisplayPort "wikilink")는 전송속도가 고정이어서 여러가지 클럭주파수가 존재하는 영상신호에 대해서 낮은 주파수에서는 손실이 발생하여 수신측에서는 클럭을 재생 할 필요가 있다. 이러한 이유로 [LVDS](https://ko.wikipedia.org/wiki/LVDS "wikilink")에서 해결 해야 할 과제는 많다.

상기의 배경에 근거하여 V-by-One HS의 개발이 진행 되었다. 즉 이퀄라이저기능의 도입으로 기존의 [LVDS](https://ko.wikipedia.org/wiki/LVDS "wikilink")와 비교해 전송품질이 향상되고, 고속화 (최대1Pair당 3.75Gbps)를 실현했다. 또한 Clock Data Recovery의 채용으로 기존에 LVDS에서 문제화 되었던 케이블 Skew의 문제를 해결했다. 그리고 [LVDS](https://ko.wikipedia.org/wiki/LVDS "wikilink")에서 필요로 했던 클럭전송(고정주파수의 전송)이 필요없기 때문에 EMI Noise가 감소되었다.

전송속도의 고속화로 케이블 배선수와 커넥터수를 줄여 종합적인 원가가 절감되고, 공간절약등이 가능할 것으로 기대되고 있다. 예를 들면 Ultra Display Panel (3840×2160)에서는 [LVDS](https://ko.wikipedia.org/wiki/LVDS "wikilink")를 이용하면 96Pair의 케이블이 필요하나, V-by-One HS에서는 16Pair로 전송이 가능하다. 또한 전송속도가 가변이기 때문에 기존의 [LVDS](https://ko.wikipedia.org/wiki/LVDS "wikilink") 설계에서 큰 변경없이 V-by-One HS로 설계가 가능하다. 개발사인 [THine Electronics사에서](https://ko.wikipedia.org/wiki/THine_Electronics "wikilink") 사양이 공개되어 Open Standard화가 되어있다.

## 외부 링크

  - [V-by-One® HS Standard](https://web.archive.org/web/20120617024235/http://www.thine.co.jp/products_e/V-by-One_HS/)
  - [THine Electronics](https://web.archive.org/web/20120719050310/http://www.thine.co.jp/index_e.php)

[분류:컴퓨터 버스](https://ko.wikipedia.org/wiki/분류:컴퓨터_버스 "wikilink") [분류:텔레비전 기술](https://ko.wikipedia.org/wiki/분류:텔레비전_기술 "wikilink") [분류:영상 기술](https://ko.wikipedia.org/wiki/분류:영상_기술 "wikilink") [분류:텔레비전 용어](https://ko.wikipedia.org/wiki/분류:텔레비전_용어 "wikilink") [분류:표준](https://ko.wikipedia.org/wiki/분류:표준 "wikilink")