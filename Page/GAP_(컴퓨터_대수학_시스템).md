> This article is converted from Wikipedia: [GAP \(컴퓨터 대수학 시스템\)](https://ko.wikipedia.org/wiki/GAP_\(컴퓨터_대수학_시스템\)).


**GAP**([군](../Page/군_\(수학\).md "wikilink"), [알고리즘](../Page/알고리즘.md "wikilink") 그리고 [프로그래밍](../Page/컴퓨터_프로그래밍.md "wikilink"))은 특히 [계산군론](https://ko.wikipedia.org/wiki/계산군론 "wikilink")에 중점을 둔 계산 이산 대수학을 위한 [컴퓨터 대수학 시스템이다](https://ko.wikipedia.org/wiki/컴퓨터_대수학_시스템 "wikilink").

## 역사

GAP는 독일의 [아헨 공과대학교의](../Page/아헨_공과대학교.md "wikilink") Lehrstuhl D für Mathematik (LDFM)에서 1986년부터 1997년까지 개발되었다. J. Neubüser가 LDFM의 의장에서 은퇴한 뒤, GAP의 개발과 유지는 [스코틀랜드](../Page/스코틀랜드.md "wikilink")의 [세인트앤드루스 대학교의](../Page/세인트앤드루스_대학교.md "wikilink") 수리과학과와 계산과학과와 연합하였다. 2005년 여름의 연합은 [세인트앤드루스 대학교](../Page/세인트앤드루스_대학교.md "wikilink"), [아헨 공과대학교](../Page/아헨_공과대학교.md "wikilink"), [브라운슈바이크 공과대학](https://ko.wikipedia.org/wiki/브라운슈바이크_공과대학 "wikilink"), 그리고 [포트콜린스](../Page/포트콜린스.md "wikilink")의 [콜로라도 주립 대학교에](https://ko.wikipedia.org/wiki/콜로라도_주립_대학교 "wikilink") 위치한 네 'GAP Centres'의 공동 조합으로 이전되었다.

## 배포

패키지(사용자 기여 프로그램의 모음), 데이터 라이브러리([작은 군의 목록을](../Page/작은_군의_목록.md "wikilink") 포함) 그리고 매뉴얼을 포함하는 GAP와 그 소스는 "[카피레프트](../Page/카피레프트.md "wikilink")" 조건에 종속되어 무료로 배포 되었다. GAP는 [윈도우에서](../Page/마이크로소프트_윈도우.md "wikilink") 어떤 [유닉스](../Page/유닉스.md "wikilink") 시스템과, [매킨토시](../Page/매킨토시.md "wikilink") 시스템에서 작동한다. 표준 배포는 300 MB (패키지를 로드 할 경우에는 약 400 MB)가 필요하다. GAP를 실행시키기 위해서, RAM 128 MB면 충분하다.

사용자 기여 패키지는 많은 기능을 추가하는 시스템의 중요한 형태이다. GAP는 패키지 저자에게 이 패키지를 최종 패키지의 질을 크게 증가시키고, 그 저자의 학술지와 비슷한 인식을 제공하게 하는 [동료평가](https://ko.wikipedia.org/wiki/동료평가 "wikilink")의 처리에 전송할 기회를 제공한다. , GAP와 같이 배포된 패키지가 58개가 있고, 대략 35개가 이 과정을 거쳤다.

인터페이스는 GAP 내에서 [SINGULAR](https://ko.wikipedia.org/wiki/Singular_\(소프트웨어\) "wikilink") 컴퓨터 대수학 시스템을 사용하는 것이 가능하다. GAP은 또한 수학 소프트웨어 시스템 [SageMath](https://ko.wikipedia.org/wiki/SageMath "wikilink")를 포함한다.

## 샘플 세션

<span style="color: darkblue;">`gap>`</span>` `<span style="color: #B60000;">`G:=SmallGroup(8,1);`</span>` `<span style="color: darkgray;">`# Set G to be a group of order 8.`</span>
`<pc group of size 8 with 3 generators>`
<span style="color: darkblue;">`gap>`</span>` `<span style="color: #B60000;">`i:=IsomorphismPermGroup(G);`</span>` `<span style="color: darkgray;">`# Find an isomorphism from G to a group of permutations`</span>
<action isomorphism>
<span style="color: darkblue;">`gap>`</span>` `<span style="color: #B60000;">`Image(i,G);`</span>` `<span style="color: darkgray;">`# The image of G under I - these are the generators of im G.`</span>
`Group([ (1,5,3,7,2,6,4,8), (1,3,2,4)(5,7,6,8), (1,2)(3,4)(5,6)(7,8) ])`
<span style="color: darkblue;">`gap>`</span>` `<span style="color: #B60000;">`Elements(Image(i,G));`</span>` `<span style="color: darkgray;">`# All the elements of im G.`</span>
`[ (), (1,2)(3,4)(5,6)(7,8), (1,3,2,4)(5,7,6,8), (1,4,2,3)(5,8,6,7),`
`   (1,5,3,7,2,6,4,8), (1,6,3,8,2,5,4,7), (1,7,4,5,2,8,3,6), (1,8,4,6,2,7,3,5) ]`

## 같이 보기

  - [컴퓨터 대수학 시스템의 비교](https://ko.wikipedia.org/wiki/컴퓨터_대수학_시스템의_비교 "wikilink")

## 참고 문헌

## 외부 링크

  -
  - [GAP package singular – The GAP interface to Singular](http://www.gap-system.org/Packages/singular.html)

  - [Frontend for GAP computer algebra system](http://ggap.sourceforge.net/)

[분류:리눅스용 컴퓨터 대수학 시스템 소프트웨어](https://ko.wikipedia.org/wiki/분류:리눅스용_컴퓨터_대수학_시스템_소프트웨어 "wikilink") [분류:MacOS용 컴퓨터 대수학 시스템 소프트웨어](https://ko.wikipedia.org/wiki/분류:MacOS용_컴퓨터_대수학_시스템_소프트웨어 "wikilink") [분류:윈도우즈용 컴퓨터 대수학 시스템 소프트웨어](https://ko.wikipedia.org/wiki/분류:윈도우즈용_컴퓨터_대수학_시스템_소프트웨어 "wikilink") [분류:자유 컴퓨터 대수학 시스템](https://ko.wikipedia.org/wiki/분류:자유_컴퓨터_대수학_시스템 "wikilink")