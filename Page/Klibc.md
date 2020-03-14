> This article is converted from Wikipedia: [Klibc](https://ko.wikipedia.org/wiki/Klibc).


**klibc**는 [C 표준 라이브러리의](https://ko.wikipedia.org/wiki/C_표준_라이브러리 "wikilink") 미니멀리스틱한 부분 집합이다. 이것은 주로 리눅스 시작 프로세스 동안에 사용되기 위해 개발되었으며 [초기 사용자 공간의](https://ko.wikipedia.org/wiki/리눅스_시작_프로세스 "wikilink") 한 부분이다. 즉, 커널 스타트업 시에 사용되는 구성 요소이지만 커널 모드에서 실행되지는 않는다.\[1\] 이러한 구성 요소들은 일반적인 사용자 공간 프로그램들에 의해 사용되는 표준 라이브러리(주로 [glibc](https://ko.wikipedia.org/wiki/GNU_C_라이브러리 "wikilink"))에 접근할 수 없다.

문서에 의하면 klibc 라이브러리는 작은 크기와 정확성에 최적화되었다.\[2\] 이 디자인 때문에 klibc는 또한 일반적으로 임베디드 소프트웨어에 적합하다. klibc는 완전 [GPL](https://ko.wikipedia.org/wiki/GNU_일반_공중_사용_허가서 "wikilink") 라이센스 하에 있기 때문에 상용 임베디드 소프트웨어에 사용하기에는 제한이 따른다.\[3\]

리눅스 스타트업 과정에서 klibc는 [initramfs](https://ko.wikipedia.org/wiki/initramfs "wikilink")(임시 [램 파일 시스템](../Page/Tmpfs.md "wikilink")) 내에서 로드된다. 이것은 디폴트로 데비안에서 `mkinitramfs` 스크립트\[4\]에 의해 생성되는 초기 램 파일 시스템에 포함된다. 게다가 초기 사용자 공간에서 사용할 수 있는 작은 유닉스 유틸리티들의 집합도 갖는다: cpio, dash, fstype, [mkdir](https://ko.wikipedia.org/wiki/mkdir "wikilink"), [mknod](https://ko.wikipedia.org/wiki/장치_파일 "wikilink"), mount, nfsmount, run-init 등.\[5\] 대체 전략은 프로그램을 인자나 [심볼릭 링크를](../Page/심볼릭_링크.md "wikilink") 통해 결정하는 [비지박스](https://ko.wikipedia.org/wiki/비지박스 "wikilink") 같이 모든 것을 한 실행 파일 안에 포함하는 것이다.

## 같이 보기

  - 다른 [C 표준 라이브러리들](https://ko.wikipedia.org/wiki/C_표준_라이브러리 "wikilink")

<!-- end list -->

  - [Bionic libc](https://ko.wikipedia.org/wiki/Bionic "wikilink")
  - [dietlibc](https://ko.wikipedia.org/wiki/dietlibc "wikilink")
  - [EGLIBC](https://ko.wikipedia.org/wiki/임베디드_GLIBC "wikilink")
  - [glibc](https://ko.wikipedia.org/wiki/GNU_C_라이브러리 "wikilink")
  - [musl](https://ko.wikipedia.org/wiki/musl "wikilink")
  - [Newlib](https://ko.wikipedia.org/wiki/Newlib "wikilink")
  - [uClibc](https://ko.wikipedia.org/wiki/uClibc "wikilink")

## 각주

## 외부 링크

  - [Source archive](https://web.archive.org/web/20070107103708/http://ftp.kernel.org/pub/linux/libs/klibc/)
  - [Browsable development tree](http://www.kernel.org/git/?p=libs/klibc/klibc.git;a=summary)
  - [Mailing list](http://www.zytor.com/mailman/listinfo/klibc/)
  - [initramfs and where user space truly begins](http://lwn.net/Articles/191004/) - LWN, [Jonathan Corbet](../Page/LWN.net.md "wikilink"), July 11, 2006.

[분류:C 표준 라이브러리](https://ko.wikipedia.org/wiki/분류:C_표준_라이브러리 "wikilink") [분류:리눅스 커널의 인터페이스](https://ko.wikipedia.org/wiki/분류:리눅스_커널의_인터페이스 "wikilink") [분류:C로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C로_작성된_자유_소프트웨어 "wikilink") [분류:BSD 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:BSD_라이선스_소프트웨어 "wikilink") [분류:GPL 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:GPL_라이선스_소프트웨어 "wikilink") [분류:자유 라이브러리](https://ko.wikipedia.org/wiki/분류:자유_라이브러리 "wikilink")

1.  <http://free-electrons.com/kerneldoc/latest/early-userspace/README>
2.
3.
4.  [Debian Wheezy Klibc](http://packages.debian.org/source/wheezy/klibc).
5.