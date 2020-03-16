> This article is converted from Wikipedia: [ \(CPU\)](https://ko.wikipedia.org/wiki/_\(CPU\)).


**크레이트 아키텍처**(Krait architecture)는 [퀄컴](../Page/퀄컴.md "wikilink") [스냅드래곤](../Page/스냅드래곤.md "wikilink") S4 및 스냅드래곤 400, 600, 800 SoC 중 일부 모델에 사용되는 ARM 기반 프로세서이다. 2012년에 [스콜피온](https://ko.wikipedia.org/wiki/스콜피온 "wikilink")의 후속작으로 공개되었으며, ARMv7 명령어 집합을 지원하며 ARM Cortex-A15와 비슷한 아키텍처를 갖는다.

## 특징

과거의 스콜피온 CPU에 비해서 파이프라인의 구조가 11단계로 변경되었고, 3중 디코드 및 4중 비순차 예측 실행 수퍼스칼라 아키텍처를 채택하였다. 부동 소숫점 연산 장치(FPU)도 기존의 파이프라인 VFPv3에서 VFPv4로 변경되었고 128비트 NEON 명령을 지원한다.\[1\] L0 캐시는 4+4KB 다이렉트 매핑, L1 캐시는 16+16KB 4-way, L2 캐시는 8-way 1MB(듀얼코어) 및 2MB(쿼드코어)로, 스콜피온의 256/512KB에 비해서 4배 증가하였다. 프로세서의 제조 공정은 [TSMC](../Page/TSMC.md "wikilink")의 28 nm LP 및 HPm(Krait 400 이후)을 채택하였다. Krait 400 이후 프로세서는 이전에 비해서 최고 클럭이 높아졌다.

스콜피온 아키텍처와 마찬가지로 소비전력을 감소 시키기 위하여 비동기 코어 제어 방식을 채택하였으며, 각 코어의 클럭 속도는 부하에 따라 능동적으로 조절된다. Krait 300 아키텍처에서는 L2 캐시에 하드웨어적 Data Prefetcher가 도입되었으며 분기 예측이 향상되어 단일 스레드에서의 IPC(클럭 당 명령어 처리)가 향상되었다. 그 결과 부동소수점 성능과 자바스크립트 성능이 향상되었다.\[2\]

여러 종류의 파생형이 있으며 각각의 특징은 다음과 같다.

  - Krait: S4 Plus 및 Prime에 적용되었다. 제조 공정은 28nm이며 성능은 3.3DMIPS/MHz이다.
  - Krait 200: S4 Pro, 400 일부 제품군에 적용되었다. 제조 공정은 28nm이며 성능은 3.1DMIPS/MHz이다.
  - Krait 300: S4 Pro, 400 일부 및 600 제품군에 적용되었다. 제조 공정은 28nm이며 성능은 3.39DMIPS/MHz이다.\[3\]
  - Krait 400: 800 제품군에 적용되었다. 제조 공정은 28nm이며 성능은 3.39DMIPS/MHz이다.
  - Krait 450: 805 제품군에 적용되었다. 제조 공정은 20nm이며 성능은 3.51DMIPS/MHz이다.

## 참고/각주

[분류:퀄컴](https://ko.wikipedia.org/wiki/분류:퀄컴 "wikilink") [분류:ARM 아키텍처](https://ko.wikipedia.org/wiki/분류:ARM_아키텍처 "wikilink")

1.
2.
3.