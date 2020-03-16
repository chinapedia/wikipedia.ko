> This article is converted from Wikipedia: [LPT](https://ko.wikipedia.org/wiki/LPT).


[섬네일](https://ko.wikipedia.org/wiki/파일:25_Pin_D-sub_pinout.svg "wikilink") **LPT**(Line Print Terminal)은 [IBM PC 호환](../Page/IBM_PC_호환기종.md "wikilink") [병렬 포트](../Page/병렬_포트.md "wikilink") 인터페이스의 이름이다. [IBM](../Page/IBM.md "wikilink")의 8비트 [확장 ASCII](https://ko.wikipedia.org/wiki/확장_ASCII "wikilink") [문자열 집합을](https://ko.wikipedia.org/wiki/문자열_인코딩 "wikilink") 사용했던 텍스트 [프린터](../Page/프린터.md "wikilink")를 운영하기 위해 만들어진 것이다. 이 이름은 [라인 프린터가](https://ko.wikipedia.org/wiki/라인_프린터 "wikilink") 텍스트 프린터의 일반 용어로 자리잡았다는 사실에서 유래한다. 다른 장치의 호스트에 이은 그래픽 프린터는 시스템과 통신하기 위해 고안되었다. 이는 또한 여러 해 동안 [de facto](https://ko.wikipedia.org/wiki/de_facto "wikilink") 산업 표준이었으며, [1990년대](../Page/1990년대.md "wikilink") 말에 끝내 [IEEE 1284](https://ko.wikipedia.org/wiki/IEEE_1284 "wikilink") 표준으로 자리잡았다. 오늘날 병렬 포트 인터페이스는 [USB](../Page/USB.md "wikilink")와 [파이어와이어](https://ko.wikipedia.org/wiki/파이어와이어 "wikilink") 장치가 쓰이면서 점점 쓰이지 않고 있다.

## 역사

[1980년대](../Page/1980년대.md "wikilink"), 1990년대의 대부분의 PC 호환 시스템은 다음과 같이 정의된 통신 인터페이스가 포함된 한 두 개의 포트를 갖고 있었다.

  - **LPT1**: [입출력 포트](https://ko.wikipedia.org/wiki/MMIO "wikilink") 0x378, [IRQ](../Page/인터럽트_요청.md "wikilink") 7
  - **LPT2**: 입출력 포트 0x278, IRQ 5

일부 시스템은 **LPT3** 포트도 갖고 있었지만 제대로 정의되지는 않았다. 사실 컴퓨터가 두 개 이상의 LPT 포트를 사용하는 일은 드물다.

다양한 장치는 병렬 포트에서 동작하도록 고안되었다. 대부분은 단방향 장치였고, PC에서 송신된 정보에 반응만 한다는 것을 뜻한다. 그러나 [ZIP 드라이브와](https://ko.wikipedia.org/wiki/ZIP_드라이브 "wikilink") 같은 일부 장치들은 양방향 모드로 동작한다. 프린터는 또한 송신될 정보의 다양한 정보를 보고하기 위해 양방향 시스템을 사용하였다.

[MS-DOS](../Page/MS-DOS.md "wikilink"), [PC-DOS](../Page/PC-DOS.md "wikilink")에서, 병렬 포트는 [명령 줄에](https://ko.wikipedia.org/wiki/명령_줄 "wikilink") 직접 접근할 수 있다. 이를테면, "`type c:\autoexec.bat > LPT1`"는 [AUTOEXEC.BAT](../Page/AUTOEXEC.BAT.md "wikilink")의 내용을 프린터 포트에 내보낸다. **PRN** 장치는 LPT1의 하나로 사용할 수도 있었다. "print"라는 특별한 명령어도 존재하였는데 이와 같은 결과를 보여 준다. [마이크로소프트 윈도는](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 이러한 기능이 잘 드러나 있지 않으나 아직도 이러한 방법을 많은 경우에 사용하고 있다. [리눅스](../Page/리눅스.md "wikilink") 운영 체제에서는, 첫 LPT 포트를 파일 시스템 /dev/lp0을 통해 사용할 수 있다.

## 핀 출력

LPT 포트의 데이터 전송 속도는 초당 12,000 킬로비트에 이르며, LPT 포트는 다음과 같이 이루어져 있다.

  - 8비트의 병렬 데이터 버스
  - 제어 출력을 위한 4핀
      - 스트로브(Strobe)
      - 라인피드(Linefeed)
      - 이니셜라이즈(Initialize)
      - 셀렉트 인(Select In)
  - 제어 입력을 위한 5핀
      - ACK
      - 사용 중
      - 선택
      - 오류
      - 종이 출력

## 같이 보기

  - [COM 포트](https://ko.wikipedia.org/wiki/COM_\(하드웨어_인터페이스\) "wikilink")
  - [강화 병렬 포트](https://ko.wikipedia.org/wiki/IEE_1284 "wikilink") (SPP, EPP, ECP)

[분류:컴퓨터 버스](https://ko.wikipedia.org/wiki/분류:컴퓨터_버스 "wikilink")