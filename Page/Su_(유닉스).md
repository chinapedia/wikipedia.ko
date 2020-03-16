> This article is converted from Wikipedia: [Su \(\)](https://ko.wikipedia.org/wiki/Su_\(\)).


**su**(*substitute user*\[1\] 의 줄임말)는 [유닉스](../Page/유닉스.md "wikilink") 명령을 로그아웃하지 않고 다른 사용자의 권한으로 [셸](../Page/셸.md "wikilink")을 실행하는 데 사용된다.일반적으로 관리 작업을 위해 다시 로그오프하지 않고 [사용자의](../Page/사용자_\(컴퓨팅\).md "wikilink") 권한을 [루트로](https://ko.wikipedia.org/wiki/슈퍼_사용자 "wikilink") 변경하는 데 사용된다. 같은 방법으로 다른 사용자로 전환하는 데 사용된다. [KDE](../Page/KDE.md "wikilink")와 [그놈](../Page/그놈.md "wikilink")과 같은 [데스크톱 환경은](../Page/데스크톱_환경.md "wikilink") 사용자가 이러한 액세스를 필요로 하는 명령들을 실행할 수 있도록 하기 위하여 비밀 번호를 입력할 수 있는 상자를 보여주는 프로그램들이 있다.

어떤 사용자의 권한으로 실행할지 정하지 않고 실행한 경우에는, 루트 사용자로 간주된다(`su root)`와 동일).

## 사용법

[명령줄](https://ko.wikipedia.org/wiki/명령줄 "wikilink")에서 실행하였을 때, su는 일반적으로 목적 사용자의 비밀 번호를 묻고, 제대로 입력되었다면, 해당 계정과 연관된 모든 파일에 대한 사용자 접근 권한을 부여한다.

``` console
john@localhost:~$ su
Password:
root@localhost:/home/john# exit
logout
john@localhost:~$
```

또한, 수퍼 사용자가 아닌 다른 사용자로 전환할 수 있다. 예를 들어 `su jane`.

``` console
john@localhost:~$ su jane
Password:
jane@localhost:/home/john$ exit
logout
john@localhost:~$
```

일반적으로 [관리자](https://ko.wikipedia.org/wiki/관리자 "wikilink")들은 [하이픈](https://ko.wikipedia.org/wiki/하이픈 "wikilink")을 붙여서 사용하는데,\[2\], 이는 로그인 셸을 시작하는 데 사용할 수 있다.이렇게 하여 사용자가 목적 사용자의 [사용자 환경을](https://ko.wikipedia.org/wiki/사용자_환경 "wikilink") 얻을 수 있다.

``` console
john@localhost:~$ su - jane
Password:
jane@localhost:~$
```

관련 명령인 [`sudo`](https://ko.wikipedia.org/wiki/sudo "wikilink")는 다른 사용자로 명령을 실행하지만, 어떤 사용자가 어떤 명령을 어떤 다른 사용자로 수행할 수 있는지에 대하여 제한(일반적으로 `/etc/sudoers`라는 설정 파일에 저장되어 있고 `visudo`등을 이용하면 편집할 수 있다.)할 수 있다.`su`와는 달리, `sudo`는 인증할 때 다른 사용자의 비밀 번호가 아닌, 자신의 비밀 번호로 인증한다(특정 호스트에 있는 특정 사용자에게 명령 수행을 위임할 때, 암호를 서로 공유하지 않고 할 수 있게 해 주고, 모든 무인 단말기의 위험을 방지함).

일부 [유닉스 계열](../Page/유닉스_계열.md "wikilink") 운영 체제에서는 *[wheel](https://ko.wikipedia.org/wiki/wheel "wikilink")* 그룹에 속해 있는 사용자들에게만 수퍼 사용자로 su할 수 있다.\[3\] 침입자가 그 그룹에 속해 있는 계정들 중에 하나를 침입할 수도 있기 때문에, 이러한 보안 문제를 완화하지 않을 수도 있다. 그러나 [GNU su는](https://ko.wikipedia.org/wiki/GNU_su "wikilink") wheel 그룹을 지원하지 않는다;이것은 철학적인 이유 때문이다.\[4\]

## 참조

## 외부 링크

  - [su](https://web.archive.org/web/20130807001725/http://www.gnu.org/software/coreutils/manual/html_node/su-invocation.html) - 매뉴얼 페이지 ([GNU](../Page/GNU.md "wikilink") [coreutils](https://ko.wikipedia.org/wiki/coreutils "wikilink"))
  - [su 명령](http://www.linfo.org/su.html) - 리눅스 정보 프로젝트 (LINFO)
  - [su의 정의](https://web.archive.org/web/20080611162545/http://dictionary.die.net/su) - dictionary.die.net
  - [runas](https://web.archive.org/web/20091211222740/http://www.microsoft.com/resources/documentation/windows/xp/all/proddocs/en-us/runas.mspx) - Windows XP에 있는 유사한 명령

[분류:유닉스 사용자 관리 및 지원 관련 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_사용자_관리_및_지원_관련_유틸리티 "wikilink") [분류:시스템 관리](https://ko.wikipedia.org/wiki/분류:시스템_관리 "wikilink")

1.
2.  `su -`로, `su - root`와 동일하다
3.
4.