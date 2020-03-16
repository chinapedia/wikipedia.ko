> This article is converted from Wikipedia: [CLIST](https://ko.wikipedia.org/wiki/CLIST).


**CLIST**(Command List, "시-리스트"로 발음)는 [MVS](../Page/MVS.md "wikilink") 시스템의 [TSO를](../Page/시분할_선택_기능.md "wikilink") 위한 [절차적](../Page/절차적_프로그래밍.md "wikilink") [프로그래밍 언어이다](../Page/프로그래밍_언어.md "wikilink"). [OS/360](https://ko.wikipedia.org/wiki/OS/360 "wikilink") 릴리스 20에서 기원하였으며 TSO/E 버전 2에서 [REXX](../Page/REXX.md "wikilink")를 사용할 수 있게 된 뒤로 2차적 역할을 맡고 있다. CLIST라는 용어는 [넷뷰](https://ko.wikipedia.org/wiki/티볼리_매니지먼트_프레임워크 "wikilink") 사용자들이 작성한 명령어 목록을 위해 사용되기도 한다.\[1\]

기본 형태로 CLIST 프로그램(간단히 CLIST)는 순차적으로 실행할 [명령어의](https://ko.wikipedia.org/wiki/명령어_\(컴퓨팅\) "wikilink") 단순 목록 형태를 취할 수 있다. (마치 .bat 확장자의 [도스](../Page/도스.md "wikilink") [배치 파일처럼](../Page/배치_파일.md "wikilink")) 그러나 CLIST는 또한 If-Then-Else 로직과 루프 구성체를 지원한다.

CLIST는 [인터프리트 언어이다](https://ko.wikipedia.org/wiki/인터프리트_언어 "wikilink"). 즉, 컴퓨터는 프로그램이 실행될 때마다 CLIST를 번역해야 한다. 그러므로 CLIST는 [코볼](../Page/코볼.md "wikilink"), [포트란](../Page/포트란.md "wikilink"), [PL/1](https://ko.wikipedia.org/wiki/PL/1 "wikilink")과 같은 [컴파일 언어로](../Page/컴파일_언어.md "wikilink") 작성된 프로그램 보다 속도가 더 느린 경향이 있다. (컴파일 언어로 작성된 프로그램은 번역되면 "로드 모듈"이나 [실행 파일을](../Page/실행_파일.md "wikilink") 만든다.)

CLIST는 MVS 파일을 읽고 쓸 수 있으며, TSO 터미널을 경유하여 읽고 쓸 수 있다. 호출자로부터 매개변수를 읽을 수 있으며, 전역 변수를 보유하다가 CLIST들 간에 이들을 전달하는 기능도 제공한다. 또, CLIST는 (예를 들어 [코볼](../Page/코볼.md "wikilink")이나 [PL/I](https://ko.wikipedia.org/wiki/PL/I "wikilink")으로 작성된) MVS 응용 프로그램을 호출할 수도 있다. CLIST는 (TSO 제어 프로그램 IKJEFT01이라는 TSO 제어 프로그램을 실행하는 [JCL을](../Page/작업_제어_언어.md "wikilink") 수행함으로써) 백그라운드에서 실행이 가능하다. [ISPF](../Page/ISPF.md "wikilink") 다이얼로그 서비스들을 사용하는 TSO 입출력 화면과 메뉴는 CLIST를 통해 표시할 수 있다.

## 예제 프로그램

`PROC 0`
`WRITE HELLO WORLD!`

If-Then-Else 로직을 추가하면:

``` rexx numberLines
   /********************************************************************/
   /*  MULTI-LINGUAL "HELLO WORLD" PROGRAM.                            */
   /*                                                                  */
   /*  THIS CLIST, STORED AS USERID.TSO.CLIST(TEST), CAN BE INVOKED    */
   /*  FROM THE ISPF COMMAND LINE AS SHOWN IN THE FOLLOWING EXAMPLE:   */
   /*                                                                  */
   /*     COMMAND ===> TSO TEST SPANISH                                */
   /*                                                                  */
   /********************************************************************/
   PROC 1 LANGUAGE
     IF &LANGUAGE = SPANISH THEN +
        WRITE HOLA, MUNDO
     ELSE IF &LANGUAGE = FRENCH THEN +
        WRITE BONJOUR, MONDE
     ELSE +
        WRITE HELLO, WORLD
   EXIT
```

## 같이 보기

  - [REXX](../Page/REXX.md "wikilink")

## 각주

[분류:IBM 메인프레임 운영 체제](https://ko.wikipedia.org/wiki/분류:IBM_메인프레임_운영_체제 "wikilink") [분류:절차적 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:절차적_프로그래밍_언어 "wikilink") [분류:셸](https://ko.wikipedia.org/wiki/분류:셸 "wikilink") [분류:스크립트 언어](https://ko.wikipedia.org/wiki/분류:스크립트_언어 "wikilink")

1.