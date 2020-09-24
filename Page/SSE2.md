> This article is converted from Wikipedia: [SSE2](https://ko.wikipedia.org/wiki/SSE2).


**SSE2**(Streaming SIMD Extensions 2)는 [IA-32](../Page/IA-32.md "wikilink") [SIMD](../Page/SIMD.md "wikilink")(Single Instruction, Multiple Data) [명령어 집합](../Page/명령어_집합.md "wikilink") 중의 하나이다. SSE2는 2001년 [인텔](../Page/인텔.md "wikilink")의 [펜티엄 4에서](../Page/펜티엄_4.md "wikilink") 처음으로 발표되었다. SSE 명령어 집합의 확장이며 [MMX](../Page/MMX.md "wikilink")를 완전히 대신하고자 하였다. 인텔은 2004년에 [SSE3](../Page/SSE3.md "wikilink")를 발표함으로써 SSE2를 확대하였다. SSE2는 144개의 새로운 명령어를 70개의 명령어로 구성된 SSE에 추가하였다. 인텔의 경쟁사인 AMD는 이 명령어를 2003년 옵테론과 애슬론 64에서부터 지원하기 시작했다.

## 변경 사항

SSE2는 XMM레지스터에서 동작하는 MMX명령어의 확장이며, 프로그래머가 8개의 64비트 MMX레지스터들이 본래의 IA-32부동소수점 레지스터들로 별칭되는 것을 피하게 해준다. 이것은 MMX와 [x87](https://ko.wikipedia.org/wiki/x87 "wikilink") 부동소수점간 필요한 모드의 변경없이 정수 SIMD와 스칼라 부동소수점이 혼합하여 처리되는 것을 허용한다. 그러나 이것은 더 넓은 SSE 레지스터들위에서 MMX처리가 가능하다는 가치에 의해 빛이 바랬다.

또 다른 SSE2 확장은 끊임없이 연속되는 무한 정보를 처리할 때 발생하는 [캐시](../Page/캐시.md "wikilink") 오염을 최소화하기 위한 캐시 제어 명령어 집합과 복잡하고 정교한 숫자형 변환 명령어를 포함한다.

AMD는 추가 8개의 레지스터를 포함하여 SSE2명령어를 AMD64([x86-64](https://ko.wikipedia.org/wiki/x86-64 "wikilink"))에서 지원하기 시작했다. 따라서 XMM0부터 XMM15까지 총 16개의 레지스터를 지원한다. 이러한 추가적인 레지스터들은 64비트 모드에서만 동작할 때 보인다. 인텔은 2004년도에 이 추가 레지스터들을 “인텔 64”라고 하는 x86-64 아키텍처 지원의 일부로서 지원하게 되었다.

## x87 FPU 와 SSE2의 차이점

FPU명령어는 일반적으로 중간결과를 80비트의 정밀도에 저장을 한다. 종래의 FPU 소프트웨어 알고리즘이 SSE2에 포팅될 때에는 특정한 수학처리의 조합이나 데이터집합의 입력일 경우에 측정할 수 있는 수치 편차가 발생한다. 이것은 과학 계산시에 다른 아키텍처의 컴퓨터결과와 비교해야 할 정도로 매우 중요한 것이다.

주목할 만한 문제는 컴파일러가 여러 동작을 포함하는 수학 표현(더하기, 빼기, 나누기, 곱하기)을 해석할 때 발생한다. 컴파일러와 최적화 방법에 따라 주어진 수치 표현의 다른 중간 결과값을 임시로 저장한 후 나중에 다시 불러들이는 과정이 필요할 수 있다. 이것은 x87 FPU에서 80비트를 64비트로 줄인 결과이다. 이러한 절단이 언제 실행되느냐에 따라 최종 수치 결과는 다르게 될 수 있다. 다음은 예로서 G95로 컴파일된 포트란 코드이다.

``` fortran
 program hi
 real a,b,c,d
 real x,y,z
 a=.013
 b=.027
 c=.0937
 d=.79
 y=-a/b + (a/b+c)*EXP(d)
 print *,y
 z=(-a)/b + (a/b+c)*EXP(d)
 print *,z
 x=y-z
 print *,x
 end
```

  - 387 부동소수점 명령어로 컴파일 및 실행 결과

<!-- end list -->

``` bash
 $ g95 -o hi -mfpmath=387 -fzero -ftrace=full -fsloppy-char hi.for
 $ ./hi
  0.78587145
  0.7858714
  5.9604645E-8
```

  - SSE2 명령어로 컴파일 및 실행 결과

<!-- end list -->

``` bash
 $ g95 -o hi -mfpmath=sse -msse2 -fzero -ftrace=full -fsloppy-char hi.for
 $ ./hi
  0.78587145
  0.78587145
  0.
```

## MMX 와 SSE2의 차이점

SSE는 MMX레지스터에서 동작하는 MMX명령어의 확장이다. 따라서 모든 기존에 존재하는 MMX 코드를 SSE2로 바꿀 수가 있다. XMM레지스터가 MMX레지스터의 두배의 길이에 해당하기때문에 루프 카운터들과 메모리 접근과 같은 코드들은 조정이 필요한 경우가 있다.

비록 하나의 SSE2명령어가 두배의 MMX 명령어로 동작이 되지만 SSE2로 성능의 향상은 커다랗지 않다. 커다란 두가지 이유는 첫째, 16바이트 경계에 정렬되지 않은 메모리에 SSE2 데이터의 접근은 커다란 불이익이 발생하기 때문이고 두 번째로는 대부분의 x86에서 SSE2명령어의 처리량은 일반적으로 MMX 명령어보다 작다. 인텔은 첫 번째 문제를 정렬되지 않은 데이터의 접근할 때 생기는 추가적인 동작들을 줄이기 위해 [SSE3](../Page/SSE3.md "wikilink")명령어를 추가함으로써 해결을 하였으며 두 번째 문제는 인텔 [코어 마이크로아키텍처에서](https://ko.wikipedia.org/wiki/코어_마이크로아키텍처 "wikilink") 실행 엔진을 확대함으로써 해결을 하였다.

## 컴파일러 사용

2000년도에 처음 소개되었을 때, 소프트웨어 개발 툴은 SSE2를 지원하지 않았다. 예를 들면, 마이크로소프트 개발자 스튜디오 프로젝트에서 SSE2를 사용하기 위해서는 프로그래머가 직접 손으로 인라인 어셈블러를 작성하거나 또는 외부 소스로부터 오브젝트 코드를 불러와야 했다. 후에 비주얼 C++ 프로세서 팩에서는 [비주얼 C++과](https://ko.wikipedia.org/wiki/비주얼_C++ "wikilink") [MASM](https://ko.wikipedia.org/wiki/MASM "wikilink")에 SSE2를 지원을 추가하였다.

[인텔 C++ 컴파일러는](../Page/인텔_C++_컴파일러.md "wikilink") 손으로 작성된 어셈블리없이 자동으로 SSE4/SSSE3/SSE3/SSE2 와 SSE-코드를 생성하며 프로그래머가 어셈블리 수준에서 어떻게 적용할까 고민하는 것 대신에 알고리즘 개발에 더 집중하게 만들어 준다. SSE2의 발표 이후로 인텔 C 컴파일러는 윈도용 응용 소프트웨어 개발에서 SSE2의 채택을 가속화하였다.

[GCC](https://ko.wikipedia.org/wiki/GCC "wikilink") 3이후, GCC는 자동으로 SSE/SSE2 스칼라 코드를 생성하였으며 SSE/SSE2의 [자동 벡터화는](https://ko.wikipedia.org/wiki/자동_벡터화 "wikilink") GCC4부터 지원되었다. [썬 스튜디오 컴파일러 슈트](https://ko.wikipedia.org/wiki/썬_스튜디오_컴파일러_슈트 "wikilink") 또한 SSE2명령어를 컴파일러 플래그가 xvector=simd일 때 생성한다

## SSE2를 지원하는 CPU

  - AMD K8기반 CPU들 (애슬론 64, 샘프론 64, 튜리온 64, 등등)
  - [인텔](../Page/인텔.md "wikilink") [넷버스트](https://ko.wikipedia.org/wiki/넷버스트 "wikilink")기반 CPU들 ([펜티엄 4](../Page/펜티엄_4.md "wikilink"), [제온](../Page/제온.md "wikilink"), [셀러론](../Page/셀러론.md "wikilink"), [셀러론 D](https://ko.wikipedia.org/wiki/셀러론_D "wikilink"), 등등)
  - [인텔](../Page/인텔.md "wikilink") [펜티엄 M](../Page/펜티엄_M.md "wikilink") 와 [셀러론 M](https://ko.wikipedia.org/wiki/셀러론_M "wikilink")
  - [인텔 코어기반](../Page/인텔_코어.md "wikilink") CPU들 (코어 듀오, 코어 솔로, 등등)
  - [인텔 코어 2기반](../Page/인텔_코어_2.md "wikilink") CPU들 (코어 2 듀오, 코어 2 쿼드, 등등)
  - [인텔](../Page/인텔.md "wikilink") [아톰](../Page/인텔_아톰.md "wikilink")
  - 트렌스메타 Efficeon
  - 비아 C7
  - 비아 Nano

## SSE2를 지원하지 않는 IA-32 CPU

SSE2는 [IA-32](../Page/IA-32.md "wikilink") 아키텍처의 확장이다. 따라서 IA-32를 지원하지 않는 아키텍처는 SSE2를 지원하지 않는다. 모든 [x86-64](https://ko.wikipedia.org/wiki/x86-64 "wikilink") CPU는 SSE2를 적용하고 있다. IA-32는 SSE2보다 이전이기 때문에 초기 IA-32 CPU는 SSE2를 지원하지 않는다. SSE2와 다른 SIMD 명령어 집합은 주로 CPU의 게임등과 같은 실시간 그래픽의 향상을 위해서였다.

아래의 CPU들은 SSE2가 개발된 이후의 IA-32이지만 SSE2를 지원하지 않는다.

  - 소켓 A기반의 CPU를 포함하여 [애슬론 64](../Page/애슬론_64.md "wikilink") 이전의 [AMD](https://ko.wikipedia.org/wiki/AMD "wikilink") CPU
  - [펜티엄 4](../Page/펜티엄_4.md "wikilink") 이전 인텔 CPU
  - 비아 C3
  - 트렌스메타 크루소

## 같이 보기

<table>
<tbody>
<tr class="odd">
<td><ul>
<li><a href="../Page/스트리밍_SIMD_확장.md" title="wikilink">스트리밍 SIMD 확장</a> (SSE)</li>
<li><a href="../Page/SSE3.md" title="wikilink">SSE3</a></li>
<li><a href="../Page/SSSE3.md" title="wikilink">SSSE3</a></li>
<li><a href="../Page/SSE4.md" title="wikilink">SSE4</a></li>
<li><a href="../Page/SIMD.md" title="wikilink">SIMD</a></li>
</ul></td>
<td><ul>
<li><a href="https://ko.wikipedia.org/wiki/넷버스트_마이크로아키텍처" title="wikilink">넷버스트 마이크로아키텍처</a></li>
<li><a href="https://ko.wikipedia.org/wiki/네할렘_마이크로아키텍처" title="wikilink">네할렘 마이크로아키텍처</a></li>
<li><a href="../Page/마이크로아키텍처.md" title="wikilink">마이크로아키텍처</a></li>
<li><a href="https://ko.wikipedia.org/wiki/콘로" title="wikilink">콘로</a></li>
<li><a href="../Page/제온.md" title="wikilink">제온</a></li>
<li><a href="https://ko.wikipedia.org/wiki/코어_마이크로아키텍처" title="wikilink">코어 마이크로아키텍처</a></li>
</ul></td>
</tr>
</tbody>
</table>

[분류:SIMD 컴퓨팅](https://ko.wikipedia.org/wiki/분류:SIMD_컴퓨팅 "wikilink") [분류:X86 명령어](https://ko.wikipedia.org/wiki/분류:X86_명령어 "wikilink")