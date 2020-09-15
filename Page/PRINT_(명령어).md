> This article is converted from Wikipedia: [PRINT \(명령어\)](https://ko.wikipedia.org/wiki/PRINT_\(명령어\)).



 [대체글=에](https://ko.wikipedia.org/wiki/파일:RT-11_help.jpg "wikilink") 표시된 [RT-11SJ의](https://ko.wikipedia.org/wiki/:en:RT-11 "wikilink") PRINT 명령에 대한 설명.\]\] **`print`**(프린트)[명령은](../Page/명령어_\(컴퓨팅\).md "wikilink") 다수의 운영 체제에서 단일 사용자의 인쇄 [스풀링](../Page/스풀링.md "wikilink") 기능을 제공한다. [유닉스 시스템 V](https://ko.wikipedia.org/wiki/유닉스_시스템_V "wikilink") [lp](../Page/시스템_V_인쇄_시스템.md "wikilink") 및 [BSD](../Page/BSD.md "wikilink") lpr 인쇄 스풀러 시스템에서 제공하는 것과 대략 유사하다.

## 구현

이 명령은 [DEC](../Page/디지털_이큅먼트_코퍼레이션.md "wikilink") RT-11,\[1\] OS / 8,\[2\] TOPS-10,\[3\] 및 TOPS-20\[4\] 운영 체제 및 [DR](../Page/디지털_리서치.md "wikilink") FlexOS,\[5\] [DR DOS](../Page/DR-DOS.md "wikilink"), TSL PC-MOS,\[6\] Paragon Technology [PTS-DOS](../Page/PTS-DOS.md "wikilink"),\[7\] [IBM](../Page/IBM.md "wikilink") [OS / 2](https://ko.wikipedia.org/wiki/OS/2 "wikilink"),\[8\] [마이크로소프트](../Page/마이크로소프트.md "wikilink") [Windows](../Page/마이크로소프트_윈도우.md "wikilink"), [프리DOS](../Page/프리도스.md "wikilink"),\[9\] Stratus OpenVOS,\[10\] AROS,\[11\] 및 [HP](../Page/휴렛_팩커드.md "wikilink") MPE / iX\[12\]에서 사용할수 있다.

[프리DOS](../Page/프리도스.md "wikilink") 버전은 James Tabor에 의해 개발되었고 [GNU 일반 공중 사용 허가서에](../Page/GNU_일반_공중_사용_허가서.md "wikilink") 따라 라이선스가 부여되었다.\[13\]

### DOS(도스), OS / 2, Windows(윈도우)

#### 배경

이 명령은 [MS-DOS](../Page/MS-DOS.md "wikilink")/[IBM PC DOS](https://ko.wikipedia.org/wiki/IBM_PC_DOS "wikilink") 2.0에 도입되었다.\[14\]\[15\] DR DOS 6.0은 `print` 명령의 구현을 포함한다.\[16\]

[도스](../Page/도스.md "wikilink") 초기 버전에서는 인쇄할 파일을 인쇄 장치를 나타내는 파일([장치파일](../Page/장치_파일.md "wikilink"))에 [`copy`](../Page/Copy_\(명령어\).md "wikilink") (복사) 명령을 사용하여 인쇄를 수행했다.\[17\] 인쇄 작업이 완료되면 사용자에게 제어권이 반환된다.\[18\] DOS 2.0을 시작으로,\[19\] 인쇄가 백그라운드에서 발생한 동안 컴퓨터를 계속 사용할 수 있는 기능, 인쇄할 작업의 대기열을 생성할 수 있는 기능 등 기본적인 인쇄 스풀을 할 수 있도록 인쇄 명령이 포함되었다.\[20\]

#### 묘사

`print` 인쇄 명령은 가능한 많은 로컬 프린터 인터페이스 중 하나를 지정할 수 있도록 허용했으며,\[21\] `net` 명령을 사용하여 네트워크 프린터를 사용할 수 있었다.\[22\] 최대 파일 수와 최대 버퍼 크기를 지정할 수 있으며, 추가 명령줄 옵션을 통해 대기열에서 파일을 추가 및 제거할 수 있다. 여백, 페이지 길이 및 사본 수뿐만 아니라\[23\] 인쇄 속도 대 컴퓨터 응답성 사이에서 조정하기 위한 매개 변수도 설정할 수 있다.

#### 망측량

`print` 명령의 초기 릴리스의 사용자들은 새로 도입된 하위 [디렉토리](../Page/디렉토리.md "wikilink")에 대한 지원 부족뿐만 아니라 인쇄 속도가 느리고 자원 사용량이 높다고 언급했다.\[24\] 이 명령은 최초의 [RAM](../Page/랜덤_액세스_메모리.md "wikilink") 상주 프로그램 중 하나였으며, 많은 사용자가 RAM 상주 프로그램을 어떻게 작성해야 하는지를 결정하기 위해 바이너리를 분해하는 등 널리 사용되는 첫 번째 프로그램이었다.\[25\]

## 같이 보기

  - [도스 명령 목록](../Page/도스_명령어_목록.md "wikilink")
  - [유닉스 명령어 목록](../Page/유닉스_명령어_목록.md "wikilink")

## 각주

## 추가 자료

  -
  -
  -
## 외부 링크

  - [인쇄 | Mic](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/print)[rosoft 문서](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/print)
  - [MS-DOS v2.0과 함께 제공되는 오픈 소스 PRINT 구현](https://github.com/microsoft/MS-DOS/blob/master/v2.0/source/PRINT.ASM)

[분류:윈도우 관리](https://ko.wikipedia.org/wiki/분류:윈도우_관리 "wikilink") [분류:윈도우 명령어](https://ko.wikipedia.org/wiki/분류:윈도우_명령어 "wikilink") [분류:OS/2 명령어](https://ko.wikipedia.org/wiki/분류:OS/2_명령어 "wikilink") [분류:외부 도스 명령어](https://ko.wikipedia.org/wiki/분류:외부_도스_명령어 "wikilink")

1.  <http://paleoferrosaurus.com/beta/documents/rt11help.html#PRINT>
2.  "Concise Command Language" (CCL).
3.
4.
5.  <http://www.bitsavers.org/pdf/digitalResearch/flexos/1073-2003_FlexOS_Users_Guide_V1.3_Nov86.pdf>
6.  [PC-MOS User Guide](https://github.com/roelandjansen/pcmos386v501/blob/master/DOCS/v4/PCMOSv4UserManual.pdf)
7.
8.
9.  <http://www.ibiblio.org/pub/micro/pc-stuff/freedos/files/distributions/1.2/repos/pkg-html/group-base.html>
10. <http://stratadoc.stratus.com/vos/19.1.0/r098-19/wwhelp/wwhimpl/common/html/r098-19.pdf>
11. <http://aros.sourceforge.net/documentation/users/shell/index.php>
12. [MPE/iX Command Reference Manual](http://www.teamnaconsulting.com/compresources/pdfs/c01687363.pdf)
13. <http://www.ibiblio.org/pub/micro/pc-stuff/freedos/files/distributions/1.2/repos/pkg-html/print.html>
14. <cite class="citation web">[Paterson, Tim](https://ko.wikipedia.org/wiki/Tim_Paterson "wikilink") (19 December 2013) \[1983\]. ["Microsoft DOS V1.1 and V2.0: /msdos/v20source/PRINT.ASM"](http://www.computerhistory.org/atchm/microsoft-research-license-agreement-msdos-v1-1-v2-0/). [Computer History Museum](https://ko.wikipedia.org/wiki/Computer_History_Museum "wikilink"), [Microsoft](https://ko.wikipedia.org/wiki/Microsoft "wikilink")<span class="reference-accessdate">. Retrieved <span class="nowrap">1 October</span> 2015</span>.</cite><templatestyles src="Module:Citation/CS1/styles.css"></templatestyles>
15. <cite class="citation web">Shustek, Len (24 March 2014). ["Microsoft MS-DOS early source code"](http://www.computerhistory.org/atchm/microsoft-ms-dos-early-source-code/). Software Gems: The Computer History Museum Historical Source Code Series<span class="reference-accessdate">. Retrieved <span class="nowrap">1 October</span> 2015</span>.</cite><templatestyles src="Module:Citation/CS1/styles.css"></templatestyles>
16.
17. <cite class="citation news">Dickinson, John (11 November 1986). ["Mastering Your Printer's Options"](https://books.google.com/books?id=VomWiyJuttsC&pg=PA363). *PC Magazine*. p. 363.</cite><templatestyles src="Module:Citation/CS1/styles.css"></templatestyles>
18. <cite class="citation news">Rubenking, Neil J. (29 June 1993). ["Moving PRINT.COM"](https://books.google.com/books?id=gCfzPMoPJWgC&pg=RA1-PA299). *PC Magazine*.</cite><templatestyles src="Module:Citation/CS1/styles.css"></templatestyles>
19. <cite class="citation news">Norton, Peter (July 1983). ["The Dark Side of PC-DOS 2.0"](https://books.google.com/books?id=V2588uIxmAQC&pg=PA290). *PC Magazine*. p. 290.</cite><templatestyles src="Module:Citation/CS1/styles.css"></templatestyles>
20. <cite class="citation book">Cooper, Jim (2002). [*Using MS-DOS 6.22*](https://books.google.com/books?id=u7oN-5y7nGsC&pg=PA324) (3rd ed.). Que. pp. 322–325. [ISBN](https://ko.wikipedia.org/wiki/International_Standard_Book_Number "wikilink") [<bdi>0-7897-2573-8</bdi>](https://ko.wikipedia.org/wiki/Special:BookSources/0-7897-2573-8 "wikilink").</cite><templatestyles src="Module:Citation/CS1/styles.css"></templatestyles>
21. <cite class="citation book">Cooper, Jim (2002). [*Using MS-DOS 6.22*](https://books.google.com/books?id=u7oN-5y7nGsC&pg=PA324) (3rd ed.). Que. pp. 322–325. [ISBN](https://ko.wikipedia.org/wiki/International_Standard_Book_Number "wikilink") [<bdi>0-7897-2573-8</bdi>](https://ko.wikipedia.org/wiki/Special:BookSources/0-7897-2573-8 "wikilink").</cite><templatestyles src="Module:Citation/CS1/styles.css"></templatestyles>
22. <cite class="citation book">Ivens, Kathy (2005). "Network Printing and MS-DOS". *Home Networking Annoyances*. O'Reilly. p. 117–118. [ISBN](https://ko.wikipedia.org/wiki/International_Standard_Book_Number "wikilink") [<bdi>0-596-00808-2</bdi>](https://ko.wikipedia.org/wiki/Special:BookSources/0-596-00808-2 "wikilink").</cite><templatestyles src="Module:Citation/CS1/styles.css"></templatestyles>
23. <cite class="citation book">[*Using the Xerox 9700 Page Printer*](https://books.google.com/books?id=qIJQAAAAMAAJ&pg=RA7-PA36). Memo 800. University of Michigan Computing Center. September 1988. p. 37.</cite><templatestyles src="Module:Citation/CS1/styles.css"></templatestyles>
24. <cite class="citation news">Norton, Peter (July 1983). ["The Dark Side of PC-DOS 2.0"](https://books.google.com/books?id=V2588uIxmAQC&pg=PA290). *PC Magazine*. p. 290.</cite><templatestyles src="Module:Citation/CS1/styles.css"></templatestyles>
25. <cite class="citation news">Rubenking, Neil J. (29 June 1993). ["Moving PRINT.COM"](https://books.google.com/books?id=gCfzPMoPJWgC&pg=RA1-PA299). *PC Magazine*.</cite><templatestyles src="Module:Citation/CS1/styles.css"></templatestyles>