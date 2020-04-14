> This article is converted from Wikipedia: [JMP \(x86 명령어\)](https://ko.wikipedia.org/wiki/JMP_\(x86_명령어\)).


x86 [어셈블리어](../Page/어셈블리어.md "wikilink")에서, **`JMP`** [명령어는](../Page/명령어_집합.md "wikilink") 무조건 점프를 수행한다. 예를 들면 [프로그램 카운터의](../Page/프로그램_카운터.md "wikilink") 변경을 통해 실행 흐름을 이동할 수 있다. 점프를 수행하는 여러 종류의 [명령 코드가](../Page/명령_코드.md "wikilink") 있는데, 중앙 처리 장치가 [리얼 모드인지](../Page/리얼_모드.md "wikilink") 또는 [보호 모드인지에](../Page/보호_모드.md "wikilink") 의존한다. 명령어들은 [16비트](../Page/16비트.md "wikilink"), [32비트](../Page/32비트.md "wikilink") 또는 세그먼트:오프셋 [포인터를](../Page/포인터_\(프로그래밍\).md "wikilink") 가진다.\[1\]

여러 종류의 점프 형식이 있다. 상대, 조건부, 절대 그리고 간접 레지스터 점프가 그것이다.

아래의 예제들은 다음을 의미한다.

1.  16비트 포인터를 통한 상대 점프
2.  long 점프 (세그먼트 내의), 32비트 포인터를 통한 상대 점프
3.  그리고 EAX 레지스터를 이용한 간접 레지스터 절대 점프

(비록 처음과 두번째 점프가 상대적이지만, 보통 [옵코드에](../Page/명령_코드.md "wikilink") 부호화된 상대적인 오프셋 대신에, 목적지 주소가 보인다.)

예시 1: 새 값인 `0x89AB`를 IP로 로드한 다음, [CS 레지스터에는](https://ko.wikipedia.org/wiki/CS_레지스터 "wikilink") `0xACDC` 를, 그리고 IP에는 `0x5578`를 로드한다.

``` asm
JMP 0x89AB
JMP 0xACDC:0x5578
```

예시 2: `0x56789AB1`값을 IP를 로드한다. 오직 보호 모드나 [언리얼 모드에서만](https://ko.wikipedia.org/wiki/언리얼_모드 "wikilink") 가능하다.

``` asm
JMP 0x56789AB1
```

예시 3: EAX 레지스터에 저장되어 있는 값으로 점프. 오직 보호 모드에서만 가능하다.

``` asm
JMP EAX
```

## 각주

[분류:X86 명령어](https://ko.wikipedia.org/wiki/분류:X86_명령어 "wikilink")

1.