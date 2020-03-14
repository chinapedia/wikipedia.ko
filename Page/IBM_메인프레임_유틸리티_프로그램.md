> This article is converted from Wikipedia: [IBM   ](https://ko.wikipedia.org/wiki/IBM___).


**IBM 메인프레임 유틸리티 프로그램**은 [MVS](../Page/MVS.md "wikilink")와 같은 [IBM](https://ko.wikipedia.org/wiki/IBM "wikilink") [메인프레임](https://ko.wikipedia.org/wiki/메인프레임 "wikilink") [운영 체제에](https://ko.wikipedia.org/wiki/운영_체제 "wikilink") 공급되는 [유틸리티 소프트웨어로서](https://ko.wikipedia.org/wiki/유틸리티_소프트웨어 "wikilink"), [데이터셋](https://ko.wikipedia.org/wiki/데이터셋 "wikilink") 등에 관련한 다양한 작업을 수행한다.

다음의 목록은 [OS/360](https://ko.wikipedia.org/wiki/OS/360 "wikilink") 이후 세대에 배포된 유틸리티를 기술한다. [VSE나](../Page/VSE_\(운영_체제\).md "wikilink") [VM](https://ko.wikipedia.org/wiki/VM_\(운영_체제\) "wikilink") 유틸리티는 포함되지 않는다.

## 역사/공통 JCL

유틸리티들 다수가 IBM 사용자들에 의해 설계되었다.

이 유틸리티들은 [작업 제어 언어](https://ko.wikipedia.org/wiki/작업_제어_언어 "wikilink")(JCL)를 통해 호출되는 것이 보통이다. 이들은 데이터셋을 위해 공통 JCL DD 식별자를 사용하는 경향이 있다.

| DDNAME   | 기능                                              |
| -------- | ----------------------------------------------- |
| SYSIN    | 유틸리티의 '명령어'를 위한 입력 파일. 기본 동작을 원하는 경우 DUMMY로 설정. |
| SYSUT1   | 입력 파일                                           |
| SYSUT2   | 출력 파일                                           |
| SYSUT3   | 출력물 (SYSUT1)를 위한 작업용 파일 (자주 쓰이지 않음)             |
| SYSUT4   | 출력물 (SYSUT2)를 위한 작업용 파일 (자주 쓰이지 않음)             |
| SYSPRINT | 유틸리티로부터 PRINT된 출력물을 위한 출력 파일                    |
| SYSOUT   | 유틸리티로부터의 메시지를 위한 출력 파일                          |
| SYSUDUMP | 프로그램 실패 시 시스템 덤프를 위한 출력 파일                      |

## 데이터셋 유틸리티

<table>
<thead>
<tr class="header">
<th><p>유틸리티</p></th>
<th><p>기능</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>IDCAMS</p></td>
<td><p><a href="../Page/가상_기억_접근_방식.md" title="wikilink">VSAM</a>, 비VSAM 데이터셋을 만들고 수정한다.</p></td>
</tr>
<tr class="even">
<td><p>IEBCOMPR</p></td>
<td><p>순차 또는 파티션된 데이터셋의 레코드를 비교한다.</p></td>
</tr>
<tr class="odd">
<td><p>IEBCOPY</p></td>
<td><p>파티션된 데이터셋을 복사, 압축, 병합한다.</p></td>
</tr>
<tr class="even">
<td><p>IEBDG</p></td>
<td><p>패턴화된 데이터를 이루는 테스트 데이터셋을 만든다.</p></td>
</tr>
<tr class="odd">
<td><p>IEBEDIT</p></td>
<td><p>JCL의 일부를 선택적으로 복사한다.</p></td>
</tr>
<tr class="even">
<td><p>IEBGENER</p></td>
<td><p>순차 데이터셋으로부터 레코드를 복사하거나 파티션된 데이터셋을 만든다.</p></td>
</tr>
<tr class="odd">
<td><p>IEBIMAGE</p></td>
<td><p>IBM 3800 레이저 인쇄 하위 시스템과 IBM 4248 프린터를 위한 여러 종류의 정의들(이미지)을 조작한다.</p></td>
</tr>
<tr class="even">
<td><p>IEBISAM</p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/ISAM" title="wikilink">ISAM</a> 데이터셋의 적재를 해제하거나 적재하고, 복사하고 인쇄한다.</p></td>
</tr>
<tr class="odd">
<td><p>IEBPTPCH</p></td>
<td><p>순차 또는 파티션된 데이터셋으로부터의 레코드를 출력하거나 천공한다.</p></td>
</tr>
<tr class="even">
<td><p>IEBUPDTE</p></td>
<td><p>순차 또는 파티션된 데이터셋의 변경 사항들을 통합한다. UNIX의 patch 유틸리티와 비슷하지만 상이한 입력 포맷 마커를 사용한다.<br />
(예: MVS의 "./ INSERT ..."는 유닉스 Patch의 "@@..." 가 된다.)</p></td>
</tr>
</tbody>
</table>

### IDCAMS

IDCAMS ("Access Method Services")는 [가상 기억 접근 방식](../Page/가상_기억_접근_방식.md "wikilink")(VSAM)과 VSAM이 아닌 데이터셋을 만들고 수정한다. IDCAMS는 [OS/VS](https://ko.wikipedia.org/wiki/OS/VS "wikilink")의 VSAM과 함께 도입되었다. "접근 방식" 참조는 "VSAM이 다른 모든 접근 방식을 대체한다"는 OS/VS의 마인드에서 비롯된다. IDCAMS는 VSAM과 비VSAM 파일 모두를 위해 수많은 기능을 수행하는 것으로 간주된다.

예:

``` jcl
//XXXXXXXW JOB  XXXXXXX,AAAA,CLASS=G,MSGCLASS=1,NOTIFY=&SYSUID
//STEP001  EXEC PGM=IDCAMS
//SYSIN    DD *
   REPRO INFILE(FILE01) OUTFILE(FILE02)
/*
//FILE01   DD DSN=PROD.FILE1.INPUT,disp=shr   .....
//FILE02   DD DSN=PROD.FILE2.OUTPUT,
//            DISP=(NEW,CATLG,DELETE),
//            UNIT=DASD,
//            SPACE=(TRK,(100,10),RLSE),
//            DCB=(RECFM=FB,BLKSIZE=0,LRECL=80)
//SYSPRINT DD SYSOUT=*
//SYSOUT   DD SYSOUT=*
//SYSUDUMP DD SYSOUT=*

//*
```

위의 예에서 SYSIN 컨트롤 카드들은 인스트림 파일에서 가져오지만, 사용자가 원하는 경우 순차 파일이나 PDS 멤버, 또는 임시 데이터셋을 가리키게 할 수도 있다. SYSIN 파일의 사용 예는 다음과 같다:

``` jcl
//SYSIN    DD DSN=PROD.MYFILE.REPRO,DISP=SHR
```

다음과 같이 할 수도 있다:

``` jcl
//SYSIN    DD DSN=PROD.MYLIB.CNTLLIB(REPRO),
//            DISP=SHR
```

### IEBCOMPR

IEBCOMPR는 순차 또는 파티션 데이터셋의 레코드들을 비교한다.

IEBCOMPR 유틸리티는 두 개의 순차 또는 파티션 데이터셋을 비교하는데 사용된다. 이 데이터셋 비교는 논리 레코드 수준에서 수행된다. 그러므로 IEBCOMPR은 데이터셋의 백업 사본이 올바른지 (원본과 완전히 일치하는지) 확인하는데 흔히 사용된다.

처리 중에 IEBCOMPR은 각각의 데이터셋에서 각각의 레코드를 하나씩 비교한다. 레코드가 동등하지 않으면, IEBCOMPR은 SYSOUT에 다음의 정보를 나열한다:

  - 의문시되는 레코드 및 블록 번호.
  - 불일치가 발생한 DD 문의 이름.
  - 동등하지 않은 레코드.

순차 데이터셋을 비교할 때, IEBCOMPR은 다음의 조건이 충족하는 경우 데이터셋을 동등하다고 인식한다:

:\* 데이터셋에 동일한 수의 레코드가 포함되어 있다.

:\* 일치하는 레코드와 키가 동일하다.

파티션 데이터셋의 경우, IBECOMPR은 다음의 조건이 충족하는 경우 데이터셋을 동등하다고 인식한다:

:\* 두 개의 파티션 데이터셋의 디렉터리 엔트리가 일치한다. 즉, 이름이 동일하고 엔트리 수도 동일하다.

:\* 일치하는 멤버에는 동일한 수의 레코드를 포함하고 있다.

:\* 일치하는 레코드와 키는 동일하다.

10개의 동등하지 않은 비교가 처리 중에 발생하면, IECOMPR은 적절한 메시지와 함께 종료된다.

``` jcl
//XXXXXXXW JOB   XXXXXXX,AAAA.A.A,CLASS=G,MSGCLASS=1,NOTIFY=XXXXX
//STEP01   EXEC PGM=IEBCOMPR,ACCT=PJ00000000
//     INCLUDE  MEMBER=@BATCHS
//*SYSIN    DD DUMMY
//SYSIN DD *
   COMPARE TYPORG=PO
/*
//SYSUT1   DD DSN=XXXXXXX.OLDFILE,UNIT=DASD,DISP=SHR
//SYSUT2   DD DSN=XXXXXXX.NEWFILE,UNIT=DASD,DISP=SHR
//SYSUT#   DD
```

참고: IEBCOMPR은 사용자에게 친숙하도록 설계된 비교 프로그램이 아니다. 특정한 컬럼에만 비교를 제한할 수 없고, 공백의 차이를 무시할 수도 없으며, 레코드의 어느 부분에서 차이가 있는지 알려주지도 않으며, 10개의 차이 이후에는 중단된다. 한편, 속도가 빠르며 모든 IBM 메인프레임에 존재한다. 그러므로 재차단되지 않은 로드 모듈을 비교한다든지, 복사 작업이 올바르게 이루어졌는지를 확인하는 등 완전히 일치하는지를 확인할 때 유용하다. 프로그램이나 보고서를 비교할 때에는 [ISPF](../Page/ISPF.md "wikilink") SuperC (ISRSUPC) 비교 프로그램이 대신 종종 사용된다.

### IEBCOPY

IEBCOPY는 파티션된 데이터셋을 복사, 압축, 병합한다. 또, 복사 작업 도중 지정된 멤버를 선택, 제외시킬 수 있으며, 멤버를 대체하거나 멤버 이름을 바꿀 수 있다.

IBECOPY 유틸리티의 경우, 복사에 필요한 JCL 문은 다음과 같다:

``` jcl
//stepname EXEC PGM=IEBCOPY
//SYSPRINT DD SYSOUT=class
//MYDD1    DD DSN=xxxx.ppp.psps,DISP=SHR
//MYDD2    DD DSN=xxxx.ppp.pssp,DISP=SHR
//SYSIN    DD *
    COPY INDD=MYDD1,OUTDD=MYDD2
       SELECT MEMBER=(MEM1,MEM2,MEM3)/ EXCLUDE MEMBER=(SF,DF,SA)
```

### IEBDG

IEBDG('Data Generator')는 패턴화된 데이터를 이루는 테스트 데이터셋을 만든다.

### IEBEDIT

IEBEDIT는 JCL의 일부를 선택적으로 복사한다.

IEBEDIT 프로그램의 예는 다음과 같다:

``` jcl
//IEBEDITJ JOB ACCT,'',CLASS=P,MSGCLASS=T,MSGLEVEL=(1,1),NOTIFY=&SYSUID
//STEP0001 EXEC PGM=IEBEDIT
//SYSPRINT DD SYSOUT=*
//SYSUT1   DD DSN=xxxxx.yyyyy.zzzzz,DISP=SHR
//SYSUT2   DD SYSOUT=(*,INTRDR)
//SYSIN    DD *
    EDIT TYPE=INCLUDE,STEPNAME=(STEP10,STEP5,STEP15)
/*
//
```

### IEBGENER

IEBGENER는 순차 데이터셋으로부터 레코드를 복사하거나 파티션된 데이터셋을 만든다.

IEBGENER 프로그램을 사용하여 데이터셋을 다른 것으로 복사하는 예이다:

``` jcl
//IEBGENER JOB  ACCT,'DATA COPY',MSGCLASS=J,CLASS=A
//STEP010  EXEC PGM=IEBGENER
//SYSUT1   DD DSN=xxxxx.yyyyy.zzzzz,DISP=SHR
//SYSUT2   DD DSN=aaaaa.bbbbb.ccccc,DISP=(,CATLG),
//            UNIT=SYSDA,SPACE=(TRK,(5,5),RLSE),
//            DCB=(RECFM=FB,LRECL=1440)
//SYSPRINT DD SYSOUT=*
//SYSIN    DD DUMMY
```

### IEBIMAGE

IEBIMAGE는 IBM 3800 레이저 인쇄 하위 시스템과 IBM 4248 프린터를 위한 여러 종류의 정의들(이미지)을 조작한다. 일반적으로는 FCB(forms control buffer), 문자 정렬표, 문자 정의, 폼의 이미지가 텍스트와 나란히 출력물에 인쇄한다든지, 회사 로고를 문서에 인쇄한다든지, 단순히 그레이바 페이지를 인쇄하는 목적으로 사용된다. 이 유틸리티를 사용하여 다른 수많은 형태의 로고들을 그림으로 저장할 수 있고 필요하면 인쇄할 수도 있으며 모두 동일한 표준 블랙 페이퍼를 사용하므로 미리 인쇄된 수많은 폼을 쌓아둘 필요가 없고 조작자가 프린터들 중단하고 용지를 교환할 필요도 없다.

### IEBISAM

IEBISAM은 [ISAM](https://ko.wikipedia.org/wiki/ISAM "wikilink") 데이터셋의 적재를 해제하거나 적재하고, 복사하고 인쇄한다. ISAM은 현대의 대부분의 운영 체제에서 VSAM으로 대체되었기 때문에 흔히 사용되지 않는다. VSAM 파일들은 IEBISAM 대신 IDCAMS 유틸리티를 사용한다.

### IEBPTPCH

IEBPTPCH ("PrinT and PunCH")는 순차 또는 파티션된 데이터셋으로부터의 레코드를 출력하거나 천공한다.

``` jcl
//IEBPTPCH JOB
//         EXEC PGM=IEBPTPCH
//SYSIN    DD *
 PRINT     MAXFLDS=2
 TITLE     ITEM=('Name',22),
           ITEM=('GPA',50)
 TITLE     ITEM=(' ',1)
 RECORD    FIELD=(25,1,,22),
           FIELD=(4,51,,50)
/*
//SYSPRINT DD SYSOUT=*
//SYSUT1   DD *
Person 1                 307 C Meshel Hall        3.89
Second person            123 Williamson Hall      2.48
3rd person               321 Maag Library         1.52
/*
//SYSUT2   DD SYSOUT=*
//
```

**비어있는 데이터셋 확인:** 데이터셋이 비어있는 것으로 확인되면 RC=4를, 그렇지 않으면 0을 반환한다.

``` jcl
//IEBPTPCH JOB
//         EXEC PGM=IEBPTPCH
//SYSUT1   DD DSN=<filename>,DISP=SHR
//SYSUT2   DD DUMMY,
//         DCB=(BLKSIZE=<block size>,RECFM=FA)
//SYSIN    DD *
 PRINT TYPORG=PS
/*
//SYSPRINT DD SYSOUT=*
//
```

### IEBUPDTE

IEUPDTE는 순차 또는 파티션된 데이터셋의 변경 사항들을 통합한다. UNIX의 patch 유틸리티와 비슷하지만 상이한 입력 포맷 마커를 사용한다. (예: MVS의 "./ INSERT ..."는 유닉스 Patch의 "@@..." 가 된다.)

IEUPDTE에 쓰이는 작업 제어는 다음과 같다:

``` jcl
//stepname EXEC PGM=IEUPDTE,PARM=NEW
//SYSPRINT DD SYSOUT=class
//SYSUT1   DD ...
//SYSUT2   DD ...
//SYSIN    DD ...
```

## 스케줄러 유틸리티

### IEFBR14

[IEFBR14](https://ko.wikipedia.org/wiki/IEFBR14 "wikilink")는 데이터셋의 할당이나 삭제만 취할 경우 JCL에 흔히 추가하는 더미 프로그램이다.

IEFBR14의 스텝의 예는 다음과 같다:

``` jcl
//IEFBR14  JOB  ACCT,'DELETE DATASET'
//STEP01   EXEC PGM=IEFBR14
//DELDD    DD DSN=xxxxx.yyyyy.zzzzz,
//            DISP=(MOD,DELETE,DELETE),UNIT=DASD
```

## 시스템 유틸리티

<table>
<thead>
<tr class="header">
<th><p>유틸리티</p></th>
<th><p>기능</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ICKDSF</p></td>
<td><p>운영 체제 하에서 또는 독립적으로 DASD를 설치, 초기화, 관리한다.</p></td>
</tr>
<tr class="even">
<td><p>IEHDASDR</p></td>
<td><p>현재의 z/OS 매뉴얼에서는 보이지 않는 오래된 프로그램으로서, 디스크로부터 데이터셋을 프린터로 덤프하거나 백업 장치로부터 이들을 백업/복구한다.<br />
IEHDASDR는 MVS/XA에서 제거되었다.[1]</p></td>
</tr>
<tr class="odd">
<td><p>IEHINITT</p></td>
<td><p>테이블 레이블을 기록함으로써 테이프를 초기화한다.</p></td>
</tr>
<tr class="even">
<td><p>IEHLIST</p></td>
<td><p>파티션된 데이터셋(PDS) 디렉터리의 항목을 나열하거나 볼륨 목록(<a href="https://ko.wikipedia.org/wiki/VTOC" title="wikilink">VTOC</a>)의 내용을 나열하기 위해 사용한다.</p></td>
</tr>
<tr class="odd">
<td><p>IEHMOVE</p></td>
<td><p>데이터 집합을 이동하거나 복사한다.</p></td>
</tr>
<tr class="even">
<td><p>IEHPROGM</p></td>
<td><p>시스템 제어 데이터를 빌드하고 관리한다.</p></td>
</tr>
</tbody>
</table>

## 지원 프로그램

<table>
<thead>
<tr class="header">
<th><p>유틸리티</p></th>
<th><p>기능</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>SORT</p></td>
<td><p>SORT/MERGE 유틸리티는 지정된 순서로 파일 내의 레코드를 정렬하거나 미리 정렬된 파일을 병합하기 위해 사용하는 프로그램이다.</p></td>
</tr>
<tr class="even">
<td><p>컴파일러/링커</p></td>
<td><p>컴퓨터 가게에 쓰이는 각 <a href="https://ko.wikipedia.org/wiki/프로그래밍_언어" title="wikilink">프로그래밍 언어는</a> 원시 프로그램을 기계어 오브젝트 모듈로 변환하는 관련 <a href="https://ko.wikipedia.org/wiki/컴파일러" title="wikilink">컴파일러</a>를 갖추고 있을 수 있다.<br />
컴파일러로부터 가져온 오브젝트 모듈은 실행 가능한 로드 모듈을 만들기 위해 IEWL이라는 링키지 에디터를 통해 처리되어야 한다.</p></td>
</tr>
<tr class="odd">
<td><p>DFSMS</p></td>
<td><p>운영 체제 스스로가 스토리지 관리 작업(이전에 시스템 프로그래머가 수동으로 수행한 작업)의 다수를 장악하는 프로그램들의 집합이다.</p></td>
</tr>
</tbody>
</table>

## 각주

<references />

## 외부 링크

  - [IBM: z/OS 1.8 DFSMSdfp utilities manual](http://publibz.boulder.ibm.com/epubs/pdf/dgt2u130.pdf)
  - [IBM: z/OS 1.8 IDCAMS utility manual](http://publibz.boulder.ibm.com/epubs/pdf/dgt2i250.pdf)
  - [IBM: z/OS 1.8 ADRDSSU utility manual](http://publibz.boulder.ibm.com/epubs/pdf/dgt2u250.pdf)
  - [MVS UTILITIES](http://ibmmainframes.com/references/a20.html)

[분류:IBM 메인프레임 운영 체제](https://ko.wikipedia.org/wiki/분류:IBM_메인프레임_운영_체제 "wikilink") [분류:유틸리티 소프트웨어](https://ko.wikipedia.org/wiki/분류:유틸리티_소프트웨어 "wikilink")

1.