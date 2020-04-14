> This article is converted from Wikipedia: [Win32 스레드 정보 블록](https://ko.wikipedia.org/wiki/Win32_스레드_정보_블록).


**TIB ()** (TIB)은 Win32의 [자료 구조로서](../Page/자료_구조.md "wikilink") 현재 실행 중인 [스레드](https://ko.wikipedia.org/wiki/스레드 "wikilink")에 대한 정보를 저장하고 있다. 이 구조체는 또한 스레드 환경 블록 (TEB: Thread Environment Block)으로도 알려져 있다.\[1\]

이 TIB는 공식적으로 윈도 9x에서는 문서화되어 있지 않다. 윈도 NT 시리즈 DDK는 하위 시스템 독립적인 부분을 문서화한 winnt.h에 NT_TIB 구조체를 포함한다. [와인은](../Page/와인_\(소프트웨어\).md "wikilink") 확장된 (구체적인 하위 시스템 부분의) TIB를 위한 선언을 포함한다. 수 많은 Win32 프로그램들은 실질적으로 API의 한 부분이라고 할 수 있는 이 문서화되지 않은 필드들을 사용한다. 특히 첫 번째 필드는 마이크로소프트의 자체 컴파일러에서 직접적으로 코드에 의한 참조가 일어난다.\[2\]

TIB는 Win32 API를 호출하지 않고도 프로세스에 대한 많은 정보를 얻기 위해 사용될 수 있다. [PEB](https://ko.wikipedia.org/wiki/PEB "wikilink")를 가리키는 포인터를 통해서 IAT에 대한 접근, 프로세스 시작 인수, 이미지 이름 등을 얻을 수 있다.

## TIB의 내용 (32비트 윈도우)

| 위치                                                                     | 길이   | 윈도우 버전       | 설명                                                                                                                  |
| ---------------------------------------------------------------------- | ---- | ------------ | ------------------------------------------------------------------------------------------------------------------- |
| FS:\[0x00\]                                                            | 4    | Win9x and NT | 현재 Structured Exception Handling (SEH) 프레임                                                                          |
| FS:\[0x04\]                                                            | 4    | Win9x and NT | 스택 베이스 / 스택의 바닥 (높은 주소)                                                                                             |
| FS:\[0x08\]                                                            | 4    | Win9x and NT | 스택 한계 / 스택의 천장 (낮은 주소)                                                                                              |
| FS:\[0x0C\]                                                            | 4    | NT           | SubSystemTib                                                                                                        |
| FS:\[0x10\]                                                            | 4    | NT           | [Fiber data](https://ko.wikipedia.org/wiki/스레드 "wikilink")                                                          |
| FS:\[0x14\]                                                            | 4    | Win9x and NT | 임의 데이터 슬롯                                                                                                           |
| FS:\[0x18\]                                                            | 4    | Win9x and NT | Thread Environment Block                                                                                            |
| \---- [NT subsystem](../Page/윈도우_NT_아키텍처.md "wikilink") 독립적인 부분 끝 ---- |      |              |                                                                                                                     |
| FS:\[0x1C\]                                                            | 4    | NT           | Environment Pointer                                                                                                 |
| FS:\[0x20\]                                                            | 4    | NT           | 프로세스 ID (몇몇 윈도우 버전에서 이 필드는 'DebugContext'로 쓰인다.)                                                                    |
| FS:\[0x24\]                                                            | 4    | NT           | 현재 스레드 ID                                                                                                           |
| FS:\[0x28\]                                                            | 4    | NT           | 활동중인 RPC 핸들                                                                                                         |
| FS:\[0x2C\]                                                            | 4    | Win9x and NT | thread-local storage 배열의 선형 주소                                                                                      |
| FS:\[0x30\]                                                            | 4    | NT           | Process Environment Block (PEB)의 선형 주소                                                                              |
| FS:\[0x34\]                                                            | 4    | NT           | 마지막 오류 번호                                                                                                           |
| FS:\[0x38\]                                                            | 4    | NT           | Count of owned critical sections                                                                                    |
| FS:\[0x3C\]                                                            | 4    | NT           | CSR 클라이언트 스레드의 주소                                                                                                   |
| FS:\[0x40\]                                                            | 4    | NT           | Win32 스레드 정보                                                                                                        |
| FS:\[0x44\]                                                            | 124  | NT, Wine     | Win32 클라이언트 정보 (NT), user32 private data (Wine), 0x60 = LastError (Win95), 0x74 = LastError (WinME)                 |
| FS:\[0xC0\]                                                            | 4    | NT           | Reserved for Wow64. Wow64에서 FastSysCall에 대한 포인터를 포함한다.                                                              |
| FS:\[0xC4\]                                                            | 4    | NT           | Current Locale                                                                                                      |
| FS:\[0xC8\]                                                            | 4    | NT           | FP Software Status Register                                                                                         |
| FS:\[0xCC\]                                                            | 216  | NT, Wine     | Reserved for OS (NT), kernel32 private data (Wine) herein: FS:\[0x124\] 4 NT Pointer to KTHREAD (ETHREAD) structure |
| FS:\[0x1A4\]                                                           | 4    | NT           | 예외 코드                                                                                                               |
| FS:\[0x1A8\]                                                           | 18   | NT           | Activation context stack                                                                                            |
| FS:\[0x1BC\]                                                           | 24   | NT, Wine     | Spare bytes (NT), ntdll private data (Wine)                                                                         |
| FS:\[0x1D4\]                                                           | 40   | NT, Wine     | Reserved for OS (NT), ntdll private data (Wine)                                                                     |
| FS:\[0x1FC\]                                                           | 1248 | NT, Wine     | GDI TEB Batch (OS), vm86 private data (Wine)                                                                        |
| FS:\[0x6DC\]                                                           | 4    | NT           | GDI Region                                                                                                          |
| FS:\[0x6E0\]                                                           | 4    | NT           | GDI 펜                                                                                                               |
| FS:\[0x6E4\]                                                           | 4    | NT           | GDI 브러시                                                                                                             |
| FS:\[0x6E8\]                                                           | 4    | NT           | Real Process ID                                                                                                     |
| FS:\[0x6EC\]                                                           | 4    | NT           | Real Thread ID                                                                                                      |
| FS:\[0x6F0\]                                                           | 4    | NT           | GDI cached process handle                                                                                           |
| FS:\[0x6F4\]                                                           | 4    | NT           | GDI 클라이언트 프로세스 ID (PID)                                                                                             |
| FS:\[0x6F8\]                                                           | 4    | NT           | GDI 클라이언트 스레드 ID (TID)                                                                                              |
| FS:\[0x6FC\]                                                           | 4    | NT           | GDI thread locale information                                                                                       |
| FS:\[0x700\]                                                           | 20   | NT           | Reserved for user application                                                                                       |
| FS:\[0x714\]                                                           | 1248 | NT           | Reserved for GL                                                                                                     |
| FS:\[0xBF4\]                                                           | 4    | NT           | 마지막 상태 값                                                                                                            |
| FS:\[0xBF8\]                                                           | 532  | NT           | Static UNICODE_STRING buffer                                                                                       |
| FS:\[0xE0C\]                                                           | 4    | NT           | deallocation stack에 대한 포인터                                                                                          |
| FS:\[0xE10\]                                                           | 256  | NT           | TLS 슬롯, 슬롯 당 4 byte                                                                                                 |
| FS:\[0xF10\]                                                           | 8    | NT           | TLS 링크 (LIST_ENTRY structure)                                                                                      |
| FS:\[0xF18\]                                                           | 4    | NT           | VDM                                                                                                                 |
| FS:\[0xF1C\]                                                           | 4    | NT           | Reserved for RPC                                                                                                    |
| FS:\[0xF28\]                                                           | 4    | NT           | 스레드 에러 모드(RtlSetThreadErrorMode)                                                                                    |

FS는 TIB를 저장하는데, TDB(스레드 데이터 베이스)라고 알려진 데이터 블록에 내장되어 있다. TIB는 스레드에 관련된 예외 핸들링 체인과 TLS(thread local storage)에 대한 포인터를 포함한다.

노트: 위의 설명은 오직 x86 32비트 윈도우에서 설명하는 것이다. x86-64 (64-bit) 윈도우에서, GS (FS가 아니라)는 TIB를 가리키는 세그먼트 레지스터로 사용된다. 게다가 위 구조체의 몇몇 변수 슬롯들은 다른 크기를 가진다.

## TIB에 접근하기

현재 스레드의 TIB는 세그먼트 [레지스터](../Page/프로세서_레지스터.md "wikilink") FS (x86) 또는 GS (x64)의 오프셋으로 접근할 수 있다.

FS:\[0\] 부터 오프셋으로 TIB 필드에 접근하는 것 대신 FS:\[0x18\]에 저장된 먼저 선형 자기 참조 포인터를 가지는 것이 TIB 필드에 접근하는 보편적인 방식이다. 이 포인터는 포인터 연산 등에 사용될 수 있다.

32-bit x86에서의 C inlined-assembly 예시:

``` c
// gcc (AT&T-style inline assembly).
void *getTIB() {
    void *pTIB;
    __asm__("movl %%fs:0x18, %0" : "=r" (pTIB) : : );
    return pTIB;
}
```

``` c
// Microsoft C
void *getTIB() {
    void *pTIB;
    __asm {
        mov EAX, FS:[0x18]
        mov pTIB, EAX
    }
    return pTIB;
}
```

``` c
// Using Microsoft's intrinsics instead of inline assembly
void *getTIB() {
    return = (void *)__readfsdword(0x18);
}
```

## 읽어보기

  - [마이크로소프트의 예외 처리 메커니즘](../Page/마이크로소프트의_예외_처리_메커니즘.md "wikilink")(SEH)

## 각주

## 함께 읽기

  -
## 외부 링크

  - [TEB layout on NTinternals.net](http://undocumented.ntinternals.net/UserMode/Undocumented%20Functions/NT%20Objects/Thread/TEB.html)
  - [Structured Exception Handling and the TIB](https://web.archive.org/web/20150929000043/http://www.microsoft.com/msj/0197/exception/exception.aspx)

[분류:마이크로소프트 API](https://ko.wikipedia.org/wiki/분류:마이크로소프트_API "wikilink") [분류:스레드](https://ko.wikipedia.org/wiki/분류:스레드 "wikilink")

1.
2.