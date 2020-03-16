> This article is converted from Wikipedia: [AWK](https://ko.wikipedia.org/wiki/AWK).


**AWK**(오크)는 [유닉스](../Page/유닉스.md "wikilink")에서 처음 개발된 일반 [스크립트 언어이다](../Page/스크립트_언어.md "wikilink"). AWK의 기본 기능은 텍스트 형태로 되어있는 입력 데이터를 행과 단어 별로 처리해 출력하는 것이다. AWK라는 이름은 이 스크립트 언어를 만든 [앨프리드 에이호](https://ko.wikipedia.org/wiki/앨프리드_에이호 "wikilink"), 피터 와인버거, [브라이언 커니핸](../Page/브라이언_커니핸.md "wikilink") 세 명의 성의 앞글자를 따서 붙여졌다.

AWK는 문자열 데이터와 연관 배열(배열의 인덱스가 숫자가 아닌 임의의 값이 될 수 있는 배열), [정규 표현식을](https://ko.wikipedia.org/wiki/정규_표현식 "wikilink") 주로 사용한다. AWK와 [sed가](../Page/Sed_\(유틸리티\).md "wikilink") 결합하면 간결하면서도 강력한 스크립팅이 가능하다.\[1\] AWK는 유닉스 버전 7에 처음 등장해서 지금까지 사용되는 매우 오래된 도구로, 오늘날에는 거의 모든 [유닉스 계열](../Page/유닉스_계열.md "wikilink") 운영체제에 포함되어 있는 표준 도구로 자리잡았으며 다른 운영체제에서도 사용할 수 있다.

AWK 프로그램은 기본적으로 패턴과 패턴을 처리하는 명령어 짝을 늘여놓은 구조로 이루어져 있다. 입력으로부터 한 줄씩을 읽어서 [정규 표현식으로](https://ko.wikipedia.org/wiki/정규_표현식 "wikilink") 조건이 맞는지를 검사하고 참으로 판명되면 그 줄에 대해 명령어를 실행하는 형식이다.

## awk 프로그램의 구조

awk는 크게 명령 파일과 주 입력 파일 두 가지 데이터를 받아 실행된다. 명령 파일은 awk가 입력 데이터를 어떤 규칙에 따라 처리할지를 지시한다. 명령 파일은 커맨드 라인을 통해 직접 입력될 수도 있으며 미리 작성된 파일일 수도 있다. 입력파일은 보통 특정한 형식에 따라 작성된 텍스트 파일이다. 입력 역시 실제 파일 형태로 입력될 수도 있고, 표준입력을 통해 입력될 수도 있다. 명령 파일에 해당하는 awk 프로그램은 다음 형태의 명령이 여러 줄 이어진 구조로 되어 있다.

``` awk
 /패턴/ { 동작 }
```

여기서 *패턴*은 [정규 표현식이며](https://ko.wikipedia.org/wiki/정규_표현식 "wikilink"), *동작*은 실행명령이다. awk는 입력파일을 처음부터 한 줄씩 입력받아 주어진 *패턴*과 일치하는 줄을 찾으면 그 줄에서 *동작*에 해당하는 명령을 실행한다. 패턴-동작의 형태 이외에도 다음과 같은 명령도 awk 프로그램에서 가능하다.

``` awk
BEGIN { 동작 } # 입력을 읽기 전에 주어진 '동작'을 먼저 실행한다.
END { 액션 } # 위와 비슷하다. 주입력을 모두 훑고 마지막에 주어진 '액션'을 실행한다.
/패턴/ # '패턴'에 일치하는 줄을 출력한다.
{ 동작 } # 매 줄을 읽을 때마다 '동작'을 실행한다.
```

각 형태의 명령은 명령 파일에서 여러번 올 수 있다. 각각은 명령 파일에 쓰여진 순서에 따라 실행된다. 즉, "`BEGIN`" 문이 두번 주어져 있으면 앞에 있는 "`BEGIN`" 문이 실행된 후에 다음에 오는 "`BEGIN`" 문이 실행된다. 그러나 "`BEGIN`" 문은 다른 명령들 사이에 있더라도 다른 명령들이 실행되기 전에 실행된다. 이는 "`END`" 문에 대해서도 마찬가지이다.

## Awk 명령어

awk 명령어는 위에서 *동작*이라고 쓰인 위치에 쓰여 실제 동작을 지시하는 명령어이다. awk 명령어는 함수호출, 변수값 지정, 산술계산과 이들을 조합한 어떤 것이 될 수 있다. awk는 다양한 함수들을 기본적으로 지원하고 변종에 따라 다른 기타 기능들이 들어갈 수 있다. 어떤 것은 [동적 링크 라이브러리를](../Page/동적_링크_라이브러리.md "wikilink") 지원하기도 한다.

간결성을 위해서 아래 예에서 중괄호(`{ }`)는 생략했다.

### *`print`* 명령어

*`print`* 는 텍스트를 출력한다. 이 명령어만 홀로 쓰면,

``` awk
 print
```

현재 줄의 내용을 출력한다. awk에서 한 줄은 자동적으로 여러 개의 *필드*\[2\]로 구분지어진다. 필드는 print 명령에서 다음과 같이 따로따로 출력될 수 있다.

``` awk
print $1 # 현재 줄의 첫 번째 필드를 출력한다.
print $1, $3 # 첫 번째와 세 번째 필드를 출력하며,
# 둘 사이에는 디폴트로 빈칸(스페이스) 하나로 주어지는 OFS(출력 필드 구분자, output field seperator)가 들어간다.
```

X(X는 숫자)번째 필드는 *`$X`* 로 표시되며, 특별히 *`$0`*은 줄 전체를 지정한다. 실제로 "`print`" 과 "`print $0`" 는 똑같은 결과를 가져온다.

*print*는 계산의 결과나 함수호출의 결과값을 뿌릴 수도 있다:

``` awk
 print 3+2
 print foobar(3)
 print foobar(variable)
 print sin(3-2)
```

물론 출력은 다음과 같이 하여 표준출력이 아닌 다른 파일로 쓸 수도 있다.

``` awk
 print "expression" > "file name"
```

### 변수 등등

변수 이름은 알파벳 대소문자와 숫자\[3\]로 표현되는 문자들의 조합으로 만들 수 있다. 단 awk의 예약어는 변수가 될 수 없다. `+ - * /`는 각각 덧셈, 뺄셈, 곱셈, 나눗셈을 나타낸다. 문자열을 합치고 싶을 때에는 단순히 변수나 고정 문자열을 붙여 쓰기만 하면 된다. 고정 문자열은 겹따옴표로 구분되며, 세미콜론으로 문(statement)의 끝을 표시할 필요는 없다. 주석문은 첫머리에 *\#*를 달아 표시한다.

### 사용자 정의 함수

[C와](../Page/C_\(프로그래밍_언어\).md "wikilink") 비슷하게, 함수 선언은 함수 이름과 함수의 인자들로 이루어진다.

``` awk
 function add_three (number ,temp) {
   temp = number + 3
   return temp
 }
```

이 함수는 다음과 같이 쓰일 수 있다.

``` awk
 print add_three(36)     # prints '''39'''
```

함수는 함수 내부에서만 쓰이는 지역변수를 가질 수 있다. 이 지역변수는 인자 목록 끝에 포함된다. 그러나 함수를 부를 때는 이 변수 자리에 아무것도 쓰지 않는다. 이들을 구분하기 위해 함수가 넘겨받는 인자와 지역변수 사이에 빈칸을 좀 집어넣어 구분하는 것이 암묵적 약속이다.

## 예제

### [Hello World 프로그램](https://ko.wikipedia.org/wiki/Hello_World_프로그램 "wikilink")

``` awk
 BEGIN { print "Hello, world!" }
```

### 80자보다 글자수가 많은 줄만 출력

`length`는 현재 줄의 길이를 가지며, *동작*이 지정되지 않았을 때에는 `print`가 기본 동작이다.

``` awk
 length > 80
```

### 파일의 낱말 수를 세기

`NF`는 **N**umber of **F**ields, 즉 현재 줄의 필드의 개수이며, `NR`은 **N**umber of **R**ecords 레코드의 개수인데, 각 줄이 레코드이다. 결국 입력파일의 **줄 수**, 빈칸으로 구분된 **낱말 수**, **문자수** 를 출력한다.

``` awk
 { w += NF; c += length}
 END { print NR, w, c }
```

### 첫 번째 필드의 값을 쭉 더하기

``` awk
 { s += $1 }
 END { print s }
```

### 입력파일의 낱말 빈도 계산

``` awk
 {
   for (i=1; i<=NF; i++)
     words[$i]++
 }

 END {
   for (i in words)
     print i, words[i]
 }
```

위 소스를 word_frequency.awk 로 저장하고 [애국가](https://ko.wikipedia.org/wiki/애국가 "wikilink") 가사를 입력으로 주어 실행한 결과는 다음과 같다.

``` bash
 $ awk -f word_frequency.awk aegukga.txt
 백두산이 1
 충성을 1
 소나무 1
 대한으로 4
 마르고 1
 괴로우나 1
 우리가슴 1
 높고 1
 가을하늘 1
 저 1
 남산위에 1
 길이 4
 하느님이 1
 두른 1
 즐거우나 1
 기상과 1
 밝은 1
 불변함은 1
 보우하사 1
 맘으로 1
 대한사람 4
 달은 1
 우리나라 1
 공활한데 1
 바람 1
 나라 1
 이 2
 우리 1
 서리 1
 동해물과 1
 무궁화 4
 철갑을 1
 삼천리 4
```

## 같이 보기

  - [cut](https://ko.wikipedia.org/wiki/cut "wikilink")
  - [sed](https://ko.wikipedia.org/wiki/sed "wikilink")
  - [perl](../Page/펄.md "wikilink")

## 각주

<references />

## 외부 링크

  - [KLDP의 간단한 한국어 설명 문서](http://wiki.kldp.org/wiki.php/Awk)

  - [The Amazing Awk Assembler](http://doc.cat-v.org/henry_spencer/amazing_awk_assembler/) - [Henry Spencer](https://ko.wikipedia.org/wiki/:en:Henry_Spencer "wikilink").

  - [Awk Community Portal](http://awk.info/)

  - [Awk on flossmanuals.net](https://web.archive.org/web/20120310003603/http://en.flossmanuals.net/command-line/ch044_awk/)

  -
[분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink") [분류:표준 유닉스 프로그램](https://ko.wikipedia.org/wiki/분류:표준_유닉스_프로그램 "wikilink") [분류:크로스 플랫폼 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_소프트웨어 "wikilink") [분류:스크립트 언어](https://ko.wikipedia.org/wiki/분류:스크립트_언어 "wikilink") [분류:1977년 소프트웨어](https://ko.wikipedia.org/wiki/분류:1977년_소프트웨어 "wikilink") [분류:자유 컴파일러와 인터프리터](https://ko.wikipedia.org/wiki/분류:자유_컴파일러와_인터프리터 "wikilink")

1.  [래리 월이](../Page/래리_월.md "wikilink") AWK의 한계 때문에 [펄](../Page/펄.md "wikilink")을 개발했다.
2.  *필드*는 비약해 말하자면 빈칸으로 구분되는 각 문자열이다.
3.  알파벳 대문자 A부터 Z까지, 소문자 a부터 z까지, 아라비아 숫자 0부터 9까지 그리고 밑줄