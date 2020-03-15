> This article is converted from Wikipedia: [-C](https://ko.wikipedia.org/wiki/-C).


**오브젝티브-C**()는 [C 프로그래밍 언어에](../Page/C_\(프로그래밍_언어\).md "wikilink") [스몰토크](https://ko.wikipedia.org/wiki/스몰토크 "wikilink") 스타일의 메시지 구문을 추가한 [객체 지향](https://ko.wikipedia.org/wiki/객체_지향 "wikilink") 언어이다. 현재, 이 언어는 [애플의](https://ko.wikipedia.org/wiki/애플_\(기업\) "wikilink") [매킨토시](../Page/매킨토시.md "wikilink")의 [운영 체제인](../Page/운영_체제.md "wikilink") [OS X과](https://ko.wikipedia.org/wiki/OS_X "wikilink") [아이폰](../Page/아이폰.md "wikilink")의 [운영 체제인](../Page/운영_체제.md "wikilink") [iOS](https://ko.wikipedia.org/wiki/iOS "wikilink")에서 사용되고 있다. 오브젝티브-C는 애플의 [코코아를](../Page/코코아_\(API\).md "wikilink") 사용하기 위한 기본 언어이며, 원래는 [넥스트의](https://ko.wikipedia.org/wiki/넥스트_사 "wikilink") NeXTSTEP [운영 체제에서](../Page/운영_체제.md "wikilink") 주 언어였다. 일반적인(Generic) 오브젝티브-C는 앞에서 언급한 라이브러리를 사용하지 않는다.

## 역사

1980년대 초, 소프트웨어 공학의 일반적 관행은 [구조적 프로그래밍의](https://ko.wikipedia.org/wiki/구조적_프로그래밍 "wikilink") 관습을 따르는 것이었다. 이 프로그래밍 기법은 프로그램을 잘개 쪼개어 작업하기 쉽도록 만드는 것을 돕기 위한 기법이었다. 하지만 풀어야 할 문제 규모가 커짐에 따라 [구조적 프로그래밍](https://ko.wikipedia.org/wiki/구조적_프로그래밍 "wikilink") 기법의 유용성은 감소하였는데, 더 많은 프로시저가 작성되어야 하다 보니 재사용성이 떨어지고 프로그램 제어 흐름도 복잡해지기 때문이었다.

많은 사람들은 [객체 지향 프로그래밍](../Page/객체_지향_프로그래밍.md "wikilink") 기법이 이 문제에 대한 해답이 될 수 있지 않을까 하고 생각하였다. 사실, [스몰토크](https://ko.wikipedia.org/wiki/스몰토크 "wikilink")라는 프로그래밍 언어는 이미 이러한 공학 이슈들을 섭렵하고 있었다. 세상에서 가장 복잡한 시스템들 중 몇몇이 [스몰토크](https://ko.wikipedia.org/wiki/스몰토크 "wikilink") 환경에서 작성되었다. 하지만 이 언어에도 한 가지 문제는 있었으니 [가상 머신을](../Page/가상_머신.md "wikilink") 사용하는 점이었다. [스몰토크](https://ko.wikipedia.org/wiki/스몰토크 "wikilink")의 가상 머신은 이미지(image)라고 불리는 객체 메모리를 두고 여기에 모든 개발 도구들을 저장해두었다. 그러다보니 메모리 요구량이 그 당시로는 비합리적일 정도로 늘어났고, 느리게 동작할 수 밖에 없었다. 이는 부분적으로는 가상머신(VM)이나 컨테이너(container) 개념을 쓸만하게 지원하는 하드웨어가 없었기 때문이기도 했다.

오브젝티브-C는 스텝스톤(Stepstone)이라는 회사에서 일하고 있던 [브래드 콕스](https://ko.wikipedia.org/wiki/브래드_콕스 "wikilink")(Brad Cox)와 톰 러브(Tom Love)라는 두 연구원이 만들었다. 역시 1980년대 초의 일이다. 이 두 사람은 1981년 ITT의 프로그래밍 기술 센터(Programming Technology Center)에서 일하던 시절 [스몰토크](https://ko.wikipedia.org/wiki/스몰토크 "wikilink")를 처음 접했다. 콕스는 소프트웨어 설계와 프로그래밍에 있어서 재사용성의 문제에 흥미를 느끼게 되었고, [스몰토크](https://ko.wikipedia.org/wiki/스몰토크 "wikilink")같은 프로그래밍 언어가 ITT 시스템 개발자들이 개발을 진행할 강력한 환경을 만드는 데 필요불가결한 요소임을 깨닫게 되었다. 콕스는 [C](../Page/C_\(프로그래밍_언어\).md "wikilink") 컴파일러를 고쳐 [스몰토크](https://ko.wikipedia.org/wiki/스몰토크 "wikilink")의 기능 일부를 추가하기 시작했고, 곧 그 스스로 OOPC라고 불렀던 C의 객체 지향 버전을 내놓게 되었다. 한편 러브는 1982년에 슐럼버거 리서치(Schlumberger Research)에 채용되었고, 스몰토크-80의 최초 상업적 버전을 써 볼 기회를 얻었다. 스몰토크-80은 이후 오브젝티브-C의 성장에 큰 영향을 끼쳤다.

새로운 언어가 가질 실질적인 파급력을 증명하기 위해, 콕스는 기존 툴에 몇 가지 사소한 변경만 가하면 재사용이 가능한 소프트웨어 컴포넌트를 만들 수 있음을 시연해보였다. 특히 컴포넌트들은 객체를 유연하게 지원해야 했고, 라이브러리들과 함께 제공되어야 했으며, 코드 (그리고 그 코드가 필요로 하는 자원들)는 하나의 단일한 플랫폼-중립적 포맷으로 저장될 수 있어야 했다.

결국 콕스와 러브는 프로덕티비티 프로덕츠 인터네셔널(Productivity Products International; PPI)이라는 새로운 벤처 회사를 설립한다. 목적은 오브젝티브-C 컴파일러와 강력한 클래스 라이브러리를 결합한 상업 제품을 만들어 파는 것이었다.

1986년에 콕스는 오브젝티브-C의 명세를 담은 책 "객체 지향 프로그래밍"(Object-Oriented Programming, An Evolutionary Approach)를 출간한다. 이 책에서 그는 재사용성의 문제가 단순히 언어 차원의 문제가 아님을 지적하였으나, 이후 오브젝티브-C는 종종 다른 언어와 기능적으로 비교되고는 했다.

### NeXT로 인기를 얻다

[스티브 잡스는](../Page/스티브_잡스.md "wikilink") [애플을](https://ko.wikipedia.org/wiki/애플_\(기업\) "wikilink") 떠난 후, [넥스트라는](../Page/NeXT.md "wikilink") 회사를 설립한다. 1988년, 넥스트는 스텝스톤(StepStone; 앞에서 말한 PPI 회사의 새로운 이름이며, 오브젝티브-C의 상표권자이다.)에게 오브젝티브-C의 사용 허가를 받고, 오브젝티브-C를 지원하기 위하여 [GCC](https://ko.wikipedia.org/wiki/GCC "wikilink") 컴파일러를 확장시키고 나서, [넥스트스텝](https://ko.wikipedia.org/wiki/NeXTSTEP "wikilink") 사용자 인터페이스와 [인터페이스 빌더](../Page/인터페이스_빌더.md "wikilink")(Interface Builder)를 구축하는 데 쓰일 앱키트(AppKit)와 파운데이션 키트(Foundation Kit)를 개발했다. 비록 넥스트가 내놓은 워크스테이션들은 시장에 강력한 영향력을 행사하지는 못했지만, 그 툴들만큼은 업계에 널리 퍼지게 되었다. 결국 넥스트는 하드웨어 제작을 포기하고 소프트웨어 툴들에 집중하기로 방향을 선회하여 [넥스트스텝](https://ko.wikipedia.org/wiki/NeXTSTEP "wikilink") (그리고 [오픈스텝](../Page/오픈스텝.md "wikilink")(OpenStep))을 독립적인 사용자 프로그래밍 환경으로 판매하기 시작했다.

이 때 [넥스트스텝의](https://ko.wikipedia.org/wiki/NeXTSTEP "wikilink") 무료버전을 구축하려는 프로젝트가 [GNU](../Page/GNU.md "wikilink")에서 시작되었는데, 그 이름은 [그누스텝](../Page/그누스텝.md "wikilink")(GNUstep)이었으며, [오픈스텝](../Page/오픈스텝.md "wikilink") 표준에 바탕을 둔 것이었다. 1992년 데니스 글래팅(Dennis Glatting)이 GNU 오브젝티브-C의 런타임을 처음으로 작성했다. 1993년 이후로는 크레스텐 크랩 토룹(Kresten Krab Thorup)이 덴마크에서 대학생 시절에 만든 런타임이 널리 쓰였다. 토룹 또한 1993년부터 1996년까지 넥스트에서 일했다.

1996년에 넥스트는 [애플에](https://ko.wikipedia.org/wiki/애플_\(기업\) "wikilink") 합병되었다. [애플은](https://ko.wikipedia.org/wiki/애플_\(기업\) "wikilink") [오픈스텝](../Page/오픈스텝.md "wikilink")을 기반으로 [맥 OS X라는](https://ko.wikipedia.org/wiki/맥_OS_X "wikilink") 새로운 [운영 체제를](../Page/운영_체제.md "wikilink") 내놓는다. 이 안에는 오브젝티브-C와, 넥스트의 오브젝티브-C 기반 개발 툴들이 포함되어 있었다. 프로젝트 빌더(Project Builder) (나중에 [엑스코드](../Page/엑스코드.md "wikilink")(Xcode)라는 이름으로 바뀐다)라는 개발환경이 제공되었고, [인터페이스 빌더라는](../Page/인터페이스_빌더.md "wikilink") 인터페이스 설계 툴이 제공되었다. 오늘날 애플의 [Cocoa API](../Page/코코아_\(API\).md "wikilink") 대부분은 [오픈스텝](../Page/오픈스텝.md "wikilink") 인터페이스 객체에 기반을 둔 것이며, 아마 이것이 현존하는 오브젝티브-C 개발 환경 중 가장 널리 쓰이면서도 중요한 것일 것이다.

## 문법

오브젝티브-C는 C 위에 덮인 얇은 층이라 볼 수 있다. 오브젝티브-C는 [C++](https://ko.wikipedia.org/wiki/C++ "wikilink")와 달리 C 언어의 *엄격한* 상위집합이다. 엄격한 상위집합이라는 말은 모든 C프로그램은 다 오브젝티브-C로 컴파일 가능하며, 프로그램의 의미도 양 언어가 동일하다는 의미이다. 오브젝티브-C는 C 언어와 스몰토크 양쪽에서 유래한 문법을 사용하고 있다. 전처리(preprocessing), 표기(expressions), 함수 선언(function declarations), 그리고 함수 호출(function calls) 등과 같은 대부분의 문법은 C에서 상속된 것이며, 객체 지향적인 기능들은 스몰토크 방식의 메시지 전달을 통해서 구현되었다.

C++와는 달리 다중상속을 지원하지 않으며, 그 대신 [자바의](../Page/자바_\(프로그래밍_언어\).md "wikilink") 인터페이스에 해당하는 프로토콜(protocol)을 정의할 수 있다. 또한 카테고리(category)를 통해 기존 클래스에 새로운 메쏘드를 추가함으로써 클래스의 기능을 확장할 수 있다. 이는 상속을 통해서만 기능을 확장할 수 있는 대다수의 객체 지향 언어와 크게 구별되는 특성이다. C++나 자바 등과는 달리 객체에 대해서 완전한 동적 형 변환(dynamic typing)을 지원한다.

### 메시지

메시지는 [객체 지향 프로그래밍을](../Page/객체_지향_프로그래밍.md "wikilink") 지원하기 위해 내부적으로 추가된 문법이다. 오브젝티브-C의 객체 지향 프로그래밍에 대한 모델로 메시지를 객체에 전달하는 방식을 채용하고 있다. 이는 스몰토크와 매우 유사한 모델이다. 하지만 이는 C++와 다른 언어에서 사용하는 [시뮬라](../Page/시뮬라.md "wikilink")(Simula) 프로그래밍 모델과는 구별되는 것이다. 이러한 특징은 중요한 의미를 갖는다. 오브젝티브-C의 기본적인 차이점은 *메소드를 호출*하는 것이 아니라 *메시지를 전달*한다는 것이다.

`doSomething`이라는 메서드를 갖는 클래스로부터 `obj`라는 개체가 구현된다면 이는 메시지 `doSomething`에 대해서 "응답"하는 것이다. C++에서는 `doSomething` 메시지를 `obj`로 보내는 행위는 다음과 같은 코드를 필요로 할 것이다:

``` cpp
obj.doSomething();
```

오브젝티브-C에서는 다음과 같이 쓰인다:

``` objc
[obj doSomething];
```

이러한 작동 방식은 심지어 객체가 메시지에 응답할 수 없다 하더라도 그 개체에 메시지를 보낼 수 있도록 해준다.

오브젝티브-C는 동적 형 변환을 사용한다. 이는 모든 메소드가 사전에 정의되어야만 호출이 가능한 C++이나 자바와 같은 정적·명시적 형 변환을 사용하는 언어와 다른 점이다.

[C++](https://ko.wikipedia.org/wiki/C++ "wikilink")과 다르게 가상함수의 선언없이 [자바와](../Page/자바_\(프로그래밍_언어\).md "wikilink") 같이 자식클래스에서 메소드를 오버라이딩 하는 것 만으로 다형성이 제공된다.

### 클래스의 선언과 구현

C++와 비슷하게 클래스의 선언과 구현은 헤더파일과 소스파일로 나뉜다. 헤더파일의 확장자는 .h로 동일하나 소스파일의 확장자는 .c나 .cpp가 아닌 .m(.c 에 대응) 또는 .mm(.cpp 에 대응)이다. 확장자가 .m 또는 .mm으로 정해진 이유는 단지 .o와 .c가 C에 의해 사용되고 있었기 때문이다.\[1\]

#### 선언(Interface)

선언(interface)은 클래스의 기본적인 구조를 열거하는 것이며, 일반적으로 헤더파일 .h에 기록된다.

``` objc
@interface classname : superclassname // 부모클래스 이름
{
    // 클래스 변수
}
+ classMethod1; // 클래스 메소드
+ (return_type)classMethod2;
+ (return_type)classMethod3:(param1_type)param1_varName;

- (return_type)instanceMethod1:(param1_type)param1_varName :(param2_type)param2_varName; // 인스턴스 메소드
- (return_type)instanceMethod2WithParameter:(param1_type)param1_varName andOtherParameter:(param2_type)param2_varName;
@end
```

클래스의 선언은 @interface로 시작하고 @end로 끝난다. +기호는 클래스 메소드를 뜻한다. [자바의](../Page/자바_\(프로그래밍_언어\).md "wikilink") 정적메소드와 동일하며, 선언된 클래스의 인스턴스의 유무에 상관없이 항상 존재한다. 클래스 메소드는 클래스 변수에 대한 접근권한이 없다. -기호는 인스턴스 메소드이며 클래스가 인스턴스화가 되어야만 사용할 수 있다.

메소드에 매개변수가 있을 경우 일반적인 프로그래밍 언어와 다르게 괄호대신 콜론으로 구분한다. 변수가 2개 이상일 경우 그 해당 변수가 무슨 역할을 하는지 라벨을 따로 붙여준다. 이 레이블은 코드를 더 읽기 쉽게 도와준다.

``` objc
- (void)setRangeStart:(int)start end:(int)end;
- (void)setWithLatename:(NSString *)last firstname:(NSString *)first middlename:(NSString *)middle;
```

실제 코드 상에선 다음과 같이 호출된다.

``` objc
[setRangeStart:4 end:10];
[setWithLatename:@"Last" firstname:@"First" middlename:@"Middle"];
```

#### 구현(Implementation)

``` objc
@implementation classname
+ (return_type)classMethod
{
    // 구현
}
- (return_type)instanceMethod
{
    // 구현
}
@end
```

클래스의 구현은 @implementation으로 시작하고 @end로 끝난다. 클래스 변수를 다시 적을 필요는 없고, 선언한 메소드의 구현만 하면된다.

### 프로토콜(Protocols)

[NeXT](../Page/NeXT.md "wikilink")는 오브젝티브-C에 [다중 상속을](https://ko.wikipedia.org/wiki/다중_상속 "wikilink") 스펙(specification)에 도입하기 위하여 확장하였지만, 그러나 구현(implementation)하지는 못 했으며, 단지 [프로토콜만을](https://ko.wikipedia.org/wiki/protocol_\(object-oriented_programming\) "wikilink") 도입했다. 이것은 [C++](https://ko.wikipedia.org/wiki/C++ "wikilink")에서 추상적으로 다중 상속되는 기본 클래스 또는 [자바 (프로그래밍 언어)나](../Page/자바_\(프로그래밍_언어\).md "wikilink") [C\#에서](../Page/C_샤프.md "wikilink") "인터페이스(interface)"를 성취하기 위한 패턴이다. 오브젝티브-C는 비공식 프로토콜(informal protocol)이라고 불리는 ad-hoc 프로토콜과, 공식 프로토콜이라고 불리는 컴파일러가 강제하는 프토토콜을 통해 다중 상속과 유사한 기능을 하도록 만들 수 있다. 참고로 후에 개발된 [자바 (프로그래밍 언어)의](../Page/자바_\(프로그래밍_언어\).md "wikilink") 경우에도 다중 상속을 지원하지 않고 인터페이스라는 이름으로 오브젝티브-C의 프로토콜의 개념을 사용한다.\[2\]

비공식 프로토콜(Informal protocols)은 클래스가 구현할 수 있는 메소드의 리스트이다. 클래스가 구현하기 위하여 선택한 메소드 리스트이다. 이것은 그 문서에 명세 되어 있는데, 왜냐하면 언어 안에는 그 리스트를 표현하기 위한 문법이 없기 때문이다. 비공식 프로토콜은 종종 선택적 메소드(optional method)를 포함하는데, 이 메소드가 구현되면, 클래스의 동작(behavior)이 바뀔 수 있기 때문이다. 예를 들어, 텍스트 필드 클래스는 유저가 타이핑한 글을 자동 완성 기능(auto-complete feature)을 수행하기 위한 선택적 메소드를 가진 비공식 프로토콜 구현하기 위한 [대리자를](https://ko.wikipedia.org/wiki/Delegation_\(programming\) "wikilink") 가질 수 있다. 그 텍스트 필드는 그 위임이 그 메소드를 ([반영 (컴퓨터 과학)](https://ko.wikipedia.org/wiki/반영_\(컴퓨터_과학\) "wikilink")(Reflection)을 통해서) 구현되며, 그것이 분명하면, 자동 완성 기능을 지원하기 위하여 그 위임된 메소드를 호출한다.

공식 프로토콜(formal protocol)은 자바와 C\#의 인터페이스와는 유사하다. 이 프로토콜은 어떤 클래스가 메소드들을 구현하기 하기 위한 리스트이다. 오브젝티브-C 2.0 이전 버전들에서는 클래스는 그 자신 스스로 채택하여 선언하고 있는 프로토콜 안에 들어 있는 모든 메소드를 구현해야 한다고 요구하고 있다; 반면에 컴파일러는 만약 그 클래스에서 선언된 프로토콜이 가지고 있는 모든 메소드가 구현되지 않았다면 에러를 생략할 것이다. 오브젝티브-C 2.0은 프로토콜 안에 있는 특정 메소드가 선택적(optional)이라고 표시하기 위한 지원을 추가했으며, 컴파일러는 선택적(optional) 메소드들을 강제로 구현하지 않을 것이다.

오브젝티브-C이 가지고 있는 프로토콜(protocols) 개념은 [자바나](../Page/자바_\(프로그래밍_언어\).md "wikilink") [C\#의](../Page/C_샤프.md "wikilink") 인터페이스와는 좀 다르다. 왜냐하면 클래스를 구현할 때, 특정 프로토콜을 구현하도록 선언하지 않아도 그 프로토콜을 구현해 버릴 수 있기 때문이다. 그 차이는 외부 코드에서는 알아챌 수 없다. 공식 프로토콜은 어떤 구현도 제공할 수 없으며, 단순히 특정한 프로토콜을 만족하는 클래스는 해당 프로토콜에 속한 모든 메소드를 구현해야 한다는 것을 강제하기 위해 쓰인다. 넥스트/애플 라이브러리에서, 프로토콜은 분산 객체 시스템(Distributed Objects system)에서 어떤 원격 시스템에서 일하는 객체의 능력을 표현하기 위하여 자주 사용된다.

구문

``` obic
@protocol Locking
- (void)lock;
- (void)unlock;
@end
```

이것은 락을 걸고 푼다는 추상 아이디어를 명시하고 있다. 클래스를 정의할 때에는 다음과 같이 쓴다.

``` objc
@interface SomeClass : SomeSuperClass <Locking>
@end
```

SomeClass에 의해 만들어진 객체들은 Locking 프로토콜에 명시된 두 개의 인스턴스 메소드의 구현을 제공할 것임을 명시하고 있다. 일례로 이런 추상화된 명세법은 구현 계층(hierarchy)이 어떻게 만들어져야하는지를 지정하지 않더라도 플러그인에 요구되는 행위 형태를 기술할 수 있어서 특히 효과적이다.

## [헬로 월드 프로그램](https://ko.wikipedia.org/wiki/헬로_월드_프로그램 "wikilink")

``` objc

#import <Foundation/Foundation.h>

int main (int argc, const char * argv[]) {
    NSAutoreleasePool * pool = [[NSAutoreleasePool alloc] init];  //AutoreleasePool을 할당하고 초기화

    NSString *helloWorldStr = [NSString stringWithString:@"Hello World!"]; // helloWorldStr에 "Hello World!" 대입
    NSLog(@"%@",helloWorldStr); // 출력
    [pool drain];  //AutoreleasePool Drain
    return 0;
}
```

``` objc
// 최근의 문법 변경으로 쉬워짐
#import <Foundation/Foundation.h>

int main (int argc, const char * argv[]) {
    @AutoreleasePool //AutoreleasePool을 할당하고 초기화

    NSLog(@"  Hello World");
    return 0;
}
```

이 프로그램은 표준 콘솔 출력으로 `Hello World!`를 출력한다. 원래 6, 7번째 줄을 NSLog(@"Hello World\!"); 로 바꾸어도 동일하게 동작하지만, C와, 오브젝티브-C의 다른 점을 보여주기 위해 NSString형의 helloWorldStr 변수를 이용하여 표현하였다.

## 변종

### 오브젝티브-C++

오브젝티브-C++은 [GNU 컴파일러 모음](../Page/GNU_컴파일러_모음.md "wikilink")(GCC)과 [클랭](../Page/클랭.md "wikilink")에 대한 프론트엔드가 수용하는 언어 변종이다. C++와 오브젝티브-C 문법의 모음을 이용하는 소스 파일을 컴파일할 수 있다. 오브젝티브-C++는 C++에 오브젝티브-C의 C 추가 확장 기능을 포함시킨다.

### 오브젝티브-C 2.0

2006년 [세계 개발자 회의에서](https://ko.wikipedia.org/wiki/애플_세계_개발자_회의 "wikilink") 애플은 "현대적인 가비지 콜렉션, 문법 기능 향상\[3\], 런타임 성능 개선\[4\], 64비트 지원"을 포함하는, 오브젝티브-C 언어의 리비전으로서 오브젝티브 C-2.0 공개를 발표하였다.

## 각주

## 외부 링크

  - *[The Objective-C 2.0 Programming Language](https://developer.apple.com/library/mac/#documentation/Cocoa/Conceptual/ObjectiveC/Introduction/introObjectiveC.html)* - 애플
  - [Objective-C GNUstep Base Programming Manual](http://www.gnu.org/software/gnustep/resources/documentation/Developer/Base/ProgrammingManual/manual_toc.html)
  - [Objective-C by Brad Cox](https://web.archive.org/web/20120204044211/http://virtualschool.edu/objectivec/)
  - [Objective-C FAQ](http://www.faqs.org/faqs/computer-lang/Objective-C/faq/)

[오브젝티브-C](https://ko.wikipedia.org/wiki/분류:오브젝티브-C "wikilink") [분류:객체 지향 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:객체_지향_프로그래밍_언어 "wikilink") [분류:1986년 개발된 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:1986년_개발된_프로그래밍_언어 "wikilink") [분류:C 프로그래밍 언어 계열](https://ko.wikipedia.org/wiki/분류:C_프로그래밍_언어_계열 "wikilink") [분류:NeXT](https://ko.wikipedia.org/wiki/분류:NeXT "wikilink")

1.  [Why do Objective C files use the .m extension?](http://stackoverflow.com/questions/652186/why-do-objective-c-files-use-the-m-extension), 오브젝티브-C의 개발자인 Brad Cox의 답변.
2.  181쪽,
3.
4.