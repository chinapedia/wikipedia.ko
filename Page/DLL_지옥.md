> This article is converted from Wikipedia: [DLL 지옥](https://ko.wikipedia.org/wiki/DLL_지옥).


**DLL 지옥**()은 [마이크로소프트 윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 기반의 프로그램에서 [DLL을](../Page/동적_링크_라이브러리.md "wikilink") 사용할 경우 발생할 수 있는 복잡성을 뜻하는 말이다. 이 용어는 릭 엔더슨(Rick Anderson)이 [2000년](../Page/2000년.md "wikilink") [1월](../Page/1월.md "wikilink")에 발표한 〈DLL 지옥의 종말(The End of DLL Hell)〉 이라는 문서를 통해 대중에 소개되었다. 그 전에는 잠시 동안 [마이크로소프트](../Page/마이크로소프트.md "wikilink") 내부에서 사용되었다.

DLL 지옥은 DLL을 관리할 때 발생할 수 있는 모든 문제를 뜻한다. 여기에는 DLL 버전 충돌 문제, 프로그램이 의존하는 DLL 파일을 찾을 때의 어려움, 불필요한 DLL 파일 복사본이 만들어지는 문제 등이 포함된다.

DLL 지옥은 잠재적인 운영 체제 설계 결함의 한 예이다. 이 결함으로 인해 잘 작성된 프로그램도 문제를 일으킬 수 있는데, 이는 허술하게 작성된 프로그램의 나쁜 프로그래밍 습관이나 버그로부터 영향을 받을 수 있고, 이를 운영체제가 묵인하기 때문이다.

## 문제점

DLL을 사용하다 보면 많은 문제들에 마주치게 되는데, 이는 특히 시스템에 많은 프로그램을 설치한 후 제거한 상황이라면 더욱 두드러진다. 이중 가장 일반적이면서도 까다로웠던 문제는 시스템 DLL이 다른 버전의 DLL로 덮어 써져서, 일부 애플리케이션이 동작하지 않게 되는 경우였다. 마이크로소프트에서 'DLL 스탐핑(DLL Stomping)'이라고도 부르는 이러한 DLL 덮어쓰기 문제는 [윈도 2000을](https://ko.wikipedia.org/wiki/마이크로소프트_윈도의_역사 "wikilink") 통해 소개된 윈도 파일 보호(Windows File Protection, WFP)[1](https://web.archive.org/web/20060811234801/http://www.microsoft.com/whdc/winlogo/drvsign/wfp.mspx) 기능을 통해 대부분 해결되었다. WFP이 있기 전에는 다음과 같은 원인들 때문에 DLL 호환 관련 문제가 발생했었다:

  - 의무적인 표준 DLL 버전 관리 방식과 이름 짓기, 파일 시스템 위치 스키마가 없었다는 점.
  - 의무적인 표준 소프트웨어 설치 방법이 없었다는 점.
  - DLL [애플리케이션 이진 인터페이스](https://ko.wikipedia.org/wiki/애플리케이션_이진_인터페이스 "wikilink") 관리를 위한 중앙 집중적인 권위 있는 지원이 없었다는 점.
  - 파일 이름이 같은 서로 호환되지 않는 DLL들을 허용할 수 있는 안전 장치가 없었다는 점.
  - 배포되는 버전 구별을 위한 내부 버전 번호가 없었다는 점.
  - 사용자가 의심스러운 DLL을 복사하거나, 기존의 DLL을 변경하는 것을 예방하는 간단한 관리 도구조차 없었다는 점.

DLL 호환 문제 해결을 위한 '병렬식 컴포넌트 공유(Side-by-Side Component Sharing)'[2](http://msdn.microsoft.com/library/default.asp?url=/library/en-us/dnsetup/html/sidebyside.asp) 같은 일부 예방 기법은 DLL의 복사본을 만들고, 각 버전의 DLL들이 필요에 따라 따로 메모리로 올려지도록 하기 때문에, DLL 공유에 따른 메모리 절약 효과가 감소하게 된다. 또한 버그 수정과 보안 업데이트 시에도 복잡성 증가 등의 영향을 받게 된다.

## 사례들

DLL 지옥은 위에서 보는 것처럼 윈도 2000 이전에는 매우 일반적인 현상이었다. DLL 지옥의 주요 원인은 운영 체제에서 DLL 설치에 대해 어떠한 제한도 하지 않았다는 점이다. 운영 체제는 단지 애플리케이션 설치 프로그램이 항상 올바르게 동작하기를 바랐으며, 시스템 DLL을 덮어 쓰기 전에 DLL의 버전을 확인해야 하는 것도 설치 프로그램의 몫이었다. 애플리케이션의 설치를 단순화하는 표준 도구 프로그램들은 마이크로소프트와 기타 업체들에 의해 제공되었다. 마이크로소프트는 자사 로고의 사용 승인을 받길 원하는 소프트웨어 벤더들에게 먼저 표준 인스톨러를 사용하여 올바르게 동작하는 보증된 설치 프로그램을 만들 것을 요구하기도 하였다. DLL 설치에 대한 이러한 접근 방법은 그리 큰 해결책은 되지 못했으며, 사용자는 [인터넷](../Page/인터넷.md "wikilink")의 인기에 따라 올바른 설치 프로그램을 가지지 않는 애플리케이션을 접할 기회가 점점 더 많아져 갔다.

제임스 도널드(James Donald)는 자신의 [2003년](../Page/2003년.md "wikilink")도 문서 〈공유 라이브러리의 개선된 이식성(Improved Portability of Shared Libraries)[3](https://web.archive.org/web/20070926130800/http://www.princeton.edu/~jdonald/research/shared_libraries/cs518_report.pdf)〉에서 DLL 지옥이 마이크로소프트 윈도보다는 [리눅스](../Page/리눅스.md "wikilink")에서 더 심각하다고 주장하였다. 여러 [리눅스 배포판들은](../Page/리눅스_배포판.md "wikilink") 자신의 배포판에 맞춰 패키징되지 않은 [소프트웨어의](https://ko.wikipedia.org/wiki/컴퓨터_소프트웨어 "wikilink") [라이브러리](https://ko.wikipedia.org/wiki/라이브러리 "wikilink")를 업데이트하는데 있어 문제를 앓고 있는데, 이는 일부 [오픈 소스](../Page/오픈_소스.md "wikilink") 라이브러리가 버전이 바뀜에 따라 [API](../Page/API.md "wikilink")를 변경하는 경우도 있기 때문이다. 윈도 환경이 아닌 다른 곳에서는 이 문제를 [의존성 지옥이라](https://ko.wikipedia.org/wiki/의존성_지옥 "wikilink") 부른다. 그러나 이것과 DLL 지옥을 혼동해서는 안 된다. DLL 지옥은 의존성 지옥의 한 형태일 뿐이다.

마이크로소프트 윈도, 리눅스, [OS X을](https://ko.wikipedia.org/wiki/OS_X "wikilink") 통틀어 의존성 지옥에 대한 최근의 사례를 든다면 [모질라](../Page/모질라.md "wikilink") 프로젝트에서 사용하는 [게코 런타임 엔진](https://ko.wikipedia.org/wiki/게코_런타임_엔진 "wikilink")(Gecko Runtime Engine, GRE)을 꼽을 수 있다. 모질라 재단이 발표하는 모든 소프트웨어 제품은 각각 자신만의 게코 런타임 엔진을 포함하는데, 이는 프로그래밍 인터페이스가 서로 충돌할 수 있는 환경이기 때문이다. 따라서 만약 사용자가 [선더버드](../Page/모질라_선더버드.md "wikilink"), [파이어폭스](../Page/모질라_파이어폭스.md "wikilink"), [선버드를](../Page/모질라_선버드.md "wikilink") 설치하게 된다면, 사용자의 시스템에는 세 개의 GRE가 복사되게 된다. 이 세 개의 GRE는 언제 GRE의 [소스](../Page/소스_코드.md "wikilink") 트리로부터 갈래되었는지에 따라 서로 호환될 수도, 호환되지 않을 수도 있다. [에피퍼니](https://ko.wikipedia.org/wiki/에피퍼니 "wikilink")(Epiphany) 같은 모질라 재단 밖의 프로젝트는 GRE를 사용하기 위해 특정 버전의 [모질라 스위트](../Page/모질라_애플리케이션_스위트.md "wikilink")(Mozilla Suite)에 의존하는데, 이 경우 버전이 달라지면 동작하지 않게 된다. 반면에 [엔뷰](../Page/엔뷰.md "wikilink")(Nvu) 같은 프로젝트는 자신만의 GRE 복사본을 사용한다.

## 대응 수단

DLL 지옥을 피하는 데에는 여러 방법이 알려져 있으며, 이들 모두를 동시에 사용하면 최적의 효과를 얻을 수 있다:

  - **레지스트레이션-프리 COM**: [윈도 XP는](https://ko.wikipedia.org/wiki/윈도_XP "wikilink") '레지스트레이션-프리 COM(Registration-free COM, 등록이 필요없는 COM)'이라 불리는 새로운 [COM](../Page/컴포넌트_오브젝트_모델.md "wikilink") 오브젝트 등록 모드를 소개하였다. 이 기능은 [닷넷의](../Page/닷넷_프레임워크.md "wikilink") 발표와 맞물려 소개되었기 때문에 그리 잘 광고되지는 않았다. 레지스트레이션-프리 COM은 애플리케이션이 COM 오브젝트들을 설치할 때 COM 등록에 필요한 정보를 전역적인 [레지스트리가](https://ko.wikipedia.org/wiki/윈도_레지스트리 "wikilink") 아닌 자신의 디렉터리에 저장하여 사용할 수 있도록 한다. 엄밀히 말해 이 기능은 해당 COM 컴포넌트들을 단일 애플리케이션에서 사용할 경우에만 적용이 가능하다. 이 기능을 통해 각 애플리케이션은 자신에게 필요한 버전의 COM DLL을 설치하여 사용할 수 있는데, 이 결과로 시스템에는 특정 DLL에 대한 다양한 버전의 DLL 파일들이 존재하게 된다. (마이크로소프트에서는 이를 '병렬식 어셈블리(Side-by-side Assemblies)'[4](http://msdn.microsoft.com/library/default.asp?url=/library/en-us/sbscs/setup/side_by_side_assemblies.asp) 라 부른다.) 레지스트레이션-프리 COM 을 사용하면 대부분 DLL 지옥을 피할 수 있다. 다만 최소 윈도 XP 또는 그 이상의 상위 버전의 OS가 필요하며, EXE COM 서버 및 시스템 전역적인 컴포넌트들 즉 MDAC, MSXML, [다이렉트X](https://ko.wikipedia.org/wiki/다이렉트엑스 "wikilink") 및 [인터넷 익스플로러](../Page/인터넷_익스플로러.md "wikilink") 등에는 사용할 수 없다.

<!-- end list -->

  - DLL 파일들의 의존성을 추적 및 관리할 수 있는 [패키지 관리 시스템을](https://ko.wikipedia.org/wiki/패키지_관리_시스템 "wikilink") 운영 체제에 포함하여, 사용자에게 패키지 관리 시스템의 사용을 장려하고, 수동으로 DLL 파일을 설치하지 말 것을 권고한다.

<!-- end list -->

  - 라이브러리 배포에 대한 사항을 중앙에서 집중 관리할 수 있는 시스템을 마련하고, 라이브러리를 변경하려면 이 시스템을 통하도록 한다; 이를 통해, 여러 버전의 소프트웨어에 대해서도 서로 호환성이 유지되도록 할 수 있다. 예를 들어 만약 특정 하위 버전의 소프트웨어가 현재의 라이브러리와 서로 호환되지 않는다면, 그 소프트웨어를 위해 시스템은 호환 가능한 인터페이스를 제공하거나, 적절히 격리된 형태로 해당 소프트웨어가 요구하는 버전의 패키지를 공급하도록 할 수 있다.

<!-- end list -->

  - 만약 소프트웨어 개발에서 라이브러리의 수정이 불가피하다면, 이 라이브러리의 DLL을 프로그램의 개인적인 공간 즉 프로그램 디렉터리 같은 곳에 두거나, 라이브러리를 프로그램에 정적으로 링크하여 [컴파일하도록](../Page/컴파일러.md "wikilink") 한다.

<!-- end list -->

  - 적절한 소프트웨어 디자인 방법을 따른다. DLL은 시스템의 구성 요소들을 모듈화하여 별개의 라이브러리로 만드는 훌륭한 방법이다; 그러나 모든 경우에서 항상 사용해야 하는 것은 아니다. 예를 들어 만약 프로그램이 다른 어느 곳에서도 사용되지 않는 라이브러리를 필요로 한다면, 이를 정적으로 링크하여 용량 증가 등의 특별한 불이익 없이 실행 속도를 향상시킬 수 있다.

## .NET에 대한 동기 부여로서 DLL 지옥

[2002년](../Page/2002년.md "wikilink") [2월](../Page/2월.md "wikilink"), 마이크로소프트는 대중에 닷넷 프레임워크를 공개하였다. 이 프레임워크는 [어셈블리](http://msdn.microsoft.com/library/default.asp?url=/library/en-us/dndotnet/html/dplywithnet.asp)(assemblies)라 불리는 새로운 버전의 패키지 배포 시스템을 포함하고 있으며, 공용 라이브러리 런타임(common library runtime)에 대한 지원을 제공한다. 공용 라이브러리 런타임에서 많은 DLL 코드가 베이스 파운데이션 클래스(base foundation class)로 이동되었다.

## 같이 보기

  - [의존성 지옥](https://ko.wikipedia.org/wiki/의존성_지옥 "wikilink")([:en:Dependency hell](https://ko.wikipedia.org/wiki/:en:Dependency_hell "wikilink"))
  - [자바 클래스로더](../Page/자바_클래스로더.md "wikilink")([:en:Java classloader](https://ko.wikipedia.org/wiki/:en:Java_classloader "wikilink"), 일명: JAR 지옥)
  - [범용 운영체제](https://ko.wikipedia.org/wiki/범용_운영체제 "wikilink")
  - [전용 운영체제](https://ko.wikipedia.org/wiki/전용_운영체제 "wikilink")

## 외부 링크

  - [The End of DLL Hell](http://msdn.microsoft.com/library/default.asp?url=/library/en-us/dnsetup/html/dlldanger1.asp) MSDN 문서

  - [.NET 프레임워크를 사용하여 배포를 단순화하고 DLL 지옥 해결하기](http://msdn.microsoft.com/library/default.asp?url=/library/en-us/dndotnet/html/dplywithnet.asp) MSDN 문서

  - [DLL 지옥 피하기: .NET 프레임워크에서의 애플리케이션 메타데이터 소개](https://web.archive.org/web/20060831042832/http://msdn.microsoft.com/msdnmag/issues/1000/metadata/default.aspx) Matt Pietrek 씀

  - [Dll 무료 다운로드](http://kr.dll-download-system.com)

[분류:안티패턴](https://ko.wikipedia.org/wiki/분류:안티패턴 "wikilink") [분류:정보기술 용어](https://ko.wikipedia.org/wiki/분류:정보기술_용어 "wikilink")