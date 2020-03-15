> This article is converted from Wikipedia: [FPGA](https://ko.wikipedia.org/wiki/FPGA).


[섬네일](https://ko.wikipedia.org/wiki/파일:알테라_사이클론2_FPGA.jpg "wikilink") 사이클론2 FPGA 칩\]\] **FPGA**(, 필드 프로그래머블 게이트 어레이)는 [설계 가능 논리 소자와](../Page/설계_가능_논리_소자.md "wikilink") 프로그래밍이 가능한 내부 회로가 포함된 [반도체](https://ko.wikipedia.org/wiki/반도체 "wikilink") 소자이다. 설계 가능 논리 소자는 [AND](https://ko.wikipedia.org/wiki/논리곱_소자 "wikilink"), [OR](https://ko.wikipedia.org/wiki/논리합_소자 "wikilink"), [XOR](https://ko.wikipedia.org/wiki/배타적_논리합_소자 "wikilink"), [NOT](https://ko.wikipedia.org/wiki/부정_소자 "wikilink"), 더 복잡한 디코더나 계산기능의 [조합 기능같은](https://ko.wikipedia.org/wiki/조합_논리 "wikilink") 기본적인 [논리 게이트의](https://ko.wikipedia.org/wiki/논리_게이트 "wikilink") 기능을 복제하여 프로그래밍할 수 있다. 대부분의 FPGA는 프로그래밍 가능 논리 요소 (FPGA 식으로는 논리 블록이라고도 함)에 간단한 [플립플롭](https://ko.wikipedia.org/wiki/플립플롭 "wikilink")이나 더 완벽한 메모리 블록으로 된 메모리 요소를 포함하고 있다.

프로그램이 가능한 내부선 계층구조는 FPGA의 논리블록을 시스템 설계자가 요구하는 대로 단일 칩 프로그래밍가능 [브레드보드](https://ko.wikipedia.org/wiki/브레드보드 "wikilink")처럼 내부연결을 할 수 있다. 이 논리블록과 내부선은 제조공정 이후에 소비자/설계자가 프로그램할 수 있으므로 요구되는 어떠한 논리기능도 수행할 수 있다.(그러한 이유로 "현장 프로그래머블")

FPGA는 일반적으로 [주문형 반도체](../Page/주문형_반도체.md "wikilink")(ASIC) 대용품보다 느리고, 복잡한 설계에 적용할 수 없으며, 소비전력이 크다. 그러나 [개발시간](https://ko.wikipedia.org/wiki/개발시간 "wikilink")이 짧고, 오류를 현장에서 재수정할 수 있고, [초기 개발비가](https://ko.wikipedia.org/wiki/초기_개발비 "wikilink") 저렴하다는 장점이 있다. 제조사는 설계 이후에 수정할 수 없도록 할당된 덜 유연한 FPGA 버전으로 싸게 팔 수 있다. 이런 설계개발은 일반적인 FPGA에서 만들었고 좀 더 ASIC와 비슷한 고정된 버전으로 변경되었다. [CPLD](https://ko.wikipedia.org/wiki/CPLD "wikilink")는 비슷한 역할을 할 수 있는 소자이다.

## 역사

FPGA의 역사적 근원은 1980년대초의 [복합 프로그래머블 논리 소자](https://ko.wikipedia.org/wiki/복합_프로그래머블_논리_소자 "wikilink") (CPLD)이다. [자일링스](https://ko.wikipedia.org/wiki/자일링스 "wikilink") 공동 창립자인 [로스 프리맨](https://ko.wikipedia.org/wiki/로스_프리맨 "wikilink") ()은 1984년에 FPGA를 발명하였다. FPGA는 [CPLD](https://ko.wikipedia.org/wiki/CPLD "wikilink")보다 상대적으로 프로그램되는 논리 요소가 많다. [CPLD](https://ko.wikipedia.org/wiki/CPLD "wikilink")에는 수천에서 수만의 논리 게이트가 있지만, FPGA에는 일반적으로 수만에서 수백만의 논리 게이트가 있다.

CPLD와 FPGA의 가장 큰 차이점은 구조적인 차이이다. CPLD는 하나 이상의 프로그램되는 상대적으로 적은 수의 동기 [레지스터를](https://ko.wikipedia.org/wiki/하드웨어_레지스터 "wikilink") 제공하는 곱의 합 논리 어레이로 구성된 제한적인 구조이다. 이러한 것은 지연을 더 예측가능하게 하고 논리-내부선 속도를 더 빠르게 하지만 유연성이 떨어진다. 반대로 FPGA 구조는 내부선에 따라 결정된다. 내부선은 FPGA를 (내부적으로 동작하는 실제적인 설계범위의 기간에) 더 유연하고 설계에 더 복합적으로 만든다.

다음으로 큰 CPLD와 FPGA의 차이점은 높은 수준의 내장 기능 (가산기와 곱셈기)과 내장 메모리의 존재여부이다. 또한 대부분의 FPGA는 완전히 혹은 부분적으로 시스템상에서 재설정을 지원하며 이들의 설계를 시스템 향상이나 시스템 동작의 일반적인 부분처럼 동적 재설정하여 "즉흥적으로" 변경하는 것을 가능하게 한다. 어떤 FPGA에는 다른 부분이 계속 동작하는 동안 소자의 일부분을 재프로그램하는 [부분적 재설정의](https://ko.wikipedia.org/wiki/부분적_재설정 "wikilink") 기능이 있다.

## 현대의 개발

최근 경향은 성긴(coarse-grained) 구조적 접근을 채택하고 있다. 이는 임베디드 프로세서와 관련 주변기기를 전통적인 FPGA의 논리블록과 내부선에 조합하여, 완전한 "프로그래머블칩 시스템"을 만드는 것이다. 이런 하이브리드 기술의 예로는 자일링스 버텍스2 프로, 버텍스4 소자, 그리고 한 개이상의 PowerPC 프로세서가 FPGA의 논리 구조에 내장된 것을 들 수 있다. 아트멜 FPSLIC도 이런 소자 중 하나며, 아트멜의 프로그래머블 논리 구조와 조합되어 [AVR](https://ko.wikipedia.org/wiki/아트멜_AVR "wikilink") 프로세서를 사용한다. 또 다른 접근은 내부 FPGA 논리로 구현된 "소프트" 프로세서 [코어를](https://ko.wikipedia.org/wiki/반도체_지적_재산_코어 "wikilink") 쓰는 것이다. 이런 코어들로는 제 3자의 (상업용이거나 무료인) 프로세서 코어로 알려진, 자일링스 [매크로블래이즈](https://ko.wikipedia.org/wiki/매크로블래이즈 "wikilink")와 [피코블래이즈](https://ko.wikipedia.org/wiki/피코블래이즈 "wikilink"), [알테라](https://ko.wikipedia.org/wiki/알테라 "wikilink") 나이오스와 나이오스2 프로세서, 오픈 소스 [래티스미코32](http://www.latticesemi.com/products/intellectualproperty/ipcores/mico32/index.cfm/)와 [래티스미코8](http://www.latticesemi.com/products/intellectualproperty/referencedesigns/8bitmicrocontrollermico8.cfm/)등이 있다. 중앙 처리 장치 구조가 내장된 하드 중앙 처리 장치 코어는 소프트코어 중앙 처리 장치보다 성능이 우월할 것이다. (예시: 중앙 처리 장치의 프로그래머블 논리 실행)

이전에 언급했듯이 대다수 현대의 FPGA는 "동작 시간" 동안에 재프로그램할 수 있고, [리컨피규러블 컴퓨팅이나](https://ko.wikipedia.org/wiki/리컨피규러블_컴퓨팅 "wikilink") 즉시 태스트를 적용하도록 재설정하는 [리컨퓨규러블 시스템](https://ko.wikipedia.org/wiki/리컨퓨규러블_시스템 "wikilink") — [중앙 처리 장치의](https://ko.wikipedia.org/wiki/중앙_처리_장치 "wikilink") 아이디어를 이끌었다. 그러나, 현대의 FPGA 도구는 이런 방법론을 완벽하게 지원하지 않는다.

덧붙여 지금은 비FPGA 구조가 나오기 시작했다. [Stretch S5000같은](https://ko.wikipedia.org/wiki/Stretch_S5000 "wikilink") 소프트웨어로 설정되는 [마이크로프로세서](https://ko.wikipedia.org/wiki/마이크로프로세서 "wikilink")는 하나의 칩에 프로세서 코어 어레이와 FPGA같은 프로그래머블 코어를 제공함으로써 하이브리드 접근이 도입된다. (현장 프로그래머블 오브젝트 어레이 () 같은) 다른 소자는 FPGA의 논리블록과 복합 프로세서 중간상태로 높은수준의 프로그래머블 오브젝트 어레이를 제공한다.

## 응용

FPGA의 응용으로 [디지털 신호 프로세서](https://ko.wikipedia.org/wiki/디지털_신호_프로세서 "wikilink") (DSP), [소프트웨어로 정의된 라디오](https://ko.wikipedia.org/wiki/소프트웨어로_정의된_라디오 "wikilink"), [우주과학](https://ko.wikipedia.org/wiki/우주과학 "wikilink")과 [방어](https://ko.wikipedia.org/wiki/방어_\(군대\) "wikilink") 시스템, [주문형 반도체](../Page/주문형_반도체.md "wikilink") ([ASIC](https://ko.wikipedia.org/wiki/ASIC "wikilink")) 초기버전, [의료 영상](https://ko.wikipedia.org/wiki/의료_영상 "wikilink"), [컴퓨터 비전](https://ko.wikipedia.org/wiki/컴퓨터_비전 "wikilink"), [음성 인식](https://ko.wikipedia.org/wiki/음성_인식 "wikilink"), [암호학](https://ko.wikipedia.org/wiki/암호학 "wikilink"), [생물정보학](https://ko.wikipedia.org/wiki/생물정보학 "wikilink"), [컴퓨터 하드웨어 에뮬레이터와](https://ko.wikipedia.org/wiki/에뮬레이터 "wikilink") 성장하는 다른영역에 사용된다. FPGA는 [복합 프로그래머블 논리 소자의](https://ko.wikipedia.org/wiki/복합_프로그래머블_논리_소자 "wikilink") 경쟁소자로 처음에 시작되었고, [PCB에서](https://ko.wikipedia.org/wiki/인쇄_회로_기판 "wikilink") [글루 논리의](https://ko.wikipedia.org/wiki/글루_논리 "wikilink") 비슷한 크기로 경쟁하였다. 용량 및 속도가 향상되어 어떤 것은 완전한 칩의 시스템 ([SOC](https://ko.wikipedia.org/wiki/단일_칩_시스템 "wikilink"))처럼 지금 판매되는 상황으로 더욱 더 큰 기능을 넘어서기 시작했다.

FPGA는 어떤 영역이나 구조에 따라 제공된 거대 병렬 알고리즘에 특히 유용하다. 이 중 하나는 암호 체계에 대한 [무차별 대입 공격](https://ko.wikipedia.org/wiki/무차별_대입_공격 "wikilink") () 암호해독기이다.

## 구조

일반적인 기본 구조는 컨피규러블 논리 블록 () 어레이와 라우팅 채널로 구성된다. 다중 [I/O 패드는](https://ko.wikipedia.org/wiki/I/O_패드 "wikilink") 한행의 높이나 한열의 너비에 적합할지도 모른다. 일반적으로 모든 라우팅 채널은 동일한 (전선수) 폭을 가지고 있다.

응용회로는 적합한 자원을 가지는 FPGA를 반드시 매핑해야한다.

일반적인 FPGA의 논리 블록은 아래에 보이는 것처럼 4개의 입력 [룩업 테이블](https://ko.wikipedia.org/wiki/룩업_테이블 "wikilink") ()과 [플립플롭](https://ko.wikipedia.org/wiki/플립플롭 "wikilink")으로 구성된다.

[frame](https://ko.wikipedia.org/wiki/파일:Logic_block.gif "wikilink")

레지스터나 언레지스터 룩업 테이블이 가능한 하나의 출력만 있다. 논리 블록에는 룩업 테이블을 위한 4개의 입력과 클럭 입력이 있다. 클럭 신호 (와 높은 [팬 아웃](https://ko.wikipedia.org/wiki/팬_아웃 "wikilink") 신호)는 일반적으로 특별용도 전용 라우팅망을 통하여 연결되고 다른 신호는 분리하여 관리하기 때문이다.

이 예시구조로 FPGA의 논리 블록 핀 위치는 아래와 같이 보인다. [frame](https://ko.wikipedia.org/wiki/파일:logic_block_pins.svg "wikilink")

각 입력은 출력핀이 바로 연결된 채널과 논리 블록을 통한 채널으로된 라우팅 전선을 연결할 수 있는 동안에 논리 블록의 한면으로 접근할 수 있다.

각 논리 블록 출력핀은 이렇게 이웃한 채널에서 분할된 전선 중 하나를 연결할 수 있다.

비슷하게 I/O 패드도 이렇게 이웃한 채널에서 분할된 전선중 하나를 연결할 수 있다. 예시로 칩의 맨위에 있는 I/O 패드는 바로 밑의 수평 채널에 있는 W 전선 (W는 채널 폭임)의 어떤것과 연결할 수 있다.

일반적으로 FPGA의 라우팅은 분할되지 않는다. 각 전선의 분할은 스위치 상자로 차단되기 이전에 하나의 논리 블록과 연결되어 있다. 스위치 상자 내부의 프로그래머블 스위치를 켜서 긴 라인을 구성할 수 있다. 고속의 내부선을 위해서 FPGA의 구조는 다중의 논리 블록과 연결된 긴 라우팅 라인을 사용한다.

어떤 수평 채널이나 수직 채널도 스위치 상자를 교차한다. 이 구조에서 전선이 스위치 상자로 들어갈 때 인접한 채널 분할에서 3개의 다른 전선을 연결할 수 있는 3개의 프로그래머블 스위치가 있다. 이 구조에서 사용되는 스위치의 패턴이나 위상은 평면이나 도메이기반의 스위치 상자 위상이다. 스위치 상자 위상에서 트랙 숫자 1의 전선은 인접한 채널 분할에 있는 트랙 숫자 1의 전선에만 연결되고, 트랙 숫자 2의 전선은 트랙 숫자 2의 다른전선에만 연결되며 이렇게 반복 연결된다. 아래의 그림은 스위치 상자에 있는 연결을 설명한다.

[frame](https://ko.wikipedia.org/wiki/파일:switch_box.svg "wikilink") 현대의 FPGA 계열은 반도체 공정 기술의 발전에 의해 높은 수준의 기능들을 가지게 되었으며, 초기 버전보다 속도와 기능이 향상되었다. 이런 기능들로는 곱셈기, 일반적인 DSP 블록, 임베디드 프로세서, 고속 IO 논리, 임베디드 메모리 등을 들 수 있다.

FPGA는 이전 실리콘의 유효성, 이후 실리콘의 유효성, 펌웨어 개발을 포함하여 시스템 유효성 검사에 널리 사용되고 있다. 칩이 공장에서 생산되기 이전에 설계를 검증하는 칩 회사가 생겨서 개발시간이 짧아졌다.

## FPGA 설계와 프로그래밍

FPGA의 동작 정의를 위해서 사용자에게 [하드웨어 기술 언어](https://ko.wikipedia.org/wiki/하드웨어_기술_언어 "wikilink") (HDL)나 [도면](https://ko.wikipedia.org/wiki/도면 "wikilink") 설계를 제공하고 있다. 일반적인 하드웨어 기술 언어는 [VHDL](https://ko.wikipedia.org/wiki/VHDL "wikilink")과 [베릴로그](https://ko.wikipedia.org/wiki/베릴로그 "wikilink")가 있다. [전자 설계 자동화](https://ko.wikipedia.org/wiki/전자_설계_자동화 "wikilink") 도구를 사용하면 기술적으로 매핑된 [넷리스트](https://ko.wikipedia.org/wiki/넷리스트 "wikilink")가 생성된다. 넷리스트는 [배치와 배선라고](https://ko.wikipedia.org/wiki/배치와_배선 "wikilink") 불리는 작업을 통해 실제 FPGA에 적합하게 할 수 있으며, 일반적으로 FPGA 회사 자산인 배치와 배선 소프트웨어로 수행한다. 사용자는 맵, [타이밍 분선을](https://ko.wikipedia.org/wiki/타이밍_분선 "wikilink") 통한 배치와 배선, [시뮬레이션](https://ko.wikipedia.org/wiki/시뮬레이션 "wikilink"), 다른 [검증](https://ko.wikipedia.org/wiki/검증 "wikilink") 방법론으로 검증할 것이다. 한번 설계와 검증 과정이 완료되면, (FPGA 회사 자산 소프트웨어를 사용하여) 생성된 이진 파일을 FPGA의 (재)설정에 사용한다.

하드웨어 기술 언어들을 도입함으로써 [어셈블리어](https://ko.wikipedia.org/wiki/어셈블리어 "wikilink")와 비교해서 설계의 복잡성을 감소시키는 경향으로 설계를 추상적인 수준으로 끌어올린다. [캐던시 디자인 시스템](https://ko.wikipedia.org/wiki/캐던시_디자인_시스템 "wikilink"), [시놉시스](https://ko.wikipedia.org/wiki/시놉시스 "wikilink"), [셀록시카](https://ko.wikipedia.org/wiki/셀록시카 "wikilink") 같은 회사들은 전통적인 하드웨어 기술 언어를 사용하여 가능한것보다 FPGA 설계 주기를 더 빠르게 가능한 병행 모델을 갖는 높은 수준 언어를 조합하는 방법으로 [시스템C](https://ko.wikipedia.org/wiki/시스템C "wikilink")를 선전하였다. (라이브러리나 다른 확장이 되는 병렬 프로그래밍을 가지는) 표준 [C나](https://ko.wikipedia.org/wiki/C_\(프로그래밍_언어\) "wikilink") [C++](https://ko.wikipedia.org/wiki/C++ "wikilink") 기반의 접근은 [멘토 그래픽스의](https://ko.wikipedia.org/wiki/멘토_그래픽스 "wikilink") 캐터펄트 C 도구나 임펄스 가속 기술의 [임펄스 C](https://ko.wikipedia.org/wiki/임펄스_C "wikilink") 도구들이 발견된다. 아나폴리스 마이크로 시스템 ()의 코어파이어 디자인 슈트는 높은 수준 설계 엔트리에 그림형태의 [데이터흐름](https://ko.wikipedia.org/wiki/데이터흐름 "wikilink") 접근을 제공한다. [시스템베릴로그](https://ko.wikipedia.org/wiki/시스템베릴로그 "wikilink"), [시스템VHDL](https://ko.wikipedia.org/wiki/시스템VHDL "wikilink"), ([셀록시카](https://ko.wikipedia.org/wiki/셀록시카 "wikilink")로부터) [헨델 C같은](https://ko.wikipedia.org/wiki/헨델_C "wikilink") 언어들은 동일한 목적을 성취하려고 추구하였지만 생산된 현재의 하드웨어 공학은 더 생산적인것과 생산된 FPGA는 현재의 소프트웨어 공학에 더 접근하는 게 목적이다.

FPGA에서 복잡한 시스템의 설계를 간단히 하려고 설계 과정을 빠르게 검증하고 최적화한 미리 정의된 복잡한 기능과 회로의 라이브러리가 존재한다. 미리 정의된 회로는 일반적으로 “[IP 코어](https://ko.wikipedia.org/wiki/반도체_지적재산_코어 "wikilink")”라고 불리고 (드물게 자유 라이선스와 일반적으로 사유 라이선스로 공개한) FPGA 제조사와 제 3의 IP 공급자에게서 제공받을 수 있다. 다른 미리 정의된 회로는 (일반적으로 “[자유 소프트웨어](https://ko.wikipedia.org/wiki/자유_소프트웨어 "wikilink")", [GNU 일반 공중 사용 허가서](https://ko.wikipedia.org/wiki/GNU_일반_공중_사용_허가서 "wikilink"), [BSD 사용 허가서와](https://ko.wikipedia.org/wiki/BSD_사용_허가서 "wikilink") 비슷한 라이선스로 공개한) [오픈코어](http://www.opencores.org/)와 다른 제공 커뮤니티같은 개발자 커뮤니티로부터 제공받을 수 있다.

일반적인 설계 흐름에서 FPGA 응용 개발자는 설계과정을 거치며 여러 단계에서 설계를 시뮬레이션할 것이다. 초기에 [VHDL](https://ko.wikipedia.org/wiki/VHDL "wikilink")이나 [Verilog (베릴로그)로](https://ko.wikipedia.org/wiki/Verilog_\(베릴로그\) "wikilink") 된 [RTL](https://ko.wikipedia.org/wiki/RTL "wikilink") 기술은 시스템을 시뮬레이션하고 결과를 관측하기 위해 생성된 테스트 벤치에 따라 시뮬레이션한다. 그런 다음 합성 엔진은 설계를 넷리스트에 매핑한후 넷리스트는 게이트 수준 기술로 번역하며 시뮬레이션은 합성을 진행하는 중에 오류가 없는지 확인을 되풀이한다. 마지막으로 설계는 FPGA에 배치하는 경우에 어떤 지점의 전달 지연은 추가될 수 있고 시뮬레이션은 이런 값을 넷리스트에 기록하여 다시 실행한다.

## 기본적인 제조기술 종류

  - [에스램](https://ko.wikipedia.org/wiki/에스램 "wikilink") - 정적 메모리 기술 기반. 시스템에서 프로그램과 리프로그램이 됨. 외부 부트소자가 필요함. [시모스](https://ko.wikipedia.org/wiki/시모스 "wikilink").
  - [안티퓨즈](https://ko.wikipedia.org/wiki/안티퓨즈 "wikilink") - 한번만 프로그램이 됨. 시모스.
  - [이피롬](https://ko.wikipedia.org/wiki/이피롬 "wikilink") - 소거 및 프로그램되는 읽기용 메모리 기술. 일반적으로 플라스틱 패키지의 제품은 한번만 프로그램이 됨. 창이있는 소자는 자외선 (UV)로 삭제할 수 있음. 시모스.
  - [이이피롬](https://ko.wikipedia.org/wiki/이이피롬 "wikilink") - 전기적소거 및 프로그램되는 읽기용 메모리 기술. [플라스틱](../Page/플라스틱.md "wikilink") 패키지라도 소거할 수 있음. 일부 EEPROM 소자는 시스템에서 프로그램할 수 있음. 시모스.
  - [플래시 메모리](../Page/플래시_메모리.md "wikilink") - 플래시소거 이이피롬 기술. 플라스틱 패키지라도 소거할 수 있음. 일부 플래시 소자는 시스템에서 프로그램할 수 있음. 일반적으로 플래시 셀은 동등한 이이피롬 셀보다 작고 제조비용이 저렴함. 시모스.
  - [퓨즈](https://ko.wikipedia.org/wiki/퓨즈_\(전기\) "wikilink") - 한번만 프로그램됨. 접합형.

## FPGA 제조회사와 특징

2005년 후반에 FPGA 시장은 2개의 주된 “일반용” FPGA 제조사와 제공된 특별한 능력으로 구별하는 몇 개의 다른 용도로 거의 안정되었다.

  - [자일링스](https://ko.wikipedia.org/wiki/자일링스 "wikilink")와 [알테라](https://ko.wikipedia.org/wiki/알테라 "wikilink")는 두개의 큰 FPGA 선도회사이다.
  - [래티스 세미컨덕터는](https://ko.wikipedia.org/wiki/래티스_세미컨덕터 "wikilink") 에스램과 비휘발성을 가지는 플래시 기반 FPGA를 제공한다.
  - [액텔](https://ko.wikipedia.org/wiki/액텔 "wikilink")은 안티퓨즈와 재프로그램되는 플래시 기반 FPGA가 있고, 신호가 혼합된 플래시 기반 FPGA도 제공한다.
  - [아트멜](https://ko.wikipedia.org/wiki/아트멜 "wikilink")은 [자일링스](https://ko.wikipedia.org/wiki/자일링스 "wikilink") XC62xx처럼 미립자의 재설정되는 소자를 공급한다. 동일한 다이 (칩)의 FPGA 구조에 [AVR](https://ko.wikipedia.org/wiki/아트멜_AVR "wikilink") 마이크로프로세서를 포함하고 있다.
  - 알테라는 2015년 6월 1일 인텔에 인수합병되었다.

## 같이 보기

  -
  - [현장 프로그래머블 아날로그 어레이](https://ko.wikipedia.org/wiki/현장_프로그래머블_아날로그_어레이 "wikilink") (FPAA)
  - [VHDL](https://ko.wikipedia.org/wiki/VHDL "wikilink"): [VHSIC](https://ko.wikipedia.org/wiki/VHSIC "wikilink") () 하드웨어 기술 언어
  - [베릴로그](https://ko.wikipedia.org/wiki/베릴로그 "wikilink"): [Verilog](https://ko.wikipedia.org/wiki/Verilog "wikilink")하드웨어 기술 언어
  - [조금다른 하드웨어 기술 언어](https://ko.wikipedia.org/wiki/조금다른_하드웨어_기술_언어 "wikilink") (JHDL)
  - [FPGA에서 임베디드 시스템 설계](https://ko.wikipedia.org/wiki/FPGA에서_임베디드_시스템_설계 "wikilink")
  - [컨피그웨어](https://ko.wikipedia.org/wiki/컨피그웨어 "wikilink")

## 외부 링크

  - [FPGA와 CPLDs의 구조](http://www.eecg.toronto.edu/~jayar/pubs/brown/survey.html) 설명서
  - [FPGA FAQ](https://web.archive.org/web/20110615111604/http://www.fpga-faq.org/) FPGA FAQ 모음집. comp.arch.fpga 기록이 포함됨.
  - [Cornell ECE576 알테라 FPGA 설계 예제](http://instruct1.cit.cornell.edu/courses/ece576/)
  - [FPGA Central (본부): 납품업자, 공개토론, IP, Webcast 의 뉴스](https://web.archive.org/web/20190627070133/http://www.fpgacentral.com/)
  - [COPACOBANA (비용 최적화된 병렬 코드 브레이커), FPGA 기반의 재설정되는 코드 브레이커](https://web.archive.org/web/20090720052253/http://www.copacobana.org/)
  - [FPGA를 사용한 새로운 15 나노메터 크로스바 어레이](http://www.pcworld.com/article/id,128530-c,cpuarchitecture/article.html)
  - [OpenFPGA 사이트](https://web.archive.org/web/20070710211329/http://www.openfpga.org/)

[분류:게이트 어레이](https://ko.wikipedia.org/wiki/분류:게이트_어레이 "wikilink") [분류:미국의 발명품](https://ko.wikipedia.org/wiki/분류:미국의_발명품 "wikilink") [분류:반도체 소자](https://ko.wikipedia.org/wiki/분류:반도체_소자 "wikilink") [분류:전자 설계 자동화](https://ko.wikipedia.org/wiki/분류:전자_설계_자동화 "wikilink") [분류:집적 회로](https://ko.wikipedia.org/wiki/분류:집적_회로 "wikilink") [분류:FPGA 장치](https://ko.wikipedia.org/wiki/분류:FPGA_장치 "wikilink")

[fr:Circuit logique programmable\#FPGA](https://ko.wikipedia.org/wiki/fr:Circuit_logique_programmable#FPGA "wikilink")