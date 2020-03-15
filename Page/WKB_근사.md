> This article is converted from Wikipedia: [WKB ](https://ko.wikipedia.org/wiki/WKB_).


[양자역학](https://ko.wikipedia.org/wiki/양자역학 "wikilink")에서, **WKB 근사**(WKB近似, )는 [슈뢰딩거 방정식을](https://ko.wikipedia.org/wiki/슈뢰딩거_방정식 "wikilink") 풀 때, 순수하게 양자역학적인 효과가 작아 [파동 함수의](https://ko.wikipedia.org/wiki/파동_함수 "wikilink") 진폭 또는 위상이 거의 일정하다는 가정 아래 푸는 근사법이다.

## 1차원 퍼텐셜 속의 입자

1차원 공간에서 에너지 \(E\)를 가지고 퍼텐셜 \(V(x)\)에 영향을 받는 입자의 [파동 함수](https://ko.wikipedia.org/wiki/파동_함수 "wikilink") \(\Psi(x)\)는 다음과 같은 시간 무관 [슈뢰딩거 방정식을](https://ko.wikipedia.org/wiki/슈뢰딩거_방정식 "wikilink") 따른다.

\[-\frac{\hbar^2}{2m} \frac{\mathrm{d}^2}{\mathrm{d}x^2} \Psi(x) + V(x) \Psi(x) = E \Psi(x)\]. 이제 파동 함수 \(\Psi\)를 다음과 같이 그 로그의 실수 및 허수 성분의 도함수로 나타내자.

\[\Psi(x)=\exp\left(\int (A(x)+iB(x))\,dx\right)\]. 이를 슈뢰딩거 방정식에 대입하여 정리하면 다음과 같은 두 방정식을 얻는다.

\[A'(x) + A(x)^2 - B(x)^2 = \frac{2m}{\hbar^2} \left( V(x) - E \right)\]

\[B'(x) + 2 A(x) B(x) = 0\].

이 연립 [미분 방정식을](https://ko.wikipedia.org/wiki/미분_방정식 "wikilink") 풀기 위해, 다음과 같은 반고전 근사법()을 취한다. 우선, 파동 함수 성분\(A\)와 \(B\)를 [디랙 상수](https://ko.wikipedia.org/wiki/디랙_상수 "wikilink") \(\hbar\)에 대한 [테일러 급수로](https://ko.wikipedia.org/wiki/테일러_급수 "wikilink") 전개한다. (위 식에 따라 \(A,B=O(1/\hbar)\)이므로 그 첫 항은 \(\hbar^0\)이 아니라 \(\hbar^{-1}\)이 된다.)

\[A(x)=\sum_{n=0}^\infty \hbar^{n-1} A_n(x)\]

\[B(x)=\sum_{n=0}^\infty \hbar^{n-1} B_n(x)\]. 디랙 상수는 아주 작으므로, 급수의 가장 낮은 차수의 항부터 먼저 보자.

\[A_0(x)^2-B_0(x)^2=2m\left( V(x) - E \right)\]

\[A_0(x)B_0(x)=0\]. 두 번째 방정식에 따라 \(A_0=0\) 또는 \(B_0=0\)이다. 첫 번째 방정식에 따라 \(V(x)<E\)이면 \(A_0=0\), \(B_0\ne0\)으로, \(V(x)>E\)이면 \(A_0\ne0\), \(B_0=0\)으로 놓는다. 전자는 고전적인 경우, 후자는 [터널링](https://ko.wikipedia.org/wiki/터널링 "wikilink")이 일어나는 경우를 나타낸다.

그 다음 차수의 항은 다음과 같다.

\[A_0'(x)+2A_0(x)A_1(x)-2B_0(x)B_1(x)=0\]

\[B_0'(x)+2A_0(x)B_1(x)+2A_1(x)B_0(x)=0\]. 첫 번째 식에 의해, \(A_0=0\)이면 \(B_1=0\)이다. 두 번째 식에 의해, \(B_0=0\)이어도 \(B_1=0\)이다.

### 고전적인 경우

이 경우는 총 에너지 \(E\)가 위치 에너지 \(V(x)\)보다 더 크므로, 입자가 고전적으로 존재할 수 있는 영역이다. 여기서는 \(A_0=0\)이고,

\[B_0(x)=\pm\sqrt{ 2m \left( E - V(x) \right) }\] 이다. 이는 파동 함수의 진폭(\(A\))은 별로 변하지 않지만 그 위상(\(B\))이 많이 변하는 꼴이다.

다음 차수의 항 \(A_1\)을 구하면 다음과 같다.

\[A_1=-B_0'/2B_0=-\frac12(\ln B_0)'\]. 따라서 파동 함수 \(\Psi(x)\)는 대략

\[\Psi(x)\approx CB_0^{-1/2}\exp\left(i\int B_0\,dx\right)=\frac{C_+\exp\left(i \int \sqrt{\frac{2m}{\hbar^2} \left( E - V(x) \right)} dx\right)+
C_-\exp\left(-i \int \sqrt{\frac{2m}{\hbar^2} \left( E - V(x) \right)} dx\right)
}{\sqrt[4]{\frac{2m}{\hbar^2} \left( E - V(x) \right)}}\] 으로 근사할 수 있다. 여기서 \(C_+\)와 \(C_-\)는 임의의 적분 상수이다. 이에 따라, 고전적인 영역에서는 파동 함수는 대략 사인파의 모양이다.

### 터널 효과

이 경우는 위치 에너지 \(V\)가 총 에너지 \(E\)보다 더 크므로 입자가 고전적으로 존재할 수 없는 영역이다. 즉, [터널 효과에](https://ko.wikipedia.org/wiki/터널_효과 "wikilink") 해당한다. 여기에는 \(B_0(x) = 0\)이고,

\[A_0(x) = \pm \sqrt{ 2m \left( V(x) - E \right) }\] 이다. 다음 차수의 항 \(A_1\)을 구하면 다음과 같다.

\[A_1=-A_0'/2A_0=-\frac12(\ln A_0)'\]. 따라서 파동 함수 \(\Psi(x)\)는 대략

\[\Psi(x)\approx DA_0^{-1/2}\exp\left(\int A_0\,dx\right)=\frac{ D_{+}\exp\left(\int\sqrt{\frac{2m}{\hbar^2} \left( V(x) - E \right)}\,dx\right) + D_{-} \exp\left(-\int\sqrt{\frac{2m}{\hbar^2} \left( V(x) - E \right)}\,dx\right)}{\sqrt[4]{\frac{2m}{\hbar^2} \left( V(x) - E \right)}}\] 으로 근사할 수 있다. 여기서 \(D_+\)와 \(D_-\)는 임의의 적분 상수이다. 이에 따라, 터널링 영역에서는 파동 함수는 [지수 함수의](https://ko.wikipedia.org/wiki/지수_함수 "wikilink") 모양을 따른다.

### 연결 공식

고전적인 경우와 [터널 효과인](https://ko.wikipedia.org/wiki/터널_효과 "wikilink") 경우의 해는 \(V\approx E\)가 되는 점 근처에서 발산한다. 따라서 이런 점 근처에는 **연결 공식**()를 사용하여 두 해의 계수 \(C_\pm\), \(D_\pm\)를 (전체 파동 함수가 [연속 미분 가능하게끔](https://ko.wikipedia.org/wiki/연속_미분_가능 "wikilink")) 서로 맞추어야 한다.

고전적인 영역과 터널링 영역이 \(x_0\)에서 만난다고 하자. 즉,

\[V(x_0)=E\] 이라고 하자. 그렇다면 \(x_0\) 근처에서 퍼텐셜 \(V(x)\)를

\[V(x)\approx V'(x_0)(x-x_0)+E\] 와 같이 근사할 수 있다. 그렇다면 풀어야 할 슈뢰딩거 방정식은 다음과 같다.

\[\frac{\hbar^2}{2m}\Psi''=V'(x_0)\Psi(x)(x-x_0)\]. 이는 [에어리 함수를](https://ko.wikipedia.org/wiki/에어리_함수 "wikilink") 사용하여 풀 수 있다. 그 일반적인 해는 다음과 같다.

\[\Psi(x)=aAi(\sqrt[3]{2mV'(x_0)/\hbar^2}x)+bBi(\sqrt[3]{2mV'(x_0)/\hbar^2}x)\]. 여기서 \(a\)와 \(b\)는 임의의 상수이다.

\(x\gg1\)일 때, 에어리 함수는 다음을 만족한다.

\[Ai(x)\approx\frac{\exp(-\frac23x^{3/2})}{2\sqrt{\pi}x^{1/4}}\] (분모에 2가 있는 것에 주의\!)

\[Bi(x)\approx\frac{\exp(\frac23x^{3/2})}{\sqrt{\pi}x^{1/4}}\]

\[Ai(-x)\approx\frac{\sin(\frac23x^{3/2}+\pi/4)}{\sqrt{\pi}x^{1/4}}\]

\[Bi(-x)\approx\frac{\cos(\frac23x^{3/2}+\pi/4)}{\sqrt{\pi}x^{1/4}}\]. 이를 고전적 영역의 해와 터널링 영역의 해와 비교하면 계수 사이의 관계를 얻을 수 있다. 이를 **연결 공식**이라고 한다. 예를 들어, \(x<x_0\)은 고전적인 영역이고, \(x>x_0\)은 터널링 영역이라고 하자. 그렇다면

\[D_+-2iD_-=2C_+\exp(-i\pi/4)\]

\[D_++2iD_-=2C_-\exp(i\pi/4)\] 이다. 그 반대로, \(x>x_0\)이 고전적이고 \(x<x_0\)이 터널링인 경우에도 유사한 공식을 유도할 수 있다.

## 일반적 경우

\(n\)차원 [리만 다양체](https://ko.wikipedia.org/wiki/리만_다양체 "wikilink") \(M\) 위의 입자가 퍼텐셜 \(V\colon M\to\mathbb R\) 속에서 움직인다고 하자. 이 경우, [파동 함수에](https://ko.wikipedia.org/wiki/파동_함수 "wikilink") 대하여 다음과 같은 [가설 풀이를](https://ko.wikipedia.org/wiki/가설_풀이 "wikilink") 고르자.

\[\psi(x)=\exp(iS(x)/\hbar)\sum_{k=0}^\infty a_k(x)\hbar^k\] 여기서, 각 항의 단위는 다음과 같다.

  - \(S(x)\)는 작용의 단위를 갖는다.
  - \(a_k(x)\)는 \[길이\]<sup>−*n*/2</sup>\[작용\]<sup>−k</sup>의 단위를 갖는다.

이를 [슈뢰딩거 방정식](https://ko.wikipedia.org/wiki/슈뢰딩거_방정식 "wikilink")

\[0=\left(-\hbar^2\nabla^2+2m(V(x)-E)\right)\psi\] 에 대입하여 \(\hbar\)의 각 계수별로 비교하면, 다음과 같은 일련의 [편미분 방정식을](https://ko.wikipedia.org/wiki/편미분_방정식 "wikilink") 얻는다.\[1\]

\[\nabla^\mu S(x)\nabla_\mu S(x)=2m\left(E-V(x)\right)\]

\[\left(\left(\nabla^2S(x)\right)+2(\partial^\mu S)\partial_\mu\right)a_0(x)=0\]

\[\left(\left(\nabla^2S(x)\right)+2(\partial^\mu S)\partial_\mu\right)a_k(x)=i\nabla^2a_{k-1}(x)\] 고전적 영역에서는 \(S\)는 실수이며, 터널 영역에서는 \(S\)는 허수가 된다.

처음 두 개의 [편미분 방정식은](https://ko.wikipedia.org/wiki/편미분_방정식 "wikilink") 다음과 같이 기하학적으로 해석할 수 있다. 우선, [심플렉틱 다양체](https://ko.wikipedia.org/wiki/심플렉틱_다양체 "wikilink") \(T^*M\)의 다음과 같은 [라그랑주 부분 다양체를](../Page/라그랑주_부분_다양체.md "wikilink") 정의하자.

\[L=\{(x,p)\colon x\in M,\;p=\partial_\mu S(x)\in T_x^*M\}\subset T^*M\] 이 경우, 다음과 같은 자연스러운 사영 사상이 존재하며, 이는 [미분 동형을](https://ko.wikipedia.org/wiki/미분_동형 "wikilink") 이룬다.

\[\pi\colon L\to M\]

\[\pi\colon (x,p)\mapsto x\] 그렇다면, 처음 두 개의 WKB 방정식은 다음과 같이 해석할 수 있다.\[2\]

  - \(S\)에 대한 방정식은 [해밀턴-야코비 방정식이며](https://ko.wikipedia.org/wiki/해밀턴-야코비_방정식 "wikilink"), 이는 [해밀토니언](https://ko.wikipedia.org/wiki/해밀토니언 "wikilink")을 \(L\)에 국한하였을 경우 [상수 함수임을](../Page/상수_함수.md "wikilink") 뜻한다.
      -
        \(H|_L=E\)
  - \(a_0\)에 대한 방정식 \(\nabla^\mu(a^2\partial_\mu S)=0\)은 수송 방정식()이며, 이는 \(L\) 위에 정의된 [밀도](../Page/밀도_다발.md "wikilink") \(\pi^*\left(a_0^2(x)\sqrt{\det g(x)} dx^1\wedge\cdots\wedge dx^n\right)\)가 해밀토니언 벡터장 \((X_H)^I=(\omega^{-1})^{IJ}\partial_JH\)에 대하여 불변인 것을 뜻한다. ([해밀턴-야코비 방정식에](https://ko.wikipedia.org/wiki/해밀턴-야코비_방정식 "wikilink") 의하여, 해밀토니언 벡터장은 항상 \(L\)의 접벡터이다.) 여기서 \(\mathcal L\)은 [밀도의](../Page/밀도_다발.md "wikilink") [리 미분이며](../Page/리_미분.md "wikilink"), \(\pi^*\)는 \(\pi\)에 대한 [당김이다](https://ko.wikipedia.org/wiki/당김_\(미분기하학\) "wikilink").
      -
        \(\mathcal L_{X_H}\pi^*\left(a_0^2(x)\sqrt{\det g(x)}dx^1\wedge\cdots\wedge dx^n\right)=0\)

따라서, 처음 두 WKB 방정식은 [기하학적 양자화에서](../Page/기하학적_양자화.md "wikilink"), [라그랑주 부분 다양체](../Page/라그랑주_부분_다양체.md "wikilink") 및 그 위에 주어진 [½-밀도로서](../Page/밀도_다발.md "wikilink") 주어진 고전적 상태가 만족시켜야 하는 조건을 나타낸다. 그러나 나머지 WKB 방정식들은 이와 같이 간단한 기하학적 해석을 부여하기 힘들다.

## 역사

1923년에 영국의 수학자 해럴드 제프리스()가 이 근사법을 이차 [미분 방정식에](https://ko.wikipedia.org/wiki/미분_방정식 "wikilink") 대한 일반적인 근사법으로 도입하였다.\[3\] 1925년 [슈뢰딩거 방정식이](https://ko.wikipedia.org/wiki/슈뢰딩거_방정식 "wikilink") 발표되자, 그 이듬해인 1926년에 독일의 [그레고어 벤첼](https://ko.wikipedia.org/wiki/그레고어_벤첼 "wikilink")()\[4\], 네덜란드의 [헨드릭 안토니 크라머르스](../Page/헨드릭_안토니_크라머르스.md "wikilink")\[5\], 프랑스의 [레옹 브릴루앵](https://ko.wikipedia.org/wiki/레옹_브릴루앵 "wikilink")\[6\] 이 독자적으로 이에 대한 근사법을 발표하였다. 넷 다 사실상 같은 방법이었으나 이들은 서로의 업적을 처음에 알지 못했다. 이에 따라 보통 WKB 또는 JWKB 근사법으로 불린다.

## 참고 문헌

  -
## 외부 링크

  -
  -
  -
  -
## 같이 보기

  - [투과계수](https://ko.wikipedia.org/wiki/투과계수 "wikilink")
  - [기하학적 양자화](../Page/기하학적_양자화.md "wikilink")

[분류:양자역학](https://ko.wikipedia.org/wiki/분류:양자역학 "wikilink") [분류:수리물리학](https://ko.wikipedia.org/wiki/분류:수리물리학 "wikilink")

1.
2.
3.
4.
5.
6.