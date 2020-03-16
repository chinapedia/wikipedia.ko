> This article is converted from Wikipedia: [Bad command or file name](https://ko.wikipedia.org/wiki/Bad_command_or_file_name).


**Bad command or file name**은 [MS-DOS](../Page/MS-DOS.md "wikilink")에서 유효하지 않은 명령을 내릴 경우에 나타나는 오류 메시지이다. [구문 오류](https://ko.wikipedia.org/wiki/구문_오류 "wikilink") 메시지이며 [1980년대](../Page/1980년대.md "wikilink") [베이직](../Page/베이직.md "wikilink") [인터프리터](../Page/인터프리터.md "wikilink")가 그 기원이다. [COMMAND.COM](../Page/COMMAND.COM.md "wikilink") 파일에 내장된 내부 명령어가 아니면서 디렉터리에 해당 실행파일이 존재하지 않을 경우\[1\] 이 메시지가 출력된다.

    C:₩>abc
    Bad command or file name.

    C:₩>_

위의 예는 COMMAND.COM에 ABC라는 내부 명령어가 내장되어 있지 않고 또 ABC.COM, ABC.EXE, ABC.BAT 셋 중 어느 하나도 C:\\에 없음을 의미한다.

## 관련 메시지

  - 최근의 한국어판 MS-DOS 기준으로, (biling.sys가 CONFIG.SYS를 통해 로드되어 있고 한글 바이오스가 실행되고 있으며 코드페이지가 949로 되어 있는 경우) 다음과 같은 메시지가 출력된다.:

  - 옛날의 한국어판 MS-DOS 기준으로 다음과 같은 메시지가 출력된다.:

  - [GUI를](../Page/그래픽_사용자_인터페이스.md "wikilink") 사용하는 OS/2와 최근의 윈도 NT 계열(윈도 XP, 비스타, 7 등)의 가상 도스에서는 다음과 같은 메시지가 출력된다.:



이렇게 메시지가 길어진 까닭은 초보자들이 단순히 "명령 또는 파일 이름이 잘못되었다"는 메시지를 잘 이해하지 못하였기 때문이다.

  - 그 밖의 다른 비슷한 오류 메시지는 도스의 종류나 환경에 따라 달라질 수 있다.

## 참고

<references />

[분류:컴퓨터 오류](https://ko.wikipedia.org/wiki/분류:컴퓨터_오류 "wikilink")

1.  [AUTOEXEC.BAT](../Page/AUTOEXEC.BAT.md "wikilink") 파일에서 PATH=로 설정된 경로, 또는 명령 프롬프트에서 직접 PATH=로 지정된 경로에 있는 실행파일은 디렉터리에 관계없이 실행된다.