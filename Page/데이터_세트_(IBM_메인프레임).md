> This article is converted from Wikipedia: [  \(IBM \)](https://ko.wikipedia.org/wiki/__\(IBM_\)).


[IBM](https://ko.wikipedia.org/wiki/IBM "wikilink") [메인프레임 컴퓨터의](https://ko.wikipedia.org/wiki/메인프레임_컴퓨터 "wikilink") 문맥에서 **데이터 세트**\[1\](data set)는 [레코드 조직을](https://ko.wikipedia.org/wiki/레코드_지향_파일_시스템 "wikilink") 보유하고 있는 [컴퓨터 파일의](https://ko.wikipedia.org/wiki/컴퓨터_파일 "wikilink") 하나이다. 이 용어의 이용은 [OS/360](https://ko.wikipedia.org/wiki/OS/360 "wikilink")과 함께 시작하였으며 현재의 [z/OS](https://ko.wikipedia.org/wiki/z/OS "wikilink")를 포함한 이후 세대에서도 여전히 사용되고 있다. 이러한 시스템들의 문서들은 역사적으로 [파일](https://ko.wikipedia.org/wiki/컴퓨터_파일 "wikilink") 보다는 이 용어를 선호하였다.

데이터 세트는 일반적으로 [직접 접근 기억 장치](../Page/직접_접근_기억_장치.md "wikilink")(DASD)나 [자기 테이프에](https://ko.wikipedia.org/wiki/자기_테이프 "wikilink") 저장되어 있지만, 천공 카드 리더, 카드 펀치, 라인 프린터와 같은 유닛 레코드 장치들은 데이터 세트(파일)을 위한 입출력을 제공할 수 있다.\[2\]

데이터 세트들은 구조화되지 않은 [바이트](https://ko.wikipedia.org/wiki/바이트 "wikilink") 스트림이 아니며, `DSORG`(data set organization의 준말로, 데이터 세트 조직을 뜻함), `RECFM`(record format의 준말로 레코드 포맷을 뜻함) 등의 매개변수들에 의해 결정되는 다양한 논리 레코드와 블록 구조로 조직되어 있다. 이러한 매개변수들은 데이터 세트 할당(작성) 시에 지정되는데, 이를테면 [작업 제어 언어](https://ko.wikipedia.org/wiki/작업_제어_언어 "wikilink")(JCL)의 `DD` 문들을 통해 실행된다. 하나의 잡 안에서, 이들은 데이터 세트를 저장하기 위해 사용되는 자료 구조인 [데이터 제어 블록](https://ko.wikipedia.org/wiki/데이터_제어_블록 "wikilink")(DCB) 안에 (이를테면 [접근 방식을](https://ko.wikipedia.org/wiki/접근_방식 "wikilink") 이용하여) 저장된다.

## 데이터 세트 조직

OS/360의 경우, DCB의 DSORG 매개변수는 데이터 세트가 어떻게 조직되어 있는지를 규정한다. 물리적으로 순차적이거나(PS), 색인 순차적이거나(IS), 파티션되어 있거나(PO), 직접 접근(DA)일 수 있다. 테이프의 데이터 세트는 DSORG=PS로만 지정된다. 조직의 선택은 데이터의 접근 방식에 따라, 특히 어떻게 업데이트될 것인지에 따라 달라진다.

프로그래머들은 프로그램에서 다양한 [접근 방식](https://ko.wikipedia.org/wiki/접근_방식 "wikilink")([QSAM](../Page/QSAM.md "wikilink")이나 [VSAM](https://ko.wikipedia.org/wiki/VSAM "wikilink") 등)을 사용하여 데이터 세트를 읽고 기록한다. 접근 방식은 주어진 데이터 세트 조직에 따라 다르다.

## 레코드 포맷 (RECFM)

조직에 관계 없이 각 레코드의 물리적 구조는 동일해야 하며 데이터 세트를 통틀어 통일성이 있어야 하다. 이는 DCB `RECFM` 파라미터에 정의된다. `RECFM=F`는 레코드가 고정 길이임을 의미하며, 레코드 길이는 `LRECL` 파라미터를 통해 지정된다. `RECFM=V`는 가변 길이 레코드임을 나타낸다. V 레코드들은 미디어에 저장할 때 레코드 서술자 워드(Record Descriptor Word, RDW)에 의해 접두사가 붙으며 바이트 단위의 정수 길이의 레코드를 포함한다. RECFM=FB, RECFM=VB를 사용하여 여러 개의 논리 레코드들을 함께 테이프나 디스크 상의 하나의 [물리 블록으로](https://ko.wikipedia.org/wiki/블록_\(컴퓨팅\) "wikilink") 묶을 수 있다. FB와 VB는 fixed-blocked와 variable-blocked를 각각 나타낸다. `BLKSIZE` 파라미터는 블록의 최대 길이를 규정한다. 마지막 것을 제외한 모든 블록이 완전한 `BLKSIZE` 길이여야 한다는 fixed-blocked standard를 뜻하는 `RECFM=FBS`를 정의할 수도 있다. variable-blocked spanned를 뜻하는 `RECFM=VBS`는 논리 레코드가 2개 이상의 블록을 가로지를 수 있음을 의미하며, RDW를 플래그하면 레코드 세그먼트가 다음 블록으로 계속되는지 이전 것으로부터 계속되었는지를 표시한다.

## 파티션 데이터 세트

**파티션 데이터 세트**(partitioned data set, PDS)는 여러 개의 멤버(member)를 포함하는 데이터 세트로, 각 멤버는 별개의 하위 데이터 세트를 보유하고 있는데 이는 마치 다른 종류의 [파일 시스템의](https://ko.wikipedia.org/wiki/파일_시스템 "wikilink") [디렉터리](https://ko.wikipedia.org/wiki/디렉터리 "wikilink")와 비슷하다. 이러한 종류의 데이터 세트는 종종 실행 프로그램(로드 모듈), 소스 프로그램 라이브러리(특히 어셈블러 매크로 정의), [작업 제어 언어](https://ko.wikipedia.org/wiki/작업_제어_언어 "wikilink")(JCL)을 보관하기 위해 종종 사용된다.

## 같이 보기

  - [볼륨 목록](../Page/볼륨_목록.md "wikilink")(VTOC)

## 각주

[분류:데이터 관리](https://ko.wikipedia.org/wiki/분류:데이터_관리 "wikilink") [분류:IBM 메인프레임 운영 체제](https://ko.wikipedia.org/wiki/분류:IBM_메인프레임_운영_체제 "wikilink") [분류:파일 시스템](https://ko.wikipedia.org/wiki/분류:파일_시스템 "wikilink") [분류:컴퓨터 파일](https://ko.wikipedia.org/wiki/분류:컴퓨터_파일 "wikilink")

1.
2.  <http://publib.boulder.ibm.com/infocenter/zvm/v5r4/index.jsp?topic=/com.ibm.zvm.v54.hcpa7/hcse7b3050.htm>