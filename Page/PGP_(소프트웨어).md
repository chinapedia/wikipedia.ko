> This article is converted from Wikipedia: [PGP \(\)](https://ko.wikipedia.org/wiki/PGP_\(\)).


**PGP**는 'Pretty Good Privacy'의 약자로서, 컴퓨터 파일을 [암호화](https://ko.wikipedia.org/wiki/암호화 "wikilink")하고 [복호화](https://ko.wikipedia.org/wiki/복호화 "wikilink")하는 프로그램이다. 1991년 [필립 짐머만이](https://ko.wikipedia.org/wiki/필립_짐머만 "wikilink") 개발하였으며, 현재 전 세계적으로 이메일 보안의 표준으로 자리잡았다.

## 전자서명

PGP로 [전자서명](../Page/전자서명.md "wikilink")을 할 수도 있다. 원본 파일을 작성하고, 그 파일에 대해 sig 파일을 생성하여 상대방에게 원본 파일과 sig 파일을 함께 배포하며, 상대방은 PGP를 이용해 sig 파일을 검증한다. sig 파일이 생성된 후에 원본 파일이 변경되었으면, sig 파일 검증시 Bad signature라고 출력된다.

1991년 개발된 PGP 프로그램을 이용한 [전자서명](../Page/전자서명.md "wikilink")은, 전 세계적으로 보편화 되어, 일반적으로 사용하지만, [대한민국 전자서명법상의](https://ko.wikipedia.org/wiki/대한민국_전자서명법 "wikilink") 보호를 받는 전자서명으로 인정받고 있지는 않다. [공인인증서](../Page/공인인증서.md "wikilink")만이 [대한민국 전자서명법에](https://ko.wikipedia.org/wiki/대한민국_전자서명법 "wikilink") 의해 인정받고 있다. PGP 전자서명은 무료인 반면에, 공인인증서 전자서명은 2011년 현재 1년 4,400원을 지불해야 한다.

## AES256

[위키리크스](https://ko.wikipedia.org/wiki/위키리크스 "wikilink")의 [줄리언 어산지는](../Page/줄리언_어산지.md "wikilink") 미국의 외교기밀문서를 압축하여 AES 256 비트 암호화를 하여 전 세계에 배포해, 자신이 형사처벌을 받으면 그 암호를 공개하겠다고 협박했다. PGP 프로그램을 통해 AES 256 비트 암호화와 복호화가 가능하다. [고급 암호화 표준](../Page/고급_암호화_표준.md "wikilink")(AES)는 미국 정부가 제정한 최신 암호화 기술이다.

미국 정부가 제정한 기존의 암호화 표준은 56비트 DES 암호 코드였다. 그러나 DES가 슈퍼컴퓨터를 사용하면 수시간내에 해독될 수 있게 되자, 256비트 키를 사용하는 차세대 표준 AES를 제정했다.

어산지가 배포한 파일 중 하나는 1.4기가바이트(GB) 용량인 insurance.aes256 인데, 영국 석유회사 BP와 관타나모 수용소 관련 기록 등을 담고 있는 것으로서, 슈퍼컴퓨터로도 해독에 수십년 이상이 걸리는 것으로 알려졌다.\[1\]\[2\]\[3\]

## GnuPG

PGP는 [GNU](https://ko.wikipedia.org/wiki/GNU "wikilink") 프로젝트의 하나인 [그누 프라이버시 가드로도](https://ko.wikipedia.org/wiki/그누_프라이버시_가드 "wikilink") 개발되어, 전 세계적으로 광범위하게 사용되고 있다.

## 각주

## 같이 보기

  - [GNU 프라이버시 가드](https://ko.wikipedia.org/wiki/GNU_프라이버시_가드 "wikilink")
  - [트루크립트](https://ko.wikipedia.org/wiki/트루크립트 "wikilink")
  - [프리넷](https://ko.wikipedia.org/wiki/프리넷 "wikilink")

[분류:암호학사](https://ko.wikipedia.org/wiki/분류:암호학사 "wikilink") [분류:암호 소프트웨어](https://ko.wikipedia.org/wiki/분류:암호_소프트웨어 "wikilink") [분류:1991년 소프트웨어](https://ko.wikipedia.org/wiki/분류:1991년_소프트웨어 "wikilink") [분류:인터넷 프라이버시 소프트웨어](https://ko.wikipedia.org/wiki/분류:인터넷_프라이버시_소프트웨어 "wikilink") [분류:프라이버시 소프트웨어](https://ko.wikipedia.org/wiki/분류:프라이버시_소프트웨어 "wikilink") [분류:OpenPGP](https://ko.wikipedia.org/wiki/분류:OpenPGP "wikilink") [분류:암호화 토론](https://ko.wikipedia.org/wiki/분류:암호화_토론 "wikilink")

1.  <http://news.naver.com/main/read.nhn?mode=LSD&mid=sec&sid1=104&oid=015&aid=0002355621>
2.  <http://news.naver.com/main/read.nhn?mode=LSD&mid=sec&sid1=104&oid=025&aid=0002111116>
3.  <http://news.naver.com/main/read.nhn?mode=LSD&mid=sec&sid1=104&oid=081&aid=0002141892>