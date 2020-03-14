> This article is converted from Wikipedia: [WxPerl](https://ko.wikipedia.org/wiki/WxPerl).


**wxPerl**은 Mattia Barbon이 개발한 [펄 모듈의](../Page/펄_모듈.md "wikilink") 하나로, [펄 프로그래밍 언어로](https://ko.wikipedia.org/wiki/펄 "wikilink") [그래픽 사용자 인터페이스](https://ko.wikipedia.org/wiki/그래픽_사용자_인터페이스 "wikilink")(GUI)를 개발할 수 있게 도와준다. [wxWidgets](https://ko.wikipedia.org/wiki/wxWidgets "wikilink")(C++ [GUI](https://ko.wikipedia.org/wiki/그래픽_사용자_인터페이스 "wikilink") [위젯 툴킷](https://ko.wikipedia.org/wiki/위젯_툴킷 "wikilink"))용 [XS](https://ko.wikipedia.org/wiki/XS_\(펄\) "wikilink") 래퍼로 작성되었다. wxPerl로 개발된 여러 프로그램들 중에는 [Padre](https://ko.wikipedia.org/wiki/Padre "wikilink")라는 펄 IDE와 [오픈코어](https://ko.wikipedia.org/wiki/오픈코어 "wikilink")(Openkore)라는 이북 리더를 포함한다. 펄과 wxWidgets처럼 wxPerl은 [자유 소프트웨어이다](https://ko.wikipedia.org/wiki/자유_소프트웨어 "wikilink").

## 예제 코드

아래는 단순한 [Hello world](https://ko.wikipedia.org/wiki/Hello_world "wikilink") 모듈이다.

``` perl
use Wx;

my $app = Wx::SimpleApp->new;
my $frame = Wx::Frame->new( undef, -1, 'Hello, world!' );

$frame->Show;
$app->MainLoop;
```

## 각주

<references />

## 외부 링크

  - [wxPerl's web site](http://www.wxperl.it)

  - [wxPerl on CPAN](https://metacpan.org/module/Wx)

  - [wxPerl User Wiki](https://web.archive.org/web/20130206024924/http://wiki.wxperl.nl/)

  - [CitrusPerl, a Perl distribution that includes wxPerl](http://www.citrusperl.org)

[분류:위젯 툴킷](https://ko.wikipedia.org/wiki/분류:위젯_툴킷 "wikilink") [분류:펄 모듈](https://ko.wikipedia.org/wiki/분류:펄_모듈 "wikilink")