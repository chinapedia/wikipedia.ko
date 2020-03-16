> This article is converted from Wikipedia: [Typedef](https://ko.wikipedia.org/wiki/Typedef).


**typedef**는 [C와](../Page/C_\(프로그래밍_언어\).md "wikilink") [C++](https://ko.wikipedia.org/wiki/C++ "wikilink") [프로그래밍 언어의](../Page/프로그래밍_언어.md "wikilink") [예약어](https://ko.wikipedia.org/wiki/예약어 "wikilink")이다. 다른 [자료형의](../Page/자료형_체계.md "wikilink") 별명을 만들기 위해 사용된다.\[1\] 이처럼, struct와 union 타입으로 이루어진 복잡한 자료 구조를 선언하는 문을 단순하게 만들기 위해 종종 사용되지만 다양한 길이의 정수 자료형에 대한 특정한 서술형 이름을 지정하는 것으로 일반화되어 있다. [C 표준 라이브러리나](../Page/C_표준_라이브러리.md "wikilink") [POSIX](../Page/POSIX.md "wikilink")와 같은 규칙들은 예를 들어 [size_t](https://ko.wikipedia.org/wiki/size_t "wikilink")와 [time_t](https://ko.wikipedia.org/wiki/time_t "wikilink")처럼 종종 typedef 형의 이름을 '_t'로 끝맺는 것이 종종 권장된다.

## 문법

typedef를 만드는 문법은 다음과 같다: **typedef** 형선언;\[2\]

일부 예:

    typedef int Length;

위의 문은 int의 동의어로 Length를 만든다.

    typedef int (*PFI)(char *, char *);

위의 문은 int를 반환하는 2개의 char \* 인수의 함수에 대한 포인터를 위한 동의어로 PFI를 만든다.

## C++에서의 사용

C++에서 형 이름은 매우 복잡할 수 있으며 typedef는 이러한 형에 대한 단순한 이름을 할당하기 위한 구조를 제공한다.

이것과

``` text
std::vector<std::pair<std::string, int> > values;
for (std::vector<std::pair<std::string, int> >::const_iterator i = values.begin(); i != values.end(); ++i)
{
   std::pair<std::string, int> const & t = *i;
   // do something
}
```

이것을 고려할 수 있다.

``` text
typedef std::pair<std::string, int> value_t;
typedef std::vector<value_t> values_t;

values_t values;
for (values_t::const_iterator i = values.begin(); i != values.end(); ++i)
{
   value_t const & t = *i;
   // do something
}
```

## 같이 보기

  - [추상 자료형](../Page/추상_자료형.md "wikilink")
  - [C 문법](https://ko.wikipedia.org/wiki/C_문법 "wikilink")

## 각주

[분류:C 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:C_프로그래밍_언어 "wikilink") [분류:C++](https://ko.wikipedia.org/wiki/분류:C++ "wikilink")

1.
2.