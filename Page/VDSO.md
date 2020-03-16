> This article is converted from Wikipedia: [VDSO](https://ko.wikipedia.org/wiki/VDSO).


**vDSO** (**virtual dynamically linked shared object**)는 신중하게 선택된 커널 영역 루틴들의 집합을 사용자 영역 애플리케이션으로 내보내는 리눅스 커널 메커니즘이다. 이를 통해 애플리케이션은 [시스템 호출](../Page/시스템_호출.md "wikilink") 인터페이스로 커널 영역 루틴들을 호출할 때 생기는 [문맥 교환의](https://ko.wikipedia.org/wiki/문맥_교환 "wikilink") 패널티 없이, 프로세스 내에서 이러한 커널 영역 루틴들을 호출할 수 있게 된다.\[1\]

**vDSO**는 **vsyscall**의 기능들을 제공함과 동시에 한계들을 극복하기 위해 개발되었다 : 오직 4개의 시스템 호출만을 허용하는 작은 양의 할당된 메모리 그리고 각 프로세스에서 같은 주소를 갖음으로 인한 보안의 위협이 그것이다.

**vDSO**는 [링킹과](../Page/링커_\(컴퓨팅\).md "wikilink") [로딩](https://ko.wikipedia.org/wiki/로더_\(컴퓨팅\) "wikilink")(표준 [ELF 파일 형식](https://ko.wikipedia.org/wiki/ELF_파일_형식 "wikilink"))을 위한 표준 메커니즘을 사용한다.\[2\]\[3\]

**vDSO**는 몇몇 커널 기능들을 드러내는 사용자 공간에 할당된 메모리 공간이다. **vDSO**는 더 안전한 메모리 공간 랜덤화와 4개 이상의 시스템 호출들을 제공하며 동적으로 할당된다(vsyscall은 정적으로 할당된다). **vDSO** 링크들은 [glibc](../Page/GNU_C_라이브러리.md "wikilink") 라이브러리를 통해 제공된다. 만약 리눅스 커널이 **vDSO** 지원을 제공하지 않는다면 전통적인 [syscall이](../Page/시스템_호출.md "wikilink") 만들어 진다.\[4\]

이것은 간단한 커널 루틴들의 호출에 의한 오버헤드를 감소시키며 또한 몇몇 아키텍처에서는 최선의 시스템 호출 방식을 고르는 방법으로 사용될 수 있다.

다른 방식보다 장점으로는 이러한 내보내진 루틴들이 적절한 [DWARF](../Page/DWARF.md "wikilink") (Debug With Attributed Record Format) 디버깅 정보를 제공할 수 있다는 점이다.

## 같이 보기

  - [응용 프로그램 이진 인터페이스](../Page/응용_프로그램_이진_인터페이스.md "wikilink")

## 각주

[분류:API](https://ko.wikipedia.org/wiki/분류:API "wikilink") [분류:운영 체제 기술](https://ko.wikipedia.org/wiki/분류:운영_체제_기술 "wikilink")

1.
2.
3.
4.