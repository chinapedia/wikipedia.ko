> This article is converted from Wikipedia: [Matroska](https://ko.wikipedia.org/wiki/Matroska).


**마트료시카 멀티미디어 컨테이너**()는 [오픈 표준](https://ko.wikipedia.org/wiki/오픈_표준 "wikilink") [자유](https://ko.wikipedia.org/wiki/자유_파일_포맷 "wikilink") [컨테이너 포맷이다](https://ko.wikipedia.org/wiki/컨테이너_포맷_\(디지털\) "wikilink"). 또한 개수 제한 없이 비디오, 오디오, 그림, 자막 트랙을 한 파일 안에 담을 수 있는 [파일 형식이기도](https://ko.wikipedia.org/wiki/파일_형식 "wikilink") 하다.\[1\] 흔히 쓰이는 영화/드라마 등의 멀티미디어 콘텐트를 담기 위한 보편적인 포맷으로서 개발되었다. [AVI](../Page/오디오_비디오_인터리브.md "wikilink"), [MP4](https://ko.wikipedia.org/wiki/MP4 "wikilink") 혹은 [ASF](https://ko.wikipedia.org/wiki/능동_스트리밍_포맷 "wikilink") 등을 대체하기 위해 만들어졌다. 하지만 마트료시카 포맷은 완전한 [오픈 소스이다](../Page/오픈_소스.md "wikilink"). 마트료시카 파일 확장자로서, 비디오 파일에는 **`.MKV`**를 쓰고, 오디오 파일에는 **`.MKA`**를 쓴다.

마트료시카는 [영어](../Page/영어.md "wikilink")로는 "Matroska"라고 표기한다. 인형 속에 계속 인형이 들어 있는 러시아 민속 인형인 [마트료시카](https://ko.wikipedia.org/wiki/마트료시카 "wikilink") 인형을 뜻하는 [러시아어](../Page/러시아어.md "wikilink") 단어 матрёшка(발음은 [IPA](https://ko.wikipedia.org/wiki/위키백과:IPA "wikilink") , [영어](../Page/영어.md "wikilink")로 Matryoshka가 된다. 철자가 약간 다르다.)에서 온 말이다. 마트료시카 팀은 마트료시카 인형 속에 인형이 계속 들어 있는 점에 착안하여 이러한 이름을 붙였다. 비디오 및 오디오 데이터를 담는 컨테이너이므로 마트료시카 인형에 비유한 것이다.

## 역사

마트료시카 프로젝트는 [2003년](../Page/2003년.md "wikilink") [12월 7일](../Page/12월_7일.md "wikilink") 발표되었다. 이전의 컨테이너 포맷으로부터의 [포크였다](https://ko.wikipedia.org/wiki/포크_\(소프트웨어\) "wikilink"). 다른 바이너리 포맷 대신 [확장형 이진 메타 언어](https://ko.wikipedia.org/wiki/확장형_이진_메타_언어 "wikilink")(EBML)을 쓰는 것에 대해 프로젝트의 창설자와 주 개발자 사이에 이견이 있었기 때문이었다. 마트료시카 프로젝트의 창설자는 EBML을 사용한다면 많은 이점이 있을 것이라고 생각하였다. 프로젝트의 목표가 바뀌거나 새로운 포맷이 등장한다든가 해도 파일 포맷을 쉽게 확장할 수 있다고 봤기 때문이었다.

## 목표

마트료시카는 EBML에 뿌리를 두고 있다. 그러한 까닭에 마트료시카는 지속 가능성과 확장성을 염두에 두고 설계되었다. (AVI와는 다른 점이다.) 마트료시카 팀은 Doom9.org 나 hydrogenaudio.org와 같은 사이트에서 공공연하게 그들의 장기적인 목표는 현대적이고, 유연성 있고, 크로스-플랫폼인 멀티미디어 포맷을 개발하는 것이라고 밝히고 있다. 또한 다음과 같이 전개되는 것을 목표로 하고 있다:

  - 스트리밍에 대한 강건한 지원;
  - EBML에 기반한 "DVD-like" 메뉴 시스템;
  - 마트료시카 파일을 생성하고 편집해줄 수 있는 다양한 툴 개발;
  - 개발자들이 마트료시카 포맷 지원 기능을 애플리케이션에 쉽게 첨가할 수 있는 라이브러리 개발;
  - 하드웨어 제조사들이 임베디드 멀티미디어 기기에서의 마트료시카 포맷 지원 기능을 추가하도록 도움;
  - 여러 [운영 체제](../Page/운영_체제.md "wikilink") 상에서 마트료시카의 네이티브(native) 지원.

## 지원 소프트웨어

다음과 같은 소프트웨어들이 마트료시카를 (네이티브하게) 지원한다.

  - [아주어러스](https://ko.wikipedia.org/wiki/아주어러스 "wikilink") [뷰즈](https://ko.wikipedia.org/wiki/뷰즈 "wikilink") 미디어 플레이어
  - [BS.Player](https://ko.wikipedia.org/wiki/BS.Player "wikilink")
  - [더 코어 미디어 플레이어](https://ko.wikipedia.org/wiki/더_코어_미디어_플레이어 "wikilink")
  - 코어플레이어 모바일
  - [The Core Pocket Media Player](https://ko.wikipedia.org/wiki/The_Core_Pocket_Media_Player "wikilink")
  - [곰플레이어](../Page/곰플레이어.md "wikilink")
  - [Gstreamer](https://ko.wikipedia.org/wiki/Gstreamer "wikilink")-기반의 플레이어들 ([토템 (미디어 플레이어)](https://ko.wikipedia.org/wiki/토템_\(미디어_플레이어\) "wikilink") 등등)
  - [HandBrake](https://ko.wikipedia.org/wiki/HandBrake "wikilink")
  - [젯오디오](https://ko.wikipedia.org/wiki/젯오디오 "wikilink")
  - [The KMPlayer](https://ko.wikipedia.org/wiki/The_KMPlayer "wikilink")
  - [미디어 플레이어 클래식](../Page/미디어_플레이어_클래식.md "wikilink")
  - [미디어포털](https://ko.wikipedia.org/wiki/미디어포털 "wikilink")\[2\]
  - [메즈모](https://ko.wikipedia.org/wiki/메즈모 "wikilink")(Mezzmo) 미디어 플레이어
  - [엠플레이어](https://ko.wikipedia.org/wiki/엠플레이어 "wikilink")
  - [토템 (미디어 플레이어)](https://ko.wikipedia.org/wiki/토템_\(미디어_플레이어\) "wikilink")
  - [VLC 미디어 플레이어](../Page/VLC_미디어_플레이어.md "wikilink")
  - [VSO 소프트웨어](https://ko.wikipedia.org/wiki/VSO_소프트웨어 "wikilink")
  - [WinDVD](../Page/WinDVD.md "wikilink")
  - [Xbox Media Center](https://ko.wikipedia.org/wiki/Xbox_Media_Center "wikilink")
  - [xine](https://ko.wikipedia.org/wiki/xine "wikilink")
  - [줌 플레이어](https://ko.wikipedia.org/wiki/줌_플레이어 "wikilink")
  - [팟플레이어](../Page/팟플레이어.md "wikilink")
  - [무비스트](https://ko.wikipedia.org/wiki/무비스트_\(소프트웨어\) "wikilink")

## 하드웨어 지원

[시그마 디자인즈](https://ko.wikipedia.org/wiki/시그마_디자인즈 "wikilink") 사의 8634, 8635 칩이 마트료시카를 지원한다. 단, 적절한 펌웨어의 지원을 받아야 하고, 마트료시카 파일은 H.264 혹은 MPEG-4 ASP 비디오( HD 해상도 포함 ), MP3, AAC, DTS, AC3 오디오를 담고 있어야 한다. 이러한 칩에 기반한 초창기 제품들로서는 Syabas PopCorn Hour NMT-A100 네트워크 스트리밍 클라이언트가 있다.

[스카이디지털](https://ko.wikipedia.org/wiki/스카이디지털 "wikilink")의 Venice V38 Combo, V38 SATA, V13 HD도 MKV와 MKA 재생을 지원한다.

[맥시안](https://ko.wikipedia.org/wiki/맥시안 "wikilink")의 D900/E900/L900 시리즈도 MKV와 MKA 재생을 지원한다.

[코원시스템](../Page/코원시스템.md "wikilink")의 A3도 Matroska(MKV, MKA) 파일의 재생을 지원한다.

## 마트료시카 콘텐츠

초창기에는 이 포맷의 사용은 저조하였다. [일본의 애니메이션계의](../Page/일본의_애니메이션.md "wikilink") [OGM](https://ko.wikipedia.org/wiki/OGM "wikilink") 포맷과 경쟁하였다. 이 두 포맷 모두 멀티플 오디오 트랙을 지원했고 자막 내장을 지원했기 때문이었다. 하지만, 최근 들어서는 마트료시카 포맷이 더 널리 사용되고 있는데, 그 까닭은 "릴리즈 계"(release scene, 영화 등을 불법으로 배포하는 문화 집단)가 TV 쇼, [HD-DVD](../Page/HD-DVD.md "wikilink"), [블루레이](https://ko.wikipedia.org/wiki/블루레이 "wikilink") 등의 [HDTV](https://ko.wikipedia.org/wiki/HDTV "wikilink") 립(rip)으로서 마트료시카 포맷을 자주 사용하기 때문이다. 마트료시카 컨테이너 안에는 보통 [H.264/AVC](https://ko.wikipedia.org/wiki/H.264/AVC "wikilink") 비디오 및 [AC3](https://ko.wikipedia.org/wiki/AC3 "wikilink")/[AAC](../Page/고급_오디오_부호화.md "wikilink")/[DTS](https://ko.wikipedia.org/wiki/디지털_시어터_시스템 "wikilink") (다중) 오디오 트랙, (때때로) 자막 트랙 등이 들어가 있다. H.264가 널리 쓰이기 이전에는 대부분의 MKV 파일 안에는 [리얼비디오](https://ko.wikipedia.org/wiki/리얼비디오 "wikilink")(RV9, RV10)로 인코딩된 비디오 트랙이 들어 있었다. 당시에는 이 코덱들이 [MPEG-4 파트 2](../Page/MPEG-4_파트_2.md "wikilink")(다시 말해, [DivX](../Page/DivX.md "wikilink"), [Xvid](https://ko.wikipedia.org/wiki/Xvid "wikilink") 코덱)보다 성능이 조금 나았기 때문이었다. 특히 [애니메](../Page/일본의_애니메이션.md "wikilink") 콘텐츠일 때 심했다. 또한 애니메 콘텐츠에는 [MP3](https://ko.wikipedia.org/wiki/MP3 "wikilink")이나 [보비스](https://ko.wikipedia.org/wiki/보비스 "wikilink") 코덱으로 인코딩된 오디오 스트림과 소프트-서브타이틀이 흔히 들어갔다.

## 라이선스

마트료시카는 공개형 표준, 즉 오픈 스탠다드(open standards) 프로젝트이다. 누구든지 무료로 사용할 수 있다. 즉 개인이 비트 스트림을 기술하는 기술 사양을 활용해서든지, 회사가 그것을 사용하려든지 누구나, 언제나, 누구에게나 공개할 수 있다. 마트료시카 개발 팀이 개발한 라이브러리는 [LGPL](https://ko.wikipedia.org/wiki/LGPL "wikilink") 라이선스가 걸려 있다. 이외에도 여러 파싱, 재생 라이브러리가 BSD 라이선스 하에 나와 있는데, 이들은 독자적(proprietary) 소프트웨어에 이용될 수 있다.

## EBML

확장형 이진 메타 언어(EBML)는 [XML](../Page/XML.md "wikilink")을 기본으로 삼아 만든, 데이터 컨테이너 방식이다. 태그 형식([바이너리의](../Page/이진_파일.md "wikilink") 의사 형식)으로 기술된다. 해석할 수 없는 태그는 무시하게 되어 있어서, 새로운 기능을 추가하기 쉽다.

## 확장자

  - .mkv Matroska Video (영상)
  - .mka Matroska Audio (음성만)
  - .mks Matroska Subtitles (자막만)

## 같이 보기

  - [LiVES](https://ko.wikipedia.org/wiki/LiVES "wikilink")
  - [컨테이너 포맷 비교](https://ko.wikipedia.org/wiki/컨테이너_포맷_비교 "wikilink")
  - [오픈 소스 코덱 및 컨테이너](https://ko.wikipedia.org/wiki/오픈_소스_코덱_및_컨테이너 "wikilink")

## 각주

## 외부 링크

  - [Official Matroska Homepage](http://www.Matroska.org/)

  - [Technical specifications for the Matroska Container Format](https://web.archive.org/web/20080125102107/http://www.matroska.org/technical/)

  - [Proposed RFC](https://web.archive.org/web/20081219000405/http://www.matroska.org/technical/specs/rfc/)

  - [CoreCodec – Official Matroska Developer Project Home](http://coreforge.org/)

  - [Perian (MKV) QuickTime Component For Mac](http://perian.org/#detail)

  - [Haali Media splitter](https://web.archive.org/web/20040707171532/http://haali.cs.msu.ru/mkv/)

  - [Project Announcement](http://forum.doom9.org/showthread.php?s=&postid=221947) on Doom9 forums

  - [Parser, de-/muxer and player](http://sourceforge.net/projects/guliverkli/)

  - [Linux and Windows tools for Matroska](https://web.archive.org/web/20080201013659/http://www.bunkus.org/videotools/mkvtoolnix/)

  - [The XviD-Ogg-MKV Walkthrough](https://web.archive.org/web/20080203114551/http://neap0litan.net/xvid/) – Step-by-step instructions for MKV encoding in Microsoft Windows

[분류:파일 포맷](https://ko.wikipedia.org/wiki/분류:파일_포맷 "wikilink") [분류:자유 멀티미디어 코덱](https://ko.wikipedia.org/wiki/분류:자유_멀티미디어_코덱 "wikilink") [분류:오픈 포맷](https://ko.wikipedia.org/wiki/분류:오픈_포맷 "wikilink")

1.
2.  [MediaPortal Features](http://www.team-mediaportal.com/content/view/42/117/) (01/01/2007)