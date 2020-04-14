> This article is converted from Wikipedia: [MSI 프로토콜](https://ko.wikipedia.org/wiki/MSI_프로토콜).


**MSI 프로토콜**(MSI protocol)은 [멀티프로세서](https://ko.wikipedia.org/wiki/멀티프로세서 "wikilink") 시스템에서 사용되는 기초적인 [캐시 일관성](../Page/캐시_일관성.md "wikilink") [프로토콜](https://ko.wikipedia.org/wiki/프로토콜 "wikilink")이다. MSI 프로토콜은 메모리가 가질 수 있는 세 가지의 캐시 상태를 정의하며, MSI라는 이름은 캐시 상태의 이니셜에서 따온 것이다. MSI에서 메모리 블록이 가지는 상태는 다음과 같다.

  - **M**odified: 블록이 캐시에서 수정된 상태이다. 메모리는 수정되지 않았으며 캐시만 수정되었기 때문에 캐시와 메모리는 다른 데이터를 가지고 있다. 이러한 캐시 블록을 캐시에서 내보낼 때(evict) 메모리에 그 변경된 내용을 반영해야 한다.
  - **S**hared: 블록이 캐시로 공유된 상태이다. 캐시와 메모리의 상태가 동일하기 때문에 해당 블록을 캐시에서 내보낼 때 메모리에 쓰기 작업을 할 필요가 없다.
  - **I**nvalid: 블록이 유효하지 않은 상태이다. 해당 블록의 내용을 캐시로 올리기 위해서는 메모리나 다른 캐시에서 갱신된 내용을 확인할 필요가 있다.

프로그램이 M 상태나 S 상태에 있는 블록을 읽으려고 하는 경우에는 별다른 조치 없이 캐시에서 읽을 수 있다. 만약 I 상태의 메모리 블록을 읽으려고 하는 경우에는 다른 캐시에서 그 메모리를 M 상태로 가지고 있는지를 확인하며, 그에 따른 갱신 작업이 추가적으로 이루어진다.

<table>
<thead>
<tr class="header">
<th></th>
<th><p> M </p></th>
<th><p> S </p></th>
<th><p> I </p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p> M </p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p> S </p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p> I </p></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## 유사한 프로토콜

MSI 프로토콜에 다른 상태를 가지는 확장 프로토콜이 여럿 존재한다. 대표적으로 "Exclusive" 상태를 추가한 [MESI 프로토콜과](https://ko.wikipedia.org/wiki/MESI_프로토콜 "wikilink") "Owned" 상태를 가지는 [MOSI 프로토콜](https://ko.wikipedia.org/wiki/MOSI_프로토콜 "wikilink") 그리고 이 두 상태를 모두 추가한 [MOESI 프로토콜이](https://ko.wikipedia.org/wiki/MOESI_프로토콜 "wikilink") 있다.

## 관련 문서

  - [캐시 일관성](../Page/캐시_일관성.md "wikilink")
  - [MESI 프로토콜](https://ko.wikipedia.org/wiki/MESI_프로토콜 "wikilink")
  - [MOSI 프로토콜](https://ko.wikipedia.org/wiki/MOSI_프로토콜 "wikilink")
  - [MOESI 프로토콜](https://ko.wikipedia.org/wiki/MOESI_프로토콜 "wikilink")

[분류:캐시 일관성](https://ko.wikipedia.org/wiki/분류:캐시_일관성 "wikilink")