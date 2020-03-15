> This article is converted from Wikipedia: [C  ](https://ko.wikipedia.org/wiki/C__).


프로그래밍 언어 [C는](https://ko.wikipedia.org/wiki/C_\(프로그래밍_언어\) "wikilink") [파일](https://ko.wikipedia.org/wiki/컴퓨터_파일 "wikilink") [입출력](https://ko.wikipedia.org/wiki/입출력 "wikilink")을 위한 많은 [표준 라이브러리](https://ko.wikipedia.org/wiki/표준_라이브러리 "wikilink") [기능들을](https://ko.wikipedia.org/wiki/서브루틴 "wikilink") 제공한다. 이 기능들은 대부분 [C 표준 라이브러리](https://ko.wikipedia.org/wiki/C_표준_라이브러리 "wikilink") [헤더 파일](https://ko.wikipedia.org/wiki/헤더_파일 "wikilink") 로부터 구성된다.\[1\] 이 기능들은 1970년대 초반 벨 연구소의 [마이크 레스크가](https://ko.wikipedia.org/wiki/마이크_레스크 "wikilink") 작성한 "휴대용 입출력 패키지"에서 왔으며,\[2\] [유닉스](https://ko.wikipedia.org/wiki/유닉스 "wikilink") [버전 7에서](https://ko.wikipedia.org/wiki/버전_7_유닉스 "wikilink") 정식으로 운영체제의 한 부분이 되었다.\[3\]

C의 입출력 기능은 현대의 표준의 기준으로 하면 상당이 낮은 수준이다. C는 입력 스트림이나 출력 스트림과 같은 파일에 대한 모든 작업들을 [바이트](https://ko.wikipedia.org/wiki/바이트 "wikilink") 단위의 흐름으로 추상화한다. 과거의 다른 프로그래밍 언어와는 달리 C는 데이터 파일에 [임의 액세스를](https://ko.wikipedia.org/wiki/임의_액세스 "wikilink") 하는 기능을 제공하지 않고 대신, 파일 매체 저장소를 읽기 위해 프로그래머가 스트림을 생성해줘야 한다. 파일 매체를 찾고, 스트림에서 바이트 단위로 연속으로 읽는다.

파일 입출력의 스트림 모델은 C 프로그래밍 언어가 개발되었을 때 같이 개발되던 유닉스를 통해 대중화되었다. 수많은 현대 운영체제는 유닉스로부터 스트림을 물려받았으며, [C 프로그래밍 언어군의](https://ko.wikipedia.org/wiki/:분류:C_프로그래밍_언어군 "wikilink") 많은 언어들도 C의 파일 입출력 인터페이스를 약간의 수정을 거쳐 물려받았다. (예시 - [PHP](https://ko.wikipedia.org/wiki/PHP "wikilink")).

## 개요

### 기능

C 파일 입출력 기능의 대부분은 [C 표준 라이브러리](https://ko.wikipedia.org/wiki/C_표준_라이브러리 "wikilink") [헤더 파일](https://ko.wikipedia.org/wiki/헤더_파일 "wikilink")\<stdio.h\> 에 정의되어 있다. (C++의 경우 표준 C 기능을 포함한 헤더 cstdio에 있으며 std 이름공간을 포함해야 함.)

<table>
<thead>
<tr class="header">
<th></th>
<th><p>바이트 문자</p></th>
<th><p>확장 문자</p></th>
<th><p>설명</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>파일 접근</p></td>
<td><p><a href="http://en.cppreference.com/w/c/io/fopen">fopen</a></p></td>
<td><p>파일 열기(윈도우에선 비-유니코드 파일 이름, 유닉에서는 UTF-8 파일 이름)</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="http://en.cppreference.com/w/c/io/freopen">freopen</a></p></td>
<td><p>존재하는 스트림으로 다른 파일 열기</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="http://en.cppreference.com/w/c/io/fflush">fflush</a></p></td>
<td><p>대응되는 파일로 출력 스트림 동기화하기</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="http://en.cppreference.com/w/c/io/fclose">fclose</a></p></td>
<td><p>파일 닫기</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="http://en.cppreference.com/w/c/io/setbuf">setbuf</a></p></td>
<td><p>파일 스트림에 버퍼 장착시키기</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="http://en.cppreference.com/w/c/io/setvbuf">setvbuf</a></p></td>
<td><p>파일 스트림 크기에 맞게 버퍼 장착</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="http://en.cppreference.com/w/c/io/fwide">fwide</a></p></td>
<td><p>전각 문자와 반각 문자간 파일 스트림 교환</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>직접 입출력</p></td>
<td><p><a href="http://en.cppreference.com/w/c/io/fread">fread</a></p></td>
<td><p>파일 읽기</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="http://en.cppreference.com/w/c/io/fwrite">fwrite</a></p></td>
<td><p>파일 쓰기</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>언포맷 입출력</p></td>
<td><p><a href="http://en.cppreference.com/w/c/io/fgetc">fgetc</a><br />
<a href="http://en.cppreference.com/w/c/io/getc">getc</a></p></td>
<td><p><a href="http://en.cppreference.com/w/c/io/fgetwc">fgetwc</a><br />
<a href="http://en.cppreference.com/w/c/io/getwc">getwc</a></p></td>
<td><p>파일 스트림으로 부터 바이트/ 읽기</p></td>
</tr>
<tr class="odd">
<td><p><a href="http://en.cppreference.com/w/c/io/fgets">fgets</a></p></td>
<td><p><a href="http://en.cppreference.com/w/c/io/fgetws">fgetws</a></p></td>
<td><p>파일 스트림으로 부터 바이트/ 라인 읽기</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="http://en.cppreference.com/w/c/io/fputc">fputc</a><br />
<a href="http://en.cppreference.com/w/c/io/putc">putc</a></p></td>
<td><p><a href="http://en.cppreference.com/w/c/io/fputwc">fputwc</a><br />
<a href="http://en.cppreference.com/w/c/io/putwc">putwc</a></p></td>
<td><p>파일 스트림에 바이트/ 쓰기</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="http://en.cppreference.com/w/c/io/fputs">fputs</a></p></td>
<td><p><a href="http://en.cppreference.com/w/c/io/fputws">fputws</a></p></td>
<td><p>파일 스트림에 바이트/ 문자열 입력</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="http://en.cppreference.com/w/c/io/getchar">getchar</a></p></td>
<td><p><a href="http://en.cppreference.com/w/c/io/getwchar">getwchar</a></p></td>
<td><p>표준 입력으로 부터 바이트/ 입력</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><s><a href="http://en.cppreference.com/w/c/io/gets">gets</a></s></p></td>
<td></td>
<td><p>새 줄이 나오거나 파일 끝까지 갈때 까지 표준 입력으로 부터 바이트 문자열 읽기 (deprecated in C99, C11에서 삭제)</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="http://en.cppreference.com/w/c/io/putchar">putchar</a></p></td>
<td><p><a href="http://en.cppreference.com/w/c/io/putwchar">putwchar</a></p></td>
<td><p>표준 출력으로 바이트/ 입력</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="http://en.cppreference.com/w/c/io/puts">puts</a></p></td>
<td></td>
<td><p>표준 출력으로 바이트 문자열 입력</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="http://en.cppreference.com/w/c/io/ungetc">ungetc</a></p></td>
<td><p><a href="http://en.cppreference.com/w/c/io/ungetwc">ungetwc</a></p></td>
<td><p>파일 스트림에 바이트/ 제자리에 돌려놓기</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>포맷 입출력</p></td>
<td><p><a href="http://en.cppreference.com/w/c/io/scanf">scanf</a><br />
<a href="http://en.cppreference.com/w/c/io/fscanf">fscanf</a><br />
<a href="http://en.cppreference.com/w/c/io/sscanf">sscanf</a></p></td>
<td><p><a href="http://en.cppreference.com/w/c/io/wscanf">wscanf</a><br />
<a href="http://en.cppreference.com/w/c/io/fwscanf">fwscanf</a><br />
<a href="http://en.cppreference.com/w/c/io/swscanf">swscanf</a></p></td>
<td><p>파일 스트림이나 버퍼의 표준 입력으로 부터 형식화된 바이트/ 입력 읽기</p></td>
</tr>
<tr class="even">
<td><p><a href="http://en.cppreference.com/w/c/io/vscanf">vscanf</a><br />
<a href="http://en.cppreference.com/w/c/io/vfscanf">vfscanf</a><br />
<a href="http://en.cppreference.com/w/c/io/vsscanf">vsscanf</a></p></td>
<td><p><a href="http://en.cppreference.com/w/c/io/vwscanf">vwscanf</a><br />
<a href="http://en.cppreference.com/w/c/io/vfwscanf">vfwscanf</a><br />
<a href="http://en.cppreference.com/w/c/io/vswscanf">vswscanf</a></p></td>
<td><p>가변 인자 목록을 쓰는 파일 스트림이나 버퍼의 표준 입력으로 부터 형식화된 입력 바이트/ 읽기</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="http://en.cppreference.com/w/c/io/printf">printf</a><br />
<a href="http://en.cppreference.com/w/c/io/fprintf">fprintf</a><br />
<a href="http://en.cppreference.com/w/c/io/sprintf">sprintf</a><br />
<a href="http://en.cppreference.com/w/c/io/snprintf">snprintf</a></p></td>
<td><p><a href="http://en.cppreference.com/w/c/io/wprintf">wprintf</a><br />
<a href="http://en.cppreference.com/w/c/io/fwprintf">fwprintf</a><br />
<a href="http://en.cppreference.com/w/c/io/swprintf">swprintf</a></p></td>
<td><p>파일 스트림이나 버퍼의 표준 출력으로 형식화된 바이트/ 출력을 출력하기</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="http://en.cppreference.com/w/c/io/vprintf">vprintf</a><br />
<a href="http://en.cppreference.com/w/c/io/vfprintf">vfprintf</a><br />
<a href="http://en.cppreference.com/w/c/io/vsprintf">vsprintf</a><br />
<a href="http://en.cppreference.com/w/c/io/vsnprintf">vsnprintf</a></p></td>
<td><p><a href="http://en.cppreference.com/w/c/io/vwprintf">vwprintf</a><br />
<a href="http://en.cppreference.com/w/c/io/vfwprintf">vfwprintf</a><br />
<a href="http://en.cppreference.com/w/c/io/vswprintf">vswprintf</a></p></td>
<td><p>가변 인자 목록을 쓰는 파일 스트림이나 버퍼의 표준 출력으로 형식화된 바이트/ 출력을 출력</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="http://en.cppreference.com/w/c/io/perror">perror</a></p></td>
<td></td>
<td><p>표준 에러에 <a href="https://ko.wikipedia.org/wiki/errno.h" title="wikilink">현재 에러</a> 설명 쓰기</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>파일 위치 조정</p></td>
<td><p><a href="http://en.cppreference.com/w/c/io/ftell">ftell</a><br />
ftello</p></td>
<td><p>현재 파일 포인터 되돌려주기</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="http://en.cppreference.com/w/c/io/fseek">fseek</a><br />
fseeko</p></td>
<td><p>파일의 특정 위치로 파일 포인터 이동</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="http://en.cppreference.com/w/c/io/fgetpos">fgetpos</a></p></td>
<td><p>파일 포인터 얻기</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="http://en.cppreference.com/w/c/io/fsetpos">fsetpos</a></p></td>
<td><p>파일의 특정 위치로 파일 포인터 이동</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="http://en.cppreference.com/w/c/io/rewind">rewind</a></p></td>
<td><p>파일 포인터를 파일의 첫 시작 부분으로 이동</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>에러 조작</p></td>
<td><p><a href="http://en.cppreference.com/w/c/io/clearerr">clearerr</a></p></td>
<td><p>에러 삭제</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="http://en.cppreference.com/w/c/io/feof">feof</a></p></td>
<td><p>파일의 끝 체크</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="http://en.cppreference.com/w/c/io/ferror">ferror</a></p></td>
<td><p>파일 에러 체크</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>파일 조작 명령</p></td>
<td><p><a href="http://en.cppreference.com/w/c/io/remove">remove</a></p></td>
<td><p>파일 삭제</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="http://en.cppreference.com/w/c/io/rename">rename</a></p></td>
<td><p>파일 이름 <a href="https://ko.wikipedia.org/wiki/수정_(컴퓨터)" title="wikilink">수정</a></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="http://en.cppreference.com/w/c/io/tmpfile">tmpfile</a></p></td>
<td><p>임시 파일로 포인터 되돌리기</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="http://en.cppreference.com/w/c/io/tmpnam">tmpnam</a></p></td>
<td><p>특수 파일 이름 되돌려주기</p></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

### 상수

헤더에 파일 입출력과 관련해 다음과 같은 상수들이 정의되어 있다.

<table>
<thead>
<tr class="header">
<th><p>이름</p></th>
<th><p>설명</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/End-of-file" title="wikilink">EOF</a></p></td>
<td><p>파일의 끝의 상태를 나타내는  타입의 음수의 정수</p></td>
</tr>
<tr class="even">
<td><p><a href="http://c-p-p.net/c/stdio.h/bufsiz">BUFSIZ</a></p></td>
<td><p>함수에 의해 사용되는 버퍼의 크기를 나타내는 정수</p></td>
</tr>
<tr class="odd">
<td><p>FILENAME_MAX</p></td>
<td><p>열릴 수 있는 모든 파일의 이름을 충분히 저장할 수 있을 정도로 큰  배열의 크기</p></td>
</tr>
<tr class="even">
<td><p>FOPEN_MAX</p></td>
<td><p>동시에 열려있는 파일들의 개수를 나타내며 최소 8로 표시됨</p></td>
</tr>
<tr class="odd">
<td><p>_IOFBF</p></td>
<td><p>"input/output fully buffered"의 축약어. 열린 스트림에 블록 버퍼링된 입출력을 요청하는  함수에 전달되는 정수</p></td>
</tr>
<tr class="even">
<td><p>_IOLBF</p></td>
<td><p>"input/output line buffered"의 축약어; 열린 스트림에 라인 버퍼링된 입출력을 요청하는  함수에 전달되는 정수</p></td>
</tr>
<tr class="odd">
<td><p>_IONBF</p></td>
<td><p>"input/output not buffered"의 축약어; 열린 스트림에 대해 버퍼링되지 않은 입출력을 요청하기 위한  함수에 전달되는 정수</p></td>
</tr>
<tr class="even">
<td><p>L_tmpnam</p></td>
<td><p>함수에 의해 생성된 임시 파일 이름을 저장할 수 있을 정도의 크기를 가진  배열의 크기</p></td>
</tr>
<tr class="odd">
<td><p>NULL</p></td>
<td><p><a href="../Page/널_포인터.md" title="wikilink">널 포인터</a> 상수에 확장하는 매크로. 메모리 안의 객체의 유효한 주소가 아니도록 한 포인터 값을 나타낸 상수</p></td>
</tr>
<tr class="even">
<td><p>SEEK_CUR</p></td>
<td><p>현재 파일 위치에 대해 위치 변경을 요청하는 에 전달되는 정수</p></td>
</tr>
<tr class="odd">
<td><p>SEEK_END</p></td>
<td><p>파일의 끝에 대해 위치 조정을 요청하기 위한  함수에 전달되는 정수.</p></td>
</tr>
<tr class="even">
<td><p>SEEK_SET</p></td>
<td><p>파일의 시작 위치를 기준으로 한 위치 지정을 요청하기 위한  함수에 전달되는 정수.</p></td>
</tr>
<tr class="odd">
<td><p>TMP_MAX</p></td>
<td><p>기능에 의해 만들어 지는 특수 파일이름의 최대 길이. (최소 25자)</p></td>
</tr>
</tbody>
</table>

### 변수

헤더에 포함된 변수들로 다음과 같이 정의된 것들이 있다.

| 이름                                                                         | 설명                                             |
| -------------------------------------------------------------------------- | ---------------------------------------------- |
| [stdin](https://ko.wikipedia.org/wiki/표준_스트림#표준_입력_\(stdin\) "wikilink")   | 표준 입력 스트림으로 나타나는 파일에 대한 포인터. 키보드로 주로 쓰임.       |
| [stdout](https://ko.wikipedia.org/wiki/표준_스트림#표준_출력_\(stdout\) "wikilink") | 표준 출력 스트림으로 나타나는 파일에 대한 포인터. 디스플레이 터미널로 주로 쓰임. |
| [stderr](https://ko.wikipedia.org/wiki/표준_스트림#표준_에러_\(stderr\) "wikilink") | 표준 에러 스트림으로 나타나는 파일에 대한 포인터. 디스플레이 터미널로 쓰임.    |

### 맴버 타입

헤더에 정의된 데이터 타입으로 다음과 같은 것들이 있다.

  - – 파일 [핸들이라고도](../Page/핸들_\(컴퓨팅\).md "wikilink") 한다. 다음과 같은 입출력 명령을 수행을 필요로 하는 파일이나 텍스트 스트림에 관한 정보를 담은 [오파크 타입이다](https://ko.wikipedia.org/wiki/오파크_포인터 "wikilink").

      - [파일 식별자와](https://ko.wikipedia.org/wiki/파일_식별자 "wikilink") 같은 입출력 장치와 연관련 플랫폼 특수 식별자.
      - 버퍼
      - 스트림 지향 식별자 (unset, 좁은, 혹은 넓게)
      - 상태 식별자를 버퍼링하는 스트림 (버퍼링되지 않음, 라인 버퍼링, 완전 버퍼림)
      - I/O 모드 식별자 (입력 스트림, 출력 스트림, 업데이트 스트림)
      - 바이너리/텍스트 모드 식별자
      - 파일의 끝 식별자
      - 에러 식별자
      - 현재 스트림 위치 및 멀티바이트 전환 상태 (fpos_t 타입의 객체)
      - 재귀 잠금 ([C11](https://ko.wikipedia.org/wiki/C11_\(C_표준_개정\) "wikilink") 요구함)

  - – 특별히 식별된 파일의 모든 바이트의 위치와 모든 지원되는 멀티바이트 문자 인코딩에 일어날 수 있는 모든 전환 상태를 담은 비배열 타입.

파일에서 모든 바이트의 위치를 고유하게 식별할 수 있는 비라이언트 유형, 모든 지원되는 멀티 부팅 문자 인코딩에서 발생할 수 있는 모든 변환 상태

  - –  오퍼레이터의 결과를 나타낸 [unsigned 정수](https://ko.wikipedia.org/wiki/signed와_unsigned "wikilink").

### 확장

[POSIX](https://ko.wikipedia.org/wiki/POSIX "wikilink") 표준은 메모리를 할당하는  함수와,  객체와 [파일 식별자간](https://ko.wikipedia.org/wiki/파일_식별자 "wikilink") 링크를 만드는 ,  함수와, 메모리 내 버퍼를 가리키는  객체를 생성하는 함수 그룹 등  기능들로 구성된 몇가지 확장 기능을 정의한다.\[4\]

## 예시

아래 C 프로그램은 'myfile'이라는 바이너리 파일을 열고 파일 안의 다섯 바이트를 읽고 파일을 닫는 과정을 거친다.

``` c
#include <stdio.h>
#include <stdlib.h>

int main(void)
{
    char buffer[5] = {0};  /* 초기화 */
    int i;
    FILE *fp = fopen("myfile", "rb");

    if (fp == NULL) {
        perror("파일 열기 실패. \"myfile\"");
        return EXIT_FAILURE;
    }

    for (i = 0; i < 5; i++) {
        int rc = getc(fp);
        if (rc == EOF) {
            fputs("읽는 도중 에러 발생.\n", stderr);
            return EXIT_FAILURE;
        }
        buffer[i] = rc;
    }

    fclose(fp);

    printf("파일에는 다음과 같은 글자들이 있습니다. %x %x %x %x %x\n", buffer[0], buffer[1], buffer[2], buffer[3], buffer[4]);

    return EXIT_SUCCESS;
}
```

## 각주

[분류:C 표준 라이브러리](https://ko.wikipedia.org/wiki/분류:C_표준_라이브러리 "wikilink") [분류:입출력](https://ko.wikipedia.org/wiki/분류:입출력 "wikilink")

1.
2.
3.
4.