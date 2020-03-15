> This article is converted from Wikipedia: [Shift JIS](https://ko.wikipedia.org/wiki/Shift_JIS).


[frame](https://ko.wikipedia.org/wiki/파일:Shiftjis-map.png "wikilink")

**Shift_JIS** 또는 **Shift-JIS**는 [JIS X 0201과](../Page/JIS_X_0201.md "wikilink") [JIS X 0208](../Page/JIS_X_0208.md "wikilink") 등을 사용하는 [일본어](../Page/일본어.md "wikilink") [문자 인코딩이며](../Page/문자_인코딩.md "wikilink"), 보통 **SJIS**로 줄여 부른다. [1982년](../Page/1982년.md "wikilink")에 [일본](../Page/일본.md "wikilink")의 여러 업체들이 중심이 되어 개발했으나, 나중에 일본 안에서 널리 쓰이게 되자 JIS X 0208:1997의 부속서 1로 표준화되었다.

## 역사

[1980년대](../Page/1980년대.md "wikilink") 이전의 컴퓨터에서는 JIS X 0201을 사용한 인코딩이 주로 사용되었다. 즉, 32부터 127까지의 바이트(GL)에는 영문자를, 160부터 255까지의 바이트(GR)에는 [가타카나](../Page/가타카나.md "wikilink")를 배당한 것이다. 시간이 지나면서 한자를 표시할 수 있는 하드웨어가 등장했고 그에 맞는 문자 인코딩이 필요해졌으나, 이미 널리 사용되는 인코딩에서 GR을 사용하고 있었기 때문에 [ISO/IEC 2022의](https://ko.wikipedia.org/wiki/ISO/IEC_2022 "wikilink") 확장 방법으로는 하위 호환성을 유지하면서 JIS X 0208을 지원할 수 없었다. Shift_JIS는 이전 인코딩과의 호환을 위해 JIS X 0208에서 사용하고 있지 않던 영역(0x81\~0x9F, 0xE0\~0xEF)에 JIS X 0208을 별도의 계산 과정으로 할당하는 방법을 썼다. 또한 두 번째 바이트를 128 이상으로 제한할 경우 JIS X 0208의 모든 문자를 대응시킬 수 없었기 때문에, 두 번째 바이트에 128보다 작은 바이트도 사용할 필요가 있었다.

Shift_JIS를 개발한 업체들에 대해서는 몇 가지 설이 있다. 일본 마이크로소프트 전 회장인 [후루카와 토오루](https://ko.wikipedia.org/wiki/후루카와_토오루 "wikilink")()에 따르면 [아스키](https://ko.wikipedia.org/wiki/주식회사_아스키 "wikilink"), [마이크로소프트](../Page/마이크로소프트.md "wikilink"), [미쓰비시 전기](https://ko.wikipedia.org/wiki/미쓰비시_전기 "wikilink"), 마이크로소프트웨어 어소시에이트, [디지털 리서치가](../Page/디지털_리서치.md "wikilink") 관련되었으며, 특히 아스키의 야마시타 료조()가 중심이 되어 만들어졌다고 하지만, [교토 대학](../Page/교토_대학.md "wikilink") 조교수인 야스오카 코이치()는 마이크로소프트웨어 어소시에이트와 미쓰비시 전기만이 관련되었다고 주장하고 있다.\[1\] 개발 주체와는 별개로, [마이크로소프트](../Page/마이크로소프트.md "wikilink") 등의 회사들이 얼마 지나지 않아 자신들의 제품에서 Shift_JIS를 지원했던 것은 사실이다.

JIS X 0208에 비어 있는 영역이 꽤 있고, Shift_JIS 자체에도 0xF0부터 0xFF까지의 첫 바이트에는 아무 글자도 할당되어 있지 않았기 때문에 다양한 확장들이 만들어졌다. 예를 들어, 이 확장들 중 가장 많이 쓰이는 마이크로소프트의 [코드 페이지 932](https://ko.wikipedia.org/wiki/코드_페이지_932 "wikilink")(엄밀하게는 Windows-31J)는 JIS X 0208의 확장이며, 일본 [휴대폰](https://ko.wikipedia.org/wiki/휴대폰 "wikilink") 업체들은 [전자 메일에서](https://ko.wikipedia.org/wiki/전자_메일 "wikilink") 사용하기 위해 여러 그림 문자를 0xF3부터 0xF9까지의 영역에 할당해서 쓰고 있다. 이러한 확장들은 대부분 확장된 영역에서 서로 호환되지 않으며 [IANA](https://ko.wikipedia.org/wiki/IANA "wikilink")에도 등록되어 있지 않은 것이 많아 혼동을 주곤 한다.

본래는 [일본 산업 규격과는](https://ko.wikipedia.org/wiki/일본_산업_규격 "wikilink") 상관 없이 만들어진 인코딩이지만, Shift_JIS가 많이 쓰이게 되면서 사실상의 표준이 되었기 때문에 [1997년](../Page/1997년.md "wikilink")판부터는 부속서 1에 ‘시프트 부호화 표현()’로 이 인코딩을 설명하고 있다. 여기에도 몇 가지 확장이 있는데, [2000년](../Page/2000년.md "wikilink")에 제정된 [JIS X 0213을](https://ko.wikipedia.org/wiki/JIS_X_0213 "wikilink") 반영한 **Shift_JISX0213**과, JIS X 0213이 [2004년](../Page/2004년.md "wikilink")에 개정되면서 이를 반영한 **Shift_JIS-2004**가 있다.

## 구성

Shift_JIS는 JIS X 0201을 기반으로, 사용되지 않는 두 영역에 JIS X 0208을 간단한 계산으로 다음과 같이 잘라 넣는다.

1.  행 번호에 0xE1(0x60행 이하) 또는 0x161(0x61행 이상)을 더한다. 이 값을 2로 나눈 몫을 첫 번째 바이트로 한다.
2.  1에서 나온 값이 짝수인가 홀수인가에 따라, 열 번호에 0x1F(홀수)나 0x7D(짝수)를 더한다.
3.  2에서 나온 값이 0x7F보다 크거나 같으면 1을 더해 두 번째 바이트로 하고, 아니면 그 값을 그대로 두 번째 바이트로 한다.

이렇게 해서 계산된 첫 번째 바이트는 0x81부터 0x9F까지와 0xE0부터 0xEF까지이고, 두 번째 바이트는 0x40부터 0x7E까지와 0x80부터 0xFC까지가 된다. 두 번째 바이트의 최상위 비트가 설정되지 않을 수도 있기 때문에 Shift_JIS 인코딩을 인식하는 것은 쉽지 않을 수 있다. 또한 두 번째 바이트에는 [역슬래시](../Page/역슬래시.md "wikilink")(\\, 0x5C)가 포함되기 때문에 Shift_JIS를 사용하는 시스템에서 압축한 [ZIP](https://ko.wikipedia.org/wiki/ZIP "wikilink") 파일을 다른 시스템에서 풀 수 없는 경우도 생긴다.

## 같이 보기

  - [코드 페이지 932](https://ko.wikipedia.org/wiki/코드_페이지_932 "wikilink")(Windows-31J) - 가장 많이 쓰이는 Shift_JIS의 확장
  - [EUC-JP](https://ko.wikipedia.org/wiki/EUC-JP "wikilink")

## 참조

<references/>

## 외부 링크

  - [일본어 텍스트 인코딩 (Ka-Ping Yee)](http://lfw.org/text/jp.html)

  - [JIS X 0201 부분을 뺀 Shift_JIS 변환표](http://www.rikai.com/library/kanjitables/kanji_codes.sjis.shtml)

  - [Shift_JIS 전각 문자](http://www.page.sannet.ne.jp/mtoga/etc/cpu/bih-g_cj.htm)

  - [Shift_JIS 제 1수준 한자](http://www.page.sannet.ne.jp/mtoga/etc/cpu/bih-g_ck.htm)

  - [Shift_JIS 제 2수준 한자](http://www.page.sannet.ne.jp/mtoga/etc/cpu/bih-g_cl.htm)

  - [기타 Shift_JIS 문자](http://www.page.sannet.ne.jp/mtoga/etc/cpu/bih-g_cm.htm)

[분류:문자 인코딩](https://ko.wikipedia.org/wiki/분류:문자_인코딩 "wikilink")

1.  [일본 슬래시닷의 글](http://slashdot.jp/~yasuoka/journal/334730)을 참고하라. 그에 따르면 이런 주장이 마이크로소프트웨어 어소시에이트가 아스키와 마이크로소프트의 자회사로 설립되었기 때문에 일어난 오해라고 한다.