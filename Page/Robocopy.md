> This article is converted from Wikipedia: [Robocopy](https://ko.wikipedia.org/wiki/Robocopy).


**Robocopy**(로보카피), 또는 "Robust File Copy"(로버스트 파일 카피)는 [명령 줄에서](../Page/명령_줄_인터페이스.md "wikilink") 동작하는 디렉터리 및 파일 복제 [명령어](https://ko.wikipedia.org/wiki/명령어 "wikilink")이다. Robocopy 기능은 여러 옵션과 함께 [Xcopy](https://ko.wikipedia.org/wiki/Xcopy "wikilink")를 대체한다. 윈도우 NT 4.0의 경우 [윈도우 리소스 킷의](https://ko.wikipedia.org/wiki/윈도우_리소스_킷 "wikilink") 일부로서 이용이 가능하였으며 [윈도우 비스타와](../Page/윈도우_비스타.md "wikilink") [윈도우 서버 2008의](../Page/윈도우_서버_2008.md "wikilink") 표준 기능으로 첫 도입되었다. 명령어는 `robocopy`이다.

## 기능

Robocopy는 윈도우에 내장된 [copy](https://ko.wikipedia.org/wiki/copy "wikilink")와 [XCOPY](https://ko.wikipedia.org/wiki/XCOPY "wikilink") 명령어 대비 다음과 같은 기능들로 우위를 자랑한다:

  - 네트워크 간섭을 견디고 복사를 이어서 할 수 있는 기능. (불완전한 파일들은 1970-01-01 타임 스탬프로 표시해두고 복구 레코드를 포함하므로 Robocopy는 어디에서 계속할지의 여부를 알 수 있다)
  - 무한 루프(`/XJ`)로 인해 복사 실패를 일으킬 수 있는 [NTFS 정션 포인트를](https://ko.wikipedia.org/wiki/NTFS_정션_포인트 "wikilink") 건너뛰는 기능
  - [명령 줄 스위치를](https://ko.wikipedia.org/wiki/명령_줄_스위치 "wikilink") 사용함으로써 파일 데이터와 특성을 올바르게 복사하고 원래의 타임스탬프, NTFS [ACL](../Page/접근_제어_목록.md "wikilink"), 소유자 정보, 감사 정보를 보존하는 기능. (`/COPYALL` 또는 `/COPY:`) 나중 버전에서는 폴더의 타임스탬프도 복사가 가능하다 (`/DCOPY:T`).
  - [윈도우 NT](../Page/윈도우_NT.md "wikilink") "백업 권한"(backup right)의 [표명](../Page/표명.md "wikilink")(assert) 기능 (`/B`). 관리자는 관리자에게 읽기가 거부된 파일들을 포함하여 디렉터리 전체를 복사할 수 있다.
  - 퍼시스턴스(persistence)가 기본. 파일을 열 수 없는 경우 자동 재시도 횟수를 프로그래밍할 수 있음.
  - 원본에 더 이상 존재하지 않는, 목적지 밖에서 선택적으로 파일을 삭제함으로써 트리의 동기화를 유지하는 미러(mirror) 모드.
  - 목적 폴더에 이미 등장하는 동일한 크기와 타임스탬프의 파일을 건너뛰는 기능.
  - 지속적으로 업데이트되는 명령 줄 진행 표시기.
  - 259자를 초과하는 경로를 복사할 수 있는 기능 — 이론적 제한은 약 32,000자 — 오류 없이.\[1\]
  - 멀티스레드 복사. (윈도우 7, 윈도우 서버 2008 R2)\[2\]
  - 배치 파일 사용 중 프로그램 종료 시 반환 코드\[3\].

## 버전

참고: 여러 버전의 Robocopy는 명령 줄에서 `robocopy /?`를 실행할 때 버전 번호를 표시하지 않는다. 그러나 실행 파일 자체에는 버전이 저장되어 있으며 이를테면 파워셸을 통해 조회가 가능하다.(`gcm robocopy | fl *`)

| 제품 버전 | 파일 버전            | 연도   | 기원                                                                                                                                                                              | 기타          |
| ----- | ---------------- | ---- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------- |
| 1.70  | \-               | 1997 | Windows NT Resource Kit                                                                                                                                                         |             |
| 1.71  | 4.0.1.71         | 1997 | Windows NT Resource Kit                                                                                                                                                         |             |
| 1.95  | 4.0.1.95         | 1999 | Windows 2000 Resource Kit                                                                                                                                                       |             |
| 1.96  | 4.0.1.96         | 1999 | Windows 2000 Resource Kit                                                                                                                                                       | © 1995-1997 |
| XP010 | 5.1.1.1010       | 2003 | [Windows 2003](https://ko.wikipedia.org/wiki/Windows_2003 "wikilink") Resource Kit                                                                                              |             |
| XP026 | 5.1.2600.26      | 2005 | Robocopy GUI v.3.1.2와 함께 다운로드                                                                                                                                                   |             |
| XP027 | 5.1.10.1027      | 2008 | 다음에 기본 포함: [Windows Vista](https://ko.wikipedia.org/wiki/Windows_Vista "wikilink"), Server 2008, [Windows 7](https://ko.wikipedia.org/wiki/Windows_7 "wikilink"), Server 2008r2 | © 1995-2004 |
| 6.1   | 6.1.7601         | 2009 | [KB2639043](http://support.microsoft.com/kb/2639043)                                                                                                                            | © 2009      |
| 6.2   | 6.2.9200         | 2012 | 다음에 기본 포함: [Windows 8](https://ko.wikipedia.org/wiki/Windows_8 "wikilink")                                                                                                      | © 2012      |
| 6.3   | 6.3.9600         | 2013 | 다음에 기본 포함: [Windows 8.1](https://ko.wikipedia.org/wiki/Windows_8.1 "wikilink")                                                                                                  | © 2013      |
| 10.0  | 10.0.10240.16384 | 2015 | 다음에 기본 포함: [Windows 10](https://ko.wikipedia.org/wiki/Windows_10 "wikilink")                                                                                                    | © 2015      |

## 같이 보기

  - 명령 줄
      - [도스 명령어 목록](../Page/도스_명령어_목록.md "wikilink")
      - [copy](https://ko.wikipedia.org/wiki/copy "wikilink")
      - [XCOPY](https://ko.wikipedia.org/wiki/XCOPY "wikilink")
      - [rsync](https://ko.wikipedia.org/wiki/rsync "wikilink")
  - GUI
      - [GS RichCopy 360](https://ko.wikipedia.org/wiki/GS_RichCopy_360 "wikilink")
      - [SyncToy](https://ko.wikipedia.org/wiki/SyncToy "wikilink")
      - [RichCopy](https://ko.wikipedia.org/wiki/RichCopy "wikilink")
      - [Ultracopier](https://ko.wikipedia.org/wiki/Ultracopier "wikilink")

## 각주

## 외부 링크

  - 공식 출처
      - [Robocopy download](http://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd&displaylang=en) (Version XP010) as part of Windows Server 2003 Resource Kit Tools. Includes 35-page documentation "robocopy.doc".
      - \[<https://technet.microsoft.com/en-us/library/cc733145(WS.10>).aspx Robocopy short documentation\] on Microsoft TechNet Library
      - [Robocopy GUI download](https://technet.microsoft.com/en-us/magazine/2006.11.utilityspotlight.aspx) (Version 3.1.2.0) on Microsoft TechNet Magazine
  - Other
      - [ROBOCOPY.exe (XP Resource Kit/Standard Vista command)](http://ss64.com/nt/robocopy.html)

[분류:파일 복사 유틸리티](https://ko.wikipedia.org/wiki/분류:파일_복사_유틸리티 "wikilink")

1.
2.
3.