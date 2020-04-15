> This article is converted from Wikipedia: [스튜던트 t 분포](https://ko.wikipedia.org/wiki/스튜던트_t_분포).


{\\Gamma(\\nu/2)2^{\\nu/2-1}},\\;\\nu\>0</math>, \(K_{\nu}(x)\)는 [베셀 함수](../Page/베셀_함수.md "wikilink") }} **스튜던트 t 분포**(Student t分布, )는 [정규 분포의](../Page/정규_분포.md "wikilink") 평균을 측정할 때 주로 사용되는 분포이다.

## 정의

**스튜던트 t 분포**는 다음 [확률변수](https://ko.wikipedia.org/wiki/확률변수 "wikilink")의 분포로 정의된다.

\[\frac{Z}{\sqrt{V/\nu}}\] 여기에서 \(Z\)는 [표준정규분포](https://ko.wikipedia.org/wiki/표준정규분포 "wikilink"), \(V\)는 [카이제곱 분포](../Page/카이제곱_분포.md "wikilink") \(\nu\)인 [자유도](https://ko.wikipedia.org/wiki/자유도 "wikilink")이다.

t 분포는 종모양으로서 t=0에서 좌우대칭을 이룬다. t 분포의 모양을 결정하는 것은 자유도이며, 자유도가 커질수록 [표준정규분포](https://ko.wikipedia.org/wiki/표준정규분포 "wikilink")에 가깝게 된다.\[1\]

## 정규분포에서의 추정

어떤 정규분포의 [평균](../Page/평균.md "wikilink")이 \(\mu\)이고 [분산](../Page/분산.md "wikilink")이 \(\sigma^2\)일 때, 그 분포에서 n개의 표본을 추출한 것을 \(X_1, \cdots, X_n\)라고 표기한다. 표본평균과 표본분산은 다음과 같다.

\[\overline{X} = \frac{1}{n}(X_1+\cdots+X_n)\]

\[S^{\;2} = \frac{1}{n-1}\sum_{i=1}^n\left(X_i-\overline{X}\right)^2\] 이 값들은 실제 평균과 분산에 대한 [불편추정값](https://ko.wikipedia.org/wiki/불편추정값 "wikilink")이다. 이때,

\[V = (n-1)\frac{S^2}{\sigma^2}\] 은 자유도가 \(n-1\)인 [카이제곱 분포가](../Page/카이제곱_분포.md "wikilink") 된다는 것이 Cochran 정리에 의해 알려져 있다. 또한

\[Z = \left(\overline{X}-\mu\right)\frac{\sqrt{n}}{\sigma}\] 는 평균이 0이고 분산이 1인 정규분포를 가지며, \(V, Z\)는 서로 독립이라는 것을 증명할 수 있다.

이때 \(Z\)에서 \(\sigma^2\) 대신 \(S^{\;2}\)로 대체한 추축량(pivot quantity)은 다음과 같다.

\[T \equiv \frac{Z}{\sqrt{V/\nu}} = \left(\overline{X}-\mu\right)\frac{\sqrt{n}}{S}\] 이때 \(T\)에는 \(\sigma^2\)가 사용되지 않으므로, 이 분포는 분산을 모를 때의 평균값 \(\mu\)를 추정하는 데에 사용이 가능하다. 이때 \(T\)의 분포는 자유도 n-1인 t-분포가 된다.

### 구간 추정

자유도 n-1인 t 분포 \(T\)에 대해,

\[\Pr(-A<T<A) = 0.9\] 을 만족하는 실수 \(A\)는 수치적으로 계산이 가능하다. 이때,

\[\Pr(-A<T<A) = \Pr\left(-A < {\overline{X} - \mu \over S/\sqrt{n}} < A \right) =  \Pr\left(\overline{X}_n - A{S \over \sqrt{n}} < \mu < \overline{X} + A{S \over \sqrt{n}}\right) = 0.9\] 이므로, [정규분포](https://ko.wikipedia.org/wiki/정규분포 "wikilink")의 평균은 90%의 신뢰도로 \(\overline{X}\pm A\frac{S}{\sqrt{n}}\) [신뢰구간](https://ko.wikipedia.org/wiki/신뢰구간 "wikilink")에 속하게 된다.

## 역사

프리드리히 로베르트 헬메르트()가 1875년에 도입하였다.\[2\]\[3\]\[4\]\[5\] 이듬해 [야코프 뤼로트](https://ko.wikipedia.org/wiki/야코프_뤼로트 "wikilink")()도 같은 분포를 재발견하였다.\[6\]\[7\] 그러나 헬메르트와 뤼로트의 논문은 영문 학계에 널리 알려지지 않았다.

1908년에 [윌리엄 고셋이](https://ko.wikipedia.org/wiki/윌리엄_고셋 "wikilink") "스튜던트"(, ‘학생’)라는 [필명](https://ko.wikipedia.org/wiki/필명 "wikilink")으로 1908년 재발견하였다.\[8\] 고셋은 [기네스 양조 공장에서](https://ko.wikipedia.org/wiki/기네스_\(맥주\) "wikilink") 일했고, 맥주에 사용되는 보리의 질을 시험하기 위해 이 분포를 도입하였고, 경쟁사들에게 기네스의 획기적인 통계 기법을 숨기기 위해 필명을 사용하였다고 한다.\[9\] 이후 저명한 통계학자인 [로널드 피셔는](../Page/로널드_피셔.md "wikilink") 이 분포를 "스튜던트 분포"라고 불렀고, *t*라는 기호를 사용하였다.\[10\] 피셔 이후 이 분포는 고셋의 필명을 따 "스튜던트 t 분포"로 알려지게 되었다.

## 참고 문헌

## 같이 보기

  - [카이제곱 분포](../Page/카이제곱_분포.md "wikilink")
  - [F 분포](../Page/F_분포.md "wikilink")
  - [정규분포](https://ko.wikipedia.org/wiki/정규분포 "wikilink")
  - [t-test](https://ko.wikipedia.org/wiki/t-test "wikilink")

[분류:연속분포](https://ko.wikipedia.org/wiki/분류:연속분포 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.