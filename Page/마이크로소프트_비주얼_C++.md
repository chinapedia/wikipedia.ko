> This article is converted from Wikipedia: [  C++](https://ko.wikipedia.org/wiki/__C++).


**마이크로소프트 비주얼 C++**(Microsoft Visual C++, 줄여서 MSVC)은 [마이크로소프트](https://ko.wikipedia.org/wiki/마이크로소프트 "wikilink")사가 [C](https://ko.wikipedia.org/wiki/C_\(프로그래밍_언어\) "wikilink"), [C++](https://ko.wikipedia.org/wiki/C++ "wikilink"), [C++/CLI](https://ko.wikipedia.org/wiki/C++/CLI "wikilink") [프로그래밍 언어](https://ko.wikipedia.org/wiki/프로그래밍_언어 "wikilink") 도구로 계획한 [통합 개발 환경](https://ko.wikipedia.org/wiki/통합_개발_환경 "wikilink") (IDE) 제품이다. [개발](https://ko.wikipedia.org/wiki/소프트웨어_개발_프로세스 "wikilink") 및 C++ (특히 [마이크로소프트 윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") [API](../Page/API.md "wikilink"), [다이렉트X](https://ko.wikipedia.org/wiki/다이렉트X "wikilink") API, [닷넷 프레임워크로](../Page/닷넷_프레임워크.md "wikilink") 작성된 코드)의 [디버깅을](https://ko.wikipedia.org/wiki/디버그 "wikilink") 위한 도구를 가지고 있다.

## 현재의 제품

현재 사용할 수 있는 비주얼 C++ 제품은 다음과 같다:

  - 마이크로소프트 비주얼 C++ 2017 익스프레스 에디션
  - 마이크로소프트 비주얼 스튜디오 2017 엔터프라이즈
  - 마이크로소프트 비주얼 스튜디오 2017 프로페셔널
  - 마이크로소프트 비주얼 스튜디오 2017 커뮤니티

비주얼 C++은 [비주얼 스튜디오](https://ko.wikipedia.org/wiki/마이크로소프트_비주얼_스튜디오 "wikilink") 안에 포함되어 있다.

기본적으로 비주얼 스튜디오 패키지로 구매하거나 [MSDN](../Page/마이크로소프트_개발자_네트워크.md "wikilink") 제품 구독으로 사용권을 얻을 수 있는 상용 프로그램이다. 반면 익스프레스 에디션과 커뮤니티 에디션은 [MSDN](../Page/마이크로소프트_개발자_네트워크.md "wikilink") 또는 공식 사이트에서 누구나 무료로 내려 받아 설치하고 사용할 수 있다.

## 버전

패키지 이름은 출시 당시 또는 현재 판매하고 있는 상품명으로 정하고 있으며, 버전 6.0까지는 내부 갱신 번호와 같지만 2002 버전 이후에는 출시 예정 또는 출시 연도를 이름에 붙이고 있다. 컴파일러 버전은 패키지 이름 또는 내부 갱신 번호와는 다르며 비주얼 C++ 내부에 포함된 컴파일러인 "MS C/C++"의 순수 버전이다. 명령행 컴파일러 "CL.EXE"로 확인할 수 있다. _MSC_VER는 전처리를 할 때 컴파일러 버전을 알 수 있는 유일한 매크로 상수이다.

| 패키지 이름                  | 컴파일러 버전         | 출시                                                      | _MSC_VER | [MFC](../Page/마이크로소프트_파운데이션_클래스_라이브러리.md "wikilink") | [닷넷](../Page/닷넷_프레임워크.md "wikilink") | 지원 아키텍처                |
| ----------------------- | --------------- | ------------------------------------------------------- | ---------- | ---------------------------------------------------- | ------------------------------------ | ---------------------- |
| 마이크로소프트 C 5.0 / 퀵-C 1.0 | 5.0             | [1987년](https://ko.wikipedia.org/wiki/1987년 "wikilink") | 500        | \-                                                   | \-                                   | DOS                    |
| 마이크로소프트 C 5.1 / 퀵-C 2.0 | 5.1             | [1989년](https://ko.wikipedia.org/wiki/1989년 "wikilink") | 500        | \-                                                   | \-                                   | WIN16                  |
| 마이크로소프트 C 6.0           | 6.0             | [1989년](https://ko.wikipedia.org/wiki/1989년 "wikilink") | 600        | \-                                                   | \-                                   | WIN16                  |
| 마이크로소프트 C/C++ 7.0       | 7.0             | [1992년](https://ko.wikipedia.org/wiki/1992년 "wikilink") | 700        | 1.0                                                  | \-                                   | WIN16                  |
| 비주얼 C++ 1.0 / 퀵-C 2.5   | 8.0             | [1993년](https://ko.wikipedia.org/wiki/1993년 "wikilink") | 800        | 2.0                                                  | \-                                   | WIN16                  |
| 비주얼 C++ 1.5             | 8.0             | [1993년](https://ko.wikipedia.org/wiki/1993년 "wikilink") | 800        | 2.5                                                  | \-                                   | WIN16                  |
| 비주얼 C++ 1.52c           | 8.0             | [1994년](https://ko.wikipedia.org/wiki/1994년 "wikilink") | 800        | 2.5                                                  | \-                                   | WIN16                  |
| 비주얼 C++ 2.0             | 9.0             | [1995년](https://ko.wikipedia.org/wiki/1995년 "wikilink") | 900        | 3.0                                                  | \-                                   | WIN16, X86             |
| 비주얼 C++ 2.1             | 9.1             | [1995년](https://ko.wikipedia.org/wiki/1995년 "wikilink") | 900        | 3.1                                                  | \-                                   | WIN16, X86             |
| 비주얼 C++ 2.2             | 9.2             | [1995년](https://ko.wikipedia.org/wiki/1995년 "wikilink") | 900        | 3.2                                                  | \-                                   | WIN16, X86             |
| 비주얼 C++ 4.0             | 10.0            | [1996년](https://ko.wikipedia.org/wiki/1996년 "wikilink") | 1000       | 4.0                                                  | \-                                   | X86                    |
| 비주얼 C++ 4.1             | 10.1            | [1996년](https://ko.wikipedia.org/wiki/1996년 "wikilink") | 1010       | 4.1                                                  | \-                                   | X86                    |
| 비주얼 C++ 4.2             | 10.2            | [1996년](https://ko.wikipedia.org/wiki/1996년 "wikilink") | 1020       | 4.2                                                  | \-                                   | X86                    |
| 비주얼 C++ 5.0             | 11.0            | [1997년](https://ko.wikipedia.org/wiki/1997년 "wikilink") | 1100       | 4.21                                                 | \-                                   | X86                    |
| 비주얼 C++ 6.0             | 12.0            | [1998년](https://ko.wikipedia.org/wiki/1998년 "wikilink") | 1200       | 6.0                                                  | \-                                   | X86                    |
| 비주얼 C++ .NET 2002 (7.0) | 13.00           | [2002년](https://ko.wikipedia.org/wiki/2002년 "wikilink") | 1300       | 7.0                                                  | 1.0                                  | X86                    |
| 비주얼 C++ .NET 2003 (7.1) | 13.10           | [2003년](https://ko.wikipedia.org/wiki/2003년 "wikilink") | 1310       | 7.1                                                  | 1.1                                  | X86, AMD64             |
| 비주얼 C++ 2005 (8.0)      | 14.00.50727.762 | [2005년](https://ko.wikipedia.org/wiki/2005년 "wikilink") | 1400       | 8.0                                                  | 2.0                                  | X86, AMD64, 아이테니엄      |
| 비주얼 C++ 2008 (9.0)      | 15.00.30729.01  | [2007년](https://ko.wikipedia.org/wiki/2007년 "wikilink") | 1500       | 9.0                                                  | 3.5                                  | X86, AMD64, 아이테니엄      |
| 비주얼 C++ 2010 (10.0)     | 16.00.40219.01  | [2010년](https://ko.wikipedia.org/wiki/2010년 "wikilink") | 1600       | 10                                                   | 4.0                                  | X86, AMD64, 아이테니엄      |
| 비주얼 C++ 2012 (11.0)     | 17.00.60315.1   | [2012년](https://ko.wikipedia.org/wiki/2012년 "wikilink") | 1700       | 11                                                   | 4.5                                  | X86, AMD64, 아이테니엄, ARM |
| 비주얼 C++ 2013 (12.0)     | 18.0.21005.1    | [2013년](https://ko.wikipedia.org/wiki/2013년 "wikilink") | 1800       | 12                                                   | 4.5.1                                | X86, AMD64, ARM        |
| 비주얼 C++ 2015 (14.0)     |                 | [2015년](https://ko.wikipedia.org/wiki/2015년 "wikilink") | 1900       | 14                                                   |                                      | X86, AMD64, ARM        |
| 비주얼 C++ 2017 Community  |                 |                                                         | 1914       |                                                      |                                      |                        |

### 비주얼 C++ 2012

비주얼 C++ 2012는 이전 버전과 확연한 차이점이 존재한다.

  - 이 버전부터 다국어 UI를 지원한다. 언어팩을 설치하여 사용하고자 하는 언어로 변경할 수 있다.
  - [윈도 8](https://ko.wikipedia.org/wiki/윈도_8 "wikilink"), [윈도 RT](https://ko.wikipedia.org/wiki/윈도_RT "wikilink") 전용 소프트웨어인 [윈도 스토어](https://ko.wikipedia.org/wiki/윈도_스토어 "wikilink") 지원 앱을 만들 수 있다.
  - [ARM 아키텍처에서](https://ko.wikipedia.org/wiki/ARM "wikilink") 구동할 수 있는 윈도 스토어 전용 앱을 만들 수 있다.
  - 출시 초기에는 [윈도 7](https://ko.wikipedia.org/wiki/윈도_7 "wikilink") 이상에서만 구동할 수 있는 실행 파일만 만들 수 있었지만, 업데이트 1 이상으로 갱신하면 [윈도 XP에서도](https://ko.wikipedia.org/wiki/윈도_XP "wikilink") 구동할 수 있는 실행 파일을 만들 수 있다.
  - 테스트 프로페셔녈 버전에는 컴파일러가 포함되어 있지 않다.
  - HLSL 컴파일 기능과 DirectX 그래픽 디버거를 포함한다. (XP 지원 모드 제외)
  - 컴파일 속도가 개선되었다.
  - 표준 C++11을 도입했다.

### 비주얼 C++ 2013

  - 더 나은 C++11, C99 지원이 포함되며 [REST](../Page/REST.md "wikilink") SDK를 도입하였다.\[1\]
  - [윈도 8.1용](https://ko.wikipedia.org/wiki/윈도_8.1 "wikilink") [윈도 스토어](https://ko.wikipedia.org/wiki/윈도_스토어 "wikilink") 앱을 만들 수 있다.
  - [윈도 폰 8용](https://ko.wikipedia.org/wiki/윈도_폰 "wikilink") SDK와 에뮬레이터를 포함하며 앱을 만들 수 있다.
  - [C++/CX](https://ko.wikipedia.org/wiki/C++/CX "wikilink")라는 신규 규격이 추가되었다.
  - DirectX SDK PIX의 DirectX 11.1 디버깅 기능을 IDE에 포함시켰다.
  - 인텔 Itanium 프로세서용 빌드를 더 이상 지원하지 않는다.

## 참조

<references />

## 외부 링크

  - [마이크로소프트 비주얼 C++ 개발자 센터](http://msdn.microsoft.com/visualc/)

[분류:통합 개발 환경](https://ko.wikipedia.org/wiki/분류:통합_개발_환경 "wikilink") [분류:C 컴파일러](https://ko.wikipedia.org/wiki/분류:C_컴파일러 "wikilink") [분류:C++ 컴파일러](https://ko.wikipedia.org/wiki/분류:C++_컴파일러 "wikilink") [C++](https://ko.wikipedia.org/wiki/분류:마이크로소프트_비주얼_스튜디오 "wikilink")

1.