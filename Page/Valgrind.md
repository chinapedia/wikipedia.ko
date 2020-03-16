> This article is converted from Wikipedia: [Valgrind](https://ko.wikipedia.org/wiki/Valgrind).


**Valgrind**(밸그린드, )는 [리눅스](../Page/리눅스.md "wikilink") 기반의 오픈소스 ([GPL](https://ko.wikipedia.org/wiki/GPL "wikilink") 라이선스) DBI 도구이다. 이는 클라이언트 프로그램 (valgrind 에 입력으로 들어가는)의 실행 코드를 실행 시간에 직접 가공하는 기회를 제공함을 뜻한다. valgrind는 크게 코어(Core)와 도구(Tool)로 구성되어 있는데 일반적으로 valgrind 라 함은 코어를 뜻한다.\[1\]

## Instrumentation

Instrumentation은 코드 세그먼트(영역)에서 코드에 필요한 내용을 추가하여 원하는 결과를 내도록 하는 작업을 통틀어 말한다. 이 instrumentation이란 여러 단계에 걸쳐 일어날 수 있는데,

  - 소스 코드
  - 프리프로세서(Preprocessor code)
  - 어셈블리 코드
  - 기계 코드
  - 이진 실행 파일

등의 과정에서 어느 단계에서든 가능하다. 일반적으로 정적 instrumentation을 의미하는 데 이는, 일단 위 단계의 코드를 분석하여 필요한 추가 코드를 삽입하는 것을 뜻한다. 그리고 instrumented code를 실행시켜 원하는 결과를 얻는다.

그러나 dynamic instrumentation의 경우 runtime에 instrumentation 을 수행하여 바로 실행토록 한다. Static instrumentation 의 경우 실행 중에 발생하는 상황을 알 수 없기 때문에 dynamic instrumentation은 실행 중의 메모리나 캐시의 동작을 관찰하여 대응할 수 있는 장점이 있다.

Valgrind 는 대표적인 dynamic instrumentation framework이다.

## 구조

Valgrind는 크게 코어와 도구들로 구성되어 있다. 코어는 instrumentation을 위한 환경을 제공해 주며 도구들은 instrumented될 코드들을 포함한다. 모든 도구의 사용에 있어서 코어는 build하는 과정에서 tool의 function들에 wrapper를 사용하여 모든 tool에 core가 공통적인 동작을 수행토록 한다.

다시 말하면 코어에 사용되는 모든 함수(instrumentation 관련)들은 valgrind의 실행 파일이 생성되는 과정 (정확히는 도구들 의 실행 파일 생성 과정)에서 도구들의 함수 이름을 pointing한다. 따라서 도구들 에 링크되는 코어는 해당 도구가 필요로 하는 동작을 자동으로 수행하게 되는 것이다.

## 확장성

현재 valgrind는 [리눅스](../Page/리눅스.md "wikilink")와 [macOS](https://ko.wikipedia.org/wiki/macOS "wikilink"), [솔라리스를](../Page/솔라리스_\(운영_체제\).md "wikilink") 지원하고 있으며 AMD, X86, PPC, AIX, MIPS 등의 아키텍처를 지원한다.

## 같이 보기

  - [동적 프로그램 분석](../Page/동적_프로그램_분석.md "wikilink")
  - [Pin](https://ko.wikipedia.org/wiki/Pin_\(컴퓨팅\) "wikilink")
  - [DynamoRIO](https://ko.wikipedia.org/wiki/DynamoRIO "wikilink")

## 참고 문헌

  -
  -
  -

<references />

## 외부 링크

  -
[분류:디버거](https://ko.wikipedia.org/wiki/분류:디버거 "wikilink") [분류:프로파일러](https://ko.wikipedia.org/wiki/분류:프로파일러 "wikilink") [분류:소프트웨어 테스트 도구](https://ko.wikipedia.org/wiki/분류:소프트웨어_테스트_도구 "wikilink") [분류:자유 소프트웨어 테스트 도구](https://ko.wikipedia.org/wiki/분류:자유_소프트웨어_테스트_도구 "wikilink")

1.  [Valgrind FAQ](http://www.valgrind.org/docs/manual/faq.html#faq.whence)