> This article is converted from Wikipedia: [PCSX2](https://ko.wikipedia.org/wiki/PCSX2).


**PCSX2**는 [마이크로소프트 윈도와](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") [리눅스](../Page/리눅스.md "wikilink") [운영 체제용](../Page/운영_체제.md "wikilink") [플레이스테이션 2](../Page/플레이스테이션_2.md "wikilink")(PS2) [에뮬레이터](../Page/에뮬레이터.md "wikilink")이다. 최근 버전에서는 상당 수의 PS2 게임들이 작동 가능하며 (속도 문제로 게임을 즐기기에 현실적으로 어려운 경우가 있지만, 점차 개선중에 있다.), 일부 게임은 완벽하게 실행된다고 한다.

PCSX2 는 전작인 [PCSX](../Page/PCSX.md "wikilink")와 마찬가지로 플러그인 구조 기반이므로, 일부 기능은 핵심 에뮬레이터에서 분리되어있다. 분리된 기능은 그래픽, 조작, CD/DVD 드라이브, [USB](../Page/USB.md "wikilink"), 음성, [IEEE 1394](../Page/IEEE_1394.md "wikilink") 포트 관련 부분이다. 다른 플러그인을 이용하는 것은 호환성이나 성능 면에서 차이를 불러올 수 있다. PCSX2의 작동을 위해서는 PS2 바이오스의 복사본이 필요한데, 개발자는 저작권이나 법적 문제를 피하기 위해 이를 소프트웨어에 포함하지 않고 있다.

공식 사이트는 [1](http://pcsx2.net/) 에서 자세한 확인을 할 수 있으며, 개발 사이트는 \[[http://code.google.com/p/pcsx2/\]에서](http://code.google.com/p/pcsx2/%5D에서) 현재 최신 리버전이 올라오고 있다.

현재 2 코어를 완벽하게 지원하며, 최근에 들어서야 SVN R4865 버전 이후부터는 MTVU (Multi-Threaded microVU1) 기능이 추가되어 트리플 코어 이상 및 CPU 에서 [멀티 스레드를](https://ko.wikipedia.org/wiki/멀티스레드 "wikilink") 다양하게 사용이 가능해졌다. 그렇기 때문에 트리플 코어 이상에서의 프레임 향상 및 [EE](https://ko.wikipedia.org/wiki/EE "wikilink") 사용률이 많이 낮아지는 효과가 있으나 단점으로는 [GS](https://ko.wikipedia.org/wiki/GS "wikilink") 사용률 (그래픽 사용률) 이 급격하게 높아진다는 점이다. 그래픽 성능이 떨어지는 사양으로 이 기능을 사용할 시 속도상승 효과가 나타나지 않는 문제가 있으며, 초기단계인 관계로 일부 타이틀에선 안정적인 [프레임](https://ko.wikipedia.org/wiki/프레임 "wikilink") 유지가 어려운 현상이 나타나기도 한다. 그러나 물리적인 [코어](https://ko.wikipedia.org/wiki/코어 "wikilink") 프로그래밍이 아닌 멀티스레드 프로그래밍으로써 PCSX2 의 쿼드이상의 코어가 제대로 적용된 것은 아니다. 그러므로 그 이상의 [쿼드 코어를](https://ko.wikipedia.org/wiki/쿼드_코어 "wikilink") 지원하지 않은 상태이며, 제작자는 차후에 추가하겠다고 포럼에서 밝혔다. 여담으로 사용하고자 하는 pc가 고사양이더래도, 일부 다수의 게임들이 에뮬에 최적화가 안된 나머지 과거와는 달리 프레임 드랍현상은 없으나, 그래픽 깨짐현상 및 기타 여러문제가 확인되고 있는 실정이다. 간혹 PCSX2로만 꼭 플레이 하여야겠다는 강박관념을 가진 유저들이 있다지만, 이러한 문제들에 대해서는 제작자측이 해당 게임에 대해 최적화를 해주지 않는 이상, 위 고질적인 문제들은 에뮬의 버전업이 되어도 여전히 해결되지 않을것으로 보이며, 해결방법은 최적화를 기다리며 플레이에 지장이 없을정도의 문제라면 문제점을 무시하고 그냥 플레이를 하든가, 아니면 PS2를 중고로 구입하여 플레이 하는 것이 가장 바람직하다고 본다.

## 사양

**최소사양**

  - 윈도 운영 체제 및 [리눅스](../Page/리눅스.md "wikilink") 운영 체제
  - [CPU](../Page/중앙_처리_장치.md "wikilink") : [SSE2](../Page/SSE2.md "wikilink") 명령어 지원 가능 및 인텔 [펜티엄 4](../Page/펜티엄_4.md "wikilink") 이상, AMD [애슬론 64](../Page/애슬론_64.md "wikilink") 이상
  - [GPU](../Page/그래픽_처리_장치.md "wikilink") : [셰이더](../Page/셰이더.md "wikilink") 모델 2.0 지원 이상 (단, 엔비디아 [지포스 FX](https://ko.wikipedia.org/wiki/지포스_FX "wikilink") 시리즈는 셰이더 모델 2.0 은 제대로 지원하지 않기 때문에 제외 대상)
  - 메모리 512MB 이상 (비스타 운영 체제 일 경우 최소 메모리 2GB 용량이 필요)

**권장사양**

  - [윈도 비스타](https://ko.wikipedia.org/wiki/윈도_비스타 "wikilink") 및 [윈도 7](https://ko.wikipedia.org/wiki/윈도_7 "wikilink") (32비트 또는 64비트) 와 함께 [DirectX](../Page/DirectX.md "wikilink") 런타임 최신 버전 요구.
  - CPU : [인텔 코어 2](../Page/인텔_코어_2.md "wikilink") 듀오 @ 3.2Ghz 클럭 이상

(PCSX2 에뮬은 오로지 CPU클럭빨이라는 거짓된 정보를 믿어선 아니된다. 높은3D 텍스쳐를 요구하는 타이틀일수록 CPU 의존도와 더불어 VGA 의 의존도도 높으며 VGA의 성능이 이를 뒷받침해 주지 못함으로 인한 병목현상 즉 프레임 저하현상이 나타나기도 한다.)

  - GPU : 엔비디아 지포스 8800GT 및 라데온 HD4850 이상 (DirectX 10 이상 지원)
  - 윈도 XP 또는 리눅스 운영 체제일 경우, 메모리 1GB 이상 ([윈도 비스타](https://ko.wikipedia.org/wiki/윈도_비스타 "wikilink") 및 [윈도 7](https://ko.wikipedia.org/wiki/윈도_7 "wikilink") 일 경우, 메모리 2GB 이상을 권장)

## 같이 보기

  - [PCSX](../Page/PCSX.md "wikilink")

## 외부 링크

  - [공식 웹사이트](http://www.pcsx2.net)

  - [PCSX2 프로젝트 페이지](http://code.google.com/p/pcsx2/) - [구글 코드](https://ko.wikipedia.org/wiki/구글_코드 "wikilink")

[분류:에뮬레이션 소프트웨어](https://ko.wikipedia.org/wiki/분류:에뮬레이션_소프트웨어 "wikilink") [분류:C++로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C++로_작성된_자유_소프트웨어 "wikilink") [분류:GPL 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:GPL_라이선스_소프트웨어 "wikilink") [분류:자유 에뮬레이션 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_에뮬레이션_소프트웨어 "wikilink")