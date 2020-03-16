> This article is converted from Wikipedia: [RPython](https://ko.wikipedia.org/wiki/RPython).


**RPython**(←)은 [파이썬](../Page/파이썬.md "wikilink") [프로그래밍 언어의](../Page/프로그래밍_언어.md "wikilink") [부분 집합이다](https://ko.wikipedia.org/wiki/부분_집합 "wikilink"). [PyPy](../Page/PyPy.md "wikilink")를 개발하기 위해 개발되었다.

효율적인 정적 컴파일을 위해 기능을 제한하고 있다. 표준 파이썬과 다르게 정적 타입을 사용한다.

번역기를 이용하여 RPython 코드를 [C](../Page/C_\(프로그래밍_언어\).md "wikilink"), [자바 바이트코드](../Page/자바_바이트코드.md "wikilink"), [공통 중간 언어와](../Page/공통_중간_언어.md "wikilink") 같은 [저급 언어로](https://ko.wikipedia.org/wiki/저급_언어 "wikilink") 변환할 수 있다. 인터프리터에 [JIT 컴파일러를](../Page/JIT_컴파일.md "wikilink") 만드는 생성기가 있다. 만들어진 JIT 컴파일러는 tracing JIT이다.

## 예제

아래의 예제는 [Low Level RPython](https://www.youtube.com/watch?v=kkt_BtR9Kzk)라는 강좌에 포함되어 있는 것을 옮긴 것이다.

``` python
# fib.py

def fib(n):
    if n < 2:
        return 1
    else:
        return fib(n-1) + fib(n-2)

# entry point. Like C main()
def main(argv):
    print fib(int(argv[1]))
    return 0

def target(*args):
    return main, None
```

RPython은 target이라는 함수가 돌려주는 함수에 대해 변환을 하므로 target을 반드시 정의해 줘야 한다. target이 돌려주는 변환 대상인 함수는 명령줄에 주어진 값을 인수로 받고 정수값을 돌려주는 형태여야 한다.

이 예제를 실행해 보는 일은 PyPy를 소스로부터 만드는 과정과 완전히 같은 것이다. 단지 대상만 PyPy 자신이 아니라 fib.py로 바뀌는 것이다.

    pypy <PyPy 소스 디렉토리>/rpython/bin/rpython fib.py

또는 CPython를 사용해서

    python <PyPy 소스 디렉토리>/rpython/bin/rpython fib.py

라고 해도 된다.

RPython은 엄청난 양의 출력을 쏟아 내면서 변환 과정을 진행한다. 컴퓨터의 성능에 따라 다르겠지만, 수십 초에서 길면 수 분도 걸리는 작업이다.

최종적으로 fib-c(윈도에서는 fib-c.exe)라는 파일을 만들어 낸다. 당연히 이 최종결과를 얻으려면 컴퓨터에 C 컴파일러가 설치되어 있어야 한다.

## 같이 보기

  - [PyPy](../Page/PyPy.md "wikilink")

## 외부 링크

  - [PyPy coding-guide/Restricted-Python](https://web.archive.org/web/20070707005837/http://codespeak.net/pypy/dist/pypy/doc/coding-guide.html#restricted-python)
  - 문서: [RPython's Documentation](http://rpython.readthedocs.org)

[분류:파이썬](https://ko.wikipedia.org/wiki/분류:파이썬 "wikilink")