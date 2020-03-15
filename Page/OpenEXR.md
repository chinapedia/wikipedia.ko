> This article is converted from Wikipedia: [OpenEXR](https://ko.wikipedia.org/wiki/OpenEXR).


**OpenEXR**은 [ILM에서](../Page/인더스트리얼_라이트_&_매직.md "wikilink") 개발한 [HDR](https://ko.wikipedia.org/wiki/HDRI "wikilink") 이미지 포맷이다. [자유 소프트웨어](../Page/자유_소프트웨어.md "wikilink") 라이선스로 공개되었다.\[1\] 채널당 16비트 이상의 컬러를 사용할 수 있으며, 비손실 압축 기법을 지원한다. [2003년](../Page/2003년.md "wikilink") 발표되었고, 주로 영화업계에서 사용되고 있다.

이것은 잠재적으로 다른 픽셀 크기의 다중 채널을 지원하는 것은 주목할만한 특징이다. 또한 임의의 채널을 가질 수 있으며 왼쪽 및 오른쪽 카메라 이미지와 같은 여러 시점을 인코딩할 수 있기에 입체적인 기술을 지원하는 그래픽 포맷이다.\[2\]

예를 들면, 기존의 이미지 처리에서는 컬러에대한 정보만을 주로 다루었지만, [조지 루카스는](https://ko.wikipedia.org/wiki/조지_루카스 "wikilink") 이미지정보에 컬러뿐만 아니라, 현장 요구에 부응하는 [알파채널](https://ko.wikipedia.org/wiki/알파채널 "wikilink")이나 카메라 앵글에 대한 정보를 담는 파일 포맷을 필요로 했고 이를 개발해냈다.

## 기술

EXR 형식의 완전한 기술적인 소개는 무료로 OpenEXR.org 공식 웹 사이트에서 제공되는데, 이러한 기술의 혜택 뿐만아니라 수정및 변형을 통한 커스터마이징이 가능하다.

## OpenEXR로 개발하기

OpenEXR [라이브러리는](../Page/라이브러리_\(컴퓨팅\).md "wikilink") [C++](https://ko.wikipedia.org/wiki/C++ "wikilink") 로 개발되었으며 [Microsoft Windows](https://ko.wikipedia.org/wiki/Microsoft_Windows "wikilink") , [macOS](https://ko.wikipedia.org/wiki/macOS "wikilink") 및 [Linux](https://ko.wikipedia.org/wiki/Linux "wikilink") 용 소스 형식 및 컴파일된 형식으로 사용할 수 있다. 라이브러리를위한 [파이썬](../Page/파이썬.md "wikilink") 바인딩도 사용할 수 있다.\[3\]

2006년 6월 8일에 릴리스된 버전 1.3.0부터는 OpenEXR에 다중 스레드 읽기 및 쓰기 기능이 추가되었다. 다중 스레드 읽기 및 쓰기는 다중 코어 또는 CPU가 있는 시스템의 성능을 향상시키는데, 이것이 의미하는 바는 [렌더링](../Page/렌더링.md "wikilink") 시에 [베오울프같은](../Page/베오울프_클러스터.md "wikilink") 병렬 처리 슈퍼컴퓨팅을 이용하는데 최적화된다. OpenEXR은 [쓰레드](https://ko.wikipedia.org/wiki/쓰레드 "wikilink") 풀(thread pool)을 사용하여 읽기 및 쓰기를 처리한다.

## 같이 보기

  - [하이 다이내믹 레인지 이미징](../Page/하이_다이내믹_레인지_이미징.md "wikilink")
  - [픽사](../Page/픽사.md "wikilink")의 [랜더맨](https://ko.wikipedia.org/wiki/랜더맨 "wikilink")

## 참고문헌

  - [openEXR](https://web.archive.org/web/20170721234341/http://www.openexr.com/OpenEXR_Press_Release_1_22_03.pdf)

## 각주

## 외부 링크

  - [OpenEXR - ILM](http://www.openexr.com/)

[분류:그래픽 파일 포맷](https://ko.wikipedia.org/wiki/분류:그래픽_파일_포맷 "wikilink") [분류:오픈 포맷](https://ko.wikipedia.org/wiki/분류:오픈_포맷 "wikilink") [분류:BSD 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:BSD_라이선스_소프트웨어 "wikilink") [분류:자유 그래픽 스포트웨어](https://ko.wikipedia.org/wiki/분류:자유_그래픽_스포트웨어 "wikilink")

1.
2.
3.  <https://pypi.python.org/pypi/OpenEXR>