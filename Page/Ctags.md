> This article is converted from Wikipedia: [Ctags](https://ko.wikipedia.org/wiki/Ctags).


**Ctags**는 다양한 [프로그래밍 언어로](https://ko.wikipedia.org/wiki/프로그래밍_언어 "wikilink") 된 소스와 헤더 파일에서 보이는 이름의 인덱스(또는 태그) 파일을 생성하는 [프로그래밍 도구이다](https://ko.wikipedia.org/wiki/프로그래밍_도구 "wikilink"). 언어에 따라 [함수](https://ko.wikipedia.org/wiki/함수 "wikilink"), [변수](https://ko.wikipedia.org/wiki/변수 "wikilink"), [클래스](https://ko.wikipedia.org/wiki/클래스 "wikilink") 멤버, [매크로](https://ko.wikipedia.org/wiki/매크로_\(컴퓨터_과학\) "wikilink") 등을 색인할 수 있다. 이 태그들은 정의들을 빠르고 쉽게 [문서 편집기나](https://ko.wikipedia.org/wiki/문서_편집기 "wikilink") 다른 유틸리티에 의해 위치시킬 수 있게 한다. 그 외에, [상호 참조](https://ko.wikipedia.org/wiki/상호_참조 "wikilink") 파일을 생성하는 출력 모드도 있어서 언어 파일 집합에서 보이는 다양한 이름에 대한 정보를 [사람이 읽을 수 있는](https://ko.wikipedia.org/wiki/사람이_읽을_수_있는_매체 "wikilink") 형태로 나열할 수 있다.

오리지널 **Ctags**는 [BSD](https://ko.wikipedia.org/wiki/BSD "wikilink")에 도입되었으며 [켄 아놀드가](https://ko.wikipedia.org/wiki/켄_아놀드 "wikilink") 작성하였고, 짐 클레크너가 [포트란](https://ko.wikipedia.org/wiki/포트란 "wikilink") 지원을, [빌 조이가](https://ko.wikipedia.org/wiki/빌_조이 "wikilink") [파스칼](https://ko.wikipedia.org/wiki/파스칼_\(프로그래밍_언어\) "wikilink") 지원을 맡았다.

## ctags를 지원하는 편집기

태그 인덱스 파일들은 다음을 포함하여 수많은 [소스 코드 편집기에](../Page/소스_코드_편집기.md "wikilink") 의해 지원된다:

  - [아톰](../Page/아톰_\(문서_편집기\).md "wikilink")
  - [BBEdit 8+](https://ko.wikipedia.org/wiki/BBEdit "wikilink")
  - [코드라이트](https://ko.wikipedia.org/wiki/코드라이트 "wikilink") (코드 완성을 위한 코드 인덱서로서)
  - [Cloud9 IDE](https://ko.wikipedia.org/wiki/Cloud9_IDE "wikilink") (내부적으로 사용하지만 노출하지는 않음)
  - [에디트플러스](https://ko.wikipedia.org/wiki/에디트플러스 "wikilink")
  - [이맥스](https://ko.wikipedia.org/wiki/이맥스 "wikilink"), [XEmacs](https://ko.wikipedia.org/wiki/XEmacs "wikilink")
  - [엠에디터 프로페셔널](https://ko.wikipedia.org/wiki/엠에디터 "wikilink")
  - [기니](../Page/기니_\(소프트웨어\).md "wikilink")
  - [Gedit](https://ko.wikipedia.org/wiki/Gedit "wikilink") (gedit-symbol-browser-plugin을 통해. \[[https://web.archive.org/web/20080117145432/http://www.micahcarrick.com/11-14-2007/gedit-symbol-browser-plugin.html\]에서](https://web.archive.org/web/20080117145432/http://www.micahcarrick.com/11-14-2007/gedit-symbol-browser-plugin.html%5D에서) 확인 가능.)
  - 그놈 빌더
  - [JED](https://ko.wikipedia.org/wiki/JED_\(문서_편집기\) "wikilink")
  - [JEdit](https://ko.wikipedia.org/wiki/JEdit "wikilink") (플러그인 CodeBrowser, Tags, ClassBrowser, CtagsSideKick, Jump를 통해)
  - [JOE](https://ko.wikipedia.org/wiki/Joe's_Own_Editor "wikilink")
  - [KDevelop](../Page/KDevelop.md "wikilink")
  - [Kate](https://ko.wikipedia.org/wiki/Kate "wikilink")
  - [mcedit](https://ko.wikipedia.org/wiki/mcedit "wikilink") (미드나이트 커맨더 내장 편집기) [1](http://www.midnight-commander.org)
  - [NEdit](https://ko.wikipedia.org/wiki/NEdit "wikilink")
  - [노트패드++](https://ko.wikipedia.org/wiki/노트패드++ "wikilink") (OpenCTags 플러그인을 통해)
  - [Programmer's Notepad](https://ko.wikipedia.org/wiki/Programmer's_Notepad "wikilink")
  - [QDevelop](https://ko.wikipedia.org/wiki/QDevelop "wikilink")
  - 스크래치(Scratch)
  - [TSE (매크로를 통해)](https://ko.wikipedia.org/wiki/The_SemWare_Editor "wikilink")
  - [서브라임 텍스트](../Page/서브라임_텍스트.md "wikilink") (플러그인을 통해. \[[https://github.com/SublimeText/CTags\]에서](https://github.com/SublimeText/CTags%5D에서) 확인 가능.)
  - [텍스트메이트](../Page/텍스트메이트.md "wikilink") (코드브라우저-플러그인을 통해)
  - [UltraEdit](https://ko.wikipedia.org/wiki/UltraEdit "wikilink")
  - [TextPad](https://ko.wikipedia.org/wiki/TextPad "wikilink")
  - [VEDIT](https://ko.wikipedia.org/wiki/VEDIT "wikilink")
  - [Vi](https://ko.wikipedia.org/wiki/Vi "wikilink") (및 [Elvis](https://ko.wikipedia.org/wiki/Elvis "wikilink"), [Nvi](https://ko.wikipedia.org/wiki/Nvi "wikilink"), [Vim](https://ko.wikipedia.org/wiki/Vim "wikilink"), [vile](https://ko.wikipedia.org/wiki/vile "wikilink") 등의 파생 편집기를 통해)
  - [Xedit (X11)](https://ko.wikipedia.org/wiki/Xedit_\(X11\) "wikilink")

## 같이 보기

  - [GNU GLOBAL](https://ko.wikipedia.org/wiki/GNU_GLOBAL "wikilink")

## 외부 링크

  -
  - [Universal Ctags on Github](https://ctags.io)

  - [Exuberant ctags homepage](http://ctags.sourceforge.net)

  - [Ctags on VMS](http://polarhome.com/ctags/?lang=en)

  - [source code for Emacs vtags.el module](http://cvs.savannah.gnu.org/viewvc/vtags/vtags/vtags.el?view=markup)

[분류:유닉스 프로그래밍 도구](https://ko.wikipedia.org/wiki/분류:유닉스_프로그래밍_도구 "wikilink") [분류:표준 유닉스 프로그램](https://ko.wikipedia.org/wiki/분류:표준_유닉스_프로그램 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink")