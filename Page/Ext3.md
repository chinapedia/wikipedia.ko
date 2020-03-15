> This article is converted from Wikipedia: [Ext3](https://ko.wikipedia.org/wiki/Ext3).


**ext3**(extended file system 3, 확장된 파일 시스템 3)는 [파일 시스템](https://ko.wikipedia.org/wiki/파일_시스템 "wikilink") 가운데 하나로 만든 이는 [스테펜 트위디](https://ko.wikipedia.org/wiki/스테펜_트위디 "wikilink")(Stephen Tweedie)이다. 2001년 11월 [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink") 커널 2.4.15판에서 처음 모습을 드러냈다. [ext4](https://ko.wikipedia.org/wiki/ext4 "wikilink") 파일시스템이 ext3를 계승했다.

## 장점

  - [ext2](https://ko.wikipedia.org/wiki/ext2 "wikilink")에서 자료 삭제 및 손실 없이 ext3으로 변경할 수 있다(자료를 백업할 필요가 없음).
  - [저널링](https://ko.wikipedia.org/wiki/저널링 "wikilink")
  - 온라인 파일 시스템 증대
  - 큰 규모의 디렉터리를 위한 Htree(btree의 고급판)

이 밖의 모든 것들은 ext2와 같다. ext2를 유지하고 복구하기 위해 충분한 테스트를 거쳐 보다 완전해진 파일 시스템 유지보수 유틸리티들을 포함하여 ext2 파일 시스템에서 큰 변화 없이 ext3와 함께 사용될 수 있도록 하였다. ext2와 ext3 둘 다 [e2fsprogs](https://ko.wikipedia.org/wiki/e2fsprogs "wikilink")를 사용하며 이 유틸리티는 [fsck](https://ko.wikipedia.org/wiki/fsck "wikilink")를 포함하고 있다. 이러한 밀접한 관련으로 이 두 파일 시스템들은 상호 변환이 용이하다.

## 저널링

Ext3를 지원하는 리눅스 시스템에서는 다음과 같은 3단계 저널링을 사용할 수 있다.

  - **Journal (리스크 최소)**

두 파일 시스템의 메타 데이터와 파일 컨텐츠는 메인 파일 시스템에 전달되기 전에 저널에 기록된다. 저널은 비교적 디스크와 관련이 있어서 어떤 경우에는 성능을 향상시킬 수 있으나, 데이터가 저널에 한 번, 파일 시스템에 한 번, 이렇게 두 번 기록되기 때문에 성능이 저하될 수도 있다.

  - **Ordered (리스크 중간)**

메타 데이터만 저널에 기록된다. 파일 컨텐츠는 기록되지는 않지만 만일 관련된 메타 데이터가 저널에 기록되면 파일 컨텐츠는 디스크에 반드시 기록된다. 이는 많은 리눅스 배포판에 기본 설정으로 되어 있다. 만일 파일을 읽거나 쓰는 도중에 전원이 갑자기 꺼지거나 [커널 패닉](../Page/커널_패닉.md "wikilink") 상태가 되면, 저널은 새로운 파일을 가리키게 되거나 추가된 데이터가 넘겨지지 않으며, 삭제 처리된다. 하지만, 중복 쓰기가 된 파일은 원본이 저장되지 않아 파일이 손상될 수 있는데, 파일을 복구하기 위한 충분한 정보 없이 새 파일과 이전 파일의 중간 상태에서 파일이 종료될 수 있다. - 새로운 데이터는 완벽하게 디스크에 저장되지 않으며, 이전 데이터는 어디에도 저장되지 않는다. - 심한 경우에는, 중간 상태가 이전 데이터와 새 데이터 사이에 혼란을 줄 수 있다.\[1\]\[2\]

  - **Writeback (리스크 최고)**

메타 데이터만 저널에 기록되며, 파일의 내용은 기록되지 않는다. 파일 내용은 저널이 업데이트된 후에나 아니면 그 이전에 기록될 수 있으며, 결과적으로 충돌 바로 전에 수정된 파일들은 손상될 수 있다. 예를 들어, 추가된 파일이 실제 크기보다 더 큰 파일로 저널에 기록되면, 결국은 "쓰레기(의미 없는 정보)"를 만들게 된다. 오래된 파일일수록 저널이 복구된 후에 예상치 못한 결과가 나타날 수 있다. 데이터와 저널 사이에 동시성이 결여되며 대부분의 경우에서 점점 심해진다. XFS와 JFS는 이러한 저널링 레벨을 사용하지만 데이터를 기록하지 않기 때문에 모든 "쓰레기"는 재부팅 시 완전히 삭제된다.

일부 상황에서는 동적 inode 할당 및 확장과 같은 현대 파일시스템의 기능 부족이 단점으로 여겨질 수 있지만, 복구의 측면에서는 이러한 사실이 아주 뛰어난 장점이 된다. 파일 시스템의 메타 데이터는 모두 수정되고, 잘 알려진 위치에 존재하며, 데이터 구조에 일부 중복성이 내재되어 있어, 트리 기반의 파일 시스템이 복구되기 어려운 상황에서도 뚜렷한 데이터 손상에도 불구하고 ext2 및 ext3 파일시스템이 복구될 수 있다.

## 단점

  - [JFS](https://ko.wikipedia.org/wiki/JFS "wikilink"), [ReiserFS](../Page/ReiserFS.md "wikilink"), [XFS](../Page/XFS.md "wikilink") 등에 비해 낮은 처리 속력

<!-- end list -->

  - **기능 (Functionality)**

ext3는 ext2와 대부분 호환이 가능하도록 하는 것을 목표로 하였고, 많은 on-disk 구조들이 ext2의 on-disk와 비슷하다. 이 때문에, ext3는 inode의 동적 할당 및 다양한 블록 크기(frag와 tail)와 같은 최신 파일시스템 설계의 기능들이 부족하다. ext3 파일 시스템은 쓰기를 위해 마운트 되어있는 동안에는 fsck를 할 수 없다. 읽기-쓰기가 마운트 되어있는 동안 수집된 파일 시스템의 덤프 작업은 데이터 손상을 가져올 수 있다.

ext3는 JFS, ext4, 그리고 XFS와 같은 다른 파일 시스템에서 볼 수 있는 기능인 extents 기능을 지원하지 않는다.

하위 디렉토리에 생성될 수 있는 서브디렉토리의 최대 수는 31998 개 이다. 이는 아이노드가 32000개의 링크를 지원하기 때문이다. (./ 현재폴더, ../ 상위폴더 링크)

  - **조각 모음 (Defragmentation)**

파일 시스템 레벨에서 사용할 수 있는 온라인 ext3 조각 모음 기능은 없다. e2defrag라고 하는 오프라인 ext2 조각 모음기가 있지만 ext3 파일 시스템은 ext2로 먼저 재변환되어야 한다. e2defrag는 데이터를 손상시킬 수 있다. 왜냐하면 e2defrag는 ext3의 새로운 기능들을 어떻게 다루어야 하는지 잘 알지 못하기 때문이다.\[3\]

사용자 공간에서 이용할 수 있는 defragmentation 도구에는 Shake\[4\] 와 defrag\[5\] 등이 있다. Shake는 전체 파일을 위한 공간을 바로 할당하며 단편화가 많이 되지 않도록 새롭게 파일을 할당하는 역할을 한다. 또한, 다음에 같이 사용되는 파일을 서로 쓸 수 있도록 한다. Defrag는 각 파일 스스로가 복사할 수 있도록 한다. 하지만 이러한 도구들은 파일 시스템이 비어 있을 때만 작동한다. 실제 조각 모음 도구는 ext3를 위해 존재하는 것이 아니다.\[6\] 'Linux System Administrator Guide' 에서는 "현재의 리눅스 파일 시스템은 연속적인 섹터에 저장될 수 없음에도 불구하고 서로가 파일 상에서 근접하게 모든 블록을 최소한으로 유지함으로써 단편화를 허용한다. 따라서 리눅스 시스템에서 단편화를 걱정할 필요는 없다." 라고 기술되어 있다.\[7\]

전술한 것과는 상관 없이, 파일 단편화는 멀티미디어 서버 응용 프로그램에서와 같은 서버 환경에서는 매우 중요한 문제가 될 수 있다. ext3는 FAT 파일 시스템보다는 파일 단편화에 강한 편이지만 그럼에도 불구하고 ext3 파일 시스템은 시간이 지날수록 단편화가 더욱 진행된다. 결과적으로 ext3의 다음 버전인 ext4의 경우 파일 시스템 조각 모음 유틸리티를 포함하며 extents 또한 지원하게 된다. 속도가 빠르고, 동시적이며 랜덤한 파일 생성, 업데이트 및 접근이 일어나는 곳에서의 서버 응용 프로그램들은, (ext3와 같은) 일부 리눅스 파일 시스템에 조각 모음 기능이 없어서 큰 문제가 되기도 한다. 이러한 시스템에는 큰 규모의 carrier grade 음성 메일 시스템을 포함, Media-Messaging Service Centers(MMSCs) 및 SMS/SMSC(Short Message Service Centers) 서버도 포함된다. 규모가 큰 음성 메일과 같은 미디어 서버나 UMS 서버는 거의 실시간 상태로 수많은 사용자에게 음성 및 영상 스트림을 연결해주어야 한다. 이러한 타입의 응용 프로그램들은 파일 단편화가 이루어질 가능성이 있다. 음성이나 영상 파일을 재생하는 동안 미디어 파일 내에 많은 단편화 현상 때문에 접근 지연으로 재생 불능이나 재생 방해가 발생할 수 있다. 단편화 현상이 증가함에 따라, CPU 및 I/O 오버헤드 증가로 디스크 thrashing을 일으켰던 단편화를 가져오게 됨으로써 이러한 시스템들의 서비스 능력이 떨어지게 된다.

  - **압축 (Compression)**

ext3의 비공식 패치에서는 투명 압축이 지원된다. 이 패치는 e2compr의 직접적인 포트이며 개발이 더 필요한 상태이며, 업스트림 커널과 컴파일 및 부팅이 잘 되지만 저널링은 아직 구현되지 않았다. 현재 패치는 e3compr이며 다음 링크에서 확인할 수 있다: <http://sourceforge.net/projects/e3compr/>

  - **크기 제한 (Size limits)**

ext3는 개별 파일 및 전체 파일 시스템 상의 최대 크기에 제한을 두고 있다. 이러한 제한은 파일 시스템의 블록 사이즈에 따라 결정된다.\[8\] (다음 차트 참조)

|       |          |              |
| ----- | -------- | ------------ |
| 블록 크기 | 파일 최대 크기 | 파일 시스템 최대 크기 |
| 1KiB  | 16GiB    | 2TiB         |
| 2KiB  | 256GiB   | 8TiB         |
| 4KiB  | 2TiB     | 16TiB        |
| 8KiB  | 2TiB     | 32TiB        |
|       |          |              |

제한 크기

**참고** 8KiB 블록 사이즈는 8KiB 페이지(Alpha와 같은)를 허용하는 아키텍처에서만 가능하다. [영문 ext3 wiki](https://en.wikipedia.org/wiki/Ext3#Size_limits) 여기와 내용이 틀림.

  - **Checksum을 검사하지 않는다. (No checksumming in journal)**

Ext3는 저널에 기록할 때 checksum 검사를 하지 않는다. ‘barrier=1’이 마운트 옵션 (/etc/fstab)으로써 활성화되지 않고, 하드웨어가 캐시에 기록이 되지 않을 때, 충돌이 일어나는 동안 심각한 파일 시스템 손상의 위험을 일으킨다.\[9\]\[10\] (이 옵션은 대부분 모든 유명한 리눅스 배포판에는 기본적으로 비활성화 상태로 되어 있는데 이것은 대부분의 리눅스 배포판들이 이러한 위험에 노출되어 있다는 것을 의미한다.) 다음과 같은 시나리오를 생각해 볼 수 있다. 하드 디스크 쓰기가 제대로 작동하지 않는다면 (쓰기 속도를 향상시키기 위한 하드 디스크 캐싱 때문에), 하드 디스크는 다른 관련된 블록에 쓰기가 실행되기 전에 하나의 트랜잭션의 commit 블록을 종종 쓰게 된다. 다른 블록들에 쓰기가 되기 전에 전원이 잘못되거나 커널 패닉이 발생하면, 시스템은 재부팅을 해야만 하는 상태가 된다. 리부팅 시, 파일 시스템은 정상적으로 로그를 읽어 들여와서, winners (유효한 commit 블록과 함께 표시되도록 했던 유효하지 않은 트랜잭션을 포함하여 commit 블록이 있는 트랜잭션)를 재실행한다. 종료되지 않은 디스크 쓰기는 결과적으로 진행될 것이지만 손상된 저널 데이터를 사용하게 된다. 파일 시스템은 저널을 재실행하는 동안 손상된 데이터와 함께 정상적인 데이터의 중복 쓰기를 실행한다. 만일 checksum이 사용되었더라면 (상호 checksum으로 fake winner 트랜잭션의 블록이 표시가 된다면), 파일 시스템은 보다 더 잘 알게 되고 디스크 상에서 손상된 데이터를 다시 실행할 필요가 없다.

## 명세

|             |                                                                                                                                           |
| ----------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| Ext3        |                                                                                                                                           |
| 개발자         | Stephen Tweedie                                                                                                                           |
| 이름          | Third Extended File System                                                                                                                |
| 배포          | 2001년 11월 (Linux 2.4.15)                                                                                                                  |
| 파티션 식별자     | 0x83 (MBR) EBD0A0A2-B9E5-4433-87C0-68B6B72699C7 (GPT)                                                                                     |
| 구조          |                                                                                                                                           |
| 디렉터리 내용     | Table, h-Tree, dir_index                                                                                                                 |
| 파일 할당       | bitmap (free space), table (metadata)                                                                                                     |
| 배드 블록       | Table                                                                                                                                     |
| 제한          |                                                                                                                                           |
| 최대 파일 크기    | 16GiB – 2TiB                                                                                                                              |
| 최대 파일 개수    | 파일 시스템 생성 시 다양하게 지정 가능\[11\]                                                                                                              |
| 최대 파일 이름 길이 | 255 바이트                                                                                                                                   |
| 최대 볼륨 크기    | 2TiB – 32TiB                                                                                                                              |
| 파일 이름 허용 문자 | NUL 및 ‘/’를 제외한 모든 바이트 단위 문자                                                                                                               |
| 특징          |                                                                                                                                           |
| 기록 날짜       | 수정 (mtime), 속성 수정 (ctime), 접근 (atime)                                                                                                     |
| 날짜 표현 범위    | 1901년 12월 14일 - 2038년 1월 18일                                                                                                              |
| 날짜 표현 단위    | 1s                                                                                                                                        |
| Forks       |                                                                                                                                           |
| 속성          | No-atime, append-only, synchronous-write, no-dump, h-tree (directory), immutable, journal, secure-delete, top (directory), allow-undelete |
| 파일 시스템 권한   | 유닉스 권한, ACLs 및 임의의 보안 속성 (Linux 2.6 이후 버전)                                                                                                |
| 투명 압축       | 지원 안함                                                                                                                                     |
| 투명 암호와      | 지원 안함 (블록 장치 레벨에서 제공됨)                                                                                                                    |
| 지원 OS       | Linux, BSD, Windows (IFS를 통해 지원)                                                                                                          |

## 같이 보기

  - [ext](https://ko.wikipedia.org/wiki/ext "wikilink")
  - [ext2](https://ko.wikipedia.org/wiki/ext2 "wikilink")
  - [ext4](https://ko.wikipedia.org/wiki/ext4 "wikilink")

## 각주

<references />

## 외부 링크

  - [Linux ext3 FAQ](http://batleth.sapienti-sat.org/projects/FAQs/ext3-faq.html)
  - [Introducing ext3 - IBM developerWorks Advanced filesystem implementor's guide, Part 7](http://www-128.ibm.com/developerworks/linux/library/l-fs7.html)
  - [Ext2 File System For Windows](http://sourceforge.net/projects/ext2fsd) GPL ext2/ext3 file system driver for Windows NT/2000/XP/Vista (opensource, supports read & write)
  - [Ext2 Installable File System For Windows](http://www.fs-driver.org/) ext2/ext3 file system driver for MS Windows NT/2000/XP (freeware, supports read & write on Windows NT4.0/2000/XP/2003/Vista on x86/AMD64)
  - [EXT2 IFS](https://web.archive.org/web/20070829085513/http://uranus.it.swin.edu.au/~jn/linux/ext2ifs.htm) ext2/ext3 file system driver for MS Windows NT/2000/XP (opensource, doesn't support writing, doesn't support Windows XP SP2 or Windows Vista)
  - [Explore2fs](http://www.chrysocome.net/explore2fs) An explorer-like GUI tool for accessing ext2/ext3 filesystems under MS Windows
  - [ext2/ext3 resizing tools](http://ext2resize.sourceforge.net/)
  - [Presentation on EXT3 Journaling Filesystem](http://olstrans.sourceforge.net/release/OLS2000-ext3/OLS2000-ext3.html) by Dr. Stephen Tweedie at the Ottawa Linux Symposium, 20 July, 2000
  - [Tutorial](http://www.howtoadvice.com/Ext3Max/) - Determining Your EXT3 Size Limits

[분류:자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_소프트웨어 "wikilink") [분류:파일 시스템](https://ko.wikipedia.org/wiki/분류:파일_시스템 "wikilink") [분류:2001년 소프트웨어](https://ko.wikipedia.org/wiki/분류:2001년_소프트웨어 "wikilink")

1.  curious onloooker: Speeding up ext3 filesystems
2.  Common threads: Advanced filesystem implementor's guide, Part 8
3.  Andreas Dilger. Post to the ext3-users mailing list. ext3-users mailing list post.
4.  Vleu.net: Shake
5.  Index of /apps/defrag
6.  RE: searching for ext3 defrag/file move program
7.  <http://www.tldp.org/LDP/sag/html/filesystems.html>
8.  Matthew Wilcox. Documentation/filesystems/ext2.txt. Linux kernel source documentation.
9.  Re: Frequent metadata corruption with ext3 + hard power-off
10.
11. inode의 최대 개수는 파일 시스템 생성시 결정된다 (즉, 파일 및 디렉터리의 최대 개수). V는 바이트 단위의 볼륨 사이즈를 말하며, inode의 디폴트 개수는 V/213이고 (또는 블록의 개수, 어느 것이든 해당 개수보다 작다), V/223가 최솟값이다. 디폴트 값은 대부분의 응용 프로그램에서 충분한 값이다. 한 디렉터리가 포함하는 하위 디렉터리의 최대 개수는 32000으로 고정된다.