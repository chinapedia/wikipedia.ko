> This article is converted from Wikipedia: [Xz](https://ko.wikipedia.org/wiki/Xz).


**xz**는 무손실 데이터 압축 프로그램 및 LZMA2 압축 [알고리즘](https://ko.wikipedia.org/wiki/알고리즘 "wikilink") 파일 형식이다.

XZ는 [7-Zip](https://ko.wikipedia.org/wiki/7-Zip "wikilink") 프로그램의 축소 된 버전으로 간주 할 수 있다.\[1\]

## 디자인

XZ는 입력을 하나의 파일로 압축하는데, 여러 파일을 하나로 압축시키는 옵션은 제공하지 않는다. 그렇기 때문에 보통 [Tar (파일 포맷)](https://ko.wikipedia.org/wiki/Tar_\(파일_포맷\) "wikilink") 또는 CPIO [유닉스](https://ko.wikipedia.org/wiki/유닉스 "wikilink") 프로그램에 의해 생성된 단일 파일을 압축하는 것이 일반적이다.\[2\]

## 역사

LZMA2 압축 알고리즘을 사용하는 원조 [7-Zip](https://ko.wikipedia.org/wiki/7-Zip "wikilink") 프로그램으로도 빠르게 압축된 파일을 생성 할 수 있었지만, 그 아카이브 형식 주로 윈도에서만 작동하고, 유닉스 기능을 지원하지 않았다.\[3\]

## 구현

XZ파일 형식은 XZ Utils을 통해 온라인에서 자유롭게 구현 할 수 있다. 대부분의 이 소프트웨어는 (예를 들어, liblzma) 라이센스가 GNU LGPL 와 GNU GPL로 공개 소프트웨어 라이센스이다.\[4\] GNU 타르의 1.22 버전은 XZ 파일이 원활하게 실행하도록 지원해 준다.\[5\]\[6\] FreeBSD 타르는 (2009년 4월 17일에 출시) r191190부터 XZ파일을 지원한다. [7-Zip](https://ko.wikipedia.org/wiki/7-Zip "wikilink")는 9.04 베타 버전 이후 지원한다.(9.20 버전 이후 안정적)\[7\]

## 사용

XZ는 [GNU](https://ko.wikipedia.org/wiki/GNU "wikilink") coreutils 프로젝트,\[8\] Debian, [openSUSE](https://ko.wikipedia.org/wiki/openSUSE "wikilink"),\[9\] ,Fedora,\[10\] Arch Linux,\[11\] Slackware,\[12\] [FreeBSD](https://ko.wikipedia.org/wiki/FreeBSD "wikilink"),\[13\] Gentoo,\[14\] [GNOME](https://ko.wikipedia.org/wiki/GNOME "wikilink"),\[15\] 과 TeX Live\[16\] 에서 패키지 압축으로 유명하다. 이 뿐만 아니라 리눅스 커널로 컴파일 된 파일을 압축하는 기능도 있다.\[17\]

2013년 2월, 리눅스 커널 메인테이너는 그들의 2014년도부터 [bzip2](https://ko.wikipedia.org/wiki/bzip2 "wikilink") 대신 XZ를 압축 도구로 발표했다.\[18\]

## 같이 보기

  - [LZMA](https://ko.wikipedia.org/wiki/LZMA "wikilink")
  - [Gzip](https://ko.wikipedia.org/wiki/Gzip "wikilink")
  - [Bzip2](https://ko.wikipedia.org/wiki/Bzip2 "wikilink")
  - [lzip](https://ko.wikipedia.org/wiki/lzip "wikilink")

## 각주

<references/>

[분류:파일 포맷](https://ko.wikipedia.org/wiki/분류:파일_포맷 "wikilink") [분류:데이터 압축](https://ko.wikipedia.org/wiki/분류:데이터_압축 "wikilink")

1.  .
2.
3.
4.  [XZ Utils Web site](http://tukaani.org/xz/)
5.  [GNU tar Web site: References](http://www.gnu.org/software/tar/#releases)
6.  [Changelog for Tar 1.22](http://git.savannah.gnu.org/cgit/tar.git/tree/ChangeLog.CVS?id=9077de9fa91886697a1294891a8d4e6d17fcd30b)
7.  .
8.   (see version 7.1 and newer files ending in *.tar.xz*).
9.  .
10. .
11. .
12. .
13. .
14. .
15. .
16. .
17. .
18. <https://www.kernel.org/happy-new-year-and-good-bye-bzip2.html>