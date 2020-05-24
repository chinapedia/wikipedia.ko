> This article is converted from Wikipedia: [Memtest86](https://ko.wikipedia.org/wiki/Memtest86).


**MemTest86**와 **Memtest86+**는 대부분의 메모리 주소에 테스트 패턴을 기록하고 데이터를 다시 읽어보고 오류를 비교함으로써 [x86](https://ko.wikipedia.org/wiki/x86 "wikilink") 아키텍처 컴퓨터의 [랜덤 액세스 메모리](../Page/랜덤_액세스_메모리.md "wikilink")(RAM)의 오류를 위한 [스트레스 테스트](../Page/스트레스_테스트.md "wikilink") 및 일반 테스트를 수행하기 위해 설계된 [메모리 테스트 소프트웨어](https://ko.wikipedia.org/wiki/메모리_테스트_소프트웨어 "wikilink") 프로그램이다.\[1\] 기록되는 임의의 데이터 패턴을 RAM이 수용하고 올바르게 보관하는지, 각기 다른 비트의 메모리가 상호작용하는 부분에 오류가 없는지, 메모리 주소 간 충돌이 없는지 확인을 시도한다.

## 역사

MemTest86은 1994년 크리스 브래디(Chris Brady)가 개발하였다.\[2\] MemTest86가 버전 3.0(2002년 릴리스)에서 2년 간 멈춰있는 동안, Samuel Demeulemeester는 더 새로운 CPU와 칩셋을 지원하기 위해 Memtest86+ 포크를 만들었다. 2018년1월 기준으로 최신 버전의 Memtest86+는 5.01이다.\[3\]\[4\]

MemTest86는 [C와](../Page/C_\(프로그래밍_언어\).md "wikilink") x86 [어셈블리어](../Page/어셈블리어.md "wikilink")로 작성되었다. MemTest86(바이오스 버전)과 MemTest86+ 포크의 소스 코드는 [GNU 일반 공중 사용 허가서](../Page/GNU_일반_공중_사용_허가서.md "wikilink")(GPL)로 공개되어 있다. 부트로딩 코드는 처음부터 [리눅스 1.2.1에서](../Page/리눅스_커널.md "wikilink") 비롯된 것이다.\[5\] 프로그램은 [위치 독립 코드로](https://ko.wikipedia.org/wiki/위치_독립_코드 "wikilink") 컴파일되어 있어서 직접 이동해가며 메모리 영역 전반을 테스트할 수 있다.\[6\] 두 버전 모두 현행의 [멀티 코어](../Page/멀티_코어.md "wikilink") [CPU](../Page/중앙_처리_장치.md "wikilink") 및 호환 칩셋을 지원한다.\[7\]\[8\]

MemTest86 2.3과 Memtest86+ 1.60을 기점으로 [리눅스 커널용](../Page/리눅스_커널.md "wikilink") BadRAM 패치에 의해 예측되는 포맷으로 불량 RAM 영역 목록을 출력할 수 있다.\[9\]\[10\] [GRUB](../Page/GRUB.md "wikilink")을 사용하면 패치되지 않은 커널의 동일한 정보를 제공할 수 있으므로 BadRAM 패치가 필요하지 않다.\[11\]

2013년 2월, 오리지널 MemTest86은 패스마크(PassMark)에 판매되었다. 바이오스 버전은 버전 4.3.7까지 GPL 라이선스로 업데이트되었다. 그때까지 2개 포크의 기능 집합은 대체적으로 동일하였다.\[12\]

버전 5.0(2013년 12월 3일)은 [UEFI](../Page/통일_확장_펌웨어_인터페이스.md "wikilink") 부팅을 위해 다시 작성되어 [안전 부팅](../Page/통일_확장_펌웨어_인터페이스.md "wikilink")(secure boot) 승인과 마우스 지원을 가능케 한다. 모든 UEFI 버전들은 사유 프리웨어 라이선스로 공개된다. UEFI를 사용할 수 없는 경우 버전 5.0 이상에서 BIOS 부팅으로 회귀하여 구 버전 4.3.7을 불러들인다. 버전 6.0.0(2015년 12월 13일)은 DDR4 RAM 지원, 또 김윤구 등의 연구에 기반한 row-hammer 테스트를 추가한다.\[13\]\[14\]\[15\]

## 각주

## 외부 링크

  - [Official website of Memtest86+](http://www.memtest.org/)

[분류:컴퓨터 메모리](https://ko.wikipedia.org/wiki/분류:컴퓨터_메모리 "wikilink") [분류:윈도우용 유틸리티](https://ko.wikipedia.org/wiki/분류:윈도우용_유틸리티 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.  <https://www.memtest86.com/support/ver_history.htm>
10. <http://www.memtest.org/#change>
11.
12.
13.
14.
15.