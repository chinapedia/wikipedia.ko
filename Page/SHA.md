> This article is converted from Wikipedia: [SHA](https://ko.wikipedia.org/wiki/SHA).


**SHA**(Secure Hash Algorithm, 안전한 해시 알고리즘) 함수들은 서로 관련된 [암호학적 해시 함수들의](https://ko.wikipedia.org/wiki/암호학적_해시_함수 "wikilink") 모음이다. 이들 함수는 [미국 국가안보국](../Page/미국_국가안보국.md "wikilink")(NSA)이 [1993년](../Page/1993년.md "wikilink")에 처음으로 설계했으며 [미국](../Page/미국.md "wikilink") 국가 표준으로 지정되었다. SHA 함수군에 속하는 최초의 함수는 공식적으로 **SHA**라고 불리지만, 나중에 설계된 함수들과 구별하기 위하여 **SHA-0**이라고도 불린다. 2년 후 SHA-0의 변형인 **SHA-1**이 발표되었으며, 그 후에 4종류의 변형, 즉 **SHA-224**, **SHA-256**, **SHA-384**, **SHA-512**가 더 발표되었다. 이들을 통칭해서 **SHA-2**라고 하기도 한다.

SHA-1은 SHA 함수들 중 가장 많이 쓰이며, [TLS](https://ko.wikipedia.org/wiki/트랜스포트_레이어_보안 "wikilink"), [SSL](https://ko.wikipedia.org/wiki/SSL "wikilink"), [PGP](../Page/PGP_\(소프트웨어\).md "wikilink"), [SSH](../Page/시큐어_셸.md "wikilink"), [IPSec](https://ko.wikipedia.org/wiki/IPSec "wikilink") 등 많은 보안 프로토콜과 프로그램에서 사용되고 있다. SHA-1은 이전에 널리 사용되던 [MD5](../Page/MD5.md "wikilink")를 대신해서 쓰이기도 한다. 혹자는 좀 더 중요한 기술에는 SHA-256이나 그 이상의 알고리즘을 사용할 것을 권장한다.

SHA-0과 SHA-1에 대한 공격은 이미 발견되었다. SHA-2에 대한 공격은 아직 발견되지 않았으나, 전문가들은 SHA-2 함수들이 SHA-1과 비슷한 방법을 사용하기 때문에 공격이 발견될 가능성이 있다고 지적한다. [미국 표준 기술 연구소](https://ko.wikipedia.org/wiki/미국_표준_기술_연구소 "wikilink")(NIST)는 [SHA-3](../Page/SHA-3.md "wikilink")로 불리는 새로운 암호화 해시 알고리즘에 대한 후보를 공모하였다.

## SHA 함수군

[섬네일은](https://ko.wikipedia.org/wiki/파일:SHA-1.svg "wikilink") 2<sup>32</sup> 모듈로 덧셈을 나타낸다.\]\]

최초의 알고리즘은 [1993년](../Page/1993년.md "wikilink")에 [미국 표준 기술 연구소](https://ko.wikipedia.org/wiki/미국_표준_기술_연구소 "wikilink")(NIST)에 의해 **안전한 해시 표준**(Secure Hash Standard, [FIPS](https://ko.wikipedia.org/wiki/연방_정보_처리_표준 "wikilink") PUB 180)으로 출판되었으며, 다른 함수들과 구별하려 보통 SHA-0이라고 부른다. 얼마 안 있어 NSA는 이 표준을 폐기했고, [1995년](../Page/1995년.md "wikilink")에 개정된 알고리즘(FIPS PUB 180-1)을 새로 출판했으며 이를 SHA-1이라고 부른다. SHA-1은 SHA-0의 압축 함수에 비트 회전 연산을 하나 추가한 것으로, NSA에 따르면 이는 원래 알고리즘에서 암호학적 보안을 감소시키는 문제점을 고친 것이라고 하지만 실제로 어떤 문제점이 있었는지는 공개하지 않았다. 일반적으로 SHA-1은 SHA-0보다 암호학적 공격이 힘든 것으로 알려져 있으며, 따라서 NSA의 주장은 어느 정도 설득력이 있다. SHA-0과 SHA-1은 최대 2<sup>64</sup>비트의 메시지로부터 160비트의 해시값을 만들어 내며, [로널드 라이베스트가](../Page/로널드_라이베스트.md "wikilink") [MD4](../Page/MD4.md "wikilink") 및 [MD5](../Page/MD5.md "wikilink") 해시 함수에서 사용했던 것과 비슷한 방법에 기초한다.

NIST는 나중에 해시값의 길이가 더 긴 네 개의 변형을 발표했으며, 이들을 통칭하여 SHA-2라 부른다. SHA-256, SHA-384, SHA-512는 [2001년](../Page/2001년.md "wikilink")에 초안으로 처음으로 발표되었으며, [2002년](../Page/2002년.md "wikilink")에 SHA-1과 함께 정식 표준(FIPS PUB 180-2)으로 지정되었다. [2004년](../Page/2004년.md "wikilink") 2월에 [삼중 DES의](https://ko.wikipedia.org/wiki/Triple_DES "wikilink") 키 길이에 맞춰 해시값 길이를 조정한 SHA-224가 표준에 추가되었다. SHA-256과 SHA-512는 각각 32바이트 및 64바이트 워드를 사용하는 해시 함수이며, 몇몇 상수들이 다르긴 하지만 그 구조는 라운드의 수를 빼고는 완전히 같다. SHA-224와 SHA-384는 서로 다른 초기값을 가지고 계산한 SHA-256과 SHA-512 해시값을 최종 해시값 길이에 맞춰 잘라낸 것이다.

### 크기 비교

다음은 SHA 함수들의 특성을 요약한 표이다.

| 알고리즘            | 해시값 크기  | 내부 상태 크기 | 블록 크기 | 길이 한계 | 워드 크기 | 과정 수 | 사용되는 연산                | 충돌       |
| --------------- | ------- | -------- | ----- | ----- | ----- | ---- | ---------------------- | -------- |
| **SHA-0**       | 160     | 160      | 512   | 64    | 32    | 80   | \+,and,or,xor,rotl     | 발견됨      |
| **SHA-1**       | 160     | 160      | 512   | 64    | 32    | 80   | \+,and,or,xor,rotl     | 발견됨\[1\] |
| **SHA-256/224** | 256/224 | 256      | 512   | 64    | 32    | 64   | \+,and,or,xor,shr,rotr | \-       |
| **SHA-512/384** | 512/384 | 512      | 1024  | 128   | 64    | 80   | \+,and,or,xor,shr,rotr | \-       |

여기서 내부 상태는 데이터 블록 하나를 압축한 뒤의 "내부적인 해시값"의 크기를 나타낸다. 또한 SHA는 내부적으로 메시지 채움을 위해 데이터의 길이와 같은 추가적인 변수를 사용하며, 길이 한계는 이때 사용되는 변수의 크기를 나타낸다. 메시지 채움에 대한 자세한 설명은 [머클-담고르 해시 함수를](https://ko.wikipedia.org/wiki/머클-담고르_해시_함수 "wikilink") 참고하라.

## 예제

다음은 SHA-1 해시값의 예제이다.

`SHA1("The quick brown fox jumps over the lazy dog")`
`  = 2fd4e1c67a2d28fced849ee1bb76e7391b93eb12`

해시값은 [눈사태 효과](https://ko.wikipedia.org/wiki/눈사태_효과 "wikilink") 때문에 메시지가 조금만 바뀌어도 완전히 바뀔 수 있다. 다음 예시는 위의 예제 끝에 마침표(.)를 찍은 것이다.

`SHA1("The quick brown fox jumps over the lazy dog.")`
`  = 408d94384216f890ff7a0c3528e8bed1e0b01621`

빈 문자열의 해시는 다음과 같다.

`SHA1("") = da39a3ee5e6b4b0d3255bfef95601890afd80709`

## 구현

미국과 캐나다 정부(NIST와 CSE)에서는 SHA 구현들을 검증하기 위한 프로그램을 제공한다. 또한 정식 검증 절차를 거치지 않고도 사용할 수 있는 예제 테스트 데이터도 함께 제공하고 있다. 예제 데이터와 실제 검증 과정은 수만 개의 테스트가 포함되어 있으며, 몇몇 경계 조건과 자주 나타나는 구현 에러를 잡아 낼 수 있도록 설계되어 있다.

[2006년](../Page/2006년.md "wikilink") 5월 초 기준으로, 적어도 463개의 검증된 SHA 구현이 존재하며 그중 7개는 바이트 단위가 아닌 임의의 이진 데이터도 처리할 수 있다. 이외에도 인터넷에는 SHA-1 표준에 있는 예제는 통과하지만 NIST 검증 페이지의 예제들은 통과하지 못하는 구현들이 몇몇 있다.

## 각주

[분류:암호화 해시 함수](https://ko.wikipedia.org/wiki/분류:암호화_해시_함수 "wikilink")

1.