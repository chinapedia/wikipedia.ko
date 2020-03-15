> This article is converted from Wikipedia: [Rm \(\)](https://ko.wikipedia.org/wiki/Rm_\(\)).


**rm** (*remove*의 축약)은 [파일 시스템으로부터](https://ko.wikipedia.org/wiki/파일_시스템 "wikilink") 파일을 삭제할 때에 사용되는 [유닉스](https://ko.wikipedia.org/wiki/유닉스 "wikilink") 명령어이다.

## 옵션

rm에 덧붙여 사용할 수 있는 옵션에는 다음과 같은 것이 있다.:

  - \-r, 디렉터리를 삭제한다, 하위의 내용을 먼저 삭제한다. (하위에 존재하는 파일이 남아있으면 안 되기 때문에) ("recursive", 재귀적으로)
  - \-i, 삭제를 할 때에 매번 삭제 여부를 사용자에게 묻는다. ("interactive", 대화식으로)
  - \-f, 존재하지 않는 파일을 무시하고 어떠한 확인 메시지도 보여주지 않는다. ("force", 강제로)
  - \-v, 삭제를 하는 동안 삭제되는 내용을 보여준다 ("verbose", 장황하게)

rm은 실수로 삭제되는 것을 방지하기 위해 "rm -i"으로 alias 하여 많이 사용한다. 이 경우 만약 이용자가 많은 양의 파일을 확인 없이 삭제하고자 할 때에는 -f 옵션을 붙여 사용한다. ("rm -i -f"와 같이 두 옵션을 모두 지정한 경우 뒤쪽의 옵션이 우선순위를 갖게 된다.)

**rm -rf** (또는, `rm -rf /`, `rm -rf *`, 등등)은 유닉스 재앙의 농담이나 비화에 많이 등장한다. 이들 명령이 [슈퍼유저](https://ko.wikipedia.org/wiki/슈퍼유저 "wikilink")에 의해 루트 디렉터리에서 실행되게 되면, 컴퓨터 파일 시스템 상의 쓰기 가능한 모든 파일이 삭제되는 그야말로 재앙이 일어난다.

rm은 종종 삭제된 파일의 목록을 공급하기 위해 [xargs](https://ko.wikipedia.org/wiki/xargs "wikilink")와 결합하여 사용하기도 한다:

[`xargs`](https://ko.wikipedia.org/wiki/xargs "wikilink")` rm < filelist`

rm이 [심볼릭 링크에](../Page/심볼릭_링크.md "wikilink") 사용될 때에는, 링크는 삭제하지만, 링크의 대상에는 영향을 미치지 않는다.

## 권한

일반적으로 거의 모든 파일시스템에서, 파일을 삭제하기 위해서는 그 파일의 부모 디렉터리에 파일 쓰기 권한이 있어야 한다. (더불어 일단 디렉터리에 들어가기 위해 실행 권한이 있어야 한다). (초심자에겐 혼란스럽겠지만, 파일 자체의 권한은 상관이 없다.)

디렉터리를 (`rm -r`)으로 삭제하기 위해선, 그 아래의 내용을 재귀적으로 모두 지워야 한다. 이것은 그 디렉터리를 쓰고 실행하는 권한을 요구하고 (만약 그것이 비어있지 않다면) 그리고 안의 서브 디렉터리들 역시 비워야 한다 (어떠한 것이든지). 이런 원리는 좀 재미있는 상황을 만들기도 하는데, 디렉터리가 비어있지 않고, 쓰기 권한이 없다면, 그 하위의 내용을 지울 수 없기 때문에 디렉터리를 지울 수 없는 반면에, 이 디렉터리가 비어있기만 하면, 디렉터리에 쓰기 권한이 없더라도 삭제할 수 있다.

만약에 파일이 디렉터리에 [sticky bit세트와](https://ko.wikipedia.org/wiki/sticky_bit "wikilink") 함께 있다면, 그 때는 파일의 삭제를 위해 파일의 소유자가 수행해야 한다.

## 기타

썬은 [솔라리스](https://ko.wikipedia.org/wiki/솔라리스_\(운영_체제\) "wikilink") 10에서 "`rm -rf /`" 방지를 소개한다. 명령어를 실행하면서, 시스템은 / (루트 디렉터리)에 명령을 적용할 수 없다고 보고한다.\[1\] [GNU 코어 유틸리티의](../Page/GNU_코어_유틸리티.md "wikilink") 6.4 버전 이후로는 기본값으로 되어 있는 `--preserve-root` 옵션이 주어진다면, [GNU](https://ko.wikipedia.org/wiki/GNU "wikilink") `rm` 은 `rm -rf /` 의 실행을 거절한다.

## 같이 보기

  - [unlink()](https://ko.wikipedia.org/wiki/unlink_\(유닉스\) "wikilink"): 사용자 영역의 rm 명령에 의해 호출되는 [시스템 콜](https://ko.wikipedia.org/wiki/시스템_콜 "wikilink")
  - [del (명령어)](https://ko.wikipedia.org/wiki/del_\(명령어\) "wikilink")
  - [deltree](https://ko.wikipedia.org/wiki/deltree "wikilink")

## 참조

## 외부 링크

  -
  -
[분류:표준 유닉스 프로그램](https://ko.wikipedia.org/wiki/분류:표준_유닉스_프로그램 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink")

1.