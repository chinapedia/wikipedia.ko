> This article is converted from Wikipedia: [Chkrootkit](https://ko.wikipedia.org/wiki/Chkrootkit).


**chkrootkit** (**Check Rootkit**)은 [시스템 관리자가](https://ko.wikipedia.org/wiki/시스템_관리자 "wikilink") 자신의 시스템을 알려진 [루트킷](../Page/루트킷.md "wikilink")들로부터 보호하는 것을 돕기 위해 개발된 유닉스 기반 프로그램이다. 이것은 시그니처를 통해서 그리고 [/proc](../Page/Procfs.md "wikilink") 파일시스템의 순회와 [ps](../Page/Ps_\(유닉스\).md "wikilink") 명령어의 결과를 비교함으로써 코어 시스템 프로그램들을 찾기 위해 *strings*나 *[grep](https://ko.wikipedia.org/wiki/grep "wikilink")* 명령어 같은 유닉스/리눅스 툴들을 사용하는 [셸 스크립트이다](../Page/셸_스크립트.md "wikilink").

chkrootkit은 루트킷 탐지를 수행하는데 사용될 명령어 프로그램들이 이미 감염되었을지도 모르기 때문에, "rescue disc" (일반적으로 [라이브 CD](../Page/라이브_CD.md "wikilink"))에서 사용되거나 또는 자신의 명령어들 모두를 실행하는 대체 디렉토리에서 사용될 수 있다. 이러한 기법들은 chkrootkit이 자신이 의존하는 명령어를 더 신뢰할 수 있게 해준다.

탐지하려고 시도하는 프로그램들의 신뢰성에 대해서는 자체적으로 한계가 존재할 수 밖에 없다. 최신 루트킷들은 구체적으로 chkrootkit 프로그램들의 사본들을 탐지하거나 이것들의 탐지를 회피하려는 여러 조치들을 시도한다.

## 같이 보기

  - [rkhunter](https://ko.wikipedia.org/wiki/rkhunter "wikilink")

## 외부 링크

  -
  - [Auto Install Script for CHKrootkit](https://web.archive.org/web/20160313220939/https://solidshellsecurity.com/tools/chkrootkit-automatic-script-installer.php)

  - [chkrootkit](http://freecode.com/projects/chkrootkit/)<span> at </span>Freecode

[분류:보안 소프트웨어](https://ko.wikipedia.org/wiki/분류:보안_소프트웨어 "wikilink") [분류:루트킷](https://ko.wikipedia.org/wiki/분류:루트킷 "wikilink")