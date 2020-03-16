> This article is converted from Wikipedia: [Nmap](https://ko.wikipedia.org/wiki/Nmap).


**Nmap**(network mapper)은 원래 [고든 라이온](https://ko.wikipedia.org/wiki/고든_라이온 "wikilink")(Gordon Lyon)이 작성한 보안 스캐너이다. 이것은 컴퓨터와 서비스를 찾을 때 쓰이며, 네트워크 "지도"를 함께 만든다. 다른 간단한 포트 스캐너들처럼, Nmap은 서비스 탐지 프로토콜로 자신을 광고하지 않는 수동적인 서비스들도 찾아낼 수 있다. 게다가 Nmap은 원격 컴퓨터들의 자세한 정보를 알아낼 수 있다. 이 상세 정보에는 운영 체제, 장치 종류, 운영 시간, 서비스에 쓰이는 소프트웨어 제품, 그 제품의 정확한 버전, 방화벽 기술의 존재와 심지어 근거리 네트워크에서 네트워크 카드의 공급자도 포함한다.

Nmap은 [리눅스](../Page/리눅스.md "wikilink"), [윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink"), [솔라리스와](../Page/솔라리스_\(운영_체제\).md "wikilink") [맥 OS X를](https://ko.wikipedia.org/wiki/맥_OS_X "wikilink") 포함한 [BSD](../Page/BSD.md "wikilink"), [AmigaOS](https://ko.wikipedia.org/wiki/AmigaOS "wikilink") 에서 실행된다. [리눅스](../Page/리눅스.md "wikilink")가 가장 자주 사용하는 nmap 플랫폼이며, 윈도가 그 두 번째이다.

## 기능

  - 호스트 탐지 - 네트워크상의 컴퓨터들을 확인한다. 예를 들어 ping 응답이나 특정 포트가 열린 컴퓨터들을 나열한다.
  - [포트 스캔](../Page/포트_스캔.md "wikilink") - 하나 혹은 그 이상의 대상 컴퓨터들에 열린 포트들을 나열한다.
  - 버전 탐지 - 응용 프로그램의 이름과 버전 번호를 확인하기 위해 원격 컴퓨터의 네트워크 서비스에 주의를 기울인다.
  - [운영 체제](../Page/운영_체제.md "wikilink") 탐지 - 원격으로 운영 체제와 네트워크 장치의 하드웨어 특성을 확인한다.

## 그래픽 인터페이스

그래픽 인터페이스는 **NmapFE**, *Zach Smith*가 작성하였으며, Nmap 2.2부터 4.22까지 공식 GUI였다. Nmap 4.5(원래는 4.22SOC 개발시리즈)부터 NmapFE는 *Adriano Monteiro Marques*가 개발한 **UMIT**를 기반으로 둔 새로운 GUI **Zenmap**으로 대체되었다.

웹 브라우저에서 Nmap을 제어할 수 있는 다양한 웹 기반의 인터페이스 역시 사용가능하다. LOCALSCAN, nmap-web, Nmap-CGI등이 있다.

[윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 기반의 GUI도 존재한다. NMapWin은 2003년 6월에 공개되었으나 v1.40부터 업데이트되지 않고 않으며, Syhunt가 작성한 NmapW도 있다.

파일:Zenmap.png|*Zenmap*, 위키백과에 대한 포트스캔 결과를 보여주고있다. 파일:Nmapfe_screenshot.png|*NmapFE*, 위키백과에 대한 포트스캔 결과를 보여주고있다. 파일:Xnmap.png|*XNmap*, Mac OS X GUI.

## Nmap에서 사용하는 모듈과 라이브러리

Nmap에서 선호되는 출력 포맷은 XML이다. 사용자 스크립트에 의해 분석하고, 곧바로 정보를 제공하는 편리한 인터프리트 언어이기 때문이다.

## 역사

Nmap은 1997년 9월에 [Phrack](https://ko.wikipedia.org/wiki/Phrack "wikilink")지의 기사로 처음 출시되었다. 어떤 서비스가 동작하고 있는지 결정할 수 있는 더 좋은 알고리즘을 포함한 추가 개발을 할 수 있도록 소스 코드도 함께 공개되었다. 코드는 C에서 C++로 다시 쓰여졌다. 추가적인 스캔 타입과 프로토콜(예: IPv6) 지원하는 Nmap이 4.0 버전이 2006년 1월에 출시되었으며, 4.5버전이 2007년 12월에 나왔다. 각 공개판의 변경 사항들은\[1\]에 기록되어 있다.

## 논란

대부분의 컴퓨터 보안 도구가 그렇듯이, Nmap 역시 크래커의 해킹에 사용되거나, 컴퓨터 시스템에 허가 받지 않은 접근 시도를 할 수 있다. 보통은 운영 중인 서버의 열린 포트를 찾는 데 사용되며, 해당 정보를 이용하여 다른 공격 프로그램을 사용하게 된다.

시스템 관리자는 종종 자신의 네트워크에 허가받지 않은 서버나 가장 낮은 보안레벨을 가진 컴퓨터가 있는지 찾는 데 사용한다.

Nmap은 가끔 Nessus와 같은 취약점 평가 프로그램으로 오인받는다. 이러한 프로그램들은 대상의 취약한 열린 포트들을 테스트한다.

특정 사법권 내에서는 허가 받지 않은 포트 스캐닝이 불법으로 간주되기도 한다.

## 참조

## 외부 링크

  - [공식 웹사이트](http://nmap.org/)

[분류:보안 소프트웨어](https://ko.wikipedia.org/wiki/분류:보안_소프트웨어 "wikilink") [분류:리눅스 보안 소프트웨어](https://ko.wikipedia.org/wiki/분류:리눅스_보안_소프트웨어 "wikilink") [분류:네트워크 분석기](https://ko.wikipedia.org/wiki/분류:네트워크_분석기 "wikilink") [분류:크로스 플랫폼 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_자유_소프트웨어 "wikilink")

1.  [Nmap Changelog](http://nmap.org/changelog.html)