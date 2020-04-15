> This article is converted from Wikipedia: [Copy \(명령어\)](https://ko.wikipedia.org/wiki/Copy_\(명령어\)).


[컴퓨팅](../Page/컴퓨팅.md "wikilink")에서 **`copy`**는 [RT-11](https://ko.wikipedia.org/wiki/RT-11 "wikilink"), [RSX-11](https://ko.wikipedia.org/wiki/RSX-11 "wikilink"), [TOPS-20](https://ko.wikipedia.org/wiki/TOPS-20 "wikilink")\[1\], [오픈VMS](https://ko.wikipedia.org/wiki/오픈VMS "wikilink"), [DOS](https://ko.wikipedia.org/wiki/DOS "wikilink"), [OS/2](https://ko.wikipedia.org/wiki/OS/2 "wikilink"), [마이크로소프트 윈도우](../Page/마이크로소프트_윈도우.md "wikilink") [운영 체제의](../Page/운영_체제.md "wikilink") 명령어이다. 이 명령은 한 [디렉터리](https://ko.wikipedia.org/wiki/디렉터리 "wikilink")에서 다른 곳으로 [컴퓨터 파일을 복사한다](https://ko.wikipedia.org/wiki/파일_복사 "wikilink").\[2\]\[3\] 기본 목적지는 현재 [작업 디렉터리이다](https://ko.wikipedia.org/wiki/작업_디렉터리 "wikilink"). 하나 이상의 원본 파일이 지정될 경우 목적지는 반드시 디렉터리여야 한다. 이와 동일한 [유닉스](../Page/유닉스.md "wikilink") 명령어는 [`cp`](../Page/Cp_\(유닉스\).md "wikilink")이다. 더 진보화된 복사 명령어의 이름은 [`xcopy`](https://ko.wikipedia.org/wiki/xcopy "wikilink")이다. 이 명령어는 [OpenVOS의](https://ko.wikipedia.org/wiki/Stratus_VOS "wikilink") `copy_file` 명령어와 유사하다.\[4\]

## 도스용의 예시

`copy `*`letter.txt`*` [`*`목적지`*`]`

파일은 [장치 파일로](../Page/장치_파일.md "wikilink") 복사할 수 있다. (예를 들어 `copy letter.txt lpt1`는 파일을 lpt1의 [프린터로](https://ko.wikipedia.org/wiki/컴퓨터_프린터 "wikilink") 보낸다. `copy letter.txt con`는 [`type`](../Page/TYPE_\(도스_명령어\).md "wikilink")과 같이 [stdout](https://ko.wikipedia.org/wiki/stdout "wikilink")으로 출력을 보낸다. `copy page1.txt+page2.txt book.txt`는 파일의 뒤에 내용을 [연결시키고](../Page/문자열_연결.md "wikilink") 이를 `book.txt`로 출력한다. 마치 [`cat`](https://ko.wikipedia.org/wiki/cat_\(유닉스\) "wikilink") 명령어가 하는 바와 비슷하다).

다른 디스크 드라이브 간에 파일을 복사할 수도 있다.

파일 연결 시 동작을 수정하기 위한 2개의 [명령 줄 스위치가](../Page/명령_줄_인터페이스.md "wikilink") 있다:

  - 텍스트 모드 - 파일의 텍스트 내용을 복사하고 [EOF](https://ko.wikipedia.org/wiki/파일_끝 "wikilink") 문자가 오면 중단한다.

`copy /a doc1.txt + doc2.txt doc3.txt`

  - 바이너리 모드 - 파일을 완전히 연결하되 EOF 문자를 무시한다.

`copy /b image1.jpg + image2.jpg image3.jpg`

## 같이 보기

  - [XCOPY](https://ko.wikipedia.org/wiki/XCOPY "wikilink"): 도스, OS/2, 윈도우 등.
  - [cp (유닉스)](https://ko.wikipedia.org/wiki/cp_\(유닉스\) "wikilink")

## 각주

[분류:내부 도스 명령어](https://ko.wikipedia.org/wiki/분류:내부_도스_명령어 "wikilink") [분류:OS/2 명령어](https://ko.wikipedia.org/wiki/분류:OS/2_명령어 "wikilink") [분류:윈도우 명령어](https://ko.wikipedia.org/wiki/분류:윈도우_명령어 "wikilink") [분류:마이크로컴퓨터 소프트웨어](https://ko.wikipedia.org/wiki/분류:마이크로컴퓨터_소프트웨어 "wikilink") [분류:윈도우 관리](https://ko.wikipedia.org/wiki/분류:윈도우_관리 "wikilink") [분류:파일 복사 유틸리티](https://ko.wikipedia.org/wiki/분류:파일_복사_유틸리티 "wikilink")

1.
2.  [Microsoft TechNet Copy article](https://technet.microsoft.com/en-us/library/bb490886.aspx)
3.  <https://archive.org/details/1988-rugheimer-spanik-amigados-quick-reference>
4.  <http://stratadoc.stratus.com/vos/19.1.0/r098-19/wwhelp/wwhimpl/common/html/r098-19.pdf>