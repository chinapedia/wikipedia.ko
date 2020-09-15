> This article is converted from Wikipedia: [Ntdetect.com](https://ko.wikipedia.org/wiki/Ntdetect.com).


**ntdetect.com**은 [x86](https://ko.wikipedia.org/wiki/x86 "wikilink") 아키텍처를 운영하는 [마이크로소프트](../Page/마이크로소프트.md "wikilink") [윈도 NT](https://ko.wikipedia.org/wiki/윈도_NT "wikilink") [운영 체제의](../Page/운영_체제.md "wikilink") 구성 요소이다. [윈도 NT 시작 프로세스](https://ko.wikipedia.org/wiki/윈도_NT_시작_프로세스 "wikilink") 동안에 실행되며 운영 체제를 시작하는 데 요구되는 기본 하드웨어를 감지한다.

## 들어가며

ntdetect.com은 [NTLDR](../Page/NTLDR.md "wikilink")에 의해 호출되고 작업이 끝나면 윈도 커널 [ntoskrnl.exe](https://ko.wikipedia.org/wiki/ntoskrnl.exe "wikilink")에 전달하기 위해 해당 정보를 NTLDR에게 되돌려 준다.

ntdetect.com은 [바이오스](../Page/바이오스.md "wikilink") 펌웨어를 사용하는 컴퓨터에서 돌아간다. [IA-64](https://ko.wikipedia.org/wiki/IA-64 "wikilink")와 같은 [확장 펌웨어 인터페이스를](https://ko.wikipedia.org/wiki/확장_펌웨어_인터페이스 "wikilink") 사용하는 컴퓨터들은 운영 체제에 구속되지 않는 장치 검색 방식을 사용한다.

하드웨어 감지는 하드웨어의 [ACPI](../Page/ACPI.md "wikilink") 지원 여부에 따라 조금 다르게 동작한다. ACPI를 지원하면, 발견된 장치들의 목록은 커널에 맡겨지고, 윈도는 각 장치의 일부 리소스를 할당한다. ACPI를 지원하지 않는 오래된 하드웨어를 사용하면 운영 체제가 아닌 [바이오스](../Page/바이오스.md "wikilink")가 리소스를 직접 할당하며, 이때 정보는 커널에도 전달된다.

또한, ntdetect.com은 어느 하드웨어 프로파일을 사용할지 결정한다. 윈도는 여러 개의 하드웨어 프로파일을 구분하여 단일 복사본의 윈도가 기본 설계 상의 하드웨어가 변경되어도 잘 동작하게 만들어 준다. 이는 [도킹 스테이션에](https://ko.wikipedia.org/wiki/도킹_스테이션 "wikilink") 연결하는 휴대용 컴퓨터와 같다.

[윈도 비스타](https://ko.wikipedia.org/wiki/윈도_비스타 "wikilink") 이후의 운영체제에서는 ntdetect.com는 오직 ACPI만 지원하며, 윈도는 모든 컴퓨터의 하드웨어 리소스 할당을 동일한 방법으로 제어할 수 있다. 하드웨어 프로파일들은 더 이상 윈도 비스타에서 지원되지 않는다.

ntdetect.com이 수집한 정보는 시동 작업이 끝나갈 무렵 [윈도 레지스트리의](https://ko.wikipedia.org/wiki/윈도_레지스트리 "wikilink") `HKLM\HARDWARE\DESCRIPTION` 키에 저장된다.

## 하드웨어 감지 종류

  - 하드웨어 인식
  - 하드웨어 날짜 및 시간
  - 버스 및 어댑터 종류
  - [스커지](https://ko.wikipedia.org/wiki/스커지 "wikilink") 어댑터
  - 비디오 어댑터
  - 키보드
  - 직렵 및 병렬 통신 포트
  - 하드 드라이브
  - 플로피 디스크
  - 마우스
  - [부동소수점](../Page/부동소수점.md "wikilink") [코프로세서](../Page/코프로세서.md "wikilink")
  - [ISA 버스](../Page/ISA_버스.md "wikilink") 기반의 장치

## 문제 해결

문제가 있다면 마이크로소프트의 ntdetect.com의 디버그 버전을 내려 받으면 된다. 감지되는 하드웨어에 대해 자세한 정보를 보여 준다.

## 같이 보기

  - [윈도 NT 시작 프로세스](https://ko.wikipedia.org/wiki/윈도_NT_시작_프로세스 "wikilink")
  - [NTLDR](../Page/NTLDR.md "wikilink")
  - [ntoskrnl.exe](https://ko.wikipedia.org/wiki/ntoskrnl.exe "wikilink")
  - [ACPI](../Page/ACPI.md "wikilink")

## 외부 링크

  - [Download of ntdetect.chk for Windows 2000](https://web.archive.org/web/20060109212835/http://www.microsoft.com/windows2000/techinfo/reskit/tools/existing/ntdetect-o.asp)
  - [Windows XP SP2 Support Tools](http://www.microsoft.com/downloads/details.aspx?FamilyId=49AE8576-9BB9-4126-9761-BA8011FABF38&displaylang=en) includes ntdetect.chk for [Windows XP](https://ko.wikipedia.org/wiki/Windows_XP "wikilink").
  - [Troubleshooting Windows NT Boot Failures](https://web.archive.org/web/20081004142126/http://www.windowsitlibrary.com/Content/169/01/31.html)

[분류:윈도우 구성 요소](https://ko.wikipedia.org/wiki/분류:윈도우_구성_요소 "wikilink")