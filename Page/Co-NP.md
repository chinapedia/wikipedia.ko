> This article is converted from Wikipedia: [Co-NP](https://ko.wikipedia.org/wiki/Co-NP).


[계산 복잡도 이론에서](https://ko.wikipedia.org/wiki/계산_복잡도_이론 "wikilink") **co-NP**는 [복잡도 종류이다](https://ko.wikipedia.org/wiki/복잡도_종류 "wikilink"). 문제 \(\mathcal{X}\)가 **co-NP**에 들어 있다는 것은 그 [보완](https://ko.wikipedia.org/wiki/보완_\(복잡도\) "wikilink") 문제인 \(\overline{\mathcal{X}}\)가 **[NP](https://ko.wikipedia.org/wiki/NP_\(복잡도\) "wikilink")**에 속한다는 것과 동치이다. 간단히 말하면, **co-NP**는 *아니오* 보기(*반례*라고도 한다)에 대해 효율적으로 검증할 수 있는 증명이 있는 문제의 집합이다.

NP-완전 문제 중 [부분집합 합 문제가](https://ko.wikipedia.org/wiki/부분집합_합_문제 "wikilink") 있다. 이 문제는 정수 유한집합이 있을 때, 이 집합의 공집합이 아닌 부분집합 중 원소를 다 더하면 0이 되는 것이 있는지를 묻는 문제이다. 이 문제의 보완 문제는 co-NP에 들어가는데, 정수 유한집합이 주어질 때, 공집합이 아닌 부분집합은 모두, 원소를 다 더했을 때 0이 아닌지를 묻는 문제가 된다. "아니오" 보기에 대한 증명을 하려면, 합이 0이 되고 공집합이 아닌 부분집합을 찾아야 한다. 그렇게 하면 이 증명은 검증하기 쉬워진다.

다항 시간에 풀 수 있는 문제인 **P**는 **NP**와 **co-NP** 모두의 부분집합이다. **P**는 두 경우 모두 진부분집합일 것으로 추측하고 있다. (한쪽만 진부분집합이고, 다른 쪽은 아닌 경우는 불가능함을 보일 수 있다.) **NP**와 **co-NP** 역시, 같은 집합이 아닐 것이다. 만약 그렇지 않다면, **[NP-완전](https://ko.wikipedia.org/wiki/NP-완전 "wikilink")** 문제가 **co-NP**에 들어갈 수 있고, **[co-NP-완전](https://ko.wikipedia.org/wiki/co-NP-완전 "wikilink")** 문제가 **NP**에 들어갈 수 있기 때문이다.

이는 다음과 같이 보일 수 있다. **co-NP**에 들어가는 **NP-완전** 문제가 있다고 하자. 모든 **NP** 문제는 이 문제로 환산할 수 있기 때문에, 각 **NP**문제에 대해서 그 보완 문제를 다항 시간에 판정할 수 있는 비결정적인 튜링 기계를 만들 수 있다. 다시 말해서, **NP**가 **co-NP**의 부분집합이 된다. 따라서 **NP** 문제의 보완을 모은 집합이 **co-NP** 문제의 보완을 모은 집합의 부분집합이 된다. 곧, **co-NP**가 **NP**의 부분집합이 된다. 앞에서 **NP**가 **co-NP**의 부분집합임을 보였으므로, 이는 두 집합이 같다는 뜻이 된다. **co-NP-완전** 문제가 **NP**일 수 없음을 보이는 증명은 이 증명과 대칭을 이룬다.

어떤 문제가 **NP**와 **co-NP** 둘 다 된다는 것을 보였다면, 이는 그 문제가 **NP-완전**이 아닐 것이라는 강력한 증거가 된다. (**NP-완전**이라면 **NP** = **co-NP**이기 때문)

정수의 [소인수 분해](https://ko.wikipedia.org/wiki/소인수_분해 "wikilink") 문제는 **NP**와 **co-NP**에 모두 들어가는, 유명한 문제이다. 양의 정수 *m*과 *n*이 있을 때 *m*에 *n*보다 작고 1보다 큰 약수가 있는지를 묻는다. 있는 경우를 보이는 쪽은 쉽다. *m*에 그런 약수가 있다면, 그 약수로 나누어 보면 된다. 반대쪽은 좀 어려운데, 그런 약수가 없다는 것을 보이려면 일일이 나누어 보아야 한다.

[소인수 분해](https://ko.wikipedia.org/wiki/소인수_분해 "wikilink") 문제를 [소수](https://ko.wikipedia.org/wiki/소수_\(수론\) "wikilink") 문제와 헷갈리는 사람이 많다. 소수 문제도 소인수 분해 문제처럼 **NP**와 **co-NP** 둘 다에 들어간다. 그러나 아직 확실치 않은 소인수 분해와는 달리, 소수 문제는 **P**이다.\[1\]

## 외부 링크

  - [복잡도 동물원 co-NP 우리](https://web.archive.org/web/20061128071923/http://qwiki.caltech.edu/wiki/Complexity_Zoo#conp)

## 참고 문헌

<references />

[분류:복잡도 종류](https://ko.wikipedia.org/wiki/분류:복잡도_종류 "wikilink")

1.   [소수 문제가 P임을 밝힌 논문](http://www.math.princeton.edu/~annals/issues/2004/Sept2004/Agrawal.pdf)