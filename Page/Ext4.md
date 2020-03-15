> This article is converted from Wikipedia: [Ext4](https://ko.wikipedia.org/wiki/Ext4).


**ext4**(**ext**ended file system **4** , 확장된 파일 시스템 4)는 [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink")의 [저널링 파일 시스템](../Page/저널링_파일_시스템.md "wikilink") 중 하나로, ext3 파일 시스템의 향상된 버전이다.

## 역사

64비트 기억 공간 제한을 없애고 ext3의 성능을 향상시키며, [하위 호환성이](../Page/하위_호환성.md "wikilink") 있는 확장 버전으로서, 많은 부분이 본래, [러스터](https://ko.wikipedia.org/wiki/러스터_\(파일_시스템\) "wikilink") 파일시스템을 위해 [클러스터 파일 시스템스사에서](https://ko.wikipedia.org/wiki/클러스터_파일_시스템스 "wikilink") 개발되었다.\[1\] 그러나 다른 커널 개발자들은 안정성을 이유로 이를 반대했으며, 모든 개발에서 ext3 사용자에게는 영향을 주지 않으면서 ext3에서 fork하여 ext4로 이름을 변경하기를 제안했다. 이 제안이 받아들어져 [2006년](https://ko.wikipedia.org/wiki/2006년 "wikilink") [6월 28일](https://ko.wikipedia.org/wiki/6월_28일 "wikilink") ext3를 유지 보수하던 [Theodore Ts'o는](https://ko.wikipedia.org/wiki/Theodore_Ts'o "wikilink") 새로운 ext 개발 계획을 발표하였다.

ext4의 초기 버전은 리눅스 커널 버전 2.6.19에 포함되었다. 2008년 10월 11일, ext4는 안정화된 코드로 리눅스 2.6.28 소스 코드 저장소에 추가되었고, 개발 과정 종료의 조짐과 ext4 채택 권장이 있었다. ext4 [파일 시스템을](https://ko.wikipedia.org/wiki/파일_시스템 "wikilink") 포함하는 커널 2.6.28은 마침내 2008년 12월 25일에 공개되었다. 2010년 1월 15일, 구글은 자사의 스토리지 인프라를 ext2에서 ext4로 업그레이드한다고 발표했다.

## 특징

  - 대형 파일 시스템
    최대 1[엑사바이트](https://ko.wikipedia.org/wiki/엑사바이트 "wikilink")의 볼륨과 최대 16[테라바이트](https://ko.wikipedia.org/wiki/테라바이트 "wikilink")의 파일을 지원한다. 현재 e2fsprogs는 16 테라바이트의 파일 시스템만 다룰 수 있지만, 보다 큰 드라이브를 지원하기 위한 개발이 진행 중이다.

<!-- end list -->

  - Extent
    Extent는 ext2와 ext3에서 쓰이던 전통적인 [블록 매핑](https://ko.wikipedia.org/wiki/블록_매핑 "wikilink")(block mapping) 방식을 대체하기 위한 것이다. Extent는 인접한 물리적 블록의 묶음으로, 대용량 파일 접근 성능을 향상시키고 단편화를 줄인다. ext4에서 하나의 extent는 최대 128 [MiB](https://ko.wikipedia.org/wiki/MiB "wikilink")의 연속적인 공간에 매핑될 수 있으며, 그 공간은 4 [KiB](https://ko.wikipedia.org/wiki/KiB "wikilink") 크기의 블록으로 구분된다.\[2\] [inode](https://ko.wikipedia.org/wiki/inode "wikilink")에는 4개의 extent가 존재할 수 있다. 하나의 파일에 extent가 4개 이상 할당되는 경우에는, 나머지 extent들이 [Htree](https://ko.wikipedia.org/wiki/Htree "wikilink")에 인덱스된다.

<!-- end list -->

  - [하위 호환성](../Page/하위_호환성.md "wikilink")
    ext3과 ext2에 대한 하위 호환성이 있어서 ext3과 ext2 파일 시스템을 ext4로 마운트하는 것이 가능하다. 이는 성능을 조금 향상시킬 수 있는데, ext4의 새 기능 중 새로운 블록 할당 알고리즘과 같은 것은 ext3과 ext2에서도 사용될 수 있기 때문이다. ext3은 ext4 파일 시스템을 마운트할 수 있는, ext4에 대한 부분적인 [상위 호환성이](../Page/상위_호환성.md "wikilink") 있다. 하지만 ext4 파티션이 ext4의 중요한 새 특징인 Extents를 사용한다면, ext3으로 마운트는 불가능하다.

<!-- end list -->

  - 지연된 할당
    ext는 지연된 할당이라고도 알려진, allocate-on-flush라는 파일 시스템 성능 기술을 사용한다. 이는 데이터가 디스크에 쓰여지기도 전에 블록을 할당하는 다른 파일 시스템과는 다르게, 데이터가 디스크에 쓰여지기 전까지 블록 할당을 지연시킨다. 따라서 실제 파일 크기에 기반하여 블록 할당을 결정함으로 인해 향상된 블록 할당이 가능하게 되어 하나의 파일에 대한 블록이 여러 곳으로 분산되는 현상을 막는다. 이는 다시 디스크 이동을 최소화 시킴으로써 성능을 향상 시킨다.

<!-- end list -->

  - 32,000개의 하위 디렉터리 제한 없음
    ext3에서 하위 디렉터리의 수는 32,000개로 제한되어 있다. 이 제한은 ext4에서 64,000개로 늘어났으며, "dir_nlink" 기능은 이보다 더 큰 개수도 허용한다. (비록 부모의 링크 수가 더 이상 증가하지 않게 되더라도). 더 큰 디렉터리를 가능하게 하면서도 지속된 성능을 얻기 위해서, Htree 인덱스 (B-tree의 특별한 버전)은 기본적으로 사용된다. 이 기능은 커널 2.6.23에서 구현되었다. Htree는 ext3에서도 "dir_index" 기능이 켜져있으면 사용 가능하다.

## 단점

### 지연된 할당과 데이터 유실 가능성

지연된 할당은 프로그래머가 ext3에서 의도했던 동작을 변경하기 때문에, 이 특성은 모든 데이터가 디스크에 기록되기 전에 발생한 시스템 [충돌이나](../Page/충돌_\(컴퓨팅\).md "wikilink") 전원 차단 시 추가적인 데이터 유실 위험을 야기한다. 그래서 2.6.30 이상의 커널에서는 자동으로 이런 경우를 알아차리고 이전의 동작으로 되돌린다.

## 참고 자료

<references/>

[분류:파일 시스템](https://ko.wikipedia.org/wiki/분류:파일_시스템 "wikilink") [분류:자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_소프트웨어 "wikilink") [분류:파일 시스템](https://ko.wikipedia.org/wiki/분류:파일_시스템 "wikilink") [분류:2008년 소프트웨어](https://ko.wikipedia.org/wiki/분류:2008년_소프트웨어 "wikilink")

1.
2.