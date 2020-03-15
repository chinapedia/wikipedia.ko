> This article is converted from Wikipedia: [Libumem](https://ko.wikipedia.org/wiki/Libumem).


**Libumem**은 응용 프로그램 안에서 메모리 관리 버그를 찾아내는데 사용되는 라이브러리이다. [슬랩 얼로케이터](https://ko.wikipedia.org/wiki/슬랩_얼로케이터 "wikilink") 개념에 기반을 두고 있다. Libumem은 솔라리스 9 업데이트 3 이상부터 [솔라리스의](https://ko.wikipedia.org/wiki/솔라리스_\(운영_체제\) "wikilink") 표준적인 일부로 사용할 수 있다.

## 함수

이 라이브러리의 함수들은 [멀티스레드](https://ko.wikipedia.org/wiki/스레드 "wikilink") 응용 프로그램 지원과 더불어 빠르고 확장 가능한 객체 캐시 메모리 할당을 제공한다. [표준 malloc(3C) 계열의 함수](https://ko.wikipedia.org/wiki/C_동적_메모리_할당 "wikilink") 및 더 유연한 umem_alloc(3MALLOC) 계열 외에도 libumem은 umem_cache_create(3MALLOC)에서 기술되었듯이 강력한 객체 캐시 서비스들을 제공한다.\[1\]

libumem을 처음 시작하는 것은 쉽다. "libumem.so"에 대해 LD_PRELOAD를 설정하면 실행되는 프로그램은 libumem의 malloc(3C)과 free(3C) (또는 new 또는 delete)를 사용한다.\[2\] 이 슬랩 얼로케이터는 수많은 스레드의 수많은 CPU의 시스템을 위해 설계되어 있다. 네이티브 얼로케이터의 메모리 할당은 심각한 병목 현상을 일으킬 수 있다.

## 출처

  - [Portable Umem: An opensource effort to port libumem to other UNIX-like systems](http://labs.omniti.com/labs/portableumem)

[분류:오픈솔라리스](https://ko.wikipedia.org/wiki/분류:오픈솔라리스 "wikilink") [분류:솔라리스 소프트웨어](https://ko.wikipedia.org/wiki/분류:솔라리스_소프트웨어 "wikilink")

1.  [Memory Leak Detection with libumem](https://blogs.oracle.com/dlutz/entry/memory_leak_detection_with_libumem)
2.  [Adam Leventhal's Weblog](https://blogs.oracle.com/ahl/entry/solaris_10_top_11_20)