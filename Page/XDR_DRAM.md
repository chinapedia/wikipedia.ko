> This article is converted from Wikipedia: [XDR DRAM](https://ko.wikipedia.org/wiki/XDR_DRAM).


[섬네일](https://ko.wikipedia.org/wiki/파일:XDRAM.jpg "wikilink") **XDR DRAM**(extreme data rate dynamic random-access memory)은 [램버스](https://ko.wikipedia.org/wiki/램버스 "wikilink") [RDRAM](../Page/RDRAM.md "wikilink")의 뒤를 잇는 고성능 [램](https://ko.wikipedia.org/wiki/램 "wikilink") 인터페이스이다. [DDR2 SDRAM과](../Page/DDR2_SDRAM.md "wikilink") [GDDR4](../Page/GDDR4.md "wikilink") 기술과 경쟁한다. [소니](../Page/소니.md "wikilink")의 게임 콘솔 [PS3에](../Page/플레이스테이션_3.md "wikilink") 쓰인 램이다.

## 프로토콜

<table>
<caption>XDR DRAM 요청 패킷 포맷[1]</caption>
<thead>
<tr class="header">
<th><p>클럭<br />
에지</p></th>
<th><p>비트</p></th>
<th></th>
<th><p>NOP</p></th>
<th></th>
<th><p>컬럼 읽기/쓰기</p></th>
<th></th>
<th><p>캘리브레이트/파워 다운</p></th>
<th></th>
<th><p>프리차지/리프레시</p></th>
<th></th>
<th><p>로우 액티베이트</p></th>
<th></th>
<th><p>마스크 화이트</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>비트</p></td>
<td><p>비트</p></td>
<td><p>설명</p></td>
<td><p>비트</p></td>
<td><p>설명</p></td>
<td><p>비트</p></td>
<td><p>설명</p></td>
<td><p>비트</p></td>
<td><p>설명</p></td>
<td><p>비트</p></td>
<td><p>설명</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>↓</p></td>
<td><p>RQ11</p></td>
<td><p>0</p></td>
<td><p>0</p></td>
<td><p>COL opcode</p></td>
<td><p>0</p></td>
<td><p>COLX opcode</p></td>
<td><p>0</p></td>
<td><p>ROWP opcode</p></td>
<td><p>0</p></td>
<td><p>ROWA opcode</p></td>
<td><p>1</p></td>
<td><p>COLM opcode</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>↓</p></td>
<td><p>RQ10</p></td>
<td><p>0</p></td>
<td><p>0</p></td>
<td><p>0</p></td>
<td><p>0</p></td>
<td><p>1</p></td>
<td><p>M3</p></td>
<td><p>Write mask<br />
low bits</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>↓</p></td>
<td><p>RQ9</p></td>
<td><p>0</p></td>
<td><p>0</p></td>
<td><p>1</p></td>
<td><p>1</p></td>
<td><p>R9</p></td>
<td><p>Row address<br />
high bits</p></td>
<td><p>M2</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>↓</p></td>
<td><p>RQ8</p></td>
<td><p>0</p></td>
<td><p>1</p></td>
<td><p>0</p></td>
<td><p>1</p></td>
<td><p>R10</p></td>
<td><p>M1</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>↓</p></td>
<td><p>RQ7</p></td>
<td><p>x</p></td>
<td><p>WRX</p></td>
<td><p>Write/Read bit</p></td>
<td><p>x</p></td>
<td><p>예비</p></td>
<td><p>POP1</p></td>
<td><p>Precharge delay (0–3)</p></td>
<td><p>R11</p></td>
<td><p>M0</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>↓</p></td>
<td><p>RQ6</p></td>
<td><p>x</p></td>
<td><p>C8</p></td>
<td><p>Column address<br />
high bits</p></td>
<td><p>x</p></td>
<td><p>POP0</p></td>
<td><p>R12</p></td>
<td><p>예비</p></td>
<td><p>C8</p></td>
<td><p>Column address<br />
high bits</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>↓</p></td>
<td><p>RQ5</p></td>
<td><p>x</p></td>
<td><p>C9</p></td>
<td><p>x</p></td>
<td><p>x</p></td>
<td><p>예비</p></td>
<td><p>R13</p></td>
<td><p>C9</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>↓</p></td>
<td><p>RQ4</p></td>
<td><p>x</p></td>
<td><p>C10</p></td>
<td><p>예비</p></td>
<td><p>x</p></td>
<td><p>x</p></td>
<td><p>R14</p></td>
<td><p>C10</p></td>
<td><p>예비</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>↓</p></td>
<td><p>RQ3</p></td>
<td><p>x</p></td>
<td><p>C11</p></td>
<td><p>XOP3</p></td>
<td><p>Subopcode</p></td>
<td><p>x</p></td>
<td><p>R15</p></td>
<td><p>C11</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>↓</p></td>
<td><p>RQ2</p></td>
<td><p>x</p></td>
<td><p>BC2</p></td>
<td><p>Bank address</p></td>
<td><p>XOP2</p></td>
<td><p>BP2</p></td>
<td><p>Precharge bank</p></td>
<td><p>BA2</p></td>
<td><p>Bank address</p></td>
<td><p>BC2</p></td>
<td><p>Bank address</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>↓</p></td>
<td><p>RQ1</p></td>
<td><p>x</p></td>
<td><p>BC1</p></td>
<td><p>XOP1</p></td>
<td><p>BP1</p></td>
<td><p>BA1</p></td>
<td><p>BC1</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>↓</p></td>
<td><p>RQ0</p></td>
<td><p>x</p></td>
<td><p>BC0</p></td>
<td><p>XOP0</p></td>
<td><p>BP0</p></td>
<td><p>BA0</p></td>
<td><p>BC0</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>↑</p></td>
<td><p>RQ11</p></td>
<td><p>x</p></td>
<td><p>DELC</p></td>
<td><p>Command delay (0–1)</p></td>
<td><p>x</p></td>
<td><p>예비</p></td>
<td><p>POP2</p></td>
<td><p>Precharge enable</p></td>
<td><p>DELA</p></td>
<td><p>Command delay (0–1)</p></td>
<td><p>M7</p></td>
<td><p>Write mask<br />
high bits</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>↑</p></td>
<td><p>RQ10</p></td>
<td><p>x</p></td>
<td><p>x</p></td>
<td><p>예비</p></td>
<td><p>x</p></td>
<td><p>ROP2</p></td>
<td><p>Refresh command</p></td>
<td><p>R8</p></td>
<td><p>Row address<br />
low bits</p></td>
<td><p>M6</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>↑</p></td>
<td><p>RQ9</p></td>
<td><p>x</p></td>
<td><p>x</p></td>
<td><p>x</p></td>
<td><p>ROP1</p></td>
<td><p>R7</p></td>
<td><p>M5</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>↑</p></td>
<td><p>RQ8</p></td>
<td><p>x</p></td>
<td><p>x</p></td>
<td><p>x</p></td>
<td><p>ROP0</p></td>
<td><p>R6</p></td>
<td><p>M4</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>↑</p></td>
<td><p>RQ7</p></td>
<td><p>x</p></td>
<td><p>C7</p></td>
<td><p>Column address<br />
low bits</p></td>
<td><p>x</p></td>
<td><p>DELR1</p></td>
<td><p>Refresh delay (0–3)</p></td>
<td><p>R5</p></td>
<td><p>C7</p></td>
<td><p>Column address<br />
low bits</p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>↑</p></td>
<td><p>RQ6</p></td>
<td><p>x</p></td>
<td><p>C6</p></td>
<td><p>x</p></td>
<td><p>DELR0</p></td>
<td><p>R4</p></td>
<td><p>C6</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>↑</p></td>
<td><p>RQ5</p></td>
<td><p>x</p></td>
<td><p>C5</p></td>
<td><p>x</p></td>
<td><p>x</p></td>
<td><p>예비</p></td>
<td><p>R3</p></td>
<td><p>C5</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>↑</p></td>
<td><p>RQ4</p></td>
<td><p>x</p></td>
<td><p>C4</p></td>
<td><p>x</p></td>
<td><p>x</p></td>
<td><p>R2</p></td>
<td><p>C4</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>↑</p></td>
<td><p>RQ3</p></td>
<td><p>x</p></td>
<td><p>SC3</p></td>
<td><p>Sub-column address</p></td>
<td><p>x</p></td>
<td><p>x</p></td>
<td><p>R1</p></td>
<td><p>SC3</p></td>
<td><p>Sub-column address</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>↑</p></td>
<td><p>RQ2</p></td>
<td><p>x</p></td>
<td><p>SC2</p></td>
<td><p>x</p></td>
<td><p>BR2</p></td>
<td><p>Refresh bank</p></td>
<td><p>R0</p></td>
<td><p>SC2</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>↑</p></td>
<td><p>RQ1</p></td>
<td><p>x</p></td>
<td><p>SC1</p></td>
<td><p>x</p></td>
<td><p>BR1</p></td>
<td><p>SR1</p></td>
<td><p>Sub-row address</p></td>
<td><p>SC1</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>↑</p></td>
<td><p>RQ0</p></td>
<td><p>x</p></td>
<td><p>SC0</p></td>
<td><p>x</p></td>
<td><p>BR0</p></td>
<td><p>SR0</p></td>
<td><p>SC0</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## 각주

## 외부 링크

  - [Rambus XDR Product Page](http://www.rambus.com/us/products/xdr_xdr2/index.html)

[분류:컴퓨터 메모리](https://ko.wikipedia.org/wiki/분류:컴퓨터_메모리 "wikilink")

1.  [XDR™ Architecture](http://www.rambus.com/assets/documents/products/dl_0161_v0_8.pdf)  (Rambus)