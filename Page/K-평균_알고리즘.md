> This article is converted from Wikipedia: [K- ](https://ko.wikipedia.org/wiki/K-_).


**k-평균 알고리즘**()은 주어진 [데이터](https://ko.wikipedia.org/wiki/데이터 "wikilink")를 k개의 [클러스터](https://ko.wikipedia.org/wiki/클러스터 "wikilink")로 묶는 알고리즘으로, 각 클러스터와 거리 차이의 [분산](https://ko.wikipedia.org/wiki/분산 "wikilink")을 최소화하는 방식으로 동작한다. 이 알고리즘은 [자율 학습의](https://ko.wikipedia.org/wiki/자율_학습_\(기계_학습\) "wikilink") 일종으로, 레이블이 달려 있지 않은 입력 데이터에 레이블을 달아주는 역할을 수행한다. 이 알고리즘은 [EM 알고리즘을](https://ko.wikipedia.org/wiki/EM_알고리즘 "wikilink") 이용한 클러스터링과 비슷한 구조를 가지고 있다.

## 도입

### 역사

"k-평균"에 대한 개념은 1957년 [후고 스테인하우스에](../Page/후고_스테인하우스.md "wikilink") 의해 소개되었으나,\[1\] 용어 자체는 1967년에 제임스 매퀸()에 의해 처음 사용되었다.\[2\] 현재 사용되고 있는 [표준 알고리즘은](https://ko.wikipedia.org/wiki/#표준_알고리즘 "wikilink") 1957년에 스튜어트 로이드()가 [펄스 부호 변조](../Page/펄스_부호_변조.md "wikilink")(PCM)를 목적으로 처음으로 고안 하였으나 1982년이 되어서야 컴퓨터 과학 매거진에 처음 공개되었다.\[3\] 알고리즘이 공개되기 이전인 1965년에 E. W. Forgy 또한 같은 알고리즘을 제안하였다.\[4\] 차후 1975년과 1979년에 Hartigan과 Wong에 의해 거리 계산이 필요하지 않은 좀 더 효율적인 방법이 소개 되었다.\[5\]\[6\]

### 개요

k-평균 클러스터링 알고리즘은 클러스터링 방법 중 분할법에 속한다. 분할법은 주어진 데이터를 여러 파티션 (그룹) 으로 나누는 방법이다. 예를 들어 n개의 데이터 오브젝트를 입력받았다고 가정하자. 이 때 분할법은 입력 데이터를 n보다 작거나 같은 k개의 그룹으로 나누는데, 이 때 각 군집은 클러스터를 형성하게 된다. 다시 말해, 데이터를 한 개 이상의 데이터 오브젝트로 구성된 k개의 그룹으로 나누는 것이다. 이 때 그룹을 나누는 과정은 거리 기반의 그룹간 비유사도 (dissimilarity) 와 같은 비용 함수 (cost function) 을 최소화하는 방식으로 이루어지며, 이 과정에서 같은 그룹 내 데이터 오브젝트 끼리의 유사도는 증가하고, 다른 그룹에 있는 데이터 오브젝트와의 유사도는 감소하게 된다.\[7\] k-평균 알고리즘은 각 그룹의 중심 (centroid)과 그룹 내의 데이터 오브젝트와의 거리의 제곱합을 비용 함수로 정하고, 이 함수값을 최소화하는 방향으로 각 데이터 오브젝트의 소속 그룹을 업데이트 해 줌으로써 클러스터링을 수행하게 된다.

### 목표

n개의 d-차원 데이터 오브젝트 (**x**<sub>1</sub>, **x**<sub>2</sub>, …, **x**<sub>*n*</sub>) 집합이 주어졌을 때, k-평균 알고리즘은 n개의 데이터 오브젝트들을 각 집합 내 오브젝트 간 응집도를 최대로 하는 \(k(\leq n)\) 개의 집합 **S** = {*S*<sub>1</sub>, *S*<sub>2</sub>, …, *S*<sub>*k*</sub>} 으로 분할한다. 다시 말해, ***μ***<sub>*i*</sub>가 집합 *S*<sub>*i*</sub>의 중심점이라 할 때

<center>

\(\underset{\mathbf{S}} {\operatorname{arg\,min}}  \sum_{i=1}^{k} \sum_{\mathbf x \in S_i} \left\| \mathbf x - \boldsymbol\mu_i \right\|^2\)

</center>

각 집합별 중심점\~집합 내 오브젝트간 거리의 제곱합을 최소로 하는 집합 **S**를 찾는 것이 이 알고리즘의 목표다. 이 목적 함수의 전역 최솟값 (global minimum) 을 찾는 것은 [NP-난해](../Page/NP-난해.md "wikilink") 문제이므로, 언덕 오르기 (hill climbing) 방식으로 목적 함수의 오차를 줄여나가며 지역 최솟값 (local minimum) 을 발견했을 때 알고리즘을 종료함으로써 근사 최적해를 구한다.

## 알고리즘

### 표준 알고리즘

\(i\)번째 클러스터의 중심을 \(\mu_i\), 클러스터에 속하는 점의 집합을 \(S_i\)라고 할 때, 전체 분산은 다음과 같이 계산된다.

\[V = \sum_{i=1}^{k} \sum_{j \in S_i} |x_j - \mu_i |^2\]

이 값을 최소화하는 \(S_i\)을 찾는 것이 알고리즘의 목표가 된다.

알고리즘은 우선 [초기의 \(\mu_i\)를 설정하는](https://ko.wikipedia.org/wiki/#초기화_기법 "wikilink") 것으로 시작한다. 이후 다음의 두 단계를 반복한다.

  - **클러스터 설정**: 각 데이터로부터 각 클러스터들의 \(\mu_i\)까지의 [유클리드 거리를](https://ko.wikipedia.org/wiki/유클리드_거리 "wikilink") 계산하여, 해당 데이터에서 가장 가까운 클러스터를 찾아 데이터를 배당한다.

\[S^{(t)}_i = \{ x_p : |x_p - \mu_i^{(t)}|^2 \leq |x_p - \mu_j^{(t)}|^2 \forall j, 1 \leq j \leq k \}\]

  - **클러스터 중심 재조정**: \(\mu_i\)를 각 클러스터에 있는 데이터들의 [무게중심](https://ko.wikipedia.org/wiki/무게중심 "wikilink") 값으로 재설정해준다.

\[\mu^{(t+1)}_i = \frac{1}{|S^{(t)}_i|} \sum\limits_{x_j \in S^{(t)}_i} x_j\]

  -

      -
        만약 클러스터가 변하지 않는다면 반복을 중지한다.

맨 처음, 각 [점들을](../Page/점_\(기하학\).md "wikilink") \(k\)개 [집합](../Page/집합.md "wikilink")으로 나눈다. 이때 임의로 나누거나, 어떤 [휴리스틱 기법을](https://ko.wikipedia.org/wiki/휴리스틱_기법 "wikilink") 사용할 수도 있다. 그 다음 각 집합의 무게 중심을 구한다. 그 다음, 각각의 점들을 방금 구한 무게중심 가운데 제일 가까운 것에 연결지음으로써 새로이 집합을 나눌 수 있다. 이 작업을 반복하면 점들이 소속된 집합을 바꾸지 않거나, [무게중심](https://ko.wikipedia.org/wiki/무게중심 "wikilink")이 변하지 않는 상태로 수렴될 수 있다. [섬네일](https://ko.wikipedia.org/wiki/파일:Kmeans_animation_withoutWatermark.gif "wikilink")

파일:K Means Example Step 1.svg|1) 초기 *k* "평균값" (위의 경우 *k*=3) 은 데이터 오브젝트 중에서 무작위로 뽑힌다. (색칠된 동그라미로 표시됨). 파일:K Means Example Step 2.svg|2) *k* 각 데이터 오브젝트들은 가장 가까이 있는 평균값을 기준으로 묶인다. 평균값을 기준으로 분할된 영역은 [보로노이 다이어그램](https://ko.wikipedia.org/wiki/보로노이_다이어그램 "wikilink") 으로 표시된다.. 파일:K Means Example Step 3.svg|3) *k*개의 클러스터의 [중심점을](../Page/질량_중심.md "wikilink") 기준으로 평균값이 재조정된다. 파일:K Means Example Step 4.svg|4) 수렴할 때 까지 2), 3) 과정을 반복한다.

<table>
<tbody>
<tr class="odd">
<td><p>입력값</p>
<ol>
<li>k: 클러스터 수</li>
<li>D: n 개의 데이터 오브젝트를 포함하는 집합</li>
</ol>
<p>출력값: k 개의 클러스터</p>
<p>알고리즘</p>
<ol>
<li>데이터 오브젝트 집합 D에서 k 개의 데이터 오브젝트를 임의로 추출하고, 이 데이터 오브젝트들을 각 클러스터의 중심 (centroid) 으로 설정한다. (초기값 설정)</li>
<li>집합 D의 각 데이터 오브젝트들에 대해 k 개의 클러스터 중심 오브젝트와의 거리를 각각 구하고, 각 데이터 오브젝트가 어느 중심점 (centroid) 와 가장 유사도가 높은지 알아낸다. 그리고 그렇게 찾아낸 중심점으로 각 데이터 오브젝트들을 할당한다.</li>
<li>클러스터의 중심점을 다시 계산한다. 즉, <strong>2</strong>에서 재할당된 클러스터들을 기준으로 중심점을 다시 계산한다.</li>
<li>각 데이터 오브젝트의 소속 클러스터가 바뀌지 않을 때 까지 <strong>2</strong>, <strong>3</strong> 과정을 반복한다.</li>
</ol></td>
</tr>
</tbody>
</table>

**2**는 위의 클러스터 설정 단계에 해당하고, **3** 과정이 위의 클러스터 중심 재조정 단계에 해당한다.\[8\]

### 초기화 기법

#### 무작위 분할 (Random Partition)

무작위 분할 알고리즘은 가장 많이 쓰이는 초기화 기법으로\[9\], 각 데이터들을 임의의 클러스터에 배당한 후, 각 클러스터에 배당된 점들의 평균 값을 초기 \(\mu_i\)로 설정한다. 무작위 분할 기법의 경우 다른 기법들과는 달리 데이터 순서에 대해 독립적이다. 무작위 분할의 경우 초기 클러스터가 각 데이터들에 대해 고르게 분포되기 때문에 각 초기 클러스터의 무게중심들이 데이터 집합의 중심에 가깝게 위치하는 경향을 띈다. 이러한 특성 때문에 [k-조화 평균이나](https://ko.wikipedia.org/wiki/k-조화_평균 "wikilink") [퍼지 k-평균에서는](https://ko.wikipedia.org/wiki/퍼지_k-평균 "wikilink") 무작위 분할이 선호된다.\[10\]

#### Forgy

Forgy 알고리즘은 1965년 Forgy에 의해 고안되었으며\[11\] 현재 주로 쓰이는 초기화 기법 중 하나로, 데이터 집합으로부터 임의의 \(k\)개의 데이터를 선택하여 각 클러스터의 초기 \(\mu_i\)로 설정한다. [무작위 분할 기법과](https://ko.wikipedia.org/wiki/#무작위_분할_\(Random_Partition\) "wikilink") 마찬가지로 Forgy 알고리즘은 데이터 순서에 대해 독립적이다.\[12\] Forgy 알고리즘의 경우 초기 클러스터가 임의의 \(k\)개의 점들에 의해 설정되기 때문에 각 클러스터의 무게중심이 중심으로부터 퍼져있는 경향을 띈다. 이러한 특성 때문에 [EM 알고리즘이나](https://ko.wikipedia.org/wiki/EM_알고리즘 "wikilink") [표준 k-평균 알고리즘에서는](https://ko.wikipedia.org/wiki/#표준_알고리즘 "wikilink") Forgy 알고리즘이 선호된다.\[13\]

#### MacQueen

1967년 MacQueen에 의해 고안된 MacQueen 알고리즘은\[14\] [Forgy 알고리즘과](https://ko.wikipedia.org/wiki/#Forgy "wikilink") 마찬가지로 데이터 집합으로 부터 임의의 \(k\)개의 데이터를 선택하여 각 클러스터의 초기 \(\mu_i\)로 설정한다. 이후 선택되지 않은 각 데이터들에 대해, 해당 점으로부터 가장 가까운 클러스터를 찾아 데이터를 배당한다. 모든 데이터들이 클러스터에 배당되고 나면 각 클러스터의 무게중심을 다시 계산하여 초기 \(\mu_i\)로 다시 설정한다. MacQueen 알고리즘의 경우 최종 수렴에 가까운 클러스터를 찾는 것은 비교적 빠르나, 최종 수렴에 해당하는 클러스터를 찾는 것은 매우 느리다.\[15\]

#### Kaufman

1990년에 Kaufman과 Rousseeuw에 의해 고안된 Kaufman 알고리즘\[16\] 은 전체 데이터 집합 중 가장 중심에 위치한 데이터를 첫번째 \(\mu_i\)로 설정한다. 이후 선택되지 않은 각 데이터들에 대해, 가장 가까운 무게중심 보다 선택되지 않은 데이터 집합에 더 근접하게 위치한 데이터를 또 다른 \(\mu_i\)로 설정하는 것을 총 \(k\)개의 \(\mu_i\)가 설정될 때 까지 반복한다. [무작위 분할과](https://ko.wikipedia.org/wiki/#무작위_분할_\(Random_Partition\) "wikilink") 마찬가지로, Kaufman 알고리즘은 초기 클러스터링과 데이터 순서에 대해 비교적 독립적이기 때문에 해당 요소들에 의존적인 다른 알고리즘들 보다 월등한 성능을 보인다.\[17\]

## 복잡도

k-평균 알고리즘의 계산 복잡도에 크게 영향을 미치는 요소 두가지는 [유클리드 공간](../Page/유클리드_공간.md "wikilink") 와 클러스터의 수 이다. 클러스터의 수가 작더라도, 일반적인 [유클리드 공간](../Page/유클리드_공간.md "wikilink") 에서 k-평균 알고리즘의 최적 해를 찾는 것은 [NP-난해](../Page/NP-난해.md "wikilink")이다.\[18\]\[19\] 반대로 낮은 차원의 [유클리드 공간일지라도](../Page/유클리드_공간.md "wikilink"), 개의 클러스터에 대해 최적 해를 찾는 것 또한 [NP-난해](../Page/NP-난해.md "wikilink")이다.\[20\]

이러한 이유로 k-평균 알고리즘에서는 위와 같은 [휴리스틱 기법을](https://ko.wikipedia.org/wiki/발견법 "wikilink") 주로 사용한다. [Lloyd 알고리즘의](https://ko.wikipedia.org/wiki/#표준_알고리즘 "wikilink") 경우, [시간 복잡도는](../Page/시간_복잡도.md "wikilink") 클러스터의 수, 데이터 [벡터](https://ko.wikipedia.org/wiki/벡터 "wikilink")의 차원, 데이터 [벡터](https://ko.wikipedia.org/wiki/벡터 "wikilink")의 수에 각각 비례한다. 또한 알고리즘이 해가 수렴하기까지 반복되므로, 알고리즘이 반복된 횟수에도 비례한다. 즉, 개의 -차원 데이터 [벡터](https://ko.wikipedia.org/wiki/벡터 "wikilink")들을 번의 반복을 통해 개의 클러스터로 묶는데 걸리는 시간은 \(O(nkdi)\)이다. 보통 데이터 오브젝트의 개수보다 클러스터의 개수가 훨씬 적으므로 \(k \ll n\)이고, 알고리즘 반복 횟수 역시 데이터 오브젝트 개수보다 훨씬 적으므로 \(i\ll n\)이다. 따라서, k-평균 알고리즘은 많은 환경에서 빠르게 수렴하고, 대규모 데이터를 처리하는데 적합하므로 널리 사용된다.

  - Smoothed analysis 경우의 복잡도는 다항 시간이다. \([0, 1]^d\)내의 임의의 개의 점들의 집합에 대해, 집합 내의 각 점들이 평균 , 분산\(\sigma^2\)의 정규분포를 이룬다면, 해당 집합을 개의 클러스터로 묶는데 걸리는 시간이 \(O(n^{34}k^{34}d^8\log^4(n)/\sigma^2)\)임이 증명된 바 있다.<ref name="arthur2009">

</ref>

  - 다항을 넘는() 시간(\(2^{\Omega(\sqrt{n})}\))이 걸리는 경우도 존재한다.\[21\]
  - [공간 복잡도의](https://ko.wikipedia.org/wiki/공간_복잡도 "wikilink") 경우, 알고리즘은 각 클러스터의 무게중심 [벡터](https://ko.wikipedia.org/wiki/벡터 "wikilink")들에 대한 정보를 추가로 저장해야 하고, 이 무게중심 [벡터](https://ko.wikipedia.org/wiki/벡터 "wikilink")들은 매 반복마다 독립적이기 때문에, k-평균 알고리즘은 \(O((n+k)d)\)의 [공간 복잡도를](https://ko.wikipedia.org/wiki/공간_복잡도 "wikilink") 가진다.

## 한계점

k-평균 알고리즘은 몇 가지 한계점을 가지고 있다.

  - 클러스터 개수 k값을 입력 파라미터로 지정해주어야 한다.

이 알고리즘은 k값에 따라 결과값이 완전히 달라진다. 예를 들어, 실제 데이터가 4개의 클러스터를 가지고 있는데, k=3으로 입력했다고 가정하자. 그러면 아래와 같은 결과가 나올 수 있다.

[center](https://ko.wikipedia.org/wiki/파일:Kmeans_wrongK.PNG "wikilink")

이는 실제 클러스터의 수 보다 k값이 작을 때 발생하는 현상이다. 반대로, 실제 클러스터가 5개인데 k=8을 입력했다고 가정하자. 결과는 아래와 같다.

[섬네일](https://ko.wikipedia.org/wiki/파일:Kmeans_toomany.PNG "wikilink")

따라서, k값을 어떻게 주느냐에 따라 클러스터링의 결과가 극명하게 달라지며, 좋지 못한 결과를 보여줄 가능성이 있다.

  - 알고리즘의 에러 수렴이 전역 최솟값이 아닌 지역 최솟값으로 수렴할 가능성이 있다.

이 알고리즘은 초기값을 어떻게 주느냐에 따라 최적화의 결과가 전역 최적값 (global optimum) 이 아닌 지역 최적값 (local optimum) 으로 빠질 가능성이 있다. 예를 들어, 실제 데이터는 3개의 클러스터를 가지고 있고, k도 3이라고 하자. 데이터와 초기 중심값의 분포는 아래와 같다.

[섬네일](https://ko.wikipedia.org/wiki/파일:Kmeans_wronginit1.PNG "wikilink")

그러나 알고리즘을 수행하면서 비용 함수 최소화를 진행하면 아래와 같이 지역 최솟값에 빠져 그대로 수렴하게 된다.

[섬네일](https://ko.wikipedia.org/wiki/파일:Kmeans_wronginit2.PNG "wikilink")

즉, 비용 함수의 함수 공간에서 최적화를 시행할 때, 에러가 줄어드는 방향으로 최적해를 찾아가게 되는데, 전역이 아닌 지역 최솟값에 도달해도 알고리즘의 수렴 조건을 만족하게 되므로 더 이상 최적화를 진행하지 않게 된다. 따라서, 사용자가 기대한 결과를 얻지 못하게 되는 것이다. 이를 방지하기 위해 [담금질 기법](../Page/담금질_기법.md "wikilink") (Simulated Annealing) 을 수행하여 의도적으로 에러가 줄어드는 방향을 피하는 방식을 이용하거나, 서로 다른 초기값으로 여러 번 시도해본 뒤 가장 에러값이 낮은 결과를 사용하는 기법 등을 이용함으로써 이 문제를 완화할 수 있다.

  - 이상값 (outlier) 에 민감하다.

k-평균 알고리즘은 이상값 (outlier) 에 민감하게 반응한다. 이상값이란 다른 대부분의 데이터와 비교했을 때 멀리 떨어져 있는 데이터를 의미한다. 이러한 이상값은 알고리즘 내에서 중심점을 갱신하는 과정에서 클러스터 내의 전체 평균 값을 크게 왜곡시킬 수 있다. 따라서 클러스터의 중심점이 클러스터의 실제 중심에 있지 않고 이상값 방향으로 치우치게 위치할 수 있다. 아래의 경우를 살펴보면

[섬네일](https://ko.wikipedia.org/wiki/파일:Kmeans_outlier.PNG "wikilink")

실제 데이터 클러스터는 오른쪽 중간에 위치해있는데 반해 클러스터의 중심은 클러스터로부터 왼쪽으로 상당히 떨어진 지점에 위치한다. 이는 실제 클러스터 외부에 퍼져 있는 이상값들이 중심점 계산에 있어 그 값을 크게 왜곡시켰기 때문이다. 이를 방지하기 위해 k-평균 알고리즘을 실시하기 전에 이상값을 제거하는 프로세스를 먼저 실행하거나, 분할법의 일종인 k-대푯값 알고리즘 (k-medoids algorithm) 을 이용하면 이상값의 영향을 줄일 수 있다.

  - 구형 (spherical) 이 아닌 클러스터를 찾는 데에는 적절하지 않다.

k-평균 알고리즘은 비용 함수를 계산할 때 중심점과 각 데이터 오브젝트간의 거리를 계산하게 된다. 이 때 사용하는 거리는 [유클리드 거리이다](https://ko.wikipedia.org/wiki/유클리드_거리 "wikilink"). 따라서, 알고리즘 수행 시 중심점으로부터 구형으로 군집화가 이루어지게 된다. 만약 주어진 데이터 집합의 분포가 구형이 아닐 경우에는 클러스터링 결과가 예상과 다를 수 있다. 아래의 경우를 살펴보자.

[섬네일](https://ko.wikipedia.org/wiki/파일:Kmeans_nonspherical.PNG "wikilink")

위의 경우에는 총 4개의 클러스터가 존재하는데, 구형인 클러스터는 2개만 존재한다. 위와 같은 경우 클러스터링을 시행하면 중심점으로부터 가까이 있는 데이터 오브젝트들을 한 그룹으로 묶게 되는데, 그러면 얼굴 형상의 데이터 분포를 고르게 4 조각으로 자르는 형상이 나오게 된다. 이는 알고리즘 사용자가 원하는 결과와는 크게 다르다. 위와 같은 경우에는 비슷한 밀도를 가진 데이터 군집을 하나의 클러스터링으로 묶는 방법인 DBSCAN (Density-Based Spatial Clustering of Applications with Noise) 알고리즘이나 mean-shift 클러스터링 알고리즘을 사용하면 원하는 결과를 얻을 수 있다.

## 클러스터의 수

주어진 데이터 집합에서 구하고자 하는 클러스터의 숫자를 설정할 때 다음의 방법론들을 이용할 수 있다.

### Rule of thumb

가장 간단한 방법으로, 데이터의 수가 *n*이라 할 때, 필요한 클러스터의 수는 다음과 같이 계산될 수 있다.\[22\]

  -
    \(k \approx \sqrt{n/2}\)

### Elbow Method

클러스터의 수를 순차적으로 늘려가면서 결과를 모니터링 한다. 만약 하나의 클러스터를 추가했을 때 이전보다 훨씬 더 나은 결과를 나타내지 않는다면, 이전의 클러스터의 수를 구하고자 하는 클러스터의 수로 설정한다.

### 정보 기준 접근법 (Information Criterion Approach)

클러스터링 모델에 대해 [가능도](../Page/가능도.md "wikilink")를 계산하는 것이 가능할 때 사용하는 방법으로, [베이지안 정보 기준](https://en.wikipedia.org/wiki/Bayesian_information_criterion) 등이 있다. k-평균 클러스터링 모델의 경우 [가우시안](https://ko.wikipedia.org/wiki/정규분포 "wikilink") [혼합 모델에](../Page/혼합_모델.md "wikilink") 가깝기 때문에, 가우시안 혼합 모델에 대한 가능도를 만들어 정보 기준 값을 설정할 수 있다.\[23\]

## 클러스터링 평가 척도

클러스터링이 얼마나 잘 되었는가를 측정하는 방법으로 내부 평가 혹은 외부 평가, 크게 2가지 방법론을 이용할 수 있다.

### 내부 평가

내부 평가 (internal evaluation) 은 데이터 집합을 클러스터링한 결과 그 자체를 놓고 평가하는 방식이다. 이러한 방식에서는 클러스터 내 높은 유사도 (high intra-cluster similarity) 를 가지고, 클러스터 간 낮은 유사도 (low inter-cluster similarity) 를 가진 결과물에 높은 점수를 준다. 이와 같은 평가 방법은 오로지 데이터를 클러스터링한 결과물만을 보고 판단하기 때문에, 평가 점수가 높다고 해서 실제 참값 (ground truth) 에 가깝다는 것을 반드시 보장하지는 않는다는 단점이 있다.\[24\]

#### Davies-Bouldin index

Davies-Bouldin index는 아래의 식으로 계산된다.

\[DB = \frac {1} {n} \sum_{i=1}^{n} \max_{j\neq i}\left(\frac{\sigma_i + \sigma_j} {d(c_i,c_j)}\right)\] n은 클러스터의 개수, \(c_x\)는 클러스터 \(x\)의 중심점, \(\sigma_x\)는 클러스터 \(x\)내의 모든 데이터 오브젝트로부터 중심점 \(c_x\)까지 거리의 평균값이며 \(d(c_i,c_j)\)는 중심점 \(c_i\)와 중심점 \(c_j\)간의 거리이다. 높은 클러스터 내 유사도를 가지고 낮은 클러스터간 유사도를 가지는 클러스터들을 생성하는 클러스터링 알고리즘은 낮은 Davies-Bouldin index 값을 가지게 된다. 따라서, 이 지표가 낮은 클러스터링 알고리즘이 좋은 클러스터링 알고리즘으로 평가된다.

#### Dunn index

Dunn index는 밀도가 높고 잘 나뉜 클러스터링 결과를 목표로 한다. 이 지표는 클러스터간 최소 거리와 클러스터간 최대 거리의 비율로 정의된다. 각 클러스터에 대하여, Dunn index를 아래의 식으로 계산할 수 있다.\[25\]

\[D = \frac{\min_{1 \leq i < j \leq n} d(i,j)}{\max_{1 \leq k \leq n} d^{\prime}(k)} \,,\] *d*(*i*,*j*)는 클러스터 *i*와 클러스터 *j*간의 거리이고 *d* '(*k*)는 클러스터 *k*의 클러스터 내 거리 (dissimilarity)를 측정한 값이다. 클러스터 간 거리 *d*(*i*,*j*)는 두 클러스터의 중심점 끼리의 거리, 혹은 두 클러스터의 각 데이터 오브젝트끼리의 거리의 평균 등 어떤 방식으로든 계산될 수 있다. 마찬가지로, 클러스터 내 거리 *d* '(*k*) 역시 클러스터 내 가장 멀리 떨어진 데이터 오브젝트 간 거리 등으로 구할 수 있다. 내부 평가 방식은 높은 클러스터 내 유사도와 낮은 클러스터간 유사도에 높은 점수를 주기 때문에, Dunn index값이 높은 클러스터링 알고리즘은 클러스터링 성능이 좋은 것으로 판단할 수 있다.

#### 실루엣 기법

1986년 Peter J. Rousseeuw에 의해 처음으로 서술된 [실루엣](https://en.wikipedia.org/wiki/Silhouette_\(clustering\)) 은 간단한 방법으로 데이터들이 얼마나 잘 클러스터링 되었는지를 나타낸다.\[26\] 하나의 데이터 *i* 에 대해, 해당 데이터가 속한 클러스터 내부의 데이터들과의 부동성을 \(a(i)\)라 하고, 해당 데이터가 속하지 않은 클러스터들의 내부의 데이터들과의 부동성을 \(b(i)\)라 할 때, 실루엣 \(s(i)\)은 다음과 같이 계산될 수 있다.

\[s(i) = \frac{b(i) - a(i)}{\max\{a(i),b(i)\}}\] 이때 계산된 \(s(i)\)는 다음의 값을 가진다.

\[-1 \leq s(i) \leq 1\]

\(s(i)\)가 1에 가까울 수록 데이터 데이터 *i* 는 올바른 클러스터에 분류된 것이며, -1에 가까울 수록 잘못된 클러스터에 분류되었음을 나타낸다.

### 외부 평가

외부 평가 방식 (external evaluation)에서 클러스터링의 결과물은 클러스터링에 사용되지 않은 데이터로 평가된다. 다시 말해, 클러스터링의 결과물을 전문가들이 미리 정해높은 모범답안 혹은 외부 벤치마크 평가 기준 등을 이용해서 클러스터링 알고리즘의 정확도를 평가하는 것이다. 이러한 평가 방식은 클러스터링 결과가 미리 정해진 결과물과 얼마나 비슷한지를 측정한다.

#### 랜드 측정

[랜드 측정](https://ko.wikipedia.org/wiki/랜드_인덱스 "wikilink")(Rand measure)는 클러스터링 알고리즘에 의해 형성된 클러스터링 결과물이 미리 정해진 모범 답안과 얼마나 비슷한지를 계산한다.\[27\] 이 척도는 클러스터링 알고리즘이 얼마나 답을 잘 맞추었는지를 퍼센티지로 표현해준다. 식은 아래와 같다.

\[RI = \frac {TP + TN} {TP + FP + FN + TN}\] \(TP\)는 참인 것을 참이라고 답한 것의 개수, \(TN\)은 거짓인 것을 거짓이라고 답한 것의 개수이며 \(FP\)는 거짓인 것을 참으로 판정한 것의 개수 그리고 \(FN\)는 참인 것을 거짓으로 판정한 것의 개수이다. 이 방식의 문제점은 \(FP\)와 \(FN\)을 같은 비중으로 계산한다는 것이다. 이와 같은 방식으로는 일부 클러스터링 알고리즘을 평가할 때 좋지 않을 수 있다. F-measure는 이 문제를 어느 정도 완화한 방식이다.

#### F 측정

[F 측정](https://ko.wikipedia.org/wiki/F1_스코어 "wikilink")(F-measure)은 \(\beta \geq 0\)값을 바꾸면서 [재현율을](../Page/정밀도와_재현율.md "wikilink") 조정함으로써 FN값의 비중을 변화시킨다. [정밀도와 재현율은](../Page/정밀도와_재현율.md "wikilink") 아래와 같이 정의된다.

\[P = \frac {TP } {TP + FP }\]

\[R = \frac {TP } {TP + FN}\] F-measure 값은 아래의 식으로 구할 수 있다.\[28\]

\[F_{\beta} = \frac {(\beta^2 + 1)\cdot P \cdot R } {\beta^2 \cdot P + R}\] \(\beta=0\)일 때, \(F_{0}=P\)이다. 다시 말해, 재현율은 \(\beta=0\)일 때 어떠한 영향을 미치지 못한다. \(\beta\)값을 키울수록 최종 F-measure에 재현율이 미치는 영향은 커진다.

#### 자카드 지수

[자카드 지수](https://ko.wikipedia.org/wiki/자카드_지수 "wikilink")(Jaccard index)는 두 데이터 집합 간의 유사도를 정량화하는 데 사용되며, 0과 1 사이의 값을 가진다. 이 값이 1이라는 것은 두 데이터 집합이 서로 동일하다는 것을 의미하며, 반대로 0일 때는 두 데이터 집합은 공통된 요소를 전혀 가지지 않는다는 것을 뜻한다. Jaccard index는 아래의 식으로 정의된다.

\[J(A,B) = \frac {|A \cap B| } {|A \cup B|} = \frac{TP}{TP + FP + FN}\] 이 값은 두 데이터 집합 간의 공통 원소들의 개수를 두 데이터 집합의 합집합의 원소 개수로 나눈 것이다.

## 응용

k-평균 알고리즘은 시장 분할, [컴퓨터 비전](https://ko.wikipedia.org/wiki/컴퓨터_비전 "wikilink"), 지질통계학, 천문학 및 농업 등 광범위한 분야에 적용될 수 있다. 이 기법은 주로 어떤 알고리즘을 수행하기 전 데이터를 전처리 (pre-processing) 하는 용도로 많이 쓰인다.

### 이미지 분할

컴퓨터 비전 분야에서 [이미지 분할](../Page/영상_분할.md "wikilink") (image segmentation) 은 디지털 이미지를 여러 개의 부분 (segments), 즉 픽셀들의 집합 (통칭 superpixel) 으로 나누는 과정이다. 좀 더 자세히 말하자면, 이미지 분할은 각 픽셀에 어떤 레이블을 붙여줌으로써 비슷한 성질을 가진 픽셀 끼리 같은 레이블을 가지게 하는 것이다. 이미지 분할의 목표는 주어진 이미지를 단순화하고 이미지 표현 방식을 단순화하여 이미지를 좀 더 분석하기 편한 형태로 만드는 것이다.

이미지 분할의 결과물은 전체 이미지를 모두 포함하는 부분 (segments) 들의 집합 혹은 이미지로부터 추출한 윤곽선들의 집합이다. 오른쪽 결과물은 SLIC (Simple Linear Iterative Clustering)\[29\] 기법을 이용하여 이미지를 분할한 결과물로, k-평균 알고리즘을 기반으로 한 이미지 분할 기법이다. 이미지 분할을 통해 이미지 내 비슷한 색상 및 위치에 있는 픽셀들 끼리 하나의 부분 (segment) 로 묶을 수 있고, 이를 통해 이미지를 크게 단순화할 수 있다.

### 벡터 양자화

k-평균 알고리즘은 신호 처리 분야에서 나온 것이며, 여전히 그 분야에서 사용되고 있다. 예를 들어 [컴퓨터 그래픽스](../Page/컴퓨터_그래픽스.md "wikilink") 분야에서는, 색상 양자화를 하는데 k-평균 알고리즘이 사용된다. 색상 양자화는 이미지에 사용된 색의 종류를 k개의 색으로 줄이는 과정이다. 예를 들어, 원래 색상이 65536개의 스펙트럼으로 이루어져 있다고 가정할 때, 이것을 256개 씩 묶게 되면 256개의 색상 스펙트럼으로 줄일 수 있는 것이다. [frame](https://ko.wikipedia.org/wiki/파일:Spatial_color_quantization_-_rainbow,_4_colors.png "wikilink")

### 클러스터 분석

클러스터 분석 시, k-평균 알고리즘은 입력 데이터를 k개의 파티션 (클러스터) 으로 나누는 데 사용될 수 있다. 그러나 순수 k-평균 알고리즘은 사용에 있어 적용성이 떨어진다. 위의 한계점에서 다루었듯이 k 값을 정하기 어렵고, 비 수치 데이터를 입력으로 받았을 때나 임의의 거리 측도를 이용해야 할 때는 사용될 수 없다. 이러한 경우에는 일반적으로 k-평균 알고리즘 이외의 다른 알고리즘을 사용한다.

## 다른 통계 기반 기계 학습 알고리즘간의 관계

### EM 알고리즘

[가우시안](https://ko.wikipedia.org/wiki/가우시안_분포 "wikilink") [혼합 모델을](../Page/혼합_모델.md "wikilink") 이용한 [EM 알고리즘 (기댓값 최대화 알고리즘)](../Page/기댓값_최대화_알고리즘.md "wikilink") 과 k-평균 알고리즘을 비교했을 때 이 둘은 밀접한 연관성을 가지고 있다.\[30\] k-평균 알고리즘은 각 데이터 오브젝트를 클러스터에 강하게 결속시킨다. 다시 말해, 데이터 오브젝트는 오로지 하나의 클러스터에만 속하게 되는데, 이를 hard assignment라고 한다. 반면에, EM 알고리즘은 데이터 오브젝트를 클러스터링할 때 클러스터에의 소속 여부를 해당 클러스터에서 데이터 오브젝트가 나타날 확률값으로 표현한다. 즉, 데이터 오브젝트들이 k-평균 알고리즘과 다르게 어느 한 클러스터에만 결속되지 않게 된다. 이러한 클러스터링 방식을 soft assignment라고 한다. [섬네일을](https://ko.wikipedia.org/wiki/파일:ClusterAnalysis_Mouse.svg "wikilink") 맨 왼쪽의 데이터셋 "mouse" 에 적용한 결과. k-평균 알고리즘은 같은 크기의 클러스터를 만드는 것을 선호하므로, 가운데와 같이 좋지 못한 결과를 낸다. 그러나 가우시안 혼합 모델을 사용한 EM 알고리즘은 분산값도 조정을 하기 때문에, k-평균 알고리즘보다 좋은 결과를 보여준다.\]\] 공분산 행렬을 [단위 행렬 (identity matrix)에](https://ko.wikipedia.org/wiki/단위_행렬 "wikilink") ε을 곱한 (εΙ) 가우시안 혼합 모델을 가정해보자. 이 때 ε은 분산값을 조절하는 파라미터로, 모든 식의 구성요소가 공유한다. 그렇다면 가우시안 혼합 모델이 주어졌을 때 데이터 오브젝트가 나타날 우도 확률은 아래와 같이 주어진다.

<center>

\(P(\mathbf{x}\vert\boldsymbol{\mu}_k, \boldsymbol{\sigma}_k) = \frac{1}{(2\pi\epsilon)^{M/2}}\exp \left\{-\frac{1}{2\epsilon} \left\| \mathbf x - \boldsymbol\mu_k \right\|^2\right\}\)

</center>

이 식에서 EM 알고리즘을 k 개의 가우시안 혼합 모델에 적용할 때, ε값을 추정해야 할 값으로 보지 않고 고정된 값으로 만들자. 한편, 데이터 오브젝트 \(\mathbf{x}_n\)에 대한 가우시안 혼합 모델에서의 사후 확률은 아래와 같이 주어진다.

<center>

\(\gamma(z_{nk}) = \frac{{\pi}_k\exp\left\{-\left\| \mathbf x_n - \boldsymbol\mu_k \right\|^2/{2\epsilon} \right\}}{\sum_{j}{\pi}_j\exp\left\{-\left\| \mathbf x_n - \boldsymbol\mu_j \right\|^2/{2\epsilon} \right\}}\)

</center>

만약 ε값을 0에 근접시키면, 분모의 \(\left\| \mathbf x_n - \boldsymbol\mu_j \right\|^2\)가 가장 작을 때, 0으로 가장 천천히 근접해갈 것이다. 따라서, 그 경우에 데이터 오브젝트 \(\mathbf{x}_n\)의 사후 확률값 \(\gamma(z_{nk})\)은 j값 이외의 경우 모두 0으로 근접하게 된다. 즉, \(\frac{\infty}{\infty}\)에서 분모에 데이터 오브젝트로부터 가장 가까운 평균값일때만 1이 되고, 그 이외의 경우는 0이 되는 것이다. 결과적으로, 데이터 오브젝트의 사후 확률은 하나의 클러스터에만 1의 값을 가지고, 나머지 클러스터에서는 0의 값을 가지게 된다. 따라서, 데이터 오브젝트 들은 가장 가까운 평균점에 hard-clustering이 되고, 이는 k-평균 알고리즘의 결과와 일치한다. 참고로, k-평균 알고리즘에서 클러스터 설정 과정은 EM 알고리즘에서의 E-step에 해당하고, 클러스터 중심 재조정 과정은 M-step에 해당한다.

### 평균점 이동 클러스터링

기본적인 평균점 이동 클러스터링 (mean-shift clustering) 알고리즘은 [비모수적인](https://ko.wikipedia.org/wiki/비모수_통계 "wikilink") 클러스터링 방법으로, 데이터 오브젝트들의 분포에서 그 밀도가 가장 높은 곳 ([mode - 최빈값](https://ko.wikipedia.org/wiki/최빈값 "wikilink")) 을 찾는 방식으로 그룹화를 수행한다. 간단히 설명하자면, 이 알고리즘은 각 데이터 오브젝트에서 미리 지정된 크기의 윈도우 이내의 데이터 오브젝트들을 찾고, 윈도우 내의 평균 값을 구한다. 그리고, 다시 그 평균값에서 같은 크기의 윈도우 이내의 데이터 오브젝트들을 찾고, 윈도우 내의 평균 값을 구한다. 이 방식을 계속하면 데이터 오브젝트들의 지역 밀도가 최대인 곳에서 윈도우의 움직임이 멈추게 된다. 이곳이 데이터 오브젝트 밀도의 지역 최댓값 (최빈값) 이다. 이런 방식으로 모든 데이터 오브젝트에 대해 지역 최댓값을 알아낸다. 이 때, 같은 최빈값으로 수렴한 데이터 오브젝트는 같은 클러스터로 간주하고, 한 클러스터로 묶어준다. 평균점 이동 클러스터링은 k-평균 알고리즘과 다르게 k값을 필요로 하지 않는다는 장점이 있다. 하지만 모든 데이터 오브젝트로부터 무게 중심 이동 과정을 수렴할 때 까지 거쳐야 하므로 k-평균 알고리즘보다 수행 시간이 훨씬 오래 걸린다. 참고로, 평균점 이동 클러스터링은 컴퓨터 비전 및 이미지 프로세싱 분야에서 주로 사용되며, 이미지 분할, 객체 추적 등에 이용된다.

## 의사 코드\[31\]

k-평균 알고리즘 메인 함수 <span style="font-family: Courier;">

<span style="color: blue;">`def`</span>` kmeans(dataSet, k):`
`   `<span style="color: green;">`# Initialize centroids randomly`</span>
`   numFeatures = dataSet.getNumFeatures()`
`   centroids = getRandomCentroids(numFeatures, k)`

`   `<span style="color: green;">`# Initialize book keeping vars.`</span>
`   iterations = 0`
`   oldCentroids = None`

`   `<span style="color: green;">`# Run the main k-means algorithm`</span>
`   `<span style="color: blue;">`while not`</span>` shouldStop(oldCentroids, centroids, iterations):`
`       `<span style="color: green;">`# Save old centroids for convergence test. Book keeping.`</span>
`       oldCentroids = centroids`
`       iterations += 1`

`       `<span style="color: green;">`# Assign labels to each datapoint based on centroids`</span>
`       labels = getLabels(dataSet, centroids)`

`       `<span style="color: green;">`# Assign centroids based on datapoint labels`</span>
`       centroids = getCentroids(dataSet, labels, k)`

`   `<span style="color: green;">`# We can get the labels too by calling getLabels(dataSet, centroids)`</span>
`   `<span style="color: blue;">`return`</span>` centroids`

</span>

k-평균 종료 조건 만족 여부 함수 <span style="font-family: Courier;">

<span style="color: blue;">`def`</span>` shouldStop(oldCentroids, centroids, iterations):`
`   if iterations > MAX_ITERATIONS: return True`
`   `<span style="color: blue;">`return`</span>` oldCentroids == centroids`

</span>

클러스터 설정 함수 <span style="font-family: Courier;">

<span style="color: blue;">`def`</span>` getLabels(dataSet, centroids):`
`  dataSet.label = reassignToNearestCentroid(dataSet, centroids)`
`  `<span style="color: blue;">`return`</span>` dataSet.label`

</span>

중심점 재계산 함수 <span style="font-family: Courier;">

<span style="color: blue;">`def`</span>` getCentroids(dataSet, labels, k):`
`   newCentroids = computeCentroids(dataSet, labels, k)`
`   `<span style="color: blue;">`return`</span>` newCentroids`

</span>

## 변형

### k-평균++

k-평균 클러스터링은 초기 값을 어떻게 선택 하는가에 성능이 따라 크게 달라지는 성질을 가지고 있다. 2007년 David Arthur와 Sergei Vassilvitskii은 이러한 성질로 인한 피해를 줄이기 위해 [k-평균++](https://ko.wikipedia.org/wiki/k-평균++ "wikilink") 을 제안하였다.\[32\] k-평균++ 알고리즘은 k-평균 클러스링 알고리즘의 초기 값을 선택하는 알고리즘이다.

<table>
<tbody>
<tr class="odd">
<td><ol>
<li>데이터 집합으로부터 임의의 데이터를 하나 선택하여 첫 번째 중심으로 설정한다.</li>
<li><em>k</em>개의 중심이 선택될 때 까지 다음의 단계를 반복한다.
<ol>
<li>데이터 집합의 각 데이터에 대해서, 해당 데이터와 선택된 중심점들 중 가장 가까운 중심과의 거리 <strong>D(x)</strong>를 계산한다.</li>
<li>확률이 <strong>D(x)</strong>^2에 비례하는 편중 확률 분포를 사용하여 임의의 데이터를 선택한 후, <em>n</em>번째 중심으로 설정한다.</li>
</ol></li>
<li>선택된 <em>k</em>개의 중심들을 초기 값으로 하여 k-평균 클러스터링을 수행한다.</li>
</ol></td>
</tr>
</tbody>
</table>

k-평균++ 알고리즘은 초기 값을 설정하기 위해 추가적인 시간을 필요로 하지만, 이후 선택된 초기 값은 이후 k-평균 알고리즘이 \(O(log k)\)의 시간 동안 최적 k-평균 해를 찾는 것을 보장한다. 일반적으로 [데이터 마이닝에서](../Page/데이터_마이닝.md "wikilink") 사용된다.

### k-중간점

[k-중간점](https://ko.wikipedia.org/wiki/k-중간점 "wikilink") 은 클러스터의 무게중심을 구하기 위해 데이터의 [평균](../Page/평균.md "wikilink") 대신 [중간점](https://ko.wikipedia.org/wiki/중간점 "wikilink")을 사용하며, k-평균 알고리즘과 다르게 [유클리드 거리뿐](https://ko.wikipedia.org/wiki/유클리드_거리 "wikilink") 아니라 임의의 거리 함수에 대해서도 동작한다. k-중간점 알고리즘은 1987년 Kaufman과 Rousseeuw에 의해 고안되었다.\[33\] 가장 일반적인 예로 중간점 주변 분할 알고리즘이 있다.

<table>
<tbody>
<tr class="odd">
<td><ol>
<li>데이터 집합으로부터 임의의 <em>k</em>개의 데이터를 선택하여 중간점(medoid)로 설정한다.</li>
<li>선택된 중간점들이 바뀌지 않을 때 까지 다음의 단계를 반복한다.
<ol>
<li>선택되지 않은 데이터들을 가장 가까운 중간점과 묶는다. 이때 <a href="https://ko.wikipedia.org/wiki/유클리드_거리" title="wikilink">유클리드 거리</a> 뿐 아니라 다른 거리 함수도 사용 가능하다.</li>
<li>선택되지 않은 각 데이터들에 대해, 해당 데이터를 자신이 포함된 집합의 새로운 중간점으로 가정하여 거리 비용을 계산한다.</li>
<li>기존의 중간점들에 대한 거리 비용과 새로 제안된 중간점들에 대한 거리 비용을 비교하여, 비용이 낮아질 경우 중간점을 교체한다.</li>
</ol></li>
</ol></td>
</tr>
</tbody>
</table>

k-중간점 알고리즘의 경우 데이터 간의 거리를 계산하기 위해 대부분의 시간을 소비한다. 때문에 데이터간 거리 값을 미리 계산하여 저장하거나 [휴리스틱 기법등을](https://ko.wikipedia.org/wiki/휴리스틱_기법 "wikilink") 이용하여 알고리즘의 속도를 빠르게 할 수 있다.\[34\]

### k-중앙값 클러스터링

[k-중앙값 클러스터링](https://ko.wikipedia.org/wiki/k-중앙값_클러스터링 "wikilink")\[35\]\[36\] 은 각 클러스터의 무게중심을 구하기 위해 [평균](../Page/평균.md "wikilink")을 사용하는 대신 [중앙값](../Page/중앙값.md "wikilink")을 사용한다. [\(L_2\) 거리를](https://ko.wikipedia.org/wiki/유클리드_거리 "wikilink") 최소화하는 k-평균과는 달리, k-중앙값 클러스터링은 [\(L_1\) 거리를](../Page/맨해튼_거리.md "wikilink") 최소화 한다.

### 퍼지 C-평균 클러스터링

[퍼지 C-평균 클러스터링](https://ko.wikipedia.org/wiki/퍼지_클러스터링 "wikilink") 의 경우 k-평균 알고리즘과는 다르게 각 점이 완전히 하나의 클러스터에 속하는 것이 아니라, 해당 클러스터에 속한 정도를 나타내는 수치를 갖는다. 그러므로 각 클러스터의 무게중심은 해당 클러스터에 속한 정도를 비중두어 모든 점들의 평균을 계산한 값이 된다.\[37\]

<table>
<tbody>
<tr class="odd">
<td><ol>
<li>각 데이터에 대해 편중 계수를 임의의 값으로 초기화 한다.</li>
<li>계산된 편중 계수의 변화가 주어진 <span class="math inline"><em>ε</em></span>보다 작을 때 까지 다음 단계를 반복한다.
<ol>
<li>계산된 편중 값을 적용하여 각 클러스터의 무게중심을 계산한다.</li>
<li>데이터가 각 클러스터에 속한 정도를 계산하여 새로운 편중 계수로 설정한다.</li>
</ol></li>
</ol></td>
</tr>
</tbody>
</table>

퍼지 C-평균 클러스터링은 k-평균 알고리즘의 완화 버전(soft version)이라고 할 수 있다.

## 참고 문헌

  - [D. Arthur](https://web.archive.org/web/20060902143345/http://www.stanford.edu/~darthur/), [S. Vassilvitskii](https://web.archive.org/web/20060830055220/http://www.stanford.edu/~sergeiv/) (2006): "How Slow is the k-means Method?," Proceedings of the 2006 Symposium on Computational Geometry (SoCG).
  - H.-H. Bock (2007) : " [Clutering Methods: A History of k-Means Algorithms](http://link.springer.com/chapter/10.1007%2F978-3-540-73560-1_15#page-1)", Proceedings of Selected Contributions in Data Analysis and Classification, 2:161-172
  - Han Jiawei, Jian Pei and Micheline Kamber (2012). 《Data Mining: Concepts and Tech-niques》. Morgan Kaufmann
  - Bishop, C. M. (2006). Pattern recognition and machine learning (Vol. 4, No. 4, p. 12). New York: Springer.
  - [Six methods for determining an optimal k value for k-means analysis](http://stackoverflow.com/a/15376462/1036500)

## 각주

## 외부 링크

  - [Numerical Example of K means clustering](http://people.revoledu.com/kardi/tutorial/kMean/NumericalExample.htm)

[분류:알고리즘](https://ko.wikipedia.org/wiki/분류:알고리즘 "wikilink") [분류:기계 학습](https://ko.wikipedia.org/wiki/분류:기계_학습 "wikilink")

1.
2.
3.   Published in journal much later:
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
17.
18.
19.
20.
21.
22.
23.  see especially Figure 14 and appendix.
24.
25.
26.
27.
28.
29. Achanta, R., Shaji, A., Smith, K., Lucchi, A., Fua, P., & Süsstrunk, S. (2010). Slic superpixels (No. EPFL-REPORT-149300)
30. Bishop, C. M. (2006). Pattern recognition and machine learning (Vol. 4, No. 4, p. 12). New York: springer.
31. <http://stanford.edu/~cpiech/cs221/handouts/kmeans.html>
32.
33.
34.
35.
36.
37.