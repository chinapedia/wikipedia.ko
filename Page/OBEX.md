> This article is converted from Wikipedia: [OBEX](https://ko.wikipedia.org/wiki/OBEX).


**OBEX**(OBject EXchange 또는 IrOBEX)는 장치 간 바이너리 오브젝트 교환을 용이케 하는 통신 프로토콜이다. [IrDA](../Page/IrDA.md "wikilink")에 의해 관리되고 있으나 [블루투스 스페셜 인터레스트 그룹과](https://ko.wikipedia.org/wiki/블루투스_스페셜_인터레스트_그룹 "wikilink") [오픈 모바일 연합의](../Page/오픈_모바일_연합.md "wikilink") [SyncML](../Page/SyncML.md "wikilink")에도 채택되고 있다. OBEX가 최초로 응용된 사례들 중에는 [팜 III가](https://ko.wikipedia.org/wiki/팜_III "wikilink") 있다. [PDA와](../Page/개인_정보_단말기.md "wikilink") 수많은 이후 세대들은 OBEX를 사용하여 명함, 데이터, 심지어는 애플리케이션의 교환도 가능케 했다.

OBEX가 원래 적외선용으로 설계되었으나 현재는 [블루투스](../Page/블루투스.md "wikilink")에 채택되었으며 [RS-232](../Page/RS-232.md "wikilink"), [USB](../Page/USB.md "wikilink"), [WAP](../Page/무선_애플리케이션_프로토콜.md "wikilink"), 그리고 [Livescribe](https://ko.wikipedia.org/wiki/Livescribe "wikilink") 스마트펜 등의 장치들에도 채택되고 있다.

## 구현

### javax.obex

[블루투스용 Java API의](https://ko.wikipedia.org/wiki/블루투스용_Java_API "wikilink") 선택적 패키지 javax.obex는 [자바로](../Page/자바_\(프로그래밍_언어\).md "wikilink") OBEX의 구현체를 제공한다.\[1\]

### OpenObex

OpenObex는 OBEX의 [C](../Page/C_\(프로그래밍_언어\).md "wikilink") 언어 오픈 소스 구현체이다. [IrDA](../Page/IrDA.md "wikilink"), [블루투스](../Page/블루투스.md "wikilink"), [USB](../Page/USB.md "wikilink"), [TCP/IP](https://ko.wikipedia.org/wiki/TCP/IP "wikilink")를 통한 연결 기능을 제공하며 오브젝트를 만들고 수신 데이터를 관리한다. 클라이언트 애플리케이션의 예는 다음과 같다:

``` cpp
void callback_function(...) {
  /* process received data */
}

int main() {
  OBEX_Init(..., callback_function);
  OBEX_TransportConnect(...);

  object=OBEX_ObjectNew(...);
  OBEX_ObjectAddHeader(object, ...);
  OBEX_ObjectAddHeader(object, ...);
  OBEX_Request(..., object);
  while(...)
    OBEX_HandleInput(...)

  object=OBEX_ObjectNew(...);
  OBEX_ObjectAddHeader(object, ...);
  OBEX_Request(..., object);
  while(...)
    OBEX_HandleInput(...)

  /* ... */

  OBEX_TransportDisconnect(handle);
  OBEX_Cleanup(handle);
}
```

### PyOBEX 및 nOBEX

PyOBEX는 [파이썬](../Page/파이썬.md "wikilink")으로 OBEX의 부분 지원을 제공한다.\[2\] nOBEX는 더 완전한 OBEX 지원을 제공하는 PyOBEX의 포크(fork)이며 블루투스 핸즈프리 프로파일을 지원한다.\[3\]

## 각주

## 외부 링크

  - [OBEX specification at IrDA.org](http://www.irda.org/)
  - [Bluetooth profiles](https://developer.bluetooth.org/TechnologyOverview/Pages/Profiles.aspx), including specifications for OBEX and OBEX-based protocols (GOEP, FTP, OBEX push, SYNC)
  - [OpenOBEX](https://web.archive.org/web/20061209175248/http://www.openobex.org/) an open source implementation of the OBEX protocol

[분류:블루투스](https://ko.wikipedia.org/wiki/분류:블루투스 "wikilink")

1.  [javax.obex API](http://docs.oracle.com/javame/config/cldc/opt-pkgs/api/bluetooth/jsr082/index.html)
2.  [PyOBEX](https://pypi.python.org/pypi/PyOBEX)
3.  [nOBEX](https://github.com/nccgroup/nOBEX)