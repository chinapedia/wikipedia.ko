> This article is converted from Wikipedia: [PE ](https://ko.wikipedia.org/wiki/PE_).


**PE 포맷**()은 [윈도우](https://ko.wikipedia.org/wiki/윈도우 "wikilink") 운영 체제에서 사용되는 [실행 파일](https://ko.wikipedia.org/wiki/실행_파일 "wikilink"), [DLL](https://ko.wikipedia.org/wiki/동적_링크_라이브러리 "wikilink"), object 코드, FON 폰트 파일\[1\] 등을 위한 파일 형식이다. PE 포맷은 윈도우 로더가 실행 가능한 코드를 관리하는데 필요한 정보를 캡슐화한 데이터 구조체이다. 이것은 [링킹을 위한 동적 라이브러리 참조](https://ko.wikipedia.org/wiki/라이브러리_\(컴퓨팅\) "wikilink"), [API](../Page/API.md "wikilink") 익스포트와 임포트 테이블, 자원 관리 데이터 그리고 [TLS](https://ko.wikipedia.org/wiki/스레드_로컬_저장소 "wikilink") 데이터를 포함한다. [윈도우 NT](https://ko.wikipedia.org/wiki/윈도우_NT "wikilink") 운영체제에서, PE 포맷은 [EXE](https://ko.wikipedia.org/wiki/EXE "wikilink"), [DLL](https://ko.wikipedia.org/wiki/DLL "wikilink"), [SYS](https://ko.wikipedia.org/wiki/SYS "wikilink") ([디바이스 드라이버](https://ko.wikipedia.org/wiki/디바이스_드라이버 "wikilink")), 그리고 다른 파일 종류들에서 쓰인다. [통일 확장 펌웨어 인터페이스](https://ko.wikipedia.org/wiki/통일_확장_펌웨어_인터페이스 "wikilink") (EFI) 설명서는 PE가 EFI 환경에서 표준 실행 파일 형식이라고 언급한다.\[2\]

윈도우 NT 운영 체제에서, PE는 현재 [IA-32](https://ko.wikipedia.org/wiki/IA-32 "wikilink"), [IA-64](https://ko.wikipedia.org/wiki/IA-64 "wikilink"), [x86-64](https://ko.wikipedia.org/wiki/x86-64 "wikilink") (AMD64/Intel64), 그리고 [ARM](https://ko.wikipedia.org/wiki/ARM_아키텍처 "wikilink") instruction set architectures (ISAs)를 지원한다. 윈도우 2000 이전에서, 윈도우 NT는 (그리고 PE) MIPS, Alpha, 그리고 [파워PC](../Page/파워PC.md "wikilink") ISAs를 지원했다. PE가 [윈도우 CE에서](https://ko.wikipedia.org/wiki/윈도우_CE "wikilink") 사용되므로 이것은 MIPS, ARM (Thumb 포함), 그리고 SuperH ISA의 변형들을 지원하고 있다.

PE와 비슷한 형식으로 ELF ([리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink")와 대부분의 다른 [유닉스](https://ko.wikipedia.org/wiki/유닉스 "wikilink") 버전들) 와 Mach-O ([Mac OS X](https://ko.wikipedia.org/wiki/OS_X "wikilink"))가 있다.

## 역사

마이크로소프트는 \[\[윈도우_NT_3.1|윈도우 NT 3.1\]\] 운영 체제의 도입과 함께 PE 포맷으로 옮긴다. 윈도우의 이후 버전들도 이 형식을 지원한다. 이 형식은 도스와 NT 시스템 사이의 차이를 연결하기 위한 한정된 유산을 가지고 있다. 예를 들면, PE/COFF 헤더들은 아직도 [MS-DOS 실행 파일을](../Page/MZ_실행_파일.md "wikilink") 포함한다. 기본적으로 이것은 "This program cannot be run in DOS mode" 메시지를 보여주는 [스텁이다](../Page/메소드_스텁.md "wikilink").\[3\] PE는 또한 윈도우 플랫폼의 변화를 계속해서 지원한다. 이것들은 .NET PE 포맷, PE32+로 불리는 64비트 버전 (가끔은 PE+), 그리고 윈도우 CE를 위한 명세서가 있다.

## 기술적 세부사항

### 레이아웃

[섬네일](https://ko.wikipedia.org/wiki/파일:Portable_Executable_32_bit_Structure_in_SVG.svg "wikilink") PE 파일은 [동적 링커에게](https://ko.wikipedia.org/wiki/동적_링커 "wikilink") 파일을 메모리로 어떻게 매핑할지 설명하는 많은 헤더들과 섹션들로 이루어져 있다. 실행 가능한 이미지는 (각각 다른 메모리 보호를 요구하는) 여러 다른 영역으로 이루어져 있다. 그래서 각 섹션의 시작은 반드시 페이지 경계에 맞춰 정렬되어야 한다. 예를 들면, 전형적인 .text 섹션(프로그램 코드를 가지는)의 경우 execute/readwrite 으로 매핑되어야 하고 .data 섹션(전역 변수들을 가지는)의 경우 no-execute/readwrite로 매핑되어야 한다. 그러나 공간 낭비를 피하기 위해서, 다른 섹션들은 디스크에서 페이지 정렬되어 있지 않다. 동적 링커의 일 중 하나는 각 섹션을 개별적으로 메모리에 매핑하고, 헤더에 있는 지시에 따라 그곳에 정확한 권한을 할당하는 것이다.

### 임포트 테이블

import address table (IAT) 섹션은 응용 프로그램이 다른 모듈에서 함수를 호출할 때 검색 테이블로 사용된다. 이것은 [서수에 의한 들여오기나 이름에 의한 들여오기가](https://ko.wikipedia.org/wiki/동적_링크_라이브러리 "wikilink") 될 수 있다. 컴파일 된 프로그램은 의존하는 라이브러리의 메모리 위치를 모르기 때문에 API 호출 시 간접적인 점프가 요구된다. 동적 링커가 모듈을 로드하고 연결시키고, 실제 주소를 IAT에 넣는다. 그 후 상응하는 라이브러리 함수의 메모리 위치를 가리키게 된다. 비록 이 추가로 인해 모듈 내부의 호출에도 추가적인 점프가 요구되지만 이것은 중요한 이점을 가진다. 로더에 의해 변경되며 [copy-on-write](https://ko.wikipedia.org/wiki/copy-on-write "wikilink")가 요구되는 메모리 페이지들의 수가 최소화돼서 메모리와 디스크의 입출력 시간을 절약할 수 있다. 만약 컴파일러가 호출이 모듈 내부에서 일어나는 것이라고 미리 안다면 더 최적화된 코드를 생산할 수도 있다.

### 재배치

PE 파일들은 [위치 독립적 코드를](https://ko.wikipedia.org/wiki/위치_독립적_코드 "wikilink") 포함하지 않는다. 대신에 선호되는 우선되는 베이스 주소로 컴파일되고, 모든 주소들은 그 전에 고정된다. 만약 PE 파일이 우선되는 주소에 로드될 수 없다면(다른게 이미 위치하고 있는 경우) 운영 체제는 베이스 주소를 바꾼다. 이것은 모든 절대 주소를 다시 계산하고 새로운 값을 사용하도록 코드를 바꾸는 것을 포함한다. 로더는 이것을 우선되는 주소와 실제 로드될 주소를 비교하고 델타 값을 계산함으로써 수행한다. 그 후 우선되는 주소에 새로운 주소의 위치에 대한 값이 더해진다. 베이스 재배치들은 메모리 위치에 목록화되고 저장된다. 결과 코드는 이제 프로세스에 사적이 되고 공유될 수 없게 됨으로써 DLL의 수많은 메모리 절약 이점이 사라진다. 또한 모듈을 로딩하는 시간도 매우 느려지게 된다. 이 이유로 이러한 재배치는 가능한 한 피해지며, 마이크로소프트에서 나온 DLL들은 겹쳐질 수 없게 만들어져 있다.

## 다른 운영 체제에서의 사용

[x86](https://ko.wikipedia.org/wiki/x86 "wikilink")의 [유닉스 계열](https://ko.wikipedia.org/wiki/유닉스_계열 "wikilink") 운영체제들에서 몇몇 윈도우 바이너리들은 [와인으로](https://ko.wikipedia.org/wiki/와인_\(소프트웨어\) "wikilink") 돌아갈 수 있다. [맥 OS X 10.5는](https://ko.wikipedia.org/wiki/맥_OS_X_10.5 "wikilink") PE 파일들을 로드하고 분석할 수 있는 기능을 갖지만 윈도우와 호환은 되지 않는다.\[4\]

## 같이 보기

  - [EXE](https://ko.wikipedia.org/wiki/EXE "wikilink")
  - [A.out](https://ko.wikipedia.org/wiki/A.out "wikilink")
  - [실행 파일 압축](https://ko.wikipedia.org/wiki/실행_파일_압축 "wikilink")
  - [응용 프로그램 가상화](https://ko.wikipedia.org/wiki/응용_프로그램_가상화 "wikilink")

## 각주

## 관련 도서

  - 《Windows 시스템 실행 파일의 구조와 원리》

## 외부 링크

  - [마이크로소프트 PE Coff 파일포맷 스페시피케이션](http://www.microsoft.com/whdc/system/platform/firmware/PECOFF.mspx)
  - [매트 피트렉, 최초의 PE 관련기사 (MSDN 매거진, 1994년 3월호)](http://msdn2.microsoft.com/en-us/library/ms809762.aspx)
  - [Part I. An In-Depth Look into the Win32 Portable Executable File Format by Matt Pietrek ([MSDN](https://ko.wikipedia.org/wiki/마이크로소프트_개발자_네트워크 "wikilink") Magazine, February 2002)](https://web.archive.org/web/20071003062701/http://msdn.microsoft.com/msdnmag/issues/02/02/PE/default.aspx)
  - [Part II. An In-Depth Look into the Win32 Portable Executable File Format by Matt Pietrek ([MSDN](https://ko.wikipedia.org/wiki/마이크로소프트_개발자_네트워크 "wikilink") Magazine, March 2002)](https://web.archive.org/web/20070907211207/http://msdn.microsoft.com/msdnmag/issues/02/03/PE2/default.aspx)
  - [PE File Format Diagram](http://www.openrce.org/reference_library/)
  - [The .NET File Format by Daniel Pistelli](https://web.archive.org/web/20070327230345/http://www.codeproject.com/dotnet/dotnetformat.asp)
  - [Creating the smallest possible PE executable 97bytes](https://web.archive.org/web/20091221124836/http://www.phreedom.org/solar/code/tinype/)
  - [Detailed description of the PE format by Johannes Plachy](http://www.csn.ul.ie/~caolan/publink/winresdump/winresdump/doc/pefile.html)
  - [윈도우 실행 정보](http://code.google.com/p/corkami/wiki/PE101)

### 관련 도구

  - [PEBrowse](http://www.smidgeonsoft.com/) PE 파일 뷰어 유틸리티.
  - [CFF Explorer](http://www.ntcore.com/exsuite.php) PE 편집기. [닷넷 프레임워크를](../Page/닷넷_프레임워크.md "wikilink") 지원하는 최초의 PE 편집기.
  - [PE Explorer](http://www.heaventools.com/) PE 파일 뷰어/편집기. (셰어웨어)
  - [yoda's LordPE Deluxe](https://web.archive.org/web/20120117181944/http://www.woodmann.net/collaborative/tools/images/Bin_LordPE_2007-10-21_1.48_LordPE_1.41_Deluxe_b.zip), 덤퍼가 포함된 PE 편집기.
  - [PEDUMP](http://download.microsoft.com/download/8/3/f/83f69587-47f1-48e2-86a6-aab14f01f1fe/PE.exe) 콘솔 응용 프로그램 + 소스 코드(C++), 텍스트로 리디렉트한 다음 두 텍스트를 비교하기 좋음.
  - [GNU Binutils](https://ko.wikipedia.org/wiki/GNU_바이너리_유틸리티 "wikilink") --target=i386-pe, --target=mips-pe
  - [Anywhere PE Viewer](https://web.archive.org/web/20071002071010/http://www.ucware.com/apev/) 자바 응용 프로그램.
  - [PE](https://web.archive.org/web/20070930021637/http://www.bigosoupsoftware.com/product.html) PE (.exe, .ocx, .dll 등)을 읽어서 섹션(section)을 볼 수 있고 리소스를 불러오거나 내보낼 수 있음.
  - [SK PEInfo for Windows CE](https://web.archive.org/web/20070928212753/http://pocketpcfreewares.com/en/index.php?soft=660) 윈도우 CE용 PE 뷰어.
  - [pefile](http://code.google.com/p/pefile/) 파이썬(프로그래밍) 모듈.
  - [anal_pe](http://www.mikekohn.net/file_formats/anal_pe.php) 명령 줄 기반의 도구. [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink")와 윈도우에서 동작.

[분류:파일 포맷](https://ko.wikipedia.org/wiki/분류:파일_포맷 "wikilink") [분류:실행 파일 포맷](https://ko.wikipedia.org/wiki/분류:실행_파일_포맷 "wikilink")

1.  , a note on p.18, states that "this image type is chosen to enable UEFI images to contain Thumb and Thumb2 instructions while defining the EFI interfaces themselves to be in ARM mode."
2.  , a note on p.18, states that "this image type is chosen to enable UEFI images to contain Thumb and Thumb2 instructions while defining the EFI interfaces themselves to be in ARM mode."
3.  E.g. Microsoft's linker has [/STUB switch](http://msdn.microsoft.com/en-us/library/7z0585h5.aspx) to attach one
4.