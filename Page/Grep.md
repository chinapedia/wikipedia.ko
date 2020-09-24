> This article is converted from Wikipedia: [Grep](https://ko.wikipedia.org/wiki/Grep).


**grep**(그렙)은 [유닉스](../Page/유닉스.md "wikilink")를 위해 만들어진 텍스트 검색 기능을 가진 명령어이다. 그 이름은 [유닉스](../Page/유닉스.md "wikilink") [ed의](https://ko.wikipedia.org/wiki/ed_\(문서_편집기\) "wikilink") 명령어로 비슷한 기능을 수행하는 *g/re/p*에서 유래되었다.\[1\]

*grep*은 엄밀히 말하면 두문자어(머리글자로 된 말)은 아니지만 *global* / *regular expression* / *print* 에서 각각의 머릿글자를 따 온 것이며 이것은 ed 텍스트 편집기에서 쓰이는 연속적인 지시어이다. *grep* 명령어는 파일이나 표준 입력을 검색하여 주어진 [정규 표현식과](https://ko.wikipedia.org/wiki/정규_표현식 "wikilink") 맞는 줄을 찾아 프로그램의 표준 출력으로 출력한다.

## 사용

*grep*의 일반적인 사용 예는 아래와 같다 :

``` bash
grep apple fruitlist.txt
```

이 경우, grep은 'fruitlist.txt'라는 파일에서 'apple'이라는 단어를 포함하는 모든 줄을 단어 경계와 상관없이 찾아서 출력한다; 따라서 'pineapple'이나 'apple'을 포함하는 모든 줄도 출력된다. grep 명령은 case sensitive(대문자와 소문자의 사용에 따라 단어의 뜻이 달라지는 경우가 있음) 하기 때문에 위와 같은 사용에서 출력된 결과에는 'apple'가 같이 들어 있지 않으면서 'Apple'가 들어있는 줄은 없을 것이다.

다른 대부분의 유닉스 명령어와 같이 grep은 위의 경우나 다른 많은 행동을 수정하기 위해 옵션을 사용할 수 있다. 예를 들어 :

``` bash
grep -i apple fruitlist.txt
```

위와 같은 명령은 대문자 사용 여부와 관계 없이 'apple'이 포함되어 있는 모든 줄을 출력해 줄 것이다. '-i' 옵션은 grep명령어로 하여금 대문자 사용에 대해 반응하지 않거나, 대문자 사용을 무시하도록 해 준다.

'apple' 이 독립적인 한 단어로서 들어 있는 모든 줄을 출력하려면('pineapple'등이 들어 있는 줄은 출력되지 않도록):

``` bash
grep -w apple fruitlist.txt
```

간단하게 하기 위하여 위의 용례는 하나의 영어 단어를 사용하였다. 하지만 [정규 표현식을](https://ko.wikipedia.org/wiki/정규_표현식 "wikilink") 사용하는 경우에는 매우 복잡하며 해독하기 어렵기로 악명이 높다.

grep명령어에 대한 더 자세한 사항들을 위해서는 (사용시 옵션이나 regular expression capabilities/syntax등에 관해서) 보충 설명에 있는 특정 문서들을 참조해야 한다.

## 변형

현존하는 많은 운영 체제에서 grep 명령어는 수많은 보충 기능과 파생 기능을 가지고 있다. grep의 초기 변형어로는 **egrep** 과 **fgrep**이 있었다. 전자는 켄 톰프슨의 원래의 정규 표현식 구현 이후에 이루어진 확장된 정규 표현식 문법 기능을 제공하였다. 후자는 아호-코라식(Aho-Corasick) 알고리즘을 사용하여 고정된 문자열의 리스트를 검색하는 기능을 가지고 있었다. 이와 같은 변형들은 최근의 grep 명령어 보완에 포함되어 대부분이 옵션 기능으로 바뀌었다. 이와 같은 통합 보완 체제 하에서는 grep은 사용되는 이름에 따라 서로 다른 기능을 수행할 수도 있으나, fgrep, egrep, 그리고 grep은 모두 같은 프로그램으로 연결되는 명령어로 기능한다.

Tcgrep은 grep의 보완된 형태로 Perl언어를 사용한다.

'grep'이라는 단어를 포함하는 다른 명령들은 그들이 검색 기능을 갖는다는 의미를 내포하고 있다. 예를 들어 [pgrep](https://ko.wikipedia.org/wiki/pgrep "wikilink") 기능은 주어진 regular expression에 일치하는 이름을 가진 프로세스들의 목록을 보여 준다.

[펄](../Page/펄.md "wikilink")에서 grep은 목록에 존재하는 요소를 검색하는 내장 기능의 이름이다.\[2\] 기술적 프로그래밍 언어에서 이와 같은 기능은 보통 'filter'라고 이름붙여져 있다.

**pcregrep** 명령은 [펄 정규 표현식](https://ko.wikipedia.org/wiki/정규_표현식 "wikilink") 문법을 사용하는 grep의 구현체이다.\[3\] GNU 버전의 grep에서도 -P 플래그를 사용하여 비슷한 기능을 호출할 수 있다.\[4\]

[도스](../Page/도스.md "wikilink"), [OS/2](https://ko.wikipedia.org/wiki/OS/2 "wikilink"), 그리고 [마이크로소프트 윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 기반의 시스템은 간단한 검색 기능을 가진 명령어를 제공한다. 윈도에는 "findstr"이라는 명령어가 있는데 이 명령어는 "grep"과 기능적 측면에서 매우 유사하며 혹은 윈도에서도 [시그윈](../Page/시그윈.md "wikilink")을 이용하여 grep의 변형된 버전을 이용할 수 있다.

## 일상 회화에서의 사용

"grep"이라는 용어는 *찾다*라는 의미를 가진 동사로 활용될 수 있다; 일반적으로는 사람들이 grep 명령어가 수행하는 기능에서 떠올릴 수 있듯 주어진 파일들 내에서의 검색을 칭한다. 직접 목적어는 검색당하는 파일들이 된다: "[Kibo](https://ko.wikipedia.org/wiki/제임스_페리 "wikilink") grepped his [Usenet](../Page/유즈넷.md "wikilink") spool for his name." *[google](https://ko.wikipedia.org/wiki/:en:Google_\(verb\) "wikilink")*이라는 동사와 비교될 수 있다. 때때로 *visual grep* 이라는 구는 무언가를 찾기 위해 텍스트를 훑어본다는 의미로 사용된다.

2003년 12월, [옥스포드 영어사전](../Page/옥스포드_영어사전.md "wikilink") 온라인 은 "grep"이라는 단어를 명사와 동사로써 추가했다.

일반적으로는 "You can't grep dead trees"라는 표현이 사용되기도 하는데, 이것은 전산화된 문서가 종이로 출력된 문서(죽은 나무로 만들어진 종이)보다 더욱 편리하다는 뜻이며, 이는 컴퓨터로는 grep과 같은 명령어를 사용하여 검색을 할 수 있기 때문이다.

## 같이 보기

  - [보이어-무어 문자열 검색 알고리즘](https://ko.wikipedia.org/wiki/보이어-무어_문자열_검색_알고리즘 "wikilink")
  - [유닉스 명령어 목록](../Page/유닉스_명령어_목록.md "wikilink")

## 참고 문헌

  -
  - Hume, Andrew *[A tale of two greps](http://www3.interscience.wiley.com/cgi-bin/abstract/113446956/ABSTRACT?CRETRY=1&SRETRY=0),* Software—Practice and Experience 18, ( 11 ), 1063–1072 ( 1988).

  - Hume, Andrew *Grep wars: The strategic search initiative.* In Peter Collinson, editor, *Proceedings of the EUUG Spring 88 Conference*, pages 237–245, Buntingford, UK, 1988. European UNIX User Group.

## 각주

## 외부 링크

  - [GNU grep (german)](https://www.grepmaster.eu)

  -

  - [The grep Command](http://www.linfo.org/grep.html) - by The Linux Information Project (LINFO)

  - ["The Treacherous Optimization"](http://ridiculousfish.com/blog/archives/2006/05/30/old-age-and-treachery/) - article on tradeoffs in grep to favor best-case over worst-case scenarios

  - [Egrep for linguists](http://stts.se/index.php?lang_id=en_uk&page=egrep) An introduction to egrep

  - [Tony Abou-Assaleh's list of Greps](http://tony.abou-assaleh.net/GREPs)

[분류:유닉스 텍스트 처리 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_텍스트_처리_유틸리티 "wikilink") [분류:표준 유닉스 프로그램](https://ko.wikipedia.org/wiki/분류:표준_유닉스_프로그램 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink") [분류:GNU 프로젝트 소프트웨어](https://ko.wikipedia.org/wiki/분류:GNU_프로젝트_소프트웨어 "wikilink")

1.
2.
3.
4.