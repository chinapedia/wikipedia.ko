> This article is converted from Wikipedia: [MS-DOS API](https://ko.wikipedia.org/wiki/MS-DOS_API).


**MS-DOS API**는 [86-DOS](https://ko.wikipedia.org/wiki/86-DOS "wikilink")를 기원으로 하고 [MS-DOS](https://ko.wikipedia.org/wiki/MS-DOS "wikilink")/[PC-DOS](../Page/PC-DOS.md "wikilink") 및 기타 [도스](https://ko.wikipedia.org/wiki/도스 "wikilink") 호환 운영 체제에 쓰이는 [API](../Page/API.md "wikilink")이다. 도스 API의 대부분의 호출은 [소프트웨어 인터럽트](../Page/인터럽트.md "wikilink") 21h (INT 21h)를 이용하여 불러낸다. AH [프로세서 레지스터의](https://ko.wikipedia.org/wiki/프로세서_레지스터 "wikilink") 하부 함수 번호, 다른 레지스터의 다른 변수와 더불어 INT 21h를 호출함으로써 다양한 도스 서비스를 불러낸다. 도스 서비스에는 키보드 입력, 비디오 출력, 디스크 파일 접근, 프로그램 실행, 메모리 할당 등이 있다. 1980년대 말에 [DPMI](../Page/DPMI.md "wikilink") 등의 [도스 확장자를](../Page/도스_확장자.md "wikilink") 통해 프로그램들이 16비트나 32비트 보호 모드에서 실행할 수 있게 되었으며 여전히 도스 API로의 접근을 소유하고 있다.

## 역사

86-DOS, MS-DOS 1.0에 있던 본래의 DOS API는 [CP/M](https://ko.wikipedia.org/wiki/CP/M "wikilink")과의 기능 호환을 위해 설계되었다. 파일은 [파일 제어 블록](https://ko.wikipedia.org/wiki/파일_제어_블록 "wikilink")(FCBs)을 이용하여 접근된다. 도스 API는 MS-DOS 2.0에서 [파일 처리](https://ko.wikipedia.org/wiki/파일_서술자 "wikilink"), [계층 디렉터리](https://ko.wikipedia.org/wiki/디렉터리 "wikilink"), 장치 입출력 제어를 이용한 파일 접근과 같은 몇 가지 유닉스 개념과 더불어 더 많이 확장되었다. 도스 3.1에서 네트워크 리다이렉터 지원이 추가되었다. MS-DOS 3.31에서 INT 25h/26h 함수가 강화되어 32 MB 이상의 하드 디스크를 지원한다. MS-DOS 5에는 [상위 메모리 영역](https://ko.wikipedia.org/wiki/상위_메모리_영역 "wikilink")(UMBs) 이용 지원이 추가되었다. MS-DOS 5 이후로 DOS API에는 변경 사항이 없다.

## DOS API와 윈도

[윈도 9x에서](https://ko.wikipedia.org/wiki/윈도_9x "wikilink") 도스는 일반적으로 [보호 모드](../Page/보호_모드.md "wikilink") 운영 체제와 그래픽 셸을 불러들이는 부트로더로 사용되었다. 도스는 일반적으로 [가상 도스 머신](../Page/가상_도스_머신.md "wikilink")(VDM)으로부터 접근되었으나 윈도를 로드하지 않고 리얼 모드 MS-DOS 7.0로 직접 시동할 수도 있었다. 도스 API는 강화된 국제화 지원 및 [긴 파일 이름](../Page/긴_파일_이름.md "wikilink") 지원으로 강화되었는데, 여기서 긴 파일 이름 지원은 VDM을 통해서만 이용할 수 있었다. [윈도 95](https://ko.wikipedia.org/wiki/윈도_95 "wikilink") OSR2에서는 도스가 7.1로 업데이트되면서 [FAT32](https://ko.wikipedia.org/wiki/FAT32 "wikilink") 지원이 추가되었으며 DOS API가 이를 지원하는 기능이 추가되었다. [윈도 98](https://ko.wikipedia.org/wiki/윈도_98 "wikilink"), [윈도 Me](https://ko.wikipedia.org/wiki/윈도_Me "wikilink") 또한 MS-DOS 8.0을 표방하면서 MS-DOS 7.1 API가 추가되어 있다.

[윈도 NT](https://ko.wikipedia.org/wiki/윈도_NT "wikilink") 계열 운영 체제([윈도 XP](https://ko.wikipedia.org/wiki/윈도_XP "wikilink"), [윈도 비스타](https://ko.wikipedia.org/wiki/윈도_비스타 "wikilink"), [윈도 7](https://ko.wikipedia.org/wiki/윈도_7 "wikilink"), [윈도 8](https://ko.wikipedia.org/wiki/윈도_8 "wikilink") 등)는 MS-DOS 기반은 아니지만 [가상 머신](../Page/가상_머신.md "wikilink") [NTVDM을](../Page/가상_도스_머신.md "wikilink") 사용하여 도스 API를 처리한다. NTVDM은 [가상 8086 모드](https://ko.wikipedia.org/wiki/가상_8086_모드 "wikilink")([80386](https://ko.wikipedia.org/wiki/80386 "wikilink") 이상의 프로세서에서 이용할 수 있는 [보호 모드](../Page/보호_모드.md "wikilink") 안의 [리얼 모드의](../Page/리얼_모드.md "wikilink") 에뮬레이션)에서 도스 프로그램을 실행함으로써 동작한다. NTVDM은 도스 5.0 API를 지원한다. [리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink")용 [DOSEMU](../Page/DOSEMU.md "wikilink")는 비슷한 접근 방식을 사용한다.

## 도스에 쓰이는 인터럽트 벡터

<table>
<thead>
<tr class="header">
<th><p>인터럽트 벡터</p></th>
<th><p>설명</p></th>
<th><p>버전</p></th>
<th><p>비고</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><code>20h</code></p></td>
<td><p>프로그램 끝내기</p></td>
<td><p>1.0 이상</p></td>
<td><p>도스 커널에 추가됨</p></td>
</tr>
<tr class="even">
<td><p><code>21h</code></p></td>
<td><p>주요 도스 API</p></td>
<td><p>1.0 이상</p></td>
<td><p>도스 커널에 추가됨</p></td>
</tr>
<tr class="odd">
<td><p><code>22h</code></p></td>
<td><p>프로그램 끝내기 주소</p></td>
<td><p>1.0 이상</p></td>
<td><p>프로그램 호출시 주소 반환</p></td>
</tr>
<tr class="even">
<td><p><code>23h</code></p></td>
<td><p>Control-C 핸들러 주소</p></td>
<td><p>1.0 이상</p></td>
<td><p>기본 핸들러는 도스 셸에 있음 (일반적으로 COMMAND.COM)</p></td>
</tr>
<tr class="odd">
<td><p><code>24h</code></p></td>
<td><p>심각한 오류 핸들러 주소</p></td>
<td><p>1.0 이상</p></td>
<td><p>기본 핸들러는 도스 셸에 있음 (일반적으로 COMMAND.COM)</p></td>
</tr>
<tr class="even">
<td><p><code>25h</code></p></td>
<td><p>절대 디스크 읽기</p></td>
<td><p>1.0 이상</p></td>
<td><p>도스 커널에 추가됨, 도스 3.31에서 강화되어 최대 2 GB 파티션 지원</p></td>
</tr>
<tr class="odd">
<td><p><code>26h</code></p></td>
<td><p>절대 디스크 쓰기</p></td>
<td><p>1.0 이상</p></td>
<td><p>도스 커널에 추가됨, 도스 3.31에서 강화되어 최대 2 GB 파티션 지원</p></td>
</tr>
<tr class="even">
<td><p><code>27h</code></p></td>
<td><p><a href="https://ko.wikipedia.org/wiki/종료_후_상주_프로그램" title="wikilink">종료 후 상주</a></p></td>
<td><p>1.0 이상</p></td>
<td><p>도스 1.0 및 도스 2.0 이상의 도스 커널에서 COMMAND.COM에 추가됨</p></td>
</tr>
<tr class="odd">
<td><p><code>28h</code></p></td>
<td><p>유휴 호출</p></td>
<td><p>2.0 이상</p></td>
<td><p>입력을 기다릴 때 도스 커널이 호출함</p></td>
</tr>
<tr class="even">
<td><p><code>29h</code></p></td>
<td><p>고속 콘솔 출력</p></td>
<td><p>2.0 이상</p></td>
<td><p>내장 콘솔 장치 드라이버나, ANSI.SYS와 같은 대안 드라이버에 의해 추가됨</p></td>
</tr>
<tr class="odd">
<td><p><code>2Ah</code></p></td>
<td><p>네트워크 및 중요 섹션</p></td>
<td><p>3.0 이상</p></td>
<td><p>네트워크 소프트웨어와의 상호 작용을 목적으로 도스 커널이 호출함</p></td>
</tr>
<tr class="even">
<td><p><code>2Bh</code></p></td>
<td><p>사용 안 함</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><code>2Ch</code></p></td>
<td><p>사용 안 함</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><code>2Dh</code></p></td>
<td><p>사용 안 함</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><code>2Eh</code></p></td>
<td><p>임시 항목 다시 불러오기(Reload transient)</p></td>
<td><p>2.0 이상</p></td>
<td><p>COMMAND.COM에 추가됨</p></td>
</tr>
<tr class="even">
<td><p><code>2Fh</code></p></td>
<td><p>다중 송신</p></td>
<td><p>3.0 이상</p></td>
<td><p>하부 함수 번호에 따라 도스 커널 및<br />
다양한 프로그램(PRINT, MSCDEX, DOSKEY, APPEND 등)에 추가됨</p></td>
</tr>
</tbody>
</table>

## DOS INT 21h 서비스

| `AH`  | 설명                                                | 버전      |
| ----- | ------------------------------------------------- | ------- |
| `00h` | 프로그램 끝내기                                          | 1.0 이상  |
| `01h` | 문자 입력                                             | 1.0 이상  |
| `02h` | 문자 출력                                             | 1.0 이상  |
| `03h` | 보조 입력                                             | 1.0 이상  |
| `04h` | 보조 출력                                             | 1.0 이상  |
| `05h` | 프린터 출력                                            | 1.0 이상  |
| `06h` | 직접 콘솔 입출력                                         | 1.0 이상  |
| `07h` | echo 없이 직접 콘솔 입력                                  | 1.0 이상  |
| `08h` | echo 없이 콘솔 입력                                     | 1.0 이상  |
| `09h` | 문자열 표시                                            | 1.0 이상  |
| `0Ah` | 버퍼 처리된 키보드 입력                                     | 1.0 이상  |
| `0Bh` | 입력 상태 가져오기                                        | 1.0 이상  |
| `0Ch` | 입력 버퍼 및 입력 플러시(flush) 처리                          | 1.0 이상  |
| `0Dh` | 디스크 초기화                                           | 1.0 이상  |
| `0Eh` | 기본 드라이브 설정                                        | 1.0 이상  |
| `0Fh` | 파일 열기                                             | 1.0 이상  |
| `10h` | 파일 닫기                                             | 1.0 이상  |
| `11h` | 첫 번째 파일 찾기                                        | 1.0 이상  |
| `12h` | 다음 파일 찾기                                          | 1.0 이상  |
| `13h` | 파일 삭제                                             | 1.0 이상  |
| `14h` | 연속 읽기                                             | 1.0 이상  |
| `15h` | 연속 쓰기                                             | 1.0 이상  |
| `16h` | 파일 만들기/끊기                                         | 1.0 이상  |
| `17h` | 파일 이름 변경                                          | 1.0 이상  |
| `18h` | 예비                                                | 1.0 이상  |
| `19h` | 기본 드라이브 가져오기                                      | 1.0 이상  |
| `1Ah` | 디스크 전송 주소 설정                                      | 1.0 이상  |
| `1Bh` | 기본 드라이브에 대한 할당 정보 가져오기                            | 1.0 이상  |
| `1Ch` | 지정된 드라이브에 대한 할당 정보 가져오기                           | 1.0 이상  |
| `1Dh` | 예비                                                | 1.0 이상  |
| `1Eh` | 예비                                                | 1.0 이상  |
| `1Fh` | 기본 드라이브에 대한 디스크 변수 블록 가져오기                        | 1.0 이상  |
| `20h` | 예비                                                | 1.0 이상  |
| `21h` | 랜덤 읽기                                             | 1.0 이상  |
| `22h` | 랜덤 쓰기                                             | 1.0 이상  |
| `23h` | 레코드의 파일 크기 가져오기                                   | 1.0 이상  |
| `24h` | 랜덤 레코드 번호 설정                                      | 1.0 이상  |
| `25h` | 인터럽트 벡터 설정                                        | 1.0 이상  |
| `26h` | PSP 만들기                                           | 1.0 이상  |
| `27h` | 랜덤 블록 읽기                                          | 1.0 이상  |
| `28h` | 랜덤 블록 쓰기                                          | 1.0 이상  |
| `29h` | 파일 이름 분석(Parse)                                   | 1.0 이상  |
| `2Ah` | 날짜 가져오기                                           | 1.0 이상  |
| `2Bh` | 날짜 설정                                             | 1.0 이상  |
| `2Ch` | 시간 가져오기                                           | 1.0 이상  |
| `2Dh` | 시간 설정                                             | 1.0 이상  |
| `2Eh` | 유효 플래그 설정                                         | 1.0 이상  |
| `2Fh` | 디스크 전송 주소 가져오기                                    | 2.0 이상  |
| `30h` | 도스 버전 가져오기                                        | 2.0 이상  |
| `31h` | 종료 후 상주                                           | 2.0 이상  |
| `32h` | 지정된 드라이브에 대한 디스크 변수 블록 가져오기                       | 2.0 이상  |
| `33h` | Ctrl-Break 가져오기 또는 설정                             | 2.0 이상  |
| `34h` | InDOS 플래그 포인터 가져오기                                | 2.0 이상  |
| `35h` | 인터럽트 벡터 가져오기                                      | 2.0 이상  |
| `36h` | 디스크 남은 공간 가져오기                                    | 2.0 이상  |
| `37h` | 스위치 문자 가져오기 또는 설정                                 | 2.0 이상  |
| `38h` | 국가 정보 가져오기 또는 설정                                  | 2.0 이상  |
| `39h` | 하위 디렉터리 만들기                                       | 2.0 이상  |
| `3Ah` | 하위 디렉터리 제거                                        | 2.0 이상  |
| `3Bh` | 현재 디렉터리 변경                                        | 2.0 이상  |
| `3Ch` | 파일 만들기 또는 끊기                                      | 2.0 이상  |
| `3Dh` | 파일 열기                                             | 2.0 이상  |
| `3Eh` | 파일 닫기                                             | 2.0 이상  |
| `3Fh` | 파일 또는 장치 읽기                                       | 2.0 이상  |
| `40h` | 파일 또는 장치 쓰기                                       | 2.0 이상  |
| `41h` | 파일 삭제                                             | 2.0 이상  |
| `42h` | 파일 포인터 이동                                         | 2.0 이상  |
| `43h` | 파일 특성 가져오기 또는 설정                                  | 2.0 이상  |
| `44h` | 장치에 대한 입출력 제어                                     | 2.0 이상  |
| `45h` | 핸들 복제                                             | 2.0 이상  |
| `46h` | 핸들 우회                                             | 2.0 이상  |
| `47h` | 현재 디렉터리 가져오기                                      | 2.0 이상  |
| `48h` | 메모리 할당                                            | 2.0 이상  |
| `49h` | 메모리 해제                                            | 2.0 이상  |
| `4Ah` | 메모리 다시 할당                                         | 2.0 이상  |
| `4Bh` | 프로그램 실행                                           | 2.0 이상  |
| `4Ch` | 반환 코드로 끝내기                                        | 2.0 이상  |
| `4Dh` | 프로그램 반환 코드 가져오기                                   | 2.0 이상  |
| `4Eh` | 첫 번째 파일 찾기                                        | 2.0 이상  |
| `4Fh` | 다음 파일 찾기                                          | 2.0 이상  |
| `50h` | 현재의 PSP 설정                                        | 2.0 이상  |
| `51h` | 현재의 PSP 가져오기                                      | 2.0 이상  |
| `52h` | 도스 내부 포인터 가져오기 (SYSVARS)                          | 2.0 이상  |
| `53h` | 디스크 변수 블록 만들기                                     | 2.0 이상  |
| `54h` | 유효 플래그 가져오기                                       | 2.0 이상  |
| `55h` | 프로그램 PSP 만들기                                      | 2.0 이상  |
| `56h` | 파일 이름 변경                                          | 2.0 이상  |
| `57h` | 파일 날짜 및 시간 가져오기 또는 설정                             | 2.0 이상  |
| `58h` | 할당 전략 가져오기 또는 설정                                  | 2.11 이상 |
| `59h` | 확장 오류 정보 가져오기                                     | 3.0 이상  |
| `5Ah` | 고유 파일 만들기                                         | 3.0 이상  |
| `5Bh` | 파일 새로 만들기                                         | 3.0 이상  |
| `5Ch` | 파일 잠금 / 잠금 해제                                     | 3.0 이상  |
| `5Dh` | 파일 공유 기능                                          | 3.0 이상  |
| `5Eh` | 네트워크 기능                                           | 3.0 이상  |
| `5Fh` | 네트워크 우회 기능                                        | 3.0 이상  |
| `60h` | 파일 이름 제한                                          | 3.0 이상  |
| `61h` | 예비                                                | 3.0 이상  |
| `62h` | 현재의 PSP 가져오기                                      | 3.0 이상  |
| `63h` | DBCS 리드 바이트 테이블 포인터(lead byte table pointer) 가져오기 | 3.0 이상  |
| `64h` | 외부 이벤트 플래그 대기 설정                                  | 3.2 이상  |
| `65h` | 확장 국가 정보 가져오기                                     | 3.3 이상  |
| `66h` | 코드 페이지 가져오기 또는 설정                                 | 3.3 이상  |
| `67h` | 핸들 수 설정                                           | 3.3 이상  |
| `68h` | 파일 위탁(commit)                                     | 3.3 이상  |
| `69h` | 미디어 ID 가져오기 또는 설정                                 | 4.0 이상  |
| `6Ah` | 파일 위탁(commit)                                     | 4.0 이상  |
| `6Bh` | 예비                                                | 4.0 이상  |
| `6Ch` | 파일 확장 열기/만들기                                      | 4.0 이상  |

## MS-DOS API를 지원하는 운영 체제

  - [MS-DOS](https://ko.wikipedia.org/wiki/MS-DOS "wikilink")
  - [PC DOS](https://ko.wikipedia.org/wiki/IBM_PC_DOS "wikilink")
  - [DR-DOS](https://ko.wikipedia.org/wiki/DR-DOS "wikilink")
  - [PTS-DOS](https://ko.wikipedia.org/wiki/PTS-DOS "wikilink")
  - [ROM-DOS](https://ko.wikipedia.org/wiki/ROM-DOS "wikilink")
  - [FreeDOS](https://ko.wikipedia.org/wiki/FreeDOS "wikilink")
  - [윈도 95](https://ko.wikipedia.org/wiki/윈도_95 "wikilink") - MS-DOS 7.0 포함
  - [윈도 98](https://ko.wikipedia.org/wiki/윈도_98 "wikilink") - MS-DOS 7.1 포함
  - [윈도 98 SE](https://ko.wikipedia.org/wiki/윈도_98_SE "wikilink") - MS-DOS 7.1 포함
  - [윈도 ME](https://ko.wikipedia.org/wiki/윈도_ME "wikilink") - MS-DOS 8.0 포함

## MS-DOS API 지원 프로그램

  - [PCMODE](https://ko.wikipedia.org/wiki/멀티유저_도스 "wikilink") 포함 [컨커런트 CP/M-86](https://ko.wikipedia.org/wiki/MP/M "wikilink") (3.1 전용)
  - [컨커런트 도스](https://ko.wikipedia.org/wiki/멀티유저_도스 "wikilink")
  - [도스 플러스](https://ko.wikipedia.org/wiki/도스_플러스 "wikilink")
  - [멀티유저 도스](https://ko.wikipedia.org/wiki/멀티유저_도스 "wikilink")
  - [NTVDM.EXE](../Page/가상_도스_머신.md "wikilink") ([윈도 NT](https://ko.wikipedia.org/wiki/윈도_NT "wikilink") 계열)
  - [DOSEMU](../Page/DOSEMU.md "wikilink") ([리눅스](https://ko.wikipedia.org/wiki/리눅스 "wikilink"))
  - [도스박스](../Page/도스박스.md "wikilink")

## 같이 보기

  - [바이오스 인터럽트 호출](https://ko.wikipedia.org/wiki/바이오스_인터럽트_호출 "wikilink")
  - [도스 확장자](../Page/도스_확장자.md "wikilink")

## 참고문헌

  - [The x86 Interrupt List](http://www.cs.cmu.edu/~ralf/files.html) (a.k.a. RBIL, Ralf Brown's Interrupt List)

  - [ctyme.com - INT Calls by function](http://www.ctyme.com/intr/cat-010.htm)

  - [wustl.edu - Description of MS-DOS services](https://web.archive.org/web/20020622163518/http://www.arl.wustl.edu/~lockwood/class/cs306/books/artofasm/toc.html)

  - [IBM PC DOS 7 Technical Update](https://web.archive.org/web/20060721115437/http://www.redbooks.ibm.com/redbooks/pdfs/gg244459.pdf)

  - *Microsoft MS-DOS Programmer's Reference - The Official Technical Reference to MS-DOS*, Microsoft Press, 1993

  - *The MS-DOS Encyclopedia*, Microsoft Press, 1988,

  - *Advanced MS-DOS Programming: The Microsoft Guide for Assembly Language and C Programmers* by Ray Duncan, Microsoft Press, 1988

  - *The Programmer's PC Sourcebook* by Thom Hogan, Microsoft Press, 1991

  - *The New Peter Norton Programmer's Guide to the IBM PC & PS/2* by Peter Norton and Richard Wilton, Microsoft Press, 1987 .

  - Caldera, Inc. (1997). *OpenDOS Developer's Reference Series — OpenDOS Programmer's Guide — System and Programmer's Guide*. Printed in the UK, August 1997. Caldera Part No. 200-DOPG-003 ([1](https://web.archive.org/web/20120625021802/http://www.drdos.net/documentation/sysprog/httoc.htm)).

[분류:도스 기술](https://ko.wikipedia.org/wiki/분류:도스_기술 "wikilink") [분류:X86 아키텍처](https://ko.wikipedia.org/wiki/분류:X86_아키텍처 "wikilink") [분류:인터럽트](https://ko.wikipedia.org/wiki/분류:인터럽트 "wikilink") [분류:마이크로소프트 API](https://ko.wikipedia.org/wiki/분류:마이크로소프트_API "wikilink") [분류:운영 체제 API](https://ko.wikipedia.org/wiki/분류:운영_체제_API "wikilink")