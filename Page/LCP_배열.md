> This article is converted from Wikipedia: [LCP 배열](https://ko.wikipedia.org/wiki/LCP_배열).


<table>
<thead>
<tr class="header">
<th><p>LCP 배열</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/자료구조의_목록" title="wikilink">유형</a></p></td>
</tr>
<tr class="even">
<td><p>고안자 {{!}} colspan="2" {{!}} </p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/빅_오_표기법" title="wikilink">빅 오 표기법에</a> 따른<br />
<a href="../Page/시간_복잡도.md" title="wikilink">시간 복잡도</a></p></td>
</tr>
<tr class="even">
<td></td>
</tr>
<tr class="odd">
<td><p>공간</p></td>
</tr>
<tr class="even">
<td><p>구현</p></td>
</tr>
</tbody>
</table>

LCP배열 (Longest Common Prefix array, 최장 공통 접두사 배열)은 [접미사 배열에서](https://ko.wikipedia.org/wiki/접미사_배열 "wikilink") 이전 접미사와 공통되는 접두사의 길이를 저장한 배열이다.

## LCP 배열을 구현하는 알고리즘

### 나이브한 알고리즘

접미사 배열에서 인접한 두 접미사끼리 직접 비교한다. 한 쌍의 접미사에서 공통되는 접두사의 길이는 \(\mathcal{O}(n)\)에 구할 수 있으므로 총 시간 복잡도는 \(\mathcal{O}(n^2)\)가 된다.

### Kasai의 알고리즘

Kasai의 알고리즘은 접미사 배열이 사전순으로 정렬되어있다는 특성을 이용한 알고리즘이다. 이 알고리즘은 가장 긴 접미사(원본 문자열)부터 길이가 짧아지는 순서대로 접미사를 탐색하며 최장공통접두사의 길이를 구한다. 이 알고리즘의 핵심적인 생각은 현재 탐색하고 있는 접미사의 최장공통접두사 길이가 \(k\)라면 다음에 탐색하는 접미사의 최장공통접두사의 길이는 \(k-1\) 이상이라는 것이다. 이는 다음과 같이 증명할 수 있다.

1\. 최장공통접두사의 길이가 0 이상이라는 것은 자명하므로 \(k\)가 0 또는 1인 경우에 대해서 성립한다.

2\. 만약 \(k\)가 2 이상이면 다음과 같이 표현할 수 있다.

\(S_{prev1} = c_1 C_2 D\)

\(S_{now1} = c_1 C_2 F\)

이때 \(S_{now1}\)은 현재 탐색하고 있는 접미사이고, \(S_{prev1}\)은 접미사배열에서 자신의 이전 인덱스에 있는 접미사이다. 그리고 구성요소인 \(c1\)은 공통된 첫 문자, \(C_2\)는 첫 문자 뒤로 공통된 문자열, \(D\)와 \(F\)는 서로 다른 문자열이다. 또한 \(C_2\)의 길이는 \(k-1\)이 된다.

각 접미사에서 첫번째 문자를 뺀 문자열에는 \('\)를 붙이기로 하자. 따라서 다음과 같다.

\({S'}_{prev1} = C_2 D\)

\({S'}_{now1} = C_2 F\)

이제 다음 탐색에서 최장공통접미사의 길이가 \(k-1\)이상이라는 것을 보일 것이다. 다음으로 탐색할 접미사 \(S_{now2}\)는 길이가 1만큼 짧아졌으므로

\(S_{now2} = {S'}_{now1} = C_2 F\)

이다.

이때 접미사 배열에서 다음과 같은 순서가 성립한다.

\({S'}_{prev1} = C_2 D\)

\({S}_{prev2} = C_2 E\)

\({S}_{now2} = C_2 F\)

\(S_{now1}\)과 \(S_{prev1}\)는 사전순으로 정렬되어있었으므로, 첫번째 문자를 뺀 \({S'}_{now1}\)과 \({S'}_{prev1}\)에 대해서도 순서관계가 성립하게 된다. 즉, 항상 \({S'}_{prev1}\)는 \({S'}_{now1}\)보다 앞선 인덱스에 있게 된다. 또한 \({S'}_{prev1}\)의 인덱스는 항상 \({S'}_{now1} = S_{now2}\)*의 인덱스*\(- 1\)보다 작으므로 \(S_{prev2}\)는 항상 \(S_{now2}\)와 \({S'}_{prev1}\) 사이에 있게 된다. 이때, 접미사 배열은 모든 접미사에 대해 사전순으로 정렬된 배열이기 때문에 \({S'}_{prev1} \leq S_{prev2} < S_{now2}\)가 성립하므로 \(S_{prev2}\) 역시 \(C_2\)를 공통으로 가지게 된다. 즉, 최장공통접미사의 길이는 \(C_2\)의 길이인 \(k-1\)보다 길다.

[분류:배열](https://ko.wikipedia.org/wiki/분류:배열 "wikilink")