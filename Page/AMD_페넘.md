> This article is converted from Wikipedia: [AMD ](https://ko.wikipedia.org/wiki/AMD_).


**페넘**()은 [미국](../Page/미국.md "wikilink") [AMD](https://ko.wikipedia.org/wiki/AMD "wikilink")사가 제조한 쿼드 코어/트리플 코어 데스크톱 중앙처리장치이다. 기존과 달리 [K10 마이크로아키텍처로](../Page/AMD_K10.md "wikilink") 설계되었다.

## 시리즈 번호

| 시리즈 번호\[1\]                |
| -------------------------- |
| 프로세서 시리즈                   |
| 페넘 X4 쿼드 코어 (아제나-Agena)    |
| 페넘 X3 트리플 코어 (톨리먼-Toliman) |
| 애슬론 듀얼 코어 (쿠마-Kuma)        |
| 애슬론 싱글 코어 (리마-Lima)        |
| 셈프론 싱글 코어 (스파르타-Sparta)    |

## TLB 에러 (B2 스테핑)

페넘과 3세대 [옵테론](../Page/옵테론.md "wikilink") 프로세서의 B2 스테핑에서는 [가상화](../Page/가상화.md "wikilink") 환경과 같은 특수한 상황에서 시스템이 셧다운 되는 에러가 발견되었으며, [TLB의](https://ko.wikipedia.org/wiki/트랜슬레이션_룩어사이드_버퍼 "wikilink") 문제로 생긴 에러라는 것이 밝혀졌다. 인텔의 [코어2](../Page/인텔_코어_2.md "wikilink") 제품군의 콘로 B2 스테핑에서 발견된 TLB 에러와 바이오스나 운영체제등을 통해 해결이 가능하다는 것에서는 같으나, 페넘 B2 스테핑에서 발견된 TLB 에러는 바이오스 또는 프로그램(AMD 오버드라이브)를 통해 해결은 가능하나 평균 20% 정도의 비교적 큰 성능 하락이 있어 콘로 B2 스테핑의 경우와 달리 이슈가 되기도 하였다. [윈도 비스타](https://ko.wikipedia.org/wiki/윈도_비스타 "wikilink") SP1에서는 해결된 것이 기본값이며, 마찬가지로 성능하락이 있다. AMD는 B3 스테핑에서는 성능저하 없이 오류를 해결하였다.

한편, [리눅스](../Page/리눅스.md "wikilink")는 [커널](https://ko.wikipedia.org/wiki/커널 "wikilink") 패치를 통해 1% 정도의 성능 하락으로 페넘 B2 스테핑의 TLB 에러를 해결하였다.\[2\]

## 차세대 페넘 (페넘 II)

AMD K10.5 아키텍처로 개발되었으며, 공식적으로 페넘 II로 명명되었다.

## 제품군

[AMD](https://ko.wikipedia.org/wiki/AMD "wikilink") 페넘 프로세서는 다음과 같은 제품군으로 이루어져 있다. 현재까지의 모든 제품군은 65nm 공정과 SSE4A의 지원, 2MB의 L3 캐시, 코어당 128KB의 L1캐시와 512KB의 L2캐시를 공통적으로 장착하고 있으며 940핀, HT 3.0의 [소켓 AM2+](../Page/소켓_AM2+.md "wikilink") 형식으로 출시된 바 있으며, [바이오스](../Page/바이오스.md "wikilink") 업데이트 만으로 [소켓 AM2](../Page/소켓_AM2.md "wikilink") 메인보드에서 사용할 수 있으나 일부의 메인보드만이 해당 바이오스 업데이트를 지원한다. 페넘 X2로 알려졌던 쿠마는 [애슬론 X2인](https://ko.wikipedia.org/wiki/애슬론_X2 "wikilink") 것으로 확인되었다.

### 페넘 X4 시리즈 (쿼드 코어)

#### 아제나 (65 nm)

##### B3 스테핑

B2 스테핑에서 발생하던 TLB 에러를 해결한 버전이다.

  - AMD 페넘 X4 아제나 9950 블랙 에디션(2.6GHz, HT 4.0GT/s, TDP 140W, 배수제한 없음)
  - AMD 페넘 X4 아제나 9850 블랙 에디션(2.5GHz, HT 4.0GT/s, TDP 125W, 배수제한 없음)
  - AMD 페넘 X4 아제나 9750 (2.4GHz, HT 3.6GT/s, TDP 95/125W)
  - AMD 페넘 X4 아제나 9650 (2.3GHz, HT 3.6GT/s, TDP 95W, OEM용으로만 공급)
  - AMD 페넘 X4 아제나 9550 (2.2GHz, HT 3.6GT/s, TDP 95W)
  - AMD 페넘 X4 아제나 9350e (2.0GHz, HT 3.6GT/s, TDP 65W)
  - AMD 페넘 X4 아제나 9150e (1.8GHz, HT 3.2GT/s, TDP 65W)

##### B2 스테핑

  - AMD 페넘 X4 아제나 9600 블랙 에디션(2.3GHz, TDP 95W, 배수제한 없음)
  - AMD 페넘 X4 아제나 9500 (2.2GHz, TDP 95W)
  - AMD 페넘 X4 아제나 9100e (1.8GHz, TDP 65W)

### 페넘 X3 시리즈 (트리플 코어)

#### 톨리만 (65 nm, HT 3.6GT/s)

##### B3 스테핑

B2 스테핑에서 발생하던 TLB 에러를 해결한 버전이다.

  - AMD 페넘 X3 8750 (2.4GHz, B3, TDP 95W)
  - AMD 페넘 X3 8650 (2.3GHz, B3, TDP 95W)
  - AMD 페넘 X3 8450 (2.1GHz, B3, TDP 95W)

##### B2 스테핑

  - AMD 페넘 X3 8600 (2.3GHz, B2, TDP 95W, OEM용으로만 공급)
  - AMD 페넘 X3 8400 (2.1GHz, B2, TDP 95W, OEM용으로만 공급)

## 블랙 에디션 (Black Edition)

블랙 에디션은 CPU에 걸려 있는 상향 배수 조절 제한(배수락) 을 제거한 모델이다. 일반 모델과 다른 박스에 담겨있다. 90nm 윈저 코어의 애슬론 64 X2 6400+ 에서 처음으로 출시된 바 있으며, 페넘 쿼드코어 제품군으로는 X4 9950과 9850, 9600, 트리플 코어 제품군으로는 X3 8750이 있다.

## 같이 보기

  - [K10 마이크로아키텍처](../Page/AMD_K10.md "wikilink")

## 참조

<references />

## 외부 링크

  - [AMD Phenom Processor Family](http://www.amd.com/us-en/Processors/ProductInformation/0,,30_118_15331,00.html)

[분류:AMD x86 마이크로프로세서](https://ko.wikipedia.org/wiki/분류:AMD_x86_마이크로프로세서 "wikilink")

1.  [VR-Zone report](http://www.vr-zone.com/articles/AMD_Revised_Desktop_Model_Number_Structure/5330.html), retrieved October 9, 2007
2.  [Linux kernel patch reveals TLB bug's workings - The Tech Report](http://techreport.com/discussions.x/13742)