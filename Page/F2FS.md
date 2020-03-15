> This article is converted from Wikipedia: [F2FS](https://ko.wikipedia.org/wiki/F2FS).


**F2FS**(Flash-Friendly File System)는 [삼성전자](https://ko.wikipedia.org/wiki/삼성전자 "wikilink")가 [리눅스 커널을](https://ko.wikipedia.org/wiki/리눅스_커널 "wikilink") 위해 개발한 [플래시 파일 시스템이다](https://ko.wikipedia.org/wiki/플래시_파일_시스템 "wikilink").\[1\]

F2FS를 개발한 동기는 파일 시스템을 모바일 장치부터 서버에 이르는 컴퓨터 시스템에 널리 사용되는 [NAND 플래시 메모리](https://ko.wikipedia.org/wiki/NAND_플래시_메모리 "wikilink") 기반 스토리지 장치(예: [솔리드 스테이트 디스크](https://ko.wikipedia.org/wiki/솔리드_스테이트_디스크 "wikilink"), [eMMC](https://ko.wikipedia.org/wiki/eMMC "wikilink"), [SD](https://ko.wikipedia.org/wiki/시큐어_디지털 "wikilink") 카드)의 특징을 염두에 둔 파일 시스템을 처음부터 만드는 것이다.

F2FS는 [로그 구조 파일 시스템](https://ko.wikipedia.org/wiki/로그_구조_파일_시스템 "wikilink") 접근법에 기초하여 설계되었으며 더 새로운 형태의 스토리지에 채택된다. F2FS의 개발자는 wandering tree의 [눈덩이 효과라든지](https://ko.wikipedia.org/wiki/눈덩이_효과 "wikilink") high cleaning 부하와 같은 로그 구조 파일 시스템의 일부 알려진 문제\[2\]를 해결한다고 언급하였다. 또, NAND 기반 기억 장치가 내부적인 플래시 메모리 관리 스킴에 따라 다른 특징(플래시 번역 계층, 즉 FTL 등)을 보이기 때문에 디스크 상의 설계 구성뿐 아니라 할당/cleaning 알고리즘을 선택하기 위한 다양한 매개변수를 지원한다.

## 기능

  - 멀티 헤드 로깅
  - 디렉터리 항목에 대한 다단계 해시 테이블
  - 정적 / 동적으로 신규 데이터 및 오래된 데이터 분리
  - 적응 로깅 방식
  - 구성 가능한 운영 단위
  - 이중 체크포인트
  - 롤백 및 롤포워드 복구
  - 힙 스타일의 블록 할당
  - [TRIM](https://ko.wikipedia.org/wiki/TRIM "wikilink")/FSTRIM 지원\[3\]
  - 온라인 FS [조각 모음](https://ko.wikipedia.org/wiki/조각_모음 "wikilink")/파일 조각 모음\[4\]
  - 인라인 xattrs/data\[5\]/data\[6\]/dir\[7\]
  - 오프라인 [파일시스템 검사](https://ko.wikipedia.org/wiki/Fsck "wikilink")(불일치 확인 후 수정\[8\])
  - [원자 작업](https://ko.wikipedia.org/wiki/원자_작업 "wikilink")\[9\]
  - [파일 시스템 수준 암호화](https://ko.wikipedia.org/wiki/파일_시스템_수준_암호화 "wikilink")\[10\]
  - 오프라인 크기 조절(Offline resizing)\[11\]
  - 내부의 주기적인 데이터 플러시(Inner periodically data flush)\[12\]
  - 익스텐트(extent) 캐시\[13\]

## 각주

## 외부 링크

  - [Flash Friendly File System (F2FS), Embedded Linux Conference](http://elinux.org/images/1/12/Elc2013_Hwang.pdf) (2013-02-22)
  - [A New File System Designed for Flash Storage in Mobile, Embedded Linux Conference Europe](http://elinux.org/images/8/81/A_New_File_System_Designed_for_Flash_Storage_in_Mobile.pdf) (2012-11-05)
  - [Flash Memory Filesystem, Korea Linux Forum](https://web.archive.org/web/20150226070132/http://events.linuxfoundation.org/images/stories/pdf/klf2012_j_kim.pdf) (2012-10-12)
  - [LWN.net: An f2fs teardown](https://lwn.net/Articles/518988/) (2012-10-10)
  - [The f2fs filesystem](https://git.kernel.org/cgit/linux/kernel/git/jaegeuk/f2fs.git)
  - [Userland tools for the f2fs filesystem](https://git.kernel.org/cgit/linux/kernel/git/jaegeuk/f2fs-tools.git)
  - [F2FS wiki for developers](https://f2fs.wiki.kernel.org/start)

[분류:임베디드 리눅스](https://ko.wikipedia.org/wiki/분류:임베디드_리눅스 "wikilink") [분류:파일 시스템](https://ko.wikipedia.org/wiki/분류:파일_시스템 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.