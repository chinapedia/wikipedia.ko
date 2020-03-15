> This article is converted from Wikipedia: [Sudo](https://ko.wikipedia.org/wiki/Sudo).


**sudo** 명령어는 [유닉스](https://ko.wikipedia.org/wiki/유닉스 "wikilink") 및 [유닉스 계열](../Page/유닉스_계열.md "wikilink") [운영 체제에서](https://ko.wikipedia.org/wiki/운영_체제 "wikilink"), 다른 사용자의 보안 권한, 보통 [슈퍼유저](https://ko.wikipedia.org/wiki/슈퍼유저 "wikilink")로서 프로그램을 구동할 수 있도록 하는 [프로그램](https://ko.wikipedia.org/wiki/프로그램 "wikilink")이다. 명칭은 본래 슈퍼유저로서의 실행에 사용되던 것에서 “superuser do”에서 유래하였으나, 후에 프로그램의 기능이 확장되며 “substitute user do”(다른 사용자의 권한으로 실행)의 줄임말로 해석되게 되었다. 기본적으로 Sudo는 사용자 비밀번호를 요구하지만 루트 비밀번호(root password)가 필요할 수도 있고, 한 터미널에 한번만 입력하고 그 다음부터는 비밀번호가 필요 없다.\[1\] Sudo는 각 명령줄에 사용할 수 있으며 일부 상황에서는 관리자 권한을 위한 슈퍼유저 로그인(superuser login)을 완벽히 대신하며, 주로 [우분투](https://ko.wikipedia.org/wiki/우분투 "wikilink"), [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink")와 [애플의](https://ko.wikipedia.org/wiki/애플_\(기업\) "wikilink") [OS X](https://ko.wikipedia.org/wiki/OS_X "wikilink") 에서 볼 수 있다.\[2\]\[3\]

## 역사

Robert Coggeshall과 Cliff Spencer는 1980년 즈음 [SUNY/버펄로의](../Page/버펄로_대학교.md "wikilink") 컴퓨터 과학부에서 오리지널 하위 시스템을 작성했다.\[4\] Robert Coggeshall은 sudo를 [콜로라도 볼더 대학교로](https://ko.wikipedia.org/wiki/콜로라도_볼더_대학교 "wikilink") 가져왔다. 1986년부터 1993년까지 코드와 기능은 콜로라도 볼더 대학교 컴퓨터 과학부, College of Engineering and Applied Science의 IT 직원들(Todd C. Miller 등)에 의해 실질적으로 수정되었다.\[5\] 현재 버전은 1994년 이후로 [OpenBSD](https://ko.wikipedia.org/wiki/OpenBSD "wikilink")의 개발자 Todd C. Miller가 공개적으로 유지보수하고 있으며,\[6\] 1999년 이후로 [SC-스타일](https://ko.wikipedia.org/wiki/ISC_라이선스 "wikilink") 라이선스로 배포되고 있다.\[7\]

2009년에 [MS가](https://ko.wikipedia.org/wiki/마이크로소프트 "wikilink") sudo 명령어를 특허로 등록했다는 것이 밝혀져 큰 파장을 일으켰으나\[8\], 그 청구항들은 sudo의 개념이라기보다는 특정한 [GUI에](https://ko.wikipedia.org/wiki/그래픽_사용자_인터페이스 "wikilink") 대해 좁게 고안된 것이었다\[9\].

## 예제

sudo 명령어를 실행하기 전에, 사용자들은 비밀번호를 입력한다. 한 번 승인되고 만약 /etc/sudoers 설정 파일이 그 유저를 승인한다면, 명령은 실행된다. kdesu, kdesudo, gksu, gksudo와 같이 GUI 환경에서 사용할 수 있는 몇몇 명령어 들이 있다.\[10\] 다음은 접근이 거부된 예이다.

``` console
snorri@rimu:~$ sudo emacs /etc/resolv.conf

We assume you have received the usual lecture from the local System
Administrator. It usually boils down to these three things:

1) Respect the privacy of others.
2) Think before you type.
3) With great power comes great responsibility.

Password:
snorri is not in the sudoers file. This incident will be reported.
```

아래의 로그는 실패한 시도와, snorri를 /etc/sudoers에 추가한 뒤에 성공한 시도이다.

``` console
snorri@rimu:~$ sudo tail /var/log/auth.log
Aug 5 06:00:28 localhost sudo: snorri : user NOT in sudoers ; TTY=pts/1 ; PWD =/home/snorri ; USER=root ; COMMAND=/usr/bin/emacs /etc/resolv.conf
Aug 5 06:01:15 localhost su[15573]: (pam_unix) session opened for user root by snorri(uid=1000)
Aug 5 06:02:09 localhost sudo: snorri : TTY=pts/1 ; PWD=/home/snorri ; USER=root ; COMMAND=/usr/bin/emacs /etc/resolv.conf
Aug 5 06:02:49 localhost sudo: snorri : TTY=pts/1 ; PWD=/home/snorri ; USER=root ; COMMAND=/usr/bin/tail /var/log/auth.log
```

## runas, su, 그리고 sudo

윈도는 [runas](https://ko.wikipedia.org/wiki/runas "wikilink")라고 불리는 명령어를 가지고 있다. 이것의 기능은 비슷하나, runas도 아니고 [사용자 계정 컨트롤](../Page/사용자_계정_컨트롤.md "wikilink")(UAC)도 아닌 것이 sudo이다. - 그들은 권한을 추가하기 보다는 다른 사용자를 가장한다.

runas와 su:

  - 권한이 부여된 유저가 그들 고유의 글을 이용하여 높은 권한의 프로세스를 실행하는 것을 허락치 않는다.
  - 사용자의 프로파일과 객체의 소유권을 보존하지 않는다.

runas명령어는 sudo가 아니라 유닉스의 su와 더 동등하다. sudo가 su에 비해 더 우수한 이유는 su는 사용자의 고유 신분에 기반해 권한이동을 엑세스 하고, 가장 중요한 것은 sudo는 비밀번호 공유가 필요 없기 때문이다. runas나 su를 특권 계정을 엑세스하기 위해 사용하는 것은 관리자-가능 계정의 비밀번호를 유포하는것이 필요하기 때문에, sudo에는 없는 보안상의 약점을 가지고 있다.

## RBAC

[SELinux](https://ko.wikipedia.org/wiki/SELinux "wikilink")와 함께 사용하면, sudo는 [역할 기반 접근 제어](../Page/역할_기반_접근_제어.md "wikilink")(RBC)의 역할 전환을 위해 사용할 수 있다.\[11\]

## 도구 및 유사 프로그램

  - visudo - `/etc/sudoers`파일을 수정하여 사용하는 vi 기반 프로그램.

## 각주

## 외부 링크

  - [공식 홈페이지](http://www.sudo.ws/)

  - [rootsh](http://sourceforge.net/projects/rootsh) 와 [sudosh](http://sourceforge.net/projects/sudosh/)

  - [*Sudo Fun*](http://rixstep.com/2/20070201,00.shtml) - OS X에서 sudo를 사용하는 법에 대한 가이드

  - (한글) [리눅스 root와 sudo 명령어 접두사 개념과 사용법](https://swiftcoding.org/remind-of-cli-commands)

[분류:보안 소프트웨어](https://ko.wikipedia.org/wiki/분류:보안_소프트웨어 "wikilink") [분류:유닉스 사용자 관리 및 지원 관련 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_사용자_관리_및_지원_관련_유틸리티 "wikilink") [분류:시스템 관리](https://ko.wikipedia.org/wiki/분류:시스템_관리 "wikilink")

1.
2.  [RootSudo - Community Ubuntu Documentation](https://help.ubuntu.com/community/RootSudo)
3.  [MacDevCenter.com - Top Ten Mac OS X Tips for Unix Geeks](http://www.macdevcenter.com/pub/a/mac/2002/10/22/macforunix.html)
4.
5.
6.
7.
8.
9.  <http://blog.seattlepi.com/microsoft/2009/11/12/did-microsoft-just-sneakily-patent-an-open-source-tool/>
10. [Introduction to Authorization Services Programming Guide](http://developer.apple.com/mac/library/documentation/Security/Conceptual/authorization_concepts/01introduction/introduction.html)
11.