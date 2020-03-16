> This article is converted from Wikipedia: [A.out](https://ko.wikipedia.org/wiki/A.out).


**a.out**은 과거 [유닉스 계통](https://ko.wikipedia.org/wiki/유닉스_계통 "wikilink") [운영 체제에서](../Page/운영_체제.md "wikilink") 사용하던 [실행 파일과](../Page/실행_파일.md "wikilink") [목적 파일](../Page/목적_파일.md "wikilink") 형식이다. 이후에는 [공유 라이브러리](https://ko.wikipedia.org/wiki/공유_라이브러리 "wikilink") 형식으로도 사용되었다. a.out이라는 이름은 [어셈블러](https://ko.wikipedia.org/wiki/어셈블러 "wikilink") 출력(assembler output)을 줄인 말이다.

a.out을 사용하던 대부분의 운영 체제는 이후 [ELF](https://ko.wikipedia.org/wiki/실행_및_링크_가능_포맷 "wikilink") 형식으로 대체하였다. 현재 a.out라는 명칭은 몇몇 [컴파일러](../Page/컴파일러.md "wikilink")나 [링커에서](../Page/링커_\(컴퓨팅\).md "wikilink") 출력 파일명 기본값으로 사용되는 것에서 흔적을 찾을 수 있다.

## 역사

UNIX 첫 번째 버전은 [PDP-7](https://ko.wikipedia.org/wiki/PDP-7 "wikilink")에서 사용되었고, 이때 a.out의 초기 형식이 등장했다. 이후 [PDP-11](../Page/PDP-11.md "wikilink")에서 형식이 약간 개선되었다.

이후 AT\&T [유닉스 시스템 V에서는](https://ko.wikipedia.org/wiki/유닉스_시스템_V "wikilink") [COFF](https://ko.wikipedia.org/wiki/COFF "wikilink") 형식으로 대체되었고, [릴리즈 4에서](https://ko.wikipedia.org/wiki/유닉스_시스템_V "wikilink") [ELF](https://ko.wikipedia.org/wiki/실행_및_링크_가능_포맷 "wikilink") 형식으로 대체되었다.

[BSD](../Page/BSD.md "wikilink") 계열에서는 a.out 형식을 비교적 오래 사용했지만, 결과적으로 대부분의 BSD 운영체제는 ELF 형식을 사용하기 시작했다. [NetBSD](../Page/NetBSD.md "wikilink")/i386은 1.5 릴리즈에서, [FreeBSD](../Page/FreeBSD.md "wikilink")/i386은 2.2 릴리즈에서 3.0 릴리즈로 올리는 과정에서 ELF를 채택했다.

a.out 형식은 디버그에 대한 정보를 위한 직접적인 지원이 없었지만, 데이터를 저장하는 special symbol table entries에 사용되는 stabs로 지원되긴 했다.

[리눅스](../Page/리눅스.md "wikilink")는 또한 커널 버전1.2까지는 a.out을 사용했다.(ELF는 experimental 1.1.52 에 추가되었다) 리눅스가 ELF로 바꾸는데는 더도말고 플랫폼에 있는 라이브러리를 공유하는데 있어서 a.out을 만들 때 복잡한 특징 때문이었다. a.out의 플랫폼은 공유라이브러리 재배치가 불가능 할 때, 중앙 권한과 함께 라이브러리가 있는 가상주소공간을 등록해야만 했다. 리눅스가 ELF로 바꾼 이후에도 많은 BSD 사용자들은 계속해서 a.out 을 사용했다. 리눅스와 비교해서 BSD의 a.out 형식은 다소 유연성이 있었기 때문이다.

## 형식

a.out은 주로 OMAGIC, NMAGIC, QMAGIC, ZMAGIC 중 한 가지에서 실행 가능하다. QMAGIC 형식은 헤더 다음에 계속되는 세그먼트를 가지고 있으며, 텍스트와 데이터를 구분하지 않는다. NMAGIC 형식은 QMAGIC과 비슷하지만 데이터 세그먼트가 텍스트 세그먼트 바로 뒤에 로드돼 있고, 텍스트 세그먼트는 읽기 전용이다. ZMAGIC 형식은 페이지요구를 위한 기능이 추가되었다. 그리고 QMAGIC은 a.out 헤더가 텍스트 세그먼트의 첫 번째 페이지와 합쳐지도록 만들었는데, 이것은 주로 메모리를 절약하게 했다. QMAGIC 바이너리는 주로 가상주소공간의 아랫 부분 위쪽에 한 개의 페이지에 로드되었는데, 이것은 세그먼트 폴트의 경우 널포인터의 trap을 위한 것이다.

a.out 파일은 7개의 구역으로 나뉘어 있다.

  - exec 헤더
    이 구역은 메모리에 바이너리 파일을 로드하거나 실행하기 위해서, 커널에 의해서 사용되는 파라메터들을 포함하고 있다. 이 구역은 필수적인 구역이다.

<!-- end list -->

  - text 세그먼트
    이 구역은 프로그램이 실행될 때 메모리에 로드된 연관된 데이터나 기계코드를 포함하고 있다. 읽기전용으로 로드된다.

<!-- end list -->

  - data 세그먼트
    이 구역은 초기화된 데이터를 포함하고 있다. 항상 쓰기 가능한 메모리에 로드된다.

<!-- end list -->

  - text 재배치
    이 구역은 바이너리 파일이 조합될 때 텍스트에 있는 포인터를 업데이트하기 위해서 링크 에디터에 의해서 사용된 기록을 포함하고 있다.

<!-- end list -->

  - data 재배치
    text 재배치 구역과 비슷하지만, data 세그먼트 포인터가 없다.

<!-- end list -->

  - symbol table
    이 구역은 링크 에디터에 의해서 바이너리 파일 사이에서 이름 지어진 변수나 함수(functions)의 주소들의 기록을 포함하고있다.

<!-- end list -->

  - string table
    이 구역은 symbol names 과 비슷한 스트링들을 포함하고 있다.

## 외부 링크

  - [a.out 형식](https://web.archive.org/web/20110103155407/http://osxfaq.com/man/5/a.out.ws)

  - [a.out 형식의 유닉스 man 페이지](https://web.archive.org/web/20110721104412/http://fuse4bsd.creo.hu/localcgi/man-cgi.cgi?a.out+5)

[분류:파일 포맷](https://ko.wikipedia.org/wiki/분류:파일_포맷 "wikilink") [분류:실행 파일 포맷](https://ko.wikipedia.org/wiki/분류:실행_파일_포맷 "wikilink") [분류:라이브러리](https://ko.wikipedia.org/wiki/분류:라이브러리 "wikilink")