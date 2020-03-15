> This article is converted from Wikipedia: [JFFS](https://ko.wikipedia.org/wiki/JFFS).


**저널링 플래시 파일 시스템**( 흔히들 **JFFS**라고 한다.)은 NOR [플래시 메모리](../Page/플래시_메모리.md "wikilink") 장치에 쓰이는 [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink") [로그 구조 파일 시스템이다](https://ko.wikipedia.org/wiki/로그_구조_파일_시스템 "wikilink"). 후속 버전으로는 [JFFS2](https://ko.wikipedia.org/wiki/JFFS2 "wikilink")가 있다.

## 설계

플래시 메모리는 마그네틱 디스크와는 달리 제약 사항이 몇 가지 있다. 특히 플래시 메모리의 어떤 부분을 지우는 것은

  - "쓰기" 동작을 하기 전에 필요한 동작이다.
  - 느린 동작이다.
  - 비교적 큰 세그먼트(보통 64 KiB 혹은 그 이상)에 대해서 행해지는 동작이다.
  - 일정 회수 이하로만 가능한 동작이다. (보통 백만번 이하)

[ext2](https://ko.wikipedia.org/wiki/ext2 "wikilink")와 같은 파일 시스템들은, 대개, 파일 시스템용 자료 구조들을 자체 공간을 사용하는 방식(in-place 방식)으로 업데이트한다. 수정 동작(modification) 후 행해지는, [아이노드](../Page/아이노드.md "wikilink")(inode) 및 디렉터리 등과 같은 자료 구조들 업데이트 말이다. [웨어 레벨링](https://ko.wikipedia.org/wiki/웨어_레벨링 "wikilink")(wear leveling)의 결여(디스크 수명을 생각하지 않음) 때문에, 전통적인 파일 시스템은 플래시 장치에 적당하지 않다.

JFFS는 플래시 장치를 일종의 순환 로그(circular log)로서 취급한다. 그럼으로써 JFFS는 [웨어 레벨링을](https://ko.wikipedia.org/wiki/웨어_레벨링 "wikilink") 하고 있다. JFFS는 노드들 내의 로그(log) 꼬리(tail)에, 파일과 디렉터리에 관한 모든 변경 사항을 기록한다. 각 노드 내에서는 파일 메타데이터를 담고 있는 헤더가 먼저 기록되고, 그것에 이어 데이터가 기록된다. JFFS는 노드들을 오프셋 포인터(offset pointer)를 써서 체인(Hyungrak-Jo)처럼 엮고 있다. 노드들은 처음에는 "유효"(valid) 상태로 시작했다가 나중에 그 노드의 새로운 버전이 생성되면 "쓸모없음"(obsolete) 상태가 된다.

로그의 꼬리(tail)와 로그의 머리(head)사이의 공간이 파일 시스템의 남은 공간(free space)이 된다. 이 남은 공간이 많이 부족할 경우 JFFS는 [쓰레기 수집을](../Page/쓰레기_수집_\(컴퓨터_과학\).md "wikilink") 한다. 쓰레기 수집 동작 중 머리부터 시작해 유효한 노드들은 로그의 꼬리쪽으로 보내고 쓸모없는 노드들은 그냥 지나친다. 그렇게 함으로써 디스크 공간을 확보한다.

## 단점

  - 마운트 시점에, JFFS 드라이버는 모든 inode 체인을 읽어 들여 메모리 상에 올려 놓고 유지해야 한다. 이 동작에 시간이 오래 걸릴 수 있다. JFFS의 메모리 소모량은 파일의 개수와 비례한다.
  - 순환 로그를 쓰기 때문에, 어떤 데이터가 고정되어 있든 아니든, 다시 기록(re-written)할 수밖에 없다. 그러므로 불필요한 삭제(erase) 사이클이 필요하게 되며, 플래시 장치의 수명이 줄어들게 된다.

## 같이 보기

  - [JFFS2](https://ko.wikipedia.org/wiki/JFFS2 "wikilink")
  - [YAFFS](https://ko.wikipedia.org/wiki/YAFFS "wikilink")

## 참고문헌

  - Woodhouse, David. *[JFFS2: The Journalling Flash File System, version 2](http://sources.redhat.com/jffs2/)*.

## 외부 링크

  -

  - [JFFS documentation and official mailing list](http://developer.axis.com/software/jffs/)

[분류:파일 시스템](https://ko.wikipedia.org/wiki/분류:파일_시스템 "wikilink")