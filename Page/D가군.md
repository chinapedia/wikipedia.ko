> This article is converted from Wikipedia: [D](https://ko.wikipedia.org/wiki/D).


[수학](https://ko.wikipedia.org/wiki/수학 "wikilink")에서, **D가군**()은 [미분 연산자들의](https://ko.wikipedia.org/wiki/미분_연산자 "wikilink") 환에 대한 [가군층](../Page/가군층.md "wikilink")이다. 선형 [편미분 방정식의](https://ko.wikipedia.org/wiki/편미분_방정식 "wikilink") 추상화이며, 또한 평탄한 [코쥘 접속을](https://ko.wikipedia.org/wiki/코쥘_접속 "wikilink") 갖춘 [벡터 다발의](https://ko.wikipedia.org/wiki/벡터_다발 "wikilink") 일반화이다.

## 정의

\(X\)가 [표수 0인](https://ko.wikipedia.org/wiki/체의_표수 "wikilink") [체](https://ko.wikipedia.org/wiki/체_\(수학\) "wikilink") \(k\)에 대한 [비특이 대수다양체라고](https://ko.wikipedia.org/wiki/비특이_대수다양체 "wikilink") 하고, \(X\) 위의 정칙함수들의 [층을](https://ko.wikipedia.org/wiki/층_\(수학\) "wikilink") \(\mathcal O_X\)라고 하자. 또한, \(X\) 위의 (대수적) 벡터장들로 생성되는 \(\mathcal O_X\)-[가군층](../Page/가군층.md "wikilink") \(\mathcal D_X\)를 생각하자. 이는 미분 연산자들로 간주할 수 있다.

\(X\) 위의 **D가군** \((\mathcal M,\nabla)\)은 다음과 같은 데이터로 이루어져 있다.

  - \(\mathcal O_X\)-[가군층](../Page/가군층.md "wikilink") \(\mathcal M\)
  - \(k\)-[선형사상](https://ko.wikipedia.org/wiki/선형사상 "wikilink") \(\nabla\colon\mathcal D_X\to\operatorname{End}(M)\), \(v\mapsto\nabla_v\)

이는 다음과 같은 공리를 만족시켜야 한다. 모든 \(\mathcal O_X\)의 단면 \(f\), \(\mathcal M\)의 단면 \(m\), \(X\) 위의 [벡터장](https://ko.wikipedia.org/wiki/벡터장 "wikilink") \(u,v\)에 대하여,

  - (\(\mathcal O_X\)-선형성) \(\nabla_{fv}m=f(\nabla_vm)\)
  - ([곱의 법칙](https://ko.wikipedia.org/wiki/곱의_법칙_\(미적분학\) "wikilink")) \(\nabla_v(fm)=(\nabla_vf)m+f\nabla_vm\)
  - ([리 괄호에](https://ko.wikipedia.org/wiki/리_괄호 "wikilink") 대한 [준동형](https://ko.wikipedia.org/wiki/준동형 "wikilink")) \(\nabla_{[u,v]}=[\nabla_v,\nabla_v]\)

## 예

[국소 자유 가군층은](https://ko.wikipedia.org/wiki/국소_자유_가군층 "wikilink") [벡터 다발로](https://ko.wikipedia.org/wiki/벡터_다발 "wikilink") 여길 수 있으며, [국소 자유 가군층인](https://ko.wikipedia.org/wiki/국소_자유_가군층 "wikilink") D가군은 단순히 평탄한 [코쥘 접속이](https://ko.wikipedia.org/wiki/코쥘_접속 "wikilink") 주어진 [벡터 다발이다](https://ko.wikipedia.org/wiki/벡터_다발 "wikilink").

\(\mathcal D_X\) 자체는 자명하게 D가군을 이룬다.

복소 [아핀 공간](https://ko.wikipedia.org/wiki/아핀_공간 "wikilink") \(\mathbb C^n\) 위의 함수 공간 \(F\)가 다음 성질들을 만족시킨다면, \(F\)는 D가군을 이룬다.

  - \(F\)는 덧셈 및 곱셈에 대하여 닫혀 있다.
  - \(\mathbb C[x_1,\dots,x_n]\subset F\). 즉, \(F\)는 모든 다항함수를 포함한다.
  - \(F\)는 미분에 대하여 닫혀 있다.

### 선형 편미분 방정식에 대응하는 D가군

\(\mathbb C^n=\{(z_1,\dots,z_n)\}\) 위의 선형 미분 연산자

\[D=\sum_{\alpha,\beta\in\mathbb N^n}C_{\alpha,\beta}z^\alpha\partial_\beta\] 로 정의되는 선형 [편미분 방정식](https://ko.wikipedia.org/wiki/편미분_방정식 "wikilink")

\[Df=0\] 을 생각해 보자. 그렇다면, 이 편미분 방정식에 대응되는 D가군은 \(D\)로 생성되는 \(\mathcal D_{\mathbb C^n}\)의 [아이디얼](https://ko.wikipedia.org/wiki/아이디얼 "wikilink") \((D)\)에 대한 [몫환](https://ko.wikipedia.org/wiki/몫환 "wikilink")

\[\mathcal D_{\mathbb C^n}/(D)\] 이다. 이 경우, D가군을 이루는 어떤 함수 공간 \(F\) 속에서,

\[Df=0\qquad(f\in F)\] 의 해들의 공간은

\[\hom_{\mathcal D_{\mathbb C^n}}(\mathcal D_{\mathbb C^n}/(D),F)\] 과 같다.

## 외부 링크

  -
  -
[분류:층론](https://ko.wikipedia.org/wiki/분류:층론 "wikilink") [분류:편미분방정식](https://ko.wikipedia.org/wiki/분류:편미분방정식 "wikilink")