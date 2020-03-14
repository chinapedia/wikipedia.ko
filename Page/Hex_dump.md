> This article is converted from Wikipedia: [Hex dump](https://ko.wikipedia.org/wiki/Hex_dump).


[thumb의](https://ko.wikipedia.org/wiki/파일:Wikipedia_favicon_hexdump.svg "wikilink") hex dump\]\] **hex dump**는 램 또는 파일이나 저장장치에 있는 컴퓨터 데이터의 [십육진법](https://ko.wikipedia.org/wiki/십육진법 "wikilink")적인 보임새이다. 데이터의 hex dump를 보는 것은 주로 [디버깅이나](https://ko.wikipedia.org/wiki/디버그 "wikilink") [리버스 엔지니어링의](https://ko.wikipedia.org/wiki/리버스_엔지니어링 "wikilink") 한 부분이다.

hex dump에서, 각 바이트는 2 숫자의 16진법 수로 표현된다. Hex dumps는 주로 8 또는 16바이트의 행으로 조직되며, 가끔은 흰 공간으로 분리된다. 몇몇 hex dump들은 시작에서나 마지막 라인의 [체크섬](https://ko.wikipedia.org/wiki/체크섬 "wikilink") 바이트에서 16진법의 [메모리 주소를](https://ko.wikipedia.org/wiki/메모리_주소 "wikilink") 갖는다.

비록 이름은 16 기반 출력을 암시하지만, 몇몇 덤핑 소프트웨어는 8 기반이나 10 기반 출력도 갖는다. 이 프로그램 기능을 갖는 흔한 이름으로, **hexdump**, **od**, **xxd** 그리고 단순히 **dump** 또는 심지어 **D**도 있다.

## 샘플

[유닉스](https://ko.wikipedia.org/wiki/유닉스 "wikilink") 프로그램에서 생성된 hex dump 샘플의 한 부분.

` 00105e0 e6b0 343b 9c74 0804 e7bc 0804 e7d5 0804`
` 00105f0 e7e4 0804 e6b0 0804 e7f0 0804 e7ff 0804`
` 0010600 e80b 0804 e81a 0804 e6b0 0804 e6b0 0804`

그러나 위의 예시는 [바이트 순서가](https://ko.wikipedia.org/wiki/엔디언 "wikilink") 불확실하기 때문에 hex dump의 모호한 형태를 대표한다. 이러한 hex dump들은 잘 알려진 표준의 문맥에서만 좋다. 또는 아래 처럼 값들이 의도적으로 전체 형태가 주어진 경우.

` 00105e0 e6 b008 04e79e08 04e7bc 08 04 e7 d50804`

명백한 바이트 순서가 요구되는 경우, (예를 들면 [기계어](https://ko.wikipedia.org/wiki/기계어 "wikilink") 프로그램의 hex dump나 [ROM의](https://ko.wikipedia.org/wiki/고정_기억_장치 "wikilink") 내용 같이) byte-by-byte 표시가 선호된다. (주로 16바이트 행들로 조직된다.)

` 00105e0 e6 b0 08 04 e7 9e 08 04-e7 bc 08 04 e7 d5 08 04`
` 00105f0 e7 e4 08 04 e6 b0 08 04-e7 f0 08 04 e7 ff 08 04`
` 0010600 e8 0b 08 04 e8 1a 08 04-e6 b0 08 04 e6 b0 08 04`

값 사이의 공백 없이 거의 요약되지 않은 형태도 사용된다. 

` 00105e0 e6b00804e79e0804e7bc0804e7d50804`
` 00105f0 e7e40804e6b00804e7f00804e7ff0804`
` 0010600 e80b0804e81a0804e6b00804e6b00804`

x86 컴퓨터에서, 같은 바이트들이 유닉스에서는 기본 화면으로 아래와 같이 나온다.

` 00105e0 b0e6 0408 9ee7 0408 bce7 0408 d5e7 0408`
` 00105f0 e4e7 0408 b0e6 0408 f0e7 0408 ffe7 0408`
` 0010600 0be8 0408 1ae8 0408 b0e6 0408 b0e6 0408`

종종 상응하는 [아스키](https://ko.wikipedia.org/wiki/아스키 "wikilink") 코드를 변환해서 보여주는 추가적인 열이 보일 수 있다. (예를 들어 hexdump -C 또는 hd):

``` hexdump
0000: 57 69 6B 69 70 65 64 69 61 2C 20 74 68 65 20 66  Wikipedia, the f
0010: 72 65 65 20 65 6E 63 79 63 6C 6F 70 65 64 69 61  ree encyclopedia
0020: 20 74 68 61 74 20 61 6E 79 6F 6E 65 20 63 61 6E   that anyone can
0030: 20 65 64 69 74 00 00 00 00 00 00 00 00 00 00 00   edit...........
```

## 체크섬

hex dump들이 손수 컴퓨터에 입력되는 경우,  들어온 경우, [체크섬](https://ko.wikipedia.org/wiki/체크섬 "wikilink") 바이트가 추가될 수 있다. 이것은 사용자가 각 행을 정확히 입력했는지 알 수 있게 도와준다.

## 똑같은 라인들의 압축

유닉스 프로그램인 **od**와 **hexdump**에서, 표시되는 모든 라인들이 보이는 것과 같은 출력을 가지는 것은 아니다. \*는 두 0 블록들 사이가 모두 0이라는 말이다.

` 0000000 0000 0000 0000 0000 0000 0000 0000 0000`
` *`
` 0000030`

이러한 압축 특징은 큰 파일이나 복잡한 장치를 볼 때 유용한 도구가 될 수 있다. 현대의 리눅스에서, 모두 비어 있다면 전체 하드 드라이브를 스캔하는 것을 편리하게 할 수 있다.

` # hexdump /dev/sda (replace sda with the proper name for the device to be scanned)`

\-v 옵션은 **hexdump**와 **od**이 모든 입력 데이터를 보이게 한다.

` 0000000 0000 0000 0000 0000 0000 0000 0000 0000`
` 0000010 0000 0000 0000 0000 0000 0000 0000 0000`
` 0000020 0000 0000 0000 0000 0000 0000 0000 0000`

## 외부 링크

  - [hexdump](http://www.oreillynet.com/linux/cmd/cmd.csp?path=h/hexdump) Linux in a Nutshell
  - [Manual on How to Use the Hexdump Unix Utility](http://256.com/gray/docs/misc/hexdump_manual_how_to.html) Argument Description
  - [Doing a Reverse Hex Dump](http://www.linuxjournal.com/content/doing-reverse-hex-dump) using xxd command
  - [hdr](https://metacpan.org/release/Data-HexDump-Range) Hexdump with colored ranges to ease visualization. Options to skip data, displaying bitfields, complex range definition, ... follow the link to 'hdr_examples.pod'.
  - \[<https://metacpan.org/pod/Data>::HexDump::Range <Data::HexDump>::Range\] Module used by the hdr command. Use it to create applications that display complex binary data.
  - [hexd](http://www.ioplex.com/~miallen/libmba/) Hexdump with colored ranges application part of libma.
  - [Hex cheatsheet](http://www.hex-codes.com) for looking up byte-nibbles and nibble-bits.
  - RFC 4194 "The S Hexdump Format"

[분류:디버깅](https://ko.wikipedia.org/wiki/분류:디버깅 "wikilink")