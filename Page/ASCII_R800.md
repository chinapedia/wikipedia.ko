> This article is converted from Wikipedia: [ASCII R800](https://ko.wikipedia.org/wiki/ASCII_R800).


[thumb](https://ko.wikipedia.org/wiki/파일:R800_02.jpg "wikilink") **R800**은 1990년 [아스키](../Page/아스키_\(기업\).md "wikilink") 사(ASCII Corporation)에서 개발한 [Z80](https://ko.wikipedia.org/wiki/Z80 "wikilink") 호환 16비트 CPU로 [MSX Turbo-R에](https://ko.wikipedia.org/wiki/MSX_Turbo-R "wikilink") 사용되었다.

## 주요 특징

  - 7.16[MHz](https://ko.wikipedia.org/wiki/MHz "wikilink")의 클럭으로 오리지널 [Z80](https://ko.wikipedia.org/wiki/Z80 "wikilink") 3.57[MHz](https://ko.wikipedia.org/wiki/MHz "wikilink")에 비해 2배 향상
  - [Z80](https://ko.wikipedia.org/wiki/Z80 "wikilink") 명령어 호환
      - 16비트 [ALU](https://ko.wikipedia.org/wiki/ALU "wikilink")로 기존 Z80에 비해 연산 속도 향상
      - MULUB(8비트), MULUW (16비트)의 2개의 곱셈 명령어 추가
      - IX, IY [레지스터를](../Page/프로세서_레지스터.md "wikilink") 8비트(IXh, IXl, IYh, IYl)로 사용하는 등의 은폐 명령어를 정식 지원
      - 몇몇 명령어를 최고 1클럭에 실행할 수 있는 등의 고속화.

예를 들어, ADD HL, BC 같이 기존의 11클럭 걸리던 명령어를 1클럭에 실행할 수 있었다.

  - 24비트 주소 버스로 16MB의 메모리 지원([MMU](../Page/메모리_관리_장치.md "wikilink")), 데이터 버스는 이전과 동일한 8비트
      - M1사이클을 폐지하는 등 메모리 접근 사이클을 고속화
      - 주소의 상위 바이트가 바뀌지 않을 때 접근 속도를 빠르게 하는 페이지 주소 모드를 도입

<!-- end list -->

1.  Z80, 사이클 1: 상위 8비트 주소 설정
2.  Z80, 사이클 2: 하위 8비트 주소 설정
3.  Z80, 사이클 3: 대기상태
4.  Z80, 사이클 4: 리프레시, 파트 1
5.  Z80, 사이클 5: 리프레시, 파트 2

위와 같이 [MSX](../Page/MSX.md "wikilink")는 명령어와 데이터를 256×256바이트 블록의 메모리에 배치하여 수행하는데 R800 마지막으로 수행한 상위 8비트의 상태를 저장하였다가 다음 명령이 같은 256바이트 영역을 이용하는 경우 상위 8비트 어드레스를 생략하는 수법으로 사이클을 절약할 수 있다.

  - [DRAM](https://ko.wikipedia.org/wiki/DRAM "wikilink") 인터페이스, 클락 제너레이터를 내장
  - 기존 Z80 인터럽트 모드에 추가로 7개의 인터럽트 모드를 추가했다.
      - Z80 인터럽트 : NMI\#, INT\#
      - 추가된 인터럽트 : NINT1\#\~7
  - [DMA](https://ko.wikipedia.org/wiki/기억_직접_접근 "wikilink") 콘트롤러 내장
      - DMA0과 DMA1의 2개 채널
      - 메모리 대 메모리, 입출력 대 메모리, 메모리 대 입출력, 입출력 대 입출력의 전송 가능
      - 전송 주소는 24비트 리니어 지정 가능
      - [DMA](https://ko.wikipedia.org/wiki/기억_직접_접근 "wikilink") 주소 자동 증가 기능 내장
  - QFP([Quad Flat Package](https://ko.wikipedia.org/wiki/Quad_Flat_Package "wikilink"))패키지 100핀(0.65 mm피치).

## 기타 사항

[MSX turbo-R에서는](https://ko.wikipedia.org/wiki/MSX_turbo-R "wikilink") 기존 [MSX](../Page/MSX.md "wikilink")와 호환성 문제로 DMA, MMU를 사용하지 않았고 어드레스 확장도 뱅크 교환의 메모리 맵핑으로 구현했다. 또한 [MSX2+](https://ko.wikipedia.org/wiki/MSX2+ "wikilink")까지와의 상위 호환성을 위해 추가로 [Z80](https://ko.wikipedia.org/wiki/Z80 "wikilink")을 탑재하였다.

[분류:마이크로프로세서](https://ko.wikipedia.org/wiki/분류:마이크로프로세서 "wikilink") [분류:MSX](https://ko.wikipedia.org/wiki/분류:MSX "wikilink")