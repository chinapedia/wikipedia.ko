> This article is converted from Wikipedia: [XDCAM](https://ko.wikipedia.org/wiki/XDCAM).


**XDCAM**은 테이프가 없는 전문 비디오 시스템으로 [소니](../Page/소니.md "wikilink")가 2003년에 도입하였다. 처음 두 세대, XDCAM과 XDCAM HD는 [프로페셔널 디스크](https://ko.wikipedia.org/wiki/프로페셔널_디스크 "wikilink")(PFD)를 기록 매체로 이용한다. 이 디스크는 [블루레이 디스크와](https://ko.wikipedia.org/wiki/블루레이_디스크 "wikilink") 비슷하며 23 기가바이트의 데이터(PFD23, 단면) 또는 50 기가바이트의 데이터(PFD50, 양면)를 담을 수 있다. 3세대 XCDCAM EX는 솔리드 스테이트 SxS 카드를 사용한다. 2008년 11월에 [JVC](../Page/JVC.md "wikilink")는 XDCAM EX 포맷을 지원하기로 소니와 계약을 맺었다.

## 압축 방식

XDCAM 포맷은 여러 가지 압축 방식과 포맷을 사용한다. 대부분의 SD급 XDCAM 캠코더들은 IMX에서 DVCAM까지 스위치를 통해 변경할 수 있지만 DVCAM 전용 모델과 IMX 전용 모델에서만 사용할 수 있다.

  - IMX (MPEG IMX)
  - DVCAM (DV25)
  - XDCAM HD (XDCAM HD420, MPEG HD420)
  - XDCAM HD422 (MPEG HD422)
  - 프록시 스트림

## 녹화 포맷

<table>
<caption>XDCAM 포맷</caption>
<thead>
<tr class="header">
<th><p>포맷 이름</p></th>
<th><p>용기</p></th>
<th><p>비디오 코딩</p></th>
<th><p>비트 깊이</p></th>
<th><p>컬러 샘플링</p></th>
<th><p>프레임 크기</p></th>
<th><p>프레임 속도 및 주사 형태</p></th>
<th><p>비디오 비트 레이트 (M비트/초)</p></th>
<th><p>오디오 코딩</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>DVCAM</p></td>
<td><p>MXF,<br />
DV-AVI</p></td>
<td><p>DV</p></td>
<td><p>8</p></td>
<td><p>4:2:0</p></td>
<td><p>720x576</p></td>
<td><p>25i, 25p</p></td>
<td><p>25 (CBR)</p></td>
<td><p>PCM 4 채널/16 비트/48 kHz</p></td>
</tr>
<tr class="even">
<td><p>4:1:1</p></td>
<td><p>720x480</p></td>
<td><p>29.97i, 29.97p</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>MPEG IMX</p></td>
<td><p>MXF</p></td>
<td><p>MPEG-2 422P@ML</p></td>
<td><p>8</p></td>
<td><p>4:2:2</p></td>
<td><p>720x576</p></td>
<td><p>25i, 25p</p></td>
<td><p>30 (CBR), 40 (CBR), 50(CBR)</p></td>
<td><p>PCM 8 채널/16 비트/48 kHz,<br />
또는 4 채널/24 비트/48 kHz</p></td>
</tr>
<tr class="even">
<td><p>720x480</p></td>
<td><p>29.97i, 29.97p, 23.98p</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>MPEG HD</p></td>
<td><p>MXF,<br />
MP4</p></td>
<td><p>MPEG-2 MP@H14/HL</p></td>
<td><p>8</p></td>
<td><p>4:2:0</p></td>
<td><p>1920x1080</p></td>
<td><p>29.97i, 25i, 29.97p, 25p, 23.98p</p></td>
<td><p>35 (VBR)</p></td>
<td><p>PCM 4 채널/16 비트/48 kHz</p></td>
</tr>
<tr class="even">
<td><p>1440x1080</p></td>
<td><p>29.97i, 29.97p, 23.98p (pulldown), 25p</p></td>
<td><p>18 (VBR), 25 (CBR), 35 (VBR)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>1280x720</p></td>
<td><p>59.94p, 29.97p, 23.98p, 50p, 25p</p></td>
<td><p>25 (CBR), 35 (VBR), 19 (CBR)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>MPEG HD422</p></td>
<td><p>MXF</p></td>
<td><p>MPEG-2 422P@HL</p></td>
<td><p>8</p></td>
<td><p>4:2:2</p></td>
<td><p>1920x1080</p></td>
<td><p>29.97i, 25i, 29.97p, 25p, 23.98p</p></td>
<td><p>50 (CBR)</p></td>
<td><p>PCM 8 채널/16 비트/48 kHz,<br />
또는 4 채널/24 비트/48 kHz</p></td>
</tr>
<tr class="odd">
<td><p>1280x720</p></td>
<td><p>59.94p, 50p, 23.98p (pulldown)</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>프록시 AV</p></td>
<td><p>?</p></td>
<td><p>MPEG-4 Part-2 (ASP)</p></td>
<td><p>8</p></td>
<td><p>4:2:0</p></td>
<td><p>CIF (50i - 352x288)</p></td>
<td><p>?</p></td>
<td><p>1.5</p></td>
<td><p>A-Law 4 채널/8 비트/8 kHz</p></td>
</tr>
</tbody>
</table>

## 같이 보기

  - [HDCAM](../Page/HDCAM.md "wikilink")

## 참조

  - [XDCAM 기술과 미래에 대한 공식 정보](https://web.archive.org/web/20120416135609/http://www.sony.co.jp/SonyInfo/technology/technology/theme/xdcam_01.html)
  - [소니의 공식 XDCAM 웹 사이트](https://web.archive.org/web/20080422223805/http://bssc.sel.sony.com/BroadcastandBusiness/markets/10014/xdcam_index.shtml)

## 외부 링크

  - [XDCAM 프로 사용자 그룹](https://web.archive.org/web/20080918183703/http://xdcam.com.au/modules/news/)

[분류:영상 저장 매체](https://ko.wikipedia.org/wiki/분류:영상_저장_매체 "wikilink")