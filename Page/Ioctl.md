> This article is converted from Wikipedia: [Ioctl](https://ko.wikipedia.org/wiki/Ioctl).


컴퓨터에서 **ioctl**은 기본 운영 체제의 [컴퓨터 사용자와](https://ko.wikipedia.org/wiki/컴퓨터_사용자 "wikilink") [커널을](https://ko.wikipedia.org/wiki/커널_\(컴퓨팅\) "wikilink") 잇는 인터페이스의 일부이다. "[입출력](../Page/입출력.md "wikilink") 제어"(I/O control)의 준말인 ioctl은 보통 사용자 공간의 코드가 하드웨어 장치, 커널 구성 요소와 통신할 수 있게 도와 주는 역할을 한다. '아이억털'(/aɪˈɒktəl/), '아이오씨티엘', '인풋/아웃풋 컨트롤'로 발음한다.

## 배경

기본 운영 체제는 두 개의 계층, [사용자 공간](https://ko.wikipedia.org/wiki/사용자_공간 "wikilink"), [커널로](https://ko.wikipedia.org/wiki/커널_\(컴퓨팅\) "wikilink") 나뉜다. [문서 편집기와](https://ko.wikipedia.org/wiki/문서_편집기 "wikilink") 같은 응용 프로그램 코드는 사용자 공간에 상주하는 반면, [네트워크 스택과](https://ko.wikipedia.org/wiki/프로토콜_스택 "wikilink") 같은 운영 체제의 기반이 되는 코드는 커널에 상주한다. 커널 코드는 민감한 리소스를 관리하며 응용 프로그램 사이의 보안과 신뢰 장벽을 제공한다. 이러한 까닭에 사용자 모드 응용 프로그램은 CPU에 의해 커널 리소스를 직접 접근하는 것을 막는다.

[사용자 공간](https://ko.wikipedia.org/wiki/사용자_공간 "wikilink") 응용 프로그램은 사용자 모드에서 커널 모드로 이동하는 특별한 서브루틴 콜인 [시스템 콜의](https://ko.wikipedia.org/wiki/시스템_콜 "wikilink") 수단으로 기본 커널의 대부분의 요청을 취한다. 보통 시스템 콜 벡터와 함께 추가되며 여기서 요청자는 원하는 시스템 콜을 색인 숫자로 기록한다. 이를테면, "exit"은 시스템 콜 1이 될 수 있고, "write"는 시스템 콜 4가 될 수 있다. 시스템 콜 벡터와 색인은 요청을 관리하기 위해 커널 기능을 살피는 데 쓰인다. 이런 식으로 기본 운영 체제는 보통 수백 개의 시스템 콜을 제공하게 된다.

시스템 콜의 편리한 설계에도 불구하고 이는 드라이버 장치를 막아 버린다. 대부분의 하드웨어 주변 기기는 반드시 커널 안에서만 직접 접근하여야 한다. 그러나 사용자 코드는 장치와 통신해야 할 수도 있다. 이를테면, 관리자는 [이더넷](https://ko.wikipedia.org/wiki/이더넷 "wikilink") 인터페이스의 미디어 종류를 구성해야 할 수 있다. 현대의 운영 체제는 다양한 장치를 지원하며, 그 가운데 많은 수가 사용자에게 보이는 세세한 인터페이스를 제공하지만 모든 장치가 운영 체제 제공 업체에 알려져 있는 것은 아니다. 그러므로 어렵게 코드된 시스템 콜 숫자가 포함한 장치 [API](../Page/API.md "wikilink")를 제공하기가 어려워지게 된다.

**Ioctl** 인터페이스는 모든 장치 드라이버가 공유하는 하나의 시스템 콜을 할당함으로써 이 문제를 피할 수 있게 도와 준다. 이러한 시스템 콜을 통해 다양한 장치의 특정한 요청의 방향을 바꿀 수 있다. 그러므로 커널은 관리가 불가능한 시스템 콜 테이블을 만들지 않고도 유동적으로 장치에 대한 콜을 처리할 수 있다.

## 기능

### 유닉스

유닉스의 ioctl 콜은 다음과 같은 [매개 변수를](https://ko.wikipedia.org/wiki/매개_변수 "wikilink") 취한다.

1.  열려 있는 [파일 서술자](https://ko.wikipedia.org/wiki/파일_서술자 "wikilink")
2.  요청 코드 번호
3.  드라이버 서명이 되지 않은 정수값, 또는 [포인터](https://ko.wikipedia.org/wiki/포인터_\(프로그래밍\) "wikilink")

### Win32

Win32 *DeviceIoControl*은 다음과 같은 매개 변수를 취한다.

1.  열려 있는 객체 관리 (파일 서술자와 동등)
2.  요청 코드 번호 (제어 코드)
3.  입력 매개 변수를 위한 버퍼
4.  출력 결과를 위한 버퍼
5.  OVERLAPPED 구조 ([오버랩 입출력이](https://ko.wikipedia.org/wiki/오버랩_입출력 "wikilink") 쓰이는 경우)

Win32 장치 제어 코드는 기능의 수행 여부를 결정한다.\[1\]

1.  METHOD_IN_DIRECT - 버퍼 주소는 사용자 모드 호출자가 있을 수 있게 한다.
2.  METHOD_OUT_DIRECT - 버퍼 주소는 사용자 모드 호출자가 쓸 수 있게 한다.
3.  METHOD_NEITHER - 사용자 모드 가상 주소는 매핑이나 확인 과정 없이 드라이버로 통과된다.
4.  METHOD_BUFFERED - 공유 버퍼로 제어되는 입출력 관리자는 데이터를 사용자 모드에 입력하거나 가져온다.

## 같이 보기

  - [입출력](../Page/입출력.md "wikilink")

## 참조

<references />

[분류:유닉스](https://ko.wikipedia.org/wiki/분류:유닉스 "wikilink")

1.  [DeviceIoControl Function (Windows)](http://msdn2.microsoft.com/en-us/library/aa363216.aspx)