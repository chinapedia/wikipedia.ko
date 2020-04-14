> This article is converted from Wikipedia: [Zip 폭탄](https://ko.wikipedia.org/wiki/Zip_폭탄).


**zip 폭탄**(zip bomb), **죽음의 zip**(zip of death), **압축 해제 폭탄**(decompression bomb)은 프로그램이나 시스템이 읽을 때 충돌하거나 뻗어버리게 만드는 악의적인 컴퓨터 [압축](https://ko.wikipedia.org/wiki/압축_소프트웨어 "wikilink") [파일이다](../Page/컴퓨터_파일.md "wikilink"). 이 파일은 전통적인 방식의 바이러스가 침입하기 편하게 [바이러스 검사 소프트웨어를](../Page/바이러스_검사_소프트웨어.md "wikilink") 꺼버리는 역할을 한다.

이 프로그램은 정상적인 컴퓨터 동작을 방해하지 않으며 겉보기에는 평범한 [ZIP](../Page/ZIP_\(파일_포맷\).md "wikilink") 파일이다. 하지만 만일 바이러스 검사 소프트웨어가 검사하려 시도하는 등 이 파일의 압축을 해제하려 시도할 경우 엄청난 양의 하드디스크 용량과 메모리 용량이 필요하다.

현대 바이러스 검사 소프트웨어는 zip 파일이 zip 폭탄인지 아닌지 감별하며, 폭탄인 경우에는 압축을 풀지 않는 과정이 포함되어 있다.\[1\]

## 자세한 설명

zip 폭탄은 사용자의 의심을 피하기 위해 압축된 상태의 용량은 작다. 그러나, 이 파일의 압축을 풀려 할때 파일의 용량은 시스템이 버틸 수 있는 한도를 초과해 버린다. 이 기술은 과거 [전자 게시판](../Page/전자_게시판.md "wikilink") 전화 접속 시절에 이용하였다.\[2\]

zip 폭탄의 대표적인 예로 42.zip 파일이 있다. 이 파일은 압축된 상태에서는 42KB이나, 이 압축된 파일은 안에 압축된 파일 16개가 각각 5겹으로 16개씩 존재한다. 가장 마지막 층에는 4.3GB(4 294 967 295 bytes)짜리 파일이 1개 있으며, 압축을 풀 경우 전체 파일의 용량은 3.99PB(4 503 599 626 321 920 Bytes)가 된다.\[3\] 이 파일은 다양한 웹 사이트에서 다운로드 받을 수 있다. 많은 바이러스 검사 소프트웨어에서는 [버퍼 오버플로](https://ko.wikipedia.org/wiki/버퍼_오버플로 "wikilink"), [메모리 부족](https://ko.wikipedia.org/wiki/메모리_부족 "wikilink"), 프로그램 액세스 허용 시간 초과를 일으키는 공격을 막기 위해 [반복](https://ko.wikipedia.org/wiki/반복 "wikilink")되는 몇겹만 추출하여 검사한다.

zip 폭탄은 극단적인 압축률을 이루기 위해 파일 대부분이 반복되는 문구열인 경우가 많다. 이러한 파일을 압축하기 위하여 단 하나의 파일만이 각 재귀적인 층을 따라가고 기하급수적인 효율성을 이루기 위해 동적 프로그래밍 방법을 이용하기도 한다.

또한, 압축을 풀 때 [스스로를 복제하는 방식으로 이루어져 있는](https://ko.wikipedia.org/wiki/콰인 "wikilink") zip 파일도 있다.\[4\]\[5\]

2019년 7월 2일, 재귀적인 방법을 사용하지 않으면서 [파일 헤더와](https://ko.wikipedia.org/wiki/파일_헤더 "wikilink") 내용을 서로 겹쳐 쓰는 방식으로 작성한 zip 폭탄이 제시되었다. 이 파일은 압축 상태에서 10MB 정도이지만 압축을 풀면 281TB의 파일이 한꺼번에 튀어나온다.\[6\]

## 더 보기

  - [빌리언 러프](https://ko.wikipedia.org/wiki/빌리언_러프 "wikilink")(Billion laughs) - XML 파서에서의 비슷한 공격
  - [메일폭탄](https://ko.wikipedia.org/wiki/메일폭탄 "wikilink")
  - [논리 폭탄](https://ko.wikipedia.org/wiki/논리_폭탄 "wikilink")
  - [포크 폭탄](https://ko.wikipedia.org/wiki/포크_폭탄 "wikilink")
  - [비지 비버](https://ko.wikipedia.org/wiki/비지_비버 "wikilink") - 종료하기 전까지 최대한 많은 출력물을 만들어내는 프로그램

## 각주

## 외부 링크

  - ["DoS risk from Zip of death attacks on AV software?"](http://www.theregister.co.uk/2001/07/23/dos_risk_from_zip/), 2001 story on "The Register"
  - ["Zip Files All The Way Down"](http://research.swtch.com/zip), 2010
  - [ZIP File Quine](http://www.steike.com/code/useless/zip-file-quine/)
  - [Zip Bomb](https://web.archive.org/web/20141231095149/http://xeushack.com/tutorials/initiation/ZipBomb#welcome)
  - [42.zip](http://www.unforgettable.dk/) and [42.zip](http://www.securityfocus.com/bid/3027/exploit/)
  - [Decompression bomb vulnerabilities](http://www.aerasec.de/security/advisories/decompression-bomb-vulnerability.html)

[분류:서비스 거부 공격](https://ko.wikipedia.org/wiki/분류:서비스_거부_공격 "wikilink") [분류:악성 소프트웨어](https://ko.wikipedia.org/wiki/분류:악성_소프트웨어 "wikilink")

1.
2.
3.
4.
5.
6.