> This article is converted from Wikipedia: [Behat](https://ko.wikipedia.org/wiki/Behat).


**Behat**은 [PHP 프로그래밍 언어로](../Page/PHP.md "wikilink") 개발된 [행위 중심 개발을](https://ko.wikipedia.org/wiki/행위_중심_개발 "wikilink") 위한 테스트 [프레임워크이다](../Page/소프트웨어_프레임워크.md "wikilink"). Behat은 Konstantin Kudryashov가 개발했으며 개발은 [깃허브](../Page/깃허브.md "wikilink")를 통해 이루어지고 있다.

## 목적

Behat은 소프트웨어 개발 프로세스 가운데에서 개발자, 고객, 기타 주주들 간의 대화를 돕기 위해 설계되었다. 소프트웨어의 의도한 동작의 테스트 가능한 예제의 분명한 문서화를 허용한다. Behat 테스트 시나리오는 정의된 패턴에 따른 비즈니스적인 도메인 특화 언어인 [Gherkin](https://ko.wikipedia.org/wiki/Cucumber "wikilink")\[1\]로 개발되었다.

## 예제

"Given" 뒤의 전제 조건은 실행할 PHP 메서드 이름과 일치한다:

``` cucumber
Feature: Function to test description

    Free text

    Scenario: Scenario 1
        Given preconditions
        When actions
        Then results

    Scenario: Scenario 2
        ...
```

## 각주

<references />

## 외부 링크

  -
[분류:PHP 소프트웨어](https://ko.wikipedia.org/wiki/분류:PHP_소프트웨어 "wikilink") [분류:PHP](https://ko.wikipedia.org/wiki/분류:PHP "wikilink")

1.  <https://github.com/cucumber/cucumber/wiki/Gherkin>