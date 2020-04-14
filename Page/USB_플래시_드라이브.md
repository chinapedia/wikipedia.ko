> This article is converted from Wikipedia: [USB 플래시 드라이브](https://ko.wikipedia.org/wiki/USB_플래시_드라이브).


[섬네일](https://ko.wikipedia.org/wiki/파일:SanDisk_USB.jpg "wikilink") [섬네일](https://ko.wikipedia.org/wiki/파일:USB_flash_drive.JPG "wikilink")

**USB 플래시 드라이브**()는 [USB](../Page/USB.md "wikilink") 포트에 꽂아 쓰는 [플래시 메모리를](../Page/플래시_메모리.md "wikilink") 이용한 이동형 저장 장치를 말한다. 일반적으로 [광학 디스크 드라이브에](../Page/광학_디스크_드라이브.md "wikilink") 비해 크기가 훨씬 작지만, 쉽게 제거할 수(removable) 있고 [데이터](https://ko.wikipedia.org/wiki/데이터 "wikilink")를 다시 기록할 수(rewritable) 있다. 2014년 기준으로 1[TB까지](https://ko.wikipedia.org/wiki/테라바이트 "wikilink") 다양한 용량의 제품이 판매 중으로, 그 중에서 4\~32[기가바이트](https://ko.wikipedia.org/wiki/기가바이트 "wikilink") 용량의 제품이 일반적이다. **USB 메모리**(USB memory)나 **USB 스틱**(USB stick), **USB 키**(USB key) 등으로도 불린다. 간단히 USB라고 부르는 경우도 있는데 USB는 [컴퓨터](../Page/컴퓨터.md "wikilink")와 주변기기를 연결하는 [인터페이스](https://ko.wikipedia.org/wiki/인터페이스 "wikilink")의 한 종류이지 이동형 저장장치의 종류가 아니므로, 엄밀히 말해 틀린 표현이다.

크기가 일회용 라이터 정도에 불과해 휴대하기도 매우 간편하다. 또한 큰 용량의 파일을 가지고 다닐 때나 파일을 옮길 때 편리하며 보안용 암호장치도 있어 자료를 안전하게 보관할 수 있다. 특히 대한민국 환경에서는 [인터넷 뱅킹](https://ko.wikipedia.org/wiki/인터넷_뱅킹 "wikilink") 사용자가 회사나 PC방에서 거래할 때 필요한 [공인인증서](../Page/공인인증서.md "wikilink")를 안전하게 쓸 수 있어 정보의 외부유출 위험을 줄일 수 있다. 다만 공인인증서는 한 폴더만 복사하면 바로 인증서를 사용할 수 있기 때문에 각별한 주의가 요구된다.

## 역사

### 특허

말레이시아의 푸아(Pua Khein-Seng)는 많은 사람들에게 "펜 드라이브의 아버지"로 간주된다. 세계 최초의 싱글 칩 USB 플래시 컨트롤러를 통합한 것으로 유명하다. 현재 그는 타이완 [파이슨](https://ko.wikipedia.org/wiki/파이슨 "wikilink")(Phison) 일렉트로닉스의 CEO이자 창립자이다.\[1\] 푸아는 4개의 다른 특허와 함께 파이슨 일렉트로닉스를 설립했으며 시스템 온 칩 기출을 포함한 세계 최초의 USB 플래시 드라이브를 생산한 것으로 알려져 있다.

### 최초의 상용화 제품

[트렉 테크놀로지와](https://ko.wikipedia.org/wiki/트렉_2000_인터내셔널 "wikilink") [IBM](../Page/IBM.md "wikilink")은 2000년에 최초의 USB 플래시 드라이브를 상용화하여 판매하기 시작했다. 트렉 테크놀로지의 모델 브랜드 이름은 "섬드라이브"(ThumbDrive)였고, IBM의 이름은 북아메리카 기준으로 "디스크온키"(DiskOnKey)인데 이는 이스라엘 회사 [M-시스템즈](https://ko.wikipedia.org/wiki/M-시스템즈 "wikilink")가 개발, 제조한 것이다.\[2\]\[3\] IBM의 USB 플래시 드라이브는 2000년 12월 15일에 판매가 시작되었고\[4\] 용량은 8 MB였는데, 이는 당시 일반적으로 쓰였던 [플로피 디스크](https://ko.wikipedia.org/wiki/플로피_디스크 "wikilink") 보다 5배나 용량이 많았다.

## 설계와 구현

<table>
<tbody>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/파일:Usbkey_internals.jpg" title="wikilink">350px</a><br />
<strong>일반적인 USB 플래시 드라이브의 내부</strong></p></td>
</tr>
<tr class="even">
<td><p>1</p></td>
</tr>
<tr class="odd">
<td><p>2</p></td>
</tr>
<tr class="even">
<td><p>3</p></td>
</tr>
<tr class="odd">
<td><p>4</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
</tr>
<tr class="odd">
<td><p>6</p></td>
</tr>
<tr class="even">
<td><p>7</p></td>
</tr>
<tr class="odd">
<td><p>8</p></td>
</tr>
</tbody>
</table>

USB 플래시 드라이브에서 장치의 한쪽 끝은 단일 [표준-A USB 플러그로](../Page/USB.md "wikilink") 되어 있고, 일부 플래시 드라이브는 여기에 [마이크로 USB](https://ko.wikipedia.org/wiki/마이크로_USB "wikilink") 플러그를 제공함으로써 다른 장치 간 데이터 전송을 용이하게 하고 있다.\[5\]

플라스틱 케이스 내부에는 조그마한 회로 기판이 있으며 여기에는 약간의 전기 회로 부품과 적은 수의 [표면 실장](../Page/표면_실장_기술.md "wikilink") [집적 회로](../Page/집적_회로.md "wikilink")(IC)가 포함되어 있다. 일반적으로 이러한 IC들 중 하나는 USB 단자와 기판 메모리 사이의 접점을 제공하는 반면, 다른 하나는 [플래시 메모리이다](../Page/플래시_메모리.md "wikilink"). 드라이브는 일반적으로 [USB 대용량 저장소 장치 유형을](../Page/USB_대용량_저장소_장치_유형.md "wikilink") 사용하여 호스트와 통신한다.

## 기술

플래시 메모리는 더 오래된 수많은 기술들을 병합한 것으로, [마이크로프로세서](../Page/마이크로프로세서.md "wikilink") 기술의 진보로 말미암아 단가와 전력 소비량이 낮고 크기가 작아졌다. 메모리 용량은 초기 [EPROM](../Page/EPROM.md "wikilink") 및 [EEPROM](../Page/EEPROM.md "wikilink") 기술을 기반에 두고 있었다.

[USB](../Page/USB.md "wikilink")와 같은 고속 직렬 데이터 인터페이스의 개발을 통해 직렬로 접근되는 스토리지를 갖춘 반도체 메모리 시스템이 가시권에 들어섰고, 동시에 고속의 저전력 마이크로프로세서 시스템의 개발을 통해 매우 작은 시스템으로 통합을 가능케 하였다.

### 필수 부품

일반적으로 플래시 드라이브에는 5가지 부품이 있다:

  - 표준-A USB 플러그
  - USB 대용량 저장소 컨트롤러
  - [NAND 플래시](https://ko.wikipedia.org/wiki/NAND_플래시 "wikilink") 메모리 칩
  - [결정 진동자](../Page/결정_진동자.md "wikilink")
  - 덮개

### 추가 부품

다음이 더 포함될 수 있다.

  - [점퍼](https://ko.wikipedia.org/wiki/점퍼 "wikilink")와 테스트 핀
  - [LED](../Page/발광_다이오드.md "wikilink")
  - [쓰기 보호](https://ko.wikipedia.org/wiki/쓰기_보호 "wikilink") 스위치
  - 비장착 공간
  - USB 단자 덮개
  - 전송 보조 덮개
  - 일부 드라이브는 마치 메모리 [카드 리더처럼](../Page/카드_리더.md "wikilink") 내장 [메모리 카드](../Page/메모리_카드.md "wikilink") 슬롯을 통해 스토리지 확장을 제공한다.\[6\]\[7\]

## 같이 보기

  - [외장 하드 디스크](https://ko.wikipedia.org/wiki/외장_하드_디스크 "wikilink")
  - [파일 동기화](https://ko.wikipedia.org/wiki/파일_동기화 "wikilink")
  - [라이브 USB](../Page/라이브_USB.md "wikilink")
  - [플래시 메모리](../Page/플래시_메모리.md "wikilink")

## 각주

[분류:USB](https://ko.wikipedia.org/wiki/분류:USB "wikilink") [분류:컴퓨터 저장 매체](https://ko.wikipedia.org/wiki/분류:컴퓨터_저장_매체 "wikilink") [분류:이스라엘의 발명품](https://ko.wikipedia.org/wiki/분류:이스라엘의_발명품 "wikilink")

1.
2.  [도브 모란, 실패를 통한 배움의 가치를 논하다](http://www.itdaily.kr/news/articleView.html?idxno=35102), IT데일리
3.
4.
5.
6.  [PNY USB Flash Drive – CES 2006 – LetsGoDigital](http://www.ces-show.com/2006/review/pny/pny_usb_flash_drive.html). Ces-show.com. Retrieved on 2011-05-18.
7.  [BlueTrek Bizz – an expandable USB and a Bluetooth headset in one](http://www.techchee.com/2008/05/20/bluetrek-bizz-an-expandable-usb-drive-and-a-bluetooth-headset-in-one/) . TechChee.com (2008-05-20). Retrieved on 2011-05-18.