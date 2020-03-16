> This article is converted from Wikipedia: [C  ](https://ko.wikipedia.org/wiki/C__).


**C 대체 토큰**은 [C의](../Page/C_\(프로그래밍_언어\).md "wikilink") 공용 연산자를 다르게 부르는 말의 세트를 일컫는 말이다. 이 대체 토큰은 `iso646.h` 헤더 안의 [C 표준 라이브러리내](../Page/C_표준_라이브러리.md "wikilink") 매크로 상수 모음에 의해 실행된다. 이 토큰은 1995년 개정된 [C90](https://ko.wikipedia.org/wiki/C90_\(C_버전\) "wikilink") 표준에 처음 추가되었다.

대체 토큰을 통하여 프로그래머에게 하여금 일부 [국제](https://ko.wikipedia.org/wiki/국제 "wikilink") 표준과 비[쿼티](https://ko.wikipedia.org/wiki/쿼티 "wikilink") 키보드에선 입력하기 어려울 수 있는 [C언어의](../Page/C_\(프로그래밍_언어\).md "wikilink") 비트 및 논리 [연산자](https://ko.wikipedia.org/wiki/연산자 "wikilink")를 쓸 수 있도록 해준다. 많은 지역적 차이로 구성된 7비트 문자가 담긴 [ISO/IEC 646](https://ko.wikipedia.org/wiki/ISO/IEC_646 "wikilink") 표준을 참조하는 이 헤더 파일의 이름 중 일부는 C 연산자에 의해 쓰이는 문장 부호를 대체하는 악센트 문자가 있다.

## 매크로

`iso646.h` 헤더는 아래에 기술된대로 11개의 매크로를 정의한다.\[1\]

| style="padding-left:1em;padding-right:1em" | 매크로 | 정의             |
| ------------------------------------------------ | -------------- |
| `and`                                            | `&&`           |
| `and_eq`                                         | `&=`           |
| `bitand`                                         | `&`            |
| `bitor`                                          | `\|`           |
| `compl`                                          | `~`            |
| `not`                                            | `!`            |
| `not_eq`                                         | `!=`           |
| `or`                                             | <code><nowiki> |
| `or_eq`                                          | `\|=`          |
| `xor`                                            | `^`            |
| `xor_eq`                                         | `^=`           |

## 각주

[분류:C 표준 라이브러리](https://ko.wikipedia.org/wiki/분류:C_표준_라이브러리 "wikilink")

1.