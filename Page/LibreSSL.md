> This article is converted from Wikipedia: [LibreSSL](https://ko.wikipedia.org/wiki/LibreSSL).


**LibreSSL**은 [SSL](https://ko.wikipedia.org/wiki/SSL "wikilink")과 [TLS](https://ko.wikipedia.org/wiki/TLS "wikilink") 프로토콜의 [오픈소스](https://ko.wikipedia.org/wiki/오픈소스 "wikilink") 구현판이다. 2014년 4월에 [OpenBSD](../Page/OpenBSD.md "wikilink")개발자들이 [하트블리드](../Page/하트블리드.md "wikilink") [보안취약점](https://ko.wikipedia.org/wiki/보안취약점 "wikilink")에 대응하기 위해, [OpenSSL](../Page/OpenSSL.md "wikilink") [암호학](../Page/암호학.md "wikilink") [소프트웨어 라이브러리의](https://ko.wikipedia.org/wiki/소프트웨어_라이브러리 "wikilink") 코드를 [리팩토링](https://ko.wikipedia.org/wiki/리팩토링 "wikilink")해 더 안전한 구현을 만들기 위해 OpenSSL로 부터 [포크 (소프트웨어 개발)했다](../Page/포크_\(소프트웨어_개발\).md "wikilink").\[1\]\[2\]\[3\]

LibreSSL OpenSSL의 1.0.1g 브랜치로부터 포크되었으며 OpenBSD 프로젝트의 보안 가이드라인을 따른다.\[4\]

## 역사

OpenSSL에서 하트블리드 버그가 발견된 다음, OpenBSD팀은 코드를 새로이 검토하였으며, 포크한 코드를 스스로 유지보수해야함을 알게되었다\[5\] . libressl.org 도메인은 4월 11일에 등록되으며; 프로젝트는 4월 22일에 발표됐다.

코드 가지치기의 첫번째 주에서, 90,000줄 이상의 C코드들이 제거되었다.\[6\]\[7\] 오래되거나 쓰이지 않는 코드들과 몇몇 오래되고 지금은 잘 쓰이지 않는 운영체제 지원 코드들은 제거되었다. LibreSSL은 초기 OpenSSL을 OpenBSD 5.6버전에서 제거하기위해 개발되었으나, 코드 제거작업된 라이브러리가 안정이 되면 다른 플랫폼으로 다시 포팅될 것 기대되고 있다.\[8\] , 프로젝트는 현재 안정적인 외부 자금 기부자를 찾고있다.\[9\]

## 변화

### 메모리 관련

더 자세히 들어가면, 지금까지의 일부 눈에띄고 중요한 변화 중에는 커스텀 메모리 호출을 표준 라이브러리로 바꾼것이다(예를 들어 [:en:strlcpy](https://ko.wikipedia.org/wiki/:en:strlcpy "wikilink"), [:en:calloc](https://ko.wikipedia.org/wiki/:en:calloc "wikilink"), [:en:asprintf](https://ko.wikipedia.org/wiki/:en:asprintf "wikilink"), [:en:reallocarry](https://ko.wikipedia.org/wiki/:en:reallocarry "wikilink"), 등).\[10\]\[11\] 이 절차는 나중에 더 나은 메모리 [디버거](../Page/디버거.md "wikilink")를 사용하거나 프로그램 오류 발생을 관찰([주소 공간 배치 난수화](https://ko.wikipedia.org/wiki/주소_공간_배치_난수화 "wikilink")(ASLR), [NX 비트](../Page/NX_비트.md "wikilink"), Stack Canary 등을 통해) [버퍼 오버플로에러를](https://ko.wikipedia.org/wiki/버퍼_오버플로 "wikilink") 수정하는데 도움을 줄 수도 있다.

잠재적인 Double Free(C 동적 메모리 할당에러) 해결은 [CVS](../Page/CVS.md "wikilink") 커밋 로그(명시적 [널 포인터](../Page/널_포인터.md "wikilink") 변수 할당 포함)\[12\]에 언급되어있다.또한 인자 길이, 부호없는 변수를 부호화된 변수에 할당, 포인터 변수, 함수의 반환 값의 보장과 관련된 Sanity 검사또한 커밋 로그에 언급되어있다.

### 사전 방지책

좋은 프로그래밍 결과를 유지하기 위해 안전을 위해 디자인된 많은 컴파일러 옵션과 플래그들이 잠재적인 문제를 감지해 더 빨리 오류를 고치기 위해 기본적으로 활성화 되어있다(-Wall, -Werror, -Wextra, -Wuninitialized). 차후 공헌자들의 프로그램 검수를 돕기 위해 코드의 가독성 업데이트 또한 포함되어있다(Kernel Normal Form, 공백, 라인 감싸기 등). 불필요한 메소드 감싸개와 매크로의 수정 또한 코드 가독성과 검사에 도움을 주고 있다(에러와 I/O추상화 라이브러리 레퍼런스).

LibreSSL은 [2038년에](../Page/2038년_문제.md "wikilink") 호환성을 갖추고 코드가 비슷한 플랫폼에 이식성을 갖도록 변화하였다.

### 암호학

불안정한 시드입력 절차를 바꿈으로써 난수생성기기반의 메소드의 [난수조건을](https://ko.wikipedia.org/wiki/난수#의사난수_생성_방법 "wikilink") 적절하게 만드는 변화가 있었다(커널이 자체 제공하는 기능을 사용하였다).\[13\]\[14\] 주목할만한 추가라는 측면에서, OpenBSD는 새로운 그리고 더 훌륭한 알고리즘(ChaCha 스트림 암호화와 Poly1305-AES 메시지 인증코드)과 함께 더 안전한 [타원곡선](../Page/타원곡선.md "wikilink")셋(Brainpool 곡선 [RFC5639](http://tools.ietf.org/html/rfc5639), 최고 512bit 강도) 지원을 추가했다.

### 코드제거

[하트블리드](../Page/하트블리드.md "wikilink")에 대응하기 위해 초기에 LibreSSL에서 제거된 특징중 하나는 heartbeat 기능이었다.\[15\] 게다가 필요하지 않은 운영체제와 하드웨어 아키텍처 지원([맥 OS](../Page/맥_OS.md "wikilink"), [넷웨어](../Page/넷웨어.md "wikilink"), [OS/2](https://ko.wikipedia.org/wiki/OS/2 "wikilink"), [VMS](../Page/OpenVMS.md "wikilink"), [윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 등), 불필요하거나 안전하지 못하다고 여겨진 [전처리기 매크로](https://ko.wikipedia.org/wiki/C_언어_전처리기 "wikilink"), [어셈블리어](../Page/어셈블리어.md "wikilink"), [C 언어](https://ko.wikipedia.org/wiki/C_언어 "wikilink"), [Perl](https://ko.wikipedia.org/wiki/Perl "wikilink")과 같이 오래된 데모와 문서파일들 또한 제거되었다.

백도어를 가졌다고 의심되어온 Dual_EC_DRBG알고리즘\[16\]또한 [FIPS표준안이](https://ko.wikipedia.org/wiki/:en:Federal_Information_Processing_Standards "wikilink") 요구함에 따라 제거되었다. 쓰이지 않는 통신규약 및 불안전한 알고리즘([MD2](https://ko.wikipedia.org/wiki/:en:MD2_\(cryptography\) "wikilink"), [:en:SSL v2](https://ko.wikipedia.org/wiki/:en:SSL_v2 "wikilink"), [커베로스](../Page/커베로스.md "wikilink"), [J-PAKE](https://ko.wikipedia.org/wiki/:en:Password_Authenticated_Key_Exchange_by_Juggling "wikilink"), [SRP](https://ko.wikipedia.org/wiki/:en:Secure_Remote_Password_protocol "wikilink")) 또한 제거되었다.

### 남아있는 버그

OpenSSL의 해결되지 못한 불만 중 하나는 버그 트래커에 있는 알려진 버그들이 갑자기 주목되지 않는곳으로 사라지거나 몇년동안 무시되는 것이었다. 오래된 버그들은 현재 LibreSSL에서 해결되는 중이다.\[17\]

## 같이 보기

  - [:en:Comparison of TLS implementations](https://ko.wikipedia.org/wiki/:en:Comparison_of_TLS_implementations "wikilink")
  - [:en:POSSE project](https://ko.wikipedia.org/wiki/:en:POSSE_project "wikilink")
  - [오픈SSH](../Page/오픈SSH.md "wikilink"), OpenBSD 커뮤니티에 의해 포크된 또 다른 보안 소프트웨어

## 참고문헌

## 외부 링크

  -
  - [LibreSSL source code (OpenGrok)](https://web.archive.org/web/20140424095911/http://bxr.su/OpenBSD/lib/libssl/src/ssl/)

  - [OpenSSL Valhalla Rampage](http://opensslrampage.org/) (blog of highlights of the code cleanup)

[분류:암호 소프트웨어](https://ko.wikipedia.org/wiki/분류:암호_소프트웨어 "wikilink") [분류:C 라이브러리](https://ko.wikipedia.org/wiki/분류:C_라이브러리 "wikilink") [분류:OpenBSD](https://ko.wikipedia.org/wiki/분류:OpenBSD "wikilink") [분류:2014년 소프트웨어](https://ko.wikipedia.org/wiki/분류:2014년_소프트웨어 "wikilink") [분류:자유 보안 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_보안_소프트웨어 "wikilink") [분류:C로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C로_작성된_자유_소프트웨어 "wikilink") [분류:소프트웨어 포크](https://ko.wikipedia.org/wiki/분류:소프트웨어_포크 "wikilink") [분류:전송 계층 보안 구현](https://ko.wikipedia.org/wiki/분류:전송_계층_보안_구현 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
17.