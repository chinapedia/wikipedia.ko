> This article is converted from Wikipedia: [스핀C 다양체](https://ko.wikipedia.org/wiki/스핀C_다양체).


[미분기하학](../Page/미분기하학.md "wikilink")에서, **스핀C 다양체**(spin多樣體, )는 그 [직교 틀다발이](https://ko.wikipedia.org/wiki/직교_틀다발 "wikilink") [스핀C 군에](../Page/스핀C_군.md "wikilink") 대한 [주다발](../Page/주다발.md "wikilink")로의 올림을 갖춘 [준 리만 다양체이다](../Page/준_리만_다양체.md "wikilink"). 스핀C 구조는 [자이베르그-위튼 방정식](../Page/자이베르그-위튼_이론.md "wikilink") 등을 정의하기 위한 [필요 조건이다](https://ko.wikipedia.org/wiki/필요_조건 "wikilink").

## 정의

**스핀C 구조**()의 정의는 [스핀 구조의](https://ko.wikipedia.org/wiki/스핀_구조 "wikilink") 정의와 유사하지만, [스핀 군](https://ko.wikipedia.org/wiki/스핀_군 "wikilink") 대신 [스핀C 군을](../Page/스핀C_군.md "wikilink") 사용한다.

즉, \(n\)차원 [가향](https://ko.wikipedia.org/wiki/가향_다양체 "wikilink") [준 리만 다양체](../Page/준_리만_다양체.md "wikilink") \((M,g)\) 위의 **스핀C 구조**()는 다음 조건을 따르는 Spin(*n*)<sup>c</sup>-주다발 \(\pi_{\operatorname{Spin^c}}\colon P_{\operatorname{Spin^c}}(M)\twoheadrightarrow M\)과 [주다발 사상](https://ko.wikipedia.org/wiki/주다발_사상 "wikilink") \(p\colon P_{\operatorname{Spin^c}}(M)\to P_{\operatorname{SO}}(M)\) 으로 구성된다.

  - \(\pi_{\operatorname{SO}}\circ p=\pi_{\operatorname{Spin^c}}\)
  - 임의의 \(x\in P_{\operatorname{Spin^c}}\), \(h\in\operatorname{Spin^c}(n)\)에 대하여 \(p(x\cdot h)=p(x)\cdot\rho(h)\)이다. (여기서 \(\cdot\)은 적절한 [군의 작용이며](../Page/군의_작용.md "wikilink"), \(\rho\colon\operatorname{Spin^c}(n)\twoheadrightarrow\operatorname{SO}(n)\)은 [군 준동형이다](https://ko.wikipedia.org/wiki/군_준동형 "wikilink").) 즉 군의 작용은 \(p\)와 가환한다.

## 성질

[매끄러운 다양체](../Page/매끄러운_다양체.md "wikilink") \(M\) 위에 스핀C 구조가 존재할 [필요 충분 조건은](https://ko.wikipedia.org/wiki/필요_충분_조건 "wikilink") 3차 정수 [슈티펠-휘트니 특성류](../Page/슈티펠-휘트니_특성류.md "wikilink")

\[W_3(M)=\beta w_2(M)\in\operatorname H^3(M;\mathbb Z)\] 가 0인지 여부이다. 여기서 \(\beta\)는 [복시테인 준동형](../Page/복시테인_준동형.md "wikilink")

\[\beta\colon\operatorname H^2(M;\mathbb Z/2)\to\operatorname H^3(M;\mathbb Z)\] 이다.

## 분류

만약 다양체 \(M\) 위에 스핀C 구조가 존재할 수 있다면, 가능한 스핀C 구조들의 공간은 \(\operatorname H^2(M;\mathbb Z)\) 위의 [아핀 공간이다](../Page/아핀_공간.md "wikilink").

이는 직관적으로 다음과 같이 해석할 수 있다. [아벨 군의](../Page/아벨_군.md "wikilink") [짧은 완전열](https://ko.wikipedia.org/wiki/짧은_완전열 "wikilink")

\[0\to\mathbb Z\stackrel{\cdot2}\hookrightarrow\mathbb Z\stackrel{+2\mathbb Z}\twoheadrightarrow\mathbb Z/2\to0\] 을 생각하자. 이에 따라, [지그재그 보조정리를](https://ko.wikipedia.org/wiki/지그재그_보조정리 "wikilink") 사용하여 다음과 같은 [긴 완전열이](https://ko.wikipedia.org/wiki/긴_완전열 "wikilink") 존재한다.

\[\dotsb\to\operatorname H^2(M,\mathbb Z)\xrightarrow{\cdot2}\operatorname H^2(M;\mathbb Z)\xrightarrow{\bmod2}\operatorname H^2(M;\mathbb Z/2)\xrightarrow\beta\operatorname H^3(M;\mathbb Z)\to\cdots\] 여기서 \(\beta\)는 [복시테인 준동형이다](../Page/복시테인_준동형.md "wikilink").

스핀C 구조는 원래 방해물(obstruction)에 막혀 [스핀 구조를](https://ko.wikipedia.org/wiki/스핀_구조 "wikilink") 이루지 못하는 구조를, 같은 방해물에 막혀 [U(1)](https://ko.wikipedia.org/wiki/U\(1\) "wikilink") [주다발](../Page/주다발.md "wikilink")을 이루지 못하는 구조로 뒤틀어(twist) 만든 것이다. [U(1)](https://ko.wikipedia.org/wiki/U\(1\) "wikilink") [주다발](../Page/주다발.md "wikilink")들은 그 [천 특성류](../Page/천_특성류.md "wikilink") \(c_2\in H^2(M,\mathbb Z)\)에 의하여 분류된다. 이는 위 [긴 완전열에서](https://ko.wikipedia.org/wiki/긴_완전열 "wikilink") 첫 \(H^2(M,\mathbb Z)\)에 해당하며, 이는 두 번째 \(H^2(M,\mathbb Z)\)에서 \(\cdot2\)의 [상에](../Page/상_\(수학\).md "wikilink") 해당한다. 반면, 방해물에 막힌 U(1) ‘주다발’은 두 번째 \(H^2(M,\mathbb Z)\)에서 \(\cdot2\)의 [상에](../Page/상_\(수학\).md "wikilink") 속하지 않은 원소들이다. 이 원소를 \(\alpha\in H^2(M;\mathbb Z)\)라고 하자. 스핀 구조의 방해물은 2차 [슈티펠-휘트니 특성류](../Page/슈티펠-휘트니_특성류.md "wikilink") \(w_2\in H^2(M;\mathbb Z/2)\)이므로, 이 방해물이 U(1) ‘주다발’의 방해물 \(\alpha\)와 같으려면 \(\bmod2\)에 따른 \(\alpha\)의 [상이](../Page/상_\(수학\).md "wikilink") \(w_2\)이어야 한다. [완전열](../Page/완전열.md "wikilink")의 성질에 의하여, 이 조건은 \(w_2\)의 [복시테인 준동형에](../Page/복시테인_준동형.md "wikilink") 따른 상 \(\beta w_2=W_3\in\operatorname H^3(M,\mathbb Z)=0\)인 조건과 [동치](../Page/동치.md "wikilink")이다.

## 예

다음과 같은 다양체들은 적어도 하나의 스핀C 구조를 갖는다.

  - 모든 4차원 이하 [콤팩트](../Page/콤팩트_공간.md "wikilink") [유향 다양체는](https://ko.wikipedia.org/wiki/유향_다양체 "wikilink") 스핀C 구조를 갖는다.
  - 모든 [개복소 다양체는](https://ko.wikipedia.org/wiki/개복소_다양체 "wikilink") 스핀C 구조를 갖는다. 이 경우 대응되는 [복소수 선다발은](https://ko.wikipedia.org/wiki/복소수_선다발 "wikilink") [복소수 접다발](https://ko.wikipedia.org/wiki/복소수_접다발 "wikilink") \(\mathrm T^+M\)의 [행렬식 선다발](https://ko.wikipedia.org/wiki/행렬식_선다발 "wikilink") \(\textstyle\bigwedge^{\dim_{\mathbb C}M}\mathrm T^+M\)이다.
  - 모든 [스핀 다양체는](../Page/스핀_다양체.md "wikilink") 스핀C 구조를 갖는다. 이 경우 대응되는 [복소수 선다발은](https://ko.wikipedia.org/wiki/복소수_선다발 "wikilink") 자명한 다발이다.

## 외부 링크

  -
  -
  -
  -
[분류:리만 기하학](https://ko.wikipedia.org/wiki/분류:리만_기하학 "wikilink")