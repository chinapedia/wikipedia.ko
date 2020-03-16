> This article is converted from Wikipedia: [IEEE 802.11e-2005](https://ko.wikipedia.org/wiki/IEEE_802.11e-2005).


**IEEE 802.11e-2005** 혹은 **IEEE 802.11e**는 [IEEE 802.11](../Page/IEEE_802.11.md "wikilink") 표준의 향상된 추가 개정판이다. 이 표준은 무선 랜에서의 [QoS](../Page/QoS.md "wikilink") 기능 지원에 관한 내용을 담고있다. 이를 위해서 [무선 랜의](https://ko.wikipedia.org/wiki/무선_랜 "wikilink") [매체 접근 제어](https://ko.wikipedia.org/wiki/매체_접근_제어 "wikilink")(MAC) 계층에 해당하는 부분을 수정하였다. 이 표준은 [VoWLAN](https://ko.wikipedia.org/wiki/VoWLAN "wikilink")(Voice over Wireless LAN)나 [스트리밍 멀티미디어와](https://ko.wikipedia.org/wiki/스트리밍_멀티미디어 "wikilink") 같은 전송 지연에 민감한 애플리케이션을 위해 만들어졌다. 이 개정판은 [IEEE 802.11-2007](https://ko.wikipedia.org/wiki/IEEE_802.11-2007#802.11-2007 "wikilink") 표준에 통합되었다.

[802.11은](../Page/IEEE_802.11.md "wikilink") 노트북이나 핸드폰 같은 장비들을 가정, 사무실, 상업 시설들에서 널리 사용하는 무선 LAN에 접속하여 사용할 수 있도록 해주는 [IEEE](https://ko.wikipedia.org/wiki/IEEE "wikilink") 표준이다.

## 기존의 802.11 MAC

### 분산 조정 함수

기본적인 802.11 MAC 계층은 여러 중계역이 무선 매체를 공유하는데 분산 조정 함수(distributed coordination function; DCF)라는 방법을 사용한다. DCF는 [반송파 감지 다중 접속 및 충돌 회피](https://ko.wikipedia.org/wiki/반송파_감지_다중_접속_및_충돌_회피 "wikilink") (CSMA/CA)를 기본으로 하고, 선택적으로 [IEEE 802.11 RTS/CTS를](https://ko.wikipedia.org/wiki/IEEE_802.11_RTS/CTS "wikilink") 사용하여 중계역(station)간 매질을 공유한다. 이 방식은 몇가지 한계점이 있다.

  - 많은 중계역들이 동시에 통신하려는 경우 충돌이 많이 일어난다. 이는 사용 가능한 대역폭을 낮추고 [congestive collapse를](https://ko.wikipedia.org/wiki/congestive_collapse "wikilink") 야기시킨다.
  - 서비스 품질(QoS)을 보장하지 않는다. 즉, 전송 우선 순위에 대한 개념이 없다.
  - 일단 하나의 station이 매질을 사용하게 되면 해당 중계역이 원하는 만큼 계속 독점적으로 해당 매체를 사용하게 된다. 만약 그중계역이 낮은 전송 속도를 갖고 있다면 (예를 들어 1 Mbit/s) 패킷을 보내는데 매우 오랜 시간이 걸릴 것이고, 그동안 다른 모든 중계역은 데이터 전송을 하지 못하게 된다.

### 점 조정 함수

원래의 802.11 MAC은 점 조정 함수(point coordination function; PCF)라고 불리는 또다른 조정 함수를 가지고 있다. 이 방식은 인프라스트럭처(infrastructure) 모드에서만 사용 가능하다. 인프라스트럭처 모드란 중계역들이 [접근점](https://ko.wikipedia.org/wiki/접근점 "wikilink")(Access Point; AP)를 통해서 네트워크에 접속하는 방식을 말한다. 이러한 방식은 선택적인 것이고 실제로 이 기능이 적용된 AP나 Wi-Fi 어댑터들은 얼마 되지 않는다. AP는 규칙적으로 *[beacon](https://ko.wikipedia.org/wiki/Electric_beacon#Wi-Fi "wikilink")* 프레임을 보낸다. (일반적으로 매 0.1초 마다 한개의 beacon 프레임을 전송한다.) 이 *beacon* 프레임 사이에 PCF는 두가지 구간을 정한다. 하나는 비경쟁구간 Contention Free Period (CFP)이고 다른 하나는 경쟁 구간 Contention Period (CP)이다. 경쟁구간에서는 DCF가 사용된다. 비경쟁구간에서 AP는 Contention-Free-Poll (CF-Poll) 패킷을 각 station에 차례차례 전송하게 된다. CF-Poll을 받은 station은 패킷을 전송할 권한을 갖는다. 즉 AP가 경쟁에 관한 중재자가 된다. 비록 이 방법이 QoS를 관리하는데 더 좋긴하지만 PCF는 [802.1p](https://ko.wikipedia.org/wiki/802.1p "wikilink")나 [DiffServ](https://ko.wikipedia.org/wiki/DiffServ "wikilink") 같은 다른 QoS 시스템에서 일반적으로 사용하는 트래픽별 전송 우선 순위를 사용하지는 않는다.

## 802.11e의 MAC

[섬네일](https://ko.wikipedia.org/wiki/파일:OSI-80211e.png "wikilink")\[1\]\]\] 802.11e은 새로운 조정 함수인 하이브리드 조정 함수(hybrid coordination function; HCF)를 사용하여 기존의 DCF와 PCF를 향상시켰다. HCF는 기존의 802.11 MAC에서 정의된 것과 유사한 두가지 채널 접근 방식을 사용한다. HCF 통제 채널 접근(HCCA)과 향상된 분산 채널 접근(EDCA)이 바로 그것이다. EDCA와 HCCA 모두 전송 우선 순위인 트래픽 범주를 정의한다. 예를 들어 [이메일](https://ko.wikipedia.org/wiki/이메일 "wikilink")은 낮은 전송 우선 순위 집단에 할당하고, 무선랜을 통한 음성통신은 높은 전송 우선순위 집단에 할당하는 것이다.

### 향상된 조정 채널 접근

[와이파이 멀티미디어](https://ko.wikipedia.org/wiki/와이파이_멀티미디어 "wikilink")(WMM)는 EDCA의 와이파이 협력 버전이다. QOS에 관한 강력한 요구로 IEEE 802.11e가 승인 받기 전에 WMM이 미리 발표되었다. 내용상으로는 거의 같다.

EDCA에서 높은 우선순위를 가진 트래픽은 낮은 우선순위를 가진 트래픽에서 전송될 기회를 더 많이 갖는다. 평균적으로, 높은 우선순위 트래픽을 가지고 있는 station은 패킷을 전송하기 전에 낮은 우선 순위 트래픽을 가지고 있는 중계역보다 더 조금 기다린다. 이것은 높은 우선순위 트래픽에 대해서 더 짧은 contention window (CW)와 더 짧은 [프레임간 공간 중재](https://ko.wikipedia.org/wiki/프레임간_공간_중재 "wikilink")(arbitration inter-frame space; AIFS)를 할당함으로써 가능하다. 또한 EDCA는 전송 기회(Transmit Opportunity; TXOP)라고 부르는 기간동안 채널에 경쟁없이 접속할 수 있도록 해준다. TXOP의 최대 기간을 넘지 않는 한도에서 정해진 TXOP 기간동안 중계역은 가능한 많은 패킷을 전송할 수 있다. 만약 하나의 프레임이 너무 길어서 한번의 TXOP동안 다 전송할 수 없는 경우 작은 프레임으로 잘라서 전송할 수 있다. TXOP의 사용은 기존의 [802.11](https://ko.wikipedia.org/wiki/802.11 "wikilink") [DCF](https://ko.wikipedia.org/wiki/DCF "wikilink") 맥이 가지고 있던 문제점인 낮은 전송률을 가진 station이 과도하게 채널을 점유하는 상황을 줄인다. TXOP 시간 간격이 0인 경우 이것은 하나의 [MAC 서비스 데이터 유닛이나](https://ko.wikipedia.org/wiki/MAC_서비스_데이터_유닛 "wikilink") MMPDU를 의미한다.

access categories (ACs). EDCA에서의 전송 우선순위 단계

| AC                   | CWmin | CWmax | AIFSN | 최대 TXOP |
| -------------------- | ----- | ----- | ----- | ------- |
| 배경 (AC_BK)          | 31    | 1023  | 7     | 0       |
| Best Effort (AC_BE) | 31    | 1023  | 3     | 0       |
| 영상 (AC_VI)          | 15    | 31    | 2     | 3.008ms |
| 음성 (AC_VO)          | 7     | 15    | 2     | 1.504ms |
| 레거시 DCF              | 15    | 1023  | 2     | 0       |

AC별 EDCA 설정 기본값

AC와 이더넷의 [class of service (CoS)](https://ko.wikipedia.org/wiki/IEEE_802.1p "wikilink") 우선순위 레벨의 비교:\[2\]

| 우선순위 | 802.1D 우선순위 | 802.1D 지정 | 접근 범주       |
| ---- | ----------- | --------- | ----------- |
| 낮음   | 1           | BK        | AC_BK      |
|      | 2           | 예비        | AC_BK      |
|      | 0           | BE        | AC_BE      |
|      | 3           | EE        | AC_BE      |
|      | 4           | CL        | 영상 (AC_VI) |
|      | 5           | VI        | 영상 (AC_VI) |
|      | 6           | VO        | 음성 (AC_VO) |
| 높음   | 7           | NC        | 음성 (AC_VO) |

QoS의 가장 주요한 목적은 높은 우선순위의 데이터를 낮은 우선순위의 데이터로부터 보호하는 것이다. 하지만 이와 동시에 데이터를 같은 우선순위의 다른 데이터들로부터 역시 보호해야한다. EDCA의 입장관리는 바로 이런 종류의 문제에 대해 다룬다. AP가 beacon 데이터에 사용 가능한 대역폭(bandwidth)를 적어 알리면 clients는 데이터를 더 전송하기 전에 대역폭을 점검할 수 있다.

[와이파이 멀티미디어](https://ko.wikipedia.org/wiki/와이파이_멀티미디어 "wikilink")(WMM) 인증 AP는 반드시 EDCA와 TXOP을 사용해야한다. 다른 802.11e 기능들은 선택적으로 사용할 수 있다.

### HCF 제어 채널 접근

와이파이 멀티미디어 스케줄 접근(Wi-Fi Multi Media Scheduled Access, WMM-SA)은 HCCA의 와이파이 협력 버전이다. 하지만 WMM-SA는 Wi-Fi 협력 인증으로 사용되지는 않는다.

일반적으로 HCCA는 가장 향상된(그리고 복잡한) 조정 함수이다. HCCA를 이용해서 QoS를 매우 세밀하게 설정할 수 있다. QoS 지원 중계역은 전송속도나 지터(jitter)와 같은 전송 인수를 지정할 수 있다. 이를 통해 와이파이 네트워크 상에서 [VoIP](https://ko.wikipedia.org/wiki/VoIP "wikilink")나 비디오 스트리밍 같은 보다 진보된 서비스를 제공할 수 있다.

HCCA 지원은 802.11e AP의 필수 요구 사항은 아니다. 사실 현재 HCCA를 지원하는 AP는 거의 없다. HCCA를 단말 중계역에 적용할 때에는 채널 접속에 관한 기존의 DCF 메커니즘을 사용한다(DCF나 EDCA의 동작 방식을 그대로 사용하면 된다). 중계역은 poll 메시지에 응답할 수 만 있으면 된다. AP의 경우 스케줄러와 큐잉 메커니즘이 필요하다.

## 그외 802.11e의 특징들

HCCA, EDCA, TXOP 이외에도 802.11e은 802.11 MAC layer의 QoS 향상을 위해 선택적으로 사용할 수 있는 몇가지 추가적인 프로토콜을 정의하고 있다.

### 자동 절전 전달

자동 절전 전달(Automatic power save delivery)은 레거시 802.11 절전 폴링보다 더 효율적인 절전 방법이다.

### 묶음 전송 확인 (Block acknowledgments)

묶음 전송 확인 (Block acknowledgments)은 전체 TXOP에 대해서 한개의 ACK 프레임만으로 전송 확인을 하는 것이다. TXOP가 길게 설정되어 있는 경우 여러번의 ACK 전송으로 인한 불필요한 자원 낭비를 막아준다.

### NoAck

QoS에서 전송 프레임은 QosAck 또는 QosNoAck 값을 가질 수 있다. QosNoAck 값으로 설정된 프레임은 전송에 대한 수신 확인(ACK)을 받지 않는다. 전송 시간에 매우 민감한 데이터의 경우 이미 지나간 데이터를 재전송을 하는 것 보다 시간에 맞는 새로운 데이터를 보내는 것이 더 유리하기 때문에 이러한 방식을 사용한다.

### 직접 링크 설정

직접 링크 설정은 [기본 서비스 셋](https://ko.wikipedia.org/wiki/기본_서비스_셋 "wikilink") 내에서 station간 프레임 직접 전송을 허용한다. station간 전송을 많이 사용하는 소비자를 대비하여 설계되었다.

### 입장 관리 (Admission Control)

특정 접근 범주(Access Category; AC)에 대해 입장 관리(Admission Control)를 사용할 수 있다. AP는 특정 AC가 입장 관리를 사용할 것인지 여부를 EDCA 파라메터의 ACM(Admission Control Mandatory) 필드를 통해 station에 알려주게 된다. 입장 관리를 사용하도록 설정된 AC의 데이터를 전송하려는 station은 데이터 전송 전에 AP로부터 사용 허가를 받은 후 데이터를 전송해야한다. 허가 없이 데이터를 전송하려는 경우 입장 관리가 설정되어 있지 않은 최하위 우선순의를 갖는 AC로 데이터를 전송해야한다. 특정 AC에 ACM이 설정되어있는 경우 그보다 높은 우선순위를 갖는 AC 역시 모두 ACM이 설정되어있어야한다.

## 각주

<references />

[분류:IEEE 802.11](https://ko.wikipedia.org/wiki/분류:IEEE_802.11 "wikilink")

1.
2.  Perahia and Stacey, *Next Generation Wireless LANs*, Cambridge University Press, 2008