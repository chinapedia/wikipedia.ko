> This article is converted from Wikipedia: [Dmesg](https://ko.wikipedia.org/wiki/Dmesg).


**dmesg** ("display message" 또는 "driver message"를 의미)는 대부분의 [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink")와 [유닉스](https://ko.wikipedia.org/wiki/유닉스 "wikilink") 기반 운영 체제에 있는 명령어로 [커널의](https://ko.wikipedia.org/wiki/커널_\(컴퓨팅\) "wikilink") 메시지 버퍼를 출력한다.

## 부팅

컴퓨터가 처음 [부팅](https://ko.wikipedia.org/wiki/부팅 "wikilink")될 때 커널이 메모리로 불러 들여진다. 이 단계에서 커널에 내장된 각 장치 드라이버가 해당 하드웨어를 탐색한다. 하드웨어를 발견하면 정확하게 무엇을 발견했는지 알려주는 메시지를 출력한다. 커널 내 다른 요소도 특정한 모듈의 존재 여부와 전달된 매개 변수 값을 출력한다. 그 메시지를 얼마나 자세하게 출력할지 제어하는 부팅 매개 변수를 설정할 수도 있다. 그런데 이 메시지는 모두 읽기 전에 화면에서 사라질 정도로 빨리 지나간다. 일부 시스템에서는 키보드 특정 키를 누르면 화면 출력을 일시 정지할 수 있다. dmesg 명령어로 시스템이 부팅된 후에 이러한 메시지를 검토할 수 있다.

## 부팅 이후

시스템이 부팅을 완료한 후에라도 커널이 가끔 진단 메시지를 추가로 출력할 수 있다. 실례를 들면 I/O 장치에서 오류가 발생하거나 USB가 핫 플러그될 때이다. dmesg는 이후에 이러한 메시지를 검토할 수 있는 수단을 제공한다. 이 메시지가 처음 출력될 때에는 시스템 콘솔로 출력된다. 그러므로 콘솔이 사용 중이라면 이 메시지는 사용자 프로그램 출력과 섞이거나 덮어쓰인다.

## 출력

dmesg 출력은 화면을 몇 번이나 채운다. 이 때문에 이 출력은 more, tail, less, grep과 같은 표준 텍스트 제어 도구를 이용해서 보통 검토한다. 이 출력은 syslog와 같은 시스템 데몬이 시스템 로그파일에 기록한다. 리눅스에서는 /var/log 디렉토리에 있는 로그 파일에서 유사한 정보를 찾을 수 있다.

## 브랜드 화면

많은 상용 운영 체제는 이 단계의 부팅 과정에서 브랜드 화면을 보여주어서 사용자는 메시지를 볼 수 없다. 하지만 ESC 키를 눌러 브랜드 화면을 끝내고 메시지를 볼 수 있는 방법도 자주 쓰이는 방법이다. 이것은 부팅이 안 될 때 아주 유용한 기능이다. 또한 dmesg처럼 부팅한 후에 이러한 메시지를 검토하는 방법도 있다.

## 같이 보기

  - [lspci](https://ko.wikipedia.org/wiki/lspci "wikilink"): 모든 PCI 버스와 장치에 관한 정보
  - [lsusb](https://ko.wikipedia.org/wiki/lsusb "wikilink"): 모든 USB 포트와 장치에 관한 정보
  - [uname](https://ko.wikipedia.org/wiki/uname "wikilink"): 시스템과 운영 체제 등에 관한 정보 출력

## 외부 링크

  - [dmesg(8)](http://man.freebsd.org/dmesg) FreeBSD 매뉴얼
  - [dmesg 명령어](http://www.linfo.org/dmesg.html) 리눅스 정보 프로젝트(LINFO)
  - [dmesg 설명](http://linuxgazette.net/issue59/nazario.html): 커널 출력 예시

[분류:유닉스 소프트웨어](https://ko.wikipedia.org/wiki/분류:유닉스_소프트웨어 "wikilink")