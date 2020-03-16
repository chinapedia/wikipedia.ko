> This article is converted from Wikipedia: [RSA ](https://ko.wikipedia.org/wiki/RSA_).


**RSA 암호**는 [공개키 암호시스템의](../Page/공개_키_암호_방식.md "wikilink") 하나로, 암호화뿐만 아니라 [전자서명](../Page/전자서명.md "wikilink")이 가능한 최초의 [알고리즘](../Page/알고리즘.md "wikilink")으로 알려져 있다. RSA가 갖는 [전자서명](../Page/전자서명.md "wikilink") 기능은 인증을 요구하는 [전자 상거래](../Page/전자_상거래.md "wikilink") 등에 RSA의 광범위한 활용을 가능하게 하였다.

1978년 [로널드 라이베스트](../Page/로널드_라이베스트.md "wikilink")(Ron Rivest), [아디 샤미르](../Page/아디_샤미르.md "wikilink")(Adi Shamir), [레너드 애들먼](https://ko.wikipedia.org/wiki/레너드_애들먼 "wikilink")(Leonard Adleman)의 연구에 의해 체계화되었으며, RSA라는 이름은 이들 3명의 이름 앞글자를 딴 것이다. 이 세 발명자는 이 공로로 2002년 [튜링상](../Page/튜링상.md "wikilink")을 수상했다. 그러나 RSA 방식을 제일 먼저 개발한 사람은 영국 [GCHQ](https://ko.wikipedia.org/wiki/GCHQ "wikilink")에 근무하던 수학자였으며, 이보다 빠른 1973년도에 개발하게 된다. 이 내용은 GCHQ에서 비밀로 취급되었으며, 이후 1997년 세상으로 발표되게 된다.\[1\]

RSA 암호체계의 안정성은 큰 숫자를 [소인수 분해하는](../Page/섹스_돌.md "wikilink") 것이 어렵다는 것에 기반을 두고 있다. 그러므로 큰 수의 소인수 분해를 획기적으로 빠르게 할 수 있는 알고리즘이 발견된다면 이 암호 체계는 가치가 떨어질 것이다. [1993년](../Page/1993년.md "wikilink") [피터 쇼어는](https://ko.wikipedia.org/wiki/피터_쇼어 "wikilink") [쇼어 알고리즘을](https://ko.wikipedia.org/wiki/쇼어_알고리즘 "wikilink") 발표하여, 양자 컴퓨터를 이용하여 임의의 정수를 [다항 시간](https://ko.wikipedia.org/wiki/다항_시간 "wikilink") 안에 소인수 분해하는 방법을 발표하였다. 따라서 양자 컴퓨터가 본격적으로 실용화되면 RSA 알고리즘은 무용지물이 될 것이다. 그러나 양자 컴퓨터가 이 정도 수준으로 실용화되려면 아직 여러 해가 더 필요할 것으로 보인다.

RSA 암호화 알고리즘은 [1983년](../Page/1983년.md "wikilink")에 발명자들이 소속되어 있던 [매사추세츠 공과대학교](../Page/매사추세츠_공과대학교.md "wikilink")(MIT)에 의해 [미국](../Page/미국.md "wikilink")에 [특허](../Page/특허.md "wikilink")로 등록되었고, [2000년](../Page/2000년.md "wikilink") [9월 21일에](../Page/9월_21일.md "wikilink") 그 특허가 만료되었다.

## 방식

### 개요

RSA는 두 개의 **키**를 사용한다. 여기서 키란 메시지를 열고 잠그는 상수(constant)를 의미한다. 일반적으로 많은 공개키 알고리즘의 **공개키**(public key)는 모두에게 알려져 있으며 메시지를 암호화(encrypt)하는데 쓰이며, 암호화된 메시지는 **개인키**(private key)를 가진 자만이 복호화(decrypt)하여 열어볼 수 있다. 하지만 RSA 공개키 알고리즘은 이러한 제약조건이 없다. 즉 개인키로 암호화하여 공개키로 복호화할 수도 있다.

공개키 알고리즘은 누구나 어떤 메시지를 암호화할 수 있지만, 그것을 해독하여 열람할 수 있는 사람은 개인키를 지닌 단 한 사람만이 존재한다는 점에서 대칭키 알고리즘과 차이를 가진다.

RSA는 소인수 분해의 난해함에 기반하여, 공개키만을 가지고는 개인키를 쉽게 짐작할 수 없도록 디자인되어 있다.

보다 이해하기 쉬운 예를 들자면, A라는 사람에게 B라는 사람이 메시지를 전하고자 할 때 B는 A의 열린 자물쇠를 들고 와 그의 메시지를 봉인(공개키 암호화 과정에 해당)하고, 그런 다음 A에게 전해 주면, 자물쇠의 열쇠(개인키에 해당)를 가지고 있는 A가 그 메시지를 열어보는(개인키 복호화 과정에 해당) 식이 된다. 중간에 그 메시지를 가로채는 사람은 그 열쇠를 가지고 있지 않으므로 메시지를 열람할 수 없다.

메시지와 공개키 모두를 알 수 있다면 변조된 메시지를 보낼 수 있기 때문에, 실제로는 수신측의 공개키만을 사용하여 암호화하는 경우는 드물다. 송수신 양측의 키쌍을 사용하는 방법으로는 A의 개인키로 암호화 -\> B의 공개키로 암호화 한 메시지를 전달하고 복호화 과정은 B의 개인키로 복호화 -\> A의 공개키로 복호화로 구성된 방식이 일반적이다. RSA의 디자인 상, 그 열쇠(개인키에 해당)는 자물쇠의 형태(공개키에 해당)만 보고서는 쉽게 제작할 수가 없게 되어 있다.

### 키의 생성

A와 B가 보안이 보장되어 있지 않은 환경에서 서로 비밀 메시지를 주고 받고 싶다고 가정하자. B가 A에게 메시지를 전달하기 위해서는 A의 공개키가 필요하다. A는 아래와 같은 방법을 통해 그만의 공개키와 개인키를 제작한다.

p 와 q 라고 하는 두 개의 서로 다른 (\(p \ne q\)) [소수를](../Page/소수_\(수론\).md "wikilink") 고른다.

1.  두 수를 곱하여 \(N = p q \,\) 을 찾는다.
2.  \(\varphi(N) = (p-1)(q-1) \,\) 를 구한다.
3.  \(\varphi(N)\) 보단 작고, \(\varphi(N)\)와 [서로소](https://ko.wikipedia.org/wiki/서로소 "wikilink")인 정수 *e*를 찾는다.
4.  [확장된 유클리드 호제법을](https://ko.wikipedia.org/wiki/유클리드_호제법#호제법의_확장 "wikilink") 이용하여 \(d\times e\)를 \(\varphi(N)\)로 나누었을 때 나머지가 1인 정수 *d*를 구한다. (\(d e \equiv 1 \pmod{\varphi(N)}\))

A의 공개키는 위에서 구한 두 개의 숫자로 이루어진 \<*N*, *e*\>이고, 개인키는 \<*N*, *d*\>이다. A는 \<*N*, *e*\>만을 B에게 공개하고, B는 이 공개키를 사용하여 자신의 메시지를 암호화하게 된다. 여기서 *p*와 *q*의 보안은 매우 중요하다. 이를 가지고 *d*와 *e*의 계산이 가능하기 때문이다. 그리하여 공개키와 개인키가 생성이 된 후에는 이 두 숫자를 지워버리는 것이 안전하다.

### 암호화

B가 *M*이란 메시지를 A에게 보내고 싶다고 하자. 일단 B는 이 *M을* *N*보다 작은 숫자 m으로 변환한다. (이 변환법(padding scheme)은 A에게도 미리 알려져 있어야 한다. 이를테면, 메시지를 토막내어 하나의 메시지가 일정 수의 비트를 넘지 않게 하는 방법이 있다. 하지만 실제로는 이중보안을 위해 더욱 복잡한 변환법이 사용된다.) 그리고 B는 A의 공개키 \<*N*, *e*\>를 획득하고, 다음과 같이 *c*를 계산한다.

  -
    \(c = m^e \mod{N}\)

그리고 이 *c*를 A에게 보낸다.

### 복호화

A는 암호화된 메시지 *c*를 B에게서 건네받았고, *N*과 *d*를 알고 있다. 다음 식을 통해 *m*을 찾는다.

  -
    \(m = c^d \mod{N}\)

위에서 설명하였듯 *m*을 가지고 A는 *M*을 찾아낼 수 있는 방법을 알고 있다.

### 증명

이 해독법이 가능한 이유는 다음과 같다.

  -
    \(c^d \equiv (m^e)^d \equiv m^{ed} \equiv m^{k(p-1)(q-1)+1} \equiv m \pmod{N}\).

마지막 등식이 성립하는 이유는 다음과 같다. 위의 식에서 *mod N* 대신 *mod p* 사용하여 풀이했을 때,

  -
    \(m^{k(p-1)(q-1)+1} \equiv (m^{p-1})^{k(q-1)}m \pmod{p}\)

가 된다. *p*가 소수이므로, m이 p의 배수가 아니라면 서로소이므로 [페르마의 소정리를](../Page/페르마의_소정리.md "wikilink") 다음 식과 같이 적용할 수 있다. 만약 m이 p의 배수라면 양변이 p의 배수이므로 0과 동치가 되어 역시 다음 식이 성립된다.

  -
    \((m^{p-1})^{k(q-1)}m \equiv 1^{k(q-1)}m \equiv m \pmod{p}\)

*mod q*를 사용하여도 똑같은 풀이가 가능하다. *N* = *pq* 이므로, *mod N*에도 같은 식이 성립하게 된다.

### RSA증명 영문버전에 대한 상세 번역

RSA의 정확성 검증관련하여 2가지 방안으로 설명코자 한다.

#### <u>페르마의 소정리를 이용한 검증</u>

첫번째 방법은 페르마의 소정리를 이용하여 검증하는 방법으로 다음과 같다.

RSA의 정확성에 대한 검증은 페르마의 소정리에 근거하고 있다.

이 정리(theorem)는 ***p***가 소수이고, ***p***가 정수 ***a***를 나눌 수 없다면 \(a^{p-1}\equiv1\pmod{p}\)이 성립함을 보여주고 있다.

***p***와 ***q***가 별개의 소수이고 ***e***와 ***d***가 양의 정수이면서 \(ed\equiv1\pmod{\lambda({pq})}\)를 만족한다면

모든 정수 **m**에 대해

> \(m^{ed}\equiv m \pmod{pq}\)

이 성립함을 보이고자 한다.

\(\lambda(pq)\)는 구성식에 의해 **p–1**과 **q–1**의 최소공배수로, **p-1**과 **q-1**로 나누어 질 수 있기 때문에 **0** 또는 **양수 h**와 **k**에 대하여

> \(ed-1=h(p-1)=k(q-1)\)

와 같이 표현할 수 있다.

(주: 특히, 위의 설명은 (**p-1)(q-1)**이 **λ(pq)** 또는 **λ(pq)**가 **(p-1)&(q-1)**로 나누어질 수 있기 때문에 어떤 **e**와 **d**에 대하여도 합동식 \(ed\equiv 1 \pmod{(p-1)(q-1)}\)이 성립함을 나타내고 있다.

그러나 **RSA**의 최근 구현에서,약하지만 충분 조건\<\(ed\equiv1\pmod{\lambda({pq})}\)\>을 만족하는 **reduced private exponent d**를 사용하는 것이 일반적이다)

두개의 숫자 **m<sup>ed</sup>와 m이\(\mod{pq}\)**에 대하여 합동인지, \(\mod{pq}\)**가\(\mod{p}\) 와\(\mod{q}\)** 각각의 경우에도 합동인지를 확인하기 위해(이 부문은 **CRT**검증의 부분이며, 중요한 부분은 아니지만) 아울러, **\(m^{ed}\equiv m \pmod{p}\)** 인지를 알아 보기위해,

두가지의 케이스를 고려해 보자 **m ≡ 0 (mod p) and m ≢ 0 (mod p)**.

첫번째 Case의 경우 **m**이 **p**의 배수이므로, \(m^{ed}\)가 **p**의 배수가 된다.

따라서 **m<sup>ed</sup>는 mod p**에 대하여 나머지가 **zero**인 합동이다.

두번째 Case의 경우

> **\(m^{ed} = m^{ed - 1} m = m^{h(p - 1)} m = (m^{p - 1})^h m \equiv 1^h m \equiv m \pmod{p}\)**

관련하여, 페르마의 소정리를 이용하여 **m<sup>p−1</sup> mod p**를 **1**로 대체하면 \(m^{ed}=m\pmod{p}\)가 성립함을 알수 있다.

**mod q**의 경우에도 유사한 방법으로 수행하여

첫번째 Case의 경우 **m<sup>ed</sup>**는 **q**의 배수이므로, **m<sup>ed</sup>**는 **mod q**와 나머지가 **zero**인 합동이다.

두번째 Case의 경우 **\[\(m^{ed} = m^{ed - 1} m = m^{k(q - 1)} m = (m^{q - 1})^k m \equiv 1^k m \equiv m \pmod{q}\)\]**

관련하여, 페르마의 소정리를 이용하여 **m<sup>q−1</sup> mod q**를 **1**로 대체하면

**\(m^{ed}\equiv m \pmod{q}\)**가 성립함을 알수 있다.

이것으로 어떤 정수 **m**, 그리고 **e**, **d** 관련하여, 다음의 합동식이 성립함을 검증하였다. \[***ed ≡ 1 (mod λ : (pq)**, **(m<sup>e</sup>)<sup>d</sup> ≡ m(mod pq)*****\]**

#### <u>오일러의 정리를 이용한 검증</u>

두번째 방법은 오일러의 정리를 이용해 검증을 하고자 한다.

Rivest, Shamir, Adleman의 논문\[2\]은 페르마의 소정리를 이용하여 RSA의 동작원리를 설명했지만, 오일러의 정리를 이용해 증명하는 것이 일반적이다.

\(N=pq\) (두 개의 서로 다른 소수 ***p***와 ***q***의 곱 ***N***)과 \(ed\equiv 1\pmod{\phi (n)}\) 를 만족하는 양의 정수 ***e***와 ***d***를 이용해

> \(m^{ed}\equiv m\pmod{n}\)

를 보이고자 한다.

***e***와 ***d***가 양수이기 때문에 \(ed=1+h\phi(n)\)라고 쓸 수 있다.(***h***는 음이 아닌 정수)

***m***을 ***n***과 서로소라고 가정하면,

> \(m^{ed}=m^{1+h\phi(n)}=m(m^{\phi(n)})^h\equiv m(1)^h\equiv m\pmod{n}\)

끝에서 두번째 합동식 \(m(m^{\phi(n)})^h\equiv m(1)^h\) 는 오일러의 정리에 따른 것이다.

좀 더 일반적으로 \(ed\equiv1 \pmod{\lambda (n)}\)를 만족하는 임의의 ***e***와 ***d***는,

***n***과 서로소인 ***m***은 \(m^{\lambda (n)}\equiv1\pmod{n}\)라고 명시된 Carmichael의 '오일러 이론의 일반화'를 보면 알 수 있다.

***m***이 ***n***과 서로소가 아니면 이 이론은 성립하지 않는다.

매우 드문 확률(\(\frac{1}{p}+\frac{1}{q}-\frac{1}{pq}\)의 비율)이지만 이 경우에도 합동은 성립한다.

\(m\equiv0\pmod{p}\)나 \(m\equiv0\pmod{q}\), 그리고 이 경우는 이전의 증명으로 해결할 수 있다.

### 예제

아래는 작은 수를 이용해 암호화 방식을 예로 든 것이다.

공개 키와 개인 키 생성 과정은 다음과 같다.

1.  서로 다른 두 소수를 선택한다.
      -
        예를 들어 \(p = 61\)과 \(q = 53\)을 선택했다고 하자.
2.  \(N = p q\) 를 계산한다.
    \[N = 61 \times 53 = 3233\].
3.  \(N\)의 [오일러 피 함수](../Page/오일러_피_함수.md "wikilink") \(\phi(N) = (p-1)(q-1)\) 를 계산한다.
    \[\phi(3233) = (61 - 1)(53 - 1) = 3120244444\].
4.  \(1 < e < 3120\)인 숫자 \(e\) 가운데 \(\phi(N)\)과 [서로소인](https://ko.wikipedia.org/wiki/서로소_정수 "wikilink") 임의의 숫자를 선택한다.
    \[e = 17\]을 선택하자. .
5.  \(e\text{ (mod }\phi(N)\text{)}\)에 대해 곱의 [역원](https://ko.wikipedia.org/wiki/역원 "wikilink"), 즉 \(e d \text{ (mod }\phi(N)\text{)}=1\) 인 숫자 \(d\)를 계산한다.
    \[17 \times 2753 = 46801 = 1 \text{ (mod 3120) }\]
    \[d = 2753\].

<!-- end list -->

  -
    **공개 키**는 (\(N = 3233\), \(e = 17\))이며, 평문 \(m\)은 다음 함수로 암호화할 수 있다. \(m^{17}\text{ (mod }3233\text{)}\)

<!-- end list -->

  -
    **개인 키**는 (\(N = 3233\), \(d = 2753\))이며, 암호문 \(c\)는 다음 함수로 복호화할 수 있다. \(c^{2753}\text{ (mod }3233\text{)}\)

예를 들어 평문 \(m = 65\)는 다음과 같이 암호화된다

\[c = 65^{17}\text{ (mod }3233\text{)} = 2790\].

암호문 \(c = 2790\)은 다음과 같이 복호화된다

\[m = 2790^{2753}\text{ (mod }3233\text{)} = 65\].

위는 수학적인 관점에서의 복호화이고 실제 프로그래밍으로 구현시 pq같은 거대한 수의 연산은 부담이 되므로 유명한 암호화 라이브러리(OpenSSL, Java and .NET)들에서는 [중국인의 나머지 정리를](../Page/중국인의_나머지_정리.md "wikilink") 기초로 컴퓨터 연산에 효율적인 복호화를 수행한다. pq보다 작은 수인 p, q를 모듈러로 개별 연산 후 조합하는 방식을 취하므로 이 경우 p, q값을 보존하고 있어야 한다.

\(d_p\), \(d_q\), \(q_{Inv}\)는 복호화시 항상 사용되는 값들이므로 미리 계산해 저장해둔다.

  - \(d_p = d\text{ (mod }(p-1)\text{)} = 2753 \text{ (mod } (61-1)\text{)} = 53\)
  - \(d_q = d\text{ (mod }(q-1)\text{)} = 2753 \text{ (mod } (53-1)\text{)} = 49\)
  - \(q_{Inv} = q^{-1} \text{ (mod } p\text{)} = 53^{-1} \text{ (mod } 61\text{)} = 38\)

암호문은 다음과 같이 복호화된다.

  - \(m_1 = c^{d_p} \text{ (mod } p\text{)} = 2790^{53} \text{ (mod } 61\text{)} = 4\)
  - \(m_2 = c^{d_q} \text{ (mod } q\text{)} = 2790^{49} \text{ (mod } 53\text{)} = 12\)
  - \(h = (q_{Inv} \times (m_1 - m_2)) \text{ (mod } p\text{)} = (38 \times -8) \text{ (mod } 61\text{)} = 1\)
  - \(m = m_2 + h \times q = 12 + 1 \times 53 = 65\)

결과는 같지만 더 작은 수를 이용해 계산하므로 연산이 빨라진다. 그리고 모듈러 연산이므로 h\<p, 따라서 h의 최대값은 p-1, 마찬가지로 m2의 최대값은 q-1이므로 m2 + hq의 최대값은 q-1 + (p-1)q = pq-1이다. 이 값은 반드시 pq보다 작으므로 pq보다 큰 수인지 체크해서 나누는 과정을 수행할 필요 없이 바로 평문이 된다. 즉 복호화에서 연산부담이 되는 매우 큰 수 pq의 연산을 배제할 수 있게 된다.

### d test code (javascript)

``` javascript
<script>
<!-- this is tested on mozilla firefox 47.0 -->
function modular_multiplicative_inverse() {

var a =  Math.abs(document.form.e.value);
var n = Math.abs(document.form.mod.value);

   var t  = 0;
   var nt = 1;
   var r  = n;
   var nr = a % n;

        if (n < 0){
            n = -n;
        }
        if (a < 0){
            a = n - (-a % n);
        }
        while (nr !== 0) {
            var quot= (r/nr) | 0;
            var tmp = nt;  nt = t - quot*nt;  t = tmp;
                tmp = nr;  nr = r - quot*nr;  r = tmp;
        }
        if (r > 1) { return -1; }
        if (t < 0) { t += n; }

alert("d value="+t);

        return t;

    }
</script>
<html>
<form name="form" >
e <input type="text" name="e">
mod() <input type = "text" name="mod">
</form>
<a href="javascript:void(0);" onclick=modular_multiplicative_inverse();>Click me to get the inverse value of mod for d...</a>
</html>
```

## 각주

## 외부 링크

  - [A Method for Obtaining Digital Signatures and Public-Key Cryptosystems](http://people.csail.mit.edu/rivest/Rsapaper.pdf) R. Rivest, A. Shamir, L. Adleman, Communications of the ACM, Vol. 21 (2), 1978, pages 120--126.

[분류:암호학](https://ko.wikipedia.org/wiki/분류:암호학 "wikilink")

1.  <http://www.bristol.ac.uk/graduation/honorary-degrees/hondeg08/cocks.html>
2.