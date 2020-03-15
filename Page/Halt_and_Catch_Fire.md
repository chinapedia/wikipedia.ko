> This article is converted from Wikipedia: [Halt and Catch Fire](https://ko.wikipedia.org/wiki/Halt_and_Catch_Fire).


**Halt and Catch Fire**는 니모닉(mnemonic) HCF라고 불리며 원래는 존재하지 않는 가공의 컴퓨터 [기계어](https://ko.wikipedia.org/wiki/기계어 "wikilink") 명령어였는데 "Execute Operator"같은 명령어들과 함께 [IBM](https://ko.wikipedia.org/wiki/IBM "wikilink")이 [System/360](https://ko.wikipedia.org/wiki/System/360 "wikilink")([IBM 시스템/360](https://ko.wikipedia.org/wiki/IBM_시스템/360 "wikilink"))에서 사용하기 위해 개발한 것으로 알려지고 있다.

실제로 HCF는 이상한 효과를 가지거나 프로세서를 테스트하는 용도의 비공식(undocumented) 기계어를 의미한다. 오래된 "Halt and Catch Fire"와 HCF 니모닉은 사용자들이 의도하지 않은 명령어를 실행하는 방법으로 발견하였는데 이런 방법은 시스템의 실행을 실패하거나 멈추는 경우가 많았으며 이것을 은유적으로 "catch fire"라고 표현하였다.

출처가 밝혀지지 않은 이야기가 있는데 [컴퓨터](../Page/컴퓨터.md "wikilink")에서 [자기 코어 메모리를](../Page/자기_코어_메모리.md "wikilink") 사용하던 1960년대 말은 코어 메모리의 속도 증가가 요구되던 시기로 기술자들은 기존의 제품보다 읽기/쓰기의 속도 증가를 위해 품질 좋은 와이어로 코어를 꿰었다. 컴퓨터가 일반적인 프로그램을 실행하면 [메모리](https://ko.wikipedia.org/wiki/메모리 "wikilink") 액세스는 메모리 전체로 확대된다. 하지만 HALT 명령어는 제자리로 점프(Jump to self)하는 방법을 사용하는데 이것은 하나의 코어 메모리 구역만 반복적으로 액세스하는 것을 의미한다. 그 결과 좋은 품질의 와이어라도 쉽게 과열되어 연기가 나게 된다. 여기에서 "Halt and Catch Fire"가 유래되었다고 전해진다.

## HCF의 발견

[모토로라 6800에서](https://ko.wikipedia.org/wiki/모토로라_6800 "wikilink") HCF 오프코드(opcode)를 최초로 발견한 것으로 널리 알려져 있다. 6800 HCF 오프코드(0xDD 또는 0xD9)는 게리 윌러(Gerry Wheeler 1952–2006)가 발견해 1977년 12월 [바이트 매거진](https://ko.wikipedia.org/wiki/바이트_매거진 "wikilink")(BYTE magazine)에 비공개 오프코드로 기사화되었다.\[1\] 이 명령어는 프로세서가 제조시의 테스트 모드로 전환되어 명령어의 개입없이 끊임없이 메모리 주소를 바꾸어가며 메모리 읽기를 실행한다. 이것은 어드레스 버스를 [타이머](../Page/타이머.md "wikilink")로 작동하게 해서 [CPU의](https://ko.wikipedia.org/wiki/중앙_처리_장치 "wikilink") 모든 어드레스 라인을 재빨리 검사한다. 프로세서가 한번 테스트 모드로 전환되면 [인터럽트](../Page/인터럽트.md "wikilink")에 응답하지 않기 때문에 일반 작업을 실행하려면 리셋을 해야 한다.

## HCF 오프코드가 확인된 프로세서

  - [6502와](https://ko.wikipedia.org/wiki/MOS_6502 "wikilink") 일반적인 NMOS 650x, 651x 프로세서 시리즈<ref><http://www.easy68k.com/paulrsm/6502/AAL/AAL8103.TXT>

`Apple Assembly Line Volume 1 Issue 6`</ref>

  - [6800](https://ko.wikipedia.org/wiki/모토로라_6800 "wikilink")\[2\]
  - [MIPS-X](https://ko.wikipedia.org/wiki/MIPS-X "wikilink"): 프로그래머 매뉴얼에 NSA 버전 프로세서의 HSC (Halt and Spontaneously Combust) 명령어를 표기\[3\]

## 참조

[분류:컴퓨터 문화](https://ko.wikipedia.org/wiki/분류:컴퓨터_문화 "wikilink")

1.  Wheeler, Gerry (December 1977) "Undocumented M6800 Instructions". BYTE 2 (12): 46–47.
2.
3.