> This article is converted from Wikipedia: [MySQL](https://ko.wikipedia.org/wiki/MySQL).


**MySQL**(마이에스큐엘, )\[1\]은 세계에서 가장 많이 쓰이는\[2\] 오픈 소스의 [관계형 데이터베이스 관리 시스템](../Page/관계형_데이터베이스_관리_시스템.md "wikilink")(RDBMS)이다.\[3\] 다중 스레드, 다중 사용자 형식의 구조질의어 형식의 데이터베이스 관리 시스템으로서 [오라클이](../Page/오라클_\(기업\).md "wikilink") 관리 및 지원하고 있으며, [Qt처럼](../Page/Qt_\(프레임워크\).md "wikilink") 이중 라이선스가 적용된다. 하나의 옵션은 [GPL](https://ko.wikipedia.org/wiki/GPL "wikilink")이며, GPL 이외의 라이선스로 적용시키려는 경우 전통적인 지적재산권 라이선스의 적용을 받는다.

위와 같은 지원 방식은 [자유 소프트웨어 재단이](../Page/자유_소프트웨어_재단.md "wikilink") 프로젝트에 저작권을 적용하는 방법과 비슷한 JBoss의 모델과 유사하다. 그러나 기반코드가 개인의 소유자에게 저작권이 있고 커뮤니티에 의해 개발되는 아파치 프로젝트와는 다르다.

MySQL AB는 또한 MaxDB라고 불리는 MySQL AB와는 기반코드가 다른 데이터베이스 관리 시스템을 판매했으나 2007년 이래로 MaxDB는 [SAP AG가](https://ko.wikipedia.org/wiki/SAP_AG "wikilink") 소유하고 있다.\[4\]

[썬 마이크로시스템즈에](../Page/썬_마이크로시스템즈.md "wikilink") 10억 달러에 인수되었으나, [썬 마이크로시스템즈가](../Page/썬_마이크로시스템즈.md "wikilink") [오라클에](../Page/오라클_\(기업\).md "wikilink") 인수되며 같이 넘어갔다.\[5\]

## 인터페이스

[섬네일](https://ko.wikipedia.org/wiki/파일:Mysqlwb-homepage.png "wikilink")\]\] MySQL은 [관계형 데이터베이스 관리 시스템](../Page/관계형_데이터베이스_관리_시스템.md "wikilink")(RDBMS)으로, 데이터베이스를 관리하거나 자료를 관리하기 위한 [GUI](https://ko.wikipedia.org/wiki/GUI "wikilink") 관리툴은 내장되어 있지 않다.\[6\]\[7\] 따라서 이용자들은 [명령 줄 인터페이스](../Page/명령_줄_인터페이스.md "wikilink") 도구들을 이용하거나 또는 데이터베이스를 만들고, 관리하는데, 데이터를 백업하는데, 상태를 검사하고, 데이터베이스 구조를 생성하는데, 또는 데이터 레코더를 작성하는데 있어서 MySQL 프론트엔드 데스크톱 소프트웨어나 웹 애플리케이션을 사용해야 한다.\[8\]\[9\]\[10\]\[11\] 공식적인 MySQL 프론트엔드 툴인 [MySQL 워크벤치는](../Page/MySQL_워크벤치.md "wikilink") [오라클](https://ko.wikipedia.org/wiki/오라클 "wikilink")에 의해 개발되었으며, 자유롭게 사용할 수 있다.\[12\]

### 그래픽

공식 툴인 [MySQL 워크벤치는](../Page/MySQL_워크벤치.md "wikilink") 사용자에게 MySQL 데이터베이스 관리를 그래픽적으로 지원하게 하며, 데이터베이스 구조의 설계도 시각적으로 하게 해주는 MySQL AB에 의해 개발된 자유로운 집적 환경을 가지고 있다. 이것은 이전의 패키지 소프트웨어였던 [MySQL GUI 툴즈를](https://ko.wikipedia.org/wiki/MySQL_GUI_툴즈 "wikilink") 대체하였다. 여타의 제3자 패키지와 유사하지만, MySQL 현장에서 신뢰할 수 있는 툴로 여겨지고 있으며, 이것은 이용자가 데이터베이스를 설계하고, 모델링, SQL 관리(MySQL 쿼리 브라우저 대체) 그리고 데이터베이스 관리(MySQL Administrator 대체)까지할 수 있도록 지원한다.

MySQL 워크벤치는 2가지 판이 존재하는데, MySQL 홈페이지에서 다운받을 수 있는 보통의 자유, 공개 소스인 ‘커뮤니티 판’(*Community Edition*)과 커뮤니티 판을 확장하여 개선시킨 유료의 ‘스탠더드 판’(*Standard Edition*)이 존재한다.

## 프로그래밍 언어

응용 프로그램에서 MySQL [데이터베이스](../Page/데이터베이스.md "wikilink")에 접근하기 위해 다수의 [프로그래밍 언어로](../Page/프로그래밍_언어.md "wikilink") 된 [API](../Page/API.md "wikilink")를 사용할 수 있다. 이들 API는 언어에 종속적이다.

MySQL은 공식적으로 아래의 프로그래밍 언어를 지원한다.

  - C/C++
  - C\#/F\#
  - 볼랜드 [델파이](../Page/델파이.md "wikilink") (dbExpress를 통한)
  - [자바](../Page/자바_\(프로그래밍_언어\).md "wikilink") (네이티브 자바 드라이버를 통한)
  - [파이썬](../Page/파이썬.md "wikilink")
  - [루비](../Page/루비_\(프로그래밍_언어\).md "wikilink")
  - REALbasic ([매킨토시](../Page/매킨토시.md "wikilink") 계열)
  - [프리베이직](https://ko.wikipedia.org/wiki/프리베이직 "wikilink")
  - [스몰토크](../Page/스몰토크.md "wikilink")
  - [Eiffel](https://ko.wikipedia.org/wiki/Eiffel "wikilink")
  - [리스프](../Page/리스프.md "wikilink")
  - [펄](../Page/펄.md "wikilink")
  - [Tcl](../Page/Tcl.md "wikilink")
  - [PHP](../Page/PHP.md "wikilink") {{·}}[PHP](../Page/PHP.md "wikilink")4 {{·}}[PHP](../Page/PHP.md "wikilink")5 {{·}}[PHP](../Page/PHP.md "wikilink")6
  - [델파이](../Page/델파이.md "wikilink")1 {{·}} 델파이2 {{·}} 델파이3 {{·}}델파이4 {{·}}델파이5{{·}}델파이6{{·}}델파이7{{·}}델파이8
  - [델파이2007](https://ko.wikipedia.org/wiki/델파이2007 "wikilink"){{·}}델파이2008{{·}}델파이2009
  - [파파라치](https://ko.wikipedia.org/wiki/파파라치_\(프로그램_언어\) "wikilink")

MySQL은 [MyODBC](https://ko.wikipedia.org/wiki/MyODBC "wikilink")라고 불리는 [ODBC](../Page/ODBC.md "wikilink") 인터페이스를 지원해서 다른 프로그래밍 언어를 지원한다. 그 예로 [ASP와](../Page/액티브_서버_페이지.md "wikilink") [콜드퓨전](https://ko.wikipedia.org/wiki/콜드퓨전 "wikilink")을 들 수 있다. MySQL은 대부분 ANSI C로 구현되었다.

## 사용

MySQL은 [미디어위키](../Page/미디어위키.md "wikilink")와 [드루팔](../Page/드루팔.md "wikilink")과 같은 인기있는 웹 애플리케이션에 사용된다. 그리고 LAMP, MAMP, WAMP (리눅스/매킨토시/윈도-아파치-MySQL-PHP/펄/파이썬) 플랫폼의 데이터베이스 구성체로서 작동하며 버그질라와 같은 오픈소스 버그 추적 도구에도 사용된다.

웹 애플리케이션으로서의 MySQL의 인기는 [PHP](../Page/PHP.md "wikilink")의 인기도와 맞물려 있다. PHP는 종종 MySQL과 결합되며, 다이내믹 듀오(Dynamic Duo)라는 별칭이 붙었다. 인터넷 상의 여러 웹사이트, 혹은 서적을 통해서 MySQL과 PHP의 연동에 대한 정보를 쉽게 찾을 수 있다. 최근의 플랫폼에서는 이들의 연동을 자동으로 해 주는 경우가 있다.

또한 SUN 인수 이후, 중소기업이나 개인용 사이트뿐만 아니라 대기업에서도 점차 관심을 보이고 있다. [위키백과](../Page/위키백과.md "wikilink")\[13\], [구글](../Page/구글.md "wikilink")(검색 엔진은 제외)\[14\]\[15\], [페이스북](../Page/페이스북.md "wikilink")\[16\]\[17\]\[18\], [트위터](../Page/트위터.md "wikilink")\[19\], [플리커](../Page/플리커.md "wikilink")\[20\], [노키아닷컴](http://www.nokia.com)\[21\], [유튜브](../Page/유튜브.md "wikilink")\[22\] 등에서 사용하고 있다.

## 버전

<timeline> Define $now = 12/11/2012 Define $begindate = 01/01/1999 Define $width = 700 Define $warning = 380 \# $width - 120 Define $height = 750 ImageSize = width:$width height:$height PlotArea = left:40 right:10 bottom:100 top:20 DateFormat = dd/mm/yyyy Period = from:$begindate till:$now TimeAxis = orientation:ver Alignbars = early Legend = orientation:vertical position:bottom columns:1

1.  1.
2.  Color definitions \#

    1.  1.
Colors =

`id:col5.1 value:rgb(0.4,0.6,1) Legend:Active_Development`
`id:col5.0 value:rgb(1,0.6,0.4) Legend:NO_Active_Development`
`id:col2.0-l1 value:black`
`id:col2.0-l2 value:gray(0.98)`
`id:colbg value:gray(0.98)`
`id:colgrmaj value:gray(0.5)`
`id:colgrmin value:gray(0.8)`
`id:lighttext value:rgb(0.5,0.5,0.5)`

ScaleMajor = gridcolor:colgrmaj unit:year increment:1 start:$begindate ScaleMinor = gridcolor:colgrmin unit:month increment:3 start:$begindate BackgroundColors = canvas:colbg

PlotData=

`##################################################`
`# 3.23 filled bar #`
`##################################################`
`bar:3.23 width:40 from:05/07/1999 till:11/09/2003 color:col5.0 mark:(line,col5.0)`

`##################################################`
`# 3.23 line for all other versions #`
`##################################################`
`bar:3.23 mark:(line,col2.0-l2)`
`at: 08/07/1999 shift:(0,-15) # 3.23.1`
`at: 09/08/1999 shift:(0,-15) # 3.23.2`
`at: 13/09/1999 shift:(0,-15) # 3.23.3`
`at: 28/09/1999 shift:(0,-15) # 3.23.4`
`at: 20/10/1999 shift:(0,-15) # 3.23.5`
`at: 15/12/1999 shift:(0,-15) # 3.23.6`
`at: 10/12/1999 shift:(0,-15) # 3.23.7`
`at: 02/01/2000 shift:(0,-15) # 3.23.8`
`at: 29/01/2000 shift:(0,-15) # 3.23.9`
`at: 30/01/2000 shift:(0,-15) # 3.23.10`
`at: 16/02/2000 shift:(0,-15) # 3.23.11`
`at: 07/03/2000 shift:(0,-15) # 3.23.12`
`at: 14/03/2000 shift:(0,-15) # 3.23.13`
`at: 09/04/2000 shift:(0,-15) # 3.23.14`
`at: 08/05/2000 shift:(0,-15) # 3.23.15`
`at: 16/05/2000 shift:(0,-15) # 3.23.16`
`at: 07/06/2000 shift:(0,-15) # 3.23.16`
`at: 11/06/2000 shift:(0,-15) # 3.23.17`
`at: 11/07/2000 shift:(0,-15) # 3.23.18`
`at: 04/07/2000 shift:(0,-15) # 3.23.21`
`at: 31/07/2000 shift:(0,-15) # 3.23.22`
`at: 01/09/2000 shift:(0,-15) # 3.23.23`
`at: 08/09/2000 shift:(0,-15) # 3.23.24`
`at: 29/09/2000 shift:(0,-15) # 3.23.25`
`at: 18/10/2000 shift:(0,-15) # 3.23.26`
`at: 24/10/2000 shift:(0,-15) # 3.23.27`
`at: 06/12/2000 shift:(0,-15) # 3.23.29`
`at: 04/01/2001 shift:(0,-15) # 3.23.30`
`at: 22/01/2001 shift:(0,-15) # 3.23.32`
`at: 09/02/2001 shift:(0,-15) # 3.23.33`
`at: 10/03/2001 shift:(0,-15) # 3.23.34`
`at: 11/03/2001 shift:(0,-15) # 3.23.34a`
`at: 15/03/2001 shift:(0,-15) # 3.23.35`
`at: 27/03/2001 shift:(0,-15) # 3.23.36`
`at: 17/04/2001 shift:(0,-15) # 3.23.37`
`at: 09/05/2001 shift:(0,-15) # 3.23.38`
`at: 12/06/2001 shift:(0,-15) # 3.23.39`
`at: 18/07/2001 shift:(0,-15) # 3.23.40`
`at: 11/08/2001 shift:(0,-15) # 3.23.41`
`at: 08/09/2001 shift:(0,-15) # 3.23.42`
`at: 04/10/2001 shift:(0,-15) # 3.23.43`
`at: 31/10/2001 shift:(0,-15) # 3.23.44`
`at: 22/11/2001 shift:(0,-15) # 3.23.45`
`at: 29/11/2001 shift:(0,-15) # 3.23.46`
`at: 27/12/2001 shift:(0,-15) # 3.23.47`
`at: 14/02/2002 shift:(0,-15) # 3.23.49`
`at: 21/04/2002 shift:(0,-15) # 3.23.50`
`at: 31/05/2002 shift:(0,-15) # 3.23.51`
`at: 14/08/2002 shift:(0,-15) # 3.23.52`
`at: 09/10/2002 shift:(0,-15) # 3.23.53`
`at: 05/12/2002 shift:(0,-15) # 3.23.54`
`at: 23/01/2003 shift:(0,-15) # 3.23.55`
`at: 13/03/2003 shift:(0,-15) # 3.23.56`
`at: 06/06/2003 shift:(0,-15) # 3.23.57`

`##################################################`
`# 3.23 line & text for first version every year #`
`##################################################`
`bar:3.23 mark:(line,col2.0-l1) align:center fontsize:S textcolor:red`
`at: 05/07/1999 text:"3.23.0 Alfa" shift:(50,-3)`
`at: 28/06/2000 shift:(54,-3) text:"3.23.20 Beta"`
`at: 22/11/2000 shift:(51,-8) text:"3.23.28 RC"`
`at: 17/01/2001 shift:(54,1) text:"3.23.31 FCS"`
`at: 07/02/2002 shift:(42,-3) text:"3.23.48"`
`at: 11/09/2003 text:"3.23.58" shift:(0,5)`

`##################################################`
`# 4.0 filled bar #`
`##################################################`
`bar:4.0 width:40 from:01/10/2001 till:12/02/2007 color:col5.0 mark:(line,col5.0)`

`##################################################`
`# 4.0 line for all other versions #`
`##################################################`
`bar:4.0 mark:(line,col2.0-l2)`
`at: 23/12/2001 shift:(0,-15) # 4.0.1`
`at: 01/07/2002 shift:(0,-15) # 4.0.2`
`at: 29/09/2002 shift:(0,-15) # 4.0.4`
`at: 13/11/2002 shift:(0,-15) # 4.0.5`
`at: 20/12/2002 shift:(0,-15) # 4.0.7`
`at: 07/01/2003 shift:(0,-15) # 4.0.8`
`at: 09/01/2003 shift:(0,-15) # 4.0.9`
`at: 29/01/2003 shift:(0,-15) # 4.0.10`
`at: 20/02/2003 shift:(0,-15) # 4.0.11`
`at: 16/05/2003 shift:(0,-15) # 4.0.13`
`at: 18/07/2003 shift:(0,-15) # 4.0.14`
`at: 03/09/2003 shift:(0,-15) # 4.0.15`
`at: 17/10/2003 shift:(0,-15) # 4.0.16`
`at: 14/12/2003 shift:(0,-15) # 4.0.18`
`at: 04/05/2004 shift:(0,-15) # 4.0.19`
`at: 17/05/2004 shift:(0,-15) # 4.0.20`
`at: 06/09/2004 shift:(0,-15) # 4.0.21`
`at: 27/10/2004 shift:(0,-15) # 4.0.22`
`at: 18/12/2004 shift:(0,-15) # 4.0.23`
`at: 05/07/2005 shift:(0,-15) # 4.0.25`
`at: 08/09/2005 shift:(0,-15) # 4.0.26`
`at: 06/05/2006 shift:(0,-15) # 4.0.27`

`##################################################`
`# 4.0 line & text for first version every year #`
`##################################################`
`bar:4.0 mark:(line,col2.0-l1) align:center fontsize:S textcolor:red`
`at: 01/10/2001 text:"4.0.0 Alfa" shift:(46,-3)`
`at: 26/08/2002 shift:(48,-3) text:"4.0.3 Beta"`
`at: 14/12/2002 shift:(45,-3) text:"4.0.6 RC"`
`at: 15/03/2003 shift:(51,-2) text:"4.0.12 FCS"`
`at: 12/02/2004 shift:(40,-3) text:"4.0.18"`
`at: 04/03/2005 shift:(40,-3) text:"4.0.24"`
`at: 12/02/2007 text:"4.0.30" shift:(0,5)`

`##################################################`
`# 4.1 filled bar #`
`##################################################`
`bar:4.1 width:40 from:03/04/2003 till:01/12/2008 color:col5.0 mark:(line,col5.0)`

`##################################################`
`# 4.1 line for all other versions #`
`##################################################`
`bar:4.1 mark:(line,col2.0-l2)`
`at: 01/12/2003 shift:(0,-15) # 4.1.1`
`at: 28/05/2004 shift:(0,-15) # 4.1.2`
`at: 16/09/2004 shift:(0,-15) # 4.1.5`
`at: 10/10/2004 shift:(0,-15) # 4.1.6`
`at: 14/12/2004 shift:(0,-15) # 4.1.8`
`at: 12/02/2005 shift:(0,-15) # 4.1.10`
`at: 01/04/2005 shift:(0,-15) # 4.1.11`
`at: 13/05/2005 shift:(0,-15) # 4.1.12`
`at: 15/07/2005 shift:(0,-15) # 4.1.13`
`at: 17/08/2005 shift:(0,-15) # 4.1.14`
`at: 13/10/2005 shift:(0,-15) # 4.1.15`
`at: 29/11/2005 shift:(0,-15) # 4.1.16`
`at: 29/04/2006 shift:(0,-15) # 4.1.19`
`at: 24/05/2006 shift:(0,-15) # 4.1.20`
`at: 19/07/2006 shift:(0,-15) # 4.1.21`
`at: 02/11/2006 shift:(0,-15) # 4.1.22`

`##################################################`
`# 4.1 line & text for first version every year #`
`##################################################`
`bar:4.1 mark:(line,col2.0-l1) align:center fontsize:S textcolor:red`
`at: 03/04/2003 text:"4.1.0 Alfa" shift:(46,-3)`
`at: 28/06/2004 shift:(48,-8) text:"4.1.3 Beta"`
`at: 26/08/2004 shift:(45,-4) text:"4.1.4 RC"`
`at: 23/10/2004 shift:(48,-2) text:"4.1.7 FCS"`
`at: 11/01/2005 shift:(37,1) text:"4.1.9"`
`at: 27/01/2006 shift:(40,-3) text:"4.1.18"`
`at: 12/06/2007 shift:(40,-3) text:"4.1.23"`
`at: 01/03/2008 shift:(40,-3) text:"4.1.24"`
`at: 01/12/2008 text:"4.1.25" shift:(0,5)`

`##################################################`
`# 5.0 filled bar #`
`##################################################`
`bar:5.0 width:40 from:22/12/2003 till:21/03/2012 color:col5.0 mark:(line,col5.0)`

`##################################################`
`# 5.0 line for all other versions #`
`##################################################`
`bar:5.0 mark:(line,col2.0-l2)`
`at: 01/12/2004 shift:(0,-15) # 5.0.2`
`at: 16/04/2005 shift:(0,-15) # 5.0.4`
`at: 26/05/2005 shift:(0,-15) # 5.0.6`
`at: 10/06/2005 shift:(0,-15) # 5.0.7`
`at: 05/07/2005 shift:(0,-15) # 5.0.9`
`at: 27/07/2005 shift:(0,-15) # 5.0.10`
`at: 06/08/2005 shift:(0,-15) # 5.0.11`
`at: 02/09/2005 shift:(0,-15) # 5.0.12`
`at: 10/11/2005 shift:(0,-15) # 5.0.16`
`at: 14/12/2005 shift:(0,-15) # 5.0.17`
`at: 21/12/2005 shift:(0,-15) # 5.0.18`
`at: 31/03/2006 shift:(0,-15) # 5.0.20`
`at: 18/04/2006 shift:(0,-15) # 5.0.20a`
`at: 02/05/2006 shift:(0,-15) # 5.0.21`
`at: 24/05/2006 shift:(0,-15) # 5.0.22`
`at: 27/07/2006 shift:(0,-15) # 5.0.24`
`at: 25/08/2006 shift:(0,-15) # 5.0.24a`
`at: 12/09/2006 shift:(0,-15) # 5.0.25`
`at: 03/10/2006 shift:(0,-15) # 5.0.26`
`at: 21/10/2006 shift:(0,-15) # 5.0.27`
`at: 24/10/2006 shift:(0,-15) # 5.0.28`
`at: 14/11/2006 shift:(0,-15) # 5.0.30`
`at: 20/12/2006 shift:(0,-15) # 5.0.32`
`at: 09/01/2007 shift:(0,-15) # 5.0.33`
`at: 17/01/2007 shift:(0,-15) # 5.0.34`
`at: 20/02/2007 shift:(0,-15) # 5.0.36`
`at: 12/04/2007 shift:(0,-15) # 5.0.36sp1`
`at: 27/02/2007 shift:(0,-15) # 5.0.37`
`at: 20/03/2007 shift:(0,-15) # 5.0.38`
`at: 17/04/2007 shift:(0,-15) # 5.0.40`
`at: 01/05/2007 shift:(0,-15) # 5.0.41`
`at: 23/05/2007 shift:(0,-15) # 5.0.42`
`at: 21/06/2007 shift:(0,-15) # 5.0.44`
`at: 01/08/2007 shift:(0,-15) # 5.0.44a`
`at: 04/07/2007 shift:(0,-15) # 5.0.45`
`at: 13/07/2007 shift:(0,-15) # 5.0.46`
`at: 27/08/2007 shift:(0,-15) # 5.0.48`
`at: 19/10/2007 shift:(0,-15) # 5.0.50`
`at: 12/12/2007 shift:(0,-15) # 5.0.50sp1`
`at: 15/11/2007 shift:(0,-15) # 5.0.51`
`at: 11/01/2008 shift:(0,-15) # 5.0.51a`
`at: 24/04/2008 shift:(0,-15) # 5.0.51b`
`at: 30/11/2007 shift:(0,-15) # 5.0.52`
`at: 14/12/2007 shift:(0,-15) # 5.0.54`
`at: 11/01/2008 shift:(0,-15) # 5.0.54a`
`at: 06/02/2008 shift:(0,-15) # 5.0.56`
`at: 30/03/2008 shift:(0,-15) # 5.0.56sp1`
`at: 28/04/2008 shift:(0,-15) # 5.0.60`
`at: 27/06/2008 shift:(0,-15) # 5.0.60sp1`
`at: 12/05/2008 shift:(0,-15) # 5.0.62`
`at: 10/06/2008 shift:(0,-15) # 5.0.64`
`at: 09/07/2008 shift:(0,-15) # 5.0.66`
`at: 16/07/2008 shift:(0,-15) # 5.0.66a`
`at: 23/10/2008 shift:(0,-15) # 5.0.66sp1`
`at: 04/08/2008 shift:(0,-15) # 5.0.67`
`at: 13/08/2008 shift:(0,-15) # 5.0.68`
`at: 27/09/2008 shift:(0,-15) # 5.0.70`
`at: 24/10/2008 shift:(0,-15) # 5.0.72`
`at: 13/01/2009 shift:(0,-15) # 5.0.72sp1`
`at: 03/12/2008 shift:(0,-15) # 5.0.74`
`at: 30/04/2009 shift:(0,-15) # 5.0.74sp1`
`at: 17/12/2008 shift:(0,-15) # 5.0.75`
`at: 28/01/2009 shift:(0,-15) # 5.0.77`
`at: 06/02/2009 shift:(0,-15) # 5.0.78`
`at: 09/03/2009 shift:(0,-15) # 5.0.79`
`at: 01/05/2009 shift:(0,-15) # 5.0.80`
`at: 01/05/2009 shift:(0,-15) # 5.0.81`
`at: 20/05/2009 shift:(0,-15) # 5.0.82`
`at: 21/07/2009 shift:(0,-15) # 5.0.82sp1`
`at: 29/05/2009 shift:(0,-15) # 5.0.83`
`at: 07/07/2009 shift:(0,-15) # 5.0.84`
`at: 30/09/2009 shift:(0,-15) # 5.0.84sp1`
`at: 11/08/2009 shift:(0,-15) # 5.0.85`
`at: 09/09/2009 shift:(0,-15) # 5.0.86`
`at: 15/10/2009 shift:(0,-15) # 5.0.87`
`at: 03/02/2010 shift:(0,-15) # 5.0.87sp1`
`at: 04/11/2009 shift:(0,-15) # 5.0.88`
`at: 02/12/2009 shift:(0,-15) # 5.0.89`
`at: 05/05/2010 shift:(0,-15) # 5.0.91`
`at: 05/05/2011 shift:(0,-15) # 5.0.93`
`at: 05/07/2011 shift:(0,-15) # 5.0.94`

`##################################################`
`# 5.0 line & text for first version every year #`
`##################################################`
`bar:5.0 mark:(line,col2.0-l1) align:center fontsize:S textcolor:red`
`at: 22/12/2003 text:"5.0.0 Alfa" shift:(46,-3)`
`at: 27/07/2004 shift:(36,-3) text:"5.0.1"`
`at: 23/03/2005 shift:(48,-3) text:"5.0.3 Beta"`
`at: 22/09/2005 shift:(48,-8) text:"5.0.13 RC"`
`at: 19/10/2005 shift:(51,1) text:"5.0.15 FCS"`
`at: 04/03/2006 shift:(40,-3) text:"5.0.19"`
`at: 19/01/2007 shift:(50,-3) text:"5.0.30sp1"`
`at: 11/01/2008 shift:(52,-3) text:"5.0.50sp1a"`
`at: 05/01/2009 shift:(40,-3) text:"5.0.76"`
`at: 15/01/2010 shift:(40,-3) text:"5.0.90"`
`at: 07/02/2011 shift:(40,-3) text:"5.0.92"`
`at: 10/01/2012 shift:(40,-3) text:"5.0.95"`
`at: 21/03/2012 shift:(0,5) text:"5.0.96"`

`##################################################`
`# 5.1 filled bar #`
`##################################################`
`bar:5.1 width:40 from:25/11/2005 till:$now color:col5.1 mark:(line,col5.1)`

`##################################################`
`# 5.1 line for all other versions #`
`##################################################`
`bar:5.1 mark:(line,col2.0-l2)`
`at: 29/11/2005 shift:(0,-15) # 5.1.3`
`at: 21/12/2005 shift:(0,-15) # 5.1.4`
`at: 10/01/2006 shift:(0,-15) # 5.1.5`
`at: 01/02/2006 shift:(0,-15) # 5.1.6`
`at: 27/02/2006 shift:(0,-15) # 5.1.7`
`at: 12/04/2006 shift:(0,-15) # 5.1.9`
`at: 25/05/2006 shift:(0,-15) # 5.1.11`
`at: 24/10/2006 shift:(0,-15) # 5.1.12`
`at: 05/12/2006 shift:(0,-15) # 5.1.14`
`at: 25/01/2007 shift:(0,-15) # 5.1.15`
`at: 26/02/2007 shift:(0,-15) # 5.1.16`
`at: 04/04/2007 shift:(0,-15) # 5.1.17`
`at: 08/05/2007 shift:(0,-15) # 5.1.18`
`at: 25/05/2007 shift:(0,-15) # 5.1.19`
`at: 25/06/2007 shift:(0,-15) # 5.1.20`
`at: 16/08/2007 shift:(0,-15) # 5.1.21`
`at: 29/01/2008 shift:(0,-15) # 5.1.23`
`at: 08/04/2008 shift:(0,-15) # 5.1.24`
`at: 28/05/2008 shift:(0,-15) # 5.1.25`
`at: 30/06/2008 shift:(0,-15) # 5.1.26`
`at: 28/08/2008 shift:(0,-15) # 5.1.28`
`at: 11/10/2008 shift:(0,-15) # 5.1.29`
`at: 19/03/2009 shift:(0,-15) # 5.1.31sp1`
`at: 12/02/2009 shift:(0,-15) # 5.1.32`
`at: 13/03/2009 shift:(0,-15) # 5.1.33`
`at: 02/04/2009 shift:(0,-15) # 5.1.34`
`at: 25/06/2009 shift:(0,-15) # 5.1.34sp1`
`at: 13/05/2009 shift:(0,-15) # 5.1.35`
`at: 16/06/2009 shift:(0,-15) # 5.1.36`
`at: 13/07/2009 shift:(0,-15) # 5.1.37`
`at: 10/10/2009 shift:(0,-15) # 5.1.37sp1`
`at: 01/09/2009 shift:(0,-15) # 5.1.38`
`at: 04/09/2009 shift:(0,-15) # 5.1.39`
`at: 06/10/2009 shift:(0,-15) # 5.1.40`
`at: 25/11/2009 shift:(0,-15) # 5.1.40sp1`
`at: 05/11/2009 shift:(0,-15) # 5.1.41`
`at: 15/12/2009 shift:(0,-15) # 5.1.42`
`at: 15/01/2010 shift:(0,-15) # 5.1.43`
`at: 25/03/2010 shift:(0,-15) # 5.1.43sp1`
`at: 04/02/2010 shift:(0,-15) # 5.1.44`
`at: 01/03/2010 shift:(0,-15) # 5.1.45`
`at: 06/04/2010 shift:(0,-15) # 5.1.46`
`at: 23/06/2010 shift:(0,-15) # 5.1.46sp1`
`at: 06/05/2010 shift:(0,-15) # 5.1.47`
`at: 02/06/2010 shift:(0,-15) # 5.1.48`
`at: 09/07/2010 shift:(0,-15) # 5.1.49`
`at: 28/09/2010 shift:(0,-15) # 5.1.49sp1`
`at: 03/08/2010 shift:(0,-15) # 5.1.50`
`at: 10/09/2010 shift:(0,-15) # 5.1.51`
`at: 11/10/2010 shift:(0,-15) # 5.1.52`
`at: 21/02/2011 shift:(0,-15) # 5.1.52sp1`
`at: 03/11/2010 shift:(0,-15) # 5.1.53`
`at: 26/11/2010 shift:(0,-15) # 5.1.54`
`at: 01/03/2011 shift:(0,-15) # 5.1.56`
`at: 05/05/2011 shift:(0,-15) # 5.1.57`
`at: 05/07/2011 shift:(0,-15) # 5.1.58`
`at: 15/09/2011 shift:(0,-15) # 5.1.59`
`at: 16/11/2011 shift:(0,-15) # 5.1.60`
`at: 10/01/2012 shift:(0,-15) # 5.1.61`
`at: 21/03/2012 shift:(0,-15) # 5.1.62`
`at: 07/05/2012 shift:(0,-15) # 5.1.63`
`at: 09/08/2012 shift:(0,-15) # 5.1.65`
`at: 28/09/2012 shift:(0,-15) # 5.1.66`

`##################################################`
`# 5.1 line & text for first version every year #`
`##################################################`
`bar:5.1 mark:(line,col2.0-l1) align:center fontsize:S textcolor:blue`
`at: 25/11/2005 text:"5.1.3" shift:(36,-8)`
`at: 10/01/2006 text:"5.1.5" shift:(36,1)`
`at: 25/01/2007 text:"5.1.15" shift:(40,-3)`
`at: 24/09/2007 text:"5.1.22 RC" shift:(49,-3)`
`at: 29/01/2008 text:"5.1.23" shift:(40,-3)`
`at: 14/11/2008 text:"5.1.30 GA" shift:(49,-5)`
`at: 19/01/2009 text:"5.1.31" shift:(40,0)`
`at: 15/01/2010 text:"5.1.43" shift:(40,-3)`
`at: 07/02/2011 text:"5.1.55" shift:(40,-3)`
`at: 10/01/2012 text:"5.1.61" shift:(40,-3)`

`##################################################`
`# 5.5 filled bar #`
`##################################################`
`bar:5.5 width:40 from:07/12/2009 till:$now color:col5.1 mark:(line,col5.1)`

`##################################################`
`# 5.5 line for all other versions #`
`##################################################`
`bar:5.5 mark:(line,col2.0-l2)`
`at: 04/01/2010 shift:(0,-15) # 5.5.1`
`at: 12/02/2010 shift:(0,-15) # 5.5.2`
`at: 24/03/2010 shift:(0,-15) # 5.5.3`
`at: 09/04/2010 shift:(0,-15) # 5.5.4`
`at: 06/07/2010 shift:(0,-15) # 5.5.5`
`at: 13/09/2010 shift:(0,-15) # 5.5.6`
`at: 14/10/2010 shift:(0,-15) # 5.5.7`
`at: 12/03/2010 shift:(0,-15) # 5.5.8`
`at: 07/02/2011 shift:(0,-15) # 5.5.9`
`at: 15/03/2011 shift:(0,-15) # 5.5.10`
`at: 07/04/2011 shift:(0,-15) # 5.5.11`
`at: 05/05/2011 shift:(0,-15) # 5.5.12`
`at: 31/05/2011 shift:(0,-15) # 5.5.13`
`at: 05/07/2011 shift:(0,-15) # 5.5.14`
`at: 28/07/2011 shift:(0,-15) # 5.5.15`
`at: 15/09/2011 shift:(0,-15) # 5.5.16`
`at: 19/10/2011 shift:(0,-15) # 5.5.17`
`at: 16/11/2011 shift:(0,-15) # 5.5.18`
`at: 08/12/2011 shift:(0,-15) # 5.5.19`
`at: 10/01/2012 shift:(0,-15) # 5.5.20`
`at: 17/02/2012 shift:(0,-15) # 5.5.21`
`at: 21/03/2012 shift:(0,-15) # 5.5.22`
`at: 12/04/2012 shift:(0,-15) # 5.5.23`
`at: 07/05/2012 shift:(0,-15) # 5.5.24`
`at: 30/05/2012 shift:(0,-15) # 5.5.25`
`at: 05/07/2012 shift:(0,-15) # 5.5.25a`
`at: 02/08/2012 shift:(0,-15) # 5.5.27`
`at: 28/09/2012 shift:(0,-15) # 5.5.28`

`##################################################`
`# 5.5 line & text for first version every year #`
`##################################################`
`bar:5.5 mark:(line,col2.0-l1) align:center fontsize:S textcolor:blue`
`at: 07/12/2009 text:"5.5.0 M2" shift:(45,-3)`
`at: 24/03/2010 text:"5.5.3 M3" shift:(45,-3)`
`at: 13/09/2010 text:"5.5.6 RC" shift:(45,-3)`
`at: 03/12/2010 text:"5.5.8 GA" shift:(45,-3)`
`at: 07/02/2011 text:"5.5.9" shift:(36,0)`
`at: 10/01/2012 text:"5.5.20" shift:(40,-3)`

1.  1.
`# 5.6 filled bar #`
`##################################################`
`bar:5.6 width:40 from:11/04/2011 till:$now color:col5.1 mark:(line,col5.1)`

`##################################################`
`# 5.6 line for all other versions #`
`##################################################`
`bar:5.6 mark:(line,col2.0-l2)`
`at: 11/04/2011 shift:(0,-15) # 5.6.2`
`at: 03/10/2011 shift:(0,-15) # 5.6.3`
`at: 20/12/2011 shift:(0,-15) # 5.6.4`
`at: 10/04/2012 shift:(0,-15) # 5.6.5`
`at: 07/08/2012 shift:(0,-15) # 5.6.6`
`at: 29/09/2012 shift:(0,-15) # 5.6.7`
`at: 07/11/2012 shift:(0,-15) # 5.6.8`
`at: 12/11/2012 shift:(0,-15) # 5.6.9`

`##################################################`
`# 5.6 line & text for first version every year #`
`##################################################`
`bar:5.6 mark:(line,col2.0-l1) align:center fontsize:S textcolor:blue`
`at: 11/04/2011 text:"5.6.2 M5" shift:(45,-3)`
`at: 04/10/2012 text:"5.6.5 M8" shift:(45,-3)`

</timeline> \[23\]\[24\]\[25\]\[26\]\[27\]\[28\]\[29\]

## 역사

버전 별 두드러진 특징은 다음과 같다.

  - [1994년](../Page/1994년.md "wikilink") MySQL의 원 개발(마이클 위데니우스와 데이빗 액스마크에 의한)\[30\]
  - [1995년](../Page/1995년.md "wikilink") 5월 최초의 국제화판
  - 3.19 판: 1996년 말, www.tcx.se에서
  - 3.20 판: 1997년 1월
  - [1998년](../Page/1998년.md "wikilink") 1월 8일 윈도 판(Windows 95와 NT) 출시
  - 3.21 판: 제품 출시 1998년 www.mysql.com 에서
  - 3.22 판: 1998년부터 알파, 베타판
  - 3.23 판: 2000년 7월 베타판으로부터, 2001년 1월 22일 제품 출시\[31\]
  - 4.0 판: 2002년 8월 베타판으로부터, 2003년 3월 제품 출시([unions](https://ko.wikipedia.org/wiki/Set_operations_\(SQL\) "wikilink"))
  - 4.01 판: 2003년 8월 베타판으로부터, Jyoti 데이터베이스 트래킹용으로 MySQL 채택
  - **4.1 판**: [2004년](../Page/2004년.md "wikilink") 6월 베타판으로부터, 2004년 10월 제품 출시 ([R 트리와](../Page/R_트리.md "wikilink") [B 트리](../Page/B_트리.md "wikilink"), [서브쿼리](https://ko.wikipedia.org/wiki/서브쿼리 "wikilink"), prepared statements 지원)
  - **5.0 판**: 2005년 3월 베타판, 2005년 10월 제품 출시([커서](../Page/데이터베이스_커서.md "wikilink"), [저장 프로시저](../Page/저장_프로시저.md "wikilink"), [트리거](../Page/데이터베이스_트리거.md "wikilink"), [뷰](https://ko.wikipedia.org/wiki/뷰_\(SQL\) "wikilink"), [XA 트랜잭션](../Page/데이터베이스_트랜잭션.md "wikilink") 지원)

<!-- end list -->

  -
    페더레이티드 스토리지 엔진의 개발자는 다음과 같은 말을 했다. "Federated 스토리지 엔진은 [proof-of-concept](../Page/개념_증명.md "wikilink") 스토리지 엔진이지만",\[32\] 주요 MySQL 5.0 판에 포함되어 기본값으로 활성화되어 있다. "MySQL Federated 테이블에 일부 단점들을 정리한 문서 : The Missing Manual".\[33\]

<!-- end list -->

  - [썬마이크로시스템즈](https://ko.wikipedia.org/wiki/썬마이크로시스템즈 "wikilink")는 2008년 [MySQL AB를](https://ko.wikipedia.org/wiki/MySQL_AB "wikilink") 인수했다.\[34\]
  - **5.1 판**: 2008년 11월 27일 출시(이벤트 스케줄러, [파티셔닝](https://ko.wikipedia.org/wiki/파티션_\(데이터베이스\) "wikilink"), 플러그인 API, 열 기반의 복제, [서버 로그](https://ko.wikipedia.org/wiki/서버_로그 "wikilink") 테이블)

<!-- end list -->

  -
    5.1 판에는 5.0에 있던 35개의 현재의 버그 외에 20개의 알려진 크래싱, 그리고 잘못된 결과 버그를 포함하고 있다. *(5.1.51판에는 거의 모두 픽스함)*.\[35\]
    MySQL 5.1과 6.0은 [데이터 웨어하우징으로](../Page/데이터_웨어하우스.md "wikilink") 사용할 때는 빈약한 성능을 보인다.  — 부분적으로 단일 쿼리를 진행할 때 다중 CPU 코어를 사용할 수 없기 때문에\[36\]

<!-- end list -->

  - [오라클](https://ko.wikipedia.org/wiki/오라클 "wikilink")이 2010년 1월 27일 [썬마이크로시스템즈](https://ko.wikipedia.org/wiki/썬마이크로시스템즈 "wikilink")를 인수했다.\[37\]
  - MySQL 서버 5.5는 현재 널리 사용가능하다(). 다음과 같은 성능 향상과 특징을 가지고 있다:
      - 기본 스토리지 엔진이 InnoDB이며, 이것은 트랜잭션과 참조 무결성 제한을 지원한다.
      - 개선된 InnoDB I/O 서브시스템\[38\]
      - 향상된 [SMP](https://ko.wikipedia.org/wiki/대칭형_다중_처리 "wikilink") 지원\[39\]
      - Semisynchronous 복제.
      - SQL 표준에 대응한 SIGNAL 과 RESIGNAL 구문.
      - 유니코드 문자셋 utf16, utf32, 그리고 utf8mb4 지원.
      - 사용자 정의 파티셔닝에 대한 새로운 옵션.

MySQL 서버 6.0.11-알파가 6.0 라인의 최신 판으로 2009년 5월 22일 발표되었다.\[40\] 이후의 MySQL 서버 개발은 새로운 릴리스 모델을 사용할 것이다. 6.0은 미리 출시판으로 통합될 것이다.

MySQL 5.6은 새로운 출시판의 시금석이 될 예정으로 2011년 MySQL 이용자 컨퍼런스에서 소개되었다. 새로운 특징으로 쿼리 옵티마이저에 대한 성능 향상과 InnoDB의 고성능 트랜잰션 결과, 새로운 [NoSQL](https://ko.wikipedia.org/wiki/NoSQL_\(concept\) "wikilink")-스타일 메모리 캐시된 API, 대용량 테이블의 조작과 퀘리를 위한 파티셔닝의 성능 향상, 복제와 성능 모니터링 개선을 PERFORMANCE_SCHEMA를 통해 데이터 확장으로 나은 성능을 보여줄 수 있게 되었다.\[41\]

## 같이 보기

  - [마리아 DB](https://ko.wikipedia.org/wiki/마리아_DB "wikilink")

## 각주

## 외부 링크

  - [MySQL 공식 홈페이지](http://www.mysql.com/)

  - [MySQL 5.5 Reference Manual](http://dev.mysql.com/doc/refman/5.5/en/index.html)

[MySQL](https://ko.wikipedia.org/wiki/분류:MySQL "wikilink") [분류:자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_소프트웨어 "wikilink") [분류:데이터베이스 관리 시스템](https://ko.wikipedia.org/wiki/분류:데이터베이스_관리_시스템 "wikilink") [분류:1995년 소프트웨어](https://ko.wikipedia.org/wiki/분류:1995년_소프트웨어 "wikilink") [분류:오라클 소프트웨어](https://ko.wikipedia.org/wiki/분류:오라클_소프트웨어 "wikilink") [분류:GPL 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:GPL_라이선스_소프트웨어 "wikilink") [분류:관계형 데이터베이스 관리 시스템](https://ko.wikipedia.org/wiki/분류:관계형_데이터베이스_관리_시스템 "wikilink") [분류:자유 데이터베이스 관리 시스템](https://ko.wikipedia.org/wiki/분류:자유_데이터베이스_관리_시스템 "wikilink")

1.
2.
3.
4.  [MySQL loses joint custody of SAP database](https://www.theregister.co.uk/2007/10/03/mysql_sap_netweaver_love-in/)
5.  [썬 마이크로시스템즈의 인수에 관한 기사](http://blogs.mysql.com/kaj/2008/01/16/sun-acquires-mysql/)
6.  [mysql — The MySQL Command-Line Tool](http://dev.mysql.com/doc/refman/5.5/en/mysql.html), MySQL Reference Manual
7.  [mysqladmin - the MySQL command-line tool](http://dev.mysql.com/doc/refman/5.5/en/mysqladmin.html), MySQL Reference Manual
8.  [MySQL Client Programs](http://dev.mysql.com/doc/refman/5.0/en/programs-client.html), MySQL Reference Manual
9.  [MySQL Tools Family](http://www.sqlmaestro.com/products/mysql/), SQLMaestro Group
10. [MySQL GUI Tools](http://www.webyog.com/en/) , WebYog
11. [HeidiSQL](http://www.heidisql.com/), HeidiSQL MySQL GUI
12. [MySQL Workbench](http://dev.mysql.com/downloads/workbench/), MySQL Downloads
13.
14.
15.
16.
17.
18.
19.
20.
21.
22.
23.
24.
25.
26.
27.
28.
29.
30.
31.
32.
33.
34.
35.
36.
37.
38.
39.
40.
41.