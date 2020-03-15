> This article is converted from Wikipedia: [ROT13](https://ko.wikipedia.org/wiki/ROT13).


[right](https://ko.wikipedia.org/wiki/파일:ROT13_table_with_example.svg "wikilink")

**ROT13**(Rotate by 13)은 단순한 **[카이사르 암호](https://ko.wikipedia.org/wiki/카이사르_암호 "wikilink")**의 일종으로 영어 알파벳을 13글자씩 밀어서 만든다. 흔히 **ROT-13** 혹은 **rot13**이라고도 쓴다. 예를 들어서 'I LOVE YOU'를 ROT13으로 암호화하면 'V YBIR LBH'가 된다. 이 방법은 [유즈넷](../Page/유즈넷.md "wikilink")을 비롯한 온라인 게시판에서 퍼즐의 정답이나 [스포일러](../Page/스포일러.md "wikilink") 등과 같이 미리 보기를 원치 않는 내용을 암호화하는 데 자주 사용된다.

## 역사

ROT13은 [1980년대](../Page/1980년대.md "wikilink") 초반의 [net.jokes](http://groups.google.com/group/net.jokes) [뉴스그룹](https://ko.wikipedia.org/wiki/뉴스그룹 "wikilink")에서 유래하였다. 원래 목적은 보기에 따라서 모욕적일 수 있는 내용이나, 유머에서 가장 중요한 마지막 줄들을 실수로 미리 보는 일이 없도록 하려는 것이었다. 처음에는 모욕적인 농담을 다른 뉴스그룹에 올려서 분류하려 하기도 했으나, 관리자들은 그런 뉴스그룹을 만드는 것이 마치 어떤 모욕적인 내용이라도 해당 그룹에 올리면 문제가 없다는 식으로 보일 수 있다는 이유로 이를 반대했다. ROT13은 그 단순함 때문에 이런 용도에 알맞았다.

ROT13은 영어 알파벳을 다른 영어 알파벳으로 치환만 하기 때문에, 알파벳 이외의 일반적이지 않은 문자를 처리하지 못하는 [뉴스리더](https://ko.wikipedia.org/wiki/뉴스리더 "wikilink")에서도 문제를 발생시키지 않았다. ROT13은 영어에서 가능한 25가지의 카이사르 암호(ROT-1부터 ROT-25까지) 중에서 암호화와 복호화가 같은 유일한 방법이었기 때문에 선택되었다. (만약 영어 알파벳이 26자가 아니라, [폴란드어](../Page/폴란드어.md "wikilink")같이 더 많거나 [하와이어](../Page/하와이어.md "wikilink")같이 더 적었다면 다른 방법이 선택되었을 것이다.)

손으로 메시지를 암호화하고 복호화할 수도 있지만, 자동으로 암호화나 복호화를 해 주는 것이 더 편리하다. 예를 들어 ROT13이 만들어진 지 얼마 안 있어 뉴스리더 소프트웨어들은 자동으로 복호화하는 기능을 지원하였으며, [유닉스 계열](../Page/유닉스_계열.md "wikilink") 시스템들은 [tr](https://ko.wikipedia.org/wiki/tr_\(프로그램\) "wikilink")(transliterate의 약자)이라는 표준 유틸리티를 지원하기 때문에 다음과 같은 방법으로 ROT13 암호화 및 복호화를 할 수 있다.

``` bash
 $ echo "Or fher gb qevax lbhe Binygvar" | tr 'A-Za-z' 'N-ZA-Mn-za-m'
 Be sure to drink your Ovaltine
```

## 암호학적인 관점

한마디로하면 카이사르암호에 키값으로 13을 준것과 동일하다. 그런데 ROT13이라는 이름에서 이미 키값이 공개되어있으므로 이하의 문단에서는 키가 없고, 키가 공개되어있으므로 암호화가 안된다고 표현한다.

ROT13은 별도의 [열쇠값](https://ko.wikipedia.org/wiki/열쇠값 "wikilink")이 없는 암호화 방법이기 때문에, ROT13을 사용했다는 사실만 알면 누구라도 메시지를 복호화할 수 있다. 비록 ROT13을 사용했다는 사실을 알지 못하더라도 [카이사르 암호를](https://ko.wikipedia.org/wiki/카이사르_암호 "wikilink") 푸는 데 사용하는 [빈도 분석](https://ko.wikipedia.org/wiki/빈도_분석 "wikilink") 등의 방법을 사용하면 간단하게 복호화가 가능하다. 따라서 이 방법은 [암호학](../Page/암호학.md "wikilink")적으로는 [기밀성](https://ko.wikipedia.org/wiki/기밀성 "wikilink")을 전혀 보장하지 못하며, 약한 암호화 방법을 비유할 때 잘 사용된다.

ROT13의 실제 용도는 메시지를 보는 사람이 암호화된 메시지를 복호화할 것인지 말 것인지를 선택할 수 있게 하는 것이다. 인증되지 않은 사람이 비밀스런 메시지를 볼 수 없게 하는 것과는 다르게, ROT13은 [스포일러](../Page/스포일러.md "wikilink")와 같이 의도적이지 않게 해당 내용을 보게 되는 상황을 막아 준다.

영어 알파벳은 26글자이기 때문에 ROT13 암호화를 두 번 하면 원래의 평문을 얻을 수 있으며, 따라서 [암호화](../Page/암호화.md "wikilink")와 [복호화](../Page/복호화.md "wikilink")가 동일하다. 이 사실 때문에 종종 **이중 ROT13**, **2ROT13**, **ROT26**라는 용어를 농담삼아 쓰기도 한다. (앞에서 말했듯이 이 방법들은 평문을 전혀 암호화하지 않는다.) 비슷하게 그냥 ROT13과 동일한 **삼중 ROT13**이라는 용어도 사용된다. 아마 이는 [삼중 DES의](https://ko.wikipedia.org/wiki/삼중_DES "wikilink") 패러디로 보인다.

## 외부 링크

  - [온라인 ROT13 암호화 및 복호화](http://www.rot13.com/)

[분류:고전 암호](https://ko.wikipedia.org/wiki/분류:고전_암호 "wikilink") [분류:인터넷 문화](https://ko.wikipedia.org/wiki/분류:인터넷_문화 "wikilink")