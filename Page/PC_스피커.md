> This article is converted from Wikipedia: [PC ](https://ko.wikipedia.org/wiki/PC_).


**PC 스피커**()는 일부 [IBM PC 호환](../Page/IBM_PC_호환기종.md "wikilink") 컴퓨터에 내장된 [스피커](../Page/스피커.md "wikilink")이다. 최초의 [IBM 개인용 컴퓨터인](../Page/IBM_PC.md "wikilink") 모델 [5150](../Page/IBM_PC.md "wikilink") 모델에는 표준 2.25인치 자기 구동 스피커를 이용하였다.\[1\] 더 최근에 출시된 컴퓨터들은 압전소자(피에조) 방식의 스피커를 대신 이용한다.\[2\] 이 스피커는 [소프트웨어](../Page/소프트웨어.md "wikilink")와 [펌웨어](../Page/펌웨어.md "wikilink")가 사용자에게 소리로 하드웨어 실패와 같은 보고를 하기 위해 [피드백](../Page/피드백.md "wikilink")을 전달할 수 있다. PC 스피커는 [프로그래머블 인터벌 타이머](https://ko.wikipedia.org/wiki/프로그래머블_인터벌_타이머 "wikilink")(PIT), [인텔 8253](https://ko.wikipedia.org/wiki/인텔_8253 "wikilink"), [8254](https://ko.wikipedia.org/wiki/인텔_8254 "wikilink") 칩을 사용하여 파형을 만들어 내보낸다.\[3\]

## 용도

### 바이오스 오류 코드

PC 스피커는 [시동 자체 시험](../Page/시동_자체_시험.md "wikilink")(POST) 시퀀스 중에 [부팅](../Page/부팅.md "wikilink") 오류를 지시하기 위해 사용된다. [그래픽 카드](../Page/그래픽_카드.md "wikilink") 이전에 활성화되기 때문에 훨씬 더 복잡한 그래픽 카드의 초기화를 방해하는 문제들에 관한 "비프 코드" 통신에 사용할 수 있다. 이를테면, [비디오 바이오스는](../Page/비디오_바이오스.md "wikilink") 작동 중인 램이 시스템에 존재하지 않을 경우 일반적으로 그래픽 카드를 활성화할 수 없는 반면, 스피커의 비프음은 ROM과 CPU 레지스터만 있어도 동작할 수 있다. 일반적으로 각기 다른 오류 코드들은 특정한 비프음 패턴에 의해 인지할 수 있는데, 이를테면 "하나의 비프음, 잠시 정지, 세 개의 비프음, 잠시 정지, 반복"과 같은 형태이다. 이러한 패턴들은 [바이오스](../Page/바이오스.md "wikilink") 제조업체마다 다르며 일반적으로 메인보드의 기술 문서에 문서화되어 있다.

### 게임

PC 스피커는 당시 1990년대 중순의 [루카스아츠](../Page/루카스아츠.md "wikilink") 시리즈의 어드벤처 게임과 같은 컴퓨터 게임의 [폴리포니](https://ko.wikipedia.org/wiki/폴리포니 "wikilink") 음악이나 효과음을 만드는데 매우 혁신적인 방법으로 종종 사용되었다. 《[스페이스 헐크](../Page/스페이스_헐크.md "wikilink")》와 《[핀볼 판타지](https://ko.wikipedia.org/wiki/핀볼_판타지 "wikilink")》와 같은 여러 게임들이 이러한 효과음을 내기 위해 PC 스피커를 사용했으며, 스페이스 헐크는 특히 완전한 사람의 언어도 출력이 가능했다.

그러나 PCM 재생에 사용된 방식이 타이밍 문제에 매우 민감했기 때문에 이 결과로 저속의 PC에서는 눈에 띄게 느려지고, 고속의 PC(프로그램 개발 당시의 것보다 더 빠른 PC)에서는 완전히 재생을 실패하는 일이 가끔 있다. 또, 프로그램들이 소리 등을 재생하는 중에 디스플레이 업데이트하는 일이 어려운 편에 속했다. 그러므로 1990년 이후 사운드 카드(초기화 시 CPU와 독립적으로 복잡한 소리를 출력할 수 있음)가 PC 시장의 주류로 되었을 때 선호되는 출력 장치로서 빠르게 PC 스피커를 대체해나갔다. 최신의 PC 게임들은 1990년대 중순 PC 스피커 지원을 중단하였다.

### 기타 프로그램

MP(모듈 플레이어, 1989년), [스크림트래커](https://ko.wikipedia.org/wiki/스크림트래커 "wikilink"), [패스트 트래커](https://ko.wikipedia.org/wiki/패스트_트래커 "wikilink"), [임펄스 트래커를](https://ko.wikipedia.org/wiki/임펄스_트래커 "wikilink") 포함한 여러 프로그램들, 심지어는 [리눅스](../Page/리눅스.md "wikilink")\[4\] 및 [마이크로소프트 윈도우용](../Page/마이크로소프트_윈도우.md "wikilink") [장치 드라이버는](../Page/장치_드라이버.md "wikilink") 본문에 나중에 기술될 특수 기법을 사용하여 PC 스피커를 통해 [펄스 부호 변조](../Page/펄스_부호_변조.md "wikilink")(PCM)를 재생할 수 있다.

현대의 마이크로소프트 윈도우 운영 체제들은 특수 기능을 갖춘 별도의 장치로서 PC 스피커를 지원하고 있는데, 즉 일반 오디오 출력 장치로 구성이 불가능함을 뜻한다. 일부 소프트웨어는 이 특수한 사운드 채널을 사용하여 소리를 출력한다. 이를테면 [스카이프](../Page/스카이프.md "wikilink")는 주 오디오 출력 장치를 들을 수 없을 때(이를테면 볼륨이 최소 수준으로 설정되었다든지 앰프가 꺼져있는 경우)를 대비해 리버스 콜링 시그널(reserve calling signal) 장치로 PC 스피커를 사용할 수 있다.

## 핀 출력

[섬네일](https://ko.wikipedia.org/wiki/파일:JPANEL_MB_IMG_1121.JPG "wikilink") [섬네일](https://ko.wikipedia.org/wiki/파일:PC-Speaker_IMG_9311-9312.JPG "wikilink")(piezoelectric) PC 스피커는 4핀 2선 연결을 사용한다.\]\] 일부의 경우 PC 스피커는 컴퓨터의 [메인보드](../Page/메인보드.md "wikilink")에 직접 부착되어 있다. 최초의 IBM PC를 포함한 그 밖의 경우 스피커는 메인보드의 단자에 선을 통해 연결된다. 일부 PC 케이스들은 PC 스피커가 미리 설치되어 있는 경우가 있다. 유선 PC 스피커 단자는 2, 3, 4핀 구성일 수 있으며 2\~3개의 선일 수 있다. 스피커의 암(female) 단자는 메인보드의 SPEAKER, SPKR로 표시되곤 하는 [핀 헤더에](https://ko.wikipedia.org/wiki/핀_헤더 "wikilink") 연결한다.

| 핀 번호 | 핀 이름       | 핀 기능            |
| ---- | ---------- | --------------- |
| 1    | \-SP       | 스피커 음극          |
| 2    | GND 또는 KEY | 접지 또는 선 연결 없는 키 |
| 3    | GND        | 접지 (그라운드)       |
| 4    | \+SP5V     | 스피커 양극 +5V DC   |

4핀, 3선 PC 스피커 핀 출력\[5\]\[6\]

## 펄스폭 변조

PC 스피커는 일반적으로 오직 2 레벨의 출력을 통해 [방형파](https://ko.wikipedia.org/wiki/방형파 "wikilink")를 재생하는 것을 의미한다. (스피커는 오직 2개의 전압 레벨로 구동되는데, 일반적으로 0 V와 5 V이다) 그러나 짧은 [펄스](https://ko.wikipedia.org/wiki/펄스 "wikilink")의 타이밍을 조심스럽게 조절함으로써(예: 출력 레벨에서 다른 레벨로 이동하고 다시 처음으로 되돌아올 때), 또 스피커의 물리적 필터링 특성에 의존함으로써(제한된 주파수 반응, 자기 인덕턴스 등) 최종 결과는 중간의 사운드 레벨과 일치하게 된다. 이는 효율적으로 스피커가 대체적인 6비트 [DAC](../Page/디지털-아날로그_변환회로.md "wikilink")\[7\]로 기능할 수 있다는 것을 의미하므로 [PCM 오디오의](https://ko.wikipedia.org/wiki/PCM_오디오 "wikilink") 대략적인 재생을 가능케 한다. 이 기법을 [펄스 폭 변조](https://ko.wikipedia.org/wiki/펄스_폭_변조 "wikilink")(PWM)라 부르며 특히 [클래스 D](../Page/증폭_회로.md "wikilink") [앰프](../Page/앰프.md "wikilink")에서 사용된다.

PC 스피커를 사용하면 이 방식은 제한된 품질의 재생을 달성할 수 있다. 즉, 품질은 PWM [반송 주파수](https://ko.wikipedia.org/wiki/반송_주파수 "wikilink")(효율적인 샘플레이트)와 출력 레벨의 수(효율적인 비트레이트) 간에 타협을 보며 결정된다. 스피커를 구동하는 PC의 [프로그래머블 인터벌 타이머](https://ko.wikipedia.org/wiki/프로그래머블_인터벌_타이머 "wikilink")(PIT)의 클럭 속도는 1,193.18 kHZ로 고정된다.\[8\] 이렇게 상대적으로 낮은 변조 주파수는 제한된 해상력의 인지는 가능한 저품질 오디오를 만들어낸다.\[9\]

[사운드 블라스터와](../Page/사운드_블라스터.md "wikilink") 기타 [사운드 카드의](../Page/사운드_카드.md "wikilink") 등장에 힘입어, 복잡한 소리 출력에 PC 스피커를 사용하는 일은 흔치 않다.

## 같이 보기

  - [인텔 8253](https://ko.wikipedia.org/wiki/인텔_8253 "wikilink")
  - [리얼사운드](../Page/리얼사운드.md "wikilink")

## 각주

## 외부 링크

  - [Smacky](http://smacky.sourceforge.net/) Open-source C++ software for playing songs on the PC speaker.
  - [Site for old PC without sound cards](http://spkcorner.tripod.com/).
  - [PCGPE article on programming the PC Speaker](https://web.archive.org/web/20151208061729/https://courses.engr.illinois.edu/ece390/resources/sound/speaker.txt.html).
  - [Part 1 of another article about programming the PC speaker](https://web.archive.org/web/20140307023908/http://fly.srk.fer.hr/GDM/articles/sndmus/speaker1.html).
  - [Part 2 of the article](https://web.archive.org/web/20140307043446/http://fly.srk.fer.hr/GDM/articles/sndmus/speaker2.html)
    (includes a very detailed explanation of how to play back PCM audio on the PC speaker, and why it works)
  - [Bleeper Music Maker](http://robbi-985.homeip.net:8000/hosted_programs/update/bmm/index.html) A freeware to use the PC speaker to make music (superseded by [BaWaMI](http://robbi-985.homeip.net:8000/hosted_programs/update/bawami/))
  - [Article about programming PC speaker using C++](http://www.frank-buss.de/beep/index.html)
  - [Commandline PC speaker program for Linux](http://www.johnath.com/beep/)[FTP](https://web.archive.org/web/20030820082835/http://ftp.falsehope.com/pub/beep/)
  - [Practical article on implementing a Linux Kernel Driver](https://web.archive.org/web/20040820223947/http://linuxgazette.net/issue69/mathew.html)
  - [Timing on the PC family under DOS](http://www.phatcode.net/articles.php?id=246) (Sections 7.5, 7.29, 7.30, and 10.7 – 10.7.4 in particular)

[분류:스피커](https://ko.wikipedia.org/wiki/분류:스피커 "wikilink")

1.
2.
3.
4.
5.
6.
7.  <http://www.oldskool.org/sound/pc/#digitized>
8.
9.