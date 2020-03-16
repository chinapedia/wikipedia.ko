> This article is converted from Wikipedia: [ K](https://ko.wikipedia.org/wiki/_K).


[수학](../Page/수학.md "wikilink")에서, **대수적 K이론**(代數的K理論, )은 [환의](../Page/환_\(수학\).md "wikilink") [가군](../Page/가군.md "wikilink")들을 다루는 [K이론](../Page/K이론.md "wikilink")의 한 종류다.

## 정의

대수적 K이론에서 다루는 중심 개념은 **(대수적) K군**() \(\operatorname K_\bullet(-)\)이다. 이들은 주어진 [환](../Page/환_\(수학\).md "wikilink") \(R\)에 대하여 주어지는 일련의 [아벨 군들이다](../Page/아벨_군.md "wikilink").

K군은 다양하게 정의할 수 있다.

  - **퀼런 플러스 구성**()은 역사적으로 가장 최초의 정의이다. 이 정의는 주어진 [환의](../Page/환_\(수학\).md "wikilink") 무한 [일반선형군](../Page/일반선형군.md "wikilink")의 [분류 공간에](../Page/분류_공간.md "wikilink") 그 [기본군](../Page/기본군.md "wikilink")의 일부를 죽이는 연산을 가한 뒤, [호모토피 군을](../Page/호모토피_군.md "wikilink") 취하는 것으로 구성된다. [대니얼 퀼런이](../Page/대니얼_퀼런.md "wikilink") 도입하였다.
  - **퀼런 Q-구성**() 역시 [대니얼 퀼런이](../Page/대니얼_퀼런.md "wikilink") 도입하였다. 이 정의는 **[퀼런 완전 범주](../Page/퀼런_완전_범주.md "wikilink")**라는 특정한 [가법 범주에](https://ko.wikipedia.org/wiki/가법_범주 "wikilink") 대하여 적용되며, 퀼런 완전 범주에서 대상을 그대로 두고 사상을 다르게 정의한 뒤, 이에 대응하는 [단체 집합을](../Page/단체_집합.md "wikilink") 취하고, 그 [호모토피 군을](../Page/호모토피_군.md "wikilink") 취한다. Q-구성을 [환](../Page/환_\(수학\).md "wikilink") \(R\) 위의 [유한 생성](../Page/유한_생성_가군.md "wikilink") [사영 가군](../Page/사영_가군.md "wikilink") 범주 \(\operatorname{fgProjMod}_R\)에 적용할 경우, 이는 퀼런 플러스 구성과 일치한다.
  - **발트하우젠 S-구성**()은 **발트하우젠 범주**()라는 구조가 주어진 [범주에](../Page/범주_\(수학\).md "wikilink") 대하여 적용된다. [퀼런 완전 범주](../Page/퀼런_완전_범주.md "wikilink") 위의 유계 [사슬 복합체의](../Page/사슬_복합체.md "wikilink") 범주 \(\operatorname{bCh}(\mathcal E)\)는 자연스럽게 발트하우젠 범주를 이루며, 이에 따라 발트하우젠 S-구성은 퀼런 Q-구성을 일반화한다. 프리트헬름 발트하우젠()이 도입하였다.

### 퀼런 플러스 구성

[환](../Page/환_\(수학\).md "wikilink") \(R\)가 주어졌다고 하자. 그렇다면, ([이산 공간으로](../Page/이산_공간.md "wikilink") 간주한) 그 [일반선형군](../Page/일반선형군.md "wikilink") \(\operatorname{GL}(n;R)\)들의 [귀납적 극한](../Page/귀납적_극한.md "wikilink")

\[\operatorname{GL}(\infty;R)=\varinjlim_{n\to\infty}\operatorname{GL}(n;R)\] 을 취하자. 이는 [위상군](../Page/위상군.md "wikilink")을 이룬다. 이 위상군의 [분류 공간](../Page/분류_공간.md "wikilink") \(\operatorname B(\operatorname{GL}(\infty;R))\)을 취하자.

위상 공간 \(\operatorname B(\operatorname{GL}(\infty;R))\) 위에 **플러스 구성** \(\operatorname B(\operatorname{GL}(\infty;R))^+\)을 가할 수 있다. 이 경우 그 [호모토피 군들이](../Page/호모토피_군.md "wikilink") 바뀌지만, [호몰로지 군은](https://ko.wikipedia.org/wiki/호몰로지_군 "wikilink") 바뀌지 않는다. 구체적으로, \(\operatorname{GL}(\infty;R)\cong\pi_1(\operatorname B(\operatorname{GL}(\infty;R)))\)의 [정규 부분군](../Page/정규_부분군.md "wikilink") \(E\triangleleft \operatorname{GL}(\infty;R)\)은 하나의 성분을 제외하고 다른 모든 성분이 모두 무한 [단위 행렬을](https://ko.wikipedia.org/wiki/단위_행렬 "wikilink") 이루는 원소들로부터 생성된다. 그렇다면, [기본군](../Page/기본군.md "wikilink")의 [정규 부분군](../Page/정규_부분군.md "wikilink") \(E\)를 죽이는 플러스 연산을 가하여 위상 공간 \(\operatorname B(\operatorname{GL}(\infty;R))^+\)을 얻는다. 그렇다면, \(i>0\)에 대하여 \(i\)차 **K군** \(\operatorname K_i(R)\)은 \(\operatorname B(\operatorname{GL}(\infty;R))^+\)의 \(i\)차 [호모토피 군이다](../Page/호모토피_군.md "wikilink").

\[\operatorname K_i(R)=\pi_i(\operatorname B(\operatorname{GL}(\infty;R))^+)\qquad(i>0)\] \(i=0\)일 경우 위 공식은 성립하지 않는다. (\(\operatorname B(\operatorname{GL}(\infty;R))^+\)는 항상 [경로 연결 공간이다](https://ko.wikipedia.org/wiki/경로_연결_공간 "wikilink").) 환의 0차 K군 \(\operatorname K_0(R)\)는 독립적으로 간단히 정의될 수 있으며, 이 경우

\[\pi_i(R)=\pi_i\left(\operatorname B(\operatorname{GL}(\infty;R))^+\times\operatorname K_0(R)\right)\] 로 정의할 수 있다. (여기서 \(\operatorname K_0(R)\)는 [이산 위상을](https://ko.wikipedia.org/wiki/이산_위상 "wikilink") 준 [위상군](../Page/위상군.md "wikilink")이다.)

### 퀼런 Q-구성

[퀼런 완전 범주](../Page/퀼런_완전_범주.md "wikilink") \(\mathcal E\)가 주어졌다고 하자. 그렇다면, 범주 \(\operatorname Q(\mathcal E)\)는 다음과 같은 범주이다.

  - \(\operatorname Q(\mathcal E)\)의 대상은 \(\mathcal E\)의 대상과 같다.
  - \(\operatorname Q(\mathcal E)\)에서 \(X,Y\in\mathcal E\) 사이의 사상은 \(\mathcal E\)에서의 그림 \(X\twoheadleftarrow A\hookrightarrow Y\)의 동치류이다. 여기서, 두 그림 \(X\twoheadleftarrow A\hookrightarrow Y\), \(X\twoheadleftarrow A'\hookrightarrow Y\) 사이에 다음 그림을 가환 그림으로 만드는 [동형 사상](../Page/동형_사상.md "wikilink") \(A\to A'\)이 존재한다면 두 그림을 서로 동치로 간주한다.
    :<math>\\begin{matrix}

X&\\twoheadleftarrow\&A&\\hookrightarrow\&Y\\\\ \\|&&\\downarrow&&\\|\\\\ X&\\twoheadleftarrow\&A'&\\hookrightarrow\&Y \\end{matrix}</math>

  - \(\operatorname Q(\mathcal E)\)에서 항등 사상은 \(X\overset{\operatorname{id}}\twoheadleftarrow X\overset{\operatorname{id}}\hookrightarrow X\)이다.
  - \(\operatorname Q(\mathcal E)\)에서 사상의 합성은 [당김을](../Page/당김_\(범주론\).md "wikilink") 통해 정의된다. 즉, 그림 \(X\twoheadleftarrow A\hookrightarrow Y\)와 \(Y\twoheadleftarrow B\hookrightarrow Z\)의 합성은 다음과 같은 [당김](../Page/당김_\(범주론\).md "wikilink") \(A\times_YB\)로서 정의된다.
    :<math>\\begin{matrix}

&\&A&\\twoheadleftarrow\&A\\times_YB&\\hookrightarrow\&B\\\\ &&\\|&&&&\\|\\\\ X&\\twoheadleftarrow\&A&\\hookrightarrow\&Y&\\twoheadleftarrow\&B&\\hookrightarrow\&Z \\end{matrix}</math>

이제, \(\operatorname Q(\mathcal E)\)의 [신경](../Page/신경_\(범주론\).md "wikilink") \(\operatorname{nerve}(\operatorname Q(\mathcal E))\)을 취하자. 이는 [단체 집합이다](../Page/단체_집합.md "wikilink"). \(\mathcal E\)의 \(i\)차 **K군**()은 \(\operatorname{nerve}(\operatorname Q(\mathcal E))\)의 (기하학적 실현의) \(i+1\)차 [호모토피 군이다](../Page/호모토피_군.md "wikilink").

\[\operatorname K_i(\mathcal E)=\pi_{i+1}(\operatorname{nerve}(\operatorname Q(\mathcal E)))\]

### 발트하우젠 S-구성

**발트하우젠 범주**(Waldhausen範疇, ) \((\mathcal C,\mathfrak W,\mathfrak C)\)는 다음과 같은 데이터로 구성된다.

  - \(\mathcal C\)는 [영 대상을](https://ko.wikipedia.org/wiki/영_대상 "wikilink") 갖는 [범주이다](../Page/범주_\(수학\).md "wikilink").
  - \(\mathfrak W\)는 \(\mathcal C\)의 사상들의 [모임이다](../Page/모임_\(수학\).md "wikilink"). 그 원소를 **약한 동치**()라고 한다. 이를 \(\xrightarrow\sim\)로 나타내자.
  - \(\mathfrak C\)는 \(\mathcal C\)의 사상들의 [모임이다](../Page/모임_\(수학\).md "wikilink"). 그 원소를 **쌍대올뭉치**()라고 한다. 이를 \(\hookrightarrow\)로 나타내자.

이 데이터는 다음 조건을 만족시켜야 한다.

  - 모든 [동형 사상은](../Page/동형_사상.md "wikilink") 약한 동치이자 쌍대올뭉치이다.
  - [영 대상으로부터의](https://ko.wikipedia.org/wiki/영_대상 "wikilink") 사상 \(0\to X\)는 쌍대올뭉치이다.
  - 쌍대올뭉치는 합성에 대하여 닫혀 있다.
  - 임의의 \(X\hookleftarrow Z\to Y\)에 대하여, [밂](../Page/밂_\(범주론\).md "wikilink") \(X\cup_ZY\)으로 가는 표준적 사상 \(Y\to X\cup_ZY\)는 쌍대올뭉치이다.
  - 다음 가환 그림이 주어졌을 때, 유도 사상 \(X\cup_ZY\to \tilde X\cup_{\tilde Z}\tilde Y\)는 약한 동치이다.
    :<math>\\begin{matrix}

X&\\hookleftarrow\&Z&\\to\&Y\\\\ {\\scriptstyle\\wr}\\downarrow&&\\downarrow\\scriptstyle\\wr&&\\downarrow\\scriptstyle\\wr\\\\ \\tilde X&\\hookleftarrow&\\tilde Z&\\to&\\tilde Y \\end{matrix}</math>

발트하우젠 범주 \(\mathcal C\) 및 자연수 \(n\in\mathbb N\)이 주어졌을 때, 다음과 같은 범주 \(\mathcal S_n(\mathcal C)\)을 생각하자.

  - \(\mathcal S_n(\mathcal C)\)의 대상은 다음 조건을 만족시키는 대상 \(X_{i,j}\) (\(i\le j\)) 및 이들 사이의 적절한 사상으로 구성된다.
      - \(X_{ii}=0\)
      - 쌍대올뭉치의 열 \(0=X_{0,0}\hookrightarrow X_{0,1}\hookrightarrow X_{0,2}\hookrightarrow\cdots\hookrightarrow X_{0,n}\)이 존재한다.
      - \(i\le j\le k\)에 대하여, \(X_{jk}\)는 \(0\leftarrow X_{i,j}\hookrightarrow X_{i,k}\)의 [밂이다](../Page/밂_\(범주론\).md "wikilink").
  - \(\mathcal S_n(\mathcal C)\)의 사상은 적절한 그림들을 가환 그림으로 만드는 \(\mathcal C\)-사상들의 열 \(f_{i,j}\colon X_{i,j}\to Y_{i,j}\)로 구성된다.

그렇다면, 각 \(\mathcal S_n(\mathcal C)\) 역시 자연스럽게 발트하우젠 범주를 이룬다. 또한, 이들을 모두 모은 \(\mathcal S_\bullet(\mathcal C)\)는 자연스럽게 단체 범주(, (작은) 범주의 범주에서의 [단체 대상](https://ko.wikipedia.org/wiki/단체_대상 "wikilink"))를 이룬다.

이 연산 \(\mathcal S_\bullet(-)\)을 거듭해서 가하자. 그렇다면, 일련의 단체 범주 \(\mathcal C,\mathcal S_\bullet(\mathcal C),\mathcal S_\bullet(\mathcal S_\bullet(\mathcal C)),\dots\)들을 얻는다. 이들은 자연스럽게 [스펙트럼](../Page/스펙트럼_\(위상수학\).md "wikilink") \(\mathcal S(\mathcal C)\)을 이룬다.

\(\mathcal C\)의 **K군**들은 [스펙트럼](../Page/스펙트럼_\(위상수학\).md "wikilink") \(\mathcal S(\mathcal C)\)의 [안정 호모토피 군들이다](https://ko.wikipedia.org/wiki/안정_호모토피_군 "wikilink").

## 낮은 차수의 K군

### K<sub>0</sub>

\(R\)가 (단위원을 가진) [환이라고](../Page/환_\(수학\).md "wikilink") 하자. **0차 K군** \(\operatorname K_0(R)\)는 \(R\)의 [유한 생성](../Page/유한_생성_가군.md "wikilink") [사영 가군들의](../Page/사영_가군.md "wikilink") [그로텐디크 군이다](../Page/그로텐디크_군.md "wikilink"). 이는 [세르-스완 정리에](../Page/세르-스완_정리.md "wikilink") 따라서, [벡터 다발의](../Page/벡터_다발.md "wikilink") [그로텐디크 군인](../Page/그로텐디크_군.md "wikilink") [위상 K군에](../Page/위상_K이론.md "wikilink") 대응한다.

[유사환](../Page/유사환.md "wikilink")에 대해서도 K군을 정의할 수 있다. 포함 함자 \(\operatorname{Ring}\hookrightarrow\operatorname{Rng}\)의 [수반 함자를](../Page/수반_함자.md "wikilink") 사용해, 유사환 \(S\)에 단위원을 추가해 [환](../Page/환_\(수학\).md "wikilink") \(R\cong S\oplus\mathbb Z\)으로 만들 수 있다. 이에 따라 [짧은 완전열](https://ko.wikipedia.org/wiki/짧은_완전열 "wikilink")

\[0\to S\to R\to0\] 이 존재한다. 그렇다면 \(S\)의 K군 \(K_0(S)\)는 이에 의하여 유도되는 [군 준동형](https://ko.wikipedia.org/wiki/군_준동형 "wikilink")

\[K_0(R)\to K(\mathbb Z)\cong\mathbb Z\] 의 [핵이다](../Page/핵_\(수학\).md "wikilink").

보다 일반적으로, [퀼런 완전 범주](../Page/퀼런_완전_범주.md "wikilink") \(\mathcal E\)의 **0차 K군** \(\operatorname K_0(\mathcal E)\)는 \(\mathcal E\)의 대상의 동형류들로 생성되는 [자유 아벨 군으로부터](../Page/자유_아벨_군.md "wikilink"), 모든 허용 확대 \(X\hookrightarrow Y\twoheadrightarrow Z\)에 대하여 \([X]-[Y]+[Z]\)로 생성되는 [부분군](../Page/부분군.md "wikilink")에 대한 [몫군](https://ko.wikipedia.org/wiki/몫군 "wikilink")을 취한 것이다.

### K<sub>1</sub>

\(R\)가 (단위원을 가진) [환이라고](../Page/환_\(수학\).md "wikilink") 하자. 그렇다면, 무한 [일반선형군](../Page/일반선형군.md "wikilink")을 다음과 같은 [귀납적 극한으로](../Page/귀납적_극한.md "wikilink") 정의하자.

\[\operatorname{GL}(\infty;R)=\varinjlim_{n\to\infty}\operatorname{GL}(n,R)\] 그렇다면, **1차 K군** \(\operatorname K_1(R)\)는 무한 일반선형군의 [아벨화](https://ko.wikipedia.org/wiki/아벨화 "wikilink")이다.

\[\operatorname K_1(R)=\operatorname{GL}(\infty;R)^{\operatorname{ab}}=\operatorname{GL}(\infty;R)/[\operatorname{GL}(\infty;R),\operatorname{GL}(\infty;R)]\]

### K<sub>2</sub>

\(R\)가 (단위원을 가진) [환이라고](../Page/환_\(수학\).md "wikilink") 하자. 그렇다면, [일반선형군](../Page/일반선형군.md "wikilink") \(\operatorname{GL}(\infty;R)\)의 [교환자 부분군](../Page/교환자_부분군.md "wikilink") \([\operatorname{GL}(\infty;R),\operatorname{GL}(\infty;R)]\)을 생각하자. 이는 [완전군](../Page/완전군.md "wikilink")이며, 따라서 [보편 중심 확대를](https://ko.wikipedia.org/wiki/보편_중심_확대 "wikilink") 갖는다. 이 보편 중심 확대를 \(R\)의 **스테인베르그 군**(Steinberg群, ) \(\operatorname{St}R\)라고 한다. 이는 [로베르트 스테인베르그가](../Page/로베르트_스테인베르그.md "wikilink") 도입하였다.

**2차 K군** \(\operatorname K_2(R)\)는 \(R\)의 스테인베르그 군 \(\operatorname{St}R\)의 [중심이다](https://ko.wikipedia.org/wiki/군의_중심 "wikilink").

\[\operatorname K_2(R)=\operatorname Z(\operatorname{St}R)\]

## 예

### 유한체

[유한체](../Page/유한체.md "wikilink") \(\mathbb F_q\)의 K군은 다음과 같다.

\[\operatorname K_0(\mathbb F_q)=\mathbb Z\]

\[\operatorname K_{2i}(\mathbb F_q)=0\qquad(i>0)\]

\[\operatorname K_{2i-1}(\mathbb F_q)=\mathbb Z/(q^i-1)\qquad(i>0)\]

### 정수환

[정수환](https://ko.wikipedia.org/wiki/정수환 "wikilink") \(\mathbb Z\)의 K군의 계산은 매우 어려운 문제이다.

\[\operatorname K_0(\mathbb Z)=\mathbb Z\]

\[\operatorname K_1(\mathbb Z)=\mathbb Z/2\]

\[\operatorname K_2(\mathbb Z)=\mathbb Z/2\]

\[\operatorname K_3(\mathbb Z)=\mathbb Z/48\]

\[\operatorname K_4(\mathbb Z)\]는 알려지지 않았으나, 아마 0일 것으로 추측된다.

## 역사

[K이론](../Page/K이론.md "wikilink")의 시초는 [알렉산더 그로텐디크에](../Page/알렉산더_그로텐디크.md "wikilink") 의한 [그로텐디크-리만-로흐 정리의](../Page/그로텐디크-리만-로흐_정리.md "wikilink") 증명으로 여겨진다 (1956년).\[1\] 곧 1950년대 말에 [마이클 아티야와](../Page/마이클_아티야.md "wikilink") [프리드리히 히르체브루흐는](../Page/프리드리히_히르체브루흐.md "wikilink") 이를 위상 공간 위의 유한 차원 [벡터 다발에](../Page/벡터_다발.md "wikilink") 적용하여 [위상 K이론을](../Page/위상_K이론.md "wikilink") 개발하였다.

[세르-스완 정리에](../Page/세르-스완_정리.md "wikilink") 따라, [가환환](../Page/가환환.md "wikilink") 위의 "유한 차원 벡터 다발"은 [유한 생성](../Page/유한_생성_가군.md "wikilink") [사영 가군이다](../Page/사영_가군.md "wikilink"). 이를 사용하여, 1962년에 [하이먼 배스와](../Page/하이먼_배스.md "wikilink") [스티븐 섀뉴얼이](../Page/스티븐_섀뉴얼.md "wikilink") [환의](../Page/환_\(수학\).md "wikilink") 0차·1차 K군을 엄밀히 정의하였다.\[2\] 2차 K군의 정의는 [존 밀너가](../Page/존_밀너.md "wikilink") 1970년에 발견하였다.\[3\] 밀너는 이 구성을 고차 \(n\)에 대하여 일반화하였는데, 이를 [밀너 K군이라고](https://ko.wikipedia.org/wiki/밀너_K군 "wikilink") 한다. 그러나 고차 밀너 K군은 고차 K군과 일반적으로 다르다.

고차 K군의 올바른 정의는 [대니얼 퀼런이](../Page/대니얼_퀼런.md "wikilink") 1970년대 초에 발견하였다. 퀼런은 플러스 구성\[4\]\[5\]\[6\]과 Q-구성\[7\]을 정의하였으며, 두 구성이 서로 일치함을 증명하였다.

이후 1985년에 프리트헬름 발트하우젠(, 1938\~)이 퀼런 Q-구성을 [호모토피 이론적으로](https://ko.wikipedia.org/wiki/호모토피_이론 "wikilink") 일반화한 S-구성을 발표하였다.\[8\]

## 참고 문헌

  -
  -
  -
  -   -
      -
  -   -
      -
  -
  -
  -
  -
  -
## 외부 링크

  -
  -
  -   -
  -   -
  -
  -
  -
  -   -
  -
  -
[분류:K이론](https://ko.wikipedia.org/wiki/분류:K이론 "wikilink") [분류:대수기하학](https://ko.wikipedia.org/wiki/분류:대수기하학 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.