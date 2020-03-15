> This article is converted from Wikipedia: [Ark ](https://ko.wikipedia.org/wiki/Ark_).


**Ark 라이브러리**(ArkLibrary)는 [반디집](../Page/반디집.md "wikilink")을 만든 반디소프트(대표 박근홍)에서 개발한 압축 파일 처리용 상용 미들웨어이다. 5.0 버전까지는 일부 비상업적 용도에 한하여 무료로 사용이 가능하였지만, 6.0 버전부터는 상용 구매를 목적으로 하는 테스트 이외에는 구매 후 사용하도록 라이선스가 바뀌었다.\[1\] [반디집](../Page/반디집.md "wikilink") 자체도 Ark 라이브러리를 이용하여 개발되었기 때문에 Ark 라이브러리를 이용하면 반디집에서 제공하는 압축파일과 관련된 모든 기능을 사용할 수 있다. 32비트 및 64비트의 [마이크로소프트 윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 운영 체제 계열 중 [윈도 7](https://ko.wikipedia.org/wiki/윈도_7 "wikilink"), [윈도 8](https://ko.wikipedia.org/wiki/윈도_8 "wikilink"), [윈도 10을](../Page/윈도우_10.md "wikilink") 지원하며, [POSIX](https://ko.wikipedia.org/wiki/POSIX "wikilink") 시스템 은 [OS X](https://ko.wikipedia.org/wiki/OS_X "wikilink"), [우분투](https://ko.wikipedia.org/wiki/우분투 "wikilink"), [FreeBSD](https://ko.wikipedia.org/wiki/FreeBSD "wikilink") 와 같은 대부분의 운영 체제를 지원한다.

## 주요 기능

제작사에서 밝힌 주요 기능은 다음과 같다.\[2\]

  - ZIP, ALZ, EGG, TAR, BH, 7Z, WIM, RAR, ARJ, LZH, GZ, BZ2, ISO, UDF, IMG, CAB, XZ, Z, LZMA를 비롯한 많은 압축포맷의 압축 해제를 지원한다.
  - ZIP, TAR, TGZ 포맷의 압축하기 기능을 지원하며, 분할 ZIP 포맷도 생성이 가능하다.
  - 기능에 비하여 DLL 파일의 용량이 매우 작다.
  - C++ 인터페이스를 지원하며, 사용방법이 매우 쉽다.
  - 많은 유저들이 사용하는 [반디집](../Page/반디집.md "wikilink")에 사용되는 라이브러리로서, 안정적이다.
  - 64비트 운영 체제를 지원한다.

## 특징

다양한 형식을 가지는 압축파일의 압축해제 지원 및 ZIP 포맷 등의 압축 파일 생성 기능 지원 언어: C++ (Visual Studio, GCC, Clang) 지원 OS: Windows(7/8/8.1/10, x86/x64/ARM64), macOS, Linux, FreeBSD

## 지원 포맷

1\. 압축 해제 ZIP: Deflate / BZ2 / Deflate64 / LZMA / implode / shrink / Jpeg / Wavpack 압축 알고리즘 지원, ZipCrypto / AES128 / AES192 / AES256 암호화 알고리즘 지원, ZIP64 / ZIPX 포맷 지원, 여러 형태의 분할 압축된 파일 지원. ALZ: Deflate/변형 BZ2 알고리즘 지원, 분할 압축 지원 EGG: Deflate / BZ2 / LZMA 압축 알고리즘 지원, ZipCrypto / AES128 / AES256 / LEA 암호화 알고리즘 지원, 분할 압축 지원 TAR: 8기가 이상의 파일 처리 지원, UStar / LongLink 처리 지원, Sparse 포맷 지원, 심볼릭 링크 지원 BH: FUSE / Deflate 압축 알고리즘 지원, ZipCrypto 암호화 알고리즘 지원 7z: .7z.001 형태의 분할 압축파일 지원 WIM: RAW 및 압축된 포맷 지원 RAR: 분할 압축 지원, RAR4/RAR5 포맷 지원 ARJ: 분할 압축된 파일 지원, 암호걸린 파일은 미지원 ACE: unacev2.dll 파일 및 unace32.exe 파일 필요 CAB: LZX, MSZIP, QUANTUM 알고리즘 지원, SFX 및 분할 압축된 파일 지원 기타: LZH, GZ, BZ2, ISO, BIN, UDF, IMG, XZ, Z, LZMA, J2J, NSIS, AES, Arc, LZIP, ZPAQ, MS Compound 포맷 지원

2\. 압축 파일 생성 ZIP: Deflate / LZMA / XZ 알고리즘 지원, ZipCrypto 2.0 / AES 암호화 지원, ZIP 표준 분할압축, ZIP64 지원 7z: LZMA / LZMA2 알고리즘 지원, AES 암호화 지원, 헤더 암호화/압축 지원 기타: TAR, TGZ, LZH, ISO(Joliet), GZ, XZ 포맷 압축 및 생성기능 제공

## 관련 문서

  - [반디집](../Page/반디집.md "wikilink")

## 외부 링크

  - [반디소프트::Ark 라이브러리 공식 홈페이지](https://www.bandisoft.com/ark/)

## 각주

<references />

[분류:압축 소프트웨어](https://ko.wikipedia.org/wiki/분류:압축_소프트웨어 "wikilink") [분류:윈도우 소프트웨어](https://ko.wikipedia.org/wiki/분류:윈도우_소프트웨어 "wikilink") [분류:C++ 라이브러리](https://ko.wikipedia.org/wiki/분류:C++_라이브러리 "wikilink") [분류:반디소프트](https://ko.wikipedia.org/wiki/분류:반디소프트 "wikilink")

1.
2.