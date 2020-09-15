> This article is converted from Wikipedia: [Kon-Boot](https://ko.wikipedia.org/wiki/Kon-Boot).


Kon-Boot는 [Microsoft Windows](https://ko.wikipedia.org/wiki/Microsoft_Windows "wikilink") 및 [Apple macOS](../Page/MacOS.md "wikilink") 로그인 비밀번호 (Linux의 경우, 빈도가 적어 지원 중단 되었다.)를 인증우회할 수 있는 소프트웨어 도구이다. Windows 10 온라인(live), Windows 그리고 macOS 비밀번호를 동시에 지원하는 첫 번째 툴이기도 하다.\[1\]

## 이력

Kon-Boot은 본래 비밀번호를 자주 잊는 사용자들을 위한 프로토타입 보안 프리웨어로서 제작되었다. 프로그램의 메인 컨셉은, 사용자가 정확한 비밀번호를 모르는 상태에서도 로그인을 지원하거나 또는 지속적으로 비밀번호를 변경하지 않아도 되게 하는 목적이었다.

첫 Kon-Boot릴리즈는 2008년, DailyDave 메일링 리스트였다\[2\]. 버전 1.0(프리웨어)는 Linux 기반 운영체제 사용자에 로그인 및 인증프로세스 우회(암호를 몰라도 시스템에 액세스하도록)를 지원하였다.

이후 2009년, 이 소프트웨어의 개발자는 추가적으로 Linux 및 32 비트 Microsoft Windows 시스템용 Kon-Boot를 출시 했다\[3\].

당 버전에서는 Windows Server 2008부터 Windows 7를 포괄하는 전 버전 Windows 운영 체제의 시스템 로그인암호를 우회하는 기능이 추가되었다. 이 버전은 여전히 프리웨어로 제공되고 있다.\[4\]

Kon-Boot 최신 버전만이 상용제품으로 판매되고 있으며\[5\]\[6\]버전은 여전히 유지보수 되고 있다.

현재 버전 (3.1)은 다음 운영체제 시스템의 비밀번호 우회를 지원한다:

| 마이크로소프트 윈도우즈 지원 \[7\]                                                                       |
| ------------------------------------------------------------------------------------------- |
| Microsoft Windows XP                                                                        |
| Microsoft Windows Vista Home Basic 32Bit/64Bit                                              |
| Microsoft Windows Vista Home Premium 32Bit/64Bit                                            |
| Microsoft Windows Vista Business 32Bit/64Bit                                                |
| Microsoft Windows Vista Enterprise 32Bit/64Bit                                              |
| Microsoft Windows Server 2003 Standard 32Bit/64Bit                                          |
| Microsoft Windows Server 2003 Datacenter 32Bit/64Bit                                        |
| Microsoft Windows Server 2003 Enterprise 32Bit/64Bit                                        |
| Microsoft Windows Server 2003 Web Edition 32Bit/64Bit                                       |
| Microsoft Windows Server 2008 Standard 32Bit/64Bit                                          |
| Microsoft Windows Server 2008 Datacenter 32Bit/64Bit                                        |
| Microsoft Windows Server 2008 Enterprise 32Bit/64Bit                                        |
| Microsoft Windows 7 Home Premium 32Bit/64Bit                                                |
| Microsoft Windows 7 Professional 32Bit/64Bit                                                |
| Microsoft Windows 7 Ultimate 32Bit/64Bit                                                    |
| Microsoft Windows 8 and 8.1 all versions (32Bit/64Bit—includes live/online password bypass) |
| Microsoft Windows 10 all versions (32Bit/64Bit—includes live/online password bypass)        |

| 애플 Mac Os 지원\[8\]               |
| ------------------------------- |
| Apple OS X 10.6                 |
| Apple OS X 10.7                 |
| Apple OS X 10.8                 |
| Apple OS X 10.9                 |
| Apple OS X 10.10                |
| Apple OS X 10.11                |
| Apple macOS Sierra (10.12)      |
| Apple macOS High Sierra (10.13) |
| Apple macOS Mojave (10.14)      |

## 테크놀로지

프로그램 Kon-Boot는 BIOS 메모리에 자신을 은폐한다. Kon-Boot는 운영체제가 가동되는 동안 사용자의 인증 데이터 코드를 일시적으로 변경하는 원리로 작동된다\[9\].

CHNTPW\[10\]등의 암호 재설정툴과는 대조적으로, Kon-Boot는 시스템 파일 및 SAM hive를 수정하지 않으며 당 프로그램으로 발생한 수정사항은 일시적인 것으로 시스템 재부팅 시 모두 사라지게 된다.

## 한계 (방어)

Kon-Boot와 같은 툴 자체에 우려가 있는 사용자의 경우, Kon-Boot 프로그램이 디스크 암호화를 우회할 수 없는 점을 감안하여야 한다.

BIOS 암호 및 SecureBoot\[11\] 활성화 역시 좋은 방어책이 될 수 있다.

## 참조

## 외부 링크

  - [공식 웹사이트](https://www.piotrbania.com/all/kon-boot/)

[분류:암호 소프트웨어](https://ko.wikipedia.org/wiki/분류:암호_소프트웨어 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.