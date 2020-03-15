> This article is converted from Wikipedia: [GParted](https://ko.wikipedia.org/wiki/GParted).


**GParted**는 [디스크 파티션](https://ko.wikipedia.org/wiki/디스크_파티션 "wikilink") 편집 소프트웨어다. 글씨(텍스트)만으로 이루어져 있는 [GNU 파티드를](https://ko.wikipedia.org/wiki/GNU_파티드 "wikilink") [GTK+](https://ko.wikipedia.org/wiki/GTK+ "wikilink")를 통해 [GUI로](https://ko.wikipedia.org/wiki/그래픽_사용자_인터페이스 "wikilink") 구현한 소프트웨어로 libparted를 통해 디스크 장치를 찾아내고 분석하여 디스크 장치 안에 어떤 토막(파티션)들이 어떤 꼴로 있는지를 알아내며 토막을 만들거나, 지우거나, 크기를 바꾸거나, 옮기거나, 검사하거나, 베낄 수 있다.

[C++](https://ko.wikipedia.org/wiki/C++ "wikilink")로 쓰였으며 [GNU 일반 공중 사용 허가서를](https://ko.wikipedia.org/wiki/GNU_일반_공중_사용_허가서 "wikilink") 따른다.

## 지원하는 꼴(포맷)

|                                                            | 찾기 | 읽기  | 만들기 | 늘리기   | 줄이기   | 옮기기 | 베끼기 | 검사하기 | 이름표 |
| ---------------------------------------------------------- | -- | --- | --- | ----- | ----- | --- | --- | ---- | --- |
| [btrfs](https://ko.wikipedia.org/wiki/btrfs "wikilink")    | 예  | 아니오 | 아니오 | 아니오   | 아니오   | 아니오 | 아니오 | 아니오  | 아니오 |
| [ext2](https://ko.wikipedia.org/wiki/ext2 "wikilink")      | 예  | 예   | 예   | 예     | 예     | 예   | 예   | 예    | 예   |
| [ext3](https://ko.wikipedia.org/wiki/ext3 "wikilink")      | 예  | 예   | 예   | 예     | 예     | 예   | 예   | 예    | 예   |
| [ext4](https://ko.wikipedia.org/wiki/ext4 "wikilink")      | 예  | 예   | 예   | 예     | 예     | 예   | 예   | 예    | 예   |
| [ebr](https://ko.wikipedia.org/wiki/ebr "wikilink")        | 예  | 예   | 예   | 부분적으로 | 부분적으로 | 아니오 | 아니오 | 아니오  |     |
| [fat16](../Page/파일_할당_테이블.md "wikilink")                   | 예  | 예   | 예   | 예     | 예     | 예   | 예   | 예    | 예   |
| [fat32](../Page/파일_할당_테이블.md "wikilink")                   | 예  | 예   | 예   | 예     | 예     | 예   | 예   | 예    | 예   |
| [hfs](https://ko.wikipedia.org/wiki/HFS "wikilink")        | 예  | 예   | 예   | 아니오   | 예     | 예   | 예   | 아니오  | 아니오 |
| [hfs+](https://ko.wikipedia.org/wiki/HFS+ "wikilink")      | 예  | 예   | 예   | 아니오   | 예     | 예   | 예   | 예    | 아니오 |
| [jfs](https://ko.wikipedia.org/wiki/JFS "wikilink")        | 예  | 예   | 예   | 예     | 아니오   | 예   | 예   | 예    | 예   |
| [swap](https://ko.wikipedia.org/wiki/가상_메모리 "wikilink")    | 예  | 아니오 | 예   | 예     | 예     | 예   | 예   | 아니오  | 아니오 |
| [ntfs](https://ko.wikipedia.org/wiki/ntfs "wikilink")      | 예  | 예   | 예   | 예     | 예     | 예   | 예   | 예    | 예   |
| [reiser4](https://ko.wikipedia.org/wiki/라이저4 "wikilink")   | 예  | 예   | 예   | 아니오   | 아니오   | 예   | 예   | 예    | 아니오 |
| [reiserfs](https://ko.wikipedia.org/wiki/라이저FS "wikilink") | 예  | 예   | 예   | 예     | 예     | 예   | 예   | 예    | 예   |
| [ufs](../Page/유닉스_파일_시스템.md "wikilink")                    | 예  | 아니오 | 아니오 | 아니오   | 아니오   | 예   | 예   | 아니오  | 아니오 |
| [xfs](../Page/XFS.md "wikilink")                           | 예  | 예   | 예   | 예     | 부분적으로 | 예   | 예   | 예    | 예   |

## 함께 보기

  - [디스크 파티션](https://ko.wikipedia.org/wiki/디스크_파티션 "wikilink")
  - [GNU Parted](../Page/GNU_Parted.md "wikilink")
  - [Qt파티드](https://ko.wikipedia.org/wiki/Qt파티드 "wikilink") - [Qt판](https://ko.wikipedia.org/wiki/Qt_\(툴킷\) "wikilink") GNU 파티드

## 각주

## 외부 링크

  - [G파티드 공식 사이트](http://gparted.sourceforge.net/)

[분류:디스크 편집 소프트웨어](https://ko.wikipedia.org/wiki/분류:디스크_편집_소프트웨어 "wikilink") [분류:GNU GPL을 따르는 소프트웨어](https://ko.wikipedia.org/wiki/분류:GNU_GPL을_따르는_소프트웨어 "wikilink") [분류:C++로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C++로_작성된_자유_소프트웨어 "wikilink")