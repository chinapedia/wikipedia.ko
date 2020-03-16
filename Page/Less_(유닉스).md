> This article is converted from Wikipedia: [Less \(\)](https://ko.wikipedia.org/wiki/Less_\(\)).


**less**(레스)는 [유닉스](../Page/유닉스.md "wikilink")나 [윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink"), [유닉스 계열](../Page/유닉스_계열.md "wikilink") 시스템에서 텍스트 파일을 한 번에 한 화면씩 보여주는 터미널 페이저(terminal pager)이다. less는 기능적으로 more와 유사하나 파일의 앞쪽과 뒤쪽으로 이동할 수 있는 more의 개량형 명령어라고 볼 수 있다. 대부분의 유닉스의 문서 편집기나 뷰어와는 다르게 less는 구동 전에 전체 파일을 읽지 않기 때문에 큰 용량의 파일을 더 빨리 읽을 수 있다.

## 역사

`less`는 1983\~85년에 [Mark Nudelman에](https://ko.wikipedia.org/wiki/Mark_Nudelman "wikilink") 의해 more 명령어[`more`](https://ko.wikipedia.org/wiki/more "wikilink")에 텍스트의 뒤로 스크롤하는 것을 가능하게 하기 위해 만들어졌다. less라는 이름은 "뒤로도 more"라는 이유로 재미있게 지어졌다.`less`는 현재 [GNU](../Page/GNU.md "wikilink") 프로젝트의 한 부분으로 대부분의 유닉스 계열 시스템에 사용되고 있다.

## 사용법

`less`가 구동되는 동안 그것의 옵션을 통해 구동 환경을 변경시킬 수 있다. 예를 들면, 옵션 `-n` 또는 `--line-number` 을 통해 한 페이지에 출력되는 줄 수를 조절할 수 있다. `less`가 파일 내용을 보여주는 동안 여러 가지 명령어들을 사용할 수 있다. 이러한 명령어들은 `more`와 [`vi`](https://ko.wikipedia.org/wiki/vi "wikilink").에도 동일하게 적용된다. 또한 텍스트 파일에 있는 문자열도 찾을 수 있다.

결론적으로, `less`는 파일 내용을 [표준 출력](https://ko.wikipedia.org/wiki/표준_출력 "wikilink")(한 번에 한 화면씩) 해준다. 만약 파일 이름이 생략된다면 less는 표준 입력(보통 파이프를 통한 다른 명령어들의 출력)의 내용을 표준 출력 해준다. 만약 출력이 터미널 이외의 것으로 다시 지정되면 예를 들어 다른 명령의 [pipe](https://ko.wikipedia.org/wiki/파이프라인_\(유닉스\) "wikilink")), `less`는 [`cat`](https://ko.wikipedia.org/wiki/cat_\(유닉스\) "wikilink")과 같은 역할을 수행한다.

명령어 용법\[1\]:

`less `*`[options]`*` `*`file_name`*

### 자주 사용되는 명령어

  - ////: 이동.

  - : 다음 페이지로 이동.

  - **b**: 전 페이지로 이동.

  - *n***g**: *n*줄만큼 이동. 기본적으로 파일의 시작.

  - *n***G**: *n*줄만큼 이동. 기본적으로 파일의 끝.

  - **/***pattern*: 문자 패턴을 찾는다. 정규 표현이 사용될 수 있다.

  - **n**: 일치하는 다음 문자열로 이동 (검색 후에 사용).

  - **N**: 일치하는 바로 전 문자열로 이동.

  - **m***letter*: 현재의 문자의 위치를 기억.

  - **'***letter*: 기억한 위치로 이동

  - **'^** or **g**: 파일의 시작으로 이동.

  - **'$** or **G**: 파일의 끝으로 이동.

  - **s**: 현재 내용을 저장

  - **=**: 파일 정보.

  - **F**: 파일의 정보를 마지막 내용까지 지속적으로 읽는다. logs watching에 효과적이다. 이 모드를 종료하려면 +를 누른다.

  - **h**: 도움말.

  - **q**: 종료

### 자주 사용되는 옵션

  - `-?`: less에서 사용할 수 있는 명령들에 대한 도움말을 제공한다. 이 옵션이 사용되면 다른 인수는 무시되고, 도움말 화면을 보여준다.
  - `-a`: 마지막 라인이 화면에 출력되고 나서 탐색을 시작한다.
  - `-c`: 필요할 때 전체 화면은 다시 갱신한다.
  - `-e`: 두 번째로 파일의 끝에 도달하면 자동적으로 종료한다.
  - `-E`: 파일의 끝에 도달하기만 하면 자동적으로 종료한다.
  - `-i`: 대소문자를 구분하지 않고 탐색한다.
  - `-N`: 행 번호를 추가한다.
  - `-q`: 특정 오류가 발생하지 않으면 아무 소리도 내지 않고 조용히 동작한다.
  - `-Q`: 결코 아무 소리도 내지 않는다.
  - `-s`: 연속되는 공백 라인은 한 행의 공백으로 처리한다.
  - `-x숫자`: 수치를 지정해서 탭 간격을 조정한다. 기본값은 8이다.

## 사용 예

``` bash
less -M readme.txt
file * | less
grep -i void *.c | less -I -p void
```

## 각주

## 외부 링크

  - [공식 홈페이지](http://www.greenwoodsoftware.com/less/)
  - [less 관련 개인 홈페이지](http://www.linuxmanpages.com/man1/)

### `less`의 변화

  - [맥 오에스 텐에서](https://ko.wikipedia.org/wiki/맥_오에스_텐 "wikilink") 사용되는 [AquaLess](http://aqualess.sourceforge.net/)

[분류:GNU 프로젝트 소프트웨어](https://ko.wikipedia.org/wiki/분류:GNU_프로젝트_소프트웨어 "wikilink") [분류:터미널 페이저](https://ko.wikipedia.org/wiki/분류:터미널_페이저 "wikilink")

1.