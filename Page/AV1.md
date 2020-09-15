> This article is converted from Wikipedia: [AV1](https://ko.wikipedia.org/wiki/AV1).


**AOMedia Video 1**(**AV1**)은 [오픈 포맷인](https://ko.wikipedia.org/wiki/오픈_포맷 "wikilink") [비디오](../Page/비디오.md "wikilink") [압축 포맷이다](https://ko.wikipedia.org/wiki/압축_포맷 "wikilink"). [Google](https://ko.wikipedia.org/wiki/Google "wikilink"), [Facebook](https://ko.wikipedia.org/wiki/Facebook "wikilink") 등이 참여하는 [Alliance for Open Media에서](https://ko.wikipedia.org/wiki/Alliance_for_Open_Media "wikilink") 만들었으며, 파일 포맷이 공개되어 있다. VP9, Daala, Thor 등을 계승한다.

## 프로파일과 레벨

### 프로파일

<table>
<caption>AV1 프로파일 간 비교</caption>
<thead>
<tr class="header">
<th></th>
<th><p>Main (0)</p></th>
<th><p>High (1)</p></th>
<th><p>Professional (2)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>비트 심도</p></td>
<td><p>8 또는 10비트</p></td>
<td><p>8 또는 10비트</p></td>
<td><p>8, 10 &amp; 12비트</p></td>
</tr>
<tr class="even">
<td><p>크로마 서브샘플링</p></td>
<td><p>4:0:0</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>4:2:0</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>4:2:2</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>4:4:4</p></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

### 레벨

| 레벨  | MaxPicSize (Samples) | MaxHSize (Samples) | MaxVSize (Samples) | MaxDisplayRate (Samples/sec) | MaxDecodeRate (Samples/sec) | MaxHeader Rate (/sec) | MainMbps (MBits/sec) | HighMbps (MBits/sec) | Min Comp Basis | Max Tiles | Max Tile Cols | 예시               |
| --- | -------------------- | ------------------ | ------------------ | ---------------------------- | --------------------------- | --------------------- | -------------------- | -------------------- | -------------- | --------- | ------------- | ---------------- |
| 2.0 | 147456               | 2048               | 1152               | 4,423,680                    | 5,529,600                   | 150                   | 1.5                  | \-                   | 2              | 8         | 4             | 426×240@30fps    |
| 2.1 | 278784               | 2816               | 1584               | 8,363,520                    | 10,454,400                  | 150                   | 3.0                  | \-                   | 2              | 8         | 4             | 640×360@30fps    |
| 3.0 | 665856               | 4352               | 2448               | 19,975,680                   | 24,969,600                  | 150                   | 6.0                  | \-                   | 2              | 16        | 6             | 854×480@30fps    |
| 3.1 | 1065024              | 5504               | 3096               | 31,950,720                   | 39,938,400                  | 150                   | 10.0                 | \-                   | 2              | 16        | 6             | 1280×720@30fps   |
| 4.0 | 2359296              | 6144               | 3456               | 70,778,880                   | 77,856,768                  | 300                   | 12.0                 | 30.0                 | 4              | 32        | 8             | 1920×1080@30fps  |
| 4.1 | 2359296              | 6144               | 3456               | 141,557,760                  | 155,713,536                 | 300                   | 20.0                 | 50.0                 | 4              | 32        | 8             | 1920×1080@60fps  |
| 5.0 | 8912896              | 8192               | 4352               | 267,386,880                  | 273,715,200                 | 300                   | 30.0                 | 100.0                | 6              | 64        | 8             | 3840×2160@30fps  |
| 5.1 | 8912896              | 8192               | 4352               | 534,773,760                  | 547,430,400                 | 300                   | 40.0                 | 160.0                | 8              | 64        | 8             | 3840×2160@60fps  |
| 5.2 | 8912896              | 8192               | 4352               | 1,069,547,520                | 1,094,860,800               | 300                   | 60.0                 | 240.0                | 8              | 64        | 8             | 3840×2160@120fps |
| 5.3 | 8912896              | 8192               | 4352               | 1,069,547,520                | 1,176,502,272               | 300                   | 60.0                 | 240.0                | 8              | 64        | 8             | 3840×2160@120fps |
| 6.0 | 35651584             | 16384              | 8704               | 1,069,547,520                | 1,176,502,272               | 300                   | 60.0                 | 240.0                | 8              | 128       | 16            | 7680×4320@30fps  |
| 6.1 | 35651584             | 16384              | 8704               | 2,139,095,040                | 2,189,721,600               | 300                   | 100.0                | 480.0                | 8              | 128       | 16            | 7680×4320@60fps  |
| 6.2 | 35651584             | 16384              | 8704               | 4,278,190,080                | 4,379,443,200               | 300                   | 160.0                | 800.0                | 8              | 128       | 16            | 7680×4320@120fps |
| 6.3 | 35651584             | 16384              | 8704               | 4,278,190,080                | 4,706,009,088               | 300                   | 160.0                | 800.0                | 8              | 128       | 16            | 7680×4320@120fps |

## 외부 링크

  -
[분류:영상 코덱](https://ko.wikipedia.org/wiki/분류:영상_코덱 "wikilink") [분류:화상 통화](https://ko.wikipedia.org/wiki/분류:화상_통화 "wikilink")