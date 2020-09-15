> This article is converted from Wikipedia: [Cppcheck](https://ko.wikipedia.org/wiki/Cppcheck).


**Cppcheck**는 [C](../Page/C_\(프로그래밍_언어\).md "wikilink"), [C++](https://ko.wikipedia.org/wiki/C++ "wikilink") [프로그래밍 언어용](../Page/프로그래밍_언어.md "wikilink") [정적 코드 분석](../Page/정적_프로그램_분석.md "wikilink") 도구이다. 비표준 코드를 검사할 수 있는 다목적 도구이다.\[1\] 제작자이자 선임 개발자는 Daniel Marjamäki이다.

Cppcheck는 [GNU 일반 공중 사용 허가서로](../Page/GNU_일반_공중_사용_허가서.md "wikilink") 배포되는 [자유 소프트웨어이다](../Page/자유_소프트웨어.md "wikilink").

## 기능

Cppcheck는 컴파일러 자체에서 다루지 않을 수 있는 다양한 정적 검사를 지원한다. 해당 검사들은 정벅 분석 검사들이며 소스 코드 레벨에서 수행이 가능하다. 이 프로그램은 [휴리스틱 이론이](../Page/휴리스틱_이론.md "wikilink") 아닌 엄격한 정적 분석 검사를 지향한다.

지원되는 검사들 중 일부는 다음을 포함한다:

  - [자동 변수](../Page/자동_변수.md "wikilink") 검사
  - 배열 오버런(overrun) [경계 검사](../Page/경계_검사.md "wikilink")
  - [클래스](../Page/클래스_\(컴퓨터_프로그래밍\).md "wikilink") 검사 (예: 미사용 함수, 변수 초기화, 메모리 중복)
  - [오픈 그룹에](../Page/오픈_그룹.md "wikilink") 의거한 구식(deprecated) 처리 또는 대체된 함수의 사용\[2\]
  - 예외 안전 검사(예: 메모리 할당 사용 및 소멸자 검사)
  - [메모리 누수](../Page/메모리_누수.md "wikilink") (예: 할당 해제 없이 스코프 소실)
  - [자원 누수](../Page/자원_누수.md "wikilink") (예: 파일 핸들을 닫는 것을 잊음)
  - 유효하지 않은 [표준 템플릿 라이브러리](../Page/표준_템플릿_라이브러리.md "wikilink") 함수 및 [관용구](https://ko.wikipedia.org/wiki/관용구 "wikilink") 사용
  - 기타 스타일 및 성능 오류

## 플러그인

다음과 같은 [IDE용](../Page/통합_개발_환경.md "wikilink") 플러그인이 존재한다.\[3\]

  - [젯브레인즈](../Page/젯브레인즈.md "wikilink")\[4\]
  - [Code::Blocks](../Page/Code::Blocks.md "wikilink") - 연동.
  - [코드라이트](https://ko.wikipedia.org/wiki/코드라이트 "wikilink") - 연동.
  - [이클립스](../Page/이클립스_\(소프트웨어\).md "wikilink")\[5\]
  - [이맥스](../Page/이맥스.md "wikilink")\[6\]
  - [Gedit](../Page/Gedit.md "wikilink")\[7\]
  - [허드슨](../Page/허드슨_\(소프트웨어\).md "wikilink")\[8\]
  - [Jenkins](../Page/젠킨스.md "wikilink")\[9\]
  - [케이트](https://ko.wikipedia.org/wiki/케이트_\(문서_편집기\) "wikilink")\[10\]
  - [KDevelop](../Page/KDevelop.md "wikilink")\[11\]
  - [Qt 크리에이터](https://ko.wikipedia.org/wiki/Qt_크리에이터 "wikilink")\[12\]
  - [서브라임 텍스트](../Page/서브라임_텍스트.md "wikilink")\[13\]
  - [마이크로소프트 비주얼 스튜디오](../Page/마이크로소프트_비주얼_스튜디오.md "wikilink")\[14\]\[15\]\[16\]
  - [Yasca](https://ko.wikipedia.org/wiki/Yasca "wikilink")\[17\]

## 각주

## 외부 링크

  -
[분류:크로스 플랫폼 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_자유_소프트웨어 "wikilink") [분류:C++로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C++로_작성된_자유_소프트웨어 "wikilink") [분류:GPL 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:GPL_라이선스_소프트웨어 "wikilink") [분류:자유 소프트웨어 테스트 도구](https://ko.wikipedia.org/wiki/분류:자유_소프트웨어_테스트_도구 "wikilink") [분류:정적 프로그램 분석 도구](https://ko.wikipedia.org/wiki/분류:정적_프로그램_분석_도구 "wikilink")

1.
2.  <http://www.opengroup.org/onlinepubs/9699919799/xrat/V4_xsh_chap03.html>
3.
4.
5.
6.
7.
8.
9.
10.  Get an Edge in Editing|access-date=2016-12-14}}
11.
12.
13.
14.
15.
16.
17.