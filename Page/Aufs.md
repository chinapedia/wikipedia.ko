> This article is converted from Wikipedia: [Aufs](https://ko.wikipedia.org/wiki/Aufs).


**aufs** (**advanced multi-layered unification filesystem**)는 [리눅스](../Page/리눅스.md "wikilink") [파일 시스템을](../Page/파일_시스템.md "wikilink") 위한 [유니언 마운트를](https://ko.wikipedia.org/wiki/유니언_마운트 "wikilink") 구현한다. 이 이름은 원래 버전 2까지 **AnotherUnionFS**를 의미하였다.

2006년에 [Junjiro Okajima에](https://ko.wikipedia.org/wiki/Junjiro_Okajima "wikilink") 의해 개발된\[1\] aufs는 초기의 [UnionFS](https://ko.wikipedia.org/wiki/UnionFS "wikilink")를 완전히 재작성한 것이다. 신뢰성과 성능 개선을 목표로 하였으나 writable branch balancing,\[2\] 및 기타 개선사항과 같은 일부 새로운 개념들도 도입하였으며, 이 중 일부는 현재 UnionFS 2.x 브랜치에 구현되어 있다.

aufs는 주류 리눅스로의 통합이 거부되었다. 코드는 빽빽하고 읽기 어려우며 주석이 안 되어 있다는 이유로 비평을 받았다.\[3\] 그 대신 [OverlayFS](https://ko.wikipedia.org/wiki/OverlayFS "wikilink")가 리눅스 커널에 통합되었다.\[4\]\[5\] 개발자는 aufs를 주류 커널에 통합하려고 수차례 시도하다 끝내 포기하였다.\[6\]

## 이용

Aufs는 [데비안](../Page/데비안.md "wikilink") "jessie"와 [우분투](../Page/우분투_\(운영_체제\).md "wikilink") 16.04에 별도로 포함되어 있다. 데비안의 "stretch"는 aufs를 더 이상 포함하지 않지만 [델](../Page/델.md "wikilink")의 [dkms를](https://ko.wikipedia.org/wiki/동적_커널_모듈_지원 "wikilink") 사용하여 aufs 커널 모듈을 자동으로 컴파일하는 aufs-dkms 패키지를 제공한다.

[도커는](../Page/도커_\(소프트웨어\).md "wikilink") 원래 컨테이너 파일시스템 계층을 위해 aufs를 사용하였다. 지원되는 스토리지 백엔드들 중 하나로 여전히 이용이 가능하다.

일부 [리눅스 배포판들은](../Page/리눅스_배포판.md "wikilink") UnionFS 대신 aufs를 채택하고 있는데, 이를테면 다음과 같다:

  - [크노픽스](../Page/크노픽스.md "wikilink") [라이브 CD](../Page/라이브_CD.md "wikilink") [리눅스 배포판](../Page/리눅스_배포판.md "wikilink") - 2006년 말 이후, "더 나은 안정성과 성능을 위해"\[7\]
  - [NimbleX](https://ko.wikipedia.org/wiki/NimbleX "wikilink") 버전 2008 이후. Linux-Live와 함께 동시에 전환됨
  - [Porteus](https://ko.wikipedia.org/wiki/Porteus "wikilink") LiveCD, 온전히 RAM에서 동작
  - [SLAX](../Page/SLAX.md "wikilink") (및 Linux-Live 스크립트) 버전 6 이후\[8\]
  - [잰드로스](../Page/잰드로스.md "wikilink") 리눅스 배포판, ASUS [Eee PC](https://ko.wikipedia.org/wiki/Eee_PC "wikilink") 모델 901에서 사용 가능
  - [우분투](../Page/우분투_\(운영_체제\).md "wikilink") 10.04 LTS Live CD
  - [데비안](../Page/데비안.md "wikilink") 6.0 라이브 미디어
  - [젠투 리눅스](../Page/젠투_리눅스.md "wikilink") LiveDVD 11.0\[9\]
  - [젠투 리눅스](../Page/젠투_리눅스.md "wikilink") LiveDVD 11.2\[10\]
  - [젠투 리눅스](../Page/젠투_리눅스.md "wikilink") LiveDVD 12.0\[11\]
  - [Salix Live](https://ko.wikipedia.org/wiki/Salix_OS "wikilink") 버전 13.1.1까지는 Linux-Live 스크립트를 통해, 버전 13.37부터는 SaLT를 통해
  - [퍼피 리눅스](../Page/퍼피_리눅스.md "wikilink") 버전은 종료 시 디스크에 변경사항을 저장함과 동시에 온전히 RAM에서 구동이 가능하다. 예; LiveCD로 동작하는 Slacko 5.3.3.

## 같이 보기

  - [OverlayFS](https://ko.wikipedia.org/wiki/OverlayFS "wikilink")
  - [파일 시스템](../Page/파일_시스템.md "wikilink")
  - [유니언 마운트](https://ko.wikipedia.org/wiki/유니언_마운트 "wikilink")(Union mount)
  - [UnionFS](https://ko.wikipedia.org/wiki/UnionFS "wikilink")
  - [Syslinux](https://ko.wikipedia.org/wiki/Syslinux "wikilink")

## 각주

## 외부 링크

  - [AuFS 프로젝트 홈페이지](http://aufs.sourceforge.net/)
  - [단순한 예제](http://bbs.archlinux.org/viewtopic.php?pid=314698)

[분류:유니언 파일 시스템](https://ko.wikipedia.org/wiki/분류:유니언_파일_시스템 "wikilink")

1.
2.  [Goals and new features of aufs in the project's homepage](http://aufs.sourceforge.net/)
3.
4.
5.
6.
7.
8.  [Linux Live scripts](http://www.linux-live.org/?changes)  use AUFS for better stability
9.
10.
11.