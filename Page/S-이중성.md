> This article is converted from Wikipedia: [S-이중성](https://ko.wikipedia.org/wiki/S-이중성).


[이론물리학](https://ko.wikipedia.org/wiki/이론물리학 "wikilink")에서, **S-이중성**(S-二重性, )은 서로 다른 듯한 두 물리 이론이 [결합 상수의](../Page/결합_상수.md "wikilink") [역수](https://ko.wikipedia.org/wiki/역수 "wikilink")를 취하는 변환에 의하여 서로 동등한 현상이다. 즉, 결합 상수가 작은 한 이론은 결합 상수가 큰 다른 이론과 동등하게 된다. [양자장론](../Page/양자장론.md "wikilink")과 [끈 이론에서](../Page/끈_이론.md "wikilink") 나타난다.

## 양자장론의 S-이중성

양자장론에서는 여러 가지의 S-이중성을 찾을 수 있다. 이들은 대부분 일종의 [초대칭](../Page/초대칭.md "wikilink")을 가정하며, 궁극적으로 [초끈 이론의](../Page/초끈_이론.md "wikilink") S-이중성에서 비롯된다.

### 전기-자기 이중성

S-이중성의 가장 기본적인 형태는 [맥스웰 방정식의](../Page/맥스웰_방정식.md "wikilink") **전기-자기 이중성**(電氣磁氣二重性, )이다. 대전 입자를 포함하지 않는 [맥스웰 방정식은](../Page/맥스웰_방정식.md "wikilink") [전기장](../Page/전기장.md "wikilink")과 [자기장](../Page/자기장.md "wikilink")을 치환하여도 동등하다. 여기에 전기적으로 대전된 입자만 추가하면 전기-자기 이중성이 깨지지만, [자기적으로 대전된 입자도](../Page/자기_홀극.md "wikilink") 추가하면 다시 전기-자기 이중성이 성립한다. 여기서 전기적으로만 대전된 입자는 전기 홀극, 자기적으로만 대전된 입자는 [자기 홀극](../Page/자기_홀극.md "wikilink"), 전기와 자기 둘 다 대전된 입자를 **[다이온](https://ko.wikipedia.org/wiki/다이온 "wikilink")**이라고 한다.

부호수가 \((p,4-p)\)인 4차원 다양체 \(M\)를 생각하자. 그 가운데 호몰로지 \(H^2(M)\)에 다음과 같은 연산자 \(N_\tau\colon H^2(M;\mathbb C)\to H^2(M;\mathbb C)\)를 정의하자.

\[N_\tau=\operatorname{Re}\tau+s*\operatorname{Im}\tau\] 여기서 \(p\equiv0\pmod2\)인 경우 \(s=i\), 그렇지 않은 경우 \(s=1\)로 놓는다. 이 경우, \((s*)^2=-1\)이므로, \(N_\tau\)의 역은

\[(N_\tau)^{-1}=N_{1/\tau}\] 이다. 즉, 이러한 꼴의 연산자는 단순히 [복소수](../Page/복소수.md "wikilink")로 생각할 수 있다.

U(1) 게이지 이론은 다음과 같이 기술할 수 있다. U(1) 접속의 곡률을 \(F\)라고 하자. 이는 선다발의 [천 특성류와](../Page/천_특성류.md "wikilink") 같다.

\[c_1=[F/2\pi]\in H^2(M;\mathbb Z)\] 게이지 이론의 [작용을](../Page/작용_\(물리학\).md "wikilink") 다음과 같이 적자.

\[S_\tau=\frac1{4\pi}\int_MF\wedge N_\tau F\] 통상적으로, 그 성분들은

\[\tau=\theta/2\pi+4\pi i/g^2\] 으로 적는다. 여기서

  - \(g\)는 [결합 상수](../Page/결합_상수.md "wikilink")
  - \(\theta\)는 [CP 위반](../Page/CP_위반.md "wikilink") 각

이다. 즉, 텐서 표기법으로 쓰면

\[S=\int_M\sqrt{|\det g|}\,\left(\frac1{2g^2}F_{\mu\nu}F^{\mu\nu}+\frac{\theta}{32\pi^2}\epsilon^{\mu\nu\rho\sigma}F_{\mu\nu}F_{\rho\sigma}\right)\] 이다. 이 작용은

\[F\mapsto F_D=\frac{\delta S}{\delta F}=N_\tau F\]

\[\tau\mapsto-1/\tau\] 에 대하여 불변이다. 이는 고전 전자기학의 전기-자기 이중성이다.

이 이론을 양자화하게 되면, 그 [경로 적분은](https://ko.wikipedia.org/wiki/경로_적분 "wikilink")

\[Z=\int DA\,\exp(iS)\] 이다. 이 경우, \([F/2\pi]\in H^2(M;\mathbb Z)\)이므로,

\[S_{\tau+1}-S_\tau=(\theta/2)\int_M(F/2\pi)\wedge(F/2\pi)\] 이다. 만약 \(M\)이 [스핀 다양체라면](../Page/스핀_다양체.md "wikilink"), 2차 미분형식의 [교차 형식](https://ko.wikipedia.org/wiki/교차_형식 "wikilink")(intersection form)은 짝수이므로, 항상 \(\int_M(F/2\pi)^2\)는 짝수다. 따라서

\[S_{\tau+1}-S_\tau\in\mathbb Z\] 이고, 이 경우 [경로 적분에](https://ko.wikipedia.org/wiki/경로_적분 "wikilink") 등장하는 \(\exp(iS)\)는 불변이다. 즉, 양자역학적으로

\[\tau\mapsto\tau+1\] 또한 대칭이다. 이들을 합성하면 [모듈러 군](../Page/모듈러_군.md "wikilink")

\[\tau\mapsto\frac{a\tau+b}{c\tau+d}\] (\(\begin{pmatrix}a&b\\c&d\end{pmatrix}\in\operatorname{PSL}(2;\mathbb Z)\) 을 이루게 된다. 유클리드 [계량 부호수의](https://ko.wikipedia.org/wiki/계량_부호수 "wikilink") 경우, 이는 구체적으로 [경로 적분을](https://ko.wikipedia.org/wiki/경로_적분 "wikilink") 계산해 확인할 수 있다. [맥스웰 방정식을](../Page/맥스웰_방정식.md "wikilink") 만족시키는 장세기 \(F\)는

\[dF=d*F=0\] 이므로 [조화형식](https://ko.wikipedia.org/wiki/조화형식 "wikilink")(harmonic form)을 이루며, 이는 [호지 이론에](../Page/호지_이론.md "wikilink") 따라 [코호몰로지류](https://ko.wikipedia.org/wiki/코호몰로지류 "wikilink") \(H^2(M;\mathbb R)\)에 대응한다. 유클리드 계량 부호수에서는 2차 형식에 대한 [호지 쌍대가](../Page/호지_쌍대.md "wikilink") \(*^2=1\)이므로, 호지 쌍대의 [고윳값](https://ko.wikipedia.org/wiki/고윳값 "wikilink")에 따라 임의의 장세기를

\[F=2\pi(p_++p_-)\]

\[*F=2\pi(p_++-p_-)\]

\[p_\pm\in H^2_\pm(M;\mathbb Z)\] 로 분해할 수 있다. 그렇다면

\[N_\tau F=2\pi(\tau p_++\bar\tau p_-)\] 이다. 따라서 작용은

\[S=\pi\left(\tau\langle p_+, p_+\rangle-\bar\tau\langle p_-,p_-\rangle\right)\] 가 된다. 따라서, 경로 적분은 다음과 같다.\[1\]\[2\]\[3\]

\[Z(\tau)\sim\sum_{p_+\in H^2_+(M;\mathbb Z)}q^{p_+^2/2}\sum_{p_-\in H_-^2(M;\mathbb Z)}\bar q^{p_-^2/2}\] (\(q=\exp(2\pi i\tau)\)) 이는 서로 다른 [선다발](https://ko.wikipedia.org/wiki/선다발 "wikilink")들의 합만 고려한 것이다. 여기에 유한 에너지 모드들의 기여를 고려하면, 각 모드의 에너지는 \(\operatorname{Im}\tau=1/g^2\)에 비례하며, 경로 적분에는 (에너지 연산자의 행렬식의 제곱근이므로) 각 모드가 \(\sqrt{\operatorname{Im}\tau}\)를 기여한다. 이 인자는 [경로 적분의](https://ko.wikipedia.org/wiki/경로_적분 "wikilink") [측도](../Page/측도.md "wikilink")를 국소적으로 재정의해 없앨 수 있다. 그러나 게이지 고정을 할 경우 상수 게이지 변환은 진동 모드에 영향을 미치지 않으므로 \(\operatorname{Im}\tau)^{-1/2}\)를 곱해야 하고, 또한 \(b_1\) (1차 [베티 수](../Page/베티_수.md "wikilink")) 개의 영에너지 모드는 게이지 변환에 영향을 받지 않으므로 이들은 \((\operatorname{Im}\tau)^{b_1/2}\)를 기여한다. 즉, 총 경로 적분은 다음과 같은 꼴이다.

\[Z(\tau)\sim(\operatorname{Im}\tau)^{(b_1-1)/2}\sum_{p_+\in H^2_+(M;\mathbb Z)}q^{p_+^2/2}\sum_{p_-\in H_-^2(M;\mathbb Z)}\bar q^{p_-^2/2}\] 이는 [세타 함수의](../Page/세타_함수.md "wikilink") 일종이며, 이는 무게가

\[\frac12(\chi-\sigma,\chi+\sigma)\] 인 (비정칙) [모듈러 형식이다](../Page/모듈러_형식.md "wikilink"). 여기서 \(\chi\)는 \(M\)의 [오일러 지표이고](../Page/오일러_지표.md "wikilink"), \(\chi=b_2^+-b_2^-\)는 교차 형식의 부호수이다. 무게가 0이 아닌 경우에는 고전적인 [모듈러 군](../Page/모듈러_군.md "wikilink") 대칭에 [변칙이](../Page/변칙_\(물리학\).md "wikilink") 생기는 것을 알 수 있다.

### 몬토넨-올리브 이중성

4차원에서, [\(\mathcal N=4\) 초대칭을 갖는 비가환 양-밀스 이론에서도](../Page/𝒩=4_초대칭_양-밀스_이론.md "wikilink") 일종의 S-이중성이 성립하는데, 이를 **몬토넨-올리브 이중성**()이라고 한다.\[4\]\[5\]\[6\] 이는 클라우스 몬토넨()과 데이비드 이언 올리브()가 1977년 발견하였다.\[7\]

몬토넨-올리브 이중성은 ⅡB종 [초끈 이론으로](../Page/초끈_이론.md "wikilink") 설명할 수 있다.\[8\]\[9\] \(\mathcal N=4\) \(U(N)\) 양-밀스 이론은 \(N\)개의 겹친 [D3-막들](../Page/D-막.md "wikilink") 위에 존재하는 [유효 이론이다](../Page/유효_이론.md "wikilink"). D3-막에는 [기본 끈](../Page/끈_\(물리학\).md "wikilink")(F-끈)과 [D1-막](../Page/D-막.md "wikilink")(D-끈)이 붙어 있는데, F-끈의 끝은 전기 홀극, D-끈의 끝은 [자기 홀극을](../Page/자기_홀극.md "wikilink") 이룬다. ⅡB종 초끈 이론에서는 S-이중성은 F-끈과 D-끈을 맞바꾸게 되고, 이 이중성은 물론 D3-막의 유효 이론도 따르게 된다. 이 이중성이 몬토넨-올리브 이중성이다.

### 자이베르그 이중성

4차원 \(\mathcal N=1\) [초대칭](../Page/초대칭.md "wikilink") [양-밀스 이론에서도](../Page/양-밀스_이론.md "wikilink") **[자이베르그 이중성](../Page/자이베르그_이중성.md "wikilink")**()이라는 S-이중성이 존재한다.\[10\] 이 경우, 서로 대응하는 두 이론은 일반적으로 똑같지 않지만, 낮은 에너지 눈금에서는 [재규격화군](../Page/재규격화군.md "wikilink") 흐름에 의하여 서로 같아진다. 서로 대응하는 두 이론의 [모듈러스 공간은](https://ko.wikipedia.org/wiki/모듈러스_\(물리학\) "wikilink") 서로 동형이다. [나탄 자이베르그가](../Page/나탄_자이베르그.md "wikilink") 1994년 발견하였다.\[11\]

보다 일반적으로, [맛깔](https://ko.wikipedia.org/wiki/맛깔 "wikilink") 대칭()들을 게이지하면, **이중성 폭포**()라는 일련의 관계들을 얻는다.\[12\]

### 자이베르그-위튼 이론

**[자이베르그-위튼 이론](../Page/자이베르그-위튼_이론.md "wikilink")**()은 \(\mathcal N=2\) 4차원 [초대칭 게이지 이론의](../Page/초대칭_게이지_이론.md "wikilink") 모듈러스 공간()을 다루는 이론이다. [나탄 자이베르그와](../Page/나탄_자이베르그.md "wikilink") [에드워드 위튼이](../Page/에드워드_위튼.md "wikilink") 1994년 발표하였다.\[13\] 이에 따라, 많은 경우 양자 초대칭 게이지 이론의 모듈러스 공간을 정확히 계산할 수 있고, 서로 다른 것처럼 보이는 이론들이 S-이중성에 따라 사실 같은 양자장론임을 알 수 있다.

### 6차원 (2,0) 초등각 장론으로 인한 이중성

[6차원 (2,0) 초등각 장론을](../Page/6차원_\(2,0\)_초등각_장론.md "wikilink") 각종 차원의 다양체에 [콤팩트화](https://ko.wikipedia.org/wiki/콤팩트화 "wikilink")하면, 여러 다양한 S-이중성을 얻는다. 특히, 이를 콤팩트 [리만 곡면에](../Page/리만_곡면.md "wikilink") 축소하면, 4차원 초대칭 게이지 이론의 이중성들의 여러 일반화를 얻는다.

## 끈 이론의 S-이중성

[섬네일들](https://ko.wikipedia.org/wiki/파일:Dualität.svg "wikilink") 사이의 이중성\]\] [초끈 이론들도](../Page/초끈_이론.md "wikilink") S-이중성을 나타낸다.\[14\] ⅡB종 초끈 이론은 스스로에게 대응한다. 즉, [결합 상수](../Page/결합_상수.md "wikilink") \(g\)의 ⅡB종 초끈 이론은 결합 상수 \(1/g\)의 이론과 같다. [Ⅰ종 초끈 이론은](https://ko.wikipedia.org/wiki/Ⅰ종_초끈_이론 "wikilink") SO(32) [잡종 끈 이론과](../Page/잡종_끈_이론.md "wikilink") 대응한다. ⅡA종 초끈 이론과 E<sub>8</sub> 잡종 이론은 [축소화](../Page/축소화.md "wikilink")한 [M이론](../Page/M이론.md "wikilink")에 대응하게 된다.

따라서, 일반적으로 [M이론](../Page/M이론.md "wikilink")의 이중성들의 군은 [T-이중성](../Page/T-이중성.md "wikilink")과 S-이중성들로 생성된다. T-이중성과 S-이중성을 합성한 이중성을 **[U-이중성](../Page/U-이중성.md "wikilink")**이라고 한다.\[15\]

S-이중성 아래, 기본 [끈](../Page/끈_\(물리학\).md "wikilink")(F-끈)은 [D1-막](../Page/D-막.md "wikilink")(D-끈)과 맞바뀌고, [D5-막은](../Page/D-막.md "wikilink") [NS5-막](../Page/NS5-막.md "wikilink")(F5-막)과 맞바뀐다.\[16\]

### Ⅰ종/Spin(32) 잡종 이중성

| Ⅰ종 막                                    | Spin(32) 잡종 막                           |
| --------------------------------------- | --------------------------------------- |
| [기본 끈](../Page/끈_\(물리학\).md "wikilink") | (없음)                                    |
| [D1-막](../Page/D-막.md "wikilink")       | [기본 끈](../Page/끈_\(물리학\).md "wikilink") |
| [D5-막](../Page/D-막.md "wikilink")       | [NS5](../Page/NS5-막.md "wikilink")      |
| D0-막 (非BPS)                             | Spin(32) 스피너 상태 입자 (非BPS)               |

[Ⅰ종 끈 이론의](https://ko.wikipedia.org/wiki/Ⅰ종_끈_이론 "wikilink") [기본 끈은](../Page/끈_\(물리학\).md "wikilink") 다른 끈 이론의 끈과 달리 BPS가 아니어서, 일반적으로 안정하지 않다 (즉, 끊어질 수 있다). 이는 [Ⅰ종 끈 이론은](https://ko.wikipedia.org/wiki/Ⅰ종_끈_이론 "wikilink") [캘브-라몽 장을](../Page/캘브-라몽_장.md "wikilink") 포함하지 아니하므로, 끈이 보존되는 전하에 대하여 대전되어 있지 않기 때문이다. [결합 상수가](../Page/결합_상수.md "wikilink") 작을 경우 끈이 끊어지는 속도가 느려 [섭동 이론을](../Page/섭동_이론.md "wikilink") 전개할 수 있지만, 그 S-이중 이론은 [결합 상수가](../Page/결합_상수.md "wikilink") 큰 경우에 해당하므로 Ⅰ종 끈은 곧 붕괴해 버린다. 반면 Spin(32) 잡종 끈은 BPS이므로 안정하며, I종 이론에서 [D1-막 (D-끈)으로](../Page/D-막.md "wikilink") 존재한다.

#### Spin(32)의 스피너 상태

Spin(32) 잡종 끈 이론의 (기본 끈의) 스펙트럼에는 게이지 군 Spin(32)의 [스피너](../Page/스피너.md "wikilink") 표현으로 변환하는 상태가 존재한다. 이는 질량을 가지며, BPS 상태가 아니지만, Spin(32) 게이지 전하의 보존으로 인하여 이러한 상태 가운데 가장 가벼운 것은 안정하다.

S-이중성에 따라서, [Ⅰ종 끈 이론에도](https://ko.wikipedia.org/wiki/Ⅰ종_끈_이론 "wikilink") 이에 대응하는 안정한 상태가 존재한다. S-이중성의 성질에 의하여 이는 물론 [Ⅰ종 기본 끈의](https://ko.wikipedia.org/wiki/Ⅰ종_기본_끈 "wikilink") 스펙트럼에 등장하지 않는다. ([Ⅰ종 기본 끈의](https://ko.wikipedia.org/wiki/Ⅰ종_기본_끈 "wikilink") 스펙트럼의 모든 상태는 SO(32)의 텐서 표현을 따른다.) 다만, 초중력 근사에서, 이러한 상태는 [호모토피 군](../Page/호모토피_군.md "wikilink")

\[\pi_8(\operatorname{Spin}(32)) \cong \operatorname{Cyc}(2)\] 로서 존재함을 알 수 있다.\[17\] 즉, 9+1차원 시공간 속에서, 입자 주위의 9차원 공간의 등각 무한대인 8차원 초구 \(\mathbb S^8\)를 생각하자. 이 경우 호모토피 군의 존재로 인하여, 무한대에서 위와 같이 위상수학적으로 자명하지 않은 꼴을 취하는 게이지 장의 상태를 취할 수 있다. 이는 양-밀스 방정식의 해를 이루지 않으며, 이와 같은 꼴의 해의 최저 에너지 상태는 (만약 존재한다면) 고에너지 물리학(즉, 초끈 이론)에 의존한다.

[Ⅰ종 끈 이론의](https://ko.wikipedia.org/wiki/Ⅰ종_끈_이론 "wikilink") 관점에서, 이는 BPS 조건을 따르지 않는 [D0-막](https://ko.wikipedia.org/wiki/D0-막 "wikilink")으로 여길 수 있다.\[18\]\[19\] 이는 BPS가 아니지만, 게이지 전하의 보존으로 인하여 안정하다.

### ⅡB 자기 이중성

| ⅡB종 막                                   | ⅡB종 막                                |
| --------------------------------------- | ------------------------------------ |
| [기본 끈](../Page/끈_\(물리학\).md "wikilink") | [D1-막](../Page/D-막.md "wikilink")    |
| [D3-막](../Page/D-막.md "wikilink")       | [D3-막](../Page/D-막.md "wikilink")    |
| [D5-막](../Page/D-막.md "wikilink")       | [NS5-막](../Page/NS5-막.md "wikilink") |
| [D7-막](../Page/D-막.md "wikilink")       | S7-막\[20\]                           |
| [D9-막](../Page/D-막.md "wikilink")       | S9-막\[21\]                           |

ⅡB 이론은 스스로의 S-이중 이론이다. 또한, ⅡB 이론의 S-대칭은 \(SL(2,\mathbb Z)\)이다. 이에 따라 기본 끈((1,0)-끈)은 일반적으로 *p*개의 기본 끈과 *q*개의 D-끈으로 이루어진 **(*p*,*q*)-끈**에 대응되게 된다. 마찬가지로 (*p*,*q*) 5-막도 존재한다. D3-막은 S-이중성에 따라 변환하지 않는다.

7-막과 9-막의 변환은 더 복잡하다. [D7-막](https://ko.wikipedia.org/wiki/D7-막 "wikilink")은 여차원이 2이므로, [초중력](../Page/초중력.md "wikilink")에서 그 해는 부족각(不足角, )을 가지며, 액시온(0차 [라몽-라몽 장](../Page/라몽-라몽_장.md "wikilink"))과 [딜라톤](../Page/딜라톤.md "wikilink")은 그 주위에서 [모노드로미](../Page/모노드로미.md "wikilink")를 갖는다. 7-막들은 이 액시오딜라톤의 [SL(2;ℤ)](https://ko.wikipedia.org/wiki/SL\(2;ℤ\) "wikilink") [모노드로미](../Page/모노드로미.md "wikilink") 행렬로서 분류된다. 부족각의 존재 때문에, 충분히 많은 7-막을 사용하면 ⅡB 초끈 이론의, 양의 곡률을 갖는 다양체 위의 [축소화](../Page/축소화.md "wikilink")를 정의할 수 있으며, 이 경우 7-막들은 [F이론](../Page/F이론.md "wikilink")에 의하여 [타원 곡선](https://ko.wikipedia.org/wiki/타원_곡선 "wikilink") 올의 퇴화에 해당한다.

9-막의 경우, 이는 시공간을 채우는 막이므로, 올챙이() [파인먼 도표의](https://ko.wikipedia.org/wiki/파인먼_도표 "wikilink") 상쇄를 위하여 특정한 수의 D9-막과 [오리엔티폴드](../Page/오리엔티폴드.md "wikilink")를 가해야 하며, 이 경우 [Ⅰ종 초끈 이론을](https://ko.wikipedia.org/wiki/Ⅰ종_초끈_이론 "wikilink") 얻는다.

### ⅡA / 잡종 이중성

ⅡA종 끈 이론을 [K3 곡면](../Page/K3_곡면.md "wikilink") 위에 [축소화](../Page/축소화.md "wikilink")하여 얻는, 6차원 \(\mathcal N=(1,1)\) 초끈 이론은 [잡종 끈 이론을](../Page/잡종_끈_이론.md "wikilink") 4차원 [원환면](../Page/원환면.md "wikilink") 위에 축소화하여 얻는 6차원 \(\mathcal N=(1,1)\) 초끈 이론과 같다.\[22\] 이 경우, 끈 [결합 상수가](../Page/결합_상수.md "wikilink") 서로 반비례하므로, 이는 S-이중성의 한 형태이다.

## ⅡB종 초중력의 S-이중성

ⅡB종 초중력은 ⅡB종 초끈 이론의 저에너지 [유효이론](https://ko.wikipedia.org/wiki/유효이론 "wikilink")이다. ⅡB종 초끈 이론이 \(SL(2,\mathbb Z)\) S-이중성을 가지는 것처럼, ⅡB종 초중력도 [\(SL(2,\mathbb R)\)](../Page/2차원_실수_특수선형군.md "wikilink") S-이중성을 가진다. (초중력을 [초끈 이론으로](../Page/초끈_이론.md "wikilink") 양자화하는 과정에서, 양자역학적 효과에 의하여 [\(SL(2,\mathbb R)\)가](../Page/2차원_실수_특수선형군.md "wikilink") \(SL(2,\mathbb Z)\)로 깨진다.)

ⅡB종 초중력의 보손 장들은 [\(SL(2,\mathbb R)\)에](../Page/2차원_실수_특수선형군.md "wikilink") 대하여 다음과 같이 변환한다.

| 장                                                                                                                | 행렬 \(M=\begin{pmatrix}
a&b\\c&d
\end{pmatrix}\in SL(2,\mathbb R)\)에 대한 변환 |
| ---------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| [캘브-라몽 장](../Page/캘브-라몽_장.md "wikilink") \(B_2\) 및 [라몽-라몽 2차 형식](../Page/라몽-라몽_장.md "wikilink") \(C_2\)          | \(\binom{B_2}{C_2}\mapsto M\binom{B_2}{C_2}\)                             |
| [딜라톤](../Page/딜라톤.md "wikilink") \(\Phi\) 및 [라몽-라몽 0차 형식](../Page/라몽-라몽_장.md "wikilink") \(C_0\)                 | \(\tau=C_0+i\exp(-\Phi)\), \(\tau\mapsto(a\tau+b)/(c\tau+d)\)             |
| [라몽-라몽 4차 형식](../Page/라몽-라몽_장.md "wikilink") \(C_4\)                                                             | 불변                                                                        |
| [중력장](../Page/중력장.md "wikilink") (아인슈타인 틀) \(g^{\text{(E)}}_{\mu\nu}=\exp(-\Phi/2)g^{\text{(string)}}_{\mu\nu}\) | 불변                                                                        |
|                                                                                                                  |                                                                           |

## U-이중성

[M이론](../Page/M이론.md "wikilink")에서는 [T-이중성](../Page/T-이중성.md "wikilink")과 S-이중성에 의하여, 보다 더 큰 이산대칭군이 존재한다. 이를 **[U-이중성](../Page/U-이중성.md "wikilink")**이라고 한다.

## 통계역학적 격자 모형의 S-이중성

[통계역학](../Page/통계역학.md "wikilink")에서, 각종 [격자 모형들도](https://ko.wikipedia.org/wiki/격자_모형 "wikilink") S-이중성을 만족한다. 2차원 격자 모형의 S-이중성은 **크라머르스-바니어 이중성**()이라고 하며,\[23\] [헨드릭 안토니 크라머르스와](../Page/헨드릭_안토니_크라머르스.md "wikilink") 그레고리 바니어()가 1941년 발표하였다.\[24\] 2차원 이상의 차원에도 유사한 이중성들이 존재한다.

## 참고 문헌

## 외부 링크

  -
  -
[분류:양자장론](https://ko.wikipedia.org/wiki/분류:양자장론 "wikilink") [분류:끈 이론](https://ko.wikipedia.org/wiki/분류:끈_이론 "wikilink") [분류:쌍대성이론](https://ko.wikipedia.org/wiki/분류:쌍대성이론 "wikilink") [분류:격자 모형](https://ko.wikipedia.org/wiki/분류:격자_모형 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10. {{ 웹 인용 |url=<http://www.lepp.cornell.edu/~pt267/files/notes/Seibergology.pdf> |제목=Notes on Seibergology |이름=Flip|성=Tanedo|날짜=2011 }}
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
23.
24.