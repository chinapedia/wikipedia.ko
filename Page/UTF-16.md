> This article is converted from Wikipedia: [UTF-16](https://ko.wikipedia.org/wiki/UTF-16).


**UTF-16**(16-bit Unicode Transformation Format)은 유니코드 문자 인코딩 방식의 하나이다. 주로 사용되는 [기본 다국어 평면](https://ko.wikipedia.org/wiki/기본_다국어_평면 "wikilink") (BMP, Basic multilingual plane)에 속하는 문자들은 그대로 16비트 값으로 인코딩이 되고 그 이상의 문자는 특별히 정해진 방식으로 32비트로 인코딩이 된다.

UTF-16은 유니코드 컨소시엄과 ISO/IEC 10646에 의해 정의되어 있다. 유니코드는 거기에 추가적인 내용을 정하고 있다. 정확한 차이점은 유니코드 4.0 표준의 [부록편 C](http://www.unicode.org/versions/Unicode4.0.0/appC.pdf) 부분이 자세히 기술되어 있다. ISO 표준은 [UCS-2](https://ko.wikipedia.org/wiki/UCS-2 "wikilink") 인코딩도 정의하며 여기선 BMP의 16비트 표현만을 다룬다.

기본 다국어 평면은 U+0000 에서 U+FFFF 에 놓인 문자를 담고 있다. 이 영역에는 우리가 쉽게 생각할 수 있는 문자들이 포함되며, 한글, 한자 등은 모두 여기에 포함되어 있다. 이 영역에는 서러게이트 문자(surrogate)들이 준비되어 있어 16비트 이상의 문자를 표현할 때를 대비해 놓았다.

기본 다국어 평면의 문자들은 곧바로 16비트 값으로 대응되어 인코딩되며, 이 경우에는 인코딩된 바이트 스트링의 [엔디언](../Page/엔디언.md "wikilink")만 조심하면 된다.

UTF-16-문자

`Bit`
`|15            8|7             0|`
`+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+`
`|y y y y y y y y|x x x x x x x x|`
`+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+`

UTF-16BE-코드

`    첫 번째 Byte         두 번째 Byte`
`|7             0| |7             0|`
`+-+-+-+-+-+-+-+-+ +-+-+-+-+-+-+-+-+`
`|y y y y y y y y| |x x x x x x x x|`
`+-+-+-+-+-+-+-+-+ +-+-+-+-+-+-+-+-+`

UTF-16LE-코드

`    첫째 Byte          두 번째 Byte`
`|7             0| |7             0|`
`+-+-+-+-+-+-+-+-+ +-+-+-+-+-+-+-+-+`
`|x x x x x x x x| |y y y y y y y y|`
`+-+-+-+-+-+-+-+-+ +-+-+-+-+-+-+-+-+`

기본 다국어 평면에 포함되지 않는 문자들, 즉 16비트로 값을 표현할 수 없는 문자들은 서러게이트(Surrogate) 문자 영역에 해당하는 두 개의 16비트 문자로 변환되어 이 한 쌍(즉 32비트)이 그 문자를 나타내게 된다. 그 자세한 방식은 다음 그림을 통해 설명한다.

`Bit`
`31            24|23           16|15            8|7             0|`
`+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+`
`|0 0 0 0 0 0 0 0|0 0 0 z z z z z|x x x x x x y y|y y y y y y y y|`
`+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+`

High-Surrogate (U+D800 ... U+DBFF)

`|15            8|7             0|`
`+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+`
`|1 1 0 1 1 0 Z Z|Z Z x x x x x x|`
`+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+`

Low-Surrogate (U+DC00 ... U+DFFF)

`|15            8|7             0|`
`+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+`
`|1 1 0 1 1 1 y y|y y y y y y y y|`
`+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+`

유니코드 문자 영역에서 상위 서러게이트는 U+D800 에서 U+DBFF 까지의 값을 갖는다. 즉 최상위비트 6개의 값이 그림에서 보듯이 110110 으로 일정하다. 마찬가지로 하위 서러게이트는 U+DC00 에서 U+DFFF 까지의 값을 가지며 최상위비트 6개의 값은 110111 이 된다. 각 서러게이트 문자는 하위 10비트씩의 자유도를 갖는다. 따라서 주어진 문자를 10비트씩 두조각을 내서 상위 서러게이트와 하위 서러게이트에 배정한 것이다.

여기서 다음을 만족한다.

  -
    ZZZZ=zzzzz-1.

이 방법으로 UTF-16 인코딩이 가능한 유니코드 문자의 범위가 나온다.

zzzzz=00000 이라면, 문자는 16비트 이하로 표현이 가능하다. 즉, U+00xxxx 그대로 대응되는 값을 써주면 된다. 그렇지 않다면, ZZZZ=0000..1111 이 되며,zzzzz=00001..10000 = U+01xxxx .. U+10xxxx

이 두 개의 서러게이트 문자는 상위 서러게이트, 하위 서러게이트로서 전송이 된다. 이 방법으로 U+10FFFF 까지의 문자를 인코딩 할 수 있다.

## 예시

| 코드 점               | 문자                                                        | UTF-16 코드 값 | [글리프](https://ko.wikipedia.org/wiki/글리프 "wikilink")               |
| ------------------ | --------------------------------------------------------- | ----------- | ----------------------------------------------------------------- |
| 122 (hex 7A)       | 소문자 Z([로마자](../Page/로마자.md "wikilink"))                   | 007A        | z                                                                 |
| 27700 (hex 6C34)   | 물 수([한자](../Page/한자.md "wikilink"))                       | 6C34        | 水                                                                 |
| 119070 (hex 1D11E) | [높은음자리표](https://ko.wikipedia.org/wiki/높은음자리표 "wikilink") | D834 DD1E   | 𝄞 ([10px](https://ko.wikipedia.org/wiki/파일:GClef.svg "wikilink")) |

| 인코딩      | 바이트 순서                                                    | 바이트 열                            |
| -------- | --------------------------------------------------------- | -------------------------------- |
| UTF-16LE | [리틀 엔디언](https://ko.wikipedia.org/wiki/리틀_엔디언 "wikilink") | 34 6C, 7A 00, 34 D8 1E DD        |
| UTF-16BE | [빅 엔디언](https://ko.wikipedia.org/wiki/빅_엔디언 "wikilink")   | 6C 34, 00 7A, D8 34 DD 1E        |
| UTF-16   | 리틀 엔디언, with BOM                                          | FF FE, 34 6C, 7A 00, 34 D8 1E DD |
| UTF-16   | 빅 엔디언, with BOM                                           | FE FF, 6C 34, 00 7A, D8 34 DD 1E |

水z𝄞
〔UTF-16로 인코드된 물 수, z, 높은음자리표([10px](https://ko.wikipedia.org/wiki/파일:GClef.svg "wikilink"))〕

## 같이 보기

  - [UTF-8](../Page/UTF-8.md "wikilink")

## 외부 링크

  - [Unicode Standard 4.0 Chapter 2](http://www.unicode.org/versions/Unicode4.0.0/ch02.pdf) (PDF) 일반 구조. UTF-16 는 *2.5 Encoding Forms* (S.20) 에 정의되어 있다.
  - [Unicode TN12: UTF-16 for Processing](http://www.unicode.org/notes/tn12/#U4ch2)

[분류:문자 인코딩](https://ko.wikipedia.org/wiki/분류:문자_인코딩 "wikilink") [분류:유니코드 변환 형식](https://ko.wikipedia.org/wiki/분류:유니코드_변환_형식 "wikilink")