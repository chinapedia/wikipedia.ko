> This article is converted from Wikipedia: [ANSI.SYS](https://ko.wikipedia.org/wiki/ANSI.SYS).


**ANSI.SYS**는 [도스](../Page/도스.md "wikilink") 운영 체제의 [장치 드라이버로](../Page/장치_드라이버.md "wikilink") [안시 이스케이프 코드](https://ko.wikipedia.org/wiki/안시_이스케이프_코드 "wikilink") 지원을 추가한다. 안시 X3L2 터미널 위원회에서 정의한 표준을 사용한다.

MS-DOS에서 ANSI.SYS 파일을 사용하려면 [CONFIG.SYS](../Page/CONFIG.SYS.md "wikilink") 파일에 다음을 추가한다.

`device=(`*`드라이브:`*`)(`*`경로`*`)ANSI.SYS`

드라이브와 경로는 상황에 맞게 치환하면 된다. [윈도 XP의](https://ko.wikipedia.org/wiki/윈도_XP "wikilink") 경우에는 CONFIG.NT 파일을 편집해야 할 수도 있다.

이 파일이 불러지면 [화면의](https://ko.wikipedia.org/wiki/컴퓨터_디스플레이 "wikilink") "문자와 [커서](../Page/커서_\(사용자_인터페이스\).md "wikilink")"에 보이는 색을 바꿀 수 있도록 해 주며, 텍스트 그래픽 기능을 사용할 수 있도록 해 준다. 이 드라이버를 사용하면 텍스트는 16가지 색 가운데 하나를 지정할 수 있다. 또한 80x25 텍스트 모드 화면 대신 그래픽 모드를 쓸 수 있도록 해 준다.

이 파일의 재미있는 기능은 키보드의 키를 바꿀 수 있다는 것이다. 이 기능을 악용하면 "안시 폭탄"과 같은 매핑을 만들 수 있다. 이 때의 안티바이러스 소프트웨어는 F3 키가 `DEL *.*` 또는 `FORMAT C:` 로, "아니오"로 대답하기 위한 N 키가 `Y` 키로 매핑되었는지 등을 검사해야 했다.

ANSI.SYS 파일은 몇몇 소프트웨어에서 필요했다. 특히 게시판 시스템에서 ANSI.SYS를 많이 사용하였다. [모뎀](../Page/모뎀.md "wikilink")을 사용하던 때 [대한민국](../Page/대한민국.md "wikilink") 통신 게시판에서도 안시를 사용한 장난이 유행한 적이 있었다. 또한 온라인 게임과 같은 곳에서도 [커서를](../Page/커서_\(사용자_인터페이스\).md "wikilink") 제어하기 위해서 사용했다.

## 지원 운영 체제

ANSI.SYS 파일은 일부 [마이크로소프트](../Page/마이크로소프트.md "wikilink") 운영 체제 제품에 포함되어 있다:

  - [MS-DOS](../Page/MS-DOS.md "wikilink")
  - [윈도 95](https://ko.wikipedia.org/wiki/윈도_95 "wikilink")
  - [윈도 98](https://ko.wikipedia.org/wiki/윈도_98 "wikilink")
  - [윈도 NT](https://ko.wikipedia.org/wiki/윈도_NT "wikilink")
  - [윈도 2000](https://ko.wikipedia.org/wiki/윈도_2000 "wikilink")
  - [윈도 XP](https://ko.wikipedia.org/wiki/윈도_XP "wikilink")
  - [윈도 서버 2003](https://ko.wikipedia.org/wiki/윈도_서버_2003 "wikilink") (x86 버전)
  - [윈도 비스타](https://ko.wikipedia.org/wiki/윈도_비스타 "wikilink")

## 기능

ANSI.SYS에 특화된 이스케이프 시퀀스가 몇 가지 있다.

| 시퀀스                                    | 결과        |
| -------------------------------------- | --------- |
| CSI = *n* h                            | 화면 모드 설정. |
| CSI = *n* l                            | 화면 모드 초기화 |
| CSI *code* ; *param* \[ ; *param* \] p | 키 다시 정의.  |

| 모드 | 설명                                                                       | 모드                                                    | 설명                      |
| -- | ------------------------------------------------------------------------ | ----------------------------------------------------- | ----------------------- |
| 0  | 40 × 25 모노                                                               | 1                                                     | 40 × 25 컬러              |
| 2  | 80 × 25 모노                                                               | 3                                                     | 80 × 25 컬러              |
| 4  | 320 × 200 컬러                                                             | 5                                                     | 320 × 200 모노            |
| 6  | 640 × 200 모노                                                             | 14                                                    | 640 x 200 컬러 (16색 그래픽)  |
| 13 | 320 x 200 컬러 (그래픽)                                                       | [19](https://ko.wikipedia.org/wiki/모드_13h "wikilink") | 320 x 200 컬러 (256색 그래픽) |
| 15 | 640 x 350 [모노크롬](https://ko.wikipedia.org/wiki/모노크롬 "wikilink") (2색 그래픽) | 16                                                    | 640 x 350 컬러 (16색 그래픽)  |
| 17 | 640 x 480 모노크롬 (2색 그래픽)                                                  | 18                                                    | 640 x 480 컬러 (16색 그래픽)  |
| 7  | 줄 끝에서 줄 바꿈                                                               |                                                       |                         |

화면 모드

## 같이 보기

  - [안시 이스케이프 코드](https://ko.wikipedia.org/wiki/안시_이스케이프_코드 "wikilink")

## 외부 링크

  - [도스 프롬프트](http://kb.indiana.edu/data/aamm.html)
  - [안시 폭탄](https://web.archive.org/web/20070928004721/http://nightmare.org/textfiles/ansi/ansibomb.txt)
  - [ANSI.SYS 사용하기](https://web.archive.org/web/20070623224036/http://enterprise.aacc.cc.md.us/~rhs/ansi.html)
  - [Ansilove/PHP](http://ansilove.sourceforge.net)

[분류:도스용 파일](https://ko.wikipedia.org/wiki/분류:도스용_파일 "wikilink") [분류:도스용 드라이버](https://ko.wikipedia.org/wiki/분류:도스용_드라이버 "wikilink") [분류:도스 기술](https://ko.wikipedia.org/wiki/분류:도스_기술 "wikilink")