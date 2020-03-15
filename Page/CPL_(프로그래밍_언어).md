> This article is converted from Wikipedia: [CPL \( \)](https://ko.wikipedia.org/wiki/CPL_\(_\)).


**CPL**(Combined Programming Language, 이전 명칭: Cambridge Programming Language)은 1960년대 초에 개발된 [다중 패러다임](https://ko.wikipedia.org/wiki/프로그래밍_패러다임 "wikilink") [프로그래밍 언어이다](https://ko.wikipedia.org/wiki/프로그래밍_언어 "wikilink").

## 설계

CPL(Combined Programming Language)\[1\]은 [케임브리지 대학교](https://ko.wikipedia.org/wiki/케임브리지_대학교 "wikilink") 수학 연구소와 [런던 대학교](https://ko.wikipedia.org/wiki/런던_대학교 "wikilink") 컴퓨터 유닛이 1960년대에 공동 개발하였고, 이에 따라 CPL은 "케임브리지 플러스 런던"(Cambridge Plus London)이라는 별명을 얻었다.\[2\]

## 예

Peter Norvig가 공식화한 함수 MAX:\[3\]

    Max(Items, ValueFunction) = value of
    § (Best, BestVal) = (NIL, -∞)
    while Items do §
    (Item, Val) = (Head(Items), ValueFunction(Head(Items)))
    if Val > BestVal then (Best, BestVal) := (Item, Val)
    Items := Rest(Items) §⃒
    result is Best §⃒

## 참고문헌

  - Collected papers of Christopher Strachey, section pertaining to CPL, archived at the Bodleian Library, Oxford; [CSAC 71.1.80/C.136-C.184](http://www.nationalarchives.gov.uk/a2a/records.aspx?cat=161-csac71180&cid=3-5-1#3-5-1)
  - D. W. Barron, J. N. Buxton, D. F. Hartley, E. Nixon, and C. Strachey. ["The main features of CPL"](http://comjnl.oxfordjournals.org/cgi/reprint/6/2/134) *The Computer Journal* **6**:2:134-143 (1963), available [online](http://www.math.bas.bg/~bantchev/place/cpl/features.pdf).

## 각주

[분류:1963년 도입](https://ko.wikipedia.org/wiki/분류:1963년_도입 "wikilink") [분류:절차적 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:절차적_프로그래밍_언어 "wikilink") [분류:구조적 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:구조적_프로그래밍_언어 "wikilink")

1.  \[\]
2.
3.