> This article is converted from Wikipedia: [스타일XP](https://ko.wikipedia.org/wiki/스타일XP).


**스타일XP**(StyleXP)는 [윈도 XP의](https://ko.wikipedia.org/wiki/윈도_XP "wikilink") 그래픽 사용자 인터페이스를 수정하도록 고안된 [컴퓨터 프로그램이다](../Page/컴퓨터_프로그램.md "wikilink"). 3.19 버전부터 테마, 탐색기 표시줄, 배경, 로그온 화면, 아이콘, 시동 화면, 투명도, 커서, 화면 보호기를 수정할 수 있다.

## 역사

TGTSoft가 만든 스타일XP는 [스타독](../Page/스타독.md "wikilink")의 [윈도블라인즈](https://ko.wikipedia.org/wiki/윈도블라인즈 "wikilink")와 [오브젝트 데스크톱과](https://ko.wikipedia.org/wiki/오브젝트_데스크톱 "wikilink") 같은 스킨 프로그램의 대안이다.

## 동작 방식

스타일XP는 uxtheme.dll이라는 [DLL](../Page/동적_링크_라이브러리.md "wikilink") 파일을 패치함으로써 동작한다. Uxtheme.dll은 기본적으로 사용자가 [마이크로소프트](../Page/마이크로소프트.md "wikilink")에 의해 [디지털 서명을](../Page/디지털_서명.md "wikilink") 받지 않는 테마를 설치하지 못하도록 막는다. 이러한 DLL을 패치함으로써 스타일XP는 서명을 받지 않은 테마를 설치할 수 있다. 초기 버전의 프로그램들은 디스크에 있는 uxtheme.dll 파일을 패치하였지만 새로운 버전에서는 [메모리에서](../Page/기억_장치.md "wikilink") 이러한 작업을 수행한다.

## 인기

이 프로그램의 지난 여러 해 동안 인기를 끌었다. 일부 사이트들은 스킨을 무료로 공개하였다. 이러한 스킨들은 패치된 uxtheme DLL 파일이 공개된 뒤에 인기를 끌게 되었다.

## 윈도 비스타 호환성

윈도 비스타로 업그레이드된 컴퓨터에서 스타일XP를 제거하면 시스템 아이콘이 대부분 손상되는 문제를 일으킬 수 있다. 다음의 레지스트리 키를 지움으로써 이를 해결할 수 있다.

`HKEY_LOCAL_MACHINE\Software\Microsoft\Windows\Current Version\Explorer\Shell Icons`

윈도 비스타를 새로 설치한 경우, "Shell Icons" 폴더는 존재하지 않는다.

## 외부 링크

  - [스타일XP 공식 홈페이지](https://web.archive.org/web/20070405191802/http://www.tgtsoft.com/prod_sxp.php)

[분류:윈도우 전용 소프트웨어](https://ko.wikipedia.org/wiki/분류:윈도우_전용_소프트웨어 "wikilink") [분류:그래픽 사용자 인터페이스](https://ko.wikipedia.org/wiki/분류:그래픽_사용자_인터페이스 "wikilink") [분류:윈도우용 유틸리티](https://ko.wikipedia.org/wiki/분류:윈도우용_유틸리티 "wikilink")