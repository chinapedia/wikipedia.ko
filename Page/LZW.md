> This article is converted from Wikipedia: [LZW](https://ko.wikipedia.org/wiki/LZW).


**LZW**(Lempel-Ziv-Welch)는 [아브라함 렘펠과](https://ko.wikipedia.org/wiki/아브라함_렘펠 "wikilink") [제콥 지브](https://ko.wikipedia.org/wiki/제콥_지브 "wikilink"), [테리 웰치가](https://ko.wikipedia.org/wiki/테리_웰치 "wikilink") 만든 공통 [비손실 데이터 압축](https://ko.wikipedia.org/wiki/비손실_데이터_압축 "wikilink") [알고리즘](../Page/알고리즘.md "wikilink")이다. [1978년](../Page/1978년.md "wikilink")에 렘펠과 지브가 공개한 [LZ78](https://ko.wikipedia.org/wiki/LZ78 "wikilink") 알고리즘의 개선판을 웰치에 의해 1984년에 공개하였다. 이 알고리즘은 빠른 이식을 위해 고안되었지만 데이터의 제한된 분석만 수행하기 때문에 그리 최적으로 동작하지는 않는다. Huffman의 아이디어에서 조금 더 응용된 형태이다.

## 알고리즘

압축 프로그램 알고리즘:

``` text
    w = NIL;
    add all possible charcodes to the dictionary
    for (every character c in the uncompressed data) do
        if ((w + c) exists in the dictionary) then
            w = w + c;
        else
            add (w + c) to the dictionary;
            add the dictionary code for w to output;
            w = c;
        endif
    done
    add the dictionary code for w to output;
    display output;
```

압축 해제 프로그램 알고리즘:

``` text
    add all possible charcodes to the dictionary
    read a char k;
    entry = dictionary entry for k
    output entry;
    w = entry;
    while (read a char k) do
       if (index k exists in dictionary) then
           entry = dictionary entry for k;
       else if (k == currSizeDict)
           entry = w + w[0];
       else
           signal invalid code;
       endif
       output entry;
       add w+entry[0] to the dictionary;
       w = entry;
    done
```

## 종류

  - LZMW (1985년, V. Miller, M. Wegman)\[1\]
  - LZAP (1988년, James Storer)\[2\] - LZMW의 수정판
  - [LZWL](https://ko.wikipedia.org/wiki/LZWL "wikilink")는 음절 기반의 LZW이다.

## 같이 보기

  - [LZ77과 LZ78](https://ko.wikipedia.org/wiki/LZ77과_LZ78 "wikilink")
  - [LZMA](../Page/LZMA.md "wikilink")
  - [LZSS](https://ko.wikipedia.org/wiki/LZSS "wikilink")
  - [LZJB](https://ko.wikipedia.org/wiki/LZJB "wikilink")

## 각주

## 외부 링크

  - [SharpLZW - C\# open source implementation](http://sourceforge.net/projects/sharplzw/)

[분류:아카이브 포맷](https://ko.wikipedia.org/wiki/분류:아카이브_포맷 "wikilink") [분류:무손실 압축 알고리즘](https://ko.wikipedia.org/wiki/분류:무손실_압축_알고리즘 "wikilink")

1.  David Salomon, *Data Compression - The complete reference*, 4th ed., page 209
2.  David Salomon, *Data Compression - The complete reference*, 4th ed., page 212