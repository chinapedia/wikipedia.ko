> This article is converted from Wikipedia: [IS](https://ko.wikipedia.org/wiki/IS).


**집적회로간 사운드**(Integrated Interchip Sound, **IIS**) 또는 **Inter-IC Sound**로 잘 알려진 **I<sup>2</sup>S**는 필립스에서 제정한 집적회로간 사운드 버스이다. I2는 inter ic를, S는 sound에 대한 약자이다. I2S 버스는 오디오 데이터 전송만을 다루는 목적으로 제정이 되었고 연결을 단순화하기 위해서 3 Line을 사용한다.

## 역사

이 표준은 1986년 필립스 세미컨덕터(Philips Semiconductor, 현재의 [NXP 세미컨덕터](https://ko.wikipedia.org/wiki/NXP "wikilink"))에 도입되었으며 1996년 6월 5일 마지막으로 개정되었다.\[1\]

## 라인 구성

비동기 양방향 전송을 위한 line 1개와 clock 전달을 위한 line 1개 워드 셀렉트(word select)이라고 불리는 방향 신호용 라인 1개로 구성된다.

## 송수신을 위한 역할분담

전송을 위한 구성에서 보내는 역할을 맡는 송신기(transmitter), 수신 역할을 맡는 수신기(receiver)로 구성이 되며 데이터 전송을 위해서 송/수신 측에서 같은 clock을 사용해야하므로 단순한 시스템에서는 송신기가 클럭(clock)을 제공하는 마스터(master) 역할을 한다.

따라서 송신기는 clock/data/word 선택 신호를 제공하도록 구성할 수 있다. 하지만 시스템이이 IC 간의 오디오 데이터 흐름을 조정해야할 필요가 있는 구성에서는 수신 측에서 전송데이터를 전송하는 것은 구성에서 수신기가 클럭과 word 선택 신호를 제공하는 마스터가 된다.

복수개의 IC가 존재하는 구성에서는 별도의 컨트롤러가 클럭과 word 선택신호를 제공하고 송신기와 수신기가 모두 슬레이브(slave)처럼 동작하는 구성을 사용하기도 한다.

## 용어

1.  SCK: continuous serial clock
2.  WS: word select (0은 left channel, 1 은 right channel)
3.  SD: serial data
4.  master: WS와 SCK를 공급하는 역할

## 각주

[분류:직렬 버스](https://ko.wikipedia.org/wiki/분류:직렬_버스 "wikilink")

1.