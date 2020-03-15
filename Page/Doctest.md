> This article is converted from Wikipedia: [Doctest](https://ko.wikipedia.org/wiki/Doctest).


**doctest**는 [파이썬](https://ko.wikipedia.org/wiki/파이썬 "wikilink") 언어의 표준 라이브러리로 표준 파이썬 인터프리터 셸 입출력을 [주석문자열](https://ko.wikipedia.org/wiki/주석문자열 "wikilink")에 복사 첨부함으로부써 간단하게 프로그램 시험예를 적용시킬 수 있게 해준다.

## 사용 예

### 시험 겸용 주석문자열이 어떤 함수의 주석문자열 안에 내장

``` python
# -*- coding:cp949 -*-

def list_to_0_index(lst):
    """아래의 링크에 주어진 문제의 답임:
    http://rgrig.blogspot.com/2005/11/writing-readable-code.html

    '어떤 리스트 lst가 주어졌을 때, 각 요소가 처음 나타나는 인덱스를 구하라.
    그래서 리스트 x = [0, 1, 4, 2, 4, 1, 0, 2] 는 y = [0, 1, 2, 3, 2, 1, 0, 3]로 변환된다.
    모든 i에 대해 xyi = xi 이다. 프로그래밍 언어와 데이터 표현 형식은 원하는대로 선택하라'

    >>> x = [0, 1, 4, 2, 4, 1, 0, 2]
    >>> list_to_0_index(x)
    [0, 1, 2, 3, 2, 1, 0, 3]
    >>>
    """

    return [lst.index(i) for i in lst]

def _test():
    import doctest
    doctest.testmod(verbose = True)

if "__main__" == __name__ :
    _test()
```

## 비판적 의견

개발자에 따라서는 독테스트 doctest 를 [단위 테스트](../Page/유닛_테스트.md "wikilink") unittest 처럼 사용하는 데 반대하는 의견도 있다. 독테스트는 주석문자열 docstring 안에 구현되는데, 이 주석문자열은 많은 파이썬 개발 환경에서 툴팁으로 사용된다.\[1\] 따라서 함수의 사용법에 대해 초심자들이 살펴볼 가능성이 높은데, 문제가 될 수 있는 사용례 50개가 주석문자열에 나타난다면 과연 바람직할 것인가? 라는 주장이 주요한 근거가 되고 있다.

## 같이 보기

  - [파이썬](https://ko.wikipedia.org/wiki/파이썬 "wikilink")
  - [소프트웨어 테스트](../Page/소프트웨어_테스트.md "wikilink")
  - [유닛 테스트](../Page/유닛_테스트.md "wikilink")

## 참고

<references/>

[분류:소프트웨어 테스트](https://ko.wikipedia.org/wiki/분류:소프트웨어_테스트 "wikilink") [분류:파이썬](https://ko.wikipedia.org/wiki/분류:파이썬 "wikilink") [분류:소프트웨어 테스트 도구](https://ko.wikipedia.org/wiki/분류:소프트웨어_테스트_도구 "wikilink")

1.  [처음만나는 파이썬 프로그래밍](http://juehan.github.com/DiveIntoPython3_Korean_Translation/your-first-python-program.html)