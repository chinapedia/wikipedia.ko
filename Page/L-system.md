> This article is converted from Wikipedia: [L-system](https://ko.wikipedia.org/wiki/L-system).


**L-system**(엘 시스템, Lindenmayer system)은 [형식문법](https://ko.wikipedia.org/wiki/형식문법 "wikilink")의 일종으로서, 식물의 성장 프로세스를 기초로 한 다양한 자연물의 구조를 기술하거나 표현을 가능케 하는 [알고리즘](../Page/알고리즘.md "wikilink")이다. 자연물 이외에도 망델브로 집합 반복함수계(Iterated Function System; IFS)와 같이 이른바 자기상사 도형이나 [프랙탈](../Page/프랙탈.md "wikilink") 도형을 생성할 경우에도 사용된다. L-system은 [1968년](../Page/1968년.md "wikilink"), [네덜란드](../Page/네덜란드.md "wikilink") [위트레흐트 대학교](../Page/위트레흐트_대학교.md "wikilink") 대학의 이론생물학자이자 식물학자였던 아리스티드 린덴마이어(Aristid Lindenmayer)에 의해 제창되어 발전되었다.

## 기원

생물학자였던 린덴마이어는 [효모](../Page/효모.md "wikilink")와 [곰팡이](../Page/곰팡이.md "wikilink"), 그리고 [남세균](../Page/남세균.md "wikilink")류의 *Anabaena catenula*와 같은 [조류](https://ko.wikipedia.org/wiki/조류 "wikilink") 등, 다양한 생물의 성장패턴을 연구했다. 이와 같이 L-system은 [단세포생물](https://ko.wikipedia.org/wiki/단세포생물 "wikilink") 또는 단순한 [다세포생물](https://ko.wikipedia.org/wiki/다세포생물 "wikilink")의 성장식, 식물[세포](../Page/세포.md "wikilink")에 있어서 인접한 세포의 상호관계를 기술하기 위해 개발된 것이었다. 이후 L-system은 더욱 고도로 발달한 식물의 형태, 복잡한 분기구조를 기술하기 위한 도구로 발전하게 되었다.

## L-system의 구조

L-system의 기본은 재귀성으로서, 자기상사도형, 프랙탈도형과 같은 형태를 단순히 기술하는 것이 가능하다. 식물과 그외의 형태가 자연스러운 생물구조도 함께 단순히 정의가 되어, 재귀호출의 회수를 늘려, 마치 구조가 성장, 복잡화되어가는 것처럼 보인다. L-system은 [인공생명](../Page/인공생명.md "wikilink")의 생성에도 잘 쓰인다.

L-system의 문법은 [semi-Thue grammar와](https://ko.wikipedia.org/wiki/:en:Semi-Thue_system "wikilink") 닮았다.(→[촘스키 위계](../Page/촘스키_위계.md "wikilink")) 현재, L-system은 아래와 같은 [튜플](../Page/튜플.md "wikilink")로 정의된 "파라메트릭 L-system"로서 일반에 알려져 있다.

  -
    **G** = {*V*, *S*, ω, *P*},

위의 각 요소는 이하의 의미를 갖고 있다.

  - **V**(문자): 치환규칙(다음에 기술하는 **P**)에 의해 순차적으로 바뀌어가는 [변수의](https://ko.wikipedia.org/wiki/변수_\(컴퓨터_과학\) "wikilink") 집합.

L-system의 재귀적인 반복계수가 진행해 갈 때, 무언가로 성장해 나가는 것은 이 **V**의 요소에서부터 만들어지는 문자열이다.

  - **S**: 계산이 진행되어도 변화하지 않는[정수](../Page/정수.md "wikilink")의 집합.
  - **ω**: 시스템의 초기상태를 나타내는**V**의 요소에서 만들어지는 문자열.
  - **P**: **V**를 변화시켜가는 치환규칙의 집합. 각 요소는 예를 들어 (A → AB)와 같이

치환전(치환대상)의 문자열과 치환후의 문자열의 조합에 의해 기술된다.

치환규칙 **P**에 관해, 치환대상이 단독의 문자만일 경우, L-system은 [문맥자유언어](https://ko.wikipedia.org/wiki/문맥자유언어 "wikilink")이다. 한편, 치환규칙이 인접한 문자와의 상호관계까지 고려하는 것일 경우 L-system은 [문맥의존언어](https://ko.wikipedia.org/wiki/문맥의존언어 "wikilink")이다. 또한 치환규칙**P**가 문자에 대해 매번 확실히 적용될 경우 L-system은 "[결정론](../Page/결정론.md "wikilink")적"이다 라고 불리어, D0L-system(deterministic context-free L-system)등으로 불린다. 반대로, 치환규칙의 적용이 [확률](https://ko.wikipedia.org/wiki/확률 "wikilink")에 좌우될 경우엔 "[확률론](../Page/확률론.md "wikilink")적" L-system라고 불린다.

L-system을 그래픽으로 응용하는 경우, L-system이 생성하는 문자열을, 무언가의 형태로 화면상의 도형으로 변환시키지 않으면 안 된다. 예를 들어 *FractInt*라는 프로그램에서는 [로고와](../Page/로고_\(프로그래밍_언어\).md "wikilink") 같이 터틀을 이용하여 그래픽을 생성한다. 결국 프로그램이 L-system의 문자열을 터틀의 제어명령으로 [번역](../Page/번역.md "wikilink")해서 도형을 그려지게 하는 것이다.

## 참고 문헌

  - Przemyslaw Prusinkiewicz - [PDF version available here for free](http://algorithmicbotany.org/papers/#abop)

## 외부 링크

  - [David J. Wright's article on L-systems](https://web.archive.org/web/20081225000136/http://www.math.okstate.edu/mathdept/dynamics/lecnotes/node12.html#SECTION00040000000000000000)
  - [Algorithmic Botany at the University of Calgary](http://algorithmicbotany.org/)
  - [Branching: L-system Tree](http://www.mizuno.org/applet/branching/) L-system을 사용해 나무의 성장을 시물레이션해 보기 [자바 애플릿](../Page/자바_애플릿.md "wikilink")(英語)
  - [Fractint L-System True Fractals](https://web.archive.org/web/20020503212834/http://spanky.triumf.ca/WWW/FRACTINT/lsys/truefractal.html)
  - ["An introduction to Lindenmayer systems", by Gabriela Ochoa](https://web.archive.org/web/20090326080442/http://www.biologie.uni-hamburg.de/b-online/e28_3/lsys.html). Brief description of L-systems and how the strings they generate can be interpreted by computer.
  - ["powerPlant" an open-source landscape modelling software](http://sourceforge.net/projects/pplant/)
  - [*Fractint* home page](https://web.archive.org/web/20080506072938/http://spanky.triumf.ca/www/fractint/fractint.html)

<!-- end list -->

  - ["L-system in Falk arts" The FORMA commurative issue of the conference ISKFA06](http://www.cityfujisawa.ne.jp/~intvsn/)
  - [A simple L-systems generator (Windows)](https://web.archive.org/web/20031220074045/http://www.generation5.org/content/2002/lse.asp)
  - [Lyndyhop: another simple L-systems generator (Windows & Mac)](https://web.archive.org/web/20081204101322/http://www.lab4web.com/chelmiger/lyndyhop/)
  - [An evolutionary L-systems generator (anyos\*)](http://www.cs.ucl.ac.uk/staff/W.Langdon/pfeiffer.html)
  - [L-systems gallery – a tribute to Fractint](http://fractint.oblivion.cz./)
  - ["LsystemComposition"](https://web.archive.org/web/20100616013924/http://pawfal.org/index.php?page=LsystemComposition). Page at Pawfal ("poor artists working for a living") about using L-systems and [genetic algorithms](https://ko.wikipedia.org/wiki/:en:Genetic_algorithms "wikilink") to generate music.
  - [eXtended L-Systems (XL), Relational Growth Grammars, and open-source software platform GroIMP.](http://www.grogra.de/)
  - [A JAVA applet with many fractal figures generated by L-systems.](http://to-campos.planetaclix.pt/fractal/plantae.htm)
  - [L-systems in Architecture; genetic housing.](https://web.archive.org/web/20090225060354/http://www.arch.columbia.edu/Students/Fall2003/Cheng.Chih-Wei/)
  - [L-systems in Plant Growth,Simulation and Visualization (PlantVR).](http://www.somporn.net/)
  - [Musical L-systems: Theory and applications about using L-systems to generate musical structures, from waveforms to macro-forms.](https://web.archive.org/web/20061001043429/http://www.koncon.nl/public_site/220/Sononieuw/NL/thesis-pdf/Stelios%20Manousakis-Musical%20L-systems.pdf)
  - [LSys/JS](https://web.archive.org/web/20090201053112/http://lsysjs.qwert.ch/) - Interactive L-System interpreter using the [Canvas HTML element](https://ko.wikipedia.org/wiki/:en:Canvas_\(HTML_element\) "wikilink").

[분류:프랙탈](https://ko.wikipedia.org/wiki/분류:프랙탈 "wikilink") [분류:형식 언어](https://ko.wikipedia.org/wiki/분류:형식_언어 "wikilink") [분류:컴퓨터 그래픽스 알고리즘](https://ko.wikipedia.org/wiki/분류:컴퓨터_그래픽스_알고리즘 "wikilink")