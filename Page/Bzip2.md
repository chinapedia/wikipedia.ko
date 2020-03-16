> This article is converted from Wikipedia: [Bzip2](https://ko.wikipedia.org/wiki/Bzip2).


**bzip2**는 [버로우즈-휠러 변환](../Page/버로우즈-휠러_변환.md "wikilink") 기반의 [압축 알고리즘](https://ko.wikipedia.org/wiki/압축_알고리즘 "wikilink") 및 [압축 소프트웨어이다](https://ko.wikipedia.org/wiki/압축_소프트웨어 "wikilink"). 줄리안 시워드()가 개발하였으며, [1996년](../Page/1996년.md "wikilink") 7월에 0.15 버전을 처음 공개했다. 소프트웨어는 [오픈 소스이며](../Page/오픈_소스.md "wikilink"), [BSD 허가서와](../Page/BSD_허가서.md "wikilink") 비슷한 라이선스를 갖는다.

bzip2는 [gzip](https://ko.wikipedia.org/wiki/gzip "wikilink")와 비슷하게 파일 하나만을 압축하며, 압축한 파일에는 보통 .bz2 확장자가 붙고 따라서 [tar와](../Page/Tar_\(파일_포맷\).md "wikilink") 함께 사용하는 것이 일반적이다.

## 압축 효율

bzip2는 [버로우즈-휠러 변환을](../Page/버로우즈-휠러_변환.md "wikilink") 써서 자주 반복되는 문자열을 같은 문자열로 변환한 다음 [MTF 변환](https://ko.wikipedia.org/wiki/MTF_변환 "wikilink"), [허프만 부호화를](../Page/허프만_부호화.md "wikilink") 차례대로 적용하는 구조이다. bzip2는 [gzip](https://ko.wikipedia.org/wiki/gzip "wikilink")이나 [ZIP](https://ko.wikipedia.org/wiki/ZIP "wikilink")에 비해 대체로 압축률이 좋지만 비교적 느리다.

bzip2의 이전 버전 bzip은 블록 정렬을 한 다음 [산술 부호화를](../Page/산술_부호화.md "wikilink") 사용했지만, 특허 문제 때문에 bzip2에서는 이 방식을 쓰지 않는다.

## 같이 보기

  - [압축 소프트웨어의 비교](https://ko.wikipedia.org/wiki/압축_소프트웨어의_비교 "wikilink")
  - [Tar (파일 포맷)](../Page/Tar_\(파일_포맷\).md "wikilink")
  - [Gzip](../Page/Gzip.md "wikilink")
  - [Xz](../Page/Xz.md "wikilink")

## 외부 링크

  - [bzip2와 libbzip2 홈페이지](https://web.archive.org/web/20061225094755/http://www.bzip.org/)

  - [윈도용 bzip2](http://gnuwin32.sourceforge.net/packages/bzip2.htm)

[분류:무손실 압축 알고리즘](https://ko.wikipedia.org/wiki/분류:무손실_압축_알고리즘 "wikilink") [분류:유닉스 보관 및 압축 관련 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_보관_및_압축_관련_유틸리티 "wikilink") [분류:크로스 플랫폼 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_소프트웨어 "wikilink") [분류:자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_소프트웨어 "wikilink") [분류:1996년 소프트웨어](https://ko.wikipedia.org/wiki/분류:1996년_소프트웨어 "wikilink") [분류:자유 압축 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_압축_소프트웨어 "wikilink")