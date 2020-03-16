> This article is converted from Wikipedia: [USB    ](https://ko.wikipedia.org/wiki/USB____).


**USB 대용량 저장소 장치 유형**(USB mass-storage device class, USB MSC)은 [USB](../Page/USB.md "wikilink")에 관련된 USB 인플리멘터스 포럼(Implementers Forum)이 규정한 컴퓨팅 [통신 프로토콜이다](../Page/통신_프로토콜.md "wikilink"). 이 표준은 다양한 저장매체에 대한 인터페이스를 제공한다. 이 표준을 지원하는 장치들을 대용량 저장소 유형(MSC) 장치라고 한다. MSC가 공식 머리글이지만, 온라인 은어로 UMS(Universal Mass Storage)라는 머리글을 사용하고 있다.

[섬네일](https://ko.wikipedia.org/wiki/파일:USB_flash_drive.jpg "wikilink") - USB 대용량 장치 계열 기능이 추가되어 있다.\]\]

이 표준(USB MSC)에 따라 컴퓨터와 연결되는 장치들의 일부를 살펴보면 아래와 같다.

  - 외장형 하드 드라이브
  - 외장형 광학 드라이브(CD / DVD 리더 및 기록 드라이브)
  - 이동형 플래시 메모리 장치
  - 표준 플래시 메모리 카드와 USB 연결을 이어주는 어댑터
  - 디지털 카메라
  - 다수의 디지털 오디오 플레이어와 이동형 미디어 플레이어
  - 카드 리더기
  - 이동형 게임 시스템(노키아 N-GAGE/소니 PSP)
  - 개인 정보 단말기나 휴대용 컴퓨터
  - 일부 최신 휴대전화 단말기 (이를테면, 소니 에릭슨 K800 ,K510, 노키아 N73, 노키아 E61)

## 장치 접근

USB 대용량 저장소 장치 유형은 연결되는 장치에서 사용되는 [파일 시스템을](../Page/파일_시스템.md "wikilink") 특정하고 있지는 않고, 대신 하드 디스크의 낮은 수준의 인터페이스처럼 데이터를 섹터 단위로 읽고 쓰는 수준의 단순한 인터페이스만을 규정한다. 따라서 운영 체제는 USB 드라이브를 하드 드라이브처럼 다룰 수 있고 그들이 운영 체제에서 제공하는 파일 시스템으로 [포맷하는](../Page/디스크_포맷.md "wikilink") 것도 가능한다.

디지털 카메라나, MP3 플레이어와 같은 류의 장치들에서는 FAT 파일시스템이 장치 제조사에 의해 선호된다. 이동성이 좋고 상대적으로 편리하기 때문에 USB 플래시 드라이브, 디지털 카메라, 디지털 오디어 플레이어같은 임베디드 장치에서 가장 보편적인 파일 시스템은 마이크로소프트 사의 [FAT](https://ko.wikipedia.org/wiki/FAT "wikilink")이나 [FAT32이다](../Page/파일_할당_테이블.md "wikilink"). 이런 장치에서 파일 시스템을 변경하면 장치가 동작하지 않을 수도 있으므로, 포맷 방식을 바꾸지 않는 것이 좋다.

대용량의 USB 기반 하드 디스크의 경우 [NTFS](../Page/NTFS.md "wikilink")처럼 [마이크로소프트 윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 외부에서는 지원받기 힘든 파일 시스템으로 포맷되기도 하며, 하지만 애플 매킨토시나 리눅스, 솔라리스, BSD 같은 운영 체제에서 사용되는 방식으로 포맷될 수도 있다. 물론 이런 독점적인 방식으로 포맷이 되면 디바이스의 내용에 접근하는 OS의 범위를 제한하게 되는 단점이 있다.

## USB 대용량 저장소 장치 유형의 장단점

USB 대용량 저장소 장치 유형 [인터페이스](https://ko.wikipedia.org/wiki/인터페이스 "wikilink")는 디지털 카메라나 미디어 플레이어 같은 장치들에게 매력적인 옵션이다. 이런 장치들은 복잡한 기능을 제공하기보다 단순히 데이터 저장소 역할만 할 수 있기 때문이다. 대용량 저장소 장치 인터페이스를 사용해서 단순한 데이터 저장소를 제공함으로써, 운영 체제가 제공하는 USB 드라이버 스택 상의 USB 대용량 저장소 장치 유형에 대한 높은 수준의 지원을 받을 수 있다. 또한 내부 메모리에 대한 쉬운 읽기 쓰기 접근을 허용할 수 있다. 즉, 운영 체제에서 USB 대용량 저장소 장치가 하나의 [디렉터리](https://ko.wikipedia.org/wiki/디렉터리 "wikilink")로 접근 가능해지면서 많은 응용 소프트웨어에서 장치 내부의 파일에 직접 접근할 수 있게 된다.

이런 방식의 단점은 USB 인터페이스를 통해 추가적인 기능을 제공할 수 없다는 것이다. 이를테면, 디지털 카메라 제조사는 디지털 카메라가 이미지 캡처 소프트웨어에 의해 제어되는 것을 허용하는 USB 정지 영상 장치 계열을 구현하고자 할 수도 있다. 일부 USB 디지털 카메라는 대용량 기억 장치나 정지 화면 장치 ([PictBridge](https://ko.wikipedia.org/wiki/PictBridge "wikilink") 또는 PTP) 중 하나로 보여지도록 전환하는 기능을 제공한다. 하지만 동시에 할 수는 없는데 그 이유는 운영 체제의 파일 시스템 계층이 독점적으로 장치를 사용하기 때문이다.

## 같이 보기

  - [미디어 전송 프로토콜](../Page/미디어_전송_프로토콜.md "wikilink")
  - [USB 플래시 드라이브](../Page/USB_플래시_드라이브.md "wikilink")

## 외부 링크

  - [대용량 장치 유형 규격](https://web.archive.org/web/20120220152723/http://www.usb.org/developers/devclass_docs/usb-msc-overview-1.3b.pdf) — USB 포럼

  - [대용량 장치 시동 정보](https://web.archive.org/web/20070926235808/http://www.usb.org/developers/devclass_docs/usb_msc_boot_1.0.pdf)

[분류:USB](https://ko.wikipedia.org/wiki/분류:USB "wikilink")