> This article is converted from Wikipedia: [MIMO](https://ko.wikipedia.org/wiki/MIMO).


[섬네일](https://ko.wikipedia.org/wiki/파일:MIMO_with_building.png "wikilink") **MIMO**(multiple-input and multiple-output, 미모 또는 마이모)는 [무선 통신의](https://ko.wikipedia.org/wiki/무선_통신 "wikilink") 용량을 높이기 위한 스마트 안테나 기술이다. MIMO는 기지국과 단말기에 여러 안테나를 사용하여, 사용된 안테나수에 비례하여 용량을 높이는 기술이다. 여기서 기지국은 송신단을 의미하고 단말기는 수신단을 의미한다. 예를 들면 기지국에 \(M\)개, 단말기에 \(N\)개를 설치할 경우 \(min(M,N)\) 만큼 평균 전송 용량이 늘어난다. 특별히 \(N = 1\)로 기지국에만 여러 개 안테나를 사용하는 경우를 MISO, \(M = 1\)로 단말기에만 여러 개 안테나를 사용하는 경우를 SIMO 그리고 \((M,N) = (1,1)\)인 경우를 SISO라 부른다. 다음은 각 용어의 약자를 정리한 것이다.

  - Multiple-Input Multiple-Output (MIMO)
  - Multiple-Input Single-Output (MISO)
  - Single-Input Multiple-Output (SIMO)
  - Single-Input Single-Output (SISO)

## MIMO 기술의 활용

MIMO 기술의 필요성에 대해 수신 처리 입장과 송신 처리 입장의 다른 해석이 있다. 수신 처리 입장은 간섭 제거를 중심으로한 해석이고 송신 처리 입장은 용량 증대를 중심으로 한 해석이다. 두 해석 모두 무선 통신에서 다중 안테나 기술의 중요성을 잘 반영하고 있다. 송신 처리 입장은 MIMO의 중요성을 설명하며 수신 처리 입장은 MIMO의 필요성을 설명하고 있다고 할 수 있다.

### 수신기 입장

셀룰라 이동통신에서는 셀간 원활한 동적인 주파수 할당을 위해서 공간 간섭의 제거가 중요하다. 뿐만 아니라 무선랜에서도 AP수의 증가로 인해 다른 AP에서 오는 공간 간섭의 처리가 중요하다. 공간 간섭의 처리 방법으로는 동적 또는 위치에 적응적으로 주파수 재사용 비율의 감소등을 이용할 수 있다. 하지만 이런 방법은 주파수 자원의 손실을 발생시킨다. 한편, 이를 다중 수신 안테나를 통해 처리하면 주파수의 손실 없이 가능하게 된다. 그러나 이런 장점에도 불구하고 단말기가 무선 간섭이 없는 위치에 가게되면 다중 수신 안테나의 능력을 백분 발휘할 수 없다. 이를 역이용하여 무선 간섭을 발생하면서 이로 인해 다른 이득을 가져오는 방법이 있다면 전체적인 성능 향상에 도움이 될 것이다. 이에 대한 한 가지 방법이 기지국 다중 안테나 다중 스트림 전송이다. 기지국간 간섭이 존재하면 다중 수신 안테나들은 다중 기지국 공간 간섭을 제거하고, 기지국간 간섭이 없는 위치에서는 MIMO 방식으로 다중 스트림 간섭을 제거하여 용량을 증대하는 데 기여한다.

### 송신기 입장

이 입장은 기지국간 또는 AP들 간의 간섭이 없는 경우에 주로 설명이 된다. 간섭이 없는 경우에는 수신 안테나의 간섭 처리 기능을 기지국의 다중 안테나 다중 스트림 전송을 통한 용량 증대에 활용할 수 있다. 이렇게 되면 기지국과 단말기에 설치된 안테나들 수 중 적은 안테나수에 비례하여 이론적인 용량 증대가 가능해진다.

## MIMO 용량 증대

이는 기존 통신 이론에서 다루어온 전송용량의 증가로 설명되기에는 어려움이 있다. 하지만, 다중 안테나를 통한 새로운 공간 차원을 활용하기 때문에 가능한 용량 증대라고 보면 이해하기가 쉬워진다. 기존의 통신 이론에서는 전송 용량은 사용하는 주파수와 전력에 의해서만 결정되었다. 반면, MIMO는 사용하는 기지국과 단말기 안테나 수에 대한 새로운 관계식을 정의함으로써 용량과의 관계식을 표현할 수 있다.

다음은 [정보 이론에](../Page/정보_이론.md "wikilink") 근거하여 SISO 환경과 MIMO 환경에서 용량 관계식을 개념적으로 정리한 것이다.

  - SISO 환경에서 달성 용량

\[C = W log_2 (1+SNR)\]

  - MIMO 환경에서 달성 용량 (개념식)

\[C ~= W min(M,N) log_2 (1+SNR)\]

자세한 용량 관계식을 보기 전에 송수신 관계식을 먼저 보면 다음과 같다.

기지국과 단말기에 설치된 다중 안테나를 통한 단말기 수신 신호는 다음과 같다.

\[\mathbf{y} = \mathbf{H}\mathbf{x} + \mathbf{n}\] 여기서 \(\mathbf{H}\)는 MIMO의 안테나 관계에 따른 채널을 나타내는 메트릭스이다. 또한 \(\mathbf{x}, \mathbf{n}\)는 각각 전송신호와 수신 노이즈를 나타낸다. 이상의 관계를 통해 [정보 이론으로](../Page/정보_이론.md "wikilink") 용량 관계식을 구해보면 다음과 같다. 먼저 기지국에서 채널 상황을 알 때인 폐루프 채널 용량이다.

\[C_{CL} = E[\max_{\mathbf{Q}} \log_2 (\mathbf{I} + \mathbf{H}\mathbf{Q}\mathbf{H}^{H})]\] 다음은 기지국에서 채널 상황을 모를 때인 개루프 채널 용량이다.

\[\quad C_{OL} = \max_{\mathbf{Q}}E[\log_2 (\mathbf{I} + \mathbf{H}\mathbf{Q}\mathbf{H}^{H})] = E \left[\log_2 \left( \mathbf{I} + \frac{1}{M} \mathbf{H}\mathbf{H}^{H} \right) \right]\] 여기서 \(C_{OL}\)에서는 \(\mathbf{Q}\)는 \(\frac{1}{M}\mathbf{I}\)와 같은 단위 unitary matrix를 사용하면 최대화가 가능한 것이 증명되었다. 상기 두 용량 관계식은 MIMO뿐 아니라 채널 메트릭스인 \(\mathbf{H}\)의 형태에 따라 MISO, SIMO 그리고 SISO의 경우 모두에 적용이 가능하다

### 참고 논문

  - [Multiple Input Multiple Output Systems: capacity and channel measurements](https://web.archive.org/web/20050511183030/http://www.dur.ac.uk/comms.systems/pdfs/multiple%20input%20multiple%20output.PDF)

## MIMO 통신

MIMO 통신의 발달은 우편의 그림과 같이 정리할 수 있다. MIMO 기술은 SISO 통신 기술과 방식을 계승하여 발전되어 왔으며 최근에는 새로운 통신 기술들이 그림과 같이 MIMO를 바탕으로 하여 확장되고 있다. 확장 기술은 MIMO를 확장하는 스마트 안테나 기술, MIMO의 사용을 전제로한 통신 기술 그리고 다중 소자를 사용하여 용량을 확장하는 MIMO 개념의 확대 적용 등이 있다.

3GPP LTE (Release8), WiMAX Evolution (SDD 단계 진행)등 MIMO-OFDM 기반 이동통신 표준에서는 SU-MIMO와 [MU-MIMO](https://ko.wikipedia.org/wiki/MU-MIMO "wikilink")를 포함한 MIMO의 사용을 표준화하고 있다. 여기서 SU-MIMO는 한 사용자에게 기지국의 안테나 리소스 모두를 할당하는 방식이고 MU-MIMO는 다수의 사용자에게 안테나 리소스 또는 무선 공간 자원을 분배하는 방식이다.

## 참고문헌

  - 이명원, 문철, 육종관, “제한된 피드백 정보를 이용하는 이중 공간 다중화 시스템의 Precoding 기법”, 한국전자파학회논문지, Vol. 17, No.12, 2006년 12월.

## 같이 보기

  - [빔포밍](../Page/빔포밍.md "wikilink")

## 외부 링크

  -   - 대만의 네트워크 장비 업체들에 따르면 MIMO (미모 , multi-in multi-out) 무선랜 제품과 VoIP 관련 제품들의 수출실적이 계속 크게 증가할 것으로 예상되고 있다.

  - [안테나의 끝없는 진화 - 무선통신의 핵심은 안테나 기술, 초소형 스마트 멀티... 고용량 데이터 척척, morningplus.chosun.com](http://morningplus.chosun.com/s_svc_img/pdf/weeklybiz03.pdf)

      - NASA는 최근 MIMO 기술을 적용한 안테나를 통해 탐사로봇의 정보를 빠르게 전송 받고 있다.

[분류:IEEE 802](https://ko.wikipedia.org/wiki/분류:IEEE_802 "wikilink") [분류:무선 통신](https://ko.wikipedia.org/wiki/분류:무선_통신 "wikilink") [분류:정보 이론](https://ko.wikipedia.org/wiki/분류:정보_이론 "wikilink")