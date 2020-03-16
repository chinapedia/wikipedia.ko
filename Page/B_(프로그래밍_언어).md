> This article is converted from Wikipedia: [B \( \)](https://ko.wikipedia.org/wiki/B_\(_\)).


**B**는 [AT\&T](../Page/AT&T.md "wikilink") [벨 연구소의](../Page/벨_연구소.md "wikilink") [켄 톰슨이](https://ko.wikipedia.org/wiki/켄_톰슨 "wikilink") 개발한 [프로그래밍 언어이다](../Page/프로그래밍_언어.md "wikilink"). [C 언어로](../Page/C_\(프로그래밍_언어\).md "wikilink") 흡수되는 형태로 거의 멸종했다. 켄 톰슨이 [데니스 리치의](../Page/데니스_리치.md "wikilink") 감수를 받는 형태로 설계하였으며 [1969년](../Page/1969년.md "wikilink")에 등장했다.

## 소개

B는 실질적인 C의 조상 언어로 볼 수 있다. B 언어로 만든 프로그램은 [컴파일러](../Page/컴파일러.md "wikilink")에 의해 중간 코드로 변환되어 실행하는 [인터프리터](../Page/인터프리터.md "wikilink")를 필요로 한다. 실행시에는 인터프리터 번역 순서대로 처리되기 때문에 실행 속도가 극도로 느렸다. 단 [PDP-7](https://ko.wikipedia.org/wiki/PDP-7 "wikilink") 버전은 [기계어](../Page/기계어.md "wikilink")로 처리할 수 있도록 개량되었다.

## 역사

켄 톰슨은 DEC의 컴퓨터 PDP-7로 [유닉스](../Page/유닉스.md "wikilink")를 개발하고 있었지만 당시 유닉스는 프로그램 개발을 [어셈블리 언어로](https://ko.wikipedia.org/wiki/어셈블리_언어 "wikilink") 밖에 할 수 없었다. 그래서 켄 톰슨은 유닉스에서 동작하는 고급언어 개발을 시작했다. 그는 유닉스 개발 이전 [멀틱스](../Page/멀틱스.md "wikilink") 개발에 종사하고 있었는데 멀틱스의 [BCPL](../Page/BCPL.md "wikilink")을 바탕으로 B 언어를 개발했다.

이후 B 언어는 켄 톰슨 자신과 [데니스 리치](../Page/데니스_리치.md "wikilink"), [브라이언 커니핸에](../Page/브라이언_커니핸.md "wikilink") 의해 개량되어 NewB(NB)를 거쳐 이윽고 [C 언어로](../Page/C_\(프로그래밍_언어\).md "wikilink") 발전하게 된다.

B언어는 켄 톰슨이 당시의 미니 컴퓨터의 [메모리 용량에서](https://ko.wikipedia.org/wiki/메모리_용량 "wikilink") 작동할 수 있게 하려고 불필요한 [구성 요소](https://ko.wikipedia.org/wiki/구성_요소 "wikilink")(컴포넌트)를 제거한 일종의 [BCPL](../Page/BCPL.md "wikilink") 시스템이다.

[BCPL](../Page/BCPL.md "wikilink")이나 [Forth](https://ko.wikipedia.org/wiki/Forth "wikilink")와 같이 B 언어는 워드 형태의 1개의 데이터형만 가지고 있었다. 많은 연산자(사칙 연산 등)는 이 데이터를 정수로 취급하였고, 그 이외에는 모두 [포인터로](../Page/포인터_\(프로그래밍\).md "wikilink") 다루었다. 그 이외의 부분은 C 언어의 초기 버전과 비슷하다. C 언어의 [표준 입출력 라이브러리에](../Page/C_표준_라이브러리.md "wikilink") 비견되는 [라이브러리](https://ko.wikipedia.org/wiki/라이브러리 "wikilink")를 가지고 있었다.

초기에는 유닉스를 사용한 DEC의 PDP-7용과 PDP-11에서 사용되었고 한편 [GCOS](https://ko.wikipedia.org/wiki/GCOS "wikilink")라고 하는 OS가 동작하는 [허니웰](../Page/허니웰.md "wikilink")의 36비트 [메인프레임](../Page/메인프레임.md "wikilink")에도 사용하였다. 최초의 PDP-7용에서는 [스레드 코드로](https://ko.wikipedia.org/wiki/스레드_코드 "wikilink") 컴파일 하여 데니스 리치가 기계어로 출력하는 컴파일러를 만들었다. [1970년](../Page/1970년.md "wikilink")에 PDP-11에 도입되었지만 역시 이식에는 스레드 코드가 사용되었다. 이때 최초의 [yacc](https://ko.wikipedia.org/wiki/yacc "wikilink")가 PDP-11용으로 개발되었다. 데니스 리치는 이 시기에 유지보수를 담당했다.

B 언어는 [자료형](../Page/자료형.md "wikilink")이 없는 설계로 허니웰이나 PDP-7과 같은 낡은 컴퓨터에서는 쓸모있었지만, PDP-11이나 현대적인 컴퓨터가 지원하는 문자 자료형을 적절히 처리할 수 없었기 때문에 문제가 되었다. [1971년](../Page/1971년.md "wikilink") 데니스 리치는 전면적인 변경을 시도해 컴파일러가 기계어 코드를 생성할 수 있도록 하는 한편 자료형을 변수를 추가했다. [1971년](../Page/1971년.md "wikilink")부터 [1972년](../Page/1972년.md "wikilink")까지 B 언어는 NewB 언어로 진화했고 앨런 슈나이더(Alan Snyder)의 강한 요구로 [전처리기](https://ko.wikipedia.org/wiki/전처리기 "wikilink")가 더해져서 [1972년](../Page/1972년.md "wikilink"), [1973년](../Page/1973년.md "wikilink") 두해 동안 초기의 C 언어로 진화했다. [1973년](../Page/1973년.md "wikilink") 여름에 드디어 PDP-11용 유닉스가 C 언어로 다시 씌여져서 이러한 노력은 완전한 결실을 맺게 되었다. [1973년](../Page/1973년.md "wikilink")에는 허니월 635 시스템에서 IBM 360/370 시스템으로 이식할 필요성이 제기되었는데 이 와중에 마이크 레스크(Mike Lesk)는 나중에 C 언어 표준 입출력 라이브러리(stdio)가 되는 《범용 I/O 패키지》를 작성했다.

B 언어는 허니웰의 메인프레임에서 1990년대까지 계속 이용되었다. 또한 단순 업무 활용에 필요하다든가 툴 및 라이선스 문제 등의 이유로 인해 일부 [임베디드](https://ko.wikipedia.org/wiki/임베디드 "wikilink") 시스템에서도 사용되고 있었다. 한편 유명한 오픈소스 [다중 사용자 온라인 게임](https://ko.wikipedia.org/wiki/다중_사용자_온라인_게임 "wikilink") [AberMUD](https://ko.wikipedia.org/wiki/AberMUD "wikilink")도 B 언어로 제작되었다.

B 언어는 BCPL의 영향을 그대로 받았기 때문에 명칭인 B 마저 BCPL의 머리글자를 따왔을 가능성이 높다. 하지만 켄 톰슨은 멀틱스에서 사용하기 위해 전혀 다른 방식의 언어인 [Bon를](https://ko.wikipedia.org/wiki/Bon_\(프로그래밍_언어\) "wikilink") 고안했는데 이것이 이름의 유래일 가능성이 있다.

## 코드 예제

켄 톰슨이 쓴 *《Users' Reference to B》*에서 발췌됨

    /* 다음 함수는 비음(非陰)의 숫자 n을 b진수 형태로 출력한다 (단, 2<=b<=10)
      이 루틴은 ASCII 문자 코드 값이 0에서 9까지 연속하고 있음을 이용하고 있다. */

    printn(n,b) {
            extrn putchar;
            auto a;

            if(a=n/b) /* 대입문. 등차 비교가 아님 */
                    printn(a, b); /* 재귀 호출 */
            putchar(n%b + '0');
    }

## 함께 보기

  - [BCPL](../Page/BCPL.md "wikilink")
  - [C (프로그래밍 언어)](../Page/C_\(프로그래밍_언어\).md "wikilink")

## 외부 링크

  - *[The Development of the C Language](http://cm.bell-labs.com/cm/cs/who/dmr/chist.html)*, [데니스 리치](../Page/데니스_리치.md "wikilink"). [BCPL](../Page/BCPL.md "wikilink")과 [C의](../Page/C_\(프로그래밍_언어\).md "wikilink") 관계 중 B에 대해 설명.
  - *[Users' Reference to B](https://web.archive.org/web/20060706005453/http://cm.bell-labs.com/cm/cs/who/dmr/kbman.html)*, [켄 톰슨](https://ko.wikipedia.org/wiki/켄_톰슨 "wikilink"). [PDP-11](../Page/PDP-11.md "wikilink") 버전에 관해 설명.
  - *[The Programming Language B](https://web.archive.org/web/20070808110320/http://cm.bell-labs.com/cm/cs/who/dmr/bintro.html)*, S. C. Johnson & B. W. Kernighan, Technical Report CS TR 8, [벨 연구소](../Page/벨_연구소.md "wikilink") (1973년 1월). [허니웰](../Page/허니웰.md "wikilink") 제품용 [GCOS](https://ko.wikipedia.org/wiki/GCOS "wikilink")버전 설명서

[분류:절차적 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:절차적_프로그래밍_언어 "wikilink") [분류:1969년 개발된 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:1969년_개발된_프로그래밍_언어 "wikilink")