> This article is converted from Wikipedia: [Cp \(\)](https://ko.wikipedia.org/wiki/Cp_\(\)).


`cp`는 [유닉스](../Page/유닉스.md "wikilink") [셸](../Page/셸.md "wikilink")에서 한 [파일을](../Page/컴퓨터_파일.md "wikilink") 어떤 장소에서 다른 장소로 또는 다른 파일 시스템으로 옮길 때 사용하는 명령어이다. 원본 파일은 그대로 남아있고 새로운 파일이 기존 파일과 같은 이름으로 혹은 다른 이름으로 새로 생기게 된다.

이 문서는 [POSIX](../Page/POSIX.md "wikilink") 시스템의 명령어를 서술한다. [리눅스](../Page/리눅스.md "wikilink") 시스템의 `cp`는 추가적인 옵션들을 갖는다.

## 사용법

한 파일을 다른 파일로 복사하기 위해서는

**`cp`**` [ -f ] [ -H ] [ -i ] [ -p ][ -- ] `<u>`SourceFile`</u>` `<u>`TargetFile`</u>

한 파일을 다른 디렉터리로 복사하기 위해서는

**`cp`**` [ -f ] [ -H ] [ -i ] [ -p ] [ -r | -R ] [ -- ] `<u>`SourceFile`</u>` ... `<u>`TargetDirectory`</u>

한 디렉터리를 다른 디렉터리로 복사하기 위해서는

**`cp`**` [ -f ] [ -H ] [ -i ] [ -p ] [ -- ] { -r | -R } `<u>`SourceDirectory`</u>` ... `<u>`TargetDirectory`</u>

## 옵션

  - `-f`: (force) 만약 한 목표(target) 파일이 쓰기 기능을 위해서 열리기 않는 경우 그 목표 파일을 삭제할 것을 명시한다. 이러한 삭제는 cp 명령어로 수행될 다른 복사보다 먼저 시행된다.

<!-- end list -->

  - `-P`: `cp` 명령어가 심볼릭 링크를 복사하도록 만든다. 그 기본값(내정값)은 심볼릭 링크를 따라가도록 되어 있다. 즉 파일을 기호화된 링크가 지시하는 곳으로 복사하도록 한다.

<!-- end list -->

  - `-i`: (interactive) 파일을 덮어써야 할 경우 파일이름과 함께 프롬프트가 나탄난다. 이것은 TargetDirectory 또는 TargetFile 인자가 SourceFile 또는 SourceDirectory 인자에 명세된 파일과 같은 이름을 가진 파일을 갖고 있을 경우 일어난다. 만약 y(es) 또는 현재 로케일에서 y(es)에 해당하는 것을 입력하면 cp 명령어가 진행된다. 그밖의 다른 명령어들은 cp 명령어가 그 파일을 중복 복사하는 것을 막는다.

<!-- end list -->

  - `-p`: (preserve) 각각의 소스 파일/소스 디렉터리의 다음의 문자들을 대응하는 타켓 파일이나 타겟 디렉터리 안에 복사한다:

:\* 데이터의 마지막 수정 시간이나 데이터로의 마지막 접속 시간

:\* 사용자 ID나 그룹 ID(만약 그 파일에 접속 권한이 있을 경우에만)

:\* 그 파일의 허용 비트나 [SUID](https://ko.wikipedia.org/wiki/SUID "wikilink")나 [SGID](https://ko.wikipedia.org/wiki/SGID "wikilink") 비트

  - `-R`: (recursive) 디렉터리를 복사한다(순환적으로 안에 들어있는 모든 내용물을 복사한다)

## 예제

파일을 현재 디렉터리로 복사하기 위해서는, 다음과 같이 입력 :

`   cp prog.c prog.bak`

이것은 prog.c를 prog.bak로 복사한다. 만약 prog.bak 파일이 현재 존재하지 않는다면 cp 명령어는 그 파일을 새롭게 만든다. 만약 그 파일이 존재한다면 cp 명령어는 그것을 prog.c 파일의 복사물로 대체시킨다.

현재 디렉터리 안에 있는 파일을 다른 디렉터리로 옮기기 위해서는, 다음과 같이 입력 :

`   cp jones /home/nick/clients`

이것은 jones 파일을 /home/nick/clients/jones로 복사한다.

한 파일을 새로운 파일로 복사하거나 그 파일의 수정 날짜, 시간, 소스 파일과 관련된 접근 제한 목록을 보관하기 위해서는, 다음과 같이 입력 :

`   cp -p smith smith.jr`

이것은 smith 파일을 smith.jr 파일로 복사한다. 현재 날짜나 시간 기록을 갖고 있는 파일을 새로 만들기보다는, 시스템이 smith.jr 파일에 smith 파일과 같은 날짜와 시간을 부여한다. 또한 smith.jr 파일은 smith 파일의 접근 제한 보호를 내재한다.

한 디렉터리에 있는 모든 파일들을 새로운 디렉터리로 복사하기 위해서는, 다음과 같이 입력 :

`   cp /home/janet/clients/* /home/nick/customers`

이것은 cilents 디렉터리에 있는 파일만을 customers 디렉터리로 복사한다.

모든 파일과 하부 디렉터리를 포함하여 하나의 디렉터리를 다른 디렉터리로 복사할 경우, 다음과 같이 입력 :

`   cp -R /home/nick/clients /home/nick/customers`

이것은 clients 디렉터리를, 그 안에 있는 모든 파일과, 하부 디렉터리와 하부 디렉터리 안에 있는 모든 파일들을 포함하여 customers/clients 디렉터리로 복사한다.

어떤 특별한 파일의 묶음을 다른 디렉터리로 복사할 경우, 다음과 같이 입력 :

`   cp jones lewis smith /home/nick/clients`

이것은 현재 실행중인 디렉터리 안에 있는 jones과 lewis 그리고 smith 파일을 /home/nick/clients 디렉터리로 복사한다.

파일을 복사하기 위해서 pattern-matching 문자를 사용한다. 다음과 같이 입력 :

`   cp programs/*.c .`

이것은 programs 디렉터리 안에 있는 .c로 끝나는 파일을 현재 디렉터리로 현재 디렉터리로 복사한다. 이때 .(점)은 현재 디렉터리를 나타낸다. 입력시 c와 마지막 . 사이를 스페이스로 반드시 띄어야 한다.

## 관련 유닉스 명령어

  - [`cpio`](https://ko.wikipedia.org/wiki/cpio "wikilink") : 전체 디렉터리 구조를 한 장소에서 다른 장소로 복사한다
    [`tar`](../Page/Tar_\(파일_포맷\).md "wikilink") : 파일들의 아카이브(archive)를 만든다
    [`link`](https://ko.wikipedia.org/wiki/link "wikilink") : 다른 파일이나 디렉터리를 연결하기 위한 링크를 만들기 위한 시스템 콜
    [`ln`](https://ko.wikipedia.org/wiki/ln "wikilink") : 다른 파일이나 디렉터리로의 링크를 만든다
    [`mv`](https://ko.wikipedia.org/wiki/mv "wikilink") : 파일이나 디렉터리를 이동시킨다
    [`rm`](https://ko.wikipedia.org/wiki/rm_\(유닉스\) "wikilink") : 파일이나 디렉터리를 삭제한다
    [`unlink`](https://ko.wikipedia.org/wiki/unlink "wikilink") : 파일이나 디렉터리를 삭제하기 위한 시스템 콜
    [`chmod`](https://ko.wikipedia.org/wiki/chmod "wikilink") : 파일이나 디렉터리의 사용 허가를 바꾼다
    [`chown`](https://ko.wikipedia.org/wiki/chown "wikilink") : 파일이나 디렉터리의 소유권을 바꾼다
    [`chgrp`](https://ko.wikipedia.org/wiki/chgrp "wikilink") : 파일이나 디렉터리의 그룹을 바꾼다
    [`uucp`](https://ko.wikipedia.org/wiki/uucp "wikilink") : 유닉스에서 유닉스로 복사
    [`scp`](https://ko.wikipedia.org/wiki/scp "wikilink") : [SSH로](../Page/시큐어_셸.md "wikilink") 안전하게 복사(secure copy)

## 참고

  -

  -

[분류:표준 유닉스 프로그램](https://ko.wikipedia.org/wiki/분류:표준_유닉스_프로그램 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink") [분류:파일 복사 유틸리티](https://ko.wikipedia.org/wiki/분류:파일_복사_유틸리티 "wikilink")