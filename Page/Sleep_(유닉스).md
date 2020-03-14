> This article is converted from Wikipedia: [Sleep \(\)](https://ko.wikipedia.org/wiki/Sleep_\(\)).


**sleep**은 지정된 시간 동안 프로그램 실행을 [유예시키는](https://ko.wikipedia.org/wiki/sleep_\(시스템_호출\) "wikilink") [유닉스](https://ko.wikipedia.org/wiki/유닉스 "wikilink") [명령 줄](https://ko.wikipedia.org/wiki/명령_줄 "wikilink") 프로그램이다. 이 sleep 명령은 적어도 지정된 초 (기본값), 분, 시간, 날 동안 호출 중인 프로세스를 유예한다.

## 사용법

``` bash
 sleep 숫자
```

숫자가 정수인 곳은 초 단위로 인지한다. 일부 구현체는 [부동소수점](https://ko.wikipedia.org/wiki/부동소수점 "wikilink") 숫자도 지원할 수 있다. 그 밖의 특별한 옵션은 없다.

## 예

``` bash
 sleep 5
```

현재의 터미널 세션을 5초 대기한다.

``` bash
 sleep 18000
```

현재의 터미널 세션을 5시간 대기한다.

## GNU sleep 예제

``` bash
 sleep 3h ; mplayer foo.mp3
```

3시간 대기 후 foo.mp3를 재생한다.

**`sleep 5h30m`**이나 **`sleep 5h 30m`**은 기본 문법에는 어긋나는데, 그 이유는 sleep은 기본적으로 오직 하나의 값과 단위만을 변수로 받기 때문이다. 그러나 **`sleep 5.5h`**는 허용된다. 다음과 같이 sleep을 연속하여 사용할 수도 있다.

``` bash
 sleep 5h; sleep 30m
```

위 명령은 5시간 sleep하고, 약 30분 간 sleep한다.

[GNU 프로젝트의](https://ko.wikipedia.org/wiki/GNU_프로젝트 "wikilink") sleep 구현체([coreutils](https://ko.wikipedia.org/wiki/coreutils "wikilink")의 일부)는 사용자가 여러 개의 변수를 받을 수 있게 하므로 sleep 5h 30m(시간과 분 사이 공백 필수)와 같은 명령은 [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink")를 포함한 GNU sleep을 사용하는 어떠한 시스템에서도 동작한다.

sleep의 용도로는 작업 스케줄링, 특정 프로세스 실행 지연, 공유 네트워크 연결 전 대기 등이 포함된다.

## 같이 보기

  - [sleep (시스템 호출)](https://ko.wikipedia.org/wiki/sleep_\(시스템_호출\) "wikilink")

## 외부 링크

  -
[분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink") [분류:유닉스 프로세스 및 작업 관리 관련 소프트웨어](https://ko.wikipedia.org/wiki/분류:유닉스_프로세스_및_작업_관리_관련_소프트웨어 "wikilink")