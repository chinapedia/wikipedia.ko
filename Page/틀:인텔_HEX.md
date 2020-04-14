> This article is converted from Wikipedia: [틀:인텔 HEX](https://ko.wikipedia.org/wiki/틀:인텔_HEX).


<noinclude>

이 틀은 색으로 구분된 [인텔 HEX](../Page/인텔_HEX.md "wikilink") 레코드를 만들어낸다. 시작코드(':' 문자)는 레코드의 모든 필드(데이터 필드 제외)가 주어지면 표시되고, 그렇지 않으면 생략될 것이다.

## 문법

`{{인텔 HEX | 데이터길이 | 주소 | 레코드 종류 | 데이터 | 체크섬}}`

## 예제

  - 색 일러두기

### 완전한 레코드

Complete records will have an automatically prepended start code (':') character. For example,

`{{인텔 HEX|10|0100|00|214601360121470136007EFE09D21901|40}}`

이렇게 된다.

### 부분 레코드

색을 입힌 개별 필드는 다른 필드는 비워둔 채로 틀을 요청하면 표시할 수 있다. 예를 들어,

`{{인텔 HEX||0100|||}}`

이렇게 된다.

## 각주

이 틀의 색 테마는 [Template:SREC HEX와](https://ko.wikipedia.org/wiki/Template:SREC_HEX "wikilink") 같다.

</noinclude><includeonly>{{\#if:|{{\#if:|{{\#if:|{{\#if:|<span style="background-color:#FFFFCC;font-family:monospace">:</span>|}}|}}|}}|}}<span style="background-color:#CCFFCC;font-family:monospace"></span><span style="background-color:#CCCCFF;font-family:monospace"></span><span style="background-color:#FFCCCC;font-family:monospace"></span><span style="background-color:#CCFFFF;font-family:monospace"></span><span style="background-color:#CCCCCC;font-family:monospace"></span></includeonly>