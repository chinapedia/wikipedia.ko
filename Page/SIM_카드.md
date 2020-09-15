> This article is converted from Wikipedia: [SIM 카드](https://ko.wikipedia.org/wiki/SIM_카드).


[섬네일의](https://ko.wikipedia.org/wiki/파일:Sim_card.png "wikilink") SIM 카드\]\] **유심칩**이라고도 부르는 **SIM 카드**()는 가입자 식별 모듈(Subscriber Identification Module)을 구현한 IC 카드로, [GSM](../Page/GSM.md "wikilink") 단말기의 필수 요소이다. 보통 단말기 뒤에 들어가는 슬롯이 있고, 이에 끼워넣는 작은 카드를 부르는 말이다. 최초의 SIM 카드는 [1991년](../Page/1991년.md "wikilink")에 [뮌헨](../Page/뮌헨.md "wikilink")의 스마트 카드 제조사 Giesecke & Devrient가 만들었고 첫 300 개의 SIM 카드를 무선 네트워크 통신사 Elisa Oyj (Radiolinja)에 판매하였다.

SIM 카드는 각자의 고유한 번호가 있다. 고정된 번호인 [ICCID](https://ko.wikipedia.org/wiki/:en:Subscriber_identity_module#ICCID "wikilink")(SIM 카드 외부에 기록된 89로 시작하는 19자리 숫자)와 가입자 회선마다 달라지는 [IMSI](https://ko.wikipedia.org/wiki/:en:International_mobile_subscriber_identity "wikilink")(450으로 시작하는 15자리 숫자)가 있으며, 가입자 정보를 가지고 있어서 이 카드만 꽂으면 자기 단말기처럼 쓸 수 있다. 어느 곳으로 여행을 갈 때 단말기가 아닌 이 작은, 지갑 속에도 들어가는, SIM 카드만 있으면 그 나라에서 전화기를 빌려 자기 것처럼 쓸 수 있고, 보안이 뛰어나서 전자상거래 등에서도 효용성이 높다. SIM 카드가 없으면 통화와 문자메시지 등 대부분의 서비스를 사용할 수 없지만, [응급 전화번호로는](../Page/응급_전화번호.md "wikilink") 전화할 수 있다.\[1\] SIM 카드가 장착되지 않은 단말기로 응급 전화를 걸면 상황실에는 전화번호를 알 수 없어 신고자 신원 파악을 위해 단말기 고유 번호([IMEI](https://ko.wikipedia.org/wiki/:en:International_Mobile_Station_Equipment_Identity "wikilink"))가 대신 표시된다.

## 카드 크기

[섬네일](https://ko.wikipedia.org/wiki/파일:GSM_SIM_card_evolution.svg "wikilink")

| 크기                 | 해당 표준                                                                              | 가로 (mm) | 세로 (mm) | 두께 (mm) |
| ------------------ | ---------------------------------------------------------------------------------- | ------- | ------- | ------- |
| 표준(신용카드 크기) SIM 카드 | [ISO/IEC 7810](https://ko.wikipedia.org/wiki/ISO/IEC_7810 "wikilink"):2003, ID-1   | 85.60   | 53.98   | 0.76    |
| 미니 SIM 카드          | ISO/IEC 7810:2003, ID-000                                                          | 25.00   | 15.00   | 0.76    |
| 마이크로 SIM 카드        | [ETSI](https://ko.wikipedia.org/wiki/ETSI "wikilink") TS 102 221 V9.0.0, Mini-UICC | 15.00   | 12.00   | 0.76    |
| 나노 SIM 카드          | ETSI TS 102 221 V11.0.0                                                            | 12.30   | 8.80    | 0.67    |
| 단말기 내장형 SIM 카드     | [JEDEC](https://ko.wikipedia.org/wiki/JEDEC "wikilink") Design Guide 4.8, SON-8    | 6.00    | 5.00    | \<1.0   |

SIM 카드의 크기

카드에서 칩을 제외한 부분은 부피를 차지하는 역할만을 하기 때문에, 큰 SIM을 작은 SIM의 크기, 비율로 잘라내면 호환된다. 전용 도구도 존재하지만\[2\] [커터칼](../Page/커터칼.md "wikilink") 등의 도구를 사용해 잘라써도 무방하다.\[3\]\[4\]

## 범용 사용자 식별 모듈(USIM)

3세대 이동통신 단말기에서 사용하는 사용자 식별 모듈은 *범용 사용자 식별 모듈*(Universal Subscriber Identity Module, USIM)이다. GSM의 SIM이 확장된 표준이다.

[섬네일](https://ko.wikipedia.org/wiki/파일:KTFandKT-USIM.jpg "wikilink")

### USIM의 기능

가입자 식별 모듈(USIM)은 WCDMA 네트워크 접속 및 가입자 인증용 애플리케이션으로 통신용 스마트카드인 UICC(Universal Integrated Circuit Card)에 탑재되어 구동된다. USIM 애플리케이션은 가입자 정보, 네트워크 정보, 인증 정보 등의 중요 정보와 텍스트 메시지, 이메일, 폰 북 등의 개인부가서비스 정보를 저장한다. USIM 애플리케이션은 WCDMA 가입자인증을 위하여 인증센터(AuC:Authentication Center)와 비밀키(K)를 공유하여 아래와 같은 인증절차를 수행한다.

1.  (가입자정보 판독)- 3G단말은 USIM카드로부터 가입자 정보([IMSI](https://ko.wikipedia.org/wiki/:en:International_mobile_subscriber_identity "wikilink"), [ICCID](https://ko.wikipedia.org/wiki/:en:Subscriber_identity_module#ICCID "wikilink"))를 읽어 네트워크(HLR/AuC)로 전송한다.
2.  (인증벡터 생성)- 네트워크(HLR/AuC)는 USIM카드와 공유하는 비밀키(K)로 인증벡터를 생성한 후 USIM카드로 전송한다.
3.  (네트워크 인증)- USIM카드는 비밀키(K')를 이용하여 네트워크 인증센터로부터 수신한 인증벡터(AV)를 검증한다.
4.  (인증 응답값 생성)- USIM카드는 인증 응답값(RES)를 생성하여 네트워크(HLR/AuC)로 전송한다.
5.  (USIM카드 인증)- 네트워크(HLR/AuC)는 USIM카드로부터 수신한 인증 응답값(RES)과 자신이 생성한 인증 응답값(XRES)와 상호 비교하여 USIM카드를 인증한다.

위의 과정을 통하여 USIM카드와 네트워크는 세션 키(*CK, IK*)를 획득하고 이를 통하여 무선 네트워크 서비스의 기밀성(confidentiality)과 무결성(integrity)를 제공하게 된다.

### UICC 서비스

UICC에는 통신 인증용 USIM 애플리케이션 외에도 [자바를](../Page/자바_\(소프트웨어_플랫폼\).md "wikilink") 이용한 뱅킹, 증권, 신용카드, 전자화폐 등의 다양한 응용서비스 애플리케이션을 탑재할 수 있다. 이들 서비스는 나라별로 서비스 방식이 제각각이었으나 최근에는 [SWP를](https://ko.wikipedia.org/wiki/:en:Single_Wire_Protocol "wikilink") 이용한 [NFC](https://ko.wikipedia.org/wiki/NFC "wikilink") 규격으로 통합되고 있다.

## 국가별 사용 현황

SIM 카드는 GSM 통신 방식을 사용하는 국가에서 표준으로 널리 사용된다. [CDMA](https://ko.wikipedia.org/wiki/CDMA "wikilink") 통신 방식을 사용하는 국가에서는 일반적으로 3세대 이동통신 서비스가 시작되면서 USIM 카드 형태로 도입된다.

### 대한민국에서의 이용 현황

대한민국에서 쓰이는 CDMA 방식에는 단말기 각자에 고유번호(IMEI와 ESD)를 가지고 있어서 단말기를 바꿀 수 없고 도입되지 않았다. 대한민국에서는 2002년 6월, [SK텔레콤](../Page/SK텔레콤.md "wikilink")과 [KTF](https://ko.wikipedia.org/wiki/KTF "wikilink")가 WCDMA 시범서비스를 실시하면서 일부 도입되었으며\[5\] [2007년](../Page/2007년.md "wikilink") 3월 1일 [KTF](https://ko.wikipedia.org/wiki/KTF "wikilink")가, 2007년 3월 30일 [SK텔레콤](../Page/SK텔레콤.md "wikilink")이 [WCDMA](https://ko.wikipedia.org/wiki/WCDMA "wikilink") HSDPA 전국망 서비스를 시작하며 본격적으로 보급되기 시작했다.\[6\]

대한민국의 [방송통신위원회](https://ko.wikipedia.org/wiki/방송통신위원회 "wikilink")는 2008년 5월 22일 [WCDMA](../Page/광대역_부호_다중_분할_접속.md "wikilink") 단말기의 잠금 설정(USIM Lock) 해제를 위한 관련 규정 제정을 의결하였다. 이 제도가 실제로 시행된 후 이동통신사업자를 바꾸더라도 USIM만 바꿔 꽂으면 이전 단말기를 그대로 사용할 수 있다. 하지만 2012년 5월 1일 이전에 출시한 단말기는 사업자간 시스템의 차이로 인해 음성통화와 [SMS만](../Page/단문_메시지_서비스.md "wikilink") 사용할 수 있다. 2012년 5월 이후 출시되는 단말기는 OMA-MMS를 탑재하여 사업자가 달라도 [MMS를](../Page/멀티미디어_메시지_서비스.md "wikilink") 문제없이 쓸 수 있다.

그리고 이동통신사업자가 유통을 하지 않고 사용을 허가하지 않은 단말기는 사용할 수 없도록 단말기 화이트리스트 제도를 운영하였고, 2012년 5월, 이동통신사에 등록되지 않은 단말기도 사용할 수 있게 단말기 자급제가 **일부** 시행되었다. 하지만 그 이후에도 단말기 고유 번호([IMEI](https://ko.wikipedia.org/wiki/:en:International_Mobile_Station_Equipment_Identity "wikilink"))는 여전히 통신사 종속적이다.

USIM만 있으면 기술상 큰 문제가 없지만\[7\], 대한민국에서는 이동통신사업자의 단말기 통제시스템(EIR)을 화이트리스트 방식으로 운영하여 이동통신사가 허용한 단말기에서도 이동통신사업자가 허용한 서비스만 이용이 가능하다.\[8\], 단말기에서 해당 서비스 이용이 가능하다 하더라도 이동통신사업자가 해당 단말기를 전산 등록하지 않는 한 사용할 수 없도록 단말기 통제 시스템을 구축하였다.

그러다가 [2012년](../Page/2012년.md "wikilink") [5월 1일](../Page/5월_1일.md "wikilink") **단말기 자급제**가 **일부** 시행되어 이동통신사업자에 등록되지 않은 단말기라도 (공식대리점 또는 고객센터를 방문하여)기기 등록·개통 과정을 거치지 않고 현재 사용 중인 USIM을 바로 꽂아 쓰는 것이 가능해졌다. 이 시정내용은 이동통신사업자가 유통하지 않은 자급제 단말기에 해당하는 내용으로, 이동통신사업자를 통해 유통하는 단말기(예를 들어, 대한민국에서 모델명이 숫자+S·K·L인 단말기)\[9\] 는 개통 과정이 진행되지 않은 경우 현재 사용 중인 USIM을 꽂아도 사용이 불가능하다. 즉, 경품·공장수리 등으로 지급받은 이동통신사업자 유통 단말기를 쓰려면 여전히 기존과 동일하게 개통 과정을 거쳐야 한다. 이들 이동통신사업자 유통 단말기는 개통 과정 이전에는 [응급 전화번호로만](../Page/응급_전화번호.md "wikilink") 전화를 걸 수 있다. 예를 들어, 삼성 디지털플라자 매장에서 판매하는 *자가유통용* [삼성](https://ko.wikipedia.org/wiki/삼성전자 "wikilink") 갤럭시 시리즈는 자급제 단말기가 아니라 이동통신사업자 유통 단말기이므로 현재 사용 중인 USIM을 꽂는 것만으로는 응급 전화번호 이외에는 통화가 불가능하며, 개통 과정을 거쳐야 정상적으로 사용할 수 있다.

단말기 자급제가 일부 시행된 이후([LG유플러스](../Page/LG유플러스.md "wikilink")는 2014년 7월 이후), 대한민국의 이동통신사업자 3사가 유통하지 않은 단말기, 즉 자급제 단말기에 각각의 이동통신사업자의 USIM을 꽂으면 아래 예시와 같이 해당 단말기는 "대한민국의 이동통신시업자 3사가 유통하지 않은 자급제 단말기"임을 알리는 안내 [문자 메시지가](../Page/단문_메시지_서비스.md "wikilink") 가입자에게 발송된다.

USIM을 이용해 이동통신 서비스를 제공할 경우 USIM의 고유 번호([IMSI와](https://ko.wikipedia.org/wiki/:en:International_mobile_subscriber_identity "wikilink") [ICCID](https://ko.wikipedia.org/wiki/:en:Subscriber_identity_module#ICCID "wikilink"))만으로 사용자를 식별하기 때문에 이동통신사업자의 약정·할부 프로그램으로 구입한 경우를 제외하고는\[10\] 단말기 고유 번호(IMEI)를 통제할 이유가 없어지지만, 대한민국의 형법 제 347조와 통신비밀보호법에서는 USIM의 고유 번호([IMSI](https://ko.wikipedia.org/wiki/:en:International_mobile_subscriber_identity "wikilink"), [ICCID](https://ko.wikipedia.org/wiki/:en:Subscriber_Identity_Module#ICCID "wikilink"))가 아닌 단말기 고유 번호([IMEI](https://ko.wikipedia.org/wiki/:en:International_Mobile_Station_Equipment_Identity "wikilink"))를 복제한 자를 처벌한다고 명시되어 있다.\[11\] 이동통신사업자가 단말기 고유 번호(IMEI)를 통제하는 데 법령이 일조하고 있는 셈이다. 또한 USIM의 가격이 뻥튀기되어 이동통신사업자가 부당 이득을 챙긴다는 논란이 제기되고 있다.\[12\] [2014년](../Page/2014년.md "wikilink") [국정감사](https://ko.wikipedia.org/wiki/국정감사 "wikilink")에서는 대한민국의 이동통신사업자가 USIM 판매로 4천억원 이상의 수익을 올렸다는 것을 지적하였다.\[13\] 또한 ICT 소비자정책연구원은 대한민국의 이동통신사업자가 USIM 판매로 1173억원의 부당수익을 올렸다고 주장하였다.\[14\] 2018년 3월 31일부터는 유심가격이 1100원인하되었다.

#### 대한민국의 USIM 이동성 연혁

  - [KTF](https://ko.wikipedia.org/wiki/KTF "wikilink")가 [2007년](../Page/2007년.md "wikilink") [3월 1일](../Page/3월_1일.md "wikilink"), [SK텔레콤](../Page/SK텔레콤.md "wikilink")이 2007년 [3월 30일](../Page/3월_30일.md "wikilink") [WCDMA](../Page/광대역_부호_다중_분할_접속.md "wikilink") HSDPA 서비스를 시작하면서\[15\] USIM과 이동통신단말기가 보급되기 시작하였으나, [SK텔레콤](../Page/SK텔레콤.md "wikilink")과 [KTF](https://ko.wikipedia.org/wiki/KTF "wikilink")가 각자 유통한 단말기에 타 사업자의 USIM은 인식하지 않고 거부하도록 하였다.
  - 2008년 7월 이후 출시되는 단말기는 해당 사업자의 USIM이 아닌 타 사업자의 USIM을 거부하지 않도록 시정되었다 (캐리어 락을 걸지 못하도록 시정).
      - 이 시정내용으로 인해 대한민국의 [WCDMA](../Page/광대역_부호_다중_분할_접속.md "wikilink") 이동통신사업자인 [SK텔레콤](../Page/SK텔레콤.md "wikilink")과 [KTF](https://ko.wikipedia.org/wiki/KTF "wikilink")가 각자 유통한 단말기의 [IMEI를](https://ko.wikipedia.org/wiki/:en:International_Mobile_Station_Equipment_Identity "wikilink") 공유하도록 하였다\[16\]. 이는 2012년 5월, 단말기 자급제가 일부 시행된 이후에도 여전히 유효하다.
      - 이 시정내용은 타 사업자의 USIM을 장착할 경우 음성통화와 영상통화, [SMS를](../Page/단문_메시지_서비스.md "wikilink") 문제없이 이용할 수 있게 하고 있다.
      - 이 과정에서 사업자들이 '신청한 고객에 한하여' 타 사업자의 USIM을 쓸 수 있게 하여 과징금을 부과한바 있다.\[17\]
  - 2010년 7월 이후 출시되는 단말기는 대한민국 사업자의 USIM이 아닌 해외의 USIM을 거부하지 않도록 시정되었다 (컨트리 락을 걸지 못하도록 시정).
  - 2011년 7월, [Lte](https://ko.wikipedia.org/wiki/롱_텀_에볼루션 "wikilink") 단말기의 영상통화 규격이 사업자별로 달라 Lte 단말기는 타 사업자의 USIM을 장착할 경우 Lte 영상통화를 사용할 수 없게 되었다. [WCDMA](../Page/광대역_부호_다중_분할_접속.md "wikilink") 단말기는 여전히 타 사업자의 USIM을 장착해서 3G 영상통화를 사용할 수 있다.
      - [LG유플러스](../Page/LG유플러스.md "wikilink")가 유통하지 않은 단말기를 LG유플러스에서 음성통화를 사용할 수 없는 점을 참작하여, [LG유플러스](../Page/LG유플러스.md "wikilink")에서 유통한 Lte 단말기는 [SK텔레콤](../Page/SK텔레콤.md "wikilink")과 [KT](../Page/KT.md "wikilink")의 USIM을 인식하지 않고 거부하도록 설정하여 출시하였다. (캐리어 락 일부 설정)
      - [LG유플러스](../Page/LG유플러스.md "wikilink")에서 유통한 Lte 단말기라도 SK텔레콤과 KT가 아닌 타 사업자의 USIM은 거부하지 않아, 해외 사업자의 USIM을 [LG유플러스](../Page/LG유플러스.md "wikilink")가 유통한 Lte 단말기에 장착할 경우 정상적으로 사용할 수 있다.
      - 마찬가지로 [SK텔레콤](../Page/SK텔레콤.md "wikilink")과 [KT](../Page/KT.md "wikilink")가 아닌 해외 사업자의 USIM을 장착할 경우, SK텔레콤 혹은 KT의 네트워크를 로밍으로 이용할 수 있다.
  - 2012년 5월, 단말기 자급제가 **일부** 시행되어 대한민국의 [WCDMA](../Page/광대역_부호_다중_분할_접속.md "wikilink") 이동통신사업자인 [SK텔레콤](../Page/SK텔레콤.md "wikilink")과 [KT](../Page/KT.md "wikilink")가 유통하지 않은, 즉 해당 사업자에 등록되지 않은 단말기를 거부하지 않도록 시정되었다. 이 부분을 제외한 단말기 통제 시스템(White-List)은 여전히 유효하다. 더불어 단말기 외부에 [IMEI를](https://ko.wikipedia.org/wiki/:en:International_Mobile_Station_Equipment_Identity "wikilink") 표기하도록 의무화하였다.
      - 대한민국의 이동통신사업자 3사가 참여하는 한국정보통신진흥협회에서 [분실 단말기 조회 서비스](http://www.checkimei.kr) 를 제공하게 되어 이 곳에서 [IMEI를](https://ko.wikipedia.org/wiki/:en:International_Mobile_Station_Equipment_Identity "wikilink") 조회하여 분실·도난 신고 여부를 확인할 수 있게 되었다.
  - 2012년 5월 이후 출시되는 단말기는 해당 사업자의 고유 MMS가 아닌 [OMA](https://ko.wikipedia.org/wiki/:en:Open_Mobile_Alliance "wikilink")-MMS를 탑재하여, 타 사업자의 USIM을 장착해도 [MMS를](../Page/멀티미디어_메시지_서비스.md "wikilink") 정상적으로 이용할 수 있게 되었다.
      - ①[삼성](https://ko.wikipedia.org/wiki/삼성 "wikilink") 갤럭시 시리즈: [삼성 갤럭시 R 스타일](../Page/삼성_갤럭시_R_스타일.md "wikilink") 및 [삼성 갤럭시 S III와](../Page/삼성_갤럭시_S_III.md "wikilink") 이후 출시모델, ②[LG](https://ko.wikipedia.org/wiki/LG "wikilink") 옵티머스 시리즈: [LG 옵티머스 LTE 태그](../Page/LG_옵티머스_LTE_태그.md "wikilink") 및 [LG 옵티머스 뷰와](../Page/LG_옵티머스_뷰.md "wikilink") 이후 출시모델, ③[팬택](../Page/팬택.md "wikilink") 베가 시리즈: [베가 레이서 2](https://ko.wikipedia.org/wiki/베가_레이서_2 "wikilink") 및 [베가 S5와](https://ko.wikipedia.org/wiki/베가_S5 "wikilink") 이후 출시모델. ④그리고 kt테크의 테이크 [HD](../Page/KT테크_테이크_HD.md "wikilink")·[핏](../Page/KT테크_테이크_핏.md "wikilink")·[LTE](../Page/KT테크_테이크_LTE.md "wikilink").

<!-- end list -->

  - 2013년 11월 20일 이후 출시되는 [LG유플러스](../Page/LG유플러스.md "wikilink")의 Lte 단말기는 [SK텔레콤](../Page/SK텔레콤.md "wikilink")과 [KT](../Page/KT.md "wikilink")의 USIM을 거부하지 않도록 시정되었다.
      - ①삼성 갤럭시 시리즈: [삼성 갤럭시 그랜드 2와](../Page/삼성_갤럭시_그랜드_2.md "wikilink") 이후 출시모델, ②LG G 시리즈: [LG Gx](../Page/LG_Gx.md "wikilink") 및 [LG G 프로 2와](../Page/LG_G_프로_2.md "wikilink") 이후 출시모델, ③팬택 베가 시리즈: [베가 시크릿 업](../Page/팬택_베가_시크릿_업.md "wikilink")·[아이언 2](../Page/팬택_베가_아이언_2.md "wikilink")·[팝업노트](../Page/팬택_베가_팝업노트.md "wikilink").
  - 2014년 7월 이후 출시되는 단말기는 타 사업자의 USIM을 장착해도 음성통화([WCDMA](../Page/광대역_부호_다중_분할_접속.md "wikilink") 단말기), [Lte 음성통화](https://ko.wikipedia.org/wiki/VoLTE "wikilink")([Lte](https://ko.wikipedia.org/wiki/롱_텀_에볼루션 "wikilink") 단말기), Lte 영상통화(Lte 단말기), [SMS](../Page/단문_메시지_서비스.md "wikilink"), [MMS](../Page/멀티미디어_메시지_서비스.md "wikilink"), Lte 네트워크(Lte 단말기)를 모두 정상적으로 이용할 수 있도록 시정되었다.
      - 이 시정내용은 이동통신사업자가 유통한 단말기에만 해당하여\[18\], 이동통신사업자가 유통하지 않은, 즉 해당 사업자에 등록되지 않은 단말기는 여전히 [Lte 음성통화를](https://ko.wikipedia.org/wiki/VoLTE "wikilink") 쓸 수 없는 단말기도 유통되어 [소니 엑스페리아 Z3](../Page/소니_엑스페리아_Z3.md "wikilink"), [소니 엑스페리아 C3](../Page/소니_엑스페리아_C3.md "wikilink") 등이 [Lte 음성통화를](https://ko.wikipedia.org/wiki/VoLTE "wikilink") 지원하지 않음에도 정상적으로 출시·유통되었다.
      - 그러나 이후 일간지 [아시아경제](https://ko.wikipedia.org/wiki/아시아경제 "wikilink")가 "이동통신사업자가 유통하지 않는 [레노버 PHAB Plus가](https://ko.wikipedia.org/wiki/레노버_PHAB_Plus "wikilink") [Lte 음성통화가](https://ko.wikipedia.org/wiki/VoLTE "wikilink") 불가능한데도 출시·유통되고 있다"며 이점을 지적\[19\]한 이후, 이것이 시정되어 이동통신사업자가 유통하지 않는 단말기도 이 규정을 적용받게 되었다.
      - 이 시정내용으로 인해 대한민국의 이동통신사업자 3사가 각자 유통한 단말기의 [IMEI를](https://ko.wikipedia.org/wiki/:en:International_Mobile_Station_Equipment_Identity "wikilink") 3사가 모두 공유하도록 하여\[20\], 결과적으로 '단말기 자급제'에 정면으로 배치되는, 즉 단말기 통제 시스템(White-List)이 더욱 견고해지게 되는 결과를 낳게 되었다. 이동통신사업자가 유통\[21\]하지 않는 단말기는 이러하지 않는다.
      - ①애플 아이폰 시리즈: [아이폰 6](../Page/아이폰_6.md "wikilink")·[6 플러스와](../Page/아이폰_6_플러스.md "wikilink") 이후 출시모델, ②LG G 시리즈: [LG 아이스크림 스마트](../Page/LG_아이스크림_스마트.md "wikilink"), [LG 아카와](../Page/LG_아카.md "wikilink") 이후 출시모델, ③삼성 갤럭시 시리즈: [삼성 갤럭시 노트 4](https://ko.wikipedia.org/wiki/삼성_갤럭시_노트_4 "wikilink"), [삼성 갤럭시 그랜드 맥스와](../Page/삼성_갤럭시_그랜드_맥스.md "wikilink") 이후 출시모델.

#### USIM의 PIN 번호

대한민국에서 유통되고 있는 USIM은 PIN 번호가 초기값으로 0000으로 되어 있으며, PIN2 번호는 대한민국의 이동통신사업자 3사가 유통하는 단말기에서는 사용하지 않는다는 이유로 해당 기능을 쓰지 못하게 해 두었을 뿐만 아니라, PUK2 번호 또한 공개하지 않고 있다.

각각의 USIM에는 PUK 번호 (8자리로 고정되어 있다) 와 PUK2 번호 (8자리로 고정되어 있다) 가 할당되어 있다. PIN 번호는 사용자의 필요에 따라 4\~8자리로 변경할 수 있다.

PIN 번호 혹은 PIN2 번호를 3회 연속 잘못 입력하면 잠기게 되며, PUK 번호 혹은 PUK2 번호를 입력하여 PIN 번호 혹은 PIN2 번호를 다시 설정할 수 있다. PUK 번호를 10회 연속 잘못 입력하면 폐기하고 다시 구매해야 하며, PUK2 번호를 10회 연속 잘못 입력하면 [특정 번호로의 발신 제한](https://ko.wikipedia.org/wiki/:en:Fixed_Dialing_Number "wikilink") 등 해당 기능이 잠기게 된다.

#### 대한민국 통신사의 USIM 예시

<table>
<caption>대한민국의 기간이동통신사(MNO)에서 현재 생산중인 USIM</caption>
<thead>
<tr class="header">
<th><p>구분</p></th>
<th><p>통신사</p></th>
<th><p>모델명</p></th>
<th><p><a href="https://ko.wikipedia.org/wiki/#카드_크기" title="wikilink">크기 구분</a></p></th>
<th><p><a href="https://ko.wikipedia.org/wiki/#UICC_서비스" title="wikilink">UICC 기능 구분</a></p></th>
<th><p>네트워크 구분</p></th>
<th><p>판매 가격<br />
(<a href="https://ko.wikipedia.org/wiki/부가가치세" title="wikilink">부가세</a> 포함)</p></th>
<th><p>기타 특징</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>*</p></td>
<td><p><a href="../Page/LG유플러스.md" title="wikilink">LG유플러스</a></p></td>
<td><p>xyy00</p></td>
<td><p>미니&amp;마이크로</p></td>
<td><p>통신 인증용 USIM</p></td>
<td><p>구분없음</p></td>
<td><p>2,200원</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>*</p></td>
<td><p>LG유플러스</p></td>
<td><p>xyy00</p></td>
<td><p>미니&amp;마이크로</p></td>
<td><p>통신 인증용 USIM+NFC 모듈</p></td>
<td><p>구분없음</p></td>
<td><p>7700원</p></td>
<td><p>"NFC 유심"이라고도 부른다.</p></td>
</tr>
<tr class="odd">
<td><p>*</p></td>
<td><p>LG유플러스</p></td>
<td><p>xyy00</p></td>
<td><p>나노</p></td>
<td><p>통신 인증용 USIM</p></td>
<td><p>구분없음</p></td>
<td><p>2,200원</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>*</p></td>
<td><p>LG유플러스</p></td>
<td><p>xyy00</p></td>
<td><p>나노</p></td>
<td><p>통신 인증용 USIM+NFC 모듈</p></td>
<td><p>구분없음</p></td>
<td><p>7700원</p></td>
<td><p>"NFC 유심"이라고도 부른다.</p></td>
</tr>
<tr class="odd">
<td><p>*</p></td>
<td><p><a href="../Page/SK텔레콤.md" title="wikilink">SK텔레콤</a></p></td>
<td><p>CTD-x0y</p></td>
<td><p>미니&amp;마이크로</p></td>
<td><p>통신 인증용 USIM</p></td>
<td><p>구분없음</p></td>
<td><p>5500원[22][23]</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>*</p></td>
<td><p>SK텔레콤</p></td>
<td><p>NFCD-x0y</p></td>
<td><p>미니&amp;마이크로</p></td>
<td><p>통신 인증용 USIM+NFC 모듈</p></td>
<td><p>구분없음</p></td>
<td><p>&lt;!--티머니 선탑재 정책 파기, 최초 다운로드과정 필요</p></td>
<td><p>--&gt;7700원[24]</p></td>
</tr>
<tr class="odd">
<td><p>*</p></td>
<td><p>SK텔레콤</p></td>
<td><p>CTN-x0y</p></td>
<td><p>나노</p></td>
<td><p>통신 인증용 USIM</p></td>
<td><p>구분없음</p></td>
<td><p>5500원[25][26]</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>*</p></td>
<td><p>SK텔레콤</p></td>
<td><p>NFCN-x0y</p></td>
<td><p>나노</p></td>
<td><p>통신 인증용 USIM+NFC 모듈</p></td>
<td><p>구분없음</p></td>
<td><p>&lt;!--티머니 선탑재 정책 파기, 최초 다운로드과정 필요</p></td>
<td><p>--&gt;7700원[27]</p></td>
</tr>
<tr class="odd">
<td><p>*</p></td>
<td><p>KT</p></td>
<td><p>xx-x1400</p></td>
<td><p>미니&amp;마이크로</p></td>
<td><p>통신 인증용 USIM</p></td>
<td><p><a href="../Page/광대역_부호_다중_분할_접속.md" title="wikilink">WCDMA</a></p></td>
<td><p>4400원</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>*</p></td>
<td><p><a href="../Page/KT.md" title="wikilink">KT</a></p></td>
<td><p>xx-L1650</p></td>
<td><p>미니&amp;마이크로</p></td>
<td><p>통신 인증용 USIM+NFC 모듈</p></td>
<td><p>WCDMA, <a href="https://ko.wikipedia.org/wiki/롱_텀_에볼루션" title="wikilink">LTE</a></p></td>
<td><p>7700원[28]</p></td>
<td><p>"NFC 유심", "LTE유심"이라고도 부른다.</p></td>
</tr>
<tr class="odd">
<td><p>*</p></td>
<td><p>KT</p></td>
<td><p>xx-L1655</p></td>
<td><p>나노</p></td>
<td><p>통신 인증용 USIM+NFC 모듈</p></td>
<td><p>WCDMA, LTE</p></td>
<td><p>7700원[29]</p></td>
<td><p>"NFC 유심", "LTE유심"이라고도 부른다.</p></td>
</tr>
</tbody>
</table>

<table>
<caption>대한민국의 기간이동통신사(MNO)에서 사용되었던 USIM (현재 재고 판매)</caption>
<thead>
<tr class="header">
<th><p>구분</p></th>
<th><p>통신사</p></th>
<th><p>모델명</p></th>
<th><p><a href="https://ko.wikipedia.org/wiki/#카드_크기" title="wikilink">크기 구분</a></p></th>
<th><p><a href="https://ko.wikipedia.org/wiki/#UICC_서비스" title="wikilink">UICC 기능 구분</a></p></th>
<th><p>네트워크 구분</p></th>
<th><p>선 탑재된<br />
<a href="../Page/교통카드.md" title="wikilink">교통카드</a> 애플릿</p></th>
<th><p>판매 가격<br />
(<a href="https://ko.wikipedia.org/wiki/부가가치세" title="wikilink">부가세</a> 포함)</p></th>
<th><p>기타 특징</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><p>SK텔레콤</p></td>
<td><p>CT-x0y</p></td>
<td><p>미니</p></td>
<td><p>통신 인증용 USIM</p></td>
<td><p>구분없음</p></td>
<td><p>-</p></td>
<td><p>5,500원</p></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>SK텔레콤</p></td>
<td><p>COMBI-x0y</p></td>
<td><p>미니</p></td>
<td><p>통신 인증용 USIM+금융 애플릿</p></td>
<td><p>구분없음</p></td>
<td><p><a href="../Page/티머니.md" title="wikilink">티머니</a></p></td>
<td><p>7,700원</p></td>
<td><p>"콤비 유심", "금융 유심"이라고도 부른다.</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>SK텔레콤</p></td>
<td><p>NFC-x0y</p></td>
<td><p>미니</p></td>
<td><p>통신 인증용 USIM+NFC 모듈</p></td>
<td><p>구분없음</p></td>
<td><p>티머니</p></td>
<td><p>9,900원</p></td>
<td><p>"NFC 유심"이라고도 부른다.</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>SK텔레콤</p></td>
<td><p>OPMD-x0y</p></td>
<td><p>미니</p></td>
<td><p>통신 인증용 USIM</p></td>
<td><p>구분없음</p></td>
<td><p>-</p></td>
<td><p>7,700원</p></td>
<td><p>데이터셰어링에만 사용[30]</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>SK텔레콤</p></td>
<td><p>OPMDM-x0y</p></td>
<td><p>마이크로</p></td>
<td><p>통신 인증용 USIM</p></td>
<td><p>구분없음</p></td>
<td><p>-</p></td>
<td><p>7,700원</p></td>
<td><p>데이터셰어링에만 사용[31]</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>SK텔레콤</p></td>
<td><p>CTM-x0y</p></td>
<td><p>마이크로</p></td>
<td><p>통신 인증용 USIM</p></td>
<td><p>구분없음</p></td>
<td><p>-</p></td>
<td><p>5,500원</p></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>SK텔레콤</p></td>
<td><p>NFCM-x0y</p></td>
<td><p>마이크로</p></td>
<td><p>통신 인증용 USIM+NFC 모듈</p></td>
<td><p>구분없음</p></td>
<td><p>티머니</p></td>
<td><p>9,900원</p></td>
<td><p>"NFC 유심"이라고도 부른다.</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>KT</p></td>
<td><p>AX-1400<br />
xx-B1400<br />
xx-C1400</p></td>
<td><p>미니</p></td>
<td><p>통신 인증용 USIM</p></td>
<td><p><a href="../Page/광대역_부호_다중_분할_접속.md" title="wikilink">WCDMA</a></p></td>
<td><p>-</p></td>
<td><p>5,500원</p></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>KT</p></td>
<td><p>xx-M1400</p></td>
<td><p>마이크로</p></td>
<td><p>통신 인증용 USIM</p></td>
<td><p>WCDMA</p></td>
<td><p>-</p></td>
<td><p>5,500원</p></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td><p>KT</p></td>
<td><p>xx-Z1y00</p></td>
<td><p>미니</p></td>
<td><p>통신 인증용 USIM+KT의 와이브로 인증 애플리케이션</p></td>
<td><p>WCDMA, <a href="../Page/와이브로.md" title="wikilink">WiBro</a></p></td>
<td><p>-</p></td>
<td><p>11,000원</p></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td><p>KT</p></td>
<td><p>xx-D14y0</p></td>
<td><p>미니</p></td>
<td><p>통신 인증용 USIM+금융 애플릿</p></td>
<td><p>WCDMA</p></td>
<td><p>티머니</p></td>
<td><p>8,800원</p></td>
<td><p>"콤비 유심", "금융 유심"이라고도 부른다.</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>KT</p></td>
<td><p>xx-N1650</p></td>
<td><p>미니</p></td>
<td><p>통신 인증용 USIM+NFC 모듈</p></td>
<td><p>WCDMA</p></td>
<td><p>티머니</p></td>
<td><p>5,500원[32]</p></td>
<td><p>"NFC 유심"이라고도 부른다.</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>KT</p></td>
<td><p>xx-N167y</p></td>
<td><p>미니</p></td>
<td><p>통신 인증용 USIM+NFC 모듈</p></td>
<td><p>WCDMA</p></td>
<td><p>캐시비</p></td>
<td><p>5,500원[33]</p></td>
<td><p>"NFC 유심"이라고도 부른다.</p></td>
</tr>
<tr class="even">
<td></td>
<td><p>KT</p></td>
<td><p>xx-L1670</p></td>
<td><p>미니&amp;마이크로</p></td>
<td><p>통신 인증용 USIM+NFC 모듈</p></td>
<td><p>WCDMA, LTE</p></td>
<td><p><a href="../Page/캐시비.md" title="wikilink">캐시비</a></p></td>
<td><p>8,800원[34]</p></td>
<td><p>"NFC 유심", "LTE유심"이라고도 부른다.</p></td>
</tr>
<tr class="odd">
<td></td>
<td><p>KT</p></td>
<td><p>xx-L1675</p></td>
<td><p>나노</p></td>
<td><p>통신 인증용 USIM+NFC 모듈</p></td>
<td><p>WCDMA, LTE</p></td>
<td><p>캐시비</p></td>
<td><p>8,800원[35]</p></td>
<td><p>"NFC 유심", "LTE유심"이라고도 부른다.</p></td>
</tr>
</tbody>
</table>

  - **x**는 임의의 알파벳을 나타내며, 제조사를 구분하는 데 쓰인다. 각각 [LG CNS](https://ko.wikipedia.org/wiki/LG_CNS "wikilink")(C), [젬알토](https://ko.wikipedia.org/wiki/:en:Gemalto "wikilink")(G·GE), [코나아이](https://ko.wikipedia.org/wiki/코나아이 "wikilink")(K·KE), [유비벨록스](https://ko.wikipedia.org/wiki/유비벨록스 "wikilink")(U), [솔라시아](../Page/솔라시아.md "wikilink")(S·SA) 등이다.
  - **y**는 임의의 숫자를 나타낸다.
  - KT는 위 표에서 알 수 있듯이, ①[WCDMA](../Page/광대역_부호_다중_분할_접속.md "wikilink") 전용 USIM, ②WCDMA·[LTE](https://ko.wikipedia.org/wiki/롱_텀_에볼루션 "wikilink") 겸용 USIM, ③WCDMA·[와이브로](../Page/와이브로.md "wikilink") 겸용 UICC로 각각 구분하여 제조·판매하고 있어 가입자의 혼란을 가중시키고 있다\[36\]. KT의 네트워크를 이용하는 [알뜰폰(MVNO)](https://ko.wikipedia.org/wiki/가상이동통신사업자 "wikilink") 또한 동일하게 ①[WCDMA](../Page/광대역_부호_다중_분할_접속.md "wikilink") 전용 USIM, ②WCDMA·[LTE](https://ko.wikipedia.org/wiki/롱_텀_에볼루션 "wikilink") 겸용 USIM을 구분하여 판매하고 있다.
  - KT는 위 표에서 알 수 있듯이, WCDMA·LTE 겸용 USIM은 모두 NFC 모듈이 탑재되어 있다.
  - [NFC](../Page/근거리_무선_통신.md "wikilink") 모듈이 탑재된 USIM에는 [교통카드](../Page/교통카드.md "wikilink") 애플릿, 모바일신용카드 애플릿과 [뱅크월렛](https://ko.wikipedia.org/wiki/뱅크월렛 "wikilink")([유비터치](https://ko.wikipedia.org/wiki/유비터치 "wikilink")) 애플릿을 최대 100개까지 탑재할 수 있다. [구글 안드로이드](https://ko.wikipedia.org/wiki/구글_안드로이드 "wikilink") 단말기에서 이용할 수 있으며, 관련 앱【SK텔레콤은 '[스마트터치(SmartTouch)](https://play.google.com/store/apps/details?id=com.skplanet.nfc.smarttouch)', KT는 '[CLiP](https://play.google.com/store/apps/details?id=com.kt.android.showtouch)', LG유플러스는 '[스마트월렛(SmartWallet)](https://play.google.com/store/apps/details?id=com.lguplus.usimsvcm)'】에서 주카드를 설정할 수 있다.
  - 교통카드 애플릿이 선 탑재된 경우, 별도의 발급절차 없이 단말기에 장착하는 즉시 플라스틱카드와 동일하게 충전과 결제가 가능하다. (단말기의 NFC 카드모드 에뮬레이션 기능이 켜져 있어야 한다.) [티머니](../Page/티머니.md "wikilink") 로고가 단독으로 새겨진 USIM이 이에 해당하며, 교통카드 로고가 없거나, 여러 교통카드 로고가 새겨진 USIM은 별도의 발급절차를 거쳐야 한다.
  - 엉뚱한 SIM 카드를 구입한 경우, [표준 크기용](https://ko.wikipedia.org/wiki/#카드_크기 "wikilink") 어댑터(8982로 시작하는 ICCID 바코드가 있는 테두리 부분)를 동봉하여 구입 14일 이내에 **공식대리점이 아닌** [지점](http://www.tworld.co.kr/normal.do?serviceId=S_CMIS0001&viewId=V_CENT0099#)(SK텔레콤), [플라자](https://web.archive.org/web/20130328232957/http://my.olleh.com/plaza/KTStoreSearch.action)(KT), [직영대리점](http://www.uplus.co.kr/ent/fglt/MbLteRcmPlusCash01.hpi)(LG유플러스) 혹은 구입처에서 다른 SIM 카드로 무상 교체할 수 있다. 어댑터를 분실하였거나 14일 이후라면 교체가 불가능하며 새로 구입하여야 한다. 구입한 USIM이 불량이라면 1년 이내에 동일 모델로 교체가 가능하지만 번거로운 과정 탓에 관련 민원이 다수 제기되고 있다.\[37\]

<!-- end list -->

  - [LG유플러스](../Page/LG유플러스.md "wikilink") (45006, 898206)

파일:LG유플러스-U9700.jpg|U9700 파일:LGUplus_NFC_UICC.jpg|K1200 파일:LG유플러스-K3200.jpg|K3200 |C4900 |K3700

  - [KT](../Page/KT.md "wikilink") (45008, 898230)

파일:kt-usim.jpg|OT-B1400 파일:KT-Micro-UICC.jpg|GE-M1400 파일:KT-WiBro-UICC.jpg|GE-Z1200([와이브로](../Page/와이브로.md "wikilink")겸용) 파일:KT-UICC-NFCusim.jpg|KE-N1650 파일:KT-NFC-cashbee-USIM.jpg|GE-N1670 파일:KT-UICC-combiusim.jpg|KE-D1460 |GE-L1650([LTE겸용](https://ko.wikipedia.org/wiki/롱_텀_에볼루션 "wikilink")) |KE-L1655([LTE겸용](https://ko.wikipedia.org/wiki/롱_텀_에볼루션 "wikilink")) |MV-L1675([LTE겸용](https://ko.wikipedia.org/wiki/롱_텀_에볼루션 "wikilink"))

  - [SK텔레콤](../Page/SK텔레콤.md "wikilink") (45005, 898205)

파일:skt-usim.jpg|CT-G04 파일:SKT-UICC-combiusim.jpg|COMBI-S05 파일:SKT-UICC-NFCUSIM.jpg|NFC-S03 파일:SKT-micro-UICC.jpg|CTD-W01 |NFCD-S01 파일:SKtelecom-NFCN-G03.jpg|NFCN-G03

  - [알뜰폰(MVNO)](https://ko.wikipedia.org/wiki/가상이동통신사업자 "wikilink")

파일:KCT-tplus-SKT-mvno.jpg|한국케이블텔레콤 티플러스 · 티브로드, 45011, 898211 파일:SKT-MVNO-ecomobile(tplus)-UICC.jpg|케이디링크 에코모바일, 45011, 898211 파일:Korea-LGUPLUS-MVNO-spacenet-freet.jpg|인스코비 프리티, 45006, 898206 파일:Mvno-yyt-lguplus.jpg|와이엘랜드 여유텔레콤, 45006, 898206 파일:Mvno-umobi-lguplus.jpg|미디어로그 유모비, 45006, 898206 파일:SKT-MVNO-Eyesmobile-UICC.jpg|아이즈비전 아이즈모바일, 45005, 898205 파일:SKtelink-USIM.jpg|SK텔링크 세븐모바일, 45005, 898205 파일:SKT-mvno-unicoms-MOBING.jpg|유니컴즈 모빙, 45005, 898205 파일:SKt-cjhello-MVNO.jpg|CJ헬로비전 헬로모바일, 45005, 898205 파일:프리텔레콤-freeTkt알뜰폰.jpg|프리텔레콤 프리티, 45008, 898230 파일:OnseTelecom-USIM.jpg|세종텔레콤 스노우맨, 45008, 898230 파일:KT-cjhello-3Gonly.jpg|CJ헬로비전 헬로모바일, 45008, 898230 파일:Mvno-ktmmobile-3G-kt.jpg|케이티엠모바일 Mmobile, 45008, 898230

### 중국

중국의 [차이나텔레콤](https://ko.wikipedia.org/wiki/차이나텔레콤 "wikilink")이 [CDMA](https://ko.wikipedia.org/wiki/CDMA "wikilink")에 SIM 카드가 들어간 단말기를 선보이고 있다. GSM에는 모두 쓰이고 있다.

### 일본

일본의 PDC 역시 SIM을 표준화하였으나, 상업적으로 구현되지 않았다. 2001년 10월 NTT 도코모가 '포마(FOMA) 카드'란 브랜드로 USIM을 도입하였다.

## 같이 보기

  - [스마트카드](../Page/스마트카드.md "wikilink")
  - [W-SIM](https://ko.wikipedia.org/wiki/W-SIM "wikilink")
  - [R-UIM](https://ko.wikipedia.org/wiki/R-UIM "wikilink")
  - [ISIM](https://ko.wikipedia.org/wiki/ISIM "wikilink")
  - [듀얼 SIM](https://ko.wikipedia.org/wiki/듀얼_SIM "wikilink")

## 각주

<references/>

## 외부 링크

  - [GSM 11.11](https://web.archive.org/web/20130823232049/http://www.3gpp.org/ftp/specs/html-info/1111.htm) - Specification of the Subscriber Identity Module - Mobile Equipment (SIM - ME) interface.
  - [GSM 11.14](https://web.archive.org/web/20130823234427/http://www.3gpp.org/ftp/specs/html-info/1114.htm) - Specification of the SIM Application Toolkit for the Subscriber Identity Module - Mobile Equipment (SIM - ME) interface
  - [ITU-T E.118](http://www.itu.int/rec/T-REC-E.118-200605-I/en) - The International Telecommunication Charge Card. 2006 ITU-T.

[분류:미국의 발명품](https://ko.wikipedia.org/wiki/분류:미국의_발명품 "wikilink") [분류:암호 하드웨어](https://ko.wikipedia.org/wiki/분류:암호_하드웨어 "wikilink") [분류:스마트카드](https://ko.wikipedia.org/wiki/분류:스마트카드 "wikilink") [분류:컴퓨터 접근 제어](https://ko.wikipedia.org/wiki/분류:컴퓨터_접근_제어 "wikilink")

1.
2.
3.
4.
5.  [2005년 3월 삼성에서 나온 SCH-W120가 대한민국에서 SIM 카드가 도입된 최초의 단말기이다.](http://www.areaz.net/viewer/2314919)
6.
7.  즉, USIM의 고유 번호인 [IMSI](https://ko.wikipedia.org/wiki/:en:International_mobile_subscriber_identity "wikilink"), [ICCID만으로](https://ko.wikipedia.org/wiki/:en:Subscriber_identity_module#ICCID "wikilink") 사용자를 식별할 수 있다.
8.  즉, 단말기의 고유 번호([IMEI](https://ko.wikipedia.org/wiki/:en:International_Mobile_Station_Equipment_Identity "wikilink"))를 통신사가 통제하고 있다는 것이다. 예를 들어 일반 휴대전화, 스마트폰, 태블릿·패드, 라우터·모뎀용 요금제가 각각 구분되어 있는 것도 이에 기반한다.
9.  이동통신사업자가 유통하는 단말기를 구입할 시 가입자는 단말기 대금을 연 5.9% 이율로 할부 구매할 수 있다. 또한 [이동통신단말장치 유통구조 개선에 관한 법률의](../Page/이동통신단말장치_유통구조_개선에_관한_법률.md "wikilink") 발효 이후, 이동통신사업자가 유통하는 단말기를 구입할 시 가입자는 "공시 지원금"과 "요금 할인"(일명 '선택약정') 중 하나를 선택할 수 있다. (반면, 이동통신사업자를 통해 구입하지 않은 단말기는 "요금 할인"만을 선택할 수 있다.)
10. 본인 소유 단말기로 가입하여 USIM단독 개통을 하는 경우 등
11. 즉, 사용자의 구분이 되는 전화번호를 복제한 자가 아닌, 이와는 전혀 상관없는 단말기를 복제한 자를 처벌하는 것이다.
12.
13.
14.
15.
16. 예를 들어, KT가 유통한 [삼성 갤럭시 A7](https://ko.wikipedia.org/wiki/삼성_갤럭시_A7 "wikilink")(SM-A700**K**)에 SK텔레콤 가입자의 USIM을 끼우면 '자급제 단말기'로 인식하는 것이 아니라, KT가 유통한 단말기인 "(KT)SM-A700**K**"로 정확히 인식한다.
17.
18.
19.
20.
21.
22.
23. 이동통신사업자 3사와 방송통신위원회가 공시지원금에 대한 위약금 산정 방식을 소비자에게 대단히 불리하게 수정하면서 이에 대한 보상책으로 USIM 카드 가격을 소폭 인하하였다.
24.
25. 4400원이 아니다.
26.
27.
28.
29.
30. 이 데이터셰어링은 월 3,300원짜리 부가서비스를 말하며 "3G 데이터 함께쓰기"와 "LTE 데이터 함께쓰기"에는 해당하지 않는다.
31.
32. 8,800원에서 5,500원으로 인하되었다.
33.
34.
35.
36. 예를 들어, KT의 ②LTE 겸용 USIM을 이용하면 3G WCDMA 요금제를 사용할 수 없다고 생각하여 ①WCDMA 전용 USIM을 구입해야만 3G WCDMA 요금제를 사용할 수 있을 것이라 생각하는 가입자가 있는데, 해당 USIM은 WCDMA·LTE 겸용이므로 LTE 요금제뿐만 아니라 3G WCDMA 요금제를 사용하는 데 아무 문제가 없다.
37.