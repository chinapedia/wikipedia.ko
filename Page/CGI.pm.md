> This article is converted from Wikipedia: [CGI.pm](https://ko.wikipedia.org/wiki/CGI.pm).


**CGI.pm**은 [공용 게이트웨이 인터페이스](../Page/공용_게이트웨이_인터페이스.md "wikilink")(CGI) [웹](../Page/월드_와이드_웹.md "wikilink") 애플리케이션의 [프로그래밍을](../Page/컴퓨터_프로그래밍.md "wikilink") 위해 널리 사용되는 대형 [펄 모듈로서](../Page/펄_모듈.md "wikilink"), 사용자 입력을 수신하고 처리하기 위한 일정한 [API](../Page/API.md "wikilink")를 제공한다. [HTML](../Page/HTML.md "wikilink") 또는 [XHTML](../Page/XHTML.md "wikilink") 출력을 생성하기 위한 기능도 있으나 이것들은 현재 유지보수되지 않고 있으며 배제욀 예정이다.\[1\] CGI.pm은 코어 펄 모듈이었으나 펄 v5.22를 기준으로 제거된 상태이다.\[2\] 이 모듈은 [링컨 스타인에](https://ko.wikipedia.org/wiki/링컨_스타인 "wikilink") 의해 작성되었으며 현재는 리 존슨에 의해 유지보수되고 있다.

## 예제

다음은 CGI.pm을 사용하여 펄로 작성된 단순한 CGI 페이지이다. ([객체 지향](../Page/객체_지향_프로그래밍.md "wikilink") 스타일):

``` perl
#!/usr/bin/env perl

use strict;
use warnings;

use CGI;

my $cgi = CGI->new;

print $cgi->header('text/html');

print << "EndOfHTML";
<!DOCTYPE html>
<html>
    <head>
        <title>A Simple CGI Page</title>
        <meta http-equiv="Content-Type" content="text/html; charset=iso-8859-1" />
    </head>
    <body>
        <h1>A Simple CGI Page</h1>
        <form method="post" enctype="multipart/form-data">
            Name: <input type="text" name="name"  /><br />
            Age: <input type="text" name="age"  /><p>
            <input type="submit" name="Submit!" value="Submit!" />
        </form>
        <hr />
EndOfHTML

if ( my $name = $cgi->param('name') ) {
    print "Your name is $name.<br />";
}

if ( my $age = $cgi->param('age') ) {
    print "You are $age years old.";
}

print '</body></html>';
```

## 같이 보기

  - [Mod perl](../Page/Mod_perl.md "wikilink")

## 각주

## 외부 링크

  - [CGI.pm](https://metacpan.org/module/CGI) – at the [CPAN](../Page/CPAN.md "wikilink")

[분류:펄 모듈](https://ko.wikipedia.org/wiki/분류:펄_모듈 "wikilink")

1.  <https://metacpan.org/pod/distribution/CGI/lib/CGI.pod#HTML-Generation-functions-should-no-longer-be-used>
2.  <https://metacpan.org/pod/distribution/CGI/lib/CGI.pod#CGI.pm-HAS-BEEN-REMOVED-FROM-THE-PERL-CORE>