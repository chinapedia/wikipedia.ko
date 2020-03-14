> This article is converted from Wikipedia: [Hooksafe](https://ko.wikipedia.org/wiki/Hooksafe).


**Hooksafe**는 [하이퍼바이저](https://ko.wikipedia.org/wiki/하이퍼바이저 "wikilink") 기반 경량 시스템으로서 컴퓨터의 커널을 [루트킷](https://ko.wikipedia.org/wiki/루트킷 "wikilink") 공격으로부터 보호한다.

이것은 게스트 운영 체제에서 하이재킹으로부터 수천개의 커널 훅들을 예방한다. 이것은 모든 커널 훅들의 쉐도우 복사본을 중앙 지점에 만들고 훅에 접근하려는 시도를 규제하기 위해서 간접 계층을 추가함으로써 가능해진다. Hooksafe의 프로토타입은 리눅스 게스트에서 사용되었으며, 거의 6000개의 커널 훅들을 보호하였다.\[1\]\[2\] 이것은 [함수 포인터들인](https://ko.wikipedia.org/wiki/함수_포인터 "wikilink") 커널 제어 데이터를 보호하는데 초점을 맞춘다. 작은 성능 오버헤드를 가지며, 큰 스케일의 훅 보호를 제공한다.\[3\]

## 역사

이전의 루트킷 보호 시스템들은 다음을 포함하였다. Panorama, Hookfinder 그리고 루트킷 행동 분석에 중점을 둔 시스템, Copilot, VMwatcher 그리고 증상에 기반한 루트킷 탐지 시스템, Patagonix, NICKLE 그리고 악의적인 루트킷 코드의 실행을 방지함으로써 커널 코드 무결성을 보존하는데 중점을 둔 시스템들이 그것이다.\[4\]

## 각주

## 외부 링크

  - [VMwatcher](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.80.1954&rep=rep1&type=pdf)

[분류:유틸리티 소프트웨어 종류](https://ko.wikipedia.org/wiki/분류:유틸리티_소프트웨어_종류 "wikilink")

1.
2.
3.
4.