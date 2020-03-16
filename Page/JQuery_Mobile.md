> This article is converted from Wikipedia: [JQuery Mobile](https://ko.wikipedia.org/wiki/JQuery_Mobile).


**jQuery Mobile**(제이쿼리 모바일)은 [터치에](../Page/터치스크린.md "wikilink") 최적화된 [웹 프레임워크](../Page/웹_프레임워크.md "wikilink")(모바일 프레임워크), 더 구체적으로 말해 [JQuery](../Page/JQuery.md "wikilink") 프로젝트 팀이 개발한 [자바스크립트 라이브러리이다](../Page/자바스크립트_라이브러리.md "wikilink"). 개발은 다양한 [스마트폰](../Page/스마트폰.md "wikilink")과 [태블릿 컴퓨터와](../Page/태블릿_컴퓨터.md "wikilink") [호환되는](https://ko.wikipedia.org/wiki/크로스_브라우저 "wikilink") 프레임워크를 만드는 것에 초점을 두고 있다.\[1\] (성장 중인 다기종 태블릿, 스마트폰 시장에 필수적)\[2\] jQuery Mobile 프레임워크는 다른 모바일 앱 프레임워크\[3\] 및 플랫폼([폰갭](../Page/아파치_코도바.md "wikilink"), Worklight\[4\] 등)과 호환된다.

## 사용예

``` javascript
$('div').on('tap', function(event){
  alert('element tapped ');
});
```

``` javascript
$(document).ready(function(){
    $('.myList li').on('click touchstart', function() {
        $('.myDiv').slideDown('500');
    });
}
```

## 모바일 브라우저 지원

<table>
<thead>
<tr class="header">
<th><p>플랫폼</p></th>
<th><p>버전</p></th>
<th><p>네이티브</p></th>
<th><p>Phone Gap</p></th>
<th><p><a href="../Page/오페라_모바일.md" title="wikilink">오페라 모바일</a></p></th>
<th><p><a href="../Page/오페라_미니.md" title="wikilink">오페라 미니</a></p></th>
<th><p><a href="../Page/파이어폭스_모바일.md" title="wikilink">Fennec</a></p></th>
<th><p>Ozone</p></th>
<th><p>Net front</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>0.9</p></td>
<td><p>8.5, 8.65</p></td>
<td><p>9.5</p></td>
<td><p>10</p></td>
<td><p>4.0</p></td>
<td><p>5.0</p></td>
<td><p>1.0</p></td>
<td><p>1.1*</p></td>
<td><p>0.9</p></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/IOS" title="wikilink">IOS</a></p></td>
<td><p>v2.2.1</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>v3.1.3, v3.2</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><strong>v4-7.0</strong></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/S60" title="wikilink">심비안 S60</a></p></td>
<td><p>v3.1, v3.2</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><strong>v5.0</strong></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/UIQ" title="wikilink">심비안 UIQ</a></p></td>
<td><p>v3.0, v3.1</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><strong>v3.2</strong></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/심비안_OS.md" title="wikilink">Symbian Platform</a></p></td>
<td><p>v.3.0</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/블랙베리_OS.md" title="wikilink">블랙베리 OS</a></p></td>
<td><p>v4.5</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>v4.6, v4.7</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><strong>v5.0</strong></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>v6.0</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/안드로이드_(운영_체제).md" title="wikilink">Android</a></p></td>
<td><p>v1.5, v1.6</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>v2.1</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><strong>v2.2</strong></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/윈도우_모바일.md" title="wikilink">윈도우 모바일</a></p></td>
<td><p>v6.1</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><strong>v6.5.1</strong></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>v7.0</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="../Page/웹OS.md" title="wikilink">웹OS</a></p></td>
<td><p><strong>1.4.1</strong></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/바다_(운영_체제).md" title="wikilink">바다 (운영 체제)</a></p></td>
<td><p><strong>1.0</strong></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/마에모" title="wikilink">마에모</a></p></td>
<td><p><strong>5.0</strong></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/미고_(운영_체제).md" title="wikilink">미고 (운영 체제)</a></p></td>
<td><p>1.1*</p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

**주요 사항:**

  - **** 적어도 미디어 쿼리를 지원하는 브라우저 (jQuery Mobile의 요건). These browsers will be actively tested against, but may not receive the full capabilities of jQuery Mobile.
  - **** 일일 테스트를 보증하기 위해 충분한 시장 점유율을 가지지 못하지만 지원은 하는 브라우저. 이 브라우저를 지원하기 위해 버그 픽스가 여전히 적용된다.
  - **** 미디어 쿼리를 이용할 수 없는 브라우저. They will not be provided any jQuery Mobile scripting or CSS (falling back to plain HTML and simple CSS).
  - \* - 차기 브라우저. 이 브라우저는 아직 지원되지 않으나 알파/베타 테스트 중임.

(출처: jQuery Mobile 웹사이트)\[5\]

## 출시 역사

| 출시일                                                                                                  | 버전 번호              |
| ---------------------------------------------------------------------------------------------------- | ------------------ |
| [October 16 2010](https://blog.jquerymobile.com/2010/10/16/jquery-mobile-alpha-1-released/)          | 1.0.0 Alpha 1      |
| [2010년 11월 12일](https://blog.jquerymobile.com/2010/11/12/jquery-mobile-alpha-2-released/)            | 1.0.0 Alpha 2      |
| [2011년 2월 4일](https://blog.jquerymobile.com/2011/02/04/jquery-mobile-alpha-3-released/)              | 1.0.0 Alpha 3      |
| [2011년 3월 31일](https://blog.jquerymobile.com/2011/03/31/jquery-mobile-alpha-4-released/)             | 1.0.0 Alpha 4      |
| [April 7 2011](https://blog.jquerymobile.com/2011/04/07/jquery-alpha-4-1-maintenance-release/)       | 1.0.0 Alpha 4.1    |
| [June 20 2011](https://blog.jquerymobile.com/2011/06/20/jquery-mobile-beta-1-released/)              | 1.0.0 Beta 1       |
| [August 3 2011](https://blog.jquerymobile.com/2011/08/03/jquery-mobile-beta-2-released/)             | 1.0.0 Beta 2       |
| [September 8 2011](https://blog.jquerymobile.com/2011/09/08/jquery-mobile-beta-3-released/)          | 1.0.0 Beta 3       |
| [September 29 2011](https://blog.jquerymobile.com/2011/09/29/jquery-mobile-1-0rc1-released/)         | 1.0.0 RC1          |
| [October 19 2011](https://blog.jquerymobile.com/2011/10/19/jquery-mobile-1-0rc2-released/)           | 1.0.0 RC2          |
| [November 13 2011](https://blog.jquerymobile.com/2011/11/13/jquery-mobile-rc3-released/)             | 1.0.0 RC3          |
| [November 16 2011](https://blog.jquerymobile.com/2011/11/16/announcing-jquery-mobile-1-0/)           | 1.0.0              |
| [January 26 2012](https://blog.jquerymobile.com/2012/01/26/jquery-mobile-1-0-1-released/)            | 1.0.1              |
| [2012년 2월 28일](https://blog.jquerymobile.com/2012/02/28/announcing-jquery-mobile-1-1-0-rc1/)         | 1.1.0 RC1          |
| [2012년 4월 6일](https://blog.jquerymobile.com/2012/04/06/jquery-mobile-1-1-0-rc2/)                     | 1.1.0 RC2          |
| [2012년 4월 13일](https://blog.jquerymobile.com/2012/04/13/announcing-jquery-mobile-1-1-0/)             | 1.1.0              |
| [2012년 6월 28일](https://blog.jquerymobile.com/2012/06/28/announcing-jquery-mobile-1-1-1-rc1/)         | 1.1.1 RC1          |
| [2012년 7월 12일](https://blog.jquerymobile.com/2012/07/12/jqm-1-1-1/)                                  | 1.1.1              |
| [2012년 8월 1일](https://blog.jquerymobile.com/2012/08/01/announcing-jquery-mobile-1-2-0-alpha/)        | 1.2.0 Alpha        |
| [2012년 9월 5일](https://blog.jquerymobile.com/2012/09/05/jquery-mobile-1-2-beta-released/)             | 1.2.0 Beta         |
| [2012년 9월 14일](https://blog.jquerymobile.com/2012/09/14/jquery-mobile-release-candidate-1-released/) | 1.2.0 RC1          |
| [2012년 9월 21일](https://blog.jquerymobile.com/2012/09/21/jquery-mobile-1-2-0-release-candidate-2/)    | 1.2.0 RC2          |
| [2012년 10월 2일](https://blog.jquerymobile.com/2012/10/02/announcing-jquery-mobile-1-2-0-final/)       | 1.2.0              |
| [2013년 1월 14일](https://blog.jquerymobile.com/2013/01/14/announcing-jquery-mobile-1-3-0-beta/)        | 1.3.0 Beta         |
| [2013년 2월 4일](https://blog.jquerymobile.com/2013/02/04/jquery-mobile-1-3-0-rc1-released/)            | 1.3.0 RC1          |
| [2013년 2월 20일](https://blog.jquerymobile.com/2013/02/20/jquery-mobile-1-3-0-released/)               | 1.3.0              |
| [2013년 3월 19일](https://blog.jquerymobile.com/2013/03/19/announcing-jquery-mobile-1-1-2/)             | 1.1.2              |
| [2013년 3월 22일](https://blog.jquerymobile.com/2013/03/22/announcing-jquery-mobile-1-2-1/)             | 1.2.1              |
| [2013년 4월 10일](https://blog.jquerymobile.com/2013/04/10/announcing-jquery-mobile-1-3-1/)             | 1.3.1              |
| [2013년 7월 19일](https://blog.jquerymobile.com/2013/07/19/announcing-jquery-mobile-1-3-2/)             | 1.3.2              |
| [2013년 7월 25일](https://blog.jquerymobile.com/2013/07/25/announcing-jquery-mobile-1-4-0-alpha/)       | 1.4.0 Alpha 1      |
| [2013년 8월 15일](https://blog.jquerymobile.com/2013/08/15/jquery-mobile-1-4-0-alpha-2-released/)       | 1.4.0 Alpha 2      |
| [2013년 9월 24일](https://blog.jquerymobile.com/2013/09/24/announcing-jquery-mobile-1-4-beta/)          | 1.4.0 Beta 1       |
| [2013년 10월 24일](https://blog.jquerymobile.com/2013/10/24/jquery-mobile-1-4-0-rc1-released/)          | 1.4.0 RC 1         |
| [2013년 12월 23일](https://blog.jquerymobile.com/2013/12/23/jquery-mobile-1-4-0-released/)              | 1.4.0              |
| [2014년 2월 12일](https://blog.jquerymobile.com/2014/02/12/jquery-mobile-1-4-1-released/)               | 1.4.1              |
| [2014년 2월 28일](https://blog.jquerymobile.com/2014/02/28/jquery-mobile-1-4-2-released/)               | 1.4.2              |
| [2014년 7월 1일](https://blog.jquerymobile.com/2014/07/01/jquery-mobile-1-4-3-released/)                | 1.4.3              |
| [2014년 9월 12일](https://blog.jquerymobile.com/2014/09/12/jquery-mobile-1-4-4-released/)               | 1.4.4              |
| [2014년 10월 31일](https://blog.jquerymobile.com/2014/10/31/jquery-mobile-1-4-5-released/)              | 1.4.5 **(최신 안정판)** |
| [2017년 1월 3일](http://blog.jquerymobile.com/2017/05/11/jquery-mobile-1-5-0-alpha-1-released/)         | 1.5.0-alpha.1      |

## 같이 보기

  - [jQTouch](https://ko.wikipedia.org/wiki/jQTouch "wikilink")
  - [JQuery](../Page/JQuery.md "wikilink")
  - [Content adaptation](https://ko.wikipedia.org/wiki/Content_adaptation "wikilink")
  - [DaVinci Studio](https://ko.wikipedia.org/wiki/DaVinci "wikilink")
  - [iUI](https://ko.wikipedia.org/wiki/iUI "wikilink")
  - [아파치 코도바](../Page/아파치_코도바.md "wikilink")
  - [타이젠](../Page/타이젠.md "wikilink")
  - [ViziApps](https://ko.wikipedia.org/wiki/ViziApps "wikilink")
  - [부트스트랩](https://ko.wikipedia.org/wiki/부트스트랩 "wikilink")

## 각주

## 참고 자료

  -
  -
  -
  -
  -
  -
  -
  -
  -
  -
## 외부 링크

  -
  - [The jQuery Project](https://jquery.org/)

  - [jQuery Mobile documentation and demo](https://demos.jquerymobile.com/1.0/)

  - [jQuery Mobile Framework: write less, do more](https://web.archive.org/web/20120321094122/http://www.mobicules.com/html5/jquery-mobile-framework-write-less-do-more/)

  - [jQuery Mobile C\# ASP.NET By Matthew David Elgert](http://jquerymobile.codeplex.com/)

  - [PropertyCross, Helping you select a cross-platform mobile framework: jQuery Mobile](https://archive.is/20140228104452/http://propertycross.com/jquerymobile/)

[분류:자바스크립트 라이브러리](https://ko.wikipedia.org/wiki/분류:자바스크립트_라이브러리 "wikilink") [분류:Ajax](https://ko.wikipedia.org/wiki/분류:Ajax "wikilink") [분류:웹 프레임워크](https://ko.wikipedia.org/wiki/분류:웹_프레임워크 "wikilink") [분류:모바일 웹](https://ko.wikipedia.org/wiki/분류:모바일_웹 "wikilink")

1.
2.
3.
4.
5.