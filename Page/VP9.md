> This article is converted from Wikipedia: [VP9](https://ko.wikipedia.org/wiki/VP9).


**VP9** [구글](../Page/구글.md "wikilink")이 인수한 On2 테크놀로지스의 [로열티 프리](https://ko.wikipedia.org/wiki/로열티_프리 "wikilink")\[1\] [영상 코덱](../Page/코덱.md "wikilink") 중 하나이다.

## 개요

2013년 [VP8](https://ko.wikipedia.org/wiki/VP8 "wikilink")이 포함되어 있는 [WebM](../Page/WebM.md "wikilink")의 후속 동영상 압축 기술로 발표 되었다. 비슷한 시기에 발표된 [고효율 비디오 코딩과](../Page/고효율_비디오_코딩.md "wikilink") 비교하면, 화질은 다소 떨어지나 스트리밍 환경에는 더 안정적이다고 알려져 있다\[2\].

## 기능

### 프로파일

  - 프로파일 0: [색 심도](https://ko.wikipedia.org/wiki/색_심도 "wikilink"): 8 bit/sample, [chroma subsampling](../Page/크로마_서브샘플링.md "wikilink"): 4:2:0
  - 프로파일 1: 색 심도: 8 bit, chroma subsampling: 4:2:2, 4:4:0, 4:4:4
  - 프로파일 2: 색 심도: 10–12 bit, chroma subsampling: 4:2:0
  - 프로파일 3: 색 심도: 10–12 bit, chroma subsampling: 4:2:2, 4:4:0, 4:4:4\[3\]

### 레벨

VP9는 14개 레벨을 제공한다:\[4\]

<table>
<thead>
<tr class="header">
<th><p>레벨<br />
</p></th>
<th><p>Luma Samples/s</p></th>
<th><p>Luma Picture Size</p></th>
<th><p>Max Bitrate (Mbit/s)</p></th>
<th><p>Max CPB Size for Visual Layer (MBits)</p></th>
<th><p>Min Compression Ratio</p></th>
<th><p>Max Tiles</p></th>
<th><p>Min Alt-Ref Distance</p></th>
<th><p>Max Reference Frames</p></th>
<th><p>해상도 @ 프레임레이트 예시</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p>829440</p></td>
<td><p>36864</p></td>
<td><p>0.20</p></td>
<td><p>0.40</p></td>
<td><p>2</p></td>
<td><p>1</p></td>
<td><p>4</p></td>
<td><p>8</p></td>
<td><p>256×144@15</p></td>
</tr>
<tr class="even">
<td><p>1.1</p></td>
<td><p>2764800</p></td>
<td><p>73728</p></td>
<td><p>0.80</p></td>
<td><p>1.0</p></td>
<td><p>2</p></td>
<td><p>1</p></td>
<td><p>4</p></td>
<td><p>8</p></td>
<td><p>384×192@30</p></td>
</tr>
<tr class="odd">
<td><p>2</p></td>
<td><p>4608000</p></td>
<td><p>122880</p></td>
<td><p>1.8</p></td>
<td><p>1.5</p></td>
<td><p>2</p></td>
<td><p>1</p></td>
<td><p>4</p></td>
<td><p>8</p></td>
<td><p>480×256@30</p></td>
</tr>
<tr class="even">
<td><p>2.1</p></td>
<td><p>9216000</p></td>
<td><p>245760</p></td>
<td><p>3.6</p></td>
<td><p>2.8</p></td>
<td><p>2</p></td>
<td><p>2</p></td>
<td><p>4</p></td>
<td><p>8</p></td>
<td><p>640×384@30</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>20736000</p></td>
<td><p>552960</p></td>
<td><p>7.2</p></td>
<td><p>6.0</p></td>
<td><p>2</p></td>
<td><p>4</p></td>
<td><p>4</p></td>
<td><p>8</p></td>
<td><p>1080×512@30</p></td>
</tr>
<tr class="even">
<td><p>3.1</p></td>
<td><p>36864000</p></td>
<td><p>983040</p></td>
<td><p>12</p></td>
<td><p>10</p></td>
<td><p>2</p></td>
<td><p>4</p></td>
<td><p>4</p></td>
<td><p>8</p></td>
<td><p>1280×768@30</p></td>
</tr>
<tr class="odd">
<td><p>4</p></td>
<td><p>83558400</p></td>
<td><p>2228224</p></td>
<td><p>18</p></td>
<td><p>16</p></td>
<td><p>4</p></td>
<td><p>4</p></td>
<td><p>4</p></td>
<td><p>8</p></td>
<td><p>2048×1088@30</p></td>
</tr>
<tr class="even">
<td><p>4.1</p></td>
<td><p>160432128</p></td>
<td><p>2228224</p></td>
<td><p>30</p></td>
<td><p>18</p></td>
<td><p>4</p></td>
<td><p>4</p></td>
<td><p>5</p></td>
<td><p>6</p></td>
<td><p>2048×1088@60</p></td>
</tr>
<tr class="odd">
<td><p>5</p></td>
<td><p>311951360</p></td>
<td><p>8912896</p></td>
<td><p>60</p></td>
<td><p>36</p></td>
<td><p>6</p></td>
<td><p>8</p></td>
<td><p>6</p></td>
<td><p>4</p></td>
<td><p>4096×2176@30</p></td>
</tr>
<tr class="even">
<td><p>5.1</p></td>
<td><p>588251136</p></td>
<td><p>8912896</p></td>
<td><p>120</p></td>
<td><p>46</p></td>
<td><p>8</p></td>
<td><p>8</p></td>
<td><p>10</p></td>
<td><p>4</p></td>
<td><p>4096×2176@60</p></td>
</tr>
<tr class="odd">
<td><p>5.2</p></td>
<td><p>1176502272</p></td>
<td><p>8912896</p></td>
<td><p>180</p></td>
<td><p>TBD</p></td>
<td><p>8</p></td>
<td><p>8</p></td>
<td><p>10</p></td>
<td><p>4</p></td>
<td><p>4096×2176@120</p></td>
</tr>
<tr class="even">
<td><p>6</p></td>
<td><p>1176502272</p></td>
<td><p>35651584</p></td>
<td><p>180</p></td>
<td><p>TBD</p></td>
<td><p>8</p></td>
<td><p>16</p></td>
<td><p>10</p></td>
<td><p>4</p></td>
<td><p>8192×4352@30</p></td>
</tr>
<tr class="odd">
<td><p>6.1</p></td>
<td><p>2353004544</p></td>
<td><p>35651584</p></td>
<td><p>240</p></td>
<td><p>TBD</p></td>
<td><p>8</p></td>
<td><p>16</p></td>
<td><p>10</p></td>
<td><p>4</p></td>
<td><p>8192×4352@60</p></td>
</tr>
<tr class="even">
<td><p>6.2</p></td>
<td><p>4706009088</p></td>
<td><p>35651584</p></td>
<td><p>480</p></td>
<td><p>TBD</p></td>
<td><p>8</p></td>
<td><p>16</p></td>
<td><p>10</p></td>
<td><p>4</p></td>
<td><p>8192×4352@120</p></td>
</tr>
</tbody>
</table>

## 같이 보기

  - [HTML5](../Page/HTML5.md "wikilink")
  - [WebP](../Page/WebP.md "wikilink")
  - [WebM](../Page/WebM.md "wikilink")

## 각주

## 외부 링크

  -
[분류:코덱](https://ko.wikipedia.org/wiki/분류:코덱 "wikilink") [분류:영상 코덱](https://ko.wikipedia.org/wiki/분류:영상_코덱 "wikilink") [분류:오픈 소스](https://ko.wikipedia.org/wiki/분류:오픈_소스 "wikilink") [분류:구글의 소프트웨어](https://ko.wikipedia.org/wiki/분류:구글의_소프트웨어 "wikilink") [분류:BSD 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:BSD_라이선스_소프트웨어 "wikilink") [분류:무손실 압축 알고리즘](https://ko.wikipedia.org/wiki/분류:무손실_압축_알고리즘 "wikilink") [분류:손실 압축 알고리즘](https://ko.wikipedia.org/wiki/분류:손실_압축_알고리즘 "wikilink") [분류:영상 압축](https://ko.wikipedia.org/wiki/분류:영상_압축 "wikilink") [분류:화상 통화](https://ko.wikipedia.org/wiki/분류:화상_통화 "wikilink")

1.  Janko Roettgers (Gigaom), January 2, 2014: [YouTube goes 4K, Google signs up long list of hardware partners for VP9 support](http://gigaom.com/2014/01/02/youtube-4k-streaming-vp9/)
2.
3.
4.