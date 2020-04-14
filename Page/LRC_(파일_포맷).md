> This article is converted from Wikipedia: [LRC \(파일 포맷\)](https://ko.wikipedia.org/wiki/LRC_\(파일_포맷\)).


**LRC**는 [MP3](https://ko.wikipedia.org/wiki/MP3 "wikilink")나 [OGG](../Page/Vorbis.md "wikilink"), [MIDI](../Page/MIDI.md "wikilink")와 같은 음악 파일과 동시에 동작되는 [노랫말](https://ko.wikipedia.org/wiki/노랫말 "wikilink")을 담은 [파일 확장자이다](../Page/파일_확장자.md "wikilink"). .lrc로 된 확장자를 사용하며 일반적으로 그 음악 파일과 동일한 이름으로 존재한다. 예를 들면 ***노래.mp3***와 ***노래.lrc*** 식으로 존재한다. LRC 포맷은 텍스트를 기반으로 하고 있으며 자막 파일과 비슷하다.

## 파일 포맷

### 심플 포맷

**심플 LRC 포맷**은 Kuo (Djohan) Shiang-shiang's Lyrics Displayer에 의해 설명되었는데, 이것은 [가라오케](../Page/가라오케.md "wikilink") 성능을 시뮬레이션화 하기 위해 첫 번째로 시도된 프로그램이었다. 이 프로그램은 일반적으로 가사의 전체 행을 표시하지만, 각 단어마다 표시하는게 아니라 각 행에 하나의 태그를 생성해 주면 노래방 기계에서 볼 법한 한번에 한 단어를 표시할 수 있었다.

각 줄의 시간 태그 방식은 **\[mm:ss.xx\]** 방식으로 표시하는데 여기서 **mm**은 분, **ss**는 초, **xx**는 100분의 1초다. 이 때 xx는 [밀리초](https://ko.wikipedia.org/wiki/밀리초 "wikilink")가 아니다.

  - **일반적인 예시 :**

`[00:12.00]첫 번째 가사 행`
`[00:17.20]두 번째 가사 행`
`[00:21.10]세 번째 가사 행`
`...`
`[mm:ss.xx]마지막 가사 행`

**ID태그**일부 플레이어가 무시하거나 가사전에 표시할 수 있음.

`[ar:`*`가사``   ``아티스트`*`]`
` [al:`*`노래의``   ``앨범`*`]`
` [ti:`*`가사(노래)``   ``제목`*`]`
` [au:`*`가사``   ``작성자`*`]`
`[length:`*`음악의``   ``길이`*`]`
`[by:`*`LRC파일의``   ``작성자`*`]`
` [offset:`*`+/-``   ``ms단위로``   ``전체``   ``오브셋조정`*`]`
` [re:`*`LRC를``   ``작성한``   ``플레이어나``   ``편집기`*`]`
` [ve:`*`프로그렘``   ``버전`*`]`

### 강화 포맷

**강화된 LRC 포맷**은 A2 미디어 플레이어의 디자이너에 의해 개발된 심플 LRC 포맷의 확장 버전이다. 이것은 **\<mm:ss.xx\>** 방식으로 각 단어 및 시간을 태그해 추가한다.

  - **강화된 LRC 포맷의 예시 :**

`[mm:ss.xx] <mm:ss.xx> 첫 번째 줄 첫 번째 가사 <mm:ss.xx> 첫 번째 줄 두 번째 가사 <mm:ss.xx> ... 첫 번째 줄 마지막 가사 <mm:ss.xx>`
`[mm:ss.xx] <mm:ss.xx> 두 번째 줄 첫 번째 가사 <mm:ss.xx> 두 번째 줄 두 번째 가사 <mm:ss.xx> ... 두 번째 줄 마지막 가사 <mm:ss.xx>`
`...`
`[mm:ss.xx] <mm:ss.xx> 마지막 줄 첫 번째 가사 <mm:ss.xx> 마지막 줄 두 번째 가사 <mm:ss.xx> ... 마지막 줄 마지막 가사 <mm:ss.xx>`

## 같이 보기

  - [SAMI](../Page/SAMI.md "wikilink")

[분류:오디오 파일 포맷](https://ko.wikipedia.org/wiki/분류:오디오_파일_포맷 "wikilink")