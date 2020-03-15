> This article is converted from Wikipedia: [LZMA](https://ko.wikipedia.org/wiki/LZMA).


**LZMA**(Lempel–Ziv–Markov chain algorithm)는 [데이터 압축에](https://ko.wikipedia.org/wiki/데이터_압축 "wikilink") 쓰이는 [알고리즘](https://ko.wikipedia.org/wiki/알고리즘 "wikilink")이다. 1998년 이후로 계속 개발 중이며\[1\]\[2\] [7-zip](https://ko.wikipedia.org/wiki/7-zip "wikilink") 압축 프로그램의 [7z](https://ko.wikipedia.org/wiki/7z "wikilink") 형식에 쓰인다. 이 알고리즘은 [LZ77과](https://ko.wikipedia.org/wiki/LZ77과_LZ78 "wikilink") 어느 정도 비슷한 [사전 압축](https://ko.wikipedia.org/wiki/사전_코더 "wikilink") 계획을 이용하며 일반적으로 [bzip2](https://ko.wikipedia.org/wiki/bzip2 "wikilink")보다 더 높을 만큼의\[3\]\[4\] 높은 압축률을 제공하며 최대 4 [GiB의](https://ko.wikipedia.org/wiki/기가바이트 "wikilink") 가변 압축 사전 크기를 제공한다.\[5\]

**LZMA2**는 비압축 데이터와 LZMA 데이터를 동시에 포함할 수 있는 단순 컨테이너 포맷으로, 각기 다른 여러 개의 LZMA 인코딩 변수가 포함될 수 있다. LZMA2는 임의 스케일링이 가능한 멀티스레드 방식의 압축 및 압축 해제, 그리고 부분적으로 압축이 불가능한 데이터의 효율적인 압축을 지원한다.

## 같이 보기

  - [LZW](../Page/LZW.md "wikilink")
  - [파일 압축](https://ko.wikipedia.org/wiki/파일_압축 "wikilink")

## 각주

<references />

## 외부 링크

  - [공식 웹사이트](http://www.7-zip.org/)
  - [LZMA SDK (소프트웨어 개발 키트)](http://www.7-zip.org/sdk.html)

[분류:무손실 압축 알고리즘](https://ko.wikipedia.org/wiki/분류:무손실_압축_알고리즘 "wikilink")

1.  SDK 역사 파일에는 1996년부터라고 이야기하고 있지만 [7-zip](https://ko.wikipedia.org/wiki/7-zip "wikilink")에 처음 쓰인 것은 2001년 8월 30일이다. 일부 참조가 없는 의견에는 1998년으로 되어 있지만 이 알고리즘은 [7-zip](https://ko.wikipedia.org/wiki/7-zip "wikilink")에 쓰이기 전까지는 출판된 적이 없는 것으로 보인다.
2.
3.
4.
5.  Overview of the LZMA format [7z Format](http://www.7-zip.org/7z.html)