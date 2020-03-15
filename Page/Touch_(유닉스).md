> This article is converted from Wikipedia: [Touch \(\)](https://ko.wikipedia.org/wiki/Touch_\(\)).


**touch**는 [파일의](https://ko.wikipedia.org/wiki/컴퓨터_파일 "wikilink") 접근이나 [타임스탬프의](https://ko.wikipedia.org/wiki/시스템_타임 "wikilink") 형식을 변경하는 데 사용되는 표준 [유닉스](https://ko.wikipedia.org/wiki/유닉스 "wikilink") [프로그램이다](https://ko.wikipedia.org/wiki/컴퓨터_프로그램 "wikilink"). 또한 이것은 새로운 빈 파일을 만드는 데 사용된다.

## 역사

터치 유틸리티는 AT\&T 유닉스 버전7에서 처음 선보였다. [GNU](https://ko.wikipedia.org/wiki/GNU "wikilink") [coreutils](https://ko.wikipedia.org/wiki/coreutils "wikilink")에 포함된 `touch`의 버전은 [Paul Rubin](https://ko.wikipedia.org/wiki/Paul_Rubin "wikilink"), [Arnold Robbins](https://ko.wikipedia.org/wiki/Arnold_Robbins "wikilink"), [Jim Kingdon](https://ko.wikipedia.org/wiki/Jim_Kingdon "wikilink"), [데이비드 맥켄지](https://ko.wikipedia.org/wiki/데이비드_맥켄지_\(프로그래머\) "wikilink") 그리고 [Sunil Sharma가](https://ko.wikipedia.org/wiki/Sunil_Sharma "wikilink") 사용하였다.

## 명세

[단일 유닉스 규격](../Page/단일_유닉스_규격.md "wikilink")(SUS)은 `touch`가 파일의 접근 시간이나 변경 시간, 혹은 둘 모두를 변경해야 한다고 명시한다. 파일은 단일 인수로 제공 되는 경로명에 의해 식별된다. 또한 만일 식별된 파일이 존재하지 않으면 파일을 생성하고 명시된대로 접근, 변경 시간을 설정하라고 설명한다. 새로운 타임스탬프가 명시되지 않으면, `touch`는 현재 시간을 사용한다.

## 사용법

SUS는 다음과 같은 옵션을 지정한다:

  -
    `-a`, 접근 시간만을 변경
    `-c`, 파일이 존재하지 않으면, 새 파일을 만들지 말고 이 상황을 보고하지 말 것
    `-m`, 변경 시간만을 변경
    ` -r  `*`file`*, *`file`*의 접근, 변경 시간을 사용
    ` -t  `*`time`*, 접근, 변경 시간을 업데이트하기 위해 (아래에 나와있는 포맷에) 명시된 시간을 사용

시간은 \[\[cc\]yy\]MMDDhhmm\[.ss\]의 포맷으로 명시되는데, 여기서 MM은 두 자리로 된 월(month)을, DD는 두 자리로 된 날(day)을, hh는 두 자리로 된 시간(hour) 단위를, mm은 두 자리로 된 분(minute) 단위를 의미한다. 부가적으로 ss는 두 자리로 된 초를 의미하며 cc는 그 해의 처음 두 자리, yy는 그 해의 마지막 두 자리를 의미한다.

만일 이러한 옵션들이 없다면, 현재의 날짜와 시간을 접근 시간과 변경 시간을 바꾸는 데 사용하라고 유닉스 규격은 명시한다. 이것은 시간을 따로 변경할 필요없이 파일이 업데이트를 할 수 있도록 하는데, 특정한 상황에서 권장된다.(아래의 예시를 보라.)

다른 유닉스, [유닉스 계열](../Page/유닉스_계열.md "wikilink") 운영 체제들은 다른 옵션들을 추가한다. 예를 들어 GNU `touch`는 `-d` 옵션을 추가하는데, 이는 명시된 포맷 이외의 포맷으로 시간을 입력하는 것을 가능하게 만든다.

## 예시

가장 단순한 touch의 [용도](https://ko.wikipedia.org/wiki/용도 "wikilink")는 다음과 같다:

`$ touch myfile.txt`

touch는 myfile.txt의 내용을 수정하지 않는다; 이것은 단지 파일의 [타임스탬프](../Page/타임스탬프.md "wikilink")를 컴퓨터의 현재 날짜와 시간으로 업데이트시킨다.

우리에게 이 기능이 왜 필요한지 예를 들어보자. 우리는 우리가 작성하고 있는 소프트웨어 프로젝트를 다시 [make](https://ko.wikipedia.org/wiki/make "wikilink")하고자한다. 우리는 make파일을 수정한 후에 `make` 프로그램을 다시 실행해야 한다. 그러나 만약 우리가 make를 즉시 실행시켰다면 다음과 같은 메시지를 발견할 것이다.

`$ make`
``make: nothing to be done for `all'``

소스 코드 파일이 이미 업데이트되었기 때문에, 파일 업데이트를 시뮬레이트하려면 touch를 사용해야 한다. 그러면 `make` 는 작동되고 소프트웨어는 다시 번역될 것이다.

`$ touch project.c`
`$ make`

이와 같이 실행시키면 된다.

아래는 파일의 시간과 날짜를 어떻게 바꾸는지를 보여준다.

``` bash
 $ touch -t 200701310846.26 index.html
 $ touch -d '2007-01-31 8:46:26' index.html
 $ touch -d 'Jan 31 2007 8:46:26' index.html
```

위의 세 개는 동일하다 : 이것들은 index.html의 시간과 날짜를 2007년 1월 31일 8:46:26am로 변경시킨다. 비록 cp, grep, chmod와 같은 명령어들이 하위 디렉터리에 반복적으로 적용되는 순환 스위치(-r 이나 -R 혹은 모두)를 가지고 있지만, touch는 이러한 기능은 아직 제공하고 있지 않다.(2008년 8월 현재) 다음과 같이 하면 이 기능을 사용할 수 있다 :

``` bash
 $ find . -exec touch {} \;
```

이 방법은 비교적 느리다. 더 빠른 방법은 다음과 같다 :

``` bash
 $ find . | xargs touch
```

만일 파일 이름이나 하위 디렉터리 이름이 공백을 포함한다면, 다음이 사용되어야 한다 :

``` bash
 $ find . -print0 | xargs -0 touch
```

## 다른 운영체제

유닉스의 `touch` 와 같은 기능을 수행하는 프로그램들은 [마이크로소프트 윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink"), [맥 OS와](https://ko.wikipedia.org/wiki/맥_OS "wikilink") 같은 다른 운영 체제에도 존재한다.

## 함께 보기

  - [시스템 시간](../Page/시스템_시간.md "wikilink")
  - [유닉스 명령어 목록](../Page/유닉스_명령어_목록.md "wikilink")

## 외부 링크

  - [touch에 대한 상술](http://www.opengroup.org/onlinepubs/009695399/utilities/touch.html)
  - [ntouch/dtouch 페이지](http://www.flos-freeware.ch/archive.html)
  - [touch 사용 예제](http://www.bellevuelinux.org/touch.html)

<!-- end list -->

  - 매뉴얼 페이지

<!-- end list -->

  -

  -

  - [touch](http://www.gnu.org/software/coreutils/manual/html_node/touch-invocation.html) — [GNU](https://ko.wikipedia.org/wiki/GNU "wikilink") [coreutils](https://ko.wikipedia.org/wiki/coreutils "wikilink")의 매뉴얼 페이지

  -

[분류:표준 유닉스 프로그램](https://ko.wikipedia.org/wiki/분류:표준_유닉스_프로그램 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink")