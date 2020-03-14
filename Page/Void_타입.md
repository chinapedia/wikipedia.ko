> This article is converted from Wikipedia: [Void ](https://ko.wikipedia.org/wiki/Void_).


**void 타입**은 C에서 파생된 여러 언어에서 정상적으로 반환하지만 호출자에게 결과 값을 제공하지 않는 함수의 결과를 위한 타입이다. 보통 이러한 함수들은 몇몇 작업을 수행하거나 자신의 결과 파라미터를 쓰는것 같은 그것의 [부작용을](https://ko.wikipedia.org/wiki/부작용_\(컴퓨터_과학\) "wikilink") 위해 호출된다. 이러한 문맥에서 void 타입의 사용은 [비주얼 베이직의](https://ko.wikipedia.org/wiki/비주얼_베이직 "wikilink") [서브루틴과](https://ko.wikipedia.org/wiki/함수_\(프로그래밍\) "wikilink") [파스칼의](https://ko.wikipedia.org/wiki/파스칼_\(프로그래밍_언어\) "wikilink") [함수를](https://ko.wikipedia.org/wiki/프로시저 "wikilink") 정의하는 통사적 구조체의 그것과 차별화된다. 또한 [함수형 프로그래밍과](https://ko.wikipedia.org/wiki/함수형_프로그래밍 "wikilink") [타입 이론에서](https://ko.wikipedia.org/wiki/타입_이론 "wikilink") 사용되는 [유닛 타입과](https://ko.wikipedia.org/wiki/유닛_타입 "wikilink") 비슷하지만 void 타입은 값이 없는 빈 타입이라는 점에서 허용되는 사용법에 몇몇 차이점이 있다.

C와 [C++](https://ko.wikipedia.org/wiki/C++ "wikilink") 또한 **void type에 대한 포인터** ( `void *`로 명시된)를 제공하지만, 이것은 개념과는 관련없다. 이 타입의 변수들은 명시되지 않은 타입의 데이터에 대한 [포인터 (프로그래밍)여서](https://ko.wikipedia.org/wiki/포인터_\(프로그래밍\) "wikilink"), 이 문맥의 경우 void는 일반적인 또는 [탑 타입처럼](https://ko.wikipedia.org/wiki/탑_타입 "wikilink") 행동한다. 프로그램은 아마 어느 데이터의 타입에 대한 포인터라도([함수 포인터](https://ko.wikipedia.org/wiki/함수_포인터 "wikilink") 제외) void에 대한 포인터로 변환할 수 있으며, 정보를 잃는것 없이 원래의 타입으로 돌아갈 수 있는데, 이러한 포인터들은 [다형성](https://ko.wikipedia.org/wiki/다형성 "wikilink") 함수들에 유용하다. C 언어 표준은 다른 포인터 타입들이 같은 크기를 갖는다고 보장하지 않는다.

## C와 C++에서

void 결과 타입을 갖는 함수는 함수의 끝에 도달하거나 반환 값 없이 반환문을 실행함으로써 끝난다. void 타입은 또한 [함수 프로토타입의](https://ko.wikipedia.org/wiki/함수_프로토타입 "wikilink") 유일한 [매개변수로서](../Page/매개변수_\(컴퓨터_프로그래밍\).md "wikilink") 함수가 매개변수를 갖지 않는다는 것을 나타내는 것으로 보여진다.

void의 명시적인 사용과 함수 프로토타입에서 매개변수를 적지 않는 것의 차이점은 C와 C++에서 다른 의미를 갖는다.\[1\]

<table>
<thead>
<tr class="header">
<th><p>C</p></th>
<th><p>C++ equivalent</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><code>void f(void);</code></p></td>
<td><p><code>void f();</code> (<em>선호됨</em>)<br />
<code>void f(void);</code></p></td>
</tr>
<tr class="even">
<td><p><code>void f();</code> (<em>인자를 받지만 매개변수의 수는 알지 못한다.</em>)</p></td>
<td><p><em>no equivalent</em></p></td>
</tr>
</tbody>
</table>

C 프로토타입에서 `void f()` 같은 매개변수 없는 쓰임이 사용되었지만,  [C99](https://ko.wikipedia.org/wiki/C99 "wikilink") 이후로 반대되었다.\[2\]

## 각주

[분류:자료형](https://ko.wikipedia.org/wiki/분류:자료형 "wikilink") [분류:유형 이론](https://ko.wikipedia.org/wiki/분류:유형_이론 "wikilink")

1.
2.  Bjarne Stroustrup, *[C and C++: Case Studies in Compatibility. Reconcilable differences? You decide](http://www.ddj.com/cpp/184401562)*, [Dr. Dobb's](https://ko.wikipedia.org/wiki/Dr._Dobb's "wikilink"), September 01, 2002; [print version](http://www.research.att.com/~bs/examples_short.pdf)