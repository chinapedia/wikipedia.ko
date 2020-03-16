> This article is converted from Wikipedia: [ SIMD ](https://ko.wikipedia.org/wiki/_SIMD_).


**스트리밍 SIMD 확장**(Streaming SIMD Extensions, SSE)은 [x86](https://ko.wikipedia.org/wiki/x86 "wikilink") 아키텍처에 대한 [SIMD](https://ko.wikipedia.org/wiki/SIMD "wikilink")(단일 명령 다중 데이터) [명령어 집합](../Page/명령어_집합.md "wikilink") 확장이며, [인텔](../Page/인텔.md "wikilink")이 1999년에 [펜티엄 III](../Page/펜티엄_III.md "wikilink") 시리즈 프로세서에 도입하였다. 이 기능은 1998년 등장한 [AMD](https://ko.wikipedia.org/wiki/AMD "wikilink")사의 [3D나우\!](../Page/3D나우!.md "wikilink") 기술에 대응한다. SSE는 70가지의 새로운 명령어와 추가적인 레지스터로 구성되며, 명령어의 대부분은 [부동 소수점에](https://ko.wikipedia.org/wiki/부동_소수점 "wikilink") 대한 연산이다.

SSE는 [펜티엄 III가](../Page/펜티엄_III.md "wikilink") 코드명 Katmai로 알려져 있을 시기에는 **KNI**(Katmai New Instructions)로 불렸다. 이후 이 이름은 **ISSE**(Internet Streaming SIMD Extensions)로 정해졌었으며, 이후 SSE로 변경되었다. AMD는 [애슬론 XP와](https://ko.wikipedia.org/wiki/애슬론_XP "wikilink") [듀론](../Page/듀론.md "wikilink") 프로세서를 기점으로 SSE 명령 지원을 추가했다.

## 레지스터

SSE는 x86 아키텍처에서 XMM0\~XMM7의 8개의 128비트 레지스터를 추가한다. 또한 [x86-64](https://ko.wikipedia.org/wiki/x86-64 "wikilink")에서는 XMM8\~XMM15의 8개의 레지스터가 추가되었다(단, 이 레지스터는 64비트 모드에서만 사용가능하다). 추가적으로, 32비트 레지스터 MXCSR는 SSE 명령어의 상태 및 제어에 사용된다.

[right](https://ko.wikipedia.org/wiki/파일:XMM_registers.png "wikilink")

SSE는 XMM 레지스터의 자료구조로 4개의 32비트 단정도 부동 소수점을 사용했다. 즉, 하나의 레지스터에 4개의 값이 들어가는 형태였다. SSE에서는 정수 계산을 지원하지 않는다. 이것은 [MMX](../Page/MMX.md "wikilink") 명령어를 사용하는 방식으로 극복이 가능했다. 또한, SSE2부터는 SSE를 확장하여 다음의 자료구조를 지원한다.

  - 2개의 64비트 배정도 부동 소수점
  - 2개의 64비트 정수
  - 4개의 32비트 정수
  - 8개의 16비트 정수
  - 16개의 8비트 정수

SSE를 처음 지원한 [펜티엄 III는](../Page/펜티엄_III.md "wikilink") SSE와 [FPU를](../Page/부동_소수점_장치.md "wikilink") 동시에 사용할 수 없도록 만들어졌다. 이러한 구조는 [명령어 파이프라인](../Page/명령어_파이프라인.md "wikilink") 효율성을 떨어뜨렸다.

XMM 레지스터는 태스크 스위치 시에 값을 보존해야 하는 대상이기 때문에, [운영 체제가](../Page/운영_체제.md "wikilink") 이 레지스터를 사용하도록 명시적으로 활성화하기 전까지는 사용이 불가능하다. 다시 말하면, 운영 체제가 SSE 레지스터를 보존하는 명령어인 FXSAVE와 FXSTOR를 사용할 수 있어야 한다는 의미이다. 이러한 지원은 주요 IA-32 운영 체제에서 빠르게 추가되었다.

## SSE 명령어

  - 부동 소수점 명령어
      - 메모리 대 레지스터 / 레지스터 대 메모리 / 레지스터 대 레지스터 데이터 이동
          - Scalar – MOVSS
          - Packed – MOVAPS, MOVUPS, MOVLPS, MOVHPS, MOVLHPS, MOVHLPS
      - 산술
          - Scalar – ADDSS, SUBSS, MULSS, DIVSS, RCPSS, SQRTSS, MAXSS, MINSS, RSQRTSS
          - Packed – ADDPS, SUBPS, MULPS, DIVPS, RCPPS, SQRTPS, MAXPS, MINPS, RSQRTPS
      - 비교
          - Scalar – CMPSS, COMISS, UCOMISS
          - Packed – CMPPS
      - 데이터 셔플 / 언패킹
          - Packed – SHUFPS, UNPCKHPS, UNPCKLPS
      - 자료형 변환
          - Scalar – CVTSI2SS, CVTSS2SI, CVTTSS2SI
          - Packed – CVTPI2PS, CVTPS2PI, CVTTPS2PI
      - 비트 논리 명령어
          - Packed – ANDPS, ORPS, XORPS, ANDNPS
  - 정수 명령어
      - 산술
          - PMULHUW, PSADBW, PAVGB, PAVGW, PMAXUB, PMINUB, PMAXSW, PMINSW
      - 데이터 이동
          - PEXTRW, PINSRW
      - 기타
          - PMOVMSKB, PSHUFW
  - 다른 명령어
      - MXCSR 관리
          - LDMXCSR, STMXCSR
      - 캐시 및 메모리 관리
          - MOVNTQ, MOVNTPS, MASKMOVQ, PREFETCH0, PREFETCH1, PREFETCH2, PREFETCHNTA, SFENCE

## 예

다음 예는 SSE의 장점을 보여준다. 컴퓨터 그래픽등에서 아주 자주 사용하는 명령어인 벡터 더하기를 보자. 두개의 단밀도를 더하기 위해서는 x87를 사용하는 4개의 구성요소 벡터가 4개의 부동소수점 더하기 명령어가 필요하다.

``` c
 vec_res.x = v1.x + v2.x;
 vec_res.y = v1.y + v2.y;
 vec_res.z = v1.z + v2.z;
 vec_res.w = v1.w + v2.w;
```

이것은 오브젝트코드에서 4개의 x87 FADD명령어에 해당한다. 반면에 다음 수도 코드(pseudo-code)에서는 하나의 128비트 ‘packed-add’ 명령어가 4개의 스칼라 더하기 명령어를 대체한다.

``` asm
 movaps xmm0,address-of-v1          ;xmm0=v1.w | v1.z | v1.y | v1.x
 addps xmm0,address-of-v2           ;xmm0=v1.w+v2.w | v1.z+v2.z | v1.y+v2.y | v1.x+v2.x
 movaps address-of-vec_res,xmm0
```

## 뒤에 나온 버전

  - [SSE2](../Page/SSE2.md "wikilink")
  - [SSE3](../Page/SSE3.md "wikilink")
  - [SSSE3](../Page/SSSE3.md "wikilink")
  - [SSE4](../Page/SSE4.md "wikilink")
  - [SSE5](https://ko.wikipedia.org/wiki/SSE5 "wikilink")
  - [AVX](../Page/고급_벡터_확장.md "wikilink")

## 같이 보기

  - [어셈블리어](../Page/어셈블리어.md "wikilink")
  - [MMX](../Page/MMX.md "wikilink")
  - [3D나우\!](../Page/3D나우!.md "wikilink")

[분류:중앙 처리 장치](https://ko.wikipedia.org/wiki/분류:중앙_처리_장치 "wikilink") [분류:X86 명령어](https://ko.wikipedia.org/wiki/분류:X86_명령어 "wikilink")