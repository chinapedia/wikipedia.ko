> This article is converted from Wikipedia: [M3U](https://ko.wikipedia.org/wiki/M3U).


**M3U**는 [멀티미디어](https://ko.wikipedia.org/wiki/멀티미디어 "wikilink") [재생목록](https://ko.wikipedia.org/wiki/재생목록 "wikilink")의 파일 포맷이다. [윈도우 미디어 플레이어](https://ko.wikipedia.org/wiki/윈도우_미디어_플레이어 "wikilink"), [아이튠즈](https://ko.wikipedia.org/wiki/아이튠즈 "wikilink"), [윈앰프](https://ko.wikipedia.org/wiki/윈앰프 "wikilink"), [알송](https://ko.wikipedia.org/wiki/알송 "wikilink") 등 대부분의 프로그램이 지원하고 있지만, 정식 사양은 존재하지 않고 대응 상황은 각각 다르다.

## 포맷

M3U 파일은, 하나, 또는 여러 개의 미디어 파일의 [패스를](https://ko.wikipedia.org/wiki/디렉토리 "wikilink") [플레인 텍스트](../Page/플레인_텍스트.md "wikilink")([텍스트 파일](https://ko.wikipedia.org/wiki/텍스트_파일 "wikilink"))로 기재한 것이다. 이 파일을. ".m3u" 또는 ".m3u8"의 확장자로 저장한다. M3U 파일의 인코딩은 [Windows-1252](https://ko.wikipedia.org/wiki/Windows-1252 "wikilink")의 경우가 많으나, [CP932](https://ko.wikipedia.org/wiki/CP932 "wikilink")에 대응하고 있는 것도 존재한다. 인코딩을 [UTF-8](https://ko.wikipedia.org/wiki/UTF-8 "wikilink")로 명시하였을 때, 확장자 M3U8를 사용한다.

각각의 엔트리는 아래와 같다.

  - 절대 경로(예시: C:\\My Music\\Heavysets.mp3)
  - 상대 경로 (예시: Heavysets.mp3)
  - [URL](https://ko.wikipedia.org/wiki/URL "wikilink")

M3U 파일에는 코멘트를 포함할 수가 있으며, `#` 이후가 코멘트가 된다.

M3U 포맷의 일반적인 사용방법으로 단일의 엔트리에 URL을 기재할 필요가 있다. 이 파일 덕분에, 스트리밍 액세스, 웹사이트에서의 다운로드, [인터넷 라디오의](https://ko.wikipedia.org/wiki/인터넷_라디오 "wikilink") 청취가 용이해진다.

[iOS](https://ko.wikipedia.org/wiki/iOS "wikilink")의 [HTTP 라이브 스트리밍](https://ko.wikipedia.org/wiki/HTTP_라이브_스트리밍 "wikilink") 포맷은 "M3U" and "M3U8" 파일을 기초로 하고 있다.

## Extended M3U

Extended M3U는 EXTM3U、확장M3U으로 불리는 것도 있다.

### 명령

**Extended M3U**(EXTM3U)로는 `#`는 확장 명령에도 사용된다.

  - \#EXTM3U - 머릿말. 파일의 선두에서만 기재한다.
  - \#EXTINF - 확장정보. 곡의 길이(초 단위), 타이틀 순으로 기재한다. 관례로 음악가명과 곡 제목은 `-`로 구분한다.

## 예시

  - 예시1

아래에 [윈도우에서의](https://ko.wikipedia.org/wiki/마이크로소프트_윈도우 "wikilink") 확장 M3U 파일의 예를 나타낸다. Sample.mp3와 Example.ogg는 이번에 사용할 미디어 파일이다. 123 및 321이라는 것은 길이를 초로 지정하고 있다. 지정할 미디어 파일이 스트리밍 파일인 경우, -1을 지정하는 것이 있다. 이것은 실제 길이를 알 수 없기에, 미리 정의하는 것이다. 길이 뒤의 값은 표시될 제목으로, 일반적으로 2번째 행에 적히는 파일의 경우와 비슷하다.

[OS X나](https://ko.wikipedia.org/wiki/OS_X "wikilink") [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink")로 사용할 경우는 [유닉스 패스를](https://ko.wikipedia.org/wiki/유닉스_패스 "wikilink") 사용한다.

`#EXTM3U`

`#EXTINF:123, Sample artist - Sample title`
`C:\Documents and Settings\I\My Music\Sample.mp3`

`#EXTINF:321,Example Artist - Example title`

`C:\Documents and Settings\I\My Music\Greatest Hits\Example.ogg`

  - 예시2

이 예시에서는 특정 디렉터리(예를 들면, [USB 플래시 드라이브나](https://ko.wikipedia.org/wiki/USB_플래시_드라이브 "wikilink") [CD-ROM](https://ko.wikipedia.org/wiki/CD-ROM "wikilink") 등)에 링크하는 M3U 파일의 작성방법을 나타낸다. M3U 파일로는 디렉터리의 경로 하나만 포함되지는 않는다. 개시후, 미디어 플레이어는 지정한 폴더에 있는 미디어 파일을 모두 재생한다.

`D:\Music`

  - 예시3

상대 경로를 사용한 예시도 나타낸다. M3U 파일은 음악 파일과 같은 디렉터리에 저장시킨다. 또, 하위 디렉터리가 사용되어 있을 경우, 재생 목록을 다른 디바이스에 이동시킨 후 그 디렉터리와 음악 파일도 마찬가지로 이동할 필요가 있다. 이 방법은 지정한 파일의 경로가 같게 할 필요가 없기 때문에 보다 유연하게 다룰 수 있다.

외와 같은 파일명`sample.m3u`으로 `C:\Documents and Settings\I\My Music\`에 저장한 경우를 예시로 나타낸다.

`#EXTM3U`

`#EXTINF:123, Sample artist - Sample title`
`Sample.mp3`

`#EXTINF:321,Example Artist - Example title`
`Greatest Hits\Example.ogg`

이 상대 경로로 기재하면 모든 파일을 디렉터리 구조를 유지한 채로 복사하면 다른 디바이스에서 그대로 사용할 수 있다.

  - 예시4

다음으로 상대 경로와 절대 경로 표기를 혼합한 예시를 나타낸다.

`Alternative\Band - Song.mp3`
`Classical\Other Band - New Song.mp3`
`Stuff.mp3`
`D:\More Music\Foo.mp3`
`..\Other Music\Bar.mp3`
`http://emp.cx:8000/Listen.pls`
`http://www.example.com/~user/Mine.mp3`

  - 주의

<!-- end list -->

  - Alternative와 Classical는 재생목록을 저장한 디렉터리의 하위 디렉터리.
  - "Song", "New Song"는 재생목록을 저장한 디렉터리의 하위 디렉터리에 저장되어있다.
  - "Stuff"는 재새목록을 저장한 디렉터리에 저장되어있다.
  - "Foo"는 윈도우의 특정 볼륨의 디렉터리에 있다. 어쩌면 재생목록이 저장되어 있는 디렉터리와 같을 지도 모른다.
  - "Bar"는 재생목록이 저장되어 있는 계층과 다른 디렉터리이다. `..\`는 하나 위의 디렉터리를 나타낸 것이기에, 이 하위 디렉터리인 `Bar`라는 디렉터리를 가리키고 있다.
  - "Listen"은 [샤우트캐스트](https://ko.wikipedia.org/wiki/샤우트캐스트 "wikilink")의 URL.
  - "Mine"는 웹 서버에 저장된 MP3 파일.

그 외의 M3U 파일로의 참조는 그다지 좋게 대응할 수 없다.

`AnotherPlayList.M3U`

아래의 예시는 [Mp3tag](https://ko.wikipedia.org/wiki/Mp3tag "wikilink")로 작성한 [앨리스 인 체인스의](https://ko.wikipedia.org/wiki/앨리스_인_체인스 "wikilink") EP반 [Jar of Flies의](https://ko.wikipedia.org/wiki/Jar_of_Flies "wikilink") M3U 파일이다.

`#EXTM3U`
`#EXTINF:419,Alice In Chains - Rotten Apple`
`Alice In Chains_Jar Of Flies_01_Rotten Apple.mp3`
`#EXTINF:260,Alice In Chains - Nutshell`
`Alice In Chains_Jar Of Flies_02_Nutshell.mp3`
`#EXTINF:255,Alice In Chains - I Stay Away`
`Alice In Chains_Jar Of Flies_03_I Stay Away.mp3`
`#EXTINF:256,Alice In Chains - No Excuses`
`Alice In Chains_Jar Of Flies_04_No Excuses.mp3`
`#EXTINF:157,Alice In Chains - Whale And Wasp`
`Alice In Chains_Jar Of Flies_05_Whale And Wasp.mp3`
`#EXTINF:263,Alice In Chains - Don't Follow`
`Alice In Chains_Jar Of Flies_06_Don't Follow.mp3`
`#EXTINF:245,Alice In Chains - Swing On This`
`Alice In Chains_Jar Of Flies_07_Swing On This.mp3`

## 같이 보기

  - [mp3tag](https://ko.wikipedia.org/wiki/mp3tag "wikilink")(M3U, EXTM3U)
  - [Advanced Stream Redirector](https://ko.wikipedia.org/wiki/Advanced_Stream_Redirector "wikilink") (ASX)
  - [PLS](https://ko.wikipedia.org/wiki/PLS_\(파일_포맷\) "wikilink")
  - [XSPF](https://ko.wikipedia.org/wiki/XSPF "wikilink")
  - [B4S](https://ko.wikipedia.org/wiki/B4S_\(파일_포맷\) "wikilink") - 윈앰프3 XML based playlist format
  - [윈도우 미디어 재생목록](https://ko.wikipedia.org/wiki/윈도우_미디어_재생목록 "wikilink")(WPL)

## 외부 링크

  - [A survey of playlist formats](http://gonze.com/playlists/playlist-format-survey.html) (Lucas Gonze, 2003년 11월 17일)
  - [M3U (WinAmp) Play List Specification](http://schworak.com/blog/e39/M3U-play-list-specification/)
  - [HTTP 라이브 스트리밍 (M3U 확장자)](http://tools.ietf.org/html/draft-pantos-http-live-streaming-08)

[분류:파일 포맷](https://ko.wikipedia.org/wiki/분류:파일_포맷 "wikilink")