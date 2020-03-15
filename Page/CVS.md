> This article is converted from Wikipedia: [CVS](https://ko.wikipedia.org/wiki/CVS).


**CVS**(, 동시 버전 시스템)는 동시 [버전 관리](../Page/버전_관리.md "wikilink") 시스템()으로도 알려져 있으며, [버전 관리 시스템을](https://ko.wikipedia.org/wiki/리비전_관리 "wikilink") 구현한다. 보통 소프트웨어 프로젝트를 진행할 때, 파일로 이뤄진 모든 작업과 모든 변화를 추적하고, 여러 개발자(지역적으로 떨어진)가 협력하여 작업할 수 있게 한다. CVS는 [GNU 일반 공중](../Page/GNU_일반_공중_사용_허가서.md "wikilink") [사용 허가서](https://ko.wikipedia.org/wiki/라이선스 "wikilink") 하에서 배포된다. CVS는 오픈 소스 프로젝트에서 널리 사용되었다. 현재는 CVS가 한계를 맞아, CVS를 대체하는 [서브버전](../Page/서브버전.md "wikilink")이 개발되었다.

## 특징

CVS는 클라이언트-서버 구조로 이뤄진다. 서버는 프로젝트의 현재 버전과 변화를 저장하고, 클라이언트는 서버에 접속하여 프로젝트의 완전한 복사본을 얻을 수 있다. 복사본으로 작업한 뒤에, 바뀐 내용을 체크인한다. 보통 클라이언트와 서버는 랜이나 인터넷을 통해 접속되지만, CVS를 혼자 개발하는 사람이 쓴다면, 클라이언트와 서버를 하나의 컴퓨터에서 실행시킬 수도 있다. 서버 소프트웨어는 일반적으로 유닉스(윈도 NT에서 실행되는 CVS서버도 있다)에서, CVS 클라이언트는 대부분의 범용적인 운영체제 플랫폼에서 작동된다.

여러 클라이언트가 프로젝트의 복사본을 동시에 작업할 수 있다. 달라진 내용을 체크인할 때, 서버는 그것들을 합친다. 실패할 경우, 예를 들어, 두 클라이언트가 동일한 파일의 같은 줄을 바꾼 경우에, 서버는 두 번째 체크인 작업을 무시하고, 충돌이 일어났음을 클라이언트에 알린다. 충돌을 일으킨 사용자는 그 문제를 해결해야 한다. 체크인 작업이 성공하면, 모든 파일의 버전 번호는 자동적으로 증가되며, CVS 서버는 사용자가 작성한 설명을 추가한다. 날짜와 작성자 이름은 로그 파일에 있다.

클라이언트는 다른 버전의 파일들을 비교하고, 모든 변경 내역을 요청하고, 프로젝트에서 원하는 날짜나 버전에 대한 스냅샷을 얻을 수 있다. 많은 오픈 소스 프로젝트는 익명 계정으로 읽기 접근을 허용한다. 이 특징은 [OpenBSD](../Page/OpenBSD.md "wikilink")가 선도했다. 이것은 클라이언트가 암호 없이, 공개된 암호(예를 들어, "anoncvs")로 체크아웃하거나 버전을 비교할 수 있음을 뜻한다. 오직 변경을 체크인할 때에만 개인 계정/암호가 필요하다.

클라이언트는 서버에 보관된 최신 버전의 최근 변경 내역만을 복사하기 위해, "업데이트(update)" 명령을 이용할 수 있다. 이로써 프로젝트 전체를 여러 번 내려 받을 필요가 없어진다.

CVS는 프로젝트의 서로 다른 '가지'를 관리할 수 있다. 예를 들어, 소프트웨어의 배포판이 하나의 가지가 되어, [버그를](../Page/소프트웨어_버그.md "wikilink") 수정한다. 그와 동시에 진행된, 많은 변화와 새로운 특징이 추가된 다른 버전은 분리된 가지가 된다.

CVS는 같은 파일의 다른 버전을 효율적으로 저장하기 위해 [델타 압축을](https://ko.wikipedia.org/wiki/델타_압축 "wikilink") 사용한다. 이 방법은 많은 줄을 가진 파일(텍스트 파일 같은)에 적합하다. 극단적인 경우 각 버전에 대한 개별적인 복사본은 델타 압축보다 효율적이지 못하다.

## CVS 용어

CVS로 관리되는 하나의 프로젝트(관련된 파일의 집합)를 [모듈](https://ko.wikipedia.org/wiki/모듈 "wikilink")이라 부른다. CVS 서버는 보관소에 모듈을 저장한다. 모듈의 복사본을 얻는 것은 체크 아웃(checking-out)이라 한다. 체크 아웃된 파일은 작업 중인 복사본으로 관리된다. 이 복사본을 바꾸려면 [커밋](https://ko.wikipedia.org/wiki/커밋 "wikilink")(commit)하여 보관소에 넣어야 한다. 업데이트(update)는 작업 중인 복사본이 있는 보관소에서 최근에 변경된 사항을 얻는다.

## 역사 및 상황

CVS는 아직도 쓰이는, 리비전 관리 시스템(Revision Control System)이라 불린 초기 [버전 관리 시스템에서](https://ko.wikipedia.org/wiki/리비전_관리 "wikilink") 태어났다. 각각의 파일을 관리하지만, 프로젝트 전체는 아니었다. 딕 그룬(Dick Grune)은 자신의 사이트에 CVS에 대해 짧은 역사를 기술했다. 인용하면 다음과 같다.

코드는 1986년 6월 23에 mod.sources에 배포되었다. 지금도 [구글 그룹스에서](../Page/구글_그룹스.md "wikilink") \[<http://groups.google.com/groups>?:mod.sources.\*\&hl=en\&lr=lang_en\&ie=UTF-8\&c2coff=1\&safe=off\&selm=122@mirror.UUCP\&rnum=2 유즈넷 글 원본\]을 볼 수 있다.

코드는 1989년 4월에 브라이언 베르라이너(Brian Berliner)가 시작하여 CVS라는 동일한 버전으로 탈바꿈했다. 제프 포크(Jeff Polk)와 많은 기여들이 그 뒤에 함께 했다. 브라이언 베르라이너는 CVS 프로그램을 개선한 내용을 소개한 글을 썼는데, 이 프로그램이 어떻게 확장되었고, SunOS 커널에서 작업하는 서드 파티 개발자인 프리즈마에 내부적으로 쓰인 내용을 담았으며, 그리고 GPL을 표방하는 커뮤니티를 위해 배포되었다.

현재, 지원자 그룹이 CVS 코드를 관리하고 있다. 주목할 점은 CVS의 마이크로소프트 윈도 판 개발이 CVSNT라는 이름의 프로젝트로 분리되었고 시스템의 특징을 살리는 데 더 적극적이다. 심지어 CVSNT라는 이름으로 유닉스 플랫폼을 지원하려고 한다.

역사적으로 CVS와 GNU 프로젝트의 관계는 좀 모호하다고 할 수 있다. GNU 웹사이트는 프로그램을 배포하고, 어떤 페이지에는 "GNU 패키지"라는 이름이 붙고, 다른 것은 "다른 GPL 라이선스 프로젝트"라 한다. 이것은 최근까지 엄밀했다. CVS 개발이 cvshome.org에서 CVS가 공식적으로 GNU가 아닌 savannah.nongnu.org로 옮기기 전까지 말이다. FTP 사이트에서 이 프로그램은 전통적으로 /non-gnu/ [디렉터리](https://ko.wikipedia.org/wiki/디렉터리 "wikilink")에 저장되어 있다.

## 한계

  - CVS 저장소의 파일들은 이름을 바꿀 수 없다. 제거하고 나서 다시 추가해야 한다.
  - CVS 프로토콜은 디렉터리의 이동이나 이름 변경을 허용하지 않는다. 서브 디렉터리의 파일은 모두 지우고 다시 추가해야 한다.
  - [아스키](https://ko.wikipedia.org/wiki/ASCII "wikilink") 코드로 된 [파일 이름이](../Page/파일_이름.md "wikilink") 아닌 [유니코드](../Page/유니코드.md "wikilink") 파일을 제한적으로 지원한다.

CVS를 만들었던 핵심 개발자들 몇몇은 이제 2004년 초부터 배포한 [Subversion](https://ko.wikipedia.org/wiki/Subversion "wikilink")(SVN)을 맡고 있다. CVS를 대체하기 위해 CVS의 한계를 일부 수정한 것이다. 또한 [CVS용 WANdisco](https://web.archive.org/web/20060302144122/http://www.wandisco.com/php/product_detail.php?lname=cvs) 같은 도구는 커밋의 원자성, 역할 기반의 접근 제어, 멀티 사이트 등이 없는 CVS의 여러 단점이 보완되었다.

## 외부 링크

  - [CVS - Concurrent Versions System](http://www.nongnu.org/cvs/) CVS 공식 홈페이지
  - [TortoiseCVS](http://tortoisecvs.sourceforge.net/) 윈도용 CVS 클라이언트 도구

[분류:소프트웨어 공학](https://ko.wikipedia.org/wiki/분류:소프트웨어_공학 "wikilink") [분류:자유 버전 관리 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_버전_관리_소프트웨어 "wikilink") [분류:1990년 소프트웨어](https://ko.wikipedia.org/wiki/분류:1990년_소프트웨어 "wikilink") [분류:C로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C로_작성된_자유_소프트웨어 "wikilink") [분류:GPL 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:GPL_라이선스_소프트웨어 "wikilink")