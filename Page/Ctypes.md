> This article is converted from Wikipedia: [Ctypes](https://ko.wikipedia.org/wiki/Ctypes).


**ctypes**는 [파이썬](https://ko.wikipedia.org/wiki/파이썬 "wikilink")의 [외부 함수 인터페이스](../Page/외부_함수_인터페이스.md "wikilink")(FFI) 라이브러리로, 파이썬 2.5부터 기본으로 포함되어 있다. [윈도의](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") [DLL](https://ko.wikipedia.org/wiki/DLL "wikilink")과 같은 [동적 라이브러리에](https://ko.wikipedia.org/wiki/동적_라이브러리 "wikilink") 있는 함수를 직접 호출할 수 있으며, 다양한 C 자료형을 다루기 위한 인터페이스를 제공한다. 이를 사용해 순수 파이썬 코드만으로 확장 모듈을 구현할 수도 있다.

## 예제

다음은 윈도 환경에서 msvcrt.dll의 printf 함수를 호출하는 예이다. 이미 존재하는 함수의 원형을 파이썬 환경에 적절하도록 고치는 예를 볼 수 있다.

``` python
>>> from ctypes import *
>>> printf = cdll.msvcrt.printf
>>> printf("hello world\n")
hello world
12
>>> printf.restype = None
>>> printf("hello world\n")
hello world
```

ctypes는 별도로 함수 원형을 지정하지 않아도 내부적으로 스택을 조사하여 함수의 원형을 확인하려 시도하며, 윈도 같은 환경에서는 [세그먼트 위반](https://ko.wikipedia.org/wiki/세그멘테이션_오류 "wikilink") 같은 치명적인 오류를 예외로 처리해 준다.

``` python
>>> cdll.msvcrt.strlen(None)
Traceback (most recent call last):
  File "<stdin>", line 1, in ?
WindowsError: exception: access violation reading 0x00000000
```

## 외부 링크

  - [ctypes 공식 홈페이지](https://web.archive.org/web/20061207042530/http://python.net/crew/theller/ctypes/)

  - [소스포지 프로젝트](http://sourceforge.net/projects/ctypes)

  - [한국 파이썬 사용자 모임 위키의 관련 글](https://web.archive.org/web/20060202233252/http://www.python.or.kr/pykug/CtypesModule)

[분류:파이썬](https://ko.wikipedia.org/wiki/분류:파이썬 "wikilink")