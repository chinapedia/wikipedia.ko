> This article is converted from Wikipedia: [QUnit](https://ko.wikipedia.org/wiki/QUnit).


**QUnit**은 [자바스크립트](../Page/자바스크립트.md "wikilink") 유닛 테스트 프레임워크이다. 원래 [JQuery](../Page/JQuery.md "wikilink"), [jQuery UI](https://ko.wikipedia.org/wiki/jQuery_UI "wikilink"), [jQuery Mobile을](https://ko.wikipedia.org/wiki/jQuery_Mobile "wikilink") 테스트하기 위해 개발되었으며 모든 자바스크립트 코드를 테스트하기 위한 제네릭 프레임워크이다. 웹 브라우저의 [클라이언트 사이드](../Page/클라이언트_사이드.md "wikilink") 환경과 서버사이드(예: [Node.js](../Page/Node.js.md "wikilink"))를 지원한다.

QUnit의 표명(assertion) 메서드는 [CommonJS](https://ko.wikipedia.org/wiki/CommonJS "wikilink") 유닛 테스트 사양을 준수하며 스스로 QUnit에 의해 어느 정도 영향을 받았다.

## 역사

QUnit은 [존 레식이](../Page/존_레식.md "wikilink") jQuery의 일부로서 처음 개발한 것이다. 2008년, jQuery 유닛 테스트 소스 코드로부터 추출되어 자체 프로젝트로 형성되었으며 이후 QUnit으로 알려지게 되었다. 자신만의 [유닛 테스트를](../Page/유닛_테스트.md "wikilink") 작성하기 위해 사용할 수 있다. QUnit의 초기 버전은 [DOM과의](../Page/문서_객체_모델.md "wikilink") 상호작용을 위해 jQuery를 사용하였으나, 2009년 재작성되어 QUnit은 온전히 독립적인 프로젝트가 되었다.

## 사용 및 예제

  - `QUnit.module(string)` - 하나 이상의 테스트의 묶음인 모듈을 정의한다.
  - `QUnit.test(string, function)` - 테스트를 정의한다.

QUnit은 [표명](../Page/표명.md "wikilink")(assertion) 메서드 집합을 사용하여 유닛 테스트에 시맨틱 의미를 제공한다:\[1\]

  - `assert.ok(boolean, string)` - 지정된 값을 [불리언 참](../Page/불리언_자료형.md "wikilink")(true)으로 [형 변환하도록](https://ko.wikipedia.org/wiki/형_변환 "wikilink") 표명(assert).
  - `assert.equal(value1, value2, message)` - double-equal operator를 사용하여 2개의 값을 비교한다.
  - `assert.deepEqual(value1, value2, message)` - 아이덴티티가 아닌 내용에 기반하여 2개의 값을 비교한다.
  - `assert.strictEqual(value1, value2, message)` - triple-equal operator를 사용하여 2개의 값을 엄밀히(strictly) 비교한다.

기본 예는 다음과 같다:\[2\]

``` javascript
QUnit.test('a basic test example', function (assert) {
  var obj = {};

  assert.ok(true, 'Boolean true');       // passes
  assert.ok(1, 'Number one');            // passes
  assert.ok(false, 'Boolean false');     // fails

  obj.start = 'Hello';
  obj.end = 'Ciao';
  assert.equal(obj.start, 'Hello', 'Opening greet'); // passes
  assert.equal(obj.end, 'Goodbye', 'Closing greet'); // fails
});
```

## 각주

## 외부 링크

  -
  -
[분류:자바스크립트로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:자바스크립트로_작성된_자유_소프트웨어 "wikilink")

1.
2.