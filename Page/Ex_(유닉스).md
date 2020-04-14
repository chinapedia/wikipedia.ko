> This article is converted from Wikipedia: [Ex \(유닉스\)](https://ko.wikipedia.org/wiki/Ex_\(유닉스\)).


EXtended의 축약어인 **ex**는 [유닉스](../Page/유닉스.md "wikilink") 시스템들을 위한 [라인 에디터이다](https://ko.wikipedia.org/wiki/라인_에디터 "wikilink").

최초의 `ex`는 표준 유닉스 에디터 [ed의](../Page/Ed_\(문서_편집기\).md "wikilink") 진화된 버전으로 [BSD](../Page/BSD.md "wikilink")에 포함되어 있었다. ex는 ed와 비슷하지만 어떤 스위치들과 옵션들이 변형되어 좀 더 [사용성](../Page/사용성.md "wikilink")이 큰 것이 예외다.

ex는 궁극적으로는 스크린 지향적 비주얼 인터페이스에 주어지므로(명령 줄 지향적인 작동에 더해지면서) 그 때문에 [vi](https://ko.wikipedia.org/wiki/vi "wikilink") 텍스트 에디터가 된다. 최근 들어서 ex는 vi 프로그램의 성질로서 실행된다; vi의 대부분 변수들은 여전히 명령어 `ex` 사용하면서 실행되는 "ex [모드](https://ko.wikipedia.org/wiki/모드 "wikilink")"를 갖고 있거나 **:** (컬럼) 문자를 대표하므로 하나의 명령어에 대한 vi 안으로부터의 "ex"를 갖고 있다. ex와 vi 기능성 사이에 겹치는 부분이 있다고 할지라도, 어떠한 것들은 ex 명령어에 의해서만 시행될 수 있고 vi를 사용할 경우 유용한 것들도 있다.

검색하고 대체하는 것과 관련있는, 핵심적인 ex 명령어들은 vi에 필수적이다. 예를 들어, vi `:%s/XXX/YYY/g` 로부터 나온 ex 명령어는 모든 XXX를 그 대신에 YYY로 대체한다. `%`는 파일 안의 모든 문자열을 의미한다. 'g' 방법들은 모든 문자열에 모든 예시를 대체한다(만약 이것이 지정되어 있지 않을 경우, 각각의 문자열에 첫 번째 예시만이 대체된다.)

ex는 [HP-UX](../Page/HP-UX.md "wikilink") 환경에서 [동의어](https://ko.wikipedia.org/wiki/동의어 "wikilink") **e**를 갖는다.

## 스위치

ex는 다음의 스위치들을 인식한다.

  - \- (obsolete) 사용자 쌍방의 피드백
  - \-s ([XPG4](https://ko.wikipedia.org/wiki/XPG4 "wikilink") only) 사용자 쌍방의 피드백을 억제한다
  - \-l 은 [lisp editor](https://ko.wikipedia.org/wiki/lisp_editor "wikilink") 옵션을 설정한다
  - \-r 시스템 충돌 이후 지정된 파일들을 회복시킨다
  - \-R 랜덤하게 설정한다
  - \-t tag 지정된 태그를 갖고 있는 파일을 수정한다.
  - \-v 시각적 모드를 시행한다 (vi)
  - \-w 윈도 사이즈 *n*을 설정한다
  - \-x 암호화 모드를 설정한다
  - \-C 암호화 옵션
  - file 수정될 파일을 지정한다.

[분류:유닉스 문서 편집기](https://ko.wikipedia.org/wiki/분류:유닉스_문서_편집기 "wikilink") [분류:표준 유닉스 프로그램](https://ko.wikipedia.org/wiki/분류:표준_유닉스_프로그램 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink")