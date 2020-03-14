> This article is converted from Wikipedia: [Jini](https://ko.wikipedia.org/wiki/Jini).


**Jini**(발음: 지니)는 서비스 모듈들이 서로 협력하는 방식의 [분산 시스템을](https://ko.wikipedia.org/wiki/분산_컴퓨팅 "wikilink") 위한 네트워크 아키텍처로 [아파치](https://ko.wikipedia.org/wiki/아파치_소프트웨어_재단 "wikilink") River라고도 불린다.

[썬에](https://ko.wikipedia.org/wiki/썬_마이크로시스템즈 "wikilink") 의해 처음 개발되었으며, [오픈 소스](https://ko.wikipedia.org/wiki/오픈_소스 "wikilink") 라이센스인 [아파치 라이센스로](https://ko.wikipedia.org/wiki/아파치_라이센스 "wikilink") 발표되었다. 이후 Jini에 대한 책임은 아파치 산하의 River 프로젝트로 넘어갔다.

## 역사

썬은 1998년 7월 Jini를 발표했다. 1998년 11월 썬은 몇몇 회사들이 Jini를 지원한다고 전했다.

썬의 Jini팀은 항상 Jini가 약어가 아님을 강조했는데, 몇몇 사람들은 이를가지고 "Jini Is Not Initials"라 농담을 하기도 했다. "Jini"는 스와힐리어로 "악마"를 뜻하는데, 이는 영어 "Genie"가 유래한 "신화적인 영혼"을 뜻하는 아랍어에서 가져온 단어다.

## 서비스의 사용

Jini 서비스를 만드는 첫 단계는 룩업 서비스(Lookup Service, LUS)를 찾는 것이다. 이 단계를 디스커버리(discovery) 단계라 부른다. LUS를 발견하면 Jini는 서비스 등록관(Service Registrar) 객체를 서비스에게 전달해주는데, 서비스는 이를 이용해 자기 자신을 룩업 서비스에 등록한다. 이 단계는 조인(join) 단계라 불린다. 이때 서비스는 자신의 ID, 실제 서비스를 구현하는 객체 및 서비스의 여러 속성들을 제공해야 한다.

클라이언트가 어떤 서비스를 사용하고자 해도 마찬가지로 LUS를 찾는데서 시작한다. 이는 클라이언트가 LUS의 위치를 알고있을 경우 유니케스트를 통해 이뤄지고, 혹은 동적인 멀티케스트를 통해서도 가능하다. LUS를 발견하면 마찬가지로 서비스 등록관을 받아, 이를 사용해 특정 서비스를 찾을 수 있다. 이 특정 서비스는 룩업 카탈로그를 보고 종류나 이름 혹은 설명으로 찾을 수 있다. 이후 LUS는 해당 서비스에 직접 접근할 수 있는 자바 프록시 객체를 클라이언트에게 전달해준다. 이렇게 클라이언트가 원하는 서비스의 위치를 미리 알지 않아도 찾을 수 있도록 해주는 기능은 Jini가 [자바 원격 함수 호출에](https://ko.wikipedia.org/wiki/자바_원격_함수_호출 "wikilink") 비해 가지고있는 큰 장점 중 하나다.

## 한계

Jini는 LUS를 사용해 클라이언트와 서버간의 통신을 중개한다. 이러한 중앙집중적 모델은 굉장히 큰 시스템으로 확장하는데 걸림돌이 된다. 하지만 같은 멀티케스트 그룹에 속하는 여러 인스턴스의 LUS를 둬서 수평적인 확장을 통해 이를 해결할 수 있다.

[분류:자바 플랫폼](https://ko.wikipedia.org/wiki/분류:자바_플랫폼 "wikilink") [분류:아파치 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:아파치_라이선스_소프트웨어 "wikilink")