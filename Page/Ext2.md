> This article is converted from Wikipedia: [Ext2](https://ko.wikipedia.org/wiki/Ext2).


**ext2**(second extended filesystem, 이차 확장 파일 시스템)는 [리눅스](../Page/리눅스.md "wikilink") 파일 시스템 중 하나다. Rémy Card가 [ext](https://ko.wikipedia.org/wiki/확장_파일_시스템 "wikilink")(extended file system, 확장 파일 시스템)를 대체하기 위해 고안하였다.

[리눅스 커널에](../Page/리눅스_커널.md "wikilink") 있는 ext2fs 파일시스템 드라이버는 ext2 파일 시스템을 정식으로 구현했다. 다른 곳에서는 [GNU 허드](../Page/GNU_허드.md "wikilink"), [미닉스](../Page/미닉스.md "wikilink") 3, [OS X](https://ko.wikipedia.org/wiki/OS_X "wikilink")(서드파티), [다윈](../Page/다윈_\(운영_체제\).md "wikilink")(검증 안 된 OS X와 같은 서드파티), 일부 [BSD](../Page/BSD.md "wikilink") 커널, [아타리](../Page/아타리.md "wikilink") 민트, 그리고 [마이크로소프트 윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 드라이버의 서드파티에 (다양한 품질과 완성도로) 구현되었다.

ext2는 ext2와 완전히 호환 가능한 저널링 시스템인 ext3로 대신할 때까지 [데비안](../Page/데비안.md "wikilink"), [레드햇 리눅스를](../Page/레드햇_리눅스.md "wikilink") 포함한 몇몇 [리눅스 배포판의](../Page/리눅스_배포판.md "wikilink") 기본이었다. ext2는 여전히 [플래시](https://ko.wikipedia.org/wiki/플래시_드라이브 "wikilink") 기반의 저장 매체([SD카드](https://ko.wikipedia.org/wiki/SD카드 "wikilink"), [USB 플래시 드라이브](../Page/USB_플래시_드라이브.md "wikilink"))에서 선택하는 파일 시스템인데, 이는 저널이 쓰기 횟수를 최소화하는 능력이 부족하고 플래시 장치는 쓰기 횟수 주기가 제한되었기 때문이다. 그러나 최근 커널은 ext4의 많은 장점을 살리며 ext4의 저널-부족 모드를 지원한다.

## 역사

리눅스의 초기 개발은 [미닉스](../Page/미닉스.md "wikilink") 운영 체제의 교차 개발로 만들어졌다. 당연히 미닉스 파일 시스템이 리눅스의 첫 번째 파일 시스템이 되었다. 미닉스 파일 시스템은 대부분 [버그가](../Page/소프트웨어_버그.md "wikilink") 없었으나, 16비트 오프셋을 사용했기 때문에 최대 크기가 64 [메가바이트](../Page/메가바이트.md "wikilink")로 제한되었다. 또한 파일명을 14자밖에 쓸 수 없었다. 이런 제한 때문에, 기존 파일 시스템을 리눅스를 위한 파일 시스템으로 대체하는 작업이 시작되었다.

새 파일 시스템의 추가를 완화하고 일반 파일 [API](../Page/API.md "wikilink")를 제공하기 위해 [VFS](https://ko.wikipedia.org/wiki/VFS "wikilink"), 즉 가상 파일 시스템 레이어가 리눅스 커널에 추가되었다. [확장 파일 시스템](https://ko.wikipedia.org/wiki/확장_파일_시스템 "wikilink")(ext)는, 1992년 4월에 VFS API를 사용한 파일 시스템으로 처음 발표되었고 리눅스 버전 0.96c에 포함되었다. ext 파일 시스템은 미닉스 파일 시스템의 두 가지의 주요 문제(최대 파티션 크기와 파일 이름 14자 제한)를 해결하였으며, 2 [기가바이트](https://ko.wikipedia.org/wiki/기가바이트 "wikilink")의 데이터와 255자의 파일명 제한을 허용하였다. 그렇지만 여전히 파일 접근에 대한 [타임 스탬프](https://ko.wikipedia.org/wiki/타임_스탬프 "wikilink"), [아이노드](../Page/아이노드.md "wikilink") 수정, 그리고 데이터 수정을 지원하지 않는 문제가 있었다.

그 문제의 해결 방법으로, 1993년 1월에 새로운 두 파일 시스템 [xiafs](https://ko.wikipedia.org/wiki/xiafs "wikilink")와 [버클리 고속 파일 시스템으로부터](../Page/유닉스_파일_시스템.md "wikilink") 많은 아이디어를 통합하여 확장 파일 시스템을 재검토하는 **이차 확장 파일 시스템**(**ext2, seconday extended file system**)이 개발되었다. ext2는 또한 다음 버전에서 사용할 많은 디스크상 데이터의 남은 공간에 대한 확장성을 염두에 두고 설계되었다.

그 때부터, ext2는 VFS API에 여러 가지 새 확장에 대한 테스트베드를 해 왔다. [POSIX](../Page/POSIX.md "wikilink") [접근 제어 목록과](../Page/접근_제어_목록.md "wikilink") 확장 속성은 보통 ext2에 먼저 구현되었는데, 이는 ext2가 상대적으로 확장이 단순하였고 그 내부 구조가 이해하기 쉽게 되어있었기 때문이다.

2.6.17 이전의 리눅스 커널에서\[1\] ext2 파일 시스템에 대한 블록 드라이버 크기 제한이 최대 2 테라바이트였다.

ext2는 여전히 부팅 가능한 USB 플래시 드라이브와 다른 [솔리드 스테이트 드라이브에서](../Page/솔리드_스테이트_드라이브.md "wikilink") 저널링 파일 시스템 이상을 권장하고 있다. ext2는 저널링을 쓸 필요가 없기 때문에 ext3보다 적은 쓰기를 수행한다. 플래시 칩이 노화되는 주요 원인은 지우기 사이클의 개수이며, 이는 쓰기를 할 때 빈번히 나타나고, 감소된 쓰기작업은 솔리드 스테이트 디바이스의 수명을 증가시킨다.\[2\] 같은 이유로, 플래시 장치상의 파일 시스템에 대해서는 *noatime* 마운트 옵션을 사용하는 것이 좋다.

## ext2 데이터 구조

ext2 공간은 [블록으로](https://ko.wikipedia.org/wiki/블록_\(컴퓨팅\) "wikilink") 나뉘어 있다. 이 블록은 블록 그룹으로 나뉘는데, 이는 유닉스 파일 시스템의 실린더 그룹과 비슷하다. 일반적으로 거대한 파일 시스템에 수천개의 블록이 있다. 주어진 파일의 데이터는 가능한 한 하나의 블록 그룹 내에 포함되어 있다. 이것은 [외부 단편화를](https://ko.wikipedia.org/wiki/외부_단편화 "wikilink") 줄이고 연속된 대량의 데이터를 읽을 때 디스크 탐색을 최소화시킨다.

각각의 블록 그룹은 블록 그룹 서술자 테이블과 슈퍼블록의 복사본을 포함하고 있으며, 모든 블록 그룹은 블록 비트맵, 아이노드 비트맵, 아이노드 테이블을 포함하고 있고, 마지막으로 실제 데이터 블록을 포함한다. [슈퍼블록은](../Page/유닉스_파일_시스템.md "wikilink") 매우 중요한 [운영 체제](../Page/운영_체제.md "wikilink") 부팅, 즉 파일 시스템 내 여러 블록 그룹에서 만들어진 백업한 복사본과 같은 중요한 정보를 포함한다. 그러나, 일반적으로 파일 시스템의 첫 번째 블록에서 찾을 수 있는 첫 번째 복사본만 부팅에 쓰인다.

그룹 서술자는 블록 비트맵, 아이노드 비트맵과 모든 블록 그룹의 아이노드 테이블의 시작점의 위치에 저장되며 이들은 차례로 그룹 서술자 테이블에 저장된다.

### 아이노드

모든 파일이나 디렉터리는 아이노드로 표현된다. 아이노드는 크기, 권한, 소유권, 그리고 파일이나 디렉터리의 디스크의 위치에 대한 데이터를 포함한다.

ext2 아이노드 구조의 예시:

<div align="center">

[Estructure](https://ko.wikipedia.org/wiki/파일:Ext2-inode.svg "wikilink")

</div>

ext2에 대한 커널 문서의 인용문:

> **"아이노드에서 파일의 데이터를 포함하는 첫 12블록의 포인터가 있다. (블록의 다음 세트에 포인터를 포함하는) 간접 블록에 대한 포인터, (간접 블록에 대한 포인터를 포함하는) 이중 간접 블록에 대한 포인터, 그리고 (이중 간접 블록에 대한 포인터를 포함하는) 삼중-간접 블록에 대한 포인터가 있다."**

ext2 내부는 15개의 포인터가 있는 구조며 그 중 처음부터 12번까지는 직접 블록을 위한 것이다. 13번 포인터는 간접 블록을, 14번째 블록은 이중 간접 블록을, 그리고 15번째 포인터는 삼중 간접 블록을 가리킨다.

### 디렉터리

각각의 디렉터리는 디렉터리 엔트리 목록이다. 각 디렉터리 엔트리는 파일명 하나와 아이노드 번호 하나가 연관되어 있으며, 이는 아이노드 번호, 파일명의 길이, 그리고 파일명을 나타내는 실제 텍스트로 구성되어 있다. 파일을 찾기 위해서, 디렉터리 내 관련 파일 이름을 앞에서부터 뒤로 검색한다. 디렉터리 크기가 적당하면 이렇게 해도 괜찮다. 그러나 큰 디렉터리에서는 비효율적이며, [ext3](https://ko.wikipedia.org/wiki/ext3 "wikilink")는 단순히 파일명을 목록에 올리는 것보다 더욱 효율적으로 디렉터리를 저장하는 두 번째 방법을 제공한다.

루트 디렉터리는 아이노드 번호 2에 항상 저장되며, 마운트를 할 때 파일 시스템 코드가 이를 찾을 수 있다. 서브 디렉터리는 서브 디렉터리의 이름을 이름 필드, 그리고 아이노드 필드에 있는 서브 디렉터리의 아이노드 번호에 저장함으로써 구현된다. 하드 링크는 하나 이상의 파일명과 함께 같은 아이노드 번호를 저장함으로써 구현된다. 이름에 의해 파일에 접근하는 것은 같은 아이노드 번호로 접근하는 결과를 낳으므로, 결국에는 같은 데이터로 접근하게 된다.

"."나 ".."와 같은 특별한 디렉터리는 디렉터리, 현재 아이노드 번호와 아이노드 필드에 있는 상위 디렉터리에 "."과 ".."이라는 이름을 저장하는 것과 마찬가지다. 이 두 엔트리는 새 디렉터리가 생길 때 자동으로 만들어지며, 삭제가 불가능하다.

### 할당 데이터

새 파일이나 디렉터리가 만들어지면, ext2 파일 시스템은 어디에 데이터를 저장해야 하는지 반드시 결정해야 한다. 만약 디스크가 대부분 비어있다면, 데이터는 거의 어디든지 저장될 수 있다. 그러나 찾는 시간을 최소화하기 위해 데이터가 다른 관련 데이터와 같이 클러스터된 경우 성능이 최대화된다.

ext2 파일 시스템은 상위 디렉터리를 포함하는 그룹에 각각의 새 디렉터리를 할당하려고 시도하는데, 이론상 부모와 자식 디렉터리에 접근하는 것과 밀접하게 관련될 가능성이 있다. ext2 파일 시스템은 또한 그 디렉터리 엔트리와 같은 그룹에서 파일을 배치하려는 시도를 하는데, 이는 디렉터리 접근이 파일 접근으로 자주 이어지기 때문이다. 그러나, 그룹이 가득 차면, 새 파일이나 새 디렉터리는 그렇지 않은 그룹에 배치된다.

디렉터리와 파일을 저장하는 데 필요한 데이터 블록은 데이터 할당 비트맵에서 파일을 찾을 수 있어야 한다. 아이노드 테이블 안에 있는 모든 필요 공간은 아이노드 할당 비트맵에서 찾을 수 있어야 한다.

## 파일 시스템 제한

| 블록 크기:        |   1 KB |   2 KB |  4 KB |  8 KB |
| :------------ | -----: | -----: | ----: | ----: |
| 최대 파일 크기:     |  16 GB | 256 GB |  2 TB |  2 TB |
| 최대 파일 시스템 크기: | 4\* TB |   8 TB | 16 TB | 32 TB |

리눅스에서의 이론적 ext2 파일 시스템 제한\[3\]

ext2 파일 시스템에 일부 제한이 생기는 이유는 데이터의 파일 포맷과 운영 체제의 커널 때문이다. 대부분 이 요인은 파일 시스템이 만들어질 때 한 번 결정될 것이다. 이는 블록 크기, 블록 수와 아이노드 수의 비율에 따라 달라진다.

또한 2기가바이트보다 용량이 큰 파일은 처리할 수 없는 일부 사용자 공간 프로그램도 있다.

최대 파일 크기는 파일에서 b-byte "블록"의 양을 나타내는 i_block(EXT2_N_BLOCKS의 배열)과 i_blocks(32비트 정수 값)에 의한 min( ((b/4)<sup>3</sup>+(b/4)<sup>2</sup>+b/4+12)\*b, 2<sup>32</sup>\*b )로 제한된다.

서브레벨 디렉터리는 링크 횟수 제한 때문에 31998로 제한된다. ext2는 디렉터리 색인을 제공하지 않으므로 1만개 이상의 많은 파일이 있는 디렉터리에서는 성능에 문제가 있다. 실질적인 상황에 대한 수치는 아니지만, 디렉터리에 있는 파일 수에 대한 이론적 제한은 1.3 × 10<sup>20</sup>이다.

**참고**:리눅스 커널 2.4와 그 이전 버전에서 블록 장치는 2 테라바이트로 제한되었으며, 블록 크기에 관계없이 파티션 하나의 최대 크기를 제한하였다.

## 압축 확장

**e2compr**은 [리눅스 커널에서](../Page/리눅스_커널.md "wikilink") 사용자 애플리케이션의 어떤 지원도 없이 파일 시스템에서 파일의 온라인 압축과 압축 해제를 지원하는 ext2 [파일 시스템](../Page/파일_시스템.md "wikilink") 드라이버의 변형이다.

e2compr은 on-the-fly [압축과](https://ko.wikipedia.org/wiki/디스크_압축 "wikilink") 압축 해제 기능을 제공하는 ext2 파일 시스템의 작은 패치다. e2compr은 일반 파일만 압축한다. 관리 데이터([슈퍼 블록](https://ko.wikipedia.org/wiki/블록_\(컴퓨팅\)#슈퍼_블록 "wikilink")), [아이노드](../Page/아이노드.md "wikilink"), [디렉터리](https://ko.wikipedia.org/wiki/디렉터리 "wikilink") [파일](../Page/컴퓨터_파일.md "wikilink") 등)는 보안을 이유로 압축되지 않는다. 읽기 및 쓰기 작업을 위해 압축된 [블록에](https://ko.wikipedia.org/wiki/블록_\(컴퓨팅\) "wikilink") 대한 접근이 제공된다. 압축 알고리즘과 클러스터 크기는 파일 단위로 지정된다. 디렉터리 역시 압축을 나타내며, 이 경우 디렉터리에서 새로 생성된 모든 파일이 같은 클러스터 크기와 디렉터리에 지정된 같은 알고리즘으로 자동 압축된다.

e2compr은 새로운 파일 시스템이 아니다. 단지 EXT2_COMPR_FL 플래그를 지원하도록 만들어진 ext2 파일 시스템의 패치 버전일 뿐이다. e2compr은 새로운 파티션을 만들 것을 요구하지 않으며, 이미 존재하는 ext2 파일 시스템의 읽기와 쓰기를 지속할 것이다. 간단히 gzip이나 [compress](https://ko.wikipedia.org/wiki/compress "wikilink")와 비슷한 단순 유틸리티로 만든 파일에 접근할 때 루틴을 읽고 쓰는 방법을 고려할 수도 있다. 압축된 파일과 압축 해제된 파일은 공존할 수 있다.

e2-compr에서 갈라져 나온 최신 판은 현재 리눅스 커널 2.4, 2.6, 3.0에서 사용 가능하다. 커널 3.0대의 최신 패치는 2011년 8월에 나왔으며 멀티 코어와 himem을 지원한다. 2.2와 2.0 이하 버전을 지원하는 더 안정적인 판도 있다.

## 같이 보기

  - [ext](https://ko.wikipedia.org/wiki/확장_파일_시스템 "wikilink") : ext2의 원형
  - [ext3](https://ko.wikipedia.org/wiki/ext3 "wikilink") : ext2의 확장 버전
  - [ext4](https://ko.wikipedia.org/wiki/ext4 "wikilink") : 네 번째 확장 파일 시스템

## 각주

  - 참고

<!-- end list -->

  -
  - [Sourceforge e2compr project](http://sourceforge.net/projects/e2compr)

  - [Sourceforge e2compr documentation](http://e2compr.sourceforge.net/)

  - [Sourceforge e3compr project page, ext3 compression, alpha](http://sourceforge.net/projects/e3compr)

  - [Dr. Dobb's Data Compression Newsletter Issue \#46 - September 2003](http://www.ddj.com/showArticle.jhtml?articleID=184405431&queryText=seen)

## 외부 링크

  - [ext2fs 사용자 공간 도구](http://e2fsprogs.sourceforge.net/ext2.html)
  - [윈도에서 ext2, ext3을 읽기 전용으로 볼 수 있는 소프트웨어](http://www.chrysocome.net/explore2fs)
  - [Ext2read](http://ext2read.sourceforge.net) LVM2 확장을 지원하는 ext2/ext3/ext4 파일을 읽고/복사할 수 있는 윈도 응용 소프트웨어
  - (2008년 이후로 업데이트 중단됨) [윈도 NT 4.0/2000/XP/2003/비스타/2008 리눅스 Ext2 볼륨에 모든 권한으로 접근 가능한 무료 ext2 드라이버(읽고 쓰기가 가능). (ext3에서는 읽기만 가능함 - FAQ 참고)](http://fs-driver.org/) (프리웨어)
  - [Ext2Fsd](http://sourceforge.net/projects/ext2fsd/) 윈도 200/XP/2003/비스타/2008에서 쓸 수 있는 GPL ext2/ext3 파일 시스템 드라이버(오픈 소스, 읽기와 쓰기 지원, FreeOTFE로 작동)

[분류:파일 시스템](https://ko.wikipedia.org/wiki/분류:파일_시스템 "wikilink") [분류:1993년 소프트웨어](https://ko.wikipedia.org/wiki/분류:1993년_소프트웨어 "wikilink")

1.  [linux/kernel/git/torvalds/linux-2.6.git/commitdiff:](http://git.kernel.org/?p=linux/kernel/git/torvalds/linux-2.6.git;a=commitdiff;h=a0f62ac6362c168754cccb36f196b3dfbddc3bc3) , \[PATCH\] 2TB files: add blkcnt_t, Author:Takashi Sato, 26 Mar 2006 09:37:52 +0000 (01:37 -0800) — Commit allowing for large files, git.kernel.org
2.
3.