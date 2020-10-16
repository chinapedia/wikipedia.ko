> This article is converted from Wikipedia: [Exec Shield](https://ko.wikipedia.org/wiki/Exec_Shield).


**Exec Shield**는 2002년 리눅스 시스템에 대한 웜 또는 다른 자동화된 원격 공격들을 줄이기 위한 목표로 레드햇 사에서 시작된 프로젝트이다. 이 프로젝트의 첫 번째 결과는 하드웨어에서 네이티브 NX 구현이 없는 [x86](https://ko.wikipedia.org/wiki/x86 "wikilink") [CPU](https://ko.wikipedia.org/wiki/CPU "wikilink")에서 [NX 비트를](../Page/NX_비트.md "wikilink") 에뮬레이팅하는 [리눅스 커널의](../Page/리눅스_커널.md "wikilink") [보안](../Page/컴퓨터_보안.md "wikilink") 패치였다. Exec Shield 프로젝트가 여러 다른 구성 요소들을 가지지만 어떤 사람들은 이 첫 번째 패치를 Exec Shield로 부르기도 한다.

첫 번째 Exec Shield 패치는 데이터 메모리를 실행 불가능하게 그리고 프로그램 메모리를 쓰기 불가능하게 플래그하려는 시도였다. 이것은 [버퍼 오버플로](https://ko.wikipedia.org/wiki/버퍼_오버플로 "wikilink") 같이 데이터를 겹쳐쓰고 이러한 구조에 코드를 삽입하는 것을 기반으로하는 많은 [취약점 공격을](../Page/취약점_공격.md "wikilink") 제한하였다. Exec Shield는 또한 mmap()과 힙 베이스를 위한 몇몇 주소 공간 배치 난수화를 제공한다.

패치는 추가적으로 셸코드를 삽입하고 실행하는 난이도를 증가시켜 대부분의 익스플로잇을 막았다. exec-shield를 완전히 활용하기 위한 애플리케이션의 재컴파일은 필요하지 않지만, 몇몇 애플리케이션들([모노](../Page/모노_\(소프트웨어\).md "wikilink"), [와인](../Page/와인_\(소프트웨어\).md "wikilink"), XEmacs, [엠플레이어](../Page/엠플레이어.md "wikilink"))은 완전히 호환되지는 않는다.

Exec Shield로부터 나오는 다른 특징들로 일명 [위치 독립 코드](https://ko.wikipedia.org/wiki/위치_독립_코드 "wikilink")(PIE), 리눅스 커널을 위한 주소 공간 난수화 패치, 힙과 포캣 스트링 익스플로잇을 거의 불가능하게 하는 여러 glibc 내부 보안 검사, GCC Fortify 소스 그리고 GCC 스택 프로텍터 등이 있다.

## 구현

Exec Shield는 코드 세그먼트 제한을 활용하며 모든 x86 CPU들에서 동작한다. Exec Shield가 동작하는 방식 때문에 이것은 매우 가볍다; 그러나 임의적인 [가상 메모리](../Page/가상_메모리.md "wikilink") 배치를 완전히 보호할 수는 없다. 더 높은 메모리를 실행하기 위해 mprotect()를 호출하는 방식 처럼 만약 CS 제한이 되면 그 제한 아래에 대해서는 보호되지 못한다. 다행히 대부분의 애플리케이션들은 이 지점에서 상당히 정상적이다; 중요한 부분인 스택은 매핑된 라이브러리의 적어도 윗 부분이 날아가서 애플리케이션에 의해 명시적으로 호출되는 것을 제외하고는 실행 불가능하게 된다.

2004년 8월부로 Exec Shield 프로젝트에서는 어느 아키텍처에서도 mprotect()를 제한함으로써 메모리 보호를 강화하지 않는다; 비록 메모리가 초기에 실행가능하지 않을 수 있지만, 추후에 실행 가능해지며 커널은 애플리케이션이 메모리 페이지를 쓰기 가능하고 실행 가능하게 마크하게 한다. 그러나 [SELinux](https://ko.wikipedia.org/wiki/SELinux "wikilink") 프로젝트와 함께 [페도라 코어](https://ko.wikipedia.org/wiki/페도라_코어 "wikilink") 배포판의 표준 정책은 이 행위를 금지한다.

## 같이 보기

  - [NX 비트](../Page/NX_비트.md "wikilink")
  - [PaX](https://ko.wikipedia.org/wiki/PaX "wikilink")
  - [스택가드](https://ko.wikipedia.org/wiki/스택가드 "wikilink")
  - [W^X](https://ko.wikipedia.org/wiki/W^X "wikilink")

## 외부 링크

  - [Ingo Molnar's Exec Shield patch web page](http://people.redhat.com/mingo/exec-shield/), includes documentation in the file [ANNOUNCE-exec-shield](http://people.redhat.com/mingo/exec-shield/ANNOUNCE-exec-shield)
  - [Newsforge Feature Article](https://web.archive.org/web/20050207064757/http://www.newsforge.com/os/03/05/02/1914223.shtml?tid=23)
  - [Red Hat Magazine Feature/Project Article](https://web.archive.org/web/20070208094418/http://www.redhat.com/magazine/009jul05/features/execshield/)
  - [Negative security issues with ExecShield](http://seclists.org/dailydave/2007/q2/107)

[분류:리눅스](https://ko.wikipedia.org/wiki/분류:리눅스 "wikilink") [분류:리눅스 보안 소프트웨어](https://ko.wikipedia.org/wiki/분류:리눅스_보안_소프트웨어 "wikilink") [분류:운영 체제 보안](https://ko.wikipedia.org/wiki/분류:운영_체제_보안 "wikilink")