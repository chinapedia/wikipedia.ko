> This article is converted from Wikipedia: [:IRC ](https://ko.wikipedia.org/wiki/:IRC_).


[고양이도 하는 IRC입니다. 누구나 환영합니다.](https://ko.wikipedia.org/wiki/파일:Gato_leyendo_canal_IRC_de_Wikipedia_en_español.jpg "wikilink")

위키백과 사용자들끼리의 실시간 대화를 위해서 **[IRC](https://ko.wikipedia.org/wiki/인터넷_릴레이_챗 "wikilink")** 대화방이 열려 있습니다.

## 대화방과 위키백과의 관계

위키백과 IRC 대화방은 위키미디어 재단 등이 아닌 자원봉사자에 의해 위키백과와 독립적으로 운영되는, 위키백과 사용자들이 대화를 나눌 수 있는 비공식적인 장소입니다. IRC 대화방이 위키백과에 미치는 영향은 술자리에서 하는 잡담과 마찬가지입니다. IRC 대화는 몇 명끼리만 이루어질 수 있지만, 수백 명이 엿들을 수도 있고, 기록이 공개되면 그보다 많은 사람들이 알게 될 수도 있습니다.

IRC 대화방이 위키백과 참여자를 공격하기 위해 사용되거나, IRC 대화방에서 이루어진 논의가 위키백과 상에서의 행동을 정당화하기 위해 인용될 경우, 위키백과 공동체의 분위기에 심각한 훼손을 초래하게 됩니다.

## IRC 사용방법

### IRC 클라이언트

  - IRC 대화방에 접속하려면 [Hexchat](http://hexchat.github.io/)이나 [Colloquy](http://colloquy.info/), [피진](http://www.pidgin.im), [AndChat](http://www.andchat.net)과 같은 IRC 클라이언트가 필요합니다. 클라이언트를 별도로 설치하지 않을 경우 웹 브라우저를 통해 [프리노드 웹 IRC](http://webchat.freenode.net/?channels=%23wikipedia-ko&uio=Mj10cnVlJjk9dHJ1ZSYxMT0xMDMc3)나 [키위IRC](https://kiwiirc.com/client?settings=77d28d4882cb7982d1f219a28aace3eb), [IRC Cloud](https://www.irccloud.com) 등의 서비스를 이용할 수도 있습니다.
  - [모질라 파이어폭스](../Page/모질라_파이어폭스.md "wikilink") 사용자의 경우 확장 기능인 [챗질라](https://addons.mozilla.org/ko/firefox/addon/16)(ChatZilla)를 이용하여 접속할 수 있습니다. 하지만, 파이어폭스 57 이상 버전을 이용 중인 사용자는 더 이상 챗질라를 설치할 수 없습니다.

### IRC 접속 및 사용방법

대부분 IRC 클라이언트는 실행 후 안내에 따라 chat.freenode.net로 접속한 다음, 입력창에 `/join #wikipedia-ko`를 입력해서 한국어 위키백과 채널에 접속할 수 있습니다.

닉네임은 `/nick (사용할 닉네임)`로 바꿀 수 있습니다.

### 기술적 도움말

  - 기본적으로 IRC 서버는 6667 포트를 사용합니다. 사용하는 인터넷 서비스에서 6667 포트를 차단한 경우 대신 6660\~6670, 또는 8080 중의 한 포트로 시도해 보세요. 프리노드는 보안 연결(SSL connection)을 지원하며, 이 경우 6697 포트를 사용합니다.
      - 가령 챗질라로 한국어 위키백과 주 채널에 접속할 때, 포트를 변경하려면 입력창에 '/server chat.freenode.net xxxx' 라고 입력합니다(xxxx에 6660\~6670, 8080 중 적절한 번호 입력).
  - [문자 인코딩이](../Page/문자_인코딩.md "wikilink") 맞지 않으면 대화가 깨져 나옵니다. 클라이언트에 따라 서버에서 사용하는 인코딩을 지원하지 않을 수 있으니 주의하시기 바랍니다. 각 서버의 인코딩은 아래의 서버 목록에 나와 있습니다.

### 닉네임 등록

[프리노드](../Page/프리노드.md "wikilink")에서는 Nickserv를 통해 닉네임을 등록할 수 있습니다. 닉네임을 등록하면 다른 사람의 닉네임 도용을 방지하고, 클록 등을 받을 수 있는 등의 장점이 있으니 닉네임을 등록하실 것을 권장합니다.

등록을 하시려면, `/msg nickserv REGISTER (사용할 비밀번호) (이메일)`를 입력하고 나오는 지시에 따라주시면 됩니다. 자세한 도움말은 `/msg nickserv help register`을 입력하면 볼 수 있습니다.

#### 클록

모든 위키미디어 재단 위키에서 250회 이상 기여하고, 위키미디어 계정을 만든지 3개월이 지났으며, 위키 이메일 인증을 완료한 모든 사용자는 `/msg wmopbot cloak`을 통해 클록을 요청할 수 있습니다. 클록은 IRC 사용자가 위키백과 등 프로젝트의 사용자임을 증명하며, IRC 접속에 사용하는 IP를 숨길 수 있는 등의 장점이 있습니다. 자세한 정보는 [메타의 설명 문서에서](https://ko.wikipedia.org/wiki/meta:IRC/Cloaks "wikilink") 볼 수 있습니다.

### IRC 대화방 안내

  - [프리노드](../Page/프리노드.md "wikilink")  - 주 채널입니다. [UTF-8](https://ko.wikipedia.org/wiki/UTF-8 "wikilink") 인코딩을 사용합니다.
  - <irc://irc.hanirc.org/wikipedia> - HanIRC 보조 채널입니다. [CP949](https://ko.wikipedia.org/wiki/CP949 "wikilink") 인코딩을 사용합니다.
      - <irc://utf8.hanirc.org/wikipedia> - 위와 같은 채널이며, UTF-8 인코딩을 사용합니다.
  - <irc://irc.ozinger.org/wikipedia> - 오징어 보조 채널입니다.
  - 위키미디어 [\#ko.wikipedia](https://ko.wikipedia.org/wiki/rcirc:#ko.wikipedia "wikilink") - [최근 바뀜을](https://ko.wikipedia.org/wiki/특수기능:최근바뀜 "wikilink") 실시간으로 알려 주는 채널이며, 대화는 불가능합니다. UTF-8 인코딩을 사용합니다.

한국어 위키백과 이외의 다른 프로젝트의 IRC 대화방에 대한 정보는 [m:IRC](https://ko.wikipedia.org/wiki/m:IRC "wikilink")에서 볼 수 있습니다.

## IRC 대화방 이용시 주의사항

위키백과 IRC 대화방은 사용자들의 간편한 의견 교류를 위해 존재하지만, 이곳은 한국어 위키백과나 기타 위키미디어에 관계된 **공식적인 자리가 아닙니다**. IRC 대화방에서의 어떠한 논의도 위키백과에서 이루어지는 논의의 근거가 될 수 없습니다. 또한 IRC 대화를 공개된 장소에 올리려면 그 대화의 참여자 모두에게 동의를 얻어야 합니다.

또한 개설 목적에 맞는 대화를 위해, IRC 대화방에서는 다음과 같은 규칙을 지켜야 합니다.

  - 대화방의 닉네임은 되도록 위키백과의 사용자 이름에 맞추어 주세요.
  - 자동 스크립트, 음담패설, 도배는 삼가 주세요.
      - 채널 도배 시 도배 방지 시스템에 의해 채팅 금지 (quiet) 또는 강퇴 (kick) 처리 될 수 있으며, 이에 대한 수동 검토는 이루어지지 않습니다.
  - 상대방의 인격이나 신상에 관한 모욕적인 발언은 삼가 주세요.
  - 관리자를 지속적, 주기적으로 호출하여 특정한 행위를 할 것을 요청하는 것은 권장되지 않습니다.
  - 개인정보가 연관되는 대화, 특정판 삭제 요청 등을 공개된 채널에서 하는 것은 금지되어 있습니다. 개인 메시지 기능을 이용해 주세요.
  - 프리노드의 [규정](https://freenode.net/policies)에 의거하여, 로그의 공개는 대화 당사자 전원이 동의해야 가능합니다.
  - 진행중인 선거에 관한 대화는 금지되어 있습니다.
  - 다른 사용자들이 위키백과에 관계된 이야기를 하고 있는 동안에는, 그 이야기를 방해하지 않도록 지나친 잡담은 자제해 주세요. 다른 사용자들의 대화를 방해할 정도라면 잠시 발언권을 제한할 수도 있습니다.

채널 관리자의 관리 기록은 [위키백과:IRC_대화방//기록에서](https://ko.wikipedia.org/wiki/위키백과:IRC_대화방/기록 "wikilink") 열람할 수 있습니다.

[](https://ko.wikipedia.org/wiki/분류:위키백과_사용자_모임 "wikilink")