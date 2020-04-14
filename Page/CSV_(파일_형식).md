> This article is converted from Wikipedia: [CSV \(파일 형식\)](https://ko.wikipedia.org/wiki/CSV_\(파일_형식\)).


**CSV**()는 몇 가지 필드를 [쉼표](../Page/쉼표_\(문장_부호\).md "wikilink")(,)로 구분한 [텍스트](https://ko.wikipedia.org/wiki/텍스트 "wikilink") 데이터 및 텍스트 파일이다. 확장자는 .csv이며 [MIME 형식은](../Page/MIME.md "wikilink") text/csv이다. **comma-separated variables**라고도 한다.

오래전부터 [스프레드시트](../Page/스프레드시트.md "wikilink")나 [데이터베이스](../Page/데이터베이스.md "wikilink") 소프트웨어에서 많이 쓰였으나 세부적인 [구현](../Page/구현.md "wikilink")은 소프트웨어에 따라 다르다. 그것들을 추가한 형태가 2005년 10월 RFC 4180에서 Informational([IESG](https://ko.wikipedia.org/wiki/IESG "wikilink")의 외부에서 결정된 유용한 정보의 제공)로 사양이 문서화됐다.

비슷한 포맷으로는 탭으로 구분하는 'tab-separated values'(TSV)나, 반각 스페이스로 구분하는 'space-separated values'(SSV) 등이 있으며, 이것들을 합쳐서 character-separated values (CSV), delimiter-separated values라고 부르는 경우가 많다.

## 사양

RFC 4180 은 CSV 포맷을 위한 사양을 제안하며 이것이 흔히 사용되는 정의이다. 그러나 대중적으로 사용되는 "CSV"는 하나의 잘 정의된 형식은 아니다. 그러므로 "CSV"는 실질적으로 다음을 가리키는 어느 파일이 될 수 있다:

1.  [ASCII](https://ko.wikipedia.org/wiki/ASCII "wikilink"), 다양한 [유니코드](../Page/유니코드.md "wikilink") 문자 집합(예: [UTF-8](../Page/UTF-8.md "wikilink")), [EBCDIC](https://ko.wikipedia.org/wiki/EBCDIC "wikilink"), [Shift JIS와](../Page/Shift_JIS.md "wikilink") 같은 문자 집합을 사용하는 [플레인 텍스트](../Page/플레인_텍스트.md "wikilink")
2.  [레코드](https://ko.wikipedia.org/wiki/레코드 "wikilink")로 이루어져 있음 (줄 당 하나의 레코드인 것이 보통)
3.  여러 개의 필드로 나누니 레코드. [구분 문자](../Page/구분_문자.md "wikilink")(일반적으로 쉼표, 세미콜론, 탭과 같은 하나의 예비 문자. 가끔 선택적 스페이스를 포함할 수 있음.)로 구별.
4.  모든 레코드가 동일한 시퀀스의 필드를 가진다

## 역사

CSV는 개인용 컴퓨터 역사 중 10년 이상의 역사를 지닌 데이터 포맷의 하나이다. 1972년에 CSV를 지원한 [OS/360](https://ko.wikipedia.org/wiki/OS/360 "wikilink")용 [IBM 포트란](../Page/IBM.md "wikilink")(레벨 H 확장) 컴파일러를 예로 들 수 있다.\[1\]

## 사용처

CSV는 흔히 사용되고, 비교적 단순한 파일 포맷이며, 소비자들(consumer)과 업무(business), 그리고 과학 애플리케이션에서 널리 사용되고 있다. 이것을 가장 흔히 사용하는 방법 중 하나는 호환되지 않는 포맷을 사용하는 프로그램 끼리 자료를 전달할 때 사용한다. 이렇게 사용하는 이유는 많은 프로그램들이 포맷을 내보내거나 가져올 때 조금 변형된 형태의 CSV을 지원하기 때문이다.

## 예

<table>
<thead>
<tr class="header">
<th><p>연도</p></th>
<th><p>제조사</p></th>
<th><p>모델</p></th>
<th><p>설명</p></th>
<th><p>가격</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1997</p></td>
<td><p>Ford</p></td>
<td><p>E350</p></td>
<td><p>ac, abs, moon</p></td>
<td><p>3000.00</p></td>
</tr>
<tr class="even">
<td><p>1999</p></td>
<td><p>Chevy</p></td>
<td><p>Venture "Extended Edition"</p></td>
<td></td>
<td><p>4900.00</p></td>
</tr>
<tr class="odd">
<td><p>1999</p></td>
<td><p>Chevy</p></td>
<td><p>Venture "Extended Edition, Very Large"</p></td>
<td></td>
<td><p>5000.00</p></td>
</tr>
<tr class="even">
<td><p>1996</p></td>
<td><p>Jeep</p></td>
<td><p>Grand Cherokee</p></td>
<td><p>MUST SELL!<br />
air, moon roof, loaded</p></td>
<td><p>4799.00</p></td>
</tr>
</tbody>
</table>

위의 데이터 표는 다음과 같이 CSV 형식으로 표현할 수 있다:

`연도,제조사,모델,설명,가격`
`1997,Ford,E350,"ac, abs, moon",3000.00`
`1999,Chevy,"Venture ""Extended Edition""","",4900.00`
`1999,Chevy,"Venture ""Extended Edition, Very Large""",,5000.00`
`1996,Jeep,Grand Cherokee,"MUST SELL!`
`air, moon roof, loaded",4799.00`

## 각주

[분류:데이터베이스](https://ko.wikipedia.org/wiki/분류:데이터베이스 "wikilink") [분류:파일 포맷](https://ko.wikipedia.org/wiki/분류:파일_포맷 "wikilink") [분류:데이터 직렬화 포맷](https://ko.wikipedia.org/wiki/분류:데이터_직렬화_포맷 "wikilink") [분류:오픈 포맷](https://ko.wikipedia.org/wiki/분류:오픈_포맷 "wikilink")

1.