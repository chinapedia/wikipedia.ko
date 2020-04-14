> This article is converted from Wikipedia: [Tor 함자](https://ko.wikipedia.org/wiki/Tor_함자).


[호몰로지 대수학에서](../Page/호몰로지_대수학.md "wikilink"), **Tor 함자**(Tor函子, )는 [가군](../Page/가군.md "wikilink") [텐서곱](../Page/텐서곱.md "wikilink") [함자의](../Page/함자_\(수학\).md "wikilink") [유도 함자다](../Page/유도_함자.md "wikilink").

## 정의

\(R\)이 (단위원을 가진) [환이고](../Page/환_\(수학\).md "wikilink"), \(_R{}\operatorname{Mod}\)이 \(R\)에 대한 [왼쪽 가군들의](../Page/가군.md "wikilink") [범주](../Page/범주_\(수학\).md "wikilink"), \(\operatorname{Mod}_R\)이 \(R\)에 대한 [오른쪽 가군들의](../Page/가군.md "wikilink") 범주라고 하자. 이 범주들은 [아벨 범주를](../Page/아벨_범주.md "wikilink") 이룬다.

오른쪽 가군 \(A\in\operatorname{Mod}_R\)와 왼쪽 가군 \(B\in{}_R\operatorname{Mod}\)의 [텐서곱](../Page/텐서곱.md "wikilink")을 취하여 [아벨 군](../Page/아벨_군.md "wikilink") \(A\otimes_RB\in\operatorname{Ab}\)를 취할 수 있다. 이 텐서곱 연산 \(\otimes_R\colon\operatorname{Mod}_R\times{}_R\operatorname{Mod}\to\operatorname{Ab}\)는 [쌍함자](../Page/함자_\(수학\).md "wikilink")(bifunctor)를 이룬다. 여기서 \(\operatorname{Ab}\)는 [아벨 군들의](../Page/아벨_군.md "wikilink") [범주다](../Page/범주_\(수학\).md "wikilink").

\(A\otimes_R\colon{}_R\operatorname{Mod}\to\operatorname{Ab}\)는 [오른쪽 완전 함자이며](https://ko.wikipedia.org/wiki/오른쪽_완전_함자 "wikilink"), 따라서 그 [왼쪽 유도 함자](https://ko.wikipedia.org/wiki/왼쪽_유도_함자 "wikilink") \(L^i(A\otimes)\)를 취할 수 있다. 마찬가지로, \(\otimes_RB\colon\operatorname{Mod}_R\to\operatorname{Ab}\) 또한 [오른쪽 완전 함자이며](https://ko.wikipedia.org/wiki/오른쪽_완전_함자 "wikilink"), 따라서 [왼쪽 유도 함자](https://ko.wikipedia.org/wiki/왼쪽_유도_함자 "wikilink") \(L^i(\otimes_RB)\)를 취할 수 있다. 이 둘은 사실 같은 쌍함자를 이룬다. 즉,

\[L^i(A\otimes_R)B=A(L^i\otimes_RB)=\operatorname{Tor}^R_i(A,B)\] 이다. 이 쌍함자 \(\operatorname{Tor}^R_i\colon\operatorname{Mod}_R\times{}_R\operatorname{Mod}\to\operatorname{Ab}\)를 **Tor 함자**라고 한다.

## 성질

Tor 함자는 [직합](../Page/직합.md "wikilink")을 보존한다. 즉,

\[\operatorname{Tor}_n^R\left(\bigoplus_{i\in I}M_i,\bigoplus_{j\in J}N_j\right)=\bigoplus_{i\in I}\bigoplus_{j\in J}\operatorname{Tor}_n^R(M_i,N_j)\] 이다.

만약 \(R\)가 [가환환](../Page/가환환.md "wikilink")인 경우, 다음과 같은 표준적인 동형이 존재한다.

\[\operatorname{Tor}_n^R(M,N)\cong\operatorname{Tor}_n^R(M,N)\] 또한, 이 경우 \(\operatorname{Tor}_n^R(M,N)\)은 \(R\) 위의 [가군](../Page/가군.md "wikilink")의 구조를 갖는다.

만약 \(R\)가 가환환이며, \(r\in R\)가 [영인자](../Page/영인자.md "wikilink")가 아닐 때, 다음이 성립한다.

\[\operatorname{Tor}_1^R(R/(r),M)=\ker(r\cdot)=\{m\in M\colon rm=0\}\]

## 예

### 벡터 공간

체 \(K\) 위의 [가군](../Page/가군.md "wikilink")의 범주에서의 Tor 함자를 생각해 보자. 체 위의 가군은 [벡터 공간이며](../Page/벡터_공간.md "wikilink"), 모든 벡터 공간은 [사영 가군이다](../Page/사영_가군.md "wikilink"). 즉, 벡터 공간 \(V\)의 사영 분해는 자명하다.

\[0\to P_0=V\to V\to0\] 따라서, \(K\) 위의 벡터 공간 \(V\), \(W\)가 주어졌을 때, Tor 함자는 다음과 같다.

\[\operatorname{Tor}_0^K(V,W)=V\otimes_KW\]

\[\operatorname{Tor}_n^K(V,W)=0\qquad\forall n>0\]

### 아벨 군

[정수환](https://ko.wikipedia.org/wiki/정수환 "wikilink") \(\mathbb Z\) 위의 가군의 범주에서의 Tor 함자를 생각해 보자. 정수환 위의 가군은 [아벨 군이며](../Page/아벨_군.md "wikilink"), [사영 가군은](../Page/사영_가군.md "wikilink") [자유 아벨 군이다](../Page/자유_아벨_군.md "wikilink"). 모든 아벨 군은 길이가 1 이하인 사영 분해를 갖는다. 즉, 임의의 아벨 군 \(G\)는 [자유 아벨 군](../Page/자유_아벨_군.md "wikilink") \(P_0\)의 [몫군](https://ko.wikipedia.org/wiki/몫군 "wikilink") \(P_0/P_1\)으로 나타낼 수 있으며, [자유 아벨 군의](../Page/자유_아벨_군.md "wikilink") 모든 [부분군](../Page/부분군.md "wikilink")은 자유 아벨 군이므로 다음은 사영 분해이다.

\[0\to G\to P^0\to P^1\to0\]

[아벨 군](../Page/아벨_군.md "wikilink") \(G\), \(H\)가 주어졌을 때, Tor 함자는 다음과 같다. \(G\)의 사영 분해가

\[0\to P^1\xrightarrow{\iota}P_0\to G\to0\] 이라면, Tor 함자는 다음 [사슬 복합체의](../Page/사슬_복합체.md "wikilink") [호몰로지 군이다](https://ko.wikipedia.org/wiki/호몰로지_군 "wikilink").

\[0\to P_1\otimes_{\mathbb Z} H \xrightarrow{\iota\otimes_{\mathbb Z}\operatorname{id}} P_0\otimes_{\mathbb Z}H\to0\] 따라서,

\[\operatorname{Tor}_0^{\mathbb Z}(G,H)\cong G\otimes_{\mathbb Z}H\] 이며,

\[\operatorname{Tor}_1^{\mathbb Z}(G,H)\cong\ker(\iota\otimes_{\mathbb Z}\operatorname{id})\] 이다. 특히,

\[\operatorname{Tor}_1^{\mathbb Z}(\mathbb Z,H)=0\]

\[\operatorname{Tor}_1^{\mathbb Z}(0,H)=H\]

\[\operatorname{Tor}_1^{\mathbb Z}(\mathbb Z/(n),H)=\operatorname{Tors}_n(H)=\{h\in H\colon nh=0\}\] 이다. 보다 일반적으로, Tor 함자는 [직합](../Page/직합.md "wikilink")을 보존하므로,

\[\operatorname{Tor}_1^{\mathbb Z}\left(\bigoplus_i\mathbb Z/(n_i),H\right)=\bigoplus_i\operatorname{Tors}_{n_i}(H)\] 가 된다. 또한,

\[\operatorname{Tor}_1^{\mathbb Z}(\mathbb Q/\mathbb Z,H)=\operatorname{Tors}(H)=\{h\in H\colon\exists n\in\mathbb Z^+\colon nh=0\}\] 이므로 \(H\)의 [꼬임 부분군이](https://ko.wikipedia.org/wiki/꼬임_부분군 "wikilink") 된다.

| \(G\backslash H\) | \(\mathbb Z\)     | \(\mathbb Z/(n)\)           | \(\mathbb Q\) |
| ----------------- | ----------------- | --------------------------- | ------------- |
| \(\mathbb Z\)     | \(\mathbb Z\)     | \(\mathbb Z/(n)\)           | \(\mathbb Q\) |
| \(\mathbb Z/(m)\) | \(\mathbb Z/(m)\) | \(\mathbb Z/(\gcd\{m,n\})\) | 0             |
| \(\mathbb Q\)     | \(\mathbb Q\)     | 0                           | \(\mathbb Q\) |

\(\operatorname{Tor}_0^{\mathbb Z}(G,H)=G\otimes H\)

| \(G\backslash H\) | \(\mathbb Z\) | \(\mathbb Z/(n)\)           | \(\mathbb Q\) |
| ----------------- | ------------- | --------------------------- | ------------- |
| \(\mathbb Z\)     | 0             | 0                           | 0             |
| \(\mathbb Z/(m)\) | 0             | \(\mathbb Z/(\gcd\{m,n\})\) | 0             |
| \(\mathbb Q\)     | 0             | 0                           | 0             |

\(\operatorname{Tor}_1^{\mathbb Z}(G,H)\)

### 리 대수 호몰로지

[리 대수 호몰로지는](https://ko.wikipedia.org/wiki/리_대수_호몰로지 "wikilink") [리 대수의](../Page/리_대수.md "wikilink") [보편 포락 대수의](../Page/보편_포락_대수.md "wikilink") Tor 함자와 같다.

## 어원

‘Tor’는 ([꼬임 부분군](https://ko.wikipedia.org/wiki/꼬임_부분군 "wikilink"))의 약자다. 이는 Tor 함자가 [아벨 군의](../Page/아벨_군.md "wikilink") [꼬임 부분군과](https://ko.wikipedia.org/wiki/꼬임_부분군 "wikilink") 관련있기 때문이다.

## 같이 보기

  - [Ext 함자](../Page/Ext_함자.md "wikilink")
  - [그로텐디크 군](../Page/그로텐디크_군.md "wikilink")

## 참고 문헌

  -
  -
## 외부 링크

  -
  -
[분류:호몰로지 대수학](https://ko.wikipedia.org/wiki/분류:호몰로지_대수학 "wikilink") [분류:이항연산](https://ko.wikipedia.org/wiki/분류:이항연산 "wikilink")