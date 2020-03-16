> This article is converted from Wikipedia: [TRIM](https://ko.wikipedia.org/wiki/TRIM).


**TRIM**은 [컴퓨팅](../Page/컴퓨팅.md "wikilink")에서 [운영 체제가](../Page/운영_체제.md "wikilink") 어느 블록의 데이터가 더 이상 사용되지 않고 내부적으로 삭제될 수 있는지를 [솔리드 스테이트 드라이브](../Page/솔리드_스테이트_드라이브.md "wikilink") (SSD)에 알려주는 명령이다. TRIM은 대개 대문자 그대로 사용하지만 명령어 이름이지 두문자어는 아니다.\[1\]

TRIM은 SSD가 전통적인 [하드 디스크의](https://ko.wikipedia.org/wiki/하드_디스크 "wikilink") 알맞은 대안으로 자리잡힌 직후에 도입되었다. SSD의 낮은 수준의 동작이 기존 하드 드라이브와 상당히 다른 까닭에 운영 체제가 삭제와 포맷과 같은 작업을 관리하는 일반적인 방식이 SSD의 예기치 않은 쓰기 성능 저하로 이어졌다.\[2\] TRIM은 차후 쓰기 속도를 상당히 떨어트리는 쓰레기 수집 오버헤드를 SSD가 미리 관리할 수 있게 한다.\[3\]

TRIM이 도입되기 이전에 일부 드라이브를 깨끗한 상태로 초기화하는 도구들이 존재했으나, 이 도구들은 드라이브의 모든 데이터를 지워야 했기 때문에 최적화 이용에는 실용적이지 못했다.\[4\] 최근에 출시되는 SSD들은 TRIM과 독립적으로 운용되는 내부 유휴/백그라운드 쓰레기 수집 매커니즘을 포함하고 있다. 다시 말해, TRIM을 지원하지 않는 운영 체제에서도 SSD의 성능을 성공적으로 유지시켜 주지만, [쓰기량의 증대와](https://ko.wikipedia.org/wiki/쓰기_증대 "wikilink") 플래시 셀의 마모의 단점이 있다.\[5\]

## 구현

### 운영 체제 지원

| width=""|운영 체제                                            | width=""|지원 시작 시기                                                                      |
| --------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| [DragonFly BSD](../Page/DragonFly_BSD.md "wikilink")      | <span style="display:none">2011-05</span>2011년 5월\[6\]                                 |
| [FreeBSD](../Page/FreeBSD.md "wikilink")                  | <span style="display:none">2010-07</span>8.1 - 2010년 7월\[7\]                           |
| [NetBSD](../Page/NetBSD.md "wikilink")                    | <span style="display:none">2012-10</span>2012년 10월\[8\]                                |
| [리눅스](../Page/리눅스_커널.md "wikilink")                       | <span style="display:none">2008-12-25</span>2.6.28–2008년 12월 25일\[9\]                  |
| [macOS](https://ko.wikipedia.org/wiki/macOS "wikilink")   | <span style="display:none">2011-06-23</span>10.6.8–2011년 6월 23일\[10\]                  |
| [마이크로소프트 윈도우](../Page/마이크로소프트_윈도우.md "wikilink")          | <span style="display:none">2009-10</span>윈도우 7, 윈도우 서버 2008 R2 - 2009년 10월\[11\]\[12\] |
| [오픈솔라리스](https://ko.wikipedia.org/wiki/오픈솔라리스 "wikilink") | <span style="display:none">2010-07</span>2010년 7월\[13\]                                |
| [안드로이드](../Page/안드로이드_\(운영_체제\).md "wikilink")            | <span style="display:none">2013-7</span>4.3\[14\] - 2013년 7월 24일\[15\]                 |

## 하드웨어 지원

  - ATA
  - SCSI
  - SD/MMC

## 참조

<references />

## 외부 링크

  - [*From write() down to flash chips*](https://web.archive.org/web/20100227234254/http://www.devwhy.com/blog/2009/8/4/from-write-down-to-the-flash-chips.html) – an explanation on how the TRIM command lets SSDs erase data not used by the filesystem

  - [*TRIM Command White Paper*](http://www.maximumpc.com/article/features/white_paper_trim_command) - a white paper explaining the TRIM command's purpose and actions

[분류:솔리드 스테이트 드라이브](https://ko.wikipedia.org/wiki/분류:솔리드_스테이트_드라이브 "wikilink")

1.
2.
3.  Shimpi, Anand Lal. (2009-03-18). p. 10.
4.  Shimpi, Anand Lal. (2009-03-18). p. 11.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15. ["Android 4.3 announced, rolling out to Nexus devices today"](https://www.theverge.com/2013/7/24/4550234/android-4-3-announcement).*[The Verge](https://ko.wikipedia.org/wiki/더_버지 "wikilink")*. 24 July 2013. Retrieved 24 July 2013.