> This article is converted from Wikipedia: [OLE 자동화](https://ko.wikipedia.org/wiki/OLE_자동화).


[마이크로소프트 윈도우](../Page/마이크로소프트_윈도우.md "wikilink") 애플리케이션 프로그래밍에서 **OLE 자동화**(OLE Automation, 나중에는 간단히 **자동화**로 이름이 변경됨\[1\]\[2\])는 [마이크로소프트](../Page/마이크로소프트.md "wikilink")가 개발한 [프로세스 간 통신](../Page/프로세스_간_통신.md "wikilink")(IPC) 매커니즘이다. [컴포넌트 오브젝트 모델](../Page/컴포넌트_오브젝트_모델.md "wikilink")(COM)의 하위 집합에 기반을 두며, [스크립트 언어](../Page/스크립트_언어.md "wikilink")(원래는 비주얼 베이직)를 통해 사용되도록 고안되었으나 지금은 윈도우에서 여러 언어를 통해 사용할 수 있다. 모든 자동화 오브젝트들은 [IDispatch](https://ko.wikipedia.org/wiki/IDispatch "wikilink") 인터페이스의 구현이 요구된다. "자동화 컨트롤러"라는 이름의 응용 프로그램들이 다른 응용 프로그램들이 내보낸 공유 "자동화 오브젝트"를 접근하고 조작(예: 속성 설정 또는 메소드 호출)할 수 있는 인프라스트럭처를 제공한다. 애플리케이션이 다른 애플리케이션을 통제하는 더 오래된 매커니즘인 [동적 데이터 교환](https://ko.wikipedia.org/wiki/동적_데이터_교환 "wikilink")(DDE)를 대체한다.\[3\] DDE처럼 OLE 자동화에서 자동화 컨트롤러는 "클라이언트"이며 자동화 오브젝트를 내보내는 애플리케이션은 "서버"이다.

이름과 대조적으로 자동화 오브젝트는 반드시 마이크로소프트 [OLE를](../Page/객체_연결_삽입.md "wikilink") 사용할 필요는 없으나 자동화 오브젝트들 가운데 일부는 OLE 환경에서 사용이 가능하다. 이러한 혼동은 마이크로소프트의 초기 OLE 정의에 그 뿌리를 두고 있으며 이전에는 다소 COM과 동의어로 사용되기도 했다.

## 사용

### 지원 언어

자동화는 다음을 포함한 다양한 언어를 지원한다:

  - [ABAP](../Page/ABAP.md "wikilink")
  - [C](../Page/C_\(프로그래밍_언어\).md "wikilink")
  - [C++](https://ko.wikipedia.org/wiki/C++ "wikilink") (컴파일러 COM 지원,\[4\]

[MFC](../Page/마이크로소프트_파운데이션_클래스_라이브러리.md "wikilink") 또는 [ATL](https://ko.wikipedia.org/wiki/액티브_탬플릿_라이브러리 "wikilink") 등의 라이브러리와 함께)

  - [C\#](../Page/C_샤프.md "wikilink")
  - [비주얼 베이직](../Page/비주얼_베이직.md "wikilink"), [비주얼 베이직 포 애플리케이션](../Page/비주얼_베이직_포_애플리케이션.md "wikilink")
  - [델파이](../Page/오브젝트_파스칼.md "wikilink")\[5\]
  - [마이크로소프트 닷넷](https://ko.wikipedia.org/wiki/마이크로소프트_닷넷 "wikilink") 언어\[6\]
  - [APL](../Page/APL_\(프로그래밍_언어\).md "wikilink") (대부분 윈도우 버전)
  - [자바](../Page/자바_\(프로그래밍_언어\).md "wikilink") (서드파티 도구를 통해서만)
  - [J스크립트](../Page/J스크립트.md "wikilink")\[7\] and [VB스크립트](../Page/VB스크립트.md "wikilink")
  - [오픈 오브젝트 Rexx](https://ko.wikipedia.org/wiki/오픈_오브젝트_Rexx "wikilink")\[8\]
  - [펄](../Page/펄.md "wikilink")\[9\]
  - [PHP](../Page/PHP.md "wikilink")\[10\]
  - [파워빌더](../Page/파워빌더.md "wikilink")
  - [파이썬](../Page/파이썬.md "wikilink")\[11\]\[12\]
  - [루비](../Page/루비_\(프로그래밍_언어\).md "wikilink") (표준 루비 1.8.x 이상 배포판에 포함된 'win32ole'라이브러리를 통해)
  - [Tcl](../Page/Tcl.md "wikilink")\[13\]
  - [비주얼 데이터플렉스](https://ko.wikipedia.org/wiki/비주얼_데이터플렉스 "wikilink")
  - [WinBatch](https://ko.wikipedia.org/wiki/WinBatch "wikilink")\[14\]

## 같이 보기

  - [액티브X](../Page/액티브X.md "wikilink")
  - [액티브 스크립팅](https://ko.wikipedia.org/wiki/액티브_스크립팅 "wikilink")
  - [객체 연결 삽입](../Page/객체_연결_삽입.md "wikilink") (OLE)
  - [컴포넌트 오브젝트 모델](../Page/컴포넌트_오브젝트_모델.md "wikilink") (COM)

## 각주

## 외부 링크

  - [OLE Automation](https://web.archive.org/web/20120208104440/http://www.skolob.co.uk/skolob/index.php?op=ViewArticle&articleId=5&blogId=1) General paper on the introduction and problems implementing OLE.

  - "[VOLE - A Neat C++ COM/Automation Driver](http://vole.sourceforge.net/)" — an open-source, compiler-independent C++ COM Automation driver library, for use when having to drive IDispatch directly. VOLE is highly robust, fully encapsulates all "low-level" aspects of IDispatch, and is very flexible, taking and returning normal C++ types.

  -
  -
  -
  - — full printed documentation of the object model of Microsoft Office

[분류:객체 지향 프로그래밍](https://ko.wikipedia.org/wiki/분류:객체_지향_프로그래밍 "wikilink") [분류:마이크로소프트 API](https://ko.wikipedia.org/wiki/분류:마이크로소프트_API "wikilink")

1.
2.
3.   — McComb describes how to use OLE Automation instead of DDE to control [워드퍼펙트](../Page/워드퍼펙트.md "wikilink")
4.
5.
6.
7.   — despite the title, the article discusses [JScript](https://ko.wikipedia.org/wiki/JScript "wikilink") rather than [JavaScript](https://ko.wikipedia.org/wiki/JavaScript "wikilink")
8.
9.
10.
11.
12.
13.
14.