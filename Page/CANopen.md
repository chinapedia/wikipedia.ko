> This article is converted from Wikipedia: [CANopen](https://ko.wikipedia.org/wiki/CANopen).


**CANopen**은 [자동화](../Page/자동화.md "wikilink") [임베디드 시스템을](../Page/임베디드_시스템.md "wikilink") 위한 [통신 프로토콜이며](../Page/통신_프로토콜.md "wikilink") 장치 프로파일 명세이다. [OSI 모델의](https://ko.wikipedia.org/wiki/OSI_모델 "wikilink") 측면에서 보면, CANopen은 [네트워크 계층과](../Page/네트워크_계층.md "wikilink") 그 상위 계층을 구현한다. CANopen 표준은 장치주소 명세, 몇 가지 통신 프로토콜들과 장치 프로파일에 정의된 [응용 계층으로](../Page/응용_계층.md "wikilink") 구성된다. 통신 프로토콜은 네트워크 관리와 장치 모니터링을 지원하며, 메시지 분할과 병합을 위한 [전송 계층을](../Page/전송_계층.md "wikilink") 포함한 노드 사이의 통신을 가능하게 한다. 데이터 링크 계층과 물리 계층을 위한 하위 계층으로는 보통 [CAN 버스를](../Page/CAN_버스.md "wikilink") 사용한다. 하지만, 하위 계층으로 [Ethernet Powerlink나](https://ko.wikipedia.org/wiki/:en:Ethernet_Powerlink "wikilink") [EtherCAT](https://ko.wikipedia.org/wiki/EtherCAT "wikilink")을 사용할 수도 있다.

기본 CANopen 장치와 통신 프로파일들은 [CAN in Automation에서](https://ko.wikipedia.org/wiki/:en:CAN_in_Automation "wikilink") 발표된 CiA 301 명세서에 기술되어 있다. 좀 더 특화된 장치들을 위한 프로파일들은 CAN in Automation에서 발표된 다른 표준들에 기술되어 있으며, 기본 프로파일을 공통 하부구조로 사용한다. 예로 입출력 모듈을 위한 명세는 CiA 401에 모션 제어를 위한 명세는 CiA 402에서 찾을 수 있다.

## 장치 모델

CANopen 장치는 제어 소프트웨어를 구현할 때 다음과 같은 표준 속성을 포함해야만 한다.

  - **통신 유닛**은 네트워크 상의 다른 노드들과 메시지를 교환하기 위한 프로토콜들을 구현한다.
  - 장치를 시작하거나 재시작할 때 [유한 상태 기계에](../Page/유한_상태_기계.md "wikilink") 의해 현재의 상태를 관리한다. CANopen 장치는 Initialization, Pre-operational, Operational과 Stopped 상태를 구현해야만 한다. 네트워크 관리 (NMT) 메시지를 장치에 전송하여 이러한 상태를 변경할 수 있다.
  - **object dictionary**는 장치가 지원하는 변수들의 집합이다. 16비트 인덱스 번호와 8비트의 서브인덱스 번호로 각각의 변수를 참조할 수 있다. 변수는 장치의 설정을 읽거나 변경하기 위해 사용하거나, 센서의 값을 읽기 위해 사용한다.
  - 장치를 operational 상태로 설정하면 장치의 응용계층에서 미리 설정된 object dictionary 변수들을 주기적으로 또는 특정 이벤트에 의해 전송할 수 있다.

### Object dictionary

Object dictionary (OBD)는 장치 설정과 데이터 통신을 위해 반드시 필요하다. OBD의 각 변수들은 다음과 같이 정의한다:

  - **Index**, 변수의 참조를 위한 16비트 주소
  - **Object name** (Object 타입/크기), 단순 변수인지 배열인지 등을 표현
  - **Name**, 변수 이름
  - **Type**, 변수의 데이터 타입
  - **Attribute**, 읽기만 가능한지, 쓰기만 가능한지, 읽기 쓰기 모두 가능한지 등을 표현
  - **Mandatory/Optional** (M/O), 반드시 정의해야만 하는 변수(M)인지, 개발자가 선택적으로 정의할 수 있는 변수(O) 인지를 표현

기본 장치 프로파일 CiA 301에는 인덱스 범위 0x1000-0x1FFF까지의 영역을 장치 통신 파라미터로 사용한다. 다음은 앞 부분의 몇가지 변수들을 보여준다:

| Index  | Object name | Name                     | Type       | Attribute | M/O |
| ------ | ----------- | ------------------------ | ---------- | --------- | --- |
| 0x1000 | VAR         | device type              | UNSIGNED32 | ro        | M   |
| 0x1001 | VAR         | error register           | UNSIGNED8  | ro        | M   |
| ...    |             |                          |            |           |     |
| 0x1008 | VAR         | manufacturer device name | Vis-String | const     | O   |
| ...    |             |                          |            |           |     |

## 통신

### 통신 오브젝트(Communication objects)

CANopen의 데이터 계층인 [CAN 버스는](../Page/CAN_버스.md "wikilink") 11비트 아이디, 원격전송요청(remote transmission request RTR)비트와 0에서 8 바이트 가변길이 데이터로 이루어진 짧은 메시지를 전송할 수 있다. CANopen 표준에서는 11비트 CAN 프레임 아이디를 4비트의 기능 코드와 7비트의 CANopen 노드 아이디로 나누어 사용한다. 그래서 CANopen 네트워크에서 최대 지원 가능한 노드의 수는 127개이다 (아이디 0은 브로드 캐스트 용도로 사용한다).

CAN 버스 표준의 확장인 CAN 2.0B에서는 29비트의 확장 프레임 아이디를 제공하지만, 현실적으로 이 확장 버전을 필요로 하는 CANopen 네트워크는 매우 드물다. CANopen에서는 11비트의 CAN 프레임 아이디를 communication object identifier (COB-ID)라고 부른다.

CANopen 프레임의 구성:

|        | CAN-ID  | RTR   | Data length | Data      |
| ------ | ------- | ----- | ----------- | --------- |
| Length | 11 bits | 1 bit | 4 bits      | 0-8 bytes |

CAN-ID:

|        | Function code | Node ID |
| ------ | ------------- | ------- |
| Length | 4 bits        | 7 bits  |

전송중 충돌이 발생했을 경우, CAN 버스에서는 낮은 아이디를 갖는 프레임이 버스 arbitration에 의해 네트워크를 이용할 수 있는 우선권이 있다. 그러므로 더 낮은 4비트 기능 코드를 갖는 프레임이 우선적으로 전송된다.

다음은 CANopen에 정의된 기능 코드들이다:

| 기능                       | 기능 코드        |
| ------------------------ | ------------ |
| NMT node control         | 0000b        |
| SYNC                     | 0001b        |
| Emergency                | 0001b        |
| Timestamp                | 0010b        |
| PDO                      | 0011b\~1010b |
| SDO                      | 1011b\~1100b |
| NMT node monitoring, LSS | 1110b        |

#### 미리 정의된 COB-IDs

CANopen에서는 아래와 같은 메시지 아이디들을 지원한다.

<table>
<thead>
<tr class="header">
<th><p>Communication object</p></th>
<th><p>COB-ID(s) hex</p></th>
<th><p>Slave nodes</p></th>
<th><p>Specification</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>NMT node control</p></td>
<td><p>000</p></td>
<td><p>Receive only</p></td>
<td><p>CiA 301</p></td>
</tr>
<tr class="even">
<td><p>Global failsafe command</p></td>
<td><p>001</p></td>
<td><p>?</p></td>
<td><p>CiA 304</p></td>
</tr>
<tr class="odd">
<td><p>Sync</p></td>
<td><p>080</p></td>
<td><p>Receive only</p></td>
<td><p>CiA 301</p></td>
</tr>
<tr class="even">
<td><p>Emergency</p></td>
<td><p>080 + NodeID</p></td>
<td><p>Transmit</p></td>
<td><p>CiA 301</p></td>
</tr>
<tr class="odd">
<td><p>TimeStamp</p></td>
<td><p>100</p></td>
<td><p>Receive only</p></td>
<td><p>CiA 301</p></td>
</tr>
<tr class="even">
<td><p>PDO</p></td>
<td><p>180 + NodeID<br />
200 + NodeID<br />
280 + NodeID<br />
300 + NodeID<br />
380 + NodeID<br />
400 + NodeID<br />
480 + NodeID<br />
500 + NodeID</p></td>
<td><p>1. Transmit PDO<br />
1. Receive PDO<br />
2. Transmit PDO<br />
2. Receive PDO<br />
3. Transmit PDO<br />
3. Receive PDO<br />
4. Transmit PDO<br />
4. Receive PDO</p></td>
<td><p>CiA 301</p></td>
</tr>
<tr class="odd">
<td><p>SDO</p></td>
<td><p>580 + NodeID<br />
600 + NodeID</p></td>
<td><p>Transmit<br />
Receive</p></td>
<td><p>CiA 301</p></td>
</tr>
<tr class="even">
<td><p>NMT node monitoring (node guarding/heartbeat)</p></td>
<td><p>700 + NodeID</p></td>
<td><p>Transmit</p></td>
<td><p>CiA 301</p></td>
</tr>
<tr class="odd">
<td><p>LSS</p></td>
<td><p>7E4<br />
7E5</p></td>
<td><p>Transmit<br />
Receive</p></td>
<td><p>CiA 305</p></td>
</tr>
</tbody>
</table>

### 통신 모델

CANopen 노드는 다음과 같은 종류의 통신 모델을 이용한다.

  - master/slave 모델에서 네트워크상의 한 노드는 다른 노드들에게 데이터를 보내거나 요청하는 master 역할을 한다. NMT 프로토콜은 master/slave 통신 모델의 예이다.
  - SDO 프로토콜은 client/server 모델에 기초하여 동작한다. SDO client는 SDO server상의 OBD 변수를 읽어오거나 변경할 수 있다.
  - Heartbeat이나 노드 guarding 프로토콜은 producer/consumer모델을 이용한다. Push 모델에서 producer는 특별한 요청이 없어도 consumer에게 데이터를 전송하며, Pull 모델에서 consumer는 producer에게 데이터를 요청해야만 한다.

### 프로토콜

#### Network management (NMT) 프로토콜

NMT 프로토콜은 장치의 상태를 변경하거나 장치가 부팅하고 정상적으로 동작하는지를 감지하기 위한 용도로 쓸 수 있다.

NMT master 노드는 장치의 상태를 변경하기 위해 **NMT 노드 제어 프로토콜**을 이용한다. 이 프로토콜의 COB-ID는 0이며, 네트워크 상의 모든 노드는 이 메시지를 수신하여 처리해야만 한다. 데이터는 2바이트이며, 첫번째 바이트는 변경할 상태를 나타내며, 두번째 바이트는 수신 대상 노드를 가리킨다. 두 번째 바이트가 0일 경우 네트워크 상의 모든 노드들은 첫번째 바이트에 기록된 상태로 전이해야만 한다.

| COB-ID | Data Byte 0                | Data Byte 1    |
| ------ | -------------------------- | -------------- |
| 0x000  | Requested NMT command code | Addressed node |

| NMT command code | Meaning                     |
| ---------------- | --------------------------- |
| 0x01             | Go to 'operational'         |
| 0x02             | Go to 'stopped'             |
| 0x80             | Go to 'pre-operational'     |
| 0x81             | Go to 'reset node'          |
| 0x82             | Go to 'reset communication' |

**Heartbeat 프로토콜**은 master에서 네트워크 상의 노드들이 동작하고 있는지를 확인하기 위해 사용한다. Heartbeat producer는 주기적으로 1 바이트 데이터를 포함한 메시지를 전송하여 자신의 상태를 master에게 알린다. COB-ID는 0x700 + 노드 아이디이다. 1 바이트 데이터에는 노드의 상태 코드(NMT state code)가 담겨져 있다. Heartbeat consumer는 이 메시지를 주기적으로 수신하여야 한다. 만일 OBD에 정의된 특정 시간 내에 heartbeat를 수신하지 못하였을 경우에는 해당 노드를 재시작(reset) 하거나 에러 메시지를 띄우는 방식으로 이 상황에 반응할 수 있다. 프레임 형식은 다음과 같다:

| COB-ID          | Data Byte 0 |
| --------------- | ----------- |
| 0x700 + node ID | State       |

| NMT state code | Represented state      |
| -------------- | ---------------------- |
| 0x00           | Boot up (Initialising) |
| 0x04           | Stopped                |
| 0x05           | Operational            |
| 0x7f           | Pre-operational        |

CANopen 장치는 부팅 시에 Initializing 상태에서 Pre-operational 상태로 이동하여 대기하여야 한다. Initializing 상태에서 Pre-operational 상태로 이동할 때 한 번만 1 바이트 데이터에 0을 포함한 heartbeat 메시지를 전송하며, 이것을 **bootup 프로토콜**이라고 한다. 이후에는 0이 아닌 현재의 노드 상태를 포함한 heartbeat 메시지를 주기적으로 전송한다.

노드 guarding이라고 하는 요청/응답 방식 (pull 모델)으로도 slave를 모니터링할 수 있다.

#### Service Data Object (SDO) 프로토콜

CAN 버스에 연결된 노드의 OBD에서 값을 읽거나 쓰기 위해서 SDO 프로토콜을 사용할 수 있다. SDO server는 SDO client의 요청에 의해 자신의 OBD에 있는 변수를 보내주거나 변경할 수 있다. SDO 프로토콜을 설명하는 CANopen 문서를 보면, upload와 download라는 용어를 볼 수 있다. 이는 SDO server의 관점에서 기술하는 용어이다. 즉 SDO server의 변수에 값을 읽어 SDO client에게 보내주는 동작(read)은 upload라고 하고, 값을 쓰는 행위(write)는 download라고 한다.

OBD 변수는 CAN 프레임에서 지원하는 최대 8바이트 보다 더 큰 크기를 정의할 수 있다. 따라서, SDO 프로토콜은 8바이트보다 긴 메시지를 전송하기 위한 segmentation과 desegmentation을 지원한다. CANopen 명세에서는 이를 지원하기 위한 두 가지 다른 프로토콜을 정의한다. 하나는 SDO download/upload 이고 다른 하나는 SDO Block download/upload이다. SDO 블럭 전송은 더 최근에 표준화된 프로토콜이며, 전송시 약간의 크기를 줄일 수 있고 더 큰 데이터를 전송할 수 있다.

SDO 통신을 위한 COB-ID들을 OBD에 정의하여 사용할 수 있으나, 대부분의 경우 미리 정의된 COB-ID를 사용한다. SDO client에서 server로 보내는 요청 메시지의 경우 0x600 + 노드 아이디를 사용하고 SDO server에서 client로 보내는 응답 메시지의 경우 0x580 + 노드 아이디를 사용한다. SDO 프로토콜은 부팅후 노드가 Pre-operational 상태에 있을 때 사용할 수 있다. 주로 노드의 고유 값들을 읽어오거나 설정을 변경하기 위해 사용한다.

#### Process Data Object (PDO) 프로토콜

센서에서 읽어들인 값들을 실시간으로 전송하기 위해서 PDO 프로토콜을 사용한다. PDO 메시지들을 전송하기에 앞서 매핑 과정이 필요하다. 한번에 최대 8 바이트를 PDO 메시지에 담아 전송할 수 있으므로 예를 들면 4바이트 OBD 데이터 2개 또는 4바이트 OBD 데이터 한 개와 2바이트 OBD 데이터 2개를 한 프레임에 담아 전송할 수 있다. 물론 필요하다면 1바이트의 데이터만을 전송할 수도 있다. 어떤 노드는 자신의 PDO 매핑을 미리 가지고 있기도 하며, master는 slave들의 매핑을 Pre-operational 상태에서 설정할 수 있다. 매핑을 마쳤다면, 노드를 operational 상태로 설정하여 PDO 메시지의 전송을 시작한다.

PDO 메시지는 transmit PDO와 receive PDO (TPDO와 RPDO)로 나눌 수 있다. TPDO를 전송하는 노드는 누가 발신자인지를 COB-ID에 기록하지만 수신자는 지정하지 않으며, 이를 수신할 지 말지는 수신 노드들의 설정에 의해 결정된다. RPDO를 전송하는 노드는 COB-ID에 특정 노드를 수신자로 지정하여 메시지를 송신한다. 기본적으로 한 노드는 4개씩의 TPDO와 RPDO를 사용할 수 있지만, 특정 목적에 따라 더 많은 PDO들을 정의하여 사용할 수 있다.

PDO 메시지는 동기적으로 또는 비동기적으로 전달할 수 있다. 동기적 PDO에서는 노드가 master로부터 SYNC 메시지를 수신하였을 때 PDO 메시지를 전달한다. 반면 비동기적 PDO 에서는 내부 또는 외부 트리거에 의해 메시지를 전송한다. 내부 트리거의 예는 센서에서 데이터를 감지할 때마다 PDO를 전달하는 경우이며, 외부 트리거의 예는 RTR 플래그를 설정한 빈 TPDO 메시지를 전송하여 응답형식으로 받는 경우이다.

#### Synchronization Object (SYNC) 프로토콜

SYNC producer는 SYNC consumer에서 동기화 신호를 전달한다. SYNC 메시지를 수신한 consumer는 수신시점에 동기적 작업을 시작한다. SYNC 메시지의 COB-ID는 0x080이며, 데이터 없이 COB-ID만 전달한다. OBD 0x1005에서 SYNC COB-ID를 변경할 수 있다.

## 각주

1.  CiA 301 CANopen application layer specification, [CAN in Automation](http://www.can-cia.org)에서 무료로 다운로드 가능

2.  CiA 401 CANopen device profile specification for generic I/O modules, [CAN in Automation](http://www.can-cia.org)에서 무료로 다운로드 가능

3.  CiA 402 CANopen device profile for motion controllers and drives (same as IEC 61800-7-201/301)

[분류:컴퓨터 네트워킹](https://ko.wikipedia.org/wiki/분류:컴퓨터_네트워킹 "wikilink") [분류:네트워크 프로토콜](https://ko.wikipedia.org/wiki/분류:네트워크_프로토콜 "wikilink") [분류:통신 표준](https://ko.wikipedia.org/wiki/분류:통신_표준 "wikilink")