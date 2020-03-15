> This article is converted from Wikipedia: [IEFBR14](https://ko.wikipedia.org/wiki/IEFBR14).


**IEFBR14**은 [IBM](https://ko.wikipedia.org/wiki/IBM "wikilink") [메인프레임](https://ko.wikipedia.org/wiki/메인프레임_컴퓨터 "wikilink") [유틸리티 프로그램이다](../Page/IBM_메인프레임_유틸리티_프로그램.md "wikilink"). [z/OS](https://ko.wikipedia.org/wiki/z/OS "wikilink")를 포함하여 [OS/360](https://ko.wikipedia.org/wiki/OS/360 "wikilink")에서 파생된 모든 IBM 메인프레임 환경에서 실행된다. 이것을 사용하는 목적은 [아무 일도 하지 않는 것이다](../Page/NOP.md "wikilink"). 여러 해에 걸쳐, 아무 일도 하지 않는다는 시도는 너무 간결해서 연관이 되는 도구들에 문제를 일으킬 수 있으며 프로그램이 사소하게 확장된다.

## 목적

### 할당

OS/360 파생 메인프레임 운영 체제에서 대부분의 프로그램들은 파일(일반적으로 [데이터셋](https://ko.wikipedia.org/wiki/데이터셋 "wikilink"))을 직접 규정하지 않으며, 대신 프로그램들을 호출하는 [작업 제어 언어](https://ko.wikipedia.org/wiki/작업_제어_언어 "wikilink")(JCL) 문을 통해 간접적으로 이들을 참조한다. 이러한 데이터 정의문(DD)들은 DISPOSITION(DISP=...) 매개변수를 포함하여 파일을 어떻게 관리할지 지정할 수 있다. 이를테면, 새로운 파일이 만들어질지 아니면 오래된 것을 다시 사용할지, 또 완료 후에 파일을 삭제해야 하는지 아니면 그대로 남겨두어야 하는지 등을 정할 수 있다.

IEFBR14는 DD 문들이 파일들을 쉽게 만들거나 지울 수 있는 반면, 프로그램을 실행하지 않고서는 그렇게 할 수 없었기 때문에 만들어졌다. JCL에 쓰이는 프로그램은 실제로 생성 또는 삭제를 위해 파일을 사용할 필요가 없다. DD DISP=... 사양으로 모든 작업이 수행된다. 그러므로 해당 역할을 메우기 위해서는 매우 단순한 do-nothing 프로그램이 필요하였다.

이에 따라 IEFBR14는 JCL을 이용하여 데이터셋을 만들거나 삭제할 수 있다.

### 할당 해제

IEFBR14을 실행하는 두 번째 이유는 (잡의 JCL에 오류가 발생했거나 잡이 오류로 종료된 이유 등으로) 이전 잡으로부터 마운트된 채 남겨진 테이프의 마운트를 해제하는 것이다. 어떠한 경우에서든 시스템 조작자들은 테이프의 마운트를 해제한 뒤 이 목적을 위해 DEALLOC 작업을 시작해야 했다.

단순히 다음과 같이 명령을 시스템 콘솔에 입력하면

`S DEALLOC`

시작된 작업을 실행할 수 있는데, 이 작업은 오직 하나의 [스텝으로만](https://ko.wikipedia.org/wiki/작업_제어_언어 "wikilink") 구성된다.

`//STEP01    EXEC PGM=IEFBR14`

## 사용법

[JCL의](https://ko.wikipedia.org/wiki/작업_제어_언어 "wikilink") 예는 다음과 같다:

``` jcl
//IEFBR14  JOB  ACCT,'DELETE DATASET',MSGCLASS=J,CLASS=A
//STEP0001 EXEC PGM=IEFBR14
//DELDD    DD DSN=xxxxx.yyyyy.zzzzz,
//            DISP=(MOD,DELETE,DELETE),UNIT=DASD
```

파티션 데이터셋을 만드는 구문은 다음과 같다:

``` jcl
//TZZZ84R  JOB NOTIFY=&SYSUID,MSGCLASS=X
//STEP01    EXEC PGM=IEFBR14
//DD1       DD DSN=TKOL084.DEMO,DISP=(NEW,CATLG,DELETE),
//             DCB=(RECFM=FB,LRECL=80,BLKSIZE=80,DSORG=PO),
//             SPACE=(TRK,(1,1,1),RLSE),
//             UNIT=SYSDA
```

## 같이 보기

  - [IEFBR14//dev/null](https://ko.wikipedia.org/wiki/IEFBR14/dev/null "wikilink")
  - [IEFBR14//bin/true](https://ko.wikipedia.org/wiki/IEFBR14/bin/true "wikilink")

## 외부 링크

  - [True in a Nutshell Appendix: IEFBR14](http://www.miketaylor.org.uk/tech/oreilly/iefbr14.html)
  - [True in a Nutshell Appendix: IEFBR14: Clarification](http://www.miketaylor.org.uk/tech/oreilly/more-iefbr14.html)
  - [MVS JCL User's Guide (SA22-7598)](http://www.ibm.com/servers/eserver/zseries/zos/bkserv/r8pdf/mvs.html)

[분류:IBM 메인프레임 운영 체제](https://ko.wikipedia.org/wiki/분류:IBM_메인프레임_운영_체제 "wikilink") [분류:무 (철학)](https://ko.wikipedia.org/wiki/분류:무_\(철학\) "wikilink")