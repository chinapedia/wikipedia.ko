> This article is converted from Wikipedia: [Fsck](https://ko.wikipedia.org/wiki/Fsck).


시스템 유틸리티 **fsck**(*file system consistency check*의 준말)는 [유닉스](../Page/유닉스.md "wikilink"), [유닉스 계열](../Page/유닉스_계열.md "wikilink") 운영 체제(예: [리눅스](../Page/리눅스.md "wikilink"), [macOS](https://ko.wikipedia.org/wiki/macOS "wikilink"), [FreeBSD](../Page/FreeBSD.md "wikilink"))의 [파일 시스템의](../Page/파일_시스템.md "wikilink") 무결성을 검사하기 위한 도구이다.\[1\] 비슷한 명령어인 [CHKDSK](../Page/CHKDSK.md "wikilink")는 [마이크로소프트 윈도우와](../Page/마이크로소프트_윈도우.md "wikilink") MS-DOS에 존재한다.

## 발음

발음에 대한 합의는 없다. "F-S-C-K", "F-S-check", "fizz-check", "F-sack", "fisk", "fizik", "F-sick", "F-sock", "F-sek", "feshk" "fsk", "fix", "farsk" 또는 "fusk"로 발음이 가능하다.\[2\]

## 사용

일반적으로 fsck는 부팅 시간에 자동으로 수행되거나 시스템 관리자에 의해 수동으로 수행될 수 있다. 이 명령어는 디스크에 저장된 데이터 구조에 대해 직접 동작하며 사용 중인 특정 파일 시스템에 내부적으로 특정하여 동작한다. 즉, 파일 시스템에 맞추어진 fsck 명령어는 일반적으로 필수적이다. 여러 fsck 구현체의 정확한 동작들은 다양할 수 있으나 이들은 일반적으로 통일된 순서의 내부 동작을 준수하며 통일된 명령 줄 인터페이스를 사용자에게 제공한다.

## 예제

다음의 예제는 /ur 파티션에 마운트되도록 구성된 파일 시스템을 검사한다. 파일 시스템은 먼저 언마운트 상태여야 한다:

``` bash
 fsck /usr
```

다음의 예는 mdadm 소프트웨어 [RAID](../Page/RAID.md "wikilink") 장치의 리눅스 [JFS](https://ko.wikipedia.org/wiki/JFS_\(파일_시스템\) "wikilink") 파일 시스템을 검사한다:

``` bash
 fsck -t jfs /dev/md0
```

## 같이 보기

  - [유닉스 명령어 목록](../Page/유닉스_명령어_목록.md "wikilink")
  - [파일 시스템 목록](../Page/파일_시스템_목록.md "wikilink")

## 각주

## 외부 링크

  - [man fsck](https://web.archive.org/web/20150529001726/http://www.manpagez.com/man/8/fsck/)
  - [Checking and Repairing File system with fsck](http://www.adminschoice.com/repairing-unix-file-system-fsck)
  - [Jargon File entry: fscking](http://www.catb.org/jargon/html/F/fscking.html)
  - [The many faces of fsck](http://lwn.net/Articles/248180)

[분류:파일 시스템](https://ko.wikipedia.org/wiki/분류:파일_시스템 "wikilink") [분류:유닉스 파일 시스템 관련 소프트웨어](https://ko.wikipedia.org/wiki/분류:유닉스_파일_시스템_관련_소프트웨어 "wikilink")

1.
2.