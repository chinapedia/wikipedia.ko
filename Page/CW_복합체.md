> This article is converted from Wikipedia: [CW ](https://ko.wikipedia.org/wiki/CW_).


[호모토피 이론에서](https://ko.wikipedia.org/wiki/호모토피_이론 "wikilink"), **CW 복합체**(CW復合體, )는 일련의 **세포**(細胞, )들을 이어붙여 구성할 수 있는 [위상 공간이다](https://ko.wikipedia.org/wiki/위상_공간_\(수학\) "wikilink").\[1\]\[2\] [단체 복합체의](../Page/단체_복합체.md "wikilink") 개념보다 더 자유롭고, [단체 집합의](../Page/단체_집합.md "wikilink") 개념보다 더 구체적이지만, 그 [범주](../Page/범주_\(수학\).md "wikilink") 속에서 [호모토피 이론을](https://ko.wikipedia.org/wiki/호모토피_이론 "wikilink") 용이하게 전개할 수 있으며, [단체 호몰로지와](https://ko.wikipedia.org/wiki/단체_호몰로지 "wikilink") 마찬가지로 CW 복합체 구조로부터 직접 그 [호몰로지](../Page/호몰로지.md "wikilink")와 [코호몰로지](https://ko.wikipedia.org/wiki/코호몰로지 "wikilink")를 계산할 수 있다. 이 계산법을 **세포 호몰로지**(細胞homology, ) 및 **세포 코호몰로지**(細胞cohomology, )라고 한다.

## 정의

### 직접적 정의

[하우스도르프 공간](../Page/하우스도르프_공간.md "wikilink") \(X\) 위의 **CW 복합체**는 다음과 같은 데이터로 주어진다.\[3\]

  - 각 \(n\in\mathbb N\)에 대하여, [연속 함수](../Page/연속_함수.md "wikilink") \(\mathbb D^n\to X\)들의 집합 \(\Phi_n\). \(\Phi_n\)의 원소를 \(n\)차원 **세포**()라고 한다.

이들은 다음 네 조건들을 만족시켜야 한다.

  - 각 \(n\)차원 세포 \(\phi\in\Phi_n\)에 대하여, \(\phi|_{\operatorname{int}\mathbb D^n}\)은 그 [치역](../Page/치역.md "wikilink")과의 [위상 동형이다](https://ko.wikipedia.org/wiki/위상_동형 "wikilink").
  - 각 \(x\in X\)에 대하여, \(x\in \phi(\operatorname{int}\mathbb D^n)\)인 유일한 \((n\in\mathbb N,\phi\in\Phi_n)\)이 존재한다.
  - (C) 각 \(n\)차원 세포 \(\phi\in\Phi_n\)에 대하여, 그 경계 \(\partial(\Phi_n)\)은 \(n\) 미만 차원의 유한 개의 세포들의 내부와 교차한다.
  - (W) \(X\)의 부분 집합 \(C\subseteq X\)이 [닫힌집합](https://ko.wikipedia.org/wiki/닫힌집합 "wikilink")일 [필요 충분 조건은](https://ko.wikipedia.org/wiki/필요_충분_조건 "wikilink") 모든 \(n\in\mathbb N\) 및 \(\phi\in\Phi_n\)에 대하여 \(\phi^{-1}(C)\subseteq\mathbb D^n\)가 [닫힌집합](https://ko.wikipedia.org/wiki/닫힌집합 "wikilink")인 것이다.

위 정의에서 \(\operatorname{int}\mathbb D^n=\mathbb D^n\setminus\partial\mathbb D^n\)은 \(n\)차원 닫힌 공의 [내부](../Page/내부_\(위상수학\).md "wikilink"), 즉 \(n\)차원 열린 공이다.

CW 복합체 \((X,(\Phi_n)_{n\in\mathbb N})\)의 **부분 CW 복합체**()는 다음 조건을 만족시키는 [부분 공간](https://ko.wikipedia.org/wiki/부분_공간 "wikilink") \(A\subseteq X\)이다.\[4\]

  - \(A\)는 \(X\)에 속하는 세포들로 구성된다.
  - \(A\)에 속하는 세포의 폐포는 항상 다시 \(A\)에 속한다.

CW 복합체의 임의의 열린 세포는 항상 어떤 유한 차원 부분 복합체에 포함된다. 그리고 CW 복합체의 콤팩트 부분공간은 항상 어떤 유한 개의 열린 세포에 포함되므로, CW 복합체의 임의의 [콤팩트](../Page/콤팩트_공간.md "wikilink") 부분 공간은 항상 어떤 유한 차원 부분 복합체에 포함된다.

### 귀납적 정의

CW 복합체의 개념은 다음과 같이 귀납적으로 정의될 수도 있다.\[5\]

\(n\)차원 **뼈대**()는 다음과 같이 정의될 수 있는 [위상 공간이다](https://ko.wikipedia.org/wiki/위상_공간_\(수학\) "wikilink").

1.  −1차원 뼈대는 [공집합](../Page/공집합.md "wikilink")이다.
2.  \(n-1\)차원 뼈대가 주어졌을 때, \(n\)차원 뼈대를 구성하기 위하여, 임의의 [기수](../Page/기수_\(수학\).md "wikilink") \(\kappa_n\) 및 [연속 함수](../Page/연속_함수.md "wikilink") \(\phi_n \colon (\mathbb S^{n-1})^{\sqcup \kappa_n} \to X\)에 대하여, [붙임 공간](../Page/붙임_공간.md "wikilink") \(X_n = X_{n-1} \cup_{\phi_n}(\mathbb D^n){\sqcup \kappa_n}\)을 취한다.

위 정의에서, \(\mathbb S^n\)은 \(n\)차원 [초구](../Page/초구.md "wikilink")이며 \(\mathbb D^n \supsetneq \mathbb S^{n-1}\)은 \(n\)차원 [닫힌 공이다](https://ko.wikipedia.org/wiki/닫힌_공 "wikilink"). 특히 \(\mathbb S^{-1} = \varnothing\)이며 \(\mathbb D^0 = \{\bullet\}\)이다 ([한원소 공간](https://ko.wikipedia.org/wiki/한원소_공간 "wikilink")).

\(n\)차원 뼈대 \(X_n\)이 주어졌다면, 낮은 차원의 뼈대에 대한 포함 사상

\[X_0\hookrightarrow X_1\hookrightarrow X_2\hookrightarrow\cdots\] 이 존재한다. **CW 복합체**는 유한 차원 뼈대들의 [귀납적 극한이다](../Page/귀납적_극한.md "wikilink"). 즉, 뼈대들의 포함 관계

\[X_0\hookrightarrow X_1\hookrightarrow\cdots\] 의 [귀납적 극한](../Page/귀납적_극한.md "wikilink")

\[X_\infty=\varinjlim_{n\to\infty}X_n\] 이다.

이 귀납적 정의에서, 직접적 정의의 C 조건은 자동적으로 성립한다. 이는 세포의 폐포가 [콤팩트 공간이기](../Page/콤팩트_공간.md "wikilink") 때문에, 무한 개의 세포들을 포함할 수 없기 때문이다. W 조건은 [귀납적 극한의](../Page/귀납적_극한.md "wikilink") 정의에 포함돼 있다.

### 추상적 정의

다음이 주어졌다고 하자.

  - [쌍대 완비 범주](https://ko.wikipedia.org/wiki/쌍대_완비_범주 "wikilink") \(\mathcal C\)
  - \(\mathcal C\) 속의 사상들의 [집합](../Page/집합.md "wikilink") \(\mathfrak M\subseteq \operatorname{Mor}(\mathcal C)\)
  - \(\mathcal C\) 속의 대상 \(X_0\)

그렇다면, \(\mathcal C\) 속의, \(X_0\) 위의 **세포 복합체**(細胞複合體, )는 다음과 같은 데이터로 주어진다.

  - [순서수](../Page/순서수.md "wikilink") \(\eta \in\operatorname{Ord}\)
  - 각 순서수 \(\alpha < \eta\)에 대하여, 사상 \(\iota_\alpha\colon S_\alpha\to D_\alpha\). 또한, \(\iota_\alpha\in\mathfrak M\)이다. 이를 **\(\alpha\)번째 세포**(-細胞, )라고 하자.
  - 각 순서수 \(\alpha < \eta\)에 대하여, 사상 \(\phi_\alpha \colon S_\alpha \to X_\alpha\). 이를 **접착 사상**(接着寫像, )이라고 하자.

위 정의에서, \(X_\alpha\)는 모든 \(\alpha\le\eta\)에 대하여 [초한 귀납법에](https://ko.wikipedia.org/wiki/초한_귀납법 "wikilink") 따라 다음과 같이 정의된다.

  - 만약 \(\alpha=\beta+1\)가 [극한 순서수가](https://ko.wikipedia.org/wiki/극한_순서수 "wikilink") 아닐 때, \(X_{\beta+1}\)는 [극한 순서수가](https://ko.wikipedia.org/wiki/극한_순서수 "wikilink") 아닌 \(\alpha\)에 대하여 정의되며, 다음과 같은 [밂에](../Page/밂_\(범주론\).md "wikilink") 등장하는 사상이다.
      -
        <math>\\begin{matrix}

S_\\beta & \\overset{\\iota_\\beta}\\to & D_\\beta \\\\ {\\scriptstyle\\phi_\\beta} \\downarrow {\\color{White}\\scriptstyle\\phi_\\beta} && \\downarrow \\\\ X_\\beta & \\underset{f_{\\beta+1}}\\to & X_{\\beta+1} \\end{matrix} </math>

  - 만약 \(\alpha\)가 [극한 순서수라면](https://ko.wikipedia.org/wiki/극한_순서수 "wikilink"), \(X_\alpha\)는 다음과 같은 (\((f_\beta)_{\beta<\alpha}\)들에 대한) [귀납적 극한](../Page/귀납적_극한.md "wikilink")(즉, [쌍대극한](https://ko.wikipedia.org/wiki/쌍대극한 "wikilink"))이다.
      -
        \(X_\alpha = \varinjlim_{\beta<\alpha} X_\beta\)

특히, 0은 [극한 순서수이며](https://ko.wikipedia.org/wiki/극한_순서수 "wikilink"), \(X_0\)는 빈 그림의 [쌍대극한](https://ko.wikipedia.org/wiki/쌍대극한 "wikilink")이므로 \(\mathcal C\)의 [시작 대상이다](https://ko.wikipedia.org/wiki/시작_대상 "wikilink").

이와 같은 열의 끝에서, 대상 \(X_\eta\)를 얻는다. 이는 [시작 대상](https://ko.wikipedia.org/wiki/시작_대상 "wikilink") \(X_0\) 위에 \(D_\alpha\)들을 “경계” \(S_\alpha\)를 통해 \(\eta\)번 “붙여서” 얻는 것으로 여길 수 있다.

이제, [위상 공간의](https://ko.wikipedia.org/wiki/위상_공간_\(수학\) "wikilink") [범주](../Page/범주_\(수학\).md "wikilink") \(\operatorname{Top}\)에서,

\[\eta = \omega\]

\[\iota_n \colon (\mathbb S^{n-1})^{\sqcup \kappa_n} \to (\mathbb D^n)^{\sqcup \kappa_n}\] 가 되는 상대 세포 복합체를 **CW 복합체**라고 한다. 여기서

  - \((\kappa_n)_{n<\omega}\)는 임의의 (0 또는 유한 또는 무한) [기수들의](../Page/기수_\(수학\).md "wikilink") [수열](../Page/수열.md "wikilink")이다.
  - \(\phi_n \colon (\mathbb D^n)^{\sqcup\kappa_n} \to X_n\)은 임의의 [연속 함수이다](../Page/연속_함수.md "wikilink").
  - \(\mathbb S^{-1}=\varnothing\)이며 \(\mathbb D^0 = \{\bullet\}\)([한원소 공간](https://ko.wikipedia.org/wiki/한원소_공간 "wikilink"))이다.

(이 정의는 위의 정의들과 차수가 1만큼 다르다. 즉, 이 정의에서 \(X_0=\varnothing\)이며, \(X_1\)은 [이산 공간이며](../Page/이산_공간.md "wikilink"), \(X_n\)은 \(n-1\)차원까지의 세포들로 구성된다.)

## 연산

CW 복합체들의 모임은 다음과 같은 연산에 대하여 닫혀 있다.

  - 두 CW 복합체의 [콤팩트 생성 공간으로서의](../Page/콤팩트_생성_공간.md "wikilink") 곱은 CW 복합체이다. 집합으로서 이는 항상 [곱집합](../Page/곱집합.md "wikilink")이지만 그 위의 위상은 [곱위상](../Page/곱위상.md "wikilink")보다 더 섬세할 수 있다. 구체적으로, 곱공간이 비가산 개의 세포를 포함하고 또 원래의 두 CW 복합체가 모두 [국소 콤팩트 공간이](https://ko.wikipedia.org/wiki/국소_콤팩트_공간 "wikilink") 아닐 경우 이는 곱위상보다 더 섬세한 위상을 갖는다.
  - CW 복합체의 [피복 공간은](../Page/피복_공간.md "wikilink") CW 복합체이다.
  - 만약 \(X\)와 \(Y\)가 CW 복합체이며, \(X\)가 유한 개의 세포로 구성되었다면, [콤팩트-열린 집합 위상을](https://ko.wikipedia.org/wiki/콤팩트-열린_집합_위상 "wikilink") 부여한 함수 공간 \(\hom(X,Y)\)는 CW 복합체와 [호모토피 동치이다](../Page/호모토피_동치.md "wikilink").\[6\]

## 성질

### 일반위상수학적 성질

모든 CW 복합체는 다음 성질을 만족시킨다.

  - [하우스도르프 공간이며](../Page/하우스도르프_공간.md "wikilink") [정규 공간이다](../Page/정규_공간.md "wikilink").\[7\]
  - [국소 축약 가능 공간이다](https://ko.wikipedia.org/wiki/국소_축약_가능_공간 "wikilink").\[8\]
  - [파라콤팩트 공간이다](../Page/파라콤팩트_공간.md "wikilink").
  - [콤팩트 생성 공간이다](../Page/콤팩트_생성_공간.md "wikilink").\[9\]

유한 개의 세포들로 구성된 CW 복합체는 [콤팩트 공간이다](../Page/콤팩트_공간.md "wikilink").

CW 복합체에서, 모든 세포의 [폐포는](../Page/폐포_\(위상수학\).md "wikilink") 오직 유한 개의 세포들과 [공집합](../Page/공집합.md "wikilink")이 아닌 [교집합](../Page/교집합.md "wikilink")을 갖는다. 즉, \(X\)의 세포로의 [분할이](../Page/집합의_분할.md "wikilink") \(\{e_\alpha\}_{\alpha\in I}\)라면,

\[\forall \alpha \colon |\{\beta\in I\colon e_\beta \cap \operatorname{cl}(e_\alpha) \ne \varnothing \}| < \aleph_0\] 이다.

### 호모토피 이론적 성질

#### 세포 호몰로지

[단체 복합체에](../Page/단체_복합체.md "wikilink") 대하여 [단체 호몰로지를](https://ko.wikipedia.org/wiki/단체_호몰로지 "wikilink") 정의할 수 있는 것처럼, CW 복합체에 대하여 그 CW 구조를 사용하여 **세포 호몰로지**(細胞homology, )라는 호몰로지 이론을 정의할 수 있다. CW 복합체에 대하여 이는 [특이 호몰로지와](../Page/특이_호몰로지.md "wikilink") 일치한다.

[CW 복합체](../Page/CW_복합체.md "wikilink") \(X\)의 \(n\)차원 뼈대가 \(X_n\)이라고 하자.

\[\varnothing=X_{-1}\subseteq X_0\subseteq X_1\subseteq X_2\subseteq\cdots\subseteq X_\infty=X\] 임의의 \(n\)에 대하여, [상대 호몰로지](../Page/상대_호몰로지.md "wikilink")

\[\operatorname H_n(X_n,X_{n-1})\] 는 [자유 아벨 군이며](../Page/자유_아벨_군.md "wikilink"), 그 생성원들은 \(X\)의 \(n\)차원 세포 \(\{e_\alpha^n\}_{\alpha\in I_n}\)들과 표준적으로 대응한다.

그렇다면, 다음과 같은 [사슬 복합체를](../Page/사슬_복합체.md "wikilink") 생각하자.

\[C_n=\operatorname H_n(X_n,X_{n-1})\]

\[\partial_n\colon C_n\to C_{n-1}\]

\[\partial_n\colon e_\alpha^n\mapsto\sum_\beta(\deg \chi_n^{\alpha\beta})e^{n-1}_\beta\] 여기서 \(\deg\)는 [브라우어르 차수이며](../Page/브라우어르_차수.md "wikilink"), \(\chi_n^{\alpha\beta}\)는 다음과 같다.

\[\chi_{n}^{\alpha \beta}\colon\partial e_\alpha^n \hookrightarrow X_{n - 1}  \twoheadrightarrow X_{n - 1} /( X_{n - 1} \setminus e^{n - 1}_\beta)\] 이 경우 \(\partial e_\alpha^n\cong\mathbb S^{n-1}\cong X_{n - 1} /( X_{n - 1} \setminus e^{n - 1}_\beta)\)이므로, [브라우어르 차수가](../Page/브라우어르_차수.md "wikilink") 잘 정의된다.

이 CW 복합체에 대하여 취한 [호몰로지](../Page/호몰로지.md "wikilink")를 \(X\)의 **세포 호몰로지**(細胞homology, )라고 한다. 세포 복합체를 쌍대화하여, **세포 코호몰로지**(細胞cohomology, ) 역시 정의할 수 있다.

CW 복합체의 세포 호몰로지는 그 [특이 호몰로지와](../Page/특이_호몰로지.md "wikilink") 일치한다. CW 복합체 \(X\)에서, \(n\)차원 세포의 수가 [기수](../Page/기수_\(수학\).md "wikilink") \(c_n\in\operatorname{Card}\)라면, 세포 호몰로지의 정의에 따라 \(c_n\)은 \(X\)의 \(n\)차 [베티 수의](../Page/베티_수.md "wikilink") [상계이다](https://ko.wikipedia.org/wiki/상계_\(수학\) "wikilink").

\[\dim_{\mathbb Q}\operatorname H(X;\mathbb Q) \le c_n\]

세포의 수가 유한한 CW 복합체 \(X\)에서, \(n\)차원 세포의 수가 \(c_n\)이라고 하자. 그렇다면, 세포 호몰로지의 정의에 따라 그 [오일러 지표는](../Page/오일러_지표.md "wikilink") 다음과 같다.

\[\chi(X)=\sum_{n=0}^\infty(-1)^nc_n\]

#### 화이트헤드 정리

**화이트헤드 정리**(Whitehead定理, )\[10\]\[11\]\[12\] 에 따르면, 두 CW 복합체 사이의 [연속 함수가](../Page/연속_함수.md "wikilink") [호모토피 동치가](../Page/호모토피_동치.md "wikilink") 될 필요충분조건은 이 함수가 [약한 호모토피 동치](https://ko.wikipedia.org/wiki/약한_호모토피_동치 "wikilink")(모든 [호모토피 군의](../Page/호모토피_군.md "wikilink") [동형](https://ko.wikipedia.org/wiki/동형 "wikilink")을 유도하는 [연속 함수](../Page/연속_함수.md "wikilink"))를 이루는 것이다. 따라서, CW 복합체의 경우 [호모토피 동치와](../Page/호모토피_동치.md "wikilink") [약한 호모토피 동치를](https://ko.wikipedia.org/wiki/약한_호모토피_동치 "wikilink") 구별할 필요가 없다.

#### 세포 근사 정리

두 CW 복합체 사이의 **세포 함수**(細胞函數, )는 다음 조건을 만족시키는 [연속 함수](../Page/연속_함수.md "wikilink") \(f\colon X\to Y\)이다.

  - \(f\)는 \(n\)차원 뼈대를 \(n\)차원 뼈대로 대응시킨다. 즉, 다음이 성립한다.
      -
        \(f(X_n)\subseteq Y_n\qquad\forall n\in\mathbb N\)

**세포 근사 정리**(細胞近似定理, )에 따르면, 두 CW 복합체 사이의 임의의 [연속 함수](../Page/연속_함수.md "wikilink") \(f\colon X\to Y\)는 세포 함수와 [호모토픽](https://ko.wikipedia.org/wiki/호모토픽 "wikilink")하다. 또한, 만약 부분 CW 복합체 \(A\subseteq X\)에 대하여 \(f|_A\colon A\to Y\)가 세포 함수라면, 이 호모토피는 \(A\)에 대하여 고정되게 잡을 수 있다. 따라서, 호모토피 이론에서는 CW 복합체 사이의 모든 [연속 함수를](../Page/연속_함수.md "wikilink") 세포 함수로 가정할 수 있다.

### 모형 범주 이론적 성질

추상적으로, 모든 [위상 공간의](https://ko.wikipedia.org/wiki/위상_공간_\(수학\) "wikilink") 범주에 올뭉치가 [세르 올뭉치이며](https://ko.wikipedia.org/wiki/세르_올뭉치 "wikilink"), 약한 동치가 [약한 호모토피 동치인](https://ko.wikipedia.org/wiki/약한_호모토피_동치 "wikilink") [모형 범주](../Page/모형_범주.md "wikilink") 구조를 줄 수 있다. 이 [모형 범주에서](../Page/모형_범주.md "wikilink"), 모든 CW 복합체는 [쌍대올대상](https://ko.wikipedia.org/wiki/쌍대올대상 "wikilink")이다. CW 복합체의 화이트헤드 정리는 일반적인 [모형 범주에서의](../Page/모형_범주.md "wikilink") 화이트헤드 정리의 특수한 경우이다.

## 예

일반적으로 위상 공간의 CW 복합체 구조는 [단체 복합체](../Page/단체_복합체.md "wikilink") 구조보다 더 간단하다.

### 낮은 차원의 CW 복합체

다음 세 개념이 서로 [동치](../Page/동치.md "wikilink")이다.

  - (유한 또는 무한) [이산 공간](../Page/이산_공간.md "wikilink")
  - 0차원 CW 복합체 \(X=X_0\)
  - 0차원 [단체 복합체](../Page/단체_복합체.md "wikilink")

다음 두 개념이 서로 [동치](../Page/동치.md "wikilink")이다.

  - (유한 또는 무한) [다중 그래프](../Page/다중_그래프.md "wikilink") \(\Gamma\) (특히, 양끝점이 같은 꼭짓점인 변이 존재할 수 있다)
  - 1차원 CW 복합체 \(X=X_1\)

이 경우, [그래프 이론과](../Page/그래프_이론.md "wikilink") [위상수학](../Page/위상수학.md "wikilink")의 개념이 다음과 같이 대응된다.

  -
    {| class=wikitable

\! 다중 그래프 \(\Gamma\) \!\! CW 복합체 \(X\) |- | 꼭짓점 집합 \(\operatorname V(\Gamma)\) || 0차원 뼈대 \(X_0\) |- | 변 \(e\in \operatorname E(\Gamma)\) || \(X_0\)에 연결된 1차원 세포 \(e_a\cong[0,1]\) |- | 변 \(e\)의 양끝점 \(u,v\in \operatorname V(\Gamma)\) (\(u=v\)일 수 있음) || \(e_a\)의 접착 사상 \(\phi_a \colon \{0,1\} \to X_0\)의 [치역](../Page/치역.md "wikilink") |- | [연결 다중 그래프](../Page/연결_그래프.md "wikilink") || [연결 공간](../Page/연결_공간.md "wikilink") |}

1차원 CW 복합체는 양끝점이 같은 변 및 같은 양끝점을 공유하는 변을 허용하므로, 1차원 [단체 복합체보다](../Page/단체_복합체.md "wikilink") 더 일반적인 개념이다. 사실, 1차원 [단체 복합체는](../Page/단체_복합체.md "wikilink") [그래프](https://ko.wikipedia.org/wiki/그래프 "wikilink")와 [동치](../Page/동치.md "wikilink")인 개념이다.

### 유클리드 공간

[유클리드 공간](../Page/유클리드_공간.md "wikilink") \(\mathbb R^n\) 위에는 다음과 같은 CW 구조를 줄 수 있다.

  - 0-뼈대는 격자 \(\mathbb Z^n\subset\mathbb R^n\)이다.
  - 1-뼈대는 \(\mathbb R^n\) 속의, 격자점들에 대한 선분들이다.
  - 2-뼈대는 \(\mathbb R^n\) 속의, 격자점들에 대한 정사각형들이다.
  - ⋮
  - \(n\)-뼈대는 격자점들에 대한 \(n\)차원 [초입방체](https://ko.wikipedia.org/wiki/초입방체 "wikilink")들이다.

### 초구

\(n\ge1\)차원 [초구](../Page/초구.md "wikilink") \(\mathbb S^n\) 위에는 다음과 같은, 두 개의 세포만을 갖는 CW 구조를 줄 수 있다.

  - 하나의 0차원 세포 \(\bullet\)이다.
  - 하나의 \(n\)차원 세포. 이 세포의 경계 전체는 \(\bullet\)으로 이어붙여진다.

이에 따라, \(n\ge1\)일 경우 세포 사슬 복합체의 경계 사상은 자명하며, 초구의 세포 호몰로지는

\[\operatorname H_k(\mathbb S^n)=\begin{cases}C_0\cong\mathbb Z&k=0\\
C_n\cong\mathbb Z&k=n\\
0&k\ne0
\end{cases}\] 이다.

초구 사이의 연속 함수 \(\mathbb S^m\to\mathbb S^n\)에서, \(m<n\)이라고 하자. 그렇다면 세포 근사 정리에 따라서 이 함수는 세포 함수와 [호모토픽](https://ko.wikipedia.org/wiki/호모토픽 "wikilink")하다. 밑점을 보존하는 세포 함수 \(\mathbb S^m\to\mathbb S^n\)은 (\(m<n\)이므로) 밑점으로 가는 [상수 함수](../Page/상수_함수.md "wikilink") 밖에 없다. 따라서 \(m<n\)에 대하여 \(\pi_m(\mathbb S^n)=0\)임을 알 수 있다.

### 복소수 사영 공간

\(2n\)차원 [복소수 사영 공간](https://ko.wikipedia.org/wiki/복소수_사영_공간 "wikilink") \(\mathbb{CP}^n\) 위에는 각 짝수 차원에 하나씩, 총 \(n+1\)개의 세포로 구성된 CW 구조가 존재한다. 이 세포들은 다음과 같다.

\[\mathbb{CP}^n=\mathbb C^n\sqcup\mathbb C^{n-1}\times\{\widehat\infty\}
\sqcup\mathbb C^{n-2}\times\{(\widehat\infty,\widehat\infty)\}\sqcup\cdots\sqcup\mathbb C^0\times\{(\widehat\infty,\dots,\widehat\infty)\}\] 따라서, 그 세포 호몰로지는

\[C_k(\mathbb{CP}^n)=\begin{cases}\mathbb Z&2\mid k\\0&2\nmid k\end{cases}\] 이다. 모든 경계 사상들은 자명하며, 그 (세포) 호몰로지는

\[\operatorname H_k(\mathbb{CP}^n;\mathbb Z)=C_k\cong\mathbb Z\] 이다.

### 실수 사영 공간

\(n\)차원 [실수 사영 공간](https://ko.wikipedia.org/wiki/실수_사영_공간 "wikilink") \(\mathbb{RP}^n\) 위에는 \(n+1\)개의 세포로 구성된 CW 구조가 존재한다. 이 경우, 각 차원 \(0,1,2,\dots,n\)에 세포가 하나씩 존재한다.

### 그라스만 다양체

[그라스만 다양체는](../Page/그라스만_다양체.md "wikilink") **슈베르트 세포**()라는 표준적인 CW 구조를 갖는다.

### 다양체

[다양체](../Page/다양체.md "wikilink")는 모두 CW 복합체의 [호모토피 유형을](https://ko.wikipedia.org/wiki/호모토피_유형 "wikilink") 갖는다.

4차원 이하의 콤팩트 다양체는 모두 [단체 복합체와](../Page/단체_복합체.md "wikilink") [위상 동형이며](https://ko.wikipedia.org/wiki/위상_동형 "wikilink") 따라서 CW 복합체와 위상 동형이다.\[13\]

4차원에서는 [단체 복합체의](../Page/단체_복합체.md "wikilink") 구조를 갖지 않는 콤팩트 다양체가 존재한다. CW 복합체의 구조를 갖지 않는 4차원 콤팩트 다양체가 존재하는지는 아직 알려지지 않았다.\[14\]

5차원 이상에서 모든 콤팩트 다양체는 CW 복합체의 구조를 갖는다. 그러나 [단체 복합체의](../Page/단체_복합체.md "wikilink") 구조가 항상 존재하는지는 알려지지 않았다.\[15\]

#### 모스 이론

[리만 다양체](../Page/리만_다양체.md "wikilink") \((M,g)\) 및 그 위의 [모스 함수](https://ko.wikipedia.org/wiki/모스_함수 "wikilink") \(f\colon M\to\mathbb R\)가 주어졌다고 하자. 그렇다면 \(f\)의 기울기 흐름을 사용하여 \(M\)과 [호모토피 동치인](../Page/호모토피_동치.md "wikilink") CW 복합체를 정의할 수 있다. 이 CW 복합체에서 \(n\)차원 세포는 [모스 지표가](https://ko.wikipedia.org/wiki/모스_지표 "wikilink") \(n\)인 임계점과 [일대일 대응한다](https://ko.wikipedia.org/wiki/일대일_대응 "wikilink").

### C · W 조건이 성립하지 않는 복합체

일부 저자들은 C 조건 및 W 조건이 성립하지 않을 수 있는 복합체를 “화이트헤드 복합체”나 “세포 복합체”라고 부른다.

2차원 원판 \(\mathbb D^2\) 위에 다음과 같은 화이트헤드 복합체 구조를 정의하자.\[16\]

  - 2차원 세포 \(\mathbb D^2\to\mathbb D^2\) ([항등 함수](../Page/항등_함수.md "wikilink"))
  - 각 \(x\in\partial\mathbb D^2\)에 대하여, 0차원 세포 \(\mathbb D^0\to \mathbb D^2\)

이는 CW 복합체의 정의에서 W 조건을 따르지만 C 조건만을 따르지 않아 CW 복합체가 아니다.

임의의 위상 공간 \(X\) 위에, 다음과 같이 자명한 화이트헤드 복합체 구조를 줄 수 있다.

  - 각 점 \(x\in X\)에 대하여 0차원 세포 \(\mathbb D^0\hookrightarrow X\)

이는 CW 복합체의 정의에서 C 조건을 (자명하게) 따르지만 (\(X\)가 [이산 공간이](../Page/이산_공간.md "wikilink") 아니라면) W 조건을 따르지 않아 CW 복합체를 이루지 않는다.

### CW 복합체와 위상 동형이 아닌 공간

모든 CW 복합체는 [하우스도르프 공간이며](../Page/하우스도르프_공간.md "wikilink"), 따라서 [하우스도르프 공간이](../Page/하우스도르프_공간.md "wikilink") 아닌 위상 공간은 CW 복합체와 [위상 동형일](https://ko.wikipedia.org/wiki/위상_동형 "wikilink") 수 없다.

무한 차원 [힐베르트 공간은](../Page/힐베르트_공간.md "wikilink") [하우스도르프 공간이지만](../Page/하우스도르프_공간.md "wikilink") CW 복합체와 [위상 동형이지](https://ko.wikipedia.org/wiki/위상_동형 "wikilink") 않다. 무한 차원 힐베르트 공간은 [베르 공간이므로](../Page/베르_공간.md "wikilink"), 유한 차원의 뼈대들의 [귀납적 극한으로](../Page/귀납적_극한.md "wikilink") 나타낼 수 없다. 그러나 이는 [축약 가능 공간이므로](../Page/축약_가능_공간.md "wikilink"), CW 복합체와 [호모토피 동치이다](../Page/호모토피_동치.md "wikilink").

다음과 같은 공간은 [국소 축약 가능 공간이](https://ko.wikipedia.org/wiki/국소_축약_가능_공간 "wikilink") 아니므로, CW 복합체와 [위상동형](https://ko.wikipedia.org/wiki/위상동형 "wikilink")이지 않다.

\[\{re^{2\pi i \theta} : 0 \leq r \leq 1, \theta \in \mathbb Q\} \subset \mathbb C\] 그러나 이는 [축약 가능 공간이므로](../Page/축약_가능_공간.md "wikilink"), CW 복합체와 [호모토피 동치이다](../Page/호모토피_동치.md "wikilink").

### CW 복합체의 호모토피 유형을 갖지 않는 공간

유클리드 평면 속의 다음과 같은 [부분 공간을](https://ko.wikipedia.org/wiki/부분_공간 "wikilink") 생각하자.

\[\left\{(x,y)\in\mathbb R^2\colon \exists n\in\mathbb Z^+\colon \sqrt{(x-1/n)^2+y^2}=1/n\right\}\] 이를 **하와이 귀고리**()이라고 한다. 이는 [완비 거리 공간이자](../Page/완비_거리_공간.md "wikilink") [콤팩트 공간이며](../Page/콤팩트_공간.md "wikilink") [경로 연결 공간이지만](https://ko.wikipedia.org/wiki/경로_연결_공간 "wikilink"), CW 복합체의 [호모토피 유형을](https://ko.wikipedia.org/wiki/호모토피_유형 "wikilink") 갖지 않는다.

### 다른 범주에서의 세포 복합체

임의의 범주 \(\mathcal C\)에서, 만약 사용되는 세포 \(\iota_\alpha\colon S_\alpha \to D_\alpha\)에서 정의역들이 모두 [시작 대상](https://ko.wikipedia.org/wiki/시작_대상 "wikilink") \(S_\alpha = \varnothing\)이라면, 얻는 세포 복합체 \(X_\eta\)는 단순히 [쌍대곱](../Page/쌍대곱.md "wikilink")

\[X_\eta = \bigsqcup_{\alpha<\eta} D_\alpha\] 이다.

#### 설리번 대수

[표수 0의](https://ko.wikipedia.org/wiki/표수_0 "wikilink") [체](../Page/체_\(수학\).md "wikilink") \(K\)가 주어졌다고 하고, \(K\)-[가환 미분 등급 대수의](https://ko.wikipedia.org/wiki/가환_미분_등급_대수 "wikilink") 범주 \(\operatorname{CDGA}_K\)를 생각하자.

만약 세포들을

\[S_n = K[x],\;\deg x = n,\;\mathrm dx=0\qquad (n\ge0)\]

\[D_n = K[y,\mathrm dy],\;\deg y=n-1 \qquad (n > 0)\]

\[\iota_n\colon S_n \to D_n\]

\[\iota_n\colon x \mapsto \mathrm dy \qquad (n > 0)\] 의 꼴의 \(K\)-[가환 미분 등급 대수](https://ko.wikipedia.org/wiki/가환_미분_등급_대수 "wikilink") [준동형](../Page/준동형.md "wikilink")들 및

\[\iota_0 \colon K \to S_0\]

\[\kappa \colon S_0 \to K,\; x\mapsto 0\] 들로 잡을 경우, 이로부터 얻는 세포 복합체를 **[설리번 대수](../Page/설리번_대수.md "wikilink")**라고 한다.\[17\] 이러한 [준동형](../Page/준동형.md "wikilink")들을 세포로 잡는 이유는 이 [준동형](../Page/준동형.md "wikilink")들이 \(\operatorname{CDGA}_K\)의 표준적 [모형 범주](../Page/모형_범주.md "wikilink") 구조를 생성하는 [쌍대올뭉치](https://ko.wikipedia.org/wiki/쌍대올뭉치 "wikilink")들이기 때문이다.

## 역사

[존 헨리 콘스턴틴 화이트헤드가](../Page/존_헨리_콘스턴틴_화이트헤드.md "wikilink") 1949년에 화이트헤드 정리를 증명하기 위하여 정의하였다.\[18\]\[19\] "CW 복합체"라는 이름에서, C는 "[폐포](../Page/폐포_\(위상수학\).md "wikilink") 유한"()을 뜻하고, W는 [약한 위상](https://ko.wikipedia.org/wiki/약한_위상 "wikilink")()을 뜻한다.\[20\]

  - “폐포 유한성”이란 \(n\)차원 세포 \(c_n\)의 [폐포는](../Page/폐포_\(위상수학\).md "wikilink") 오직 유한 개의 다른 세포들과 교차한다는 것이다.\[21\]
  - “약한 위상”이란 CW 복합체가 그 뼈대들의 [귀납적 극한](../Page/귀납적_극한.md "wikilink") \(\textstyle X=\varinjlim_{n\to\infty}X_n\)임을 뜻한다.\[22\]

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
  -
  -
  -
  -
  -
  -
  -
  -
[분류:호모토피 이론](https://ko.wikipedia.org/wiki/분류:호모토피_이론 "wikilink") [분류:위상 공간](https://ko.wikipedia.org/wiki/분류:위상_공간 "wikilink") [분류:대수적 위상수학](https://ko.wikipedia.org/wiki/분류:대수적_위상수학 "wikilink")

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