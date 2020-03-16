> This article is converted from Wikipedia: [H.261](https://ko.wikipedia.org/wiki/H.261).


**H.261**은 1988년 11월에 비준된 [ITU-T](../Page/ITU-T.md "wikilink") [영상 부호화](https://ko.wikipedia.org/wiki/영상_부호화 "wikilink") 표준이다.\[1\]\[2\] H.261 표준은 ITU-T [영상 부호화 전문가 그룹](https://ko.wikipedia.org/wiki/영상_부호화_전문가_그룹 "wikilink")(VCEG) H.26x 영상 부호화 표준 중에서 첫 번째 구성원이며, 실제 분야에서 효과를 거둔 첫 번째 영상 코덱이다.

H.261은 원래 데이터 레이트가 64 kbit/초인 [ISDN](../Page/ISDN.md "wikilink") 망 전송을 위해 설계되었다. 부호화 알고리즘은 40kbit/s와 2Mbit/s 사이의 영상 비트레이트로 작동될 수 있도록 설계되었다.

## 역사

디지털 영상 부호화 표준으로서 [H.120](../Page/H.120.md "wikilink")(1988년에 역사적으로 중요한 수정을 거쳤다.)이 1984년으로 H.261보다 앞서긴 하였으나, H.261이 진정한 첫 실용 디지털 영상 부호화 표준이다. 사실상 후속 국제 영상 표준들([MPEG-1 파트 2](https://ko.wikipedia.org/wiki/MPEG-1#파트_2:영상 "wikilink"), [H.262/MPEG-2 파트 2](https://ko.wikipedia.org/wiki/H.262/MPEG-2_파트_2 "wikilink"), [H.263](../Page/H.263.md "wikilink"), [MPEG-4 파트 2](../Page/MPEG-4_파트_2.md "wikilink"), [H.264/MPEG-4 AVC](https://ko.wikipedia.org/wiki/H.264/MPEG-4_AVC "wikilink"))은 H.261의 설계에 기초하고 있다. 또한, H.261 개발 위원회가 표준을 협력적으로 개발하기 위해 사용한 방법은 후속 표준화 작업을 위한 기초 작동 과정으로 굳어졌다.(S. Okubo, "Reference model methodology-A tool for the collaborative creation of video coding standards", Proceedings of the IEEE, vol. 83, no. 2, Feb. 1995, pp. 139–150 참조) 이 부호화 알고리즘은 움직임 보상을 이용한 이미지 간 예측과, 스칼라 양자화, 지그재그 스캐닝, [엔트로피 부호화를](https://ko.wikipedia.org/wiki/엔트로피_부호화 "wikilink") 동반한 공간 변형 부호화를 혼합한 방식을 사용한다.

## H.261 설계

설계의 기초처리 단위는 [매크로블록](../Page/매크로블록.md "wikilink")이며, H.261은 매크로블록 개념이 등장한 첫 번째 표준이다. 각각의 매크로 블록은 16x16의 [루마](https://ko.wikipedia.org/wiki/루마_\(비디오\) "wikilink") 샘플 배열과, [4:2:0 샘플링을](https://ko.wikipedia.org/wiki/크로마_서브_샘플링 "wikilink") 이용하고 [YCbCr](../Page/YCbCr.md "wikilink") [색 공간을](../Page/색_공간.md "wikilink") 사용하는 두 가지 일치한 8x8의 [색차](https://ko.wikipedia.org/wiki/색차 "wikilink") 샘플링으로 구성된다.

H.261 표준은 실질적으로 영상을 어떻게 디코딩할 것인가만 규정한다. 인코더 설계자들은 디코더가 표준을 따를 경우에 한하여 자유롭게 저들만의 인코딩 알고리즘을 디자인할 수 있다.

## 소프트웨어 구현

[LGPL](../Page/GNU_약소_일반_공중_사용_허가서.md "wikilink") 라이선스인 [libavcodec](https://ko.wikipedia.org/wiki/libavcodec "wikilink")은 H.261 인코더와 디코더를 갖고 있다. [VLC 미디어 플레이어](../Page/VLC_미디어_플레이어.md "wikilink"), [엠플레이어](https://ko.wikipedia.org/wiki/엠플레이어 "wikilink") 등의 자유 멀티미디어 플레이어와 [ffdshow](https://ko.wikipedia.org/wiki/ffdshow "wikilink")와 [FFmpeg](../Page/FFmpeg.md "wikilink") 디코더 프로젝트 내에서 이것을 지원한다.

## 같이 보기

  - [MPEG-1](../Page/MPEG-1.md "wikilink")
  - [H.263](../Page/H.263.md "wikilink")
  - [데이터 압축](../Page/데이터_압축.md "wikilink")

## 각주

<references/>

[분류:코덱](https://ko.wikipedia.org/wiki/분류:코덱 "wikilink") [분류:ITU](https://ko.wikipedia.org/wiki/분류:ITU "wikilink")

1.
2.