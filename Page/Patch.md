> This article is converted from Wikipedia: [Patch](https://ko.wikipedia.org/wiki/Patch).


**patch** 컴퓨터 도구는 패치 파일로 불리는 별도의 [파일](https://ko.wikipedia.org/wiki/파일 "wikilink")에 포함된 지시에 따라 텍스트 파일을 업데이트하는 [유닉스](../Page/유닉스.md "wikilink") [프로그램이다](../Page/컴퓨터_프로그램.md "wikilink"). 이 패치 파일은 줄여서 간단히 패치라고도 하며, 일련의 차이를 구성하고 있는 텍스트 파일인데 이 파일은 원래의 파일과 업데이트된 파일을 변수로 받아 관련 [diff](https://ko.wikipedia.org/wiki/diff "wikilink") 프로그램을 실행하여 만들어진다. patch로 파일을 업데이트하는 일을 "패치를 적용한다"고 표현한다.

## 역사

최초의 patch 프로그램은 [펄](../Page/펄.md "wikilink") 프로그래밍 언어를 창시한 [래리 월이](../Page/래리_월.md "wikilink") 작성하여 `mod.sources`\[1\](나중의 comp.source.unix)에 1985년 5월에 게시한 것이다. 프로그램 변종들 중 하나\[2\]\[3\]\[4\]는 [GNU 프로젝트의](../Page/GNU_프로젝트.md "wikilink") 일부로서 [FSF에](../Page/자유_소프트웨어_재단.md "wikilink") 의해 유지보수되고 있다.

## 사용 예

셸에 다음의 명령을 입력하면 패치를 만들 수 있다:

``` bash
  $ diff -u oldFile newFile > mods.diff  # -u는 통일(unified) 포맷으로 출력함을 의미
```

패치를 적용하려면 다음의 명령을 셸에 입력한다:

``` bash
  $ patch < mods.diff
```

위의 명령은 patch가 `mods.diff`에 기술된 지정 파일로 변경 사항을 적용하게 한다. 하위 디렉터리에 위치한 파일들에 대한 패치들은 추가적인 `-p`<small>`숫자`</small> 옵션을 요구하며, 여기에서 `숫자`는 소스 트리의 기본 디렉터리가 diff에 위치해 있으면 1이고, 그렇지 않으면 0으로 지정한다.

'`-R`' 옵션을 사용하면 적용된 패치를 되돌릴 수 있다:

``` bash
  $ patch -R < mods.diff
```

파일이 diff 생성 시의 버전과 유사하지 않으면 패치는 깨끗하게 적용되지 않을 수 있다. 이를테면 텍스트의 줄들이 처음에 삽입된 경우 해당 패치에서 가리키는 줄 번호를 정확하지 않을 수 있다. patch는 주변의 줄들을 찾아서 패치가 적용될 텍스트를 재할당하는 방법으로 이러한 상황을 모면할 수 있다. 이 경우 **fuzz**로 기술된다.

## 같이 보기

  - [패치 (컴퓨팅)](../Page/패치_\(컴퓨팅\).md "wikilink")
  - [diff](https://ko.wikipedia.org/wiki/diff "wikilink")

## 각주

## 외부 링크

  - [소스 코드](http://ftp.gnu.org/gnu/patch/)

  -
  - [GNU tools for Win32](http://gnuwin32.sourceforge.net/) - Win32 port of tools, including diff and patch

  - [diffstat](https://web.archive.org/web/20151211201038/http://invisible-island.net/diffstat/) - show statistics from output of diff

[분류:1984년 소프트웨어](https://ko.wikipedia.org/wiki/분류:1984년_소프트웨어 "wikilink") [분류:패치 유틸리티](https://ko.wikipedia.org/wiki/분류:패치_유틸리티 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink")

1.
2.  <http://cvsweb.openbsd.org/cgi-bin/cvsweb/src/usr.bin/patch/>  OpenBSD patch source
3.  <https://sourceforge.net/projects/schilytools/files/> A version of patch exists in the Schily tools collection
4.  A version of patch is maintained by IBM, Oracle and the Open Software Foundation