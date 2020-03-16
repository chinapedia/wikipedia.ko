> This article is converted from Wikipedia: [ADSO](https://ko.wikipedia.org/wiki/ADSO).


**ADSO**(Application Development System Online)는 [IDMS](../Page/IDMS.md "wikilink") [데이터베이스](../Page/데이터베이스.md "wikilink")를 사용하여 [모듈식 애플리케이션들의](https://ko.wikipedia.org/wiki/모듈성_\(프로그래밍\) "wikilink") 작성 및 테스트를 더 신속히 처리할 수 있도록 도와주는 도구이다. 전통적인 상세한 코드 대신 일련의 화면을 이용함으로써 제어 흐름 처리, [데이터 스토리지](https://ko.wikipedia.org/wiki/데이터_스토리지 "wikilink") 정의, 데이터 확인, 편집, [오류 처리](../Page/예외_처리.md "wikilink"), [터미널](https://ko.wikipedia.org/wiki/컴퓨터_터미널 "wikilink") 입출력, 메뉴 작성, 메뉴 표시와 같은 활동들을 규정할 수 있다.

ADSO, ADS/O, 또는 간단히 ADS는 본래 컬리넷(Cullinet)의 제품이지만 나중에 이 회사는 [CA에](../Page/CA_테크놀로지스.md "wikilink") 인수되었다.

## 구성 요소

ADS/O는 3개의 구성 요소가 있다: ADSG, ADSA, ADSR.

  - ADSA (ADS Application): 프로세스/응용 프로그램들을 개발하고 컴파일하는데 사용한다.
  - ADSG (ADS Map generator): 온라인 응용 프로그램을 위한 화면/맵을 만들고 맵을 컴파일하는데 사용한다.
  - ADSR (ADS Run time): ADSR 환경에서 adsa와 adsg가 만든 맵과 응용 프로그램을 실행하는데 사용한다.

## 도구

ADS/O와 함께 사용되는 다른 도구들은 다음과 같다:

  - DME (Dictionary Module Editor) - 응용 프로그램들을 작성하기 위해 사용하는 편집기이다. IDD를 통해 만든 프로그램들은 IDD에 저장된다.
  - MAPC (Create Maps) - 화면과 같은 사용자 인터페이스를 설계하기 위한 유틸리티이다.
  - IDDM (Integrated Data Dictionary) - 통합 데이터 사전(IDD)에서 오브젝트의 추가, 수정, 조회를 용이하게 하는 메뉴 구동 유틸리티이다.

ADSO를 사용하여 온라인, 배치 응용 프로그램들을 개발할 수 있다.

## 장점

  - 많은 코드를 작성하지 않고도 [프로토타입](../Page/프로토타입.md "wikilink")을 한다.
  - 프로세스 로직을 코딩하기 전에 표시되는 화면을 검토한다.
  - 입력 레코드들은 편집 및 오류 처리 기능을 사용하여 자동으로 편집, 검증할 수 있다.
  - 내장 [디버깅](https://ko.wikipedia.org/wiki/디버깅 "wikilink") 프로세스가 있다.
  - 런타임 성능과 자원 사용률을 감시한다.
  - 언제든지 프로세스 로직을 추가할 수 있다.
  - 필요하면 데이터를 열람하고 변경하는 기능을 테스트할 수 있다.
  - 응용 프로그램을 통해 순차적인 추적을 허용한다.

## 참고문헌

  - Martin and Leben. Fourth-Generation Languages. Prentice Hall. 1986.  Volume 2 (Representative 4GLs). Pages 42, 44, 45 and passim. [Google Books](https://books.google.com/books?id=RJ7gAAAAMAAJ).
  - Fabbri and Schwab. Practical Database Management. Pws-Kent Publishing Company. Boston. 1992. . Pages 146, 182 and 420 to 422. [Google Books](https://books.google.com/books?id=cpokAQAAIAAJ).

[분류:데이터베이스 관리 도구](https://ko.wikipedia.org/wiki/분류:데이터베이스_관리_도구 "wikilink")