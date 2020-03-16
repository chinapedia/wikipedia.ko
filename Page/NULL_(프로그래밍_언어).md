> This article is converted from Wikipedia: [NULL \( \)](https://ko.wikipedia.org/wiki/NULL_\(_\)).


**NULL**은 0차원의 [난해한 프로그래밍 언어이다](../Page/난해한_프로그래밍_언어.md "wikilink"). 하나의 양의 정수를 [소인수분해](../Page/소인수분해.md "wikilink")하여 명령을 만들어낸다.

## 런타임 환경

NULL 프로그램에서 사용할 수 있는 환경은 초기에 비어있는 3개의 대기열(Queue)과 임의의 2개의 양의 정수인 변수 'x'와 'y'로 구성된다. 'x'는 프로그램에 설정되고 'y'는 1로 설정된다.

그런 다음, 'x'를 'x'의 가장 작은 소인수로 나누고 'y'를 곱한 다음 소수 요소에 해당하는 명령어가 실행된다.

## 명령어

| 2  | 다음 대기열(Queue) 선택 (wrapping around).                                                                                                                                                                           |
| -- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 3  | 이전 대기열(Queue) 선택 (wrapping around).                                                                                                                                                                           |
| 5  | 선택한 대기열의 앞에 있는 바이트를 출력한다. (대기열이 비어있는 경우 NUL(ASCII 문자 0).                                                                                                                                                      |
| 7  | Input one byte and replace the value at the front of the selected queue with it; or, if the selected queue is empty, enqueue the value there. It is currently undefined what to do when EOF has been reached. |
| 11 | Subtract the byte at the front of the selected queue (0 if the queue is empty) from y. If this makes y less than zero, y is set to 0.                                                                         |
| 13 | 선택한 대기열의 앞에 있는 바이트 추가 (대기열이 비어있다면 값은 0) to y.                                                                                                                                                                 |
| 17 | 선택한 대기열의 앞에 Add y mod 256를 더하고, 만약 대기열이 비어있다면 y mod 256을 입력.                                                                                                                                                  |
| 19 | 선택한 대기열의 앞에 있는 바이트 제거, (use 0 if the queue is empty) and 다음 대기열에 enqueue it to the rear of the next queue (wrapping around).                                                                                  |
| 23 | 선택한 대기열의 앞에 있는 바이트 제거 (use 0 if the queue is empty) and enqueue it to the rear of the previous queue (wrapping around).                                                                                       |
| 29 | 선택한 대기열의 앞에 있는 바이트 제거.                                                                                                                                                                                        |
| 31 | 선택한 대기열의 끝에 y mod 256을 입력.                                                                                                                                                                                    |
| 37 | 만약 선택한 대기열이 비어있거나 앞의 바이트 값이 0이면, x를 그것의 가장 작은 소인수로 나누고, y를 곱한다.                                                                                                                                               |
| 41 | 두 변수(x, y)의 값을 서로 변경.                                                                                                                                                                                         |
| 43 | 프로그램 종료                                                                                                                                                                                                       |

이 명령어는 항상 14번째 소수마다 반복된다. 예를 들어, 47은 2와 같은 역할을 한다.

## 예제

### [Hello, world\!](https://ko.wikipedia.org/wiki/Hello,_world! "wikilink")

이 199자리 수는 Hello, world\!를 출력한다.

`50056520978563208516819797718881283032143646116073595166114838703987562227081772`
`27277884468665934749909633552472002670467760272184148189288786549011066838407636`
`978909259289001144030816758344442315793`

### [Cat program](https://ko.wikipedia.org/wiki/Cat_program "wikilink")

이 5자리 수는 고양이 프로그램이다. 파일을 끝내는 동작은 정의되지 않았다.

`42539`

## 외부 링크

  -
  - [NULL interpreter in Python](http://dev.tokigun.net/esolang/null/nullrun.py), with [미러 사이트](https://github.com/graue/esofiles/blob/master/null/impl/nullrun.py) in [the Esoteric File Archive](https://ko.wikipedia.org/wiki/the_Esoteric_File_Archive "wikilink")

  - [NULL interpreter in Rust](https://github.com/serprex/NULL)

[분류:난해한 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:난해한_프로그래밍_언어 "wikilink") [분류:소인수 분해 알고리즘](https://ko.wikipedia.org/wiki/분류:소인수_분해_알고리즘 "wikilink")