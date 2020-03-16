> This article is converted from Wikipedia: [SAMI](https://ko.wikipedia.org/wiki/SAMI).


**SAMI**(사미, Synchronized Accessible Media Interchange; 접근성 미디어 동기화 교환)는 [마이크로소프트](../Page/마이크로소프트.md "wikilink") 사에서 1998년에 발표한 미디어 접근 제안이다. [마크업 언어로](../Page/마크업_언어.md "wikilink") 구조화되어 있으며 개인용 컴퓨터에서의 미디어 재생용 자막을 간단히 만들 수 있도록 하는 데 중점을 두고 설계되어 방송용으로는 적합하지 않다.

SAMI 문서는 문자열로 되어 있으므로 어떠한 [문서 편집기로도](../Page/문서_편집기.md "wikilink") 기록하고 수정할 수 있다. 또, SAMI 문서를 전문적으로 만들어 주는 유틸리티도 존재한다. 파일 확장자는 .smi 또는 .sami이며, [SMIL](../Page/SMIL.md "wikilink") 파일의 확장자와 충돌 가능성이 있어 .smi가 보통 쓰인다.

각 SAMI 문서는 하나 이상의 언어를 담을 수 있으며 [대한민국](../Page/대한민국.md "wikilink")에서는 지배적으로 이 자막 포맷을 사용한다.

## 사용할 수 있는 HTML 태그와 CSS

SAMI 문서 안에서 문자열을 꾸미기 위해 [HTML](../Page/HTML.md "wikilink")과 [CSS](https://ko.wikipedia.org/wiki/CSS "wikilink")를 사용할 수 있다. 아래와 같은 HTML 태그가 SAMI에서 동작한다.

| 이름         | 설명                   |
| :--------- | :------------------- |
| B          | 굵은 글씨                |
| BASEFONT   | 기본 글꼴 크기             |
| BDO        | 글 방향 설정              |
| BIG        | 큰 글자 스타일             |
| BLOCKQUOTE | 긴 인용                 |
| BR         | 강제 개행(줄 바꾸기-"Enter") |
| CAPTION    | 표 자막                 |
| CENTER     | DIV align=center의 줄임 |
| COL        | 표 열(列)               |
| COLGROUP   | 표 열 그룹               |
| DD         | 정의 설명                |
| DIV        | 영역내 언어/스타일 지정        |
| DL         | 정의 목록                |
| DT         | 정의 용어                |
| FONT       | 특정 영역의 글꼴 지정         |
| H1         | 제목                   |
| H2         | 제목                   |
| H3         | 제목                   |
| H4         | 제목                   |
| H5         | 제목                   |
| H6         | 제목                   |
| HR         | 가로선                  |
| I          | 글자 기울임               |
| IMG        | 그림 삽입                |
| LI         | 항목 나열                |
| OL         | 순서 있는 목록             |
| P          | 문단                   |
| PRE        | 기서식된 문자열             |
| Q          | 짧은 인라인 인용            |
| S          | 글자에 삭선               |
| SMALL      | 작은 글자 스타일            |
| SPAN       | 영역내 언어/스타일 지정        |
| STRIKE     | 글자에 삭선               |
| SUB        | 아래첨자                 |
| SUP        | 위첨자                  |
| TABLE      | N/A                  |
| TBODY      | 표                    |
| TD         | 표 자료 칸               |
| TFOOT      | 표 바닥                 |
| TH         | 표 머리 칸               |
| THEAD      | 표 머리                 |
| TR         | 표 행(行)               |
| TT         | 타자기 스타일              |
| U          | 글자 밑줄                |
| UL         | 순서 없는 목록             |

## 기본 구조

``` html4strict
<sami>
 <head>
  <Title> 제목 </Title>
  <STYLE TYPE="text/css"> 설정값 </STYLE>
 </head>
 <body>
  <SYNC Start=0>
  <P Class=KRCC>한국어 자막</P>
  <P Class=ENUSCC>English Subtitle</P>

  <SYNC Start=1000>
  <P Class=KRCC> </P>
  <P Class=ENUSCC> </P>

 </body>
</sami>
```

## 같이 보기

  - [자막](https://ko.wikipedia.org/wiki/자막 "wikilink")
  - [SMIL](../Page/SMIL.md "wikilink")
  - [LRC (파일 포맷)](../Page/LRC_\(파일_포맷\).md "wikilink")

## 외부 링크

  - [SAMI](http://msdn.microsoft.com/library/default.asp?url=/library/en-us/dnacc/html/atg_samiarticle.asp)
  - [SMI SRT 자막 변환](https://convert.jamack.net/)

[분류:영상 기술](https://ko.wikipedia.org/wiki/분류:영상_기술 "wikilink")