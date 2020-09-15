> This article is converted from Wikipedia: [어셈블리 \(CLI\)](https://ko.wikipedia.org/wiki/어셈블리_\(CLI\)).


최근 버전의 [윈도우에서](../Page/마이크로소프트_윈도우.md "wikilink") [마이크로소프트](../Page/마이크로소프트.md "wikilink")가 [공통 언어 기반](../Page/공통_언어_기반.md "wikilink")(CLI)에 정의한 **어셈블리**(assembly)는 디플로이, 버전 지정, 보안을 위해 사용되는 [컴파일](https://ko.wikipedia.org/wiki/컴파일 "wikilink")된 코드 라이브러리이다. 두 종류가 있다: 프로세스 어셈블리([EXE](../Page/EXE.md "wikilink")), 라이브러리 어셈블리([DLL](../Page/동적_링크_라이브러리.md "wikilink")). 프로세스 어셈블리는 라이브러리 어셈블리에 정의되는 클래스를 사용하는 프로세스를 대표한다. CLI 어셈블리는 [CIL에](../Page/공통_중간_언어.md "wikilink") 코드를 포함하고 있으며 보통은 [CLI 언어로부터](https://ko.wikipedia.org/wiki/CLI_언어_목록 "wikilink") 생성된 뒤 [JIT 컴파일러에](https://ko.wikipedia.org/wiki/JIT_컴파일러 "wikilink") 의해 [런타임](../Page/런타임.md "wikilink") 중 [기계어](../Page/기계어.md "wikilink")로 컴파일된다. [닷넷 프레임워크](../Page/닷넷_프레임워크.md "wikilink") 구현체에서 이 컴파일러는 [공통 언어 런타임](../Page/공통_언어_런타임.md "wikilink")(CLR)의 일부이다.

어셈블리는 하나 이상의 파일로 구성될 수 있다. 코드 파일은 모듈(module)이라고 부른다. 어셈블리는 하나 이상의 코드 모듈을 포함할 수 있다. 코드 모듈을 생성하기 위해 각기 다른 [언어를](../Page/컴퓨터_언어.md "wikilink") 사용할 수 있으므로 기술적으로 각기 다른 언어들을 사용하여 어셈블리를 만들 수 있다. 그러나 [비주얼 스튜디오는](https://ko.wikipedia.org/wiki/비주얼_스튜디오 "wikilink") 한 어셈블리에 각기 다른 언어를 사용하는 것을 지원하지 않는다.

## 어셈블리 버전

CLI 어셈블리는 버전 정보를 포함할 수 있으므로 공유 어셈블리들에 의해 발생되는 응용 프로그램 간 대부분의 충돌을 제거할 수 있다.\[1\] 그러나 어셈블리 간 잠재적인 모든 버전 충돌을 제거하지는 못한다.\[2\]

## 어셈블리의 언어

어셈블리는 중간 언어인 CIL 코드로 빌드된다. 프레임워크는 내부적으로 CIL \[bytecode\]를 네이티브 [어셈블리 코드로](https://ko.wikipedia.org/wiki/어셈블리_코드 "wikilink") 변환한다. "Hello World"를 출력하는 프로그램이 있다면 그에 상응하는 CIL 코드는 다음과 같다:

``` csharp
 .method private hidebysig static void  Main(string[] args) cil managed {
  .entrypoint
  .custom instance void [mscorlib]System.STAThreadAttribute::.ctor() = ( 01 00 00 00 )
  // Code size       11 (0xb)
  .maxstack  1
  IL_0000:  ldstr      "Hello World"
  IL_0005:  call       void [mscorlib]System.Console::WriteLine(string)
  IL_000a:  ret } // end of method Class1::Main
```

CIL 코드는 String을 스택으로 적재한 뒤 WriteLine 함수를 호출하고 반환한다.

## 각주

[분류:공통 언어 기반](https://ko.wikipedia.org/wiki/분류:공통_언어_기반 "wikilink")

1.
2.