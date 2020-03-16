> This article is converted from Wikipedia: [Who \(\)](https://ko.wikipedia.org/wiki/Who_\(\)).


표준 [유닉스](../Page/유닉스.md "wikilink") 명령어 **`who`**는 현재 컴퓨터에 로그인 한 사용자 목록을 보여준다.

`who`명령어는, 유사한 정보를 제공해 주지만 추가적으로 데이터와 통계자료를 보여주는 명령어 [`w`](https://ko.wikipedia.org/wiki/w_\(유닉스\) "wikilink")와 관련되어 있다.

## 명세

단일 유닉스 명세서([SUS](../Page/단일_유닉스_규격.md "wikilink"))에서 `who`는 접근가능한 사용자들에 대한 정보를 보여주는 것으로 상술된다. [XSI](https://ko.wikipedia.org/wiki/X/Open_System_Interfaces_Extension "wikilink") extension은 또한 사용자명, 터미널, 로그인 시간, 프로세스 식별자, 터미널에서 이루어진 마지막 활동이후의 시간, 나아가, 사용자 정보로 사용되는 교체 시스템 데이터베이스에 대한 정보가 `who`에 옵션 인자(argument)로 지정될 수 있다고 상술한다.

`who`명령어는 현재의 터미널만에 대한 정보를 보기 위해 `am i` 또는 `am I` 인자와 함께 실행될 수 있다. (즉, `who am i` 또는 `am I`로 실행된다.) (이 실행과 같은 아래의 `-m`옵션을 보라. )

## 사용

extension없이 [SUS에서는](../Page/단일_유닉스_규격.md "wikilink") 오직 `-m`, `-T`, 그리고 `-u` 옵션만을 설명하고 있다. 나머지 다른 옵션들은 XSI extension에서 설명되고 있다.

  - `-a`: -b,-d,-l,-p,-r,-t,-T,-u와 함께 사용자 정보로 사용되는 시스템 데이터베이스를 처리한다.
    `-b`: 시스템이 마지막으로 재부팅된 때를 보여준다.
    `-d`: 좀비프로세스와 세부사항들을 보여준다.
    `-H`: 열(column)의 제목을 보여준다.
    `-l`: 사용자가 로그 인 할 수 있는 터미널을 보여준다.
    `-m`: 현재의 터미널만에 대한 정보를 보여준다.
    `-p`: 활성화된 프로세스를 보여준다.
    `-q`: 빠른 포맷, 로그인한 모든 사용자들의 수와 이름만을 보여준다. 다른 모든 옵션들을 무력화한다.
    `-r`: [init프로세스의](https://ko.wikipedia.org/wiki/init_\(Unix\) "wikilink") 활동수준을 보여준다.
    `-s`: (default) 이름과 터미널, 시간 사항들만을 보여준다.
    `-t`: 시스템 시계가 마지막으로 바뀐 때를 보여준다.
    `-T`: 표준형식에서 각 터미널의 세부사항을 보여준다. (예시 부분을 참고하라.)
    `-u`: 유휴시간을 보여준다. XSI는 로그인한 사용자들을 보여주고 그 터미널이 최근에 사용되었는지 여부에 대한 정보를 보여준다.

다른 유닉스와 [유닉스 계열](../Page/유닉스_계열.md "wikilink") 운영 체제는 추가 옵션을 가지고 있을 수 있다. [GNU](../Page/GNU.md "wikilink") `who`는 등록된 사용자가 메시지를 받았는지 여부를 보여주는 `-u`와 `-w`옵션과 유사함을 지닌 `-i`옵션을 포함한다. ((SUS는 `-T`옵션이 실행될때 이것을 보여준다.), 그러나 [GNU](../Page/GNU.md "wikilink") `who`와 [BSD](../Page/BSD.md "wikilink") `who` 둘다 다수의 위 옵션들(`-a`, `-b`, `-d`, 나머지들)을 허용한다.; 대신 [GNU](../Page/GNU.md "wikilink") `who`는 등록된 hostname상의 DNS lookup들을 실행하기 위해 `-l`옵션을 사용한다.

## 출력

Extension 없는 [SUS는](../Page/단일_유닉스_규격.md "wikilink") 출력형식은 완성형 정의이어야 한다고 설명한다. XSI extension은 한가지 형식을 설명한다. 그러나 완전히 특정화되지 않은 것을 언급한다. 구획문자와 필드 길이들은 정확히 설명되어 있지 않다. 그래서 출력형식은 유닉스 실행사이에서 상당히 다르다.

## 참고

  - [유닉스 프로그램 목록](https://ko.wikipedia.org/wiki/유닉스_프로그램_목록 "wikilink")

## 매뉴얼 페이지

  - [`who`](http://www.gnu.org/software/coreutils/manual/html_node/who-invocation.html) — [GNU](../Page/GNU.md "wikilink") [coreutils](https://ko.wikipedia.org/wiki/coreutils "wikilink")의 매뉴얼

  -

  -

  -

[분류:유닉스 사용자 관리 및 지원 관련 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_사용자_관리_및_지원_관련_유틸리티 "wikilink") [분류:표준 유닉스 프로그램](https://ko.wikipedia.org/wiki/분류:표준_유닉스_프로그램 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink")