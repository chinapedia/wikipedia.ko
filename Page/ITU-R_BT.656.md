> This article is converted from Wikipedia: [ITU-R BT.656](https://ko.wikipedia.org/wiki/ITU-R_BT.656).


**ITU-R BT.656**(ITU-R Recommendation BT.656) 또는 **ITU 656** 표준은 [압축되지](../Page/데이터_압축.md "wikilink") 않은 [PAL](https://ko.wikipedia.org/wiki/PAL "wikilink") 또는 [NTSC](../Page/NTSC.md "wikilink") [표준 화질 텔레비전을](https://ko.wikipedia.org/wiki/SDTV "wikilink") [스트리밍](../Page/스트리밍.md "wikilink")하기 위한 단순한 디지털 영상 [프로토콜을](../Page/통신_프로토콜.md "wikilink") 정의한다. 이 프로토콜은 [비월 주사된](https://ko.wikipedia.org/wiki/비월_주사_방식 "wikilink") 영상 데이터를 지원하며, 각 [필드](https://ko.wikipedia.org/wiki/필드 "wikilink")는 따로따로 스트리밍된다. ITU 656 프로토콜은 [TV-out](https://ko.wikipedia.org/wiki/TV-out "wikilink")용의 [DAC](../Page/디지털-아날로그_변환회로.md "wikilink") 칩으로 [비디오 프레임을](https://ko.wikipedia.org/wiki/비디오_프레임 "wikilink") 보내는 데 사용되거나 비디오 캡처용 [ADC](../Page/아날로그-디지털_변환회로.md "wikilink") 의 출력으로 사용될 수 있다.

## BT.656 데이터 스트림 형식

하나의 BT.656 스트림은 27 [MHz](https://ko.wikipedia.org/wiki/MHz "wikilink") 로 동작하는 [픽셀 클럭](https://ko.wikipedia.org/wiki/픽셀_클럭 "wikilink") 신호에 따라 동시에 8 비트를 병렬로 전송한다. 스트림 내의 비디오 [픽셀](https://ko.wikipedia.org/wiki/픽셀 "wikilink") 데이터의 수평 주사선은 SAV (Start of Active Video) 코드와 EAV (End of Active Video) 코드로 구분된다. 또한 SAV 코드는 비디오 필드 혹은 프레임 내의 라인 위치를 가리키는 상태 비트를 포함한다. 전체 프레임 내의 라인 정보는 SAV 상태 비트를 추적함으로써 알 수 있으며, 수신기가 새로운 스트림과 [동기화](../Page/동기화.md "wikilink")(synchronize)되도록 한다.

## 색 공간 (Color space)

라인 내의 각각의 픽셀은 [YUV](https://ko.wikipedia.org/wiki/YUV "wikilink") 형식으로 [부호화](https://ko.wikipedia.org/wiki/부호화 "wikilink") 된다. 4 바이트 길이의 SAV 코드가 전송된 후에 Y ([휘도](https://ko.wikipedia.org/wiki/휘도 "wikilink")) 신호의 초기 8 비트가 전송되고 그 다음에는 Cb ([색차](https://ko.wikipedia.org/wiki/색차 "wikilink") U) 신호의 8 비트가 전송되며 그 다음에는 Y 신호의 다음 8 비트, 그 다음에는 Cr (색차 V) 신호의 8 비트가 전송된다. 온전한 Y, Cb, Cr 픽셀 값을 복원하기 위해서는 반드시 [크로마 서브샘플링이](../Page/크로마_서브샘플링.md "wikilink") 필요하다.

## 외부 링크

  - [ITU-R Recommendation BT.656](http://www.itu.int/rec/R-REC-BT.656/en): Interfaces for digital component video signals in 525-line and 625-line television systems operating at the 4:2:2 level of Recommendation ITU-R BT.601 (Part A).

[분류:국제 전기 통신 연합](https://ko.wikipedia.org/wiki/분류:국제_전기_통신_연합 "wikilink") [분류:ITU-R 권고](https://ko.wikipedia.org/wiki/분류:ITU-R_권고 "wikilink")