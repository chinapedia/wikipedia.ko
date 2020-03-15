> This article is converted from Wikipedia: [Gzip](https://ko.wikipedia.org/wiki/Gzip).


**gzip**은 [파일 압축에](https://ko.wikipedia.org/wiki/파일_압축 "wikilink") 쓰이는 [응용 소프트웨어이다](https://ko.wikipedia.org/wiki/응용_소프트웨어 "wikilink"). gzip은 GNU zip의 준말이며, 초기 [유닉스](https://ko.wikipedia.org/wiki/유닉스 "wikilink") 시스템에 쓰이던 [압축](https://ko.wikipedia.org/wiki/데이터_압축 "wikilink") 프로그램을 대체하기 위한 [자유 소프트웨어이다](https://ko.wikipedia.org/wiki/자유_소프트웨어 "wikilink"). gzip은 [Jean-loup Gailly와](https://ko.wikipedia.org/wiki/Jean-loup_Gailly "wikilink") [마크 애들러가](https://ko.wikipedia.org/wiki/마크_애들러 "wikilink") 만들었다. 버전 0.1은 [1992년](https://ko.wikipedia.org/wiki/1992년 "wikilink") [10월 31일에](https://ko.wikipedia.org/wiki/10월_31일 "wikilink") 처음 공개되었으며, 버전 1.0이 1993년 2월에 뒤따라 나왔다. [오픈BSD](https://ko.wikipedia.org/wiki/오픈BSD "wikilink")의 gzip 버전은 더 오래된 [압축](https://ko.wikipedia.org/wiki/데이터_압축 "wikilink") 프로그램을 기반으로 하고 있으며, 오픈BSD 3.4에 추가되었다.

## 파일 포맷

gzip은 [ZIP (파일 포맷)과](https://ko.wikipedia.org/wiki/ZIP_\(파일_포맷\) "wikilink") 같이 [DEFLATE](https://ko.wikipedia.org/wiki/DEFLATE "wikilink") 알고리즘을 따르지만, 여러 파일을 하나의 파일로 압축하는 옵션이 없다는 점에서 차이가 난다. 여러 파일 또는 디렉터리를 하나의 파일로 압축하기 위해서 gzip은 보통 [Tar (파일 포맷)와](https://ko.wikipedia.org/wiki/Tar_\(파일_포맷\) "wikilink") 같이 사용되는 것이 일반적이다. .tar.gz 로 압축된 파일의 경우 zip과 압축 알고리즘은 같지만 더 용량이 작다. 이는 .tar.gz의 경우 서로 다른 파일끼리의 중복되는 부분을 압축시킬 수 있기 때문이다.\[1\]

## 응용과 파생

대부분의 리눅스 배포판에 포함되어 있는 tar 유틸리티는 .tar.gz 파일을 z 옵션으로 압축을 풀 수 있다. *e.g., tar -zxf file.tar.gz*

1990년대 이후로 블록 소팅 알고리즘을 이용한 [Bzip2](../Page/Bzip2.md "wikilink")와 같은 더 발전된 포맷이 gzip을 대체하는 경우가 있다.

## 같이 보기

  - [압축 소프트웨어의 비교](https://ko.wikipedia.org/wiki/압축_소프트웨어의_비교 "wikilink")
  - [Tar (파일 포맷)](https://ko.wikipedia.org/wiki/Tar_\(파일_포맷\) "wikilink")
  - [Bzip2](../Page/Bzip2.md "wikilink")
  - [Xz](../Page/Xz.md "wikilink")

## 각주

## 외부 링크

  - [원래의 gzip 홈 페이지](http://www.gzip.org/)

[분류:크로스 플랫폼 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_소프트웨어 "wikilink") [분류:GNU 프로젝트 소프트웨어](https://ko.wikipedia.org/wiki/분류:GNU_프로젝트_소프트웨어 "wikilink") [분류:유닉스 보관 및 압축 관련 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_보관_및_압축_관련_유틸리티 "wikilink") [분류:무손실 압축 알고리즘](https://ko.wikipedia.org/wiki/분류:무손실_압축_알고리즘 "wikilink") [분류:C로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C로_작성된_자유_소프트웨어 "wikilink") [분류:자유 압축 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_압축_소프트웨어 "wikilink")

1.