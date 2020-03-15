> This article is converted from Wikipedia: [JFFS2](https://ko.wikipedia.org/wiki/JFFS2).


**저널링 플래시 파일 시스템 버전 2**( 흔히들 **JFFS2**라고 한다.)는 [플래시 메모리](../Page/플래시_메모리.md "wikilink") 장치에 쓰이는 [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink") [로그 구조 파일 시스템이다](https://ko.wikipedia.org/wiki/로그_구조_파일_시스템 "wikilink"). 이전 버전으로는 [JFFS](../Page/JFFS.md "wikilink")가 있다.

JFFS2는 [리눅스 커널](../Page/리눅스_커널.md "wikilink") 2.4.10 릴리즈부터 리눅스 커널에 포함되었다. JFFS는 [오픈 펌웨어](../Page/오픈_펌웨어.md "wikilink"), [eCOS](https://ko.wikipedia.org/wiki/eCOS "wikilink") RTOS, [레드부터](https://ko.wikipedia.org/wiki/레드부터 "wikilink") 부트로더 등에서도 사용할 수 있다.

후속 버전으로, [LogFS](https://ko.wikipedia.org/wiki/LogFS "wikilink")라는 파일 시스템은 JFFS2를 대체할 목적으로 다수의 개발자들이 개발하고 있다. LogFS는 JFFS2보다 더 큰 용량의 장치들을 적용 대상으로 하고 있다.

## 특징

JFFS2에는 다음과 같은 점이 새로워졌다.

  - [NAND 플래시 메모리](../Page/플래시_메모리.md "wikilink") 장치에 대한 지원이 추가되었다. 일반적인 NAND 장치는 순차적 입출력 인터페이스를 통해 동작한다. 또한 읽기 동작을 메모리-맵트(memory-mapped) 방식으로 할 수 없다. 그러므로, NAND 플래시 메모리 장치를 위한 JFFS2를 개발하는 데에는 많은 노력이 필요하였다.
  - 하드 링크(Hard links) 온-디스크 포맷 때문에 JFFS에서는 불가능하였다.
  - 압축. [zlib](https://ko.wikipedia.org/wiki/zlib "wikilink"), rubin, rtime의 세 종류의 압축 알고리즘을 사용할 수 있다.
  - 성능 향상. JFFS는 디스크를 순수한 원형 로그(circular log)로 간주하였다. 이 때문에 불필요한 I/O가 꽤 많이 발생하였다. JFFS2의 [쓰레기 수집](../Page/쓰레기_수집_\(컴퓨터_과학\).md "wikilink") [알고리즘](https://ko.wikipedia.org/wiki/알고리즘 "wikilink")은 이러한 I/O 빈도를 꽤 많이 줄여준다.

## 설계

JFFS에서와 마찬가지로, JFFS2에서는 파일이나 디렉터리에 대한 변경 사항은 일종의 "로그"로서 "노드"에 기록된다. "노드"에는 다음 두 가지 종류가 있다.

  - [아이노드](../Page/아이노드.md "wikilink")(inodes): 파일 메타데이터를 내용으로 하는 헤더 및 그 뒤에 붙는 파일 데이터 페이로드로 구성된다. 압축된 페이로드는 한 페이지(page)로 크기가 제한된다.
  - 디렉터리 엔트리 노드(dirent nodes): 이름 및 inode 번호를 담고 있는 디렉터리 엔트리들로 구성된다. 하드 링크는 같은 inode 번호를 갖고 있는 다른 이름의 디렉터리 엔트리로 표현된다. Inode 번호 0번은 unlink를 표현한다.

JFFS에서와 마찬가지로, 노드는 처음에 생성될 때 "유효"(valid) 상태로 시작한다. 노드들은 처음에는 "유효"(valid) 상태로 시작했다가 나중에 그 노드의 새로운 버전이 장치 내 어디선가 생성되면 "쓸모없음"(obsolete) 상태가 된다.

하지만, JFFS에서와는 달리, JFFS2에는 순환 로그(circular log)가 없다. 대신, JFFS는. 플래시 장치의 지우기 동작의 세그먼트의 크기와 같은 크기의 "블록"(block)들을 활용한다. 블록들은 한 번에 한 블록씩 채워진다. "깨끗한"(clean) 블록은 "유효한"(valid) 노드들만을 담고 있는 블록을 말한다. "더러운"(dirty) 블록은 적어도 한 개의 "쓸모없는"(obsolete) 노드를 갖고 있는 블록을 말한다. "빈"(free) 블록은 노드들을 갖고 있지 않은 블록을 말한다.

[쓰레기 수집](../Page/쓰레기_수집_\(컴퓨터_과학\).md "wikilink") [알고리즘](https://ko.wikipedia.org/wiki/알고리즘 "wikilink")은 백그라운드로 수행된다. 이 작업은 "더러운"(dirty) 블록들을 빈 블록들로 전환시킨다. 블록 내의 "유효한"(valid) 노드들만을 새로운 블록으로 옮기고, 블록 내의 "쓸모없는"(obsolete) 블록들은 그냥 놓아 둔다. 마지막으로 "더러운"(dirty) 블록들을 삭제한다. 또한, 그 블록에 빈 블록이라는 것을 나타내는 특별한 마커를 지정해주는 태그를 달아준다. (지우기 동작 중 전원이 갑자기 나갔을 경우의 혼란을 없애준다.)

[웨어 레벨링을](https://ko.wikipedia.org/wiki/웨어_레벨링 "wikilink") 보다 공평하게 하기 위해서, 또한 거의 정적인 파일 시스템이 너무 집중화되는 것을 방지하기 위해서, 쓰레기 수집기(garbage collector)는 가끔 "깨끗한"(clean) 블록을 소모하기도 한다.

## 단점

  - [마운트](https://ko.wikipedia.org/wiki/마운트 "wikilink") 시점에 모든 노드들이 한 번은 스캔되어야 한다. 이 동작은 시간이 걸린다. [테라바이트](https://ko.wikipedia.org/wiki/테라바이트 "wikilink") 정도 용량의 플래시 장치를 쓸 경우 큰 문제가 된다.
  - 수많은 작은 크기의 블록들을 쓰는 것은 압축률에 부정적이 영향을 가져온다. 응용 프로그램으로 하여금 큰 크기의 쓰기 버퍼를 갖게 하는 일이 중요해진다.
  - 장치의 남은 공간이 얼마인지 정확하게 계산할 수 있는 실질적인 방법이 존재하지 않는다. 장치의 남은 공간은 데이터가 얼마나 압축될지, 또한 어떤 순서로 쓰기(writing)될지에 의해 결정되기 때문이다...

## 같이 보기

  - [JFFS](../Page/JFFS.md "wikilink")
  - [YAFFS](https://ko.wikipedia.org/wiki/YAFFS "wikilink")
  - [SquashFS](https://ko.wikipedia.org/wiki/SquashFS "wikilink")
  - [UBIFS](https://ko.wikipedia.org/wiki/UBIFS "wikilink")

## 각주

  - Woodhouse, David. [JFFS: The Journalling Flash File System](http://sources.redhat.com/jffs2/jffs2-html).

## 외부 링크

  - [Red Hat JFFS2 site](http://sources.redhat.com/jffs2/)
  - [JFFS: The Journalling Flash File System](http://sources.redhat.com/jffs2/jffs2.pdf) by David Woodhouse
  - [JFFS2 official mailing list](http://lists.infradead.org/pipermail/linux-mtd/)

[분류:파일 시스템](https://ko.wikipedia.org/wiki/분류:파일_시스템 "wikilink")