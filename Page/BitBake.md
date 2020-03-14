> This article is converted from Wikipedia: [BitBake](https://ko.wikipedia.org/wiki/BitBake).


**BitBake**는 [임베디드 리눅스의](https://ko.wikipedia.org/wiki/임베디드_리눅스 "wikilink") [크로스 컴파일](https://ko.wikipedia.org/wiki/크로스_컴파일 "wikilink") 과정을 위한 패키지와 관련파일들을 [빌드](https://ko.wikipedia.org/wiki/빌드 "wikilink")하는 데 사용되는 툴이다.

## BitBake Recipes

BitBake recipes는 특정패키지에 대한 빌드방법을 구체화하고, 패키지들의 의존성, 위치, 설정법, 컴파일, 빌드, 설치 및 제거정보를 포함한다. 그리고 패키지의 [메타데이터](https://ko.wikipedia.org/wiki/메타데이터 "wikilink") 정보를 표준화된 변수들로 가지고 있다.

BitBake recipes는 패키지의 소스 URL ([http](https://ko.wikipedia.org/wiki/http "wikilink"), [https](https://ko.wikipedia.org/wiki/https "wikilink"), [ftp](https://ko.wikipedia.org/wiki/ftp "wikilink"), [cvs](https://ko.wikipedia.org/wiki/Concurrent_Versions_System "wikilink"), [svn](https://ko.wikipedia.org/wiki/Apache_Subversion "wikilink"), [git](https://ko.wikipedia.org/wiki/Git_\(software\) "wikilink"), 로컬 파일 시스템), 패키지간의 의존성, 컴파일, 설치옵션들로 구성 되어있다. 빌드 진행중에 BitBake recipes는 패키지의 의존성을 추적하고, 네이티브 혹은 크로스 컴파일을 로컬 혹은 타겟 장치에 맞게 수행한다. 루트 [파일 시스템과](https://ko.wikipedia.org/wiki/파일_시스템 "wikilink") 완전한 이미지를 생성할 수 있다. 또한 타겟 플랫폼에 맞는 크로스 컴파일 [툴체인](https://ko.wikipedia.org/wiki/툴체인 "wikilink")을 생성한다.

## 같이 보기

  - [욕토 프로젝트](https://ko.wikipedia.org/wiki/욕토_프로젝트 "wikilink")

## 외부 링크

  - [BitBake User Manual](https://archive.is/20130415130259/http://docs.openembedded.org/bitbake/html/)

[분류:임베디드 리눅스](https://ko.wikipedia.org/wiki/분류:임베디드_리눅스 "wikilink") [분류:빌드 자동화](https://ko.wikipedia.org/wiki/분류:빌드_자동화 "wikilink") [분류:파이썬으로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:파이썬으로_작성된_자유_소프트웨어 "wikilink")