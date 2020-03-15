> This article is converted from Wikipedia: [ PAM](https://ko.wikipedia.org/wiki/_PAM).


**Linux Pluggable Authentication Modules** (PAM), 즉 리눅스 PAM은 리눅스 또는 [GNU/kFreeBSD](https://ko.wikipedia.org/wiki/GNU/kFreeBSD "wikilink") 시스템에서 애플리케이션과 서비스에 대한 동적 인증을 제공한다.\[1\]

리눅스-PAM은 인증 작업을 4가지 독립적인 관리 그룹으로 분리한다.

  - 계정 모듈(account module)들은 명시된 계정이 현재 조건에서 유효한 인증 목표인지를 검사한다. 이것은 계정 유효기간, 시간 그리고 사용자가 요청된 서비스에 접근 가능한지 같은 조건을 포함한다.
  - 인증 모듈(authentication module)들은 비밀번호를 요청하고 검사하는 것 같이 사용자의 신원을 확인한다. 또한 인증 정보를 [keyring](https://ko.wikipedia.org/wiki/keyring "wikilink") 같은 다른 시스템들에 전달한다.
  - 비밀번호 모듈(password module)들은 비밀번호 갱신을 책임진다. 또한 강력한 비밀번호 강화에도 사용된다.
  - 세션 모듈(session module)들은 세션 시작과 끝에 수행되는 행동을 정의한다. 그 후 사용자는 성공적으로 인증된다.

## 같이 보기

  - [OpenPAM](../Page/OpenPAM.md "wikilink")
  - [fprint](https://ko.wikipedia.org/wiki/fprint "wikilink")

## 각주

## 외부 링크

  - [Linux-PAM page](http://www.linux-pam.org/)
  - [pam.d(8) - Linux man page](http://linux.die.net/man/8/pam.d)
  - [Development site for the Linux-PAM project](https://fedorahosted.org/linux-pam/)
  - [*Understanding PAM*, by A.P. Lawrence](http://aplawrence.com/Basics/understandingpam.html)

[분류:리눅스 커널 특징](https://ko.wikipedia.org/wiki/분류:리눅스_커널_특징 "wikilink")

1.  <https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=220980>