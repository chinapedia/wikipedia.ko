> This article is converted from Wikipedia: [Rmdir](https://ko.wikipedia.org/wiki/Rmdir).


**`rmdir`**(혹은 **`rd`**)는 [유닉스](../Page/유닉스.md "wikilink"), [도스](../Page/도스.md "wikilink"), [OS/2](https://ko.wikipedia.org/wiki/OS/2 "wikilink")나 [마이크로소프트 윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink")\[1\] 등의 운영 체제에서 빈 디렉터리를 제거하는 명령어이다. [유닉스](../Page/유닉스.md "wikilink")에서는 대문자로 쓸 수 없지만 DOS와 OS/2 운영 체제에서는 이러한 제한 조건이 적용되지 않는다.

## 사용법

일반적으로 가장 단순하게는 아래와 같이 사용될 수 있다:

`   rmdir 디렉터리_이름`

위와 같은 형식으로 입력하며, 디렉터리_이름 대신에 삭제하고자 하는 디렉터리의 이름을 입력하면 된다.

이 명령어에 대해 유닉스에서는 -p와 같은 옵션도 존재한다. 이 옵션은 상위 디렉터리 역시 비어 있을 경우 상위 디렉터리도 함께 삭제하는 옵션이다. 예를 들어:

`   rmdir -p foo/bar/baz`

라고 입력하면 baz/가 먼저 삭제되고, 다음 bar/ 그리고 마지막으로 foo/가 삭제됨으로써 명령어에서 지정한 모든 디렉터리 트리가 전체적으로 삭제된다.

유닉스 운영 체제에서 제공되는 `rmdir` 명령어는 디렉터리가 비어 있지 않은 이상 그 디렉터리를 삭제할 수 없다. 디렉터리와 디렉터리의 모든 내용을 함께 삭제하는 방법은 `rm` 명령어를 아래와 같이 사용하는 것이다:

`   rm -r foo/bar/baz`

도스에서는 이 명령어와 같은 기능을 수행하기 위해 `deltree`라는 명령어를 사용하며 윈도에서는 `rd /s directory_name` 를 사용한다.

## 참고 자료

  -

  -

  - [`rmdir`](http://www.linuxmanpages.com/man1/rmdir.1.php) - The program's [manpage](https://ko.wikipedia.org/wiki/manpage "wikilink")

## 각주

## 외부 링크

  - [Microsoft TechNet Rmdir article](https://web.archive.org/web/20081102172123/http://technet.microsoft.com/en-us/library/cc754993.aspx)

[분류:윈도우 명령어](https://ko.wikipedia.org/wiki/분류:윈도우_명령어 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink") [분류:유닉스 파일 시스템 관련 소프트웨어](https://ko.wikipedia.org/wiki/분류:유닉스_파일_시스템_관련_소프트웨어 "wikilink") [분류:내부 도스 명령어](https://ko.wikipedia.org/wiki/분류:내부_도스_명령어 "wikilink") [분류:윈도우 관리](https://ko.wikipedia.org/wiki/분류:윈도우_관리 "wikilink")

1.  [Microsoft TechNet Rmdir article](https://technet.microsoft.com/en-us/library/cc754993.aspx)