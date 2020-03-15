> This article is converted from Wikipedia: [Chmod](https://ko.wikipedia.org/wiki/Chmod).


**`chmod`**(**ch**ange **mode**의 축약어)명령어는 [유닉스](https://ko.wikipedia.org/wiki/유닉스 "wikilink")와 [유닉스 계통](https://ko.wikipedia.org/wiki/유닉스_계통 "wikilink") 환경 안에서 쓰이는 [셸](../Page/유닉스_셸.md "wikilink") 명령어이다. 이 명령어는 [파일들이나](https://ko.wikipedia.org/wiki/컴퓨터_파일 "wikilink") [디렉터리](https://ko.wikipedia.org/wiki/디렉터리 "wikilink")의 파일 시스템 모드들을 바꾼다. 그 모드들은 [허가](../Page/허가.md "wikilink")나 특별한 모드들을 포함한다.

## 역사

`chmod` 명령어는 [AT\&T](https://ko.wikipedia.org/wiki/AT&T "wikilink") [유닉스](https://ko.wikipedia.org/wiki/유닉스 "wikilink") 버전 1에서 최초로 등장했고, 오늘날에도 여전히 유닉스 계통의 기계에서 사용된다.

## 사용법

`chmod` 명령어 옵션들은 다음과 같이 지정된다:

`$ chmod [`*`options`*`] `*`mode`*`[,`*`mode`*`] `*`file1`*` [`*`file2`*` ...]`

현재 어떤 허가들이 있는지 보기 위해서는 다음과 같이 입력한다:

`$ ls -l `*`file`*

## 옵션

`chmod` 명령어는 행동에 영향을 미치는, 수많은 명령어 옵션들을 가진다. 가장 일반적인 옵션들은 다음과 같다:

  - `-R`: [재귀](https://ko.wikipedia.org/wiki/재귀 "wikilink")적으로 파일들과 디렉터리들의 모드들을 바꾼다.

<!-- end list -->

  - `-v`: 자세한 모드; 실행되고 있는 모든 파일을 나열한다.

## 문자열 모드

`chmod` 유틸리티에 대해서는, 모든 허가들과 특수한 모드들은 모드 매개변수에 의해서 표현된다. 파일들이나 디렉터리들의 모드를 조절하기 위한 하나의 방법은 기호적인 모드를 지정하는 것이다. 이 기호적인 모드는 세 가지 구성요소로 구성되며, 그것들은 단순한 문자열을 구성하기 위해서 결합된다:

`$ chmod [`*`references`*`][`*`operator`*`][`*`modes`*`] `*`file1`*` ...`

레퍼런스들 (혹은 클래스들)은 허가가 적용되는 사용자들을 구분하기 위해서 사용된다. 만약 어떠한 레퍼런스들도 그것이 "모든 것"에 대해 기본값으로 지정하지 않았다면, 그것들은 다음 아래에 있는 문자들 중 하나 혹은 몇 개로 표현된다:

| 레퍼런스 | 클래스    | 설명                             |
| ---- | ------ | ------------------------------ |
| `u`  | 사용자    | 파일의 소유자                        |
| `g`  | 그룹     | 그 파일의 그룹 멤버인 사용자               |
| `o`  | 다른 사람들 | 그 파일의 소유자나 혹은 그 그룹의 멤버가 아닌 사용자 |
| `a`  | 모든 사람  | 위의 셋 모두, "ugo"와 같다             |

`chmod` 프로그램은 파일의 모드들이 어떻게 조정될 수 있는지를 명시하기 위해서 연산자를 사용한다. 허용되는 연산자는 다음과 같다:

| 연산자 | 설명                                       |
| --- | ---------------------------------------- |
| `+` | 지정된 모드들은 지정된 클래스들에 더한다                   |
| `-` | 지정된 클래스들로부터 지정된 모드들은 지운다                 |
| `=` | 지정된 클래스들을 위해서 지정된 모드들이 정확한 모드들로 만들어지게 된다 |

그 모드들은 어떤 허가들이 인정될 것인지 혹은 지정된 클래스들로부터 삭제될 것인지를 지정한다. 기본적인 허가들과 일치하는 세가지 기본적인 모드들이 있다:

<table>
<thead>
<tr class="header">
<th><p>모드</p></th>
<th><p>이름</p></th>
<th><p>설명</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><code>r</code></p></td>
<td><p>읽기 (read)</p></td>
<td><p>파일을 읽거나 디렉터리 안 내용물의 리스트를 보여준다</p></td>
</tr>
<tr class="even">
<td><p><code>w</code></p></td>
<td><p>쓰기 (write)</p></td>
<td><p>파일이나 디렉터리에 쓴다</p></td>
</tr>
<tr class="odd">
<td><p><code>x</code></p></td>
<td><p>실행하기 (excute)</p></td>
<td><p>파일을 실행하거나 디렉터리 트리로 되돌아간다</p></td>
</tr>
<tr class="even">
<td><p><code>X</code></p></td>
<td><p>특별한 실행하기 (special excute)</p></td>
<td><p>이는 그 자체를 허가라고 보기보다는 <code>x</code> 대신에 사용될 수 있는 것으로 보아야 한다. 이 명령어는 디렉터리들의 현재 허가 상태와 관계없이 실행 허가를 디렉터리들에 적용하거나, (사용자, 그룹이나 다른 사람들에게) 벌써 최소한 한번의 실행 허가가 설정된 적이 있는 파일에 실행 허가를 적용한다. 이 명령어는 '+'와 함께 사용되는 경우와 일반적인 파일들 (텍스트 파일들과 같이)에서는 실행 허가를 설정하지 않고 큰 디렉터리 트리에 그룹이나 다른 사람들이 접근할 수 있게 해주는 <code>-R</code> 옵션과 결합하여 사용될 경우, 이 두 경우에만 유용하다. 두 번째 경우는 "<code>chmod -R a+rx</code>"를 막 사용한 경우에 주로 발생하며, "<code>chmod -R a+rx</code>" 대신 '<code>X</code>'을 사용함으로써 같은 일을 할 수 있다.</p></td>
</tr>
<tr class="odd">
<td><p><code>s</code></p></td>
<td><p>셋유이드(setuid)<br />
/ 기드(gid)</p></td>
<td><p>상세 설명은 <a href="https://ko.wikipedia.org/wiki/#특별한_모드들" title="wikilink">특별한 모드들 섹션에</a> 있다</p></td>
</tr>
<tr class="even">
<td><p><code>t</code></p></td>
<td><p>스티키(sticky)</p></td>
<td><p>상세 설명은 <a href="https://ko.wikipedia.org/wiki/#특별한_모드들" title="wikilink">특별한 모드들 섹션에</a> 있다</p></td>
</tr>
</tbody>
</table>

이 세 가지 구성요소의 조합은 `chmod` 명령어에 의해 인식되는 문자열을 만든다. 쉼표로 다양한 기호적 모드들을 분리하므로 다양한 변화들을 지정할 수 있다.

### 문자열 모드들의 예제

예를 들어, 밑에 따라오는 명령어는 `sample`라는 이름의 파일 혹은 디렉터리의 사용자나 그룹 크래스들에게 쓰기나 읽기 허가들을 추가해 주는 데 사용된다:

`$ `**`chmod``   ``ug+rw``   ``sample`**
`$ ls -ld sample`
`drw-rw----   2 unixguy  unixguy       96 Dec  8 12:53 sample`

이 명령어는 모든 허가들을 지움으로써 어떠한 사람도 `sample`이라는 이름의 파일을 실행시키거나 읽거나 쓰게 허용하지 않는다.

`$ `**`chmod``   ``a-rwx``   ``sample`**
`$ ls -l sample`
`----------   2 unixguy  unixguy       96 Dec  8 12:53 sample`

아래의 명령어는 `sample` 파일에 대해서 사용자나 그룹의 읽기와 실행 기능만의 (쓰기 기능은 포함되지 않는다) 허가들을 변화시킨다.

`Sample file permissions before command`
`$ ls -ld sample`
`drw-rw----   2 unixguy  unixguy       96 Dec  8 12:53 sample`
`$ `**`chmod``   ``ug=rx``   ``sample`**
`$ ls -ld sample`
`dr-xr-x---   2 unixguy  unixguy       96 Dec  8 12:53 sample`

## 8진법 숫자들

`chmod` 명령어는 모드들을 나타내는 세 자리 혹은 네 자리 8진수도 받아들인다. 더 많은 정보를 원한다면 위에서 언급한 조항들을 보라. `sample`이라는 이름의 파일이나 디렉터리의 모드들을 설정하기 위해서 네 자리 8진수를 사용하는 것은 다음과 같다:

`$ chmod 0664 sample`

`setuid`, `setgid` 그리고 `sticky` 비트들이 설정되어 있지 않다면 이는 다음과 같다:

`$ chmod 664 sample`

이거나

`$ chmod +r,-x,ug+w sample`

만약 허가에 대한 문제가 생길 경우, 그 문제를 해결하기 위해서 단순히 모든 보안들을 꺼버리는 `chmod 777`를 사용해서는 안된다.

## 특별한 모드들

`chmod` 명령어는 파일이나 디렉터리의 특별한 모드들이나 추가적인 허가들 역시 바꿀 수 있다. 그 기호적인 모드들은 *[setuid](https://ko.wikipedia.org/wiki/setuid "wikilink")* 나 *[setgid](https://ko.wikipedia.org/wiki/setgid "wikilink")* 모드들을 나타내기 위해서 `s`를 사용하고, *[sticky](https://ko.wikipedia.org/wiki/sticky_bit "wikilink")* 모드를 나타내기 위해서 `t`를 사용한다. 이 모드들은 다른 클래스들이 지정되었지는 아닌지와 관계없이 적절한 클래스들에게만 적용될 수 있다. 대부분의 운영 시스템들은 8진법 모드들을 사용하여 특별한 모드들을 지정하는 것을 보조하고 있지만 어떤 운영체제들은 그렇지 않다. 이러한 시스템들에서는 오직 기호적인 모드들만 사용될 수 있다.

## 예제들

| 명령                                              | 설명                                                                                                                    |
| ----------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| <code>chmod +r *file*                           | 모두에 대해 읽기를 추가한다                                                                                                       |
| <code>chmod -x *file*                           | 모두에 대해 실행 허가를 제거한다                                                                                                    |
| <code>chmod u=rw,go= *file*                     | 파일의 읽기와 쓰기를 그 파일의 소유자에게만 설정하고 그룹이나 다른 사람들에게 설정된 모든 허가를 지운다                                                            |
| <code>chmod +rw *file*                          | 모두가 읽고 쓸 수 있도록 *file*이라는 파일의 허가들을 바꾼다                                                                                 |
| <code>chmod -R u+w,go-w docs/                   | 사용자에게는 쓰기를 추가하고 다른 모든 사람들에게는 쓰기를 제거하기 위해서 *docs*라는 디렉터리와 그 안의 모든 내용물에 대한 허가들을 바꾼다.                                    |
| <code>chmod 0 *file*                            | 모두의 모든 허가를 지운다                                                                                                        |
| <code>chmod 666 *file*                          | 그 사용자, 그 그룹이나 다른 모든 이에 대해서 쓰기나 읽기 권한을 설정한다                                                                            |
| <code>chmod 0755 *file*                         | `u=rwx (4+2+1)나 go=rx (4+1 & 4+1)`와 같다. `0`는 *어떤 특별한 모드들도* 지정하지 않는다.                                                  |
| <code>chmod 4755 *file*                         | `4`은 *[사용자 ID 설정](https://ko.wikipedia.org/wiki/setuid "wikilink")*을 지정하고 나머지는 u=rwx (4+2+1)나 go=rx (4+1 & 4+1)와 동일하다 |
| <code>find path/ -type d -exec chmod a-x {} \\; | path/부터 시작하는 트리 안에 있는 모든 디렉터리들 (파일들의 목록은 볼 수 없다)의 실행 허가를 제거한다(파일들을 일치시키기 위해서 오직‘-type f'을 사용한다).                      |
| <code>find path/ -type d -exec chmod a+x {} \\; | 만약 삼바(Samba) 쓰기에 대한 허가들을 재설정한 경우에 모든 사용자들에 대해서 디렉터리 열람을(예를 들어 ls) 허용한다.                                               |
| <code>chmod -R u+rwX,g-rwx,o-rwx *directory*    | 소유자 디렉터리에 대한 rwx(읽기, 쓰기, 실행)을, 소유자 파일들에 대해서는 rw(읽기, 쓰기)를, 그룹이나 다른 이들에 대해서는 ---를 설정하기 위해서 디렉터리 트리를 설정한다.               |
| <code>chmod -R a-x+X *directory*                | 디렉터리 트리 안에 있는 모든 파일들에 대한 실행 허가를 제거한다. 반면 디렉터리 열람은 허용한다.                                                               |

## 함께 보기

  - [파일 시스템 권한](../Page/파일_시스템_권한.md "wikilink")
  - [`chown`](https://ko.wikipedia.org/wiki/chown "wikilink"): 유닉스 계통 시스템에서 파일이나 디렉터리의 소유권을 바꾸기 위해서 사용되는 명령어
  - [`chgrp`](https://ko.wikipedia.org/wiki/chgrp "wikilink"): 유닉스 계통 시스템에서 파일이나 디렉터리의 그룹을 바꾸기 위해서 사용되는 명령어
  - [`cacls`](https://ko.wikipedia.org/wiki/cacls "wikilink"): [윈도 NT나](https://ko.wikipedia.org/wiki/윈도_NT "wikilink") 그것의 모방 제품들에서 사용되는 명령어로 파일이나 디렉터리와 관련된 권한 통제 리스트들을 조정한다.
  - [사용자 ID](https://ko.wikipedia.org/wiki/사용자_식별자_\(유닉스\) "wikilink")
  - [그룹 ID](https://ko.wikipedia.org/wiki/그룹_식별자_\(유닉스\) "wikilink")
  - [유닉스 명령어 목록](../Page/유닉스_명령어_목록.md "wikilink")

## 외부 링크

  -

  -

  - [`chmod`](http://www.gnu.org/software/coreutils/manual/html_node/chmod-invocation.html) — [GNU](https://ko.wikipedia.org/wiki/GNU "wikilink") [coreutils](https://ko.wikipedia.org/wiki/coreutils "wikilink")로부터의 매뉴얼 페이지.

  - [GNU "Setting Permissions" manual](http://www.gnu.org/software/coreutils/manual/html_node/Setting-Permissions.html)

  - [Solaris 9 chmod man page](https://web.archive.org/web/20100926051106/http://docs.sun.com/app/docs/doc/817-0689/6mgfkpckn?q=chmod&a=view)

  - [Mac OS X chmod man page](http://www.hmug.org/man/1/chmod.php), 이 또한 [접근 제어 목록들을](../Page/접근_제어_목록.md "wikilink") 보조한다.

  - [CHMOD-Win 3.0](http://neosmart.net/dl.php?id=4) — Freeware Windows' ACL ←→ CHMOD converter.

  - [What CHMOD? File Permissions Calculator](https://web.archive.org/web/20051201140107/http://www.classical-webdesigns.co.uk/resources/whatchmod.html), web-based CHMOD calculator.

  - [Beginners tutorial with on-line "live" example](http://catcode.com/teachmod/index.html)

[분류:운영 체제 보안](https://ko.wikipedia.org/wiki/분류:운영_체제_보안 "wikilink") [분류:표준 유닉스 프로그램](https://ko.wikipedia.org/wiki/분류:표준_유닉스_프로그램 "wikilink") [분류:유닉스 파일 시스템 관련 소프트웨어](https://ko.wikipedia.org/wiki/분류:유닉스_파일_시스템_관련_소프트웨어 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink")