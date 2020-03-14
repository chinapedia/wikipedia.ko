> This article is converted from Wikipedia: [Eval](https://ko.wikipedia.org/wiki/Eval).


**`eval`** 함수는 일부 [프로그래밍 언어에서](https://ko.wikipedia.org/wiki/프로그래밍_언어 "wikilink") 제공하는 [함수의](https://ko.wikipedia.org/wiki/함수_\(프로그래밍\) "wikilink") 일종이다. 문자열을 입력 받아 그 문자열을 [expression으로](https://ko.wikipedia.org/wiki/식_\(프로그래밍\) "wikilink") 처리한 후 결과값을 반환하는 함수이다.

## 보안 위험

신뢰할 수 없는 장소로부터 온 데이터에 `eval`을 사용할 때는 특별히 주의해야 한다. 이를테면, `get_data()` 함수는 인터넷으로부터 데이터를 가져온다고 할 때, 이 [파이썬](https://ko.wikipedia.org/wiki/파이썬 "wikilink") 코드는 안전하지 않다:

``` python
session['authenticated'] = False
data = get_data()
foo = eval(data)
```

공격자가 프로그램에 `"session.update(authenticated=True)"` 문자열을 데이터로 공급하면 `session` 디렉터리를 업데이트하여 인증 키를 True로 설정한다. 이를 해결하려면 `eval`을 사용하는 모든 데이터를 회피하거나 잠재적으로 유해한 기능에 대한 접근이 없는 상태에서 실행하여야 한다.

## 프로그래밍에서의 이용

### PHP

``` php
$name = 'John Doe';
$greeting = 'Hello';
$template = '"$greeting,  $name! How can I help you today?"';
print eval("return $template;");
```

### 자바스크립트

이때의 결과는 12+34의 결과인 46으로 alert창이 뜨게 된다.

``` javascript numberLines
foo = 12+34;
alert(eval(foo));
```

### 펄

``` perl
$foo = 2;
print eval('$foo + 2'), "\n";
```

### 루비

``` ruby
a = 1
eval('a + 1') #  (evaluates to 2)

# evaluating within a context
def get_binding(a)
  binding
end
eval('a+1',get_binding(3)) # (evaluates to 4, because 'a' in the context of get_binding is 3)
```

## 외부 링크

  - [ANSI and GNU Common Lisp Document: eval function](https://web.archive.org/web/20030322002401/http://www.cs.queensu.ca/software_docs/gnudev/gcl-ansi/gcl_256.html)

  - [Python Library Reference: eval built-in function](https://web.archive.org/web/20080930143344/http://docs.python.org/lib/built-in-funcs.html#l2h-25)

  - [Jonathan Johnson on exposing classes to RBScript](http://www.nilobject.com/?p=138)

[분류:제어 흐름](https://ko.wikipedia.org/wiki/분류:제어_흐름 "wikilink")