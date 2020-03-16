> This article is converted from Wikipedia: [Go \( \)](https://ko.wikipedia.org/wiki/Go_\(_\)).


[섬네일](https://ko.wikipedia.org/wiki/파일:Golang.png "wikilink") **Go**는 2009년 구글이 개발한\[1\] [프로그래밍 언어이다](../Page/프로그래밍_언어.md "wikilink"). [가비지 컬렉션](../Page/쓰레기_수집_\(컴퓨터_과학\).md "wikilink") 기능이 있고, [병행성](../Page/병행성.md "wikilink")(concurrent)을 잘 지원하는 컴파일 언어다.

Go의 초기 디자인은 2007년 9월 21일에 로버트 그리즈머, [롭 파이크](../Page/롭_파이크.md "wikilink"), [켄 톰슨이](https://ko.wikipedia.org/wiki/켄_톰슨 "wikilink") [인페르노 분산 운영체제와](../Page/인페르노_\(운영_체제\).md "wikilink") 관련된 작업을 하다가 시작되었다. 화이트 보드에 새로운 언어에 대한 스케치를 하면서 초기 20% 파트타임 프로젝트로 시작하였다가 2008년 1월 켄 톰슨이 C 코드를 만들어내는 컴파일러를 만들기 시작했고, 2008년 중반 풀타임 프로젝트로 승격되었다. 2008년 5월 [이안 테일러가](https://ko.wikipedia.org/wiki/이안_테일러 "wikilink") Go 스펙의 초안을 이용해서 GCC 프론트엔드를 만들기 시작했고, 2008년 말 러스 콕스가 참여하면서 프로토타입에서 실질적인 언어와 라이브러리들을 만들기 시작했다. 2009년 11월 10일에 [리눅스](../Page/리눅스.md "wikilink")와 [Mac OS X](https://ko.wikipedia.org/wiki/OS_X "wikilink") 플랫폼을 대상으로 공식 발표되었다. Go가 처음 런칭되었을 때는 실무적인 소프트웨어를 만들기에는 준비가 좀 덜 된 상태였지만, 2010년 5월 롭 파이크는 구글에서 실제로 사용되고 있는 부분이 있다고 공개적으로 알리게 되었다.

## 역사

2009년 11월에 Go가 발표되었다. 구글의 생산 시스템 중 일부 및 기타 기업들에 사용되고 있다. \[2\]

Go는 다른 언어의 긍정적인 특징들을 유지하면서 공통이 되는 문제들을 해결할 새로운 프로그래밍 언어를 설계하기 위해 구글의 엔지니어 Robert Griesemer, [롭 파이크](../Page/롭_파이크.md "wikilink"), [켄 톰프슨에](../Page/켄_톰프슨.md "wikilink") 의해 실험적으로 시작되었다. 이 새로운 언어는 다음의 기능을 포함할 작정이었다:\[3\]

  - 정적 타이핑 및 대형 시스템으로의 스케일 가능할 것 (마치 [자바와](../Page/자바_\(프로그래밍_언어\).md "wikilink") [C++](https://ko.wikipedia.org/wiki/C++ "wikilink")처럼)
  - 너무 많은 필수적인 키워드와 반복 없이도 [생산적이고](https://ko.wikipedia.org/wiki/프로그래밍_생산성 "wikilink") 가독성이 좋을 것\[4\] ([동적 언어와](https://ko.wikipedia.org/wiki/동적_언어 "wikilink") 같이 가벼움)
  - [통합 개발 환경이](../Page/통합_개발_환경.md "wikilink") 필요하지 않지만 지원도 가능할 것
  - 네트워킹 및 다중 처리를 지원할 것

나중의 인터뷰에서, 언어 설계자 3명 모두 자신들이 C++의 복잡성을 싫어하며 이로 인해 새로운 언어를 설계하는 계기가 되었다고 언급하였다.\[5\]\[6\]\[7\]

Go 1.0은 2012년 3월에 출시되었다.\[8\]

## 구현체

2개의 주요 구현체가 존재한다:

  - 구글의 Go 툴체인: [리눅스](../Page/리눅스.md "wikilink"), [BSD](../Page/BSD.md "wikilink"), [macOS](https://ko.wikipedia.org/wiki/macOS "wikilink"), [플랜 9](https://ko.wikipedia.org/wiki/플랜_9 "wikilink"), [윈도우](../Page/마이크로소프트_윈도우.md "wikilink"), (2015년 이후) 모바일 장치를 포함한 여러 플랫폼을 대상으로 한다.\[9\] 주요 Go 컴파일러는 버전 1.5에 [셀프 호스팅되었다](https://ko.wikipedia.org/wiki/셀프_호스팅 "wikilink").\[10\]
  - 2번째 컴파일러 gccgo는 [GCC](../Page/GNU_컴파일러_모음.md "wikilink") 프론트엔드이다.\[11\]\[12\]

GopherJS라는 이름의 3번째 Go 컴파일러\[13\]도 존재한다. GopherJS는 Go 코드를 [자바스크립트](../Page/자바스크립트.md "wikilink") 코드로 컴파일하며 Go가 [프론트엔드 개발에](https://ko.wikipedia.org/wiki/프론트엔드_웹_개발 "wikilink") 사용될 수 있게 한다.

## 언어 설계

Go의 문법은 대체로 C와 비슷하다: 코드 블록들은 중괄호로 둘러싸고 for, switch, if를 포함한 일반적인 제어구조를 가지고 있다. C와 다르게, 한 라인 끝의 세미콜론은 필수가 아닌 옵션이다. [변수 선언은](https://ko.wikipedia.org/wiki/변수_선언 "wikilink") 다르게 작성되고 대개 옵션이다. [형변환](https://ko.wikipedia.org/wiki/형변환 "wikilink")은 명시적으로 해야 한다. [병행성 프로그래밍을](https://ko.wikipedia.org/wiki/병행성_프로그래밍 "wikilink") 다루기 위해 *go*와 *select* 키워드가 사용된다. 새로운 타입은 map, [유니코드](../Page/유니코드.md "wikilink") 문자열, 배열 slice, 그리고 내부 쓰레드 통신을 위한 채널(channel)이 있다.

Go는 그리 좋지 않은 하드웨어에서도 빠르게 컴파일될 수 있도록 디자인되었다. Go는 가비지 컬렉션이 되는 언어이다. 병행성(concurrency)와 관련된 Go의 구조적인 규칙들(channel과 선택적인 channel input들)은 Tony Hoare의 [CSP로부터](https://ko.wikipedia.org/wiki/:en:Communicating_sequential_processes "wikilink") 가져온 것이다.

[C++](https://ko.wikipedia.org/wiki/C++ "wikilink")나 [자바에](../Page/자바_\(프로그래밍_언어\).md "wikilink") 있는 기능들 중 타입 상속, 제너릭, 표명(assertion), 메서드 오버로딩, 포인터 연산은 Go에서 포함하고 있지 않다. Go를 만들고 있는 개발자들은, 제너릭 등은 급하진 않지만 어느 시점에는 기능이 도입될 것이라고 한다.

### 병행성

Go를 이용해 프로그램들이 서로 소통하면서 상태를 공유하는 동시성(concurrency) 프로그램을 쉽게 만들 수 있다.\[14\]\[15\]\[16\] 동시성이란 [멀티쓰레딩](https://ko.wikipedia.org/wiki/멀티쓰레딩 "wikilink"), [병렬 컴퓨팅](../Page/병렬_컴퓨팅.md "wikilink") 뿐 아니라, 비동기성 입출력 또한 포함한다. 예를 들어, 이벤트 기반 서버와 같이, 데이터베이스나 네트워크 작업과 같이 시간이 많이 걸리는 연산을 하는 동안 프로그램이 다른 일을 하는 것을 말한다.\[17\]

## 목적

Go는 정적 타입 컴파일 언어의 효율성과 동적 언어처럼 쉬운 프로그래밍을 할 수 있도록 하는 것을 목표로 한다. 또다른 목적은:

  - 안전성 : 타입 안전성과 메모리 안전성
  - 병행성과 통신을 위한 훌륭한 지원
  - 효과적인 가비지 컬렉션
  - 빠른 [컴파일](https://ko.wikipedia.org/wiki/컴파일 "wikilink")

## 언어 도구

Go는 수많은 언어 배포판들과 동일한 종류의 디버깅, 테스트, 코드 검사 도구들을 포함하고 있다. 그 중에 Go 배포판은 다음을 포함한다:

  - `go build`: 소스 파일 자체의 정보만을 사용하여 Go 바이너리를 빌드한다. 별도의 makefile은 없다.
  - `go test`: 유닛 테스트 및 마이크로벤치마크
  - `go fmt`: 코드 서식 지정
  - `go get`: 원격 패키지의 검색 및 설치
  - `go vet`: 코드 내의 잠재적인 오류를 찾아내는 정적 분석기
  - `go run`: 코드를 빌드하고 실행하는 바로 가기
  - `godoc`: 문서를 표시. HTTP를 통해 문서 확인.
  - `gorename`: 변수, 함수 등을 형 안전(type-safe) 방식으로 이름 변경
  - `go generate`: 코드 생성기를 호출하는 표준 방식

프로파일링 및 디버깅 지원, 런타임 인스트루먼테이션(이를테면 가비지 컬렉션 일시 정지 등을 위해) 및 레이스 컨디션 테스터(race condition tester)도 포함한다.

## 예제

아래는 Go로 만든 Hello, World 프로그램이다.

``` go
package main

import "fmt"

func main() {
        fmt.Println("Hello, World")
}
```

Go는 `for` loop과 같은 경우 각 항목을 구분하는 용도로 세미콜론(;)을 사용하고 그 외에는 대부분 자동으로 세미콜론이 컴파일 시 들어가게 된다. 중요한 것은 `if`와 같은 경우 `if`가 있는 그 라인에 중괄호({)가 반드시 같이 들어가야 한다는 것이다.

### 병행의 예

``` go
package main

import (
    "fmt"
    "time"
)

func readword(ch chan string) {
    fmt.Println("Type a word, then hit Enter.")
    var word string
    fmt.Scanf("%s", &word)
    ch <- word
}

func timeout(t chan bool) {
    time.Sleep(5 * time.Second)
    t <- true
}

func main() {
    t := make(chan bool)
    go timeout(t)

    ch := make(chan string)
    go readword(ch)

    select {
    case word := <-ch:
        fmt.Println("Received", word)
    case <-t:
        fmt.Println("Timeout.")
    }
}
```

## Go를 사용하는 프로젝트

Go로 작성된 일부 저명한 [오픈 소스 소프트웨어는](../Page/오픈_소스_소프트웨어.md "wikilink") 다음과 같다:

  - [라이트닝 네트워크](https://ko.wikipedia.org/wiki/라이트닝_네트워크 "wikilink"): [비트코인](../Page/비트코인.md "wikilink") 네트워크.
  - [CockroachDB](https://ko.wikipedia.org/wiki/CockroachDB "wikilink"): SQL 데이터베이스.
  - [도커](../Page/도커_\(소프트웨어\).md "wikilink"): [리눅스](../Page/리눅스.md "wikilink") 컨테이너를 배치시키는 도구들의 집합
  - Doozer: 매니지드 호스팅 제공자 [헤로쿠](../Page/헤로쿠.md "wikilink")의 락 서비스
  - Geth 소프트웨어: [이더리움](../Page/이더리움.md "wikilink") 프로토콜 [블록체인](../Page/블록체인.md "wikilink") 기술을 이용한 golang 구현체로서, 전 세계 공유 컴퓨팅 플랫폼을 구현한다.\[18\]
  - Gogs: 셀프 호스팅 Git 서비스.\[19\]
  - [InfluxDB](https://ko.wikipedia.org/wiki/InfluxDB "wikilink"): 고가용성과 고성능 요구사항을 필요로 하는 오픈 소스 데이터베이스.
  - [Juju](https://ko.wikipedia.org/wiki/Juju "wikilink"): [캐노니컬](../Page/캐노니컬.md "wikilink")이 주관하는 서비스 오케스트레이션 도구. ([우분투](../Page/우분투_\(운영_체제\).md "wikilink") 리눅스의 패키저)
  - [Kubernetes](https://ko.wikipedia.org/wiki/Kubernetes "wikilink") 컨테이너 관리 소프트웨어
  - [오픈시프트](../Page/오픈시프트.md "wikilink"): 클라우드 컴퓨팅 플랫폼 ([레드햇](../Page/레드햇.md "wikilink")이 서비스함)
  - 패커(Packer): 여러 플랫폼을 대상으로 하나의 소스 구성을 통해 동일한 머신 이미지를 만드는 도구.
  - [스내피](https://ko.wikipedia.org/wiki/스내피 "wikilink")(Snappy): [우분투 터치용](../Page/우분투_터치.md "wikilink") 패키지 관리자 (캐노니컬 제작)
  - [Syncthing](https://ko.wikipedia.org/wiki/Syncthing "wikilink"): 오픈 소스 파일 동기화 클라이언트/서버 애플리케이션
  - [GitLab-runner](https://ko.wikipedia.org/wiki/GitLab-runner "wikilink"): 오픈 소스 CI/CD 애플리케이션.
  - 이더리움 (geth)

Go를 사용한 일부 저명한 [오픈 소스 소프트웨어](../Page/오픈_소스_소프트웨어.md "wikilink") 프레임워크는 다음과 같다:

  - [Beego](https://ko.wikipedia.org/wiki/Beego "wikilink"): 고성능 웹 프레임워크
  - [Martini](https://ko.wikipedia.org/wiki/Martini "wikilink"): 웹 애플리케이션/서비스용 패키지.
  - [고릴라](https://ko.wikipedia.org/wiki/고릴라_\(소프트웨어\) "wikilink"): Go용 웹 툴킷.
  - [Enduro/X ASG](https://ko.wikipedia.org/wiki/Enduro/X "wikilink"): 클러스터 미들웨어, 애플리케이션 서버, 분산 트랜잭션, 멀티 프로세싱 프레임워크.

이 밖에도 Go를 사용하는 저명한 기업 및 사이트는 다음과 같다(일반적으로 다른 언어와 함께 사용):\[20\]\[21\]

  - [AeroFS](https://ko.wikipedia.org/wiki/AeroFS "wikilink"): 프라이빗 클라우드 파일싱크 어플라이언트 제공자\[22\]
  - [Chango](https://ko.wikipedia.org/wiki/Chango "wikilink"): Go를 사용하는 프로그래머틱 광고 회사.\[23\]
  - [클라우드 파운드리](../Page/클라우드_파운드리.md "wikilink"): [PaaS](https://ko.wikipedia.org/wiki/PaaS "wikilink")
  - [클라우드플레어](https://ko.wikipedia.org/wiki/클라우드플레어 "wikilink")\[24\]\[25\]
  - [CoreOS](../Page/CoreOS.md "wikilink"): [도커](../Page/도커_\(소프트웨어\).md "wikilink") 컨테이너를 활용하는 리눅스 기반 운영 체제.\[26\]
  - [카우치베이스 서버](../Page/카우치베이스_서버.md "wikilink"): 쿼리 및 인덱싱 서비스 (Couchbase 서버 내)\[27\]
  - [드롭박스](../Page/드롭박스.md "wikilink"): 일부 중요한 구성 요소들을 파이썬에서 Go로 이관함.\[28\]
  - [구글](../Page/구글.md "wikilink")의 수많은 프로젝트: (download server dl.google.com 등)\[29\]\[30\]\[31\]
  - [MercadoLibre](https://ko.wikipedia.org/wiki/MercadoLibre "wikilink"): 여러 퍼블릭 API.
  - [몽고DB](../Page/몽고DB.md "wikilink"): MongoDB 인스턴스 관리 도구\[32\]
  - [넷플릭스](../Page/넷플릭스.md "wikilink"): 서버 아키텍처의 두 부분\[33\]
  - [노바티스](../Page/노바티스.md "wikilink"): 내부 인벤토리 시스템용\[34\]
  - [Plug.dj](https://ko.wikipedia.org/wiki/Plug.dj "wikilink"): 상호작용 온라인 소셜 뮤직 스트리밍 웹사이트.\[35\]
  - [Replicated](https://ko.wikipedia.org/wiki/Replicated "wikilink"): [도커](../Page/도커_\(소프트웨어\).md "wikilink") 기반 [PaaS](https://ko.wikipedia.org/wiki/PaaS "wikilink") (기업의 설치 가능 소프트웨어 제작용)\[36\]
  - [SendGrid](https://ko.wikipedia.org/wiki/SendGrid "wikilink")\[37\]
  - [사운드클라우드](../Page/사운드클라우드.md "wikilink"): 수십 개의 시스템용.\[38\]
  - [Splice](https://ko.wikipedia.org/wiki/Splice "wikilink")\[39\]
  - [ThoughtWorks](https://ko.wikipedia.org/wiki/ThoughtWorks "wikilink")\[40\]
  - [트위치](../Page/트위치.md "wikilink")\[41\]
  - [우버](../Page/우버.md "wikilink")\[42\]
  - [Zerodha](https://ko.wikipedia.org/wiki/Zerodha "wikilink")

## 각주

## 외부 링크

  -
  - [Go 언어 한국 커뮤니티 (GDG Korea Golang)](https://web.archive.org/web/20171002190450/https://golang.kr/)

  - [Golang Korea Google Plus 페이지](https://plus.google.com/u/0/b/112714242728066184635/112714242728066184635/posts)

  - [A Tour of Go (한국어)](http://go-tour-kr.appspot.com)

[분류:구글의 소프트웨어](https://ko.wikipedia.org/wiki/분류:구글의_소프트웨어 "wikilink") [분류:크로스 플랫폼 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_소프트웨어 "wikilink") [분류:절차적 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:절차적_프로그래밍_언어 "wikilink") [분류:미국의 발명품](https://ko.wikipedia.org/wiki/분류:미국의_발명품 "wikilink") [분류:2009년 개발된 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:2009년_개발된_프로그래밍_언어 "wikilink") [분류:C 프로그래밍 언어 계열](https://ko.wikipedia.org/wiki/분류:C_프로그래밍_언어_계열 "wikilink") [분류:시스템 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:시스템_프로그래밍_언어 "wikilink") [분류:BSD 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:BSD_라이선스_소프트웨어 "wikilink") [분류:크로스 플랫폼 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_자유_소프트웨어 "wikilink") [분류:자유 컴파일러와 인터프리터](https://ko.wikipedia.org/wiki/분류:자유_컴파일러와_인터프리터 "wikilink")

1.
2.
3.   [Video available](https://www.youtube.com/watch?v=7VcArS4Wpqk).
4.
5.
6.
7.
8.
9.
10.
11.
12.
13. <https://github.com/gopherjs/gopherjs>
14. [Share by communicating - Effective Go](http://golang.org/doc/effective_go.html#sharing)
15. Andrew Gerrand, [Share memory by communicating](http://blog.golang.org/share-memory-by-communicating)
16. Andrew Gerrand, [Codewalk: Share memory by communicating](http://golang.org/doc/codewalk/sharemem/)
17. 롭 파이크의 [Concurrency is not Parallelism](http://vimeo.com/49718712) 참고.
18.
19.
20. Erik Unger, [The Case For Go](https://gist.github.com/ungerik/3731476)
21. Andrew Gerrand, [Four years of Go](http://blog.golang.org/4years), The Go Blog
22.
23.
24. John Graham-Cumming, [Go at CloudFlare](http://blog.cloudflare.com/go-at-cloudflare)
25. John Graham-Cumming, [What we've been doing with Go](http://blog.cloudflare.com/what-weve-been-doing-with-go)
26.
27.
28. Patrick Lee, [Open Sourcing Our Go Libraries](https://tech.dropbox.com/2014/07/open-sourcing-our-go-libraries/), 7 July 2014.
29.
30. Matt Welsh, [Rewriting a Large Production System in Go](http://matt-welsh.blogspot.com/2013/08/rewriting-large-production-system-in-go.html)
31. David Symonds, [High Performance Apps on Google App Engine](http://talks.golang.org/2013/highperf.slide)
32.
33.
34.
35.
36.
37.
38. Peter Bourgon, [Go at SoundCloud](http://backstage.soundcloud.com/2012/07/go-at-soundcloud/)
39.
40.
41. Rhys Hiltner, [Go’s march to low-latency GC](https://blog.twitch.tv/gos-march-to-low-latency-gc-a6fa96f06eb7#.wykex6pkr), 5 July 2016.
42.