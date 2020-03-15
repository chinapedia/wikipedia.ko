> This article is converted from Wikipedia: [FLAC](https://ko.wikipedia.org/wiki/FLAC).


**FLAC**(Free Lossless Audio Codec, )은 [오디오 데이터 압축을](https://ko.wikipedia.org/wiki/오디오_데이터_압축 "wikilink") 위한 [파일 형식이다](https://ko.wikipedia.org/wiki/파일_형식 "wikilink"). [무손실 압축](https://ko.wikipedia.org/wiki/무손실_압축 "wikilink") 포맷이다. 다시 말해서, [MP3](https://ko.wikipedia.org/wiki/MP3 "wikilink"), [AAC](../Page/고급_오디오_부호화.md "wikilink"), [Vorbis](https://ko.wikipedia.org/wiki/Vorbis "wikilink")와는 달리 오디오 스트림에 손실이 발생하지 않는다.

다른 압축 방법들과 마찬가지로, FLAC의 장점은 전송율·대역폭·저장공간 등을 절약할 수 있다는 점인데, FLAC은 오디오 소스를 온전한 모습으로 보전해준다. 예를 들어, 디지털 레코딩([콤팩트 디스크](https://ko.wikipedia.org/wiki/콤팩트_디스크 "wikilink"))을 FLAC으로 인코드하였다가 디코드하면 정확히 똑같은 오디오 데이터를 얻을 수 있다. 보통, FLAC으로 압축하면 원래 크기의 40-50%로 줄어든다. (FLAC 개발자들은 약 47%이라고 주장)\[1\]

FLAC는 태깅(tagging), 앨범 아트, 빠른 건너뛰기(fast seeking)을 지원하기 때문에, 일상적인 음악 재생과 보관에 알맞다. FLAC은 [자유 소프트웨어이자](https://ko.wikipedia.org/wiki/자유_소프트웨어 "wikilink") 동시에 [오픈 소스 소프트웨어](../Page/오픈_소스_소프트웨어.md "wikilink"), 로열티 없는 소프트웨어이기 때문에, 많은 응용 소프트웨어가 FLAC을 지원하고 있다. 휴대용 음악 기기나 MP3 플레이어, 고급 오디오 시스템에서의 FLAC 지원은 얼마전까지만 해도 미미했으나 MP3 플레이어 등 휴대용 기기 한정으로 2013년 현재 상당수 기종에서 이 포맷을 지원한다. 특히 안드로이드 운영 체제를 탑재한 제품의 경우 음악 애플리케이션에 따라 이 포맷의 재생이 가능한 경우가 많다. 하지만 현재 인기있는 애플사의 제품들은, iTunes부터 FLAC 재생을 지원하지 않기 때문에 아이폰과 아이팟 모두 FLAC을 지원하지 않는다.\[2\] 그러나 iOS11에 새로 추가된 '파일'앱의 일부로 flac 재생 기능이 추가되었다.\[3\]

조시 콜슨(Josh Coalson)이 FLAC의 주요 개발자이다.

[2003년](https://ko.wikipedia.org/wiki/2003년 "wikilink") [1월 29일](https://ko.wikipedia.org/wiki/1월_29일 "wikilink"), 자이포포러스 (지금은 [Xiph.Org 재단이라](https://ko.wikipedia.org/wiki/Xiph.Org_재단 "wikilink") 불리고 있다. 자유 코덱, 자유 포맷 등을 개발하는 단체이다.) [Vorbis](https://ko.wikipedia.org/wiki/Vorbis "wikilink"), [Theora](https://ko.wikipedia.org/wiki/Theora "wikilink"), [Speex](https://ko.wikipedia.org/wiki/Speex "wikilink") 및 기타 등등과 마찬가지로, 그들의 목록에 FLAC도 편입한다고 발표하였다.\[4\]

## FLAC 프로젝트

FLAC 프로젝트는 다음과 같은 것을 포함한다.

  - 스트림 포맷.
  - 스트림을 위한 단순한 [콘테이너 포맷](https://ko.wikipedia.org/wiki/콘테이너_포맷 "wikilink"). 단순히 FLAC이라고 불린다. (혹은 Native FLAC이라고 불린다.)
  - libFLAC, 인코더와 디코더를 위한 레퍼런스 라이브러리. 메타데이터 인터페이스 포함.
  - libFLAC++, libFLAC 의 "객체 지향" 래퍼(wrapper).
  - flac, libFLAC에 대한 명령행(command-line) 래퍼(wrapper). 또한 FLAC 스트림을 디코드할 수 있다.
  - metaflac, 명령행(command-line) 메타데이터 편집기. .flac 파일을 편집할 수 있다. [리플레이 게인](https://ko.wikipedia.org/wiki/리플레이_게인 "wikilink")(Replay Gain)을 적용시킬 수도 있다.
  - 여러 음악 재생기에 대한 입력 플러그인(input plugins) ([AIMP](https://ko.wikipedia.org/wiki/AIMP "wikilink"),[윈앰프](../Page/윈앰프.md "wikilink"), [XMMS](https://ko.wikipedia.org/wiki/XMMS "wikilink"), [foobar2000](https://ko.wikipedia.org/wiki/foobar2000 "wikilink"), [musikCube](https://ko.wikipedia.org/wiki/musikCube "wikilink") 등등 )
  - Xiph.org에 편입된 후, [Ogg](../Page/Ogg.md "wikilink") 콘테이너 포맷. 스트리밍에 알맞음. (다른 말로 Ogg FLAC)

"자유"란 말은 스트림 포맷 제작자의 허락 없이 누구나 그 포맷을 구현할 수 있다는 말이자, (Xiph.org가 FLAC 스펙의 권리를 보유하고 있다. 또한 호환성을 인증할 권리를 보유하고 있다.) 어떤 특허도 FLAC 포맷 및 인코드/디코드 방법을 커버하고 있지 않다는 말이다. 또한, 레퍼런스 구현이 [자유 소프트웨어이라는](https://ko.wikipedia.org/wiki/자유_소프트웨어 "wikilink") 뜻도 된다. libFLAC 및 libFLAC++ 의 소스는 Xiph.org의 [BSD 사용 허가서](https://ko.wikipedia.org/wiki/BSD_사용_허가서 "wikilink") 하에서 배포된다. flac, metaflac 및 플러그인의 소스는 [GNU 일반 공중 사용 허가서](https://ko.wikipedia.org/wiki/GNU_일반_공중_사용_허가서 "wikilink") 하에서 배포된다.

프로젝트 목적에 대한 글에서 언급되었는 바, FLAC 프로젝트 내에서는 개발자들이 복사 방지 기능을 구현해 넣지 않는 것을 장려하고 있다.\[5\]

## 비교

FLAC은 오디오 데이터의 효율적인 압축을 위해 특수하게 설계되었다. 일반적인 무손실 압축 방식인 [ZIP](https://ko.wikipedia.org/wiki/ZIP_파일_포맷 "wikilink") 및 [gzip](https://ko.wikipedia.org/wiki/gzip "wikilink")과는 다르다. CD 품질의 오디오에 대하여, ZIP은 10 - 20%의 압축률을 보여주나, FLAC은 대개 30 - 50% 압축률을 보여준다. 보통의 음악에 경우 그러한데, 목소리 녹음의 경우에는 압축률이 더 올라간다. 비트 레이트는 약 800 - 950 kbit/s이다.

손실 압축 코덱(Lossy codecs)은 80% 이상의 압축률을 보여준다. 원본 스트림의 데이터를 까먹기 때문이다. FLAC은 [선형 예측](https://ko.wikipedia.org/wiki/선형_예측 "wikilink") 방법을 사용하는데, 오디오 샘플을 작고, 상관 관계가 없는 값들 (나머지라 부른다)의 수열로 변환한다. 이 수열은 [골롬-라이스 코딩](https://ko.wikipedia.org/wiki/골롬_코딩 "wikilink") (Golomb-Rice coding)을 사용하여 효율적으로 저장될 수 있다. 또한 FLAC은 소리 없는 구간 등 동일한 샘플의 블록들에 대해 [반복 길이 부호화를](https://ko.wikipedia.org/wiki/반복_길이_부호화 "wikilink") 사용한다. 다른 무손실 압축 코덱과 비교하면, FLAC은 스트림 가능한 것이 특징이다. 또한 FLAC의 디코딩 시간은 비교적 빠른 축에 속하는데, 이것은 압축 레벨과 관계없다.

다른 무손실 압축 방식과 마찬가지로, FLAC은 [콤팩트 디스크](https://ko.wikipedia.org/wiki/콤팩트_디스크 "wikilink") 등의 미디어 소유자가 소장하고 있는 오디오 작품을 장기간 보존하는 데 있어서, 매우 널리 쓰이는 포맷이다. 원본 미디어는 세월이 지나, 분실, 손상 등이 될 수 있지만, FLAC으로 복제된 오디오는 언제든 정확히 원본 미디어의 오디오 데이터와 동일하게 복구될 수 있다. MP3과 같은 손실 있는 코덱으로 압축된 데이터는 원본 미디어의 오디오 데이터와 동일하게 복구될 수 없다. CD를 [리핑](https://ko.wikipedia.org/wiki/리핑 "wikilink")할 때 선택적으로 [큐 시트 (음악 소프트웨어](https://ko.wikipedia.org/wiki/큐_시트_\(음악_소프트웨어 "wikilink")(.CUE 파일)을 생성할 수 있다. CD를 FLAC으로 완전히 리핑해두었다가, 훗날 이 CUE 파일의 도움을 받아 정확히 동일한 CD를 구워낼 수 있다. 트랙 순서, [프리갭](https://ko.wikipedia.org/wiki/프리갭 "wikilink"), [CD-Text](https://ko.wikipedia.org/wiki/CD-Text "wikilink") 등을 정확하게 복원할 수 있다. 하지만 일부 오디오 CD에 들어 있는 가사, [CD+G](../Page/CD+G.md "wikilink") 그래픽스 등은 CUE 파일 및 대부분의 CD 리핑 애플리케이션의 범위 밖이며, 정확히 원본대로 복원시킬 수 없다.

[유럽 방송 연합](https://ko.wikipedia.org/wiki/유럽_방송_연합 "wikilink") (EBU)은 유로라디오(Euroradio) 네트웍에서 고품질의 오디오를 배포하는 데 FLAC 포맷을 사용하기로 하였다.

하이드로젠오디오 위키(Hydrogenaudio Wiki)에 무손실 코덱간 비교표\[6\] 가 있다.

## 기술적 상세

FLAC은 [부동 소수점을](https://ko.wikipedia.org/wiki/부동_소수점 "wikilink") 지원하는 것이 아니라 오직 [고정 소수점만](https://ko.wikipedia.org/wiki/고정_소수점 "wikilink") 지원한다. 4내지 32 [비트](https://ko.wikipedia.org/wiki/비트_\(단위\) "wikilink") 샘플 크기를 지닌 [PCM](https://ko.wikipedia.org/wiki/PCM "wikilink")을 처리할 수 있으며, 샘플링 레이트는 1 [헤르츠](https://ko.wikipedia.org/wiki/헤르츠 "wikilink") 내지 1,048,570 Hz까지 1 Hz 단위로 처리할 수 있으며, 1 내지 8 채널을 처리할 수 있다. 채널은 [스테레오](../Page/스테레오.md "wikilink")나 5.1 채널 [서라운드 사운드처럼](https://ko.wikipedia.org/wiki/서라운드_사운드 "wikilink") 묶일 수 있는데, 채널간 상관 관계(correlation)을 이용하여 압축률을 높일 수 있다. 스트리밍 프로토콜에서 사용될 경우, FLAC은 [CRC](https://ko.wikipedia.org/wiki/순환_중복_검사 "wikilink") 첵섬을 사용하여, 잘못된 프레임을 골라낸다. 또한 그것의 STREAMINFO 메타데이터 헤더 내에 "본디 PCM"의 완전한 [MD5](../Page/MD5.md "wikilink") 해시값도 갖고 있다.

FLAC의 라이스 파라미터(Rice parameter)는 0-16이다. 최대 8 채널의 오디오, 최대 192kHz까지의 다양한 샘플링 레이트, 다양한 비트-퍼-샘플 너비를 지원한다. FLAC은 또한 [리플레이 게인을](https://ko.wikipedia.org/wiki/리플레이_게인 "wikilink") 지원한다.

FLAC은 libFLAC 코어 인코더 & 디코더 라이브러리로서 구현되었다. libFLAC API을 사용하는 레퍼런스 프로그램으로서 *flac*이라는 프로그램이 같이 들어있다. 이 [코덱](../Page/코덱.md "wikilink") API는 libFLAC++이라는 이름으로 C++ 버전으로서 존재한다.

FLAC의 레퍼런스 구현은 수많은 플랫폼 상에서 컴파일된다. 대부분의 [유닉스](https://ko.wikipedia.org/wiki/유닉스 "wikilink") ([솔라리스](https://ko.wikipedia.org/wiki/솔라리스_\(운영_체제\) "wikilink") 등), [유닉스 계통](https://ko.wikipedia.org/wiki/유닉스_계통 "wikilink") ([리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink"), [OS X](https://ko.wikipedia.org/wiki/OS_X "wikilink"), [BSD](https://ko.wikipedia.org/wiki/BSD "wikilink") 포함), [마이크로소프트 윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink"), [BeOS](https://ko.wikipedia.org/wiki/BeOS "wikilink"), [OS/2](https://ko.wikipedia.org/wiki/OS/2 "wikilink") 운영 체제에서 빌드된다. [Autoconf](https://ko.wikipedia.org/wiki/Autoconf "wikilink")/ [Automake](../Page/Automake.md "wikilink"), [MSVC](https://ko.wikipedia.org/wiki/MSVC "wikilink"), [Watcom C](https://ko.wikipedia.org/wiki/Watcom "wikilink"), [Xcode](https://ko.wikipedia.org/wiki/Xcode "wikilink") 등을 위한 빌드 시스템이 갖추어져 있다.

태깅(tagging) 기능을 위해, FLAC은 [보비스 코멘트와](https://ko.wikipedia.org/wiki/보비스_코멘트 "wikilink") 똑같은 시스템을 사용한다.\[7\]

## API 구성

libFLAC API는 기본 FLAC 비트스트림(bitstream)을 더 추상화한 것으로서, 스트림(stream), 건너뛰기 가능한 스트림(seekable stream), 파일(file)로 구성된다. 대부분의 FLAC 애플리케이션은 libFLAC을 이용하되 파일 레벨 인터페이스를 이용한다.

## FLAC을 지원하는 소프트웨어

### 인코딩

  - [크로스 플랫폼](https://ko.wikipedia.org/wiki/크로스_플랫폼 "wikilink")
      - [카카오인코더](https://ko.wikipedia.org/wiki/카카오인코더 "wikilink")\[8\]
      - [FFmpeg](https://ko.wikipedia.org/wiki/FFmpeg "wikilink")
      - [Flake](https://ko.wikipedia.org/wiki/Flake "wikilink")\[9\]
      - [Audacity 1.3.3 Beta](https://ko.wikipedia.org/wiki/Audacity "wikilink") 네이티브 FLAC 지원 기능이 막 포함되었다.
      - [VLC 미디어 플레이어](https://ko.wikipedia.org/wiki/VLC_미디어_플레이어 "wikilink") 0.8.6a
      - [Juce](https://ko.wikipedia.org/wiki/Juce "wikilink")
      - [aTunes](https://ko.wikipedia.org/wiki/aTunes "wikilink")
  - [마이크로소프트 윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink")
      - [AIMP](https://ko.wikipedia.org/wiki/AIMP "wikilink")
      - [Ease Audio Converter](https://ko.wikipedia.org/wiki/Ease_Audio_Converter "wikilink")
      - [Easy Media Creator](https://ko.wikipedia.org/wiki/Easy_Media_Creator "wikilink")
      - [Easy CD-DA Extractor](https://ko.wikipedia.org/wiki/Easy_CD-DA_Extractor "wikilink")
      - [Nero Burning ROM](https://ko.wikipedia.org/wiki/Nero_Burning_ROM "wikilink"). 선택적인 외부 필터 플러그-인 사용.
      - [dBpoweramp Music Converter](https://ko.wikipedia.org/wiki/DBpoweramp "wikilink"). 공식 코덱(official codec) 사용.
      - [MediaMonkey](https://ko.wikipedia.org/wiki/MediaMonkey "wikilink")
      - [윈앰프](../Page/윈앰프.md "wikilink"). 네이티브 FLAC 지원 기능이 막 포함되었다.
      - [JetAudio](https://ko.wikipedia.org/wiki/JetAudio "wikilink")
      - [foobar2000](https://ko.wikipedia.org/wiki/foobar2000 "wikilink") - 공식 외부 인코더(official external encoder) 사용.
      - [Sound Normalizer](http://www.kanssoftware.com/)
      - [MP3 Stream Editor](https://ko.wikipedia.org/wiki/MP3_Stream_Editor "wikilink") - 공식 외부 인코더 사용.
      - [Omni Encoder](https://ko.wikipedia.org/wiki/Omni_Encoder "wikilink") - 공식 외부 인코더 사용.
      - [Burrrn](https://ko.wikipedia.org/wiki/Burrrn "wikilink")
      - [Flac Frontend](https://ko.wikipedia.org/wiki/Flac_Frontend "wikilink")
      - [Total Audio Converter](https://ko.wikipedia.org/wiki/Total_Audio_Converter "wikilink")
      - [Yahoo\! Music Jukebox](https://ko.wikipedia.org/wiki/Yahoo!_Music_Jukebox "wikilink")
  - [macOS](https://ko.wikipedia.org/wiki/macOS "wikilink")
      - [Toast](https://ko.wikipedia.org/wiki/Toast_\(software\) "wikilink") 타이태니엄. 버전 7부터 지원.
      - [xACT](https://ko.wikipedia.org/wiki/xACT_\(X_Audio_Compression_Toolkit\) "wikilink") - 마이크로소프트의 XACT 오디오 프로그래밍 라이브러리와 혼동하지 말 것.
      - [Max](https://ko.wikipedia.org/wiki/Max_\(ripping_software\) "wikilink")

### 디코딩

  - [크로스 플랫폼](https://ko.wikipedia.org/wiki/크로스_플랫폼 "wikilink")
      - [FFmpeg](https://ko.wikipedia.org/wiki/FFmpeg "wikilink")
      - [aTunes](https://ko.wikipedia.org/wiki/aTunes "wikilink")
      - [Audacity 1.3.3 Beta](https://ko.wikipedia.org/wiki/Audacity "wikilink") [Audacity](https://ko.wikipedia.org/wiki/Audacity "wikilink")
      - [JUCE](https://ko.wikipedia.org/wiki/JUCE "wikilink") (크로스-플랫폼 C++ 툴킷. FLAC 지원 자체 내장.)
      - [린](https://ko.wikipedia.org/wiki/린_프로덕츠 "wikilink") 디지털 스트림 플레이어즈
      - [엠플레이어](https://ko.wikipedia.org/wiki/엠플레이어 "wikilink")
      - [송버드](https://ko.wikipedia.org/wiki/송버드 "wikilink")
      - [Squeezebox](https://ko.wikipedia.org/wiki/Squeezebox_\(network_music_player\) "wikilink")
      - [The Core Pocket Media Player](https://ko.wikipedia.org/wiki/The_Core_Pocket_Media_Player "wikilink") - flac 플러그인 사용.
      - [VLC 미디어 플레이어](https://ko.wikipedia.org/wiki/VLC_미디어_플레이어 "wikilink")
      - [Total Audio Converter](https://ko.wikipedia.org/wiki/Total_Audio_Converter "wikilink")
  - [macOS](https://ko.wikipedia.org/wiki/macOS "wikilink")
      - macOS 내장 기본 Quicktime Player (macOS 10.13 이상)
      - [Cog](http://cogx.org/): 오픈 소스
      - [xACT](https://ko.wikipedia.org/wiki/xACT_\(X_Audio_Compression_Toolkit\) "wikilink") - 마이크로소프트의 XACT 오디오 프로그래밍 라이브러리와 혼동하지 말 것.
      - [VOX](http://coppertino.com/): 무료 앱. 이 밖에 다양한 [오디오 데이터 압축](https://ko.wikipedia.org/wiki/오디오_데이터_압축 "wikilink") [파일 형식도](https://ko.wikipedia.org/wiki/파일_형식 "wikilink") 지원한다.
  - [마이크로소프트 윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink")
      - 기본 Windows Media Player (윈도우10 이상)
      - [이스트소프트](../Page/이스트소프트.md "wikilink") - [알송](../Page/알송.md "wikilink")
      - [곰앤컴퍼니](https://ko.wikipedia.org/wiki/곰앤컴퍼니 "wikilink") - [곰오디오](https://ko.wikipedia.org/wiki/곰오디오 "wikilink")
      - [AIMP](https://ko.wikipedia.org/wiki/AIMP "wikilink")
      - [Ease Audio Converter](https://ko.wikipedia.org/wiki/Ease_Audio_Converter "wikilink")
      - [foobar2000](https://ko.wikipedia.org/wiki/foobar2000 "wikilink")
      - [Cirlinca DVD-AUDIO Solo](https://web.archive.org/web/20180522115959/http://www.cirlinca.com/) - FLAC을 가져와 DVD-오디오 디스크를 구울 수 있다.
      - [JetAudio](https://ko.wikipedia.org/wiki/JetAudio "wikilink")
      - [KSP Sound Player](https://ko.wikipedia.org/wiki/KSP_Sound_Player "wikilink") - 일반 설치 내용이 포함하고 있는 플러그인 사용.
      - [MediaMonkey](https://ko.wikipedia.org/wiki/MediaMonkey "wikilink")
      - [Mixmeister Fusion](https://ko.wikipedia.org/wiki/Mixmeister_Fusion "wikilink")
      - [MP3 Stream Editor](https://ko.wikipedia.org/wiki/MP3_Stream_Editor "wikilink") - 일반 설치 내용이 포함하고 있는 플러그인 사용.
      - 콕코스 [REAPER](https://ko.wikipedia.org/wiki/REAPER "wikilink") 멀티트랙 레코더 및 에디터
      - [Quintessential Player](https://ko.wikipedia.org/wiki/Quintessential_Player "wikilink") - flac 플러그인 사용.
      - [The KMPlayer](https://ko.wikipedia.org/wiki/The_KMPlayer "wikilink")
      - [TRAKTOR 3](https://ko.wikipedia.org/wiki/Traktor_DJ_Studio "wikilink")
      - [TRAKTOR Scratch](https://ko.wikipedia.org/wiki/Traktor_DJ_Studio "wikilink")
      - [윈앰프](../Page/윈앰프.md "wikilink")
      - [XMPlay](../Page/XMPlay.md "wikilink")
      - [FairStars Audio Converter](https://ko.wikipedia.org/wiki/FairStars_Audio_Converter "wikilink")
  - [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink")
      - [Audacious](https://ko.wikipedia.org/wiki/Audacious_Media_Player "wikilink")
      - [Banshee (music player)](https://ko.wikipedia.org/wiki/Banshee_\(music_player\) "wikilink")
      - [Baudline](https://ko.wikipedia.org/wiki/Baudline "wikilink")
      - [cmus](https://ko.wikipedia.org/wiki/cmus "wikilink")
      - [mpd](https://ko.wikipedia.org/wiki/MPD_\(Music_Player\) "wikilink")
      - [ogg123](https://ko.wikipedia.org/wiki/ogg123 "wikilink") (단, flac을 사용하도록 컴파일 되었다면. ogg123은 'vorbis-tools' 패키지의 일부이다.)
      - [Xine](https://ko.wikipedia.org/wiki/Xine "wikilink")
      - [XMMS](https://ko.wikipedia.org/wiki/XMMS "wikilink")
      - [그놈](https://ko.wikipedia.org/wiki/그놈 "wikilink")
          - [그놈베이커](https://ko.wikipedia.org/wiki/그놈베이커 "wikilink")
          - [리듬박스](https://ko.wikipedia.org/wiki/리듬박스 "wikilink")
          - [토템 무비 플레이어](https://ko.wikipedia.org/wiki/토템_\(미디어_플레이어\) "wikilink")
          - [Serpentine](https://ko.wikipedia.org/wiki/Serpentine_\(software\) "wikilink")
      - [KDE](https://ko.wikipedia.org/wiki/KDE "wikilink")
          - [아마록](https://ko.wikipedia.org/wiki/아마록 "wikilink")
          - [Audiokonverter](http://www.kde-apps.org/content/show.php?content=12608/) (콘텍스트 메뉴 팝-업으로부터)

<!-- end list -->

  - 모바일
      - iOS: iOS11 이상, 아이폰7 이상
      - 안드로이드

### 리핑

  - [크로스 플랫폼](https://ko.wikipedia.org/wiki/크로스_플랫폼 "wikilink")
      - [aTunes](https://ko.wikipedia.org/wiki/aTunes "wikilink")
  - 윈도
      - [BonkEnc](https://ko.wikipedia.org/wiki/BonkEnc "wikilink") - FLAC.dll API 사용.
      - [CD to MP3 Maker](https://ko.wikipedia.org/wiki/CD_to_MP3_Maker "wikilink")
      - [CDex](https://ko.wikipedia.org/wiki/CDex "wikilink") - 외부 인코더 사용 옵션. (flac이 설치되어 있다면, 이제, "flac.dll"을 인코더 옵션으로 나열해줌.)
      - [DBpoweramp](https://ko.wikipedia.org/wiki/DBpoweramp "wikilink")
      - [Easy CD-DA Extractor](https://ko.wikipedia.org/wiki/Easy_CD-DA_Extractor "wikilink")
      - [이그잭트 오디오 카피](../Page/이그잭트_오디오_카피.md "wikilink") - 외부 인코더 사용.
      - [Foobar2000](../Page/Foobar2000.md "wikilink") - 컨버터 플러그인과 외부 인코더 사용.
      - [AIMP](https://ko.wikipedia.org/wiki/AIMP "wikilink") - 플러그인 및 내장 인코더 사용.
      - [MediaMonkey](https://ko.wikipedia.org/wiki/MediaMonkey "wikilink")
      - [MP3 스트림 에디터](https://ko.wikipedia.org/wiki/MP3_스트림_에디터 "wikilink") - 공식 외부 인코더 사용 (싱글 모드/앨범 모드/풀 앨범 아트 지원)
      - [젯오디오](https://ko.wikipedia.org/wiki/젯오디오 "wikilink")
      - [윈앰프](../Page/윈앰프.md "wikilink")
      - [PlexTools](https://ko.wikipedia.org/wiki/PlexTools "wikilink")
      - [Yahoo\! Music Jukebox](https://ko.wikipedia.org/wiki/Yahoo!_Music_Jukebox "wikilink")
  - OS X
      - [Max](https://ko.wikipedia.org/wiki/Max_\(ripping_software\) "wikilink") ([맥 오에스 10.4](https://ko.wikipedia.org/wiki/맥_오에스_10.4 "wikilink") 혹은 그 이상)
  - 리눅스
      - [ABCDE](https://ko.wikipedia.org/wiki/ABCDE "wikilink")
      - [Banshee (music player)](https://ko.wikipedia.org/wiki/Banshee_\(music_player\) "wikilink")
      - [Cdda2wav](https://ko.wikipedia.org/wiki/Cdda2wav "wikilink")
      - [Cdparanoia](https://ko.wikipedia.org/wiki/Cdparanoia "wikilink")
      - [Mencoder](https://ko.wikipedia.org/wiki/Mencoder "wikilink")
      - [RipIt](https://web.archive.org/web/20080226040110/http://www.suwald.com/ripit/ripit.html) (명령줄 툴)
      - GNOME
          - [Grip](https://ko.wikipedia.org/wiki/Grip_audio_ripper "wikilink")
          - [RipOff](https://ko.wikipedia.org/wiki/RipOff "wikilink")
          - [Sound Juicer](https://ko.wikipedia.org/wiki/Sound_Juicer "wikilink")
      - KDE
          - [K3b](https://ko.wikipedia.org/wiki/K3b "wikilink")
          - [KAudioCreator](https://ko.wikipedia.org/wiki/KAudioCreator "wikilink")
          - [Konqueror](https://ko.wikipedia.org/wiki/Konqueror "wikilink")

## 하드웨어

  - 마이크로소프트 [엑스박스](https://ko.wikipedia.org/wiki/엑스박스 "wikilink") - 단, 서드 파티 [Xbox Media Center를](https://ko.wikipedia.org/wiki/Xbox_Media_Center "wikilink") 구동해야 함.
  - [아이팟](https://ko.wikipedia.org/wiki/아이팟 "wikilink") - 비디오, 나노, 포토, 컬러, 미니 (2세대). 단, 서드 파티 [락박스](https://ko.wikipedia.org/wiki/락박스 "wikilink") 펌웨어를 사용해야 함.
  - (거의 대부분의) [락박스](https://ko.wikipedia.org/wiki/락박스 "wikilink")-호환 디지털 오디오 플레이어 - [아이리버](https://ko.wikipedia.org/wiki/아이리버 "wikilink"), [기가비트](https://ko.wikipedia.org/wiki/기가비트 "wikilink") ([도시바](../Page/도시바.md "wikilink")), 앞에서 얘기한 아이팟 포함.
  - [Escient](https://ko.wikipedia.org/wiki/Escient "wikilink")\[10\]
  - [iAudio](https://ko.wikipedia.org/wiki/iAudio "wikilink") - [코원시스템](../Page/코원시스템.md "wikilink")의 디지털 오디오 플레이어. 4, 5, 6, 7, F2, M3, M5, X5, U2, U3, A2, A3, D2, O2, S9. 새 버전의 펌웨어는 자체 지원.
  - [올리브 미디어 프로덕츠](https://ko.wikipedia.org/wiki/올리브_미디어_프로덕츠 "wikilink") (Symphony, Musica, Opus)\[11\]
  - [PhatBox](https://ko.wikipedia.org/wiki/PhatBox "wikilink") 하드 드라이브 내장 자동차 디지털 미디어 플레이어, 팻노이즈(PhatNoise) 사 판매.
  - [Rio Karma](https://ko.wikipedia.org/wiki/Rio_Karma "wikilink")
  - [Squeezebox network music player](https://ko.wikipedia.org/wiki/Squeezebox_network_music_player "wikilink") (v1 버전에서는 서버 측에서 [PCM](https://ko.wikipedia.org/wiki/PCM "wikilink")으로 트랜스코드한다. v2 및 그 이상의 버전에서는Squeezebox에서 자체 지원한다.)
  - [Sonos](https://ko.wikipedia.org/wiki/Sonos "wikilink")
  - Meizu [M6 Mini Player](https://ko.wikipedia.org/wiki/M6_Mini_Player "wikilink"), M3 Music Card
  - [Pixel Magic Systems](https://ko.wikipedia.org/wiki/Pixel_Magic_Systems "wikilink")' HD Mediabox (펌웨어 버전 1.3.4 이상)
  - Embedded Waveplayer- Module with FLAC level 0-2 support, MIDI and serial interface
  - 텍라스트 T29, T39, C260, C280, C290
  - [Trekstor Vibez](https://ko.wikipedia.org/wiki/Trekstor_Vibez "wikilink")
  - 모든 UPnP A/V / DLNA 장치 - e.g. 넷기어 EVA700, 넷기어 MP101, Roku Soundbridge 혹은 Xbox 360 (TVersity와 같은 애플리케이션을 통해 트랜스코드되어 스트림될 때. 단, 이 애플리케이션은 ffdshow를 사용.)
  - Sound Devices 7-Series Professional Audio Recorders - 단, 뱃저(badger) 펌웨어 업데이트가 되었을 때(v.2.24)\[12\]
  - Denon AVR-4308 & AVR-3808 AV 리시버\[13\]
  - T+A Music Player\[14\]
  - [린](https://ko.wikipedia.org/wiki/린_프로덕츠 "wikilink") 클라이막스 DS 디지털 뮤직 플레이어

## 같이 보기

  - [멍키 오디오](https://ko.wikipedia.org/wiki/멍키_오디오 "wikilink")
  - [TTA](https://ko.wikipedia.org/wiki/TTA_\(코덱\) "wikilink")
  - [WavPack](https://ko.wikipedia.org/wiki/WavPack "wikilink")

## 각주

<references/>

## 외부 링크

  - [공식 웹사이트](http://flac.sourceforge.net/)
  - [무손실 포맷 비교](https://web.archive.org/web/20090703042443/http://web.inter.nl.net/users/hvdh/lossless/lossless.htm) -  작성. (약간 오래된 정보)

[분류:오디오 코덱](https://ko.wikipedia.org/wiki/분류:오디오_코덱 "wikilink") [분류:자유 멀티미디어 코덱](https://ko.wikipedia.org/wiki/분류:자유_멀티미디어_코덱 "wikilink") [분류:무손실 압축 알고리즘](https://ko.wikipedia.org/wiki/분류:무손실_압축_알고리즘 "wikilink") [분류:무손실 오디오 코덱](https://ko.wikipedia.org/wiki/분류:무손실_오디오_코덱 "wikilink") [분류:오디오 파일 포맷](https://ko.wikipedia.org/wiki/분류:오디오_파일_포맷 "wikilink") [분류:2001년 소프트웨어](https://ko.wikipedia.org/wiki/분류:2001년_소프트웨어 "wikilink") [분류:오픈 포맷](https://ko.wikipedia.org/wiki/분류:오픈_포맷 "wikilink")

1.
2.  [FLAC 웹사이트](http://flac.sourceforge.net/links.html#hardware)
3.
4.
5.  [FLAC Website](http://flac.sourceforge.net/developers.html)
6.
7.
8.  [1](http://www.cacaotools.com/cacaoencoder)
9.  [Flake](http://flake-enc.sourceforge.net/)
10.
11.
12.
13.
14.