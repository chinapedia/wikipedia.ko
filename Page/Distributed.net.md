> This article is converted from Wikipedia: [Distributed.net](https://ko.wikipedia.org/wiki/Distributed.net).


**distributed.net**은 1997년 설립된 인터넷에 기반한 최초의 범용 [분산 컴퓨팅](../Page/분산_컴퓨팅.md "wikilink") 프로젝트 중 하나이다. 분산컴퓨팅의 발전을 추구하기 위하여 development, deployment, advocacy의 세 가지를 목적으로 삼는다.

## DNETC@HOME

DNETC@HOME은 distributed.net에서 수행하는 [분산 컴퓨팅](../Page/분산_컴퓨팅.md "wikilink") 기술을 활용한 프로젝트의 클라이언트 프로그램을 [BOINC](../Page/BOINC.md "wikilink") 기반으로 구동하는 프로젝트로서 **RC5**와 **OGR**이 진행되고 있다.

## 세부 프로젝트

### RC5

**RC5**는 원래 [블록 암호](https://ko.wikipedia.org/wiki/블록_암호 "wikilink") [알고리즘](../Page/알고리즘.md "wikilink")으로 [미국](../Page/미국.md "wikilink")의 [로널드 라이베스트](../Page/로널드_라이베스트.md "wikilink")()에 의해 1994년 고안되었으며 비교적 간단하고도 강력한 암호화 알고리즘으로 유명하다.

이 암호화 방식에 대해 특허권을 가지고 있는 [RSA Security에서는](https://ko.wikipedia.org/wiki/RSA_Security "wikilink") RC5로 암호화된 문장을 해독하는 사람에게 상금을 지급하였는데 이 암호화 문장을 풀기 위하여 모든 가능한 암호화 키를 하나씩 넣어서 확인해 보는 [무차별 대입 공격](https://ko.wikipedia.org/wiki/무차별_대입_공격 "wikilink")() 방식으로 암호를 풀어내는 것이 이 프로젝트의 목적이다.

지금까지 암호키의 길이에 따라 56bit, 64bit, 72bit의 세가지 암호화 문장에 대한 해독이 이루어지고 있으며 앞의 두 가지의 암호는 각각 1997년 10월 19일, \[1\] 2002년 7월 14일 \[2\] 에 풀렸으며 각각의 문장 내용은 다음과 같다.

  - RC5-56 : **It's time to move to a longer key length**
  - RC5-64 : **Some things are better left unread**
  - RC5-72 : 현재 진행 중임.

현재 수행중인 RC5-72는 2010년 10월 기준으로 2,884일, 전체 탐색 키의 1.130%가 진행 중이다. \[3\] 2007년 RSA Security로부터의 우승상금 지원이 중단되었으나 프로젝트 자체적으로 동일한 비율의 상금(발견자 1,000$(US), 발견 팀 1,000$(US), [자유 소프트웨어 재단](../Page/자유_소프트웨어_재단.md "wikilink") 2,000$(US))을 지원하기로 결정하였다. \[4\]

### OGR

OGR은 Optimal [Golomb rulers의](https://ko.wikipedia.org/wiki/Golomb_rulers "wikilink") 줄임말로서 Golomb rulers는 주어진 숫자(mark)개의 숫자를 늘어놓은 가상의 자(ruler)를 생각했을 때 각 숫자간의 거리가 모두 다르며 가장 작은 숫자(0)과 가장 큰 숫자간의 거리 차이가 가장 짧은 숫자열을 의미한다. 이러한 숫자열은 [미국](../Page/미국.md "wikilink")의 수학자 [솔로몬 골룸](https://ko.wikipedia.org/wiki/솔로몬_골룸 "wikilink")()에 의해 창안되었으며 이러한 수열을 구하는 일반적인 최적화된 방법론은 존재하지 않는다.

OGR 프로젝트에서는 최적의 order-24 \[5\] (2004년 11월 1일), order-25 \[6\] (2008년 10월 25일), order-26 \[7\] (2009년 2월 24일) 값을 찾아내었고 현재 order-27 값에 대해서 조사하고 있다.

## GPU 활용

DCNET@HOME은 계산을 수행할 때 [CPU](../Page/중앙_처리_장치.md "wikilink") 뿐만이 아니라 [그래픽 카드의](../Page/그래픽_카드.md "wikilink") [GPU](../Page/그래픽_처리_장치.md "wikilink") 자원도 활용한다. [엔비디아](../Page/엔비디아.md "wikilink")의 [CUDA](../Page/CUDA.md "wikilink") 뿐만 아니라 [AMD](https://ko.wikipedia.org/wiki/AMD "wikilink")의 스트림도 지원하며 2009년부터 지원하였다. CPU보다 높은 처리성능을 보이고 있다. \[8\]

## DNETC@HOME 의 종료

2011년 10월 DNETC@HOME 은 종료되고 새롭게 파생된 카피 프로젝트인 [<http://moowrap.net>](http://Moo!%20Wrapper) 로 이전되었다.

## 같이 보기

  - [BOINC](../Page/BOINC.md "wikilink")
  - [분산 컴퓨팅](../Page/분산_컴퓨팅.md "wikilink")

## 참고자료

<references />

## 외부 링크

  - [Moo\! Wrapper 홈페이지](http://moowrap.net/)

  - [distribute.net 홈페이지(Node Zero)](http://www.distributed.net/Main_Page)

  - [OGR FAQ](http://faq.distributed.net/cache/20.html)

  - [Golomb Rulers 설명](https://web.archive.org/web/20060430224518/http://members.aol.com/golomb20/intro.htm)

[분류:BOINC](https://ko.wikipedia.org/wiki/분류:BOINC "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.