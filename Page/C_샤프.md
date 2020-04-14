> This article is converted from Wikipedia: [C 샤프](https://ko.wikipedia.org/wiki/C_샤프).


**C\#**(, 원래는 **C♯**)는 [마이크로소프트](../Page/마이크로소프트.md "wikilink")에서 개발한 [객체 지향](../Page/객체_지향_프로그래밍.md "wikilink") [프로그래밍 언어로](../Page/프로그래밍_언어.md "wikilink"), [닷넷 프레임워크의](../Page/닷넷_프레임워크.md "wikilink") 한 부분으로 만들었으며 나중에 [ECMA](../Page/Ecma_인터내셔널.md "wikilink") (ECMA-334)와 [ISO](../Page/국제_표준화_기구.md "wikilink") (ISO/IEC/23270)의 표준으로 자리잡았다. [C++](https://ko.wikipedia.org/wiki/C++ "wikilink")와 [자바의](../Page/자바_\(프로그래밍_언어\).md "wikilink") 문법과 비슷한 문법을 가지고 있다.

## 예제

### [헬로 월드 프로그램](https://ko.wikipedia.org/wiki/헬로_월드_프로그램 "wikilink")(Hello, world\!)

``` CSharp
using System;

namespace HelloWorld
{
    class Program
    {
        private static void Main()
        {
            Console.WriteLine("Hello, World!");
        }
    }
}
```

출력 결과

`Hello, World!`

  - 마이크로소프트에서 필요 프로그램을 무료로 제공하고 있다.\[1\] 구체적인 프로그램 설치와 학습은 위키 하우(How to Create a Program in C Sharp)\[2\]에 기술되어 있다. 10분 가량 소요된다.
  - [C++](https://ko.wikipedia.org/wiki/C++ "wikilink")를 능숙하게 다루는 경우, C\#의 전반적인 사용방법을 학습하는데 이틀 가량 소요된다.
  - [Visual Basic.NET이나](../Page/비주얼_베이직_닷넷.md "wikilink") [Java를](../Page/자바_\(프로그래밍_언어\).md "wikilink") 능숙하게 다룰 수 있는 경우, C\#의 문법 및 키워드를 이해하는데 하루 가량 소요된다.

## 언어 특징

C\#은 닷넷 프로그램이 동작하는 닷넷 플랫폼을 가장 직접적으로 반영하고, 또한 닷넷 플랫폼에 강하게 의존하는 프로그래밍 언어이다. C\#은 그 문법적인 특성이 자바와 상당히 유사하며 C\#을 통하여 다룰 수 있는 닷넷 플랫폼의 기술들조차도 자바를 염두에 둔 것이 많아서 자바와 가장 많이 비교되고 있다. 하지만 C\#은 자바와 달리 불안전 코드(unsafe code)\[3\]와 같은 기술을 통하여 플랫폼 간 상호 운용성에 상당히 많은 노력을 기울이고 있다. C\#의 기본 [자료형](../Page/자료형.md "wikilink")은 닷넷의 객체 모델을 따르고 있고, 런타임 차원에서 [쓰레기 수집](../Page/쓰레기_수집_\(컴퓨터_과학\).md "wikilink")(garbage collection)이 되며 또한 클래스, 인터페이스, 위임, 예외와 같이 객체 지향 언어로서 가져야 할 모든 요소들이 포함되어 있다.

## 역사

닷넷 프레임워크를 개발하던 시절 [클래스 라이브러리는](../Page/기본_클래스_라이브러리.md "wikilink") SMC(Simple Managed C)라 불리는 관리 코드(managed code)를 사용했었다.\[4\] 1999년 1월, [아네르스 하일스베르가](../Page/아네르스_하일스베르.md "wikilink") 이끄는 팀이 새로운 언어인 Cool(C-like Object Oriented Language)을 개발했다. 마이크로소프트는 언어의 최종 이름을 Cool로 유지할지도 고려해봤지만 상표 문제로 인해 이뤄지지 않았다. 2000년 7월 PDC에서 닷넷 프로젝트가 발표될 때 즈음 Cool의 이름은 C\#으로 정해졌고 클래스 라이브러리와 [ASP.NET](../Page/ASP.NET.md "wikilink") 런타임은 C\#으로 옮겨갔다.

C\#은 ISO 소위원회 JTC 1/SC 22에 ISO/IEC 23270:2003으로 제출되었으나 철회 후 ISO/IEC 23270:2006으로 등록되었다.

### 이름

C\#이라는 이름은 음표를 연주할 때 반음 올리는 것을 표시하는 [올림표](https://ko.wikipedia.org/wiki/올림표 "wikilink")에서 따왔다. [C++](https://ko.wikipedia.org/wiki/C++ "wikilink")에서 "++"가 변수의 값을 1 증가시키는 것을 의미하는 것과 비슷하다. 마찬가지로 올림표는 네 개의 "+" 기호와 비슷하므로 C++를 한번 더 증가시켰다는 뜻도 지닌다.

기본 글꼴이나 브라우저의 기술적인 한계와 더불어 키보드에는 올림표 기호()가 포함되지 않기에 문서에서는 대체 기호로 [해시 기호](https://ko.wikipedia.org/wiki/해시_기호 "wikilink")()를 사용하며, ECMA-334 C\# 언어 사양\[5\] 에서도 확인할 수 있다. 그러나 광고나 패키지 포장 등 가능한 경우, 마이크로소프트에서는 의도한 대로 올림표를 사용한다.

### 버전

<table>
<thead>
<tr class="header">
<th><p>버전</p></th>
<th><p>언어 사양</p></th>
<th><p>날짜</p></th>
<th><p><a href="../Page/닷넷_프레임워크.md" title="wikilink">닷넷 프레임워크</a></p></th>
<th><p><a href="https://ko.wikipedia.org/wiki/비주얼_스튜디오" title="wikilink">비주얼 스튜디오</a></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="../Page/Ecma_인터내셔널.md" title="wikilink">ECMA</a></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/ISO/IEC" title="wikilink">ISO/IEC</a></p></td>
<td><p><a href="../Page/마이크로소프트.md" title="wikilink">마이크로소프트</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>C# 1.0</p></td>
<td><p><a href="http://www.ecma-international.org/publications/files/ECMA-ST-WITHDRAWN/ECMA-334,%202nd%20edition,%20December%202002.pdf">2002년 12월</a></p></td>
<td><p><a href="http://www.techstreet.com/cgi-bin/pdf/free/378672/ISO+IEC+23270-2003.pdf">2003년 4월</a></p></td>
<td><p><a href="http://download.microsoft.com/download/a/9/e/a9e229b9-fee5-4c3e-8476-917dee385062/CSharp%20Language%20Specification%20v1.0.doc">2002년 1월</a></p></td>
<td><p>2002년 1월</p></td>
</tr>
<tr class="odd">
<td><p>C# 1.2</p></td>
<td><p><a href="http://download.microsoft.com/download/5/e/5/5e58be0a-b02b-41ac-a4a3-7a22286214ff/csharp%20language%20specification%20v1.2.doc">2003년 10월</a></p></td>
<td><p>2003년 4월</p></td>
<td><p>.NET Framework 1.1</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/마이크로소프트_비주얼_스튜디오#비주얼_스튜디오_닷넷_2003" title="wikilink">비주얼 스튜디오 .NET 2002</a></p></td>
</tr>
<tr class="even">
<td><p>C# 2.0</p></td>
<td><p><a href="https://web.archive.org/web/20121202194727/http://www.ecma-international.org/publications/files/ECMA-ST/Ecma-334.pdf">2006년 6월</a></p></td>
<td><p><a href="http://standards.iso.org/ittf/PubliclyAvailableStandards/c042926_ISO_IEC_23270_2006(E).zip">2006년 9월</a></p></td>
<td><p><a href="http://download.microsoft.com/download/9/8/f/98fdf0c7-2bbd-40d3-9fd1-5a4159fa8044/csharp%202.0%20specification_sept_2005.doc">2005년 9월</a></p></td>
<td><p>2005년 11월</p></td>
</tr>
<tr class="odd">
<td><p>C# 3.0</p></td>
<td><p>colspan="2" rowspan="2" [6]</p></td>
<td><p><a href="http://download.microsoft.com/download/3/8/8/388e7205-bc10-4226-b2a8-75351c669b09/CSharp%20Language%20Specification.doc">2007년 8월</a></p></td>
<td><p>2007년 11월</p></td>
<td><p>.NET Framework 2.0 (LINQ/쿼리 확장 제외)[7]<br />
.NET Framework 3.0 (LINQ/쿼리 확장 제외)[8]<br />
.NET Framework 3.5</p></td>
</tr>
<tr class="even">
<td><p>C# 4.0</p></td>
<td><p>2010년 4월</p></td>
<td><p>2010년 4월</p></td>
<td><p>.NET Framework 4.0</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/마이크로소프트_비주얼_스튜디오#비주얼_스튜디오_2010" title="wikilink">비주얼 스튜디오 2010</a></p></td>
</tr>
<tr class="odd">
<td><p>C# 5.0</p></td>
<td><p><a href="https://www.ecma-international.org/publications/files/ECMA-ST/ECMA-334.pdf">2017년 12월</a></p></td>
<td><p><a href="https://standards.iso.org/ittf/PubliclyAvailableStandards/c075178_ISO_IEC_23270_2018.zip">2018년 12월</a></p></td>
<td><p><a href="https://www.microsoft.com/en-us/download/details.aspx?id=7029">2013년 6월</a></p></td>
<td><p>2012년 8월</p></td>
</tr>
<tr class="even">
<td><p>C# 6.0</p></td>
<td><p>colspan="2" rowspan="1" [9]</p></td>
<td></td>
<td><p>2015년 7월</p></td>
<td><p>.NET Framework 4.6</p></td>
</tr>
<tr class="odd">
<td><p>C# 7.0</p></td>
<td></td>
<td></td>
<td></td>
<td><p>2017년 5월</p></td>
</tr>
</tbody>
</table>

## 문법

C\#의 기본 문법은 C, C++, 자바 등 C 스타일 언어와 유사하다.

  - [세미콜론이](../Page/쌍반점.md "wikilink") 선언문의 끝을 나타낸다.
  - [중괄호로](https://ko.wikipedia.org/wiki/괄호#중괄호 "wikilink") 선언문을 묶는다. 보통 선언문은 메소드(함수)로, 메소드는 클래스로, 클래스는 [네임스페이스로](../Page/이름공간.md "wikilink") 묶인다.
  - 변수에 [등호](https://ko.wikipedia.org/wiki/등호 "wikilink")를 사용해서 값을 대입하고, 두 개의 등호("==")를 사용해 비교한다.
  - [대괄호는](https://ko.wikipedia.org/wiki/괄호#대괄호 "wikilink") [배열](../Page/배열.md "wikilink")의 선언 및 인덱스 접근 모두에 사용된다.

## 잘 알려진 C\# 컴파일러와 개발 도구들

  - [Microsoft Visual C\#](../Page/마이크로소프트_비주얼_C_샤프.md "wikilink"): Microsoft가 C\#에 대하여 내리는 모든 표준 정의를 가장 정확하고 안정적으로 반영하는 컴파일러이다. 최근에는 C\# 3.0에 포함될 LINQ 확장과 같은 부분에 대한 기술적인 레퍼런스를 미리 테스트해볼 수 있는 도구로도 자주 쓰인다.

<!-- end list -->

  - [Borland](../Page/볼랜드.md "wikilink")([CodeGear](../Page/코드기어.md "wikilink")) C\# Builder: [코드기어 RAD 스튜디오](https://ko.wikipedia.org/wiki/코드기어_RAD_스튜디오 "wikilink")(Codegear RAD Studio) 안에서 [Delphi.net](https://ko.wikipedia.org/wiki/Delphi.net "wikilink") 과 [C\#.net](https://ko.wikipedia.org/wiki/C_샤프_닷넷 "wikilink") 두 가지 언어로 .net 을 지원한다

<!-- end list -->

  - Microsoft Rotor 프로젝트: Microsoft .NET Framework가 발표된 후 수 개월 이후에 같이 발표되는 [오픈 소스](../Page/오픈_소스.md "wikilink") 프로젝트로 Microsoft 닷넷 플랫폼에 대한 대체 구현을 제공한다.

<!-- end list -->

  - [Mono](../Page/모노_\(소프트웨어\).md "wikilink"): 마이크로소프트 닷넷 플랫폼에 대한 구현이 시작될 무렵에 시작되었으며, 현재는 제3자 닷넷 플랫폼 중에서 가장 안정적이고 성숙되었다고 평가되는 프로젝트이다. 마이크로소프트 닷넷 플랫폼이 윈도우와 소수의 유닉스 플랫폼을 대상으로 하고 있는 것과는 달리 모노 플랫폼의 경우 윈도우보다는 리눅스, 유닉스, 맥 OS X, 솔라리스와 같이 윈도우 외의 운영 체제와 플랫폼을 대상으로 한다. 초기에는 [지미안](https://ko.wikipedia.org/wiki/지미안 "wikilink")이 호스팅했으나 현재는 [노벨에서](https://ko.wikipedia.org/wiki/노벨_\(기업\) "wikilink") 호스팅하고 있다. 모노 플랫폼을 기반으로 GTK\#, 모질라 임베딩, IKVM(Java 바이트 코드를 모노 플랫폼 위에서 에뮬레이션하여 실행하는 VM), COCOA\#, Nemerle 언어, MonoDevelop IDE 등의 기술을 지원한다. 또한 마이크로소프트 닷넷 플랫폼과 서로 호환이 가능하다. 현재는 리눅스 배포판들 사이에서 공식적으로 채택되고 있을 정도로 리눅스 환경에서는 대중적인 닷넷 플랫폼 구현이 되었다.

<!-- end list -->

  - DotGNU Project: 모노와 비슷한 시기에 개발을 시작하였지만 아직 안정적인 버전이 출시되지 못하였다. 특유의 Portable .NET 엔진을 사용하고 있다.

## C++과 C\#의 차이점

C++ 언어와 비교할 때 C\#은 다음과 같은 점에서 단순화되거나 확장되었다.

  - C\#에는 전역 변수 및 전역 함수가 존재하지 않으며, 클래스 안에 선언되어야 한다.
  - C\#의 `bool`은 오직 `true`와 `false`의 논리값만을 가질 수 있으며,상수 또는 정수형 변수에서 암시적으로 변환이 불가능하다. 직접 대입을 위해서는 변환 명령을 이용해야 한다. 반면 C++의 `bool`은 정수값을 대입할 수 있다. 또한 C\#에서는 `if`나 `while`문 등의 비교문에서 이용하는 값도 `bool` 형태로 제한되는 반면, C++에서는 상수 또는 변수를 이용하여 '0이 아닌 값' 또는 '0'의 여부로 비교할 수 있다.
  - C\#에서는 `static` 키워드를 오직 한 번만 초기화를 수행한다는 의미로 이용할 수 없다.
  - 기본적으로 C\#에서 포인터는 **unsafe 블록** 또는 **unsafe 형식**에서 사용하도록 정의되어 있으며, unsafe 키워드를 사용하려면 컴파일러에게 `/unsafe` 또는 `--unsafe` 스위치를 지정하도록 명시해야 한다. unsafe 블록의 사용 예는 다음과 같다.

>
>
> ``` csharp
> unsafe
> {
>     int *pA;
> }
> ```

  - 닷넷 플랫폼에서 포인터를 다루는 기본 단위는 `System.IntPtr`이다.

(`System.UIntPtr`은 특수한 목적으로 쓰이므로 설명에서 제외한다.)

  - C\#은 unsafe 블록 안에서 사용이 가능한 직접적인 포인터

(`IntPtr.ToPointer` 메서드로 `void*` 형식을 가져올 수 있음)도 지원한다.

  - 메모리 관리자에 의해 관리되는 데이터는 주소값이 자주 변경되므로, 잘못된 주소를 접근하는 등의 오류를 방지하기 위해 포인터는 [참조 형식의](https://ko.wikipedia.org/wiki/참조_형식 "wikilink") 인스턴스를 가리킬 수 없는 것이 기본 원칙이며, [참조 형식의](https://ko.wikipedia.org/wiki/참조_형식 "wikilink") 필드를 멤버로 가지고 있는 [구조체](https://ko.wikipedia.org/wiki/구조체 "wikilink") 역시 완전한 [값 형식으로](https://ko.wikipedia.org/wiki/값_형식 "wikilink") 판정하지 않고 [참조 형식으로](https://ko.wikipedia.org/wiki/참조_형식 "wikilink") 처리하기 때문에, 이 경우의 [구조체](https://ko.wikipedia.org/wiki/구조체 "wikilink")의 인스턴스에 대해서도 포인터로 그 주소를 가리킬 수 없다.
  - C\#의 포인터는 C++의 포인터와 비교하였을 때 문법적으로 다른 의미를 가진다.

C++에서 포인터는 특정한 형식의 인스턴스 또는 주소값을 가리키기 위한 목적으로 할당되는 주소값을 기억하기 위한 변수로 취급되지만 C\#의 포인터는 `System.IntPtr`이라는 하나의 완성된 형식에 대한 확장 사양일 뿐이다. 그래서 C++의 포인터와 같은 쓰임새를 C\#으로 이식할 수 없는 경우가 상당히 많다.

  - `void*` 포인터가 가리키는 값을 얻어낼 수 없고 `void*` 포인터에 대한 산술 연산도 수행할 수 없다.
  - 산술 연산은 컴파일러의 옵션 지정에 따라서 `/checked+` 로 지정된 경우

모든 코드 범위에서 엄격한 산술 연산 검사를 할 수 있으며 `/checked-` 로 지정된 경우 모든 코드 범위에서 산술 연산 검사를 하지 않도록 할 수 있다. 컴파일러 옵션과는 관계없이 **unchecked 블록** 안에서는 검사되지 않으며, 반대로 **checked 블록** 안에서는 검사가 이루어진다.

>
>
> ``` csharp
> int a = 0;
> unchecked
> {
>     a = int.MaxValue + 20;
> }
> checked
> {
>     a = int.MaxValue * 2;
> }
> ```

  - **fixed 블록**을 이용하여 [힙에](../Page/힙_\(자료_구조\).md "wikilink") 데이터를 고정할 수 있다.

>
>
> ``` csharp
> using System;
>
> namespace FooBar
> {
>     class Program
>     {
>         private int Test = 123;
>
>         static void Main(string[] args)
>         {
>             unsafe
>             {
>                 Program p = new Program();
>
>                 fixed (int* ptrX = &p.Test)
>                 {
>                     Console.Out.Write(Convert.ToString(*ptrX));
>                     *ptrX = 21;
>                     Console.Out.WriteLine(Convert.ToString(*ptrX));
>                 }
>             }
>         }
>     }
> }
> ```

  - C\#은 C++과는 달리 직접적인 메모리 해제 명령이 없으며, C++에서 포인터를 다룰 때 발생하기 쉬운 가비지나 매달린 포인터와 같은 복잡한 문제를 C\#에서는 가비지 컬렉터의 능력으로 자동으로 처리한다. 하지만 가비지 컬렉터가 수집을 하기 이전에 개별적으로 처리해야 할 필요가 있는 소거 작업의 구현을 위하여 `IDisposable` 인터페이스를 특정 클래스에서 구현하게 된다. `IDisposable` 인터페이스를 구현하는 클래스는 C\#의 using 구문을 이용하여 자동으로 `IDisposable.Dispose` 메서드를 호출할 수도 있다.
  - C\#은 C++과는 달리 부모 클래스를 하나만 사용할 수 있다. 즉 다중 상속은 불가능하며 구현해야 하는 인터페이스는 다수개를 지정할 수 있다. 이 점은 다중 부모 클래스로부터의 상속에서만 누릴 수 있는 이점을 잃게되는 단점을 가지지만 복잡성을 최소화하고 보다 명료한 상속 관계의 의미를 만들 수 있다는 점에서는 큰 도움이 된다.
  - C\#은 C++보다 [형 안전성에](https://ko.wikipedia.org/wiki/형_안전성 "wikilink") 대하여 더 관대하다. 이 말은 [형 안정성을](https://ko.wikipedia.org/wiki/형_안정성 "wikilink") 보장할 수 없다는 것도 동시에 뜻한다. `System.Object` 클래스가 모든 클래스의 선조 클래스이기 때문에 이러한 관대함이 가능하게 되었다. (단, unsafe 블록 내에서 사용되는 포인터 형식의 경우는 예외로 한다.)
  - [배열](../Page/배열.md "wikilink")과 [포인터를](../Page/포인터_\(프로그래밍\).md "wikilink") 정의하는 문법이 다르다. 배열 문법은 자바와 유사하다. 하지만 포인터의 경우 C\#은 `int*, void*, byte*`, ...와 같이 하나의 완성된 형식으로서 이해할 수 있지만 C++은 메모리 주소값을 저장하도록 되어있는 형태이다. 포인터를 사용하고자 하는 목적은 같지만 C++에서처럼 어떤 곳에서나 주소를 참조할 수 있는 것은 아니므로 정확한 이해가 필요하다. (다만, 특수한 `GCHandle` 형식을 활용하여 Pinned Object를 생성하는 경우에는 이러한 접근이 가능할 수 있으나 특성에 맞지도 않으며 심각한 성능 저하를 일으키므로 좋은 방법이라고 할 수 없을것이다.)

>
>
> ``` csharp
> // C#
> int[] a = new int[5];
> int* pA, pB;
> ```
>
> ``` cpp
> // C++
> int a[5];
> int *pA, *pB;
> ```

  - C\#의 [열거형](../Page/열거형.md "wikilink")은 그 자체가 하나의 형식이고 [열거형](../Page/열거형.md "wikilink") 아래에 정의된 상수들은 멤버 상수가 된다. 하지만 C++의 [열거형](../Page/열거형.md "wikilink")은 [열거형](../Page/열거형.md "wikilink") 형식 그 자체의 의미보다는 상수들이 전역적으로 쓰일 수 있다는 것에 더 초점을 둔다.
  - [형식 다형성에](https://ko.wikipedia.org/wiki/형식_다형성 "wikilink") 대한 제약을 극복하고 [형식 안정성을](https://ko.wikipedia.org/wiki/형식_안정성 "wikilink") 향상시키기 위한 목적으로 도입한 [제네릭 형식이란](https://ko.wikipedia.org/wiki/제네릭_형식 "wikilink") 것이 2.0 사양부터 존재한다. C++의 [템플릿과](../Page/템플릿_\(C++\).md "wikilink") 목표는 유사하지만 C++의 템플릿이 C++ 컴파일러보다 앞서서 처리되는 것에 비하여 C\#의 [제네릭 형식은](https://ko.wikipedia.org/wiki/제네릭_형식 "wikilink") IL [메타데이터](../Page/메타데이터.md "wikilink") 상에 실제로 정보가 남는다. 이러한 차이점으로 인하여 [마이크로소프트 비주얼 C++에는](https://ko.wikipedia.org/wiki/비주얼_C++ "wikilink") 특이한 충돌 현상이 발생하게 된다.\[10\]

<!-- end list -->

  - 데이터 멤버를 다루는 구문에 의해 메서드가 호출되는 속성 기능이 있다. 이것을 정확한 이름으로는 프로퍼티라고 하며 getter 메서드와 setter 메서드로 구분된다. C\#에서는 getter와 setter를 한꺼번에 사용할 수 있도록 아래와 같이 고정된 문법을 사용한다. [비주얼 베이직 닷넷의](../Page/비주얼_베이직_닷넷.md "wikilink") 경우에도 이와 비슷하나 프로퍼티에서도 다수의 매개 변수를 받는 것을 허용한다. 그리고 특별한 사항이 없는 대다수의 다른 언어들에서 프로퍼티는 `get_foo()` 메서드와 `set_foo()` 메서드로 구분되어 표현되곤 한다.

>
>
> ``` csharp
> public string Name
> {
>     get
>     {
>         return m_name;
>     }
>     set
>     {
>         m_name = "Name :: "+value;
>     }
> }
>
> public void MethodOne(string name)
> {
>     this.Name = "DotNet";
> }
> ```

  - C++에서 특정 컴파일러 제작사마다 조금씩 다른 방식으로 구현되었던 [런타임 형식 정보는](https://ko.wikipedia.org/wiki/런타임_형식_정보 "wikilink")

C\#에서 [리플렉션](https://ko.wikipedia.org/wiki/리플렉션 "wikilink")으로 확장하여 사용하는 것이 가능하다. [리플렉션](https://ko.wikipedia.org/wiki/리플렉션 "wikilink")은 [자바](../Page/자바_\(프로그래밍_언어\).md "wikilink") 언어의 [리플렉션](https://ko.wikipedia.org/wiki/리플렉션 "wikilink")과 같은 개념이다.

  - C\#은 C/C++과 달리 [전처리기](https://ko.wikipedia.org/wiki/전처리기 "wikilink")의 사용이 제한적이다.

즉, C/C++에서 사용되던 [\#include나](https://ko.wikipedia.org/wiki/include_가드 "wikilink") [\#pragma와](https://ko.wikipedia.org/wiki/전처리기_지시어#헤더_포함 "wikilink") 같은 지시자를 C\#에서는 사용할 수 없으며, C/C++에서 매크로 상수나 매크로 함수 등을 위해 사용되던 [\#define이](https://ko.wikipedia.org/wiki/전처리기_지시어#매크로_정의와_확장 "wikilink") C\#에서는 매우 제한적인 용도로 사용된다. 또한 C/C++에는 없던 [\#region](https://ko.wikipedia.org/wiki/#region "wikilink"), [\#endregion](https://ko.wikipedia.org/wiki/#endregion "wikilink") 지시자가 새로 추가되었다. 예를 들면 다음과 같다.

``` csharp
#define CsDebug
#region 아래는 FooClass 선언입니다.
public class FooClass
{
    private int integer;
    #if CsDebug
    private string debugmsg;
    #endif
    public string DebugMsg
    {
        get
        {
            #if CsDebug
            return this.debugmsg;
            #else
            return null;
            #endif
        }
        set
        {
            #if CsDebug
            this.debugmsg = value.Clone() as string;
            #endif
        }
    }
}
#endregion
```

  - C\#에서는 [인라인 함수가](https://ko.wikipedia.org/wiki/인라인_함수 "wikilink") 지원되지 않으며, [전역 함수나](https://ko.wikipedia.org/wiki/전역_함수 "wikilink") [전역 변수도](../Page/전역_변수.md "wikilink") 허용되지 않는다.

즉, 모든 [인스턴스](https://ko.wikipedia.org/wiki/인스턴스 "wikilink")나 [메서드](https://ko.wikipedia.org/wiki/메서드 "wikilink")는 반드시 특정 [클래스](https://ko.wikipedia.org/wiki/클래스 "wikilink")의 멤버로 소속되어야 한다.

  - C\#에서는 데이터 은닉과 보안성 향상을 위해 [프렌드 함수를](https://ko.wikipedia.org/wiki/프렌드_함수 "wikilink") 지원하지 않는다.

대신 C\# 3.0부터 이와 비슷한 [확장 메서드를](https://ko.wikipedia.org/wiki/확장_메서드 "wikilink") 지원하고 있다. [확장 메서드는](https://ko.wikipedia.org/wiki/확장_메서드 "wikilink") [정적 클래스의](https://ko.wikipedia.org/wiki/정적_클래스 "wikilink") 멤버로 있어야 하며 이 때에도 대상 클래스의 private 멤버에는 접근 할 수 없다.

``` csharp
public class Foo
{
    [MarshalAs(UnmanagedType.U4)]
    private uint dwValue;
    [MarshalAs(UnmanagedType.LPWstr)]
    private string lpcwValue;

    public uint DWValue
    {
        get { return this.dwValue; }
        set { this.dwValue = value; }
    }
    public string LPCWValue
    {
        get { return this.lpcwValue; }
        set { this.lpcwValue = value.Clone() as string; }
    }
}
public static class Bar
{
    public static string FooString(this Foo foo)
    {
        return string.Format("정수 값은 {0}, 문자열 값은 {1}입니다.", foo.DWValue, foo.LPCWValue);
    }
}
```

  - C\# 3.0부터는 임의의 자료형인 var타입을 지원한다. var의 실제 형식은 컴파일시 결정된다.

(이 부분은 [C++11](../Page/C++11.md "wikilink")에서 auto 키워드로 지원한다. )

  - C\# 3.0부터는 기존의 SQL구문을 활용한 LINQ 식을 지원한다.

아래 예제는 정수형으로 이루어진 배열에서 100을 초과하는 값만을 추출하는 코드이다.

``` csharp
public List<int> linqtest(List<int> list)
{
    var result = from k in list where k > 100 select k;
    return result;
}
```

  - C++에서는 [함수 포인터를](../Page/함수_포인터.md "wikilink") 이용하여 함수의 시작점을 전달 했지만, C\#에서는 보다 유연한 [델리게이트](https://ko.wikipedia.org/wiki/델리게이트 "wikilink")와 [무명 메서드를](https://ko.wikipedia.org/wiki/무명_메서드 "wikilink") 지원한다.

<!-- end list -->

``` csharp
public static void Print(int a, int b, Func<int> func)
{
    Console.WriteLine("{0} 더하기 {1}은 {2}입니다.", a, b, func(a, b));
}
public static void Main()
{
    Print(a, b, f => {Console.WriteLine("func가 호출되었습니다."); return a+b;});
}
```

## 같이 보기

  - [비주얼 C\#](../Page/마이크로소프트_비주얼_C_샤프.md "wikilink")
  - [비주얼 베이직 닷넷](../Page/비주얼_베이직_닷넷.md "wikilink")
  - [닷넷 프레임워크](../Page/닷넷_프레임워크.md "wikilink")
  - [C++/CLI](https://ko.wikipedia.org/wiki/C++/CLI "wikilink")
  - [자바](../Page/자바_\(프로그래밍_언어\).md "wikilink")
  - [델파이 프로그래밍 언어](https://ko.wikipedia.org/wiki/델파이_프로그래밍_언어 "wikilink")
  - [유니티 (게임 엔진)](../Page/유니티_\(게임_엔진\).md "wikilink")

## 각주

<references />

### 내용주

<references group="note" />

[C_샤프](https://ko.wikipedia.org/wiki/분류:C_샤프 "wikilink") [분류:ISO 표준](https://ko.wikipedia.org/wiki/분류:ISO_표준 "wikilink") [분류:닷넷 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:닷넷_프로그래밍_언어 "wikilink") [분류:2001년 개발된 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:2001년_개발된_프로그래밍_언어 "wikilink") [분류:함수형 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:함수형_프로그래밍_언어 "wikilink") [분류:IEC 표준](https://ko.wikipedia.org/wiki/분류:IEC_표준 "wikilink")

1.  <https://www.visualstudio.com/ko/vs/community/> 비주얼 스튜디오 커뮤니티 사이트
2.  <http://www.wikihow.com/Create-a-Program-in-C-Sharp>
3.
4.
5.
6.  C\# 3.0, 4.0은 ECMA나 ISO/IEC 사양이 존재하지 않는다.
7.
8.
9.
10. [MSDN Magazine](http://www.microsoft.com/korea/msdn/msdnmag/issues/06/04/PureC/default.aspx)