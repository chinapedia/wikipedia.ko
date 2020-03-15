> This article is converted from Wikipedia: [D \( \)](https://ko.wikipedia.org/wiki/D_\(_\)).


**D**는 [디지털 마스의](https://ko.wikipedia.org/wiki/디지털_마스 "wikilink") [월터 브라이트가](https://ko.wikipedia.org/wiki/월터_브라이트 "wikilink") 개발한 [객체 지향](https://ko.wikipedia.org/wiki/객체_지향_프로그래밍 "wikilink") [명령형](https://ko.wikipedia.org/wiki/명령형_프로그래밍 "wikilink") 프로그래밍 언어이다. 2001년 공개되었다. [C++](https://ko.wikipedia.org/wiki/C++ "wikilink")의 리엔지니어링으로 기원하였으나 D는 해당 언어와는 별개의 언어이다. 일부 핵심 C++ 기능들을 다시 설계하였으며 [자바](../Page/자바_\(프로그래밍_언어\).md "wikilink"), [파이썬](../Page/파이썬.md "wikilink"), [루비](../Page/루비.md "wikilink"), [C\#](https://ko.wikipedia.org/wiki/C_샤프 "wikilink"), [에펠](https://ko.wikipedia.org/wiki/에펠 "wikilink")과 같은 다른 언어들의 특징들을 공유하기도 한다.

이 언어의 설계 목적은 현대의 [동적](../Page/동적_프로그래밍_언어.md "wikilink") 언어의 [표현 능력을](https://ko.wikipedia.org/wiki/표현_능력 "wikilink") 가지고 [컴파일 언어의](../Page/컴파일_언어.md "wikilink") 성능과 안전의 병합을 시도하는 것이다. 관용적인 D 코드는 동등한 C++ 코드보다 크기가 짧더라도 C++만큼 속도가 빠른 것이 보통이다.\[1\] 이 언어는 전반적으로 [메모리 안전에](../Page/메모리_보안.md "wikilink") 속하지 않으나\[2\] 메모리 안전을 검사하도록 설계된 선택적 속성을 포함한다.\[3\]

## 예제 코드

### 헬로 월드 프로그램

``` d
import std.stdio;

int main(string args[])
{
    writeln("안녕. D Programming Language!");
    return 0;
}
```

### 예제2

다음 예제는 콘솔에 명령행 인자를 출력한다.

``` d
import std.stdio: writefln;

void main(string[] args)
{
    foreach (i, arg; args)
        writefln("args[%d] = '%s'", i, arg);
}
```

## 구현

현재의 대부분의 D 구현체는 효율적인 실행을 위해 [기계어](../Page/기계어.md "wikilink")로 직접 [컴파일](https://ko.wikipedia.org/wiki/컴파일 "wikilink")한다.

  - DMD (Digital Mars D. 창시자인 월터 브라이트가 주도하는 메인 프로젝트.)
  - GDC ([GCC](https://ko.wikipedia.org/wiki/GCC "wikilink") 백엔드용 프론트엔드)
  - LDC ([LLVM](../Page/LLVM.md "wikilink")을 백엔드로 사용하는 프론트엔드)
  - D 컴파일러 포 닷넷

## 관련 항목

  - [DMD 컴파일러](https://ko.wikipedia.org/wiki/DMD_컴파일러 "wikilink")

## 각주

## 외부 링크

  - [디지털 마르스의 D 프로그래밍 언어 페이지](http://www.digitalmars.com/d/)
  - [gdc](http://dgcc.sourceforge.net/): [GCC용](https://ko.wikipedia.org/wiki/GNU_컴파일러_모음 "wikilink") 프론트 엔드
  - [D언어 홈페이지](https://dlang.org/)

[분류:크로스 플랫폼 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_소프트웨어 "wikilink") [분류:다중 패러다임 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:다중_패러다임_프로그래밍_언어 "wikilink") [분류:객체 지향 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:객체_지향_프로그래밍_언어 "wikilink") [분류:절차적 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:절차적_프로그래밍_언어 "wikilink") [분류:2001년 개발된 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:2001년_개발된_프로그래밍_언어 "wikilink") [분류:C 프로그래밍 언어 계열](https://ko.wikipedia.org/wiki/분류:C_프로그래밍_언어_계열 "wikilink") [분류:시스템 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:시스템_프로그래밍_언어 "wikilink") [분류:자유 컴파일러와 인터프리터](https://ko.wikipedia.org/wiki/분류:자유_컴파일러와_인터프리터 "wikilink")

1.
2.   "It's close, and we're working to close the remaining gaps."
3.