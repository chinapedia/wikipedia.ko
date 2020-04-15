> This article is converted from Wikipedia: [모바일 PCI 익스프레스 모듈](https://ko.wikipedia.org/wiki/모바일_PCI_익스프레스_모듈).


**모바일 PCI 익스프레스 모듈**(Mobile PCI Express Module, MXM)은 [PCI 익스프레스를](../Page/PCI_익스프레스.md "wikilink") 사용하는 [랩톱 컴퓨터의](../Page/랩톱_컴퓨터.md "wikilink") [GPU](../Page/그래픽_처리_장치.md "wikilink")(MXM 그래픽스 모듈)를 위한 인터커넥트 표준으로, MXM-SIG가 개발하였다. 목적은 사유가 아닌, 산업 표준 소켓을 만들어서 완전히 새로운 시스템을 사거나 사유 벤더 업그레이드에 의존하지 않고도 노트북의 그래픽 프로세서를 쉽게 업그레이드할 수 있게 하는 것이다.

## 1세대 구성

| MXM 타입              | 너비   | 길이    | 핀        | 모듈 호환성         | 서멀 호환성         | 최대소비전력 | 최대 GPU 크기\[1\] |
| ------------------- | ---- | ----- | -------- | -------------- | -------------- | ------ | -------------- |
| MXM-I               | 70mm | 68mm  | 230      | I              | I              | 18W    | 35 mm²         |
| MXM-II              | 73mm | 78mm  | 230      | I, II          | II             | 35W    | 35 mm²         |
| MXM-III (HE)        | 82mm | 100mm | 230(232) | I, II, III     | I, II, III     | 75W    | 40 mm²         |
| MXM-IV (Deprecated) | 82mm | 117mm | 230      | I, II, III, IV | I, II, III, IV |        |                |

## 2세대 구성

| MXM 타입 | 너비   | 길이    | 모듈 호환성 | 서멀 호환성 | 최대소비전력 | GPU 메모리 버스        |
| ------ | ---- | ----- | ------ | ------ | ------ | ----------------- |
| MXM-A  | 82mm | 70mm  | A      | A      | 55W    | 64-bit or 128-bit |
| MXM-B  | 82mm | 105mm | A, B   | A, B   | 200W   | 256-bit           |

## 모듈 호환성

1세대 모듈은 2세대 모듈과 상호 호환되지 않는다. 1세대 모듈은 완전한 하위 호환성이 있다.

## MXM 카드 목록

### MXM 3.x 카드

| 벤더                         | 이름              | 출시일             | MXM 타입      | GPU          | 코어 구성\*        | TFLOPS (FP32) | TDP  |
| -------------------------- | --------------- | --------------- | ----------- | ------------ | -------------- | ------------- | ---- |
| AMD                        | FirePro S4000X  | Aug 2014        | Type-A      | Venus XT     | 640:40:16      | 1.0           | 45W  |
| FirePro S7100X             | May 2016        | Type-B          | Amethyst XT | 2048:128:32  | 3.0            | 100W          |      |
| Radeon Embedded E9260\[2\] | Sep 2016        | Type-A          | Polaris 11  | 896:56:16    | 2.5            | 50W           |      |
| Radeon Embedded E9550\[3\] | Type-B          | Polaris 10      | 2304:144:32 | 5.8          | 95W            |               |      |
| Nvidia                     | Tesla M6        | Sep 2015        | Type-B      | GM204        | 1536 / 96 / 48 | 3.0           | 100W |
| Quadro M520 Mobile\[4\]    | Jan 2017        | Type-A          | GM108       | 384 / 16 / 8 | 0.8            | 25W           |      |
| Quadro M620 Mobile\[5\]    | GM107           | 512 / 32 / 16   | 1.0         | 30W          |                |               |      |
| Quadro M1200 Mobile\[6\]   | 640 / 40 / 32   | 1.4             | 45W         |              |                |               |      |
| Quadro M2200 Mobile\[7\]   | GM206           | 1024 / 64 / 32  | 2.1         | 55W          |                |               |      |
| Quadro P3000 Mobile\[8\]   | GP104           | 1280 / 80 / 32  | 3.1         | 75W          |                |               |      |
| Quadro P4000 Mobile\[9\]   | Type-B          | 1792 / 112 / 64 | 4.4         | 100W         |                |               |      |
| Quadro P5000 Mobile\[10\]  | 2048 / 128 / 64 | 6.2             | 100W        |              |                |               |      |

## 각주

## 외부 링크

  - [MXM-SIG](https://web.archive.org/web/20081112061442/http://www.mxm-sig.org/)

[분류:컴퓨터 버스](https://ko.wikipedia.org/wiki/분류:컴퓨터_버스 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.