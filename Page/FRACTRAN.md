> This article is converted from Wikipedia: [FRACTRAN](https://ko.wikipedia.org/wiki/FRACTRAN).


**FRACTRAN**은 수학자 [존 호턴 콘웨이가](../Page/존_호턴_콘웨이.md "wikilink") 고안한 [난해한 프로그래밍 언어이다](../Page/난해한_프로그래밍_언어.md "wikilink"). FRACTRAN 프로그램은 양의 [분수](https://ko.wikipedia.org/wiki/분수 "wikilink")들로 이루어진 하나의 목록의 형태이다. 이 프로그램은 다음의 규칙으로 자연수 입력값 n을 갱신하며 작동한다.

1.  입력값 *n*과 목록의 분수 *f*에 대해 *nf*가 처음으로 자연수가 되는 수이면,*n*대신 *nf*를 입력한다.
2.  더 이상 자연수 *nf*가 없을 때까지 이 과정을 반복했다면,프로그램을 정지한다.

## 간단한 FRACTRAN 프로그래밍 예제

FRACTRAN 프로그램은 [괴델 넘버링을](https://ko.wikipedia.org/wiki/괴델_넘버링 "wikilink") 사용해 입력값과 출력값을 하나의 [소인수분해](../Page/소인수분해.md "wikilink")로 표현한다. 예를 들어 a=2, b=1, c=1 을 입력하면

  -
    \(2^2 \times 3^1 \times 5^1\)

와 같은 형태로 표현한다

**덧셈 프로그램**

a와 b를 입력하면 a+b를 출력하는 프로그램은 다음과 같다

  -
    \(\left( \frac{3}{2} \right)\)

이 프로그램은 다음 알고리즘을 따른다.

  -
    {| class="wikitable"

\! \! 상태 \! 행동 |- | align="center" | \(\frac{3}{2}\) | 2의 지수\>0 | 2의 지수에서 1을빼고
3의 지수에 1을 더한다 |- | | 2의 지수 = 0 | 정지 |}

a와 b를 입력하면 다음과 같은 소인수분해 \(2^a 3^b\)가 입력된다, 이 프로그램은 다음과 같은 수열 \(2^{a-1} 3^{b+1}\), \(2^{a-2} 3^{b+2}\)...을 생성하다가, 결국에 \(3^{a + b}\) 곧, \(a+b\)를 출력한다.

**뺄셈 프로그램**

a와 b를 입력하면 a-b를 출력하는 프로그램은 다음과 같다.

\(\left( \frac{1}{6} \right)\)

**최댓값 구하기 프로그램**

a와 b를 입력하면 a와 b중 더 큰 값을 출력하는 프로그램은 다음과 같다

  -
    \((\frac{5}{6}, \frac{5}{2}, \frac{5}{3})\)

**소수 생성 프로그램**

다음은 존 콘웨이가 제시한 소수 생성 프로그램이다.

  -
    \(\left( \frac{17}{91}, \frac{78}{85}, \frac{19}{51}, \frac{23}{38}, \frac{29}{33}, \frac{77}{29}, \frac{95}{23}, \frac{77}{19}, \frac{1}{17}, \frac{11}{13}, \frac{13}{11}, \frac{15}{2}, \frac{1}{7}, \frac{55}{1} \right)\)

n=2를 입력하면,이 프로그램은 다음과 같은 수열

  -
    2, 15, 825, 725, 1925, 2275, 425, 390, 330, 290, 770, ...

을 생성하다가, 2의 소수 거듭제곱을 포함한다.

\[2^2=4,\, 2^3=8,\, 2^5=32,\, 2^7=128,\, 2^{11}=2048,\, 2^{13}=8192,\, 2^{17}=131072,\, 2^{19}=524288,\,  \dots\]

**곱셈 프로그램**

두 자연수 a,b를 입력했을 때, ab를 출력하는 프로그램은 다음과 같다.

\[\left( \frac{455}{33}, \frac{11}{13}, \frac{1}{11}, \frac{3}{7}, \frac{11}{2}, \frac{1}{3} \right)\] [섬네일](https://ko.wikipedia.org/wiki/파일:FRACTRANmult0.gif "wikilink")

**피보나치 프로그램**

피보나치 수열을 생성하는 프로그램은 다음과 같다.

\[\left( \frac{33}{91}, \frac{13}{11}, \frac{11}{1}, \frac{34}{399}, \frac{19}{17}, \frac{17}{1}, \frac{7}{2}, \frac{5}{187}, \frac{3}{1} \right)\]

## 참고 문헌

  -
  -
  -
  -
## 외부 링크

  - ["Prime Number Pathology: Fractran"](http://scienceblogs.com/goodmath/2006/10/27/prime-number-pathology-fractra/)

  -
  - [*Prime Number Pathology*](http://brainwagon.org/?p=2207)

  - [FRACTRAN](http://www.esolangs.org/wiki/Fractran) - (Esolang wiki)

  - [Ruby implementation and example programs](https://web.archive.org/web/20130125232746/http://www.dev.gd/20130121-fun-with-john-conways-fractran.html)

  - [Project Euler Problem 308](https://projecteuler.net/problem=308)

  - ["Building Fizzbuzz in Fractran from the Bottom Up"](http://malisper.me/2016/06/11/building-fizzbuzz-fractran-bottom/)

  - [Chris Lomont, "A Universal FRACTRAN Interpreter in FRACTRAN"](https://web.archive.org/web/20180104084828/http://clomont.com/a-universal-fractran-interpreter-in-fractran/)

[분류:난해한 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:난해한_프로그래밍_언어 "wikilink") [분류:계산 모형](https://ko.wikipedia.org/wiki/분류:계산_모형 "wikilink")