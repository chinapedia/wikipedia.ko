> This article is converted from Wikipedia: [MPEG  ](https://ko.wikipedia.org/wiki/MPEG__).


**프로그램 스트림(Program stream, PS 혹은 MPEG-PS)**이란 [멀티플렉싱](https://ko.wikipedia.org/wiki/다중화 "wikilink") [디지털 오디오](https://ko.wikipedia.org/wiki/디지털_오디오 "wikilink"), [비디오](../Page/비디오.md "wikilink") 등을 담기 위한 [컨테이너 포맷이다](https://ko.wikipedia.org/wiki/컨테이너_포맷 "wikilink"). 이 포맷은 [MPEG-1](../Page/MPEG-1.md "wikilink") 부분 1(ISO/IEC 11172-1\[1\])과 [MPEG-2](../Page/MPEG-2.md "wikilink") 부분 1 시스템(ISO/IEC standard 13818-1\[2\]/ITU-T H.222.0)에 규정되어 있다. MPEG-2 프로그램 스트림은 ISO/IEC 11172 시스템 레이어와 비슷하고 이전 버전들과 호환된다.

프로그램 스트림은 [DVD-비디오](https://ko.wikipedia.org/wiki/DVD-비디오 "wikilink") 디스크와 [HD DVD](https://ko.wikipedia.org/wiki/HD_DVD "wikilink") 비디오 디스크에 사용되지만, 몇 가지 제한과 확장 사항이 있다.\[3\]

## 코딩 구조\[4\]

프로그램 스트림은 하나 또는 그 이상의 [패킷화된 기초 스트림](https://ko.wikipedia.org/wiki/패킷화된_기초_스트림 "wikilink")(PES)을 하나의 스트림으로 결합하여 생성된다. 이 포맷은, 데이터 전송을 위해 개발된 [MPEG 트랜스포트 스트림과는](../Page/MPEG_트랜스포트_스트림.md "wikilink") 다르게, 디스크처럼 합리적이고 신뢰성 있는(데이터 손실 우려가 적은) 미디어를 위해 개발되었다. 프로그램 스트림은 가변 사이즈 레코드들을 지원하며, 방송수신을 어렵게 하는 [시작 코드를](https://ko.wikipedia.org/wiki/시작_코드 "wikilink") 최소로 사용한다. 프로그램 스트림 코딩 레이어는, 트랜스포트 스트림과는 다르게, 하나 또는 그 이상의 기초 스트림의 단 하나의 [프로그램](https://ko.wikipedia.org/wiki/프로그램 "wikilink")을 하나의 스트림으로 패키지화될 수 있도록 도와준다.

MPEG-2 프로그램 스트림은 MPEG-1 부분 2 영상, MPEG-2 부분 2 영상, MPEG-1 부분 3 오디오([MP3](https://ko.wikipedia.org/wiki/MP3 "wikilink"),[MP2](https://ko.wikipedia.org/wiki/MP2 "wikilink"),[MP1](https://ko.wikipedia.org/wiki/MP1 "wikilink")) 또는 MPEG-2 부분 3 오디오를 포함할 수 있다. 이것은 또한 프로그램 MPEG-4 부분 2 영상, MPEG-2 부분 7 음성([AAC](../Page/고급_오디오_부호화.md "wikilink"))을 포함할 수 있으나, 자주 이용되지는 않는다. MPEG-2 프로그램 스트림은 소위 '개인 스트림'의 형태로 비표준 데이터(예를 들면 [AC-3](https://ko.wikipedia.org/wiki/AC-3 "wikilink") 음성과 자막\]\])에 대해서도 지원한다.\[5\] 국제 표준 기구는 [SMPTE](../Page/SMPTE.md "wikilink")을 MPEG-2 포맷 식별자에 대한 등록 기관으로 공인하였다. 여기에서 MPEG-2 트랜스포트 스트림과 프로그램 스트림에 요약 될 수 있는 압축 포맷 목록을 발표한다.\[6\]

## 코딩 세부사항

암호화되지 않은 VOB 파일이나 다른 프로그램 스트림을 [헥사 에디터로](https://ko.wikipedia.org/wiki/헥사_에디터 "wikilink") 열면, 다음과 같은 구조를 볼 수 있다.

| 이름                                                        | [비트](../Page/비트_\(단위\).md "wikilink") 수 | 설명                                                                  |
| --------------------------------------------------------- | --------------------------------------- | ------------------------------------------------------------------- |
| [싱크 바이트](https://ko.wikipedia.org/wiki/싱크_바이트 "wikilink") | 32                                      | 0x000001BA                                                          |
| 표시 비트                                                     | 2                                       | 01[b](../Page/이진법.md "wikilink")                                    |
| 시스템 클럭 \[32..30\]                                         | 3                                       | [시스템 클럭 참조](http://www.bretl.com/mpeghtml/SCR.HTM) (SCR) 비트 32에서 30 |
| 표시 비트                                                     | 1                                       | 항상 1 비트로 설정됨.                                                       |
| 시스템 클럭\[29..15\]                                          | 15                                      | 시스템 클럭 비트 29에서 15                                                   |
| 표시 비트                                                     | 1                                       | 항상 1 비트로 설정됨.                                                       |
| 시스템 클럭 \[14..0\]                                          | 15                                      | 시스템 클럭 비트 14에서 0                                                    |
| 표시 비트                                                     | 1                                       | 1 항상 1 비트로 설정됨.                                                     |
| SCR 확장                                                    | 9                                       |                                                                     |
| 표시 비트                                                     | 1                                       | 1 항상 1 비트로 설정됨.                                                     |
| [비트레이트](../Page/비트레이트.md "wikilink")                      | 22                                      | 초당 50 바이트 단위.                                                       |
| 표시 비트                                                     | 2                                       | 항상 11 비트로 설정됨.                                                      |
| 예약                                                        | 5                                       | 나중에 사용하기 위해 예약.                                                     |
| stuffing 길이                                               | 3                                       |                                                                     |
| stuffing 바이트                                              | 8\*stuffing 길이                          |                                                                     |
| 시스템 헤더 (선택적)                                              | 0 또는 그 이상                               | 시스템 헤더 시작 코드가 따라가기 시작할 시: 0x000001BB                                |

프로그램 스트림 팩 헤더 포맷 일부\[7\]

| 이름                                                        | 바이트 수 | 설명         |
| --------------------------------------------------------- | ----- | ---------- |
| [싱크 바이트](https://ko.wikipedia.org/wiki/싱크_바이트 "wikilink") | 4     | 0x000001BB |
| 헤더 길이                                                     | 2     |            |
| 레이트 바운드와 표시 비트                                            | 3     |            |
| 오디오 바운드와 플래그                                              | 1     |            |
| 플래그, 표시 비트, 비디오 바운드                                       | 1     |            |
| 패킷 레이트 제한과 예약 바이트                                         | 1     |            |

시스템 헤더 포맷 일부

## 같이 보기

  - [기초 스트림](https://ko.wikipedia.org/wiki/기초_스트림 "wikilink")
  - [MPEG 트랜스포트 스트림](../Page/MPEG_트랜스포트_스트림.md "wikilink")
  - [MPEG-1](../Page/MPEG-1.md "wikilink")
  - [MPEG-2](../Page/MPEG-2.md "wikilink")

## 각주

<references/>

[분류:MPEG](https://ko.wikipedia.org/wiki/분류:MPEG "wikilink") [분류:파일 포맷](https://ko.wikipedia.org/wiki/분류:파일_포맷 "wikilink") [분류:MPEG-2](https://ko.wikipedia.org/wiki/분류:MPEG-2 "wikilink")

1.  <http://webstore.iec.ch/preview/info_isoiec11172-1%7Bed1.0%7Den.pdf>
2.
3.  <http://dvd.sourceforge.net/dvdinfo/dvdmpeg.html>
4.  <http://www.vbrick.com/docs/VB_WhitePaper_TransportStreamVSProgramStream_rd2.pdf>
5.  <http://www.mpucoder.com/DVD/vobov.html>
6.
7.  [Pack Header](http://dvd.sourceforge.net/dvdinfo/packhdr.html)