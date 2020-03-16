> This article is converted from Wikipedia: [Wc \(\)](https://ko.wikipedia.org/wiki/Wc_\(\)).


**wc**는 표준 [유닉스](../Page/유닉스.md "wikilink") [명령어](https://ko.wikipedia.org/wiki/명령어 "wikilink") 프로그램으로서 각각의 파일에 대한 줄(line), 단어(word), 문자(char), 그리고 바이트(byte) 수를 알려준다.

## 사용법

    wc [옵션]... [파일]...

### 옵션

  - \-c, --bytes: 바이트(byte) 수를 알려준다.
  - \-m, --chars: 문자(char) 수를 알려준다.
  - \-l, --lines: 줄(line) 수를 알려준다.
  - \-L, --max-line-length: 가장 긴 줄의 길이를 알려준다.
  - \-w, --words: 단어(word) 수를 알려준다.
  - \--help 도움말을 표시하고 끝낸다.
  - \--version 버전 정보를 출력하고 끝낸다.

## wc의 실행 예

``` console
 $ wc foo bar
      40     149     947 foo
    2294   16638   97724 bar
    2334   16787   98671 total
```

## 외부 링크

  -
  - [wc(1) - Original Unix First Edition manual page for wc](http://man.cat-v.org/unix-1st/1/wc).

  -
  - [The `wc` Command](http://www.linfo.org/wc.html) by The Linux Information Project (LINFO)

[분류:유닉스 텍스트 처리 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_텍스트_처리_유틸리티 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink")