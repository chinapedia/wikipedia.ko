> This article is converted from Wikipedia: [ABC \( \)](https://ko.wikipedia.org/wiki/ABC_\(_\)).


**ABC**는 범용의 [명령형](https://ko.wikipedia.org/wiki/명령형_프로그래밍 "wikilink") 컴퓨터 [프로그래밍 언어이면서](https://ko.wikipedia.org/wiki/프로그래밍_언어 "wikilink") 프로그래밍 환경이다. ABC는 [네덜란드](https://ko.wikipedia.org/wiki/네덜란드 "wikilink") [CWI](https://ko.wikipedia.org/wiki/CWI "wikilink")(Centrum voor Wiskunde en Informatica)의 [레오 회르츠](https://ko.wikipedia.org/wiki/레오_회르츠 "wikilink"), [람베르트 메르텐스](https://ko.wikipedia.org/wiki/람베르트_메르텐스 "wikilink"), [스티븐 펨버턴이](https://ko.wikipedia.org/wiki/스티븐_펨버턴 "wikilink") 개발하였다. ABC는 상호작용적이고 [구조적](https://ko.wikipedia.org/wiki/구조적 "wikilink")인 [고수준 언어로](https://ko.wikipedia.org/wiki/고수준_언어 "wikilink"), 배우고 쓰기 쉽고, [베이직](https://ko.wikipedia.org/wiki/베이직 "wikilink"), [파스칼](https://ko.wikipedia.org/wiki/파스칼_\(프로그래밍_언어\) "wikilink") 등을 대체할 목적으로 만들어졌다.

ABC는 수, 문자열, 리스트, 순서조, 배열의 다섯 가지 데이터 형을 가지고 있으며, 변수 선언은 필요 없다. [하향식 프로그래밍을](https://ko.wikipedia.org/wiki/하향식_프로그래밍 "wikilink") 지원하며 블록 구조는 들여쓰기로 이루어진다. [무한정밀도 연산을](https://ko.wikipedia.org/wiki/무한정밀도_연산 "wikilink") 지원하며 [리스트와](https://ko.wikipedia.org/wiki/리스트_\(컴퓨팅\) "wikilink") [문자열](https://ko.wikipedia.org/wiki/문자열 "wikilink")의 길이에 제한이 없다.

ABC는 현재 [인터프리터](https://ko.wikipedia.org/wiki/인터프리터 "wikilink")/[컴파일러](https://ko.wikipedia.org/wiki/컴파일러 "wikilink") 모두 가능하며, [유닉스](https://ko.wikipedia.org/wiki/유닉스 "wikilink"), [도스](https://ko.wikipedia.org/wiki/도스 "wikilink"), [아타리](https://ko.wikipedia.org/wiki/아타리 "wikilink"), [매킨토시](https://ko.wikipedia.org/wiki/매킨토시 "wikilink") 용이 개발되어 있다.

ABC는 [파이썬](https://ko.wikipedia.org/wiki/파이썬 "wikilink") 언어에 큰 영향을 끼쳤다. 특히 블록 구조를 들여쓰는 것은 그 직접적인 영향이다. 파이썬의 개발자인 [귀도 반 로섬은](../Page/귀도_반_로섬.md "wikilink") 1980년대 초반 몇 년 동안 CWI에서 ABC 언어 개발에 참여하였다.

## 프로그램 예

무한정밀도 연산을 지원한다.

`>>> WRITE 2**1000`
`107150860718626732094842504906000181056140481170553360744375038837`
`035105112493612249319837881569585812759467291755314682518714528569`
`231404359845775746985748039345677748242309854210746050623711418779`
`541821530464749835819412673987675591655439460770629145711964776865`
`42167660429831652624386837205668069376`
`>>> PUT 1/(2**1000) IN x`
`>>> WRITE 1 + 1/x`
`107150860718626732094842504906000181056140481170553360744375038837`
`035105112493612249319837881569585812759467291755314682518714528569`
`231404359845775746985748039345677748242309854210746050623711418779`
`541821530464749835819412673987675591655439460770629145711964776865`
`42167660429831652624386837205668069377`

함수 `words`는 document에 있는 모든 워드들을 중복되지 않게 모아서 돌려준다.

    HOW TO RETURN words document:
    PUT {} IN collection
    FOR line IN document:
      FOR word IN split line:
        IF word not.in collection:
          INSERT word IN collection
    RETURN collection

## 외부 링크

  - [A Short Introduction to the ABC Language](http://www.cwi.nl/~steven/abc/)

[분류:절차적 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:절차적_프로그래밍_언어 "wikilink") [분류:교육용 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:교육용_프로그래밍_언어 "wikilink")