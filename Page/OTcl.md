> This article is converted from Wikipedia: [OTcl](https://ko.wikipedia.org/wiki/OTcl).


**OTcl**은 [Tcl](https://ko.wikipedia.org/wiki/Tcl "wikilink")의 [객체 지향](https://ko.wikipedia.org/wiki/객체_지향 "wikilink") 확장이다. 데이비드 웨더롤()이 창안하였다.\[1\]. OTcl은 네트워크 시뮬레이터인 [ns-2에서](https://ko.wikipedia.org/wiki/ns_\(시뮬레이터\) "wikilink") 쓰이고 있다. [유닉스](https://ko.wikipedia.org/wiki/유닉스 "wikilink") 환경에서 동작한다.\[2\]

## 문법 소개

예약어 "Class"를 써서, 클래스를 선언한다. 클래스 내의 메소드들은 단어 "instproc"을 써서 선언한다.\[3\] 변수 "self"는 지금 현재 쓰이고 있는 객체에 대한 포인터이다. C++/Java에서의 "this"와 같은 역할을 한다. 키워드 "-instproc"은 계층(hierarchy)를 나타내기 위해 사용한다.\[4\] 예를 들면, "Class Duck -instproc Bird"라는 것은 클래스 Duck이 클래스 Bird 를 상속한다는 말이 된다. 클래스에 대한 인스턴스를 새로 생성하려면, 프로그래머는 "set new_inst \[new Son\]"라고 적으면 된다. 다음은 코드 예제이다.

`// Sample code in OTcl`
`Class HelloWorld`
`HelloWorld instproc hello {} {`
`   puts "Hello world"`
`}`

`set helloworld [new HelloWorld]`
`//to run`
`$helloworld hello`

## 각주

<references/>

[분류:객체 지향 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:객체_지향_프로그래밍_언어 "wikilink")

1.  [OTcl Project Page](http://otcl-tclcl.sourceforge.net/otcl/)
2.  Sophie-Antipolis [NS Simulator for beginners](http://www-sop.inria.fr/maestro/personnel/Eitan.Altman/COURS-NS/n3.pdf), Lecture notes, 2003-2004, Univ. de Los Andres, Merida, Venezuela and ESSI
3.
4.