> This article is converted from Wikipedia: [MZ 실행 파일](https://ko.wikipedia.org/wiki/MZ_실행_파일).


**MZ 실행 파일** 형식은 [DOS](https://ko.wikipedia.org/wiki/DOS "wikilink")에서 [.EXE](../Page/EXE.md "wikilink") [실행 파일에](../Page/실행_파일.md "wikilink") 사용되는 [파일 형식이다](https://ko.wikipedia.org/wiki/파일_형식 "wikilink").

파일의 맨 앞에 있는 "MZ"라는 아스키 문자열([16진수로는](../Page/십육진법.md "wikilink") 4D 5A)로 식별할 수 있다. 이런 걸 "[매직 넘버](https://ko.wikipedia.org/wiki/매직_넘버 "wikilink")"라고 한다. "MZ"는 [MS-DOS](../Page/MS-DOS.md "wikilink")의 개발자였던 [Mark Zbikowski의](https://ko.wikipedia.org/wiki/:en:Mark_Zbikowski "wikilink") 머리글자를 딴 것이다.

MZ 실행 파일은 기존 COM 실행 파일 대비 새로운 형식이다. 파일은 [머리에](https://ko.wikipedia.org/wiki/헤더_\(컴퓨팅\) "wikilink") [릴로케이션](https://ko.wikipedia.org/wiki/릴로케이션_테이블 "wikilink") 정보를 가지는데, 이것은 여러 세그먼트를 임의의 메모리에 올릴 수 있도록 해준다. 그리고 64KiB보다 큰 실행 파일을 만들 수 있다. 하지만, 옵셋에 대한 64KiB의 한계는 여전하다. 이것은 나중에 나오는 [도스 확장자를](../Page/도스_확장자.md "wikilink") 사용해서 피할 수 있다.

도스를 통해 구동되는 EXE 프로그램의 환경은 [프로그램 세그먼트 프리픽스에서](https://ko.wikipedia.org/wiki/프로그램_세그먼트_프리픽스 "wikilink") 볼 수 있다.

## 기본 머리

| OFFSET | TYPE   | 설명                                                                 |
| ------ | ------ | ------------------------------------------------------------------ |
| 0000h  | c char | 'MZ'(0x4d, 0x5a)                                                   |
| 0002h  | 1 word | 마지막 페이지(블록이라고도 한다)의 바이트 수. 한 페이지는 512바이트다.                         |
| 0004h  | 1 word | 파일에 있는 총 페이지 수.                                                    |
| 0006h  | 1 word | 재배치 항목의 수                                                          |
| 0008h  | 1 word | 단락 단위의 머리 크기. 한 단락의 16바이트다.                                        |
| 000Ah  | 1 word | 파일에 포함된 실제 프로그램의 크기에 추가로 최소한 확보되어야 할 단락의 수                         |
| 000Ch  | 1 word | 최대로 확보되어야 할 단락의 수. 보통 최댓값인 65535인데, 이건 1M나 되기 때문에 남은 메모리가 모두 할당된다. |
| 000Eh  | 1 word | Initial SS relative to start of executable                         |
| 0010h  | 1 word | Initial SP                                                         |
| 0012h  | 1 word | 실행파일 체크섬 (또는 0)                                                    |
| 0014h  | 1 word | IP relative to start of executable (entry point)                   |
| 0016h  | 1 word | CS relative to start of executable (entry point)                   |
| 0018h  | 1 word | 재배치 정보표의 시작위치; 40h for new-(NE,LE,LX,W3,PE etc.) executable        |
| 001Ah  | 1 word | Overlay number (0h = 메인 프로그램)                                      |

아래 구조체는 DOSBOX의 소스에서 가져온 것이다.

``` c
#ifdef _MSC_VER
#pragma pack(1)
#endif
struct EXE_Header {
    Bit16u signature;       /* EXE 서명 MZ 또는 ZM */
    Bit16u extrabytes;      /* 마지막 페이지의 바이트 */
    Bit16u pages;           /* 파일 내 페이지 */
    Bit16u relocations;     /* 파일 내 릴로케이션 */
    Bit16u headersize;      /* 헤더 내 문단 */
    Bit16u minmemory;       /* 최소 메모리 양 */
    Bit16u maxmemory;       /* 최대 메모리 양 */
    Bit16u initSS;
    Bit16u initSP;
    Bit16u checksum;
    Bit16u initIP;
    Bit16u initCS;
    Bit16u reloctable;
    Bit16u overlay;
} GCC_ATTRIBUTE(packed);
#ifdef _MSC_VER
#pragma pack()
#endif
```

파일은 16바이트인 단락(Paragraph)과 512바이트인 페이지 단위로 크기를 표현한다. 따라서 파일의 전체 크기는 (pages - 1) \* 512 + extrabytes로 표현될 수 있다. 여기에는 머리와 재배치 정보도 포함된다. 말 그대로 전체 파일의 크기다.

꼭 그래야 하는 것은 아니지만, 코드 부분이 페이지 단위로 정렬될 수 있게 머리의 크기가 페이지 단위가 되도록 채워지는 경우가 많다. 즉, 재배치 정보가 전혀 없더라도 headersize = 32가 되는 식이다. headersize는 단락의 수이기 때문에 32 \* 16 = 512로 페이지 하나의 크기다.

## 덧붙인 머리

MZ를 만들어 낼 수 있는 다양한 제품들은 저마다 자신들만의 목적을 위해 기본 머리 뒷쪽에 뭔가를 덧붙이고 있다. 외부 링크 [EXE Format (영어)](http://www.fileformat.info/format/exe/corion-mz.htm) 에 관련한 내용이 여럿 포함되어 있다. 대부분은 어떤 제품으로 만들어졌는지를 표시하는 정도이고, 진짜로 해당 제품만을 위한 것은 구체적인 정보가 없는 상태다.

마이크로소프트의 새 실행 파일 형식인 PE도 기본은 MZ이기 때문에 덧붙인 머리에 PE 머리에 대한 정보가 추가되어 있다. 아래 구조체는 MS의 SDK에 포함된 것이다. 앞 부분은 변수명만 다르게 정의되었을 뿐 기본 머리와 같다. PE에서 실질적인 의미가 있는 것은 맨 마지막의 e_lfanew 뿐이다. 새 형식의 머리가 어디에 있는지에 대한 정보다. 나머지 덧붙인 정보들은 PE가 만들어질 때까지 여러 제품들이 추가했던 정보들을 모두 반영하기 위한 형식적인 것이다.

``` c
typedef struct _IMAGE_DOS_HEADER {      // DOS .EXE header
    WORD   e_magic;                     // Magic number
    WORD   e_cblp;                      // Bytes on last page of file
    WORD   e_cp;                        // Pages in file
    WORD   e_crlc;                      // Relocations
    WORD   e_cparhdr;                   // Size of header in paragraphs
    WORD   e_minalloc;                  // Minimum extra paragraphs needed
    WORD   e_maxalloc;                  // Maximum extra paragraphs needed
    WORD   e_ss;                        // Initial (relative) SS value
    WORD   e_sp;                        // Initial SP value
    WORD   e_csum;                      // Checksum
    WORD   e_ip;                        // Initial IP value
    WORD   e_cs;                        // Initial (relative) CS value
    WORD   e_lfarlc;                    // File address of relocation table
    WORD   e_ovno;                      // Overlay number
    WORD   e_res[4];                    // Reserved words
    WORD   e_oemid;                     // OEM identifier (for e_oeminfo)
    WORD   e_oeminfo;                   // OEM information; e_oemid specific
    WORD   e_res2[10];                  // Reserved words
    LONG   e_lfanew;                    // File address of new exe header
  } IMAGE_DOS_HEADER, *PIMAGE_DOS_HEADER;
```

## 재배치 정보

COM 처럼 64KiB 안에서만 움직인다면 프로그램을 만드는 순간에 모든 주소를 분명하게 알 수 있다. 이렇게 만들어진 프로그램은 메모리의 어떤 위치에 올리게 되더라도 시작점을 세그먼트로 잡아주기만 하면 나머지는 그에 대한 상대위치이기 때문에 실행에 아무런 문제가 없다.

그러나 MZ 형식은 64KiB라는 한계를 벗기 위해 여러 세그먼트를 가지도록 한 것이 핵심이다. 그런데 이 세그먼트란 것이 실제 메모리 위치를 가리키는 값이기 때문에 프로그램을 만들 때는 그 정확한 값을 알 수가 없다. 메모리에 올려줘야만 알 수 있다. 이 문제를 해결하려면 프로그램하는 동안에는 자신이 0번지에 올려지는 것처럼 주소를 산정하고, 실제로 특정 메모리로 올려질 때 그 시작점을 0을 기준으로 했던 모든 세그먼트에 더해줘야 한다. 이것이 재배치다.

MZ 실행 파일은 이렇게 재배치가 필요한 세그먼트가 사용된 곳를 모두 모아서 재배치 표를 만들어 가진다. 도스는 프로그램을 메모리로 올리면서 재배치 표에 기록된 즉, 프로그램 중에 세그먼트가 사용된 곳을 모두 찾아서 그기에 실제 프로그램이 시작하는 주소, 보다 정확하게는 시작 세그먼트를 더해준다.

재배치 표는 프로그램 중에 세그먼트가 사용된 곳의 주소(Segment:Offset)의 나열이다.

| OFFSET | TYPE   | 설명          |
| ------ | ------ | ----------- |
| 0000h  | 1 word | Offset      |
| 0002h  | 1 word | 재배치 Segment |

재배치 항목의 하나는 이렇게 Offset과 Segment가 각 한 워드씩 총 4바이트를 차지한다. 이런 것이 머리에 기록된 relocations 만큼 있다.

## 실제

``` asm
format MZ

entry _text:main
stack 80h

segment _text

main:
    mov ax,_data
    mov ds,ax

    mov ah,9
    mov dx,hello
    int 21h

    mov ax,4c00h
    int 21h

segment _data

hello   db 'Hello world!', 24h
```

FASM을 사용하면 이 프로그램은 77바이트의 아주 작은 MZ 파일이 된다.

``` asm
0000000: 4d5a 4d00 0100 0100 0200 0800 ffff 0300  MZM.............
0000010: 8000 0000 0000 0000 1c00 0000 0100 0000  ................
0000020: b802 008e d8b4 09ba 0000 cd21 b800 4ccd  ...........!..L.
0000030: 2100 0000 0000 0000 0000 0000 0000 0000  !...............
0000040: 4865 6c6c 6f20 776f 726c 6421 240d 0a    Hello world!$..
```

기본 머리 부분을 읽기 쉽게 바꾸면

``` c
signature="MZ"
extrabytes=77
pages=1
relocations=1
headersize=2
minmemory=8
maxmemory=65535
initSS=3
initSP=128
checksum=0
initIP=0
initCS=0
reloctable=28
overlay=0
```

당연히 시작은 "MZ"다. 그리고 파일이 77바이트이기 때문에 pages=1로 페이지는 하나뿐이고, 그 페이지의 사용 바이트는 extrabytes=77이다.

재배치 항목은 relocations=1개가 있고, 재배치 표는 reloctable=28에서 시작한다. 기본 머리의 크기가 28이므로 재배치 표가 머리 다음에 바로 이어지고 있다는 것을 알 수 있다. FASM은 별도의 추가 정보를 덧붙이지 않고 기본 머리만을 만들어내고 있는 것이다. 하나 있는 재배치 항목은 0000:0001이다.

headersize=2이므로 실제 코드의 시작은 2 \* 16으로 32(0x20)부터다. 실제로 0x20의 있는 값들은 _text 세그먼트의 코드들이다. 이를 거꾸로 역어셈블리해보면

``` asm
    mov ax,0x0002
    mov ds,ax
```

소스에서의 _data가 0x0002가 되어 있음을 확인할 수 있다. 파일 위치 0x20에서 실제 코드가 시작된다. 즉, 프로그램적으로는 여기가 시작점으로 0번지로 가정된다. 따라서 "Hello..."가 있는 0x40은 프로그램 번지로는 0x20이고, 그래서 세그먼크가 0x0002가 되는 것이다. 하지만 이 값은 실제로 이 프로그램이 메모리에 올려질 때 그 메모리 번지에 맞도록 고쳐져야 한다. 그래서 0000:0001 위치가 재배치 표에 올라 있는 것이다.

minmemory=8은 stack 80h 때문이다. stack은 초기화된다거나 하는 대상이 아니기 때문에 그냥 메모리만 확보하면 된다. 그래서 stack 80h를 한다고 하더라도 파일에 80h만큼이 공간이 확보된다거나 그러지 않는다. 단지 minmemory=8라는 설정을 통해 메모리가 추가로 80h만큼은 반드시 더 확보되도록 한다. maxmemory=65535은 남은 메모리를 모두 할당하도록 한다.

코드 부분인 _text의 크기가 0x20, _data의 크기는 0x0e지만 16바이트의 문단 단위로 메모리를 관리하기 때문에 stack은 그 이후에 잡힌다. 그래서 SS:IP가 0003:0080으로 된다. CS:IP는 0번지에서 바로 시작하므로 0000:0000이다. 만약 소스에서 _text와 _data의 위치를 서로 바꾼다면 다른 변화도 생기겠지만, CS:IP가 _data의 크기만큼 뒤로 밀리게 된다. _data은 문단 단위의 경계에 맞추려면 크기가 0x10이 되기 때문에 CS:IP는 0001:0000이 될 것이다.

## 호환성

MZ 실행 파일은 DOS와 [윈도 9x](https://ko.wikipedia.org/wiki/윈도_9x "wikilink") 계열의 OS에서 실행된다. 32비트인 [윈도 NT](https://ko.wikipedia.org/wiki/윈도_NT "wikilink") 계열에서도 [가상 도스 머신이라는](../Page/가상_도스_머신.md "wikilink") 방식으로 실행할 수 있지만, 그래픽 모드를 사용하는 일부는 안된다. 64비트 윈도에서는 실행할 수 없다. 대신에 [DOSBox](https://ko.wikipedia.org/wiki/DOSBox "wikilink"), [DOSEMU](../Page/DOSEMU.md "wikilink"), [와인](../Page/와인_\(소프트웨어\).md "wikilink") 등을 사용해서 실행할 수 있다.

[디지털 마스](https://ko.wikipedia.org/wiki/디지털_마스 "wikilink") [Optlink](https://ko.wikipedia.org/wiki/Optlink "wikilink"), [MS 링커](https://ko.wikipedia.org/wiki/MS_링커 "wikilink"), [VALX](https://ko.wikipedia.org/wiki/VALX "wikilink"), [오픈 왓콤의](https://ko.wikipedia.org/wiki/오픈_왓콤 "wikilink") WLINK, 등등의 링커로 MZ 실행 파일을 만들 수 있다. 덧붙여 [FASM](../Page/FASM.md "wikilink")로는 바로 만들 수 있다.

## 같이 보기

  - [도스](../Page/도스.md "wikilink")
  - [도스 확장자](../Page/도스_확장자.md "wikilink")
  - [MS-DOS API](../Page/MS-DOS_API.md "wikilink")

## 외부 링크

  - [EXE Format](http://www.fileformat.info/format/exe/corion-mz.htm)

  - [MZ DOS EXE file format](http://www.delorie.com/djgpp/doc/exe/)

[분류:실행 파일 포맷](https://ko.wikipedia.org/wiki/분류:실행_파일_포맷 "wikilink")