> This article is converted from Wikipedia: [HPLIP](https://ko.wikipedia.org/wiki/HPLIP).


HP([휴렛 패커드社](https://ko.wikipedia.org/wiki/휴렛_패커드 "wikilink"))가 주도하는 **HPLIP**(HP Linux Imaging and Printing)프로젝트는 완전한 인쇄, 스캔 및 팩스 지원을 통해 HP의 잉크젯 및 레이저 프린터와 상호 작용하는 [리눅스](../Page/리눅스.md "wikilink")(Linux)시스템의 능력을 향상시키는 것을 목표로 한다. 2019년 기준으로 공급되는 프린터 드라이버는 총 2,867개의 HP프린터 모델을 지원한다.\[1\] 저가형 모델의 경우 대부분이 [FOSS](https://ko.wikipedia.org/wiki/FOSS "wikilink")(FreeandOpenSource), [MIT](https://ko.wikipedia.org/wiki/MIT "wikilink"), [BSD](../Page/BSD.md "wikilink"), [GPL](https://ko.wikipedia.org/wiki/GPL "wikilink")라이센스로 라이센스가 부여되어 있지만, 다른 모델(시장에 출시된 모든 컬러 레이저 MFC프린터 포함)에는 전용 바이너리('플러그 인')가 필요하다. 이 프로젝트는 HPLIP가 [CUPS](../Page/CUPS.md "wikilink")(CommonUNIXPrintingSystem)및 [SANE](https://ko.wikipedia.org/wiki/SANE "wikilink")과 함께 작동하여 각각 인쇄와 스캔을 수행하도록 지원한다. HP OfficeJet의 프린터를 Linux와 함께 실행하도록 하는 HP OfficeJet Linux드라이버는 HPLIP의 등장으로 2006년 3월 13일 현재 개발이 중단되었으며 이후 지속적인 지원은 HPLIP에서 진행하고 있다.\[2\]\[3\]\[4\]

## HP 디바이스 메니저

HPLIP에 포함되는 HP 디바이스 메니저(HP Device Manager)는 프린터 설정등 관련 서비스를 지원한다. 또한 HPLIP는 HP 디바이스 메니저(HP Device Manager)뿐만아니라 터미널을 통해 손쉽게 작동하는 'hp-setup' 명령을 통해 GUI환경을 추가 지원한다.\[5\]\[6\] 한편 HPLIP와의 안정된 호환성을 보여주는 리눅스용 스캔프로그램인 [심플스캔](https://ko.wikipedia.org/wiki/심플스캔 "wikilink")(Simple Scan)은 [pdf를](../Page/PDF.md "wikilink") 기본으로 지원하고있다.

## hp-setup

터미널에서 'hp-setup' 명령은 GUI환경으로 설정등의 작동을 수행한다. 한편

`> hp-setup --help`

를 통해서 터미널 모드에서도 전문가 수준의 설정을 지원할수있도록 설계되어있다. 이를 통해서 복구,진단, 재설정등 다양한 기능을 확인할수있다.<ref>HP Linux Imaging and Printing System (ver. 3.19.12) Printer/Fax Setup Utility ver. 9.0

Copyright (c) 2001-18 HP Development Company, LP This software comes with ABSOLUTELY NO WARRANTY. This is free software, and you are welcome to distribute it under certain conditions. See COPYING file for more details.

`(Ubuntu 18LTS 2020.06.09)`</ref>

## HPLIP 프린터 테스트 페이지

|                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------- |
| [600px](https://ko.wikipedia.org/wiki/파일:HPLIPPrintertestPage001.pdf "wikilink")                                                              |
| [심플스캔](https://ko.wikipedia.org/wiki/심플스캔 "wikilink")에서 스캔한 'HPLIP 프린터 테스트 페이지'(HPLIP Printer Test Page)의 [PDF](../Page/PDF.md "wikilink") 파일 |

HPLIP 프린터 테스트 페이지(HPLIP Printer Test Page)는 설정을 위한 이미지에대한 다양한 정보뿐만아니라 기본적인 개인정보(시리얼넘버,로컬IP등)도 포함하고있다.

## 같이 보기

  - [장치 드라이버](../Page/장치_드라이버.md "wikilink")

## 참고

## 외부 링크

  - [HP Linux Imaging and Printing](https://hp.io/hplip) resources on the [HP Developer Portal](https://hp.io)
  - [HPLIP at SourceForge](https://sourceforge.net/projects/hplip/)

[분류:장치 드라이버](https://ko.wikipedia.org/wiki/분류:장치_드라이버 "wikilink") [분류:리눅스 소프트웨어](https://ko.wikipedia.org/wiki/분류:리눅스_소프트웨어 "wikilink")

1.
2.  ([HPLIP](https://ko.wikipedia.org/wiki/HPLIP "wikilink"), [HP Developers - Software and drivers for HP Officejet Pro 8600 e-All-in-One Printer - N911a](https://support.hp.com/us-en/drivers/selfservice/hp-officejet-pro-8600-e-all-in-one-printer-series-n911/4322914/model/4323658)
3.  [Download the Automatic Installer (.run file) Download HPLIP 3.19.12](https://developers.hp.com/hp-linux-imaging-and-printing/install/install/index)
4.  [HP Officejet Pro 8600(HPLIP) 다운로드](https://developers.hp.com/hp-linux-imaging-and-printing/gethplip)
5.  [우분투에서 APT로 인스톨하기](https://www.cyberciti.biz/faq/how-to-install-networked-hp-printer-and-scanner-on-ubuntu-linux/)
6.  HP Linux Imaging and Printing System (ver. 3.19.12) Printer/Fax Setup Utility ver. 9.0 Copyright (c) 2001-18 HP Development Company, LP This software comes with ABSOLUTELY NO WARRANTY. This is free software, and you are welcome to distribute it under certain conditions. See COPYING file for more details.