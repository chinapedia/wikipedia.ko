> This article is converted from Wikipedia: [MVS](https://ko.wikipedia.org/wiki/MVS).


**MVS**(, 멀티플 버추얼 스토리지)는 과거 [시스템/370](https://ko.wikipedia.org/wiki/시스템/370 "wikilink"), [시스템/390](https://ko.wikipedia.org/wiki/시스템/390 "wikilink") [IBM 메인프레임](../Page/IBM_메인프레임.md "wikilink") 컴퓨터에서 가장 흔히 쓰였던 [운영 체제이다](../Page/운영_체제.md "wikilink"). [IBM](../Page/IBM.md "wikilink")이 개발하였으나, [VSE](../Page/VSE_\(운영_체제\).md "wikilink"), [VM](https://ko.wikipedia.org/wiki/VM_\(운영_체제\) "wikilink"), [TPF](https://ko.wikipedia.org/wiki/TPF "wikilink")와 같은 IBM의 기타 메인프레임 운영 체제와는 관련이 없다.

1974년에 처음 출시된 MVS는 수차례 새로운 이름으로 프로그램 제품으로까지 확장되었으며, 처음에는 MVS/SE (MVS/System Extension), 다음에는 MVS/SP(MVS/System Product) 버전 1, 다음에는 [MVS/XA](https://ko.wikipedia.org/wiki/MVS/XA "wikilink") (MVS/eXtended Architecture), 다음에는 [MVS/ESA](https://ko.wikipedia.org/wiki/MVS/ESA "wikilink") (MVS/Enterprise Systems Architecture), 다음에는 [OS/390](https://ko.wikipedia.org/wiki/OS/390 "wikilink"), 끝으로 [z/OS](https://ko.wikipedia.org/wiki/z/OS "wikilink") ([64비트](../Page/64비트.md "wikilink") 지원이 [z시리즈](https://ko.wikipedia.org/wiki/IBM_시스템_Z "wikilink") 모델에 추가됨)로 이어졌다. IBM은 MVS/SP V4.3에 유닉스 지원(원래 [오픈에디션 MVS로](https://ko.wikipedia.org/wiki/유닉스_시스템_서비스 "wikilink") 부름)을 추가하였으며, [IEEE](https://ko.wikipedia.org/wiki/IEEE_컴퓨터_학회 "wikilink"), [X/Open](https://ko.wikipedia.org/wiki/X/Open "wikilink"), [오픈 그룹](../Page/오픈_그룹.md "wikilink") 등 여러 수준에서 [POSIX](../Page/POSIX.md "wikilink")와 [유닉스](../Page/유닉스.md "wikilink") 인증을 취득하였다. MVS의 핵심 부분은 근본적으로 동일한 운영 체제로 남아있다. 설계 상, MVS용으로 작성된 프로그램들은 수정 없이 z/OS에서 실행된다.

처음에는 IBM이 MVS를 [OS/VS2](https://ko.wikipedia.org/wiki/OS/VS2 "wikilink")의 새로운 판으로 기술하였으나, 사실은 완전히 다시 작성된 운영 체제이다. OS/VS2 릴리스 1은 오리지널 코드의 대부분을 보유한 [OS/360 MVT의](https://ko.wikipedia.org/wiki/OS/360 "wikilink") 업그레이드판으로, MVT처럼 주로 [어셈블리어](../Page/어셈블리어.md "wikilink")로 작성되었다. MVS 코어는 [어셈블러 XF로](https://ko.wikipedia.org/wiki/IBM_베이직_어셈블리어 "wikilink") 대부분 작성된 반면, 일부 모듈들은 [PL/S로](https://ko.wikipedia.org/wiki/IBM_PL/S "wikilink") 작성되었지만 성능에(특히 [입출력 수퍼바이저](https://ko.wikipedia.org/wiki/입출력_수퍼바이저 "wikilink"), 즉 IOS에서) 민감한 부분은 아니다. IBM의 "OS/VS2" 사용은 상위 호환성을 강조하였다. 즉, MVT 하에서 실행된 응용 프로그램들은 MVS에서의 구동을 위해 재컴파일을 할 필요가 없었다. 동일한 [JCL](../Page/작업_제어_언어.md "wikilink") 파일들은 변경하지 않은 채로 사용이 가능했다. 즉, [TSO와](https://ko.wikipedia.org/wiki/시분할_옵션 "wikilink") 같은 유틸리티와 기타 비코어 기능들을 변경 없이 실행할 수 있었다. IBM 및 사용자들은 만장일치로 처음부터 새로운 시스템을 MVS로 불렀으며, IBM은 MVS/XA와 같은 차기 주요 버전의 이름에서 "MVS"라는 용어의 사용을 계속하였다.

## 역사

MVS는 현재 z/OS의 일부이다. 최신판은 1981년에 공개된 24비트 버전의 3.8j이며, 무료로 사용이 가능하고 현재 MVS 3.8j는 메인프레임 에뮬레이터에서 무료로 구동 가능하다.

## 종류

1974년 처음 공개된 MVS는 여러 새로운 이름의 프로그램 제품으로 확장되었는데 처음에는 MVS/SE (System Extension), 그 다음은 MVS/SP (System Product) 버전 1이었으며 그 뒤 MVS/XA, MVS/ESA, OS/390, 마지막으로 z/OS(64비트 지원이 z시리즈 모델에 추가된 당시)로 이어진다.

  - MVS/370
  - MVS/XA (Multiple Virtual Storage/Extended Architecture)
  - MVS/ESA (MVS Enterprise System Architecture)

## 참고문헌

  - Bob DuCharme: "The Operating Systems Handbook, Part 06: MVS" ([여기](http://www.snee.com/bob/opsys.html)서 온라인으로 참조 가능)

  -
## 외부 링크

  - [IBM: z/OS V1R11.0 MVS Manuals](http://www-03.ibm.com/systems/z/os/zos/bkserv/r11pdf/#mvs)

  - [IBM: z/OS V1R8.0 MVS manuals](http://www-03.ibm.com/servers/eserver/zseries/zos/bkserv/r8pdf/mvs.html)

  - [MVS: the operating system that keeps the world going](https://archive.is/20010630051655/http://www.os390-mvs.freesurf.fr/mvs.htm)

  - [MVS... a long history](https://archive.is/20010716160937/http://www.os390-mvs.freesurf.fr/mvshist.htm)

  - [Functional structure of IBM virtual storage operating systems Part II: OS/VS2-2 concepts and philosophies by A. L. Scherr](http://www.research.ibm.com/journal/sj/124/ibmsj1204E.pdf)

[분류:IBM 메인프레임 운영 체제](https://ko.wikipedia.org/wiki/분류:IBM_메인프레임_운영_체제 "wikilink")