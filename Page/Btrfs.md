> This article is converted from Wikipedia: [Btrfs](https://ko.wikipedia.org/wiki/Btrfs).


**Btrfs**(B-tree file system 또는 Butter file system\[1\], Better F S\[2\])는 [파일 시스템](https://ko.wikipedia.org/wiki/파일_시스템 "wikilink") 가운데 하나로 현재 [페이스북](../Page/페이스북.md "wikilink")의 [크리스 메이슨이](https://ko.wikipedia.org/wiki/크리스_메이슨 "wikilink") 개발을 지휘하고 있다. 꽤 안정화되어 시험적으로 사용하는곳들이 생기고 있다.

[GNU 일반 공중 사용 허가서를](https://ko.wikipedia.org/wiki/GNU_일반_공중_사용_허가서 "wikilink") 따르고 있으며 2014년 2월 5일 현재 최신판은 **3.13**([리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink") 커널 2.6.32 이후 릴리즈된 커널에 기본으로 포함)이다.

## 역사

Btrfs의 핵심 데이터 구조인 카피온라이트 [B 트리](https://ko.wikipedia.org/wiki/B_트리 "wikilink")(copy-on-write B-tree)는 본래 IBM의 연구원 Ohad Rodeh이 [USENIX](https://ko.wikipedia.org/wiki/USENIX "wikilink") 2007의 발표에서 제안하였다.\[3\]

## 기능

Btrfs가 가질 주기능은 다음과 같다.

  - 동적 [아이노드](../Page/아이노드.md "wikilink") 할당
  - 기록 가능 스냅샷, 스냅샷에 대한 스냅샷
  - 하위 볼륨
  - 오브젝트 차원에서의 미러링 및 스트리핑
  - [zlib](https://ko.wikipedia.org/wiki/zlib "wikilink")을 통한 자체 압축
  - 온라인 및 오프라인 파일 시스템 검사
  - [ext3](https://ko.wikipedia.org/wiki/ext3 "wikilink") ↔ btrfs 상호간 변환
  - [솔리드 스테이트 드라이브](../Page/솔리드_스테이트_드라이브.md "wikilink") 최적화 모드
  - 온라인 [단편화 제거](../Page/단편화_제거.md "wikilink")
  - 시드 디바이스

## 각주

## 참조

## 외부 링크

  -

[분류:오라클 코퍼레이션](https://ko.wikipedia.org/wiki/분류:오라클_코퍼레이션 "wikilink") [분류:GNU GPL을 따르는 소프트웨어](https://ko.wikipedia.org/wiki/분류:GNU_GPL을_따르는_소프트웨어 "wikilink") [분류:파일 시스템](https://ko.wikipedia.org/wiki/분류:파일_시스템 "wikilink")

1.  [linux.conf.au 2008 - 발레리에 헨슨의 Chunkfs 강의 동영상 - 18분 49초 부분에서](http://mirror.linux.org.au/pub/linux.conf.au/2008/Thu/mel8-262.ogg)
2.
3.   Also