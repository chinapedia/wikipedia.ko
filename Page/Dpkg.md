> This article is converted from Wikipedia: [Dpkg](https://ko.wikipedia.org/wiki/Dpkg).


**dpkg**는 [데비안](../Page/데비안.md "wikilink") [패키지 관리 시스템의](https://ko.wikipedia.org/wiki/패키지_관리_시스템 "wikilink") 기초가 되는 [소프트웨어](../Page/소프트웨어.md "wikilink")이다. `dpkg` 명령어가 [.deb](https://ko.wikipedia.org/wiki/deb_\(파일_형식\) "wikilink") 패키지의 설치, 삭제, 정보 제공을 위해 사용된다.

`dpkg` 그 자체는 저레벨의 도구이며, [APT와](../Page/어드밴스트_패키징_툴.md "wikilink") 같은 고급 도구들이 복잡한 패키지 관계와 패키지를 원격에서 받아오는 등의 일을 한다. 앱티튜드 (Aptitude), 시냅틱 (Synaptic) 등이 `dpkg` 자체보다 많이 쓰이는데, 패키지 의존성을 다루는 더 많은 방법과 더 이해하기 편한 인터페이스를 갖고 있기 때문이다.

데비안 패키지 "dpkg"는 `dpkg` 프로그램과 더불어 패키징 시스템이 작동하게 하는 `dpkg-statoverride`, `dpkg-divert`, `dpkg-trigger` and `update-alternatives` 외의 몇몇 프로그램을 설치한다.\[1\] dpkg는 `start-stop-daemon`, `install-info`와 같은 프로그램을 설치하며, `install-info`는 일반적으로 하위 호환성을 위해 남겨진다.\[2\] (현재는 별도로 개발, 배포된다.) 데비안 패키지 "dpkg-dev"는 아래에 설명된 다양한 도구들을 포함하고 있다.

## 역사

dpkg는 원래 맷 웰쉬, 카를 스트리터와 이안 머독에 의해 [펄](../Page/펄.md "wikilink") 프로그램으로써\[3\] 개발되었으며 1994년에 대부분이 이안 잭슨에 의해 [C로](https://ko.wikipedia.org/wiki/C_\(프로그래밍_언어 "wikilink") 다시 쓰여졌다.\[4\]\[5\] **dpkg**라는 이름은 "데비안 패키지(Debian package)"의 약자였으나, 이 프로그램이 .deb 패키지 포맷의 시초였던 만큼, 데비안 패키지가 작동하는 방식이 변경하는 만큼 새롭게 변경되고 있다.

## 사용 예시

.deb 패키지를 설치하기 위해서는 다음 명령어를 실행하면 된다:

`dpkg -i `*`deb파일명`*

*deb파일명*(.deb)은 데비안 파일 이름으로 대체하면 된다.

설치된 패키지의 목록은 다음 명령어로 볼 수 있다:

`dpkg -l `*`[부가``   ``명령어]`*`  `

  -
    한편 설치된 패키지를 확인하기위해서는 dpkg - l 해당파일.deb 를 사용한다.

설치된 패키지를 삭제하기 위해서는 다음 명령어를 실행한다:

`dpkg -r `*`패키지명`*

## 개발 도구

dpkg-dev 는 데비안 소스 패키지의 언팩, 빌드, 업로드를 위해 필요한 개발 도구들의 모음을 포함한다.\[6\] 다음 프로그램을 포함한다:

  - **dpkg-source**는 데비안 패키지의 소스를 팩/언팩한다.
  - **dpkg-gencontrl**은 언팩된 데비안 트리 소스에서 정보를 읽고 바이너리 패키지 컨트롤 패키지를 생성하며 Debian/files에 항목을 생성한다.
  - **dpkg-shlibdeps**는 라이브러리에 필요한 의존성을 계산한다.
  - **dpkg-buildpackage**는 언팩된 데비안 트리 소스에서 정보를 읽고 구성된 컨트롤 파일 (.changes)를 생성한다.
  - **dpkg-distaddfile**은 debian/files에 파일을 추가한다.
  - **dpkg-parserchangelog**는 언팩된 데비안 트리 소스에서 바뀜 기록(changelog) 파일을 읽고 바뀐 내용에 대해 빠르게 준비된 결과물을 생성한다.

## 더 보기

  - [어드밴스트 패키징 툴](../Page/어드밴스트_패키징_툴.md "wikilink")
  - [에일리언 (소프트웨어)](https://ko.wikipedia.org/wiki/에일리언_\(소프트웨어\) "wikilink")
  - [데비안 빌드 툴체인](https://ko.wikipedia.org/wiki/데비안_빌드_툴체인 "wikilink")
  - dpkg 는 [RPM과](../Page/RPM_패키지_매니저.md "wikilink") 비슷한 역할을 수행한다.
  - [opkg](https://ko.wikipedia.org/wiki/opkg "wikilink")는 dpkg에서 영향을 받은 저장소가 부자연스러운 리눅스 배포판을 위한 패키지 관리 시스템이다.
  - [wpkg](https://ko.wikipedia.org/wiki/wpkg "wikilink")는 마이크로소프트 윈도 운영 체제를 위한 dpkg의 클론이다.

## 각주

## 외부 링크

  - [Debian's dpkg package](http://wiki.debian.org/Teams/Dpkg)
  - [Debian dpkg mailing list](http://lists.debian.org/debian-dpkg/)
  - [dpkg(8)](http://manpages.debian.net/cgi-bin/man.cgi?query=dpkg) 매뉴얼 페이지
  - [General Origin handling](http://www.hadrons.org/~guillem/debian/docs/origin.proposal).

[Dpkg](https://ko.wikipedia.org/wiki/분류:Dpkg "wikilink") [분류:데비안](https://ko.wikipedia.org/wiki/분류:데비안 "wikilink") [분류:C로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C로_작성된_자유_소프트웨어 "wikilink")

1.
2.
3.
4.
5.
6.