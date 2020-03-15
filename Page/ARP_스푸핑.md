> This article is converted from Wikipedia: [ARP ](https://ko.wikipedia.org/wiki/ARP_).


[오른쪽을](https://ko.wikipedia.org/wiki/파일:ARP_Spoofing.svg "wikilink") 공격자가 바꿈으로서 효과적으로 [중간자 공격을](https://ko.wikipedia.org/wiki/중간자_공격 "wikilink") 수행할 수 있도록 한다.\]\]

**ARP 스푸핑**(ARP spoofing)은 [근거리 통신망](../Page/근거리_통신망.md "wikilink")(LAN) 하에서 [주소 결정 프로토콜](../Page/주소_결정_프로토콜.md "wikilink")(ARP) 메시지를 이용하여 상대방의 데이터 패킷을 중간에서 가로채는 [중간자 공격](https://ko.wikipedia.org/wiki/중간자_공격 "wikilink") 기법이다. 이 공격은 데이터 링크 상의 프로토콜인 ARP 프로토콜을 이용하기 때문에 근거리상의 통신에서만 사용할 수 있는 공격이다.

이 기법을 사용한 공격의 경우 특별한 이상 증상이 쉽게 나타나지 않기 때문에 사용자는 특별한 도구를 사용하지 않는 이상 쉽게 자신이 공격당하고 있다는 사실을 확인하기 힘들다.

## 과정

[로컬 영역 네트워크에서](https://ko.wikipedia.org/wiki/로컬_영역_네트워크 "wikilink") 각 장비의 IP 주소와 [MAC 주소간의](../Page/MAC_주소.md "wikilink") 대응은 ARP 프로토콜을 통해 이루어진다. 이때 공격자가 의도적으로 특정 IP 주소와 자신의 MAC 주소로 대응하는 ARP 메시지를 발송하면, 그 메시지를 받은 장비는 IP 주소를 공격자 MAC 주소로 인식하게 되고, 해당 IP 주소로 보낼 패킷을 공격자로 전송하게 된다. 이 때 공격자는 그 패킷을 원하는 대로 변조한 다음 원래 목적지 MAC 주소로 발송하는 공격을 할 수도 있다.

흔히 사용되는 공격 방식은 [게이트웨이](../Page/게이트웨이.md "wikilink") IP를 스푸핑하는 것으로, 이 경우 외부로 전송되는 모든 패킷이 공격자에 의해 가로채거나 변조될 수 있다. 또는, 두 노드에 각각 ARP 스푸핑을 하여 두 장비의 통신을 중간에서 조작하는 기법도 자주 사용된다.

## 은닉성

[와이어샤크](https://ko.wikipedia.org/wiki/와이어샤크 "wikilink")와 같은 패킷 감지 프로그램을 이용하면 주기적으로 자신의 주소가 아님에도 불구하고 ARP신호를 보내는 패킷을 확인할 수 있기 때문에 쉽게 감지할 수 있다.

## 방어 방법

### 정적 ARP 엔트리 사용

로컬 방식에서 사용되는 공격 방식이기 때문에, 로컬 ARP 캐쉬를 정적으로 정의할 수 있다. 이 경우 ARP 신호를 받으면 자신의 ARP테이블을 먼저 확인하고, Static(정적)으로 입력된 MAC주소에 대해서는 갱신하지 않는다.

ARP 스푸핑을 확인하는 소프트웨어는 ARP 응답을 상호확인하는 방법이나, 특별한 형식의 인증서를 사용한다. 인증되지 않은 ARP 응답은 차단된다.

## 외부 링크

  - [마이크로소프트웨어 - 난 네가 지난번에 입력한 비밀번호를 알고 있다](http://www.imaso.co.kr/?doc=bbs/gnuboard.php&bo_table=article&wr_id=33721)(2015.12월 이후 발간종료)
  - [ARP Spoofing을 통해 전파되는 온라인 게임핵 악성코드](http://www.ahnlab.com/kr/site/securitycenter/asec/asecIssueView.do?webAsecIssueVo.seq=88)(현재 운영되지않는 사이트)
  - [ARP Spoofing의 습격, 그리고 방어 전략](https://web.archive.org/web/20110314154033/http://www.ahnlab.com/kr/site/securitycenter/asec/asecView.do?groupCode=VNI001&webNewsInfoUnionVo.seq=10289)(현재 운영되지않는 사이트)

[분류:이더넷](https://ko.wikipedia.org/wiki/분류:이더넷 "wikilink") [분류:컴퓨터 보안](https://ko.wikipedia.org/wiki/분류:컴퓨터_보안 "wikilink") [분류:네트워크 보안](https://ko.wikipedia.org/wiki/분류:네트워크_보안 "wikilink")