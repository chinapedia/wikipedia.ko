> This article is converted from Wikipedia: [DOT \(그래프 서술 언어\)](https://ko.wikipedia.org/wiki/DOT_\(그래프_서술_언어\)).


**DOT**는 [그래프](https://ko.wikipedia.org/wiki/그래프 "wikilink") 서술 언어이다. DOT 그래프의 [파일 확장자는](../Page/파일_확장자.md "wikilink") gv 또는 dot이다. 2007년 이전의 마이크로소프트 워드 버전에 사용된 dot 확장자와의 혼동을 피하기 위해 gv 확장자가 선호된다.\[1\]

## 문법

### 그래프 종류

#### 무방향 그래프

[right](https://ko.wikipedia.org/wiki/파일:DotLanguageUndirected.svg "wikilink")

``` mscgen
 // The graph name and the semicolons are optional
 graph graphname {
     a -- b -- c;
     b -- d;
 }
```

{{-}}

#### 방향 그래프

[right](https://ko.wikipedia.org/wiki/파일:DotLanguageDirected.svg "wikilink")

``` mscgen
 digraph graphname {
     a -> b -> c;
     b -> d;
 }
```

{{-}}

### 속성

[right](https://ko.wikipedia.org/wiki/파일:DotLanguageAttributes.svg "wikilink")

``` mscgen
 graph graphname {
     // This attribute applies to the graph itself
     size="1,1";
     // The label attribute can be used to change the label of a node
     a [label="Foo"];
     // Here, the node shape is changed.
     b [shape=box];
     // These edges both have different line properties
     a -- b -- c [color=blue];
     b -- d [style=dotted];
     // [style=invis] hides a node.
   }
```

{{-}}

### 주석 처리

``` text
 // This is a single line comment.
 /* This is a
    multiple line
    comment. */
 # Lines like this are also ignored.
```

{{-}}

## 단순 예시

``` mscgen
 graph ethane {
     C_0 -- H_0 [type=s];
     C_0 -- H_1 [type=s];
     C_0 -- H_2 [type=s];
     C_0 -- C_1 [type=s];
     C_1 -- H_3 [type=s];
     C_1 -- H_4 [type=s];
     C_1 -- H_5 [type=s];
 }
```

{{-}}

## 각주

## 외부 링크

  - [DOT tutorial and specification](http://www.graphviz.org/documentation/)

[분류:수학 소프트웨어](https://ko.wikipedia.org/wiki/분류:수학_소프트웨어 "wikilink")

1.