> This article is converted from Wikipedia: [7-Zip](https://ko.wikipedia.org/wiki/7-Zip).


**7-Zip**(세븐집)은 [오픈 소스로](../Page/오픈_소스.md "wikilink") 배포되고 있는 [압축 소프트웨어이다](https://ko.wikipedia.org/wiki/압축_소프트웨어 "wikilink"). 이고르 파블로프가 개발하였다. [윈도우판으로는](../Page/마이크로소프트_윈도우.md "wikilink") 7-Zip의 이름으로, 그 외의 [플랫폼에서는](../Page/컴퓨팅_플랫폼.md "wikilink") p7-zip/EZ 7z(OS X에서만)의 이름으로 배포되고 있다. [윈도우 XP](../Page/윈도우_XP.md "wikilink") 64비트를 지원한 최초의 압축 프로그램이기도 하다.

버전 9.20까지는 32비트용은 [exe](../Page/EXE.md "wikilink") 및 [msi로](https://ko.wikipedia.org/wiki/마이크로소프트_인스톨러 "wikilink") 64비트용은 msi로 배포되고 있었으나, 현재는 전부 EXE형식으로 배포하고 있다. [GNU 약소 일반 공중 사용 허가서를](../Page/GNU_약소_일반_공중_사용_허가서.md "wikilink") 따르는 부분과 unRAR 계약서를 따르는 부분으로 이루어져 있다. [윈도우 CE용으로도](https://ko.wikipedia.org/wiki/윈도우_CE "wikilink") 배포되는데, [ARM](https://ko.wikipedia.org/wiki/ARM "wikilink")아키텍처만 지원한다.

## 지원 형식

7-Zip은 7z만이 아니라 다른 형식의 압축 파일도 지원한다.

  - 압축, 압축 해제 둘 다: [7z](https://ko.wikipedia.org/wiki/7z "wikilink"), [ZIP](https://ko.wikipedia.org/wiki/ZIP "wikilink"), [gzip](https://ko.wikipedia.org/wiki/gzip "wikilink"), [bzip2](https://ko.wikipedia.org/wiki/bzip2 "wikilink"), [tar](../Page/Tar_\(파일_포맷\).md "wikilink")
  - 압축 해제만: 마이크로소프트 캐비넷(CAB), RAR, [ARJ](../Page/ARJ.md "wikilink"), Z, LHA, cpio, smzip, JAR, ISO(CD 및 DVD 이미지 - 4.42판부터), [RPM](../Page/RPM_패키지_매니저.md "wikilink"), DEB

7-Zip은 주 내용과 함께 들어 있는 메타파일에의 접근을 통해 일부 MSI 파일도 열 수 있으며 NSIS 설치기 파일도 압축 파일을 열듯 열어 직접 실행하지 않고도 그 안에 있는 파일들을 꺼낼 수 있다. ZIP 또는 gzip 파일을 압축할 때에는 압축을 더 빨리 하기 위해 자체제작한 DEFLATE 압축기를 쓰는데 이것은 [zlib](https://ko.wikipedia.org/wiki/zlib "wikilink")의 그것보다 더 높은 압축 수준을 구현하며 [AdvanceCOMP](https://ko.wikipedia.org/wiki/AdvanceCOMP "wikilink")에서도 쓸 수 있다.

## 그 밖의 특징

  - 2 패널 모드(단축키: F9)를 켜면 [토탈 커맨더와](../Page/토탈_커맨더.md "wikilink") 비슷한 인터페이스로 바뀌며 이를 통해 파일 관리자로 쓸 수도 있다.
  - 다중 CPU, 다중 코어, 다중 쓰레딩을 지원한다.
  - 압축된 파일 이름이 깨져 있는 경우 임의로 이름을 바꾸어 압축을 풀 수 있다.
  - 단일 실행 압축 파일을 만들 수 있다(단, multi-volume 형식은 지원하지 않는다).
  - [RPM 패키지 매니저](../Page/RPM_패키지_매니저.md "wikilink") 파일이나 데비안 패키지 파일을 열 수 있어 윈도우에서 유용히 쓰이기도 한다.
  - 분할파일의 이름형식을 zip.001 을 사용해서, 사람들을 헤메게 만든적이 있다. 지금은 7z.001 을 쓴다.

## 변형판

  - p7zip: [리눅스](../Page/리눅스.md "wikilink"), [OS X](https://ko.wikipedia.org/wiki/OS_X "wikilink"), [FreeBSD](../Page/FreeBSD.md "wikilink") 등에서 쓸 수 있는 CLI 이식판. 외장 라이브러리를 쓰는 7z과 내장 라이브러리를 쓰는 7za로 나뉘며 7za는 단일 파일로도 실행할 수 있으나 지원하는 압축 형식이 ZIP, gzip, bzip2, Z, tar로 한정되어 있다.
      - [HX DOS Extender](https://web.archive.org/web/20090130063413/http://www.japheth.de/HX.html) 를 사용하면 7z 또는 7za를 도스에서 실행할 수 있다.\[1\]
  - Q7Z: p7zip의 GUI [프론트엔드](https://ko.wikipedia.org/wiki/프론트엔드 "wikilink")로 [리눅스](../Page/리눅스.md "wikilink")용이다. [파이썬](../Page/파이썬.md "wikilink")에 [Qt를](https://ko.wikipedia.org/wiki/Qt_\(프레임워크\) "wikilink") 곁들여 만들어졌다.
  - \#7Z: p7zip의 윈도우용 GUI 프론트엔드
  - jZip: 7-Zip을 바탕으로 만들어진 윈도우용 압축 관리기. 7-Zip보다 더 쉽고 더 간결한 인터페이스를 가졌다. 프리웨어이나 소스코드는 공개되어 있지 않다.

## 같이 보기

  - [7z](https://ko.wikipedia.org/wiki/7z "wikilink")
  - [압축 소프트웨어의 비교](https://ko.wikipedia.org/wiki/압축_소프트웨어의_비교 "wikilink")

## 각주

## 외부 링크

  -
  -
  - [7-Zip 공식 사이트](http://www.7-zip.org)

  - [p7zip 공식 사이트](http://p7zip.sourceforge.net/)

  - [Q7Z, \#7Z 공식 사이트](http://code.google.com/p/k7z/)

  - [jZip 공식 사이트](http://www.jzip.com/)

[분류:파일 관리자](https://ko.wikipedia.org/wiki/분류:파일_관리자 "wikilink") [분류:압축 소프트웨어](https://ko.wikipedia.org/wiki/분류:압축_소프트웨어 "wikilink") [분류:크로스 플랫폼 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_자유_소프트웨어 "wikilink") [분류:윈도우 소프트웨어](https://ko.wikipedia.org/wiki/분류:윈도우_소프트웨어 "wikilink") [분류:1999년 소프트웨어](https://ko.wikipedia.org/wiki/분류:1999년_소프트웨어 "wikilink") [분류:포터블 소프트웨어](https://ko.wikipedia.org/wiki/분류:포터블_소프트웨어 "wikilink") [분류:C로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C로_작성된_자유_소프트웨어 "wikilink") [분류:C++로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C++로_작성된_자유_소프트웨어 "wikilink") [분류:LGPL 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:LGPL_라이선스_소프트웨어 "wikilink") [분류:자유 압축 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_압축_소프트웨어 "wikilink")

1.  [7-Zip::Links](http://www.7-zip.org/links.html) 참조.