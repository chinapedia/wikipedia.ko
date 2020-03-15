> This article is converted from Wikipedia: [JFace](https://ko.wikipedia.org/wiki/JFace).


**JFace**는 [이클립스에서](https://ko.wikipedia.org/wiki/이클립스_\(소프트웨어\) "wikilink") 사용되는 일반적인 [사용자 인터페이스](https://ko.wikipedia.org/wiki/사용자_인터페이스 "wikilink")(UI)를 구현하기 위해 사용되는 툴킷(toolkit)이다. JFace는 [API](../Page/API.md "wikilink")와 구현에 있어서 윈도 시스템에 독립적이고 하위 [그래픽 사용자 인터페이스](https://ko.wikipedia.org/wiki/그래픽_사용자_인터페이스 "wikilink")(GUI)인 [SWT](https://ko.wikipedia.org/wiki/SWT "wikilink")를 숨기지 않고 같이 사용되도록 구현되어 있다.

주요 기능은 액션(actions)과 뷰어(viewers)로서 액션은 사용자의 명령이 어떠한 UI에서 발생되었는지를 상관하지 않고 동일하게 처리할 수 있는 추상적인 [매커니즘](https://ko.wikipedia.org/wiki/매커니즘 "wikilink")을 제공하고 뷰어는 특정 모델 기반의 [SWT](https://ko.wikipedia.org/wiki/SWT "wikilink") [위젯](https://ko.wikipedia.org/wiki/위젯 "wikilink")(widget)의 어댑터가 되어 자료를 [목록](https://ko.wikipedia.org/wiki/목록 "wikilink")(lists), [테이블](https://ko.wikipedia.org/wiki/테이블 "wikilink")(tables), [트리](https://ko.wikipedia.org/wiki/트리 "wikilink")(trees) 형태로 표현하는 기능을 간략히 할 수 있도록 제공한다.

위 내용을 포함한 JFace가 제공하는 기능은 다음과 같다.

1.  MVC가 적용된, 필터, 정렬, 업데이트 기능을 갖춘 뷰어들을 제공한다.
2.  액션을 정의하고, 적절한 위치에 배치하는(메뉴, 툴바, 버튼) 기능을 제공한다.
3.  표준 대화상자 및 마법사를 제공한다.
4.  이미지, 글꼴등을 관리하는 레지스트리를 제공한다.

## 사용

### SWT와의 사용

JFace는 하위 UI 시스템인 [SWT](https://ko.wikipedia.org/wiki/SWT "wikilink")를 대체하기 위하여 만들어진 것이 아니고 자주 쓰이는 UI Framework을 추상화 하도록 만들어졌기 때문에 단독으로는 쓰일 수 없고 [SWT](https://ko.wikipedia.org/wiki/SWT "wikilink")와 같이 사용해야 한다. 따라서 SWT/JFace와 같이 병기하여 표기하는 일이 많다.

### 스윙과의 차이

[스윙](https://ko.wikipedia.org/wiki/스윙 "wikilink")(Swing)은 [자바](https://ko.wikipedia.org/wiki/자바_\(프로그래밍_언어\) "wikilink") 1.1 버전부터 지원하는 그래픽 라이브러리로 기존의 [AWT](https://ko.wikipedia.org/wiki/AWT "wikilink")의 단점을 보완하고자 여러 플랫폼에서 동일한 모양으로 실행될 수 있도록 만들어진 자바 표준 그래픽 [라이브러리](https://ko.wikipedia.org/wiki/라이브러리 "wikilink")이다. 그러나 느린 속도와 복잡한 개발방식, 그리고 윈도 시스템별로 다른 UI를 제공하지 못하는 한계로 인하여 일반 사용자를 대상으로 한 프로그램에서는 대중적으로 사용되지 못하였다.

그에 반에 SWT/JFace는 해당 윈도 시스템의 화면 구성 컴퍼넌트를 직접 사용하기 때문에 실행하는 윈도 시스템별로 해당 시스템 고유의 그래픽을 보여줄 수 있고 속도 또한 빠르다.

다만 이러한 구현을 위해 내부적으로 [JNI](https://ko.wikipedia.org/wiki/JNI "wikilink")(Java Native Interface)를 사용하므로 자바의 기본적인 Write Once, Run Everywhere(한번만 작성하여 VM이 존재하는 어디든 구동한다.)라는 원칙을 지키지는 못한다. 그러나 주요 OS와 윈도 시스템을 지원하므로 대부분의 경우 플랫폼에 큰 제약을 받지 않는다.

그리고 이클립스 3.2버전 이상의 SWT/JFace에서는 Swing 뿐만 아니라 AWT와도 같이 사용할 수 있는 기능을 제공한다. \[1\]

### 버전별 종속성

JFace는 [이클립스](https://ko.wikipedia.org/wiki/이클립스 "wikilink")와 함께 쓰일 수도 있고 [RCP](https://ko.wikipedia.org/wiki/RCP "wikilink")(Rich Client Platform) 형태로 별도의 프로그램으로 실행될 수 있다.(이클립스 버전 3.2부터 [SWT](https://ko.wikipedia.org/wiki/SWT "wikilink"), org.eclipse.equinox.common, org.eclipse.core.commands만 의존성을 가짐.) \[2\]

이클립스 버전 3.3부터는 OSGi와 관계된 의존성 추가로 인하여 org.osgi.framework가 추가되었다.

## 각주

<references/>

## 같이 보기

  - [SWT](https://ko.wikipedia.org/wiki/SWT "wikilink")

## 외부 링크

  - [이클립스 JFace 위키 페이지](http://wiki.eclipse.org/JFace)

[분류:위젯 툴킷](https://ko.wikipedia.org/wiki/분류:위젯_툴킷 "wikilink") [분류:이클립스 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:이클립스_라이선스_소프트웨어 "wikilink")

1.  [SWT FAQ](http://www.eclipse.org/swt/faq.php#swinginswt)
2.  [Eclipse Bug 49497 \[RCP](https://bugs.eclipse.org/bugs/show_bug.cgi?id=49497#c55) JFace dependency on org.eclipse.core.runtime enlarges standalone JFace applications\]