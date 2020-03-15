> This article is converted from Wikipedia: [Elixir](https://ko.wikipedia.org/wiki/Elixir).


**엘릭서**(Elixir)는 [얼랭](https://ko.wikipedia.org/wiki/얼랭 "wikilink")(Erlang) [가상 머신](https://ko.wikipedia.org/wiki/가상_머신 "wikilink")(BEAM) 위에서 동작하는 [함수형](https://ko.wikipedia.org/wiki/함수형_언어 "wikilink"), [동시성](../Page/병행성.md "wikilink") 프로그래밍 언어이다. 엘릭서는 얼랭이 보유하고 있는 분산 처리, 장애 내구성, 실시간, 무정지 애플리케이션 등의 특징을 공유한다. 그에 더해서 프로토콜\[1\]을 이용해 [다형성](https://ko.wikipedia.org/wiki/다형성 "wikilink")을 지원하고, Quote\[2\]과 Unquote\[3\] 그리고 [Macro](https://ko.wikipedia.org/wiki/매크로 "wikilink")\[4\]를 통한 [DSL](../Page/도메인_특화_언어.md "wikilink") 구현 등의 [메타 프로그래밍이](https://ko.wikipedia.org/wiki/메타_프로그래밍 "wikilink") 가능하다.

## 역사

엘릭서 프로그래밍 언어는 [José Valim이](https://ko.wikipedia.org/wiki/José_Valim "wikilink") 설계했으며, [Plataformatec](http://plataformatec.com.br) 의 연구과제이다. 그는 얼랭 도구와 생태계를 계승하면서 얼랭 VM에서 작동하는 높은 확장성과 생산성을 가진 언어를 만들고자 했다.\[5\]

## 특징

  - 엘릭서 [컴파일러](https://ko.wikipedia.org/wiki/컴파일러 "wikilink")는 소스코드를 [얼랭](https://ko.wikipedia.org/wiki/얼랭 "wikilink") 가상 머신용 [바이트 코드로](https://ko.wikipedia.org/wiki/바이트_코드 "wikilink") [컴파일한다](https://ko.wikipedia.org/wiki/컴파일러 "wikilink"). (BEAM)\[6\]
  - 모든 것은 expression이다.side effect를 동반하는 statement와는 다르다.\[7\]
  - 얼랭 함수들은 [런타임](https://ko.wikipedia.org/wiki/런타임 "wikilink") 영향 없이 엘릭서에서 호출될 수 있다.
  - [메타 프로그래밍을](https://ko.wikipedia.org/wiki/메타_프로그래밍 "wikilink") 지원한다.\[8\]
  - 프로토콜이라고 불리는 메카니즘에 의해 [다형성](https://ko.wikipedia.org/wiki/다형성 "wikilink")을 지원한다.[클로저](../Page/클로저_\(프로그래밍_언어\).md "wikilink") reducers에서 영향을 받았다.\[9\]
  - 마크다운 형식언어의 문서화를 지원한다.\[10\]
  - 메시지 전달 방식을 지원한다.([Actor model](https://ko.wikipedia.org/wiki/Actor_model "wikilink"))
  - 루프 대신에 재귀와 고차원 함수를 강조한다.
  - 얼랭의 메카니즘을 활용하여 경량 동시성을 지원한다. (e.g. *Task*)\[11\]
  - [Lazy와](https://ko.wikipedia.org/wiki/느긋한_계산법 "wikilink") [async collections을](https://ko.wikipedia.org/wiki/Futures_and_promises "wikilink") 지원한다.
  - 패턴매칭을 지원한다.\[12\]
  - [유니코드](https://ko.wikipedia.org/wiki/유니코드 "wikilink")를 지원하며 스트링들은 [UTF-8](https://ko.wikipedia.org/wiki/UTF-8 "wikilink")이다.

## 예제

아래 예제는 iex 셸에서 실행되거나 파일에 저장될수 있으며 ` elixir  `*<filename>* 과 같이 커맨드라인으로 실행 할 수있다.

[Hello world](https://ko.wikipedia.org/wiki/Hello_world "wikilink") 예제:

``` elixir
IO.puts "Hello World!"
```

### 컴프리헨션

``` elixir
for n <- [1,2,3,4,5], rem(n,2) == 1, do: n*n
#=> [1, 9, 25]
```

### 패턴 매칭

``` elixir
[1, a] = [1, 2]
# a => 2

{:ok, [hello: a]} = {:ok, [hello: "world"]}
# a => "world"
```

### 모듈

``` elixir
defmodule Fun do
  def fib(0) do 0 end
  def fib(1) do 1 end
  def fib(n) do fib(n-2) + fib(n-1) end
end
```

## 더 보기

## 외부 링크

  - [Elixir language website](http://elixir-lang.org)

  - [공식 홈페이지 Getting Started 한국어 번역](https://web.archive.org/web/20160305052943/https://erlnote.wordpress.com/category/elixir/)

  - [Elixir 1.0 Getting Started 한국어 번역](http://elixir-ko.github.io/getting_started/1.html)

  - [Code on GitHub](https://github.com/elixir-lang/elixir/)

  - [Elixir - A modern approach to programming for the Erlang VM video presentation](http://vimeo.com/53221562)

  - [Dave Thomas: "Programming Elixir: Functional |\> Concurrent |\> Pragmatic |\> Fun" (book)](http://pragprog.com/book/elixir/programming-elixir)

  - [Simon St. Laurent, J. David Eisenberg: "Introducing Elixir" (book)](http://shop.oreilly.com/product/0636920030584.do)

  - [Chris McCord: "Metaprogramming Elixir " (book)](http://shop.oreilly.com/product/9781680500417.do)

  - [Joe Armstrong: "A Week with Elixir" (blog entry)](https://web.archive.org/web/20130819053404/http://joearms.github.io/2013/05/31/a-week-with-elixir.html)

[분류:프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:프로그래밍_언어 "wikilink") [분류:패턴 매칭 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:패턴_매칭_프로그래밍_언어 "wikilink") [분류:2012년 개발된 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:2012년_개발된_프로그래밍_언어 "wikilink") [분류:아파치 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:아파치_라이선스_소프트웨어 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.