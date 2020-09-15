> This article is converted from Wikipedia: [PA-RISC](https://ko.wikipedia.org/wiki/PA-RISC).


[섬네일](https://ko.wikipedia.org/wiki/파일:HP_PA-RISC_7300LC.jpg "wikilink") **PA-RISC**는 [휴렛 패커드가](https://ko.wikipedia.org/wiki/휴렛_패커드 "wikilink") 개발한 [명령어 집합 아키텍처](../Page/명령어_집합.md "wikilink")(ISA)이다. 이름에 언급된대로 [RISC](https://ko.wikipedia.org/wiki/RISC "wikilink") 아키텍처의 하나로, PA는 Precision Architecture를 가리킨다. 이 디자인은 HP/PA(Hewlett Packard Precision Architecture)를 가리키기도 한다.

이 아키텍처는 1986년 2월 26일에 [HP 3000 시리즈 930과](https://ko.wikipedia.org/wiki/HP_3000 "wikilink") [HP 9000 모델840](https://ko.wikipedia.org/wiki/HP_9000 "wikilink") 컴퓨터가 TS1이라는 기능을 처음 구현하면서 도입되었다.\[1\]\[2\]

PA-RISC의 후계자는 HP와 [인텔](../Page/인텔.md "wikilink")이 함께 개발한 [아이테니엄](../Page/아이테니엄.md "wikilink") (본래 IA-64) ISA이다.\[3\] HP는 PA-RISC 기반의 HP 9000 시스템을 2008년 말에 판매를 중단하였으나 2013년까지 PA-RISC 칩을 구동하는 서버를 지원하였다.\[4\]

## CPU 사양

| 모델       | 마케팅 이름                                                                 | 연도   | 주파수 \[MHz\] | 메모리 버스 \[MB/초\] | 공정 \[µm\] | 트랜지스터 \[100만\] | 다이 크기 \[mm²\] | 전력 \[W\]    | D캐시 \[kB\] | I캐시 \[kB\] | L2 캐시 \[MB\] | ISA  | 참고    |
| -------- | ---------------------------------------------------------------------- | ---- | ----------- | --------------- | --------- | -------------- | ------------- | ----------- | ---------- | ---------- | ------------ | ---- | ----- |
| TS-1     | ?                                                                      | 1986 | 8           | ?               | ?         | —              | —             | ?           | ?          | ?          | —            | 1.0  |       |
| CS-1     | ?                                                                      | 1987 | 8           | ?               | 1.6       | 0.164          | 72.93         | 1           | —          | 0.25       | —            | 1.0  | \[5\] |
| NS-1     | ?                                                                      | 1987 | 25/30       | ?               | 1.5       | 0.144          | 70.56         | ?           | ?          | ?          | —            | 1.0  | \[6\] |
| NS-2     | ?                                                                      | 1989 | 27.5/30     | ?               | 1.5       | 0.183          | 196           | 27          | 512        | 512        | —            | 1.0  | \[7\] |
| PCX      | ?                                                                      | 1990 | ?           | ?               | ?         | ?              | ?             | ?           | ?          | ?          | ?            | 1.0  |       |
| PCX-S    | PA-7000                                                                | 1991 | 66          | ?               | 1.0       | 0.58           | 201.6         | ?           | 256        | 256        | —            | 1.1a |       |
| PCX-T    | [PA-7100](https://ko.wikipedia.org/wiki/PA-7100 "wikilink")            | 1992 | 33–100      | ?               | 0.8       | 0.85           | 196           | ?           | 2048       | 1024       | —            | 1.1b |       |
| PCX-T    | [PA-7150](https://ko.wikipedia.org/wiki/PA-7150 "wikilink")            | 1994 | 125         | ?               | 0.8       | 0.85           | 196           | ?           | 2048       | 1024       | —            | 1.1b |       |
| PCX-T'   | [PA-7200](https://ko.wikipedia.org/wiki/PA-7200 "wikilink")            | 1994 | 120         | 960             | 0.55      | 1.26           | 210           | 30          | 1024       | 2048       | —            | 1.1c |       |
| PCX-L    | [PA-7100LC](https://ko.wikipedia.org/wiki/PA-7100LC "wikilink")        | 1994 | 60–100      | ?               | 0.75      | 0.9            | 201.6         | 7–11        | —          | 1          | 2            | 1.1d |       |
| PCX-L2   | [PA-7300LC](https://ko.wikipedia.org/wiki/PA-7300LC "wikilink")        | 1996 | 132–180     | ?               | 0.5       | 9.2            | 260.1         | ?           | 64         | 64         | 0–8          | 1.1e |       |
| PCX-U    | [PA-8000](https://ko.wikipedia.org/wiki/PA-8000 "wikilink")            | 1996 | 160–180     | 960             | 0.5       | 3.8            | 337.68        | ?           | 1024       | 1024       | —            | 2.0  |       |
| PCX-U+   | [PA-8200](https://ko.wikipedia.org/wiki/PA-8000#PA-8200 "wikilink")    | 1997 | 200–240     | 960             | 0.5       | 3.8            | 337.68        | ?           | 2048       | 2048       | —            | 2.0  |       |
| PCX-W    | [PA-8500](https://ko.wikipedia.org/wiki/PA-8000#PA-8500 "wikilink")    | 1998 | 300–440     | 1920            | 0.25      | 140            | 467           | ?           | 1024       | 512        | —            | 2.0  | \[8\] |
| PCX-W+   | [PA-8600](https://ko.wikipedia.org/wiki/PA-8000#PA-8600 "wikilink")    | 2000 | 360–550     | 1920            | 0.25      | 140            | 467           | ?           | 1024       | 512        | —            | 2.0  | \[9\] |
| PCX-W2   | [PA-8700](https://ko.wikipedia.org/wiki/PA-8000#PA-8700 "wikilink")(+) | 2001 | 625–875     | 1920            | 0.18      | 186            | 304           | \<7.1@1.5 V | 1536       | 768        | —            | 2.0  |       |
| Mako     | [PA-8800](https://ko.wikipedia.org/wiki/PA-8800#PA-8800 "wikilink")    | 2003 | 800–1000    | 6400            | 0.13      | 300            | 361           | ?           | 768/코어     | 768/코어     | 0 또는 32      | 2.0  |       |
| Shortfin | [PA-8900](https://ko.wikipedia.org/wiki/PA-8000#PA-8900 "wikilink")    | 2005 | 800–1100    | 6400            | 0.13      | ?              | ?             | ?           | 768/코어     | 768/코어     | 64           | 2.0  |       |

## 각주

<references />

## 외부 링크

  - [LostCircuits](https://web.archive.org/web/20120219071600/http://www.lostcircuits.com/mambo//index.php?option=com_content&task=view&id=42&Itemid=42) Hewlett Packard PA8800 Risc Processor overview.

  - [HP's documentation](https://web.archive.org/web/20150421181801/http://h21007.www2.hp.com/portal/site/dspp/menuitem.1b39e60a9475acc915b49c108973a801?chid=6dc55e210a66a010VgnVCM100000275d6e10RCRD) - page down for PA-RISC, Architecture PDFs available.

  - [OpenPA.net](http://www.openpa.net/) Comprehensive PA-RISC chip and computer information.

  - [chipdb.org](http://www.chipdb.org/cat-pa-risc-592.htm) Images of different PA-RISC processors

[분류:HP의 마이크로프로세서](https://ko.wikipedia.org/wiki/분류:HP의_마이크로프로세서 "wikilink") [분류:컴퓨터 구조](https://ko.wikipedia.org/wiki/분류:컴퓨터_구조 "wikilink") [분류:명령어 집합 구조](https://ko.wikipedia.org/wiki/분류:명령어_집합_구조 "wikilink")

1.  "One Year Ago". (26 February 1987). *Computer Business Review*.
2.  Hewlett-Packard Company (September 1987). *Hewlett-Packard Journal* **38** (9): p. 3.
3.  [HP Completes Its PA-RISC Road Map With Final Processor Upgrade - PA-RISC Processor](http://www.informationweek.com/story/showArticle.jhtml?articleID=164302278)
4.  [How long will HP continue to support HP 9000 systems?](http://www.hp.com/products1/evolution/9000/faqs.html#2)
5.  Marston, A. et al. (1987). "A 32b CMOS single-chip RISC type processor". *ISSCC Digest of Technical Papers*. pp. 28–29.
6.  Yetter, J. et al. (1987). "A 15 MIPS 32b Microprocessor". *ISSCC Digest of Technical Papers*.
7.  Boschma, Brian D. et al. (1989). "A 30 MIPS VLSI CPU". *ISSCC Digest of Technical Papers*. pp. 82–83, 299
8.  ["HP L1000 & L2000 (rp5400/rp5450) Servers"](http://www.openpa.net/systems/hp_l1000_l2000-rp5400_rp5450.html), *openpa.net*
9.