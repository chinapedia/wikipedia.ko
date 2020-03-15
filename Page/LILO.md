> This article is converted from Wikipedia: [LILO](https://ko.wikipedia.org/wiki/LILO).


**LILO** (**LI**nux **LO**ader, 리눅스 로더)는 [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink")를 위한 [부트 로더이다](https://ko.wikipedia.org/wiki/부트_로더 "wikilink").

LILO는 처음에 Werner Almesberger가 개발하였으나, 현재의 개발자는 존 코프먼(John Coffman)이다.

LILO는 특정한 [파일 시스템에](https://ko.wikipedia.org/wiki/파일_시스템 "wikilink") 의지하지 않으며, [플로피 디스크와](https://ko.wikipedia.org/wiki/플로피_디스크 "wikilink") [하드 디스크](https://ko.wikipedia.org/wiki/하드_디스크 "wikilink")(이를테면 [리눅스](../Page/리눅스_커널.md "wikilink") [커널](https://ko.wikipedia.org/wiki/커널_\(컴퓨팅\) "wikilink"))로부터 [운영 체제를](https://ko.wikipedia.org/wiki/운영_체제 "wikilink") 시동할 수 있다. 최대 16개의 다른 이미지를 시동 메뉴 안에서 고를 수 있다. 루트 장치와 같은 여러 변수는 각 커널에 독립적으로 설정할 수 있다. LILO는 [마스터 부트 레코드](https://ko.wikipedia.org/wiki/마스터_부트_레코드 "wikilink") (MBR)이나 파티션의 시동 섹터 안에 위치한다. 후자의 경우 다른 무언가가 LILO를 불러오기 위해 MBR 안에 위치해야 한다.

시스템이 시작할 때, LILO가 하드 드라이브에 접근하도록 하기 위해 [바이오스](https://ko.wikipedia.org/wiki/바이오스 "wikilink") [드라이버만](../Page/장치_드라이버.md "wikilink") 사용할 수 있다. 이러한 까닭에, 매우 오래된 바이오스들의 경우, 접근할 수 있는 영역이 처음 두 개의 하드 디스크의 [실린더 0부터 1023까지](https://ko.wikipedia.org/wiki/실린더_1024 "wikilink") 한정되어 있다. 나중에 나온 바이오스들의 경우, LILO는 32비트 [논리 주소 어드레싱](https://ko.wikipedia.org/wiki/논리_주소_어드레싱 "wikilink") (LBA)을 사용하여 바이오스가 접근하는 모든 하드 디스크의 자료를 실용적으로 접근한다.

LILO는 [loadlin](https://ko.wikipedia.org/wiki/loadlin "wikilink")이 대중화된 뒤 여러 해 동안 대부분의 [리눅스 배포판을](https://ko.wikipedia.org/wiki/리눅스_배포판 "wikilink") 위한 기본 부트로더였다. 오늘날 대부분의 배포판들은 [GRUB](../Page/GRUB.md "wikilink")을 기본 부트로더로 사용한다.

## lilo.conf

lilo.conf 파일은 보통 /etc/lilo.conf에 위치해 있다. lilo.conf 안에는, 두 개의 종류가 있다.

1.  첫 번째 섹션: 전역 옵션을 정의하며, 시동 위치 특성을 지정하는 변수를 포함한다.
2.  두 번째 섹션: 불러올 운영 체제 이미지와 연결된 변수를 포함한다. 이 섹션 종류는 최대 16개의 다른 시동 선택으로 되풀이될 수 있다.

기본 정보는 [LILO](http://www.netadmintools.com/html/5lilo.conf.man.html) [Manpage](https://ko.wikipedia.org/wiki/Manpage "wikilink")에서 찾을 수 있다.

## 같이 보기

  - [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink")
  - [부트 로더](https://ko.wikipedia.org/wiki/부트_로더 "wikilink")
  - [GNU GRUB](https://ko.wikipedia.org/wiki/GNU_GRUB "wikilink")
  - [elilo](https://ko.wikipedia.org/wiki/elilo "wikilink")
  - [NTLDR](../Page/NTLDR.md "wikilink")

## 외부 링크

  - [공식 웹사이트 (사용자, 기술의 길잡이 포함)](http://lilo.go.dyndns.org/)
  - [LILO (freshmeat)](http://freshmeat.net/projects/lilo/)
  - [LILO 설치 안내](https://web.archive.org/web/19970507092324/http://www.acm.uiuc.edu/workshops/linux_install/lilo.html)
  - [LILO mini-HOWTO](http://www.tldp.org/HOWTO/LILO.html)
  - [LILO 오류 메시지](https://web.archive.org/web/20040805053352/http://sdb.suse.de/sdb/en/html/kgw_lilo_errmsg.html)

[분류:운영 체제 기술](https://ko.wikipedia.org/wiki/분류:운영_체제_기술 "wikilink")