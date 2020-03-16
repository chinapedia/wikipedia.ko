> This article is converted from Wikipedia: [IrDA](https://ko.wikipedia.org/wiki/IrDA).


[섬네일를](https://ko.wikipedia.org/wiki/파일:IrDA_USB.jpg "wikilink") 통한 IrDA\]\] **IrDA**(Infrared Data Association)는 PAN과 같은 비교적 짧은 범위의 데이터 교환에 사용되는 물리적 통신프로토콜이다. 자유공간 광학통신같은 예로서 매우 짧은 범위를 커버하며 팜이나 핸드폰등에 사용된다.

IrPHY, IrLAP, IrLMP, IrCOMM, Tiny TP, IrOBEX에서도 IrDA의 인터페이스가 사용되며 IrDA를 통한 통신장치는 반드시 direct line of sight를 갖고 있어야 한다.

흔히 우리가 말하는 적외선통신이다.

## 사양

[IrDA 프로토콜 스택](https://ko.wikipedia.org/wiki/파일:Irda_protocol_stack_basic.png "wikilink")

### IrPHY

IrPHY(Infrared Physical Layer Specification)는 IrDA 사양의 물리 계층이다. 이 사양의 지원은 필수이다.

### IrLAP

IrLAP(Infrared Link Access Protocol)는 IrDA 사양의 2번째 계층이다. [OSI 모델의](https://ko.wikipedia.org/wiki/OSI_모델 "wikilink") [데이터 링크 계층을](https://ko.wikipedia.org/wiki/데이터_링크_계층 "wikilink") 표현한다. 이 사양의 지원은 필수이다.

### IrLMP

IrLMP(Infrared Link Management Protocol)는 IrDA 사양의 3번째 계층이다. IrLAP 계층 위에 놓이는 LM-MUX(Link Management Multiplexer), 서비스 제공자가 자사의 서비스들을 등록하여 다른 장치들의 서비스 접근을 가능케 하는 목록을 제공하는 LM-IAS(Link Management Information Access Service)로 구성된다. 이 사양의 지원은 필수이다.

### Tiny TP

Tiny TP(Tiny Transport Protocol) 는 IrLMP 계층의 최상위에 위치한다. 이 사양은 선택사항이다.

### IrCOMM

IrCOMM(Infrared Communications Protocol)은 적외선 장치를 [직렬](../Page/직렬_포트.md "wikilink") 또는 [병렬 포트처럼](../Page/병렬_포트.md "wikilink") 동작하게 만들어준다. IrLMP 계층의 최상위에 위치한다. 이 사양의 지원은 선택사항이다.

### OBEX

OBEX(Object Exchange)는 임의의 데이터 오브젝트의 교환을 제공한다. 이 사양의 지원은 선택사항이다.

### IrLAN

IrLAN(Infrared Local Area Network)은 적외선 장치를 LAN에 연결할 수 있게 한다. 이 사양의 지원은 선택사항이다.

### IrSimple

IrSimple은 무선 IrDA 프로토콜의 효율성을 객선하여 최소 4\~10배 더 빠른 전송 속도를 제공한다. 500 KB 일반 사진을 휴대 전화로부터 1초만에 전송할 수 있다.\[1\]

### IrSimpleShot

IrSimpleShot(IrSS)은 수백 만 대의 IrDA 지원 카메라 전화들이 무선으로 프린터, 프린터 키오스크, 평판 TV에 전송할 수 있도록 허용한다.

### IrFM

IrFM(Infrared Financial Messaging)은 Infrared Data Association가 개발한 무선 지불 표준이다.

## 각주

## 외부 링크

**공식**

  -
  - [List of official specifications](https://web.archive.org/web/20191115171139/http://www.irdajp.info/specifications.html), physical layer specification is US$100

**기타**

  - [Linux Infrared HOWTO](http://www.tldp.org/HOWTO/Infrared-HOWTO/)
  - [Linux Infrared Remote Control](http://www.lirc.org)
  - [Linux status of infrared devices (IrDA, ConsumerIR, Remote Control)](https://web.archive.org/web/20130425030439/http://tuxmobil.org/ir_misc.html)
  - [IrDA project of Universidad Nacional de Colombia SIE board](https://web.archive.org/web/20110902095151/http://wiki.linuxencaja.net/wiki/Academico/Embebidos/IrDA_SIE)

[분류:무선 통신](https://ko.wikipedia.org/wiki/분류:무선_통신 "wikilink")

1.  [1](http://irdajp.info/irsimple.html)  IrDA IrSimple Specifications (Infrared Data Association - irda.org)