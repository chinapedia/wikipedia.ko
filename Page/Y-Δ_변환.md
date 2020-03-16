> This article is converted from Wikipedia: [Y- ](https://ko.wikipedia.org/wiki/Y-_).


**Y-Δ 변환**(Y-Δ transform, wye-delta transform) 또는 **T-Π 변환**(T-Π transform, star-pi transform)은 [전기 회로](../Page/전기_회로.md "wikilink") 분석을 간단하게 할 수 있는 수학적 기술 중 하나이다. 이 변환의 이름은 분석하고자 하는 [회로도](../Page/회로도.md "wikilink") 모양이 각각 알파벳 Y와 [그리스 문자](../Page/그리스_문자.md "wikilink") [Δ](../Page/Δ.md "wikilink")(델타)로 보인 것에서 따왔다. 이 회로 변환은 1899년 [아서 에드윈 케넬리가](https://ko.wikipedia.org/wiki/아서_에드윈_케넬리 "wikilink") 처음 발표하였다.\[1\] 이 변환은 오늘날 [3상전력](../Page/3상전력.md "wikilink") 회로 분석에서 광범위하게 사용된다.

Y-Δ 변환은 3개의 [저항기](../Page/저항기.md "wikilink")가 달린, [스타-매쉬 변환의](https://ko.wikipedia.org/wiki/스타-매쉬_변환 "wikilink") 특수해라고 볼 수도 있다. 수학에서 Y-Δ 변환은 [평면 그래프](../Page/평면_그래프.md "wikilink") 이론 해석에서 중요한 역할을 한다.\[2\]

## 명칭

[섬네일](https://ko.wikipedia.org/wiki/파일:Theoreme_de_kennelly2.svg "wikilink") Y-Δ 변환은 많은 다른 이름으로도 알려져 있는데, 주로 2가지 모양을 따와서 이름이 붙여있다. 하나는 **Y**를 **T**(또는 star)로 바꿔 부르거나, **Δ**(델타)를 삼각형 또는 **[Π](../Page/Π.md "wikilink")**(그리스 문자 파이), 매쉬로 바꿔서 부르기도 한다. 보통은 이 변환 이름을 와이-델타, 델타-와이, 티-파이, 파이-티 변환 4가지로 부른다.

## 기초 변환

[right](https://ko.wikipedia.org/wiki/파일:Wye-delta-2.svg "wikilink") 이 변환은 3개의 선으로 연결된 서로 다른 모양의 회로망이 실제로는 같은 것임을 보여준다. 3개의 말단부 공통 노드에 전력을 공급하는 능동소자가 하나도 없을 경우, 임피던스 변환을 통해 노드를 없앨 수 있다. 회로가 등가임을 보이기 위하여 두 회로망의 양 끝단 사이 총 임피던스는 항상 같아야 한다. 여기에 주어진 방정식은 실제로 복잡한 임피던스일 경우에도 해당된다.

### Δ에서 Y로의 변환

Y 회로의 양단 임피던스 \(R_y\)은 Δ 회로에서의 인접 노드로의 임피던스 \(R'\), \(R''\)를 이용하여 다음과 같이 나타낼 수 있다.

\[R_y = \frac{R'R''}{\sum R_\Delta}\]

여기서 \(R_\Delta\)는 Δ 회로에서의 모든 임피던스이다. 이 식을 통하여 각각의 임피던스를 구하면 다음과 같다.

\[\begin{align}
  R_1 &= \frac{R_bR_c}{R_a + R_b + R_c} \\
  R_2 &= \frac{R_aR_c}{R_a + R_b + R_c} \\
  R_3 &= \frac{R_aR_b}{R_a + R_b + R_c}
\end{align}\]

### Y에서 Δ로의 변환

Δ 회로에서 임피던스 \(R_\Delta\)를 구하는 식은 다음과 같다.

\[R_\Delta = \frac{R_P}{R_\mathrm{opposite}}\]

여기서 \(R_P = R_1R_2+R_2R_3+R_3R_1\)은 Y 회로에서 모든 임피던스 쌍의 곱의 합이며, \(R_\mathrm{opposite}\)는 \(R_\Delta\)와 정 반대에 있는 양 끝단의 Y 회로의 노드 임피던스이다. 이를 통해 구한 각각의 모서리의 임피던스는 다음과 같다.

\[\begin{align}
  R_a &= \frac{R_1R_2 + R_2R_3 + R_3R_1}{R_1} \\
  R_b &= \frac{R_1R_2 + R_2R_3 + R_3R_1}{R_2} \\
  R_c &= \frac{R_1R_2 + R_2R_3 + R_3R_1}{R_3}
\end{align}\]

## 변환의 존재성과 유일성 증명

이 변환의 존재성은 [회로 이론의 중첩 정리를](https://ko.wikipedia.org/wiki/중첩_정리 "wikilink") 통해 보일 수 있다. 더욱 일반화한 [스타-매쉬 변환에서](https://ko.wikipedia.org/wiki/스타-매쉬_변환 "wikilink") 유도하는 것 보다는 더 짧게 증명할 수 있다. 두 회로가 동등함은 3개 노드(\(N_1, N_2, N_3\))의 외부 전압(\(V_1, V_2, V_3\))과 그에 대응하는 전류(\(I_1, I_2, I_3\))가 Y 회로에서 Δ 회로로, 또는 그 반대로 넘어가도 같음을 보여 증명할 수 있다. 이 증명을 위하여 노드에 주어진 외부 전류를 통해 이를 계산할 것이다. 중첩정리에 따르면, 3개 노드의 전류를 이용하여 3가지 노드 방정식에서 전압의 선형 합을 통해 총 전압을 구할 수 있다.

  -
    (1) \((I_1-I_2)/3, -(I_1-I_2)/3, 0\)

<!-- end list -->

  -
    (2) \(0,(I_2-I_3)/3,-(I_2-I_3)/3\)

<!-- end list -->

  -
    (3) \(-(I_3-I_1)/3, 0, (I_3-I_1)/3\)

여기서 [키르히호프의 전기회로 법칙에](../Page/키르히호프의_전기회로_법칙.md "wikilink") 따라 \(I_1+I_2+I_3=0\)이다. 이 회로망에는 이상 전류원이 하나만 있기 때문에 각 방정식을 푸는 것은 간단하다. 각 상황에서 양 노드의 전압이 서로 동일하게 될려면 두 회로의 등가저항이 같아야 하는데, 이는 [직렬 회로와 병렬 회로의](https://ko.wikipedia.org/wiki/직렬_회로와_병렬_회로 "wikilink") 기초 법칙을 이용해 증명할 수 있다.

\[R_3+R_1 = \frac{(R_c+R_a)R_b}{R_a + R_b + R_c},\] \(\frac{R_3}{R_1} = \frac{R_a}{R_c}.\)

6개의 방정식은 3개의 다른 변수 \(R_a,R_b,R_c\)로 알고자 하는 변수 \(R_1,R_2,R_3\)를 나타내기 충분하나, 이 방정식이 실제 위에 나타낸 것처럼 나타낼 수 있다는 걸 보이는 건 간단하다. 실제로, 중첩정리를 통하여 저항 값 사이의 관계를 보일 수 있을 뿐 아니라, 이 해가 유일함도 보장한다.

## 회로망의 간단화

2개의 단말부가 있는 저항 회로는 이론적으로 1개의 등가저항을 가진 회로로 [간단하게 변환할](https://ko.wikipedia.org/wiki/등가_임피던스_변환 "wikilink") 수 있다. 직렬 및 병렬 변환은 간단화를 위한 가장 기초적인 도구이나 이 문서에 쓰여 있는 브릿지와 같은 복잡한 회로에는 적용하기 어렵다.

Y-Δ 변환을 이용하여 아래의 그림과 같이 한번에 1개의 노드를 없애고 더 간단한 회로망을 만들 수 있다.

[center](https://ko.wikipedia.org/wiki/파일:wye-delta_bridge_simplification.svg "wikilink")

노드를 추가하는 Δ-Y 변환 같은 경우에는 직병렬 등으로 더욱 회로 선을 단순화할 수 있도록 해준다.

[center](https://ko.wikipedia.org/wiki/파일:delta-wye_bridge_simplification.svg "wikilink")

[평면 그래프](../Page/평면_그래프.md "wikilink") 모양의 모든 2극 회로망은 직병렬 변환,Δ-Y 변환, Y-Δ 변환을 이용하여 하나의 단일 등가저항을 가진 회로로 바꿀 수 있다.\[3\] 하지만, [원환면](../Page/원환면.md "wikilink") 모양으로 정사각형 회로가 서로 이어져 있는 형태이거나, [페테르센 족](https://ko.wikipedia.org/wiki/페테르센_족 "wikilink") 모양과 같이 평면이 아닌 모양의 회로망은 Y-Δ 변환을 사용할 수 없다.

## 그래프 이론

[그래프 이론에서](../Page/그래프_이론.md "wikilink") Y-Δ 변환이란 한 그래프 내의 Y [부분 그래프를](../Page/부분_그래프.md "wikilink") 등가의 Δ 부분 그래프로 변환하는 작업을 의미한다. 이 변환은 그래프의 변 수는 그대로이나, 꼭짓점의 수나 [순환의](../Page/순환_\(그래프_이론\).md "wikilink") 수는 달라질 수 있다. 두 그래프가 한 그래프에서 Y-Δ 변환을 통해 다른 그래프로 모양을 바꿀 수 있다면 이 두 그래프는 **Y-Δ 등가**라고 부른다. 예를 들어, [페테르센 족은](https://ko.wikipedia.org/wiki/페테르센_족 "wikilink") Y-Δ [동치관계](../Page/동치관계.md "wikilink")이다.

## 예시

### Δ에서 Y로의 변환

[right](https://ko.wikipedia.org/wiki/파일:Wye-delta-2.svg "wikilink")

Δ 회로에서의 \(\{R_a, R_b, R_c\}\)를 Y 회로의 \(\{R_1,R_2,R_3\}\)로 바꾸기 위해, 두 회로에 대응되는 임피던스를 비교하자. 어느 회로에서든 임피던스는 회로에서 노드 중 하나가 끊어진 것과 같이 생각한 상태에서 결정된다.

Δ 회로에서 *N*<sub>3</sub>이 끊어진 상태에서 *N*<sub>1</sub>과 *N*<sub>2</sub> 사이의 임피던스는 다음과 같다.

\[\begin{align}
  R_\Delta(N_1, N_2) &= R_c \parallel (R_a + R_b) \\
                     &= \frac{1}{\frac{1}{R_c} + \frac{1}{R_a + R_b}} \\
                     &= \frac{R_c(R_a + R_b)}{R_a + R_b + R_c}
\end{align}\]

식을 간단하게 하기 위해, \(\{R_a, R_b, R_c\}\)를 \(R_T\)라고 정의하자.

\[R_T = R_a + R_b + R_c\]

따라서,

\[R_\Delta(N_1, N_2) = \frac{R_c(R_a+R_b)}{R_T}\]

Y 회로에서 N<sub>1</sub>과 N<sub>2</sub> 사이에 대응되는 임피던스를 구하는 법은 간단하다.

\[R_Y(N_1, N_2) = R_1 + R_2\]

그러므로,

\[R_1+R_2 = \frac{R_c(R_a+R_b)}{R_T}\]   (1)

위의 계산식을 통하여, \(R(N_2,N_3)\)의 값은 다음과 같다.

\[R_2+R_3 = \frac{R_a(R_b+R_c)}{R_T}\]   (2)

\(R(N_1,N_3)\)의 값은 다음과 같다.

\[R_1+R_3 = \frac{R_b(R_a+R_c)}{R_T}.\]   (3)

여기서, 위 3개 방정식의 선형 계산(더하기/빼기)을 통하여 \(\{R_1,R_2,R_3\}\)를 구할 수 있다.

예를 들어, (1) 식과 (3) 식을 더한 후 (2) 식을 빼면 다음과 같다.

\[R_1+R_2+R_1+R_3-R_2-R_3 =
  \frac{R_c(R_a+R_b)}{R_T}
+ \frac{R_b(R_a+R_c)}{R_T}
- \frac{R_a(R_b+R_c)}{R_T}\]

\[2R_1 = \frac{2R_bR_c}{R_T}\]

따라서,

\[R_1 = \frac{R_bR_c}{R_T}.\]

여기서, \(R_T = R_a + R_b + R_c\)이다.

식을 정리하면 다음과 같다.

\[R_1 = \frac{R_bR_c}{R_T}\] (4)

\[R_2 = \frac{R_aR_c}{R_T}\] (5)

\[R_3 = \frac{R_aR_b}{R_T}\] (6)

### Y에서 Δ로의 변환

식을 간단하게 하기 위해 다음과 같은 가정을 하자.

\[R_T = R_a+R_b+R_c\].

여기서 우리는 Δ 회로에서 Y 회로로 변환하는 방정식을 다음과 같이 세울 수 있다.

\[R_1 = \frac{R_bR_c}{R_T}\]   (1)

\[R_2 = \frac{R_aR_c}{R_T}\]   (2)

\[R_3 = \frac{R_aR_b}{R_T}.\]   (3)

3개 방정식을 두개씩 묶어 서로 곱해주면 다음과 같다.

\[R_1R_2 = \frac{R_aR_bR_c^2}{R_T^2}\]   (4)

\[R_1R_3 = \frac{R_aR_b^2R_c}{R_T^2}\]   (5)

\[R_2R_3 = \frac{R_a^2R_bR_c}{R_T^2}\]   (6)

여기서, 3개 방정식을 다 더하면 다음과 같다.

\[R_1R_2 + R_1R_3 + R_2R_3 = \frac{R_aR_bR_c^2 + R_aR_b^2R_c + R_a^2R_bR_c}{R_T^2}\]   (7)

여기서 우변 분자의 \(R_aR_bR_c\)를 묶어서 \(R_T\)를 밖으로 빼면 분모의 \(R_T\)와 나눌 수 있다.

\[R_1R_2 + R_1R_3 + R_2R_3 = \frac{(R_aR_bR_c)(R_a+R_b+R_c)}{R_T^2}\]

\[R_1R_2 + R_1R_3 + R_2R_3 = \frac{R_aR_bR_c}{R_T}\] (8)

(8)의 식과 {(1),(2),(3)} 식은 서로 유사하다.

(8)을 (1)로 나누면 다음과 같다.

\[\frac{R_1R_2 + R_1R_3 + R_2R_3}{R_1} = \frac{R_aR_bR_c}{R_T}\frac{R_T}{R_bR_c},\]

\[\frac{R_1R_2 + R_1R_3 + R_2R_3}{R_1} = R_a,\]

이 식은 \(R_a\) 값에 대한 식이다. (8) 식을 (2)나 (3)으로 나누면 \(R_b\)와 \(R_c\)를 구할 수 있다.

## 더 보기

  - [스타-매쉬 변환](https://ko.wikipedia.org/wiki/스타-매쉬_변환 "wikilink")
  - [회로 이론](../Page/회로_이론.md "wikilink")
  - [전기 회로](../Page/전기_회로.md "wikilink"), [단상 전력](https://ko.wikipedia.org/wiki/단상_전력 "wikilink"), [교류](../Page/교류.md "wikilink"), [3상전력](../Page/3상전력.md "wikilink"), [다상 시스템](https://ko.wikipedia.org/wiki/다상_시스템 "wikilink")
  - [교류 전동기](https://ko.wikipedia.org/wiki/교류전동기 "wikilink")
  - [니콜라 테슬라](../Page/니콜라_테슬라.md "wikilink")
  - [존 홉킨슨](https://ko.wikipedia.org/wiki/존_홉킨슨 "wikilink")
  - [미하일 돌리보도브로볼스키](https://ko.wikipedia.org/wiki/미하일_돌리보도브로볼스키 "wikilink")
  - [찰스 프로테우스 스타인메츠](https://ko.wikipedia.org/wiki/찰스_프로테우스_스타인메츠 "wikilink")

## 각주

## 참고 문헌

  - William Stevenson, *Elements of Power System Analysis* 3rd ed., McGraw Hill, New York, 1975,

## 외부 링크

  - [Star-Triangle Conversion](http://www.designcabana.com/knowledge/electrical/basics/resistors): Knowledge on resistive networks and resistors
  - [Calculator of Star-Triangle transform](http://www.elektro-energetika.cz/calculations/transfigurace.php?language=english)

[분류:전기 회로](https://ko.wikipedia.org/wiki/분류:전기_회로 "wikilink") [분류:회로 정리](https://ko.wikipedia.org/wiki/분류:회로_정리 "wikilink")

1.  A.E. Kennelly, "Equivalence of triangles and three-pointed stars in conducting networks", *Electrical World and Engineer*, vol. 34, pp. 413–414, 1899.
2.  E.B. Curtis, D. Ingerman, J.A. Morrow, [Circular planar graphs and resistor networks](http://www.sciencedirect.com/science/article/pii/S0024379598100873), *Linear Algebra and its Applications*, vol. 238, pp. 115–150, 1998.
3.  Klaus Truemper. [On the delta-wye reduction for planar graphs](http://onlinelibrary.wiley.com/doi/10.1002/jgt.3190130202/abstract). *J. Graph Theory* 13(2):141–148, 1989.