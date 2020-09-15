> This article is converted from Wikipedia: [GIF](https://ko.wikipedia.org/wiki/GIF).


**그래픽 인터체인지 포맷**()는 [비트맵](https://ko.wikipedia.org/wiki/비트맵 "wikilink") [그래픽 파일 포맷이다](https://ko.wikipedia.org/wiki/그래픽_파일_포맷 "wikilink"). [1987년](../Page/1987년.md "wikilink") [컴퓨서브](https://ko.wikipedia.org/wiki/컴퓨서브 "wikilink")가 발표하였으며, [월드 와이드 웹에서](../Page/월드_와이드_웹.md "wikilink") 가장 널리 쓰이는 파일 포맷이기도 하다. 특별한 플러그인을 요구하지 않고 여러 환경에서 쉽게 쓸 수 있는 까닭에 다중 프레임 애니메이션을 이용한 배너 광고 등에 널리 쓰였으나, 수많은 웹사이트에서는 GIF 대신 어도비 플래시를 사용하기도 한다.

최대 256 색까지 저장할 수 있는 [비손실 압축](https://ko.wikipedia.org/wiki/비손실_압축 "wikilink") 형식이다. GIF에 쓰인 [LZW](../Page/LZW.md "wikilink") 알고리즘에 대한 [특허](../Page/특허.md "wikilink")를 [유니시스](../Page/유니시스.md "wikilink") 사가 가지고 있다는 것이 알려지고, 또한 256 색의 제한에 한계를 느끼면서 [PNG](../Page/PNG.md "wikilink")라는 새로운 표준이 개발되었다.

GIF는 지프()나 기프(), 또는 지아이에프로 읽는다. GIF 포맷의 저자는 **지프**로 읽는다고 밝혔으나\[1\], 기프라는 발음도 계속 쓰이고 있다. Rotating earth (large).gif 사람들은 GIF를 움짤 이라고 부르기도 한다

## 유니시스와 LZW 특허

GIF에 사용되는 [LZW](../Page/LZW.md "wikilink")알고리즘은 유니시스 사에 [미국 특허 4,558,302](http://patft.uspto.gov/netacgi/nph-Parser?patentnumber=4,558,302) 로 등록되어 있다. 컴퓨서브가 처음 GIF 포맷을 공개했을 때는 LZW 알고리즘에 특허가 있는 줄 몰랐다. [1994년](../Page/1994년.md "wikilink") 12월, 유니시스는 이 특허에 대해 특허료를 받는다고 공고했다. [1999년](../Page/1999년.md "wikilink") 8월에는 무료 소프트웨어와 그 사용자에게도 특허료를 받는다고 하여 많은 반발을 불러일으켰다.

[2003년](../Page/2003년.md "wikilink") [6월 20일](../Page/6월_20일.md "wikilink"), LZW 알고리즘에 대한 유니시스의 특허가 만료되었으며, 유럽, 일본, 캐나다에서의 특허는 [2004년](../Page/2004년.md "wikilink") [6월 18일](../Page/6월_18일.md "wikilink"), [6월 20일](../Page/6월_20일.md "wikilink"), [7월 7일](../Page/7월_7일.md "wikilink") 차례대로 만료되었다\[2\].

IBM 역시 LZW 알고리즘에 대한 특허를 가지고 있으나 이 특허에 대한 권리를 주장하지는 않았다. [자유 소프트웨어 재단에](../Page/자유_소프트웨어_재단.md "wikilink") 따르면 미국에서의 특허는 [2006년](../Page/2006년.md "wikilink") [8월 11일](../Page/8월_11일.md "wikilink") 만료되었다고 한다.

## GIF 파일의 예

다음의 테이블에서의 16진수는 [리틀-엔디언](../Page/엔디언.md "wikilink") 바이트 순서로 되어 있다. {{-}}

    byte#  hexadecimal  text or
    (hex)               value       Meaning
    0:     47 49 46
           38 39 61     GIF89a      Header
                                    Logical Screen Descriptor
    6:     03 00        3            - logical screen width in pixels
    8:     05 00        5            - logical screen height in pixels
    A:     F7                        - GCT follows for 256 colors with resolution 3 x 8 bits/primary; the lowest 3 bits represent the bit depth minus 1, the highest true bit means that the GCT is present
    B:     00           0            - background color #0
    C:     00                        - default pixel aspect ratio
                       R    G    B  Global Color Table
    D:     00 00 00    0    0    0   - color #0 black
    10:    80 00 00  128    0    0   - color #1
     :                                       :
    85:    00 00 00    0    0    0   - color #40 black
     :                                       :
    30A:   FF FF FF  255  255  255   - color #255 white
    30D:   21 F9                    Graphic Control Extension (comment fields precede this in most files)
    30F:   04           4            - 4 bytes of GCE data follow
    310:   01                        - there is a transparent background color (bit field; the lowest bit signifies transparency)
    311:   00 00                     - delay for animation in hundredths of a second: not used
    313:   10          16            - color #16 is transparent
    314:   00                        - end of GCE block
    315:   2C                       Image Descriptor
    316:   00 00 00 00 (0,0)         - NW corner position of image in logical screen
    31A:   03 00 05 00 (3,5)         - image width and height in pixels
    31E:   00                        - no local color table
    31F:   08           8           Start of image - LZW minimum code size
    320:   0B          11            - 11 bytes of LZW encoded image data follow
    321:   00 51 FC 1B 28 70 A0 C1 83 01 01
    32C:   00                        - end of image data
    32D:   3B                       GIF file terminator

## 동화상 GIF

GIF에서는 사용자가 새로운 블록을 정의할 수 있다. 1990년대에 [넷스케이프](../Page/넷스케이프.md "wikilink")는 넷스케이프 애플리케이션 블록을 설계하였으며\[3\] GIF 파일이 정적인 그림 대신 움직이는 그림을 가리키게 하였다. 이러한 애니메이션은 [넷스케이프 내비게이터](../Page/넷스케이프_내비게이터.md "wikilink") 버전 2.0에 처음 등장하였으며 그 뒤에 다른 브라우저로 퍼져나갔다.\[4\]

동화상 GIF는 여러 장의 그림이나 프레임을 이루어 연속으로 보이게 만들며, 각 그림은 GCE (그래픽 제어 확장) 기능을 통해 그려진다. 그에 이어 기본적으로 모든 프레임에 적용되는 헤더가 뒤따르며 헤더 뒤에는 데이터가 고정 색인들에 위치하지 않은 스트림 지향이 되므로 GCE 시작 위치는 선행하는 GCE의 길이에 따라 달라지게 된다. GCE 안에서 LZE 코드 그림 데이터는 각기 최대 255 바이트 안에 정렬된다. 블록의 크기는 이를 선행하는 바이트에 의해 정의된다. 이를테면 아래는 애니메이션 *[Rotating earth (large).gif](https://ko.wikipedia.org/wiki/:파일:Rotating_earth_\(large\).gif "wikilink")*의 구조가 나열되어 있다.

    byte#  hexadecimal  text or
    (hex)               value     Meaning
    0:     47 49 46
           38 39 61     GIF89a    Header
                                  Logical Screen Descriptor
    6:     90 01        400        - width in pixels
    8:     90 01        400        - height in pixels
    A:     F7                      - GCT follows for 256 colors with resolution 3 x 8bits/primary
    B:     00           0          - background color #0
    C:     00                      - default pixel aspect ratio
    D:                            Global Color Table
    :
    30D:   21 FF                  Application Extension block
    30F:   0B           11         - eleven bytes of data follow
    310:   4E 45 54
           53 43 41
           50 45        NETSCAPE   - 8-character application name
           32 2E 30     2.0        - application "authentication code"
    31B:   03           3          - three more bytes of data
    31C:   01           1          - data sub-block index (always 1)
    31D:   FF FF        65535      - unsigned number of repetitions
    31F:   00                      - end of App Extension block
    320:   21 F9                  Graphic Control Extension for frame #1
    322:   04           4          - four bytes of data follow
    323:   08                      - bit-fields 3x:3:1:1, 000|010|0|0 -> Restore to bg color
    324:   09 00                   - 0.09 sec delay before painting next frame
    326:   00                      - no transparent color
    327:   00                      - end of GCE block
    328:   2C                     Image Descriptor
    329:   00 00 00 00  (0,0)      - NW corner of frame at 0, 0
    32D:   90 01 90 01  (400,400)  - Frame width and height: 400 x 400
    331:   00                      - no local color table; no interlace
    332:   08           8         LZW min code size
    333:   FF           255       - 255 bytes of LZW encoded image data follow
    334:                data
    433:   FF           255       - 255 bytes of LZW encoded image data follow
                        data
                         :
    92BA:  00                    - end of LZW data for this frame
    92BB:  21 F9                 Graphic Control Extension for frame #2
     :                                                            :
    153B7B:21 F9                 Graphic Control Extension for frame #44
     :
    15CF35:3B                    File terminator

[인터넷 익스플로러는](../Page/인터넷_익스플로러.md "wikilink") 프레임레이트가 초당 20 프레임 이상인 경우 GIF 재생 속도를 떨어트리는데, 마이크로소프트는 [구글 크롬과](https://ko.wikipedia.org/wiki/구글_크롬 "wikilink") [사파리](../Page/사파리_\(웹_브라우저\).md "wikilink") 또한 일부 GIF 애니메이션의 속도를 떨어트린다고 밝혔다.\[5\]

## 압축의 예

GIF 파일에 사용된 가변 길이 LZW 압축을 설명하기 위해 하나의 색을 가진 커다란 그림의 예는 다음과 같다.

<table>
<thead>
<tr class="header">
<th><p>코드</p></th>
<th><p>화소</p></th>
<th><p>참고</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>번호<br />
N<sub>i</sub></p></td>
<td><p>값<br />
N<sub>i</sub> + 256</p></td>
<td><p>길이<br />
(비트)</p></td>
</tr>
<tr class="even">
<td><p>0</p></td>
<td><p>100h</p></td>
<td><p>9</p></td>
</tr>
<tr class="odd">
<td><p>1</p></td>
<td><p>FFh</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>102h</p></td>
<td><p>2</p></td>
</tr>
<tr class="odd">
<td><p>3<br />
⋮<br />
255</p></td>
<td><p>103h<br />
⋮<br />
1FFh</p></td>
<td><p>3<br />
⋮<br />
255</p></td>
</tr>
<tr class="even">
<td><p>256<br />
⋮<br />
767</p></td>
<td><p>200h<br />
⋮<br />
3FFh</p></td>
<td><p>10</p></td>
</tr>
<tr class="odd">
<td><p>768<br />
⋮<br />
1791</p></td>
<td><p>400h<br />
⋮<br />
7FFh</p></td>
<td><p>11</p></td>
</tr>
<tr class="even">
<td><p>1792<br />
⋮<br />
3839</p></td>
<td><p>800h<br />
⋮<br />
FFFh</p></td>
<td><p>12</p></td>
</tr>
<tr class="odd">
<td><p>⋮</p></td>
<td><p>FFFh</p></td>
<td><p>3839</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>101h</p></td>
<td></td>
</tr>
</tbody>
</table>

## 같이 보기

  - [소프트웨어 특허](https://ko.wikipedia.org/wiki/소프트웨어_특허 "wikilink")
  - [사진](../Page/사진.md "wikilink")

## 각주

## 외부 링크

  - [GIF89a 규격](http://www.w3.org/Graphics/GIF/spec-gif89a.txt)
  - GIF 특허
      - [Burn All GIFs](https://web.archive.org/web/19991013083423/http://burnallgifs.org/)
      - [GNU 웹 페이지에 GIF 파일을 사용하지 않는 이유](http://www.gnu.org/philosophy/gif.ko.html)
      - [The GIF Controversy: A Software Developer's Perspective](http://www.cloanto.com/users/mcb/19950127giflzw.html) (Michael C. Battilana)
      - [The GIF situation](https://web.archive.org/web/20040725074609/http://lpf.ai.mit.edu/Patents/patents.html#GIF) (League of Programming Freedom)

[분류:그래픽 파일 포맷](https://ko.wikipedia.org/wiki/분류:그래픽_파일_포맷 "wikilink") [분류:오픈 포맷](https://ko.wikipedia.org/wiki/분류:오픈_포맷 "wikilink")

1.  [The GIF Pronunciation Page](http://www.olsenhome.com/gif/)
2.
3.  [All About GIF89a](http://www.etsimo.uniovi.es/gifanim/gifabout.htm#net-extension) , Royal Frazier, 1997
4.
5.  [Animated GIFs slow down to under 20 frames per second](http://blogs.msdn.com/b/ieinternals/archive/2010/06/08/animated-gifs-slow-down-to-under-20-frames-per-second.aspx)