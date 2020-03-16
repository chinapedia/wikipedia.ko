> This article is converted from Wikipedia: [Nice \(\)](https://ko.wikipedia.org/wiki/Nice_\(\)).


**`nice`**는 [리눅스](../Page/리눅스.md "wikilink") 등의 [유닉스 계열](../Page/유닉스_계열.md "wikilink") 운영 체제와 [유닉스](../Page/유닉스.md "wikilink")에서 볼 수 있는 프로그램의 하나이다. 동일한 이름의 [커널](../Page/커널_\(컴퓨팅\).md "wikilink") [호출로](../Page/시스템_호출.md "wikilink") 직접 매핑한다. `nice`는 특정한 [우선순위로](../Page/우선순위_큐.md "wikilink") [유틸리티나](../Page/유닉스_명령어_목록.md "wikilink") [셸 스크립트를](../Page/셸_스크립트.md "wikilink") 호출하는데 사용되므로 다른 프로세스보다 [프로세스](../Page/프로세스.md "wikilink")에 CPU 시간을 더 주거나 덜 줄 수 있다. nice의 우선순위 중 -20이 가장 높고, 19가 가장 낮다. 기본 프로세스 우선순위는 부모 프로세스에 종속되며 일반적으로는 0이다. [GNU](../Page/GNU.md "wikilink") [코어 유틸리티에](../Page/GNU_코어_유틸리티.md "wikilink") 포함된 `nice` 버전은 데이비드 맥켄지에 의해 작성되었다.\[1\]

## 이용 및 영향

`nice`는 여러 프로세스가 [CPU의](../Page/중앙_처리_장치.md "wikilink") 제공 가능한 범위를 넘어 더 많은 리소스를 요구할 때 유용하다. 이 상태에서 더 높은 우선순위 프로세스는 더 낮은 우선순위의 프로세스보다 더 큰 덩어리의 CPU 시간을 가진다. 오직 [슈퍼유저](https://ko.wikipedia.org/wiki/슈퍼유저 "wikilink")(루트)만이 더 낮은 값(더 높은 우선순위)으로 nice의 우선순위를 설정할 수 있다. 리눅스에서는 `/etc/security/limits.conf`를 변경함으로써 다른 사용자들이나 그룹들이 낮은 nice 값을 설정하도록 허용한다.\[2\]

사용자가 큰 파일을 압축하고 싶으나 다른 프로세스의 속도를 떨어트리기 원치 않는다면 다음과 같이 실행할 수 있다:

``` console
$ nice -n 19 tar cvzf archive.tgz largefile
```

## 같이 보기

  - [Kill](../Page/Kill.md "wikilink")
  - [Ps (유닉스)](../Page/Ps_\(유닉스\).md "wikilink")
  - [Top (소프트웨어)](../Page/Top_\(소프트웨어\).md "wikilink")
  - [Util-linux](../Page/Util-linux.md "wikilink") ionice

## 각주

## 외부 링크

  -
[분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink") [분류:유닉스 프로세스 및 작업 관리 관련 소프트웨어](https://ko.wikipedia.org/wiki/분류:유닉스_프로세스_및_작업_관리_관련_소프트웨어 "wikilink")

1.  <https://linux.die.net/man/1/nice>
2.