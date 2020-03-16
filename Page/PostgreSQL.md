> This article is converted from Wikipedia: [PostgreSQL](https://ko.wikipedia.org/wiki/PostgreSQL).


**PostgreSQL**은 확장 가능성 및 표준 준수를 강조하는 [객체-관계형 데이터베이스 관리 시스템](../Page/객체_관계_데이터베이스.md "wikilink")(ORDBMS)의 하나이다. BSD 허가권으로 배포되며 오픈소스 개발자 및 관련 회사들이 개발에 참여하고 있다. 데이터베이스 서버로서 주요 기능은 데이터를 안전하게 저장하고 다른 응용 소프트웨어로부터의 요청에 응답할 때 데이터를 반환하는 것이이다. 소규모의 단일 머신 애플리케이션에서부터 수많은 동시 접속 사용자가 있는 대형의 [인터넷 애플리케이션](../Page/웹_서비스.md "wikilink")(또는 [데이터 웨어하우스용](../Page/데이터_웨어하우스.md "wikilink"))에 이르기까지 여러 부하를 관리할 수 있으며 [macOS 서버의](https://ko.wikipedia.org/wiki/macOS_서버 "wikilink") 경우 PostgreSQL은 기본 데이터베이스이다.\[1\] \[2\]\[3\] [마이크로소프트 윈도우](../Page/마이크로소프트_윈도우.md "wikilink"), [리눅스](../Page/리눅스.md "wikilink")(대부분의 배포판에서 제공됨)용으로도 이용 가능하다.

## 이름

PostgreSQL이라는 이름의 어감이 생소해서 발음할 때 멈칫거리게 만들지만 발음은 생각보다 쉽다. /포ː스트그레스큐ː엘/ 조금 더 짧게 "포스트그레스큐엘"이라고 발음 하면 된다. 일부 프로그래머들 사이에는 "포스트그리 에스큐엘"이라고 불린다. 이전에는 일반적으로 "Postgres"라고만 불렸지만 표준 SQL을 지원하기 시작하면서 공동체에서 "Postgres"라는 이름 뒤에 SQL을 뒤에 덧붙인 것이다. 실제로 프로젝트의 공식적인 명칭은 "post-Ingres" 데이터베이스이다.

## 발자취

PostgreSQL은 캘리포니아대학교 버클리 분교에서 시작된 Ingres 프로젝트로부터 시작되었다. 프로젝트 리더인 Michael Stonebraker는 1982년 Ingres의 상용화를 위해 학교를 떠났다.

그 후, 1985년에 다시 학교로 돌아온 그는 1980년대 초반부터 급증하게 된 당시의 데이터베이스 시스템의 문제점들을 해결하고자 "post-Ingres"(후기-Ingres)프로젝트를 시작했다. 상용화 된 Ingres와는 다르게 post-Ingres에 대한 아이디어를 공유하기 위해 Ingres의 코드를 일부를 제외하고 분리시켰다.

1986년부터 개발팀은 데이터베이스 시스템의 기본적인 사항에 대해 몇 가지 논문을 제출하고 이어서 1988년까지 실제로 운영이 가능한 프로토타입을 완성한다.

1989년 6월 그들은 첫 번째 버전과 그 이듬해 6월까지 시스템 규칙을 재작성하는 두 번째 버전까지 소수의 사용자들에게만 공개했다. 1991년 세 번째 버전에서도 시스템의 규칙을 다시 썼다. 또한 다중 스토리지 관리자 및 향상된 질의엔진에 대한 지원을 추가했다. 1993년까지 많은 사용자들이 이 시스템을 사용했고 이 시스템의 지원에 관한 요청이 쇄도하기 시작했다.

개발팀이 네 번째 버전을 내놓은 후 일차적인 프로젝트가 공식적으로는 종료되었으나, BSD 허가권으로 인해 오픈소스 개발자들은 Postgres 시스템의 소스코드를 넘겨받아 개발을 계속했다.

1994년 캘리포니아대학교 버클리분교의 졸업생인 앤드류 유와 졸리 첸이 SQL의 해석기를 추가하고 기존 Ingres 기반의 질의 시스템을 대체한다. 이를 "Postgres95" 라고 한다.

1996년에는 기존의 데이터베이스 시스템에 새로운 SQL이 추가되었다는 것을 알리기 위해 Postgres95라는 이름을 PostgreSQL로 바꾼다.

1997년 PostgreSQL의 첫 번째 버전인 6.0 부터 전 세계의 데이터베이스 개발자와 자원자들이 조직을 형성하고 인터넷을 통해 협력하면서 시스템의 개발과 유지보수를 한다.

PostgreSQL을 상용 버전으로 만들 수는 있었으나, 과거와 같이 급속도로 개발되지는 않았다.

상용 PostgreSQL의 대표적인 것으로는 Paula Hawthorn\[4\]과 Michael Stonebraker가 세운 Illustra Information Technologies의 상용버전이 있다.

## 특장점

### 유연한 객체 생성

다른 관계형 데이터베이스 시스템과 달리, 연산자, 복합 자료형, 집계 함수, 자료형 변환자, 확장 기능 등 다양한 데이터베이스 객체를 사용자가 임의로 만들 수 있는 기능을 SQL 차원에서 제공한다.

이런 특징은 단순한 자료 저장소로써의 기능을 넘어 마치 하나의 새로운 프로그래밍 언어처럼 개발자의 창의성에 따라 무한한 기능을 손쉽게 구현할 수 있도록 한다.

### 상속

java 또는 C++ 프로그래밍 언어와 같이 테이블을 만들어 그 테이블 상속 기능을 이용해 하위 테이블을 만들 수 있다.

테이블에 저장된 자료는 상위 테이블을 조회하면, 해당 테이블의 하위 테이블에 포함된 모든 자료를 조회할 수 있으며, 하위 테이블을 만들 때, 상위 테이블의 칼럼을 그대로 상속 받으면서, 하위 테이블에만 속하는 칼럼을 추가로 만들 수 있다.

### 함수

때때로, '저장 프로시저'라고 불리는 SQL문으로 작성된 함수를 서버환경에서 사용할 수 있다. 비록 다른 언어와는 달리 제어문과 반복문을 사용하지는 못하지만, 다른 언어와 결합시킬 수 있다. 일부 언어에서는 심지어 트리거 내부에서 실행시킬 수 있다.

이러한 언어의 예는 다음과 같다.

  - PL/pgSQL (오라클의 PL/SQL과 유사하다)
  - 스크립트 언어를 통한 지원 (예, PL/Python, PL/php, PL/Perl)
  - 컴파일 언어를 통한 지원 (예, C/C++, PL/Java)
  - 통계적 언어를 통한 지원 (예, PL/R)

PostgreSQL은 테이블에 대한 질의 결과를 반환하기 위한 '행 반환 함수'를 지원한다.

실행권한은 함수 작성자 및, 실행자 모두에게 있다.

## 데이터베이스 관리 도구

### 서버 도구

#### postgres

최상위 서버 [데몬](../Page/데몬_\(컴퓨팅\).md "wikilink")

#### pg_ctl

서버 시작, 중지, 상태 등 서버 제어를 위한 명령어

#### initdb

데이터베이스 초기화 명령어

#### pg_resetxlog

트랜잭션 로그 초기화 명령어

### 클라이언트 도구

#### psql

기초적인 관리 툴은 `psql`이다. psql의 특징으로는 명령어 기반 인터페이스라는 점이며 셸과 유사한 자동완성 및 스크립트를 통한 자동화 기능을 지원한다.

#### pgAdmin

[pgAdmin](http://www.pgadmin.org/)은 그래픽 사용자 인터페이스를 지닌 툴로서 다수의 운영체제에서 작동하며, 배포는 [아티스틱 라이선스를](../Page/아티스틱_라이선스.md "wikilink") 따른다. PostgreSQL 6.3.2 버전부터 지원하기 시작했으며 개발초기의 이름은 pgManager였다. 현재는 pgAdmin 4이다.

#### phpPgAdmin

[phpPgAdmin](http://phppgadmin.sourceforge.net)은 웹 기반의 관리 툴이다. phpMyAdmin과 인터페이스가 거의 똑같이 구성되어있으며 PHP로 작성되었다.

## 출시 역사

{{\#tag:timeline|

1.  References:
2.  <http://www.postgresql.org/support/versioning/>
3.  <http://www.postgresql.org/docs/current/static/release.html>
4.  git log --tags --simplify-by-decoration --date=format:'%d/%m/%Y' --pretty="format:%ad %d"

Define $width = 860 Define $height = 460

Define $start = 01/01/1995 Define $end = 01/01/{{\#time: Y | +6 year }} \# major releases are supported for 5 years Define $now = {{\#time: d/m/Y }}

ImageSize = width:$width height:$height PlotArea = right:30 left:60 bottom:60 top:60 DateFormat = dd/mm/yyyy TimeAxis = orientation:horizontal AlignBars = justify Period = from:$start till:$end Legend = orientation:vertical position:bottom columns:4 columnwidth:140

Colors =

`   id:bg       value:white`
`   id:lighttext value:rgb(0.8,0.8,0.8)`
`   id:alpha    value:rgb(0.9,0.84,1)`
`   id:beta     value:rgb(1,0.8,0)`
`   id:RC       value:rgb(0,0.83,0.67)`
`   id:major    value:black`
`   id:minor    value:rgb(0.4,0.4,0.4)`
`   id:today    value:rgb(1,0.5,0.5)`
`   id:devel    value:rgb(0.86,1,0.33) Legend:Development`
`   id:prod     value:rgb(0,0.58,0.77) Legend:Production`
`   id:eol      value:rgb(0.6,0.6,0.6) Legend:Expected_EOL`

BackgroundColors = canvas:bg ScaleMajor = gridcolor:lighttext unit:year increment:1 start:01/01/1995

Define $bw = 10 \# bar width

1.  Shift text placement

Define $dy = -5 Define $dx = 2

LineData=

`  at:$now color:today width:0.1`

PlotData=

` bar:11 width:$bw color:devel align:left fontsize:M`
`   from:24/05/2018 till:05/10/2018 # REL11_BETA1, with estimated development 'till'`
`   at:24/05/2018 mark:(line,beta)  # 11 Beta 1`
`   at:28/06/2018 mark:(line,beta)  # 11 Beta 2`
`   at:09/08/2018 mark:(line,beta)  # 11 Beta 3`
`   at:20/09/2018 mark:(line,beta)  # 11 Beta 4`
`   at:21/10/2018 mark:(line,RC)    # 11 RC1`
`   barset:break color:prod from:18/10/2018 till:09/11/2023`
`   at:18/10/2018 mark:(line,major) # 11.0`
`   at:08/11/2018 mark:(line,minor) # 11.1`
`   at:$now shift:($dx,$dy) text:11.1`
`   barset:break color:eol from:$now till:09/11/2023`

` bar:10 width:$bw color:devel align:left fontsize:M`
`   from:18/05/2017 till:05/10/2017 # REL10_BETA1`
`   at:18/05/2017 mark:(line,beta)  # 10 Beta 1`
`   at:13/07/2017 mark:(line,beta)  # 10 Beta 2`
`   at:10/08/2017 mark:(line,beta)  # 10 Beta 3`
`   at:31/08/2017 mark:(line,beta)  # 10 Beta 4`
`   at:21/09/2017 mark:(line,RC)    # 10 RC1`
`   barset:break color:prod from:05/10/2017 till:30/10/2022`
`   at:05/10/2017 mark:(line,major) # 10.0`
`   at:09/11/2017 mark:(line,minor) # 10.1`
`   at:08/02/2018 mark:(line,minor) # 10.2`
`   at:01/03/2018 mark:(line,minor) # 10.3`
`   at:10/05/2018 mark:(line,minor) # 10.4`
`   at:09/08/2018 mark:(line,minor) # 10.5`
`   at:08/11/2018 mark:(line,minor) # 10.6`
`   at:$now shift:($dx,$dy) text:10.6`
`   barset:break color:eol from:$now till:30/10/2022`

` bar:9.6 width:$bw color:devel align:left fontsize:M`
`   from:09/05/2016 till:29/09/2016 # REL9_6_BETA1`
`   at:12/05/2016 mark:(line,beta)  # 9.6 Beta 1`
`   at:23/06/2016 mark:(line,beta)  # 9.6 Beta 2`
`   at:21/07/2016 mark:(line,beta)  # 9.6 Beta 3`
`   at:11/08/2016 mark:(line,beta)  # 9.6 Beta 4`
`   at:01/09/2016 mark:(line,RC)    # 9.6 RC1`
`   barset:break color:prod from:29/09/2016 till:$now`
`   at:29/09/2016 mark:(line,major) # 9.6`
`   at:27/10/2016 mark:(line,minor) # 9.6.1`
`   at:09/03/2017 mark:(line,minor) # 9.6.2`
`   at:11/05/2017 mark:(line,minor) # 9.6.3`
`   at:10/08/2017 mark:(line,minor) # 9.6.4`
`   at:31/08/2017 mark:(line,minor) # 9.6.5`
`   at:09/11/2017 mark:(line,minor) # 9.6.6`
`   at:08/02/2018 mark:(line,minor) # 9.6.7`
`   at:01/03/2018 mark:(line,minor) # 9.6.8`
`   at:10/05/2018 mark:(line,minor) # 9.6.9`
`   at:09/08/2018 mark:(line,minor) # 9.6.10`
`   at:08/11/2018 mark:(line,minor) # 9.6.11`
`   at:$now shift:($dx,$dy) text:9.6.11`
`   barset:break color:eol from:$now till:30/09/2021`

` bar:9.5 width:$bw color:devel align:left fontsize:M`
`   from:29/06/2015 till:08/10/2015 # REL9_5_ALPHA1`
`   at:02/07/2015 mark:(line,alpha) # 9.5 Alpha 1`
`   at:06/08/2015 mark:(line,alpha) # 9.5 Alpha 2`
`   at:08/10/2015 mark:(line,beta)  # 9.5 Beta 1`
`   at:12/11/2015 mark:(line,beta)  # 9.5 Beta 2`
`   at:18/12/2015 mark:(line,RC)    # 9.5 RC1`
`   barset:break color:prod from:07/01/2016 till:$now`
`   at:07/01/2016 mark:(line,major) # 9.5`
`   at:11/02/2016 mark:(line,minor) # 9.5.1`
`   at:31/03/2016 mark:(line,minor) # 9.5.2`
`   at:13/05/2016 mark:(line,minor) # 9.5.3`
`   at:11/08/2016 mark:(line,minor) # 9.5.4`
`   at:27/10/2016 mark:(line,minor) # 9.5.5`
`   at:09/03/2017 mark:(line,minor) # 9.5.6`
`   at:11/05/2017 mark:(line,minor) # 9.5.7`
`   at:10/08/2017 mark:(line,minor) # 9.5.8`
`   at:31/08/2017 mark:(line,minor) # 9.5.9`
`   at:09/11/2017 mark:(line,minor) # 9.5.10`
`   at:08/02/2018 mark:(line,minor) # 9.5.11`
`   at:01/03/2018 mark:(line,minor) # 9.5.12`
`   at:10/05/2018 mark:(line,minor) # 9.5.13`
`   at:09/08/2018 mark:(line,minor) # 9.5.14`
`   at:08/11/2018 mark:(line,minor) # 9.5.15`
`   at:$now shift:($dx,$dy) text:9.5.15`
`   barset:break color:eol from:$now till:30/01/2021`

` bar:9.4 width:$bw color:devel align:left fontsize:M`
`   from:11/05/2014 till:18/12/2014 # REL9_4_BETA1`
`   at:15/05/2014 mark:(line,beta)  # 9.4 Beta 1`
`   at:24/07/2014 mark:(line,beta)  # 9.4 Beta 2`
`   at:09/10/2014 mark:(line,beta)  # 9.4 Beta 3`
`   at:20/11/2014 mark:(line,RC)    # 9.4 RC1`
`   barset:break color:prod from:18/12/2014 till:$now`
`   at:18/12/2014 mark:(line,major) # 9.4`
`   at:05/02/2015 mark:(line,minor) # 9.4.1`
`   at:22/05/2015 mark:(line,minor) # 9.4.2`
`   at:04/06/2015 mark:(line,minor) # 9.4.3`
`   at:12/06/2015 mark:(line,minor) # 9.4.4`
`   at:08/10/2015 mark:(line,minor) # 9.4.5`
`   at:11/02/2016 mark:(line,minor) # 9.4.6`
`   at:31/03/2016 mark:(line,minor) # 9.4.7`
`   at:13/05/2016 mark:(line,minor) # 9.4.8`
`   at:11/08/2016 mark:(line,minor) # 9.4.9`
`   at:27/10/2016 mark:(line,minor) # 9.4.10`
`   at:09/03/2017 mark:(line,minor) # 9.4.11`
`   at:11/05/2017 mark:(line,minor) # 9.4.12`
`   at:10/08/2017 mark:(line,minor) # 9.4.13`
`   at:31/08/2017 mark:(line,minor) # 9.4.14`
`   at:09/11/2017 mark:(line,minor) # 9.4.15`
`   at:08/02/2018 mark:(line,minor) # 9.4.16`
`   at:01/03/2018 mark:(line,minor) # 9.4.17`
`   at:10/05/2018 mark:(line,minor) # 9.4.18`
`   at:09/08/2018 mark:(line,minor) # 9.4.19`
`   at:08/11/2018 mark:(line,minor) # 9.4.20`
`   at:$now shift:($dx,$dy) text:9.4.20`
`   barset:break color:eol from:$now till:30/12/2019`

` bar:9.3 width:$bw color:devel align:left fontsize:M`
`   from:06/05/2013 till:09/09/2013 # REL9_3_BETA1`
`   at:13/05/2013 mark:(line,beta)  # 9.3 Beta 1`
`   at:27/06/2013 mark:(line,beta)  # 9.3 Beta 2`
`   at:22/08/2013 mark:(line,RC)    # 9.3 RC1`
`   barset:break color:prod from:09/09/2013 till:08/11/2018`
`   at:09/09/2013 mark:(line,major) # 9.3`
`   at:10/10/2013 mark:(line,minor) # 9.3.1`
`   at:05/12/2013 mark:(line,minor) # 9.3.2`
`   at:20/02/2014 mark:(line,minor) # 9.3.3`
`   at:20/03/2014 mark:(line,minor) # 9.3.4`
`   at:24/07/2014 mark:(line,minor) # 9.3.5`
`   at:05/02/2015 mark:(line,minor) # 9.3.6`
`   at:22/05/2015 mark:(line,minor) # 9.3.7`
`   at:04/06/2015 mark:(line,minor) # 9.3.8`
`   at:12/06/2015 mark:(line,minor) # 9.3.9`
`   at:08/10/2015 mark:(line,minor) # 9.3.10`
`   at:11/02/2016 mark:(line,minor) # 9.3.11`
`   at:31/03/2016 mark:(line,minor) # 9.3.12`
`   at:13/05/2016 mark:(line,minor) # 9.3.13`
`   at:11/08/2016 mark:(line,minor) # 9.3.14`
`   at:27/10/2016 mark:(line,minor) # 9.3.15`
`   at:09/03/2017 mark:(line,minor) # 9.3.16`
`   at:11/05/2017 mark:(line,minor) # 9.3.17`
`   at:10/08/2017 mark:(line,minor) # 9.3.18`
`   at:31/08/2017 mark:(line,minor) # 9.3.19`
`   at:09/11/2017 mark:(line,minor) # 9.3.20`
`   at:08/02/2018 mark:(line,minor) # 9.3.21`
`   at:01/03/2018 mark:(line,minor) # 9.3.22`
`   at:10/05/2018 mark:(line,minor) # 9.3.23`
`   at:09/08/2018 mark:(line,minor) # 9.3.24`
`   at:08/11/2018 mark:(line,minor) shift:($dx,$dy) text:9.3.25`

` bar:9.2 width:$bw color:devel align:left fontsize:M`
`   from:10/05/2012 till:10/09/2012 # REL9_2_BETA1`
`   at:14/05/2012 mark:(line,beta)  # 9.2 Beta 1`
`   at:31/05/2012 mark:(line,beta)  # 9.2 Beta 2 *est from tag`
`   at:06/08/2012 mark:(line,beta)  # 9.2 Beta 3`
`   at:14/08/2012 mark:(line,beta)  # 9.2 Beta 4 *est from tag`
`   at:27/08/2012 mark:(line,RC)    # 9.2 RC1`
`   barset:break color:prod from:10/09/2012 till:09/11/2017`
`   at:10/09/2012 mark:(line,major) # 9.2`
`   at:24/09/2012 mark:(line,minor) # 9.2.1`
`   at:06/12/2012 mark:(line,minor) # 9.2.2`
`   at:07/02/2013 mark:(line,minor) # 9.2.3`
`   at:04/04/2013 mark:(line,minor) # 9.2.4`
`   at:10/10/2013 mark:(line,minor) # 9.2.5`
`   at:05/12/2013 mark:(line,minor) # 9.2.6`
`   at:20/02/2014 mark:(line,minor) # 9.2.7`
`   at:20/03/2014 mark:(line,minor) # 9.2.8`
`   at:24/07/2014 mark:(line,minor) # 9.2.9`
`   at:05/02/2015 mark:(line,minor) # 9.2.10`
`   at:22/05/2015 mark:(line,minor) # 9.2.11`
`   at:04/06/2015 mark:(line,minor) # 9.2.12`
`   at:12/06/2015 mark:(line,minor) # 9.2.13`
`   at:08/10/2015 mark:(line,minor) # 9.2.14`
`   at:11/02/2016 mark:(line,minor) # 9.2.15`
`   at:31/03/2016 mark:(line,minor) # 9.2.16`
`   at:13/05/2016 mark:(line,minor) # 9.2.17`
`   at:11/08/2016 mark:(line,minor) # 9.2.18`
`   at:27/10/2016 mark:(line,minor) # 9.2.19`
`   at:09/03/2017 mark:(line,minor) # 9.2.20`
`   at:11/05/2017 mark:(line,minor) # 9.2.21`
`   at:10/08/2017 mark:(line,minor) # 9.2.22`
`   at:31/08/2017 mark:(line,minor) # 9.2.23`
`   at:09/11/2017 mark:(line,minor) shift:($dx,$dy) text:9.2.24`

` bar:9.1 width:$bw color:devel align:left fontsize:M`
`   from:03/09/2010 till:12/09/2011 # REL9_1_ALPHA1`
`   at:07/09/2010 mark:(line,alpha) # 9.1 Alpha 1`
`   at:01/11/2010 mark:(line,alpha) # 9.1 Alpha 2`
`   at:30/12/2010 mark:(line,alpha) # 9.1 Alpha 3`
`   at:20/02/2011 mark:(line,alpha) # 9.1 Alpha 4`
`   at:29/03/2011 mark:(line,alpha) # 9.1 Alpha 5`
`   at:01/05/2011 mark:(line,beta)  # 9.1 Beta 1`
`   at:12/06/2011 mark:(line,beta)  # 9.1 Beta 2`
`   at:11/07/2011 mark:(line,beta)  # 9.1 Beta 3`
`   at:22/08/2011 mark:(line,RC)    # 9.1 RC1`
`   barset:break color:prod from:12/09/2011 till:27/10/2016`
`   at:12/09/2011 mark:(line,major) # 9.1`
`   at:26/09/2011 mark:(line,minor) # 9.1.1`
`   at:05/12/2011 mark:(line,minor) # 9.1.2`
`   at:27/02/2012 mark:(line,minor) # 9.1.3`
`   at:04/06/2012 mark:(line,minor) # 9.1.4`
`   at:17/08/2012 mark:(line,minor) # 9.1.5`
`   at:24/09/2012 mark:(line,minor) # 9.1.6`
`   at:06/12/2012 mark:(line,minor) # 9.1.7`
`   at:07/02/2013 mark:(line,minor) # 9.1.8`
`   at:04/04/2013 mark:(line,minor) # 9.1.9`
`   at:10/10/2013 mark:(line,minor) # 9.1.10`
`   at:05/12/2013 mark:(line,minor) # 9.1.11`
`   at:20/02/2014 mark:(line,minor) # 9.1.12`
`   at:20/03/2014 mark:(line,minor) # 9.1.13`
`   at:24/07/2014 mark:(line,minor) # 9.1.14`
`   at:05/02/2015 mark:(line,minor) # 9.1.15`
`   at:22/05/2015 mark:(line,minor) # 9.1.16`
`   at:04/06/2015 mark:(line,minor) # 9.1.17`
`   at:12/06/2015 mark:(line,minor) # 9.1.18`
`   at:08/10/2015 mark:(line,minor) # 9.1.19`
`   at:11/02/2016 mark:(line,minor) # 9.1.20`
`   at:31/03/2016 mark:(line,minor) # 9.1.21`
`   at:13/05/2016 mark:(line,minor) # 9.1.22`
`   at:11/08/2016 mark:(line,minor) # 9.1.23`
`   at:27/10/2016 mark:(line,minor) shift:($dx,$dy) text:9.1.24`

` bar:9.0 width:$bw color:devel align:left fontsize:M`
`   from:19/08/2009 till:20/09/2010 # REL8_5_ALPHA1`
`   at:24/08/2009 mark:(line,alpha) # 8.5 Alpha 1`
`   at:24/10/2009 mark:(line,alpha) # 8.5 Alpha 2`
`   at:21/12/2009 mark:(line,alpha) # 8.5 Alpha 3`
`   at:24/02/2010 mark:(line,alpha) # 9.0 Alpha 4`
`   at:01/04/2010 mark:(line,alpha) # 9.0 Alpha 5 *est from tag`
`   at:29/04/2010 mark:(line,beta)  # 9.0 Beta 1`
`   at:04/06/2010 mark:(line,beta)  # 9.0 Beta 2`
`   at:12/07/2010 mark:(line,beta)  # 9.0 Beta 3`
`   at:02/08/2010 mark:(line,beta)  # 9.0 Beta 4`
`   at:28/08/2010 mark:(line,RC)    # 9.0 RC1`
`   barset:break color:prod from:20/09/2010 till:08/10/2015 # policy has end date for 30/09/2015, the last planned release was made a week after`
`   at:20/09/2010 mark:(line,major) # 9.0`
`   at:04/10/2010 mark:(line,minor) # 9.0.1`
`   at:16/12/2010 mark:(line,minor) # 9.0.2`
`   at:31/01/2011 mark:(line,minor) # 9.0.3`
`   at:18/04/2011 mark:(line,minor) # 9.0.4`
`   at:26/09/2011 mark:(line,minor) # 9.0.5`
`   at:05/12/2011 mark:(line,minor) # 9.0.6`
`   at:27/02/2012 mark:(line,minor) # 9.0.7`
`   at:04/06/2012 mark:(line,minor) # 9.0.8`
`   at:17/08/2012 mark:(line,minor) # 9.0.9`
`   at:24/09/2012 mark:(line,minor) # 9.0.10`
`   at:06/12/2012 mark:(line,minor) # 9.0.11`
`   at:07/02/2013 mark:(line,minor) # 9.0.12`
`   at:04/04/2013 mark:(line,minor) # 9.0.13`
`   at:10/10/2013 mark:(line,minor) # 9.0.14`
`   at:05/12/2013 mark:(line,minor) # 9.0.15`
`   at:20/02/2014 mark:(line,minor) # 9.0.16`
`   at:20/03/2014 mark:(line,minor) # 9.0.17`
`   at:24/07/2014 mark:(line,minor) # 9.0.18`
`   at:05/02/2015 mark:(line,minor) # 9.0.19`
`   at:22/05/2015 mark:(line,minor) # 9.0.20`
`   at:04/06/2015 mark:(line,minor) # 9.0.21`
`   at:12/06/2015 mark:(line,minor) # 9.0.22`
`   at:08/10/2015 mark:(line,minor) shift:($dx,$dy) text:9.0.23`

` bar:8.4 width:$bw color:devel align:left fontsize:M`
`   from:10/04/2009 till:01/07/2009 # REL8_4_BETA1`
`   at:15/04/2009 mark:(line,beta)  # 8.4 Beta 1`
`   at:20/05/2009 mark:(line,beta)  # 8.4 Beta 2`
`   at:14/06/2009 mark:(line,RC)    # 8.4 RC1`
`   at:22/06/2009 mark:(line,RC)    # 8.4 RC2 *est from tag`
`   barset:break color:prod from:01/07/2009 till:24/07/2014`
`   at:01/07/2009 mark:(line,major) # 8.4`
`   at:09/09/2009 mark:(line,minor) # 8.4.1`
`   at:14/12/2009 mark:(line,minor) # 8.4.2`
`   at:15/03/2010 mark:(line,minor) # 8.4.3`
`   at:17/05/2010 mark:(line,minor) # 8.4.4`
`   at:04/10/2010 mark:(line,minor) # 8.4.5`
`   at:16/12/2010 mark:(line,minor) # 8.4.6`
`   at:31/01/2011 mark:(line,minor) # 8.4.7`
`   at:18/04/2011 mark:(line,minor) # 8.4.8`
`   at:26/09/2011 mark:(line,minor) # 8.4.9`
`   at:05/12/2011 mark:(line,minor) # 8.4.10`
`   at:27/02/2012 mark:(line,minor) # 8.4.11`
`   at:04/06/2012 mark:(line,minor) # 8.4.12`
`   at:17/08/2012 mark:(line,minor) # 8.4.13`
`   at:24/09/2012 mark:(line,minor) # 8.4.14`
`   at:06/12/2012 mark:(line,minor) # 8.4.15`
`   at:07/02/2013 mark:(line,minor) # 8.4.16`
`   at:04/04/2013 mark:(line,minor) # 8.4.17`
`   at:10/10/2013 mark:(line,minor) # 8.4.18`
`   at:05/12/2013 mark:(line,minor) # 8.4.19`
`   at:20/02/2014 mark:(line,minor) # 8.4.20`
`   at:20/03/2014 mark:(line,minor) # 8.4.21`
`   at:24/07/2014 mark:(line,minor) shift:($dx,$dy) text:8.4.22`

` bar:8.3 width:$bw color:devel align:left fontsize:M`
`   from:05/10/2007 till:04/02/2008 # REL8_3_BETA1`
`   at:08/10/2007 mark:(line,beta)  # 8.3 Beta 1`
`   at:30/10/2007 mark:(line,beta)  # 8.3 Beta 2`
`   at:16/11/2007 mark:(line,beta)  # 8.3 Beta 3 *est from tag`
`   at:03/12/2007 mark:(line,beta)  # 8.3 Beta 4 *`
`   at:08/01/2008 mark:(line,RC)    # 8.3 RC1`
`   at:21/01/2008 mark:(line,RC)    # 8.3 RC2`
`   barset:break color:prod from:04/02/2008 till:07/02/2013`
`   at:04/02/2008 mark:(line,major) # 8.3`
`   at:17/03/2008 mark:(line,minor) # 8.3.1`
`   at:12/06/2008 mark:(line,minor) # 8.3.3`
`   at:22/09/2008 mark:(line,minor) # 8.3.4`
`   at:03/11/2008 mark:(line,minor) # 8.3.5`
`   at:02/02/2009 mark:(line,minor) # 8.3.6`
`   at:16/03/2009 mark:(line,minor) # 8.3.7`
`   at:09/09/2009 mark:(line,minor) # 8.3.8`
`   at:14/12/2009 mark:(line,minor) # 8.3.9`
`   at:15/03/2010 mark:(line,minor) # 8.3.10`
`   at:17/05/2010 mark:(line,minor) # 8.3.11`
`   at:04/10/2010 mark:(line,minor) # 8.3.12`
`   at:16/12/2010 mark:(line,minor) # 8.3.13`
`   at:31/01/2011 mark:(line,minor) # 8.3.14`
`   at:18/04/2011 mark:(line,minor) # 8.3.15`
`   at:26/09/2011 mark:(line,minor) # 8.3.16`
`   at:05/12/2011 mark:(line,minor) # 8.3.17`
`   at:27/02/2012 mark:(line,minor) # 8.3.18`
`   at:04/06/2012 mark:(line,minor) # 8.3.19`
`   at:17/08/2012 mark:(line,minor) # 8.3.20`
`   at:24/09/2012 mark:(line,minor) # 8.3.21`
`   at:06/12/2012 mark:(line,minor) # 8.3.22`
`   at:07/02/2013 mark:(line,minor) shift:($dx,$dy) text:8.3.23`

` bar:8.2 width:$bw color:devel align:left fontsize:M`
`   from:23/09/2006 till:05/12/2006 # REL8_2_BETA1`
`   at:30/09/2006 mark:(line,beta)  # 8.2 Beta 1`
`   at:26/10/2006 mark:(line,beta)  # 8.2 Beta 2`
`   at:09/11/2006 mark:(line,beta)  # 8.2 Beta 3`
`   at:27/11/2006 mark:(line,RC)    # 8.2 RC1`
`   barset:break color:prod from:05/12/2006 till:05/12/2011`
`   at:05/12/2006 mark:(line,major) # 8.2`
`   at:08/01/2007 mark:(line,minor) # 8.2.1`
`   at:05/02/2007 mark:(line,minor) # 8.2.2`
`   at:07/02/2007 mark:(line,minor) # 8.2.3`
`   at:23/04/2007 mark:(line,minor) # 8.2.4`
`   at:17/09/2007 mark:(line,minor) # 8.2.5`
`   at:07/01/2008 mark:(line,minor) # 8.2.6`
`   at:17/03/2008 mark:(line,minor) # 8.2.7`
`   at:12/06/2008 mark:(line,minor) # 8.2.9`
`   at:22/09/2008 mark:(line,minor) # 8.2.10`
`   at:03/11/2008 mark:(line,minor) # 8.2.11`
`   at:02/02/2009 mark:(line,minor) # 8.2.12`
`   at:16/03/2009 mark:(line,minor) # 8.2.13`
`   at:09/09/2009 mark:(line,minor) # 8.2.14`
`   at:14/12/2009 mark:(line,minor) # 8.2.15`
`   at:15/03/2010 mark:(line,minor) # 8.2.16`
`   at:17/05/2010 mark:(line,minor) # 8.2.17`
`   at:04/10/2010 mark:(line,minor) # 8.2.18`
`   at:16/12/2010 mark:(line,minor) # 8.2.19`
`   at:31/01/2011 mark:(line,minor) # 8.2.20`
`   at:18/04/2011 mark:(line,minor) # 8.2.21`
`   at:26/09/2011 mark:(line,minor) # 8.2.22`
`   at:05/12/2011 mark:(line,minor) shift:($dx,$dy) text:8.2.23`

` bar:8.1 width:$bw color:devel align:left fontsize:M`
`   from:24/08/2005 till:08/11/2005 # REL8_1_0BETA1`
`   at:25/08/2005 mark:(line,beta)  # 8.1 Beta 1`
`   at:18/09/2005 mark:(line,beta)  # 8.1 Beta 2`
`   at:13/10/2005 mark:(line,beta)  # 8.1 Beta 3`
`   at:24/10/2005 mark:(line,beta)  # 8.1 Beta 4`
`   at:30/10/2005 mark:(line,RC)    # 8.1 RC1`
`   barset:break color:prod from:08/11/2005 till:16/12/2010`
`   at:08/11/2005 mark:(line,major) # 8.1`
`   at:12/12/2005 mark:(line,minor) # 8.1.1`
`   at:09/01/2006 mark:(line,minor) # 8.1.2`
`   at:14/02/2006 mark:(line,minor) # 8.1.3`
`   at:23/05/2006 mark:(line,minor) # 8.1.4`
`   at:16/10/2006 mark:(line,minor) # 8.1.5`
`   at:08/01/2007 mark:(line,minor) # 8.1.6`
`   at:05/02/2007 mark:(line,minor) # 8.1.7`
`   at:07/02/2007 mark:(line,minor) # 8.1.8`
`   at:23/04/2007 mark:(line,minor) # 8.1.9`
`   at:17/09/2007 mark:(line,minor) # 8.1.10`
`   at:07/01/2008 mark:(line,minor) # 8.1.11`
`   at:12/06/2008 mark:(line,minor) # 8.1.13`
`   at:22/09/2008 mark:(line,minor) # 8.1.14`
`   at:03/11/2008 mark:(line,minor) # 8.1.15`
`   at:02/02/2009 mark:(line,minor) # 8.1.16`
`   at:16/03/2009 mark:(line,minor) # 8.1.17`
`   at:09/09/2009 mark:(line,minor) # 8.1.18`
`   at:14/12/2009 mark:(line,minor) # 8.1.19`
`   at:15/03/2010 mark:(line,minor) # 8.1.20`
`   at:17/05/2010 mark:(line,minor) # 8.1.21`
`   at:04/10/2010 mark:(line,minor) # 8.1.22`
`   at:16/12/2010 mark:(line,minor) shift:($dx,$dy) text:8.1.23`

` bar:8.0 width:$bw color:devel align:left fontsize:M`
`   from:09/08/2004 till:19/01/2005 # REL8_0_0BETA1`
`   at:10/08/2004 mark:(line,beta)  # 8.0.0 Beta 1`
`   at:01/09/2004 mark:(line,beta)  # 8.0.0 Beta 2`
`   at:27/09/2004 mark:(line,beta)  # 8.0.0 Beta 3`
`   at:22/11/2004 mark:(line,beta)  # 8.0.0 Beta 4`
`   at:23/11/2004 mark:(line,beta)  # 8.0.0 Beta 5 *est from tag +1 day`
`   at:04/12/2004 mark:(line,RC)    # 8.0.0 RC1`
`   at:22/12/2004 mark:(line,RC)    # 8.0.0 RC2`
`   at:05/01/2005 mark:(line,RC)    # 8.0.0 RC3`
`   at:07/01/2005 mark:(line,RC)    # 8.0.0 RC4`
`   at:11/01/2005 mark:(line,RC)    # 8.0.0 RC5`
`   barset:break color:prod from:19/01/2005 till:04/10/2010`
`   at:19/01/2005 mark:(line,major) # 8.0`
`   at:31/01/2005 mark:(line,minor) # 8.0.1`
`   at:07/04/2005 mark:(line,minor) # 8.0.2`
`   at:09/05/2005 mark:(line,minor) # 8.0.3`
`   at:04/10/2005 mark:(line,minor) # 8.0.4`
`   at:12/12/2005 mark:(line,minor) # 8.0.5`
`   at:09/01/2006 mark:(line,minor) # 8.0.6`
`   at:14/02/2006 mark:(line,minor) # 8.0.7`
`   at:23/05/2006 mark:(line,minor) # 8.0.8`
`   at:16/10/2006 mark:(line,minor) # 8.0.9`
`   at:08/01/2007 mark:(line,minor) # 8.0.10`
`   at:05/02/2007 mark:(line,minor) # 8.0.11`
`   at:07/02/2007 mark:(line,minor) # 8.0.12`
`   at:23/04/2007 mark:(line,minor) # 8.0.13`
`   at:17/09/2007 mark:(line,minor) # 8.0.14`
`   at:07/01/2008 mark:(line,minor) # 8.0.15`
`   at:12/06/2008 mark:(line,minor) # 8.0.17`
`   at:22/09/2008 mark:(line,minor) # 8.0.18`
`   at:03/11/2008 mark:(line,minor) # 8.0.19`
`   at:02/02/2009 mark:(line,minor) # 8.0.20`
`   at:16/03/2009 mark:(line,minor) # 8.0.21`
`   at:09/09/2009 mark:(line,minor) # 8.0.22`
`   at:14/12/2009 mark:(line,minor) # 8.0.23`
`   at:15/03/2010 mark:(line,minor) # 8.0.24`
`   at:17/05/2010 mark:(line,minor) # 8.0.25`
`   at:04/10/2010 mark:(line,minor) shift:($dx,$dy) text:8.0.26`

` bar:7.4 width:$bw color:devel align:left fontsize:M`
`   from:05/08/2003 till:17/11/2003 # REL7_4_BETA1`
`   at:05/08/2003 mark:(line,beta)  # 7.4 Beta 1 *est from tag`
`   at:27/08/2003 mark:(line,beta)  # 7.4 Beta 2 *`
`   at:15/09/2003 mark:(line,beta)  # 7.4 Beta 3 *`
`   at:03/10/2003 mark:(line,beta)  # 7.4 Beta 4 *`
`   at:22/10/2003 mark:(line,beta)  # 7.4 Beta 5 *`
`   at:03/11/2003 mark:(line,RC)    # 7.4 RC1 *`
`   barset:break color:prod from:17/11/2003 till:04/10/2010`
`   at:17/11/2003 mark:(line,major) # 7.4`
`   at:22/12/2003 mark:(line,minor) # 7.4.1`
`   at:08/03/2004 mark:(line,minor) # 7.4.2`
`   at:14/06/2004 mark:(line,minor) # 7.4.3`
`   at:16/08/2004 mark:(line,minor) # 7.4.4`
`   at:18/08/2004 mark:(line,minor) # 7.4.5`
`   at:22/10/2004 mark:(line,minor) # 7.4.6`
`   at:31/01/2005 mark:(line,minor) # 7.4.7`
`   at:09/05/2005 mark:(line,minor) # 7.4.8`
`   at:04/10/2005 mark:(line,minor) # 7.4.9`
`   at:12/12/2005 mark:(line,minor) # 7.4.10`
`   at:09/01/2006 mark:(line,minor) # 7.4.11`
`   at:14/02/2006 mark:(line,minor) # 7.4.12`
`   at:23/05/2006 mark:(line,minor) # 7.4.13`
`   at:16/10/2006 mark:(line,minor) # 7.4.14`
`   at:08/01/2007 mark:(line,minor) # 7.4.15`
`   at:05/02/2007 mark:(line,minor) # 7.4.16`
`   at:23/04/2007 mark:(line,minor) # 7.4.17`
`   at:17/09/2007 mark:(line,minor) # 7.4.18`
`   at:07/01/2008 mark:(line,minor) # 7.4.19`
`   at:12/06/2008 mark:(line,minor) # 7.4.21`
`   at:22/09/2008 mark:(line,minor) # 7.4.22`
`   at:03/11/2008 mark:(line,minor) # 7.4.23`
`   at:02/02/2009 mark:(line,minor) # 7.4.24`
`   at:16/03/2009 mark:(line,minor) # 7.4.25`
`   at:09/09/2009 mark:(line,minor) # 7.4.26`
`   at:14/12/2009 mark:(line,minor) # 7.4.27`
`   at:15/03/2010 mark:(line,minor) # 7.4.28`
`   at:17/05/2010 mark:(line,minor) # 7.4.29`
`   at:04/10/2010 mark:(line,minor) shift:($dx,$dy) text:7.4.30`

` bar:7.3 width:$bw color:devel align:left fontsize:M`
`   from:01/09/2002 till:27/11/2002 # * est from email "Timetable for 7.3 beta"`
`   # No Beta or RC releases!`
`   barset:break color:prod from:27/11/2002 till:07/01/2008`
`   at:27/11/2002 mark:(line,major) # 7.3`
`   at:18/12/2002 mark:(line,minor) # 7.3.1`
`   at:04/02/2003 mark:(line,minor) # 7.3.2`
`   at:22/05/2003 mark:(line,minor) # 7.3.3`
`   at:24/07/2003 mark:(line,minor) # 7.3.4`
`   at:03/12/2003 mark:(line,minor) # 7.3.5`
`   at:02/03/2004 mark:(line,minor) # 7.3.6`
`   at:16/08/2004 mark:(line,minor) # 7.3.7`
`   at:22/10/2004 mark:(line,minor) # 7.3.8`
`   at:31/01/2005 mark:(line,minor) # 7.3.9`
`   at:09/05/2005 mark:(line,minor) # 7.3.10`
`   at:04/10/2005 mark:(line,minor) # 7.3.11`
`   at:12/12/2005 mark:(line,minor) # 7.3.12`
`   at:09/01/2006 mark:(line,minor) # 7.3.13`
`   at:14/02/2006 mark:(line,minor) # 7.3.14`
`   at:23/05/2006 mark:(line,minor) # 7.3.15`
`   at:16/10/2006 mark:(line,minor) # 7.3.16`
`   at:08/01/2007 mark:(line,minor) # 7.3.17`
`   at:05/02/2007 mark:(line,minor) # 7.3.18`
`   at:23/04/2007 mark:(line,minor) # 7.3.19`
`   at:17/09/2007 mark:(line,minor) # 7.3.20`
`   at:07/01/2008 mark:(line,minor) shift:($dx,$dy) text:7.3.21`

` bar:7.2 width:$bw color:devel align:left fontsize:M`
`   from:25/10/2001 till:04/02/2002 # REL7_2_BETA1`
`   at:25/10/2001 mark:(line,beta)  # 7.2 Beta 1 *est from tag`
`   at:06/11/2001 mark:(line,beta)  # 7.2 Beta 2 *`
`   at:20/11/2001 mark:(line,beta)  # 7.2 Beta 3 *`
`   at:12/12/2001 mark:(line,beta)  # 7.2 Beta 4 *`
`   at:22/01/2002 mark:(line,RC)    # 7.2 RC1 *`
`   at:25/01/2002 mark:(line,RC)    # 7.2 RC2 *`
`   barset:break color:prod from:04/02/2002 till:01/02/2007`
`   at:04/02/2002 mark:(line,major) # 7.2`
`   at:21/03/2002 mark:(line,minor) # 7.2.1`
`   at:23/08/2002 mark:(line,minor) # 7.2.2`
`   at:01/10/2002 mark:(line,minor) # 7.2.3`
`   at:30/01/2003 mark:(line,minor) # 7.2.4`
`   at:16/08/2004 mark:(line,minor) # 7.2.5`
`   at:22/10/2004 mark:(line,minor) # 7.2.6`
`   at:31/01/2005 mark:(line,minor) # 7.2.7`
`   at:09/05/2005 mark:(line,minor) shift:($dx,$dy) text:7.2.8`

` bar:7.1 width:$bw color:devel align:left fontsize:M`
`   from:04/12/2000 till:13/04/2001 # REL7_1_BETA`
`   at:04/12/2000 mark:(line,beta)  # 7.1 Beta *est from tag`
`   at:07/01/2001 mark:(line,beta)  # 7.1 Beta 2 *`
`   at:09/01/2001 mark:(line,beta)  # 7.1 Beta 3 *`
`   barset:break color:prod from:13/04/2001 till:01/04/2006`
`   at:13/04/2001 mark:(line,major) # 7.1`
`   at:05/05/2001 mark:(line,minor) # 7.1.1`
`   at:11/05/2001 mark:(line,minor) # 7.1.2`
`   at:15/08/2001 mark:(line,minor) shift:($dx,$dy) text:7.1.3`

` bar:7.0 width:$bw color:prod align:left fontsize:M`
`   from:08/05/2000 till:01/05/2005`
`   at:08/05/2000 mark:(line,major) # 7.0`
`   at:01/06/2000 mark:(line,minor) # 7.0.1`
`   at:05/06/2000 mark:(line,minor) # 7.0.2`
`   at:11/11/2000 mark:(line,minor) shift:($dx,$dy) text:7.0.3`

` bar:6.5 width:$bw color:prod align:left fontsize:M`
`   from:09/06/1999 till:01/04/2004`
`   at:09/06/1999 mark:(line,major) # 6.5`
`   at:15/07/1999 mark:(line,minor) # 6.5.1`
`   at:15/09/1999 mark:(line,minor) # 6.5.2`
`   at:13/10/1999 mark:(line,minor) shift:($dx,$dy) text:6.5.3`

` bar:6.4 width:$bw color:prod align:left fontsize:M`
`   from:30/10/1998 till:01/10/2003`
`   at:30/10/1998 mark:(line,major) # 6.4`
`   at:18/12/1998 mark:(line,minor) # 6.4.1`
`   at:20/12/1998 mark:(line,minor) shift:($dx,$dy) text:6.4.2`

` bar:6.3 width:$bw color:prod align:left fontsize:M`
`   from:01/03/1998 till:01/03/2003`
`   at:01/03/1998 mark:(line,major) # 6.3`
`   at:23/03/1998 mark:(line,minor) # 6.3.1`
`   at:07/04/1998 mark:(line,minor) shift:($dx,$dy) text:6.3.2`

` bar:6.2 width:$bw color:prod align:left fontsize:M`
`   from:02/10/1997 till:01/03/1998`
`   at:02/10/1997 mark:(line,major) # 6.2`
`   at:17/10/1997 mark:(line,minor) shift:($dx,$dy) text:6.2.1`

` bar:6.1 width:$bw color:prod align:left fontsize:M`
`   from:08/06/1997 till:02/10/1997`
`   at:08/06/1997 mark:(line,major) # 6.1`
`   at:22/07/1997 mark:(line,minor) shift:($dx,$dy) text:6.1.1`

` bar:6.0 width:$bw color:devel align:left fontsize:M`
`   from:01/05/1995 till:29/01/1997 # Postgres95`
`   at:01/05/1995 mark:(line,major) shift:($dx,8) text:PG95 # 0.01`
`   at:25/05/1995 mark:(line,minor) # 0.02`
`   at:21/07/1995 mark:(line,minor) # 0.03`
`   at:05/09/1995 mark:(line,major) # 1.0`
`   at:23/02/1996 mark:(line,minor) # 1.01`
`   at:01/08/1996 mark:(line,minor) # 1.02`
`   at:04/11/1996 mark:(line,minor) # 1.09`
`   barset:break color:prod from:29/01/1997 till:08/06/1997`
`   at:29/01/1997 mark:(line,major) shift:($dx,$dy) text:6.0`

TextData =

` fontsize:M`
` textcolor:lighttext`
` pos:(700,20)`
` text:Updated ``-``-`` # yyyy-mm-dd (Internationalized date format)`

TextData =

`  pos:(250,$height)`
`  fontsize:XL`
`  textcolor:black`
`  text:"PostgreSQL release timeline"`

}}

## 각주

<references />

## 외부 링크

  -
  -
  - [한국 사용자 커뮤니티](http://database.sarang.net/?criteria=pgsql)

  - <http://translate.postgresql.kr/redmine> 한국어 설명서

  - <http://www.postgresdba.com/> PostgreSQL/Enterprisedb 한국 커뮤니티

[분류:데이터베이스 관리 시스템](https://ko.wikipedia.org/wiki/분류:데이터베이스_관리_시스템 "wikilink") [분류:자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_소프트웨어 "wikilink") [분류:C로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C로_작성된_자유_소프트웨어 "wikilink") [분류:자유 데이터베이스 관리 시스템](https://ko.wikipedia.org/wiki/분류:자유_데이터베이스_관리_시스템 "wikilink")

1.
2.
3.
4.  원래 Ingres 개발팀원이었으며 (상용)Ingres팀으로 옮겼음