> This article is converted from Wikipedia: [OSx86](https://ko.wikipedia.org/wiki/OSx86).


**OSx86**은 [애플의](https://ko.wikipedia.org/wiki/애플_\(기업\) "wikilink") [OS X](https://ko.wikipedia.org/wiki/OS_X "wikilink") [운영 체제를](https://ko.wikipedia.org/wiki/운영_체제 "wikilink") 비 매킨토시 환경에서 깔리게 하는 해킹 프로젝트이다. OSx86은 [2005년](https://ko.wikipedia.org/wiki/2005년 "wikilink") [6월](https://ko.wikipedia.org/wiki/6월 "wikilink") 애플의 세계 개발자 회의(Worldwide Developers Conference, WWDC)에서, 예전에 쓰던 파워 PC를 인텔 마이크로프로세서로 전환할 것을 발표한 것에 기인한다.

최초의 시도는 애플이 999달러에 판매한 개발자 전환 키트의 DVD가 누출된 것이었다. OSx86의 첫 번째 패치는 개발자 전환 키트에 포함된 [로직보드](https://ko.wikipedia.org/wiki/로직보드 "wikilink")에 장착된 [신뢰 플랫폼 모듈](https://ko.wikipedia.org/wiki/신뢰_플랫폼_모듈 "wikilink")(Trusted Platform Module)을 우회하는 데 초점을 맞췄다. TPM은 파워피씨 프로그램을 인텔 기반의 매킨토시에서 구동하게 만들어 주는 [로제타를](../Page/로제타_\(소프트웨어\).md "wikilink") 기반으로 하는데, 로제타를 제거하면, OS X은 비 매킨토시에서 설치가 되었다. 로제타는 SSE3 명령을 필요로 하는데, 이 패치는 SSE2 상태를 에뮬레이트하고, SSE3를 지원하지 않는 [CPU에서](https://ko.wikipedia.org/wiki/중앙_처리_장치 "wikilink") 설치를 지원하고 있다.

2005년 10월, 애플에서 개발자 키트를 10.4.3로 업데이트하면서, [NX 비트를](https://ko.wikipedia.org/wiki/NX_비트 "wikilink") 지원하는 마이크로프로세서가 필요하게 하였다.\[1\] 패치는 이 업데이트를 회피해서 다시 나오게 되었다.\[2\]

이 같은 방법으로 OS X을 이용하는 컴퓨터를 때로 **해킨토시**(Hackintosh)라 부르는데, 이는 본래 맥 시스템을 운용하도록 개조된 [리사 2/10을](https://ko.wikipedia.org/wiki/리사_2/10 "wikilink") 가리키는 용어기도 하였다.

## 맥 OS X 10.4 타이거

[2006년](https://ko.wikipedia.org/wiki/2006년 "wikilink") [1월 10일](https://ko.wikipedia.org/wiki/1월_10일 "wikilink"), 애플은 최초의 인텔 기반의 맥킨토시에 돌아가는 맥 OS X 10.4.4 버전을 발매하였다. 이 컴퓨터는 x86에서 쓰이던 BIOS와 다른 [EFI](https://ko.wikipedia.org/wiki/확장_펌웨어_인터페이스 "wikilink")(확장 펌웨어 인터페이스) 칩을 장착하였다. [2006년](https://ko.wikipedia.org/wiki/2006년 "wikilink") [1월 14일](https://ko.wikipedia.org/wiki/1월_14일 "wikilink") 인터넷에서 Maxxuss라는 이름의 사용자가 최초로 OS X 10.4.4 버전을 크랙하였다.\[3\] 그러나, 몇시간 안에 애플에서는 10.4.5 업데이트를 하였다.\[4\], 그러나, Maxxuss가 2주내에 그에 대한 패치를 내놓았다.\[5\] [2006년](https://ko.wikipedia.org/wiki/2006년 "wikilink") [4월 3일](https://ko.wikipedia.org/wiki/4월_3일 "wikilink") 애플에서는 맥 OS X의 10.4.6 업데이트를 내놓았다.\[6\] 그리고 2주안에 10.4.6. 커널은 포함되지 않았지만 말이다. 10.4.6. 패치를 처음 내놓은 SemjaZa와 컴파일한 JaS는 6월에 매킨토시가 아닌 컴퓨터에서 돌아가는 10.4.7. 패치를 내놓았지만, 여전히 10.4.4. 커널을 사용하고 있다.

10.4.8 업데이트가 나와도, 패치의 커널은 아직도 10.4.4를 쓰고 있었다. 그러나 많은 업데이트들이 프레임워크에 대해서 10.4.8 커널의 업데이트가 필요하였다. 애플은 또 예전보다 SSE3 구조를 더 많이 쓰도록 만들어, SSE2 사용자들의 시스템은 제 성능을 발휘하지 못하게 되었다.

이러한 까닭에, Mifki/Vitaliy 와 Semthex라는 두 명의 숙련된 프로그래머에 의해서, 10.4.8. 커널이 극적으로 등장하게 되었다. 그들은 [오픈 소스인](https://ko.wikipedia.org/wiki/오픈_소스 "wikilink") XNU 트리에서 출발하여, 비 맥킨토시 하드웨어에서 돌릴 수 있는 패치를 적용할 수 있었다. Mifki이 커널을 공개함에 따라, 여러 패치들이 뒤이어 나오게 되었고, 닫힌 애플의 하드웨어에서 잘 돌아가게 되었다. 자신의 일을 커뮤니티에 돌린 Semthex의 커널은 여러 하드웨어를 사용할 수 있게 되었고, 여러 중대한 결점들을 제거하였다.

이 커널들은 여러 kexts/framework에서 벌어지는 일들을 허용해서, 일반 PC를 정품 매킨토시처럼 만들었다. Mifki가 그의 커널을 업데이트만 했지만, Semthex는 자신의 커널의 새 버전에 [AMD](https://ko.wikipedia.org/wiki/어드밴스트_마이크로_디바이시스 "wikilink"), VMware와 SSE2를 지원하게 되었다. Semthex는 자신의 해킹 커널의 소스 코드를 자신의 웹사이트에 공개하였다. 12월 24일 Semthex는 그의 최초의 소스 트리와 파일이 다른 SSE3 커널을 크리스마스 선물로 공개하였다. Semthex와 Rufus가 개발한 SSE2 에뮬레이션에 대한 특별한 배려를 하여야 하는데, 이 에뮬레이션은 OSx86의 역사에서 최초의 SSE3 구조를 완벽하게 가상으로 구현한 것이다. 예전 에뮬레이터는 불완전하였고, 새로 나온 에뮬레이터보다 느렸다. 이 효과는 높은 3차원 프로그램과, 아이튠스 프로그램을 돌릴 때 뚜렷하게 나타났다.

타이거 시리즈가 10.4.11을 마지막으로 개발이 중단되자 타이거 버전 해킨토시 개발도 XxX의 XxX 10.4.11을 마지막으로 중단되었다.

## 맥 OS X 10.5 레퍼드

해킨토시는 애플의 [레퍼드](https://ko.wikipedia.org/wiki/맥_OS_X_10.5 "wikilink") 출시와 함께 새로운 전환기를 맞게 된다. Kalyway라는 이름의 해커가 이전 타이거 시리즈보다 훨씬 안정적이고 부드러운 《Kalyway 10.5》 와 《Kalyway 10.5.1》을 공개하였고, 얼마 지나지 않아 보다 손쉬운 설치를 위해 DVD 인스톨 버전도 내놓았다. DVD 인스톨 버전으로 인해 해킨토시의 설치가 훨씬 쉬워졌고 덕분에 해킨토시는 빠른 속도로 확산되었다. 애플이 10.5.2 업데이트를 내놓자 eddie라는 해커는 JaS라는 해커와 함께 《Leo4All》를 개발하였다. 현재 해킨토시는 10.5.8까지 나와있으며 가장 흔하게 구할 수 있는 버전은 Kalyway 버전과 Leo4All 버전과 iAtkos 버전과 iDeneb, iPc 버전이다.

## [맥 OS X 10.6 스노 레퍼드](https://ko.wikipedia.org/wiki/맥_OS_X_10.6 "wikilink")

매킨토시의 10.6 스노 레퍼드이다.

## 해킨토시 PC의 출시

### Psystar PC

[2008년](https://ko.wikipedia.org/wiki/2008년 "wikilink") [2월](https://ko.wikipedia.org/wiki/2월 "wikilink"), 미국의 중소업체 Psystar는 "세계 최초의 해킨토시 탑재 PC"를 출시하였다. 이 PC의 특징은 메인보드 자체에 EFI 에뮬레이터를 탑재하였다는 것이다. 따라서 [애플에서](https://ko.wikipedia.org/wiki/애플_\(기업\) "wikilink") 파는 정품DVD를 Psystar PC에 삽입하면 그 DVD는 PC를 정품 매킨토시로 인식하여 설치를 진행한다.

이에 관련해 애플은 [EULA을](https://ko.wikipedia.org/wiki/최종_사용자_라이선스_동의 "wikilink") 위반했다며 소송을 걸 것이라고 맞섰다.

### EFI-X

## 참고 사항

## 외부 링크

  - [The OSx86 프로젝트](http://www.osx86project.org/)

  - [InsanelyMac: OSx86 프로젝트에서 분리된 포럼이다](http://www.insanelymac.com/)

  - [semthex의 블로그](http://www.semthex.com/)

  - [netkas의 블로그](https://web.archive.org/web/20190304122522/http://netkas.org/)

  - [OSx86 Ritz 블로그](http://osx86.tistory.com/)

[분류:macOS](https://ko.wikipedia.org/wiki/분류:macOS "wikilink")

1.
2.
3.
4.
5.
6.