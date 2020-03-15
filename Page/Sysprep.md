> This article is converted from Wikipedia: [Sysprep](https://ko.wikipedia.org/wiki/Sysprep).


**Sysprep**(시스프랩, System Preparation의 준말)은 [마이크로소프트 윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 운영 체제를 배포하기 위한 [마이크로소프트](https://ko.wikipedia.org/wiki/마이크로소프트 "wikilink")사의 시스템 준비 유틸리티이다.

## 역사

Sysprep은 [윈도 NT 4.0에](https://ko.wikipedia.org/wiki/윈도_NT_4.0 "wikilink") 처음 도입되었다. 그 뒤로 [윈도 2000](https://ko.wikipedia.org/wiki/윈도_2000 "wikilink"), [윈도 XP에도](https://ko.wikipedia.org/wiki/윈도_XP "wikilink") 도입되어 마이크로소프트 웹사이트에서 내려받거나 윈도 CD를 통해 이용할 수 있다. [윈도 비스타는](https://ko.wikipedia.org/wiki/윈도_비스타 "wikilink") Sysprep의 독립 버전인 [하드웨어 추상화 계층](https://ko.wikipedia.org/wiki/하드웨어_추상화_계층 "wikilink") (HAL)이 포함된 최초의 마이크로소프트 운영 체제이다.

## 목적

데스크톱 배포는 일반적으로 [디스크 복제](https://ko.wikipedia.org/wiki/디스크_복제 "wikilink") 응용 프로그램들을 통해 수행된다. Sysprep은 [디스크 이미지를](../Page/디스크_이미지.md "wikilink") 통한 디스크 복제와 복원을 위해 운영 체제를 준비하는 데 사용할 수 있다.

윈도 운영 체제 설치는 여러 대의 컴퓨터에 디스크 이미지를 저장하고 배포하기 전에 설치를 진행할 때마다 필요한 수많은 고유 요소를 포함하고 있다.

  - [컴퓨터 이름](https://ko.wikipedia.org/wiki/컴퓨터_이름 "wikilink")\[1\]
  - [보안 식별자](../Page/보안_식별자.md "wikilink") (SID)
  - 드라이버 캐시

Sysprep은 설치 과정 동안에 새로운 컴퓨터 이름, 고유 보안 식별자, 사용자 정의 드라이버 캐시 데이터베이스의 작성을 허용함으로써 이러한 문제들을 해결한다.

관리자들은 SetupMgr.exe (윈도 XP)나 [시스템 이미지 관리자](https://ko.wikipedia.org/wiki/시스템_이미지_관리자 "wikilink") (윈도 비스타)와 같은 도구들을 사용하여 시스템이 새로운 컴퓨터를 배포하기 위한 [응답 파일들을](https://ko.wikipedia.org/wiki/설치_\(컴퓨터_프로그램\) "wikilink") 만들 수 있다.

## 각주

<references />

## 외부 링크

  - [윈도 XP의 성공적인 배포를 위한 Sysprep 도구 이용법](http://support.microsoft.com/default.aspx?scid=kb;en-us;302577)
  - [Sysprep 이미지에서 "하드웨어 장치를 찾을 수 없습니다"](http://support.microsoft.com/default.aspx?scid=kb;en-us;837691)
  - [윈도 XP용 Sysprep의 새로운 기능 설명](http://support.microsoft.com/default.aspx?scid=kb;en-us;282190)
  - [Informational guide on how to use Sysprep for deploying Windows 2000/XP](http://www.vernalex.com/guides/sysprep)

[분류:윈도우 구성 요소](https://ko.wikipedia.org/wiki/분류:윈도우_구성_요소 "wikilink")

1.  [Force Sysprep to Prompt for a Computer Name During Mini-Setup in Windows XP | Capitalhead.com](http://capitalhead.com/articles/force-sysprep-to-prompt-for-a-computer-name-during-mini-setup-in-windows-xp.aspx)