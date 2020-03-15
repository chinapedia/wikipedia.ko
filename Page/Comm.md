> This article is converted from Wikipedia: [Comm](https://ko.wikipedia.org/wiki/Comm).


[유닉스](https://ko.wikipedia.org/wiki/유닉스 "wikilink")에서 **`comm`** 명령어는 일반적이고 뚜렷한 문자열들을 위해서 두 개의 [파일들을](https://ko.wikipedia.org/wiki/컴퓨터_파일 "wikilink") 비교하기 위해서 사용되는 유틸리티이다. `Comm`은 [POSIX](https://ko.wikipedia.org/wiki/POSIX "wikilink") 표준 안에서 지정된다. 이는 1980년 중반부터 후반까지 [유닉스 계통](https://ko.wikipedia.org/wiki/유닉스_계통 "wikilink") 시스템에서 폭넓게 사용되고 있다..

## 사용법

`comm`은 텍스트의 문자열들에는 상관없이 두 파일들을 입력물로서 읽는다.`comm`은 하나의 파일을 출력하는데, 이는 세 개의 열들을 포함한다. 첫 번째 두 열들은 첫 번째와 두 번째 파일과 같은 문자열들을 각각 포함한다. 마지막 열은 두 개의 파일들에 일반적인 문자열들을 포함한다. 이는 기능적으로 [`diff`](https://ko.wikipedia.org/wiki/diff "wikilink")와 비슷하다.

열들은 일반적으로 *`<tab>`* 문자에 의해서 구분된다. 만약 입력되는 파일들이 구분자 문자로 시작되는 문자열들을 포함한다면, 출력되는 열들은 모호하게 될 수도 있다.

효율성을 위해서 `comm`의 표준 실행은 두 개의 입력된 파일들이 같은 문자열 콜래이션 순서로 정열되기를 기대한다. [sort (유닉스)](https://ko.wikipedia.org/wiki/sort_\(유닉스\) "wikilink") 명령어는 이러한 목적으로 사용될 수 있다.

`comm` 알리고리즘은 현재 장소의 콜래이션 순서를 사용한다. 만약 파일 안의 문자열들이 현재 장소에 따라서 둘이 서로 순서가 맞지 않는다면, 그 결과는 정의될 수 없다.

## 리턴 코드

`diff`와는 달리, `comm`로부터의 리턴 코드는 두 개의 파일들의 관계를 고려한, 어떠한 논리적인 중요성도 갖지 않는다. 0이라는 리턴코드는 성공을 의미하고, \>0이라는 리턴 코드는 실행 중에 발생한 에러를 나타낸다.

## 예시

``` console
$ cat foo
apple
banana
eggplant
$ cat bar
apple
banana
banana
zucchini
$ comm foo bar
                  apple
                  banana
          banana
eggplant
          zucchini
```

이는 두 개의 파일이 하나의 바나나를 갖고 있으나 오직 **bar**만이 두 번째 바나나를 갖고 있음을 보여준다.

출력되는 파일은 다음과 같은 특징을 갖는다. 열이 앞선 탭 문자의 순자에 의해서 해석됨을 주의하라. \\t은 [탭 문자를](https://ko.wikipedia.org/wiki/탭_문자 "wikilink") 나타내고 \\n은 [뉴라인](https://ko.wikipedia.org/wiki/뉴라인 "wikilink")([이스케이프_시퀀스](https://ko.wikipedia.org/wiki/이스케이프_시퀀스 "wikilink"))를 나타낸다.

|   | 0   | 1   | 2 | 3 | 4 | 5 | 6 | 7   | 8   | 9   |
| - | --- | --- | - | - | - | - | - | --- | --- | --- |
| 0 | \\t | \\t | a | p | p | l | e | \\n |     |     |
| 1 | \\t | \\t | b | a | n | a | n | a   | \\n |     |
| 2 | \\t | b   | a | n | a | n | a | \\n |     |     |
| 3 | e   | g   | g | p | l | a | n | t   | \\n |     |
| 4 | \\t | z   | u | c | c | h | i | n   | i   | \\n |

## diff와의 비교

In general terms, `diff` is a more powerful utility than `comm`. The simpler `comm` is best suited for use in scripts. 일반적인 관점에서 `diff`은 `comm`보다 훨씬 강력한 유틸리티이다. 더 단순한 `comm`은 스크립트 안의 사용에 최적이다.

`comm`와 `diff` 사이의 중요한 차이점은 `comm`가 분류하기 이전의 문자열 순서에 대한 정보를 폐기한다는 것이다.

`comm`와 `diff`의 사이의 사소한 차이점은 `comm`이 두 개의 파일들 사이의 "변화된" 문자열을 표시하려고 하지 않는다는 점이다; 문자열이 "file \#1로부터", "file \#2로부터", 이나 "두 개 파일" 열들 안에 표시될 수 있다. 비록 그 차이가 미묘할지라도 두 개의 문자열들이 다르게 구분되기를 바란다면 이는 유용할 수 있다.

## 다른 옵션들

**`comm`**은 세 개의 열 중 아무거나 억누를 수 있는 옵션들을 갖는다. 이는 스크립팅하는데 있어서 유용하다.

표준 입력물로부터 하나의 파일(두 개의 파일은 아님)을 읽는 옵션이 있다.

## 한계

다음 출력어가 쓰여지기 전까지 문자열을 비교하는 동안, 전체 입력어까지는 각각의 입력된 파일들로부터 반드시 버퍼링되어야 한다.

어떤 실행들은 만약 시스템 메모리가 충분하다면 문자열 길이에 제약을 가하지 않는 `readlinebuffer()` 기능으로 문자열을 읽는다.

다른 실행들은 [`fgets`](https://ko.wikipedia.org/wiki/fgets "wikilink")() 기능으로 문자열들을 읽는다. 이 기능은 고정된 버퍼를 필요로 한다. 이러한 실행들에 있어서, 버퍼는 종종 [POSIX](https://ko.wikipedia.org/wiki/POSIX "wikilink") macro `LINE_MAX`에 따라서 크기가 주어진다.

## 함께 보기

  - [diff](https://ko.wikipedia.org/wiki/diff "wikilink")
  - [cmp](https://ko.wikipedia.org/wiki/cmp "wikilink") -- 문자열 지향적인 파일 비교
  - [cut](https://ko.wikipedia.org/wiki/cut_\(유닉스\) "wikilink") -- 열 지향적인 파일들 분리

## 각주

  -
  -
[분류:표준 유닉스 프로그램](https://ko.wikipedia.org/wiki/분류:표준_유닉스_프로그램 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink")