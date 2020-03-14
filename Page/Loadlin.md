> This article is converted from Wikipedia: [Loadlin](https://ko.wikipedia.org/wiki/Loadlin).


**loadlin**는 [도스](https://ko.wikipedia.org/wiki/도스 "wikilink")나 [마이크로소프트 윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") ([95](https://ko.wikipedia.org/wiki/윈도_95 "wikilink"), [98](https://ko.wikipedia.org/wiki/윈도_98 "wikilink"), [Me](https://ko.wikipedia.org/wiki/윈도_Me "wikilink") 전용) 환경에서 작동하는 [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink") [부트 로더이다](https://ko.wikipedia.org/wiki/부트_로더 "wikilink"). 이 로더는 리눅스 시스템을 읽거나 DOS/WINDOWS의 운영을 기존파일의 변환 없이 대체할 수 있다.

loadlin 과 [리눅스 커널](https://ko.wikipedia.org/wiki/리눅스_커널 "wikilink") 은 둘다 도스/윈도의 파일 시스템에서 접근 가능한 것들이다. 이것은 파일로부터 메모리 안의 [리눅스 커널을](https://ko.wikipedia.org/wiki/리눅스_커널 "wikilink") 불러온다. 이것은 또한 메모리안에 다양한 환경설정 매개변수로 위치해있고, 커널로의 이동을 통제한다. 커널이 도스/윈도를 완벽히 대체해 이 매개변수들을 읽어오고, 설정하고 실행할 수 있다.

선택적으로, 이것은 [RAM 디스크와](https://ko.wikipedia.org/wiki/RAM_디스크 "wikilink") 같이 리눅스커널로 이동을 통제하기 전의 메모리로 읽어진 내용들에 대해 커널의 지원을 설정할 수 있다. 이 로더는 RAM 디스크 와 그 안에 있는 커널 정보들을 넘겨줄 수도 있다. 게다가, 매개변수들은 자신들의 생성을 위해 루트파일 시스템으로 사용되는 [램 디스크에](https://ko.wikipedia.org/wiki/램_디스크 "wikilink") 넘겨질 수 도 있다. 파일 시스템 안의 스타트업 프로그램은 종종 리눅스의 또 하나의 파일 시스템을 증가시키는(아마 고정디스크)원인이 되며 그 루트파일 시스템로써의 사용으로 전환되다.

loadlin 개별 프로그램으로써 동작하며 [마스터 부트 기록을](https://ko.wikipedia.org/wiki/마스터_부트_기록 "wikilink") 수정할 수 없다, 이는 MBR의 수정(부트가 불가능한 시스템에서 읽어오는 것이 불분명하게나마 가능할 때) 에 대해 걱정되는 상황들에서 쓸모가 있다. 그것의 구조를 갖추기 위해, loadlin은 오직 도스 기반으로 움직이는 시스템에서만 작동하며, 윈도의 [NT](https://ko.wikipedia.org/wiki/윈도_NT "wikilink") 기반의 버전에서는 동작하지 않을 것이다.

## 같이 보기

  - [GNU GRUB](https://ko.wikipedia.org/wiki/GNU_GRUB "wikilink")
  - [SYSLINUX](https://ko.wikipedia.org/wiki/SYSLINUX "wikilink")
  - [WinKExec](https://ko.wikipedia.org/wiki/WinKExec "wikilink")

## 외부 링크

  - [HOWTO](http://tldp.org/HOWTO/Loadlin+Win95-98-ME.html) at the [Linux Documentation Project](https://ko.wikipedia.org/wiki/Linux_Documentation_Project "wikilink")
  - [HOWTO](http://tldp.org/HOWTO/Install-Strategies/x349.html) at the [Linux Documentation Project](https://ko.wikipedia.org/wiki/Linux_Documentation_Project "wikilink")

### 다운로드

  - <http://youpibouh.thefreecat.org/loadlin/>

[분류:부트 로더](https://ko.wikipedia.org/wiki/분류:부트_로더 "wikilink")