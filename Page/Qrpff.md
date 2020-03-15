> This article is converted from Wikipedia: [Qrpff](https://ko.wikipedia.org/wiki/Qrpff).


**qrpff**는 [Keith Winstein과](https://ko.wikipedia.org/wiki/Keith_Winstein "wikilink") Marc Horowitz(MAT SITB 출신)가 작성한 [펄](https://ko.wikipedia.org/wiki/펄 "wikilink") 스크립트이다.\[1\] 6\~7줄의 [DeCSS](https://ko.wikipedia.org/wiki/DeCSS "wikilink")를 수행한다. 이름 그 자체는 [rot-13의](https://ko.wikipedia.org/wiki/ROT13 "wikilink") "decss" 인코딩이다. 이 알고리즘은 6줄로 줄이기 위해 77번 재작성되었다.\[2\]

실제로, qrpff는 두 가지 버전이 존재한다: 짧은 버전(6줄), 빠른 버전(7줄). 두 버전은 아래와 같이 나타난다.

짧은 버전:

``` perl
#!/usr/bin/perl
# 472-byte qrpff, Keith Winstein and Marc Horowitz <sipb-iap-dvd@mit.edu>
# MPEG 2 PS VOB file -> descrambled output on stdout.
# usage: perl -I <k1>:<k2>:<k3>:<k4>:<k5> qrpff
# where k1..k5 are the title key bytes in least to most-significant order

s''$/=\2048;while(<>){G=29;R=142;if((@a=unqT="C*",_)[20]&48){D=89;_=unqb24,qT,@
b=map{ord qB8,unqb8,qT,_^$a[--D]}@INC;s/...$/1$&/;Q=unqV,qb25,_;H=73;O=$b[4]<<9
|256|$b[3];Q=Q>>8^(P=(E=255)&(Q>>12^Q>>4^Q/8^Q))<<17,O=O>>8^(E&(F=(S=O>>14&7^O)
^S*8^S<<6))<<9,_=(map{U=_%16orE^=R^=110&(S=(unqT,"\xb\ntd\xbz\x14d")[_/16%8]);E
^=(72,@z=(64,72,G^=12*(U-2?0:S&17)),H^=_%64?12:0,@z)[_%8]}(16..271))[_]^((D>>=8
)+=P+(~F&E))for@a[128..$#a]}print+qT,@a}';s/[D-HO-U_]/\$$&/g;s/q/pack+/g;eval
```

빠른 버전:

``` perl
#!/usr/bin/perl -w
# 531-byte qrpff-fast, Keith Winstein and Marc Horowitz <sipb-iap-dvd@mit.edu>
# MPEG 2 PS VOB file on stdin -> descrambled output on stdout
# arguments: title key bytes in least to most-significant order

$_='while(read+STDIN,$_,2048){$a=29;$b=73;$c=142;$t=255;@t=map{$_%16or$t^=$c^=(
$m=(11,10,116,100,11,122,20,100)[$_/16%8])&110;$t^=(72,@z=(64,72,$a^=12*($_%16
-2?0:$m&17)),$b^=$_%64?12:0,@z)[$_%8]}(16..271);if((@a=unx"C*",$_)[20]&48){$h
=5;$_=unxb24,join"",@b=map{xB8,unxb8,chr($_^$a[--$h+84])}@ARGV;s/...$/1$&/;$
d=unxV,xb25,$_;$e=256|(ord$b[4])<<9|ord$b[3];$d=$d>>8^($f=$t&($d>>12^$d>>4^
$d^$d/8))<<17,$e=$e>>8^($t&($g=($q=$e>>14&7^$e)^$q*8^$q<<6))<<9,$_=$t[$_]^
(($h>>=8)+=$f+(~$g&$t))for@a[128..$#a]}print+x"C*",@a}';s/x/pack+/g;eval
```

빠른 버전은 실제로 영화를 실시간으로 디코딩하기 충분할 정도로 속도가 빠르다.

qrpff와 관련 수집 항목들은 세계 최초의 [컴퓨터 알고리즘](https://ko.wikipedia.org/wiki/컴퓨터_알고리즘 "wikilink") 경매 사이트인 [알고리즘 옥션에](https://ko.wikipedia.org/wiki/알고리즘_옥션 "wikilink") 2,500 달러에 판매되었다.\[3\]

## 각주

## 외부 링크

  - [qrpff (fast) explained](http://perl.plover.com/qrpff/)
  - [Gallery of CSS descramblers](http://www-2.cs.cmu.edu/~dst/DeCSS/Gallery/index.html)

[분류:펄](https://ko.wikipedia.org/wiki/분류:펄 "wikilink")

1.
2.
3.