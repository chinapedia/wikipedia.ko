> This article is converted from Wikipedia: [Inotify](https://ko.wikipedia.org/wiki/Inotify).


**inotify**는 파일 시스템 이벤트 통보 기능을 제공해 주는 [리눅스 커널](https://ko.wikipedia.org/wiki/리눅스_커널 "wikilink") 서브시스템 중 하나이다. inotify는 존 맥컷챈()이 개발하였는데, 로버트 러브(Robert Love) 및 뒤이어 애이미 그리피스(Amy Griffis)의 도움을 받았다. [dnotify](https://ko.wikipedia.org/wiki/dnotify "wikilink")를 대체한다. inotify는 메인라인 커널에 2.6.13 버전부터 포함되었다. 그 전에도 [소프트웨어 패치를](https://ko.wikipedia.org/wiki/소프트웨어_패치 "wikilink") 통해서 사용이 가능하였다. inotify는 [파일 시스템의](https://ko.wikipedia.org/wiki/파일_시스템 "wikilink") 변경 사항을 알아내고, 커널에 의해 직접 응용 프로그램에 이러한 변경 사항들을 보고하기 위한 것이다.

Inotify는 [비이글과](https://ko.wikipedia.org/wiki/비이글_\(소프트웨어\) "wikilink") 같은 [데스크톱 검색](../Page/데스크톱_검색.md "wikilink") 유틸리티에 자주 이용된다. inotify를 쓰면, [파일 시스템의](https://ko.wikipedia.org/wiki/파일_시스템 "wikilink") 변경을 탐지하기 위하여 일정 주기마다 반복하여 파일 시스템을 탐색할 필요가 없이 변경된 파일들을 [리인덱싱](https://ko.wikipedia.org/wiki/인덱스_\(정보_기술\) "wikilink") 할 수 있으며, 그 덕분에 프로그램은 짧은 시간의 "변경부터 리인덱싱까지의 시간"()을 가질 수 있다. inotify는 그러한 유틸리티들로 하여금 비교적 적은 [CPU 시간만을](https://ko.wikipedia.org/wiki/CPU_시간 "wikilink") 사용하도록 해주며, 결국 inotify는 이러한 프로그램들로 하여금 훨씬 효율적인 방식을 사용할 수 있도록 해 준다.

inotify는 또한 [파일 탐색기와](../Page/파일_탐색기.md "wikilink") 같이 디렉터리 목록을 자동적으로 갱신하는 일에 쓰일 수 있다. 또한 설정 파일을 다시 읽어 들이는 일이나, 로그 변경, 백업, 동기화, 업로드 같은 일에 쓰일 수 있다.

## 장점

Inotify는 앞서 개발된 [dnotify](https://ko.wikipedia.org/wiki/dnotify "wikilink")에 비해 많은 장점을 가지고 있다. dnotify를 가지고서는 프로그램은 모니터링하는 각각의 디렉터리에 대해서 각각 하나씩의 [파일 서술자를](https://ko.wikipedia.org/wiki/파일_서술자 "wikilink") 사용했어야만 했다. 이 경우, 프로세스 당 파일 서술자의 개수가 한계에 다다를 수 있고, 또 그렇게 되면 일종의 [병목 (bottleneck)이](https://ko.wikipedia.org/wiki/병목_\(공학\) "wikilink") 되기 때문에 이것은 좋은 방법이 아니었다. dnotify는 제거 가능한 미디어(removable media)의 파일에 사용할 때에도 문제가 되었다. 파일 서술자 때문에 장치가 사용중(busy)인 상태가 되었으므로 장치가 해제(un-mount)될 수 없었다.

dnotify의 다른 단점은, 모니터(monitor)를 디렉터리 단위에서만 변경 가능하기 때문에, 세세한 제어가 불가능했다는 점이다. 프로그래머들은 Dnotify로부터 통지(notification)를 받았을 때, 무슨 일이 일어났는지 정확히 알기 위해서는 스태트(stat) 함수를 이용하고, 그 결과의 [캐시](https://ko.wikipedia.org/wiki/캐시 "wikilink")를 유지해야만 했으며, 디렉터리 안의 어떤 파일에서 변경이 일어났을 경우 새로운 스태트(stat) 스트럭쳐를 생성하고는 그것을 이미 캐시된 것과 비교해야만 했다.

inotify는 최소한의 파일 서술자만 사용하는 API를 쓰고 있다. 프로그래머들은 이미 널리 쓰이고 있는 select 및 poll 인터페이스를 이용하여 이를 사용할 수 있다. 이는 시그널 통지 방식을 채용하였던 [dnotify](https://ko.wikipedia.org/wiki/dnotify "wikilink")와 상반된다. 이 덕분에 기존의 select나 poll 기반 라이브러리(예. [Glib](https://ko.wikipedia.org/wiki/Glib "wikilink"))와의 통합이 쉬워졌다.

## 동작 방법

inotify는 inotify를 위해 특별히 고안된 일련의 [시스템 콜을](https://ko.wikipedia.org/wiki/시스템_콜 "wikilink") 이용하여 이용할 수 있다.

`int inotify_init ()`

inotify 인스턴스를 생성한다. 모든 이벤트를 읽어낼 수 있는 파일 서술자 하나를 반환한다.

`int inotify_add_watch (int fd, const char* pathname, int mask)`

pathname이 가리키는 inode에 대한 감시(watching)을 시작한다. mask에 포함된 이벤트에 대한 감시이다. (inotify 인스턴스 내에서) pathname이 가리키는 inode에 대해 고유한 감시 서술자(watch decriptor) 하나를 반환해준다. (참조: 여러 개의 pathname들이 동일한 inode/watch descriptor를 가리킬 수 있다.)

`int inotify_rm_watch (int fd, int wd)`

주어진 감시 서술자 wd에 대한 감시를 중단한다.

inotify가 올려주는 이벤트에는 다음과 같은 정보가 들어 있다:

| 인자       | 설명                                                        |
| -------- | --------------------------------------------------------- |
| `wd`     | 감시 서술자(watch descriptor )                                 |
| `mask`   | 이벤트 태그(event tag)                                         |
| `cookie` | `IN_MOVED_FROM` 및 `IN_MOVED_TO` 사이 동기화(일치)를 위한 쿠키(cookie) |
| `len`    | 이름 필드의 길이                                                 |
| `name`   | (부가요소) 이 이벤트와 관계된 파일 이름 (상위 디렉터리에 대해서 로컬 이름임.)            |

모니터될 수 있는 이벤트들은 예를 들어 다음과 같다:

  - `IN_ACCESS` - 파일의 마지막 접근
  - `IN_MODIFY` - 파일의 마지막 수정
  - `IN_ATTRIB` - 파일 속성의 변경
  - `IN_OPEN` 및 `IN_CLOSE` - 파일의 열기 혹은 닫기
  - `IN_MOVED_FROM` 및 `IN_MOVED_TO` - 파일이 이동(move)되거나 이름이 바뀜(rename)
  - `IN_DELETE` - 파일/디렉터리의 삭제
  - `IN_CREATE` - 파일/디렉터리의 생성
  - `IN_DELETE_SELF` - 모니터되는 파일 자체의 삭제

## 역사

  - 2005년 8월 - 2.6.13에 합병.
  - 2004년 7월 - [최초의 릴리즈 발표](http://groups.google.com/group/fa.linux.kernel/browse_thread/thread/6366aaa10cb23bcc/a54e97d545ad66fe)

## 같이 보기

  - [File alteration monitor](https://ko.wikipedia.org/wiki/File_alteration_monitor "wikilink")
  - [Gamin](https://ko.wikipedia.org/wiki/Gamin "wikilink")

## 외부 링크

  - [inotify-tools](http://inotify-tools.sourceforge.net) A suite of userland utilities, based on inotify, to watch and log modifications on files and directories

  - [Official inotify README](http://www.kernel.org/pub/linux/kernel/people/rml/inotify/README)

  - [Kernel Korner](http://www.linuxjournal.com/article/8478) - Intro to inotify by Robert Love (2005)

  - [LWN Article on Inotify](http://lwn.net/Articles/104343/) Watching filesystem events with inotify (partly out of date)

  - [IBM Article](http://www-128.ibm.com/developerworks/linux/library/l-inotify.html) Monitor Linux file system events with inotify (out of date)

  - [incron](http://incron.aiken.cz/) An inotify cron system. It works like a regular cron but handles filesystem events rather than time periods.

### 프로그래밍 API

  - [inotify-cxx](http://inotify-cxx.aiken.cz/) C++
  - [Linux::Inotify2](http://search.cpan.org/~mlehmann/Linux-Inotify2-1.1/Inotify2.pm) perl
  - [Pyinotify](https://web.archive.org/web/20071224004956/http://pyinotify.sourceforge.net/) python
  - [JNotify](http://jnotify.sourceforge.net/) java
  - [Ocaml Inotify](https://web.archive.org/web/20070707170610/http://tab.snarc.org/projects/ocaml_inotify/) Ocaml

[분류:리눅스](https://ko.wikipedia.org/wiki/분류:리눅스 "wikilink")