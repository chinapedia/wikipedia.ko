> This article is converted from Wikipedia: [아두이노 IDE](https://ko.wikipedia.org/wiki/아두이노_IDE).


**아두이노 통합개발환경**(Arduino IDE)은 편집기, [컴파일러](../Page/컴파일러.md "wikilink"), 업로더 등이 합쳐진 소프트웨어 환경이다. '아두이노 소프트웨어'라고도 불린다. 이와 더불어 기타 개발에 필요한 각종 옵션 및 [라이브러리](https://ko.wikipedia.org/wiki/라이브러리 "wikilink") 관리를 할 수 있다. 아두이노 프로그램 실행 시, 개인용 컴퓨터와 시리얼 통신을 할 수 있는 가상 시리얼모니터를 제공한다. 보통 USB을 통해 업로드를 하므로 아두이노 보드는 USB를 UART 통신으로 바꾸는 방법이 제공되고, [MCU가](../Page/마이크로컨트롤러.md "wikilink") 실행할 때는 이 [UART](../Page/UART.md "wikilink") 통신을 이용하여 필요한 통신을 할 수 있다. 이렇게 되려면 아두이노의 MCU는 부트로더가 올라가 있어야 한다.

특히 [아두이노](../Page/아두이노.md "wikilink") 프로그램을 '스케치(Sketch)'라고 부른다.

## 아두이노 IDE 기능

  - 편집기 : UTF-8을 기반으로 하는 편집기이다.
  - 컴파일러 : ATmega의 경우, AVR-GCC을 이용하여 [컴파일](https://ko.wikipedia.org/wiki/컴파일 "wikilink") 한다.
  - 업로드 : USB-UART 변환을 하고, MCU의 부트로더가 동작하여 기계어 코드가 업로드 된다.
  - 라이브러리 관리 : 등록 된 라이브러리 목록 및 예제를 지원한다. 공개 된 아두이노 라이브러리 찾아 파일을 받아 등록하면 초기에 장착되지 않은 각종 라이브러리를 등록 사용할 수 있다. 라이브러리 관리 프로그램도 검색 기능과 등록 기능을 제공한다.
  - 시리얼모니터
  - 아두이노 스케치 문법 및 함수등 자료 레퍼런스
  - 기타 옵션

USB가 없는 아두이노 보드는 USB-시리얼 변환 모듈을 별도 구매하여 회로 스펙에 맞게 모듈연결후 연결할 수도 있다.

## 컴파일 및 코드분할

아두이노는 프로그램 단위이자 한개의 파일인 스케치(확장자 .ino)를 단일 [컴파일](https://ko.wikipedia.org/wiki/컴파일 "wikilink")하지만 스케치를 여러개로 분할한 다중 코드작성을 지원하고 있다. 이러한 스케치의 분할은 아두이노 IDE탭 기능으로 이용할수있다. 한편 비록 아두이노 IDE탭 기능으로 스케치를 분할하여 여러 파일로 나누어 작성하더라도 컴파일시에는 여전히 단일 컴파일된다.\[1\]

## 지원 OS

[MS윈도우](../Page/마이크로소프트_윈도우.md "wikilink"),[맥OS](https://ko.wikipedia.org/wiki/맥OS "wikilink"),[리눅스](../Page/리눅스.md "wikilink")를 지원한다. 한편 리눅스계열의 [우분투](../Page/우분투_\(운영_체제\).md "wikilink") 및 [페도라는](https://ko.wikipedia.org/wiki/페도라_\(운영_체제\) "wikilink") 각각 패키지 관리자를 통해 다운로드 및 설치가 간단히 가능하나 아두이노 공식 사이트를 통한 다운로드로 최신버전을 직접 설치할수도있다.\[2\]\[3\]

## 버전

주요 버전 역사

| 아두이노 버전 | 배포        | 비고 |
| ------- | --------- | -- |
| 1.0.5   | 2013.5.15 |    |
| 1.6.1   | 2015.3.10 |    |
| 1.7.10  | 2016.6.2  |    |
| 1.8.1   | 2017.1.10 |    |
| 1.8.8   | 2018.12.6 |    |

## 같이 보기

  - [아두이노 프로그래밍](../Page/아두이노_프로그래밍.md "wikilink")

## 각주

## 외부 링크

  - [공식 아두이노 블로그](https://blog.arduino.cc/2017/07/28/a-new-era-for-arduino-begins-today/)
  - [아두이노](https://www.arduino.cc/en/Guide/HomePage)

[분류:아두이노](https://ko.wikipedia.org/wiki/분류:아두이노 "wikilink")

1.  [Hard Copy Arduino -아두이노 탭 활용하기 (ino 파일 분할)](http://www.hardcopyworld.com/ngine/aduino/index.php/archives/1075)
2.  [아두이노 소프트웨어 다운로드](https://www.arduino.cc/en/Main/Software)
3.  (우분투) \> cd ./arduino-1.8.8-linux64/install.sh \> sudo ./installl.sh)