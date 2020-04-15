> This article is converted from Wikipedia: [바이어슈트라스 M-판정법](https://ko.wikipedia.org/wiki/바이어슈트라스_M-판정법).


**바이어슈트라스 M-판정법**()은 [함수항급수](https://ko.wikipedia.org/wiki/함수항급수 "wikilink")의 [절대균등수렴](https://ko.wikipedia.org/wiki/절대균등수렴 "wikilink") 여부에 대한 판정법이다. [멱급수](../Page/멱급수.md "wikilink")를 다룰 때 유용하다.\[1\]

[카를 바이어슈트라스의](../Page/카를_바이어슈트라스.md "wikilink") 이름이 붙어 있다.

## 내용

\(f_n(x)\)를 집합 \(D\)에 정의된, 실수 또는 복소수 값 함수의 열이라고 하자. 만약 어떤 양항수열 \(M_n\)이 존재하여,

  - 임의의 자연수 \(n\)과 임의의 \(x \in D\)에 대해, \(|f_n(x)| \le M_n\)이고,
  - \(\sum_{n=1}^{\infty} M_n\)이 수렴하면,

급수 \(\sum_{n=1}^{\infty} f_n(x)\)는 \(D\)에서 절대균등수렴한다. (즉, 항별로 절댓값을 취한 급수가 균등수렴한다. 이는 동시에 절대수렴과 균등수렴인 것보다 강한 조건임에 주의해야 한다.)

바이어슈트라스 M-판정법은, 함수해석학적으로는 [균등 노름의](https://ko.wikipedia.org/wiki/균등_노름 "wikilink") 급수가 수렴하면, 함수의 급수가 절대균등수렴한다고 서술된다. 또한, 임의의 [바나흐 공간을](../Page/바나흐_공간.md "wikilink") 공역으로 하는 함수들의 급수에게도 적용된다.

## 증명

\(\sum_{n=1}^{\infty} M_n\)이 수렴하므로, 임의의 \(\epsilon > 0\)에 대해, 어떤 자연수 \(N\)이 존재하여, 임의의 \(n,m \ge N\)에 대해,

\[\sum_{k=m}^n M_k \le \epsilon\]

그러므로,

\[\left|\sum_{k=m}^n |f_k(x)|\right| \le \sum_{k=m}^n M_k \le \epsilon\]

따라서 균등수렴에 대한 코시 판정법에 의해, \(\sum_{n=1}^{\infty} f_n(x)\)는 \(D\)에서 절대균등수렴한다.

## 예

실함수항급수 \(\sum_{n=1}^{\infty} x^2e^{-nx}\)의 각 항은,

\[(x^2e^{-nx})' = xe^{-nx}(2 - nx)\]

임에 따라,

\[x^2e^{-nx} \le \left(\frac{2}{n}\right)^2e^{-2},\ \forall x \in [0, \infty)\]

이다. 조화급수 \(\sum_{n=1}^{\infty} \frac{1}{n^2}\)이 수렴하므로, \(\sum_{n=1}^{\infty} x^2e^{-nx}\)은 \([0, \infty)\)에서 균등수렴한다.

## 각주

## 참고 문헌

  - : 148.

[분류:수렴판정법](https://ko.wikipedia.org/wiki/분류:수렴판정법 "wikilink") [분류:함수해석학](https://ko.wikipedia.org/wiki/분류:함수해석학 "wikilink")

1.