> This article is converted from Wikipedia: [Smack \(소프트웨어\)](https://ko.wikipedia.org/wiki/Smack_\(소프트웨어\)).


**Smack** (전체 이름: **Simplified Mandatory Access Control Kernel**)은 [리눅스 커널](../Page/리눅스_커널.md "wikilink") [보안 모듈로서](../Page/리눅스_보안_모듈.md "wikilink") 데이터와 프로세스의 상호 작용을, 커스텀 강제적 접근 통제 규칙들을 사용해서 본연의 목적처럼 단순하게, 악의적인 조작으로부터 보호한다.\[1\] 이것은 리눅스 2.6.25 이후로 공식적으로 합쳐졌으며,\[2\] [미고](../Page/미고_\(운영_체제\).md "wikilink") 모바일 운영 체제를 위한 주요한 접근 통제 메커니즘이다.\[3\]\[4\] 이것은 또한 [타이젠](../Page/타이젠.md "wikilink") 아키텍처에서 HTML5 웹 애플리케이션들을 [샌드박싱하거나](https://ko.wikipedia.org/wiki/샌드박스_\(컴퓨터_보안\) "wikilink"),\[5\] 임베디드 장치 개발을 위한 상용 윈드 리버 리눅스 솔루션,\[6\]\[7\] 그리고 [필립스](../Page/필립스.md "wikilink") 디지털 TV 제품들에서 사용된다.\[8\]

## 설계

Smack은 세 요소로 구성되어 있다:

  - [리눅스 보안 모듈로서](../Page/리눅스_보안_모듈.md "wikilink") 구현된 커널 모듈. 이것은 확장 속성을 지원하는 [파일 시스템에서](../Page/파일_시스템.md "wikilink") 잘 동작한다.
  - 장치 파일들이 정확한 Smack 속성을 가지며 Smack 설정을 로드한다는 것을 보장하는 스타트업 스크립트.
  - Smack 확장 파일 속성을 인식하게 해주는 [GNU 코어 유틸리티의](../Page/GNU_코어_유틸리티.md "wikilink") 패치 집합들. 비지박스에 대한 비슷한 패치들 또한 생성된다. Smack은 사용자 공간 지원을 필요치 않는다.\[9\]

## 비판

Smack은 동등한 기능을 제공하는 [SELinux](../Page/보안_강화_리눅스.md "wikilink") 보안 정책 대신 새로운 LSM 모듈로서 쓰여졌다는 비판이 있어왔다. 이러한 SELinux 정책들은 제안되었지만 입증되지는 않았다. Smack의 저자는 SELinux의 복잡한 설정 문법과 Smack과 SELinux 설계의 다른 철학으로 인해 실용적이지 않다고 답했다.\[10\]

## 각주

## 더 읽어보기

  -
  -
  -

  -
  -
  -
  -
[분류:2008년 소프트웨어](https://ko.wikipedia.org/wiki/분류:2008년_소프트웨어 "wikilink") [분류:리눅스 커널 특징](https://ko.wikipedia.org/wiki/분류:리눅스_커널_특징 "wikilink") [분류:리눅스 보안 소프트웨어](https://ko.wikipedia.org/wiki/분류:리눅스_보안_소프트웨어 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.