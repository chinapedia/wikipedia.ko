> This article is converted from Wikipedia: [YCgCo](https://ko.wikipedia.org/wiki/YCgCo).


**YCgCo** (또는 *YCoCg*) 색상 모형은 휘도 Y, 녹색 색차 CG 및 주황색 색차 CO로 구성된 [색공간](https://ko.wikipedia.org/wiki/색공간 "wikilink")이다. 다른 색상 모형들보다 각 색평면 사이에 상관성이 매우 낮기 때문에 [H.264/MPEG-4 AVC](https://ko.wikipedia.org/wiki/H.264/MPEG-4_AVC "wikilink") 및 [디랙](../Page/디랙_\(코덱\).md "wikilink")\[1\] 등에 채용된 바 있다. [섬네일](https://ko.wikipedia.org/wiki/파일:Barns_grand_tetons_YCgCo_separation.jpg "wikilink")

## 다른 색상 모형과 비교

### RGB 색상 모형

YCgCo의 세 가지 값을 아래와 같은 방법으로 계산하여 RGB 색상 모형의 세 가지 값으로 바꿀 수 있다.

\[\begin{bmatrix} Y \\ Cg \\ Co \end{bmatrix}
=
\begin{bmatrix} 1/4  &  1/2  &  1/4\\
                -1/4 &  1/2  & -1/4\\
                1/2  &  0    & -1/2\end{bmatrix}
\cdot
\begin{bmatrix} R \\ G \\ B \end{bmatrix}\] 휘도 Y 값의 범위는 0부터 1까지이며 색차 CG와 색차 CO 값의 범위는 -0.5부터 0.5까지이다. 예를 들어 원색 빨강을 표현할 때 RGB 시스템에서는 \((1,0,0)\)이며 YCgCo 시스템에서는 \((\frac {1} {4},-\frac {1} {4},\frac {1} {2})\)로 표현된다.\[2\]\[3\]

YCgCo 색상 모형에서 RGB 색상 모형으로 변환하고자 할 때에는 역행렬을 써서 아래와 같이 계산한다:

\[\begin{bmatrix} R \\ G \\ B \end{bmatrix}
=
\begin{bmatrix} 1  &  -1  & 1\\
                1  &  1  &  0\\
                1  & -1  & -1\end{bmatrix}
\cdot
\begin{bmatrix} Y \\ Cg \\ Co \end{bmatrix}\] 따라서 덧셈 연산 두 번과 뺄셈 연산 두 번만 하면 변환이 끝난다. 분모를 따로 사용할 필요도 없기 때문에 정수 덧셈과 뺄셈만을 통해 효율적인 변환을 할 수 있다:

``` pascal
tmp := Y   − Cg;
R   := tmp + Co;
G   := Y   + Cg;
B   := tmp − Co;
```

### YCbCr 색상 모형

YCgCo 모형은 [YCbCr](../Page/YCbCr.md "wikilink") 색상 모형에 비해 계산이 더 간단하고 빠른 장점이 있으며 색상 계층 사이의 상관성도 더욱 낮다.\[4\]\[5\]

## 문헌

  - Tilo Strutz: *Bilddatenkompression. Grundlagen, Codierung, Wavelets, JPEG, MPEG, H.264* 4. Auflage, Vieweg+Teubner 2009, (Print), (Online)

YCgCo 색상 모형에 관련된 연구:

  - H. Malvar, G. Sullivan, *YCoCg-R: A color space with RGB reversibility and low dynamic range.* ISO/IEC JTC1/SC29/WG11 and ITU-T SG16 Q.6, Document JVT-I014, 2003.
  - S. Sun: *Residual Color Transform Using YCoCg-R.* ISO/IEC JTC1/SC29/WG11 and ITU-T Q6/SG16, Document JVT-L014, March 2004.
  - Woo-Shik Kim, Dmitry Birinov, Dae-Sung Cho, Hyun Mun Kim (Multimedia Lab, Samsung AIT); Video Coding Experts Group (VCEG): *Enhancements to RGB coding in H.264/MPEG-4 AVC FRExt*. Proposal, 26th Meeting: Busan, KR, 16–22. April 2005 ([ITU Document VCEG-Z16](https://web.archive.org/web/20150125081948/http://wftp3.itu.int/av-arch/video-site/0504_Bus/VCEG-Z16.doc), doc)
  - P. Agawane, K.R. Rao (Multimedia Processing Lab, University of Texas at Arlington): *Implementation and evaluation of residual color transform for 4:4:4 lossless RGB coding.* International Conference on Recent Advances in Communication Engineering, Hyderabad, India. 20-23 December 2008. ([ppt](https://web.archive.org/web/20100704085151/http://www-ee.uta.edu/dip/Research_Files/MPL/Research/RecentResearch/Pooja.ppt))

## 참조

[분류:색 공간](https://ko.wikipedia.org/wiki/분류:색_공간 "wikilink")

1.
2.
3.
4.
5.