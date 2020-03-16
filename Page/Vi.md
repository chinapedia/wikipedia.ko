> This article is converted from Wikipedia: [Vi](https://ko.wikipedia.org/wiki/Vi).


**vi**(브이아이, )는 [Emacs](https://ko.wikipedia.org/wiki/Emacs "wikilink")와 함께 [유닉스](../Page/유닉스.md "wikilink") 환경에서 가장 많이 쓰이는 [문서 편집기이다](../Page/문서_편집기.md "wikilink"). [1976년](../Page/1976년.md "wikilink") [빌 조이가](../Page/빌_조이.md "wikilink") 초기 [BSD](../Page/BSD.md "wikilink") 릴리즈에 포함될 편집기로 만들었다. vi라는 이름은 한 줄씩 편집하는 [줄단위 편집기가](https://ko.wikipedia.org/wiki/줄단위_편집기 "wikilink") 아니라 한 화면을 편집하는 비주얼 에디터(visual editor)라는 뜻에서 유래했다. 간결하면서도, 강력한 기능으로 열광적인 사용자가 많다.

현재는 오리지널 vi를 사용하는 경우는 거의 없고, 일반적으로 기능을 모방하여 만들어진 클론을 사용하고 있다. 이런 클론 중 많이 쓰이는 것은 기능이 다양한 것을 장점으로 내세우며, 리눅스 배포판에 포함되는 [Vim](../Page/Vim.md "wikilink"), 그리고, [BSD](../Page/BSD.md "wikilink") 라이선스로 제공되며 원본 vi의 동작과 호환성으로 정평이 나 있는 [nvi](https://ko.wikipedia.org/wiki/nvi "wikilink"), 독자적인 팬층을 확보한 elvis등이 있다.

## vi의 역사

[섬네일](https://ko.wikipedia.org/wiki/파일:KB_Terminal_ADM3A.svg "wikilink") [빌 조이는](../Page/빌_조이.md "wikilink") [캘리포니아 대학교 버클리에서](../Page/캘리포니아_대학교_버클리.md "wikilink") [Lear-Siegler](https://ko.wikipedia.org/wiki/:en:Lear-Siegler "wikilink") [ADM3A](https://ko.wikipedia.org/wiki/ADM3A "wikilink") [터미널에서](https://ko.wikipedia.org/wiki/터미널_\(컴퓨터\) "wikilink") vi를 작성했다. 그런데 이 [터미널의](https://ko.wikipedia.org/wiki/터미널_\(컴퓨터\) "wikilink") 키보드는  키가 오른쪽 현재의 우리가 많이 사용하는 IBM 호환 키보드([IBM PC 키보드](https://ko.wikipedia.org/wiki/IBM_PC_키보드 "wikilink")) 에서  키 위치에 있었기 때문에, 이 키를 가지고 사용자들이 vi 에디터 모드 변경을 매우 효과적으로 할 수 있었다. 또한 Lear-Siegler ADM3A [터미널에는](https://ko.wikipedia.org/wiki/터미널_\(컴퓨터\) "wikilink") 화살표 키에 대응할 만한 키가 없었기 때문에 vi는 [H, J, K, L 키](https://ko.wikipedia.org/wiki/HJKL_키 "wikilink")([keys *h*,*j*,*k*,*l*](https://ko.wikipedia.org/wiki/:en:HJKL_keys "wikilink"))가 지금의 화살표 키를 대신해서 커서를 이동하게 만들어졌다.

## 조작법

프로그램을 시작하면 일반적으로 명령(normal) 모드로 시작하게 된다. 이때 키보드에서  키를 누르게 되면 편집(insert)모드로 들어가게 된다.  키를 누를 때까지 문서 작성을 할 수 있다. vi에서는 편집모드에서만 내용을 넣거나 수정할 수 있다.

### Vi의 여러가지 명령어

vi 편집기는 입력, 명령, 비주얼 등의 모드가 있어 같은 키 입력이라도 현재 모드에 따라 다른 동작을 한다. 입력과 명령모드를 주로 왔다갔다 하면서 편집하게 된다. 입력모드에서는 말 그대로 입력하는 문자가 그대로 문서에 입력된다. 입력상태에서  키를 누르면 명령모드로 바뀌게 된다. 명령어 모드에서는 나  키 등을 사용하지 않고도 키를 두드려서 커서의 움직임이나, 붙여넣기, 지우기 등의 기능을 수행할 수 있다. 예를 들면, 는 커서를 아래로, 는 위로 움직이게 하며, 는 커서 위치의 한 문자를 지우고, 는 입력상태로 들어가게 한다. 명령어 모드에서  키 등을 누르면 비주얼 모드가 되고 영역을 설정할 수 있게 된다. vi 실행 초기의 모드는 명령모드이기 때문에, vi를 처음 사용하는 사용자들은 아무리 키를 눌러도 누른 키가 입력이 되지 않아 당황하는 경우가 많다.

## 기종별 다양한 Vi

물론 Vi는 [유닉스](../Page/유닉스.md "wikilink")에서 발전하였고 조금 더 개량한 vi 복제품들이 나와서 그 명성을 이어가고 있다. 또한 다음과 같이 다양한 컴퓨터에 포팅되어 있다. [섬네일](https://ko.wikipedia.org/wiki/파일:Vim.PNG "wikilink")\]\]

### [유닉스](../Page/유닉스.md "wikilink")용 vi 복제품(clone)

[Vim](../Page/Vim.md "wikilink") 은 "Vi IMproved"의 약자로 만든 이름이며 현재 vi보다 더 많이 사용되고 있다. 이 프로그램은 vi보다 더 다양한 기능([구문 강조](../Page/구문_강조.md "wikilink") 기능(또한 이 기능을 작성하는 기능), [마우스](../Page/마우스.md "wikilink") 지원, 그래픽 버전, 시각 모드, 수많은 새로운 편집 명령어들을 가지고 있다. 현재 대부분의 [리눅스](../Page/리눅스.md "wikilink") 시스템에서는 이 프로그램이 표준 모델로 들어가고 있다.

### Mac용 vim

  - [macvim: Vim for the Mac](http://code.google.com/p/macvim/): 가장 최근에 나온 맥용 Vi

## vi에 대한 다양한 평가 및 vi의 영향력

  - [emacs](https://ko.wikipedia.org/wiki/emacs "wikilink") 애용자들은 vi를 *vicious interface*라고 한다.
  - Snap.com 은 vi 인터페이스를 사용하는 인터넷 검색 엔진을 개발했다. visearch.com [웹페이지](http://www.visearch.com/)

## 외부 링크

  - [Vi Lovers 홈페이지](http://www.thomer.com/vi/vi.html)
  - [한국 Vi 사용자 모임](http://vi.kldp.org/)
  - [Vi/vim 단축키 모음](http://kldp.org/node/102947)

[Vi](https://ko.wikipedia.org/wiki/분류:Vi "wikilink") [분류:자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_소프트웨어 "wikilink") [분류:유닉스 문서 편집기](https://ko.wikipedia.org/wiki/분류:유닉스_문서_편집기 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink") [분류:BSD 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:BSD_라이선스_소프트웨어 "wikilink") [분류:자유 문서 편집기](https://ko.wikipedia.org/wiki/분류:자유_문서_편집기 "wikilink")