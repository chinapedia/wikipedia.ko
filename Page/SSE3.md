> This article is converted from Wikipedia: [SSE3](https://ko.wikipedia.org/wiki/SSE3).


[인텔](https://ko.wikipedia.org/wiki/인텔 "wikilink") 코드이름 **[프레스캇](https://ko.wikipedia.org/wiki/프레스캇 "wikilink") 신규 명령어(Prescott New Instructions)**로 알려진 **SSE3**는 [IA-32](https://ko.wikipedia.org/wiki/IA-32 "wikilink")용 3번째 [SSE명령어](../Page/스트리밍_SIMD_확장.md "wikilink") 집합이다. 인텔은 SSE3를 [펜티엄 4](../Page/펜티엄_4.md "wikilink") CPU인 [프레스캇](https://ko.wikipedia.org/wiki/프레스캇 "wikilink")과 함께 2004년 초에 발표를 하였다. 2005년 4월에 AMD는 애슬론 64 CPU의 버전 E(베니스와 샌 디에고)에서 SSE3의 일부를 발표하였다. [x86](https://ko.wikipedia.org/wiki/x86 "wikilink")플랫폼에서의 이전 [SIMD](https://ko.wikipedia.org/wiki/SIMD "wikilink")명령어 집합은 시간순으로 [MMX](../Page/MMX.md "wikilink"), [3DNow\!](https://ko.wikipedia.org/wiki/3DNow! "wikilink") (AMD에 의해 개발), [SSE](../Page/스트리밍_SIMD_확장.md "wikilink") 그리고 [SSE2](../Page/SSE2.md "wikilink")이다.

SSE3는 [SSE2](../Page/SSE2.md "wikilink")대비 13개의 새로운 명령어가 포함되어 있다.

## 변경 사항

가장 주목할 만한 변경은 모든 이전 SSE명령어들이 다소 엄격히 수직적인 동작인것에 대비해 레지스터에서 수평적으로 동작할 수 있는 기능이다. 좀 더 구체적으로, 단일 레지스터에 저장되어 있는 여러 값들을 더하고 빼기 위한 명령어들이 추가되었다. 이러한 명령어들은 여러 [디지털 신호 처리와](../Page/디지털_신호_처리.md "wikilink") 3D처리를 단순화한다. 전역 Rounding 모드의 변경없이 부동소수점 값을 정수로 바꾸는 명령어도 포함되었다. 이것으로 [파이프라인](https://ko.wikipedia.org/wiki/파이프라인 "wikilink")에서의 처리지연을 피할 수 있게 되었다. 마지막으로 LDDQU를 포함한다. 이것은 캐시라인 경계를 넘는 Load가 [넷버스트](https://ko.wikipedia.org/wiki/넷버스트 "wikilink") 아키텍처에서 더 뛰어난 성능을 발휘하도록 하는 정렬되지 않은 정수 벡터 로드(misaligned integer vector load)의 대체이다.

## SSE3를 지원하는 CPU

  - [AMD](https://ko.wikipedia.org/wiki/AMD "wikilink"):
      - [애슬론 64](../Page/애슬론_64.md "wikilink") (베니스 [스테핑](https://ko.wikipedia.org/wiki/스테핑 "wikilink") E3 와 샌 디에고 스테핑 E4 이후)
      - [애슬론 64 X2](../Page/애슬론_64_X2.md "wikilink")
      - [애슬론 64 FX](../Page/애슬론_64.md "wikilink") (샌 디에고 스테핑 E4)
      - [옵테론](../Page/옵테론.md "wikilink") (스테핑 E4 이후)
      - [셈프론](../Page/셈프론.md "wikilink") (Palermo 스테핑 E3 이후)
      - [페넘](https://ko.wikipedia.org/wiki/페넘 "wikilink")
      - [페넘 II](https://ko.wikipedia.org/wiki/페넘_II "wikilink")
      - [튜리온 64](https://ko.wikipedia.org/wiki/튜리온_64 "wikilink")
      - [튜리온 64 X2](../Page/튜리온_64_X2.md "wikilink")
  - [인텔](https://ko.wikipedia.org/wiki/인텔 "wikilink"):
      - [셀러론 D](https://ko.wikipedia.org/wiki/셀러론_D "wikilink")
      - [셀러론](https://ko.wikipedia.org/wiki/셀러론 "wikilink") 420, 430, 440
      - [펜티엄 4](../Page/펜티엄_4.md "wikilink") (프레스캇 이후)
      - [펜티엄 D](../Page/펜티엄_D.md "wikilink")
      - [펜티엄 듀얼 코어](../Page/펜티엄_듀얼_코어.md "wikilink")
      - [펜티엄 익스트림 에디션](https://ko.wikipedia.org/wiki/펜티엄_익스트림_에디션 "wikilink") (펜티엄 4 익스트림 에디션은 아님)
      - [인텔 코어](../Page/인텔_코어.md "wikilink") 듀오
      - [인텔 코어](../Page/인텔_코어.md "wikilink") 솔로
      - [인텔 코어 2](../Page/인텔_코어_2.md "wikilink") 듀오
      - [인텔 코어 2](../Page/인텔_코어_2.md "wikilink") 익스트림
      - [인텔 코어 2](../Page/인텔_코어_2.md "wikilink") 쿼드
      - [인텔 코어 i7](../Page/인텔_코어_i7.md "wikilink")
      - [제온](../Page/제온.md "wikilink") (노코나 이후)
      - [아톰](../Page/인텔_아톰.md "wikilink")
  - [비아](https://ko.wikipedia.org/wiki/비아 "wikilink")/Centaur:
      - [C7](https://ko.wikipedia.org/wiki/VIA_C7 "wikilink")
      - [Nano](https://ko.wikipedia.org/wiki/VIA_Nano "wikilink")
  - [트렌스메타](https://ko.wikipedia.org/wiki/트렌스메타 "wikilink")

## 신규 명령어

### 공통 명령어

**산술**

  - ADDSUBPD - (*Add-Subtract-Packed-Double*)
      - 입력 - { A0, A1 }, { B0, B1 }
      - 출력 - { A0 - B0, A1 + B1 }
  - ADDSUBPS - (*Add-Subtract-Packed-Single*)
      - 입력: { A0, A1, A2, A3 }, { B0, B1, B2, B3 }
      - 출력: { A0 - B0, A1 + B1, A2 - B2, A3 + B3 }

**AOS ( Array Of Structures )**

  - HADDPD - (*Horizontal-Add-Packed-Double*)
      - 입력: { A0, A1 }, { B0, B1 }
      - 출력: { A0 + A1, B0 + B1 }
  - HADDPS (*Horizontal-Add-Packed-Single*)
      - 입력: { A0, A1, A2, A3 }, { B0, B1, B2, B3 }
      - 출력: { A0 + A1, A2 + A3, B0 + B1, B2 + B3 }
  - HSUBPD - (*Horizontal-Subtract-Packed-Double*)
      - 입력: { A0, A1 }, { B0, B1 }
      - 출력: { A0 - A1, B0 - B1 }
  - HSUBPS - (*Horizontal-Subtract-Packed-Single*)
      - 입력: { A0, A1, A2, A3 }, { B0, B1, B2, B3 }
      - 출력: { A0 - A1, A2 - A3, B0 - B1, B2 - B3 }
  - LDDQU – 위에 언급되었듯이, 이것은 정렬되지 않는 정수 벡터 로드의 대체이며 비디오 압축에 유용함.
  - MOVDDUP, MOVSHDUP, MOVSLDUP – 복소수에 사용되며 소리와 같은 파형 계산에 유용함.
  - FISTTP – 옛 x87 FISTP 명령어와 같지만 부동소수점 제어 레지스터의 라운딩 모드 설정을 무시하며 대신 "chop" (절단) 모드를 사용한다. C언어와 같은 곳에서는 부동소수점을 정수로 변환시 일반적으로 절단을 한다. 이때 많은 시간이 소요되는 제어 레지스터의 로딩과 리로딩을 생략해준다.

### 인텔 명령어

  - MONITOR, MWAIT – [하이퍼 스레딩을](https://ko.wikipedia.org/wiki/하이퍼_스레딩 "wikilink") 지원하는 프로세서가 더 빠르게 실행하도록 멀티 스레드 애플리케이션을 최적화 시켜준다.

## 같이 보기

  - [스트리밍 SIMD 확장](../Page/스트리밍_SIMD_확장.md "wikilink") (SSE)
  - [SSE2](../Page/SSE2.md "wikilink")
  - [SSSE3](https://ko.wikipedia.org/wiki/SSSE3 "wikilink")
  - [SSE4](https://ko.wikipedia.org/wiki/SSE4 "wikilink")
  - [SIMD](https://ko.wikipedia.org/wiki/SIMD "wikilink")
  - [넷버스트 마이크로아키텍처](https://ko.wikipedia.org/wiki/넷버스트_마이크로아키텍처 "wikilink")
  - [네할렘 마이크로아키텍처](https://ko.wikipedia.org/wiki/네할렘_마이크로아키텍처 "wikilink")
  - [마이크로아키텍처](../Page/마이크로아키텍처.md "wikilink")
  - [콘로](https://ko.wikipedia.org/wiki/콘로 "wikilink")
  - [제온](../Page/제온.md "wikilink")
  - [코어 마이크로아키텍처](https://ko.wikipedia.org/wiki/코어_마이크로아키텍처 "wikilink")

## 외부 링크

  - [SSE3 Overview by Intel](http://www.intel.com/cd/ids/developer/asmo-na/eng/66717.htm)

  - [X-bit Labs](https://web.archive.org/web/20060531094837/http://www.xbitlabs.com/articles/cpu/display/prescott_10.html)

[분류:병렬 컴퓨팅](https://ko.wikipedia.org/wiki/분류:병렬_컴퓨팅 "wikilink") [분류:SIMD 컴퓨팅](https://ko.wikipedia.org/wiki/분류:SIMD_컴퓨팅 "wikilink") [분류:X86 명령어](https://ko.wikipedia.org/wiki/분류:X86_명령어 "wikilink")