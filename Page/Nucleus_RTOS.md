> This article is converted from Wikipedia: [Nucleus RTOS](https://ko.wikipedia.org/wiki/Nucleus_RTOS).


**Nucleus RTOS**(뉴클리어스 RTOS)는 [실시간 운영 체제의](../Page/실시간_운영_체제.md "wikilink") 한 종류이다. [멘토 그래픽스라는](../Page/멘토_그래픽스.md "wikilink") 회사의 [임베디드 시스템](../Page/임베디드_시스템.md "wikilink") 사업부에서 만들었고, 현재 다양한 CPU 플랫폼에서 동작이 가능하다. 또한 **Nucleus RTOS**는 여러가지 구성 요소로 이루어져 있는 전체 임베디드 솔루션의 한 부분이다.

일반적으로 개발은 "호스트"라고 부르는 [마이크로소프트 윈도나](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") [리눅스](../Page/리눅스.md "wikilink") 기계에서 하고 "타겟"의 CPU에 맞게끔 크로스 컴파일을 한다. 실행이나 검사는 실제 "타겟" 보드나 시뮬레이터, [EDGE SimTest](https://ko.wikipedia.org/wiki/EDGE_SimTest "wikilink") 위에서 돌아간다.

**Nucleus RTOS**는 가정용 전자 제품에 주로 사용 되도록 설계되었다. 예를 들면 셋톱 박스, 휴대 전화기나 PMP같은 휴대용 기계등을 말한다. 그리고 **Nucleus RTOS**는 제한된 메모리를 가진 시스템에서 사용 가능하도록 코드와 데이터를 합쳐서 13 KB 정도로 메모리를 줄일 수 있다. 이러한 메모리에 대한 장점 때문에 Nucleus를 많이들 사용한다.

이 운영 체제의 [커널](https://ko.wikipedia.org/wiki/커널 "wikilink")은 삼성의 [바다](../Page/바다.md "wikilink")에도 쓰였다.

## 구성 요소

### 커널

  - 실시간 커널
  - 카운팅 세마포어
  - 정적, 동적 메모리 할당
  - 동적인 태스크 생성과 삭제
  - 응용 프로그램 타이머
  - 태스크 간 통신: 큐, 메일 박스, 파이프, 세마포어, 시그널(유닉스 계열)
  - [C++](https://ko.wikipedia.org/wiki/C++ "wikilink"), [POSIX](../Page/POSIX.md "wikilink") 인터페이스
  - 비공개 소스 (단, Nucleus를 구입한 고객에게는 코드가 공개된다.)
  - 로열티 없음

### 접속성

  - [USB 2.0](https://ko.wikipedia.org/wiki/USB_2.0 "wikilink") 호스트
  - On-The-Go(OTG) 계층 함수
  - 클래스 드라이버
  - 멀티미디어 전송(MTP, PictBridge)
  - [PCI](../Page/PCI_버스.md "wikilink"), [PCI-X](../Page/PCI-X.md "wikilink")
  - [CAN](https://ko.wikipedia.org/wiki/CAN "wikilink"), [CANopen](https://ko.wikipedia.org/wiki/CANopen "wikilink")

### 네트워크

  - [IPv4](../Page/IPv4.md "wikilink"), [IPv6](../Page/IPv6.md "wikilink"), [전송 제어 프로토콜](../Page/전송_제어_프로토콜.md "wikilink")(TCP), [사용자 데이터그램 프로토콜](../Page/사용자_데이터그램_프로토콜.md "wikilink")(UDP), [IEEE 802.11](../Page/IEEE_802.11.md "wikilink"), [WEP](https://ko.wikipedia.org/wiki/WEP "wikilink"), [IEEE 802.11i](https://ko.wikipedia.org/wiki/IEEE_802.11i "wikilink")
  - [RMON](https://ko.wikipedia.org/wiki/RMON "wikilink"), [SNMP](https://ko.wikipedia.org/wiki/SNMP "wikilink") v1, v2, v3
  - [IPsec](https://ko.wikipedia.org/wiki/IPsec "wikilink") & [IKE](https://ko.wikipedia.org/wiki/IKE "wikilink"), [PPTP](https://ko.wikipedia.org/wiki/PPTP "wikilink"), [L2TP](https://ko.wikipedia.org/wiki/L2TP "wikilink")
  - [SSL](https://ko.wikipedia.org/wiki/SSL "wikilink") 2.0 & 3.0, [TLS](https://ko.wikipedia.org/wiki/트랜스포트_레이어_보안 "wikilink") 1.0

### 파일 시스템

  - [FAT](../Page/파일_할당_테이블.md "wikilink") (FAT12, FAT16, FAT32)
  - [ISO 9660](../Page/ISO_9660.md "wikilink") CD-ROM
  - 플래시 파일 시스템
  - [가상 파일 시스템](https://ko.wikipedia.org/wiki/가상_파일_시스템 "wikilink") API

### 그래픽

  - [ANSI C](../Page/ANSI_C.md "wikilink") 호환 소스코드
  - 전 윈도윙 시스템
  - 입력 가능 장치: 키패드, 마우스, 키보드, 터치 패널
  - 트루타입 글꼴과 비트맵 글꼴 사용 가능

### 보안

  - 대칭형 키 암호화 방식(CBC, ECB 방식 둘 다 가능): [DES](../Page/데이터_암호화_표준.md "wikilink"), [3DES](https://ko.wikipedia.org/wiki/3DES "wikilink"), [BLOWFISH](https://ko.wikipedia.org/wiki/BLOWFISH "wikilink"), [CAST-128](https://ko.wikipedia.org/wiki/CAST-128 "wikilink"), [고급 암호 표준](https://ko.wikipedia.org/wiki/고급_암호_표준 "wikilink")(AES)
  - 비대칭형 키 암호화 방식: [RSA](../Page/RSA_암호.md "wikilink")
  - 키 교환 프로토콜: 디피-헬만 키 교환
  - 해시 알고리즘: [MD4](../Page/MD4.md "wikilink"), [MD5](../Page/MD5.md "wikilink"), [SHA-1](https://ko.wikipedia.org/wiki/SHA-1 "wikilink"), [SHA-256](https://ko.wikipedia.org/wiki/SHA-256 "wikilink")
  - 서명 알고리즘: RSA 서명
  - 전자 인증: [X.509](../Page/X.509.md "wikilink")
  - 기타: 유사 난수 생성기, 확률기반 소수 생성기

## 각주

<references />

## 외부 링크

  - [Nucleus RTOS](http://www.mentor.com/products/embedded_software/nucleus_rtos/kernels/index.cfm)

[분류:임베디드 시스템](https://ko.wikipedia.org/wiki/분류:임베디드_시스템 "wikilink") [분류:실시간 운영 체제](https://ko.wikipedia.org/wiki/분류:실시간_운영_체제 "wikilink") [분류:ARM 운영 체제](https://ko.wikipedia.org/wiki/분류:ARM_운영_체제 "wikilink") [분류:MIPS 운영 체제](https://ko.wikipedia.org/wiki/분류:MIPS_운영_체제 "wikilink")