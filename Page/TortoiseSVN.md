> This article is converted from Wikipedia: [TortoiseSVN](https://ko.wikipedia.org/wiki/TortoiseSVN).


**TortoiseSVN**은 [마이크로소프트 윈도용](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") [서브버전](../Page/서브버전.md "wikilink") 클라이언트 프로그램이다. 설치하면 윈도 탐색기 [콘텍스트 메뉴에](https://ko.wikipedia.org/wiki/콘텍스트_메뉴 "wikilink") 등록되어 편리하게 이용할 수 있다. 또한 Merge, diff 툴을 기본으로 제공한다.\[1\]\[2\]

## 프로그램 용어

### Repository, Import, Add

  - Repository: Subversion이 version control 관련 data를 저장하는 곳이다. 구성하는 방법은 다양하다: 한 repository에 여러 project를 담을 수도 있고, 한 repository에 한 project만 담는 경우도 있다. 두 방법 모두 장단점이 있다. 한 project당 하나씩의 repository를 사용하는 것이 일반적으로 더 바람직하다.
  - 새 repository 만들기

Command line 의 경우 다음 명령어를 사용한다.

``` bash
    $ svnadmin create [대상 path 이름]
```

  - Subversion에 새 프로젝트를 import하는 법?

<!-- end list -->

1.  Project관련 file들이 저장된 folder안에서 불필요한 file들을 제거한다. 보통 임시 file, compiler나 linker가 생성하는 file들을 제거한다.
2.  svn_repository folder아래 새 folder에 그 프로젝트를 담을 repository를 만든다.
3.  Repository 안에 3개의 folder를 만든다: trunk, branch, tags.
4.  trunk로 project를 import한다. Repository 안의 잘못된 folder level로 import 하는 일이 빈번하다.
5.  작업 공간으로 다시 project를 Check-out 한다.

<!-- end list -->

  - Subversion에 새 프로젝트를 Add하는 법?

<!-- end list -->

1.  Repository browser로 repository 안에 folder를 직접 생성한다.
2.  만들어진 folder를 import하고자하는 file을 담고 있는 folder(check in 대상 project의 file들이 저장된 최상위 folder)로 check out 한다. 예를 들어 “\~/source/file.c”, “\~/source/subfolder/subfolderfile.c”를 add하고 싶다면 “\~/source/” folder로 check out 한다. Warning이 뜰 것이다. Top level folder는 version 관리 되고 있지만 내용은 version 관리되지 않고 있지 않은 상태가 될 것이다.
3.  TortoiseSVN→Add... 명령으로 version관리하고 싶은 file을 추가한다. File이나 subfolder icon이 물음표 상태로 Add.. 명령이 뜨지 않으면 folder window 배경에 오른쪽 mouse click.
4.  Top level folder를 commit한다.

<!-- end list -->

  - Repository 안의 잘못된 folder level로 import되었을 경우 바로잡기 어렵다. Move를 허용하나, move 이전과 이후의 file은 별개의 객체로 인식되는 것으로 보인다.
  - Subversion에 새 프로젝트를 import할 때 원하는 file만 import하는 것은 사실상 어렵다. 새 프로젝트를 Add하는 법 참조.
  - Subversion에 여러 Repository를 만들려면 Repository별로 하나씩 folder를 만들어 주는 것이 바람직하다.

### Check out, Update, Commit, Conflict, Resolve, Keyword

  - Check out: 저장소에서 project를 작업공간에 인출하는 것. Download와 유사하다.
  - Check out의 방식

예를 들어 저장소 안에서 check-out할 file들의 위치가 다음과 같다고 하자.

``` bash
    file:///c:/svn_repository/Project01/trunk/
```

여기서 Project01이 project 이름이고 trunk는 주류 file이라는 의미이다.

1.  작업할 folder의 상위 folder를 만든다. 우리가 희망하는 작업 공간의 위치가 다음과 같다고 하자.
      -

        ``` bash
         My Documents\Development\Project01\
        ```

        그러면 “My Documents” 아래 “Development”라는 이름의 folder를 만들면 된다.
2.  Checkout 대화상자를 연다. “Development” folder를 열고 folder 배경에서 오른쪽 Mouse click하여 SVN Checkout... menu를 선택하면 Checkout 대화상자가 열린다.
3.  “URL of repository”난의 \[...\] button을 눌러 “file:///c:/svn_repository/Project01/trunk”를 선택한다.
4.  “Checkout directory”난에 “My Documents\\Development” folder를 선택한다.
5.  Checkout Depth는 Fully recursive를 선택하자.
6.  Revision은 HEAD로 하면 최신 file이 들어온다. 만일 다른 revision을 선택하고 싶을 때는 \[Show log\] button을 눌러 확인하자.
7.  \[OK\] button을 누르면 저장소의 내용이 작업 공간으로 copy된다. 처음에는 초록색 체크 표시가 되어 있을 것이다. 이는 이 file 이 저장소의 내용과 일치한다는 의미다.

<!-- end list -->

  - Commit: 작업공간에서 수정된 project를 저장소에 반영하는 것. Upload와 유사하다. Commit하기 전에 작업 공간의 file을 충분히 시험하여야 한다.
  - 수정된 file 하나를 Commit: Check out 되어 version 관리되고 있는 file이 저장소의 내용과 일치할 때는 초록색이다. 이 file을 수정하고 나면 붉은 느낌표가 나타난다. 저장소에 변경한 내용을 반영하려면 Commit해야 한다.

<!-- end list -->

1.  File의 icon에 오른쪽 Mouse Click하면 “SVN Commit...” 명령이 나타난다.
2.  선택하면 Commit 대화 상자가 나타난다. Message난과 Changes made난이 있다.
3.  Message 난에 Commit message 를 상세히 입력한다. Changes made 난에서 수정 부분을 확인할 수 있는 “Compare with base” 명령을 선택할 수 있다.
4.  \[OK\] button을 누르면 변경 내용이 repository에 반영 된다.
5.  다른 사용자가 같은 project를 check-out하거나 “Update” 명령을 사용하면 변경 내용이 반영된다.

<!-- end list -->

  - 한 project안에서 여러개의 file을 수정한 후 한번에 Commit하는 법?

<!-- end list -->

1.  수정된 file을 담고 있는 folder icon을 확인한다. 붉은 느낌표가 떠 있으면 icon에 오른쪽 Mouse Click하여 “SVN Commit...” 명령을 선택한다.
2.  Commit 대화 상자의 Message 난에 Commit message 를 상세히 입력한다. Changes made 난에는 수정된 file의 목록이 나타난다. 필요에 따라 compare with base 하여 변경 내용을
3.  \[OK\] button을 누르면 변경 내용이 repository에 반영 된다.
4.  다른 사용자가 같은 project를 check-out하거나 “Update” 명령을 사용하면 변경 내용이 반영된다.

<!-- end list -->

  - Commit message: Commit 할 때 수정된 내용의 의미를 적어둔다.
  - Update: 공동으로 작업할 때 다른 사람들이 수정하여 commit한 모든 최신 version을 일괄적으로 받아오는 것. 역시 download와 유사하다.
  - Diff: 수정된 file의 내용 또는 저장소에 저장된 두 revision 사이의 차이를 비교해 준다.
  - Conflict<ref name=conflic_better_explained>: 개발자 Joe 와 Sue 가 같은 file의 같은 version을 수정중이었다. Joe가 자신이 수정한 file을 먼저 commit 하였다. Sue가 그 사실을 알지 못하고 수정한 file 부분이 Joe가 수정한 부분과 달랐다. 위 그림의 경우, 둘째줄이 Cheese가 되어야 하는지 Hot Dog이 되어야 하는지 혼란이 일어난 것이다. 이런 상태를 방지하기 위해 lock을 사용할 수 있다.

{{ 웹 인용 |url=<http://betterexplained.com/articles/a-visual-guide-to-version-control/> |저자=Kalid Azad |제목=A Visual Guide to Version Control |출판사= BetterExplained |확인날짜=2009-06-14 }} </ref>

  - Conflict의 해결

Sue가 r4를 우선 update 받아서 수정 (Hot Dog을 추가 또는 file 전체 덮어쓰기)한 다음 commit할 수 있다.

  - 여러사람이 동시에 작업한 결과를 안전하게 합치는 법?
      - 모든 경우에 다 가능한 것은 아니다.
      - 잘만 되면 생산성을 n배 늘릴 수도 있다.
      - CVS나 Subversion인 경우에는 가능하지만, 다른 version control system에서는 불가능할 수도 있다.
      - 주의: Commit에 성공과 compile에 성공은 별개의 문제이다. Conflict 없이 여러 commit에 error 없이 성공하더라도 build 과정에서 error가 발생할 수 있다. Compile에 성공과 bug 없는 SW도 별개의 문제이다.

<!-- end list -->

1.  먼저, 어느 version을 기반으로 작업할 것인지 결정한다.
2.  누가 어느 부분을 개정할 것인지 겹치지 않게 분명하게 결정한다. (누가 먼저 commit하더라도 상관 없도록 한다.)
3.  각자 개정 후 commit 한다.

<!-- end list -->

  - 어떤 project가 lock 되었을 때의 효과는?

Subversion은 기본적으로 locking을 별로 선호하지 않는 system이다. 충돌이 일어날 수 있는 상황인 두 사람이 같은 file 같은 version의 같은 부분을 수정할 확률이 높지 않다고 보는 것이다. 그러나 file의 크기가 크지 않은 경우에는 누가 수정을 하더라도 비슷한 위치에서 수정이 일어나기 때문에 충돌이 일어날 가능성이 더 높을 것이다. 또한, 그림 file 등과 같이 merge가 곤란한 file의 경우, lock을 하는 편이 훨씬 안전하다.

Harry가 어떤 file을 lock하면, Sally는 file을 check-out하거나 update 받을 수는 있지만 commit하지는 못한다. 이후 Harry가 lock을 풀면 Sally가 다시 commit할 수 있다.

  - Keyword란?

Subversion 안에 보관중인 file 자체에 file의 이름, 저자, 개정 번호 등의 정보를 자동적으로 기록, 갱신하기 위하여 keyword를 사용할 수 있다. Subversion에서 사용할 수 있는 keyword들 가운데는 다음과 같은 것들이 있다. (대소문자 구별)

1.  $Date$ 마지막으로 commit된 날짜
2.  $Revision$ 마지막으로 commit된 개정판
3.  $Author$ 마지막으로 commit한 개발자

<!-- end list -->

  - 예를 들어 C source에는 다음과 같이 사용할 수 있다.

<!-- end list -->

``` c
//$Date$
//$Revision$
//$Author$
#include <stdio.h>
int main ()
{
    printf (“Hello subverion!!!\n”)
}
```

1.  그 후 TortoiseSVN→Properties... 를 선택하여 대화상자를 연다.
2.  <svn:keyword를> 선택한 후 Property value난에 “Date Revision Author”를 입력한다.
3.  \[OK\] 누르고 Commit 한다.
4.  Command line을 이용한다면 다음과 같이 할 수 있다.

<!-- end list -->

``` bash
    $ svn propset svn:keywords "Date Author Revision" [대상 file 이름]
```

### Branch, Tag, Merge

[650px](https://ko.wikipedia.org/wiki/파일:Subversion_project_visualization.svg "wikilink")

  - Branch: Project의 진행에 영향을 주지 않으면서 새로운 기능, 기술 등을 시험해 보고 싶을 때가 있다. 그럴 때 branch를 만들어서 프로젝트의 본류와 병행으로 개발할 수 있다. 개발이 성공적이라면 추후에 본류에 합류시킬 수 있다. 그렇지 못하다면 합류시키지 않으면 된다.
  - Branch 또는 Tag 만들기

<!-- end list -->

1.  TortoiseSVN → Branch/tag
2.  Copy (Branch / Tag) dialog box의 To URL 항목 에서 \[...\] button 선택, Repo Browser를 연다.
3.  branch 또는 tag를 저장할 folder를 새로 만듦. 예를 들어 원류가
      -

        ``` bash
           file:///c:/svn_repository/Project01/trunk/
        ```

        였다면 branch 위치는

        ``` bash
           file:///c:/svn_repository/Project01/branch/
        ```

        와 같은 형식, Tag 위치는

        ``` bash
           file:///c:/svn_repository/Project01/tags/Success_LED_On/
        ```

        와 같은 형식으로 한다.
4.  Copy (Branch / Tag) dialog box로 돌아온다
5.  [file:///C:/svn_repository/Test/branch/\[file이름\]](file:///C:/svn_repository/Test/branch/%5Bfile이름%5D)
6.  Branch를 만들 revision을 선택
7.  Log message 기록
8.  Switch working copy to new branch/tag 선택
9.  \[OK\] click
10. Branch가 정상적으로 이루어졌는지 보려면 해당 file을 우 click하고 Revision graph 선택.

<!-- end list -->

  - Tag: 따로 뽑아둔 중요한 개정판. 상업 배포판 (예 Windows 3.0, 3.1, 95, 97, ...) 또는 중요한 성공을 이룩한 개정판은 tag를 따로 붙여준다.
  - Branch 또는 tag를 만들면 별도로 checkout해야 하는지?

불필요하다. Switch하면 변경된 data만 download 받는다. 원한다면 Main trunk를 check-out 한 folder 밖에 새로 folder를 하나 만들어서 check out할 수도 있다.

  - Merge: 별도의 branch로 개발된 성과를 본류에 합치는 것
  - Branch를 trunk에 합치기(merge)

<!-- end list -->

1.  Branch를 commit해둔다.
2.  TortoiseSVN → Switch... 선택, Switch To Branch / Tag 대화상자를 연다.
3.  To URL 난에서 trunk의 URL을 선택한다.
4.  Revision은 보통 HEAD revision을 선택한다.
5.  Click \[OK\] 하면 Working copy가 본류의 최신판으로 돌아간다.
6.  TortoiseSVN → Merge... 선택 Merge 대화상자를 연다.
7.  Merge a range of revisions를 선택한 다음 \[Next\]
8.  URL to merge from에서 아까 작업하던 branch를 선택한다. 잘 기억 나지 않으면 \[...\]을 눌러서 repo-browser로 확인한다.
9.  Revision to merge에는 보통 HEAD라고 입력한다음 \[Next\]
10. \[Test merge\]를 눌러 본다. Conflict가 나타나면 실제로 Merge할 때도 conflict가 발생할 것이다. 이는 수동으로 해소 (resolve) 해 주는 것이 바람직하다.
11. Resolve Conflict 대화상자가 나타나면 \[Edit conflict\]를 누른다.
12. Merge 화면이 나타날 것이다. 창틀(pane)이 두개면 오른쪽이 최종 결과이고, 셋이면 Merged가 최종이다. 셋인 경우를 기준으로 설명하면 위 두 창틀에서 어느쪽을 사용할 것인지 정해서 우click, Use this text block을 선택해 준다.
13. Save 하고 Merge 화면을 닫는다.
14. Resolve Conflict 대화상자에서 \[Resolved\]를 click한다. Merge 된 file이 working copy에 반영된다.
15. TortoiseSVN → Diff 선택하여 변경 내용이 바르게 반영되었는지 확인한다.
16. Commit 한다.

## 참고문헌

## 외부 링크

  - [TortoiseSVN 공식 웹사이트](http://tortoisesvn.tigris.org)
  - [TortoiseSVN 내려받기](http://tortoisesvn.net/downloads)

[분류:버전 관리 시스템](https://ko.wikipedia.org/wiki/분류:버전_관리_시스템 "wikilink") [분류:2003년 소프트웨어](https://ko.wikipedia.org/wiki/분류:2003년_소프트웨어 "wikilink") [분류:윈도우 전용 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:윈도우_전용_자유_소프트웨어 "wikilink") [분류:C++로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C++로_작성된_자유_소프트웨어 "wikilink")

1.  {{ 웹 인용 |url=<http://tortoisesvn.net/support> |제목=TortoiseSVN - A Subversion client for Windows |확인날짜=2009-06-14 }}
2.  민진우, 이인선, 2009, 이클립스 프로젝트 필수 유틸리티, , 한빛 미디어.