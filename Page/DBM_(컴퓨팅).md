> This article is converted from Wikipedia: [DBM \(컴퓨팅\)](https://ko.wikipedia.org/wiki/DBM_\(컴퓨팅\)).


**DBM**은 컴퓨팅에서 데이터에 대한 고속의 단일 키 접근을 제공하는 [라이브러리이자](../Page/라이브러리_\(컴퓨팅\).md "wikilink") 파일 포맷이다.\[1\]\[2\]\[3\]

## 역사

오리지널 dbm 라이브러리와 파일 포맷은 단순한 [데이터베이스 엔진이었으며](../Page/데이터베이스_엔진.md "wikilink") [켐 톰프슨에](https://ko.wikipedia.org/wiki/켐_톰프슨 "wikilink") 의해 개발되었고 1979년 [AT\&T](../Page/AT&T.md "wikilink")에 의해 공개되었다. 이 3 문자는 DataBase Manager에서 비롯된 것이다.

## 구현체

오리지널 AT\&T dbm 라이브러리는 여러 구현체로 대체되었다. 그 예로 다음과 같다:\[4\]

  - *ndbm* ("new dbm")
  - *gdbm* ("GNU dbm")\[5\]
  - *sdbm* ("small dbm")\[6\]\[7\]
  - [버클리 DB](https://ko.wikipedia.org/wiki/버클리_DB "wikilink")
  - [Tokyo Cabinet and Kyoto Cabinet](https://ko.wikipedia.org/wiki/Tokyo_Cabinet_and_Kyoto_Cabinet "wikilink")\[8\]

## 각주

[분류:데이터베이스 엔진](https://ko.wikipedia.org/wiki/분류:데이터베이스_엔진 "wikilink") [분류:자유 데이터베이스 관리 시스템](https://ko.wikipedia.org/wiki/분류:자유_데이터베이스_관리_시스템 "wikilink")

1.  : "DBMs have been with us since the early days of computing, when the need for fast keyed lookups was recognized. The original DBM is a UNIX-based library and file format for fast, highly-scalable keyed access to data. It was followed (in order) by NDBM ('new DBM'), GDBM ('GNU DBM'), and the Berkeley DB. This last is by far the most advanced, and the only DBM under active development today. Nevertheless, all of the DBMs from NDBM onward provide the same core functionality used by most programs, including Apache. A minimal-implementation SDBM is also bundled with [APR](https://ko.wikipedia.org/wiki/Apache_Portable_Runtime "wikilink"), and is available to applications along with the other DBMs.
    Although NDBM is now old - like the city named New Town ('Neapolis') by the Greeks in about 600BC and still called Naples today - it remains the baseline DBM. NDBM was used by early Apache modules such as the Apache 1.x versions of `mod_auth_dbm` and `mod_rewrite`. Both GDBM and Berkeley DB provide NDBM emulations, and Linux distributions ship with one or other of these emulations in place of the 'real' NDBM, which is excluded for licensing reasons. Unfortunately, the various file formats are totally incompatible, and there are subtle differences in behaviour concerning database locking. These issues led a steady stream of Linux users to report problems with DBMs in Apache 1.x."
2.  : "The most common \[single-key\] format is called DBM. Most modern versions of Unix have a DBM library installed as standard, though this is not true of some older systems. The two most common DBM libraries are *ndbm* (standard on Solaris and IRIX) and Berkeley DB Version 2 or 3 (standard on several free operating systems). Exim supports both of these, as well as the older Berkeley DB Version 1, *gdbm*, and *tdb*."
3.  : "Most UNIX systems have some kind of DBM database. DBM is a set of library routines that manages data files consisting of key and value pairs. The DBM routines control how users enter and retrieve information from the database. Although it isn't the most powerful mechanism for storing information, using DBM is a faster method of retrieving information than using a flat file. Because most UNIX sites use one of the DBM libraries, the tools you need to store your information in a DBM database are readily available.
    Almost as many flavors of the DBM libraries exist as there are UNIX systems. Although most of these libraries are compatible with each other, they all basically work the same way...
    A list follows of some of the most popular DBM libraries available:
4.
5.
6.
7.
8.