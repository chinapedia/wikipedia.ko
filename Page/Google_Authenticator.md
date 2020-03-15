> This article is converted from Wikipedia: [Google Authenticator](https://ko.wikipedia.org/wiki/Google_Authenticator).


| operating system = [안드로이드](https://ko.wikipedia.org/wiki/안드로이드_\(운영_체제\) "wikilink"), [IOS](https://ko.wikipedia.org/wiki/IOS "wikilink"), [블랙베리 OS](https://ko.wikipedia.org/wiki/블랙베리_OS "wikilink") | platform = 모바일 | size = | language = | language count = | language footnote = | genre = | license = 사유 (초기 버전은 [아파치 라이선스](https://ko.wikipedia.org/wiki/아파치_라이선스 "wikilink") 2.0) | alexa = | website = | standard = | AsOf = }}

**Google Authenticator**는 [시간 기반 일회용 비밀번호 알고리즘](https://ko.wikipedia.org/wiki/시간_기반_일회용_비밀번호_알고리즘 "wikilink")(TOTP)와 [HMAC 기반 일회용 비밀번호 알고리즘](https://ko.wikipedia.org/wiki/HMAC_기반_일회용_비밀번호_알고리즘 "wikilink")(HOTP)를 사용하여 [다요소 인증](../Page/다요소_인증.md "wikilink") 서비스를 구현하는 [소프트웨어 토큰의](https://ko.wikipedia.org/wiki/소프트웨어_토큰 "wikilink") 하나로, [구글](https://ko.wikipedia.org/wiki/구글 "wikilink")의 모바일 애플리케이션 사용자들을 인증하기 위해 사용된다. 이 서비스는 RFC 6238, RFC 4226에 규정된 알고리즘을 구현한다.\[1\]

Authenticator는 사용자 이름과 비밀번호 외에 지정해야 하는 6\~8자리의 [일회용 비밀번호를](https://ko.wikipedia.org/wiki/일회용_비밀번호 "wikilink") 제공하며 이를 통해 구글 서비스와 다른 사이트에 로그인할 수 있다. 이 Authenticator는 [패스워드 매니저나](https://ko.wikipedia.org/wiki/패스워드_매니저 "wikilink") [파일 호스팅 서비스와](https://ko.wikipedia.org/wiki/파일_호스팅_서비스 "wikilink") 같은 타사 애플리케이션에 대한 코드를 생성할 수 있다. 이전 버전의 소프트웨어는 [오픈 소스였으나](https://ko.wikipedia.org/wiki/오픈_소스_소프트웨어 "wikilink") 이후 릴리스는 [사유이다](https://ko.wikipedia.org/wiki/사유_소프트웨어 "wikilink").\[2\]

한국어 애플 앱 스토어에서는 "Google Authenticator"라는 소프트웨어 제목을 유지하며 한국어 플레이스토어에서는 "Google OTP"라는 이름이 사용된다.

## 구현체

구글은 [안드로이드](https://ko.wikipedia.org/wiki/안드로이드_\(운영_체제\) "wikilink")\[3\] [블랙베리](https://ko.wikipedia.org/wiki/블랙베리_\(스마트폰\) "wikilink"), [IOS](https://ko.wikipedia.org/wiki/IOS "wikilink")\[4\] 버전의 Authenticator를 제공한다. 일부 타사 구현체도 이용할 수 있다.

  - Windows Phone 7.5/8/8.1/10: Microsoft Authenticator\[5\] Virtual TokenFactor\[6\]
  - Windows Mobile: Google Authenticator for Windows Mobile\[7\]
  - Java CLI: Authenticator.jar\[8\]
  - Java GUI: JAuth\[9\] FXAuth\[10\]
  - J2ME: gauthj2me\[11\] lwuitgauthj2me\[12\] Mobile-OTP (중국어 전용)\[13\] totp-me\[14\]
  - Palm OS: gauthj2me\[15\]
  - Python: onetimepass\[16\], pyotp\[17\]
  - PHP: GoogleAuthenticator.php\[18\]
  - Ruby: rotp,\[19\] twofu\[20\]
  - Rails: active_model_otp\[21\] (서드파티 구현체)
  - webOS: GAuth\[22\]
  - Windows: gauth4win\[23\] MOS Authenticator\[24\] WinAuth\[25\]
  - .NET: TwoStepsAuthenticator\[26\]
  - HTML5: html5-google-authenticator\[27\]
  - MeeGo/Harmattan (노키아 N9): GAuth\[28\]
  - Sailfish OS: SGAuth,\[29\] SailOTP\[30\]
  - Apache: Google Authenticator Apache Module\[31\]
  - PAM: Google Pluggable Authentication Module\[32\] oauth-pam\[33\]
  - Backend: [LinOTP](https://ko.wikipedia.org/wiki/LinOTP "wikilink") (Management Backend implemented in python)
  - Chrome/Chrome OS: Authenticator\[34\]
  - iOS: OTP Auth\[35\]

<!-- end list -->

  - [privacyIDEA](https://ko.wikipedia.org/wiki/privacyIDEA "wikilink") Authentication System.

## 각주

## 외부 링크

  - [Google Authenticator](https://web.archive.org/web/20130302124735/http://support.google.com/a/bin/answer.py?hl=en&answer=1037451) on Google Help

  - [Google Authenticator (Android)](https://github.com/google/google-authenticator-android) and [Google Authenticator (other)](https://github.com/google/google-authenticator) legacy source code on [깃허브](https://ko.wikipedia.org/wiki/깃허브 "wikilink")

  - [Google Authenticator implementation in Python](https://stackoverflow.com/questions/8529265/google-authenticator-implementation-in-python) on [스택 오버플로 (웹사이트)](../Page/스택_오버플로_\(웹사이트\).md "wikilink")

  -
[분류:컴퓨터 접근 제어](https://ko.wikipedia.org/wiki/분류:컴퓨터_접근_제어 "wikilink") [Authenticator](https://ko.wikipedia.org/wiki/분류:구글의_서비스 "wikilink")

1.
2.  Willis, Nathan (22 January 2014)."*[FreeOTP multi-factor authentication](https://lwn.net/Articles/581086)*". *LWN.net*. Retrieved 10 August 2015.
3.  <https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2> A
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14.
15.
16.
17.
18.
19.
20.
21.
22.
23.
24.
25.
26.
27.
28.
29.
30.
31.
32.
33.
34.
35.