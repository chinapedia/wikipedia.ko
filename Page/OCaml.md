> This article is converted from Wikipedia: [OCaml](https://ko.wikipedia.org/wiki/OCaml).


**OCaml**(Objective Caml)은 [Caml](https://ko.wikipedia.org/wiki/Caml "wikilink") [프로그래밍 언어의](../Page/프로그래밍_언어.md "wikilink") 주요 구현체로서 [Xavier Leroy](https://ko.wikipedia.org/wiki/Xavier_Leroy "wikilink"), [Jérôme Vouillon](https://ko.wikipedia.org/wiki/Jérôme_Vouillon "wikilink"), [Damien Doligez](https://ko.wikipedia.org/wiki/Damien_Doligez "wikilink"), [Didier Rémy](https://ko.wikipedia.org/wiki/Didier_Rémy "wikilink") 등의 사람들이 1996년에 작성하였다. OCaml은 [INRIA에서](https://ko.wikipedia.org/wiki/Institut_National_de_Recherche_en_Informatique_et_en_Automatique "wikilink") 주도적으로 관리하고 유지하는 [오픈 소스](../Page/오픈_소스.md "wikilink") 프로젝트이다.

OCaml은 Caml 언어의 핵심 부분에 [객체 지향](https://ko.wikipedia.org/wiki/객체_지향 "wikilink") 구조를 추가한 것이다.

OCaml의 특징은 정적 타입 시스템, 타입 추론, 파라메트릭 폴리모피즘, 패턴 매칭, 펑터, 예외 처리, 쓰레기 수집 등이다.

Ocaml 도구 모음에는 대화식의 톱 레벨(top level) [인터프리터](../Page/인터프리터.md "wikilink"), [바이트코드](../Page/바이트코드.md "wikilink") [컴파일러](../Page/컴파일러.md "wikilink"), 최적화 컴파일러 등이 포함되어 있다. 또한 많은 표준 라이브러리들이 포함되어 있고 탄탄한 모듈 방식 및 대형 소프트웨어에 적용 가능한 객체 지향 프로그래밍 구조 등을 가지고 있어서, [파이썬](../Page/파이썬.md "wikilink")이나 [펄](../Page/펄.md "wikilink")과 같은 언어들로 응용 프로그램을 작성해야 하는 경우에 Ocaml도 충분히 유용하게 사용할 수 있다.

Ocaml은 [Caml Light를](https://ko.wikipedia.org/wiki/Caml_Light "wikilink") 계승하였다. CAML은 *Categorical Abstract Machine Language*의 머리글자이지만, Ocaml은 abstract machine(추상 기계) 기능을 삭제하였다.

## 예제

  - [헬로 월드 프로그램](https://ko.wikipedia.org/wiki/헬로_월드_프로그램 "wikilink")

<!-- end list -->

``` ocaml
print_endline "Hello World!"
```

  - [피보나치 수 프로그램](https://ko.wikipedia.org/wiki/피보나치_수_프로그램 "wikilink")

<!-- end list -->

``` ocaml
let rec fib_aux n a b =
  match n with
  | 0 -> a
  | _ -> fib_aux (n - 1) b (a+b)
let fib n = fib_aux n 0 1
```

  - [퀵소트](https://ko.wikipedia.org/wiki/퀵소트 "wikilink")

<!-- end list -->

``` ocaml
let rec qsort = function
   | [] -> []
   | pivot :: rest ->
       let is_less x = x < pivot in
       let left, right = List.partition is_less rest in
       qsort left @ [pivot] @ qsort right
```

## 각주

## 외부 링크

  - [Caml 언어 공식 사이트](http://caml.inria.fr/)
  - [C, C++, Java, Perl 프로그래머를 위한 OCaml 튜토리얼](http://www.ocaml-tutorial.org/)
  - [초급 OCaml 튜토리얼](http://www.ocf.berkeley.edu/~mbh/tutorial/index.html)
  - [실용적으로 접근한 튜토리얼](http://www.soton.ac.uk/~fangohr/software/ocamltutorial/index.html)
  - [OCaml Batteries Included](http://batteries.forge.ocamlcore.org), 사용자 커뮤니티에서 작성한 Ocaml 표준 라이브러리
  - [OCaml-Java](https://web.archive.org/web/20110721024935/http://ocamljava.x9c.fr/), OCaml for Java
  - [OCamIL](http://www.pps.jussieu.fr/~montela/ocamil/), [Microsoft .NET를](https://ko.wikipedia.org/wiki/.net "wikilink") 위한 Ocaml 컴파일러
  - [다양한 프로그래밍 언어의 속도 비교](https://web.archive.org/web/20120831065317/http://shootout.alioth.debian.org/) Ocaml의 결과도 있음
  - [LablGL and LablGTK](http://wwwfun.kurims.kyoto-u.ac.jp/soft/olabl/) [OpenGL](../Page/OpenGL.md "wikilink")+ 바인딩 (LablGL) 및 [GTK+](../Page/GTK+.md "wikilink") 바인딩 (LablGTK)
  - [MetaOCaml](https://web.archive.org/web/20130613174907/http://metaocaml.org/) 홈페이지
  - [GODI](http://godi.camlcity.org/godi/index.html) Ocaml을 위한 GODI 패키지 매니저
  - [OCamlcore Planet](http://planet.ocamlcore.org/) Ocaml 메타 블로그
  - [OCamlForge](http://forge.ocamlcore.org/)
  - [Ocamlwizard](http://ocamlwizard.lri.fr)

[분류:함수형 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:함수형_프로그래밍_언어 "wikilink") [분류:객체 지향 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:객체_지향_프로그래밍_언어 "wikilink") [분류:1996년 개발된 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:1996년_개발된_프로그래밍_언어 "wikilink") [분류:ML 프로그래밍 언어 계열](https://ko.wikipedia.org/wiki/분류:ML_프로그래밍_언어_계열 "wikilink") [분류:크로스 플랫폼 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_자유_소프트웨어 "wikilink") [분류:자유 컴파일러와 인터프리터](https://ko.wikipedia.org/wiki/분류:자유_컴파일러와_인터프리터 "wikilink")