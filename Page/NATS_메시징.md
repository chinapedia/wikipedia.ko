> This article is converted from Wikipedia: [NATS 메시징](https://ko.wikipedia.org/wiki/NATS_메시징).


**NATS**는 [오픈 소스](../Page/오픈_소스.md "wikilink") 메시징 시스템([메시지 지향 미들웨어](../Page/메시지_지향_미들웨어.md "wikilink"))이다. NATS 서버는 [Go](https://ko.wikipedia.org/wiki/Go "wikilink") 프로그래밍 언어로 작성되었다. 서버와의 인터페이스를 위한 클라이언트 라이브러리는 주요 프로그래밍 언어로 이용이 가능하다. NATS의 핵심 설계 원리는 성능, 확장성, 쉬운 이용이다.\[1\]

## 예시

demo.nats.io의 텔넷 연결 시 샘플 연결 문자열을 볼 수 있다\[2\]

``` go
telnet demo.nats.io 4222

Trying 107.170.221.32...
Connected to demo.nats.io.
Escape character is '^]'.
INFO {"server_id":"NDP7NP2P2KADDDUUBUDG6VSSWKCW4IC5BQHAYVMLVAJEGZITE5XP7O5J","version":"2.0.0","proto":1,"go":"go1.11.10","host":"0.0.0.0",
"port":4222,"max_payload":1048576,"client_id":13249}
```

## 각주

[분류:Go로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:Go로_작성된_자유_소프트웨어 "wikilink") [분류:메시지 지향 미들웨어](https://ko.wikipedia.org/wiki/분류:메시지_지향_미들웨어 "wikilink") [분류:자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_소프트웨어 "wikilink")

1.
2.