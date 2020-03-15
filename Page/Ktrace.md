> This article is converted from Wikipedia: [Ktrace](https://ko.wikipedia.org/wiki/Ktrace).


**ktrace**는 [디버그](https://ko.wikipedia.org/wiki/디버그 "wikilink")와 분석을 목적으로 [커널](https://ko.wikipedia.org/wiki/커널 "wikilink")과 프로그램 간 통신을 [추적하고](../Page/트레이싱.md "wikilink") 추적한 결과를 디스크에 덤프하는 [유틸리티](https://ko.wikipedia.org/wiki/유틸리티 "wikilink")의 하나로, 특정 버전의 [BSD](https://ko.wikipedia.org/wiki/BSD "wikilink")와 [맥 OS X에](https://ko.wikipedia.org/wiki/macOS "wikilink") 포함되어 있다. 추적 대상이 되는 커널 기능으로는 [시스템 호출](https://ko.wikipedia.org/wiki/시스템_호출 "wikilink"), namei 변환, [신호](../Page/유닉스_신호.md "wikilink") 처리, [입출력](https://ko.wikipedia.org/wiki/입출력 "wikilink") 등이 있다.\[1\]

ktrace는 훨씬 더 빠르다는 점을 제외하고는 [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink")의 [strace](https://ko.wikipedia.org/wiki/strace "wikilink")와 다소 비슷하다. strace의 경우 추적 대상이 되는 프로그램이 실행하는 모든 시스템 호출이 문맥 교환을 수반하지만 ktrace로 추적할 경우 커널이 실제로 수행하므로 추가적인 문맥 교환이 필요하지 않다.

ktrace가 생성하는 트레이스(기본값은 `ktrace.out`)는 **kdump** 유틸리티를 사용하여 인간이 읽을 수 있는 형태로 볼 수 있다.\[2\]

맥 OS X 10.5 이후로 ktrace는 [DTrace](../Page/DTrace.md "wikilink")로 대체된 상태이다.

## 같이 보기

  - [DTrace](../Page/DTrace.md "wikilink")
  - [Kdump](../Page/Kdump.md "wikilink")
  - [SystemTap](https://ko.wikipedia.org/wiki/SystemTap "wikilink")
  - [trace](https://ko.wikipedia.org/wiki/리눅스_트레이스_툴킷 "wikilink")

## 각주

[분류:유닉스 프로그래밍 도구](https://ko.wikipedia.org/wiki/분류:유닉스_프로그래밍_도구 "wikilink")

1.
2.