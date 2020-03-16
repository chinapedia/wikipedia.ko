> This article is converted from Wikipedia: [Cd \(\)](https://ko.wikipedia.org/wiki/Cd_\(\)).


**`cd`** 또는 **`chdir`**은 디렉터리 변경(**ch**ange **dir**ectory)의 준말이며, [유닉스](../Page/유닉스.md "wikilink"), [윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink"), [도스](../Page/도스.md "wikilink")와 같은 운영체제에서 현재의 [작업 디렉터리의](https://ko.wikipedia.org/wiki/작업_디렉터리 "wikilink") 위치를 바꾸는 [명령 줄이다](../Page/명령_줄_인터페이스.md "wikilink"). 유닉스 [셸 스크립트와](../Page/셸_스크립트.md "wikilink") 윈도, 도스의 [배치 파일에서](../Page/배치_파일.md "wikilink") 모두 사용할 수 있다.

[framed|right| 유닉스 계통 시스템의 파일 시스템의 사용자 보기는 \~로 축약되는 홈 디렉터리로 시작한다. 여기서, 트리는 더 많은 하부 디렉터리와 파일로 뻗어나갈 수 있다.](https://ko.wikipedia.org/wiki/파일:chdir_example.png "wikilink")

## 사용법

[디렉터리](https://ko.wikipedia.org/wiki/디렉터리 "wikilink")는 파일을 관리하는 데 쓰이는 [파일 시스템의](../Page/파일_시스템.md "wikilink") 논리적인 부분이다. 디렉터리는 또한 다른 디렉터리를 가지고 있을 수 있다. `cd` 명령어는 하위 디렉터리로 변경되는 데 사용될 수 있고, 부모 디렉터리로 돌아갈 수도 있으며, 완전히 루트 디렉터리 (유닉스의 경우 /, 도스의 경우 \\)로 이동할 수 있다.

text.txt라는 파일과 세 개의 하부 디렉터리를 가진 사용자의 홈 디렉터리("\~"로 표시되는)를 보여 주는 유닉스 파일 시스템의 하부 섹션이 있다고 하자(오른쪽 위 그림 참조).

사용자의 현재 작업 디렉터리가 홈 디렉터리("\~")인 경우, "`cd games`"에 이어 명령어 "`ls`"를 입력하면 다음과 같은 메시지를 만들어 낸다:

`  me@host:~$ `**[`ls`](https://ko.wikipedia.org/wiki/ls_\(유닉스\) "wikilink")**
`  workreports games encyclopedia text.txt`
`  me@host:~$ `**`cd``   ``games`**
`  me@host:~/games$`

사용자는 이제 "games" 디렉터리에 있게 된다.

도스에서 비슷한 세션이 있으며(버전에 따라 홈 디렉터리의 개념이 적용되지 않을 수도 있지만) 다음과 같다.:

`  C:\> `**[`dir`](https://ko.wikipedia.org/wiki/dir_\(명령어\) "wikilink")**
`  workreports        `

<DIR>

Wed Oct 9th 9:01

`  games              `

<DIR>

Tue Oct 8th 14:32

`  encyclopedia       `

<DIR>

Mon Oct 1st 10:05

`  text        txt           1903 Thu Oct10th  12:43`
`  C:\> `**`cd``   ``games`**
`  C:\games>`

## 옵션

### 유닉스에서의 옵션

유닉스의 버전에 따라 아래의 옵션이 달라질 수 있다.

  - \-p
  - 출력에서 -l, '\~', 또는, '\~name'
  - \-n
  - \-v

### 도스에서의 옵션

도스의 버전에 따라 아래의 옵션이 달라질 수 있다.

  - CD .. : 상위 디렉터리로 이동한다.
  - CD \\ : 루트 디렉터리로 이동한다.
  - /D : 드라이브까지 변경된다.

## 동작 방식

`cd`는 [명령 줄 인터프리터를](https://ko.wikipedia.org/wiki/명령_줄_인터프리터 "wikilink") 통해 만들어진 명령어이다. 명령 줄 인터프리터는 이를테면 대부분의 [유닉스 셸](../Page/유닉스_셸.md "wikilink")([본 셸](../Page/본_셸.md "wikilink"), [tsch](https://ko.wikipedia.org/wiki/tsch "wikilink"), [배시](https://ko.wikipedia.org/wiki/배시 "wikilink") 등), 윈도의 [cmd.exe](https://ko.wikipedia.org/wiki/cmd.exe "wikilink") 및 [윈도 파워 셸](https://ko.wikipedia.org/wiki/윈도_파워_셸 "wikilink"), 도스의 [COMMAND.COM](../Page/COMMAND.COM.md "wikilink")를 들 수 있다.

## 참조

  -

  -

[분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink") [분류:윈도우 명령어](https://ko.wikipedia.org/wiki/분류:윈도우_명령어 "wikilink") [분류:내부 도스 명령어](https://ko.wikipedia.org/wiki/분류:내부_도스_명령어 "wikilink") [분류:디렉토리](https://ko.wikipedia.org/wiki/분류:디렉토리 "wikilink") [분류:윈도우 관리](https://ko.wikipedia.org/wiki/분류:윈도우_관리 "wikilink")