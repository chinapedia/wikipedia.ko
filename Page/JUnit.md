> This article is converted from Wikipedia: [JUnit](https://ko.wikipedia.org/wiki/JUnit).


**JUnit**(제이유닛)은 [자바 프로그래밍 언어용](../Page/자바_\(프로그래밍_언어\).md "wikilink") [유닛 테스트](../Page/유닛_테스트.md "wikilink") [프레임워크이다](../Page/소프트웨어_프레임워크.md "wikilink"). JUnit은 [테스트 주도 개발](../Page/테스트_주도_개발.md "wikilink") 면에서 중요하며 [SUnit](https://ko.wikipedia.org/wiki/SUnit "wikilink")과 함께 시작된 [XUnit](../Page/XUnit.md "wikilink")이라는 이름의 [유닛 테스트](../Page/유닛_테스트.md "wikilink") 프레임워크 계열의 하나이다.

JUnit은 컴파일 타임에 [JAR로서](../Page/JAR_\(파일_포맷\).md "wikilink") 링크된다. 프레임워크는 JUnit 3.8 이하의 경우 `junit.framework` 패키지 밑에 상주하며, JUnit 4 이상의 경우 `org.junit` 패키지 밑에 상주한다.

깃허브에 호스팅된 10,000개 자바 프로젝트를 대상으로 한 2013년 수행된 연구 조사에 따르면 JUnit([slf4j-api과](https://ko.wikipedia.org/wiki/SLF4J "wikilink") 연결된)은 가장 흔히 포함시킨 외부 라이브러리였다. 각 라이브러리는 프로젝트 가운데 30.7%에 사용되었다.\[1\]

## JUnit 테스트 픽스처 예시

JUnit 테스트 픽스처(test fixture)는 자바 객체이다. 구 버전의 JUnit의 경우 픽스처는 `junit.framework.TestCase`로부터 상속해야 했으나 JUnit 4의 새 테스트는 이렇게 하지 않는다.\[2\] 테스트 메소드는 `@Test` [어노테이션을](https://ko.wikipedia.org/wiki/자바_어노테이션 "wikilink") 통해 어노테이트해야 한다. 필요한 경우,\[3\]

``` Java
import org.junit.*;

public class FoobarTest {
    @BeforeClass
    public static void setUpClass() throws Exception {
        // Code executed before the first test method
    }

    @Before
    public void setUp() throws Exception {
        // Code executed before each test
    }

    @Test
    public void testOneThing() {
        // Code that tests one thing
    }

    @Test
    public void testAnotherThing() {
        // Code that tests another thing
    }

    @Test
    public void testSomethingElse() {
        // Code that tests something else
    }

    @After
    public void tearDown() throws Exception {
        // Code executed after each test
    }

    @AfterClass
    public static void tearDownClass() throws Exception {
        // Code executed after the last test method
    }
}
```

## 포팅

  - [액션스크립트](../Page/액션스크립트.md "wikilink") ([FlexUnit](http://www.flexunit.org/))
  - [에이다](../Page/에이다_\(프로그래밍_언어\).md "wikilink") ([AUnit](http://libre.adacore.com/libre/tools/aunit/))
  - [C](../Page/C_\(프로그래밍_언어\).md "wikilink") ([CUnit](http://cunit.sourceforge.net/))
  - [C\#](../Page/C_샤프.md "wikilink") ([NUnit](https://ko.wikipedia.org/wiki/NUnit "wikilink"))
  - [C++](https://ko.wikipedia.org/wiki/C++ "wikilink") ([CPPUnit](https://ko.wikipedia.org/wiki/CPPUnit "wikilink"), [CxxTest](http://cxxtest.com/))
  - [어도비 콜드퓨전](../Page/어도비_콜드퓨전.md "wikilink") ([MXUnit](https://ko.wikipedia.org/wiki/MXUnit "wikilink"))
  - [델파이](../Page/델파이.md "wikilink") ([DUnit](https://ko.wikipedia.org/wiki/DUnit "wikilink"))
  - [얼랭](../Page/얼랭.md "wikilink") ([EUnit](http://www.erlang.org/doc/apps/eunit/chapter.html))
  - [에펠](../Page/에펠_\(프로그래밍_언어\).md "wikilink") ([Auto-Test](https://docs.eiffel.com/book/eiffelstudio/using-autotest))
  - [포트란](../Page/포트란.md "wikilink") ([fUnit](https://ko.wikipedia.org/wiki/fUnit "wikilink"), [pFUnit](https://ko.wikipedia.org/wiki/pFUnit "wikilink"))
  - [프리 파스칼](../Page/프리_파스칼.md "wikilink") ([FPCUnit](http://camelos.sourceforge.net/fpcUnit.html))
  - [Golang](../Page/Go_\(프로그래밍_언어\).md "wikilink") ([Go JUnit report](https://github.com/jstemmer/go-junit-report))
  - [하스켈](../Page/하스켈.md "wikilink") ([HUnit](http://hackage.haskell.org/package/HUnit))
  - [자바스크립트](../Page/자바스크립트.md "wikilink") ([JSUnit](https://jasmine.github.io/))
  - [마이크로소프트 닷넷](https://ko.wikipedia.org/wiki/마이크로소프트_닷넷 "wikilink") ([NUnit](https://ko.wikipedia.org/wiki/NUnit "wikilink"))
  - [오브젝티브-C](../Page/오브젝티브-C.md "wikilink") ([OCUnit](https://web.archive.org/web/20111013123951/http://www.sente.ch/software/ocunit/))
  - [OCaml](../Page/OCaml.md "wikilink") ([OUnit](http://ounit.forge.ocamlcore.org))
  - [펄](../Page/펄.md "wikilink") (\[<http://metacpan.org/module/Test>::Class Test::Class\], \[<http://metacpan.org/module/Test>::Unit Test::Unit\])
  - [PHP](../Page/PHP.md "wikilink") ([PHPUnit](../Page/PHPUnit.md "wikilink"))
  - [파이썬](../Page/파이썬.md "wikilink") ([PyUnit](https://ko.wikipedia.org/wiki/PyUnit "wikilink"), [junit-xml](https://pypi.org/project/junit-xml/))
  - [Qt](../Page/Qt_\(프레임워크\).md "wikilink") (QTestLib)
  - [R](../Page/R_\(프로그래밍_언어\).md "wikilink") ([RUnit](http://RUnit.sourceforge.net/))
  - [루비](../Page/루비_\(프로그래밍_언어\).md "wikilink") ([JUnit for Rspec](https://github.com/sj26/rspec_junit_formatter))

## 같이 보기

  - [TestNG](https://ko.wikipedia.org/wiki/TestNG "wikilink")
  - [모의 객체](../Page/모의_객체.md "wikilink")
  - [Mockito](https://ko.wikipedia.org/wiki/Mockito "wikilink"), [PowerMock](https://ko.wikipedia.org/wiki/PowerMock "wikilink")
  - [JUnit-Tools](http://www.junit-tools.org/)
  - [EvoSuite](https://ko.wikipedia.org/wiki/EvoSuite "wikilink")
  - [JUnit Foundation](https://github.com/Nordstrom/JUnit-Foundation)

## 각주

## 외부 링크

  -
  - [An early look at JUnit 4](http://www.ibm.com/developerworks/java/library/j-junit4/)

  - [JUnit Presentation](http://www.methodsandtools.com/tools/tools.php?junit)

  - [JUnit Tutorials](https://web.archive.org/web/20150128114403/http://memorynotfound.com/category/testing/junit/)

[분류:크로스 플랫폼 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_소프트웨어 "wikilink") [분류:익스트림 프로그래밍](https://ko.wikipedia.org/wiki/분류:익스트림_프로그래밍 "wikilink") [분류:자바로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:자바로_작성된_자유_소프트웨어 "wikilink") [분류:자바 개발 도구](https://ko.wikipedia.org/wiki/분류:자바_개발_도구 "wikilink") [분류:자바 플랫폼](https://ko.wikipedia.org/wiki/분류:자바_플랫폼 "wikilink") [분류:이클립스 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:이클립스_라이선스_소프트웨어 "wikilink")

1.
2.
3.