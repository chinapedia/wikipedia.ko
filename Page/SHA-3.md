> This article is converted from Wikipedia: [SHA-3](https://ko.wikipedia.org/wiki/SHA-3).


**SHA-3**은 [SHA-2](../Page/SHA-2.md "wikilink")를 대체하기위해 [미국 국립표준기술연구소가](../Page/미국_국립표준기술연구소.md "wikilink") 2015년 8월에 발표한 [암호화 해시 함수의](../Page/암호화_해시_함수.md "wikilink") 이름이다. 이 함수는 [SHA-1](https://ko.wikipedia.org/wiki/SHA-1 "wikilink")과 [SHA-2](../Page/SHA-2.md "wikilink")를 대체하기 위해 기획되었다. 기존의 해시 함수와는 다르게, 미국 국립표준기술연구소에서 직접 함수를 디자인하는 것이 아니라, 공개적인 방식을 통해 후보를 모집한 다음 함수 안전성을 분석하여 몇 차례에 걸쳐 후보를 걸러내는 방식으로 진행되었다.

2012년 10월 1일에 귀도 베르토니조앤 데먼, 질 반 아쉐, 마이클 피터스가 설계한 [Keccak](https://ko.wikipedia.org/wiki/Keccak "wikilink")이 SHA-3의 해시 알고리즘으로 선정되었다.\[1\]

2015년 8월 5일, 미국 국립표준기술연구소가 SHA-3 암호화 해시 함수 표준을 발표하였다.\[2\]

## SHA-3 예제

[미국 국립표준기술연구소가](../Page/미국_국립표준기술연구소.md "wikilink") 게시한 예제 해시 값\[3\]

<span style="color: green;">`SHA3-224("")`</span>
`6b4e03423667dbb73b6e15454f0eb1abd4597f9a1b078e3f5b5a6bc7`
<span style="color: green;">`SHA3-256("")`</span>
`a7ffc6f8bf1ed76651c14756a061d662f580ff4de43b49fa82d80a4b80f8434a`
<span style="color: green;">`SHA3-384("")`</span>
`0c63a75b845e4f7d01107d852e4c2485c51a50aaaa94fc61995e71bbee983a2ac3713831264adb47fb6bd1e058d5f004`
<span style="color: green;">`SHA3-512("")`</span>
`a69f73cca23a9ac5c8b567dc185a756e97c982164fe25859e0d1dcc1475c80a615b2123af1f5f94c11e3e9402c3ac558f500199d95b6d3e301758586281dcd26`
<span style="color: green;">`SHAKE128("", 256)`</span>
`7f9c2ba4e88f827d616045507605853ed73b8093f6efbc88eb1a6eacfa66ef26`
<span style="color: green;">`SHAKE256("", 512)`</span>
`46b9dd2b0ba88d13233b3feb743eeb243fcd52ea62b81b82b50c27646ed5762fd75dc4ddd8c0f200cb05019d67b592f6fc821c49479ab48640292eacb3b7c4be`

1비트를 변경하면 출력값의 각 비트가 50% 확률로 변경되어, [쇄도 효과](https://ko.wikipedia.org/wiki/쇄도_효과 "wikilink") 때문에 상당한 변화가 일어난다.:

<span style="color: green;">`SHAKE128("The quick brown fox jumps over the lazy dog", 256)`</span>
`f4202e3c5852f9182a0430fd8144f0a74b95e7417ecae17db0f8cfeed0e3e66e`
<span style="color: green;">`SHAKE128("The quick brown fox jumps over the lazy do`<span style="color: red;">`f`</span>`", 256)`</span>
`853f4538be0db9621a6cea659a06c1107b1f83f02b13d18297bd39d7411cf10c`

`달라진 비트는 총 126개이며, 이는 전체 비트 수 256개의 약 49.22%이다.`

## 각주

<references/>

## 외부 링크

  - [Keccak 웹사이트](http://keccak.noekeon.org/)

[분류:암호화 해시 함수](https://ko.wikipedia.org/wiki/분류:암호화_해시_함수 "wikilink")

1.  [5년간 공모 끝에 SHA-3 해시 알고리즘 최종 선정\!, 보안뉴스](http://www.boannews.com/media/view.asp?idx=33102&kind=1)(2012년 10월 5일)
2.
3.