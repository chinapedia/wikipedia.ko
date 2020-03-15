> This article is converted from Wikipedia: [PCX](https://ko.wikipedia.org/wiki/PCX).


**PCX**(PiCture eXchange)는 Z소프트에서 개발한 그래픽 파일 포맷이다. Z소프트가 개발한 [도스](../Page/도스.md "wikilink")기반의 페인트브러시 프로그램에서 사용하기 위하여 만들어졌다. [RLE 압축을](https://ko.wikipedia.org/wiki/반복_길이_부호화 "wikilink") 사용하며, 기본적으로 인덱스 컬러를 사용하지만 트루컬러로도 확장할 수 있다. 초기 도스 환경에서 인기가 많은 포맷이었으나, [PNG](../Page/PNG.md "wikilink"), [GIF](../Page/GIF.md "wikilink"), [JPEG](../Page/JPEG.md "wikilink")와 같은 더 나은 성능의 포맷에 밀려 최근에는 거의 사용되지 않는다.

## 구조

PCX 파일은 다음과 같은 순서로 세 개의 주요 부분으로 나뉜다.

1.  128 바이트 헤더
2.  그림 데이터
3.  (선택 사항) 256색 팔레트

PCX 파일은 IBM 호환 PC에서 사용하도록 설계되었으며 늘 [리틀 엔디언](https://ko.wikipedia.org/wiki/리틀_엔디언 "wikilink") 바이트 정렬를 이용한다.

## 일반 PCX 이미지 포맷

| 비트 | 플레인 | 색 수                   |
| -- | --- | --------------------- |
| 4  | 1   | 팔레트 16색               |
| 8  | 1   | 팔레트 256색              |
| 8  | 1   | 256 회색 음영             |
| 4  | 4   | 16 단계 투명도를 포함한 4095색  |
| 8  | 3   | 24비트 트루 컬러를 포함한 42억 색 |
| 8  | 4   | 256 단계 투명도를 포함한 42억 색 |

**표 A. 일반 PCX 이미지 포맷**

|                   |                   |
| :---------------: | ----------------- |
|        줄 0        | R R R R R R R R R |
|  G G G G G G G G  |                   |
| B B B B B B B B B |                   |
| A A A A A A A A A |                   |
|        줄 1        | R R R R R R R R R |
|  G G G G G G G G  |                   |
| B B B B B B B B B |                   |
| A A A A A A A A A |                   |
|     줄 2 등...      | ....              |

**표 B. 컬러 플레인에 정렬된 PCX 이미지 데이터**

## 외부 링크

  - [Z소프트의 PCX 파일 포맷 기술 설명서](http://bespin.org/~qz/pc-gpe/pcx.txt)

[분류:그래픽 파일 포맷](https://ko.wikipedia.org/wiki/분류:그래픽_파일_포맷 "wikilink")