> This article is converted from Wikipedia: [Mdir](https://ko.wikipedia.org/wiki/Mdir).


**Mdir**은 [도스](https://ko.wikipedia.org/wiki/도스 "wikilink") 사용자들이 도스 [명령 프롬프트에](https://ko.wikipedia.org/wiki/명령_프롬프트 "wikilink") 명령어를 입력하지 않아도 되도록 [사용자 인터페이스를](https://ko.wikipedia.org/wiki/사용자_인터페이스 "wikilink") 제공해 주는 유틸리티로 대한민국의 최정한이 작성했다. 제작자의 여자친구를 위해 처음 개발된 본 프로그램은, 당시에 컴퓨터를 잘 모르는 사용자들도 쉽게 컴퓨터를 다룰 수 있도록 고안되었다. 또한 개인 사용자들에게는 셰어웨어 버전으로도 다양한 기능들을 제공하였고 사용 기간에 특별한 제한이 없었다.

명령어를 일일이 입력할 필요 없이 화살표키와 엔터키만으로도 편하게 프로그램을 실행 할 수 있었기 때문에 많은 인기를 끌었다.

Mdir II에 이어, 여러 버그 수정과 기능 개선이 되고 버전이 업데이트되면서 1998년에 Mdir III 3.10까지 나왔다가 [마이크로소프트 윈도에](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 가려져 빛을 잃기 시작했다. 윈도용으로 [WinM](https://ko.wikipedia.org/wiki/WinM "wikilink")이 개발되었으나 현재는 더 이상 업데이트나 지원을 하지 않고 있다.

도스에서 M이라고 입력하면 쉽게 Mdir 프로그램이 실행되었다는 것 때문에 사람들은 이 프로그램을 **엠**이라고 줄여 부르기도 했다.

비슷한 프로그램으로는 [마이크로소프트](https://ko.wikipedia.org/wiki/마이크로소프트 "wikilink")의 [DOSSHELL](https://ko.wikipedia.org/wiki/DOSSHELL "wikilink")이 있으나 속도가 느려 인기를 끌지는 못하였다.

## 실행 파일

Mdir 유틸리티 패키지 안에는 다음과 같은 실행 파일들을 제공한다.

  - **M.EXE**: Mdir 기본 실행 프로그램
  - **MSET.EXE**: Mdir 설정 프로그램
  - **VV.EXE**: 뷰어 프로그램 "보라" - 완성형/조합형 한글을 지원하는 문서 보기 프로그램
  - **HCONV.EXE**: 텍스트 파일의 확장형/조합형 상호 변환 프로그램
  - **DSCMAN.EXE**: 하드 디스크 안에 쓸모 없는 파일을 지워 주고 정리해 주는 프로그램
  - **MCD.BAT**: 디렉터리의 트리를 나열하고 들어가는 프로그램 ([노턴](https://ko.wikipedia.org/wiki/노턴_유틸리티 "wikilink") 유틸리티에서 나온 NCD와 비슷함)
  - **MFF.EXE**: 파일 찾기 프로그램
  - **MF.EXE**: 플로피 디스크 포맷 프로그램

## 사용 환경

도스용 최신 버전 기준으로 사용 환경은 다음과 같다.\[1\]

  - [IBM](https://ko.wikipedia.org/wiki/IBM "wikilink")-PC/AT 100% 호환기종. 286, 386, 486, [펜티엄](https://ko.wikipedia.org/wiki/펜티엄 "wikilink")
  - [MS-DOS](https://ko.wikipedia.org/wiki/MS-DOS "wikilink") 3.3 100% 호환 [운영 체제](https://ko.wikipedia.org/wiki/운영_체제 "wikilink"), 윈도 3.1, 윈도 95.
  - [HGC](https://ko.wikipedia.org/wiki/허큘레스_그래픽_카드 "wikilink"), [EGA](https://ko.wikipedia.org/wiki/강화_그래픽_어댑터 "wikilink"), [VGA](https://ko.wikipedia.org/wiki/VGA "wikilink") ([CGA는](https://ko.wikipedia.org/wiki/컬러_그래픽스_어댑터 "wikilink") MSET과 보라가 지원하지 않음)
  - [기본 메모리](../Page/기본_메모리.md "wikilink") 640 킬로바이트 이상 (적어도 265K 이상 필요)
  - 보조 기억장치 ([하드 디스크에](https://ko.wikipedia.org/wiki/하드_디스크 "wikilink") 설치 권장)
  - [CD-ROM](../Page/CD-ROM.md "wikilink") 드라이브 지원
  - [LAN](https://ko.wikipedia.org/wiki/LAN "wikilink") 환경 지원 (MSET에서 지정)
  - [XMS](https://ko.wikipedia.org/wiki/연속_확장_메모리_규격 "wikilink"), [EMS](https://ko.wikipedia.org/wiki/중첩_확장_메모리_규격 "wikilink"), 디스크를 스와핑 사용함. 남은 공간 300K 이상
  - 한글/한자 바이오스에서 한글 메시지 지원.

### 제한 사항

도스용 최신 버전 기준으로 제한 사항은 다음과 같다.\[2\]

  - [윈도 95](https://ko.wikipedia.org/wiki/윈도_95 "wikilink") (MS-DOS 7.0) 이상에서만 긴 파일 이름 지원
  - 한 디렉터리에 최대 2000개까지의 파일 (메모리 부족시 500개까지)
  - 최대 1000개까지의 주석, 한 주석에 80글자까지
  - 한 드라이브에 최대 2000개까지의 디렉터리(MCD에서)

## 지원하는 압축 파일

압축 파일을 볼 수 있으나, 압축을 풀려면 별도의 유틸리티가 필요하다. 기본 단축키는 이다.

  - LZH, ICE
  - ZIP
  - ARJ
  - ARC
  - OMP
  - ZOO
  - SQZ
  - RAR
  - UC2
  - HPK
  - ACE

## 참조

<references/>

## 함께 보기

  - [WinM](https://ko.wikipedia.org/wiki/WinM "wikilink")
  - [토탈 커맨더](https://ko.wikipedia.org/wiki/토탈_커맨더 "wikilink") - Mdir, WinM과 비슷한 프로그램
  - [넥서스파일](https://ko.wikipedia.org/wiki/넥서스파일 "wikilink") - Mdir과 매우 유사한 디자인과 인터페이스를 지닌 파일 관리자

[분류:파일 관리자](https://ko.wikipedia.org/wiki/분류:파일_관리자 "wikilink")

1.  Mdir 유틸리티 소프트웨어 설명서 참조
2.