> This article is converted from Wikipedia: [XML-RPC](https://ko.wikipedia.org/wiki/XML-RPC).


**XML-RPC**란, [RPC](https://ko.wikipedia.org/wiki/RPC "wikilink") 프로토콜의 일종으로서, 인코딩 형식에서는 [XML](../Page/XML.md "wikilink")을 채택하고, 전송 방식에서는 [HTTP](../Page/HTTP.md "wikilink") 프로토콜을 사용하고 있다. XML-RPC는 매우 단순한 규약으로서, 작은 데이터 형식이나 명령을 정의하는 정도로만 사용하고 있으며, 사양서도 A4 2매 정도로 꽤나 단순한 편이다. 이건 대다수의 RPC 프로토콜 시스템이 수많은 규격을 규정하고, 실제 사용할 때에도 엄청난 양의 코딩을 요구하는 것과 비교하면 눈에 띄는 특징이라고 할 수 있다.

이 프로토콜은 [1998년](../Page/1998년.md "wikilink") 데이브 위너(Dave Winer)의 UserLand Software Ltd.가 [마이크로소프트](../Page/마이크로소프트.md "wikilink")와 공동으로 개발하였다. 이후에 이 프로토콜에 좀 더 부가적인 기능을 추가한 [SOAP](../Page/SOAP.md "wikilink") 프로토콜이 개발되었으나, 보통 SOAP 보다 단순하고 사용하기 쉬운 XML-RPC를 더욱 많이 사용하고 있다.

이와 비슷한 RPC 계열 프로토콜로는 [JSON-RPC](../Page/JSON-RPC.md "wikilink") 프로토콜이 존재한다.

## 자료형

<table>
<thead>
<tr class="header">
<th><p>이름</p></th>
<th><p>사용 예</p></th>
<th><p>설명</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>array</p></td>
<td><div class="sourceCode" id="cb1"><pre class="sourceCode xml"><code class="sourceCode xml"><span id="cb1-1"><a href="#cb1-1"></a> <span class="kw">&lt;array&gt;</span></span>
<span id="cb1-2"><a href="#cb1-2"></a>   <span class="kw">&lt;data&gt;</span></span>
<span id="cb1-3"><a href="#cb1-3"></a>     <span class="kw">&lt;value&gt;&lt;i4&gt;</span>1404<span class="kw">&lt;/i4&gt;&lt;/value&gt;</span></span>
<span id="cb1-4"><a href="#cb1-4"></a>     <span class="kw">&lt;value&gt;&lt;string&gt;</span>Something here<span class="kw">&lt;/string&gt;&lt;/value&gt;</span></span>
<span id="cb1-5"><a href="#cb1-5"></a>     <span class="kw">&lt;value&gt;&lt;i4&gt;</span>1<span class="kw">&lt;/i4&gt;&lt;/value&gt;</span></span>
<span id="cb1-6"><a href="#cb1-6"></a>   <span class="kw">&lt;/data&gt;</span></span>
<span id="cb1-7"><a href="#cb1-7"></a> <span class="kw">&lt;/array&gt;</span></span></code></pre></div></td>
<td><p>값의 배열. 키는 포함하지 않음.</p></td>
</tr>
<tr class="even">
<td><p>base64</p></td>
<td><p><base64><code>eW91IGNhbid0IHJlYWQgdGhpcyE=</code></base64></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/Base64" title="wikilink">Base64</a>로 인코딩 된 바이너리 데이터</p></td>
</tr>
<tr class="odd">
<td><p>boolean</p></td>
<td><p><boolean><code>1</code></boolean></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/논리식" title="wikilink">논리식</a> (0 또는 1)</p></td>
</tr>
<tr class="even">
<td><p>date/time</p></td>
<td><p><code>&lt;dateTime.iso8601&gt;19980717T14:08:55&lt;/dateTime.iso8601&gt;</code></p></td>
<td><p>날짜와 시간</p></td>
</tr>
<tr class="odd">
<td><p>double</p></td>
<td><p><double><code>-12.53</code></double></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/배정수" title="wikilink">배정밀도</a> <a href="https://ko.wikipedia.org/wiki/부동_소수점" title="wikilink">부동소수점</a></p></td>
</tr>
<tr class="even">
<td><p>integer</p></td>
<td><p><i4><code>42</code></i4></p>
<p>or</p>
<p><int><code>42</code></int></p></td>
<td><p><a href="../Page/정수.md" title="wikilink">정수</a></p></td>
</tr>
<tr class="odd">
<td><p>string</p></td>
<td><p><string><code>Hello world!</code></string></p></td>
<td><p>문자열. <a href="https://ko.wikipedia.org/wiki/Extensible_Markup_Language" title="wikilink">XML</a> 파일의 인코딩 형식에 따름.</p></td>
</tr>
<tr class="even">
<td><p>struct</p></td>
<td><div class="sourceCode" id="cb2"><pre class="sourceCode xml"><code class="sourceCode xml"><span id="cb2-1"><a href="#cb2-1"></a> <span class="kw">&lt;struct&gt;</span></span>
<span id="cb2-2"><a href="#cb2-2"></a>   <span class="kw">&lt;member&gt;</span></span>
<span id="cb2-3"><a href="#cb2-3"></a>     <span class="kw">&lt;name&gt;</span>foo<span class="kw">&lt;/name&gt;</span></span>
<span id="cb2-4"><a href="#cb2-4"></a>     <span class="kw">&lt;value&gt;&lt;i4&gt;</span>1<span class="kw">&lt;/i4&gt;&lt;/value&gt;</span></span>
<span id="cb2-5"><a href="#cb2-5"></a>   <span class="kw">&lt;/member&gt;</span></span>
<span id="cb2-6"><a href="#cb2-6"></a>   <span class="kw">&lt;member&gt;</span></span>
<span id="cb2-7"><a href="#cb2-7"></a>     <span class="kw">&lt;name&gt;</span>bar<span class="kw">&lt;/name&gt;</span></span>
<span id="cb2-8"><a href="#cb2-8"></a>     <span class="kw">&lt;value&gt;&lt;i4&gt;</span>2<span class="kw">&lt;/i4&gt;&lt;/value&gt;</span></span>
<span id="cb2-9"><a href="#cb2-9"></a>   <span class="kw">&lt;/member&gt;</span></span>
<span id="cb2-10"><a href="#cb2-10"></a> <span class="kw">&lt;/struct&gt;</span></span></code></pre></div></td>
<td><p>키 값을 포함한 값의 배열.</p></td>
</tr>
<tr class="odd">
<td><p>nil</p></td>
<td><p><nil/></p></td>
<td><p>NULL 식별용. XML-RPC <a href="https://web.archive.org/web/20070309154227/http://ontosys.com/xml-rpc/extensions.php">확장</a></p></td>
</tr>
</tbody>
</table>

## 사용 예

XML-RPC Call 형식의 예제

``` xml
 <?xml version="1.0"?>
 <methodCall>
   <methodName>examples.getStateName</methodName>
   <params>
     <param>
         <value><i4>40</i4></value>
     </param>
   </params>
 </methodCall>
```

XML-RPC Response 형식의 예제

``` xml
 <?xml version="1.0"?>
 <methodResponse>
   <params>
     <param>
         <value><string>South Dakota</string></value>
     </param>
   </params>
 </methodResponse>
```

XML-RPC Fault 형식의 예제

``` xml
 <?xml version="1.0"?>
 <methodResponse>
   <fault>
     <value>
       <struct>
         <member>
           <name>faultCode</name>
           <value><int>4</int></value>
         </member>
         <member>
           <name>faultString</name>
           <value><string>Too many parameters.</string></value>
         </member>
       </struct>
     </value>
   </fault>
 </methodResponse>
```

## 관련 항목

  - [원격 프로시저 호출](../Page/원격_프로시저_호출.md "wikilink")
  - [JSON-RPC](../Page/JSON-RPC.md "wikilink")
  - [REST](../Page/REST.md "wikilink")
  - [웹 서비스](../Page/웹_서비스.md "wikilink")

## 외부 링크

  - [XML-RPC Homepage](http://www.xmlrpc.com/)
  - [Forum](http://groups.yahoo.com/group/xml-rpc/)
  - [Tutorials](https://web.archive.org/web/20100914031553/http://www.xml.com/pub/rg/XML_RPC_Tutorials)
  - [Technology Reports](http://xml.coverpages.org/xml-rpc.html)
  - [Citations from CiteSeer](http://citeseer.org/cs?q=XML+and+RPC)
  - [Jabber-RPC](https://web.archive.org/web/20060925025439/http://www.jabber.org/jeps/jep-0009.html) [Jabber](https://ko.wikipedia.org/wiki/Jabber "wikilink") 프로토콜 상에서의 XML-RPC
  - [pyJabberXMLRPC](http://gdr.geekhood.net/gdrwpl/jxmlrpc.php): Python용 (Jabber 상에서의 XML-RPC)
  - [Secure Apache XML-RPC](https://web.archive.org/web/20051116090755/http://members.fortunecity.com/neptune42/xmlrpc/index.htm)
  - [RemObjects SDK](http://www.remobjects.com/ro) [SOAP등을](https://ko.wikipedia.org/wiki/Simple_Object_Access_Protocol "wikilink") 위한 XML-RPC
  - [RealThinClient SDK](http://www.realthinclient.com): Delphi/C++용
  - [XML-RPC in Flash ActionScript 2.0](http://xmlrpcflash.mattism.com)
  - [XML-RPC.NET](https://web.archive.org/web/20170620152017/http://xml-rpc.net/): .NET용
  - [Redstone XML-PRC Library](http://xmlrpc.sourceforge.net/) Java용 오픈소스 라이브러리

[분류:XML 기반 표준](https://ko.wikipedia.org/wiki/분류:XML_기반_표준 "wikilink") [분류:분산 컴퓨팅](https://ko.wikipedia.org/wiki/분류:분산_컴퓨팅 "wikilink") [분류:인터넷 프로토콜](https://ko.wikipedia.org/wiki/분류:인터넷_프로토콜 "wikilink")