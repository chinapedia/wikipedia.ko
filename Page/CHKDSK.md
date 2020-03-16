> This article is converted from Wikipedia: [CHKDSK](https://ko.wikipedia.org/wiki/CHKDSK).


**CHKDSK**(체크디스크, "check disk"의 준말)는 [도스](../Page/도스.md "wikilink"), [OS/2](https://ko.wikipedia.org/wiki/OS/2 "wikilink"), [마이크로소프트 윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 운영 체제가 설치된 컴퓨터에 쓰이는 명령어로, [하드 디스크와](https://ko.wikipedia.org/wiki/하드_디스크 "wikilink") [플로피 디스크의](https://ko.wikipedia.org/wiki/플로피_디스크 "wikilink") [파일 시스템](../Page/파일_시스템.md "wikilink") 무결성 상태를 보여주고 논리 파일 시스템 오류를 수정한다. 사용법은 명령 프롬프트로 해당 드라이버를 들어간 후 chkdsk '옵션'을 입력하면 실행된다. 옵션은 chkdsk /?를 입력하면 입력할 수 있는 옵션들이 나온다.

CHKDSK는 [도스 프롬프트](../Page/COMMAND.COM.md "wikilink"), [윈도우 탐색기](https://ko.wikipedia.org/wiki/윈도우_탐색기 "wikilink"), [윈도우 명령 프롬프트](../Page/Cmd.exe.md "wikilink"), [윈도우 파워셸](https://ko.wikipedia.org/wiki/윈도우_파워셸 "wikilink"), [복구 콘솔에서](../Page/복구_콘솔.md "wikilink") 실행할 수 있다.\[1\]

## 윈도 NT 기반 CHKDSK의 표시

    파일 시스템 유형은 NTFS입니다.

    경고!  /F 매개 변수가 지정되지 않았습니다.
    CHKDSK를 읽기 전용 모드로 실행하는 중입니다.

    1단계: 기본 파일 시스템 구조 검사...
      750848개의 파일 레코드가 처리되었습니다.
    파일 검증 작업을 완료했습니다.
      12102개의 큰 파일 레코드가 처리되었습니다.
      0개의 잘못된 파일 레코드가 처리되었습니다.

    2단계: 파일 이름 연결 검사...
      32676개의 재분석 레코드가 처리되었습니다.
      821032개의 인덱스 항목이 처리되었습니다.
    색인 검증 작업을 완료했습니다.
      0개의 인덱싱되지 않은 파일이 검색되었습니다.
      0개의 인덱싱되지 않은 파일이 손실 및 찾기로 복구되었습니다.
      32676개의 재분석 레코드가 처리되었습니다.

    3단계: 보안 설명자 검사...
    보안 설명자를 검증했습니다.
      35093개의 데이터 파일이 처리되었습니다.
    CHKDSK가 Usn 저널을 검증하고 있습니다.
      38616000개의 USN 바이트가 처리되었습니다.
    USN 저널 검증을 마쳤습니다.

    Windows에서 파일 시스템에 문제가 없음을 확인했습니다.
    더 이상 작업이 필요하지 않습니다.

    전체 디스크 공간:  419430399KB
      33259296KB (176034개 파일)
    색인 35094개:      94032KB
    잘못된 섹터:          0KB
    시스템 사용:     881131KB
    로그 파일이      65536KB가 되었습니다.
    사용 가능한 디스크 공간:  385195940KB

    각 할당 단위:       4096바이트
    디스크의 전체 할당 단위 개수:  104857599개
    디스크에서 사용 가능한 할당 단위 개수:   96298985개

## 같이 보기

  - [스캔디스크](../Page/스캔디스크.md "wikilink")
  - [단편화 제거](../Page/단편화_제거.md "wikilink")
  - [fsck](https://ko.wikipedia.org/wiki/fsck "wikilink")

## 각주

## 외부 링크

  - [Microsoft TechNet Chkdsk article](http://technet.microsoft.com/en-us/library/bb491051.aspx)

  - [Understanding what CHKDSK does (NTFS only)](http://support.microsoft.com/kb/314835/EN-US/#/) – Microsoft Article

  - [Troubleshooting Disks and File Systems](http://technet.microsoft.com/en-us/library/bb457122.aspx) - TechNet Article on Windows XP resources to troubleshoot hard disk errors

[분류:외부 도스 명령어](https://ko.wikipedia.org/wiki/분류:외부_도스_명령어 "wikilink") [분류:윈도우 명령어](https://ko.wikipedia.org/wiki/분류:윈도우_명령어 "wikilink") [분류:OS/2](https://ko.wikipedia.org/wiki/분류:OS/2 "wikilink") [분류:하드 디스크 소프트웨어](https://ko.wikipedia.org/wiki/분류:하드_디스크_소프트웨어 "wikilink")

1.