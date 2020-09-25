> This article is converted from Wikipedia: [DirectX](https://ko.wikipedia.org/wiki/DirectX).


**Microsoft DirectX**()는 [멀티미디어](../Page/멀티미디어.md "wikilink"), 특히 [게임](../Page/게임.md "wikilink") [프로그래밍](https://ko.wikipedia.org/wiki/프로그래밍 "wikilink")에서 [마이크로소프트](../Page/마이크로소프트.md "wikilink") [플랫폼에서](../Page/컴퓨팅_플랫폼.md "wikilink") 작업을 위한 [API](../Page/API.md "wikilink")의 집합이다. 다이렉트엑스는 마이크로소프트 [윈도우](../Page/마이크로소프트_윈도우.md "wikilink"), [세가](../Page/세가.md "wikilink"), [드림캐스트](../Page/드림캐스트.md "wikilink"), 마이크로소프트 [엑스박스](../Page/엑스박스.md "wikilink") 및 [엑스박스 360을](../Page/엑스박스_360.md "wikilink") 위한 [비디오 게임](../Page/비디오_게임.md "wikilink") 개발에 널리 쓰인다.

다이렉트엑스는 또한 게임뿐 아니라 최근에 나온 3차원 [그래픽 하드웨어를](../Page/그래픽_처리_장치.md "wikilink") 사용하여 높은 품질의 3차원 그래픽을 빠르게 렌더링할 수 있기 때문에 [소프트웨어](../Page/소프트웨어.md "wikilink") 업계 전반에서 사용되기도 한다.

다이렉트엑스 런타임과 소프트웨어 개발킷은 무료이지만 개조는 할 수 없는 [클로즈드 소스](https://ko.wikipedia.org/wiki/클로즈드_소스 "wikilink")([오픈 소스의](../Page/오픈_소스.md "wikilink") 반대 개념) 소프트웨어이다. 다이렉트엑스 런타임은 원래 컴퓨터 게임 개발자들에게만 공개되었으나, 최근에는 기본적으로 윈도우에 포함되어 있다. 상위 버전으로 업데이트하고 싶을 경우 마이크로소프트의 공식 홈페이지를 통해 설치할 수 있다.

Direct3D 9Ex, Direct3D 10은 [윈도우 비스타](../Page/윈도우_비스타.md "wikilink") 이상, Direct3D 11은 [윈도우 비스타](../Page/윈도우_비스타.md "wikilink") SP2 또는 [윈도우 7](https://ko.wikipedia.org/wiki/윈도우_7 "wikilink") 이상, Direct3D 12는 [윈도우 10에서만](../Page/윈도우_10.md "wikilink") 사용할 수 있다. 그 까닭은 이러한 새로운 버전들은 윈도우 비스타에 도입되었던 새로운 [윈도우 디스플레이 드라이버 모델이](../Page/윈도우_디스플레이_드라이버_모델.md "wikilink") 있어야 동작하기 때문이다. 그래서 DirectX 조건에 맞더라도 드라이버가 [윈도우 디스플레이 드라이버 모델을](../Page/윈도우_디스플레이_드라이버_모델.md "wikilink") 지원하지 않으면 사용할 수 없다. 새로운 비스타/WDDM 그래픽스 구조에는 [데스크톱 창 관리자와](../Page/데스크톱_창_관리자.md "wikilink") 같이, 그래픽 하드웨어를 여러 개의 응용 프로그램과 서비스에 가상화할 수 있게 도와 주는 새로운 비디오 메모리 관리자를 포함하고 있다.

## 개발 역사

1994년 말, 마이크로소프트는 다음 [운영 체제인](../Page/운영_체제.md "wikilink") [윈도우 95를](../Page/윈도우_95.md "wikilink") 출시할 준비가 되었다. 마이크로소프트의 3명의 직원 Craig Eisler, Alex St. John, Eric Engstrom은 [프로그래머](../Page/프로그래머.md "wikilink")들이 마이크로소프트의 이전 운영 체제인 [MS-DOS](../Page/MS-DOS.md "wikilink")를 더 나은 플랫폼으로 보는 경향이 있었기 때문에 걱정이 있었다. MS-DOS가 게임 프로그래밍을 위한 더 나은 플랫폼으로 비쳐졌는데, 그 이유는 윈도우 95용으로 개발된 게임이 거의 없어서 운영 체제가 큰 성공을 거두지 못할 것으로 생각되었기 때문이다. [라이온킹](https://ko.wikipedia.org/wiki/라이온킹_\(비디오_게임\) "wikilink") 비디오 게임의 윈도우 포팅에 관한 부정적인 반응이 함께했다.\[1\]

도스는 비디오 카드, 키보드, 마우스, 사운드 장치, 그리고 시스템의 나머지 모든 부분들에 직접 접근을 허용하였던 반면에 윈도우 95는 보호 메모리 모델이 포함되어 이 모든 것들에 대한 접근을 제한하였다. 마이크로소프트는 프로그래머들을 위한 조속한 솔루션이 필요했는데, 이 운영 체제가 출시되기 수개월 밖에 안 남았기 때문이다. Eisler (development lead), St. John, and Engstrom (program manager)은 함께 이 문제를 해결하여 솔루션을 내놓았는데 이 이름이 DirectX이다.

## 구성 요소

  - 다이렉트 그래픽 인프라스트럭처()
    ; [다이렉트2D](../Page/Direct2D.md "wikilink")()

      -
        다이렉트 엑스 10.1 표준에 포함된 [2D 그래픽](https://ko.wikipedia.org/wiki/2차원_컴퓨터_그래픽스 "wikilink") 표현 API이다. [GDI, GDI+를](../Page/그래픽_장치_인터페이스.md "wikilink") 대체한다.

  - ; [다이렉트3D](../Page/Direct3D.md "wikilink")()

      -
        [3차원 그래픽을](../Page/3차원_컴퓨터_그래픽스.md "wikilink") 그리는 데에 쓰인다.

  - ; [다이렉트 드로](https://ko.wikipedia.org/wiki/다이렉트_드로 "wikilink")()

      -
        2차원 그래픽을 그리는 데에 쓰이며, 8 이후로 다이렉트 그래픽으로 통합되면서 쓰이지 않고 있다. 다이렉트2D가 역할을 대신하고 있다.

  - [다이렉트인풋](https://ko.wikipedia.org/wiki/DirectInput "wikilink")()
    [게임 콘트롤러](https://ko.wikipedia.org/wiki/게임_콘트롤러 "wikilink") 등의 조작 장치를 제어할 때 쓰인다.(다이렉트엑스 10으로 넘어오면서 엑스인풋으로 이름이 바뀜).

  - ;[엑스인풋](https://ko.wikipedia.org/wiki/XInput "wikilink")()

      -
        Windows 크로스 플랫폼(Cross-Platform) 표준 입력(키보드 마우스 조이스틱 등등) API. Windows (XP sp1, Vista 이상) 및 XBox360 을 지원하며 DirectInput 대신에 XInput 을 사용하면 XBox360 전용 콘트롤러 및 고유한 기능(버튼,진동 등)을 Windows 에서도 사용할 수 있다.

  - [다이렉트뮤직](https://ko.wikipedia.org/wiki/DirectMusic "wikilink")()
    다이렉트 뮤직 프로듀서에 의해 만들어지는 사운드 트랙 재생.

  - 다이렉트 오디오()
    ; [다이렉트사운드](../Page/다이렉트사운드.md "wikilink")()

      -
        게임 중 음향 효과에 쓰인다. DirectX 8이후로 다이렉트 사운드3D와 통합되어, 다이렉트 오디오가 되었으나, 여전히 다이렉트사운드로 불린다.

  - ; [다이렉트사운드3D](https://ko.wikipedia.org/wiki/다이렉트사운드#다이렉트사운트3D "wikilink")()

      -
        3차원 사운드를 위한 API. DirectX 8이후로 다이렉트 오디오에 통합되었다.

  - [다이렉트라이트](https://ko.wikipedia.org/wiki/DirectWrite "wikilink") ()
    다이렉트 엑스 10.1 표준에 포함된 [글꼴](../Page/글꼴.md "wikilink") 표현 API이다.

  - [다이렉트쇼](../Page/다이렉트쇼.md "wikilink") ()
    동영상,mp3 등의 멀티미디어 재생 API. 2005년 4월이후 DirectX SDK 에서 완전히 제외되었으며, 현재는 Windows (Platform) SDK 에 포함된 상태.

  - [다이렉트플레이](https://ko.wikipedia.org/wiki/DirectPlay "wikilink")()
    네트워크 게임을 위한 API 제공, 다이렉트엑스 8 이후로 개발이 중단되었다.

  - [다이렉트컴퓨트](../Page/다이렉트컴퓨트.md "wikilink")()
    다이렉트X 11에 포함된 그래픽 프로세서를 통한 범용 연산 API, 다이렉트 10까지 지원하는 그래픽카드에 대응한다.

## 버전 역사

<table>
<thead>
<tr class="header">
<th><p>버전</p></th>
<th><p>판올림</p></th>
<th><p>OS</p></th>
<th><p>출시일자</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1.0</p></td>
<td><p>4.02.0095</p></td>
<td></td>
<td><p><a href="../Page/1995년.md" title="wikilink">1995년</a> <a href="../Page/9월_30일.md" title="wikilink">9월 30일</a></p></td>
</tr>
<tr class="even">
<td><p>2.0 / 2.0a</p></td>
<td><p>4.03.00.1096</p></td>
<td><p><a href="../Page/윈도우_95.md" title="wikilink">윈도우 95</a> OSR2 및 NT 4.0</p></td>
<td><p><a href="../Page/1996년.md" title="wikilink">1996년</a> <a href="../Page/6월_5일.md" title="wikilink">6월 5일</a></p></td>
</tr>
<tr class="odd">
<td><p>3.0 / 3.0a</p></td>
<td><p>4.04.0068 / 70</p></td>
<td><p><a href="../Page/윈도우_NT.md" title="wikilink">윈도우 NT</a> 4.0 SP3<br />
윈도우 NT 4.0의 최종 지원 판 올림</p></td>
<td><p><a href="../Page/1996년.md" title="wikilink">1996년</a> <a href="../Page/9월_15일.md" title="wikilink">9월 15일</a></p></td>
</tr>
<tr class="even">
<td><p>4.0</p></td>
<td><p>개발이 중단되어 출시 안 됨.</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>5.0</p></td>
<td><p>4.05.00.0155</p></td>
<td><p><a href="../Page/윈도우_95.md" title="wikilink">윈도우 95</a> OSR2.5, 윈도우 NT 4.0에서 설치할 수 있던 윈도우 NT 5.0용 베타를 내려 받을 수 있음.</p></td>
<td><p><a href="../Page/1997년.md" title="wikilink">1997년</a> <a href="../Page/7월_16일.md" title="wikilink">7월 16일</a></p></td>
</tr>
<tr class="even">
<td><p>5.1</p></td>
<td><p>알 수 없음</p></td>
<td><p>알 수 없음</p></td>
<td><p><a href="../Page/1997년.md" title="wikilink">1997년</a> <a href="../Page/12월_1일.md" title="wikilink">12월 1일</a></p></td>
</tr>
<tr class="odd">
<td><p>5.2</p></td>
<td><p>4.05.01.1600</p></td>
<td></td>
<td><p><a href="../Page/1998년.md" title="wikilink">1998년</a> <a href="../Page/5월_5일.md" title="wikilink">5월 5일</a></p></td>
</tr>
<tr class="even">
<td><p>5.2</p></td>
<td><p>4.05.01.1998</p></td>
<td><p><a href="../Page/윈도우_98.md" title="wikilink">윈도우 98</a></p></td>
<td><p><a href="../Page/1998년.md" title="wikilink">1998년</a> <a href="../Page/5월_5일.md" title="wikilink">5월 5일</a></p></td>
</tr>
<tr class="odd">
<td><p>6.0</p></td>
<td><p>4.06.00.0318</p></td>
<td><p><a href="../Page/드림캐스트.md" title="wikilink">드림캐스트</a></p></td>
<td><p><a href="../Page/1998년.md" title="wikilink">1998년</a> <a href="../Page/8월_7일.md" title="wikilink">8월 7일</a></p></td>
</tr>
<tr class="even">
<td><p>6.1</p></td>
<td><p>4.06.02.0436</p></td>
<td><p><a href="../Page/윈도우_98.md" title="wikilink">윈도우 98 SE</a><br />
윈도우 NT 4.0을 위한 다이렉트 미디어의 최종 지원 판 올림</p></td>
<td><p><a href="../Page/1999년.md" title="wikilink">1999년</a> <a href="../Page/2월_3일.md" title="wikilink">2월 3일</a></p></td>
</tr>
<tr class="odd">
<td><p>7.0</p></td>
<td><p>4.07.00.0700</p></td>
<td><p><a href="../Page/윈도우_2000.md" title="wikilink">윈도우 2000</a></p></td>
<td><p><a href="../Page/1999년.md" title="wikilink">1999년</a> <a href="../Page/9월_22일.md" title="wikilink">9월 22일</a></p></td>
</tr>
<tr class="even">
<td><p>7.0a</p></td>
<td><p>4.07.00.0716</p></td>
<td></td>
<td><p><a href="../Page/1999년.md" title="wikilink">1999년</a></p></td>
</tr>
<tr class="odd">
<td><p>7.1</p></td>
<td><p>4.07.01.3000</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/윈도우_Me" title="wikilink">윈도우 Me</a></p></td>
<td><p><a href="../Page/1999년.md" title="wikilink">1999년</a> <a href="../Page/9월_16일.md" title="wikilink">9월 16일</a></p></td>
</tr>
<tr class="even">
<td><p>8.0</p></td>
<td><p>4.08.00.???? (RC0)</p></td>
<td></td>
<td><p><a href="../Page/2000년.md" title="wikilink">2000년</a> <a href="../Page/9월_30일.md" title="wikilink">9월 30일</a></p></td>
</tr>
<tr class="odd">
<td><p>8.0</p></td>
<td><p>4.08.00.0400 (RC14)</p></td>
<td></td>
<td><p><a href="../Page/2000년.md" title="wikilink">2000년</a> <a href="../Page/11월_3일.md" title="wikilink">11월 3일</a></p></td>
</tr>
<tr class="even">
<td><p>8.0a</p></td>
<td><p>4.08.00.0400 (RC14)<br />
설치 프로그램 수정</p></td>
<td><p>윈도우 95를 위한 최종 지원 판 올림</p></td>
<td><p><a href="../Page/2000년.md" title="wikilink">2000년</a> <a href="../Page/11월_7일.md" title="wikilink">11월 7일</a></p></td>
</tr>
<tr class="odd">
<td><p>8.1</p></td>
<td><p>4.08.01.0810<br />
4.08.01.0881 (RC7)</p></td>
<td><p><a href="../Page/윈도우_XP.md" title="wikilink">윈도우 XP</a>, <a href="../Page/엑스박스.md" title="wikilink">엑스박스</a>, <a href="../Page/윈도우_서버_2003.md" title="wikilink">윈도우 서버 2003</a></p></td>
<td><p><a href="../Page/2001년.md" title="wikilink">2001년</a> <a href="../Page/11월_12일.md" title="wikilink">11월 12일</a></p></td>
</tr>
<tr class="even">
<td><p>9.0</p></td>
<td><p>4.09.0000.0900</p></td>
<td><p><a href="../Page/윈도우_서버_2003.md" title="wikilink">윈도우 서버 2003</a></p></td>
<td><p><a href="../Page/2002년.md" title="wikilink">2002년</a> <a href="../Page/12월_19일.md" title="wikilink">12월 19일</a></p></td>
</tr>
<tr class="odd">
<td><p>9.0a</p></td>
<td><p>4.09.0000.0901</p></td>
<td></td>
<td><p><a href="../Page/2003년.md" title="wikilink">2003년</a> <a href="../Page/3월_26일.md" title="wikilink">3월 26일</a></p></td>
</tr>
<tr class="even">
<td><p>9.0b</p></td>
<td><p>4.09.0000.0902 (RC2)</p></td>
<td></td>
<td><p><a href="../Page/2003년.md" title="wikilink">2003년</a> <a href="../Page/8월_13일.md" title="wikilink">8월 13일</a></p></td>
</tr>
<tr class="odd">
<td><p>9.0c</p></td>
<td><p>4.09.0000.0904 (RC0)</p></td>
<td><p>윈도우 XP SP2, 윈도우 서버 2003 SP1, <a href="../Page/엑스박스_360.md" title="wikilink">엑스박스 360에서의</a> 마지막 순수 32비트 판 올림</p></td>
<td><p><a href="../Page/2004년.md" title="wikilink">2004년</a> <a href="../Page/12월_13일.md" title="wikilink">12월 13일</a></p></td>
</tr>
<tr class="even">
<td><p>9.0c</p></td>
<td><p>4.09.0000.0904</p></td>
<td><p><em>9.0c를 지원했던 모든 윈도우 운영체제 버전들과 호환</em><br />
<a href="https://ko.wikipedia.org/wiki/D3DX" title="wikilink">D3DX</a> <a href="https://ko.wikipedia.org/wiki/DLL" title="wikilink">DLL</a>이 포함된 첫 버전</p></td>
<td><p><a href="../Page/2005년.md" title="wikilink">2005년</a> <a href="../Page/12월_9일.md" title="wikilink">12월 9일</a></p></td>
</tr>
<tr class="odd">
<td><p>9.0c - 두 달에 한 번 업데이트</p></td>
<td><p>4.09.0000.0904</p></td>
<td><p>윈도우 XP<br />
<em>2005년 8월에 윈도우 98, 윈도우 98SE, 윈도우 ME, 윈도우2000을 지원하는 마지막 버전이 발표되었다.</em><br />
2005년 12월, 그리고 2006년 2월 업데이트는 또한 <a href="../Page/XML.md" title="wikilink">XML</a> 형식을 몇 개의 클래스에 추가한다.</p></td>
<td><p>2005년부터 약 두 달에 한 번꼴로 새로운 버전을 발표하여 2007년 2월 버전까지 있다.</p></td>
</tr>
<tr class="even">
<td><p>10.0</p></td>
<td><p>6.0.6000.16386</p></td>
<td><p><a href="../Page/윈도우_비스타.md" title="wikilink">윈도우 비스타만</a> 지원한다. 10버전에서는 <a href="../Page/픽셀_셰이더.md" title="wikilink">픽셀 셰이더와</a> <a href="https://ko.wikipedia.org/wiki/버텍스_셰이더" title="wikilink">버텍스 셰이더를</a> 통합한 <a href="https://ko.wikipedia.org/wiki/통합_셰이더" title="wikilink">통합 셰이더를</a> 사용하고 추가적으로 지오메트리 셰이더를 지원, 셰이더 모델 4.0, 128비트 <a href="../Page/하이_다이내믹_레인지_렌더링.md" title="wikilink">HDR</a> 등이 추가되었다.</p></td>
<td><p><a href="../Page/2006년.md" title="wikilink">2006년</a> <a href="../Page/11월_30일.md" title="wikilink">11월 30일</a></p></td>
</tr>
<tr class="odd">
<td><p>10.1</p></td>
<td><p>6.0.6001.18000</p></td>
<td><p>윈도우 비스타 서비스팩 1에 포함되어 있다.</p></td>
<td><p><a href="../Page/2008년.md" title="wikilink">2008년</a> <a href="../Page/2월.md" title="wikilink">2월</a></p></td>
</tr>
<tr class="even">
<td><p>11.0</p></td>
<td><p>6.01.7600.16385</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/윈도우_7" title="wikilink">윈도우 7</a>, <a href="../Page/윈도우_서버_2008_R2.md" title="wikilink">윈도우 서버 2008 R2</a>,<a href="../Page/윈도우_서버_2008.md" title="wikilink">윈도우 서버 2008</a> SP2, <a href="../Page/윈도우_비스타.md" title="wikilink">윈도우 비스타</a> SP2에 포함되어 있다.</p></td>
<td><p><a href="../Page/2009년.md" title="wikilink">2009년</a> <a href="../Page/10월_22일.md" title="wikilink">10월 22일</a></p></td>
</tr>
<tr class="odd">
<td><p>11.1</p></td>
<td><p>6.02.9200.16384</p></td>
<td><p><a href="../Page/윈도우_8.md" title="wikilink">윈도우 8</a>, <a href="../Page/윈도우_서버_2012.md" title="wikilink">윈도우 서버 2012</a>, <a href="https://ko.wikipedia.org/wiki/윈도우_7" title="wikilink">윈도우 7</a> SP1, <a href="../Page/윈도우_서버_2008_R2.md" title="wikilink">윈도우 서버 2008 R2</a> SP1에 포함되어 있다.</p></td>
<td><p><a href="../Page/2012년.md" title="wikilink">2012년</a> <a href="../Page/10월_26일.md" title="wikilink">10월 26일</a></p></td>
</tr>
<tr class="even">
<td><p>11.2</p></td>
<td><p>6.03.9600.16384</p></td>
<td><p><a href="../Page/윈도우_8.1.md" title="wikilink">윈도우 8.1</a>, <a href="https://ko.wikipedia.org/wiki/윈도우_서버_2012_R2" title="wikilink">윈도우 서버 2012 R2에</a> 포함되어 있다.</p></td>
<td><p><a href="../Page/2013년.md" title="wikilink">2013년</a> <a href="../Page/10월_17일.md" title="wikilink">10월 17일</a></p></td>
</tr>
<tr class="odd">
<td><p>12.0</p></td>
<td><p>10.00.10240.16384</p></td>
<td><p><a href="../Page/윈도우_10.md" title="wikilink">윈도우 10에</a> 포함되어 있다.</p></td>
<td><p><a href="../Page/2015년.md" title="wikilink">2015년</a> <a href="../Page/7월_29일.md" title="wikilink">7월 29일</a></p></td>
</tr>
</tbody>
</table>

## 대안

DirectX 계열의 [응용 프로그램 프로그래밍 인터페이스에](https://ko.wikipedia.org/wiki/응용_프로그램_프로그래밍_인터페이스 "wikilink") 대한 대안으로 대부분의 기능이 있는 [OpenGL](../Page/OpenGL.md "wikilink")이 있다. 이 밖에도 [SDL](../Page/심플_다이렉트미디어_레이어.md "wikilink"), [알레그로](https://ko.wikipedia.org/wiki/알레그로_라이브러리 "wikilink"), [오픈맥스](https://ko.wikipedia.org/wiki/오픈맥스 "wikilink"), [OpenAL](../Page/OpenAL.md "wikilink"), [FMOD](../Page/FMOD.md "wikilink")가 있다. 이 라이브러리들 가운데 대다수가 크로스플랫폼이거나 오픈 코드에 기반을 두고 있다.

또, DirectX와 똑같은 API를 둔 다른 대안으로 [와인을](../Page/와인_\(소프트웨어\).md "wikilink") 들 수 있다.

## 같이 보기

  - [Direct3D](../Page/Direct3D.md "wikilink")

## 각주

## 외부 링크

  - [공식 사이트](http://www.gamesforwindows.com/en-US/directx/)

  - [개발자 네트워크](http://msdn.microsoft.com/ko-kr/directx)

  - [DirectX World](https://web.archive.org/web/20170205021949/http://directxworld.altervista.org/) - DirectX를 배우는 곳. 그래픽 엔진을 만드는 법을 가르쳐 준다.

[DirectX](https://ko.wikipedia.org/wiki/분류:DirectX "wikilink") [분류:마이크로소프트 API](https://ko.wikipedia.org/wiki/분류:마이크로소프트_API "wikilink") [분류:API](https://ko.wikipedia.org/wiki/분류:API "wikilink") [분류:1995년 소프트웨어](https://ko.wikipedia.org/wiki/분류:1995년_소프트웨어 "wikilink")

1.