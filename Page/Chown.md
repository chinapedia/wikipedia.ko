> This article is converted from Wikipedia: [Chown](https://ko.wikipedia.org/wiki/Chown).


**`chown`** 명령어는 [유닉스 계통](https://ko.wikipedia.org/wiki/유닉스_계통 "wikilink") 시스템에서 파일의 소유권을 바꾸기 위해서(<u>ch</u>ange the <u>own</u>er of a file) 사용된다. 대부분의 경우, 이것은 오직 [슈퍼 사용자만이](https://ko.wikipedia.org/wiki/슈퍼_사용자 "wikilink") 실행할 수 있다. 그들이 소유하고 있는 파일의 그룹을 바꾸고 싶어하는 [권한](https://ko.wikipedia.org/wiki/권한 "wikilink")이 없는 (일반적인) 사용자들은 [`chgrp`](https://ko.wikipedia.org/wiki/chgrp "wikilink")을 사용해야 한다.

## 사용법

`chown` 명령어에 대한 일반적인 구성은 다음과 같다:

`chown [-R] [`*`user`*`][:`*`group`*`] `*`target1`*` [`*`target2`*` ..]`

  - 선택적인 *`user`* 변수는 target들의 소유권을 가질 수 있는 새로운 사용자들을 표시한다.
  - 선택적인 *`group`* 변수(이는 반드시 콜론 `:`을 접두사로 가진다)는 target들이 관련되어 있는 그룹을 표시한다.
  - *`target`* 변수들은 사용자나 그룹들이 바뀔 수 있는 파일들이나 디렉터리들을 표시한다.
  - 폭넓게 적용되는 옵션인 `-R`은 명명되는 모든 target 디렉터리와 그 안에 들어 있는 파일들에 대해서 순환적인 변화를 지정한다.

### 참고 사항

  - *`user`* 이나 *`group`* 중 하나는 반드시 지정되어야 한다. `chown` 명령어는 적어도 그런 변수들 중 하나라도 없는 경우에는 올바르게 실행되지 않는다.
  - *`user`* 그리고 *`group`* 변수들은 상징적인 이름이나 식별자(즉, [사용자 ID이거나](https://ko.wikipedia.org/wiki/사용자_ID "wikilink") [그룹 ID](https://ko.wikipedia.org/wiki/그룹_ID "wikilink"))가 될 수 있다.

## 사용 예시들

다음 명령어들은 반드시 루트 권한으로 실행되어야 함에 주의해야 한다.

`$ chown root /var/run/httpd.pid`

`/var/run/httpd.pid`의 소유권을 'root'(슈퍼 사용자를 위한 표준 이름)으로 바꾸기.

`$ chown rob:developers strace.log`

`strace.log`의 소유권을 'rob'으로, 그리고 그룹 식별자를 'developers'로 바꾸기

`$ chown nobody:nobody /tmp /var/tmp`

`/tmp` 와 `/var/tmp`의 소유권을 ‘[nobody](https://ko.wikipedia.org/wiki/nobody_\(username\) "wikilink")’으로 바꾸기(좋은 생각은 아님) 같은 타겟들과 연관된 그룹들을 그룹 'nobody'(전통적으로 'nobody' 사용자의 그룹)로 바꾸기

`$ chown :512 /home`

`/home` 의 그룹 식별자를 512 (그룹 이름이 식별자 512로 연관이 있든지 없든지 간에)로 바꾸기

`$ chown -R us base`

`base`의 소유권을 사용자 `us`로 바꾸고 이것을 순환적으로 만든다(`-R`).

## 함께 보기

  - [chmod](https://ko.wikipedia.org/wiki/chmod "wikilink")
  - [chgrp](https://ko.wikipedia.org/wiki/chgrp "wikilink")

## 외부 링크

  -

  -

  - [chown manual page](https://web.archive.org/web/20170623021906/http://nersp.nerdc.ufl.edu/~dicke3/nerspcs/chown.html)

  - [The chown Command](http://www.linfo.org/chown.html) by The Linux Information Project (LINFO)

[분류:운영 체제 보안](https://ko.wikipedia.org/wiki/분류:운영_체제_보안 "wikilink") [분류:표준 유닉스 프로그램](https://ko.wikipedia.org/wiki/분류:표준_유닉스_프로그램 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink")