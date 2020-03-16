> This article is converted from Wikipedia: [IOCCC](https://ko.wikipedia.org/wiki/IOCCC).


**IOCCC**(International Obfuscated C Code Contest, 국제 난독화 C 코드 대회)는 가장 창의적으로 [난독화](../Page/난독화.md "wikilink")된 [C](../Page/C_\(프로그래밍_언어\).md "wikilink") [코드를](../Page/소스_코드.md "wikilink") 공모하는 [컴퓨터 프로그래밍](../Page/컴퓨터_프로그래밍.md "wikilink") 대회이다. 1984-1996, 1998, 2000, 2001, 2004-2006년까지는 해마다 개최되었으며, 2011년부터는 "celebrating \[C's\] syntactical opaqueness"로 기술된다.\[1\] 2013년에 개최된 22번째 콘테스트를 위한 코드는 2014년 1월에 공개되었다.\[2\]

2004년 이전에는 제출은 전자메일로만 받았다.\[3\] 2004년, 제17회 IOCCC에서는 웹 기반 제출 프로세스를 이용하는 방식으로 전환되었다.\[4\]

## 예

1988년에 제출된 것으로, 자신의 [넓이](../Page/넓이.md "wikilink")를 살피며 [원주율](https://ko.wikipedia.org/wiki/원주율 "wikilink")을 계산한다.:\[5\]

``` c
#define _ -F<00||--F-OO--;
int F=00,OO=00;main(){F_OO();printf("%1.3f\n",4.*-F/OO/OO);}F_OO()
{
            _-_-_-_
       _-_-_-_-_-_-_-_-_
    _-_-_-_-_-_-_-_-_-_-_-_
  _-_-_-_-_-_-_-_-_-_-_-_-_-_
 _-_-_-_-_-_-_-_-_-_-_-_-_-_-_
 _-_-_-_-_-_-_-_-_-_-_-_-_-_-_
_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_
_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_
_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_
_-_-_-_-_-_-_-_-_-_-_-_-_-_-_-_
 _-_-_-_-_-_-_-_-_-_-_-_-_-_-_
 _-_-_-_-_-_-_-_-_-_-_-_-_-_-_
  _-_-_-_-_-_-_-_-_-_-_-_-_-_
    _-_-_-_-_-_-_-_-_-_-_-_
        _-_-_-_-_-_-_-_
            _-_-_-_
}
```

다른 예는 비행 시뮬레이터로, 1998년 IOCCC에서 우승하였으며,\[6\] *Calculated Bets: Computers, Gambling, and Mathematical Modeling to Win* (2001)에 등재, 기술되었고\[7\] 그 예는 아래와 같다:

``` c
#include                                     <math.h>
#include                                   <sys/time.h>
#include                                   <X11/Xlib.h>
#include                                  <X11/keysym.h>
                                          double L ,o ,P
                                         ,_=dt,T,Z,D=1,d,
                                         s[999],E,h= 8,I,
                                         J,K,w[999],M,m,O
                                        ,n[999],j=33e-3,i=
                                        1E3,r,t, u,v ,W,S=
                                        74.5,l=221,X=7.26,
                                        a,B,A=32.2,c, F,H;
                                        int N,q, C, y,p,U;
                                       Window z; char f[52]
                                    ; GC k; main(){ Display*e=
 XOpenDisplay( 0); z=RootWindow(e,0); for (XSetForeground(e,k=XCreateGC (e,z,0,0),BlackPixel(e,0))
; scanf("%lf%lf%lf",y +n,w+y, y+s)+1; y ++); XSelectInput(e,z= XCreateSimpleWindow(e,z,0,0,400,400,
0,0,WhitePixel(e,0) ),KeyPressMask); for(XMapWindow(e,z); ; T=sin(O)){ struct timeval G={ 0,dt*1e6}
; K= cos(j); N=1e4; M+= H*_; Z=D*K; F+=_*P; r=E*K; W=cos( O); m=K*W; H=K*T; O+=D*_*F/ K+d/K*E*_; B=
sin(j); a=B*T*D-E*W; XClearWindow(e,z); t=T*E+ D*B*W; j+=d*_*D-_*F*E; P=W*E*B-T*D; for (o+=(I=D*W+E
*T*B,E*d/K *B+v+B/K*F*D)*_; p<y; ){ T=p[s]+i; E=c-p[w]; D=n[p]-L; K=D*m-B*T-H*E; if(p [n]+w[ p]+p[s
]== 0|K <fabs(W=T*r-I*E +D*P) |fabs(D=t *D+Z *T-a *E)> K)N=1e4; else{ q=W/K *4E2+2e2; C= 2E2+4e2/ K
 *D; N-1E4&& XDrawLine(e ,z,k,N ,U,q,C); N=q; U=C; } ++p; } L+=_* (X*t +P*M+m*l); T=X*X+ l*l+M *M;
  XDrawString(e,z,k ,20,380,f,17); D=v/l*15; i+=(B *l-M*r -X*Z)*_; for(; XPending(e); u *=CS!=N){
                                   XEvent z; XNextEvent(e ,&z);
                                       ++*((N=XLookupKeysym
                                         (&z.xkey,0))-IT?
                                         N-LT? UP-N?& E:&
                                         J:& u: &h); --*(
                                         DN -N? N-DT ?N==
                                         RT?&u: & W:&h:&J
                                          ); } m=15*F/l;
                                          c+=(I=M/ l,l*H
                                          +I*M+a*X)*_; H
                                          =A*r+v*X-F*l+(
                                          E=.1+X*4.9/l,t
                                          =T*m/32-I*T/24
                                           )/S; K=F*M+(
                                           h* 1e4/l-(T+
                                           E*5*T*E)/3e2
                                           )/S-X*d-B*A;
                                           a=2.63 /l*d;
                                           X+=( d*l-T/S
                                            *(.19*E +a
                                            *.64+J/1e3
                                            )-M* v +A*
                                            Z)*_; l +=
                                            K *_; W=d;
                                            sprintf(f,
                                            "%5d  %3d"
                                            "%7d",p =l
                                           /1.7,(C=9E3+
                              O*57.3)%0550,(int)i); d+=T*(.45-14/l*
                             X-a*130-J* .14)*_/125e2+F*_*v; P=(T*(47
                             *I-m* 52+E*94 *D-t*.38+u*.21*E) /1e2+W*
                             179*v)/2312; select(p=0,0,0,0,&G); v-=(
                              W*F-T*(.63*m-I*.086+m*E*19-D*25-.11*u
                               )/107e2)*_; D=cos(o); E=sin(o); } }
```

이 프로그램은 리눅스 시스템에서 컴파일하려면 다음의 줄이 필요하다:

    cc banks.c -o banks -DIT=XK_Page_Up -DDT=XK_Page_Down \
        -DUP=XK_Up -DDN=XK_Down -DLT=XK_Left -DRT=XK_Right \
        -DCS=XK_Return -Ddt=0.02 -lm -lX11 -L/usr/X11R6/lib

## 같이 보기

  - [난독화 펄 콘테스트](https://ko.wikipedia.org/wiki/난독화_펄_콘테스트 "wikilink")

## 각주

## 외부 링크

  -

[분류:프로그래밍 대회](https://ko.wikipedia.org/wiki/분류:프로그래밍_대회 "wikilink") [분류:유머상](https://ko.wikipedia.org/wiki/분류:유머상 "wikilink") [분류:난독화](https://ko.wikipedia.org/wiki/분류:난독화 "wikilink")

1.
2.
3.
4.
5.  [5th International Obfuscated C Code Contest 1988](http://www0.us.ioccc.org/years.html#1988)  (westley.c). IOCCC.
6.  [IOCCC Flight Simulator](http://www.aerojockey.com/software/ioccc/index.html). aerojockey.com. Retrieved 2013-04-08.
7.