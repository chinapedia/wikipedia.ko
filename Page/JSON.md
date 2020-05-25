> This article is converted from Wikipedia: [JSON](https://ko.wikipedia.org/wiki/JSON).


**JSON**(**제이슨**\[1\], )은 [속성-값 쌍](https://ko.wikipedia.org/wiki/속성-값_쌍 "wikilink")( attribute–value pairs and array data types (or any other serializable value)) 또는 "키-값 쌍"으로 이루어진 데이터 오브젝트를 전달하기 위해 인간이 읽을 수 있는 텍스트를 사용하는 [개방형 표준](../Page/개방형_표준.md "wikilink") 포맷이다. 비동기 브라우저/서버 통신 ([AJAX](https://ko.wikipedia.org/wiki/Ajax "wikilink"))을 위해, 넓게는 [XML](../Page/XML.md "wikilink")([AJAX가](https://ko.wikipedia.org/wiki/Ajax "wikilink") 사용)을 대체하는 주요 데이터 포맷이다. 특히, [인터넷](../Page/인터넷.md "wikilink")에서 자료를 주고 받을 때 그 자료를 표현하는 방법으로 알려져 있다. 자료의 종류에 큰 제한은 없으며, 특히 [컴퓨터 프로그램의](../Page/컴퓨터_프로그램.md "wikilink") [변수](https://ko.wikipedia.org/wiki/변수 "wikilink")값을 표현하는 데 적합하다.

본래는 [자바스크립트](../Page/자바스크립트.md "wikilink") 언어로부터 파생되어 [자바스크립트](../Page/자바스크립트.md "wikilink")의 구문 형식을 따르지만 언어 독립형 데이터 포맷이다. 즉, [프로그래밍 언어나](../Page/프로그래밍_언어.md "wikilink") [플랫폼에](../Page/컴퓨팅_플랫폼.md "wikilink") 독립적이므로, [구문 분석](../Page/구문_분석.md "wikilink") 및 JSON 데이터 생성을 위한 코드는 [C](../Page/C_\(프로그래밍_언어\).md "wikilink"), [C++](https://ko.wikipedia.org/wiki/C++ "wikilink"), [C\#](../Page/C_샤프.md "wikilink"), [자바](../Page/자바_\(프로그래밍_언어\).md "wikilink"), [자바스크립트](../Page/자바스크립트.md "wikilink"), [펄](../Page/펄.md "wikilink"), [파이썬](../Page/파이썬.md "wikilink") 등 수많은 [프로그래밍 언어에서](../Page/프로그래밍_언어.md "wikilink") 쉽게 이용할 수 있다.

JSON 포맷은 본래 [더글라스 크록포드가](https://ko.wikipedia.org/wiki/더글라스_크록포드 "wikilink") 규정하였다. RFC 7159와 ECMA-404 그리고 ISO/IEC 21778:2017\[2\] 표준에 의해 기술되고 있다. KS 부합화 표준은 아직 제정되지 않았으며, TTA 협회 표준명은 [TTAE.OT-10.0394](http://committee.tta.or.kr/data/standard_view.jsp?commit_code=STC2&firstDepthCode=STC2&pk_num=TTAE.OT-10.0394&nowSu=1)이다. ECMA 표준과 ISO/IEC 표준은 문법만 정의할 정도로 최소한으로만 정의되어 있는 반면 RFC는 시맨틱, 보안적 고려 사항을 일부 제공 한다.\[3\] JSON의 공식 인터넷 미디어 타입은 `application/json`이며, JSON의 파일 확장자는 `.json`이다.

## 역사

[섬네일](https://ko.wikipedia.org/wiki/파일:Douglas_Crockford.jpg "wikilink") JSON은 2000년대 초에 널리 사용된 방식인 [플래시](https://ko.wikipedia.org/wiki/플래시 "wikilink")나 [자바](../Page/자바_\(프로그래밍_언어\).md "wikilink") 애플릿 등의 브라우저 플러그인을 사용하지 않는 [무상태](https://ko.wikipedia.org/wiki/상태_\(컴퓨터_과학\) "wikilink"), 실시간 서버 대 브라우저 통신 프로토콜의 요구에 의거하여 성장하였다.\[4\]

[더글라스 크록포드가](https://ko.wikipedia.org/wiki/더글라스_크록포드 "wikilink") 처음으로 JSON 포맷을 정의하고 보급하였다.\[5\] 이 두문자어는 2001년 3월 크록포드 등이 공동 설립한 기업인 스테이트 소프트웨어(State Software)에서 기원하였다. 이 공동 설립자들은 표준 브라우저 기능으르 사용하였던 시스템을 빌드하기로 합의하였고 2개의 [하이퍼텍스트 전송 프로토콜](https://ko.wikipedia.org/wiki/하이퍼텍스트_전송_프로토콜 "wikilink")(HTTP) 연결을 개방시키고 추가 데이터 교환이 없으면 표준 브라우저 타임아웃 전에 이것들을 재활용함으로써 웹 서버에 영속적인 반이중 통신을 지원하는, 상태를 인지하는(stateful) 웹 애프리케이션 개발을 위해 웹 개발자들을 위한 [추상화 계층을](../Page/추상화_계층.md "wikilink") 제공하였다. 이 공동 설립자들은 원탁 회의에 참여하였고 데이터 포맷을 JSML으로 부를지, JSON으로 부를지 투표를 했으며, 어떠한 [라이선스](https://ko.wikipedia.org/wiki/소프트웨어_라이선스 "wikilink") 형태로 배포할 것인지도 논의하였다. 크록포드는 기업 법률가와 지나치게 규칙을 찾는 사람들을 조롱하고자 JSON 라이선스에다 "소프트웨어는 선을 위해 쓰여야 하며, 악을 위해 쓰여서는 안 된다"는 조항을 하나 추가하였다. [칩 모닝스타는](https://ko.wikipedia.org/wiki/칩_모닝스타 "wikilink") 스테이트 소프트웨어에서 스테이트 애플리케이션 프레임워크의 아이디어를 냈다.\[6\]\[7\] 한편, 이 조항으로 인해 JSON의 [라이선스 호환성](../Page/라이선스_호환성.md "wikilink") 문제가 다른 [오픈 소스 라이선스와](https://ko.wikipedia.org/wiki/오픈_소스_라이선스 "wikilink") 불거지게 되었다.\[8\]

JSON 라이브러리의 전신은 카툰 네트워크의 Communities.com라는 이름의 아동용 디지털 자산 트레이딩 게임 프로젝트에 사용되었으며, [DHTML](https://ko.wikipedia.org/wiki/동적_HTML "wikilink") 요소(이 시스템은 3DO 소유이기도 했음)를 조작하기 위한 사유 메시지 포맷과 더불어 브라우저 사이드 플러그인을 사용하였다. 초기 [Ajax](https://ko.wikipedia.org/wiki/Ajax "wikilink")의 기능을 발견한 digiGroups, Noosh 등은 프레임을 사용하여 웹 애플리케이션의 시각 컨텍스트를 새로 고치지 않은 채 정보를 사용자 브라우저의 시각 필드로 전달했으며, 이로써 넷스케이프 4.0.5+, IE 5+의 표준 HTTP, HTML, 자바스크립트 기능만을 사용하여 실시간 리치 웹 애플리케이션을 실현시켰다. 이때 크로포드는 자바스크립트가 이러한 시스템을 위한 객체 지향 메시지 포맷으로 사용될 수 있음을 발견하였다. 이 시스템은 [썬 마이크로시스템즈](../Page/썬_마이크로시스템즈.md "wikilink"), [아마존닷컴](https://ko.wikipedia.org/wiki/아마존닷컴 "wikilink"), \[\[전자_데이터_시스템|EDS\]로 판매되었다. JSON.org<ref>{{웹 인용\]\]는 JSON으로 자사의 [웹 서비스를](../Page/웹_서비스.md "wikilink") 제공하기 시작했다.\[9\]

JSON은 [자바스크립트](../Page/자바스크립트.md "wikilink") 스크립트 언어의 서브셋에 기반을 두었다. (구체적으로는 표준 [ECMA](../Page/Ecma_인터내셔널.md "wikilink")-262 제3판—1999년 12월\[10\]) 그리고 자바스크립트와 함께 흔히 사용되었으나 [언어 독립적인](https://ko.wikipedia.org/wiki/언어_독립_사양 "wikilink") 데이터 포맷이기도 했다. JSOn 데이터의 [구문 분석](../Page/구문_분석.md "wikilink") 및 생성을 위한 코드는 수많은 [프로그래밍 언어에서](../Page/프로그래밍_언어.md "wikilink") 쉽게 볼 수 있다. JSON의 웹사이트는 언어별로 JSON [라이브러리를](https://ko.wikipedia.org/wiki/언어_바인딩 "wikilink") 나열한다.

## 자료형과 문법

### 기본 자료형

JSON의 기본 자료형은 다음과 같다:

  - 수(Number)
  - [문자열](https://ko.wikipedia.org/wiki/문자열 "wikilink")(String): 0개 이상의 [유니코드](../Page/유니코드.md "wikilink") 문자들의 연속. 문자열은 큰 따옴표(")로 구분하며 역슬래시 [이스케이프](https://ko.wikipedia.org/wiki/이스케이프_문자 "wikilink") 문법을 지원한다.
  - [참/거짓(Boolean)](https://ko.wikipedia.org/wiki/불린_자료형 "wikilink"): `true` 또는 `false` 값
  - [배열](../Page/배열.md "wikilink")(Array): 0 이상의 임의의 종류의 값으로 이루어진 [순서가 있는 리스트](../Page/리스트_\(컴퓨팅\).md "wikilink"). 대괄호로 나타내며 요소는 쉼표로 구분한다.
  - 객체(Object): 순서가 없는 이름/값 쌍의 집합으로, 이름(키)이 문자열이다.
  - [`null`](https://ko.wikipedia.org/wiki/null "wikilink"): 빈 값으로, `null`을 사용한다.

### 수(Number)

기본 자료형의 수는 다음과 같이 표현된다. C나 자바에서의 8진수와 16진수를 표현하는 방법은 지원되지 않는다.

  - 정수

<!-- end list -->

``` json
74
1974
750
-114
-273
```

  - 실수([고정 소수점](https://ko.wikipedia.org/wiki/고정_소수점 "wikilink"))

<!-- end list -->

``` json
3.14
-2.718
```

  - 실수([부동 소수점](https://ko.wikipedia.org/wiki/부동_소수점 "wikilink"))

<!-- end list -->

``` json
1e4
2.5e12
3.4e+4
4.56e-8
5.67E+10
6.78E-5
```

### 문자열(String)

항상 큰 따옴표(")로 묶어야 하며, 그 안에는 유니코드 문자들이 나열된다. 유니코드 중 역슬래시(\\)와 큰따옴표(")는 바로 사용할 수 없다. 역슬래시는 제어문자를 표현하기 위해 사용되며 다음과 같은 의미를 지닌다.

  -
    \\b 백스페이스
    \\f 폼 피드
    \\n 개행
    \\r 캐리지 리턴
    \\t 탭
    \\" 따옴표
    \\/ 슬래시
    \\\\ 역슬래시
    \\uHHHH 16진수 네자리로되어 있는 유니코드 문자

<!-- end list -->

``` json
"1234"
"Love"
"O-matic"
"한글"
"\"JSON\""
```

### 배열(Array)

배열은 대괄호\[\]로 나타낸다. 배열의 각 요소는 기본 자료형이거나 배열, 객체이다. 각 요소들은 쉼표(,)로 구별된다. 각 요소가 나타나는 순서에 의미가 있다.

``` json numberLines
 [10, {"v": 20}, [30, "마흔"]]
```

### 객체(Object)

객체는 이름/값 쌍의 집합으로, 중괄호{}를 사용한다. 이름은 문자열이기 때문에 반드시 따옴표를 하며, 값은 기본 자료형이다. 각 쌍들은 쉼표(,)로 구별된다. 각 쌍이 나오는 순서는 의미가 없다.

``` json
 {"name2": 50, "name3": "값3", "name1": true}
```

JSON 메시지 단위는 [배열](../Page/배열.md "wikilink")이나 [객체](https://ko.wikipedia.org/wiki/객체 "wikilink")이다. 위의 두 예는 JSON 메시지가 될 수 있다.

## 예제

다음은 한 사람에 관한 정보를 갖는 JSON 객체이다.

키-값 쌍(이름:값)의 패턴으로 표현된다.

``` json numberLines
 {
    "이름": "홍길동",
    "나이": 25,
    "성별": "여",
    "주소": "서울특별시 양천구 목동",
    "특기": ["농구", "도술"],
    "가족관계": {"#": 2, "아버지": "홍판서", "어머니": "춘섬"},
    "회사": "경기 수원시 팔달구 우만동"
 }
```

## 장점

  - JSON은 텍스트로 이루어져 있으므로, 사람과 기계 모두 읽고 쓰기 쉽다.
  - [프로그래밍 언어와](../Page/프로그래밍_언어.md "wikilink") [플랫폼에](../Page/컴퓨팅_플랫폼.md "wikilink") 독립적이므로, 서로 다른 시스템간에 객체를 교환하기에 좋다.
  - [자바스크립트](../Page/자바스크립트.md "wikilink")의 문법을 채용했기 때문에, 자바스크립트에서 `eval` 명령으로 곧바로 사용할 수 있다. 이런 특성은 자바스크립트를 자주 사용하는 웹 환경에서 유리하다. 그러나 실질적으로 `eval` 명령을 사용하면 외부에서 악성 코드가 유입될 수 있다. [모질라 파이어폭스](../Page/모질라_파이어폭스.md "wikilink") 3.5, [인터넷 익스플로러](../Page/인터넷_익스플로러.md "wikilink") 8, [오페라](../Page/오페라_\(웹_브라우저\).md "wikilink") 10.5, [사파리](../Page/사파리_\(웹_브라우저\).md "wikilink"), [구글 크롬](https://ko.wikipedia.org/wiki/구글_크롬 "wikilink") 등 대부분의 최신 [웹 브라우저는](../Page/웹_브라우저.md "wikilink") JSON 전용 파서 기능을 내장하고 있으므로 이런 기능을 사용하는 것이 더 안전할 뿐만 아니라 빠른 방법이다.

## 같이 보기

  - [JSON 스트리밍](https://ko.wikipedia.org/wiki/JSON_스트리밍 "wikilink")
  - 관련 포맷
      - [GeoJSON](../Page/GeoJSON.md "wikilink")
      - [JSON-LD](../Page/JSON-LD.md "wikilink")
      - [JSON-RPC](../Page/JSON-RPC.md "wikilink")
      - [JsonML](https://ko.wikipedia.org/wiki/JsonML "wikilink")
      - [S-표현식](../Page/S-표현식.md "wikilink")
      - [SOAPjr](https://ko.wikipedia.org/wiki/SOAPjr "wikilink")
      - [GBSON](https://ko.wikipedia.org/wiki/GBSON "wikilink") - annotation format of nucleic acid sequences ([DNA](../Page/DNA.md "wikilink"), [RNA](../Page/RNA.md "wikilink"))\[11\]
  - 관련 바이너리 인코딩
      - [BSON](https://ko.wikipedia.org/wiki/BSON "wikilink")
      - [CBOR](https://ko.wikipedia.org/wiki/CBOR "wikilink")
      - [MessagePack](https://ko.wikipedia.org/wiki/MessagePack "wikilink")
      - [스마일](https://ko.wikipedia.org/wiki/스마일_\(데이터_교환_포맷\) "wikilink") - JSON 기반
      - [UBJSON](https://ko.wikipedia.org/wiki/UBJSON "wikilink")
      - EXI4JSON (EXI for JSON)
  - 구현체:
      - [잭슨](https://ko.wikipedia.org/wiki/잭슨_\(API\) "wikilink")

## 각주

<references />

## 외부 링크

  - [포맷 웹사이트](http://www.json.org/)
  - [ECMA-404](http://www.ecma-international.org/publications/files/ECMA-ST/ECMA-404.pdf) — JSON 데이터 교환 포맷
  - [JSON Formatter](https://jsonformatter.org) — JSON 포매터
  - [JSON Validator](https://codebeautify.org/jsonvalidator) JSON 검사기

[JSON](https://ko.wikipedia.org/wiki/분류:JSON "wikilink") [분류:데이터 직렬화 포맷](https://ko.wikipedia.org/wiki/분류:데이터_직렬화_포맷 "wikilink") [분류:자바스크립트](https://ko.wikipedia.org/wiki/분류:자바스크립트 "wikilink") [분류:마크업 언어](https://ko.wikipedia.org/wiki/분류:마크업_언어 "wikilink") [분류:2001년 도입](https://ko.wikipedia.org/wiki/분류:2001년_도입 "wikilink") [분류:Ajax](https://ko.wikipedia.org/wiki/분류:Ajax "wikilink") [분류:오픈 포맷](https://ko.wikipedia.org/wiki/분류:오픈_포맷 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.  [Apache and the JSON license](https://lwn.net/Articles/707510/) on LWN.net by Jake Edge (November 30, 2016)
9.
10.
11.