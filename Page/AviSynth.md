> This article is converted from Wikipedia: [AviSynth](https://ko.wikipedia.org/wiki/AviSynth).


**AviSynth**는 마이크로소프트 윈도에서 구동되는 [frameserver](https://ko.wikipedia.org/wiki/frameserver "wikilink") 프로그램으로 [밴 로디악 굴드에](https://ko.wikipedia.org/wiki/밴_로디악_굴드 "wikilink") 의해 개발되었으며 라이선스는 [GNU](../Page/GNU.md "wikilink")의 [GPL](https://ko.wikipedia.org/wiki/GPL "wikilink")에 따라 배포되고 있다. 그리고 일부 필터의 기능은 v2.5.7 릴리즈 이후 버전부터 [크리에이티브 커먼즈](../Page/크리에이티브_커먼즈.md "wikilink") Attribution-ShareAlike 3.0 License를 따른다.

[frameServer](https://ko.wikipedia.org/wiki/frameServer "wikilink")는 [동영상](https://ko.wikipedia.org/wiki/동영상 "wikilink")과 같이 용량이 큰 파일을 인코딩이나 디코딩시 한꺼번에 로딩하지 않고 필요한 부분만 조금씩 프로세싱 해주는 역할을 담당한다.

## 기능

AviSynth는 입력된 영상을 전개해, 여러가지 필터를 걸쳐 가공한 영상을 다른 동영상 편집 소프트웨어에 건네줄 수 있다.표준으로 다양한 화상 처리 필터를 갖추고 있다.또, 유저가 개발한 플러그 인의 추가도 가능하다.

AviSynth를 사용함으로써 기대되는 효과로는 1) 다양한 포맷의 동영상을 로딩할 수 있다. 2) 영상의 포맷변환, 크기변환, 프레임레이트 변환이 쉽다. 3) AviSynth Script인 [AVS](https://ko.wikipedia.org/wiki/AVS "wikilink")를 사용하여 임시파일이 필요없으며 즉시 편집을 지원, 다양한 비디오 편집 및 처리 방법을 제공한다. 4) 각 프레임당 그림으로 저장이 아닌 스크립트(문자)형태로 저장할 수 있다는 점이다.

## AviSynth 스크립트 언어

AviSynth 스크립트 언어인 [AviScript](https://ko.wikipedia.org/wiki/AviScript "wikilink")는 AviSynth를 [frameserver](https://ko.wikipedia.org/wiki/frameserver "wikilink")로서 사용하기 위한 [인터프리터](../Page/인터프리터.md "wikilink") 언어이며 이를 파일형태로 지원하기 위한 확장자로 AVS가 사용된다. AVS를 확장자로 가지는 파일을 실행 하였을 때 편집에 사용된 원본의 영상과 효과를 FrameServing하여 보여주게 되며 frameserver에서는 스크립트를 해석하여 [다이렉트쇼](../Page/다이렉트쇼.md "wikilink")로 인터프리팅 하게 된다.

### AviSynth 스크립트 언어의 특징

AviSynth 스크립트 언어는 인터프리터의 특징을 가지고 있는대 문법이 [C언어](https://ko.wikipedia.org/wiki/C언어 "wikilink")와 유사하다. AVS의 특징을 간략히 기술하면 다음과 같다.

1.  스크립트 변수는 거의 모든 길이의 문자열을 사용할 수 있으며 영어, 숫자를 포함하고 있다. 하지만 다른 문자나 숫자로 시작할 수 없다.
2.  비디오 클립을 비디오 및 오디오가 포함된, 스크립트 유형의 값을 반환해야 하며 클립이 액세스 할 수 있는 다양한 속성을 자체 필터로서 보유하고 있어야 한다.
3.  문자 텍스트를 나타내는 시퀀스는. 문자열의 반환 가능한 텍스트중 하나를 따옴표에 의해 둘러 쌓이게 되며, 텍스트 종료 인용 부호 혹은 트리플 인용 시퀀스를 제외한 모든 문자를 사용할 수 있다.
4.  프로그래밍 언어에서 주로 사용하는 조건문인 if 문을 지원하며, C언어와 유사한 삼항 연산자를 사용할 수 있다.

### "Hello World"

"Hello, world\!"라는 단어를 포함한 비디오를 생성하는 간단한 "[Hello World 프로그램](https://ko.wikipedia.org/wiki/Hello_World_프로그램 "wikilink")"은 다음과 같다.

```
 BlankClip()
 Subtitle("Hello, world!")
```

## 한계점

AviSynth를 사용하기위해서는 다음과 같은 한계가 있다. 우선 AviSynth 패키지를 사용자의 피씨에 설치해야 한다. 이는 [DirectX](../Page/DirectX.md "wikilink")에서 다이렉트쇼를 통해 프로세싱하기 위해서이다. 그리고 AviSynth는 사용자의 PC에 설치되어 있는 [코덱](../Page/코덱.md "wikilink")에 의존적이다. 코덱이 설치되지 않은 PC에서는 해당 코덱을 사용하여 인코딩된 영상을 디코딩하지 못하게 되며(코덱 의존적임), 이는 결국 편집 및 재생에 대한 frameserving이 불가능하다는 것이다. 마지막으로 AVS 파일 작성 시 폴더나 파일명은 반드시 8+3규칙을 따라야 한다. AviSynth는 원래 DOS를 기반으로 만들어진 프로그램이기 때문에 반드시 영문 8자(빈칸 없이)이내, 확장자는 3자이여야 한다는 한계가 있다.

## 외부 링크

  -
  - [소스포지 프로젝트 링크](http://sourceforge.net/projects/avisynth2/?source=directory)

[분류:윈도우 전용 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:윈도우_전용_자유_소프트웨어 "wikilink")