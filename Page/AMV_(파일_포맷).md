> This article is converted from Wikipedia: [AMV \(파일 포맷\)](https://ko.wikipedia.org/wiki/AMV_\(파일_포맷\)).


**AMV**는 [S1 MP3 플레이어와](../Page/S1_MP3_플레이어.md "wikilink") 같은 [MP4 플레이어에서](../Page/MP4_플레이어.md "wikilink") 재생하기 위해 만들어진 [사유](https://ko.wikipedia.org/wiki/사유_소프트웨어 "wikilink") [멀티미디어](../Page/멀티미디어.md "wikilink") [컨테이너 포맷이다](https://ko.wikipedia.org/wiki/컨테이너_포맷_\(디지털\) "wikilink"). 두 가지의 다른 MTV 포맷이 존재하는데 하나는 액션 칩셋에서 구동하기 위해 만들어졌으며, 다른 하나는 ALi M5661칩셋에서 구동할 수 있도록 만들어졌다. ALi 칩셋용 포맷은 ALIAVI이다.

## 형식

이 미디어 컨테이너는 [AVI](../Page/오디오_비디오_인터리브.md "wikilink") 컨테이너 형식의 수정판이다.\[1\] 영상 포맷은 [모션 JPEG의](https://ko.wikipedia.org/wiki/모션_JPEG "wikilink") 변형으로, [양자화](https://ko.wikipedia.org/wiki/양자화_\(이미지\) "wikilink") 테이블이 수정되어 있다.\[2\] 음성 포맷의 경우 IMA의 [적응 차분 펄스 부호 변조를](https://ko.wikipedia.org/wiki/적응_차분_펄스_부호_변조 "wikilink") 사용하였으며, 대부분의 AMV파일은 22050Hz의 샘플링레이트로 작동한다.\[3\]

디코더 오버헤드는 저사양 프로세서를 갖춘 S1 MP3 플레이어에 적합하도록 낮게 설계되었다. 영상 압축율과 해상도, 프레임율이 매우 낮으며(4px/바이트, 96x96\~208x176, 10\~16fps)\[4\], 파일의 크기 또한 바이트/초 수준으로 매우 낮으므로, 128x96의 해상도를 갖춘 12fps의 30분 짜리 영상이 약 80MB정도로 압축된다.

## 문서

이 포맷에 관한 문서는 아직 공개되지 않았으나, Dobrica Pavlinušić이 포맷을 [풀어내어](../Page/리버스_엔지니어링.md "wikilink")\[5\] Perl에 기반한 디코더를 만들어내었으며\[6\] Pavlinušić, Tom Van Braeckel 과 Vladimir Voroshilov가 AMV파일을 사용할 수 있는 [FFmpeg](../Page/FFmpeg.md "wikilink")를 만들어냈다\[7\]. AMV 포맷의 코드는 FFmpeg 프로젝트에 보내졌다\[8\].

## 각주

<references/>

## 외부 링크

  - [All about AMV file format](http://wiki.multimedia.cx/index.php?title=AMV) (멀티미디어 위키)

  - [Bytessence AMV Converter](http://www.bytessence.com/bmpxc.html)<small>([FFmpeg](../Page/FFmpeg.md "wikilink")기반의 [오픈 소스](../Page/오픈_소스.md "wikilink") AMV 컨버터)</small>

[분류:파일 포맷](https://ko.wikipedia.org/wiki/분류:파일_포맷 "wikilink")

1.
2.  [forcing mjpegenc to use fixed quantisation tables](http://lists.mplayerhq.hu/pipermail/ffmpeg-devel/2007-October/037336.html) (Tom Van Braeckel, FFmpeg-devel mailing list, 28 October 2007)
3.
4.
5.
6.  [AMV free decoder](http://blog.rot13.org/2007/08/amv_free_decoder_works.html) (Dobrica Pavlinušić, personal blog, 19 August 2007)
7.  [amv-codec-tools](http://code.google.com/p/amv-codec-tools/) ([Google Code](https://ko.wikipedia.org/wiki/Google_Code "wikilink"))
8.  [What needs to be done - this is an asynchronous meeting by mailing list.](http://groups.google.com/group/amv-codec-tools/browse_thread/thread/3afc2809797c1109) (Tom Van Braeckel, AMV codec tools group mailing list, 26 October 2007)