> This article is converted from Wikipedia: [Deb \(파일 형식\)](https://ko.wikipedia.org/wiki/Deb_\(파일_형식\)).


**.deb**은 [데비안](../Page/데비안.md "wikilink")의 [소프트웨어 패키지](https://ko.wikipedia.org/wiki/소프트웨어_패키지 "wikilink") 포맷의 확장자이며 데비안 소프트웨어 포맷의 [바이너리 패키지에서](https://ko.wikipedia.org/wiki/바이너리_파일 "wikilink") 가장 자주 사용되는 파일 이름이다.

## 디자인

[섬네일](https://ko.wikipedia.org/wiki/파일:Gdebi.png "wikilink")

데비안 패키지는 두 개의 [Tar](../Page/Tar_\(파일_포맷\).md "wikilink") 보존, 혹은 선택적으로 [Gzip](../Page/Gzip.md "wikilink") (zlib), [Bzip2](../Page/Bzip2.md "wikilink"), [Izma](https://ko.wikipedia.org/wiki/Izma "wikilink"), [xz](https://ko.wikipedia.org/wiki/xz "wikilink") (Izma2) 를 사용하는 표준 [유닉스](../Page/유닉스.md "wikilink") ar 보존을 사용하는데, 이 형식들은 통제 정보와 프로그램 데이터에 관한 내용을 포함한다.

허용되는 프로그램은 [Dpkg](../Page/Dpkg.md "wikilink")인데, 대부분 [APT](../Page/어드밴스트_패키징_툴.md "wikilink") 혹은 [앱티튜드](../Page/앱티튜드.md "wikilink"), 우분투 소프트웨어 센터, 시냅틱, 혹은 GDebi를 사용한다.

데비안 패키지는 에일리언 소프트웨어를 이용해 다른 패키지 형식으로 전환될 수 있으며, [체크인스톨](https://ko.wikipedia.org/wiki/체크인스톨 "wikilink")과 데비안 패키지 매니저를 이용해 소스 코드로부터 생성할 수 있다.

몇몇 코어 데비안 패키지는 **udeb** 형식 ("마이크로 debs")으로 존재하며, 일반적으로 데비안 설치판의 부트스트랩용으로만 사용된다. 이러한 파일들이 *udeb* 확장자를 사용하지만, 일반적인 *deb* 파일의 구조 정의를 따른다. 그러나, *deb*와는 다르게, *udeb*는 작동에 필요한 파일들만을 포함하고 있다.\[1\] 특히, 문서화 파일들은 일반적으로 생략된다. *udeb* 패키지는 일반적인 데비안 시스템에서 설치할 수 없다.

## 적용

데비안 버전 0.93 이후부터, deb 파일은 ar 보존 형식으로 적용되었다. [캐노니컬](../Page/캐노니컬.md "wikilink")의 아카이브 형식 적용은 다음과 같다:

  - `debian-binary`: deb 포맷의 버전. 현재 데비안 버전에서 "2.0"임.
  - `control.tar`, `control.tar.gz` or `control.tar.xz`: 모든 패키지의 메타정보. dpkg에게 패키지 설치를 어떻게 할 지 알려줌
  - `data.tar`, `data.tar.gz`, `data.tar.bz2`, `data.tar.lzma` or `data.tar.xz`: 실제 설치 파일.

`debian-binary` 파일은 보존의 초입 부분에 있어야 하며, 그렇지 않으면 데비안 패키지로 인식되지 않음.

## 적용

데비안 패키지는 데비안 기반의 GNU/리눅스 배포판 ([우분투](../Page/우분투_\(운영_체제\).md "wikilink") 등)에서 동작한다. 기본 설치 프로그램은 [dpkg](https://ko.wikipedia.org/wiki/dpkg "wikilink")이다.

## 출처

[분류:아카이브 포맷](https://ko.wikipedia.org/wiki/분류:아카이브_포맷 "wikilink") [분류:Dpkg](https://ko.wikipedia.org/wiki/분류:Dpkg "wikilink") [분류:파일 확장자](https://ko.wikipedia.org/wiki/분류:파일_확장자 "wikilink") [분류:우분투 (운영 체제)](https://ko.wikipedia.org/wiki/분류:우분투_\(운영_체제\) "wikilink") [분류:데비안](https://ko.wikipedia.org/wiki/분류:데비안 "wikilink")

1.