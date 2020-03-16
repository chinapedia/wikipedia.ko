> This article is converted from Wikipedia: [INT \(x86 \)](https://ko.wikipedia.org/wiki/INT_\(x86_\)).


**INT**는 [x86](https://ko.wikipedia.org/wiki/x86 "wikilink") [중앙 처리 장치를](../Page/중앙_처리_장치.md "wikilink") 위한 [어셈블리어](../Page/어셈블리어.md "wikilink")로서, [인터럽트](../Page/인터럽트.md "wikilink")를 발생시키는 역할을 한다. 이것은 [바이트](../Page/바이트.md "wikilink") 값으로 구성된 인터럽트 번호를 가진다.\[1\]

어셈블리어로 작성될 경우, 명령어는 아래와 같다.

  -
    ` INT  `*`X`*

 *`X`* 는 소프트웨어 인터럽트로서 (0-255)의 값으로 생성된다.

문맥과, [컴파일러](../Page/컴파일러.md "wikilink"), 또는 [어셈블리어](../Page/어셈블리어.md "wikilink")에 따라 소프트웨어 인터럽트 번호는 종종 [십육진법](../Page/십육진법.md "wikilink") 값으로 주어진다. 예를 들면 `INT 21H`은 소프트웨어 인터럽트 0x21 (10진수로는 33)을 생성한다. [MS-DOS API호출에서](../Page/MS-DOS_API.md "wikilink") 이것은 인터럽트 테이블에 있는 34번째 벡터를 가리킴으로써 이 함수를 실행시킨다.

## 리얼 모드

소프트웨어 인터럽트가 발생하면 [중앙 처리 장치는](../Page/중앙_처리_장치.md "wikilink") 인터럽트 주소 테이블(리얼모드에서는 메모리의 첫 번째 1024 바이트에 위치한)에서 256가지 함수 중 하나(가리켜진)를 호출한다. 그러므로 플래그 레지스터를 푸시한 후에 인터럽트 함수를 직접 시작함으로써, far-call 명령어를 사용하는 것이 가능하다.

도스 소프트웨어 인터럽트 중에서 가장 유용한 것은 인터럽트 0x21이다. 여러 파라미터들을 레지스터에 넣고 이것을 호출함으로써, 다양한 입출력 작업이나 문자열 출력 등에 접근하는 등의 것들이 가능해 진다.\[2\]

대부분의 [유닉스](../Page/유닉스.md "wikilink") 시스템들과 그쪽 계열들은 인터럽트 0x80을 제외하고는 [시스템 호출을](../Page/시스템_호출.md "wikilink") 위한 소프트웨어 인터럽트를 사용하지 않는다. 이것은 커널 함수에 대응하는 32-bit 값을 EAX 레지스터에 넣고, INT 0x80을 실행하는 방식이다.

## INT 3

INT 3 명령어는 [디버거](../Page/디버거.md "wikilink")가 실행중인 프로그램에 [브레이크포인트](../Page/브레이크포인트.md "wikilink")를 설정하기 위하여 사용된다. 다른 INT 명령어들은 2 바이트를 사용하지만 이것은 명령어를 패치하는데 적합하게 1바이트를 사용한다. INT 3의 옵코드는 `0xCC`이다.\[3\]

## 같이 보기

  - [INT 10H](https://ko.wikipedia.org/wiki/INT_10H "wikilink")
  - [INT 13H](https://ko.wikipedia.org/wiki/INT_13H "wikilink")
  - [INT 21H](../Page/MS-DOS_API.md "wikilink")
  - [인터럽트](../Page/인터럽트.md "wikilink")
  - [바이오스 인터럽트 호출](../Page/바이오스_인터럽트_호출.md "wikilink")
  - [랄프 브라운의 인터럽트 리스트](../Page/랄프_브라운의_인터럽트_리스트.md "wikilink")

## 각주

[분류:인터럽트](https://ko.wikipedia.org/wiki/분류:인터럽트 "wikilink") [분류:X86 명령어](https://ko.wikipedia.org/wiki/분류:X86_명령어 "wikilink")

1.
2.  [Definition of: int 21](http://www.pcmag.com/encyclopedia_term/0,2542,t=int+21&i=45064,00.asp)
3.