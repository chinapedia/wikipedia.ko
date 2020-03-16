> This article is converted from Wikipedia: [GNU arch](https://ko.wikipedia.org/wiki/GNU_arch).


**GNU arch**는 분산형 리비전 관리 소프트웨어의 일종으로 소스 트리에서 일어나는 변경들을 추적하며 통합을 비롯해 여러 사람에 의해 또는 서로 다른 여러 시간대에 일어나는 다양한 변화들을 처리한다. GNU 프로젝트 가운데 하나이며 [GNU GPL에](https://ko.wikipedia.org/wiki/GNU_GPL "wikilink") 따라 배포된다.

2009년부로 개발이 중단되어 현재 개발 트리에서는 보안 문제 수정만이 이루어진다.\[1\] GNU arch에서 [분가](https://ko.wikipedia.org/wiki/분가 "wikilink")된 소프트웨어로는 [Bazaar가](../Page/Bazaar_\(소프트웨어\).md "wikilink") 있으며 GNU 프로젝트 가운데 하나로 공식 채택된 이후 GNU arch의 대안으로 부상했다.

## 특징

GNU arch는 배포 및 분산형 버저닝 시스템이기 때문에 전역에서 각 리비전은 고유한 개체로 식별되며 이때 만들어진 식별자는 배포된 설정들의 통합을 보조하거나 전혀 다른 소스로부터 내용을 일부만 반영할 때 사용된다. 또 개발자로 하여금 변경 사항을 반영하려 할 때마다 일일이 인증을 거치게 하는 중앙 서버가 필요하지 않으며 [HTTP](../Page/HTTP.md "wikilink"), [FTP](https://ko.wikipedia.org/wiki/FTP "wikilink"), [SFTP](https://ko.wikipedia.org/wiki/SFTP "wikilink")를 통해 공식 저장소 안에서 프로젝트가 통째로 읽기 전용으로 복사되어 그쪽으로 접속하게 된다. 물론 이 때문에 개발자들은 각자의 공용 저장소 안에서 변경 사항을 반영하게 되고 공식 저장소에의 반영은 저장소 전체를 관리하는 사람이 손으로 하나하나 다 해야 한다. 하지만 저장소 전체를 관리하는 사람이 [SSH](../Page/시큐어_셸.md "wikilink"), [FTP](../Page/파일_전송_프로토콜.md "wikilink"), [SFTP](../Page/SSH_파일_전송_프로토콜.md "wikilink"), WebDAV를 통한 접속을 허용하여 인증 과정을 거친 사용자로 하여금 중앙 서버에 변경 사항을 반영하게 함으로 집중형 리비전 관리 시스템을 흉내내는 것도 가능하다.

이 밖에도 다음과 같은 특징들이 있다.

  - **분할 반영(Atomic commits):** 원래 버저닝 시스템에서 변경 사항의 반영은 모 아니면 도다. 반영에 앞서 트리가 반영을 받을 준비가 되어 있어야 하며 반영은 완료되기까지 밖에서 확인할 수 없다. 반영이 완료되지 못한 채 끊겨도 그 사실을 밖에서 확인할 수 없으며 다음 반영에 앞서 반영되기 전으로 돌려 놓아야 한다. 하지만 GNU arch는 이 특징을 가짐으로 앞에서 언급한 것과 같은 상황을 피할 수 있다.
  - **변경 사항 중시(Changeset oriented):** [CVS](../Page/CVS.md "wikilink")에서처럼 파일 하나하나를 추적하는 대신 패치와 같은 류의 변경 사항을 추적한다. 각 변경 사항은 한 소스 트리와 다른 소스 트리의 차이를 담고 있어 한 리비전에서 다른 리비전을 만들어내는 데 쓸 수 있다. 변경 사항의 반영은 기능 변경 또는 버그 수정 때마다 하는 것이 권장된다.
  - **쉬운 트리 복사(Easy branching):** 효율적이고 알아보기 쉬운 트리 복사가 가능하다. 복사된 트리는 이전 리비전에 대한 간략한 정의를 담고 있어 그곳에서 개발을 계속할 수 있다.
  - **정교한 통합(Advanced merging):** 모든 이전 리비전 및 합쳐진 리비전에 대한 기록이 영구 보관되기 때문에 리비전을 통합할 때 어떤 변경 사항이 반영된 어떤 트리와 합칠 것인지까지 선택할 수 있고, 공용되는 이전 리비전을 기반으로 하여 3개의 트리를 하나로 통합할 수도 있다.
  - **암호화된 서명(Cryptographic signatures):** 모든 변경 사항은 사고에 의한 손상을 막기 위해 해시와 함께 저장된다. GnuPG같은 외부 파일 서명 프로그램을 통해 해시에 서명하여 저장소가 해킹 등으로 무너졌을 때 트리에 원치 않는 변화가 일어나는 것을 막을 수도 있다.
  - **파일 이름 변경(Renaming):** 파일과 디렉토리의 이름을 바꾸는 것이 쉽다. 파일과 디렉토리를 이름 대신 고유의 식별자를 통해 추적하기 때문에 이름 변경 또한 변경 사항으로 기록되며 파일에 대한 패치 또한 두 트리에서 파일 이름이 각각 달라도 문제없이 적용된다.
  - **메타데이터 추적(Metadata tracking):** 파일마다 권한 식별자도 추적된다. 더 나아가서는 심볼릭 링크도 같은 방식으로 추적된다.

## 걸어온 길

### 버전 1, 그리고 tla

GNU arch를 처음 개발한 사람은 Thomas Lord로 그는 2001년에 이 프로젝트를 시작했으며 동시에 프로젝트의 첫 관리자이기도 했다. 이 소프트웨어의 실행 파일 이름은 tla로 이는 Tom Lord's Arch의 줄임말이었다. 그는 이 프로젝트를 CVS를 대체할 목적으로 시작했으며 초기의 모습은 복수의 셸 스크립트의 집합체였다.\[2\] 이 프로젝트가 GNU 프로젝트의 일부가 된 것은 2003년이다.\[3\]

다른 개발 주체에 의해 분가가 시도된 적도 몇 번 있었다. 그 중 하나는 지금은 버려졌지만 캐노니컬에서 시도했던 Baz였고 다른 하나는 Walter Landry가 시도했던 ArX였다. 둘 다 큰 반발을 불러일으켰는데 ArX는 개발 방향과 관련된 깊은 분쟁을 겪었고 Baz 프로젝트를 시도한 캐노니컬은 Thomas Lord에 의해 개발 태도와 관련된 거센 비난을 받았다.\[4\]

2005년 8월이 되자 Thomas Lord는 GNU arch 프로젝트의 관리자 자리에서 물러나면서 Baz를 GNU arch 프로젝트로 받아들이는 것을 추천했다.\[5\] 하지만 그의 추천은 받아들여지지 않았다. Baz는 캐노니컬에 의해 버려졌고 별도로 진행되던 Bazaar가 Baz의 빈 자리를 채우게 되었다.\[6\] Baz는 2006년 1.5를 마지막으로 완전히 버려졌다.\[7\] 2005년 10월, Andy Tai는 Thomas Lord와 자유 소프트웨어 재단이 자신에 대한 GNU arch 프로젝트 관리자 임명 요구를 받아들였다고 발표했다.\[8\] 그는 새 관리자가 되자마자 Baz의 많은 기능들을 tla에 이식했으나 2008년 3월이 되자 tla에 대한 더 이상의 개발은 없으며 tla는 더 이상 다른 버전 컨트롤 시스템들의 상대가 되지 못한다는 발표를 했다.\[9\]

### revc

revc는 Thomas Lord가 GNU arch의 버전 2로 삼을 것을 목적으로 하여 시작한 프로젝트로 tla와 전혀 다른 구조를 가지고 있으며 Git에서 많은 아이디어를 빌려왔다.\[10\] 처음 발표된 것은 2005년 6월이며\[11\] 첫 버전의 출시는 그 다음 달에,\[12\] 그리고 마지막 버전의 출시는 또 그 다음 달에 이루어졌으며 Thomas Lord는 직후 관리자 자리에서 물러났다.\[13\] 이 소프트웨어가 가진 명령은 10개뿐이었으며 Thomas Lord는 제한적인 네임스페이스와 복잡한 파일 명명 규칙을 없애고 속도도 높이는 것을 목표로 했었다.\[14\]

2008년 이래 마지막 버전인 0.0x2는 지금도 입수할 수 있으며\[15\] Thomas Lord는 지금도 GNU arch의 아이디어 중 일부에 흥미를 가지고 있지만 revc의 개발을 계속할 여지는 없다고 밝혔다.\[16\]

## 비판

GNU arch가 가장 많이 받은 비판은 다른 SCM 시스템에 대한 경험이 있는 사람조차 익히기 어렵다는 비판이다. 특히 명령의 수가 지나치게 많은 것은 새로운 사용자에 대한 진입 장벽이 될 수 있으며 몇몇 구성 요소는 사용자에게 Thomas Lord와 같은 방식으로 버전을 컨트롤할 것을 지나치게 강요한다는 비판을 주로 받았다.\[17\]

불필요한 파일 명명 규칙(["FunkyFileNames"](https://web.archive.org/web/20070808210711/http://www.gnuarch.org/gnuarchwiki/FunkyFileNames))로 인해서도 비판을 받았는데 이 규칙이 스크립트에의 적용이나 일부 셸에서의 사용, 그리고 비-유닉스형 운영체제에의 이식을 어렵게 한다는 내용이었다. 또한 내부 코드의 복잡함을 줄이는 데에 무게를 지나치게 두다 보니 실행 속도가 느린 결과물이 되었다는 비판도 받았다.\[18\]

## 각주

## 외부 링크

  - [공식 사이트](http://www.gnu.org/software/gnu-arch/)

[분류:GNU 프로젝트 소프트웨어](https://ko.wikipedia.org/wiki/분류:GNU_프로젝트_소프트웨어 "wikilink") [분류:C 소프트웨어](https://ko.wikipedia.org/wiki/분류:C_소프트웨어 "wikilink") [분류:2001년 소프트웨어](https://ko.wikipedia.org/wiki/분류:2001년_소프트웨어 "wikilink") [분류:C로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C로_작성된_자유_소프트웨어 "wikilink") [분류:자유 버전 관리 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_버전_관리_소프트웨어 "wikilink")

1.  [1](http://lists.gnu.org/archive/html/gnu-arch-users/2008-03/msg00003.html)
2.  [2](http://www.linuxjournal.com/article/7671)
3.  [3](http://ml.osdir.com/version-control.arch.user/2003-07/msg00833.html)
4.  [4](http://lists.gnu.org/archive/html/gnu-arch-users/2004-10/msg00771.html)
5.  [5](http://lists.gnu.org/archive/html/gnu-arch-users/2005-08/msg00030.html)
6.  [6](http://bazaar-vcs.org/Baz1x)[7](http://bazaar-vcs.org/HistoryOfBazaar)
7.
8.  [8](http://lists.gnu.org/archive/html/gnu-arch-users/2005-10/msg00246.html)
9.  [9](http://lists.gnu.org/archive/html/gnu-arch-users/2008-03/msg00003.html)
10. [10](http://ml.osdir.com/version-control.arch.devel/2005-06/msg00034.html)
11. [11](http://ml.osdir.com/version-control.arch.devel/2005-06/msg00034.html)
12.
13. [12](http://lists.gnu.org/archive/html/gnu-arch-users/2005-08/msg00009.html)
14.
15. [13](http://lists.gnu.org/archive/html/gnu-arch-users/2008-03/msg00000.html)
16. [14](http://lists.gnu.org/archive/html/gnu-arch-users/2008-03/msg00005.html)
17. [15](http://sourcefrog.net/weblog/software/vc/arch/whats-wrong.html) [16](http://sourcefrog.net/weblog/software/vc/arch/lord-interview.html)
18. [17](http://www.enyo.de/fw/software/arch/design-issues.html)