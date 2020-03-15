> This article is converted from Wikipedia: [EXPSPACE](https://ko.wikipedia.org/wiki/EXPSPACE).


[계산 복잡도 이론에서](https://ko.wikipedia.org/wiki/계산_복잡도_이론 "wikilink") **EXPSPACE**는 [결정론적 튜링 기계가](https://ko.wikipedia.org/wiki/결정론적_튜링_기계 "wikilink") [\({\color{Blue}O}(2^{p(n)})\)](https://ko.wikipedia.org/wiki/대문자_O_표기법 "wikilink") 공간을 써서 풀 수 있는 [판정 문제의](https://ko.wikipedia.org/wiki/판정_문제 "wikilink") [집합](https://ko.wikipedia.org/wiki/집합 "wikilink")이다. 여기서 \(p(n)\)은 \(n\)에 대한 다항함수이다. (일부에서는 \(p(n)\)을 [선형 함수로](https://ko.wikipedia.org/wiki/선형_함수 "wikilink") 제한하기도 하지만, 대부분은 그러한 경우를 **[ESPACE](https://ko.wikipedia.org/wiki/ESPACE "wikilink")**로 정의한다.)

**[DSPACE](https://ko.wikipedia.org/wiki/DSPACE "wikilink")**에 대한 식으로 정리하면 아래와 같다.

\[\mathsf{EXPSPACE} = \bigcup_{k\in\mathbb{N}} \mathsf{DSPACE}(2^{n^k})\]

어떤 판정 문제가 EXPSPACE이고, EXPSPACE에 있는 모든 문제가 그 문제로 [다항 시간 다대일 환산될](https://ko.wikipedia.org/wiki/다항_시간_다대일_환산 "wikilink") 수 있으면, **EXPSPACE-완전**이라고 한다. 다시 말해서, 한 인스턴스를 다른 똑같은 해의 인스턴스로 변환하는 다항 시간 [알고리즘](https://ko.wikipedia.org/wiki/알고리즘 "wikilink")이 존재한다는 뜻이다. EXPSPACE-완전 문제는 EXPSPACE 문제 가운데 가장 어려운 문제들일 것으로 추정되고 있다.

**[PSPACE](../Page/PSPACE.md "wikilink")**, **[NP](https://ko.wikipedia.org/wiki/NP_\(complexity\) "wikilink")**, **[P](https://ko.wikipedia.org/wiki/P_\(complexity\) "wikilink")**는 모두 EXPSPACE의 진부분집합이다. **[EXPTIME](../Page/EXPTIME.md "wikilink")** 역시 EXPSPACE의 진부분집합이라는 설이 유력하다.

**EXPSPACE-complete**의 예로는 두 [정규 표현식이](https://ko.wikipedia.org/wiki/정규_표현식 "wikilink") 다른 언어를 나타내는지 알아내는 문제가 있다. 여기서 표현식은 합집합, [연결 (정규 표현식)](https://ko.wikipedia.org/wiki/연결_\(정규_표현식\) "wikilink"), [클레이니 스타](https://ko.wikipedia.org/wiki/클레이니_스타 "wikilink") (0회 이상 반복), 제곱 (표현식 2회 반복) 네 연산자로 제한한다.

[클레이니 스타가](https://ko.wikipedia.org/wiki/클레이니_스타 "wikilink") 없다면 이 문제는 **[NEXPTIME](https://ko.wikipedia.org/wiki/NEXPTIME "wikilink")-완전** 문제가 된다. [NEXPTIME](https://ko.wikipedia.org/wiki/NEXPTIME "wikilink")-완전은 비결정론적 튜링 기계로 정의한다는 점을 빼면 [EXPTIME](../Page/EXPTIME.md "wikilink")-완전과 비슷하다.

베르만은 [1980년](https://ko.wikipedia.org/wiki/1980년 "wikilink")에 덧셈과 비교만 포함하는 실수 [일차 논리식을](https://ko.wikipedia.org/wiki/일차_논리 "wikilink") 검증하는 문제가 **EXPSPACE**라는 것을 보였다. (이 논리식은 곱셈을 포함하지 않는다)

## 더 보기

  - [게임 복잡도](https://ko.wikipedia.org/wiki/게임_복잡도 "wikilink")

## 참고문헌

  - L. Berman, *The complexity of logical theories*, Theoretical Computer Science Vol. 11 pp. 71–78, 1980.

  -
[분류:복잡도 종류](https://ko.wikipedia.org/wiki/분류:복잡도_종류 "wikilink")