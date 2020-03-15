> This article is converted from Wikipedia: [Cksum](https://ko.wikipedia.org/wiki/Cksum).


**cksum**은 [유닉스 계열](https://ko.wikipedia.org/wiki/유닉스_계열 "wikilink") 운영 체제의 [명령어](https://ko.wikipedia.org/wiki/명령어 "wikilink")의 하나로, 파일이나 데이터 스트림의 [체크섬](https://ko.wikipedia.org/wiki/체크섬 "wikilink") 값을 만들어준다. cksum 명령어는 변수에 지정된 각 파일을 읽으며 변수가 지정되지 않으면 [표준 입력을](https://ko.wikipedia.org/wiki/표준_스트림 "wikilink") 읽는데, 출력은 파일의 [CRC](https://ko.wikipedia.org/wiki/순환_중복_검사 "wikilink") 체크섬과 [바이트](https://ko.wikipedia.org/wiki/바이트 "wikilink") 카운트로 표시된다.

`cksum` 명령어는 파일을 그대로 두었는지 신뢰할 수 없는 수단에 의해 변경되었는지 확인하는데 사용할 수 있다.\[1\] 그러나 cksum 명령어가 계산한 CRC 체크섬은 [암호학적으로 안전한](https://ko.wikipedia.org/wiki/암호화_해시_함수 "wikilink") 것은 아니다. 즉, "우연한" 손상에 대해 보호를 하지만(손상된 데이터가 의도된 데이터와 동일한 체크섬을 가질 가능성은 거의 없음) 공격자가 체크섬의 변동이 없는 방식으로 "의도적으로" 파일을 손상시키는 것은 어렵지 않다. 유닉스 계열 운영 체제는 일반적으로 [sha256sum](https://ko.wikipedia.org/wiki/sha256sum "wikilink")과 같은 암호학적으로 안전한 체크섬을 위한 기타 명령어들을 포함하고 있다.

## 알고리즘

cksum은 [다항식](https://ko.wikipedia.org/wiki/다항식_부호 "wikilink") 0x04C11DB7을 사용하며 [리틀 엔디언](https://ko.wikipedia.org/wiki/리틀_엔디언 "wikilink") 표현으로 길이를 메시지 뒤에 추가한다. 해당 길이는 오른쪽 끝으로 잘려나간 [널 바이트를](https://ko.wikipedia.org/wiki/널_바이트 "wikilink") 가진다.\[2\]

## 문법

``` bash
cksum [파일]...
cksum [옵션]
```

## 사용 예

``` console
$ cksum test.txt
4038471504 75 test.txt
```

여기에서 `4038471504`는 체크섬 값을, `75`은 `test.txt`의 파일 크기를 나타낸다.

## 같이 보기

  - [순환 중복 검사](https://ko.wikipedia.org/wiki/순환_중복_검사 "wikilink")
  - [GNU 코어 유틸리티](../Page/GNU_코어_유틸리티.md "wikilink")
  - [`md5sum`](https://ko.wikipedia.org/wiki/md5sum "wikilink")

## 각주

## 외부 링크

  -
[분류:체크섬 알고리즘](https://ko.wikipedia.org/wiki/분류:체크섬_알고리즘 "wikilink") [분류:표준 유닉스 프로그램](https://ko.wikipedia.org/wiki/분류:표준_유닉스_프로그램 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink")

1.
2.  <http://pubs.opengroup.org/onlinepubs/9699919799/utilities/cksum.html>