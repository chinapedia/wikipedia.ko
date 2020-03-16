> This article is converted from Wikipedia: [COM ](https://ko.wikipedia.org/wiki/COM_).


[파일 확장자](../Page/파일_확장자.md "wikilink") **.com**은 다양한 컴퓨터 시스템에서 다른 목적으로 사용되어 왔다. 초기에, 이 용어는 "명령 파일"을 대표하는 말이었으며 운영 체제에 내보낼 명령어를 포함하는 텍스트 파일이었다. 1970년대로 거슬러 올라가서, [디지털 이큅먼트 코퍼레이션](../Page/디지털_이큅먼트_코퍼레이션.md "wikilink") [미니컴퓨터](../Page/미니컴퓨터.md "wikilink") 및 [메인프레임](../Page/메인프레임.md "wikilink") 컴퓨터 시스템에 실용적으로 쓰이게 되었다.

[마이크로컴퓨터](../Page/마이크로컴퓨터.md "wikilink")의 도입과 더불어, 확장자 .com으로 끝나는 파일의 사용은 점차 바뀌어 갔다. [MS-DOS](../Page/MS-DOS.md "wikilink") 호환 도스와 8 비트 [CP/M](https://ko.wikipedia.org/wiki/CP/M "wikilink")에서, **COM 파일**은 단순히 [실행 파일의](../Page/실행_파일.md "wikilink") 종류이다.

이 파일 형식의 이름은 [파일 확장자](../Page/파일_확장자.md "wikilink") .com에서 나온 것이며(최상위 도메인 [.com](../Page/.com.md "wikilink")과 헷갈리지 말 것) 각 파일에 쓰이는 초기의 확장자였다. 그러나 CP/M과 매우 초기의 MS-DOS 버전을 제외하고는 [파일 형식과](https://ko.wikipedia.org/wiki/파일_형식 "wikilink") 파일 확장자 사이의 실제적인 통합은 없었다.

## 플랫폼 지원

이 포맷은 여전히 현대의 [윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 기반의 [플랫폼의](../Page/컴퓨팅_플랫폼.md "wikilink") [실행 파일이지만](../Page/실행_파일.md "wikilink") MS-DOS 가상 구현 체계에서 돌아간다. x64 계열의 운영 체제에서는 이러한 가상 구현 체계가 없으므로 실행되지 않는다. (역자 주: 가상 구현에 대해서는 [NTVDM](https://ko.wikipedia.org/wiki/NTVDM "wikilink") 참조)

COM 파일은 또한 [도스박스](../Page/도스박스.md "wikilink")와 같은 도스 에뮬레이터를 사용하여 실행할 수 있다. 이 에뮬레이터는 모든 플랫폼에서 지원한다. "COM"은 "core image"(코어 이미지)의 준말이며, 이러한 .com 파일이 컴퓨터에서 실행할 수 있는 기본 명령어에 대한 코드를 포함했기 때문에 "command"(명령어)로 해석되기도 한다.

## 이진 포맷

COM 포맷은 가장 단순한 실행 포맷이며, [메타데이터](../Page/메타데이터.md "wikilink")는 없고, 코드와 데이터만 포함하고 있으며 일부 세그먼트의 오프셋 [0x](../Page/십육진법.md "wikilink")0100에서 [로드되어](https://ko.wikipedia.org/wiki/로더_\(컴퓨팅\) "wikilink") 실행된다. [세그멘테이션](https://ko.wikipedia.org/wiki/x86_메모리_세그먼트 "wikilink") 모델이 잘 동작하기 때문에 [구조 배치가](https://ko.wikipedia.org/wiki/릴로케이션 "wikilink") 필요하지 않다. 파일 크기가 파일 시스템의 최대 용량을 지원하는 [EXE](../Page/EXE.md "wikilink") 파일과는 달리 COM의 최대 지원 용량은 65536바이트(64[킬로바이트](../Page/킬로바이트.md "wikilink"))이다.

## 실행 우선도

실행 파일로는 EXE, COM, BAT 등이 있다. 이를테면, 한 디렉터리가 COM 파일과 EXE 파일이 확장자만 다르고 같은 이름을 가지고 있다고 하면 이 경우 COM 파일이 우선하여 실행된다.

## 외부 링크

  - [John Elliott's article on the extended CP/M-80 3.0 COM file header](http://www.seasip.demon.co.uk/Cpm/rsxrec.html)

[분류:도스 기술](https://ko.wikipedia.org/wiki/분류:도스_기술 "wikilink") [분류:실행 파일 포맷](https://ko.wikipedia.org/wiki/분류:실행_파일_포맷 "wikilink")