> This article is converted from Wikipedia: [C 문자열 처리](https://ko.wikipedia.org/wiki/C_문자열_처리).


C 프로그래밍 언어는 [표준 라이브러리에](../Page/표준_라이브러리.md "wikilink") [문자열](https://ko.wikipedia.org/wiki/문자열 "wikilink") 관련 명령을 구현하는 여러 함수들이 존재한다. 복사, [결합](https://ko.wikipedia.org/wiki/문자열_결합 "wikilink"), [토큰화](../Page/낱말_분석.md "wikilink"), 검색과 같은 다양한 명령이 지원된다. 문자열의 경우 표준 라이브러리는 문자열이 [널 종단된다는](../Page/널_종단_문자열.md "wikilink") 규칙을 사용한다: n개의 문자의 문자열은 n + 1 요소의 [배열](../Page/배열.md "wikilink")로 표현되며, 끝은 "NUL" 문자로 끝난다.

## 함수 개요

**string.h**는 [C 언어의](https://ko.wikipedia.org/wiki/C_언어 "wikilink") [표준 라이브러리로](../Page/C_표준_라이브러리.md "wikilink"), [메모리 블록이나](https://ko.wikipedia.org/wiki/메모리_블록 "wikilink") [문자열을](https://ko.wikipedia.org/wiki/C_문자열 "wikilink") 다룰 수 있는 함수들을 포함하고 있다. 유니코드 문자열을 다루려면 [wchar.h](https://ko.wikipedia.org/wiki/wchar.h "wikilink")를 사용한다.

<table>
<thead>
<tr class="header">
<th><p>함수</p></th>
<th><p>설명</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>복사</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>void * <strong>memcpy</strong> ( void * destination, const void * source, size_t num );</p></td>
<td><p>source가 가리키는 곳 부터 num바이트 만큼을 destination이 가리키는 곳에 복사한다.</p></td>
</tr>
<tr class="odd">
<td><p>void * <strong>memmove</strong> ( void * destination, const void * source, size_t num );</p></td>
<td><p>source가 가리키는 곳 부터 num바이트 만큼을 destination이 가리키는 곳으로 옮긴다.</p></td>
</tr>
<tr class="even">
<td><p>char * <strong>strcpy</strong> ( char * destination, const char * source );</p></td>
<td><p>source를 destination에 복사한다.</p></td>
</tr>
<tr class="odd">
<td><p>char * <strong>strncpy</strong> ( char * destination, const char * source, size_t num );</p></td>
<td><p>source에서 destination으로 처음 num개의 문자들을 복사한다.</p></td>
</tr>
<tr class="even">
<td><p>병합</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>char * <strong>strcat</strong> ( char * destination, const char * source );</p></td>
<td><p>source를 destination뒤에 붙인다.</p></td>
</tr>
<tr class="even">
<td><p>char * <strong>strncat</strong> ( char * destination, char * source, size_t num );</p></td>
<td><p>source에서 destination뒤에 처음 num개의 문자들을 붙인다.</p></td>
</tr>
<tr class="odd">
<td><p>비교</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>int <strong>memcmp</strong> ( const void * ptr1, const void * ptr2, size_t num );</p></td>
<td><p>ptr1이 가리키는 처음 num바이트의 데이터와 ptr2가 가리키는 처음 num바이트의 데이터를 비교한다.</p></td>
</tr>
<tr class="odd">
<td><p>int <strong>strcmp</strong> ( const char * str1, const char * str2 );</p></td>
<td><p>str1과 str2를 비교한다.</p></td>
</tr>
<tr class="even">
<td><p>int <strong>strcoll</strong> ( const char * str1, const char * str2 );</p></td>
<td><p>strcmp와 비슷하지만 LC_COLLATE에 정의되어 있는 방식에 따라 해석 된 후 비교한다.</p></td>
</tr>
<tr class="odd">
<td><p>int <strong>strncmp</strong> ( const char * str1, const char * str2, size_t num );</p></td>
<td><p>str1의 처음 num개의 문자를 str2의 처음 num개의 문자와 비교한다.</p></td>
</tr>
<tr class="even">
<td><p>size_t <strong>strxfrm</strong> ( char * destination, const char * source, size_t num );</p></td>
<td><p>source를 현재 지역 정보에 따라 문자열을 변환한 후 변환한 문자열의 처음 num개 문자를 destination에 복사한다.</p></td>
</tr>
<tr class="odd">
<td><p>탐색</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>void * <strong>memchr</strong> ( const void * ptr, int value, size_t num );</p></td>
<td><p>ptr이 가리키는 메모리의 처음 num바이트 중에서 처음으로 value와 일치하는 값(문자)의 주소를 반환한다.</p></td>
</tr>
<tr class="odd">
<td><p>char * <strong>strchr</strong> ( const char * str, int character );</p></td>
<td><p>str에서 처음으로 character와 일치하는 문자의 주소를 반환한다.</p></td>
</tr>
<tr class="even">
<td><p>size_t <strong>strcspn</strong> ( const char * str1, const char * str2 );</p></td>
<td><p>str1에서 str2의 문자들을 찾아 일치하는 문자의 처음 위치를 알려줍니다. (예)</p>
<p>char str[]="abcdefgh";</p>
<p>int idx;</p>
<p>idx=strcspn(str, "cd"); // idx=2 str[2]='c'</p>
<p>idx=strcspn(str, "fd"); // idx=3 str[3]='d'</p>
<p>idx=strcspn(str, "ecib"); // idx=1 str[1]='b'</p></td>
</tr>
<tr class="odd">
<td><p>char * <strong><a href="https://ko.wikipedia.org/wiki/strpbrk" title="wikilink">strpbrk</a></strong> ( const char * str1, const char * str2 );</p></td>
<td><p>str1에서 str2에 들어 있는 문자들을 찾아 str2의 문자들 중 str1의 문자들과 첫 번째로 일치하는 문자의 주소를 반환한다.</p></td>
</tr>
<tr class="even">
<td><p>char * <strong>strrchr</strong> ( const char * str, int character );</p></td>
<td><p>str에서 마지막으로 character와 일치하는 문자의 주소를 반환한다.</p></td>
</tr>
<tr class="odd">
<td><p>size_t <strong><a href="https://ko.wikipedia.org/wiki/strspn" title="wikilink">strspn</a></strong> ( const char * str1, const char * str2 );</p></td>
<td><p>str1에서 str2의 문자들이 아닌 문자의 처음 위치를 알려줍니다.</p>
<p>(예)</p>
<p>char str[]="abcdefgh";</p>
<p>int idx;</p>
<p>idx=strspn(str, "a"); // idx=1 str[1]='b'</p>
<p>idx=strspn(str, "abd"); // idx=2 str[2]='c'</p>
<p>idx=strspn(str, "cbae"); // idx=3 str[3]='d'</p></td>
</tr>
<tr class="even">
<td><p>char * <strong>strstr</strong> ( const char * str1, const char * str2 );</p></td>
<td><p>str1에서 str2를 검색하여 가장 먼저 나타나는 곳의 위치를 반환한다.</p></td>
</tr>
<tr class="odd">
<td><p>char * <strong><a href="https://ko.wikipedia.org/wiki/strtok" title="wikilink">strtok</a></strong> ( char * str, const char * delimiters );</p></td>
<td><p>str을 delimiters의 문자들로 분리한다.(원본 문자열 변경)</p>
<p>해당 함수를 사용하면 원본문자열의 delimeters에 해당하는 문자가 NULL로 변경되니 주의해야 한다(원본을 유지하려면 복사본으로 해당 함수를 사용해야 한다)</p>
<p>strtok() 함수는 찾는 문자열의 시작위치를 내부에서 static으로 관리하고 1번째 인자가 문자열이면 해당 문자열의 처음 위치로 설정하고 NULL이면 찾은 delimiters의 다음 위치가 설정된다</p>
<p>분리하는 도중에 다른 문자열을 분리하기 위해 해당 함수를 또 사용하면 이미 설정된 문자열의 찾는 위치가 변경되어 원하는 결과를 얻지 못한다(thread-unsafe)</p>
<p>strtok_r()을 사용하면 찾는 위치를 주어진 변수로 관리하기에 위의 문제가 없다</p>
<p>(예)</p>
<p>char str[]="12&amp;345&amp;789";</p>
<p>char *p, *s;</p>
<p>for(p=str;s=strtok(p,"&amp;");p=NULL) printf("%s\n",s);</p>
<p>[결과]</p>
<p>12</p>
<p>345</p>
<p>789</p></td>
</tr>
<tr class="even">
<td><p>char *<strong>strtok_r</strong>(char *str, const char *delim, char **pos);</p></td>
<td><p>문자열 str을 주어진 delim문자들로 분리한다(원본문자열 변경)</p>
<p>기능은 strtok()과 동일하며 다른 점은 주어진 3번째 인자로 찾는 위치를 관리하므로 중복 사용해도 문제가 없다(thread-safe)</p>
<p>(예)</p>
<p>char str[]="12&amp;&amp;345&amp;789";</p>
<p>char *p, *s, *pos;</p>
<p>for(p=str;s=strtok_r(p,"&amp;", &amp;pos);p=NULL) printf("%s\n",s);</p>
<p>[결과]</p>
<p>12</p>
<p>345</p>
<p>789</p></td>
</tr>
<tr class="odd">
<td><p>char *<strong>strsep</strong>(char **str, const char *delim);</p></td>
<td><p>문자열 str을 delim 문자들로 분리한다(원본문자열 변경)</p>
<p>strtok()과 다른 점은 1번째 인자가 포인터의 주소를 넘기는 부분과 delim 문자들로 분리 시 delim 문자가 처음이나 마지막 또는 연속될 경우 strtok()은 무시를 하지만 이 함수는 "" 값으로 분리를 한다</p>
<p>또한 strtok()은 1번째인자를 처음은 해당문자열로 설정하고 2번째 부터는 NULL로 설정하여 분리를 하지만 strsep() 함수는 NULL로 설정할 필요가 없다</p>
<p>(예)</p>
<p>char str[]="&amp;12&amp;&amp;345&amp;789&amp;";</p>
<p>char *p, *s;</p>
<p>for(p=str;s=strsep(&amp;p,"&amp;");) printf("&lt;%s&gt;\n",s);</p>
<p>[결과]</p>
<p>&lt;&gt;</p>
<p>&lt;12&gt;</p>
<p>&lt;&gt;</p>
<p>&lt;345&gt;</p>
<p>&lt;789&gt;</p>
<p>&lt;&gt;</p></td>
</tr>
<tr class="even">
<td><p>기타</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>void * <strong>memset</strong> ( void * ptr, int value, size_t num );</p></td>
<td><p>ptr이 가리키는 메모리의 처음 num바이트를 value값(문자)으로 채운다.</p></td>
</tr>
<tr class="even">
<td><p>char * <strong>strerror</strong> ( int errnum );</p></td>
<td><p>errnum(보통 errno)을 해석한 뒤 그에 해당하는 에러 문자열의 포인터를 반환한다.</p></td>
</tr>
<tr class="odd">
<td><p>size_t <strong><a href="https://ko.wikipedia.org/wiki/strlen" title="wikilink">strlen</a></strong> ( const char * str );</p></td>
<td><p>str의 길이를 반환한다.</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
</tr>
</tbody>
</table>

## 변수 · 상수 · 형식

| 이름      | 설명                                                        |
| ------- | --------------------------------------------------------- |
| 상수      |                                                           |
| NULL    | 널 포인터의 약어인 상수. 이 상수는 메모리의 어떤 유효한 위치의 개체도 가리키지 않는 포인터 값이다. |
| 형식 정의   |                                                           |
| size_t | sizeof 연산자의 결과값을 나타내는 정수(unsigned int)이다.                 |
|         |                                                           |

## 예제

다음 예제는 Hello World 문자열의 길이를 구해 출력한다. 결과는 11이 출력될 것이다.

``` c
#include <stdio.h>
#include <string.h>

int main()
{
    char *string = "Hello World";

    printf("%lu\n", (unsigned long)strlen(string));

    return 0;
}
```

## 외부 링크

  - [Fast memcpy in C](http://www.danielvik.com/2010/02/fast-memcpy-in-c.html), multiple C coding examples to target different types of CPU instruction architectures

[분류:C 표준 라이브러리 헤더](https://ko.wikipedia.org/wiki/분류:C_표준_라이브러리_헤더 "wikilink") [분류:문자열](https://ko.wikipedia.org/wiki/분류:문자열 "wikilink")