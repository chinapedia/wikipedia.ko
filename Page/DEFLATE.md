> This article is converted from Wikipedia: [DEFLATE](https://ko.wikipedia.org/wiki/DEFLATE).


**DEFLATE**는 [ZIP](https://ko.wikipedia.org/wiki/ZIP "wikilink"), [gzip](https://ko.wikipedia.org/wiki/gzip "wikilink") 등의 프로그램에서 사용되는 [무손실 압축](https://ko.wikipedia.org/wiki/무손실_압축 "wikilink") 데이터 포맷이자 [알고리즘](../Page/알고리즘.md "wikilink")이다. [필 캐츠가](../Page/필_캐츠.md "wikilink") [PKZIP](../Page/PKZIP.md "wikilink")에 쓰기 위하여 고안하였으며, 후에 이 알고리즘은 [RFC](../Page/RFC.md "wikilink") 1951로 등록되었다.

DEFLATE 알고리즘은 [특허](../Page/특허.md "wikilink")가 걸린 기술을 사용하지 않는 것으로 알려져 있으며, 때문에 필 캐츠가 설계했던 [ZIP](https://ko.wikipedia.org/wiki/ZIP "wikilink")를 비롯해 많은 파일 포맷과 프로그램에서 광범위하게 사용되고 있다. 대조적으로 [GIF](../Page/GIF.md "wikilink") 이미지 파일 포맷에서 사용된 [LZW](../Page/LZW.md "wikilink") 알고리즘의 특허는 [2003년](../Page/2003년.md "wikilink")에야 만료되었고, 이는 DEFLATE 알고리즘을 사용하는 [PNG](../Page/PNG.md "wikilink") 이미지 파일 포맷의 개발을 촉진시켰다.

## 기술

DEFLATE는 기본적으로 [LZ77](https://ko.wikipedia.org/wiki/LZ77 "wikilink") 알고리즘을 통해 데이터를 압축한 뒤, 중복되는 내용에 대한 포인터(일치하는 내용의 위치와 길이)를 [허프만 부호화를](../Page/허프만_부호화.md "wikilink") 사용하여 한 번 더 압축한다.

DEFLATE 알고리즘은 일반적으로 그 압축률에 비해 압축/해제 속도가 빠르나, 나중에 나온 압축 알고리즘에 비해서는 압축률이 다소 떨어지는 경향이 있다.

## 구현

[zlib](https://ko.wikipedia.org/wiki/zlib "wikilink") 범용 압축 라이브러리는 DEFLATE 알고리즘의 대표적인 구현이다. [7-Zip](../Page/7-Zip.md "wikilink")에서는 DEFLATE와 같은 포맷을 사용하면서 압축률을 더 높이는 알고리즘을 사용하고 있으며, 켄 실버맨(Ken Silverman)의 KZIP과 PNGOUT에서도 더 효율적인 알고리즘을 구현하고 있다.

## 외부 링크

  - RFC 1951, *DEFLATE Compressed Data Format Specification version 1.3*
  - [zlib 홈페이지](http://www.zlib.org)
  - [하드웨어 Deflate Decompress IP Cores](https://web.archive.org/web/20171113221603/http://cafe.naver.com/carroty/295575)

[분류:무손실 압축 알고리즘](https://ko.wikipedia.org/wiki/분류:무손실_압축_알고리즘 "wikilink")