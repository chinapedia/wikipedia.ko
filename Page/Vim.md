> This article is converted from Wikipedia: [Vim](https://ko.wikipedia.org/wiki/Vim).


[섬네일](https://ko.wikipedia.org/wiki/파일:Vim.png "wikilink") 환경에서 실행 중인 gVim\]\] **Vim**(빔\[1\], )은 Bram Moolenaar가 만든 [vi](https://ko.wikipedia.org/wiki/vi "wikilink") 호환 [텍스트 편집기이다](https://ko.wikipedia.org/wiki/텍스트_편집기 "wikilink"). CUI용 Vim과 GUI용 **gVim**이 있다. 본래 [아미가](../Page/아미가.md "wikilink") 컴퓨터 용 프로그램이었으나 현재는 [마이크로소프트 윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink"), [리눅스](../Page/리눅스.md "wikilink"), [맥 오에스 텐을](https://ko.wikipedia.org/wiki/맥_오에스_텐 "wikilink") 비롯한 여러 환경을 지원한다.

Vim은 vi와 호환되면서도 독자적으로 다양한 기능을 추가하여 사용자의 편의를 돕고 있다. 특히 [Vim 스크립트](https://ko.wikipedia.org/wiki/#Vim_스크립트 "wikilink") 등을 사용해서 자유롭게 편집 환경을 변경하거나, 확장된 [정규 표현식](https://ko.wikipedia.org/wiki/정규_표현식 "wikilink") 문법, 강력한 [문법 강조](https://ko.wikipedia.org/wiki/문법_강조 "wikilink") 기능, 다중 [되돌리기](https://ko.wikipedia.org/wiki/되돌리기 "wikilink"), [유니코드](../Page/유니코드.md "wikilink")를 비롯한 다국어 지원, [문법 검사](https://ko.wikipedia.org/wiki/문법_검사 "wikilink") 등을 쓸 수 있다는 점이 강점으로 꼽힌다. 한편으로는 vi와 마찬가지로 처음에 배우기 어렵다는 점이 단점으로 지적되는데, 이를 극복하기 위해 쉬운 Vim 모드를 지원한다.

## 역사

[Bram Moolenaar는](https://ko.wikipedia.org/wiki/Bram_Moolenaar "wikilink") 1988년 [아미가](../Page/아미가.md "wikilink") 컴퓨터용 Vim에 대한 작업을 시작하였다. Moolenaar는 1991년에 Vim v1.14를 처음 공개하였다.\[2\] Vim은 Tim Thompson, Tony Andrews, G.R. (Fred) Walter가 만든 [아타리 ST용](../Page/아타리_ST.md "wikilink")\[3\] 초기 편집기 Stevie에 기반을 두었다.\[4\]\[5\]

"Vim"은 "Vi IMproved"의 준말인데\[6\], 그 이유는 Vim이 프로그램 [소스 코드](../Page/소스_코드.md "wikilink") 편집 시 유용한 수많은 추가 기능이 포함된 [vi](https://ko.wikipedia.org/wiki/vi "wikilink") 편집기의 확장판이기 때문이다. 원래 "Vi IMitation"을 대표하는 말이었으나, 1993년 12월 Vim 2.0 출시와 함께 이처럼 변경되었다.\[7\]

## 인터페이스

[vi](https://ko.wikipedia.org/wiki/vi "wikilink")처럼 Vim도 CUI(명령줄 사용자 인터페이스)를 기반으로 하며, gVim이라는 GUI(그래픽 사용자 인터페이스)용 프로그램에는 메뉴와 자주 사용하는 명령어 툴바를 추가했으나 여전히 대부분의 기능은 CUI방식을 이용한다.

Vim은 초보자를 위한 내장 설명서가 있는데 터미널에서 'vimtutor'라는 명령어로 이를 볼 수 있다. 또한 더 상세한 사용자 설명서도 있다. 이 역시 Vim에서나 온라인에서 볼 수 있다. Vim에서 `:help`라는 명령어로 명령어나 기능을 검색해 볼 수도 있다.

## Vi에 비해 개선된 사항과 기능

Vim은 vi 호환 모드를 갖고 있지만 이 모드가 아닌 경우 Vim은 vi에 비해 수많은 개선사항이 있다.\[8\] 그러나 호환성 모드에서도 Vim은 [단일 유닉스 규격](../Page/단일_유닉스_규격.md "wikilink")\[9\], [POSIX](../Page/POSIX.md "wikilink")에 정의된대로 완전히 vi와 호환되는 것은 아니다. (예: Vim은 vi의 오픈 모드를 지원하지 않으며, 시각 모드만 지원한다) 그럼에도 Vim은 "Vi와 매우 호환성이 높은 것"으로 기술되고 있다.\[10\]

Vim의 개선 사항 중에는 파일의 [완성](../Page/자동_완성.md "wikilink"), [비교](https://ko.wikipedia.org/wiki/파일_비교 "wikilink"), [병합](../Page/병합.md "wikilink")(vimdiff), 통합된 도움말 시스템, 확장된 [정규 표현식](https://ko.wikipedia.org/wiki/정규_표현식 "wikilink"), 플러그인 지원을 포함한 [스크립트 언어](../Page/스크립트_언어.md "wikilink")(네이티브 및 펄, 파이썬, 루비, Tcl 등의 기타 스크립트 인터프리터를 통해), [그래픽 사용자 인터페이스](../Page/그래픽_사용자_인터페이스.md "wikilink")(gvim), 제한된 [통합 개발 환경과](../Page/통합_개발_환경.md "wikilink") 같은 기능, [마우스](../Page/마우스.md "wikilink") 상호작용(GUI와 함께/GUI 없이), 폴딩, 압축 파일([gzip](https://ko.wikipedia.org/wiki/gzip "wikilink"), [bzip2](https://ko.wikipedia.org/wiki/bzip2 "wikilink"), [zip](../Page/ZIP_\(파일_포맷\).md "wikilink"), [tar](https://ko.wikipedia.org/wiki/tar_\(파일_포맷\) "wikilink") 포맷) 및 네트워크 프로토콜([SSH](../Page/시큐어_셸.md "wikilink"), [FTP](../Page/파일_전송_프로토콜.md "wikilink"), [HTTP](../Page/HTTP.md "wikilink"))을 경유한 파일의 편집, 세션 상태 보존, [맞춤법 검사](../Page/맞춤법_검사기.md "wikilink"), 수직/수평 탭 창, [유니코드](../Page/유니코드.md "wikilink") 및 기타 다언어 지원, [문법 강조](https://ko.wikipedia.org/wiki/문법_강조 "wikilink"), 세션 경유 명령, 검색 및 커서 위치 역사, 시각 모드 등이 포함된다.

## Vim 스크립트

Vim 스크립트(Vim script, vimscript, VimL)는 Vim에 통합된 [스크립트 언어이다](../Page/스크립트_언어.md "wikilink").\[11\] 오리지널 vi 편집기의 [ex](https://ko.wikipedia.org/wiki/ex_\(유닉스\) "wikilink") 편집기 언어에 기반한 초기 버전의 Vim은 제어 흐름과 함수 정의를 위한 명령들을 추가하였다. 버전 7 이후로 Vim 스크립트는 [객체 지향 프로그래밍의](../Page/객체_지향_프로그래밍.md "wikilink") [리스트와](../Page/리스트_\(컴퓨팅\).md "wikilink") [사전과](https://ko.wikipedia.org/wiki/연관_배열 "wikilink") 같은 더 진보된 자료형을 지원한다. `map()`과 `filter()`와 같은 내장 함수들은 기본적인 형태의 [함수형 프로그래밍을](../Page/함수형_프로그래밍.md "wikilink") 지원하며, Vim 스크립트는 버전 8.0 이후로 [람다를](https://ko.wikipedia.org/wiki/익명_함수 "wikilink") 포함하고 있다. Vim 스크립트는 대체적으로 [명령형 프로그래밍 스타일로](../Page/명령형_프로그래밍.md "wikilink") 작성된다.

### 예

다음은 [`while`](https://ko.wikipedia.org/wiki/while "wikilink") 루프의 예제이다.

``` vim
" This is a simple while loop in Vim script.
let i = 1
while i < 5
  echo "count is" i
  let i += 1
endwhile
```

## Neovim

[섬네일](https://ko.wikipedia.org/wiki/파일:Neovim-logo.svg "wikilink") Neovim\[12\]은 Vim의 확대집합이 되는 Vim의 리팩터(refactor) 판이다.\[13\] Neovim은 Vim과 동일한 구성을 공유한다. 그러므로 동일한 [구성 파일을](https://ko.wikipedia.org/wiki/구성_파일 "wikilink") 두 편집기에서 사용할 수 있다.\[14\] 2015년 12월 출시된 버전 0.1을 기준으로, Neovim은 Vim 기능의 대부분과 호환된다.\[15\]

## 같이 보기

  - [편집기 전쟁](../Page/편집기_전쟁.md "wikilink")

## 각주

## 외부 링크

  -
  -
[분류:유닉스 문서 편집기](https://ko.wikipedia.org/wiki/분류:유닉스_문서_편집기 "wikilink") [분류:C로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C로_작성된_자유_소프트웨어 "wikilink") [분류:크로스 플랫폼 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_자유_소프트웨어 "wikilink") [분류:리눅스 문서 편집기](https://ko.wikipedia.org/wiki/분류:리눅스_문서_편집기 "wikilink") [분류:윈도우 문서 편집기](https://ko.wikipedia.org/wiki/분류:윈도우_문서_편집기 "wikilink") [분류:자유 문서 편집기](https://ko.wikipedia.org/wiki/분류:자유_문서_편집기 "wikilink") [분류:아미가 소프트웨어](https://ko.wikipedia.org/wiki/분류:아미가_소프트웨어 "wikilink")

1.  [Vim documentation: intro](http://vimdoc.sourceforge.net/htmldoc/intro.html): "Vim is pronounced as one word, like Jim, not vi-ai-em. It's written with a capital, since it's a name, again like Jim."
2.  <http://moolenaar.net/vimstory.pdf>
3.
4.
5.
6.
7.
8.  Vim help system (type "[`:help`](http://vimdoc.sourceforge.net/htmldoc/help.html)" within Vim)
9.
10.  (question 1.3)
11. <http://vimdoc.sourceforge.net/htmldoc/usr_41.html>
12.
13.
14.
15.