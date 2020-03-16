> This article is converted from Wikipedia: [TVM](https://ko.wikipedia.org/wiki/TVM).


[right](https://ko.wikipedia.org/wiki/파일:RepereBoard.svg "wikilink") **TVM**(, 궤도-열차간 전송)은 프랑스 및 인접한 유럽 국가, 대한민국에서 사용하는 고속 철도용 차상 신호 시스템이다. 프랑스 국내 고속선, [유로터널](https://ko.wikipedia.org/wiki/유로터널 "wikilink"), 벨기에 [HSL 1](https://ko.wikipedia.org/wiki/HSL_1 "wikilink"), 영국 [하이 스피드 1](https://ko.wikipedia.org/wiki/하이_스피드_1 "wikilink") 및 대한민국 [경부고속선](../Page/경부고속선.md "wikilink"), [호남고속선](https://ko.wikipedia.org/wiki/호남고속선 "wikilink"), [수서평택고속선](https://ko.wikipedia.org/wiki/수서평택고속선 "wikilink")에서 사용하고 있다. 프랑스 CSEE에서 개발하였다.

## 개요

TVM 시스템은 프랑스 CSEE(현 [안살도 STS](../Page/안살도_STS.md "wikilink"))에서 개발하였다. 신호 시스템 자체는 고속을 지원하지만, 릴레이와 같은 구형 부품이 일부 사용된다. 시스템 상으로 봐서는 [ATC의](../Page/자동_열차_제어_장치.md "wikilink") 일종에 속한다.

고속선용 신호는 TVM300과 TVM430 두 종류가 있다. TVM430 시스템은 [LGV 노르](https://ko.wikipedia.org/wiki/LGV_노르 "wikilink") 이후 개통된 프랑스 고속선, [채널 터널](../Page/채널_터널.md "wikilink"), 벨기에 [HSL 1](https://ko.wikipedia.org/wiki/HSL_1 "wikilink"), 영국 [하이 스피드 1](https://ko.wikipedia.org/wiki/하이_스피드_1 "wikilink"), 대한민국 [경부고속선](../Page/경부고속선.md "wikilink"), [호남고속선](https://ko.wikipedia.org/wiki/호남고속선 "wikilink"), [수서평택고속선](https://ko.wikipedia.org/wiki/수서평택고속선 "wikilink")에 설치되어 있으며 TVM300보다 더 많은 정보를 제공한다. 제동을 해방시키지 않으면서 안전하게 속도를 줄일 수 있도록 연속적인 제동 곡선을 그릴 수 있다. TVM430은 기능이 모듈화되어 있는 TVM400-TVM440(추가적 자동 열차 제어), TVM450(무인 운전) 계열에 속해 있다.

각각 폐색은 1500m 단위이며, 폐색 경계마다 표지가 설치되어 있다. 계기판에는 현재 폐색에서 낼 수 있는 최고 속도와 차후 목표 속도가 표시된다. 현재 허용되는 최고 속도는 앞 열차와의 거리, 전철기, 속도 제한, 열차 최고 속도, 고속선 종료까지 거리 등 정보로 결정된다. 열차의 제동 거리는 한 폐색 이상이므로 제동은 여러 폐색으로 나눠서 진행된다.

다른 열차가 점유하고 있는 폐색에도 진입할 수는 있으나, 이 경우 속도가 최대 시속 30km로 제한되며 시속 35km를 넘기면 비상 제동이 체결된다. Np 표시가 있는 폐색에 진입하려면 관제실의 허가를 받아야 한다. 관제실의 허가가 떨어지면 폐색 표시기가 점등되며 이때 열차가 진입할 수 있다.

## 작동 방식

TVM이 주고받는 정보는 연속 정보와 불연속 정보이다. 불연속 정보는 궤도상에 설치된 지상자를 통해서, 연속 정보는 궤도 회로를 통해서 전송된다. 연속 정보와 불연속 정보는 개별적인 안테나를 통해 모이고, 차상 컴퓨터로 신호를 해석한다. 조종석에서 볼 수 있는 정보는 현재 속도, 대상 속도, 진행 여부 등이다.

TVM 시스템은 차상자와 지상자로 이루어진다. 두 장치 모두 [모토롤라 68020](https://ko.wikipedia.org/wiki/모토롤라_68020 "wikilink") 프로세서로 가동되며, [에이다 프로그래밍 언어를](https://ko.wikipedia.org/wiki/에이다_프로그래밍_언어 "wikilink") 사용한다.

불연속 정보 지상자는 궤도변 상자에 있으며, 약 15km(10여개 폐색)를 제어한다. 모든 지상자는 중앙 교통 제어 센터로 연결된다. 연속 정보는 궤도상에 교류 전류로 전달된다.

TVM430에서 사용하는 반송 주파수는 4종류가 있으며, 고속선의 복선에서 서로 다른 두 쌍으로 사용된다. 한 쪽 선로에서 1700/2300Hz를 사용하고, 다른 쪽 선로에서 2000/2600Hz를 사용한다. 임의로 조합 가능한 27개의 음성 주파수를 이 대역으로 변조하여 보낸다. 과거 TVM300은 18개의 주파수를 사용하였고, 조합이 불가능하였다. 각각 폐색은 지상자와 통신하며, 궤도 회로가 끊기면 폐색이 점유된 것으로 간주한다.

궤도 신호를 감지하기 위해서 고속선을 운행하는 열차의 앞부분 아래쪽에 달려 있는 안테나를 사용한다. 안테나는 전방 축의 1m 앞에 달려 있다. 궤도와 전방 축 사이에 흐르는 교류 신호와 자기적으로 결합되면서 신호를 감지한다. 열차의 맨 앞과 맨 뒤에 안테나가 2개씩 있으며, 진행 방향의 안테나 2개만 활성화된다. 궤도 회로에서 온 신호는 두 개의 DSP가 처리한다.

해석된 신호는 27비트 길이이며, 각각 27개 중 하나씩의 주파수에서 온 신호를 담당한다. 신호에는 다음과 같은 정보가 들어 있다.

  - **속도 코드**는 현재 폐색의 안전 최고 속도, 현재 폐색 끝에서의 목표 속도, 다음 폐색 끝에서의 목표 속도를 포함한다.(Vc,Ve,Va) 대개 이 속도 코드는 300, 270, 230, 170, 80, 0km/h를 가리키며, 전형적인 가감속 곡선을 따르고 있다.
  - 각각 폐색에서의 평균 **구배 정보** 또한 속도 계산에 사용된다.
  - 변할 수도 있는 **폐색 길이** 역시 속도 계산에 사용된다. 평탄한 고속선에서는 폐색 길이가 1500m까지 길어질 수 있지만, [채널 터널의](../Page/채널_터널.md "wikilink") 끝에서는 150m까지 짧아진다.
  - **네트워크 코드**는 열차의 최고 속도를 포함한다. 대개의 고속선에서는 시속 300km/h까지 낼 수 있으며, 채널 터널에서는 160km/h로 제한된다. 채널 터널을 다니는 유로스타 열차는 이 정보가 필요하다.
  - 전체 27비트 워드의 오류를 검사하는 **오류 검증 코드**로 끝난다. 오류 검증 코드를 통해서 신호가 잘못 계산되었는가 여부 뿐만 아니라 오류를 자체적으로 수정할 수도 있다. 6비트 CRC 코드이다.

이 정보는 차상자로 전송되어 열차의 속도를 계산한다. 과거 TVM 시스템에서는 대상 속도가 폐색 끝에서만 갱신되어 급가속과 급감속이 필요하였다. 이후 폐색 길이와 구배 정보가 추가되어 차상자 내에서 더 매끄러운 속도 곡선을 계산할 수 있게 되었다.

속도 제어 이외의 열차 제어 기능도 있다. 궤도 회로를 통해 전송된 신호는 열차 하부의 센서를 통해 감지된다. 다음 추가 정보를 사용할 수 있다.

  - 고속선 진출입
  - TVM 시스템 활성/비활성화
  - 터널 진입 전 공조장치 폐쇄
  - [팬토그래프](https://ko.wikipedia.org/wiki/팬토그래프 "wikilink") 상승/하강
  - [절연 구간](../Page/절연_구간.md "wikilink") 안내

전체 열차 운행 상황은 블랙 박스에 기록된다. TVM430 장착 차량은 디지털 기록 시스템을 사용한다. 제동, 가속, 팬토그래프 조작 등 운전자의 모든 동작 외 각종 신호기 상황은 자기 테이프에 기록되어 나중에 분석할 수 있다.

## 차상 정보

TVM이 장착되어 있는 열차의 조종석에는 두 줄에서 세 줄의 사각형 표시등이 있다. 이 표시등을 통해서 색깔이 있는 배경 위에 제한 속도를 표시한다. 최고 속도는 녹색 배경에 검은색 숫자로 표시되며, 저속 예고 신호는 검은 배경에 흰색 숫자로 표시되고, 완전 정지는 붉은색 배경에 "000"으로 표시된다. TVM 속도 표시기 아래에는 열차 속도계가 있으며, 현재 열차의 속도를 표시한다. 열차의 현재 속도에 따라서 제동이 체결되는 속도가 달라진다. 예를 들어 시속 300km으로 주행할 때, 시속 320km를 넘어가면 비상 제동이 체결된다. 속도가 더 낮아지면 둘 사이의 간격이 더 넓어진다.

고속선에서의 차상 신호는 안전과 직결되므로, 신호가 한 번 표시되면 컴퓨터에 현재 신호가 어디에 표시되었는지 피드백을 보낸다. 차상 신호 표시기에 이상이 생기면 열차를 정지시킨다. 열차를 급격하게 제어하는 것을 방지하기 위해서 폐색에 들어가기 전 미리 제한 속도를 알려 준다. 다음 폐색에 들어갈 때 속도를 낮춰야 한다면 속도 표시기가 깜빡여서 제동을 돕는다.

아래에 나와 있는 표는 TVM 차상 신호기에 나타나는 숫자와 그 의미이다.

| 차상 신호                   |
| ----------------------- |
| 이름                      |
| 현재 속도                   |
| **Rouge** (정지)          |
| Np 표지: 0 km/h           |
| **Zéro**, 다음 신호에서 정지    |
| 이전 신호가 160A: 170 km/h   |
| **080E**, 80km/h 제한     |
| **080A**, 80km/h로 가/감속  |
| **160E**, 160km/h 제한    |
| **160A**, 160km/h로 가/감속 |
| **220E**, 220km/h 제한    |
| **220A**, 220km/h로 가/감속 |
| **270V**                |
| **270VL**, 270km/h 진행   |
| **270A**, 270km/h로 가/감속 |
| **300V**                |
| **300VL**, 300km/h 진행   |

  - 대한민국 [경부고속선](../Page/경부고속선.md "wikilink"), [호남고속선](https://ko.wikipedia.org/wiki/호남고속선 "wikilink")에는 프랑스의 F와 Nf 대신 P와 Np를 사용한다.

## 참고 자료

  - Kichenside, G. 및 Williams, A. (1998) *Two Centuries of Railway Signalling*, Oxford Publishing Co., p. 215-220,
  - Railway Group Standard (1996) *GK/RT0036:Transition Between Lineside Signalling Systems and Other Systems of Train Control*, Issue One, Appendix C: Illustration of application to Eurotunnel Cab Signalling, p. 10-12, London: Safety & Standards Directorate, Railtrack PLC [GK/RT0036](https://web.archive.org/web/20110717112738/http://www.rgsonline.co.uk/Railway_Group_Standards/Control%20Command%20and%20Signalling/Railway%20Group%20Standards/GKRT0036%20Iss%201.pdf), Accessed [15 December](https://ko.wikipedia.org/wiki/15_December "wikilink") 2008

## 외부 링크

  - [LGV signalling](https://web.archive.org/web/20071016190548/http://www.carreweb.fr/stfr/cstgv_en.html)
  - [TVM 차상 신호 정보](https://web.archive.org/web/20080302202330/http://www.carreweb.fr/signalisation_en.html)

[분류:철도 신호](https://ko.wikipedia.org/wiki/분류:철도_신호 "wikilink")