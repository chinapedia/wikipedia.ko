> This article is converted from Wikipedia: [LU 감소](https://ko.wikipedia.org/wiki/LU_감소).


**LU 감소**(LU reduction) 또는 **LU 감소 알고리즘**은 [LU 분해와](../Page/LU_분해.md "wikilink") 관련된 [알고리즘](../Page/알고리즘.md "wikilink")이다. 이 용어는 대개 [슈퍼 컴퓨터](https://ko.wikipedia.org/wiki/슈퍼_컴퓨터 "wikilink") 및 고도의 [병렬 컴퓨팅의](../Page/병렬_컴퓨팅.md "wikilink") 맥락에서 사용된다. 이는 [벤치마킹](../Page/벤치마킹.md "wikilink") 알고리즘으로도 사용된다. 즉, 서로 다른 컴퓨터의 속도를 비교 측정하는데 유용하다. LU 분해 알고리즘 예제는 Java Grande 2000 Special Issue(2001)에서 찾을 수 있다.\[1\]\[2\] 병렬화 된 버전은 일반적으로 [행렬](../Page/행렬.md "wikilink") 행에 대한 작업을 하위 노드의 단일 프로세서에 배포하고 결과를 메인 프로세서상에서 전체 행렬과 동기화한다.\[3\]

## 같이 보기

  - [LU 분해](../Page/LU_분해.md "wikilink")
  - [베오울프 클러스터](../Page/베오울프_클러스터.md "wikilink")

## 참고

<references/>

[분류:컴퓨터 그래픽스](https://ko.wikipedia.org/wiki/분류:컴퓨터_그래픽스 "wikilink") [분류:선형대수학](https://ko.wikipedia.org/wiki/분류:선형대수학 "wikilink") [분류:응용수학](https://ko.wikipedia.org/wiki/분류:응용수학 "wikilink") [분류:병렬 컴퓨팅](https://ko.wikipedia.org/wiki/분류:병렬_컴퓨팅 "wikilink")

1.  J. Oliver, J. Guitart, E. Ayguadé, N. Navarro and J. Torres. Strategies for Efficient Exploitation of Loop-level Parallelism in Java. Concurrency and Computation: Practice and Experience(Java Grande 2000 Special Issue), Vol.13 (8-9), pp. 663–680. ISSN 1532-0634, July 2001
2.  J. Guitart, X. Martorell, J. Torres, and E. Ayguadé, Improving Java Multithreading Facilities: the Java Nanos Environment, Research Report UPC-DAC-2001-8, Computer Architecture Department, Technical University of Catalonia, March 2001
3.  Arturo González-Escribano, Arjan J. C. van Gemund, Valentín Cardeñoso-Payo et al., Measuring the Performance Impact of SP-Restricted Programming in Shared-Memory Machines, In Vector and Parallel Processing — VECPAR 2000, Springer Verlag, pp. 128–141, , 2000