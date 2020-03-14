> This article is converted from Wikipedia: [ HEX](https://ko.wikipedia.org/wiki/_HEX).


**인텔 HEX**(Intel HEX)는 [ASCII](https://ko.wikipedia.org/wiki/미국정보교환표준부호 "wikilink") 텍스트 형식으로 이진 정보를 전달하는 [파일 형식이다](https://ko.wikipedia.org/wiki/파일_형식 "wikilink"). 이것은 [마이크로컨트롤러](https://ko.wikipedia.org/wiki/마이크로컨트롤러 "wikilink"), [EPROM](https://ko.wikipedia.org/wiki/EPROM "wikilink") 그리고 다른 [논리 장치의](https://ko.wikipedia.org/wiki/설계_가능_논리_소자 "wikilink") 프로그래밍을 위해 흔히 사용된다. 대표적으로 [컴파일러](https://ko.wikipedia.org/wiki/컴파일러 "wikilink")나 [어셈블러는](https://ko.wikipedia.org/wiki/어셈블리어#어셈블러 "wikilink") [컴퓨터 프로그램의](https://ko.wikipedia.org/wiki/컴퓨터_프로그램 "wikilink") [소스 코드를](https://ko.wikipedia.org/wiki/소스_코드 "wikilink") (예를 들어 [C나](https://ko.wikipedia.org/wiki/C_\(프로그래밍_언어\) "wikilink") [어셈블리어](https://ko.wikipedia.org/wiki/어셈블리어 "wikilink")) [기계어](https://ko.wikipedia.org/wiki/기계어 "wikilink")로 변환하고, 이를 HEX 파일로 출력한다. 그리고 나서 이 HEX 파일은 [소자 프로그래머가](https://ko.wikipedia.org/wiki/소자_프로그래머 "wikilink") 읽어서 [ROM를](https://ko.wikipedia.org/wiki/고정_기억_장치 "wikilink") 굽거나, 메모리에 올리고 실행하기 위해 목적 시스템으로 전송된다.\[1\]

## 형식

인텔 HEX는 [LF나](https://ko.wikipedia.org/wiki/새줄_문자 "wikilink") [CR로](https://ko.wikipedia.org/wiki/캐리지_리턴 "wikilink") 구분된 여러줄의 [ASCII](https://ko.wikipedia.org/wiki/미국정보교환표준부호 "wikilink") 텍스트로 구성된다. 각 줄은 다수의 바이너리 숫자를 [부호화한](https://ko.wikipedia.org/wiki/:en:Binary-to-text_encoding "wikilink") [16진수](https://ko.wikipedia.org/wiki/십육진법 "wikilink") 문자를 담고 있다. 이 바이너리 숫자가 줄에서의 위치, 종류, 줄의 길이에 따라 [메모리 주소나](https://ko.wikipedia.org/wiki/메모리_주소 "wikilink") 기타의 값인 데이터를 나타낼 것이다. 각 텍스트 줄을 레코드(*record*)라고 한다.

### 레코드 구조

하나의 [레코드](https://ko.wikipedia.org/wiki/:en:Record_\(computer_science\) "wikilink")(텍스트 한줄)는 왼쪽에서 오른쪽으로 순서대로 여섯가지 [필드](https://ko.wikipedia.org/wiki/Field_\(computer_science\) "wikilink")(부분)로 나타난다.

1.  **시작코드(Start code)**, 한 문자, ASCII 문자 ':'(colon).
2.  **바이트 개수(Byte count)**, 16진수 문자 두 자리, 데이터 필드에 있는 바이트(16진수 두 문자의 쌍)의 수를 가리킨다. 최대 바이트 개수는 255 (0xFF)다. 16 (0x10) 과 32 (0x20)가 흔히 쓰인다.
3.  **주소(Address)**, 16진수 문자 네 자리, 데이터의 16비트 시작 주소의 옵셋 값을 표현한다. 데이터의 물리 주소는 앞서 지정된 기준 주소에 이 옵셋을 더해서 구한다. 이런 식으로 16비트 주소의 한계인 64 킬로바이트를 넘는 주소를 지정 한다. 기준 주소의 기본값은 0이고, 여러 종류의 레코드로 값을 바꿀 수 있다. 기준 주소와 주소는 항상 [빅 엔디언으로](https://ko.wikipedia.org/wiki/엔디언 "wikilink") 표현된다.
4.  **레코드 종류(Record type)** (아래 [레코드 종류](https://ko.wikipedia.org/wiki/인텔_HEX#레코드_종류 "wikilink") 참조), 16진수 문자 두 자리, *00*에서 *05*, 데이터 필드의 종류를 정의한다.
5.  **데이터(Data)**, 2*n* 개의 16진수 문자로 표현된 *n* 바이트의 데이터 열이다. 어떤 레코드는 이 필드가 빠져 있다(*n*이 0). 데이터 바이트들의 의미나 해석은 응용프로그래밍에 달렸다.
6.  **체크섬([Checksum](https://ko.wikipedia.org/wiki/Checksum "wikilink"))**, 16진수 문자 두 자리, 레코드에 오류가 없음을 입증하는데 이용될 수 있는 계산된 값이다.

#### 색 일러두기

이 문서에서 Intel HEX 레코드의 필드들은 눈에 잘 띄도록 다음처럼 색칠된다.

#### 체크섬 계산

레코드의 [체크섬](https://ko.wikipedia.org/wiki/체크섬 "wikilink") 바이트는 레코드에서 체크섬에 앞서 있는 모든 복호화된 바이트 합의 [최하위 바이트](https://ko.wikipedia.org/wiki/최하위_비트 "wikilink")(LSB)의 [2의 보수이다](https://ko.wikipedia.org/wiki/2의_보수 "wikilink"). 이것은 복호화된 값(파일에 있는 16진수 문자가 아니라 그것을 두 개씩 짝지어 바이트로 해석한 값)들을 모두 더하고, 더한 값의 LSB(256으로 나눌 때 나머지)를 뽑아서 그것의 2의 보수(모든 비트를 [뒤집고](https://ko.wikipedia.org/wiki/1의_보수 "wikilink") 1를 더한다)를 구한 것이다.

예를 들어,  이런 레코드에서 길이부터 체크썸 전까지를 합하면  +  +  +  +  +  +  = `E2`이다. `E2`의 [2의 보수는](https://ko.wikipedia.org/wiki/2의_보수 "wikilink") 이다.

레코드의 유효함은 체크섬을 계산하고, 계산한 체크섬과 레코드에 있는 체크섬이 같다는 것을 확인해서 검사될 수 있다; 체크섬이 다르다는 것은 오류가 있음을 가리키는 것이다. 레코드의 체크섬이 데이터 체크섬의 음수라서 체크섬을 포함하는 전체 복호화된 바이트를 더하면 LSB는 0이 된다.

### 줄 종료문자

인텔 HEX 레코드는 각 레코드가 한 줄의 텍스트에 날 수 있도록 하나 이상의 ASCII 줄 끝 문자로 구분된다. 이것은 시가적인 가독성을 높여주고, 레코드 사이에 끼워져 있어 기계의 [구문 분석](https://ko.wikipedia.org/wiki/구문_분석 "wikilink") 효율을 향상시키는데 이용될 수 있다.

HEX 레코드를 만들어내는 프로그램은 전형적으로 사용하는 [운영 체제의](https://ko.wikipedia.org/wiki/운영_체제 "wikilink") 관례에 따른 줄 끝 문자를 사용한다. 예를 들어, 리눅스 프로그램은 하나의 LF([줄 바꿈](https://ko.wikipedia.org/wiki/새줄_문자 "wikilink"), 16진수 값 `0A`) 문자만 사용하고, 윈도우즈 프로그램은 CR ([CR](https://ko.wikipedia.org/wiki/캐리지_리턴 "wikilink"), 16진수 값 `0D`)과 LF를 이어서 쓴다.

### 레코드 종류

현재 여섯가지 종류가 있다.:

| Hex code | Record type | Description | Example     |
| -------- | ----------- | ----------- | ----------- |
| {{인텔 HEX | |00         | }}          | 데이터         |
| {{인텔 HEX | |01         | }}          | 파일의 끝       |
| {{인텔 HEX | |02         | }}          | 확장된 세그먼트 주소 |
| {{인텔 HEX | |03         | }}          | 시작 세그먼트 주소  |
| {{인텔 HEX | |04         | }}          | 확장된 선형 주소   |
| {{인텔 HEX | |05         | }}          | 시작 선형 주소    |

### 다른 이름

때때로 레코드 종류의 일부만 채용한 HEX 파일 형식을 지칭하기 위해 특별한 이름이 사용된다. 예를 들어:

  - **I8HEX** 파일은 과  레코드만 사용한다. (16비트 주소지정)
  - **I16HEX** 파일은 에서 까지의 레코드만 사용한다. (20비트 주소지정)
  - **I32HEX** 파일은 , ,  그리고  레코드만 사용한다. (32비트 주소지정)

## 파일 예제

이 예제는 4개의 데이터 레코드와 뒤따르는 끝 레코드를 보여준다.






## 같이 보기

  - 글

<!-- end list -->

  - [:en:Binary-to-text encoding](https://ko.wikipedia.org/wiki/:en:Binary-to-text_encoding "wikilink"), a survey and comparison of encoding algorithms
  - [SREC](https://ko.wikipedia.org/wiki/:en:SREC_\(file_format\) "wikilink"), hex file format by Motorola
  - [TekHex](https://ko.wikipedia.org/wiki/:en:Tektronix_extended_HEX "wikilink"), hex file format by Tektronix

<!-- end list -->

  - 기타

<!-- end list -->

  - [틀:인텔 HEX](../Page/틀:인텔_HEX.md "wikilink")

## 각주

## 외부 링크

  - 문서

<!-- end list -->

  - [Intel HEX format description](http://www.piclist.com/techref/fileext/hex/intel.htm)
  - [Intel HEX reference with examples](http://www.sbprojects.com/knowledge/fileformats/intelhex.php)

<!-- end list -->

  - 소프트웨어

<!-- end list -->

  - [binex](http://www.nlsw.nl/software/) , a converter between Intel HEX and binary
  - [libgis](http://github.com/vsergeev/libGIS) , open source library that converts Intel HEX and other formats
  - [SRecord](http://srecord.sourceforge.net/) , a converter between Intel HEX and binary ([usage](https://web.archive.org/web/20160304082402/https://delog.wordpress.com/2011/05/26/convert-a-bin-file-to-hex/))
  - [bincopy](https://pypi.python.org/pypi/bincopy)  is a python package for manipulating Intel HEX format files.

[분류:임베디드 시스템](https://ko.wikipedia.org/wiki/분류:임베디드_시스템 "wikilink") [분류:파일 포맷](https://ko.wikipedia.org/wiki/분류:파일_포맷 "wikilink")

1.  Intel: "[Hexadecimal Object File Format Specification](http://microsym.com/editor/assets/intelhex.pdf) ", Revision A, January 6, 1988