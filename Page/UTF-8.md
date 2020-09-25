> This article is converted from Wikipedia: [UTF-8](https://ko.wikipedia.org/wiki/UTF-8).


**UTF-8**은 [유니코드](../Page/유니코드.md "wikilink")를 위한 가변 길이 [문자 인코딩](../Page/문자_인코딩.md "wikilink") 방식 중 하나로, [켄 톰프슨과](../Page/켄_톰프슨.md "wikilink") [롭 파이크가](../Page/롭_파이크.md "wikilink") 만들었다. UTF-8은 Universal Coded Character Set + Transformation Format – 8-bit 의 약자이다. 본래는 **FSS-UTF**(File System Safe UCS/Unicode Transformation Format)라는 이름으로 제안되었다.

UTF-8 인코딩은 유니코드 한 문자를 나타내기 위해 1바이트에서 4바이트까지를 사용한다. 예를 들어서, U+0000부터 U+007F 범위에 있는 [ASCII](https://ko.wikipedia.org/wiki/ASCII "wikilink") 문자들은 UTF-8에서 1바이트만으로 표시된다. 4바이트로 표현되는 문자는 모두 [기본 다국어 평면](https://ko.wikipedia.org/wiki/기본_다국어_평면 "wikilink")(BMP) 바깥의 유니코드 문자이며, 거의 사용되지 않는다. [UTF-16](../Page/UTF-16.md "wikilink")과 UTF-8 중 어느 인코딩이 더 적은 바이트를 사용하는지는 문자열에서 사용된 코드 포인트에 따라 달라지며, 실제로 [DEFLATE](../Page/DEFLATE.md "wikilink")와 같은 일반적인 압축 알고리즘을 사용할 경우 이 차이는 무시할 수 있을 정도이다. 이러한 압축 알고리즘을 사용하기 힘들고 크기가 중요할 경우 [유니코드 표준 압축 방식](https://ko.wikipedia.org/wiki/유니코드_표준_압축_방식 "wikilink")(Standard Compression Scheme for Unicode)을 대신 사용할 수 있다.

## 구조

UTF-8은 여러 표준 문서에서 다른 방법으로 정의되어 있지만, 일반적인 구조는 모두 동일하다고 볼 수 있다.

유니코드 코드 포인트를 나타내는 비트들은 여러 부분으로 나뉘어서, UTF-8로 표현된 바이트의 하위 비트들에 들어 간다. `U+007F`까지의 문자는 7비트 [ASCII](https://ko.wikipedia.org/wiki/ASCII "wikilink") 문자와 동일한 방법으로 표시되며, 그 이후의 문자는 다음과 같은 4바이트까지의 비트 패턴으로 표시된다. 7비트 ASCII 문자와 혼동되지 않게 하기 위하여 모든 바이트들의 최상위 비트는 1이다.

<table>
<thead>
<tr class="header">
<th><p>코드 범위(<a href="../Page/십육진법.md" title="wikilink">십육진법</a>)</p></th>
<th><p><a href="https://ko.wikipedia.org/wiki/UTF-16BE" title="wikilink">UTF-16BE</a> 표현(<a href="../Page/이진법.md" title="wikilink">이진법</a>)</p></th>
<th><p>UTF-8 표현(<a href="../Page/이진법.md" title="wikilink">이진법</a>)</p></th>
<th><p>설명</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><code>000000-00007F</code></p></td>
<td><p><code>00000000 0xxxxxxx</code></p></td>
<td><p><code>0xxxxxxx</code></p></td>
<td><p>ASCII와 동일한 범위</p></td>
</tr>
<tr class="even">
<td><p><code>000080-0007FF</code></p></td>
<td><p><code>00000xxx xxxxxxxx</code></p></td>
<td><p><code>110xxxxx 10xxxxxx</code></p></td>
<td><p>첫 바이트는 <code>110</code> 또는 <code>1110</code>으로 시작하고,<br />
나머지 바이트들은 <code>10</code>으로 시작함</p></td>
</tr>
<tr class="odd">
<td><p><code>000800-00FFFF</code></p></td>
<td><p><code>xxxxxxxx xxxxxxxx</code></p></td>
<td><p><code>1110xxxx 10xxxxxx 10xxxxxx</code></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><code>010000-10FFFF</code></p></td>
<td><p><code>110110ZZ ZZxxxxxx 110111xx xxxxxxxx</code></p></td>
<td><p><code>11110zzz 10zzxxxx 10xxxxxx 10xxxxxx</code></p></td>
<td><p>UTF-16 서러게이트 쌍 영역 (ZZZZ = zzzzz - 1).<br />
UTF-8로 표시된 비트 패턴은 실제 코드 포인트와 동일하다.</p></td>
</tr>
</tbody>
</table>

예를 들어서, 문자 "위"([`U+C704`](http://www.unicode.org/charts/PDF/UAC00.pdf))는 다음과 같은 방법으로 UTF-8로 인코딩된다.

  - 이 문자는 `U+0800`부터 `U+FFFF` 사이의 영역에 있으므로, 표에 따라 `1110xxxx 10xxxxxx 10xxxxxx` 형식으로 인코딩된다.
  - [16진수](https://ko.wikipedia.org/wiki/16진수 "wikilink") C704는 [2진수](https://ko.wikipedia.org/wiki/2진수 "wikilink") `1100-0111-0000-0100`와 같다.
  - 이 비트들은 순서대로 `x`로 표시된 비트에 들어 간다: `1110`**`1100`**`  10 `**`011100`**`  10 `**`000100`**
  - 결과적으로 이 문자는 3바이트로 인코딩된다. (16진수로 표시하면 `EC 9C 84`가 된다.)
  - PHP 를 할때 이것을 쓰지않으면 한국어가 깨지는 경우가 많이 일어난다

따라서 첫 128 문자는 1바이트로 표시되고, 그 다음 1920 문자\[1\]는 2바이트로 표시되며, 나머지 문자들 중 BMP 안에 들어 있는 것은 3바이트, 아닌 것은 4바이트로 표시된다.

위의 패턴을 사용하면 더 큰 코드 포인트를 표시할 수도 있다. 원래 UTF-8은 6바이트를 사용해서 `U+7FFFFFFF`까지의 코드 포인트를 표현할 수 있게 하였으나, [2003년](../Page/2003년.md "wikilink") 11월에 발표된 [RFC 3629에서는](https://ko.wikipedia.org/wiki/RFC_3629 "wikilink") 유니코드에서 실제로 정의하는 `U+10FFFF`까지의 문자만을 표시할 수 있도록 제한하였다. 따라서 이전까지는 UTF-8에서 나타날 수 없는 바이트가 `0xFE`와 `0xFF` 뿐이었지만, RFC 3629에 따라서 `0xC0`, `0xC1`, 그리고 `0xF5`부터 `0xFF`까지의 13개의 바이트가 나타날 수 없게 되었다.

## 변형된 UTF-8

[자바는](../Page/자바_\(프로그래밍_언어\).md "wikilink") 내부적으로 문자열을 [UTF-16](../Page/UTF-16.md "wikilink") 인코딩으로 저장하며, 문자열 직렬화를 위하여 UTF-8을 변형하여 사용하고 있다. 이를 [변형된 UTF-8](http://java.sun.com/j2se/1.5.0/docs/api/java/io/DataInput.html#modified-utf-8)이라 부른다.

표준 UTF-8과의 차이는 크게 두 가지로, 한 가지는 U+0000을 1바이트가 아니라 2바이트, 즉 11000000 10000000으로 표현하는 것이다. 따라서 수정된 UTF-8에서는 인코딩된 문자열에 널 문자가 나타나지 않게 되며, 따라서 널 문자를 문자열의 끝으로 사용하는 [C와](../Page/C_\(프로그래밍_언어\).md "wikilink") 같은 언어에서 처리할 때 문자열이 잘리는 것을 막을 수 있다.

다른 한 가지 차이는 BMP 바깥의 문자를 인코딩하는 방법이다. 표준 UTF-8에서는 이 문자들은 위와 같이 4바이트로 인코딩되지만, 수정된 UTF-8에서는 이 문자들을 surrogate pair로 표시하여 두 문자로 나눈 뒤 같은 방법으로 인코딩한다. (이는 [CESU-8](https://ko.wikipedia.org/wiki/CESU-8 "wikilink")과 동일하다) 이러한 방법은 자바의 문자 형이 16비트 크기이며, 따라서 U+10000 이상의 영역에 속한 유니코드 문자는 항상 두 개의 자바 문자로 표현되어야 한다는 것에서 유래하였다. 하지만 이 방법은 BMP 바깥의 문자를 UTF-8보다 더 긴 6바이트로 인코딩해야 한다.

이러한 차이 때문에 이 인코딩은 UTF-8과 엄격하게 구별해야 하며, 자바에서 내부적인 처리에만 사용하도록 권장된다. 또한 UTF-8과는 달리 IANA에 정식으로 등록된 문자 인코딩이 아니므로 인터넷 상의 정보 교환을 위해 사용하지 않아야 한다.

## UTF-8의 설계 원칙

그 구조로부터, UTF-8이 다음과 같은 성질을 가지고 있다는 것을 알 수 있다.

  - 1바이트로 표시된 문자의 최상위 비트는 항상 0이다.
  - 2바이트 이상으로 표시된 문자의 경우, 첫 바이트의 상위 비트들이 그 문자를 표시하는 데 필요한 바이트 수를 결정한다. 예를 들어서 2바이트는 110으로 시작하고, 3바이트는 1110으로 시작한다.
  - 첫 바이트가 아닌 나머지 바이트들은 상위 2비트가 항상 10이다.

UTF-8이 이런 성질을 가지도록 설계한 까닭은 어떤 경우에도 한 문자에 대한 바이트 표현이 다른 문자에 대한 바이트 표현의 일부가 되는 경우가 없도록 하기 위함이다. 따라서 텍스트 안에 들어 있는 다른 텍스트를 찾는 데 쓰이는 바이트 단위의 부문자열 매칭이 UTF-8 문자열에서도 쓰일 수 있다. [CP949](https://ko.wikipedia.org/wiki/CP949 "wikilink"), [상용 조합형](https://ko.wikipedia.org/wiki/상용_조합형 "wikilink"), [Shift-JIS](https://ko.wikipedia.org/wiki/Shift-JIS "wikilink"), [Big5](../Page/Big5.md "wikilink")과 같이 ISO 2022 체계에 부합하지 않는 이전의 가변 길이 인코딩은 그런 성질을 지니지 않았고(기존 인코딩 가운데 [EUC-KR](https://ko.wikipedia.org/wiki/EUC-KR "wikilink")이나 [EUC-JP](https://ko.wikipedia.org/wiki/EUC-JP "wikilink") 등은 이 점에서는 UTF-8과 비슷한 성질을 지닌다.), 더 복잡한 알고리즘을 써야 했다. 왜냐하면, 이들 인코딩은 ASCII 영역의 글자를 나타내는 바이트를 2바이트로 나타내는 다른 글자의 두 번째 바이트로 사용하기 때문이다. 또한, UTF-8에서 하나 이상의 바이트들이 손실되었을 때도, 다음의 정상 문자를 찾아서 동기화할 수 있기 때문에 피해를 줄일 수 있다.

그 설계 때문에 어떤 바이트들이 올바른 UTF-8로 확인되면, 그 문자열이 실제로 UTF-8로 인코딩되었을 가능성이 매우 높다. 임의의 바이트들이 순수한 ASCII 인코딩이 아닌 UTF-8 문자열일 가능성은 2바이트 문자의 경우 1/32, 3바이트 문자의 경우 5/256으로 매우 낮다. 또한 [ISO-8859-1](https://ko.wikipedia.org/wiki/ISO-8859-1 "wikilink")과 같은 기존의 인코딩으로 표현된 자연어 문자열이나 문서를 UTF-8로 표현된 것으로 오인할 가능성도 매우 낮다.

## 오류 처리

잘못된 입력이 들어 왔을 때 UTF-8 디코더가 해야 할 동작은 표준들에 일정하게 정의되어 있지 않다. 일반적으로 이러한 경우에 디코더가 취할 수 있는 동작은 다음과 같을 수 있다.

1.  U+003F(?, [물음표](../Page/물음표.md "wikilink"))나 U+FFFD(, 유니코드 [대치 문자](https://ko.wikipedia.org/wiki/대치_문자 "wikilink")) 같은 다른 문자를 집어 넣는다.
2.  해당 바이트들을 무시한다.
3.  해당 바이트들을 다른 인코딩으로 해석한다.
4.  오류로 처리하지 않고 UTF-8과 비슷한 형식으로 취급하여 디코딩한다. (이러한 동작은 디코더의 버그일 수도 있다)
5.  오류를 보고한다.

또한 디코더들은 다른 잘못된 입력에 대해서 다른 동작을 보일 수 있다.

RFC 3629에서는 UTF-8 디코더들이 ‘너무 긴 형식’, 즉 해당 문자를 표현하는 데 필요한 최소의 바이트보다 더 많은 바이트를 사용해서 표현한 바이트들을 잘못된 입력으로 처리해야 한다고 요구하고 있다. 유니코드 표준에서는 유니코드를 따르는 디코더가 ‘잘못된 형식으로 표현된 모든 단위 문자열을 오류로 처리하고, 따라서 잘못된 형식으로 표현된 단위 문자열을 해석하거나 생성해 내서는 안 된다’라고 요구하고 있다.

모든 가능한 해석은 장단점을 가지고 있으며, 만약 UTF-8을 해석하기 전에 검증이 이루어질 경우 보안 관련해서 주의가 요구된다.

너무 긴 형식은 처리하기 곤란한 경우 중 하나이다. 현재의 RFC에는 이러한 형식이 디코드되어서는 안 된다고 규정하고 있지만, 옛 UTF-8 표준에는 경고만 하였으며 대부분의 간단한 디코더들은 이러한 데이터를 정상적으로 해석한다. 이 형식은 실제로는 같은 코드 포인트를 서로 다른 두 개의 UTF-8 문자열로 나타내어 [마이크로소프트](../Page/마이크로소프트.md "wikilink")의 IIS 웹 서버와 같은 제품의 보안 검증을 우회하는 데 사용되었다.

잘못된 입력이 들어 왔을 때 보안을 지키기 위해서는 두 가지 선택이 있다. 한 가지는 입력을 검증하기 전에 항상 UTF-8로부터 디코드하는 것이며, 다른 한 가지는 잘못된 입력을 언제나 오류로 처리하는 엄격한 디코더를 사용하는 것이다.

## 장점과 단점

### 일반적으로

  - **장점**
      - ASCII 인코딩은 UTF-8의 부분 집합이다. 일반적인 ASCII 문자열은 올바른 UTF-8 문자열이며, 따라서 하위 호환성이 보장된다.
      - UTF-8 문자열은 바이트 단위로 정렬을 수행하는 알고리즘으로도 코드 포인트 단위로 올바르게 정렬할 수 있다. (일반적인 목적으로는 재정렬이 필요하다)
      - UTF-8과 UTF-16은 XML 문서의 표준 인코딩으로, 다른 인코딩들을 사용하려면 외부에서, 또는 문서 안에서 명시적으로 인코딩을 정해야 한다. [1](http://www.w3.org/TR/REC-xml/#charencoding)
      - 다른 인코딩과의 왕복 변환이 간단하다.
      - 바이트 단위 문자열 검색 알고리즘들을 그대로 사용할 수 있다.
      - 간단한 알고리즘을 통하여 UTF-8 문자열임을 확인할 수 있다. 즉, 다른 인코딩에서 나타나는 바이트들이 올바른 UTF-8 문자열일 가능성은 낮다.
      - U+0000을 표현할 때를 제외하면, 널 문자는 UTF-8 문자열 안에 나타나지 않는다. 따라서 널 문자로 끝나는 문자열을 사용하는 C 언어의 문자열 함수(strncpy() 같은)를 그대로 사용할 수 있다..
  - **단점**
      - 나쁘게 만들어진(그리고 현재 표준을 따르지 않는) UTF-8 파서는 서로 다른 가짜 UTF-8 표현(예를 들어서 너무 긴 형식)을 같은 유니코드 문자열로 해석할 수 있다.

### 기존의 인코딩들과 비교했을 때

  - **장점**
      - UTF-8은 모든 [유니코드](../Page/유니코드.md "wikilink") 문자를 표현할 수 있다. 예를 들어서, [UCS-2](https://ko.wikipedia.org/wiki/UCS-2 "wikilink")는 BMP 안의 문자만을 표현할 수 있다.
      - 바이트 경계를 순서대로 혹은 역순으로 찾기 쉽다. 만약 여러 바이트로 표시된 문자의 중간에서 찾기 시작한다면, 단지 해당 문자만 손실되고 나머지 문자들은 손상을 입지 않는다. 기존의 많은 다중바이트 인코딩들은 이러한 재동기화가 훨씬 힘들다.
      - 한 문자를 표현하는 바이트 표현은 다른 문자를 표현하는 어떤 바이트 표현에도 포함되지 않는다. 따라서 ASCII 문자가 아닌 값들에 투명한 파일 시스템이나 다른 소프트웨어(예를 들어서 C의 printf() 함수)와 호환성을 가진다.
      - 바이트 표현의 첫 바이트만 사용하여 해당 바이트 표현의 길이를 결정할 수 있다. 따라서 부분 문자열을 얻는 과정이 매우 쉽다.
      - 인코딩에 간단한 비트 연산만 사용되므로 효과적이다. UTF-8은 곱셈이나 나눗셈과 같은 느린 연산들을 사용하지 않는다.
  - **단점**
      - 대부분의 UTF-8 문자열은 일반적으로 적당한 기존 인코딩으로 표현한 문자열보다 더 크다. 판독 기호를 사용하는 대부분의 라틴 알파벳 문자는 적어도 2바이트를 사용하며, 한중일 문자들과 표의 문자들은 적어도 3바이트를 사용한다.
      - 한중일 문자들과 표의 문자를 제외한 거의 모든 기존 인코딩들은 한 문자에 1바이트를 사용하므로 문자열 처리가 간편한 반면, UTF-8은 그렇지 않다.

### [UTF-7](../Page/UTF-7.md "wikilink")과 비교했을 때

  - **장점**
      - UTF-8은 한 문자를 표현하는 데 UTF-7보다 더 적은 바이트들을 사용한다.
      - UTF-8은 "+"를 그대로 인코딩하지만 UTF-7은 "+-"로 인코딩한다.
  - **단점**
      - UTF-8은 8비트 안전한 전송 체계가 필요하다. 전자 우편에서 quoted-printable이나 base64 인코딩을 사용한다면 전송량이 더 많아진다. 예를 들어서 base64 인코딩의 경우 인코딩된 결과는 원본보다 약 33% 더 커진다. 하지만 최근에는 대부분의 [SMTP](https://ko.wikipedia.org/wiki/SMTP "wikilink") 서버가 [8BITMIME](https://ko.wikipedia.org/wiki/8BITMIME "wikilink")을 지원하기 때문에 이런 단점은 크게 부각되지 않는다.

### [UTF-16](../Page/UTF-16.md "wikilink")과 비교했을 때

  - **장점**
      - U+0000부터 U+007F까지의 공백과 문장 부호를 포함한 ASCII 문자들은 1바이트로 표현할 수 있기 때문에, 한중일 문자와 표의 문자를 사용하지 않는 대부분의 문자열을 UTF-16보다 더 작은 크기로 표현할 수 있다.
      - [유닉스](../Page/유닉스.md "wikilink")의 파일 시스템과 여러 도구들은 [옥텟을](../Page/옥텟_\(컴퓨팅\).md "wikilink") 기본 단위로 하며, [널 문자와](../Page/널_문자.md "wikilink") 경로 식별자(`/`, 0x2F)에 특별한 의미를 부여하는 경우가 많다. 0x00이나 0x2f 옥텟이 U+0000과 U+002F가 아닌 다른 문자에서도 나타날 수 있는 UTF-16 등의 인코딩과는 달리, UTF-8은 ASCII와 호환되기 때문에 0x00이나 0x2f 옥텟이 항상 U+0000과 U+002F에 대응되므로 기존 [API](../Page/API.md "wikilink")를 약간 수정해서 쓸 수 있다.
      - UTF-16은 바이트 순서를 나타내기 위하여 [바이트 순서 문자](../Page/바이트_순서_표식.md "wikilink")(BOM, U+FEFF)가 필요하지만, UTF-8은 바이트 순서가 정해져 있기 때문에 BOM이 필요하지 않다.
  - **단점**
      - UTF-8은 가변 길이 인코딩이며, 다른 문자는 다른 바이트 수로 표현될 수 있다. 사실 이 문제는 별로 심각한 것이 아니며, UTF-8 문자열을 다루기 위한 추상적인 인터페이스를 만드는 것으로 해결될 수 있다. 실제로 기술적으로는 UTF-16도 BMP 바깥 문자를 4바이트로 표현하기 때문에 가변 길이 인코딩이다.
      - BMP에 들어 있는 한중일 문자들은 UTF-8에서 3바이트로 표현되지만, UTF-16에서는 2바이트로 표현된다. 따라서 UTF-8에서는 이러한 문자를 표현하기 위하여 더 많은 바이트가 필요하며 UTF-16과 비교할 때 최대 50%까지 크기가 늘 수 있다. 하지만 반대로 U+0000부터 U+007F 사이의 글자들은 UTF-16에서 크기가 두 배로 늘기 때문에 실질적으로는 큰 문제가 없을 수도 있다.

## 같이 보기

  - [ASCII](https://ko.wikipedia.org/wiki/ASCII "wikilink")
  - [UCS](https://ko.wikipedia.org/wiki/UCS "wikilink")
  - [바이트 순서 문자](../Page/바이트_순서_표식.md "wikilink") (BOM)
  - [UTF-16](../Page/UTF-16.md "wikilink")

## 각주

## 외부 링크

  - [UTF-8이 만들어진 계기와 개요](http://www.cl.cam.ac.uk/~mgk25/ucs/utf-8-history.txt)
  - [유니코드 용어집](http://www.unicode.org/glossary)
  - [Java 언어를 이용한 유니코드 서로게이트 프로그래밍](http://www.ibm.com/developerworks/kr/library/j-unicode/index.html)
  - [Unicode / UTF8 변환 표](http://www.utf8-chartable.de/)

[분류:문자 인코딩](https://ko.wikipedia.org/wiki/분류:문자_인코딩 "wikilink") [분류:유니코드 변환 형식](https://ko.wikipedia.org/wiki/분류:유니코드_변환_형식 "wikilink")

1.  [발음 구별 기호가](../Page/발음_구별_기호.md "wikilink") 붙은 [라틴 문자](https://ko.wikipedia.org/wiki/라틴_문자 "wikilink"), [그리스 문자](../Page/그리스_문자.md "wikilink"), [키릴 문자](../Page/키릴_문자.md "wikilink"), [콥트 문자](../Page/콥트_문자.md "wikilink"), [아르메니아 문자](../Page/아르메니아_문자.md "wikilink"), [히브리 문자](../Page/히브리_문자.md "wikilink"), [아랍 문자](../Page/아랍_문자.md "wikilink")