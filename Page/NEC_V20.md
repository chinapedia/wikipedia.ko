> This article is converted from Wikipedia: [NEC V20](https://ko.wikipedia.org/wiki/NEC_V20).


**NEC V20**(μPD70108) [NEC](https://ko.wikipedia.org/wiki/NEC "wikilink")에서 개발한 [x86](https://ko.wikipedia.org/wiki/x86 "wikilink")호환 [CPU다](https://ko.wikipedia.org/wiki/중앙_처리_장치 "wikilink").

V20은 [리버스 엔지니어링으로](https://ko.wikipedia.org/wiki/리버스_엔지니어링 "wikilink") 제작되었으며 [인텔 8088과](https://ko.wikipedia.org/wiki/인텔_8088 "wikilink") 핀 호환되며 명령어 셋은 [인텔 80186과](../Page/인텔_80186.md "wikilink") 호환된다. 약 29,000개의 [트랜지스터](https://ko.wikipedia.org/wiki/트랜지스터 "wikilink")로 구성되어 있으며 8 \~ 16MHz로 작동된다. 하드웨어 [곱셈기](../Page/곱셈기.md "wikilink")와 같이 내부 구조 개선으로 프로그램에 따라 같은 클럭의 8088보다 10\~30% 빠르다.

또 V20은 [인텔 8080](https://ko.wikipedia.org/wiki/인텔_8080 "wikilink") 에뮬레이션 모드가 포함되어 있는데 8086 모드의 BRKEM 명령과 8080 모드의 RETEM과 CALLN 명령으로 에뮬레이션 모드로 전환할 수 있다. [소니](https://ko.wikipedia.org/wiki/소니 "wikilink")에서 [라이선스](https://ko.wikipedia.org/wiki/라이선스 "wikilink")로 생산하기도 했다.

데이터 버스 폭이나 주변기기의 내장에 따라 V25, V30, V33, V40, V50등의 변종으로 나뉘는데 이를 통틀어 V 시리즈라 한다.

## V 시리즈

  - **V10**(μPD70008) : [Z80](https://ko.wikipedia.org/wiki/Z80 "wikilink") 호환 [NMOS](https://ko.wikipedia.org/wiki/NMOS "wikilink") CPU인 uPD780의 [CMOS](../Page/CMOS.md "wikilink") 버전으로 법률 문제때문에 정식으로 시판되지 않았다.
  - **V20**(μPD70108) : 8088과 핀 호환, 데이터 버스 8비트, 탠디 1110에 사용
  - **V20HL**(μPD70108H) : V20의 고클럭(16Mhz), 저전력 버전
  - **V25**(μPD70320,μPD70322) : V20에 주변 I/F를 추가한 [임베디드](https://ko.wikipedia.org/wiki/임베디드 "wikilink")용 프로세서, μPD70322은 μPD70320에서 [ROM](https://ko.wikipedia.org/wiki/ROM "wikilink")을 제거
  - **V25+**(μPD70325) : V25의 [DMA](https://ko.wikipedia.org/wiki/기억_직접_접근 "wikilink") 전송 속도를 개선과 고속화(10MHz)
  - **V30**(μPD70116) : [8086](https://ko.wikipedia.org/wiki/8086 "wikilink")과 핀 호환, 데이터 버스 16비트, 기능은 V20과 동일, Psion 3에 사용
  - **V30HL**(μPD70116H) : V30의 고클럭(16Mhz) 저전력 버전, PC-9801UF, PC-9801UR과 노트북 PC-9801NV, PC-9801NL에 사용
  - **V30MZ** : 임베디드용 [IP코어](https://ko.wikipedia.org/wiki/IP코어 "wikilink"), [휴대용 게임기](../Page/휴대용_게임기.md "wikilink") [원더스완](https://ko.wikipedia.org/wiki/원더스완 "wikilink")에 사용
  - **V33**(μPD70136) : V30의 어드레스 버스와 데이터 버스를 분리, BRKXA와 RETXA 명령 추가로 16M의 메모리 어드레싱 모드 지원, 마이크로코드의 저작권 해소를 위해 대부분의 명령어를 와이어 로직으로 변경해 V30의 2배성능으로 [80286](https://ko.wikipedia.org/wiki/80286 "wikilink")과 처리속도가 동등, 8080 에뮬레이션 모드 제거
  - **V33A**(μPD70136A) : 인터럽트 벡터등 인텔 80X86과의 호환성 개선, PC-98DO+에 사용
  - **V35**(μPD70330) : V30에 주변I/F를 추가한 임베디드용 프로세서
  - **V35+**(μPD70335) : V30의 DMA전송 속도를 개선과 고속화(10MHz)
  - **μPD9002** : V30모드와 Z80호환 모드를 가지고 있다. PC-88VA에 사용
  - **V40**(μPD70208) : V20에 클럭 제네레이터, [DRAM](https://ko.wikipedia.org/wiki/DRAM "wikilink") 리프레쉬 컨트롤, μPD71054([i8254](https://ko.wikipedia.org/wiki/i8254 "wikilink")호환) 타이머/카운트, μPD71051([i8251](https://ko.wikipedia.org/wiki/i8251 "wikilink")호환) 시리얼 UART, μPD71059([i8259](https://ko.wikipedia.org/wiki/i8259 "wikilink")호환) 인터럽트 컨트롤 유닛, μPD71071([i8237](https://ko.wikipedia.org/wiki/i8237 "wikilink")호환) DMA 컨트롤 유닛을 내장
  - **V50**(μPD70216) : V30에 클럭 제네레이터, DRAM 리프레쉬 컨트롤, μPD71054(i8254호환) 타이머/카운트, μPD71051(i8251호환) 시리얼 UART, μPD71059(i8259호환) 인터럽트 컨트롤 유닛, μPD71071(i8237호환) DMA 컨트롤 유닛을 내장
  - **V41**(μPD70270), **V51**(μPD70280) : V30HL에 8255 패러랠 포트 인터페이스, 8254 프로그래머블 인터벌 타이머, 8259 PIC, 8237 DMA 컨트롤러, 8042 키보드 컨트롤러, DRAM 컨트롤러 내장, 올리베티의 Quaderno XT-20에 사용
  - **V53**(μPD70236) : V50의 코어를 V33으로 변경
  - **V53A**(μPD70236A) : V53의 코어를 V33A로 변경
  - **V55PI**(μPD70433) : 80186 명령어 세트와 주변기기를 내장
  - **V60**(μPD70616) : 내부 32비트, 외부 16비트, 24비트 어드레스 버스의 32비트 [CISC](https://ko.wikipedia.org/wiki/CISC "wikilink") CPU, 이전 CPU와는 달리 NEC 고유의 명령어 세트가 특징이며 V30 에뮬레이트 모드와 FPU를 내장했다. [세가 시스템32와](https://ko.wikipedia.org/wiki/세가_시스템32 "wikilink") [세가 모델 1에](https://ko.wikipedia.org/wiki/세가_모델_1 "wikilink") 사용되었다.
  - **V70**(μPD70632) : V60을 내,외부 버스를 32비트로 변경, [세가 시스템 멀티 32와](https://ko.wikipedia.org/wiki/세가_시스템_멀티_32 "wikilink") [자레코 메가 시스템 32에](https://ko.wikipedia.org/wiki/자레코_메가_시스템_32 "wikilink") 사용되었다.
  - **V80** : 마지막 CISC CPU, V30 에뮬레이트 모드 제거
  - **V20, V30용 [FPU](https://ko.wikipedia.org/wiki/FPU "wikilink")**(uPD71091) : [인텔 8087과는](https://ko.wikipedia.org/wiki/인텔_8087 "wikilink") 동작이 달라 별도의 보조회로 필요
  - **V800** : [RISC](https://ko.wikipedia.org/wiki/RISC "wikilink") CPU로 V810/V830/V850 등이 있다. NEC [PC-FX](https://ko.wikipedia.org/wiki/PC-FX "wikilink")와 [닌텐도](https://ko.wikipedia.org/wiki/닌텐도 "wikilink") [버추얼 보이에](https://ko.wikipedia.org/wiki/버추얼_보이 "wikilink") 사용

## 외부 링크

  - [cpu-collection.de의 V20](http://www.cpu-collection.de/?l0=co&l1=NEC&l2=V20)
  - [Cpu World의 V20](http://www.cpu-world.com/CPUs/V20/)

[분류:X86 마이크로프로세서](https://ko.wikipedia.org/wiki/분류:X86_마이크로프로세서 "wikilink")