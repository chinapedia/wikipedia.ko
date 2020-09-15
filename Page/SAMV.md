> This article is converted from Wikipedia: [SAMV](https://ko.wikipedia.org/wiki/SAMV).


**SAMV** (반복 스파 스 점근 최소 분산\[1\])는 신호 처리의 스펙트럼 추정 및 도착 방향 (DOA) 추정을위한 파라미터 무료 슈퍼 해상도 알고리즘입니다. 이 이름은 점근 최소 분산 (AMV) 기준의 기초를 강조하기 위해 만들어 낸되었습니다. 제한된 수의 스냅 샷 낮은 신호대 잡음비 등 어려운 환경에서 여러 높은 상관 소스의 진폭과 주파수의 두 특성을 복구하는 강력한 도구입니다. 합성 개구 레이다 영상과 다양한 소스 지역화\[2\]\[3\].

## 설명

SAMV 알고리즘\[4\]도플러 레이다에 응용 된 최근의 스파 스 모델링 기반의 초 해상 기술 (Super-resolution). SAMV 알고리즘은 여러 신호 구분 등의 기존의 방법보다 우수한 결과 을 제공합니다.

## 그리드 한계 이상의 고정밀

대구경의 압축 縮의베이스의 소스 위치 특정 기술의 분해능은 위치 매개 변수 공간을 캡쳐하는 방향 그리드의 제한에 의해 제한됩니다. 거리에 의존하는 경우, 최적의 콘서트 사전의 선택이 어려움이 생기다. 계산의 복잡성은 방향 그리드의 종류와 직접적인 관계가 없기 때문에 계산할 때 실용적이지 않다. 그리드에 의해 과수 이 해결 한계를 달성하기 위해서, 확실한 최우선 순위가 위치 최적화를 최하화하는 것에 의해 위치 추정을 정확도화하는 격자 프리 SAMV-SML (反復 疎密 近近 最小 分散 - 確信 的 最尤) 제안 된 것 一 人 の ス ラ ラ ー パ ラ メ ー ター에 対 応.

## 응용 프로그램의 범위-Doppler imaging

[섬네일](https://ko.wikipedia.org/wiki/파일:IEEE_transaction_on_Signal_Processing_Paper_Results_Sample.jpg "wikilink")

SAMV 알고리즘을 사용하는 일반적인 응용 프로그램은 [Doppler radar](https://en.wikipedia.org/wiki/Pulse-Doppler_radar)에 있습니다. 이 영상 문제는 단일 스냅 샷 응용 프로그램이며 단일 스냅 샷 추정과 호환되는 알고리즘, 즉 Matched filter (MF, 주기도와 유사), IAA 및 SAMV 알고리즘 변형 (SAMV-0)이 포함됩니다. 전송 된 펄스는 30 요소 다상 [Pulse compression](https://en.wikipedia.org/wiki/Pulse_compression) P3 코드가 사용되고 총 9 개의 이동 표적이 시뮬레이션됩니다. 모든 움직이는 표적 중 3 개는 5dB 전력이고 나머지 6 개는 25dB 전력입니다. 수신 된 신호는 0dB 전력의 균일 한 백색 가우시안 잡음으로 오염 된 것으로 가정합니다.

정합 필터 검출 결과는 도플러 영역과 범위 영역에서 심한 번짐과[스펙트럼 누출](https://en.wikipedia.org/wiki/Spectral_leakage)영향을 받기 때문에 5dB 목표를 구별하는 것이 불가능합니다. 반대로, IAA 알고리즘은 관측 대상 범위 추정 및 도플러 주파수로 향상된 이미징 결과를 제공합니다. SAMV-0 방식은 매우 희소 한 결과를 제공하고 완전히 번짐 현상을 제거하지만 약한 5dB 목표를 놓치게됩니다.

## 오픈 소스 소프트웨어

SAMV 알고리즘의 오픈 소스 [MATLAB](../Page/MATLAB.md "wikilink") [소프트웨어를 다운로드 할 수 있습 니다](https://qilin-zhang.github.io/_pages/zips/Iterative_Sparse_Asymptotic_Minimum_Variance_Based_Approach_Matlab_Codes.zip?raw=true).

## 같이 보기

  - [레이다](../Page/레이다.md "wikilink")
  - [도플러 레이다](https://ko.wikipedia.org/wiki/도플러_레이다 "wikilink")

## 참조

[분류:푸리에 해석학](https://ko.wikipedia.org/wiki/분류:푸리에_해석학 "wikilink") [분류:삼각법](https://ko.wikipedia.org/wiki/분류:삼각법 "wikilink") [분류:파동역학](https://ko.wikipedia.org/wiki/분류:파동역학 "wikilink") [분류:신호 처리](https://ko.wikipedia.org/wiki/분류:신호_처리 "wikilink") [분류:신호 추정](https://ko.wikipedia.org/wiki/분류:신호_추정 "wikilink") [분류:주파수 영역 분석](https://ko.wikipedia.org/wiki/분류:주파수_영역_분석 "wikilink")

1.
2.
3.
4.