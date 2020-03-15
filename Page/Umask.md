> This article is converted from Wikipedia: [Umask](https://ko.wikipedia.org/wiki/Umask).


**umask**는 컴퓨팅에서 새로 만들어진 파일에 [파일 권한을](https://ko.wikipedia.org/wiki/파일_권한 "wikilink") 어떻게 설정할지를 제어하는 [마스크](https://ko.wikipedia.org/wiki/마스크_\(컴퓨팅\) "wikilink") 설정을 결정하는 명령어이다.

## 역사

mask, umask 명령어와 umask 함수는 원래 유닉스의 구현체의 일부가 아니었다. 해당 운영 체제는 상대적으로 크기가 작은 컴퓨터 중심 환경에서 발전하였으므로 보안은 그다지 문제가 아니었다. 이후 각기 다른 단체의 수백 명의 사용자들로 성장해갔다. 처음에 개발자들은 주요 파일들의 생성 모드를 특히 실제 보안 위반에 대해 더 제한적으로 만들었으나 이는 일반적인 해결책이 아니었다. mask와 umask 명령어는 1978년 즈음 운영 체제의 7\~9판 사이에 도입되었으므로 사이트, 그룹, 개인이 자신들의 기본값을 선택할 수 있게 되었다.\[1\]

## 셸 명령어

<table>
<caption>umask 명령어의 8진법 표기 비교</caption>
<thead>
<tr class="header">
<th><p>umask 명령어의<br />
8진법 숫자 </p></th>
<th><p> 마스크의 <br />
이진값</p></th>
<th><p> 마스크의 <br />
부정</p></th>
<th><p>논리 AND<br />
 ("rwx" 요청)[2] </p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>0</p></td>
<td><p>000</p></td>
<td><p>111</p></td>
<td><p>rwx</p></td>
</tr>
<tr class="even">
<td><p>1</p></td>
<td><p>001</p></td>
<td><p>110</p></td>
<td><p>rw-</p></td>
</tr>
<tr class="odd">
<td><p>2</p></td>
<td><p>010</p></td>
<td><p>101</p></td>
<td><p>r-x</p></td>
</tr>
<tr class="even">
<td><p>3</p></td>
<td><p>011</p></td>
<td><p>100</p></td>
<td><p>r--</p></td>
</tr>
<tr class="odd">
<td><p>4</p></td>
<td><p>100</p></td>
<td><p>011</p></td>
<td><p>-wx</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>101</p></td>
<td><p>010</p></td>
<td><p>-w-</p></td>
</tr>
<tr class="odd">
<td><p>6</p></td>
<td><p>110</p></td>
<td><p>001</p></td>
<td><p>--x</p></td>
</tr>
<tr class="even">
<td><p>7</p></td>
<td><p>111</p></td>
<td><p>000</p></td>
<td><p>---</p></td>
</tr>
</tbody>
</table>

셸에서 마스크는 umask 명령어를 사용하여 설정할 수 있다. 명령어 문법은 다음과 같다:\[3\]

``` bash
umask [-S ] [maskExpression]
```

(대괄호 안의 항목들을 선택사항이다.)

### 현재의 마스크 표시하기

umask 명령어에 어떠한 인자도 지정하지 않고 실행하면 현재의 마스크를 표시한다. 출력은 운영 체제에 따라 [8진법](https://ko.wikipedia.org/wiki/파일_권한 "wikilink") 또는 [심볼릭으로](https://ko.wikipedia.org/wiki/파일_권한 "wikilink") 표시된다.\[4\] **-S** 인자(예: umask -S)는 umask를 강제로 symbolic 표기를 사용하여 표시한다. 이를테면:

``` bash
$ umask         # 현재 값 표시 (8진법)
0022
$ umask -S      # 현재 값을 symbolic으로 표시
u=rwx,g=rx,o=rx
```

## 같이 보기

  - [파일 시스템 권한](../Page/파일_시스템_권한.md "wikilink")

## 각주

[분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink")

1.
2.  **Note:** Operating systems usually will also strip off execute permissions on newly created files.
3.
4.