> This article is converted from Wikipedia: [Tf-idf](https://ko.wikipedia.org/wiki/Tf-idf).


**TF-IDF**(Term Frequency - Inverse Document Frequency)는 [정보 검색과](../Page/정보_검색.md "wikilink") [텍스트 마이닝에서](https://ko.wikipedia.org/wiki/텍스트_마이닝 "wikilink") 이용하는 가중치로, 여러 문서로 이루어진 문서군이 있을 때 어떤 단어가 특정 문서 내에서 얼마나 중요한 것인지를 나타내는 [통계](https://ko.wikipedia.org/wiki/통계 "wikilink")적 수치이다. 문서의 [핵심어](https://ko.wikipedia.org/wiki/핵심어 "wikilink")를 추출하거나, [검색 엔진에서](https://ko.wikipedia.org/wiki/검색_엔진 "wikilink") 검색 결과의 순위를 결정하거나, 문서들 사이의 비슷한 정도를 구하는 등의 용도로 사용할 수 있다.

TF(단어 빈도, term frequency)는 특정한 단어가 문서 내에 얼마나 자주 등장하는지를 나타내는 값으로, 이 값이 높을수록 문서에서 중요하다고 생각할 수 있다. 하지만 단어 자체가 문서군 내에서 자주 사용 되는 경우, 이것은 그 단어가 흔하게 등장한다는 것을 의미한다. 이것을 DF(문서 빈도, document frequency)라고 하며, 이 값의 역수를 IDF(역문서 빈도, inverse document frequency)라고 한다. TF-IDF는 TF와 IDF를 곱한 값이다.

IDF 값은 문서군의 성격에 따라 결정된다. 예를 들어 '[원자](../Page/원자.md "wikilink")'라는 낱말은 일반적인 문서들 사이에서는 잘 나오지 않기 때문에 IDF 값이 높아지고 문서의 핵심어가 될 수 있지만, 원자에 대한 문서를 모아놓은 문서군의 경우 이 낱말은 상투어가 되어 각 문서들을 세분화하여 구분할 수 있는 다른 낱말들이 높은 가중치를 얻게 된다.

## 수학적 설명

TF-IDF는 단어 빈도와 역문서 빈도의 곱이다. 두 값을 산출하는 방식에는 여러 가지가 있다. **단어 빈도** tf(*t*,*d*)의 경우, 이 값을 산출하는 가장 간단한 방법은 단순히 문서 내에 나타나는 해당 단어의 총 빈도수를 사용하는 것이다. 문서 d 내에서 단어 t의 총 빈도를 f(*t*,*d*)라 할 경우, 가장 단순한 tf 산출 방식은 tf(*t*,*d*) = f(*t*,*d*)로 표현된다. 그 밖에 TF값을 산출하는 방식에는 다음과 같은 것들이 있다.\[1\]

  - [불린](https://ko.wikipedia.org/wiki/불린_자료형 "wikilink") 빈도: tf(*t*,*d*) = *t*가 *d*에 한 번이라도 나타나면 1, 아니면 0;
  - [로그](../Page/로그.md "wikilink") 스케일 빈도: tf(*t*,*d*) = log (f(*t*,*d*) + 1);
  - 증가 빈도: 최빈 단어를 분모로 target 단어의 TF를 나눈 값으로, 일반적으로는 문서의 길이가 상대적으로 길 경우, 단어 빈도값을 조절하기 위해 사용한다.

\[\mathrm{tf}(t,d) = 0.5 + \frac{0.5 \times \mathrm{f}(t, d)}{\max\{\mathrm{f}(w, d):w \in d\}}\]

**역문서 빈도**는 한 단어가 문서 집합 전체에서 얼마나 공통적으로 나타나는지를 나타내는 값이다. 전체 문서의 수를 해당 단어를 포함한 문서의 수로 나눈 뒤 [로그](../Page/로그.md "wikilink")를 취하여 얻을 수 있다.

\[\mathrm{idf}(t, D) =  \log \frac{|D|}{|\{d \in D: t \in d\}|}\]

  - \(|D|\): [문서 집합 D의 크기](../Page/집합의_크기.md "wikilink"), 또는 전체 문서의 수
  - \(|\{d \in D: t \in d\}|\) : 단어 \(t\)가 포함된 문서의 수.(즉, \(\mathrm{tf}(t,d) \neq 0\)). 단어가 전체 [말뭉치](../Page/말뭉치.md "wikilink") 안에 존재하지 않을 경우 이는 분모가 0이 되는 결과를 가져온다. 이를 방지하기 위해 \(1 + |\{d \in D: t \in d\}|\)로 쓰는 것이 일반적이다.

TF-IDF는 다음과 같이 표현된다.

\[\mathrm{tfidf}(t,d,D) = \mathrm{tf}(t,d) \times \mathrm{idf}(t, D)\]

특정 문서 내에서 단어 빈도가 높을 수록, 그리고 전체 문서들 중 그 단어를 포함한 문서가 적을 수록 TF-IDF값이 높아진다. 따라서 이 값을 이용하면 모든 문서에 흔하게 나타나는 단어를 걸러내는 효과를 얻을 수 있다. IDF의 로그 함수 안의 값은 항상 1 이상이므로, IDF값과 TF-IDF값은 항상 0 이상이 된다. 특정 단어를 포함하는 문서들이 많을 수록 로그 함수 안의 값이 1에 가까워지게 되고, 이 경우 IDF값과 TF-IDF값은 0에 가까워지게 된다.

## 참고자료

  - Salton G. and McGill, M. J. 1983 *Introduction to modern information retrieval*. McGraw-Hill, .

## 각주

<references/>

[분류:벡터 공간 모델](https://ko.wikipedia.org/wiki/분류:벡터_공간_모델 "wikilink") [분류:자연어 처리](https://ko.wikipedia.org/wiki/분류:자연어_처리 "wikilink") [분류:통계적 자연어 처리](https://ko.wikipedia.org/wiki/분류:통계적_자연어_처리 "wikilink")

1.