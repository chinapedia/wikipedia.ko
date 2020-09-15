> This article is converted from Wikipedia: [WavPack](https://ko.wikipedia.org/wiki/WavPack).


**WavPack**은 [자유 소프트웨어](../Page/자유_소프트웨어.md "wikilink"), [오픈 소스](../Page/오픈_소스.md "wikilink") [무손실 오디오 압축](https://ko.wikipedia.org/wiki/무손실_오디오_압축 "wikilink") [파일 형식이다](https://ko.wikipedia.org/wiki/파일_형식 "wikilink"). 데이비드 브라이언트(David Bryant)가 개발하였다.

## 특징

WavPack은 오디오 파일을 `.wv` 확장자로 압축한다. [.WAV](https://ko.wikipedia.org/wiki/웨이브 "wikilink") 파일 형식을 가진 8비트, 16, 24 그리고 32 비트 부동소수점 오디오 파일을 압축할 수 있다. [서라운드 사운드](https://ko.wikipedia.org/wiki/서라운드_사운드 "wikilink") 스트림을 지원하며, 높은 주파수의 [샘플링 레이트를](../Page/샘플링_레이트.md "wikilink") 지원한다. 다른 무손실 오디오 압축 코덱과 마찬가지로 압축률은 소스에 따라 변한다. 하지만, 일반적인 팝 음악 파일에 대해서 보통 30% 내지 70%의 압축률을 보여준다. 또한, 클래식 음악에는 더 좋은 압축률을 보여주고, 다이내믹 레인지가 큰 소스에 대해서도 더 나은 압축률을 보여준다.

WavPack은 "하이브리드" 모드를 지원한다. 하이브리드 모드는 손실 압축 파일 하나(.wv)와 "손실 보정용"(correction) 파일 하나(.wvc)로 이루어진다. 이 두 개의 손실 압축 파일과 손실 보정용 파일을 가지고서 완벽히 손실 없이 원음을 압축해제 할 수 있다. 아니면 비교적 작은 크기의 고품질 손실 압축 파일(.wv)만 활용할 수도 있다.

이러한 방법은 손실 압축 코덱과 무손실 압축 코덱의 이점을 모두 가져다 준다. 현재 이러한 "하이브리드" 기능은 [OptimFROG](https://ko.wikipedia.org/wiki/OptimFROG "wikilink")와 WavPack만이 지원하고 있다.

## 요약

  - [오픈 소스](../Page/오픈_소스.md "wikilink"), [BSD 계열 라이선스](https://ko.wikipedia.org/wiki/BSD_라이선스 "wikilink")
  - 멀티플랫폼
  - 오류 강건(Error Robustness)
  - [스트리밍](../Page/스트리밍.md "wikilink") 기능
  - 멀티채널 오디오 및 고해상도 오디오 지원
  - 하이브리드/손실 모드
  - 하드웨어 지원
  - 태깅 지원 ([ID3](../Page/ID3.md "wikilink")v1, [APEv2 태그](https://ko.wikipedia.org/wiki/APEv2_태그 "wikilink"))
  - [RIFF](../Page/RIFF.md "wikilink") 청크(chunks) 지원
  - [리플레이 게인](https://ko.wikipedia.org/wiki/리플레이_게인 "wikilink") 호환
  - Win32용 자동압축풀림 파일 생성 기능
  - 32bit 부동소수점 스트림 지원
  - 임베디드 [CUE 시트](https://ko.wikipedia.org/wiki/CUE_시트 "wikilink") 지원
  - [MD5](../Page/MD5.md "wikilink") 해시 포함. 무결성 확인.

## 같이 보기

  - [FLAC](../Page/FLAC.md "wikilink")
  - [TTA (코덱)](../Page/TTA_\(코덱\).md "wikilink")
  - [Monkey's Audio](../Page/Monkey's_Audio.md "wikilink")

## 각주

## 외부 링크

  - [공식 웹사이트](http://www.wavpack.com/)

  - [WavPack forum at Hydrogenaudio Forums](http://www.hydrogenaudio.org/forums/index.php?showforum=68)

  - [Historical versions at ReallyRareWares](https://web.archive.org/web/20090503015616/http://www.rjamorim.com/rrw/wavpack.html)

  - [A comparison of several Lossless Audio encoders](http://wiki.hydrogenaudio.org/index.php?title=Lossless_comparison) at Hydrogenaudio Wiki.

  - [WavPack on MultimediaWiki](http://wiki.multimedia.cx/index.php?title=WavPack)

[분류:오디오 파일 포맷](https://ko.wikipedia.org/wiki/분류:오디오_파일_포맷 "wikilink") [분류:오디오 코덱](https://ko.wikipedia.org/wiki/분류:오디오_코덱 "wikilink") [분류:자유 멀티미디어 코덱](https://ko.wikipedia.org/wiki/분류:자유_멀티미디어_코덱 "wikilink") [분류:무손실 압축 알고리즘](https://ko.wikipedia.org/wiki/분류:무손실_압축_알고리즘 "wikilink") [분류:무손실 오디오 코덱](https://ko.wikipedia.org/wiki/분류:무손실_오디오_코덱 "wikilink") [분류:오픈 포맷](https://ko.wikipedia.org/wiki/분류:오픈_포맷 "wikilink")