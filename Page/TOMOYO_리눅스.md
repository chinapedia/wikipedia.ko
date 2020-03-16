> This article is converted from Wikipedia: [TOMOYO ](https://ko.wikipedia.org/wiki/TOMOYO_).


**TOMOYO 리눅스**는 [강제적 접근 통제](https://ko.wikipedia.org/wiki/강제적_접근_통제 "wikilink")(MAC)를 구현한 [리눅스 커널](../Page/리눅스_커널.md "wikilink") [보안 모듈이다](../Page/리눅스_보안_모듈.md "wikilink").

## 개요

유명한 만화 캐릭터의 이름을 딴 TOMOYO는 [리눅스](../Page/리눅스.md "wikilink")를 위한 [MAC](https://ko.wikipedia.org/wiki/강제적_접근_통제 "wikilink") 구현이며 시스템의 보안을 향상시키는 것 외에도 순수한 [시스템 분석](https://ko.wikipedia.org/wiki/시스템_분석 "wikilink") 툴로도 유용하게 사용될 수 있다. 이것은 2003년 5월에 출시되었으며 2012년 5월까지 [NTT 데이터가](../Page/NTT_데이터.md "wikilink") 후원하였다.\[1\]

TOMOYO 리눅스는 시스템의 행위에 초점을 맞춘다. TOMOYO 리눅스는 각 프로세스들이 자신의 목적을 달성하기 위해 필요한 행위와 자원을 선언하게 한다. 보호가 활성화되면 TOMOYO 리눅스는 관리자에 의해 허용된 행위와 자원으로 각 프로세스를 제한한다.

## 기능

TOMOYO 리눅스의 주요한 기능들은 다음과 같다:

  - 시스템 분석
  - 강제적 접근 통제를 통한 보안 향상
  - 자동 정책 생성
  - 간단한 문법
  - 쉬운 사용법

## 역사와 버전

TOMOYO는 리눅스 버전 2.6.30(2009년 6월 10일)부터 [리눅스 커널에](../Page/리눅스_커널.md "wikilink") 포함되었다.\[2\] 이것은 [SELinux](../Page/보안_강화_리눅스.md "wikilink"), [AppArmor](../Page/AppArmor.md "wikilink") 그리고 [SMACK과](../Page/Smack_\(소프트웨어\).md "wikilink") 함께, 4가지 표준 [LSM](../Page/리눅스_보안_모듈.md "wikilink") 모듈의 중 하나이다.

TOMOYO 리눅스 프로젝트는 리눅스 커널에 MAC을 제공하기 위한 패치로부터 출발하였다. TOMOYO 리눅스를 주류 리눅스 커널에 포팅하려면 리눅스 보안 모듈(LSM)에 대한 훅(hooks)들\[3\]이 요구된다. 리눅스 보안 모듈은 특별히 SELinux와 이것의 *라벨 기반* 접근을 위해 설계되고 개발되었다.

그러나 TOMOYO 리눅스의 MAC 기능을 통합하기 위해서는 더 많은 훅(hooks)들이 필요하다. 따라서 이 프로젝트는 두 개의 병행되는 개발이 있다:

## 같이 보기

  - [강제적 접근 통제](https://ko.wikipedia.org/wiki/강제적_접근_통제 "wikilink") (MAC)
  - [SELinux](../Page/보안_강화_리눅스.md "wikilink")
  - [AppArmor](../Page/AppArmor.md "wikilink")

## 각주

## 외부 링크

  - [Comparison chart of 1.x and 2.x](http://tomoyo.osdn.jp/comparison.html.en)
  - [Comparison chart of TOMOYO 1.x, 2.x, and AKARI](http://akari.osdn.jp/comparison.html.en)
  - [TOMOYO Linux project](http://tomoyo.osdn.jp/index.html.en)
  - [TOMOYO Linux](https://web.archive.org/web/20161129021550/http://elinux.org/TOMOYO_Linux) at [Embedded Linux Wiki](https://web.archive.org/web/20010410205134/http://www.elinux.org/)
  - [LWN : TOMOYO Linux and pathname-based security](https://web.archive.org/web/20190723194605/https://lwn.net/Articles/277833/)
  - [Tomoyo – Debian Wiki](https://web.archive.org/web/20170727144446/https://wiki.debian.org/Tomoyo)
  - [TOMOYO Linux – ArchWiki](https://web.archive.org/web/20170110234734/https://wiki.archlinux.org/index.php/TOMOYO_Linux)

[분류:리눅스 커널 특징](https://ko.wikipedia.org/wiki/분류:리눅스_커널_특징 "wikilink") [분류:리눅스 보안 소프트웨어](https://ko.wikipedia.org/wiki/분류:리눅스_보안_소프트웨어 "wikilink") [분류:NTT 그룹](https://ko.wikipedia.org/wiki/분류:NTT_그룹 "wikilink")

1.
2.
3.