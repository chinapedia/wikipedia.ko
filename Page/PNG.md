> This article is converted from Wikipedia: [PNG](https://ko.wikipedia.org/wiki/PNG).


**포터블 네트워크 그래픽스**(Portable Network Graphics; PNG, \[1\]\[2\])는 [비손실](https://ko.wikipedia.org/wiki/비손실_압축 "wikilink") [그래픽 파일 포맷의](https://ko.wikipedia.org/wiki/그래픽_파일_포맷 "wikilink") 하나이다. [특허](../Page/특허.md "wikilink") 문제가 얽힌 [GIF](https://ko.wikipedia.org/wiki/GIF "wikilink") 포맷의 문제를 해결하고 개선하기 위해서 고안되었다. PNG는 공식적으로는 "핑"()이라고 읽지만, 대부분은 "피엔지"라고 영어 철자 그대로 읽는다.

PNG 포맷은 [컬러 팔레트](../Page/팔레트_\(컴퓨팅\).md "wikilink") 화상과 [그레이스케일](https://ko.wikipedia.org/wiki/그레이스케일 "wikilink") 화상, 그리고 풀 컬러 화상 방식을 모두 지원한다. 그러나 [인터넷](../Page/인터넷.md "wikilink") 상의 이미지 표시를 염두에 두고 개발되었기 때문에 [CMYK](https://ko.wikipedia.org/wiki/CMYK "wikilink") 등의 [색 공간은](../Page/색_공간.md "wikilink") 지원하지 않는다.

파일 확장자는 `PNG` 또는 `png`를 쓰며, MIME 타입은 `image/png`으로 적는다.

## 역사

PNG 포맷을 만들게 된 배경은 [1995년](../Page/1995년.md "wikilink"), [유니시스](../Page/유니시스.md "wikilink") 사가 [GIF](https://ko.wikipedia.org/wiki/GIF "wikilink")에 사용되는 [LZW](../Page/LZW.md "wikilink") [데이터 압축](https://ko.wikipedia.org/wiki/데이터_압축 "wikilink") 알고리즘에 대해 [소프트웨어 특허를](https://ko.wikipedia.org/wiki/소프트웨어_특허 "wikilink") 적용할 것이라고 공고하면서이다. 이 알고리즘은 미국 특허 4,558,302번으로 등록되어 있고, 다른 여러 나라에도 등록되어 있다. 또한 256 색만을 저장할 수 있는 GIF는 한계가 있으므로 컴퓨터 성능이 좋아지면서 문제가 되어 왔다. [1999년](../Page/1999년.md "wikilink") 8월, 유니시스가 [자유 소프트웨어](../Page/자유_소프트웨어.md "wikilink")(프리웨어)와 비상업 소프트웨어(Non-Commercial License Software, FMOD)에 대한 무료 특허 정책을 거둬들이면서 PNG는 인기를 끌기 시작했다.

  - 버전 1.0: [1996년](../Page/1996년.md "wikilink") [7월 1일](../Page/7월_1일.md "wikilink") 발표되었고, [W3C](../Page/W3C.md "wikilink")에서도 [1996년](../Page/1996년.md "wikilink") [10월 1일](../Page/10월_1일.md "wikilink") 표준으로 지정했다.
  - 버전 1.1: [1998년](../Page/1998년.md "wikilink") [12월 31일](../Page/12월_31일.md "wikilink")
  - 버전 1.2: [1999년](../Page/1999년.md "wikilink") [8월 11일](../Page/8월_11일.md "wikilink")
  - PNG는 국제 표준([ISO](https://ko.wikipedia.org/wiki/국제표준화기구 "wikilink")/IEC 15948:2003)과 W3C 표준으로 [2003년](../Page/2003년.md "wikilink") [11월 10일](../Page/11월_10일.md "wikilink") 발표되었다. 이 버전은 1.2판과 약간의 차이만이 있다.

## 기술 개요

### 파일 헤더

PNG 파일은 8바이트의 신호로 시작한다.\[3\]

| 값          | 의미                                                                                                                                                             |
| ---------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `89`       | 통신 등에서 8비트 데이터를 지원하지 않는 시스템을 찾거나 텍스트 파일과의 구분을 위해 사용된다.                                                                                                         |
| `50 4E 47` | [ASCII](https://ko.wikipedia.org/wiki/ASCII "wikilink")로 *PNG*라는 글자로, 텍스트 에디터 등에서 쉽게 구분하기 위해 쓰인다.                                                              |
| `0D 0A`    | [DOS](https://ko.wikipedia.org/wiki/DOS "wikilink")-style의 줄바꿈(CRLF)으로, DOS-Unix 변환에서 데이터 줄바꿈을 위해 쓰인다.                                                         |
| `1A`       | DOS에서 [TYPE](https://ko.wikipedia.org/wiki/TYPE "wikilink") 명령이 쓰였을 때 출력을 멈추기 위해 사용된다. [end-of-file](https://ko.wikipedia.org/wiki/end-of-file "wikilink") 문자. |
| `0A`       | Unix-style 줄바꿈으로, (LF) Unix-DOS 변환에서 줄바꿈에 사용한다.                                                                                                                |

### 파일의 청크

헤더 뒤에는 이미지에 대한 정보를 담고 있는 일련의 청크(chunk)가 온다. 청크는 그 자신을 *중요* 또는 *보조*로 선언한다. 프로그램이 받아들이지 못하는 *보조* 청크는 그냥 무시된다. 이런 식으로 청크를 통한 계층 구조는 [디지털 컨테이너 포맷과](../Page/디지털_컨테이너_포맷.md "wikilink") 같은 개념으로, PNG 포맷이 구버전과 호환되면서 쉽게 확장할 수 있도록 해준다. 이와 같은 구조가 MNG, JNG, APNG 포맷에도 사용된다. 청크는 네 가지 부분으로 구성된다. 길이(4바이트), 청크 타입(또는 이름)(4바이트), 청크 데이터(길이 바이트), 그리고 [순환 중복 검사](https://ko.wikipedia.org/wiki/CRC "wikilink")(순환 중복검사/체크섬, 4바이트). CRC는 길이를 제외한 청크 타입과 데이터로 생성된 network-byte-order CRC-32이다.

| 길이    | 청크 타입 | 청크 데이터     | CRC   |
| ----- | ----- | ---------- | ----- |
| 4 바이트 | 4 바이트 | *길이* bytes | 4 바이트 |

청크 타입은 ASCII 문자 네개로 구성된다. 대소문자는 구분된다. 이들의 대소문자 여부가 [디코더](https://ko.wikipedia.org/wiki/디코더 "wikilink")에게 청크를 인식해야 할지에 대한 정보를 준다. 첫번째 문자는 이 청크가 *중요*인지 *보조*인지 알려준다. 대문자일 경우 *중요*이고, 그렇지 않을 경우 *보조*이다. 중요 청크는 파일을 읽는데 필수적인 정보를 갖고 있다. 디코더가 해석할 수 없는 중요 청크를 받으면 파일 읽기를 중단하고 사용자에게 경고를 전달해야 한다. 두번째 문자는 청크가 "퍼블릭"(PNG파일 표준에 포함되어 있거나 특수목적 퍼블릭 청크의 레지스트리에 포함되어 있음)인지 "프라이빗"(표준이 아님)인지 판별한다. 대문자는 퍼블릭이고 소문자는 프라이빗이다. 이는 프라이빗과 퍼블릭 청크의 이름이 충돌하는 것을 막아준다.(단, 같은 이름의 프라이빗 청크는 충돌할 수 있다) 세번째 문자는 PNG 표준에 따라 대문자여야 한다. 미래의 확장을 위해 남겨둔 문자로, 디코더는 이 문자가 소문자일 경우 해석 못하는 것으로 처리해야 한다. 네번째 문자는 청크를 해석하지 못할 경우 복사가 안전한지 판별한다. 소문자일 경우 파일에 변경이 있어도 안전하게 복사될 수 있다. 대문자일 경우, 파일 변경이 중요 청크를 변경하지 않았을 경우에만 복사될 수 있다.

### 중요 청크

디코더는 PNG 파일을 읽고 렌더링하기 위해서 중요 청크를 해석할 수 있어야 한다.

  - `IHDR`는 첫번째 청크로 와야 한다. 이것은 순서대로 이미지의 ㄴ이,높이, 비트 수와 컬러 타입을 표시한다.\[4\]
  - `PLTE`는 [팔레트 (컴퓨팅)](../Page/팔레트_\(컴퓨팅\).md "wikilink"), 즉 색공간을 표시한다.
  - `IDAT`는 여러 개의 IDAT 청크로 쪼개질 수 있는 이미지를 표시한다. 파일 사이즈가 약간 커지긴 하지만 PNG를 스트리밍 방식으로 전달할 수 있게 만든다. IDAT는 압축 알고리즘의 출력 스트림을 통한 실제 이미지 파일을 갖고 있다.\[5\]
  - `IEND`는 이미지의 끝을 표시한다.

`PLTE`는 컬러 타입 3(인덱스드 컬러, 설정된 색만을 표시한다)에는 필수적이다. 컬러 타입 2와 6(트루 컬러와 트루컬러 + 알파 채널)에는 선택사항이다 그리고 컬러 타입 0와 4(그레이스케일과 그레이스케일 + 알파 채널)에는 나타내서는 안된다.

## GIF와의 비교

  - 대부분의 경우 PNG는 [GIF](https://ko.wikipedia.org/wiki/GIF "wikilink")보다 압축률이 더 높다.
  - GIF의 단색 투명층과 달리 PNG는 8비트 알파 채널을 이용한 다양한 투명층을 지원한다.
  - 256색까지 지원하는 GIF와 달리 PNG는 [트루 컬러를](https://ko.wikipedia.org/wiki/트루_컬러 "wikilink") 지원한다.
  - GIF에서는 제공되는 애니메이션을 PNG는 지원하지 않는다. (대안으로 PNG에 기반한 [APNG](https://ko.wikipedia.org/wiki/APNG "wikilink"), [JNG](https://ko.wikipedia.org/wiki/JNG "wikilink"), [MNG](https://ko.wikipedia.org/wiki/MNG "wikilink")와 같은 파일 형식이 제안되었다.)

### 파일 크기

PNG가 GIF보다 최신의 압축 알고리즘을 사용하지만, GIF보다 더 큰 파일을 만든다고 알고 있는 사람이 있다. 여기에는 몇 가지 까닭이 있는데,

  - GIF는 256색만을 지원한다. 트루 컬러 그림을 PNG로 압축할 때는 원본의 색을 다 저장하는 반면, GIF로 저장할 때는 256 색으로 수를 줄인 다음에 저장한다. 만약 원본도 256색만을 사용한다면 이런 차이는 나오지 않는다.
  - PNG 파일 형식에는 [메타데이터](../Page/메타데이터.md "wikilink")가 추가로 붙어 있는 경우가 있다. (어도비 사의 파이어웍스 등).
  - 어도비 포토샵의 일부 옛 버전에서는 PNG 압축 알고리즘을 잘 구현해 내지 못해서 큰 파일을 만들곤 했다.

PNG 파일의 크기를 줄이는 [OptiPNG](http://optipng.sourceforge.net/)나 [pngcrush](https://web.archive.org/web/20040723144359/http://pmt.sourceforge.net/pngcrush/)와 같은 [오픈 소스로](../Page/오픈_소스.md "wikilink") [MS-DOS](https://ko.wikipedia.org/wiki/MS-DOS "wikilink")에서 [유닉스](../Page/유닉스.md "wikilink")나 [리눅스](../Page/리눅스.md "wikilink") 등의 다양한 환경을 지원하여 제공하고 있다.

## JPEG와의 비교

[섬네일](https://ko.wikipedia.org/wiki/파일:Comparison_of_JPEG_and_PNG.png "wikilink") 사진과 같은 이미지에 대해서는, [JPEG](../Page/JPEG.md "wikilink")가 사진에 특화된 [손실 압축](../Page/손실_압축.md "wikilink") 알고리즘을 사용하므로 PNG에 비해 더 작은 파일을 만들 수 있다.  하지만 JPEG 압축은 양자화의 영향으로, 바라지 않던 잡티가 낄 수 있다. 문자나 날카로운 경계가 있는 그림은, JPEG에서 생기기 쉬운 뭉개짐 없이 JPEG보다 압축을 더 잘 할 수 있는 PNG를 쓰는 것이 더 낫다.

또한, PNG는 비손실 압축이므로, 나중에 고화질의 재편집을 해야 한다면 PNG로 저장해 놓는 것이 낫다. JPEG를 사용할 때는 저장을 하면 할수록 계속 손실이 누적될 수 있다.

## 같이 보기

  - [APNG](https://ko.wikipedia.org/wiki/APNG "wikilink")

## 각주

## 외부 링크

  - [PNG 홈페이지](http://www.libpng.org/pub/png/)
  - [libpng 홈페이지](http://www.libpng.org/pub/png/libpng.html)
  - [PNG를 지원하는 브라우저](http://www.libpng.org/pub/png/pngapbr.html) - 여러 [웹 브라우저들의](../Page/웹_브라우저.md "wikilink") PNG 지원 현황. 윈도 IE 4.0b1, 넷스케이프 4.04부터 PNG를 지원한다.

[분류:그래픽 파일 포맷](https://ko.wikipedia.org/wiki/분류:그래픽_파일_포맷 "wikilink") [분류:ISO 표준](https://ko.wikipedia.org/wiki/분류:ISO_표준 "wikilink") [분류:W3C 표준](https://ko.wikipedia.org/wiki/분류:W3C_표준 "wikilink") [분류:오픈 포맷](https://ko.wikipedia.org/wiki/분류:오픈_포맷 "wikilink") [분류:화상 압축](https://ko.wikipedia.org/wiki/분류:화상_압축 "wikilink")

1.
2.
3.
4.
5.