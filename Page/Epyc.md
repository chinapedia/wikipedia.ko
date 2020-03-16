> This article is converted from Wikipedia: [Epyc](https://ko.wikipedia.org/wiki/Epyc).


**Epyc**(에픽)은 [옵테론](../Page/옵테론.md "wikilink")의 후속으로 개발된 [AMD의](../Page/어드밴스트_마이크로_디바이시스.md "wikilink") [x86](https://ko.wikipedia.org/wiki/x86 "wikilink") 서버용 [프로세서이며](../Page/마이크로프로세서.md "wikilink"), 자사의 [젠 마이크로아키텍처를](../Page/젠_\(마이크로아키텍처\).md "wikilink") 기반으로 제작되었다. 2017년에 선보였다.\[1\]

## 역사

2017년 3월 AMD는 Naples 코드명의 [젠 마이크로아키텍처](../Page/젠_\(마이크로아키텍처\).md "wikilink") 기반의 서버 플랫폼을 발표하였으며 5월 Epyc이라는 브랜드 이름으로 공식 공개하였다.\[2\] 그 해 6월, AMD는 Epyc 7000 시리즈 프로세서를 출시함으로써 공식적으로 Epyc을 런칭하였다.\[3\]

## 디자인

에픽은 1\~2개 소켓 시스템을 목표로 개발되었다. 멀티프로세서 구성에서 2개의 Epyc CPU들은 AMD의 [인피니티 패브릭](../Page/하이퍼트랜스포트.md "wikilink")(Infinity Fabric)을 통해 연결되어 구동된다.\[4\] 각 서버 칩은 8채널의 메모리와 128개 레인의 [PCI 익스프레스](../Page/PCI_익스프레스.md "wikilink") 3.0을 지원하며 그 중 64개 레인은 듀얼 프로세서로 구성 시 인피니티 패브릭을 경유하는 CPU 대 CPU 통신을 위해 사용된다.\[5\] 모든 Epyc 프로세서들은 [멀티 칩 모듈에서](https://ko.wikipedia.org/wiki/멀티_칩_모듈 "wikilink") 4개의 8코어 Zeppelin 다이([라이젠](https://ko.wikipedia.org/wiki/라이젠 "wikilink") 프로세서에서 보이는 동일한 다이)로 구성되며 각 Zeppelin 다이 상의 개별 [코어 컴플렉스의](../Page/젠_\(마이크로아키텍처\).md "wikilink") 코어들을 동시에 비활성화하여 다양한 제품 코어 수를 보여준다.\[6\]\[7\]

## 반응

Epyc의 초기 반응은 대체적으로 긍정적이었다.\[8\] Epyc은 [슈퍼컴퓨터](../Page/슈퍼컴퓨터.md "wikilink"), [빅 데이터](../Page/빅_데이터.md "wikilink") 응용 등 코어가 독립적으로 동작하는 조건에서 대체적으로 인텔 CPU를 압도하는 것으로 확인되었다. Epyc은 더 높은 캐시 레이턴시로 인해 [인텔](../Page/인텔.md "wikilink")의 [제온](../Page/제온.md "wikilink") 부분과 비교해 데이터베이스 작업에서는 뒤쳐지는 것으로 나타났다.\[9\]

## Epyc 프로세서 목록

### 서버용 프로세서

#### 네이플스 (Naples)

### 임베디드 서버용 프로세서

#### 네이플스 (Naples)

2018년 2월, AMD는 EPYC 3000 시리즈의 임베디드 젠 CPU를 발표하였다.\[10\]

## 각주

[분류:AMD x86 마이크로프로세서](https://ko.wikipedia.org/wiki/분류:AMD_x86_마이크로프로세서 "wikilink")

1.
2.
3.
4.
5.
6.
7.  <https://www.nextplatform.com/2017/05/17/amd-disrupts-two-socket-server-status-quo/>
8.
9.
10.