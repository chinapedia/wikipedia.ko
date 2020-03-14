> This article is converted from Wikipedia: [Fpqc ](https://ko.wikipedia.org/wiki/Fpqc_).


[층](https://ko.wikipedia.org/wiki/층_\(수학\) "wikilink") 이론에서, **fpqc 위상**(fpqc位相, )은 [스킴의](https://ko.wikipedia.org/wiki/스킴_\(수학\) "wikilink") [범주](https://ko.wikipedia.org/wiki/범주_\(수학\) "wikilink") 위에 정의되는 매우 섬세한 [그로텐디크 위상이다](https://ko.wikipedia.org/wiki/그로텐디크_위상 "wikilink"). 이러한 섬세함에도 불구하고, fpqc 위상에서 다양한 [내림 이론을](../Page/내림_데이터.md "wikilink") 전개할 수 있다.

## 정의

### fpqc 위상

**fpqc 사상**()은 다음 조건들을 만족시키는 [스킴 사상](https://ko.wikipedia.org/wiki/스킴_사상 "wikilink") \(f\colon X\to Y\)이다.\[1\]

  - [전사 함수이다](https://ko.wikipedia.org/wiki/전사_함수 "wikilink").
  - [평탄 사상이다](https://ko.wikipedia.org/wiki/평탄_사상 "wikilink").
  - \(Y\)의 모든 [콤팩트](https://ko.wikipedia.org/wiki/콤팩트_공간 "wikilink") [열린집합](https://ko.wikipedia.org/wiki/열린집합 "wikilink") \(K_Y\subseteq Y\)에 대하여, \(f(K_X)=K_Y\)가 되는 [콤팩트](https://ko.wikipedia.org/wiki/콤팩트_공간 "wikilink") [열린집합](https://ko.wikipedia.org/wiki/열린집합 "wikilink") \(K_X\subseteq X\)가 존재한다. (여기서 [콤팩트 공간의](https://ko.wikipedia.org/wiki/콤팩트_공간 "wikilink") 정의는 [하우스도르프 조건을](https://ko.wikipedia.org/wiki/하우스도르프_공간 "wikilink") 포함하지 않는다.)

[스킴의](https://ko.wikipedia.org/wiki/스킴_\(수학\) "wikilink") [범주](https://ko.wikipedia.org/wiki/범주_\(수학\) "wikilink") \(\operatorname{Sch}\)는 모든 [쌍대곱](https://ko.wikipedia.org/wiki/쌍대곱 "wikilink")을 가지며, [집합](https://ko.wikipedia.org/wiki/집합 "wikilink")으로서 이는 [분리합집합](https://ko.wikipedia.org/wiki/분리합집합 "wikilink")이다. (그러나 [밂은](../Page/밂_\(범주론\).md "wikilink") 일반적으로 존재하지 않는다.) 같은 [공역을](https://ko.wikipedia.org/wiki/공역_\(수학\) "wikilink") 갖는 스킴 사상들의 집합 \(\{f_i\colon U_i\to U\}_{i\in I}\)에 대하여, 만약 [보편 성질에](../Page/보편_성질.md "wikilink") 의하여 존재하는 사상

\[f=\bigsqcup_{i\in I}f_i\colon\bigsqcup_{i\in I}U_i\to U\] 이 fpqc 사상이라면, \(\{f_i\}_{i\in I}\)를 **fpqc 덮개**라고 한다. fpqc 덮개들은 \(\operatorname{Sch}\) 위의 [그로텐디크 준위상을](https://ko.wikipedia.org/wiki/그로텐디크_준위상 "wikilink") 이루며, 이로부터 유도되는 [그로텐디크 위상을](https://ko.wikipedia.org/wiki/그로텐디크_위상 "wikilink") **fpqc 위상**()이라고 한다.

### fppf 위상

같은 [공역을](https://ko.wikipedia.org/wiki/공역_\(수학\) "wikilink") 갖는 [스킴 사상들의](https://ko.wikipedia.org/wiki/스킴_사상 "wikilink") 집합 \(\{f_i\colon U_i\to U\}_{i\in I}\)에 대하여, [보편 성질에](../Page/보편_성질.md "wikilink") 의하여 존재하는 사상

\[f=\bigsqcup_{i\in I}f_i\colon\bigsqcup_{i\in I}U_i\to U\] 을 생각하자. 만약

  - \(f_i\)가 각각 [국소 유한 표시 사상이자](https://ko.wikipedia.org/wiki/국소_유한_표시_사상 "wikilink") [평탄 사상이며](https://ko.wikipedia.org/wiki/평탄_사상 "wikilink")
  - \(f\)가 [전사 함수라면](https://ko.wikipedia.org/wiki/전사_함수 "wikilink")

\(\{f_i\}_{i\in I}\)를 **fppf 덮개**라고 한다.\[2\] fppf 덮개들은 \(\operatorname{Sch}\) 위의 [그로텐디크 준위상을](https://ko.wikipedia.org/wiki/그로텐디크_준위상 "wikilink") 이루며, 이로부터 유도되는 [그로텐디크 위상을](https://ko.wikipedia.org/wiki/그로텐디크_위상 "wikilink") **fppf 위상**()이라고 한다.

## 성질

### 위상의 비교

모든 fppf 덮개는 fpqc 덮개이다. 따라서, fpqc 위상은 fppf 위상보다 더 섬세하다. 마찬가지로, fppf 위상은 [에탈 위상보다](https://ko.wikipedia.org/wiki/에탈_위상 "wikilink") 더 섬세하다. fpqc 위상에서 모든 [표현 가능 준층이](https://ko.wikipedia.org/wiki/표현_가능_준층 "wikilink") [층을](https://ko.wikipedia.org/wiki/층_\(수학\) "wikilink") 이루므로, fpqc 위상은 [표준 위상보다는](https://ko.wikipedia.org/wiki/표준_위상 "wikilink") 더 엉성하다.

fpqc 위상을 스킴의 범주 위에 흔히 사용되는 위상 가운데 가장 섬세한 것이며, fpqc 위상(및 그보다 더 엉성한 모든 위상)의 경우 [준연접층](../Page/준연접층.md "wikilink")에 대한 [내림이](https://ko.wikipedia.org/wiki/내림_이론 "wikilink") 성립한다.\[3\]

### 집합론적 문제

fpqc 위상은 (더 엉성한 위상과 달리) 여러 집합론적 문제를 가진다. fppf 위상이나 [에탈 위상](https://ko.wikipedia.org/wiki/에탈_위상 "wikilink") 등의 경우, 주어진 스킴 \(S\) 위에, 다음 조건을 만족시키는 덮개들의 [집합](https://ko.wikipedia.org/wiki/집합 "wikilink") \(\{\mathcal U_i\}_{i\in I}\)이 존재한다.

  - 임의의 \(S\)의 덮개에 대하여 그보다 더 섬세한 덮개 \(\mathcal U_i\)가 존재한다.

그러나 fpqc 위상의 경우 이 조건이 성립하지 않는다. 즉, 이러한 조건을 만족시키는 덮개들의 [모임은](https://ko.wikipedia.org/wiki/모임_\(수학\) "wikilink") 일반적으로 [고유 모임이다](https://ko.wikipedia.org/wiki/고유_모임 "wikilink"). 이에 따라, fpqc 위상 위의 [준층](https://ko.wikipedia.org/wiki/준층 "wikilink")의 층화는 일반적으로 존재하지 않는다.\[4\]

## 어원

"fpqc"라는 이름은 (충실하게 평탄하며 [준콤팩트](https://ko.wikipedia.org/wiki/준콤팩트_함수 "wikilink"))라는 뜻이다. 여기서 "충실하게 평탄"하다는 것은 [전사 함수이자](https://ko.wikipedia.org/wiki/전사_함수 "wikilink") 평탄 사상이라는 것이다. 이름과 달리, fpqc 위상은 \(\bigsqcup_if_i\)가 [준콤팩트](https://ko.wikipedia.org/wiki/준콤팩트_함수 "wikilink") [전사](https://ko.wikipedia.org/wiki/전사_함수 "wikilink") 평탄 사상인 덮개로서 정의할 수 없다.\[5\] 이러한 사상들로 [그로텐디크 위상을](https://ko.wikipedia.org/wiki/그로텐디크_위상 "wikilink") 정의할 수는 있지만, 이 위상은 [준표준 위상이](https://ko.wikipedia.org/wiki/준표준_위상 "wikilink") 아니다 (즉, [층을](https://ko.wikipedia.org/wiki/층_\(수학\) "wikilink") 이루지 않는 [표현 가능 준층이](https://ko.wikipedia.org/wiki/표현_가능_준층 "wikilink") 존재한다).

"fppf"라는 이름은 (충실하게 평탄하며 [유한 표시](https://ko.wikipedia.org/wiki/유한_표시_사상 "wikilink"))라는 뜻이다. 이름과는 달리, 그 정의에서는 [유한 표시 사상](https://ko.wikipedia.org/wiki/유한_표시_사상 "wikilink") 대신 [국소 유한 표시 사상을](https://ko.wikipedia.org/wiki/국소_유한_표시_사상 "wikilink") 사용한다.

## 참고 문헌

## 외부 링크

  -
  -
  -
  -
  -
  -
  -
  -
  -
[분류:층론](https://ko.wikipedia.org/wiki/분류:층론 "wikilink") [분류:스킴 이론](https://ko.wikipedia.org/wiki/분류:스킴_이론 "wikilink")

1.
2.
3.
4.
5.