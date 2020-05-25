> This article is converted from Wikipedia: [COMMAND.COM](https://ko.wikipedia.org/wiki/COMMAND.COM).


**`COMMAND.COM`**은 [도스](../Page/도스.md "wikilink")와 [윈도우 95](../Page/윈도우_95.md "wikilink"), [98](../Page/윈도우_98.md "wikilink"), [ME](https://ko.wikipedia.org/wiki/윈도우_Me "wikilink") 등을 기본으로 하는 [운영 체제](../Page/운영_체제.md "wikilink") 셸의 파일 이름으로 명령 줄 해석기라 부른다.

시동 직후 첫 프로그램이 실행되면 [`AUTOEXEC.BAT`](../Page/AUTOEXEC.BAT.md "wikilink") 구성 파일을 실행하여 시스템을 설정할 책임을 가지고 뒤따르는 다른 과정을 밟게 된다.

## 운영 방식

[도스 셸을](../Page/도스_셸.md "wikilink") 제공하며 두 가지 기능을 제공한다. 첫째로는 사용자가 [명령어를](https://ko.wikipedia.org/wiki/명령어_\(컴퓨팅\) "wikilink") 입력하면 즉시 실행하는 사용자 대화 방식이 있다. 둘째로는 [일괄처리](https://ko.wikipedia.org/wiki/일괄처리 "wikilink")(배치) 방식이며 [문자열](https://ko.wikipedia.org/wiki/문자열 "wikilink")이 담긴 `.`[`BAT`](../Page/배치_파일.md "wikilink")라는 확장자를 가진 파일 안에 명령어들을 순서대로 나열해 두면 그 순서대로 명령어 처리기가 실행할 수 있다. [`cmd.exe`](https://ko.wikipedia.org/wiki/cmd.exe "wikilink")는 [윈도우 NT](../Page/윈도우_NT.md "wikilink"), [2000](../Page/윈도우_2000.md "wikilink"), [XP](../Page/윈도우_XP.md "wikilink"), [2003](../Page/윈도우_서버_2003.md "wikilink"), [비스타](../Page/윈도우_비스타.md "wikilink") 등 [OS/2](https://ko.wikipedia.org/wiki/OS/2 "wikilink")에서 쓰이며 [윈도우 NT](../Page/윈도우_NT.md "wikilink") 계열의 [운영 체제에서는](../Page/운영_체제.md "wikilink") [OS](https://ko.wikipedia.org/wiki/OS "wikilink") 상에서 [도스](../Page/도스.md "wikilink")를 실행 할 수는 없지만 [가상 도스 머신을](../Page/가상_도스_머신.md "wikilink") 이용하여 [DOS](../Page/도스.md "wikilink") 응용 프로그램들이 실행될 때 호환성을 제공하기 위해 쓰였다.

## 잘 알려진 내부 명령어

모든 명령어는 마지막 줄에  키가 눌린 뒤에만 실행된다. `COMMAND.COM`은 대소문자를 구별하지 않기 때문에 어느 문자열이나 대소문자가 섞여 있어도 같은 것으로 인식한다. 이를테면, dir, DIR, DiR, dIr, diR 모두 똑같이 동작한다.

### 파일 시스템 명령어

`COMMAND.COM`의 주 기능으로 여러 파일과 함께 동작할 수 있는 수많은 내장 명령어를 들 수 있다.

프로그램을 실행하려면, 단순히 실행 파일의 이름을 입력하고  키를 누르면 된다. 현재의 드라이브를 바꾸려면 드라이브 문자열에 콜론 기호를 덧붙이면 된다. (이를테면 D 드라이브로 이동할 때, `D:`) 다른 파일 시스템 명령어는 보통 다음의 것들을 들 수 있다:

  - [DIR](https://ko.wikipedia.org/wiki/Dir_\(명령어\) "wikilink") : 지정한 디렉터리의 내용을 나열한다.
    CD, [CHDIR](https://ko.wikipedia.org/wiki/chdir "wikilink") : [현재 작업하는 디렉터리를](https://ko.wikipedia.org/wiki/작업_디렉터리 "wikilink") 바꾸거나 현재의 디렉터리를 보여 준다.
    COPY : 파일을 디렉터리나 표준 입출력장치로 복사한다. 다수의 파일을 결합하거나 새로운 파일을 만들 수 있다. 대상이 이미 존재하면 MS-DOS는 기존의 대상을 대체할 것인지 묻는다. (디렉터리까지 완전히 복사하는 외부 명령어 [XCOPY](https://ko.wikipedia.org/wiki/XCOPY "wikilink")도 있다.)
    REN, RENAME : 파일이나 디렉터리의 이름을 바꾼다.
    DEL, ERASE : 파일을 삭제한다. 디렉터리로 사용될 때, 해당 디렉터리의 지정 파일을 지우지만 디렉터리 자체를 지우지는 않는다. 윈도우 XP와 윈도우 2000은 /S 옵션을 추가하면 하위 디텍터리도 삭제한다.
    MD, MKDIR : 디렉터리를 새로 하나 만든다.
    RD, [RMDIR](https://ko.wikipedia.org/wiki/rmdir "wikilink") : 빈 디렉터리를 제거한다.
    VOL : 볼륨, 곧 디스크 이름과 일련번호를 보여 준다.
    LABEL : 볼륨, 곧 디스크 이름과 일련번호를 보여 주고 이름을 바꾼다.
    VERIFY : 파일 쓰기의 유효성을 확인하게 하거나 확인하지 않게 한다.
    TYPE : 파일의 내용을 보여 준다. (TYPE은 파일의 내용을 한 화면마다 끊어서 보여 주지 않지만, 외부 명령어 MORE는 파일의 내용을 끊어서 보여 준다.)

<!-- end list -->

  - BREAK : 로 프로그램 인터럽트 관리를 제어한다. 어떠한 과정의 동작을 멈출 때 사용한다.
    [CLS](https://ko.wikipedia.org/wiki/cls_\(명령어\) "wikilink") : 화면을 지운다.
    CHCP : 현재의 시스템 [코드 페이지를](../Page/코드_페이지.md "wikilink") 보여 주거나 바꾼다. 한국어 코드 페이지를 띄우려면 chcp 949, 영문 코드 페이지를 띄우려면 chcp 437을 입력하면 된다. (MS-DOS 한글판에서는 hcode 명령어가 존재했는데 hcode /k라고 입력하면 chcp 949로, hcode /e라고 입력하면 chcp 437로 동작한다.)
    CTTY : 장치의 입출력을 정의한다.
    DATE : 시스템 날짜를 설정한다.
    ECHO : 문자열을 보여 줄지 보여 주지 않을지 정하거나 (`ECHO ON`, `ECHO OFF`) 사용자가 지정한 문자열을 화면에 보여 준다. (`ECHO 문자열`).
    LH, LOADHIGH : 프로그램을 [상위 메모리로](https://ko.wikipedia.org/wiki/상위_메모리_영역 "wikilink") 올려 놓는다 ([DR-DOS](../Page/DR-DOS.md "wikilink")의 경우 `HILOAD`).
    LOCK : 외부 프로그램이 낮은 수준의 디스크 접근을 볼륨에 수행할 수 있게 한다. ([윈도우 95](../Page/윈도우_95.md "wikilink")/[98](../Page/윈도우_98.md "wikilink")/[Me에서만](https://ko.wikipedia.org/wiki/윈도우_Me "wikilink"))
    PATH : PATH [환경 변수의](../Page/환경_변수.md "wikilink") 값을 보여 주거나 변경한다. PATH로 연결된 실행 파일을 찾게 되며, 나중에 작업 디렉터리에 실행 파일이 없어도 PATH 변수에 걸린 디렉터리에 해당 프로그램이 있으면 실행하게 된다. PATH ; 라고 입력하면 기억된 모든 경로를 삭제한다.
    PAUSE : 사용자에게 계속하려면 아무 키나 누르라는 메시지를 보여 주고, [아무 키나](../Page/아무_키.md "wikilink") 누르면 계속한다.
    PROMPT : PROMPT 환경 변수를 보여 주거나 변경한다. 프롬프트의 모습을 바꿀 수 있다.
    SET : 환경 변수의 값을 설정한다. 변수를 지정하지 않으면 정의된 모든 환경 변수를 보여 준다.
    TIME : 시스템의 시간을 설정한다.
    UNLOCK : 낮은 수준의 디스크 접근을 사용하지 않는다. ([윈도우 95](../Page/윈도우_95.md "wikilink")/[98](../Page/윈도우_98.md "wikilink")/[Me에서만](https://ko.wikipedia.org/wiki/윈도우_Me "wikilink"))
    VER : [운영 체제의](../Page/운영_체제.md "wikilink") 버전을 보여 준다.

## 제어 구조

제어 구조는 배치 파일 안에서 대부분 쓰인다.

  - :*레이블* : GOTO의 대상을 정의한다.
    FOR : 되풀이: 지정된 파일 그룹의 각 실행은 반복한다.
    GOTO : 지정된 레이블로 실행 위치를 이동한다. 레이블은 콜론(`:likethis`)과 함께 줄 맨 처음에 지정된다.
    REM : [주석](https://ko.wikipedia.org/wiki/주석_\(컴퓨터_프로그래밍\) "wikilink"): 실행을 무시할 문자열이다.
    IF : 프로그램의 실행 조건문이다. "IF EXIST F.EXE GOTO a"는 F.EXE 파일이 존재하면 a 레이블로 이동하라는 뜻이 된다.
    CALL : 배치 파일의 실행을 멈추고 다른 곳으로 돌아갔다가 계속 진행한다.
    EXIT : Command.com에서 빠져나와서 프로그램으로 돌아온다.
    SHIFT : 각 명령 줄 변수를 한 칸 뒤로 이동한다 (e.g. `%0`을 `%1`로, `%1`을 `%2`로, 등. )

## 변수

`COMMAND.COM`을 위한 배치 파일들은 다음의 네 가지 변수를 사용한다고 말할 수 있다:

1.  ERRORLEVEL
2.  [환경 변수들](../Page/환경_변수.md "wikilink")
3.  명령 줄 매개변수
4.  "For" 변수들

## 리다이렉션과 파이프

  - *명령어* \< *파일이름* : 파일/장치에서 [표준 입력을](https://ko.wikipedia.org/wiki/표준_입력 "wikilink") 리다이렉트한다
    *명령어* \> *파일이름* : [표준 출력을](https://ko.wikipedia.org/wiki/표준_출력 "wikilink") 파일로 리다이렉트한다. 대상 파일이 있으면 덮어씌운다.
    *명령어* \>\> *파일이름* : [표준 출력을](https://ko.wikipedia.org/wiki/표준_출력 "wikilink") 파일로 리다이렉트한다. 대상 파일이 있으면 그 아래 줄부터 추가한다.
    *명령어1* | *명령어2* : "명령어 1"의 [표준 출력을](https://ko.wikipedia.org/wiki/표준_출력 "wikilink") "명령어2"의 [표준 입력으로](https://ko.wikipedia.org/wiki/표준_입력 "wikilink") 파이프 처리한다.

도스가 단일 작업 운영 체제이기 때문에, 파이프는 임시 파일로, 또는 임시 파일로부터 리다이렉트하면서 명령어들을 순서대로 실행하면서 처리한다. `COMMAND.COM`은 [표준 오류](https://ko.wikipedia.org/wiki/표준_오류 "wikilink") 채널을 리다이렉트 하지 못한다.

## 버그 및 제한

명령 줄의 길이는 최대 128 문자이다. 명령어를 실행할 때 언제나 참 값을 반환한다.

## 같이 보기

  - [셸](../Page/셸.md "wikilink")
  - [CMD.EXE](https://ko.wikipedia.org/wiki/CMD.EXE "wikilink")
  - [도스 명령어 목록](../Page/도스_명령어_목록.md "wikilink")

## 각주

## 외부 링크

  - [BAT 파일: 도스 배치 파일 프로그래밍 강좌](https://web.archive.org/web/20070510025446/http://home7.inet.tele.dk/batfiles/batfiles.htm)
  - [윌리엄과 린다 앨렌의 윈도우 95/98/ME의 ERRORLEVEL 문서 (작은 ZIP 파일)](https://web.archive.org/web/20110707113138/http://www.allenware.com/mcsw/errorlevels.zip)
  - [command.com 웹사이트 (인터넷 저장 문서)](https://web.archive.org/web/20030401235450/http://command.com/)

[분류:스크립트 언어](https://ko.wikipedia.org/wiki/분류:스크립트_언어 "wikilink") [분류:도스 파일](https://ko.wikipedia.org/wiki/분류:도스_파일 "wikilink") [분류:외부 도스 명령어](https://ko.wikipedia.org/wiki/분류:외부_도스_명령어 "wikilink") [분류:셸](https://ko.wikipedia.org/wiki/분류:셸 "wikilink")