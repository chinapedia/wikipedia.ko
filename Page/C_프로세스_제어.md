> This article is converted from Wikipedia: [C 프로세스 제어](https://ko.wikipedia.org/wiki/C_프로세스_제어).


**C 프로세스 제어**는 [C](../Page/C_\(프로그래밍_언어\).md "wikilink") 언어의 [표준 라이브러리에서](../Page/C_표준_라이브러리.md "wikilink") 기본적인 프로세스 제어 행위를 구현한 함수들의 집합을 의미한다.\[1\]\[2\] 프로세스 제어 행위들은 프로그램 종류나 환경 동작들의 목록에 접근하는 것들을 포함한다.

## 함수들 개요

프로세스 제어 함수들은 `stdlib.h` 헤더에 정의되어 있다 (C++에서는 `cstdlib` 헤더).

<table>
<thead>
<tr class="header">
<th><p>함수</p></th>
<th><p>설명</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>프로그램 종료시키기</p></td>
<td><p><a href="http://en.cppreference.com/w/c/program/abort"><code>abort</code></a></p></td>
</tr>
<tr class="even">
<td><p><a href="http://en.cppreference.com/w/c/program/exit"><code>exit</code></a></p></td>
<td><p>청소와 함께 정상적인 프로그램을 종료시킨다</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://en.cppreference.com/w/c/program/_Exit"><code>_Exit</code></a></p></td>
<td><p>청소 없이 정상적인 프로그램을 종료시킨다 (<a href="../Page/C99.md" title="wikilink">C99</a>)</p></td>
</tr>
<tr class="even">
<td><p><a href="http://en.cppreference.com/w/c/program/atexit"><code>atexit</code></a></p></td>
<td><p>exit() 수행 시에 호출될 함수를 등록한다</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://en.cppreference.com/w/c/program/quick_exit"><code>quick_exit</code></a></p></td>
<td><p>청소 없이 정상적인 프로그램을 종료시키지만, IO 버퍼는 플러시한다 (<a href="https://ko.wikipedia.org/wiki/C11" title="wikilink">C11</a>)</p></td>
</tr>
<tr class="even">
<td><p><a href="http://en.cppreference.com/w/c/program/at_quick_exit"><code>at_quick_exit</code></a></p></td>
<td><p>quick_exit() 실행 시에 호출될 함수를 등록한다</p></td>
</tr>
<tr class="odd">
<td><p>환경과의 통신</p></td>
<td><p><a href="http://en.cppreference.com/w/c/program/getenv"><code>getenv</code></a></p></td>
</tr>
<tr class="even">
<td><p><a href="http://en.cppreference.com/w/c/program/system"><code>system</code></a></p></td>
<td><p>호스트 환경의 명령 프로세서를 호출한다</p></td>
</tr>
</tbody>
</table>

## 각주

[분류:C 표준 라이브러리](https://ko.wikipedia.org/wiki/분류:C_표준_라이브러리 "wikilink")

1.
2.