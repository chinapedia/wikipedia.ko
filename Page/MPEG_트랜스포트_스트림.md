> This article is converted from Wikipedia: [MPEG 트랜스포트 스트림](https://ko.wikipedia.org/wiki/MPEG_트랜스포트_스트림).


[섬네일는](https://ko.wikipedia.org/wiki/파일:MPEG_Transport_Stream_HL.svg "wikilink") TS를 디코딩하여 화면에 보여 준다. 세계 수많은 지역에서 하나 이상의 변종 모듈러 DVB 시스템을 통하여 전달이 이루어진다.\]\]  **MPEG 트랜스포트 스트림**(MPEG transport stream, TS, TP, MPEG-TS로 줄임)은 [오디오](https://ko.wikipedia.org/wiki/오디오 "wikilink"), [비디오](../Page/비디오.md "wikilink"), [데이터](https://ko.wikipedia.org/wiki/데이터 "wikilink") 전송을 위한 [통신 프로토콜이다](../Page/통신_프로토콜.md "wikilink"). PES(packetized elementary streams) 와 기타 데이터를 포함하는 디지털 컨테이너 포맷의 일종이다. TS는 [MPEG-2](../Page/MPEG-2.md "wikilink") 파트 1, 시스템([ISO](../Page/국제_표준화_기구.md "wikilink")/[IEC](https://ko.wikipedia.org/wiki/국제_전기_표준_회의 "wikilink") 표준 13818-1)에 규정되어 있다.\[1\] ITU-T Rec. H.222.0으로도 알려져 있다. 디지털 영상과 소리를 [다중화](https://ko.wikipedia.org/wiki/다중화 "wikilink")하고 출력을 동기화하는 것이 이 시스템의 목표이다. 트랜스포트 스트림은 신뢰할 수 없는 매체의 [오류 정정](https://ko.wikipedia.org/wiki/오류_정정 "wikilink") 기능을 제공하고 [DVB와](../Page/디지털_비디오_방송.md "wikilink") [ATSC](https://ko.wikipedia.org/wiki/ATSC "wikilink")와 같은 영상 응용에도 쓰인다. [DVD](../Page/DVD.md "wikilink")와 같은 신뢰할 수 있는(데이터 손실 우려가 없는) 매체용으로 개발된 [MPEG 프로그램 스트림과는](../Page/MPEG_프로그램_스트림.md "wikilink") 대조된다.

## 통신 계층

[OSI 네트워크](https://ko.wikipedia.org/wiki/OSI_모델 "wikilink") [프로토콜 스택과](https://ko.wikipedia.org/wiki/프로토콜_스택 "wikilink") 비슷하게 트랜스포트 스트림은 계층 구조에서 수신기가 처리한다. 이를테면 비디오를 포함하는 스트림은 다음과 같은 처리를 할 수 있다.

1.  다양한 프로그램 구성
2.  PES (패킷화된 기초 스트림, Packetized Elementary Stream)
3.  ES (기초 스트림, Elementary stream) - 소리 및 영상 (아래의 것은 영상만)
4.  GOP 구조 (Group of pictures) - 임의 접근 포인트 제공
5.  슬라이스 (Slice) - 상호 예측을 통하여 파급된 오류 방지
6.  매크로블록 - 6\~12개의 [DCT](../Page/이산_코사인_변환.md "wikilink") 블록으로 이루어져 있음
7.  인코딩 블록 / 단순 블록 - [DCT](../Page/이산_코사인_변환.md "wikilink") 인코딩 블록, 8x8 화소

트랜스포트 스트림(TS)으로 다중화 처리된 데이터의 예가 바로 [EPG](https://ko.wikipedia.org/wiki/EPG "wikilink") (전자 프로그램 안내)이다. 더 자세한 내용은 [프로그램과 시스템 정보 프로토콜을](https://ko.wikipedia.org/wiki/프로그램과_시스템_정보_프로토콜 "wikilink") 참고하라.

## 트랜스포트 스트림의 중요 요소

### 패킷

패킷은 트랜스포트 스트림의 기본 데이터 단위이다. 값이 0x47인 [싱크 바이트와](https://ko.wikipedia.org/wiki/싱크_바이트 "wikilink") 그 뒤를 이어 3개의 1비트 플래그와 13비트의 PID (패킷 증명자), 4비트의 연속 카운터, 추가적인 유효한 필드 신호가 있으면 추가로 선택할 수 있는 트랜스포트 필드가 온다. 패킷의 나머지는 페이로드(payload)다. 패킷들의 길이는 188 바이트이지만\[2\] 통신 매체는 패킷에다 오류 정정 바이트를 몇 개 추가할 수 있다. [ISDB-T](https://ko.wikipedia.org/wiki/ISDB-T "wikilink") 및 DVB-T/C/S의 전송 패킷 크기(트랜스포트 스트림 패킷 + FEC 데이터)는 204 바이트이며 ATSC 8-VSB의 전송 패킷 크기는 208 바이트이다. ATSC는 20바이트의 [리드 솔로몬](https://ko.wikipedia.org/wiki/리드_솔로몬_부호 "wikilink") [전방 오류 정정을](https://ko.wikipedia.org/wiki/전방_오류_정정 "wikilink") 사용하여 208바이트의 패킷을 만들어낸다.\[3\] 188바이트의 패킷 크기는 원래 [ATM 체계와의](../Page/비동기_전송_방식.md "wikilink") 호환성을 위하여 선정된 것이다.\[4\]\[5\]

<table>
<caption>TS 패킷 포맷 일부</caption>
<thead>
<tr class="header">
<th><p>이름</p></th>
<th><p><a href="../Page/비트_(단위).md" title="wikilink">비트</a> 수</p></th>
<th><p>32-bit <a href="../Page/엔디언.md" title="wikilink">BE</a> mask</p></th>
<th><p>설명</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/싱크_바이트" title="wikilink">싱크 바이트</a></p></td>
<td><p>8</p></td>
<td><p>0xff000000</p></td>
<td><p>0x47 (ASCII char 'G')</p></td>
</tr>
<tr class="even">
<td><p>전송 오류 표시기 (TEI)</p></td>
<td><p>1</p></td>
<td><p>0x800000</p></td>
<td><p>스트림에서 오류를 정정할 수 없으면 <a href="https://ko.wikipedia.org/wiki/복조" title="wikilink">복조</a>를 통하여 설정됨. 역다중화기(demultiplxer)에 패킷에 정정할 수 없는 오류가 있음을 알려 준다[6]</p></td>
</tr>
<tr class="odd">
<td><p>페이로드 유닛 시작 표시기</p></td>
<td><p>1</p></td>
<td><p>0x400000</p></td>
<td><p>1은 PES(PSI)의 시작을 나타내고 그렇지 않으면 0이다.</p></td>
</tr>
<tr class="even">
<td><p>전송 우선 순위</p></td>
<td><p>1</p></td>
<td><p>0x200000</p></td>
<td><p>1은 같은 PID를 갖는 다른 패킷들보다 더 높은 우선 순위를 갖는 것을 뜻한다.</p></td>
</tr>
<tr class="odd">
<td><p>PID</p></td>
<td><p>13</p></td>
<td><p>0x1fff00</p></td>
<td><p>패킷 ID</p></td>
</tr>
<tr class="even">
<td><p>스크램블 제어</p></td>
<td><p>2</p></td>
<td><p>0xc0</p></td>
<td><p>'00' = 스크램블(scramble) 안 함.   DVB 기준:[7]   '01' = 사용 예약,   '10' = 짝수로 스크램블,   '11' = 홀수로 스크램블</p></td>
</tr>
<tr class="odd">
<td><p>유효 필드 제어</p></td>
<td><p>2</p></td>
<td><p>0x30</p></td>
<td><p>01 - 유효 필드 없음, 페이로드 존재 10 - 유효필드 존재, 페이로드 없음</p>
<p>11 - 유효필드 다음에 페이로드 존재</p>
<p>00 - 추후 사용. (현재는 사용하지 않음)</p></td>
</tr>
<tr class="even">
<td><p>연속 카운터</p></td>
<td><p>4</p></td>
<td><p>0xf</p></td>
<td><p>각 스트림에서 페이로드 패킷의 연속된 숫자. 페이로드가 있을때만 증가되며 각 PID 단위로 증가된다.</p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><p>|알림: 위의 총 비트 수는 32이며 트랜스포트 스트림 4바이트 접두사(prefix)이다.</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>유효 필드</p></td>
<td><p>0 이상</p></td>
<td><p>|플래그에 의존</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/페이로드_(소프트웨어)" title="wikilink">페이로드</a> <a href="https://ko.wikipedia.org/wiki/데이터" title="wikilink">데이터</a></p></td>
<td><p>0 이상</p></td>
<td><p>|플래그에 의존</p></td>
<td></td>
</tr>
</tbody>
</table>

| 이름                                                                  | 비트 수 | 설명                                                      |
| ------------------------------------------------------------------- | ---- | ------------------------------------------------------- |
| 유효 필드 길이                                                            | 8    | 즉각 이 바이트의 길이만큼 유효 필드가 따라온다                              |
| 불연속 표시기                                                             | 1    | TS 패킷의 연속 카운터가 연속적이지 않으면 1로 설정한다                        |
| 임의 접근 표시기                                                           | 1    | 이 TS 패킷의 PES 패킷이 영상/소리 시퀀스를 시작하면 1로 설정한다                |
| [기초 스트림](https://ko.wikipedia.org/wiki/기초_스트림 "wikilink") 우선 순위 표시기 | 1    | 1 = 높은 순위                                               |
| PCR 플래그                                                             | 1    | 1이면 유효 필드가 PCR 필드를 포함한다는 것을 뜻한다                         |
| OPCR 플래그                                                            | 1    | 1이면 유효 필드가 OPCR 필드를 포함한다는 것을 뜻한다                        |
| 접합(Splicing) 포인트 플래그                                                | 1    | 1이면 유효 필드에 접합 카운트다운 필드가 존재한다는 것을 뜻한다                    |
| 트랜스포트 개별 데이터 플래그                                                    | 1    | 1이면 유효 필드에 개별 데이터 바이트가 존재한다는 것을 뜻한다                     |
| 유효 필드 확장 플래그                                                        | 1    | 1이면 유효 필드 확장이 존재한다는 것을 뜻한다                              |
| 아래의 필드는 선택 사항이다                                                     | 가변값  | 플래그에 의존                                                 |
| PCR                                                                 | 33+9 | 프로그램 클록 참조                                              |
| OPCR                                                                | 33+9 | OP(Original Program) 클록 참조.. 하나의 TS가 다른 곳으로 복사될 때 도와준다. |
| 접합(Splice) 카운트다운                                                    | 8    | 이 곳으로부터 얼마나 많은 TS 패킷에 접합 포인트가 발생하였는지 알려 준다 (음수값)        |
| 빈 자리 메우는 바이트                                                        | 가변값  |                                                         |

유효 필드 포맷

<div style="clear:both">

</div>

### PID

TS의 각 테이블이나 기초 스트림(ES)은 13비트 패킷 ID (PID)로 식별한다. 역다중화기(demultiplexer)는 같은 PID로 식별된 패킷을 검색하여 부분적으로 TS로부터 기초 스트림을 추출한다. [시분할 다중화는](../Page/시분할_다중화.md "wikilink") 얼마나 자주 특정한 PID가 TS에 나타나는지를 결정하는 데 쓰인다.

### 프로그램

TS에는 프로그램 개념이 있다. 각 프로그램은 고유 PID를 갖는 프로그램 맵 테이블 (PMT)로 기술되며 그 프로그램과 연결된 기초 스트림은 PMT에 나열된 PID를 가진다. 이를테면 디지털 TV에 쓰이는 TS는 세 개의 텔레비전 채널을 표현하기 위하여 이러한 프로그램들을 포함할 수 있다. 각 채널이 하나의 비디오 스트림과 한 두 개의 오디오 스트림, 또 필요한 메타 데이터를 갖고 있다는 가정을 해 볼 수 있다. [수신기가](https://ko.wikipedia.org/wiki/ATSC_튜너 "wikilink") 특정한 채널을 디코딩하려면 이 프로그램에 연결된 각 PID의 페이로드를 디코딩하여야 한다.

### 프로그램 지정 정보 (PSI)

프로그램 지정 정보에는 4개의 [PSI가](https://ko.wikipedia.org/wiki/프로그램_지정_정보 "wikilink") 있다.

  - 프로그램 연결 (Program Association, PAT)
  - 프로그램 맵 (Program Map ,PMT)
  - 조건식 제한 접근(Conditional Access, CAT)
  - 네트워크 정보(Network Information, NIT)

MPEG-2 규격은 CAT와 NIT 포맷에 대하여 규정해 놓지 않았다.

### PAT

PAT (프로그램 연결 테이블, Program Association Table)는 TS에서 사용할 수 있는 모든 프로그램을 나열한다. 나열된 프로그램은 각각 program_number (프로그램 계수)라 불리는 16비트 값으로 식별된다. PAT에 나열된 프로그램은 제각각 프로그램 맵 테이블(PMT)의 PID 연결 값을 갖고 있다.

program_number의 값 0x0000는 PID에 네트워크 정보 테이블 위치를 부여하기 위해 보존된다. 해당 프로그램이 PAT에 존재하지 않으면 기본 PID 값 (0x0010)이 NIT에 쓰인다.

### PMT

프로그램 맵 테이블(PMT)은 프로그램에 대한 정보를 갖고 있다. 각 프로그램마다 PMT가 존재한다. MPEG-2 표준이 하나 이상의 PMT 섹션이 단일 PID에 전송될 수 있는 기능을 제공하지만 ATSC와 SCTE와 같은 영역에 속한 대부분의 MPEG-2 사용자들은 각 PMT가 다른 어떠한 패킷에도 쓰이지 않는 하나의 구별된 PID 상에서 전송할 것을 요구한다. PMT는 program_number를 비롯하여 TS에 존재하는 각 프로그램에 대한 정보를 제공하며 기술된 MPEG-2 프로그램을 구성하는 기초 스트림을 나열한다. 각 기초 스트림을 위한 선택적 기술자뿐 아니라 완전한 MPEG-2 스트림을 기술하는 선택적 기술자를 위한 위치 정보도 제공한다. 각 기초 스트림은 stream_type (스트림 종류) 값으로 그 이름이 붙어 있다.

### PCR

연결된 영상과 결합된 오디오 트랙과 같이 동기화된 콘텐츠를 표현하는 디코더를 사용하려면 적어도 100 밀리초마다 프로그램 클록 참조(PCR)가 MPEG-2 TS 패킷의 유효 필드에 전송되어야 한다. MPEG-2 프로그램을 위한 PCR이 있는 PID는 연결된 프로그램 맵 테이블(PMT) 안에서 pcr_pid 값으로 식별된다. 문제가 없다면 PCR의 값은 디코더 안에서 system_timing_clock (시스템 타이밍 클록)을 만들어 낸다. 여기에도 문제가 없으면 STC 디코더는 영상 및 소리의 기초 시스템을 동기화하는 데 쓰이는 더 정확한 시간대를 제공한다. MPEG2 타이밍은 이 클록을 참조하는데 이를테면 [재현 시간표](https://ko.wikipedia.org/wiki/재현_시간표 "wikilink") (PTS)는 PCR에 관련되어 있다. 처음 33비트는 90kHz 클록에 기반을 두며 마지막 9비트는 27MHz 클록에 기반을 둔다. PCR이 허용하는 최대 지터는 +/- 500 나노초이다.

### Null 패킷

[ATSC](https://ko.wikipedia.org/wiki/ATSC "wikilink")와 [DVB](https://ko.wikipedia.org/wiki/DVB "wikilink")와 같은 일부 전송 체계는 엄격한 고정 비트레이트를 TS에 요구한다. 스트림이 고정 비트레이트를 유지하려면 다중화기는 일부 추가적인 패킷을 삽입하여야 한다. 이에 PID 0x1FFF가 예약돼 있다. null 패킷의 페이로드는 데이터에 전혀 포함되지 않으며 수신기가 null 패킷의 콘텐츠 내용을 무시하게 된다.

## TS 파일 지원 프로그램

### 다중 운영 체제

  - [FFmpeg](../Page/FFmpeg.md "wikilink")
  - [엠플레이어](https://ko.wikipedia.org/wiki/엠플레이어 "wikilink")\[8\]
  - 비디오랜 [VLC 미디어 플레이어](../Page/VLC_미디어_플레이어.md "wikilink")\[9\]

### 리눅스

  - [xine](https://ko.wikipedia.org/wiki/xine "wikilink")
  - [MythTV](../Page/MythTV.md "wikilink")
  - [GStreamer](../Page/GStreamer.md "wikilink")
  - OpenCaster\[10\]\[11\]

### 윈도

  - [컴바인드 커뮤니티 코덱 팩](https://ko.wikipedia.org/wiki/컴바인드_커뮤니티_코덱_팩 "wikilink")\[12\]
  - 스퀘어드 5 [MPEG 스트림클립](https://ko.wikipedia.org/wiki/MPEG_스트림클립 "wikilink")\[13\]
  - [토탈 비디오 컨버터](https://ko.wikipedia.org/wiki/토탈_비디오_컨버터 "wikilink")
  - [AVS 비디오 컨버터](https://ko.wikipedia.org/wiki/AVS_비디오_컨버터 "wikilink")
  - [포맷팩토리](https://ko.wikipedia.org/wiki/포맷팩토리 "wikilink")
  - [LEADTOOLS MPEG-2 Transport SDK Module](https://web.archive.org/web/20100402091329/http://www.leadtools.com/sdk/mpeg2-transport.htm)

### macOS

  - 스퀘어드 5 [MPEG 스트림클립](https://ko.wikipedia.org/wiki/MPEG_스트림클립 "wikilink")\[14\]
  - iFunia 비디오 컨버터\[15\]

## 같이 보기

  - [MPEG-2](../Page/MPEG-2.md "wikilink")
  - [플래시 비디오](../Page/플래시_비디오.md "wikilink")
  - [IPTV](../Page/IPTV.md "wikilink")

## 각주

## 외부 링크

  - [MPEG-2 Systems FAQ](http://mpeg.chiariglione.org/faq/mp2-sys/mp2-sys.htm)
  - [MPEG-4 Systems FAQ](http://mpeg.chiariglione.org/faq/mp4-sys/mp4-sys.htm)
  - [MPEG-1 설명](http://mpeg.chiariglione.org/standards/mpeg-1/mpeg-1.htm)
  - [Powerpoint MPEG-2 Transport Stream introduction](https://web.archive.org/web/20100331134640/http://chapters.scte.org/cascade/DVB%20Overview.ppt) [1](http://www.glue.umd.edu/~karir/mpeg2/MPEG-2.PPT)
  - [DVB Transport Stream.pdf](https://web.archive.org/web/20070221121842/http://www.abo.fi/~jbjorkqv/digitv/lect4.pdf)
  - [MPEG-2 Transport Stream](http://wiki.multimedia.cx/index.php?title=MPEG-2_Transport_Stream)

[분류:MPEG](https://ko.wikipedia.org/wiki/분류:MPEG "wikilink") [분류:파일 포맷](https://ko.wikipedia.org/wiki/분류:파일_포맷 "wikilink") [분류:MPEG-2](https://ko.wikipedia.org/wiki/분류:MPEG-2 "wikilink") [분류:ITU-T 권고](https://ko.wikipedia.org/wiki/분류:ITU-T_권고 "wikilink")

1.
2.
3.
4.  [MPEG Systems FAQ](http://mpeg.chiariglione.org/faq/mp2-sys/mp2-sys.htm#mp2-12)
5.
6.
7.  [DVB scrambling control bits defined. Page 6](http://www.bjpace.com.cn/data/tec/tec-DVB/DVB%20BlueBooks%20Standards/Specifications%20and%20Standards/conditional%20access/dvb-csa/A007.pdf)
8.  [Entering MPlayer homepage](http://www.mplayerhq.hu/)
9.  [VideoLAN - VLC media player - Open Source Multimedia Framework and Player](http://www.videolan.org/vlc/)
10.
11.
12.
13. [Squared 5 - MPEG Streamclip video converter for Mac and Windows](http://www.squared5.com/)
14.
15.