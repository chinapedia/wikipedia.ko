> This article is converted from Wikipedia: [A∞-오퍼라드](https://ko.wikipedia.org/wiki/A∞-오퍼라드).


[오퍼라드 이론에서](https://ko.wikipedia.org/wiki/오퍼라드_이론 "wikilink"), **A<sub>∞</sub>-오퍼라드**()는 [호모토피](../Page/호모토피.md "wikilink")를 무시한다면 [결합 법칙이](https://ko.wikipedia.org/wiki/결합_법칙 "wikilink") 성립하는 대수들을 나타내는 [오퍼라드](../Page/오퍼라드.md "wikilink")이다.

## 정의

[위상 공간](https://ko.wikipedia.org/wiki/위상_공간_\(수학\) "wikilink") 위에 작용하는 오퍼라드 \(A\)에 대하여, 만약 \(A(n)\)이 ([이산 공간의](../Page/이산_공간.md "wikilink") 위상을 준) [대칭군](../Page/대칭군_\(군론\).md "wikilink") \(\operatorname{Sym}(n)\)과 [호모토피 동치이며](../Page/호모토피_동치.md "wikilink"), 또한 \(A(n)\) 위의 대칭군 \(\operatorname{Sym}(n)\)의 작용이 군 위의 스스로의 작용과 같다면, \(A\)를 **A<sub>∞</sub>-오퍼라드**라고 한다.

## A<sub>∞</sub>-대수

A<sub>∞</sub>-오퍼라드를 [벡터 공간의](../Page/벡터_공간.md "wikilink") [모노이드 범주](../Page/모노이드_범주.md "wikilink") 위에 표현하면, **A<sub>∞</sub>-대수**를 얻는다. A<sub>∞</sub>-대수 \(A\)는 다음과 같이 정수 등급을 갖는 벡터 공간이며,

\[A=\bigoplus_{p\in\mathbb Z}A^p\] 다음과 같은 무한한 수의 연산들을 갖는다. 모든 \(n\ge1\)에 대하여, \(n\)항 \(n\)겹선형 연산

\[m_n\colon A^{\oplus n}\to A\]

\[\deg m_n=2-n\] 이 존재한다.

이들은 다음과 같은 무한한 수의 항등식들을 만족시킨다. 모든 \(n\ge1\)에 대하여 다음이 성립한다.

\[\sum_{r+s+t=n}(-1)^{r+st}m_{r+1+t}(a_1,\dots,a_r,m_s(b_1,\dots,b_s),c_1,\dots,c_t)=0\qquad\forall a_i,b_i,c_i\in A\] 처음 몇 개의 항등식은 다음과 같다. 여기서 \(m_1=\delta\), \(m_2=\cdot\)으로 쓰자.

  - (공경계의 멱영성) \(\delta^2=0\)
  - ([곱 규칙](../Page/곱_규칙.md "wikilink")) \(\delta(ab)=(\delta a)b+a(\delta b)\)
  - (호모토피 [결합 법칙](https://ko.wikipedia.org/wiki/결합_법칙 "wikilink")) \(a(bc)-(ab)c=\delta m_3(a,b,c)+m_3(\delta a,b,c)+m_3(a,\delta b,c)+m_3(a,b,\delta c)\)
  - \(m_3(ab,c,d)-m_3(a,bc,d)+m_3(a,b,cd)-m_3(a,b,c)d-am_3(b,c,d)=-\delta m_4(a,b,c,d)+m_4(\delta a,b,c,d)+m_4(a,\delta b,c,d)+m_4(a,b,\delta c,d)+m_4(a,b,c,\delta d)\)
  - \(\vdots\)

따라서, \((A,\delta)\)는 [공사슬 복합체를](https://ko.wikipedia.org/wiki/공사슬_복합체 "wikilink") 이룬다.

두 A<sub>∞</sub>-대수 \(A\), \(B\) 사이의 **사상**은 다음과 같은 데이터로 주어진다.

  - 각 \(n\ge1\)에 대하여, 차수 \(1-n\)인 겹선형 사상 \(f_n\colon A^{\otimes n}\to B\)

이는 다음 조건을 만족시켜야 한다. 모든 \(n\ge1\)에 대하여,

\[\sum_{r+s+t=n}(-1)^{r+st}f_{r+1+t}(a_1,\dots,a_r,m_s(a_{r+1},\dots,a_{r+s}),a_{r+s+1},\dots,a_n)=\sum_{k=1}^n\sum_{i_1+\cdots+i_k=n}(-1)^{\sum_{\ell=1}^k(k-\ell)(i_\ell-1)}m_r(f_{i_1}(a_1,\dots,a_{i_1},f_2(\dots),\dots,f_{i_k}(\dots,a_n))\] 구체적으로, 처음 몇 \(n\)에 대하여 이 조건은 다음과 같다.

\[f_1\circ\delta=\delta\circ f_1\]

\[f_1(a\cdot b)=f_1(a)\cdot f_1(b)+\delta f_2(a,b)+f_2(\delta a,b)+f_2(a,\delta b)\]

\[\vdots\]

A<sub>∞</sub>-대수 \(A\)의 [코호몰로지](https://ko.wikipedia.org/wiki/코호몰로지 "wikilink") \(H^\bullet(A)\)를 취하자. 그렇다면, \(H^\bullet(A)\) 위에도 자연스러운 A<sub>∞</sub>-대수의 구조가 존재하며, 이 경우 \(m_1=0\)이 된다.

## 예

**결합 오퍼라드**는 \(A(n)=\operatorname{Sym}(n)\)인 오퍼라드이다. 즉, 결합 법칙이 (호모토피를 무시하지 않아도) 정확하게 성립하는 대수를 나타낸다.

**작은 구간 오퍼라드**()의 경우, \(A(n)\)은 단위 구간 \((0,1)\) 속에 존재하는 \(n\)개의 서로소 열린 구간들의 공간이다.

## 참고 문헌

  -   -
  -
  -
## 외부 링크

  -
  -
[분류:호모토피 이론](https://ko.wikipedia.org/wiki/분류:호모토피_이론 "wikilink") [분류:대수](https://ko.wikipedia.org/wiki/분류:대수 "wikilink") [분류:대수적 위상수학](https://ko.wikipedia.org/wiki/분류:대수적_위상수학 "wikilink")