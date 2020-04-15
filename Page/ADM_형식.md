> This article is converted from Wikipedia: [ADM 형식](https://ko.wikipedia.org/wiki/ADM_형식).


**아노윗-데세르-미스너 수식 체계**(Arnowitt-Deser-Misner數式體系, , 약자 **ADM 수식 체계**)는 [일반 상대성 이론을](https://ko.wikipedia.org/wiki/일반_상대성_이론 "wikilink") [해밀턴 역학으로](../Page/해밀턴_역학.md "wikilink") 표현하는 방법이다.\[1\]\[2\]\[3\]\[4\]\[5\]\[6\] [시공간](https://ko.wikipedia.org/wiki/시공간 "wikilink")에 공간적 [엽층](../Page/엽층.md "wikilink")을 준 뒤, 엽층의 각 잎의 (시공의 부분 [다양체](../Page/다양체.md "wikilink")로서) 유도된 [계량 텐서에](https://ko.wikipedia.org/wiki/계량_텐서 "wikilink") 대하여 [일반화 운동량을](../Page/일반화_운동량.md "wikilink") 정의한다. 잎의 계량 텐서 및 그 운동량에 포함되지 않는 ([질량 껍질](https://ko.wikipedia.org/wiki/질량_껍질 "wikilink") 밖) 자유도는 [라그랑주 승수](https://ko.wikipedia.org/wiki/라그랑주_승수 "wikilink") 꼴로 나타나, 이론에 [제약](../Page/제약.md "wikilink")을 준다.

## 전개

그리스 문자 첨자 \(\mu,\nu,\dots=0,1,\dots,D\)는 \(D+1\)차원 시공간을, 로마자 첨자 \(i,j,\dots=1,\dots,D\)는 \(D\)차원 공간만을 나타낸다. 여기서는 −+++ [계량 부호수를](https://ko.wikipedia.org/wiki/계량_부호수 "wikilink") 쓴다. 편의상 \(c=1\)로 놓자.

### 계량 텐서의 분해

\(D+1\)차원에서, [일반 상대성 이론의](https://ko.wikipedia.org/wiki/일반_상대성_이론 "wikilink") 동적 변수는 대칭 텐서인 [계량 텐서](https://ko.wikipedia.org/wiki/계량_텐서 "wikilink") \(g^{(D+1)}_{\mu\nu}\)의 \((D+1)(D+2)/2\)개의 성분들이다. 그러나 일반 상대성 이론은 임의의 [미분 동형 사상을](https://ko.wikipedia.org/wiki/미분_동형_사상 "wikilink") [게이지 대칭으로](https://ko.wikipedia.org/wiki/게이지_대칭 "wikilink") 가지며, 이는 (국소적으로) \(x^\mu\mapsto x^\mu+\delta x^\mu\)와 같은 꼴이므로, \(g^{(D+1)}_{\mu\nu}\)의 성분 가운데 \(D+1\)개는 [게이지 변환을](https://ko.wikipedia.org/wiki/게이지_변환 "wikilink") 통해 흡수될 수 있으며, 따라서 실제 동적인 장들은 그 가운데

\[\frac12(D+1)(D+2)-(D+1)=\frac12D(D+1)\] 개이다. 즉, 계량 텐서를 다음과 같은 꼴로 표시할 수 있다.\[7\]

\[g^{(D+1)}_{\mu\nu}=\begin{pmatrix}
g^{ij}N_iN_j-N^2&N_i\\
N_i&g_{ij}
\end{pmatrix}\]

\[g_{(D+1)}^{\mu\nu}=\begin{pmatrix}
-1/N^2&g^{ij}N_jN^2\\
g^{ij}N_j/N^2&g^{ij}-g^{im}g^{jn}N_mN_n/N^2
\end{pmatrix}\] 여기서 [보조장](../Page/보조장.md "wikilink") \(N\)과 \((N_i)_{i=1,\dots,D}\)는 각각 **경과장**(經過場, ) 및 **이동장**(移動場, )이라고 불린다. \((g^{ij})_{i,j=1,\dots,D})\)는 \((g_{ij})_{i,j=1,\dots,D}\)의 [역행렬](https://ko.wikipedia.org/wiki/역행렬 "wikilink")이다(특히, \((g^{(D+1)}_{\mu\nu})_{\mu,\nu=0,\dots,D})\)의 역행렬의 성분이 아니다). \(g_{(D+1)}^{0,0}\)는 \((g^{(D+1)}_{\mu\nu})_{\mu,\nu=0,\dots,D}\)의 역행렬의 한 성분이다.

이 경우, \(D+1\)차원 계량 텐서의 [행렬식](../Page/행렬식.md "wikilink")은 다음과 같다.\[8\]

\[-\det(g_{\mu\nu})=N^2\det(g_{ij})\] 즉, 경과장 \(N\)은 \(D+1\)차원 계량으로 측정한 \(D+1\)차원 초부피 원소([야코비 행렬식](https://ko.wikipedia.org/wiki/야코비_행렬식 "wikilink"))와 \(D\)차원 계량으로 측정한 \(D\)차원 부피 원소(야코비 행렬식)의 비이다.

이러한 분해는 [전자기 퍼텐셜](https://ko.wikipedia.org/wiki/전자기_퍼텐셜 "wikilink") \(A_\mu=(A_0,A_i)\)의 분해와 마찬가지다. 전자기학에서 \(A_0\)가 게이지 변환에 의하여 [라그랑주 승수](https://ko.wikipedia.org/wiki/라그랑주_승수 "wikilink") [보조장](../Page/보조장.md "wikilink")이 되는 것처럼, \(N\)과 \(N_i\) 역시 마찬가지 역할을 한다.

### 운동량과 작용

[일반 상대성 이론은](https://ko.wikipedia.org/wiki/일반_상대성_이론 "wikilink") [아인슈타인-힐베르트 작용으로](https://ko.wikipedia.org/wiki/아인슈타인-힐베르트_작용 "wikilink") 나타낼 수 있다.

\[16\pi G\mathcal L=\sqrt{-\det(g_{\mu\nu}^{(D+1)})}R^{(D+1)}\] 여기서 \(g_{\mu\nu}\)는 [계량 텐서](https://ko.wikipedia.org/wiki/계량_텐서 "wikilink"), \(R^{(D+1)}\)은 \(g_{\mu\nu}^{(D+1)}\)로 계산한 [리치 스칼라다](https://ko.wikipedia.org/wiki/리치_스칼라 "wikilink").

이제 편의상 \(D+1=3+1\)인 경우만을 생각하자. \(g_{ij}\)에 대한 [일반화 운동량](../Page/일반화_운동량.md "wikilink") \(\pi^{ij}\)를 계산하면 다음과 같다.

\[\pi^{ij}=\frac{\delta\mathcal L}{\delta(\dot g_{ij})}=\frac1{16\pi G}\sqrt{-\det g_{\mu\nu}} \left(\Gamma^0_{pq} - g_{pq} \Gamma^0_{rs}g^{rs} \right) g^{ip}g^{jq}\] \(g_{ij}\)에 대하여 [해밀토니언](https://ko.wikipedia.org/wiki/해밀토니언 "wikilink")을 정의하자. 그렇다면 작용은 다음과 같다.

\[16\pi G\mathcal L=-g_{ij}\dot\pi^{ij}-NH-N_iP^i+\partial_i(\cdots)^i\] 여기서

\[H=-\frac1{16\pi G}\sqrt{-\det g_{ij}}\left(R+\frac1{\det g_{ij}}\left(\frac12(\det\pi^{ij})^2-\pi^{ij}\pi_{ij}\right)\right)\]

\[P^i=-\frac1{8\pi G}\nabla_j\pi^{ij}\] 이다. 즉 \(N\)과 \(N_i\)는 [라그랑주 승수가](https://ko.wikipedia.org/wiki/라그랑주_승수 "wikilink") 되며, 그 [운동 방정식에](https://ko.wikipedia.org/wiki/운동_방정식 "wikilink") 따라 \(H=P^i=0\)이다.

## 성질

### 운동 방정식

\(g_{ij}\) 및 \(\pi^{ij}\)에 대한 [오일러-라그랑주 방정식은](../Page/오일러-라그랑주_방정식.md "wikilink") 다음과 같다.

\[\dot g_{ij} = 2Ng^{-1/2} \left( \pi_{ij} - \frac12 \pi g_{ij} \right) + 2\nabla_{(i;j)}\]

\[\dot\pi^{ij} = -N\sqrt{\det(g_{ij})} ( R^{ij} - \frac12 R g^{ij} ) + \frac12 N(\det(g_{ij}))^{-1/2}g^{ij} ( \pi^{mn}\pi_{mn} - \frac12 \pi^2) - 2Ng^{-1/2} ( \pi^{in}\pi_{n}{}^{j} - \frac12\pi\pi^{ij} )\]

\[-\sqrt{\det(g_{ij})}(\nabla^{i}\nabla^{j}N -g^{ij}\nabla^2N) + \nabla_{n}( \pi^{ij}N^{n} ) -2\pi^{n(i}\nabla_nN^{j)}\]

[보조장](../Page/보조장.md "wikilink")들에 대한 운동 방정식은 다음과 같다.

\[H=0\]

\[P^i=0\] 이들은 [위상 공간의](../Page/위상_공간_\(물리학\).md "wikilink") 제약을 나타내며, 전자기장의 가우스 법칙 제약과 유사하다. 보조장 \(N\) 및 \(N_i\) 자체는 임의로 값을 줄 수 있다. 이는 [일반 상대성 이론에서](https://ko.wikipedia.org/wiki/일반_상대성_이론 "wikilink") [미분 동형 사상](https://ko.wikipedia.org/wiki/미분_동형_사상 "wikilink") 대칭이 [게이지 대칭이기](https://ko.wikipedia.org/wiki/게이지_대칭 "wikilink") 때문이다.

### 위상 공간

일반적으로, \(d+1\)차원 시공간 \(\Sigma\times\mathbb R\)에서, ADM 수식 체계에 의한, [일반 상대성 이론의](https://ko.wikipedia.org/wiki/일반_상대성_이론 "wikilink") [위상 공간은](../Page/위상_공간_\(물리학\).md "wikilink") \(\Sigma\) 위의 [매끄러운 올다발의](https://ko.wikipedia.org/wiki/매끄러운_올다발 "wikilink") [매끄러운 단면의](https://ko.wikipedia.org/wiki/매끄러운_단면 "wikilink") 공간이다. 이 올다발의 올의 차원은 \((d+1)(d-2)\)이다.\[9\] 이는 다음과 같이 얻어진다.

  -
    {| class=wikitable

\! 설명 \!\! 성분 |- | 계량 텐서 \(g_{ij}\) 및 그 일반화 운동량 || \(d(d+1)\) |- | 에너지 제약 \(H=0\) 및 그 게이지 조건 || −2 |- | 운동량 제약 \(P^i = 0\) 및 그 게이지 조건 || \(-2d\) |- \! 계 || \(d(d+1) - 2-2d = d^2-d-2 = (d+1)(d-2)\) |}

## 역사

[섬네일](https://ko.wikipedia.org/wiki/파일:ArnowittDeserMisner2009_01.jpg "wikilink") 리처드 루이스 아노윗(, 1928\~2014) · 스탠리 데세르(, 1931\~) · 찰스 미스너(, 1932\~)가 1959년\~1961년에 도입하였다.\[10\]\[11\]\[12\]\[13\]\[14\]\[15\]\[16\]\[17\]\[18\]\[19\]

## 참고 문헌

[분류:일반 상대성이론](https://ko.wikipedia.org/wiki/분류:일반_상대성이론 "wikilink")

1.
2.
3.   영역
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