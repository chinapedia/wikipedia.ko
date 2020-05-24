> This article is converted from Wikipedia: [SAM 잠금 도구](https://ko.wikipedia.org/wiki/SAM_잠금_도구).


**SAM 잠금 도구** 또는 **Syskey**([실행 파일의](../Page/실행_파일.md "wikilink") 이름)는 128비트 [RC4](../Page/RC4.md "wikilink") [암호 키를](https://ko.wikipedia.org/wiki/키_\(암호\) "wikilink") 사용하여 [보안 계정 관리자](../Page/보안_계정_관리자.md "wikilink")(SAM) [데이터베이스](../Page/데이터베이스.md "wikilink")를 [암호화](../Page/암호화.md "wikilink")하는 [Windows NT의](https://ko.wikipedia.org/wiki/Windows_NT "wikilink") 구성 요소였다.\[1\]

[윈도우 NT 4.0](../Page/윈도우_NT_4.0.md "wikilink") 서비스 팩 3에서 처음 등장하였으나, RC4 알고리즘이 더 이상 안전하지 않은 것으로 여겨지고 있으며, [랜섬웨어](../Page/랜섬웨어.md "wikilink") 사기의 일부로 사용되면서 [윈도우 10과](../Page/윈도우_10.md "wikilink") [윈도우 서버 2016에서](../Page/윈도우_서버_2016.md "wikilink") 제거되었다. [마이크로소프트](../Page/마이크로소프트.md "wikilink")에서는 공식적으로 [비트로커](../Page/비트로커.md "wikilink")를 대신 사용할 것을 권고하고 있다.\[2\]\[3\]

## 역사

[윈도우 NT 4.0](../Page/윈도우_NT_4.0.md "wikilink") 서비스 팩 3에서 처음 등장한\[4\] SAM 잠금 도구는 SAM 파일의 무단 복제본 소유자가 정보를 추출하지 못하게 하여 [오프라인](https://ko.wikipedia.org/wiki/오프라인 "wikilink") 암호 크래킹 공격을 방지하기 위한 목적으로 사용되었다.\[5\]

SAM 잠금 도구는 [부팅](../Page/부팅.md "wikilink") 과정에서 사용자에게 암호를 요구하거나(시작 암호) [플로피 디스크에다](https://ko.wikipedia.org/wiki/플로피_디스크 "wikilink") 암호를 저장하도록 구성할 수 있다.\[6\]

마이크로소프트는 윈도우 10 1709 이후 버전에서 SAM 잠금 도구를 제거하였다.\[7\] 마이크로소프트는 "SAM 잠금 도구 대신 비트로커 또는 비슷한 유틸리티를 사용할 것"을 권고하고 있다.

## 보안 문제

### Syskey 버그

1999년 11월, [BindView의](https://ko.wikipedia.org/wiki/:en:BindView "wikilink") 보안 팀에서는 특정 형태의 오프라인 암호 해독이 가능하며, [무차별 대입 공격](https://ko.wikipedia.org/wiki/무차별_대입_공격 "wikilink") 기법을 사용할 수 있는 것으로 보이는 보안 구멍을 발견하였다.\[8\]

이후 마이크로소프트는 "Syskey 버그"라고도 불리는 이 문제를 수정하는 프로그램을 발표하였다.\[9\] 이 버그는 [윈도우 NT 4.0과](../Page/윈도우_NT_4.0.md "wikilink") [윈도우 2000](../Page/윈도우_2000.md "wikilink") 릴리즈 후보 3(RC3) 이전 버전에서 발생한다.\[10\]

### 랜섬웨어 악용

SAM 잠금 도구는 [랜섬웨어](../Page/랜섬웨어.md "wikilink") 형태의 [기술 지원 사기](https://ko.wikipedia.org/wiki/:en:Technical_support_scam "wikilink") 기법으로 자주 사용된다.\[11\]\[12\]

## 같이 보기

  - [pwdump](https://ko.wikipedia.org/wiki/pwdump "wikilink")
  - [kon-boot](https://ko.wikipedia.org/wiki/Kon-Boot "wikilink")

## 각주

## 외부 링크

  - [Windows에서 Syskey를 제거하는 방법(영어)](https://web.archive.org/web/20190203030514/https://www.computernetworkingnotes.com/sysadmin-tutorials-collection/how-to-remove-syskey-in-windows-explained-with-examples.html)

[분류:암호 소프트웨어](https://ko.wikipedia.org/wiki/분류:암호_소프트웨어 "wikilink") [분류:윈도우 관리](https://ko.wikipedia.org/wiki/분류:윈도우_관리 "wikilink")

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
11.
12.