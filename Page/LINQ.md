> This article is converted from Wikipedia: [LINQ](https://ko.wikipedia.org/wiki/LINQ).


**LINQ**('링크'로 발음, Language Integrated Query)는 네이티브 데이터 [질의](https://ko.wikipedia.org/wiki/질의어 "wikilink") 기능을 [닷넷 언어에](https://ko.wikipedia.org/wiki/CLI_언어_목록 "wikilink") 추가하는 [마이크로소프트](../Page/마이크로소프트.md "wikilink") [닷넷 프레임워크](../Page/닷넷_프레임워크.md "wikilink") 구성 요소이며 2007년 [닷넷 프레임워크 3.5의](https://ko.wikipedia.org/wiki/닷넷_프레임워크_3.5 "wikilink") 중요 부분으로 처음 출시되었다.

LINQ는 [SQL](../Page/SQL.md "wikilink") 문과 비슷하게 질의식의 추가를 통해 언어를 확장하며 [배열](../Page/배열.md "wikilink"), 열거식 클래스, [XML](../Page/XML.md "wikilink") 도큐먼트, [관계형 데이터베이스](https://ko.wikipedia.org/wiki/관계형_데이터베이스 "wikilink"), 서드파티 데이터 소스로부터 데이터를 편리하게 추출하고 가공하기 위해 사용할 수 있다. 질의식을 임의의 계산을 읽기 쉽게 구성하기 위한 일반적인 프레임워크로 활용하는 다른 용례로는 이벤트 핸들러 구성\[1\], 모나딕 [파서가](../Page/구문_분석.md "wikilink") 포함된다.\[2\]

LINQ의 포팅판으로는 [PHP](../Page/PHP.md "wikilink")([PHPLinq](https://phplinq.codeplex.com/)), [자바스크립트](../Page/자바스크립트.md "wikilink")([linq.js](https://github.com/mihaifm/linq)), [타입스크립트](../Page/타입스크립트.md "wikilink")([linq.ts](https://github.com/kutyel/linq.ts)), [액션스크립트](../Page/액션스크립트.md "wikilink")([ActionLinq](https://web.archive.org/web/20181225143803/http://actionlinq.riaforge.org/))용으로 존재하지만 이 중 어느 것도 닷넷 파생 언어 C\#, F\#, VB.NET과 완전히 동일한 것은 아니다.

## PLINQ

닷넷 프레임워크 버전 4에는 [PLINQ](https://ko.wikipedia.org/wiki/PLINQ "wikilink")(Parallel LINQ)가 포함되어 있으며 이는 LINQ 쿼리들을 위한 [병렬](../Page/병렬_컴퓨팅.md "wikilink") 실행 엔진이다. `ParallelQuery`<T> 클래스를 정의한다. `IEnumerable`<T> 인터페이스 구현체는 닷넷 프레임워크의 System.Linq 이름공간의 ParallelEnumerable 클래스에 의해 정의된 `AsParallel`<T>`(this IEnumerable`<T>`)` 확장 메소드를 호출함으로써 PLIQ 엔진의 이점을 활용할 수 있다.\[3\] PLIQ 엔진은 다중 스레드로 동시에 쿼리의 일부를 실행할 수 있어서 더 빠른 결과를 도출해 낸다.\[4\]

## 같이 보기

  - [객체 관계 매핑](https://ko.wikipedia.org/wiki/객체_관계_매핑 "wikilink") (ORM)
  - [리스트 캄프리헨션](../Page/리스트_캄프리헨션.md "wikilink")
  - [느긋한 계산법](../Page/느긋한_계산법.md "wikilink")

## 각주

## 외부 링크

  - [Official Microsoft LINQ Project](http://msdn.microsoft.com/en-us/netframework/aa904594.aspx)
  - [LINQ to Objects for the .NET developer](http://www.developerfusion.com/article/8250/linq-to-objects-for-the-net-developer/)
  - [Future of LINQ to SQL](https://web.archive.org/web/20200721231257/https://social.msdn.microsoft.com/Forums/en-US/b0ed008e-b4f6-47f6-8b43-9838b94f5ced/what-is-the-future-of-linq-to-sql-as-of-2016?forum=linqtosql)
  - [How does it work in C\#? - Part 3 (C\# LINQ in detail)](http://www.codeproject.com/Articles/383749/How-does-it-work-in-Csharp-Part-3-Csharp-LINQ-in-d)

[분류:질의어](https://ko.wikipedia.org/wiki/분류:질의어 "wikilink")

1.
2.
3.
4.