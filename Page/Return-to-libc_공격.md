> This article is converted from Wikipedia: [Return-to-libc 공격](https://ko.wikipedia.org/wiki/Return-to-libc_공격).


**“return-to-libc” 공격**은 보통([NX 비트가](../Page/NX_비트.md "wikilink") 존재하는 경우 이것을 우회함으로써), [콜 스택의](../Page/콜_스택.md "wikilink") 서브루틴 반환 주소를 이미 프로세스의 실행 가능 메모리에 위치한 서브루틴의 주소로 교체되게 하는, [버퍼 오버플로](https://ko.wikipedia.org/wiki/버퍼_오버플로 "wikilink") 시에 사용되는 [컴퓨터 보안](../Page/컴퓨터_보안.md "wikilink") 공격이다.

[POSIX](../Page/POSIX.md "wikilink")를 준수하는 [운영 체제에서](../Page/운영_체제.md "wikilink") [C 표준 라이브러리는](../Page/C_표준_라이브러리.md "wikilink") 일반적으로 [C 언어로](https://ko.wikipedia.org/wiki/C_언어 "wikilink") 쓰여진 프로그램을 위한 표준 런타임 환경을 제공하는데 사용된다. 비록 공격자가 코드 반환을 어느 곳에서든 할 수 있지만(대부분의 프로그램에 항상 링크된 `libc` 가 목표이다) 공격자에게 유용한 호출을 제공한다(셸 명령어를 실행시키는데 필요한 `system` 함수 같이).

## return-to-libc 공격으로부터의 방어

[실행 불가능한](../Page/NX_비트.md "wikilink") 스택은 몇몇 버퍼 오버플로 익스플로잇을 방지할 수 있지만, return-to-libc 공격에서는 단지 존재하는 실행 가능 코드가 사용되기 때문에 return-to-libc을 막을 수는 없다. [스택 스매싱 보호는](https://ko.wikipedia.org/wiki/스택_스매싱_보호 "wikilink") 스택의 오염을 탐지할 수 있으므로 이 취약점 공격을 막거나 방해할 수 있다.

"ASCII armoring"은 이러한 종류의 공격을 방해하는데 사용되는 기법이다. 이것을 사용하면 모든 시스템 라이브러리 주소들은 NULL 바이트(0x00)를 갖는다. 이것은 이 값 까지의 모든 주소들이 적어도 하나의 NULL 바이트를 갖도록, 메모리의 0x01010100 까지 위치 시킴으로써(약 16MB로서 "ASCII armour 영역"이라고 불린다) 일반적으로 수행된다. 이것은 `strcpy()` 같은 문자열 조작 함수들을 사용해서 이러한 주소들을 포함하는 코드를 설치하는 것을 불가능하게 한다. 그러나 이 기법은 만약 공격자가 NULL 바이트를 스택에 오버플로 할 방법을 알지 못하면 통하지 않는다. 만약 프로그램이 첫 16MB에 맞추기에 너무 크다면, 방어는 완전하지 못하게 된다.\[1\] 이 기법은 또한 더 진화된 방법인 **return-to-plt** 에 의해 극복될 수 있는데 이것은 libc에 반환하는 것 대신, 공격자가 바이너리에 로드된 Procedure Linkage Table (PLT) 함수들을 사용한다(예를 들면 `system@plt, execve@plt, sprintf@plt, strcpy@plt` 등).\[2\]

주소 공간 배치 난수화(ASLR)는 64비트 기계에서 함수들의 메모리 위치를 랜덤화해서 이 공격이 거의 성공하지 못하게 한다. 32비트 시스템에서 ASLR은 랜덤화에 단지 16비트만 사용 가능해서 약간의 유용함만을 제공하며 수분 이내에 무차별 대입 공격으로 무력화될 수 있다.\[3\]

## 같이 보기

  - [버퍼 오버플로](https://ko.wikipedia.org/wiki/버퍼_오버플로 "wikilink")
  - [스택 버퍼 오버플로](../Page/스택_버퍼_오버플로.md "wikilink")
  - [스택 스매싱 방어](https://ko.wikipedia.org/wiki/스택_스매싱_방어 "wikilink")
  - [NX 비트](../Page/NX_비트.md "wikilink")
  - [주소 공간 배치 난수화](https://ko.wikipedia.org/wiki/주소_공간_배치_난수화 "wikilink")
  - [반환 지향형 프로그래밍](../Page/반환_지향형_프로그래밍.md "wikilink")

## 각주

## 외부 링크

  - [Bypassing non-executable-stack during exploitation using return-to-libc](http://www.infosecwriters.com/text_resources/pdf/return-to-libc.pdf) by c0ntex at InfoSecWriters.com

[분류:C 표준 라이브러리](https://ko.wikipedia.org/wiki/분류:C_표준_라이브러리 "wikilink") [분류:취약점 공격](https://ko.wikipedia.org/wiki/분류:취약점_공격 "wikilink")

1.
2.
3.