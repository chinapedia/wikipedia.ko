> This article is converted from Wikipedia: [Foreach ](https://ko.wikipedia.org/wiki/Foreach_).


[섬네일](https://ko.wikipedia.org/wiki/파일:For-Loop-Mint-Programming-Language-Type-2.gif "wikilink") **For each**(또는 foreach)는 컬렉션 안의 항목들을 횡단하는 [제어 흐름](https://ko.wikipedia.org/wiki/제어_흐름 "wikilink") 문이다. Foreach는 표준 [For](https://ko.wikipedia.org/wiki/For_루프 "wikilink") [문](https://ko.wikipedia.org/wiki/문_\(프로그래밍\) "wikilink") 대신 사용되는 것이 일반적이다. 그러나 loop 구조체를 위한 다른 루프와 달리 foreach 루프\[1\]는 일반적으로 명시적인 카운터를 관리하지 않는다. 즉, "이것을 x번 하라"라고 하지 않고 "이 집합 안에서 모든 것에 대해 이것을 하라"라고 필수적으로 명시하게 된다. 잠재적인 [순환 횟수 오류](https://ko.wikipedia.org/wiki/순환_횟수_오류 "wikilink")(off-by-one error)를 예방하고 코드를 더 단순하게 읽힐 수 있게 만들어준다. 객체 지향 언어에서는 횡단을 위해 비명시적인 경우에도 [반복자](../Page/반복자.md "wikilink")가 종종 사용된다.

## 문법

문법은 언어에 따라 다양하다. 대부분은 다음과 비슷한 형태로 단순한 낱말 `for`를 사용한다:

`for each item in collection:`
`  do something to item`

## 언어 지원

### 펄

리스트 리터럴의 예:

``` Perl
foreach (1, 2, 3, 4) {
    print $_;
}
```

배열의 예:

``` Perl
foreach (@arr) {
    print $_;
}
```

``` Perl
foreach $x (@arr) { #$x is the element in @arr
    print $x;
}
```

해시(Hash)의 예:

``` Perl
foreach $x (keys %hash) {
    print $x . " = " . $hash{$x}; # $x is a key in %hash and $hash{$x} is its value
}
```

콜렉션 멤버들의 직접 수정:

``` Perl
@arr = ( 'remove-foo', 'remove-bar' );
foreach $x (@arr){
    $x =~ s/remove-//;
}
# Now @arr = ('foo', 'bar');
```

### 자바스크립트

Object 내의 키를 순서 없이 반복시키기 위해 자바스크립트는 `for...in` 루프를 사용한다:

``` JavaScript
for (var key in object) {
    // Do stuff with object[key]
}
```

## 같이 보기

  - [Do while 루프](https://ko.wikipedia.org/wiki/Do_while_루프 "wikilink")
  - [For 루프](https://ko.wikipedia.org/wiki/For_루프 "wikilink")
  - [While 루프](https://ko.wikipedia.org/wiki/While_루프 "wikilink")

## 각주

[분류:제어 흐름](https://ko.wikipedia.org/wiki/분류:제어_흐름 "wikilink")

1.