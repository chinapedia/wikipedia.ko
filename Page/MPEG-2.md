> This article is converted from Wikipedia: [MPEG-2](https://ko.wikipedia.org/wiki/MPEG-2).


[오른쪽](https://ko.wikipedia.org/wiki/파일:Mpeg.svg "wikilink") **MPEG-2**(엠펙 투)는 [MPEG](../Page/MPEG.md "wikilink")(Moving Picture Expert Group)이 정한 오디오와 비디오 인코딩(부호화)에 관한 일련의 표준을 말하며, ISO 표준 13818(13818-1은 시스템, 13818-2는 비디오 부호화, 13818-3은 오디오...)로 공표되었다. MPEG-2는 일반적으로 디지털 위성방송, 디지털 유선방송 등의 디지털 방송을 위한 오디오와 비디오 정보 전송을 위해 쓰이고 있다. 또, MPEG-2의 표준을 약간 변형한 인코딩 포맷은 상업 [DVD](https://ko.wikipedia.org/wiki/DVD "wikilink")의 표준으로 돌비 디지털, DTS와 함께 사용되고 있다.

MPEG-2 13818-2 비디오 표준은 [MPEG-1](../Page/MPEG-1.md "wikilink")과 비슷하지만, [텔레비전](https://ko.wikipedia.org/wiki/텔레비전 "wikilink") 방송에서 사용하는 [비월주사](https://ko.wikipedia.org/wiki/비월주사 "wikilink") 방식의 영상을 지원한다. MPEG-2 비디오(부분 2)는 저속 비트율(1 Mbit/s) 환경에는 부적합하지만, 초당 3 메가비트 이상을 요구하는 MPEG-1보다는 향상된 압축률을 보이고 있다. MPEG-2의 MPEG-1과 구별되는 특징으로는 데이터 유실이 많은 전송 환경에도 적합한 [트랜스포트 스트림이](../Page/MPEG_트랜스포트_스트림.md "wikilink") 정의되어 있다는 점을 들 수 있으며, 이는 현재 디지털 방송에 사용되고 있다. MPEG-2는 원래 MPEG-3로 개발하려던 [HDTV](https://ko.wikipedia.org/wiki/HDTV "wikilink")(고선명 텔레비전) 전송의 표준 또한 포함한다. 또한 MPEG-1과도 호환성도 보장되어 표준을 따르는 MPEG-2 디코더는 MPEG-1 스트림도 재생할 수 있다. 이 부분의 표준은 [ITU-T](../Page/ITU-T.md "wikilink")의 [비디오 코딩 전문가 그룹](https://ko.wikipedia.org/wiki/비디오_코딩_전문가_그룹 "wikilink")(Video Coding Experts Group, VCEG)과 [ISO/IEC](https://ko.wikipedia.org/wiki/ISO/IEC "wikilink")의 [동화상 전문가 그룹](https://ko.wikipedia.org/wiki/동화상_전문가_그룹 "wikilink")(Moving Picture Experts Group, MPEG)이 공동으로 표준화를 진행하였으며, 따라서 [ITU-T](../Page/ITU-T.md "wikilink")의 H.262와 [MPEG](../Page/MPEG.md "wikilink")의 13818-2는 동일하다.

MPEG-2 13818-3 오디오 표준은 MPEG-1 오디오 표준에서 발전되어 채널의 확장을 하는 MC (다중 채널)과 낮은 표본화 주파수를 제공하는 LSF (낮은 샘플링 주파수:Low Sampling Frequency)(24 kHz, 22.05 kHz, 16 kHz)로 구성되어 있다. 또한 두가지 모두 MPEG-1 오디오를 복호화할 수 있는 하위 호환성의 특성을 가지고 있다. 알고리즘 측면에서는 추가된 내용이 없기 때문에 이론적으로 MPEG-1과 동일한 압축율을 가진다고 봐도 무방하다.

하지만 MPEG-2에서는 압축율을 높이는 대신, 하위 호환성을 지원하지 않는 AAC (고급 오디오 코딩)를 13818-3이 표준화 된 후 13818-7로 표준화하고 있다. AAC에는 기존 MPEG 오디오에서 사용되지 않던, LTP, TNS, 예측 도구가 추가되었으며 레이어로 구분하던 MPEG-1,2와는 달리 도구의 집합인 프로파일로 구분하여 정의하고 있다. (덜 복잡함, 조절할 수 있는 샘플 속도)

## 기술

### MPEG-2 표준

DVD / DVB 에서 사용되는 변경된 표준을 제외한 MPEG-2 비디오와 MPEG-2 오디오에 대한 일반 정보. .

  - 영상 데이터 + 타임 스탬프(시각 정보)
  - 소리 데이터 + 타임 스탬프

### 간략한 MPEG-2 비디오 인코딩 절차

MPEG-2는 *오디오 신호를 비롯한 동영상의 일반적인 인코딩(부호화)*을 위한 규약이다. 부호화된 비디오 스트림은 화면 내 예측(**I**ntra), 전방 예측(**P**redictive), 양방향 예측(**B**idirectional)의 세가지 프레임들의 배치를 규정한 GOP(Group of Pictures) 구조로 구성된다. 일반적으로 부호화할 원본은 소리가 포함된 일정한 해상도의 영상이 초당 25([CCIR](https://ko.wikipedia.org/wiki/CCIR "wikilink")규정) 프레임 또는 초당 29.97([FCC](https://ko.wikipedia.org/wiki/FCC "wikilink")규정) 프레임의 속도로 바뀌는 동영상이다.

MPEG-2는 [비월주사](https://ko.wikipedia.org/wiki/비월주사 "wikilink")(interlaced scan)와 [순차주사](https://ko.wikipedia.org/wiki/순차주사 "wikilink")(progressive scan) 두 가지 방식의 비디오 스트림을 모두 지원한다. 순차주사 방식에선 부호화의 기본 유닛이 프레임(한 장의 영상)이 되고, 비월주사 방식에선 필드(한 장의 영상의 홀수줄, 혹은 짝수줄만으로 이루어짐)이다. 아래 설명에서 "픽처" 혹은 "정지 영상"이라고 말한 것은 각각의 기본 유닛(즉 필드나 프레임)을 가리킨다.

MPEG-2 스트림은 단일 영상을 부호화한 데이터 프레임의 연속이다. 각 정지영상을 부호화하는 방법엔 화면 내 예측(I), 전방 예측(P), 양방향 예측(B) 세 가지가 있다.

각 비디오 이미지는 루미넌스(명도) 성분 Y 와 두 개의 크로미넌스(색차) U, V 채널로 우선 나뉜다. 각각에 대해 공간적으로 "매크로 블록(macroblock)"이라 불리는 16x16 크기의 격자로 나뉘며, 이 매크로 블록이 부호화의 기본적인 조각이 된다. 매크로 블록은 8x8 크기의 "블록" 4개가 합쳐진 것이다. 원본 이미지의 색상 샘플링 포맷에 따라 한 매크로 블록이 8x8 크기의 색차 정보 블록을 가질지, 아니면 16x16을 가질지가 결정된다. 예를 들어, 일반적으로 쓰이는 [4:2:0](https://ko.wikipedia.org/wiki/4:2:0 "wikilink") 포맷에서는, 한 색상이 매크로 블록 하나(16x16)당 한 개의 크로미넌스 블록(8x8)만을 갖게 되어, 하나의 매크로 블록은 4개의 명도 정보(Luminance) 블록, 1개의 U블록, 1개의 V블록으로 총 6개의 블록을 갖게 된다.

I 픽처의 경우 이미지 데이터는 다음 문단에서 설명하는 인코딩 절차를 바로 거치게 되며, P (혹은 B) 픽처의 경우엔 우선 "움직임 보상"(motion compensation)이라 불리는 과정을 거쳐 이전 영상(B의 경우엔 이전과 이후의 영상)과의 관련성을 검색하여 이용한 후 다음 인코딩을 진행하게 된다. 움직임 보상에선 P (혹은 B) 픽처로 만들어질 영상의 각 매크로 블록이 이전(B의 경우엔 이후도 포함) 영상의 어느 부분과 가장 관련성이 높은가를 알아내어 그 부분과의 공간상의 변위인 "움직임 벡터"(motion vector)와 두 영상간의 차이가 다음과 같이 부호화 되어 전송되게 된다.

각 블록은 8x8 [이산 코사인 변환](https://ko.wikipedia.org/wiki/이산_코사인_변환 "wikilink")(discrete cosine transformation)의 과정을 거치게 된다. 변환으로 얻어진 각 계수들은 미리 정해진 값들로 나누어 양자화 되고, 지그재그로 재배열 된 후 영에 대한 [RLC](https://ko.wikipedia.org/wiki/RLC "wikilink")을 하게 된다. 마지막으로 [허프만 코딩으로](https://ko.wikipedia.org/wiki/허프만_코딩 "wikilink") 부호화를 마친다.

I 픽처 인코딩은 공간적인 반복성에 대한 것이고, P 와 B 픽처는 시간적인 반복성에 대한 것이다. 다시 말해, 동영상을 이루는 이어지는 두개의 정지영상은 서로 상당히 비슷하며, 그래서 P 픽처는 보통 I 픽처의 10%, B 픽처는 2%의 크기로 부호화된다.

이 세 가지 프레임으로 이루어지는 일련의 프레임들은 GOP(Group of Pictures)라 불리는 구조를 이룬다. 다양한 구조의 GOP가 가능하지만 많이 쓰이는 것은 I_BB_P_BB_P_BB_P_BB_P_BB_ 의 순서로 15개의 프레임이 하나의 GOP를 구성하는 것이다. 이와 유사하게 12개의 프레임으로 만들어진 GOP구조도 자주 쓰인다. GOP 구조의 I, P, B 프레임의 구성 비율은 비디오 스트림의 성격, 출력 스트림이 가져야 하는 대역폭(bandwidth)등에 따라 정해진다. 인코딩에 걸리는 시간도 비율을 결정하는 한 요소이다. 이를테면 실시간으로 전송해야 하는 생방송의 경우에 인코딩에 동원되는 자원은 한정되어 있으며, B 픽처가 많이 들어간 스트림은 I 픽처만으로 이루어진 스트림에 비해 인코딩에 3배 정도의 시간이 들 수 있다.

MPEG-2 인코더의 출력 비트율은 일정해야 하거나, 정해진 최대 비트율을 갖고 변할 수 있다. 가변 비트율의 예로 10.4 Mbps를 최대 비트율로 갖는 DVD 영화를 들 수 있다. 일정한 비트율을 얻기 위해서 양자화의 수준을 변경시킬 수 있다. 그러나 양자화가 심하게 될 경우엔 전송된 스트림이 디코딩 된 화면에 격자모양이 나타날 수 있다. 이 현상은 비트율이 내려갈수록 더욱 심각해진다.

### MPEG-2 오디오 부호화

MPEG-2 는 또한 새로운 오디오 인코딩 방식을 도입한다. 이는

  - 반으로 줄어든 샘플링 율을 사용하는 저속 비트율 인코딩 (MPEG-1 Layer 1/2/3 LSF)
  - 다채널 인코딩. 최고 5.1 채널
  - 돌비를 견제하기 위해서 개발하였지만, 결국 돌비 디지털에 밀려서 거의 사장됨.
  - 새로운 오디오 인코딩 방식인 AAC 코덱에 대한 표준화

### DVD의 MPEG-2

DVD 표준에는 다음과 같은 제한 사항이 더해진다.

  - 해상도의 제한
      - 720 x 480 픽셀, 초당 59.94 필드 (FCC)
      - 720 x 480 픽셀, 초당 29.97 프레임 (FCC)
      - 720 x 576 픽셀, 초당 50 필드 (CCIR)
      - 720 x 576 픽셀, 초당 25 프레임 (CCIR)
  - 초당 최고 9,8 메가비트
  - YUV 4:2:0
  - 부가적인 자막 가능
  - 오디오
      - 48 kHz MPEG-2 Layer 2 가능
      - 48 kHz 최고 초당 448 킬로비트의 디지털 돌비 가능
      - 754 또는 초당 1510 킬로비트 의 DTS 가능
      - 최소한 하나의 MPEG 오디오 또는 DD 오디오 트랙 포함
  - GOP 구조의 제한

### DVB에서의 MPEG-2

[DVB](https://ko.wikipedia.org/wiki/DVB "wikilink")-MPEG에 더해진 제한 사항.

  - 다음의 SDTV 급 해상도만 허용됨.
      - 720 × 480 화소, 24/1.001, 24, 30/1.001 또는 30 프레임/초
      - 640 × 480 화소, 24/1.001, 24, 30/1.001 또는 30 프레임/초
      - 544 × 480 화소, 24/1.001, 24, 30/1.001 또는 30 프레임/초
      - 480 × 480 화소, 24/1.001, 24, 30/1.001 또는 30 프레임/초
      - 352 × 480 화소, 24/1.001, 24, 30/1.001 또는 30 프레임/초
      - 352 × 240 화소, 24/1.001, 24, 30/1.001 또는 30 프레임/초
      - 720 × 576 화소, 25 프레임/초
      - 544 × 576 화소, 25 프레임/초
      - 480 × 576 화소, 25 프레임/초
      - 352 × 576 화소, 25 프레임/초
      - 352 × 288 화소, 25 프레임/초

### MPEG-2 표준 문서

  - ISO/IEC 13818-1 : 시스템 - 비디오와 오디오 데이터의 동기화와 다중 송신을 정의.
    ISO/IEC 13818-2 : 비디오 - 비월주사, 순차주사 비디오 신호의 압축 코덱을 정의.
    ISO/IEC 13818-3 : 오디오 - 오디오 신호의 개념적인 압축 코덱, MPEG-1 ([MP3](https://ko.wikipedia.org/wiki/MP3 "wikilink"))에 여러 채널을 쓸 수 있게 한 확장을 정의.
    ISO/IEC 13818-4 : 테스트 절차를 정의. 호환성 테스트를 위한 절차를 서술하였음.
    ISO/IEC 13818-5 : 소프트웨어 시뮬레이션 시스템을 정의.
    ISO/IEC 13818-6 : DSM-CC (Digital Storage Media Command and Control의 약자)의 확장을 정의.
    ISO/IEC 13818-7 : [AAC](../Page/고급_오디오_부호화.md "wikilink") ([고급 오디오 코딩](https://ko.wikipedia.org/wiki/고급_오디오_코딩 "wikilink"))
    ISO/IEC 13818-9 : 실시간 인터페이스를 위한 확장.
    ISO/IEC 13818-10 : DSM-CC의 순응 확장
    ISO/IEC 13818-11 : MPEG2 시스템 위의 IPMP

## 같이 보기

  - [MPEG-ts](../Page/MPEG_트랜스포트_스트림.md "wikilink")
  - [DVD](https://ko.wikipedia.org/wiki/DVD "wikilink")
  - [AAC](../Page/고급_오디오_부호화.md "wikilink")
  - [MPEG-4](https://ko.wikipedia.org/wiki/MPEG-4 "wikilink")

## 외부 링크

  - [MPEG-2 표준에 대한 간단 안내](https://web.archive.org/web/20071023053620/http://www.fh-friedberg.de/fachbereiche/e2/telekom-labor/zinke/mk/mpeg2beg/beginnzi.htm)
  - [MPEG-2 살펴 보기](http://www.erg.abdn.ac.uk/research/future-net/digital-video/mpeg2.html)
  - [MPEG-2 영상 압축](http://www.bbc.co.uk/rd/pubs/papers/paper_14/paper_14.shtml)

[MPEG-2](https://ko.wikipedia.org/wiki/분류:MPEG-2 "wikilink") [분류:ISO 표준](https://ko.wikipedia.org/wiki/분류:ISO_표준 "wikilink") [분류:DVD](https://ko.wikipedia.org/wiki/분류:DVD "wikilink") [분류:영상 코덱](https://ko.wikipedia.org/wiki/분류:영상_코덱 "wikilink") [분류:오디오 코덱](https://ko.wikipedia.org/wiki/분류:오디오_코덱 "wikilink") [분류:MPEG](https://ko.wikipedia.org/wiki/분류:MPEG "wikilink") [분류:ISO/IEC 표준](https://ko.wikipedia.org/wiki/분류:ISO/IEC_표준 "wikilink") [분류:영상 압축](https://ko.wikipedia.org/wiki/분류:영상_압축 "wikilink")