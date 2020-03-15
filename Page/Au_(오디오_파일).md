> This article is converted from Wikipedia: [Au \( \)](https://ko.wikipedia.org/wiki/Au_\(_\)).


**Au 파일 포맷**은 [선 마이크로시스템즈이](https://ko.wikipedia.org/wiki/선_마이크로시스템즈 "wikilink") 개발한 [오디오 파일 포맷이다](../Page/오디오_파일_포맷.md "wikilink"). Au 포맷은 [NeXT](../Page/NeXT.md "wikilink") 시스템과 초기 웹페이지에서 널리 사용되었다. 원래 헤더 파일이 없었으며 8000 Hz의 [샘플링 레이트에](https://ko.wikipedia.org/wiki/샘플링_레이트 "wikilink") 8비트 [µ-law방식으로](https://ko.wikipedia.org/wiki/뮤_법칙_알고리즘 "wikilink") 인코딩되었으나, 다른 기업들의 하드웨어에서 비디오 신호의 정수 요소로서 8192 Hz의 샘플링 레이트를 사용하기 시작했다. 현재 사용되는 파일들은 여섯 [unsigned](https://ko.wikipedia.org/wiki/unsigned "wikilink") 32비트로 작성된 헤더 파일을 가진다.

이 포맷은 현재 다양한 [오디오 인코딩](https://ko.wikipedia.org/wiki/디지털_오디오 "wikilink") 포맷을 지원하지만 [µ-law](https://ko.wikipedia.org/wiki/뮤_법칙_알고리즘 "wikilink") 로그 부호화와 관련이 있다. 이 부호화는, [썬OS](https://ko.wikipedia.org/wiki/썬OS "wikilink")가 /dev/audio 인터페이스를 통해 이 부호화를 응용 프로그램에 노출시키던 [SPARCstation 1](https://ko.wikipedia.org/wiki/SPARCstation_1 "wikilink") 하드웨어에서 유래되었다. 이 부호화와 인터페이스는 [유닉스](https://ko.wikipedia.org/wiki/유닉스 "wikilink") 운영체제 소리의 [데 팍토](https://ko.wikipedia.org/wiki/데_팍토 "wikilink") 표준이 되었다.

## 새 포맷

모든 필드는 샘플 데이터와 함께 [엔디언](../Page/엔디언.md "wikilink") 포맷으로 저장되어 있다.

{{-}}

<table>
<thead>
<tr class="header">
<th><p>32 비트 워드 (unsigned)</p></th>
<th><p>필드</p></th>
<th><p>설명/내용 <a href="https://ko.wikipedia.org/wiki/C_(프로그래밍_언어)" title="wikilink">C</a> 주석 내의 <a href="https://ko.wikipedia.org/wiki/16진법" title="wikilink">16진수</a> |- valign = top</p></th>
<th><p>0</p></th>
<th><p><a href="https://ko.wikipedia.org/wiki/마법의_숫자(프로그래밍)" title="wikilink">마법의 숫자</a></p></th>
<th><p>값 <code>0x2e736e64</code> ( ASCII 네 문자 ".snd") |- valign = top</p></th>
<th><p>1</p></th>
<th><p>데이터 오프셋</p></th>
<th><p>바이트로 된 데이터의 오프셋이며 8로 나눌 수 있어야 한다. 이것은 추가 정보에 대한 공백이 없는 헤더 길이(여섯 32 비트 워드)이기 때문에 최소 유효 숫자는 24(십진법)이다. 현재 주석 필드이 있는 최소 유효 숫자는 32(십진법)이다. |- valign = top</p></th>
<th><p>2</p></th>
<th><p>데이터 사이즈</p></th>
<th><p>바이트로 된 데이터 사이즈. 모를 경우, 값 <code>0xffffffff</code>을 사용해야 함. |- valign = top</p></th>
<th><p>3</p></th>
<th><p>인코딩</p></th>
<th><p>데이터 인코딩 포맷:</p>
<ul>
<li>1 = 8-bit <a href="https://ko.wikipedia.org/wiki/G.711" title="wikilink">G.711</a> <a href="https://ko.wikipedia.org/wiki/mu-law_알고리즘" title="wikilink">µ-law</a></li>
<li>2 = 8-bit 선형 <a href="../Page/펄스_부호_변조.md" title="wikilink">PCM</a></li>
<li>3 = 16-bit 선형 <a href="../Page/펄스_부호_변조.md" title="wikilink">PCM</a></li>
<li>4 = 24-bit 선형 <a href="../Page/펄스_부호_변조.md" title="wikilink">PCM</a></li>
<li>5 = 32-bit 선형 <a href="../Page/펄스_부호_변조.md" title="wikilink">PCM</a></li>
<li>6 = 32-bit <a href="https://ko.wikipedia.org/wiki/IEEE_부동_소수점_표준" title="wikilink">IEEE 고정 소수점</a></li>
<li>7 = 64-bit <a href="https://ko.wikipedia.org/wiki/IEEE_부동_소수점_표준" title="wikilink">IEEE 고정 소수점</a></li>
<li>8 = 조각난 샘플링 데이터</li>
<li>9 = DSP 프로그램</li>
<li>10 = 8 비트 <a href="https://ko.wikipedia.org/wiki/고정_소수점" title="wikilink">고정 소수점</a></li>
<li>11 = 16 비트 <a href="https://ko.wikipedia.org/wiki/고정_소수점" title="wikilink">고정 소수점</a></li>
<li>12 = 24 비트 <a href="https://ko.wikipedia.org/wiki/고정_소수점" title="wikilink">고정 소수점</a></li>
<li>13 = 32 비트 <a href="https://ko.wikipedia.org/wiki/고정_소수점" title="wikilink">고정 소수점</a></li>
<li>18 = 16 비트 linear with emphasis</li>
<li>19 = 16 비트 linear compressed</li>
<li>20 = 16 비트 linear with emphasis and compression</li>
<li>21 = Music kit DSP commands</li>
<li>23 = 4 비트 ISDN <a href="https://ko.wikipedia.org/wiki/mu-law_알고리즘" title="wikilink">u-law</a> compressed using the <a href="https://ko.wikipedia.org/wiki/G.726" title="wikilink">ITU-T G.721</a> <a href="https://ko.wikipedia.org/wiki/ADPCM" title="wikilink">ADPCM</a> 음성 데이터 인코딩 스킴</li>
<li>24 = <a href="https://ko.wikipedia.org/wiki/G.722" title="wikilink">ITU-T G.722</a> <a href="https://ko.wikipedia.org/wiki/ADPCM" title="wikilink">ADPCM</a></li>
<li>25 = <a href="https://ko.wikipedia.org/wiki/G.723" title="wikilink">ITU-T G.723</a> 3-bit <a href="https://ko.wikipedia.org/wiki/ADPCM" title="wikilink">ADPCM</a></li>
<li>26 = <a href="https://ko.wikipedia.org/wiki/G.723" title="wikilink">ITU-T G.723</a> 5-bit <a href="https://ko.wikipedia.org/wiki/ADPCM" title="wikilink">ADPCM</a></li>
<li>27 = 8-bit <a href="https://ko.wikipedia.org/wiki/G.711" title="wikilink">G.711</a> <a href="https://ko.wikipedia.org/wiki/A-law_알고리즘" title="wikilink">A-law</a></li>
</ul>
<p>|- valign = top</p></th>
<th><p>4</p></th>
<th><p>샘플링 레이트</p></th>
<th><p>초당 샘플링 수 |- valign = top</p></th>
<th><p>5</p></th>
<th><p>채널</p></th>
<th><p>인터리브된 채널 수. e.g., 1은 모노, 2는 스테레오; 더 많은 채널 수도 가능하나, 재생 기기에서 지원하지 않을 수도 있다.</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

부호화의 종류는 '부호화(인코딩) 필드' 값이 결정한다(워드 3의 헤더). 포맷 2에서 7은 비압축 [PCM](https://ko.wikipedia.org/wiki/PCM "wikilink")이므로 [무손실 압축이다](https://ko.wikipedia.org/wiki/무손실_압축 "wikilink"). 포맷 23에서 26은 대략 4:1의 손실 압축인 ADPCM이다. 포맷 1부터 27은 각각 μ-법칙과 A-법칙 알고리즘이며 둘 다 손실 압축이다. 몇몇 다른 것들은 [NeXT](../Page/NeXT.md "wikilink") [뮤직 키트](https://ko.wikipedia.org/wiki/뮤직_키트_\(소프트웨어\) "wikilink") 소프트웨어로 처리하도록 설계된 DSP 명령 혹은 데이터이다.

## 같이 보기

  - [WAV](../Page/WAV.md "wikilink")
  - [AIFF](../Page/AIFF.md "wikilink")
  - [오디오 파일 포맷](../Page/오디오_파일_포맷.md "wikilink")

## 외부 링크

  - [샘플 .AU 파일](http://www.nch.com.au/acm/sample.au)
  - [Sun .au 소리 파일 형식](https://web.archive.org/web/20110514220509/http://www.opengroup.org/public/pubs/external/auformat.html)

<!-- end list -->

  - [Au 파일 포맷에 대한 세부 정보](http://www-mmsp.ece.mcgill.ca/Documents/AudioFormats/AU/AU.html)

[분류:오디오 파일 포맷](https://ko.wikipedia.org/wiki/분류:오디오_파일_포맷 "wikilink")