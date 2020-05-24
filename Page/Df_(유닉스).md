> This article is converted from Wikipedia: [Df \(유닉스\)](https://ko.wikipedia.org/wiki/Df_\(유닉스\)).


****(***d**isk **f**ree*의 준말)는 이 명령을 호출을 하는 사용자가 적절한 읽기 접근 권한이 있는 [파일 시스템에](../Page/파일_시스템.md "wikilink") 대해 사용 가능한 디스크 공간의 양을 표시하기 위해 사용되는 표준 [유닉스](../Page/유닉스.md "wikilink") 명령어이다. 는 일반적으로 [statfs](https://ko.wikipedia.org/wiki/statfs "wikilink") 또는 statvfs 시스템 호출을 사용하여 구현된다.

## 역사

는 버전 1 [AT\&T UNIX에](https://ko.wikipedia.org/wiki/AT&T_UNIX "wikilink") 처음 등장하였다. [GNU](../Page/GNU.md "wikilink") [coreutils에](../Page/GNU_코어_유틸리티.md "wikilink") 기본 포함된 버전은 Torbjorn Granlund, David MacKenzie, Paul Eggert에 의해 작성되었다.\[1\]

## 사용법

의 [단일 유닉스 규격](../Page/단일_유닉스_규격.md "wikilink")(SUS) 사양은 다음과 같다:

`df [-k] [-P|-t] [-del] [file...]`

  -
    공간 수치를 작성할 때 기본값인 512바이트 단위 대신 1024바이트 단위를 사용한다
  -
    표준의 이식 가능한 출력 포맷을 사용한다
  -
    [XSI를](https://ko.wikipedia.org/wiki/X/Open_System_Interfaces_Extension "wikilink") 준수하여 할당 공간도 표시한다
  -
    KB, MB 또는 GB로 표시한다
  -
    지정된 파일을 포함하는 파일 시스템의 여유 공간의 양을 작성한다

대부분의 [유닉스](../Page/유닉스.md "wikilink"), [유닉스 계열](../Page/유닉스_계열.md "wikilink") 운영 체제는 추가 옵션들을 추가한다. [BSD](../Page/BSD.md "wikilink"), [GNU 코어 유틸리티](../Page/GNU_코어_유틸리티.md "wikilink") 버전들은 를 포함하여, 이는 사람이 읽기 쉬운 포맷으로 여유 공간을 나열해준다. 추가로 포함되는 는 [아이노드](../Page/아이노드.md "wikilink") 사용률을 나열하고 는 로컬 파일시스템으로 표시를 제한시킨다. [GNU](../Page/GNU.md "wikilink") 는 파일시스템 타입 정보를 나열하는 도 포함하고 있으나 는 기본적으로 1K 블록의 크기를 표시한다.

## 예제

다음은 df 명령의 출력 예시이다.

``` console
$ df
Filesystem    1024-blocks      Free %Used    Iused %Iused Mounted on
/dev/hd4            32768     16016   52%     2271    14% /
/dev/hd2          4587520   1889420   59%    37791     4% /usr
/dev/hd9var         65536     12032   82%      518     4% /var
/dev/hd3           819200    637832   23%     1829     1% /tmp
/dev/hd1           524288    395848   25%      421     1% /home
/proc                   -         -    -         -     -  /proc
/dev/hd10opt        65536     26004   61%      654     4% /opt
```

## 같이 보기

  - [유닉스 명령어 목록](../Page/유닉스_명령어_목록.md "wikilink")
  - [Du (유닉스)](../Page/Du_\(유닉스\).md "wikilink")

## 각주

## 외부 링크

  -
### 매뉴얼 페이지

  - [df](https://www.gnu.org/software/coreutils/manual/html_node/df-invocation.html) — manual page from [GNU](../Page/GNU.md "wikilink") [GNU 코어 유틸리티](../Page/GNU_코어_유틸리티.md "wikilink")

  -
  - [The df Command](http://www.linfo.org/df.html) – by The Linux Information Project (LINFO)

[분류:표준 유닉스 프로그램](https://ko.wikipedia.org/wiki/분류:표준_유닉스_프로그램 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink")

1.  <https://linux.die.net/man/1/df>