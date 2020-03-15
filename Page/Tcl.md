> This article is converted from Wikipedia: [Tcl](https://ko.wikipedia.org/wiki/Tcl).


[섬네일](https://ko.wikipedia.org/wiki/파일:Tcl.svg "wikilink") **Tcl** (원래 "Tool Command Language"에서 왔지만 관례적으로 "TCL"이 아니라 "Tcl"이라고 쓰며 "티클" 또는 "티씨엘"\[1\]로 발음한다.)은 [스크립트 언어로써](../Page/스크립트_언어.md "wikilink") 존 오스터하우트가 만들었다. 처음에 같이 일하던 프로그래머들이 응용 프로그램에 포함시키기 위한 (조악한) 언어를 직접 만들며 좌절하는 모습을 보고 만들었다고 하지만, Tcl은 빠르게 인기를 얻었다. 비교적 배우기 쉽다고 알려져 있지만 충분히 강력하다. 보통 [빠른 프로토타이핑](https://ko.wikipedia.org/wiki/빠른_프로토타이핑 "wikilink"), 스크립트 프로그램, GUI 및 테스팅에 많이 사용된다. 임베디드 플랫폼에서도 광범위하게 사용되며 Tcl 언어 전체 또는 그 작은 일부분만 떼어낸 버전을 이용하기도 한다. 또한 [CGI와](../Page/공용_게이트웨이_인터페이스.md "wikilink") [IRC 봇을](https://ko.wikipedia.org/wiki/IRC_봇 "wikilink") 만드는 데에도 사용되고 있다.

Tcl과 [Tk](https://ko.wikipedia.org/wiki/Tk_\(프레임워크\) "wikilink") [GUI 툴킷을](https://ko.wikipedia.org/wiki/위젯_툴킷 "wikilink") 묶어서 **Tcl/Tk**라고 자주 부른다.

## 특징

Tcl은 아래와 같은 특징이 있다:

  - 언어 구조를 포함해서 모든 것은 [명령어이며](https://ko.wikipedia.org/wiki/명령어_\(컴퓨팅\) "wikilink"), [전위 표기법으로](https://ko.wikipedia.org/wiki/전위_표기법 "wikilink") 표현한다.
  - 명령어는 [가변인자](https://ko.wikipedia.org/wiki/가변인자 "wikilink")를 받을 수 있다.
  - 모든 것을 동적으로 재정의하고 오버라이드할 수 있다.
  - [코드를](https://ko.wikipedia.org/wiki/부호_\(정보\) "wikilink") 포함한 모든 [자료형](../Page/자료형.md "wikilink")을 [문자열](https://ko.wikipedia.org/wiki/문자열 "wikilink")로 다룰 수 있다.
  - 극히 간단한 [문법](https://ko.wikipedia.org/wiki/문법_\(프로그래밍_언어\) "wikilink") 규칙.
  - [소켓과](https://ko.wikipedia.org/wiki/인터넷_소켓 "wikilink") [파일에](https://ko.wikipedia.org/wiki/컴퓨터_파일 "wikilink") 대해 [이벤트 구동 방식](https://ko.wikipedia.org/wiki/이벤트_구동_방식 "wikilink") 인터페이스를 가지고 있다. 시간 기반 이벤트 및 사용자 정의 이벤트가 모두 가능하다.
  - 유연한 [변수 영역](../Page/변수_영역.md "wikilink") 규칙을 지원해서, 정적 영역 규칙이 기본이지만 uplevel과 upvar는 proc이 둘러싸고있는 함수의 영역까지 작용할 수 있도록 허용한다.
  - 모든 명령어가 실행 후 반환하는 예외 코드를 이용한 간단한 예외 처리
  - Tcl에 정의된 모든 명령어는 잘못된 사용에 대해 의미있는 오류 메시지를 만들어낸다.
  - [C](https://ko.wikipedia.org/wiki/C_\(프로그래밍_언어\) "wikilink"), [C++](https://ko.wikipedia.org/wiki/C++ "wikilink"), [자바](https://ko.wikipedia.org/wiki/자바_\(프로그래밍_언어\) "wikilink") 및 Tcl을 통해 바로 확장할 수 있다.
  - [인터프리터](https://ko.wikipedia.org/wiki/인터프리터 "wikilink") 언어이지만 [바이트코드](../Page/바이트코드.md "wikilink")를 이용하여 동적인 수정이 가능한 특성을 유지하면서 속도가 빨라짐.
  - 1999년에 처음 출시한 완전한 [유니코드](https://ko.wikipedia.org/wiki/유니코드 "wikilink") (3.1) 지원.
  - 플랫폼 독립적: [Win32](https://ko.wikipedia.org/wiki/Win32 "wikilink"), [UNIX](https://ko.wikipedia.org/wiki/유닉스 "wikilink"), [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink"), [애플 매킨토시](https://ko.wikipedia.org/wiki/매킨토시 "wikilink"), 등.
  - 윈도([GUI](https://ko.wikipedia.org/wiki/그래픽_사용자_인터페이스 "wikilink")) 인터페이스 [Tk와](https://ko.wikipedia.org/wiki/Tk_\(프레임워크\) "wikilink") 밀접한 결합.
  - 코드를 관리하기 쉽다. 많은 경우 Tcl 스크립트는 다른 언어로 동일한 기능을 작성했을 때보다 더 작고 읽기 쉬운 코드가 된다.
  - 다양한 목적과 환경에서 사용된다: 텍스트 전용 스크립트 언어, 애플리케이션 프로그램을 위한 GUI 가능한 언어, (서버측 또는 [Tclets](https://ko.wikipedia.org/wiki/Tclets "wikilink")과 같이 클라이언트측) 웹페이지와 ([PostgreSQL](../Page/PostgreSQL.md "wikilink")과 같이 서버측) 데이터베이스를 위한 임베디드 언어 등.
  - 개발용 버전(예, ActiveState Tcl), tclkit (일종의 실행용 버전, 1 메가바이트밖에 안됨), starpack (단일 실행파일), BSD 라이선스의 자유로이 배포가능한 소스 등 여러가지로 존재한다.

Tcl은 원래 함수형 언어로써 [객체 지향](https://ko.wikipedia.org/wiki/객체_지향_프로그래밍 "wikilink") 문법을 지원하지는 않았다. 그러나 최근 버전은 XOTcl과 같이 객체 지향 기능을 제공하는 확장을 지원한다. incr Tcl, Snit, 및 STOOOP (simple tcl-only object-oriented programming)와 같은 다른 객체 지향 확장도 존재한다.

Tcl은 고차 함수와 함수 요약이 언어 자체에서 지원되므로 [함수형 프로그래밍은](https://ko.wikipedia.org/wiki/함수형_프로그래밍 "wikilink") 쉽게 가능하지만 그러한 목적으로 많이 쓰이지는 않는다. 아래 예는 쉽게 두 함수를 합성할 수 있음을 보여준다.

``` tcl
proc o {f g x} {$f [$g $x]}
```

## 예제

아래 예제는 아무 Tcl 셸에 붙여넣어도 실행 가능한 간단한 코드이다.

### 수 더하기

방법 (ㄱ) - 'foreach' 반복문을 이용하여 덧셈

``` tcl
set numbers {1 2 3 4 5 6 7 8 9 10}
set result 0
foreach number $numbers {
    set result [expr {$result + $number}]
}
puts $result
```

방법 (ㄴ) - 'join' 명령을 이용하여 훨씬 더 우아한 방법으로 덧셈

``` tcl
 set numbers {1 2 3 4 5 6 7 8 9 10}
 puts [expr [join $numbers +]]
```

방법 (ㄷ) - 더하기 명령을 리스트 펼치기 문법과 함께 사용

``` tcl
 namespace import tcl::mathop::+
 set numbers {1 2 3 4 5 6 7 8 9 10}
 puts [+ {*}$numbers]
```

### 메아리 서버

이벤트 기반 소켓 처리를 보여주는 잘 동작하는 간단한 예제

``` tcl
#!/usr/bin/env tclsh

# echo server that can handle multiple
# simultaneous connections.

proc newConnection { sock addr port } {

     # client connections will be handled in
     # line-buffered, non-blocking mode
     fconfigure $sock -blocking no -buffering line

     # call handleData when socket is readable
     fileevent $sock readable [ list handleData $sock ]
}

proc handleData { sock } {
     puts -nonewline $sock [ gets $sock ]
     if { [ eof $sock ] } {
        close $sock
     }
}

# handle all connections to port given
# as argument when server was invoked
# by calling newConnection
set port [ lindex $argv 0 ]
socket -server newConnection $port

# enter the event loop by waiting
# on a dummy variable that is otherwise
# unused.
vwait forever
```

### 전자 시계

Tk와 timer 이벤트를 이용하는 또다른 예제([A simple A/D clock](https://web.archive.org/web/20080906222256/http://wiki.tcl.tk/2563)). 네 줄의 코드로 전자 시계를 만든다.

``` tcl
package require Tk
proc every {ms body} {
    eval $body
    after $ms [list every $ms $body]
}
pack [label .clock -textvar time]
every 1000 {set ::time [clock format [clock seconds] -format %H:%M:%S]} ;# RS
```

설명: 첫 번째 줄은 Tk 패키지를 불러들인다. (실제로는 4줄에 걸쳐있는) 두 번째 줄은 액션('body')를 매 'ms' 밀리초마다 반복해서 실행하는 명령어 "every"를 정의하고, 세 번째 줄은 변수 'time'에 연동되는 라벨을 만들고 스크린에 출력되도록 한다. 네 번째 줄은 매 초마다 변수 'time'이 형식이 갖춰진 지역 시간으로 갱신되도록 한다.

## 각주

<references/>

## 외부 링크

  -
[분류:스크립트 언어](https://ko.wikipedia.org/wiki/분류:스크립트_언어 "wikilink") [분류:1988년 개발된 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:1988년_개발된_프로그래밍_언어 "wikilink") [분류:C로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C로_작성된_자유_소프트웨어 "wikilink") [분류:크로스 플랫폼 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_자유_소프트웨어 "wikilink") [분류:자유 컴파일러와 인터프리터](https://ko.wikipedia.org/wiki/분류:자유_컴파일러와_인터프리터 "wikilink")

1.  *Tcler's Wiki [Tcl vs. TCL](http://wiki.tcl.tk/11902) *