> This article is converted from Wikipedia: [HyperZ](https://ko.wikipedia.org/wiki/HyperZ).


[섬네일](https://ko.wikipedia.org/wiki/파일:AMD_HyperZ.svg "wikilink") **HyperZ**는 [ATI 테크놀로지스](../Page/ATI_테크놀로지스.md "wikilink") 사가 그 회사가 제조/판매했던 [레이디언](https://ko.wikipedia.org/wiki/레이디언 "wikilink")(Radeon) [그래픽 처리 장치에](https://ko.wikipedia.org/wiki/그래픽_처리_장치 "wikilink") 한 때 사용했던 소정의 [컴퓨터 그래픽스](https://ko.wikipedia.org/wiki/컴퓨터_그래픽스 "wikilink") 처리 기술을 일컫는 말이다.

[레이디언 R100](https://ko.wikipedia.org/wiki/레이디언_R100 "wikilink") 기반 코어(core) 때부터 HyperZ 기술이 사용되기 시작했다. [레이디언 R100](https://ko.wikipedia.org/wiki/레이디언_R100 "wikilink") 기반 코어(core)에 기반한 레이디언 DDR부터 레이디언 7500까지의 비디오 카드에 대하여, ATI 사 측은 20%의 전반적인 렌더링(rendering) 효율 향상이 있다고 주장하였다. HyperZ를 사용하면, 비디오 카드의 이론적 필레이트(fillrate)인 1.2 기가텍셀(Gigatexel)을 넘어선 초당 1.5 기가텍셀(Gigatexel) 필레이트(fillrate)의 성능을 보여준다고 주장하였다. 테스트 상황에서, 경쟁 카드인 [지포스 2 GTS를](https://ko.wikipedia.org/wiki/지포스_2 "wikilink") 따라잡을 만한 성능을 보여주었다. \[1\]

후속 코어가 출시될 때마다, ATI 측은 이 기술을 손을 봤으며 향상시켰다. [레이디언 R200](https://ko.wikipedia.org/wiki/레이디언_R200 "wikilink") (8500-9250)에서는 **HyperZ II**가 구현되었다. **HyperZ III+**는 [레이디언 R300](https://ko.wikipedia.org/wiki/레이디언_R300 "wikilink") 기반 카드에 사용되었으며, **HyperZ HD**는 [레이디언 R420](https://ko.wikipedia.org/wiki/레이디언_R420 "wikilink") 기반 카드에 들어가 카드와 함께 출시되었다.

[엔비디아](https://ko.wikipedia.org/wiki/엔비디아 "wikilink")도 이에 질세라 비슷한 기술을 [지포스 3부터](https://ko.wikipedia.org/wiki/지포스_3 "wikilink") 도입하였다. 엔비디아의 기술 이름은 [라이트스피드 메모리 아키텍처](https://ko.wikipedia.org/wiki/라이트스피드_메모리_아키텍처 "wikilink")(LMA)였다. 예를 들어, 지포스2 울트라 (NV15)와 [지포스4 MX는](https://ko.wikipedia.org/wiki/지포스_4 "wikilink") 같은 패밀리(family)였으며 NV15가 두 배의 파이프라인 수를 갖고 있었다. 그런데 라이트스피드 메모리 아키텍처 기술을 지포스 4 MX의 NV17 코어에 사용함으로써, NV17이 NV15보다 나은 성능을 내게 했다.\[2\]

## 기능

HyperZ는 세 개의 메커니즘으로 구성된다.

  - **Z 압축**() — Z-버퍼(Z-Buffer)가 [무손실 압축](https://ko.wikipedia.org/wiki/무손실_압축 "wikilink") 형태로 저장된다. Z 읽기(read) 및 쓰기(write) 동작이 일어날 때의 [Z-버퍼](https://ko.wikipedia.org/wiki/Z-버퍼 "wikilink") 밴드위스를 줄이기 위함이다. 초창기 [레이디언 256에서](https://ko.wikipedia.org/wiki/레이디언_256 "wikilink") 쓰였던 압축 기법 대비, [레이디언 8500에](https://ko.wikipedia.org/wiki/레이디언_8500 "wikilink") 와서 압축 기법이 20% 효율이 좋아졌다.
  - **빠른 Z 청소**() — Z-버퍼에 전부 0(zeros)를 쓰는(write) 동작(다른 Z-버퍼 쓰기(write) 밴드위스를 저해한다.) 대신, "빠른 Z 청소" 기술은 Z-버퍼의 각각의 블록에 대해 그 블록이 "청소된"(cleared) 상태라고 태그(tag)를 할 수 있게 해준다. 청소(clear)되면서 태그가 되어야 할 블록에만 태그를 달 수 있게 해 준다. [레이디언 8500에](https://ko.wikipedia.org/wiki/레이디언_8500 "wikilink") 와서, ATI 측은, "빠른 Z 청소" 기술이 없었을 때보다 64배가량 빠르게 Z-버퍼를 "청소"할 수 있었노라고 주장하였다.
  - **계층적 Z-버퍼**() — 렌더링하고자 하는 픽셀(pixel)이 실제로 렌더링 파이프라인(들)에 도착하기 전에, 미리 그 픽셀에 대한 [Z-버퍼](https://ko.wikipedia.org/wiki/Z-버퍼 "wikilink")를 첵크(check)할 수 있도록 해 준다. 그릴 필요가 없는 픽셀은 빨리 제외해버릴 수 있다. (이른바 이른 Z 거부, )

## 각주

## 외부 링크

  - [Anandtech's Preview of Radeon 256](http://www.anandtech.com/showdoc.aspx?i=1230)

  - [ATI glossary entry](http://ati.com/companyinfo/glossary/includes/list.html#hz)

  - [Beyond3D's explanation of HyperZ from Radeon 8500](http://www.beyond3d.com/reviews/ati/radeon8500p2/index4.php)

  - [Tom's Hardware Guide pages matching "HyperZ"](http://www17.tomshardware.com/search/search.html?category=all&words=HyperZ)

[분류:AMD 기술](https://ko.wikipedia.org/wiki/분류:AMD_기술 "wikilink") [분류:ATI 테크놀로지스](https://ko.wikipedia.org/wiki/분류:ATI_테크놀로지스 "wikilink") [분류:그래픽 카드](https://ko.wikipedia.org/wiki/분류:그래픽_카드 "wikilink")

1.
2.