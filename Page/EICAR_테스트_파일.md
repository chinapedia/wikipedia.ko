> This article is converted from Wikipedia: [EICAR 테스트 파일](https://ko.wikipedia.org/wiki/EICAR_테스트_파일).


**EICAR Anti-Virus Test File**\[1\] 또는 **EICAR test file**(EICAR 테스트 파일)은 [European Institute for Computer Antivirus Research](../Page/EICAR.md "wikilink")(EICAR)와 [Computer Antivirus Research Organization](https://ko.wikipedia.org/wiki/CARO "wikilink")(CARO)에서 개발된 컴퓨터 파일이다. 이 프로그램은 [안티바이러스](https://ko.wikipedia.org/wiki/안티바이러스 "wikilink") 소프트웨어를 테스트하기 위해 제작되었다.\[2\] 실제로 컴퓨터에 피해를 줄 수 있는 바이러스 파일을 사용하는 대신 이 테스트 파일을 사용하면 안전하게 백신 프로그램을 테스트할 수 있다.\[3\]

안티바이러스 프로그래머는 EICAR 테스트 파일을 이미 식별된 다른 서명들과 유사하게 하여 verified 바이러스처럼 만든다. EICAR 테스트 파일이 호환되는 바이러스 스캐너는 이 파일을 탐지할 때 컴퓨터 바이러스를 감지한 것과 동일하게 응답한다. 그러나 일부 바이러스 스캐너는 올바르게 구성되었음에도 EICAR 테스트 파일을 바이러스로 감지하지 않는다. 파일이 감지되는 방식과 the wording with which it is flagged는 표준화되지 않았으며, 실제 멀웨어가 flagged 하는 방식과 다를 수 있으나, [EICAR](../Page/EICAR.md "wikilink")가 지정한 엄격한 사양을 충족하는 한 실행되지 않아야 한다.\[4\]

EICAR 테스트 파일의 사용은 간단한 바이러스 탐지뿐만 아니라 EICAR 테스트 파일이 포함된 파일은 압축되거나 보관될 수 있으며, 안티바이러스 소프트웨어를 실행하여 압축된 파일에서 EICAR 테스트 파일를 탐지할 수 있는지 확인하여 프로그램이 바이러스를 탐지할 수 있는지 확인하는 데에 사용되기도 한다. 대부분의 [AMTSO](https://ko.wikipedia.org/wiki/AMTSO "wikilink") Feature Settings Checks은\[5\] EICAR 테스트 파일을 기반으로 한다.\[6\]

## 만드는 방법

EICAR 테스트 파일은 68바이트에서 128바이트 크기의 [TXT](https://ko.wikipedia.org/wiki/TXT "wikilink") 파일이다.\[7\] 이 파일은 [MS-DOS](../Page/MS-DOS.md "wikilink")와 그 후속 운영체제인 [OS/2](https://ko.wikipedia.org/wiki/OS/2 "wikilink") 그리고 [Windows](https://ko.wikipedia.org/wiki/Windows "wikilink")에서 실행할 수 있는 [COM 파일이다](../Page/COM_파일.md "wikilink")(16비트 제한으로 인한 64비트 제외). 이 파일을 실행시키면 EICAR 테스트 파일이 "EICAR-STANDARD-ANTIVIRUS-TEST-FILE\!"를 표시하고 멈출 것이다. 테스트 문자열은 사람이 읽기 편하도록 [아스키](https://ko.wikipedia.org/wiki/아스키 "wikilink") 문자로 구성되어 있으며, 일반적인 [컴퓨터 키보드로](https://ko.wikipedia.org/wiki/컴퓨터_키보드 "wikilink") 쉽게 작성할 수 있다. It makes use of [self-modifying code](https://ko.wikipedia.org/wiki/self-modifying_code "wikilink") to work around technical issues that this constraint imposes on the execution of the test string.

EICAR 테스트 문자열은\[8\] 다음과 같다:\[9\]

`X5O!P%@AP[4\PZX54(P^)7CC)7}$EICAR-STANDARD-ANTIVIRUS-TEST-FILE!$H+H*`

## 같이 보기

  - [EICAR](../Page/EICAR.md "wikilink")
  - [GTUBE](https://ko.wikipedia.org/wiki/GTUBE "wikilink")  – 원하지 않는 대량 전자 메일에 대한 테스트 ([스팸 메일](https://ko.wikipedia.org/wiki/스팸_메일 "wikilink"))

## 각주

## 외부 링크

  - [Official Site of the European Institute For Computer Antivirus Research](http://www.eicar.org) (also known as the European Expert Group for IT-Security)
  - [Assembly-language analysis of the EICAR test file](http://thestarman.pcministry.com/asm/eicar/eicarcom.html)
  - [Antivirus results from scanning the EICAR file](https://www.virustotal.com/en/file/275a021bbfb6489e54d471899f7db9d1663fc695ec2fe2a2c4538aabf651fd0f/analysis/1425909746/)
  - [AMTSO guidelines on the use and misuse of test files in security product testing, including simulators, the EICAR string, CloudCar, and Spycar.](https://web.archive.org/web/20170816151919/http://amtso.org/download/amtso-use-and-misuse-of-test-files/?wpdmdl=1132)

[분류:보안 소프트웨어](https://ko.wikipedia.org/wiki/분류:보안_소프트웨어 "wikilink")

1.
2.
3.   ZDNet|last=Hess|first=Ken|work=ZDNet|access-date=2017-04-17|language=en}}
4.
5.  <http://amtso.org/security-features-check/>
6.  <http://amtso.org/feature-settings-check-for-desktop-solutions/>
7.  [Eddy Willems, “The Winds of Change: Updates to the EICAR Test File”, Virus Bulletin June 2003](https://www.virusbtn.com/pdf/magazine/2003/200306.pdf)
8.  <https://secure.eicar.org/eicar.com.txt>
9.   Virus Profile & Definition {{\!}} McAfee Inc.|website=home.mcafee.com|language=en|access-date=2017-04-17}}