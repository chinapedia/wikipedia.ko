> This article is converted from Wikipedia: [Supercollider](https://ko.wikipedia.org/wiki/Supercollider).


**슈퍼콜라이더**()는 음악작곡, 오디오 신디시스를 위해 1996년 James McCartney에 의해 최초로 개발된 프로그래밍 언어 및 오디오엔진이다.

Smalltalk 및 Ruby 언어 등에 영향을 받은 강력한 고수준의 문법과 소리생성, 제어를 위한 다양한 Ugen들을 제공하여 현재 Max/MSP, Pd등과 함께 가장 널리 사용되는 전자음악 도구가 되었다.

시작버젼은 MacOSX를 중심으로 개발되었으나 (GUI, IDE등이 OSX 전용 개발 프레임워크를 사용), 현재는 다양한 플랫폼에서 동일한 프로그래밍 환경을 제공하는 크로스플랫폼 어플리케이션으로 진화하였다.

2018-10-31기준으로 최신 버전은 3.9.3으로 2018-4-8일에 수정되었으며 <http://supercollider.github.io를> 통해 다운로드할 수 있다.

<http://sccode.org> 와 <https://github.com/supercollider/supercollider> 에는 유저들의 다양한 예제 코드들이 공유되고 있으며,여러 프로그래밍 방법론들을 통해 유저마다 각자만의 사용하는 방식들이 존재함을 알 수 있다.

SuperCollider는 GPL v3 기반의 완전한 오픈소스 프로그램으로, 공식적으로 배포되는 어플리케이션 외에 여러가지 사용 환경(IDE,언어)들이 존재한다.

**SuperCollider를 통해서 할 수 있는 것**

  - 소리합성
  - 전자/컴퓨터음악 작곡 (테잎음악, 라이브 일렉트로닉 음악)
  - 사용자 그래픽 인터페이스(GUI) 구축
  - Plug-in 설계
  - 2D 그래픽 작업
  - 다른 언어 또는 어플리케이션(예, MaxMSP, Processing 등)과 OSC(Open Sound Control) 또는 MIDI 신호로 소통
  - 외부 기기(예, Arduino, 신디사이저, 미디 콘트롤러, Wii 등)를 이용한 실시간 제어

## 아키텍쳐

SC의 환경은 버전 3부터 2가지 요소로 구성되었다: Scsynth(server) , sclang(client).(위의 구성은 OSC(Open Sound Control)와 상호 통신한다.) SuperCollider는 기본적으로 오디오엔진(소리합성)을 담당하는 scsynth(server)와 그 엔진을 제어하는 sclang(client)로 구성되어 있으며 서로 간에 OSC(OpenSoundControl) 프로토콜을 통해 제어 메시지 및 데이터를 주고 받다. 최근엔 Shared memory interface를 지원하여 서버와 클라이언트가 같은 머쉰안에 존재한다면 메모리르 통해 컨트롤 값 및 오디오데이터(forScope)를 빠르게 주고 받을 수 있다.

### SuperCollider 합성 서버(scsynth)

SuperCollider의 사운드 생성은 최적화된 명령 행 실행 파일(scsynth)에 번들로 제공된다. 대부분의 경우 SuperCollider 프로그래밍 언어 내에서 제어되지만 독립적으로 사용할 수 있다. 오디오 서버에는 다음과 같은 기능이 있다.

  - 열린 소리 제어 액세스
  - 간단한 ANSI C 및 C ++ 11 플러그인 API
  - 대용량 멀티 채널 셋업을 포함하여 다양한 수의 입출력 채널 지원
  - 실행 순서를 정의하는 합성 노드 의 순서화 된 트리 구조에 대한 액세스를 제공한다.
  - 신호 흐름을 동적으로 재구성 할 수있는 버스 시스템
  - 쓰기 및 읽기 용 버퍼
  - 필요에 따라 다른 요율로 계산: 오디오 속도, 제어 속도, 요구율
  - 서버 아키텍처의 독립적 인 구현 인 Supernova는 합성 노드의 명시적인 병렬 그룹화를 통해 다중 프로세서 지원을 추가한다.

### SuperCollider 프로그래밍 언어 ( sclang )

sclang에서 사용자가 쓰는 인간의 언어란 프로그래밍 언어를 지칭하는 것으로서, 실제 인간의 언어 또는 사고 체계와 비슷한 체계를 가지는 객체지향(OOP, Object-oriented Programming)이라는 특징을 가진 언어이며, 매우 다양한 표현 능력을 우리에게 제공한다. 이것을 높은 레벨(high-level)의 언어라고 한다. 이것은 sclang의 해석기에 의해 OSC 메시지 형태로 해석되는데, 이것을 낮은 레벨(low-level)의 언어라고 한다.

sclang은 이 두 가지 언어를 모두 다룰 수 있게 해 준다. 즉, 우리는 OOP의 높은 레벨의 언어를 이용해서 주문서를 작성할 수도 있고, 또는 .sendMsg 또는 다른 비슷한 단어들을 이용해서 낮은 레벨인 OSC 메시지의 형태로 서버에 직접 전달할 수도 있다. 우리가 흔히 사용하는 방법은 당연히 OOP의 풍부한 문법을 이용하는 높은 레벨의 언어이며, 특정 경우에는 OSC 메시지 형태를 사용하는것이 더 편리할 때도 있다. (예를 들어, 단순 플레이 후 스스로 할당에서 제외해야 하는 수많은 그레인들을 만들 때.)

### GUI 시스템

ixiQuarks GUI 도구를 실행하는 SuperCollider의 스크린 샷

[400px](https://ko.wikipedia.org/wiki/파일:IxiQuarks.jpg "wikilink")

## 인터페이스 및 시스템 지원

### 클라이언트

서버는 [OSC(Open Sound Control)를](https://ko.wikipedia.org/wiki/OSC\(Open_Sound_Control\) "wikilink") 사용하여 제어되기 때문에 다양한 응용 프로그램을 사용하여 서버를 제어 할 수 있다. SuperCollider의 언어 환경이 일반적으로 사용되지만 Pure Data와 같은 다른 OSC 인식 시스템을 사용할 수 있다.

SuperCollider 서버에대한 “타사” 클라이언트가 존재한다. 여기에는 Haskell, ScalaCollider, Scala기반의 Scheme 클라이언트인 [hsc3](https://ko.wikipedia.org/wiki/hsc3 "wikilink"), [Clojure](https://ko.wikipedia.org/wiki/Clojure "wikilink") 및 [Sonic Pi를](https://ko.wikipedia.org/wiki/Sonic_Pi "wikilink") 기반으로 한 [Scala](https://ko.wikipedia.org/wiki/Scala "wikilink"), [Overtone](https://ko.wikipedia.org/wiki/Overtone "wikilink")을 기반으로 하는 [rs3](https://ko.wikipedia.org/wiki/rs3 "wikilink")가 있다. 이것들은 SuperCollider의 프로그래밍언어에 대한 인터페이스를 제공하지 않기 때문에 밑에 언급하게 될 개발환경과 구별된다. 대신 오디오 서버와 직접 통신하고 사용자 표현을 용이하게 하는 고유한 방식을 제공한다.

  - [Pure Data](https://ko.wikipedia.org/wiki/Pure_Data "wikilink"): 대화형 컴퓨터 음악 및 멀티미디어 작품 제작을 위해 개발된 시각적 프로그래밍언어
  - [Haskell](https://ko.wikipedia.org/wiki/Haskell "wikilink"): 정적 타이핑을 가진 프로그래밍 언어

#### 서버 구조의 장점과 단점

##### 장점

  - [안정성](https://ko.wikipedia.org/wiki/안정성 "wikilink"): 클라이언트가 붕괴되어도 서버는 일을 계속한다. 즉, 소리는 계속 발생한다. 이것은 라이브 상황에서 중요하다. 반대로, 서버 또한 클라이언트로부터 독립해서 붕괴할 수 있다.
  - [모듈방식](https://ko.wikipedia.org/wiki/모듈방식 "wikilink"): 모듈이란 서로 의존적이지만, 다분히 독립적인 개체들을 말한다. SC에 있어 합성과 제어는 서로 다른 것이다. 합성은 scsynth가 하고, 제어는 sclang 뿐 아니라 다른 프로그램들도 클라이언트가 되어 scsynth를 제어할 수 있다.
  - [원격제어](https://ko.wikipedia.org/wiki/원격제어 "wikilink"): 클라이언트 / 서버는 본인 컴퓨터의 외부에, 예를 들어 인터넷을 통해 존재할 수 있다.

##### 단점

  - [대기시간(latency)](https://ko.wikipedia.org/wiki/대기시간\(latency\) "wikilink"): 메시지를 보내는 과정에서 약간의 대기시간이 발생한다. 이것은 메시지를 보내는 쪽과 그것을 받아서 행동하는 다른 쪽 사이에서 발생하는 것으로서 일반적으로는 매우 작은 시간이며 크게 중요하게 작용하지 않는다. 이것은 'internal' 서버를 사용함으로써 더 적게 만들 수 있다.
  - [비동시적 실행(asynchronous execution)](https://ko.wikipedia.org/wiki/비동시적_실행\(asynchronous_execution\) "wikilink"): 클라이언트에서 서버에 명령을 했을 때 서버에서 그 명령을 실행시키는 데에 상당 시간이 걸리는 경우가 있다. 예를 들면, 큰 사운드 파일을 처리하게 하거나, 버퍼(Buffer)를 마련한다거나, SynthDef를 서버에 등록한다거나, 컨트롤 버스에 값을 정하거나 불러올 때 등이 이에 해당한다.

더 구체적으로 예를 들면, 버퍼를 하나 마련해서 큰 사운드파일을 거기에 불러오게 한 후 그 버퍼의 내용을 가지고 소리를 만들고자 할 경우, 버퍼 마련과 사운드파일을 그 버퍼에 불러오는 데에 시간이 걸리기 때문에, 즉시 그 버퍼를 가지고 처리를 하려고 하면, 내용이 아직 없는 관계로 에러가 나게 된다. 그럴 경우에는 버퍼 준비가 끝났다는 것을 서버가 클라이언트 측으로 다시 메시지를 보내올 필요가 있고, 그렇게 서버로 부터 연락이 왔을 때 일을 시작하게끔 해야 한다. 그러한 비동시적이라는 문제를 해결하기 위해서 많은 경우 action, comletionMessage가 아규멘트로 마련되어 있고, 또는 의도적으로 시간을 지연 시켜서 처리하게 한다.

### 지원되는 운영체제

[thumb](https://ko.wikipedia.org/wiki/파일:SuperCollider_screenshot2.jpg "wikilink") SuperCollider는 [macOS](https://ko.wikipedia.org/wiki/macOS "wikilink"), [Linux](https://ko.wikipedia.org/wiki/Linux "wikilink"), [Windows](https://ko.wikipedia.org/wiki/Windows "wikilink"), [FreeBSD](https://ko.wikipedia.org/wiki/FreeBSD "wikilink") 및 [OpenSUSE](https://ko.wikipedia.org/wiki/OpenSUSE "wikilink")에서 실행된다. 각 운영체제에는 SuperCollider와 함께 사용할 수 있는 여러 가지 언어 편집환경과 클라이언트가 있다. SuperCollider는 [Android](https://ko.wikipedia.org/wiki/Android "wikilink") 및 [iOS](https://ko.wikipedia.org/wiki/iOS "wikilink")에서 실행이 가능한다.

### 편집 환경

[thumb](https://ko.wikipedia.org/wiki/파일:Puredyne-supercollider-eee.png "wikilink") SuperCollider 코드는 자신의 [IDE](https://ko.wikipedia.org/wiki/IDE "wikilink")([Linux](https://ko.wikipedia.org/wiki/Linux "wikilink"), [Mac](https://ko.wikipedia.org/wiki/Mac "wikilink") 및 [Windows](https://ko.wikipedia.org/wiki/Windows "wikilink")를 지원)내에서 가장 일반적으로 편집되고 사용된다. SuperCollider를 지원하는 다른 개발환경은 다음과 같다.

  - Emacs ([Linux](https://ko.wikipedia.org/wiki/Linux "wikilink"), [Mac](https://ko.wikipedia.org/wiki/Mac "wikilink"), [Windows](https://ko.wikipedia.org/wiki/Windows "wikilink"))
  - Vim ([Linux](https://ko.wikipedia.org/wiki/Linux "wikilink"), [Mac](https://ko.wikipedia.org/wiki/Mac "wikilink"))
  - Atom ([Linux](https://ko.wikipedia.org/wiki/Linux "wikilink"), [Mac](https://ko.wikipedia.org/wiki/Mac "wikilink"), [Windows](https://ko.wikipedia.org/wiki/Windows "wikilink"))
  - gedit ([Linux](https://ko.wikipedia.org/wiki/Linux "wikilink"), [Windows](https://ko.wikipedia.org/wiki/Windows "wikilink"))
  - Kate ([Linux](https://ko.wikipedia.org/wiki/Linux "wikilink"))

## 코드예제

``` sc
// Print "Hello world!"
"Hello world!".postln;
```

``` sc
// Play a mixture of an 800 Hz sine tone and pink noise
{ SinOsc.ar(800, 0, 0.1) + PinkNoise.ar(0.01) }.play;
```

``` sc
// Modulate a sine frequency and a noise amplitude with another sine
// whose frequency depends on the horizontal mouse pointer position
{
    var x = SinOsc.ar(MouseX.kr(1, 100));
    SinOsc.ar(300 * x + 800, 0, 0.1)
    + PinkNoise.ar(0.1 * x + 0.1)
}.play;
```

``` sc
// List iteration: multiply the elements of a collection by their indices
[1, 2, 5, 10, -3].collect { |elem, idx| elem * idx };
```

``` sc
// Factorial function
f = { |x| if(x == 0) { 1 } { f.(x-1) * x } };
```

## 서버 사용하는 방법

### 주요 인스턴스 변수/메쏘드

  - s.boot; // 서버 부팅(켜기).
  - s.quit; // 서버 끄기.
  - s.reboot; // 서버 재부팅(다시 켜기).
  - s.waitForBoot{ "Hi, SuperCollider".speak }; // 부트 시키고 부트되자마자 함수 실행.
  - s.doWhenBooted{ "Hi, SuperCollider".speak }; // 부트 됐는지 확인해서 함수 실행. 자체 부트 기능 없음.
  - s.freeAll; // 서버의 모든 노드들 해제하기.
  - s.options; // 이 서버에 적용된 ServerOptions의 인스턴스.
  - s.ping; // 서버와 클라이언트 사이의 메시지 주고받는 데에 걸리는 시간.
  - s.dumpOSC(1); // 현재 서버와 클라이언트 사이에 주고받는 메시지 도청.
  - s.dumpOSC(0); // 현재 서버와 클라이언트 사이에 주고받는 메시지 도청 끄기.
  - s.queryAllNodes; // 서버의 현재 노드트리를 포스트창 찍기.
  - s.volume; // 이 서버에 적용된 Volume 의 인스턴스. 서버 전체 소리에 적용되는 볼륨 설정.
  - s.mute; // 서버 뮤트시키기.
  - s.unmute; // 서버 뮤트 해제하기.
  - s.inputBus; // 서버의 인풋 버스의 넘버와 개수를 나타내는 Bus의 인스턴스.
  - s.outputBus; // 서버의 아웃풋 버스의 넘버와 개수를 나타내는 Bus의 인스턴스.
  - s.peakCPU; // 서버가 사용하는 CPU의 최대 점유율.
  - s.avgCPU; // 서버가 사용하는 CPU의 평균 점유율.
  - s.numSynths; // 현재 작동 중인 Synth 노드 개수.
  - s.numGroups; // 현재 작동 중인 Group 노드 개수. 기본적으로 0번과 1번 그룹 2개.
  - s.numUGens; // 현재 소리를 만들기 위해 사용되고 있는 UGen들의 총 개수.
  - s.numSynthDefs; // 현재 서버에 등록된 SynthDef 들의 개수.
  - s.pid; // 서버의 프로세스 ID. internal 서버는 해당없음.
  - s.defaultGroup; // 서버의 디폴트 그룹.

[주의](https://ko.wikipedia.org/wiki/주의 "wikilink") : 서버를 부팅했는데, 사용자가 원하는 오디오 인터페이스로 부팅이 안될 때에는 시스템의 오디오 디폴트 장치를 바꿔줘야 한다. OSX 에서는 "Audio MIDI Setup.app" 또는 "System Preferences"의 "Sound"에서 인/아웃풋 장치를 바꿔준 후에 서버를 재부팅해야 한다. 또는 "Alt+메뉴바의 스피커 클릭"을 통해서도 인/아웃풋 장치를 바꿀 수 있다.

### GUI 관련 인스턴스 메쏘드

  - s.makeWindow; // 서버 전용 GUI 열기.
  - s.scope; // 파형 보기.
  - s.freqscope; // 스펙트럼 보기.
  - s.plotTree; // 서버의 현재 노트트리를 그래픽적으로 보기.
  - s.meter; // 레벨미터 보기.

### 주요 클래스 변수/메쏘드

  - Server.all; // 현재 생성된 모든 서버의 목록 보기.
  - Server.allRunningServers; // 현재 켜져 있는 서버의 목록 보기.
  - Server.quitAll; // 모든 등록된 서버(Server.all로 확인되는 서버) 끄기.
  - Server.killAll; // 모든 서버 강제로 끄기.
  - Server.freeAll; // 등록된 서버들의 모든 노드들 해제하기.

### 소리내기

  - s.boot;

{SinOsc.ar(440, mul: 0.2)}.play(s); // Function.play의 첫째 아규멘트는 타겟으로서 저 소리(node)가 만들어지는 서버 또는 그룹을 지정할 수 있다. 아무것도 지정 안 하면 디폴트 서버의 디폴트 그룹에서 생성된다.

  - Server.internal.boot;

{SinOsc.ar(440, mul: 0.2)}.play(Server.internal); // internal 서버로 소리 생성

## 오류 메시지 설명

다음을 실행하면 포스트창에 오류 메시지가 뜬다.

100.babo(10); // 이 줄에 커서를 위치시키고, 'Shift + backspace'

일반적인 오류 메시지는 크게 세 부분 또는 네 부분으로 되어 있고 위에서부터 다음의 순서로 되어 있다.

  - ERROR: 축약적으로 설명한 한 줄짜리 오류 내용.

<!-- end list -->

  - RECEIVER: 오류를 일으킨 메소드를 받은 리시버의 모든 내용(덤프).

<!-- end list -->

  - ARGS: 오류를 일으킨 메소드의 아규멘트. (내용이 없는 경우도 있음.)

<!-- end list -->

  - CALL STACK: 컴퓨터가 실행을 시작한 후 오류가 일어난 지점까지의 구체적인 모든 내용(덤프). 위에 쓰여진 내용이 가장 최근의 실행 내용이고, 제일 아래가 실행 초기의 내용이다. 그러므로 아래에서부터 위의 방향으로 컴퓨터의 시간적인 작업 내용을 추적해야 한다.

또는, 다음과 같이 단순한 기호누락이거나, 정의가 안된 변수를 쓰는 경우에 점(•)으로 문법적인 오류를 지적해 준다.

{SinOsc.ar(500, 0 0.3)}.play;

포스트 창에 뜨는 오류 메시지 중에 다음 부분이 있는데, 이것은 점이 있는 앞 부분에 문법적인 문제가 있음을 표현하는 것이다.

여기에서는 쉼표(,)가 빠졌음을 표시해 주고 있다.

{SinOsc.ar(500, 0 0.3•)}.play;

## 유용한 단축키

### MAC

  - 선택된 코드 실행: 'Shift + return', 'fn + return', 'control + return', 'control + c'
  - 괄호 안 영역 설정: 'Shift + Cmd + b'
  - 소리멈춤, 노드프리, 클럭멈춤: 'Cmd + .'
  - 헬프파일: 클래스명 영역 선택 후 'Cmd + d'
  - post 창 깨끗이 하기: 'Shift + Cmd + c'
  - 라이브러리 재컴파일(SC를 껐다가 다시 시작하는 효과): 'Cmd + k'
  - 클래스 소스파일(.sc) 오픈: 클래스명 영역 선택 후 'Cmd + y', 'Cmd + j'
  - 메시지(메소드, 클래스변수, 인스턴스변수)가 정의된 클래스 목록: 메시지 선택 후 'Cmd + y'
  - 특정 클래스 또는 메시지가 다른 어떤 클래스나 메소드 정의에서 사용되었는지에 관한 목록: 클래스 또는 메시지 선택 후 'Cmd + Shift + y'
  - 코드 내의 단어별 색깔화: 'Cmd + ' (작은 따옴표)'
  - 영역 코맨트화: 영역 설정 후 'Cmd + /'
  - 영역 코맨트 해제: 영역 설정 후 'Cmd + Alt + /'
  - 영역 전체 오른쪽으로 한 탭 이동: 영역 설정 후 'Cmd + \]'
  - 영역 전체 왼쪽으로 한 탭 이동: 영역 설정 후 'Cmd + \['

### Windows

  - 선택된 코드 실행: 'Shift + backspace', 'Fn + backspace', 'control + backspace', 'control + c'
  - 괄호 안 영역 설정: 'Shift + Windows + b'
  - 소리멈춤, 노드프리, 클럭멈춤: 'Windows + .'
  - 헬프파일: 클래스명 영역 선택 후 'Windows + d'
  - post 창 깨끗이 하기: 'Shift + Windows + c'
  - 라이브러리 재컴파일(SC를 껐다가 다시 시작하는 효과): 'Windows + k'
  - 클래스 소스파일(.sc) 오픈: 클래스명 영역 선택 후 'Windows + y', 'Windows + j'
  - 메시지(메소드, 클래스변수, 인스턴스변수)가 정의된 클래스 목록: 메시지 선택 후 'Windows + y'
  - 특정 클래스 또는 메시지가 다른 어떤 클래스나 메소드 정의에서 사용되었는지에 관한 목록: 클래스 또는 메시지 선택 후 'Windows + Shift + y'
  - 코드 내의 단어별 색깔화: 'Windows + ' (작은 따옴표)'
  - 영역 코맨트화: 영역 설정 후 'Windows + /'
  - 영역 코맨트 해제: 영역 설정 후 'Windows + Alt + /'
  - 영역 전체 오른쪽으로 한 탭 이동: 영역 설정 후 'Windows + \]'
  - 영역 전체 왼쪽으로 한 탭 이동: 영역 설정 후 'Windows + \['

## 외부 링크

  -
  - [SuperCollider users mailing list](https://web.archive.org/web/20081015155331/http://www.beast.bham.ac.uk/research/sc_mailing_lists.shtml)

  - [Workshop on SuperCollider](https://web.archive.org/web/20110820003031/http://www.informatics.sussex.ac.uk/users/nc81/courses/cm1/workshop.html) by Nick Collins

  - [SuperCollider Online Help](http://doc.sccode.org)

  - [해외 커뮤니티(페이스북)](https://www.facebook.com/groups/2222754532/)

  - [국내 커뮤니티(페이스북)](https://www.facebook.com/groups/soundartlab/)

  - [국내 네이버 카페](http://cafe.naver.com/supercollider)

  - [James McCartney의 홈페이지](http://www.audiosynth.com/)

[분류:2002년 소프트웨어](https://ko.wikipedia.org/wiki/분류:2002년_소프트웨어 "wikilink") [분류:객체 지향 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:객체_지향_프로그래밍_언어 "wikilink") [분류:소프트웨어 신시사이저](https://ko.wikipedia.org/wiki/분류:소프트웨어_신시사이저 "wikilink")