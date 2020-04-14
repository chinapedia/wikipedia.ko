> This article is converted from Wikipedia: [CAT\(κ\) 공간](https://ko.wikipedia.org/wiki/CAT\(κ\)_공간).


[기하학](../Page/기하학.md "wikilink")에서, **CAT(*κ*) 공간**(-空間, )은 [단면 곡률이](../Page/단면_곡률.md "wikilink") 어디서나 \(\kappa\) 이하인 [거리 공간이다](../Page/거리_공간.md "wikilink").

## 정의

임의의 실수 \(\kappa\in\mathbb R\)에 대하여, \(\Sigma_\kappa\)가 [단면 곡률이](../Page/단면_곡률.md "wikilink") \(\kappa\)인 2차원 [연결](../Page/연결_공간.md "wikilink") [단일 연결](https://ko.wikipedia.org/wiki/단일_연결 "wikilink") [공간 형식이라고](https://ko.wikipedia.org/wiki/공간_형식 "wikilink") 하자. 즉, \(\kappa>0\)일 경우 이는 [구](../Page/구_\(기하학\).md "wikilink"), \(\kappa=0\)일 경우는 [유클리드 평면](https://ko.wikipedia.org/wiki/유클리드_평면 "wikilink"), \(\kappa<0\)일 경우는 [쌍곡 평면이다](https://ko.wikipedia.org/wiki/쌍곡_평면 "wikilink"). 이 공간 형식의 [지름](https://ko.wikipedia.org/wiki/지름 "wikilink")은 다음과 같다.

\[\operatorname{diam}\Sigma_\kappa=\begin{cases}\pi/\sqrt\kappa&\kappa>0\\\infty&\kappa\le0\end{cases}\]

**측지선 거리 공간**() \((X,d)\)은 다음 조건을 만족시키는 [길이 거리 공간이다](../Page/길이_거리_공간.md "wikilink").

  - 임의의 두 점 \(x,y\in X\)에 대하여, 두 점을 잇는 [측지선](../Page/측지선.md "wikilink") \(\gamma\)가 존재한다.
    \[\gamma\colon[0,1]\to X\]
    \[\gamma(0)=x\]
    \[\gamma(1)=y\]
    \[d(\gamma(s),\gamma(t))=|t-s|\qquad(s,t\in[0,1])\]

두 점 \(x,y\in X\)를 잇는 측지선을 \(\gamma_{xy}\colon[0,1]\to X\)로 표기하자.

측지선 거리 공간 \((X,d)\) 속의 세 점 \(x,y,z\in X\)에 대하여, 다음 조건들을 모두 만족시키는 \(x',y',z'\in\Sigma_\kappa\)가 존재한다면, 삼각형 \(\triangle xyz\)가 **\(\operatorname{CAT}(\kappa)\) 부등식**을 만족시킨다고 한다.

  - \(d(x,y)=d(x',y')\), \(d(y,z)=d(y',z')\), \(d(z,x)=d(z',x')\)
  - \(\triangle xyz\) 위의 두 점 사이의 거리는 \(\triangle x'y'z'\) 위의 대응하는 하는 두 점 사이의 거리보다 같거나 짧다. 즉, 다음이 성립한다.
      - 임의의 \(s,t\in[0,1]\)에 대하여, \(d(\gamma_{xy}(s),\gamma_{yz}(t))\le d(\gamma_{x'y'}(s),\gamma_{y'z'}(t))\)
      - 임의의 \(s,t\in[0,1]\)에 대하여, \(d(\gamma_{yz}(s),\gamma_{zx}(t))\le d(\gamma_{y'z'}(s),\gamma_{z'x'}(t))\)
      - 임의의 \(s,t\in[0,1]\)에 대하여, \(d(\gamma_{zx}(s),\gamma_{xy}(t))\le d(\gamma_{z'x'}(s),\gamma_{x'y'}(t))\)

측지선 거리 공간 \((X,d)\) 속의 임의의 세 점 \(x,y,z\in X\)에 대하여 \(\operatorname{CAT}(\kappa)\) 부등식이 성립한다면, \((X,d)\)를 **\(\operatorname{CAT}(\kappa)\) 공간**이라고 한다.

[완비](../Page/완비_거리_공간.md "wikilink") \(\operatorname{CAT}(0)\) 공간을 **아다마르 공간**()이라고 한다.

## 성질

임의의 \(\operatorname{CAT}(\kappa)\) 공간은 \(\operatorname{CAT}(\lambda)\) 공간이다 (\(\lambda>\kappa\)). 만약 [거리 공간](../Page/거리_공간.md "wikilink") \(X\)가 모든 \(\lambda>\kappa\)에 대하여 \(\operatorname{CAT}(\lambda)\) 공간이라면, \(X\)는 \(\operatorname{CAT}(\kappa)\) 공간이다.

## 예

모든 (완비일 필요가 없는) [내적 공간은](../Page/내적_공간.md "wikilink") \(\operatorname{CAT}(0)\) 공간이다. 임의의 [노름 공간](../Page/노름_공간.md "wikilink") \(V\)가 어떤 실수 \(\kappa\)에 대하여 \(\operatorname{CAT}(\kappa)\) 공간이라면, \(V\)는 [내적 공간이다](../Page/내적_공간.md "wikilink").

\(n\)차원 [쌍곡 공간은](https://ko.wikipedia.org/wiki/쌍곡_공간 "wikilink") \(\operatorname{CAT}(-1)\) 공간이다.

반지름이 \(r\)인 \(n\)차원 [초구](../Page/초구.md "wikilink") \(\mathbb S^n\)은 \(\operatorname{CAT}(1/r^2)\) 공간이다. (이 초구의 [길이 거리 공간으로서의](../Page/길이_거리_공간.md "wikilink") [지름](https://ko.wikipedia.org/wiki/지름 "wikilink")은 \(\pi r\)이다.)

## 역사

CAT(*κ*) 공간의 개념은 [알렉산드르 다닐로비치 알렉산드로프가](../Page/알렉산드르_다닐로비치_알렉산드로프.md "wikilink") 도입하였다. 알렉산드로프는 이를 원래 "\(\mathfrak R_\kappa\) 영역"으로 명명하였다. 이후 [미하일 그로모프가](https://ko.wikipedia.org/wiki/미하일_그로모프 "wikilink") 1987년의 유명한 논문에서 "CAT(*κ*) 공간"이라는 용어를 도입하였다. 이름에서 "CAT"는 [앙리 카르탕](../Page/앙리_카르탕.md "wikilink")(Cartan) · [알렉산드르 다닐로비치 알렉산드로프](../Page/알렉산드르_다닐로비치_알렉산드로프.md "wikilink")(Александров) · [빅토르 안드레예비치 토포고노프](https://ko.wikipedia.org/wiki/빅토르_안드레예비치_토포고노프 "wikilink")(Топоногов)의 머릿글자를 딴 것이다.

## 참고 문헌

  -
  -
## 외부 링크

  -
[분류:계량기하학](https://ko.wikipedia.org/wiki/분류:계량기하학 "wikilink")