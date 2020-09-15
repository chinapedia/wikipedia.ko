> This article is converted from Wikipedia: [H-공간](https://ko.wikipedia.org/wiki/H-공간).


**H-공간**()과 **쌍대 H-공간**()은 위상 공간으로부터 정의된 대수 구조이다.

## 정의

위상 공간 \(X\)가 주어졌을 때, H-공간은 다음과 같은 데이터로 구성된다.

  - 연속 함수 \(\mu \colon X \times X \to X\)
  - [항등원](../Page/항등원.md "wikilink") \(e \in X\): 모든 \(x \in X\)에 대해 \(x \mapsto \mu(x, e)\)와 \(x \mapsto \mu(e, x)\)가 모두 항등 함수 \(\operatorname{id}_x\)와 호모토피 동치가 되게 한다.

H-공간은 항등원이 있는 [마그마이지만](../Page/마그마_\(수학\).md "wikilink") 일반적으로 역원이 존재하지 않고 [결합 법칙이](https://ko.wikipedia.org/wiki/결합_법칙 "wikilink") 성립하지 않는다. 만약 군의 공리를 만족하는 경우 **H-군**()이라 부른다.

### 쌍대 H-공간

쌍대 H-공간은 다음과 같은 데이터로 구성된다.

  - 연속 함수 \(\mu \colon X \to X \vee X\)
  - [항등원](../Page/항등원.md "wikilink") \(e \in X\)

## 예와 성질

### 위상군

[위상군](../Page/위상군.md "wikilink") \(G\)와 그 연산 \(G \times G \to G\)는 그 자체로 H-군을 이룬다.

### 초구

[초구](../Page/초구.md "wikilink")의 경우 H-공간이 되는 것은 \(\mathbb S^0\), \(\mathbb S^1\), \(\mathbb S^3\), \(\mathbb S^7\)밖에 없다. \(\mathbb S^7\)을 제외한 나머지 3개는 모두 H-군이며 [리 군을](../Page/리_군.md "wikilink") 이룬다.

\(n \ge 1\)일 경우 초구 \(\mathbb S^n\)에 다음과 같은 [CW 복합체](../Page/CW_복합체.md "wikilink") 구조를 줄 수 있다:

  - 0차원 세포 1개 \(\bullet\). 이는 \(\mathbb S^n\)의 적도 위의 한 점이다.
  - \(n-1\)차원 세포 1개. 즉, \(n-1\)차원 뼈대는 [초구](../Page/초구.md "wikilink") \(\mathbb S^{n-1}\)이다. 이는 \(\mathbb S^n\)의 적도에 해당한다.
  - \(n\)차원 세포 2개. 이들은 각각 \(\mathbb S^n\)의 북반구와 남반구에 대응한다.

적도에 있는 \(n-1\)차원 세포 \(\mathbb S^{n-1}\hookrightarrow\mathbb S^n\)에 대한 [몫공간](../Page/몫공간.md "wikilink") \(\mathbb S^n/\mathbb S^{n-1}\)을 취하면 두 초구의 [쐐기합](https://ko.wikipedia.org/wiki/쐐기합 "wikilink")을 얻는다.

\[w_n\colon \mathbb S^n\twoheadrightarrow\mathbb S^n/\mathbb S^{n-1}\cong\mathbb S^n\vee\mathbb S^n\] 이 [몫공간](../Page/몫공간.md "wikilink") 함수 \(w_n\)을 연산자로 삼아서 \(\mathbb S^n\) 위의 쌍대 H-공간을 정의할 수 있다.

### 현수 공간과 고리 공간

일반적으로 임의의 [점을 가진 공간](../Page/점을_가진_공간.md "wikilink") \(X\)에 대하여 그 [축소 현수](https://ko.wikipedia.org/wiki/축소_현수 "wikilink") \(\Sigma X\)는 쌍대 H-공간을 이룬다. \(\Sigma X = X\wedge\mathbb S^1 = (X\times\mathbb S^1)/(X\vee\mathbb S^1)\) 위에서 연산을 다음과 같이 정의한다.

\[(\operatorname{id}_X\wedge w_1)\colon X\wedge\mathbb S^1\to X\wedge(\mathbb S^1\vee\mathbb S^1)\cong(X\wedge\mathbb S^1)\vee(X\wedge\mathbb S^1)\]

여기서 \(\wedge\)는 [분쇄곱](../Page/분쇄곱.md "wikilink"), \(\vee\)는 [쐐기합](https://ko.wikipedia.org/wiki/쐐기합 "wikilink")이고, \(w_1\)은 위 초구의 쌍대 H-공간에서 정의한 연산이다. 초구의 경우 \(\Sigma \mathbb S^{n-1}\simeq\mathbb S^n\)이므로, 초구의 쌍대 H-공간 구조는 현수의 쌍대 H-공간 구조의 특수한 경우이다.

거꾸로 [고리 공간](../Page/고리_공간.md "wikilink") \(\Omega X\)는 H-공간을 이룬다. 구체적으로, \(\Omega X\) 위의 곱셈은 다음과 같다.

\[m\colon (\gamma,\gamma')\mapsto (\gamma\vee\gamma')\circ w_1\] 여기서

\[\gamma,\gamma'\colon\mathbb S^1\to X\]

\[\gamma\vee\gamma'\colon\mathbb S^1\vee\mathbb S^1\to X\]

\[w_1\colon\mathbb S^1\to\mathbb S^1\vee\mathbb S^1\] 이다.

### 에일렌베르크-매클레인 공간과 피터슨 공간

[아벨 군](../Page/아벨_군.md "wikilink") \(G\) 및 자연수 \(n\)에 대하여, [에일렌베르크-매클레인 공간](../Page/에일렌베르크-매클레인_공간.md "wikilink") \(K(G,n)\)는 다른 공간의 고리 공간이다.

\[K(G,n)\simeq \Omega K(G,n+1)\] 그러므로 에일렌베르크-매클레인 공간 \(K(G,n)\)은 H-공간을 이룬다.

마찬가지로 [유한 생성 아벨 군](https://ko.wikipedia.org/wiki/유한_생성_아벨_군 "wikilink") \(G\) 및 \(n\ge3\)의 경우 [피터슨 공간](https://ko.wikipedia.org/wiki/피터슨_공간 "wikilink") \(P(G,n)\)는 다른 공간의 축소 현수 공간이다.

\[P(G,n)\simeq\Sigma P(G,n-1)\] 그러므로 피터슨 공간 \(P(G,n)\)은 쌍대 H-공간을 이룬다.

### 호모토피류의 연산

[호모토피 군은](../Page/호모토피_군.md "wikilink") 초구에서 공간 \(X\)으로 가는 호모토피류 \([\mathbb S^n,X]_\bullet\)로, 그 위에서의 연산은 호모토피 합성함수 \(h \colon \mathbb S^n \vee \mathbb S^n \to \mathbb S^n\)에 의해 정의된다:

  -
    \([f] \cdot [g] \colon x \mapsto (f \vee g)(h(x))\)

일반적으로, 쌍대 H-공간 \((X, \mu)\)에서 공간 \(Y\)로 가는 호모토피류 \([X,Y]_\bullet\) 위의 [이항 연산을](https://ko.wikipedia.org/wiki/이항_연산 "wikilink") 다음과 같이 정의할 수 있다.

  -
    \([f] \cdot [g] \colon x \mapsto (f \vee g)(\mu(x))\)

거꾸로 공간 \(X\)에서 H-공간 \((Y, \mu)\)로 가는 호모토피류의 연산을 다음과 같이 정의할 수 있다.

\[[f]\cdot[g] \colon x \mapsto \mu(f(x),g(x))\]

위에서 만약 각각이 (쌍대) H-군의 구조를 가질 경우 \([X,Y]_\bullet\)은 [군의](../Page/군_\(수학\).md "wikilink") 구조를 가진다.

[에크만-힐튼 쌍대성에](https://ko.wikipedia.org/wiki/에크만-힐튼_쌍대성 "wikilink") 의해 [축소 현수](https://ko.wikipedia.org/wiki/축소_현수 "wikilink") \(\Sigma\)와 [고리 공간](../Page/고리_공간.md "wikilink") \(\Omega\)는 서로 [수반 함자를](../Page/수반_함자.md "wikilink") 이루므로, 이에 의한 호모토피류의 군 구조도 서로 일치한다:

  -
    \([X,\Omega Y]_\bullet \cong [\Sigma X,Y]_\bullet\)

특히, \(\Sigma \mathbb S^{n-1} \cong \mathbb S^n\)이므로 호모토피 군에 대해 \(\pi_{n-1}(\Omega X) \cong \pi_n(X)\)가 성립한다.

## 역사

[장피에르 세르가](../Page/장피에르_세르.md "wikilink") [하인츠 호프의](../Page/하인츠_호프.md "wikilink") 이론에 영향을 받아 만들었고, 호프의 이름의 머리글자인 H를 붙였다.\[1\]

## 참고 문헌

<references/>

[분류:호모토피 이론](https://ko.wikipedia.org/wiki/분류:호모토피_이론 "wikilink")

1.  J. R. Hubbuck. "A Short History of H-spaces", History of topology, 1999, pages 747–755.