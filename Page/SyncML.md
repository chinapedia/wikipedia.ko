> This article is converted from Wikipedia: [SyncML](https://ko.wikipedia.org/wiki/SyncML).


**SyncML** (**Synchronization Markup Language**)은 플랫폼 독립적인 데이터 동기화 표준이다. 즉, MS 윈도우를 사용하는 PC, 리눅스를 사용하는 PC, Palm PDA, 휴대전화, 아이팟, 아이폰 등의 어떤 기기와도 자유롭게 데이터를 동기화할 수 있다. **SyncML**은 [XML](../Page/XML.md "wikilink")을 기반으로 한다.

## 내부 동작

리프레시(refresh) 동기화 시작을 위해 Alert 명령을 포함한 메시지의 예:

``` xml
<?xml version="1.0"?>
<!DOCTYPE SyncML PUBLIC "-//SYNCML//DTD SyncML 1.2//EN" "http://www.openmobilealliance.org/tech/DTD/OMA-TS-SyncML_RepPro_DTD-V1_2.dtd">
<SyncML ns="SYNCML:SYNCML1.2">
 <SyncHdr>
  <VerDTD>1.1</VerDTD>
  <VerProto>SyncML/1.1</VerProto>
  <SessionID>1</SessionID>
  <MsgID>1</MsgID>
  <Target><LocURI>PC Suite</LocURI></Target>
  <Source><LocURI>IMEI:3405623856456</LocURI></Source>
  <Meta><MaxMsgSize ns="syncml:metinf">8000</MaxMsgSize></Meta>
 </SyncHdr>

 <SyncBody>
  <Alert>
   <CmdID>1</CmdID>
   <Data>203</Data>   <!-- 203 = mobile signals a refresh from it to computer -->
   <Item>
    <Target><LocURI>Events</LocURI></Target>
    <Source><LocURI>/telecom/cal.vcs</LocURI></Source>
    <Meta><Anchor ns="syncml:metinf"><Last>42</Last><Next>42</Next></Anchor></Meta>
   </Item>
  </Alert>

  <Final/>
 </SyncBody>
</SyncML>
```

컴퓨터로부터 온 응답:

``` xml
<?xml version="1.0"?>
<!DOCTYPE SyncML PUBLIC "-//SYNCML//DTD SyncML 1.2//EN" "http://www.openmobilealliance.org/tech/DTD/OMA-TS-SyncML_RepPro_DTD-V1_2.dtd">
<SyncML>
 <SyncHdr>
  <VerDTD>1.1</VerDTD>
  <VerProto>SyncML/1.1</VerProto>
  <SessionID>1</SessionID>
  <MsgID>1</MsgID>
  <Target><LocURI>IMEI:3405623856456</LocURI></Target>
  <Source><LocURI>PC Suite</LocURI></Source>
 </SyncHdr>

 <SyncBody>

  <!-- accept the header of the last message from the client -->
  <Status>
   <CmdID>1</CmdID>
   <MsgRef>1</MsgRef>
   <CmdRef>0</CmdRef>   <!-- 0 = header of the message -->
   <Cmd>SyncHdr</Cmd>
   <TargetRef>PC Suite</TargetRef>
   <SourceRef>IMEI:3405623856456</SourceRef>
   <Data>200</Data> <!-- 200 = ok, accepted -->
  </Status>

  <!-- accept the request of the mobile for a sync -->
  <Status>
   <CmdID>2</CmdID> <!-- this is command #2 -->
   <MsgRef>1</MsgRef>
   <CmdRef>1</CmdRef>   <!-- it respond to command msg=1,cmd=1 -->
   <Cmd>Alert</Cmd>
   <TargetRef>Events</TargetRef>
   <SourceRef>/telecom/cal.vcs</SourceRef>
   <Meta><Anchor ns="syncml:metinf"><Next>0</Next><Last>0</Last></Anchor></Meta>
   <Data>200</Data> <!-- 200 = ok, accepted -->
  </Status>

  <Final/>
 </SyncBody>
</SyncML>
```

## 외부 링크

  - [OMA Data Synchronization Working Group](http://www.openmobilealliance.org/Technical/DS.aspx)
  - [SyncML - Data Synchronization and Device Management](http://www.openmobilealliance.org/syncml/)

[분류:XML 기반 표준](https://ko.wikipedia.org/wiki/분류:XML_기반_표준 "wikilink") [분류:오픈 포맷](https://ko.wikipedia.org/wiki/분류:오픈_포맷 "wikilink") [분류:데이터 동기화](https://ko.wikipedia.org/wiki/분류:데이터_동기화 "wikilink") [분류:컴퓨터 표준](https://ko.wikipedia.org/wiki/분류:컴퓨터_표준 "wikilink")