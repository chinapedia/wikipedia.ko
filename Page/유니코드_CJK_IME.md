> This article is converted from Wikipedia: [ CJK IME](https://ko.wikipedia.org/wiki/_CJK_IME).


**유니코드 CJK IME**는 한중일 문자 처리에 모두 똑같이 쓰이는 기술(특히 한자)을 하나로 묶은 솔루션으로, [한국과학기술정보연구원](../Page/한국과학기술정보연구원.md "wikilink")과 [조선민주주의인민공화국](../Page/조선민주주의인민공화국.md "wikilink")의 [평양정보센터](https://ko.wikipedia.org/wiki/평양정보센터 "wikilink")가 남북 정보 기술 협력 사업의 일환으로 같이 개발했다.

설계는 남측에서, 코딩은 북측에서 한 것으로 전해진다. 한편, 한자 사전 자료는 [고려대학교 민족문화연구원이](https://ko.wikipedia.org/wiki/고려대학교_민족문화연구원 "wikilink") 맡았다. [MS IME가](https://ko.wikipedia.org/wiki/MS_IME "wikilink") 기업 작품이라면 이 [IME](https://ko.wikipedia.org/wiki/IME "wikilink")는 연구소 작품이다.

## 특징

[한글](https://ko.wikipedia.org/wiki/한글 "wikilink"), [중국어](../Page/중국어.md "wikilink"), [일본어](../Page/일본어.md "wikilink") IME와 [러시아](../Page/러시아.md "wikilink") 문자 입력기가 한 세트로 개발되었고, 개발 방향 특성에 따라 한자 관련 기능이 MS IME 이상으로 대단히 강력하다. 따라서, 중국어·일본어, 우리 옛글([옛 한글과](https://ko.wikipedia.org/wiki/옛_한글 "wikilink") 한자들) 자료를 많이 입력하는 사람에게 큰 도움이 될 것으로 보인다.

  - 유니코드 모든 영역 한자(서러게이트(surrogate) 빼고)에 대해 [부수](../Page/부수.md "wikilink"), 획수, 독음 정보를 가지고 있고, [한중일 통합 한자](../Page/한중일_통합_한자.md "wikilink")(확장 빼고)는 뜻 정보도 있다.
  - 상당히 정교하고 복잡한 각종 보조 입력 도구들이 있다.
  - 한글 낱자는 U+3130\~U+318F 안에 있는 호환용 낱자가 입력되는 게 아니라 U+1100\~U+11FF 안에 있는 첫가끝 자모가 입력된다.
  - 겹받침 낱자를 따로 조합할 수 있다.
  - 일부 한자는 [한어 병음과](../Page/한어_병음.md "wikilink") 일본어 [훈독](../Page/훈독.md "wikilink")·[음독](https://ko.wikipedia.org/wiki/음독 "wikilink") 정보도 있어서 한중일 어느 IME를 쓰든지 이 정보를 볼 수 있다. (다 제각기 자기 영역에서 쓰이므로)
  - [한양 PUA 코드를](https://ko.wikipedia.org/wiki/한양_PUA_코드 "wikilink") 기반으로 [옛 한글](https://ko.wikipedia.org/wiki/옛_한글 "wikilink") 입력을 옵션으로 지정할 수 있다. 여전히 한양 PUA 코드를 쓰는 [한/글](https://ko.wikipedia.org/wiki/한/글 "wikilink")과 연동하기 좋다.
  - 부수나 독음뿐만 아니라 [사각호마](https://ko.wikipedia.org/wiki/사각호마 "wikilink"), [뿌리법](https://ko.wikipedia.org/wiki/뿌리법 "wikilink"), [재춘법](../Page/재춘법.md "wikilink")(한자 모습을 부호화해 해당 부호로 한자 넣기)으로 한자를 입력할 수 있다.
  - 유니코드 모든 영역 문자표와 [KSC5601](https://ko.wikipedia.org/wiki/KSC5601 "wikilink")에 따른 문자표를 지원하며, 유니코드 문자를 마우스로 두 번 눌러 코드 번호를 직접 입력해서 문자를 넣을 수 있다.
  - [소프트 키보드도](https://ko.wikipedia.org/wiki/소프트_키보드 "wikilink") IME 차원에서 지원한다. (MS IME는 TSF 모듈만 지원)
  - 낱말 [사전](../Page/사전.md "wikilink")을 가지고 있어서 대화 상자를 통해 바뀐 한자를 본문에다 넣을 수 있다.
  - 사전을 인터넷으로 업데이트 할 수 있다.

## 단점

  - 남북 합작품답게 남북한 표준 글자판을 지원하나, [세벌식](https://ko.wikipedia.org/wiki/세벌식 "wikilink")은 전혀 지원하지 않는다.
  - 제품 이름대로, [유니코드](../Page/유니코드.md "wikilink") [API](../Page/API.md "wikilink")로 개발되어 [윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 2000/XP 계열에서만 쓸 수 있다.
  - 구동할 때 여러 [DLL](https://ko.wikipedia.org/wiki/DLL "wikilink")들을 불러들인다. 그 가운데는 [MFC를](../Page/마이크로소프트_파운데이션_클래스_라이브러리.md "wikilink") 쓰는 것도 있다. IME가 MFC를 쓴다는 건 용량을 많이 쓴다는 뜻이다.
  - [조합 윈도가](https://ko.wikipedia.org/wiki/조합_윈도 "wikilink") 어절을 조합하는 것처럼 길쭉하다.
  - 한글 독음으로 한자를 넣을 때, 백여 글자가 넘는 한자 리스트를 빈도는 생각하지 않고 코드 순으로만 보여 준다.
  - [TSF](https://ko.wikipedia.org/wiki/TSF "wikilink") 쪽 [인터페이스는](../Page/인터페이스_\(컴퓨팅\).md "wikilink") 지원하지 않기 때문에 윈도 XP에서 이 IME만 혼자 회색 도구 모음 줄을 따로 띄워 놓는다.
  - TSF를 지원하지 않기 때문에 MS IME처럼 직관적으로 한글 낱말을 바로 한자로 바꿀 수는 없다.

## 오류

  - 환경 설정에서 ‘옛글 포함’ 옵션을 지정하지 않아도 ㄱ+ㄹ로 ᇃ 받침을 조합할 수 있다. 하지만 ᇃ 받침을 조합했을 때, [도깨비불 현상은](https://ko.wikipedia.org/wiki/도깨비불_현상 "wikilink") 제대로 일어나지만 상식적으로 생각할 수 없는 이상한 글자가 뜬다. ‘옛글 포함’ 옵션을 설정해도 ᇃ 받침 버그는 여전하다. 이는 유니코드에서 종성 ᇂ(U+11C2) 다음에 종성 ᇃ(U+11C3)이 있는 것과 관련이 있는 것으로 보이나 자세한 사항은 알 수 없다.
      - ᄀ+ᅡ+ᇃ=개
      - ᄂ+ᅵ+ᇃ=다
      - ᄒ+ᅵ+ᇃ=힤(U+D7A4)

## 현재 버전

파일 버전 리소스를 보면 4.0 버전이라고 나와 있으나, 이 프로그램이 지금도 계속해서 업데이트와 개발이 되고 있는지는 알려지지 않았다.

## 외부 링크

  - [소개](https://web.archive.org/web/20050905102411/http://www.hanasoft.com.cn/frmMain.html?PageID=Work&SubjectID=CJK_IME)
  - [KRISTAL](http://www.kristalinfo.com/download/): 현재 이 페이지의 하단에서 다운로드가 가능하다.

[분류:입력기](https://ko.wikipedia.org/wiki/분류:입력기 "wikilink")