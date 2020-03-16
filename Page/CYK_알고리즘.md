> This article is converted from Wikipedia: [CYK ](https://ko.wikipedia.org/wiki/CYK_).


**CYK 알고리즘**(Cocke-Younger-Kasami 알고리즘, CYK Algorithm)은 특정한 [문자열](https://ko.wikipedia.org/wiki/문자열 "wikilink")에 대해, 그 문자열이 특정한 [문맥 자유 문법에](https://ko.wikipedia.org/wiki/문맥_자유_문법 "wikilink") 속하는지를 판단하고, 또한 어떠한 방식으로 생성되는지를 판단하는 [파싱](https://ko.wikipedia.org/wiki/파싱 "wikilink") 알고리즘이다. 이 알고리즘은 [동적 계획법을](../Page/동적_계획법.md "wikilink") 사용하며, [상향식 파싱](https://ko.wikipedia.org/wiki/상향식_파싱 "wikilink") 구조를 가지고 있다.

기본적으로 CYK 알고리즘에서는 [촘스키 정규 형식으로](https://ko.wikipedia.org/wiki/촘스키_정규_형식 "wikilink") 표현된 문맥 자유 문법을 사용하지만, 모든 문맥 자유 문법은 촘스키 정규 형식으로 변환이 가능하기 때문에 CYK 알고리즘을 사용할 수 있다.

문자열의 길이가 \(n\)일 때, CYK 알고리즘은 [Θ](https://ko.wikipedia.org/wiki/대문자_O_표기법 "wikilink")(n<sup>3</sup>)의 시간 복잡도를 가진다. 이것은 현재 모든 문맥 자유 문법을 파싱할 수 있는 가장 효율적인 알고리즘이다. (CYK 알고리즘보다 효율적으로 동작하는 몇몇 알고리즘이 있지만, 그 알고리즘은 특정한 문법의 경우에만 사용이 가능하다.)

## 알고리즘

membership 문제를 푸는 CYK 알고리즘은 아래와 같다:

**`Let`**` the input string consist of `*`n`*` letters, `*`a`*<sub>`1`</sub>` ... `*`a`*<sub>*`n`*</sub>`.`
**`Let`**` the grammar contain `*`r`*` terminal and nonterminal symbols `*`R`*<sub>`1`</sub>` ... `*`R`*<sub>*`r`*</sub>`.`
`This grammar contains the subset R`<sub>`s`</sub>` which is the set of start symbols.`
**`Let`**` P[n,n,r] be an array of booleans. Initialize all elements of P to false.`
**`For``   ``each`**` i = 1 to n`
`  `**`For``   ``each`**` unit production R`<sub>`j`</sub>` -> a`<sub>`i`</sub>`, `**`set`**` P[i,1,j] = true.`
**`For``   ``each`**` i = 2 to n -- Length of span`
`  `**`For``   ``each`**` j = 1 to n-i+1 -- Start of span`
`    `**`For``   ``each`**` k = 1 to i-1 -- Partition of span`
`      `**`For``   ``each`**` production R`<sub>`A`</sub>` -> R`<sub>`B`</sub>` R`<sub>`C`</sub>
`        `**`If`**` P[j,k,B] and P[j+k,i-k,C] `**`then`**` set P[j,i,A] = true`
**`If`**` any of P[1,n,x] is true (x is iterated over the set s, where s are all the indices for R`<sub>`s`</sub>`)`
`  `**`Then`**` string is member of language`
`  `**`Else`**` string is not member of language`

## 예

예시 문법은 다음과 같다.

  -
    <math chem>\\begin{align}

\\ce{S} & \\ \\ce{-\> NP\\ VP}\\\\ \\ce{VP} & \\ \\ce{-\> VP\\ PP}\\\\ \\ce{VP} & \\ \\ce{-\> V\\ NP}\\\\ \\ce{VP} & \\ \\ce{-\> eats}\\\\ \\ce{PP} & \\ \\ce{-\> P\\ NP}\\\\ \\ce{NP} & \\ \\ce{-\> Det\\ N}\\\\ \\ce{NP} & \\ \\ce{-\> she}\\\\ \\ce{V} & \\ \\ce{-\> eats}\\\\ \\ce{P} & \\ \\ce{-\> with}\\\\ \\ce{N} & \\ \\ce{-\> fish}\\\\ \\ce{N} & \\ \\ce{-\> fork}\\\\ \\ce{Det} & \\ \\ce{-\> a} \\end{align}</math>

## 참고 문헌

  - [John Cocke](https://ko.wikipedia.org/wiki/John_Cocke "wikilink") and Jacob T. Schwartz (1970). Programming languages and their compilers: Preliminary notes. Technical report, Courant Institute of Mathematical Sciences, New York University.
  - T. Kasami (1965). An efficient recognition and syntax-analysis algorithm for context-free languages. Scientific report AFCRL-65-758, Air Force Cambridge Research Lab, Bedford, MA.
  - Daniel H. Younger (1967). Recognition and parsing of context-free languages in time *n*<sup>3</sup>. *Information and Control* 10(2): 189–208.

[분류:파싱 알고리즘](https://ko.wikipedia.org/wiki/분류:파싱_알고리즘 "wikilink")