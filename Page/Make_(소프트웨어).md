> This article is converted from Wikipedia: [Make \(소프트웨어\)](https://ko.wikipedia.org/wiki/Make_\(소프트웨어\)).


**`make`**는 [소프트웨어 개발을](https://ko.wikipedia.org/wiki/소프트웨어_개발 "wikilink") 위해 [유닉스 계열](../Page/유닉스_계열.md "wikilink") 운영 체제에서 주로 사용되는 프로그램 빌드 도구이다.

여러 파일들끼리의 의존성과 각 파일에 필요한 명령을 정의함으로써 프로그램을 컴파일할 수 있으며 최종 프로그램을 만들 수 있는 과정을 서술할 수 있는 표준적인 문법을 가지고 있다.

위의 구조로 기술된 파일(주로 Makefile이라는 파일명)을 `make`가 해석하여 프로그램 빌드를 수행하게 된다.

## 파생

  - SunPro make
  - dmake(Distributed Make)
  - [BSD](../Page/BSD.md "wikilink") make(pmake\[1\], bmake, fmake)
  - [GNU](../Page/GNU.md "wikilink") make(gmake)
  - Glenn Fowler의 nmake\[2\]
  - [마이크로소프트](../Page/마이크로소프트.md "wikilink") nmake
  - [리서치 유닉스의](https://ko.wikipedia.org/wiki/리서치_유닉스 "wikilink") Mk

## Makefile

`make`을 실행하기 전에 프로젝트의 목록 및 컴파일 및 링크 규칙을 만들어야 한다. 이것은 보통 Makefile을 사용한다. 이 파일에 규칙을 입력하여 파일로 만든다.

### 규칙

`TARGET ...: PREREQUISITES ...`
`RECIPE`
`...`

또 다른 형식은

`TARGETS: PREREQUISITES ; RECIPE`
`RECIPE`
`...`

  - TARGET: 실행 파일, object 파일, 라이브러리 등 목적 규칙을 정의한다. RECIPE에서 실행된 결과로 만들어진다. RECIPE 여러개의 명령줄을 사용할 수가 있어 복잡한 기능도 수행이 가능하다. 생성파일이나 install 같은 기능적 블럭도 가능하다.
    PREREQUISITES: TARGET을 만들 때, 의존성(연관관계)를 규정한다. 이 부분에 나열된 파일 중 수정된 파일이 있으면 TARGET을 다시 만든다.
    RECIPE: TARGET을 만들기 위한 실행 파일이다. 이 실행 규칙에 따라 TARGET이 생성 된다. 주로 cc나 리눅스 명령어를 사용한다. 이 명령 줄은 여러 줄이 가능하다. 주의 할 것은 RECIPE 부분의 앞 공간은 키보드 을 사용해야 한다. 키로 공간을 넣으면 안 된다.

<!-- end list -->

``` make
     foo.o : foo.c defs.h       # module for twiddling the frobs
             cc -c -g foo.c
```

foo.c나 defs.h가 변경 되면 `cc -c -g foo.c`명령을 실행해 foo.o을 만든다.

### Makefile 예

``` make numberLines
     objects = main.o kbd.o command.o display.o \
               insert.o search.o files.o utils.o

     edit : $(objects)
             cc -o edit $(objects)

     main.o : defs.h
     kbd.o : defs.h command.h
     command.o : defs.h command.h
     display.o : defs.h buffer.h
     insert.o : defs.h buffer.h
     search.o : defs.h buffer.h
     files.o : defs.h buffer.h command.h
     utils.o : defs.h

     .PHONY : clean
     clean :
             rm edit $(objects)
```

\[3\]

위의 예에서 최종 실행 출력 파일은 `edit`이다. `edit` 실행 파일을 만들기 위해 여러 개의 소스 코드 파일을 이용하여 작성한 경우이다. 어떤 프로그램 소스 파일이 있는가는 objects 변수에 의해 설정되었다.

`.PHONY : make clean`을 실행하면 `rm` 명령만을 실행하게 한다. 위의 경우 단순히 명령줄로 사용할 때 사용한다. `clean` 뒤에 의존성 파일이 없으므로 타겟을 변경할 필요가 없어진다. 따라서 `rm`을 실행하지 않는다. 업데이트 필요성이 없어진다. 생성 파일이 아니 단순 타켓으로만 인식하게 할 수 있다.

clean을 실행해서 삭제하고 다시 컴파일하려면

``` bash
 $ make clean
```

명령

``` make
 rm edit $(objects)
```

이 실행되어 모든 오브젝트 파일이 삭제 된다. 동시에 실행 파일 edit도 삭제된다.

위의 예에서 구조를 다음과 같이 간단히 줄일 수 있다.

``` make
     objects = main.o kbd.o command.o display.o \
               insert.o search.o files.o utils.o

     edit : $(objects)
             cc -o edit $(objects)

     $(objects) : defs.h
     kbd.o command.o files.o : command.h
     display.o insert.o search.o files.o : buffer.h
```

## 와일드카드

와일드카드는 명령에서 사용될 수 있다. 이것은 셸에 의해서 확장된다.

모든 오브젝트 파일들을 삭제하는 규칙

``` bash
clean:
        rm -f *.o
```

### 와일드카드 예제

와일드카드는 규칙의 종속물에서도 유용하다. makefile의 다음 규칙에서 '`make print`'는 대상의 인쇄한 마지막 시간 이후로 변경된 모든 '.c' 파일들을 인쇄할 것이다:

``` make
print: *.c
        lpr -p $?
        touch print
```

### 와일드카드 함수

와일드 카드는 규칙 안에서 자동으로 확장된다. 그러나 와일드 카드 확장은 일반적으로 변수가 설정되었을 때, 또는 함수의 매개변수 안에서는, 일반적으로 발생하지 않는다. 그런 경우에서 와일드카드 확장을 하려고 한다면 다음과 같이 wildcard 함수를 사용해야 한다.

``` make
$(wildcard pattern...)

$(wildcard *.c) # 한 디렉토리에 있는 모든 C 소스 파일들의 리스트를 획득하는 것이다.
$(patsubst %.c,%.o,$(wildcard *.c)) # '.c' 접미사를 '.o'로 변경해서 오브젝트 파일들의 리스트로 변경할 수 있다.
```

한 디렉토리에 있는 모든 C 파일들을 컴파일하고 이들을 모두 모아서 링크하려고 하는 makefile은 다음과 같이 작성될 수 있다:

``` make
objects := $(patsubst %.c,%.o,$(wildcard *.c))

foo : $(objects)
        cc -o foo $(objects)
```

## make의 재귀적 사용

재귀적 사용이란 make를 makefile에서 하나의 명령으로 사용한다는 것이다. 큰 시스템을 만드는 여러 서브시스템들을 위한 여러 분리된 makefile들을 make 실행할 때 유용하다. 예를 들어서 자신의 makefile을 가지고 있는 'subdir' 서브디렉토리를 가지고 있고 상위 디렉토리의 makefile을 사용해서 그 서브 디렉토리에 대해서 make를 실행하고자 한다고 가정하자.

다음과 같이 할 수 있다:

``` make
subsystem:
        cd subdir && $(MAKE)
```

또는:

``` make
subsystem:
        $(MAKE) -C subdir
```

재귀적인 make 명령들은, 다음에서 볼 수 있듯이 '`make`' 명령 이름을 명시적으로 쓰지 않고, 항상 `MAKE` 변수를 사용하는 것이 좋다.

### 서브-make에 대한 통신 변수

특정 변수가 sub-make에 익스포트되기를 원한다면 export 지시어를 사용한다.

``` make
export variable ...

unexport variable ...
```

open_filelist() 어떤 변수를 정의하면서 동시에 그것을 익스포트할 수 있다 :

``` make
export variable = value
```

이것은 다음과 같은 결과를 가진다:

``` make
variable = value
export variable
```

다른 참조도 가능하다.

``` make
export variable := value
```

``` make
export variable += value
```

### 서브-make에 대한 통신 옵션

'-s'와 '-k' 같은 플래그들은 자동으로 변수 MAKEFLAGS를 통해서 서브-make에게 전달된다.

'-C', '-f', '-o', 그리고 '-W' 옵션들은 MAKEFLAGS에 들어가지 않는다; 이들 옵션들은 아래로 전달되지 않는다.

다른 플래그들은 아래로 전달하고자 하지 않는다면 반드시 다음과 같이 MAKEFLAGS의 값을 변경해야 한다:

``` make
subsystem:
        cd subdir && $(MAKE) MAKEFLAGS=

MAKEOVERRIDES =
```

## 빈 명령 사용하기

아무것도 하지 않는 명령들을 정의하는 것이 때때로 유용하다.

``` make
target: ;
```

## 동작

make는 일반적으로 실행 가능한 프로그램과 라이브러리를 소스 코드로부터 [빌드하는](https://ko.wikipedia.org/wiki/소프트웨어_빌드 "wikilink") 데 사용된다. 그러나 일반적으로 소스 파일을 대상 결과물로 변환하는 데 기여하는 어떠한 프로세스라도 (임의의 명령어들을 실행함으로써) make에 적용할 수 있다.

make는 [명령 줄 변수로서](../Page/명령_줄_인터페이스.md "wikilink") 빌드할 대상 파일의 목록과 더불어 불러낼 수 있다:

``` bash
  $ make 대상 [대상 ...]
```

변수 없이 `make`를 실행하면 makefile 안에 보이는 첫 번째 대상만을 빌드한다.

## 같이 보기

  - [CMake](../Page/CMake.md "wikilink")

## 각주

## 외부 링크

  - [GNU make 홈페이지](http://www.gnu.org/software/make/)
  - [KLDP GNU make](https://web.archive.org/web/20120831105433/http://wiki.kldp.org/KoreanDoc/html/GNU-Make/GNU-Make.html)

[분류:GNU 프로젝트 소프트웨어](https://ko.wikipedia.org/wiki/분류:GNU_프로젝트_소프트웨어 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink") [분류:빌드 자동화](https://ko.wikipedia.org/wiki/분류:빌드_자동화 "wikilink") [분류:스크립트 언어](https://ko.wikipedia.org/wiki/분류:스크립트_언어 "wikilink")

1.
2.
3.  <http://www.gnu.org/software/make/manual/make.txt>