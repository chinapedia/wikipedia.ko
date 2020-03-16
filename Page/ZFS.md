> This article is converted from Wikipedia: [ZFS](https://ko.wikipedia.org/wiki/ZFS).


**ZFS** 파일 시스템은 기존의 유닉스 파일시스템을 대체하기 위하여 2005년 SOLARIS10에서 처음 소개된 파일시스템으로, 파일시스템들 가운데 최초로 128비트 파일 시스템을 적용하여 거의 무한대의 용량을 제공하며 파일시스템 자체에서 볼륨 매니저 기능을 포함하여 시스템 내에 있는 하드 디스크들을 구성하거나 스토리지 풀로 통합하여 사용하는 것이 특징이다.

## 기능

### 용량

ZFS는 [128비트](../Page/128비트.md "wikilink") 파일 시스템이므로\[1\]\[2\] [Btrfs](../Page/Btrfs.md "wikilink")와 같은 64비트 시스템 보다 1.84 × 10<sup>19</sup>배 더 많은 데이터의 주소를 할당할 수 있다. ZFS의 제한은 매우 크게 설계되어 있어서 현실적으로 이 제한을 마주치는 일은 없다. 이를테면 2<sup>128</sup> 비트의 데이터가 있는 하나의 zpool을 완전히 채우려면 10<sup>24</sup> 3 TB의 하드 디스크 드라이브가 필요하다.\[3\]

## 역사

ZFS는 Jeff Bonwick, 빌 무어\[4\], Matthew Ahrens의 주도 하에 썬의 팀이 설계하고 구현하였다. 2004년 9월 14일 발표되었지만\[5\] 개발은 2001년에 시작되었다.\[6\] ZFS의 소스코드는 2005년 10월 31일 [솔라리스](../Page/솔라리스_\(운영_체제\).md "wikilink") 개발의 메인 trunk에 통합되었으며\[7\] 2005년 11월 16일 오픈솔라리스 빌드 27의 일부로 릴리스되었다.

## 각주

[분류:파일 시스템](https://ko.wikipedia.org/wiki/분류:파일_시스템 "wikilink") [분류:유닉스](https://ko.wikipedia.org/wiki/분류:유닉스 "wikilink") [분류:2005년 소프트웨어](https://ko.wikipedia.org/wiki/분류:2005년_소프트웨어 "wikilink") [분류:오라클 소프트웨어](https://ko.wikipedia.org/wiki/분류:오라클_소프트웨어 "wikilink")

1.
2.
3.
4.
5.
6.
7.