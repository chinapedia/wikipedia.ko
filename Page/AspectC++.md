> This article is converted from Wikipedia: [AspectC++](https://ko.wikipedia.org/wiki/AspectC++).


**AspectC++**는 [C와](../Page/C_\(프로그래밍_언어\).md "wikilink") [C++](https://ko.wikipedia.org/wiki/C++ "wikilink") 언어의 [관점 지향](../Page/관점_지향_프로그래밍.md "wikilink") 확장이다. AspectC++ [소스 코드를](../Page/소스_코드.md "wikilink") 호환 C++로 번역하는 [소스 대 소스 컴파일러를](https://ko.wikipedia.org/wiki/소스_코드_번역 "wikilink") 보유하고 있다. 이 컴파일러는 [GNU GPL](../Page/GNU_일반_공중_사용_허가서.md "wikilink") 하에서 이용할 수 있으나 일부 [마이크로소프트 윈도우에](../Page/마이크로소프트_윈도우.md "wikilink") 특화된 [확장들은](../Page/컴퓨팅.md "wikilink") 순수 시스템 GmbH를 통해서만 이용이 가능하다.

[관점 지향 프로그래밍은](../Page/관점_지향_프로그래밍.md "wikilink") 횡단 관심사를 하나의 [모듈](../Page/프로그래밍_언어.md "wikilink"), 즉 [관점](../Page/컴퓨터_과학.md "wikilink")(애스펙트, aspect)로 모듈화하는 것을 허용한다. 애스펙트는 기존의 [클래스를](../Page/컴퓨터_과학.md "wikilink") 수정할 수 있지만 대체적으로는 기존 기능의 이전(before), 이후(after), 주변(around)에 실행할 "어드바이스"(advice)를 제공한다.

## 예

특정 기능에 대한 모든 호출들은 'cerr'이나 인쇄문을 여러 곳에 삽입하지 않고 애스펙트를 사용하여 추적할 수 있다:

``` aspectj
aspect Tracer
{
   advice call("% %Iter::Reset(...)") : before()
   {
      cerr << "about to call Iter::Reset for " << JoinPoint::signature() << endl;
   }
};
```

Tracer 애스펙트는 `%Iter::Reset`에 대한 호출 이전에 메시지를 출력한다. `%Iter` 문법은 Iter로 끝나는 모든 클래스와 일치시킨다는 것을 의미한다.

소스 코드 내에서 각각의 '일치된' 위치는 [조인 포인트라](https://ko.wikipedia.org/wiki/조인_포인트 "wikilink") 부르며, 어드바이스는 해당 코드와 결합된다. AspectC++은 조인 포인트 API를 제공함으로써 해당 조인 포인트에 대한 정보를 제공하고 접근할 수 있게 한다. 이를테면 다음의 함수가 있다고 하면,

``` cpp
JoinPoint::signature()
```

호출될 함수의 이름(`%Iter::Reset`와 일치되는)을 반환한다.

## 각주

## 외부 링크

  - [AspectC++](http://www.aspectc.org/)
  - [Articles on aspect-oriented programming and AspectC++ at past AOSD conferences](http://www.aosd.net)

[분류:관점 지향 프로그래밍](https://ko.wikipedia.org/wiki/분류:관점_지향_프로그래밍 "wikilink") [분류:C++ 프로그래밍 언어 계열](https://ko.wikipedia.org/wiki/분류:C++_프로그래밍_언어_계열 "wikilink")