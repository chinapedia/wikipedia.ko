> This article is converted from Wikipedia: [Python Imaging Library](https://ko.wikipedia.org/wiki/Python_Imaging_Library).


**Python Imaging Library**(PIL)은 [파이썬](../Page/파이썬.md "wikilink") [인터프리터](../Page/인터프리터.md "wikilink")에 다양한 [이미지](https://ko.wikipedia.org/wiki/이미지 "wikilink") 파일 형식을 지원하고 강력한 [이미지 처리와](https://ko.wikipedia.org/wiki/이미지_처리 "wikilink") [그래픽](https://ko.wikipedia.org/wiki/그래픽 "wikilink") 기능을 제공하는 [자유-오픈 소스 소프트웨어](../Page/자유-오픈_소스_소프트웨어.md "wikilink") [라이브러리](https://ko.wikipedia.org/wiki/라이브러리 "wikilink")이다. 줄여서 **PIL**이라고 부른다. [윈도우](https://ko.wikipedia.org/wiki/윈도우 "wikilink")와 [맥 오에스 엑스](https://ko.wikipedia.org/wiki/맥_오에스_엑스 "wikilink"), [리눅스](../Page/리눅스.md "wikilink")를 지원한다. PIL의 최신 버젼은 1.1.7이고 2009년 9월에 릴리즈 되었으며 [파이썬](../Page/파이썬.md "wikilink") 1.5-2.7을 지원한다.

개발은 2011년 PIL 저장소에 대한 마지막 커밋으로 중단된 것으로 보이며 **Pillow**라는 후속 프로젝트가 PIL 저장소에서 갈려져 나와 Python 3.x 지원을 추가 했다. Pillow는 PIL 후속 프로젝트로써 [데비안](../Page/데비안.md "wikilink") 및 [우분투](https://ko.wikipedia.org/wiki/우분투 "wikilink") 등의 [리눅스 배포판에서](../Page/리눅스_배포판.md "wikilink") PIL을 대체하기 위해서 채택 되었다.

## 지원하는 이미지 형식

지원되는 파일 형식 중에는 [PPM](https://ko.wikipedia.org/wiki/PPM "wikilink") , [PNG](../Page/PNG.md "wikilink") , [JPEG](../Page/JPEG.md "wikilink") , [GIF](../Page/GIF.md "wikilink") , [TIFF](https://ko.wikipedia.org/wiki/TIFF "wikilink") , [BMP](https://ko.wikipedia.org/wiki/BMP "wikilink") 등의 이미지 형식을 지원 하고 있고 지원하지 않는 파일 형식은 라이브러리를 확장해서 새로운 파일 [디코더](https://ko.wikipedia.org/wiki/디코더 "wikilink")를 만드는 것이 가능하다.

## 기능

PIL 이미지 작업을 위한 표준 절차를 제공하고 있으며, 다음과 같은 것이있다.

  - 픽셀 단위의 조작
  - 마스킹 및 투명도 제어
  - 흐림, 윤곽 보정 다듬어 윤곽 검출 등의 이미지 필터
  - 선명하게, 밝기 보정, 명암 보정, 색 보정 등의 화상 조정
  - 이미지에 텍스트 추가
  - 기타 여러가지

## 사용 예제

이 예제는 하드 드라이브에서 이미지를 읽어 흐리게 만듭니다.

``` python numberLines
from PIL import Image, ImageFilter  # 라이브러리를  임포트 한다.

original = Image.open("file.ppm") # 하드 드라이브에서 이미지를 읽어 들인다.
blurred = original.filter(ImageFilter.BLUR) # 이미지를 흐리게 한다.

original.show() # 두 이미지를 디스플레이 한다.
blurred.show()
```

## 참조

## 외부 링크

  -
  - [PIL Library reference](http://www.pythonware.com/library/pil/handbook/)

  - [Pillow (Successor project)](http://python-pillow.org)

[분류:파이썬 라이브러리](https://ko.wikipedia.org/wiki/분류:파이썬_라이브러리 "wikilink") [분류:그래픽 라이브러리](https://ko.wikipedia.org/wiki/분류:그래픽_라이브러리 "wikilink")