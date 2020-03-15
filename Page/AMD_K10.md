> This article is converted from Wikipedia: [AMD K10](https://ko.wikipedia.org/wiki/AMD_K10).


[오른쪽](https://ko.wikipedia.org/wiki/파일:AMD_K10_Arch.svg "wikilink") **K10 마이크로아키텍처**([영어](https://ko.wikipedia.org/wiki/영어 "wikilink"): K10 Microarchitecture)는 [AMD](https://ko.wikipedia.org/wiki/AMD "wikilink")의 [K8 마이크로아키텍처를](https://ko.wikipedia.org/wiki/K8_마이크로아키텍처 "wikilink") 잇는 새로운 x86/x64 마이크로아키텍처의 이름이다. 3세대 [옵테론](../Page/옵테론.md "wikilink")과 [페넘](https://ko.wikipedia.org/wiki/페넘 "wikilink") 제품군 등에서 사용된 마이크로아키텍처이며, **스타 코어 마이크로아키텍처**라고도 한다. 초기 개발단계에서는 K8 Rev.H 또는 K8L 이라고 불리는 것이 일반적이었다.\[1\]

## 특징

K8 마이크로아키텍처를 기본으로 하며, 서버용 CPU에 주로 쓰이던 L3캐시를 내장하고, [하이퍼트랜스포트](../Page/하이퍼트랜스포트.md "wikilink") 3.0으로 메모리와 통신하게 되어, 병목현상이 이전 아키텍처에 비해 크게 줄었으며, 부동소수점 연산과 [SSE](../Page/스트리밍_SIMD_확장.md "wikilink") 유닛이 128BIT로 확장되어 SSE 명령 처리에 있어서 향상점이 있다. 이전의 K8 마이크로아키텍처에 비해서 높은 클럭당 명령 실행 수(Instructions Per Clock, IPC)를 가진다.

## 개선 또는 새로 적용된 기술

  - 128BIT로 확장된 SSE 유닛
  - 2개의 독립된 메모리 컨트롤러 사용
      - 일반적인 듀얼채널과 비슷한 개념인 Ganged Mode와 두개의 메모리 채널이 동시에 작동하는 Unganged mode로 나뉜다.(듀얼 채널 여부와는 별개)
  - 하이퍼트랜스포트 3.0
  - 어드밴스트 메모리 프리페처
      - 데이터를 L2 캐시에서 찾을 필요없이 메모리로부터 L1 캐시로 가져올 수 있으며, 지연시간이 줄며 L2 캐시의 부담을 줄일 수 있다.
      - K8 마이크로아키텍처에 비해 명령어를 위한 데이터 버퍼가 32 바이트로 늘었다.
  - 통합 L3 캐시
  - [SSE4](https://ko.wikipedia.org/wiki/SSE4 "wikilink")A
      - 다음과 같은 4개의 명령어를 지원한다. EXTRQ/INSERTQ, MOVNTSD/MOVNTSS, LZCNT, POPCNT

## K10 아키텍처가 사용된 제품

  - [페넘](https://ko.wikipedia.org/wiki/페넘 "wikilink")
  - [옵테론](../Page/옵테론.md "wikilink") (3세대)
  - [애슬론 X2](https://ko.wikipedia.org/wiki/애슬론_X2 "wikilink") (쿠마)

## 각주

[분류:AMD x86 마이크로프로세서](https://ko.wikipedia.org/wiki/분류:AMD_x86_마이크로프로세서 "wikilink") [분류:마이크로아키텍처](https://ko.wikipedia.org/wiki/분류:마이크로아키텍처 "wikilink")

1.