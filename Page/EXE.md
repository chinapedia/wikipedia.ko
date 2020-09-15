> This article is converted from Wikipedia: [EXE](https://ko.wikipedia.org/wiki/EXE).


**EXE**는 일반적인 [파일 확장자로](../Page/파일_확장자.md "wikilink") [컴퓨터 프로그램의](../Page/컴퓨터_프로그램.md "wikilink") [실행 파일을](../Page/실행_파일.md "wikilink") 가리킨다. [오픈VMS](https://ko.wikipedia.org/wiki/오픈VMS "wikilink"), [도스](../Page/도스.md "wikilink"), [마이크로소프트 윈도우](../Page/마이크로소프트_윈도우.md "wikilink"), [리엑트오에스](https://ko.wikipedia.org/wiki/리엑트오에스 "wikilink"), [OS/2](https://ko.wikipedia.org/wiki/OS/2 "wikilink") 운영 체제에서 사용할 수 있다.

실행 프로그램 자체뿐 아니라, 많은 EXE 파일들은 비트맵, 실행 프로그램이 [그래픽 사용자 인터페이스를](../Page/그래픽_사용자_인터페이스.md "wikilink") 사용하는, 아이콘과 같은 [리소스라고](https://ko.wikipedia.org/wiki/리소스_\(컴퓨터_과학\) "wikilink") 불리는 다른 구성 요소들을 포함할 수 있다.

도스 실행 파일 포맷은 64 [킬로바이트](../Page/킬로바이트.md "wikilink")로 크기가 제한되는 [COM](../Page/COM_파일.md "wikilink") 실행 파일과 다르다. 도스 실행 파일 헤더는 여러 개의 세그먼트가 [DMA에서](https://ko.wikipedia.org/wiki/기억_직접_접근 "wikilink") 로드될 수 있으며 64 킬로바이트 이상의 실행 파일을 지원하는 리로케이션 정보를 포함하고 있다.

## 파일 형식

### 도스

.exe 확장자와 함께 쓰이는 여러 종류의 다양한 [파일 형식이](https://ko.wikipedia.org/wiki/파일_형식 "wikilink") 있다.

  - 16-bit DOS MZ 실행 파일 (Executable):원래 도스 실행 파일 포맷. 이것들은 파일 시작 부분의 아스키 코드 "MZ" 문자로 구별된다.
    16-bit New 실행 파일 (Executable):멀티태스킹 MS-DOS 4.0에서 도입되어, 16-bit OS/2 와 윈도우에서 사용되었으며, NE는 아스키 코드 "NE" 문자로 구별된다.

### OS/2

  - 32-bit 선형 실행 파일 (Linear Executable):OS/2 2.0에서 도입되었으며, 이것들은 아스키 코드 "LX"로 구별된다. 이것들은 오직 OS/2 2.0와 그 이상 버전에서만 사용 가능하다.<ref>{{웹 인용

`|url=`<http://www.operating-system.org/betriebssystem/_english/bs-os2.htm>
`|title=OS/2 Operating System`
`|date=2004-04-03`
`|accessdate=2016-02-12`
`|work=operating system documentation project`

}}</ref> 또한 몇몇 DOS extenders에 의해 사용된다.

  - Mixed 16/32-bit 선형 실행 파일 (Linear Executable): OS/2 2.0에서 도입되었으며, 이것들은 아스키 코드 "LE"로 구별된다. 이 포맷은 [VxD](https://ko.wikipedia.org/wiki/VxD "wikilink") 드라이버로 사용되며, 또한 몇몇 DOS extenders에 의해 사용된다. ([윈도우 3.x](https://ko.wikipedia.org/wiki/윈도우_3.x "wikilink"), [OS/2](https://ko.wikipedia.org/wiki/OS/2 "wikilink"), 그리고 윈도우 9x)

### 윈도우

  - 16-bit New Executable:16비트 또는 32비트 윈도우 실행 파일은 NE 또는 PE에서 실행되며, MZ 코드는 "DOS stub"이라고 불리며 무시된다.<ref>{{웹 인용

`|title=/STUB (MS-DOS Stub File Name)`
`|url=`<http://msdn.microsoft.com/en-us/library/7z0585h5.aspx>
`|work=MSDN`
`|publisher=`[`마이크로소프트`](../Page/마이크로소프트.md "wikilink")
`|accessdate=2016-02-12`

}}</ref>\[1\] [도스](../Page/도스.md "wikilink")에서 실행되는 경우, 스텁 코드는 "This program cannot be run in DOS mode" 메시지를 표시하고 종료된다. [regedit](../Page/윈도우_레지스트리.md "wikilink")\[2\] 이나 오래된 WinZIP self extractors 같은 소수의 듀얼 모드 프로그램은 더 기능적인 DOS 섹션을 포함한다.\[3\]

  - 32-bit Portable Executable:윈도우 NT에 도입되었으며, 아스키 코드 "PE"로 구별된다. (비록 시작 부분은 아니지만 이 파일도 "MZ"로 시작한다)<ref>{{웹 인용

`|url=`<http://msdn.microsoft.com/en-us/windows/hardware/gg463119.aspx>
`|title=Microsoft PE and COFF Specification`

}}</ref>

  - 64-bit Portable Executable (PE32+):64비트 버전의 윈도우에서 도입되었으며 확장된 필드를 갖는 PE 파일이다. 대부분의 경우 코드는 32비트 또는 64비트 어느 하나에서 돌아갈 수 있게 써질 수 있다.<ref>{{저널 인용

`|url=`<http://msdn.microsoft.com/en-us/magazine/cc301805.aspx>
`|title=An In-Depth Look into the Win32 Portable Executable File Format`
`|work=MSDN Magazine`
`|publisher=`[`마이크로소프트`](../Page/마이크로소프트.md "wikilink")
`|date=February 2002`
`|first=Matt`
`|last=Pietrek`

}}</ref>

## 같이 보기

  - [실행 파일](../Page/실행_파일.md "wikilink")
  - [MZ 실행 파일](../Page/MZ_실행_파일.md "wikilink")
  - [PE 포맷](../Page/PE_포맷.md "wikilink")

## 각주

## 외부 링크

  - [MZ EXE header format](http://www.delorie.com/djgpp/doc/exe/)

[분류:파일 포맷](https://ko.wikipedia.org/wiki/분류:파일_포맷 "wikilink") [분류:실행 파일 포맷](https://ko.wikipedia.org/wiki/분류:실행_파일_포맷 "wikilink") [분류:도스 기술](https://ko.wikipedia.org/wiki/분류:도스_기술 "wikilink") [분류:윈도우 관리](https://ko.wikipedia.org/wiki/분류:윈도우_관리 "wikilink")

1.
2.
3.