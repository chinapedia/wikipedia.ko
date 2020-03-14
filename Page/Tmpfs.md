> This article is converted from Wikipedia: [Tmpfs](https://ko.wikipedia.org/wiki/Tmpfs).


**tmpfs**는 수많은 [유닉스 계열](https://ko.wikipedia.org/wiki/유닉스_계열 "wikilink") 운영 체제의 [임시 파일](https://ko.wikipedia.org/wiki/임시_파일 "wikilink") 스토리지 기능을 일컫는 이름이다. 마운트된 [파일 시스템처럼](https://ko.wikipedia.org/wiki/파일_시스템 "wikilink") 보이지만 영구적인 기억 장치가 아닌 [휘발성 메모리에](https://ko.wikipedia.org/wiki/휘발성_메모리 "wikilink") 저장된다. 가상 디스크 드라이브처럼 보이면서도 [디스크 파일 시스템을](https://ko.wikipedia.org/wiki/파일_시스템 "wikilink") 호스팅하는 [램 디스크와](https://ko.wikipedia.org/wiki/램_디스크 "wikilink") 구조가 비슷하다.

## 구현

### 썬OS/솔라리스

[썬OS](https://ko.wikipedia.org/wiki/썬OS "wikilink") 4는 tmpfs의 최초 구현체에 상당한 것을 포함하고 있다. 1987년 말, 어떠한 오브젝트라도 메모리 매핑을 할 수 있게 도와주는 새로운 수직 주소 공간 관리와 더불어 썬OS 4.0에 처음 등장하였다.\[1\]\[2\]

1994년 11월 공개된 [솔라리스](https://ko.wikipedia.org/wiki/솔라리스_\(운영_체제\) "wikilink") /tmp 디렉터리는 솔라리스 2.1부터 기본적으로 tmpfs 파일 시스템으로 구성되었다. 솔라리스의 df 명령어를 통한 출력은 tmpfs 볼륨에 대응하여 swap이라는 파일 시스템으로 표시한다:

``` console
# df -k
Filesystem  kbytes  used   avail capacity  Mounted on
swap        601592     0  601592     0%    /tmp/test
```

### 리눅스

tmpfs는 [리눅스 커널](https://ko.wikipedia.org/wiki/리눅스_커널 "wikilink") 버전 2.4 이상부터 지원한다.\[3\] tmpfs (과거 이름: shmfs)는 시동 중 사용되는 ramfs 코드에 기반을 두며 페이지 캐시를 사용하지만, ramfs와는 달리 덜 사용되는 페이지들을 스왑 공간으로 스왑 아웃 처리를 지원하며, [메모리 부족](https://ko.wikipedia.org/wiki/메모리_부족 "wikilink") 상황을 피하기 위해 파일 시스템 크기와 inode 제한을 지원한다. (각각, 기본적으로 물리 RAM의 절반, RAM 페이지 수의 절반)\[4\] 이러한 옵션들은 마운트 시에 설정되며 파일 시스템을 다시 마운트함으로써 수정할 수 있다:

` df -h`
` mount -o remount,size=4G /tmp`
` df -h`

다시 마운트하기 전에 (free 명령을 사용하여) 충분한 여유 RAM 공간이 있는지 확인할 필요가 있다. 이를테면 2GB 이상 사용하려고 하면 64비트 [리눅스 커널이](https://ko.wikipedia.org/wiki/리눅스_커널 "wikilink") 필요하다. ([uname](https://ko.wikipedia.org/wiki/uname "wikilink") -a 명령으로 확인 가능)

## 각주

<references />

## 외부 링크

  -

[분류:파일 시스템](https://ko.wikipedia.org/wiki/분류:파일_시스템 "wikilink")

1.
2.
3.
4.