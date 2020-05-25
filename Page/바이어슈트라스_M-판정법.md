> This article is converted from Wikipedia: [바이어슈트라스 M-판정법](https://ko.wikipedia.org/wiki/바이어슈트라스_M-판정법).


[해석학에서](../Page/해석학_\(수학\).md "wikilink"), **바이어슈트라스 M-판정법**()은 [함수항 급수가](https://ko.wikipedia.org/wiki/함수항_급수 "wikilink") [균등 수렴할](https://ko.wikipedia.org/wiki/균등_수렴 "wikilink") [충분 조건을](https://ko.wikipedia.org/wiki/충분_조건 "wikilink") 제시하는 [수렴 판정법이다](https://ko.wikipedia.org/wiki/수렴_판정법 "wikilink"). [멱급수](../Page/멱급수.md "wikilink")를 다룰 때 유용하다.\[1\]

## 정의

\(\mathbb K\in\{\mathbb R,\mathbb C\}\)가 [실수체](https://ko.wikipedia.org/wiki/실수체 "wikilink") 또는 [복소수체](https://ko.wikipedia.org/wiki/복소수체 "wikilink")라고 하자.

### 실숫값 또는 복소숫값 함수항 급수

[집합](../Page/집합.md "wikilink") \(S\) 및 [함수열](https://ko.wikipedia.org/wiki/함수열 "wikilink") \(f_n\colon S\to\mathbb K\) (\(n\in\mathbb N\))이 주어졌다고 하자. 또한, 다음을 만족시키는 음이 아닌 실수의 열 \((M_n)_{n\in\mathbb N}\subseteq[0,\infty)\)이 존재한다고 하자.

  - 임의의 \(n\in\mathbb N\) 및 \(s\in S\)에 대하여, \(|f_n(s)|\le M_n\)
  - \(\textstyle\sum_{n=0}^\infty M_n<\infty\)

**바이어슈트라스 M-판정법**에 따르면, 함수항 급수 \(\textstyle\sum_{n=0}^\infty f_n\)는 [균등 수렴한다](https://ko.wikipedia.org/wiki/균등_수렴 "wikilink").  임의의 양의 실수 \(\epsilon>0\)에 대하여, \(\textstyle\sum_{n=0}^\infty M_n\)의 부분합이 [코시 수열이므로](https://ko.wikipedia.org/wiki/코시_수열 "wikilink"), 다음을 만족시키는 자연수 \(N_\epsilon\in\mathbb N\)가 존재한다.

  -
    임의의 \(m,n>N_\epsilon\)에 대하여, \(\textstyle\left|\sum_{k=m+1}^n M_k\right|<\epsilon\)

[삼각 부등식에](https://ko.wikipedia.org/wiki/삼각_부등식 "wikilink") 따라, 임의의 \(m,n>N_\epsilon\) 및 \(s\in S\)에 대하여,

\[\left|\sum_{k=m+1}^nf_k(s)\right|\le\sum_{k=m+1}^n|f_k(s)|\le\sum_{k=m+1}^nM_n<\epsilon\] 이다. [균등 수렴에](https://ko.wikipedia.org/wiki/균등_수렴 "wikilink") 대한 [코시 수렴 판정법에](../Page/코시_수렴_판정법.md "wikilink") 따라, \(\textstyle\sum_{n=0}^\infty f_n\)은 [균등 수렴한다](https://ko.wikipedia.org/wiki/균등_수렴 "wikilink").

### 바나흐 공간 값의 함수항 급수

보다 일반적으로, [집합](../Page/집합.md "wikilink") \(S\) 및 \(\mathbb K\)-[바나흐 공간](../Page/바나흐_공간.md "wikilink") \((X,\Vert\cdot\Vert)\) 및 [함수열](https://ko.wikipedia.org/wiki/함수열 "wikilink") \(f_n\colon S\to X\) (\(n\in\mathbb N\))이 주어졌다고 하자. 또한, 다음을 만족시키는 음이 아닌 실수의 열 \((M_n)_{n\in\mathbb N}\subseteq[0,\infty)\)이 존재한다고 하자.

  - 임의의 \(n\in\mathbb N\) 및 \(s\in S\)에 대하여, \(\Vert f_n(s)\Vert\le M_n\)
  - \(\textstyle\sum_{n=0}^\infty M_n<\infty\)

**바이어슈트라스 M-판정법**에 따르면, 함수항 급수 \(\textstyle\sum_{n=0}^\infty f_n\)는 [균등 수렴한다](https://ko.wikipedia.org/wiki/균등_수렴 "wikilink").  [유계 함수](../Page/유계_함수.md "wikilink") \(S\to X\)의 [벡터 공간](../Page/벡터_공간.md "wikilink") \(\mathcal B(S,X)\) 위에 다음과 같은 [상한 노름을](https://ko.wikipedia.org/wiki/상한_노름 "wikilink") 줄 수 있다.

\[\Vert f\Vert_\infty=\sup_{s\in S}\Vert f(s)\Vert\qquad(f\in\mathcal B(S,X))\] 이 경우 \(\mathcal B(S,X)\)는 위 노름에 대하여 [바나흐 공간을](../Page/바나흐_공간.md "wikilink") 이룬다 (증명: [완비 거리 공간\#완비 공간 값의 유계 함수](https://ko.wikipedia.org/wiki/완비_거리_공간#완비_공간_값의_유계_함수 "wikilink")).

각 \(n\in\mathbb N\)에 대하여 \(\Vert f_n\Vert_\infty\le M_n\)이며, \(\textstyle\sum_{n=0}^\infty M_n<\infty\)이므로, \(\textstyle\sum_{n=0}^\infty\Vert f_n\Vert_\infty<\infty\)이다. 즉, \(\textstyle\sum_{n=0}^\infty f_n\)은 (상한 노름에 대하여) [절대 수렴한다](../Page/절대_수렴.md "wikilink"). 따라서 \(\textstyle\sum_{n=0}^\infty f_n\)은 (상한 노름에 대하여) 수렴한다. 즉, [균등 수렴한다](https://ko.wikipedia.org/wiki/균등_수렴 "wikilink").

## 예

다음과 같은 함수열 \(f_n\colon[0,\infty)\to\mathbb R\) (\(n\in\mathbb Z^+\))을 생각하자.

\[f_n\colon x\mapsto x^2\exp(-nx)\] 그렇다면

\[f_n'(x)=x\exp(-nx)(2-nx)\] 이므로 각 \(f_n\)은 \(\textstyle x=\frac 2n\)에서 최댓값 \(\textstyle\left(\frac 2n\right)^2\exp(-2)\)을 가진다. \(\textstyle\sum_{n=1}^{\infty}\frac 1{n^2}<\infty\)이므로, \(\textstyle\sum_{n=1}^{\infty}f_n\)은 [균등 수렴한다](https://ko.wikipedia.org/wiki/균등_수렴 "wikilink").

## 역사

[카를 바이어슈트라스의](../Page/카를_바이어슈트라스.md "wikilink") 이름을 땄다.

## 각주

## 참고 문헌

  - : 148.

[분류:수렴판정법](https://ko.wikipedia.org/wiki/분류:수렴판정법 "wikilink") [분류:함수해석학](https://ko.wikipedia.org/wiki/분류:함수해석학 "wikilink")

1.