> This article is converted from Wikipedia: [Script \(유닉스\)](https://ko.wikipedia.org/wiki/Script_\(유닉스\)).


**script** 명령어는 [터미널](../Page/단말기.md "wikilink") 세션을 기록하는 [유닉스 유틸리티이다](../Page/유닉스_명령어_목록.md "wikilink").\[1\] *scriptreplay* 명령어는 script에 리플레이 기능을 제공한다.\[2\] 이 세션은 기본적으로 typescript라는 파일 이름으로 포착된다. 다른 파일 이름을 지정하려면 script 명령어 뒤에 공백을 두고 다음과 같이 파일 이름을 지정하면 된다: `script recorded_session`.

[ttyrec](https://ko.wikipedia.org/wiki/ttyrec "wikilink") 프로그램은 동일한 종류의 기능 외에 다른 몇 가지 바인딩을 제공한다.

기록된 셸 세션들은 온라인 서비스들을 사용하여 공유할 수 있다.\[3\] 일반적인 스크린캐스트로부터 이러한 형태로 기록된 세션을 사용할 때의 이점은 셸 명령들을 쉽게 플레이어 스크린에서 복사해서 붙여넣을 수 있다는 것이다.

## script 명령어의 대안

script 명령어의 문제점들 가운데 하나는 자식 프로세스의 로깅만을 허용한다는 것이다. 또, 새로운 프로세스를 스폰(spawn)하지 않고 현재의 프로세스의 명령을 로깅해야 할 수 있는데, 이를테면 자체 출력을 기록할 수 있는 스크립트의 자동화가 필요한 시점을 들 수 있다. [유닉스](../Page/유닉스.md "wikilink") 운영 체제는 파이프와 리다이렉트를 사용하여 이를 가능케 한다. 다음의 예들을 고려할 수 있다:

### 본 셸

[본 셸과](../Page/본_셸.md "wikilink") 관련되는 모든 셸([sh](../Page/톰프슨_셸.md "wikilink"), [bash](../Page/배시_\(유닉스_셸\).md "wikilink"), [ksh](../Page/콘_셸.md "wikilink"))들은 stdout과 stderr이 [지명 파이프에](../Page/명명된_파이프.md "wikilink") 부착되도록 할 수 있으며 [tee 명령어로](https://ko.wikipedia.org/wiki/tee_\(명령어\) "wikilink") 리다이렉트가 가능하게 할 수 있다.

**예**

``` bash
LOGNAME="script"
rm -f $LOGNAME.p $LOGNAME.log
mknod $LOGNAME.p p
tee  <$LOGNAME.p $LOGNAME.log &
exec >$LOGNAME.p 2>&1
```

위의 스크립트는 script.log에 "exec" 명령의 모든 출력을 기록한다. 그러나 동일한 상호작용 프로그램(예: [파이썬](../Page/파이썬.md "wikilink"))들은 결과 셸 아래에 있을 때 표준 입력을 표시하지 않지만 script 명령 하에서 실행할 때에는 표준 입력을 표시한다.

## 같이 보기

  - [명령 줄 인터프리터](../Page/명령_줄_인터페이스.md "wikilink")
  - [셔뱅](../Page/셔뱅.md "wikilink")
  - [본 셸](../Page/본_셸.md "wikilink")
  - [Bash](../Page/배시_\(유닉스_셸\).md "wikilink")
  - [C 셸](../Page/C_셸.md "wikilink")
  - [파이썬](../Page/파이썬.md "wikilink")
  - [파일 확장자](../Page/파일_확장자.md "wikilink"), [명령 이름 문제](../Page/파일_확장자.md "wikilink")
  - [펄](../Page/펄.md "wikilink")
  - [스크립트 언어](../Page/스크립트_언어.md "wikilink")
  - [유닉스 셸](../Page/유닉스_셸.md "wikilink")

## 각주

[분류:유닉스 소프트웨어](https://ko.wikipedia.org/wiki/분류:유닉스_소프트웨어 "wikilink")

1.  <http://www.freebsd.org/cgi/man.cgi?query=script>
2.
3.  The instructions at this link no longer work due to the demise of the shelr.tv service. [OMG\! Ubuntu\! - How To Record And Share Terminal Screencasts Quickly](http://www.omgubuntu.co.uk/2012/04/how-to-record-and-share-terminal-screencasts-quickly/)