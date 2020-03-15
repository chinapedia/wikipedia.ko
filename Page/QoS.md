> This article is converted from Wikipedia: [QoS](https://ko.wikipedia.org/wiki/QoS).


**QoS**(Quality of Service)는 다른 응용 프로그램, 사용자, 데이터 흐름 등에 우선 순위를 정하여, 데이터 전송에 특정 수준의 성능을 보장하기 위한 능력을 말한다. 이를 굳이 한국말로 번역하여 말하자면, "통신 서비스 품질"이라고 할 수 있지만, 대한민국에서는 특별히 QoS를 한국말로 옮겨 사용하는 예는 드물고, 용도가 확고하게 정해진 바도 현재로서는 없다.

## 유래

전화 분야에서 QoS는 1994년 [국제전기통신연합](https://ko.wikipedia.org/wiki/국제전기통신연합 "wikilink")에 의해 정의되었다.\[1\]

[네트워크](https://ko.wikipedia.org/wiki/네트워크 "wikilink")는 크게 [패킷 교환 네트워크](https://ko.wikipedia.org/wiki/패킷_교환_네트워크 "wikilink")(packet switched network)와 [회선 교환 네트워크](https://ko.wikipedia.org/wiki/회선_교환_네트워크 "wikilink")(circuit switched network)가 있다. 패킷교환 네트워크는 이른바 우리가 이야기하는 [인터넷](../Page/인터넷.md "wikilink") [네트워크를](https://ko.wikipedia.org/wiki/컴퓨터_네트워크 "wikilink") 포함하고, 인터넷이 대중화되기 이전의 패킷 기반의 다른 방식 네트워크까지 두루 일컫는다. (다시 말해, TCP/IP 기반이 아닌 네트워크도 존재했다.) 회선교환 네트워크는 간단히 [PSTN](https://ko.wikipedia.org/wiki/PSTN "wikilink") 방식의 전화망을 생각하면 된다.

QoS 문제는 패킷 교환 네트워크에서 인터넷이 특별히 개별 흐름(flow) 또는 하나의 인터넷 연결에 대해서 더 우선권을 부여하지 않기 때문에 발생하는 문제이다. 우선권이 없다는 것은 곧 모든 인터넷 연결이 같은 중요도를 가지고 서비스를 받는다는 것을 뜻한다. 이를테면, 50Mbps 공유 링크가 있을 때, 10 명이 사용해서 인터넷 연결이 동시에 10 개가 생성되면, 각각은 5Mbps의 속도를 이용하게 된다.

그러나 인터넷 활용이 늘어남에 따라 인터넷 연결에도 분류를 나눠서 특정 분류의 연결을 더 우선적으로 서비스하거나 공유 링크의 특정 비율까지 차별적으로 이용하게 하려는 시도가 일어났다. 처음에는 이를 CoS(Class of Service)라고 불렀다.

그러나 차츰 이 용어보다는 QoS라는 용어가 대중화되었는데, 이는 특정 분류에 따른 차등 서비스보다는 개별 연결에 각각의 차등적인 서비스를 하려는 개념이다.

## QoS 제공 방법

[서버](../Page/서버.md "wikilink")(서비스를 제공하는 컴퓨터)와 [클라이언트](https://ko.wikipedia.org/wiki/클라이언트 "wikilink")(서비스를 이용하는 컴퓨터나 사용자) 자체적으로는 연결된 인터넷 연결의 서비스 정도를 달리할 방법이 없다.

그러므로 인터넷을 이루는 [접속 라우터](../Page/라우터.md "wikilink")(Access Router)나 [백본 라우터](https://ko.wikipedia.org/wiki/백본_라우터 "wikilink")(Backbone router)에서 주된 차등 서비스가 이루어진다.

## QoS 구현을 통한 응용 사례

### 미국 타임워너 사의 케이블 서비스

미국 타임워너(Timewarner) 사의 케이블 서비스는 소위 [3중 서비스](https://ko.wikipedia.org/wiki/3중_서비스 "wikilink")(Triple Play)를 하고 있다. 이는 하나의 케이블망을 통해서 케이블 TV, 전화, 인터넷을 동시에 서비스하는 것이다 .

여기서 중요한 것은 전화를 하면서 케이블 TV도 볼 수 있고, 동시에 다른 한 사람은 인터넷을 사용한다는 점이다. 이 때, 전화도 끊기면 안되고, TV도 화면이 멈추거나 손상되어서는 안 된다. 이것은 하나의 케이블망(물론 인터넷망)에 3개의 연결이 존재하는 것이며, 이 때, 우선 순위는 "TV \> 전화 \> 인터넷" 순서이다. 케이블 TV를 보는데, 화면이 멈추거나 망가지는 현상은 가입자에게 있을 수 없는 일이다. 하지만, 전화는 필요한 대역폭도 매우 적은데다가 잠깐 안 들려도 사람이 다시 의사를 전달하기 때문에 TV 보다 우선 순위가 낮아도 큰 지장이 없다. 인터넷은 당연히 느릴 수도 있기 때문에 사람들은 3개 서비스를 동시에 사용할 때, 인터넷이 잠시 느려지더라도 잘 인지하지 못한다.

만약, 이 때, QoS가 구현되지 않아서 TV나 전화, 그리고 인터넷이 똑같은 우선순위로 케이블망을 사용하게 되면 인터넷 사용자가 다운로드를 동시에 여러 개 시도할 경우, TV는 당장 볼 수 없는 지경에 이르고, 전화는 불통에 이르고 만다.

## QoS 우선 순위

| 우선 순위 | 트래픽 종류 |
| ----- | ------ |

| 0 (가장 낮음) | 최적 조건 |
| --------- | ----- |

| 1 | 배경 |
| - | -- |

| 2 | 표준 (예비) |
| - | ------- |

| 3 | 최적의 로드 (사업 결정) |
| - | -------------- |

| 4 | 제어 받는 로드 (스트리밍 멀티미디어) |
| - | --------------------- |

<table>
<thead>
<tr class="header">
<th><p>5</p></th>
<th><p>소리 및 영상 (인터렉티브 미디어 및 소리)</p>
<p>[100ms 이하의 레이턴시와 불안성]</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

<table>
<thead>
<tr class="header">
<th><p>6</p></th>
<th><p>계층 3의 네트워크 제어 보존 트래픽</p>
<p>[10ms 이하의 레이턴시와 불안성]</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

<table>
<thead>
<tr class="header">
<th><p>7 (가장 높음)</p></th>
<th><p>계층 2의 네트워크 제어 보존 트래픽</p>
<p>[가장 낮은 레이턴시와 불안성]</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

## 각주

[분류:통신공학](https://ko.wikipedia.org/wiki/분류:통신공학 "wikilink") [분류:컴퓨터 네트워크](https://ko.wikipedia.org/wiki/분류:컴퓨터_네트워크 "wikilink")

1.   Updated September 2008 as *Definitions of terms related to quality of service*