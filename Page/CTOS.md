> This article is converted from Wikipedia: [CTOS](https://ko.wikipedia.org/wiki/CTOS).


[섬네일](https://ko.wikipedia.org/wiki/파일:CTOS-B25.JPG "wikilink") **CTOS**(Convergent Technologies Operating System) 또는 **BTOS**, **STARSYS**는 모듈 방식의 [메시지 전달](https://ko.wikipedia.org/wiki/메시지_전달 "wikilink"), 멀티프로세스 기반 [운영 체제이다](../Page/운영_체제.md "wikilink").

## 개요

CTOS는 당시 수많은 혁신 기능이 포함되었다. 시스템 접근은 사용자 비밀번호와 볼륨, 또는 디스크 비밀번호로 통제되었다. 이를테면 볼륨에 대해 누군가가 비밀번호를 알고 있으면 해당 볼륨(하드 디스크)의 파일이나 디렉터리에 접근이 가능했다. 각 볼륨과 디렉터리는 식별을 위해 구분자(delimiter)로 참조되었으며 {Network Node}\[VolumeName\]<DirectoryName>FileName과 같은 방식으로 동작에 따라 파일명이 뒷따랐다.

기능의 추가/제거를 위해 운영 체제를 커스텀-링크(custom-link)하는 것도 가능했다.

CTOS는 직렬 [RS-422](../Page/RS-422.md "wikilink") 케이블(데이지 체인 토폴로지)을 통해 전달되는 투명한 P2P 네트워크를 지원했으며 나중 버전에서는 RS-422 어댑터와 함께 트위스티드 페어(스타 토폴로지)로 전달되었다. 각 워크그룹(클러스터)은 서버(마스터)에 연결되었다. 보통 [디스크리스](https://ko.wikipedia.org/wiki/디스크리스_워크스테이션 "wikilink") 형태인 워크스테이션은 마스터로부터 [클러스터 네트워크를 경유한 부팅이](https://ko.wikipedia.org/wiki/네트워크_부팅 "wikilink") 수행되었고 부착된 하드 드라이브를 통해 로컬에서 부팅이 선택적으로 가능하였다.

메시지의 요청과 응답의 경우 [프로세스 간 통신](../Page/프로세스_간_통신.md "wikilink")(IPC)이 주로 사용되었으며 이는 내부, 외부 환경을 위한 서비스 간 엔터프라이즈 애플리케이션 통합(Enterprise Application Integration)을 강화시켰다. 그러므로 CTOS는 메시지 기반 [마이크로커널](../Page/마이크로커널.md "wikilink") 아키텍처로 잘 알려져 있다.

CTOS는 [인텔](../Page/인텔.md "wikilink") [x86](https://ko.wikipedia.org/wiki/x86 "wikilink") 컴퓨터에서 실행되었으며 [유니시스](../Page/유니시스.md "wikilink") PC에서 [윈도우 NT와](../Page/윈도우_NT.md "wikilink") 동시에 실행이 가능했다.

시스템 API는 고급 언어와 어셈블리어로 표현되었다.

## 참고문헌

  -
## 외부 링크

  - [The CTOS FAQ October 1999](https://web.archive.org/web/20110708212436/http://www.ctosfaq.com/CtosFaqOct1999.htm)
  - [CTOS Revealed, Byte, December 1994](https://web.archive.org/web/20080828190425/http://www.byte.com/art/9412/sec13/art2.htm)
  - [Paul Mooney's CTOS Central](http://www.angelfire.com/ga/paulmooney/ctos.html)
  - [The CTOS FAQ Picture Archive](https://web.archive.org/web/20111020190645/http://www.ctosfaq.com/CTOSPictures.htm)
  - [Exhuming CTOS: The Convergent Technologies Project, Nadia Ilyin](http://www.softwarepreservation.org/meetings/2006/2006-05-17/CTOS_Intro_2006_05_17.pdf)
  - [Convergent archive](http://bitsavers.org/pdf/convergent) at bitsavers.org

[분류:유니시스 운영 체제](https://ko.wikipedia.org/wiki/분류:유니시스_운영_체제 "wikilink")