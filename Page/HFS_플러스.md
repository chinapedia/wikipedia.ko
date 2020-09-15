> This article is converted from Wikipedia: [HFS 플러스](https://ko.wikipedia.org/wiki/HFS_플러스).


**HFS 플러스**(HFS Plus, HFS+)는 [애플](../Page/애플.md "wikilink")이 개발한 [파일 시스템이다](../Page/파일_시스템.md "wikilink"). [OS X의](https://ko.wikipedia.org/wiki/OS_X "wikilink") 주 파일 시스템으로 사용된다. [매킨토시](../Page/매킨토시.md "wikilink") 컴퓨터(또는 [맥 OS를](../Page/맥_OS.md "wikilink") 구동하는 다른 시스템)의 주 파일 시스템으로 사용되었던 [계층적 파일 시스템](../Page/계층적_파일_시스템.md "wikilink")(HFS)을 대체하기 위해 개발되었다. 디지털 음악 플레이어인 [아이팟](../Page/아이팟.md "wikilink")에서 사용되는 포맷 중 하나이기도 하다. 이전 버전에 해당하는 HFS가 *맥 OS 스탠다드* 또는 *HFS 스탠다드*로 불렸기 때문에 HFS 플러스는 **맥 OS 익스텐디드**(Mac OS Extended) 또는 "HFS 익스텐디드"(HFS Extended)로 불리기도 한다. 애플은 이 파일 시스템을 개발할 때 이를 코드네임 세쿼이아(Sequoia)로 불렀다.\[1\]

HFS 플러스는 HFS의 개량 버전으로서, 훨씬 더 큰 크기의 파일을 지원(블록 주소가 16 비트에서 32 비트 길이로 확장됨)하며, 파일 및 폴더 이름에 [유니코드](../Page/유니코드.md "wikilink")를 사용(기존의 맥 OS 로만 또는 다른 문자셋을 대체)하고, [유니코드 정규화 방식 D와](../Page/유니코드_정규화.md "wikilink") 거의 동일한 방식의 정규화(‘å’와 같은 조합문자가 파일명에서 두 개의 코드로 저장되며 [유니코드 기본 다국어 평면](https://ko.wikipedia.org/wiki/유니코드_블록 "wikilink") 밖의 문자들 또한 두 개의 코드로 저장됨)를 적용한다.\[2\] HFS 플러스에서는 파일 이름은 최대 255 UTF-16 코드 길이가 될 수 있으며, [NTFS](../Page/NTFS.md "wikilink")와 유사한 n-포크(n-forked) 파일이 허용되었다. 2005년까지만 해도 데이터 포크와 리소스 포크 외에 포크를 사용하는 시스템은 거의 없었다. HFS가 16비트 할당 맵핑 테이블을 사용했던데 반해 HFS 플러스는 32비트 할당 맵핑 테이블을 사용한다. HFS의 경우 할당 맵핑 테이블 크기의 제약으로 인해 디스크당 최대 65,536개의 할당 블록만 관리할 수 있다는 점이 심각한 제약사항이었다. 이는 과거 디스크 용량이 작던 시절에는 문제가 되지 않았으나, 디스크 용량이 점점 커짐에 따라 파일이 사용할 수 있는 가장 작은 영역(단일 할당 블록)의 크기도 매우 커져서 전체 디스크 용량을 낭비하게 된다는 문제를 발생시켰다. 예를 들어, 1GB 용량의 디스크에 HFS를 적용하면 할당 블록의 사이즈가 16KB가 되어 1바이트짜리 파일도 항상 16KB의 디스크 용량을 차지하게 되는 것이다. 다른 대부분의 파일 시스템들과 달리 HFS 플러스는 디렉토리에 대한 하드 링크를 지원한다.

대부분의 볼륨 [메타데이터](../Page/메타데이터.md "wikilink")를 저장하는 데에 HFS 플러스는 HFS와 마찬가지로 [B 트리를](../Page/B_트리.md "wikilink") 사용한다.

## 역사

HFS 플러스는 [1998년](../Page/1998년.md "wikilink") [1월 19일](../Page/1월_19일.md "wikilink") [맥 OS 8.1의](https://ko.wikipedia.org/wiki/맥_OS_8 "wikilink") 릴리즈와 함께 도입되었다.\[3\]

[2002년](../Page/2002년.md "wikilink") [11월 11일](../Page/11월_11일.md "wikilink") [맥 OS X v10.2.2](../Page/맥_OS_X_10.2.md "wikilink") 업데이트의 릴리즈와 함께 애플은 HFS 플러스에 데이터 신뢰성을 향상시키는 [저널링](../Page/저널링_파일_시스템.md "wikilink") 옵션을 추가하였다. 맥 OS X 서버에서는 이 기능에 쉽게 접근할 수 있었으나, 데스크탑 클라이언트에서는 커맨드 라인을 통해서만 접근이 가능했다.\[4\] [맥 OS X 10.3에](https://ko.wikipedia.org/wiki/맥_OS_X_10.3 "wikilink") 와서는, 맥의 모든 HFS 플러스 볼륨에 저널링이 기본으로 적용되었다. 시스템 내에서 저널링이 적용된 HFS 플러스 볼륨은 **HFSJ**로 표시된다.

## 각주

## 외부 링크

  - [Apple Technote 1189](http://developer.apple.com/technotes/tn/tn1189.html) - The Monster Disk Driver Technote

  - [hfsdebug](https://web.archive.org/web/20090725161028/http://osxbook.com/software/hfsdebug/) - A debugger for HFS Plus volumes by Amit Singh

  - [HFSExplorer](https://web.archive.org/web/20130202112051/http://hem.bredband.net/catacombae/hfsx.html) - A free Java-based utility to read HFS Plus on Windows

[분류:파일 시스템](https://ko.wikipedia.org/wiki/분류:파일_시스템 "wikilink") [분류:맥 OS](https://ko.wikipedia.org/wiki/분류:맥_OS "wikilink") [분류:MacOS](https://ko.wikipedia.org/wiki/분류:MacOS "wikilink")

1.
2.
3.
4.