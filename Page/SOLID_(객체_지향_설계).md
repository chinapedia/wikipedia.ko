> This article is converted from Wikipedia: [SOLID \(객체 지향 설계\)](https://ko.wikipedia.org/wiki/SOLID_\(객체_지향_설계\)).


[컴퓨터 프로그래밍에서](../Page/컴퓨터_프로그래밍.md "wikilink") **SOLID**란 [로버트 마틴](https://ko.wikipedia.org/wiki/로버트_마틴 "wikilink")\[1\]\[2\]이 2000년대 초반\[3\]에 명명한 [객체 지향 프로그래밍](../Page/객체_지향_프로그래밍.md "wikilink") 및 [설계의](https://ko.wikipedia.org/wiki/객체_지향_설계 "wikilink") 다섯 가지 기본 원칙을 마이클 페더스가 [두문자어](../Page/두문자어.md "wikilink") [기억술](../Page/기억술.md "wikilink")로 소개한 것이다. 프로그래머가 시간이 지나도 [유지 보수와](https://ko.wikipedia.org/wiki/소프트웨어_유지_보수 "wikilink") 확장이 쉬운 시스템을 만들고자 할 때 이 원칙들을 함께 적용할 수 있다.\[4\] SOLID 원칙들은 소프트웨어 작업에서 프로그래머가 [소스 코드가](../Page/소스_코드.md "wikilink") 읽기 쉽고 확장하기 쉽게 될 때까지 소프트웨어 소스 코드를 [리팩터링](../Page/리팩터링.md "wikilink")하여 [코드 냄새를](https://ko.wikipedia.org/wiki/코드_냄새 "wikilink") 제거하기 위해 적용할 수 있는 지침이다. 이 원칙들은 [애자일 소프트웨어 개발과](../Page/애자일_소프트웨어_개발.md "wikilink") [적응적 소프트웨어 개발의](https://ko.wikipedia.org/wiki/적응적_소프트웨어_개발 "wikilink") 전반적 전략의 일부다.\[5\]

## 개요

<table>
<thead>
<tr class="header">
<th><p>두문자</p></th>
<th><p>약어</p></th>
<th><p>개념</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>S</p></td>
<td><p><a href="../Page/단일_책임_원칙.md" title="wikilink">SRP</a></p></td>
<td><dl>
<dt><a href="../Page/단일_책임_원칙.md" title="wikilink">단일 책임 원칙 (Single responsibility principle)</a></dt>
<dd>한 <a href="https://ko.wikipedia.org/wiki/클래스_(컴퓨터_과학)" title="wikilink">클래스는</a> 하나의 책임만 가져야 한다.
</dd>
</dl></td>
</tr>
<tr class="even">
<td><p>O</p></td>
<td><p><a href="../Page/개방-폐쇄_원칙.md" title="wikilink">OCP</a></p></td>
<td><dl>
<dt><a href="../Page/개방-폐쇄_원칙.md" title="wikilink">개방-폐쇄 원칙 (Open/closed principle)</a></dt>
<dd>“소프트웨어 요소는 확장에는 열려 있으나 변경에는 닫혀 있어야 한다.”
</dd>
</dl></td>
</tr>
<tr class="odd">
<td><p>L</p></td>
<td><p><a href="../Page/리스코프_치환_원칙.md" title="wikilink">LSP</a></p></td>
<td><dl>
<dt><a href="../Page/리스코프_치환_원칙.md" title="wikilink">리스코프 치환 원칙 (Liskov substitution principle)</a></dt>
<dd>“프로그램의 <a href="https://ko.wikipedia.org/wiki/객체" title="wikilink">객체</a>는 프로그램의 정확성을 깨뜨리지 않으면서 하위 타입의 인스턴스로 바꿀 수 있어야 한다.” <a href="https://ko.wikipedia.org/wiki/계약에_의한_설계" title="wikilink">계약에 의한 설계를</a> 참고하라.
</dd>
</dl></td>
</tr>
<tr class="even">
<td><p>I</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/인터페이스_분리_원칙" title="wikilink">ISP</a></p></td>
<td><dl>
<dt><a href="https://ko.wikipedia.org/wiki/인터페이스_분리_원칙" title="wikilink">인터페이스 분리 원칙 (Interface segregation principle)</a></dt>
<dd>“특정 클라이언트를 위한 인터페이스 여러 개가 범용 인터페이스 하나보다 낫다.”[6]
</dd>
</dl></td>
</tr>
<tr class="odd">
<td><p>D</p></td>
<td><p><a href="../Page/의존관계_역전_원칙.md" title="wikilink">DIP</a></p></td>
<td><dl>
<dt><a href="../Page/의존관계_역전_원칙.md" title="wikilink">의존관계 역전 원칙 (Dependency inversion principle)</a></dt>
<dd>프로그래머는 “추상화에 의존해야지, 구체화에 의존하면 안된다.”[7] <a href="../Page/의존성_주입.md" title="wikilink">의존성 주입은</a> 이 원칙을 따르는 방법 중 하나다.
</dd>
</dl></td>
</tr>
</tbody>
</table>

## 같이 보기

### 기본 개념과 연관 주제

  - [적응적 소프트웨어 개발](https://ko.wikipedia.org/wiki/적응적_소프트웨어_개발 "wikilink")
  - [애자일 소프트웨어 개발](../Page/애자일_소프트웨어_개발.md "wikilink")
  - [코드 재사용](../Page/코드_재사용.md "wikilink")
  - [객체 지향 프로그래밍](../Page/객체_지향_프로그래밍.md "wikilink")
      - [상속 (객체 지향 프로그래밍)](../Page/상속_\(객체_지향_프로그래밍\).md "wikilink")
  - [오컴의 면도날](../Page/오컴의_면도날.md "wikilink")

### 설계와 개발 원칙

  - [패키지 원칙](https://ko.wikipedia.org/wiki/패키지_원칙 "wikilink")
  - [DRY](https://ko.wikipedia.org/wiki/Don't_repeat_yourself "wikilink")
  - [GRASP](https://ko.wikipedia.org/wiki/GRASP_\(객체_지향_프로그래밍\) "wikilink")
  - [KISS](https://ko.wikipedia.org/wiki/KISS_원칙 "wikilink")
  - [YAGNI](https://ko.wikipedia.org/wiki/You_aren't_gonna_need_it "wikilink")

## 출처

<references />

[분류:소프트웨어 설계](https://ko.wikipedia.org/wiki/분류:소프트웨어_설계 "wikilink") [분류:객체 지향 프로그래밍](https://ko.wikipedia.org/wiki/분류:객체_지향_프로그래밍 "wikilink") [분류:프로그래밍 원칙](https://ko.wikipedia.org/wiki/분류:프로그래밍_원칙 "wikilink")

1.  [“Principles Of OOD”](http://butunclebob.com/ArticleS.UncleBob.PrinciplesOfOod), [로버트 마틴](https://ko.wikipedia.org/wiki/로버트_마틴 "wikilink"), (이 문서에서 두문자어가 쓰이진 않았지만 첫 다섯 원칙(“first five principles”)을 살펴볼 것) 날짜가 최소한 2005년 이전이다.
2.  [“Getting a SOLID start.”](https://sites.google.com/site/unclebobconsultingllc/getting-a-solid-start), [로버트 마틴](https://ko.wikipedia.org/wiki/로버트_마틴 "wikilink")
3.  [“SOLID Object-Oriented Design”](http://www.confreaks.com/videos/240-goruco2009-solid-object-oriented-design) , Sandi Metz (Duke University), 2009년 5월에 2009 고담 [루비](../Page/루비_\(프로그래밍_언어\).md "wikilink") 컨퍼런스에서 발표함.
4.
5.
6.  [“Design Principles and Design Patterns”](http://www.objectmentor.com/resources/articles/Principles_and_Patterns.pdf) , [로버트 마틴](https://ko.wikipedia.org/wiki/로버트_마틴 "wikilink")
7.