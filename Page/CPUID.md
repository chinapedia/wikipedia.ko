> This article is converted from Wikipedia: [CPUID](https://ko.wikipedia.org/wiki/CPUID).


**CPUID** [opcode](https://ko.wikipedia.org/wiki/opcode "wikilink")는 [x86](https://ko.wikipedia.org/wiki/x86 "wikilink") 아키텍처를 위한 프로세서 기계 명령어이다. (CPUID는 [CPU](https://ko.wikipedia.org/wiki/중앙_처리_장치 "wikilink") IDentification에서 비롯한다.) [인텔](https://ko.wikipedia.org/wiki/인텔 "wikilink")이 펜티엄과 SL 강화 486 프로세서를 내세운 1993년에 도입하였다.\[1\]

CPUID opcode를 사용하여 소프트웨어는 프로세서 종류와 [MMX](../Page/MMX.md "wikilink")/[SSE와](../Page/스트리밍_SIMD_확장.md "wikilink") 같은 기능들을 결정할 수 있다. CPUID opcode는 0FA2h이며 EAX 레지스터 값은 어떠한 정보를 반환할지를 결정한다.

CPUID 명령을 일반적으로 사용하기까지 프로그래머들은 프로세서 메이커와 모델을 결정하기 위하여 CPU 동작에 사소한 차이를 불러일으킬 수 있는 비밀스러운 [기계어](https://ko.wikipedia.org/wiki/기계어 "wikilink")를 기록하여야 했다.\[2\]\[3\]

## CPUID 호출

[어셈블리어](https://ko.wikipedia.org/wiki/어셈블리어 "wikilink")에서 CPUID 명령은 CPUID가 EAX 레지스터를 그대로 사용하므로 매개변수를 이용하지 않는다. EAX 레지스터는 어떠한 정보를 반환할지를 지정하는 값과 함께 로드되어야 한다. CPUID는 EAX = 0으로 먼저 호출되어야 하는데, 이는 CPU가 지원하는 가장 높은 호출 변수를 반환할 것이기에 그러한 것이다. 확장 정보를 가져오려면 CPUID는 비트 31의 EAX 집합을 사용하여 호출되어야 한다. 가장 높은 확장 명령 호출 변수를 결정하려면 EAX = 80000000h를 사용하여 CPUID를 호출하면 된다.

\=== EAX=0: 제조업체 ID 가져오기 === 이것은 CPU의 제조업체 ID 문자열을 반환한다. 이 문자열은 EBX, EDX, ECX 순으로 저장된 12자리 아스키 문자열이다. 가장 높은 기본 호출 변수는 EAX로 반환된다.

다음은 잘 알려진 제조업체 ID 문자열이다.

  - `"AMDisbetter!"` - [AMD K5](../Page/AMD_K5.md "wikilink") 프로세서 초기 샘플
  - `"AuthenticAMD"` - [AMD](https://ko.wikipedia.org/wiki/AMD "wikilink")
  - `"CentaurHauls"` - [Centaur](https://ko.wikipedia.org/wiki/Centaur "wikilink")
  - `"CyrixInstead"` - [사이릭스](../Page/사이릭스.md "wikilink")
  - `"GenuineIntel"` - [인텔](https://ko.wikipedia.org/wiki/인텔 "wikilink")
  - `"GenuineTMx86"`, `"TransmetaCPU"` - [Transmeta](https://ko.wikipedia.org/wiki/Transmeta "wikilink")
  - `"Geode by NSC"` - [내셔널 세미컨덕터](../Page/내셔널_세미컨덕터.md "wikilink")
  - `"NexGenDriven"` - [NexGen](https://ko.wikipedia.org/wiki/NexGen "wikilink")
  - `"RiseRiseRise"` - [Rise](https://ko.wikipedia.org/wiki/Rise "wikilink")
  - `"SiS SiS SiS "` - [SiS](../Page/SiS.md "wikilink")
  - `"UMC UMC UMC "` - [UMC](https://ko.wikipedia.org/wiki/UMC "wikilink")
  - `"VIA VIA VIA "` - [VIA](../Page/비아_테크놀로지스.md "wikilink")

이를테면 GenuineIntel 프로세서 값은 EBX로 0x756e6547를, EDX로 0x49656e69를 ECX로 0x6c65746e로 반환된다.

``` asm
.section .data
s0: .string "최대로 지원하는 표준 명령어 수: %i\n"
s1: .string "업체 ID: %s\n"
.text
 .global main

 .type main, @function
main:
 push rbp
 mov rbp, rsp

 sub rsp, 16
 xor eax, eax
 mov [rsp + 12], eax
 cpuid

 mov [rsp], ebx
 mov [rsp + 4], edx
 mov [rsp + 8], ecx
 mov edi, $s0
 mov esi, eax
 xor eax, eax
 call printf

 mov rdi, $s1
 mov rsi, rsp
 xor eax, eax
 call printf

 xor eax, eax
 mov rsp, rbp
 pop rbp
 ret
```

C언어

``` C
#include <stdio.h>
#include <Windows.h>

int main (int argc, char** argv)
{
    ULONG EAX_REG;
    ULONG EBX_REG;
    ULONG ECX_REG;
    ULONG EDX_REG;
    ULONG temp;

    __asm{
        pushad

        mov eax,0
        cpuid

        mov EAX_REG, eax
        mov EBX_REG, ebx
        mov EDX_REG, edx
        mov ECX_REG, ecx

        popad
    }

    printf("0x%08x 0x%08x 0x%08x 0x%08x \n",EAX_REG,EBX_REG,EDX_REG,ECX_REG);

    for(int i = 0; i < 4; i++)
    {
        temp = (EBX_REG & (0xFF << (8 * i)));
        temp >>= (8 * i);
        printf("%c",(char)temp);
    }
    for(int i = 0; i < 4; i++)
    {
        temp = (EDX_REG & (0xFF << (8 * i)));
        temp >>= (8 * i);
        printf("%c",(char)temp);
    }
    for(int i = 0; i < 4; i++)
    {
        temp = (ECX_REG & (0xFF << (8 * i)));
        temp >>= (8 * i);
        printf("%c",(char)temp);
    }

    printf("\n");
    return 0;
}
```

\=== EAX=1: 프로세서 정보 및 기능 비트 === CPU의 [스테핑](https://ko.wikipedia.org/wiki/스테핑 "wikilink"), 모델, 계열 정보를 EAX(CPU 서명이라고도 불림)로, 기능 플래그를 EDX와 ECX로, 부가 기능 정보를 EBX로 반환한다.

EAX로 반환되는 정보 형태는 다음과 같다:

  - 3:0 - 스테핑
  - 7:4 - 모델
  - 11:8 - 계열
  - 13:12 - 프로세서 유형
  - 19:16 - 확장 모델
  - 27:20 - 확장 계열

\=== EAX=2: 캐시 및 TLB 서술자 정보 ===  === EAX=3: 프로세서 일련 번호 ===  === EAX=80000000h: 가장 높은 확장 함수 가져오기 ===  === EAX=80000001h: 확장 프로세서 정보 및 기능 비트 ===  === EAX=80000002h,80000003h,80000004h: 프로세서 브랜드 문자열 === 프로세서 브랜드 문자열은 EAX, EBX, ECX, EDX로 반환된다.

``` asm
.section .data
s0: .string "프로세서 브랜드 문자열: %s\n"
.text
 .global main

 .type main, @function
main:
 pushq %rbp
 movq %rsp, %rbp

 subq $48, %rsp
 movl $0x80000002, %eax
 cpuid

 movl %eax, (%rsp)
 movl %ebx, 4(%rsp)
 movl %ecx, 8(%rsp)
 movl %edx, 12(%rsp)

 movl $0x80000003, %eax
 cpuid

 movl %eax, 16(%rsp)
 movl %ebx, 20(%rsp)
 movl %ecx, 24(%rsp)
 movl %edx, 28(%rsp)

 movl $0x80000004, %eax
 cpuid

 movl %eax, 32(%rsp)
 movl %ebx, 36(%rsp)
 movl %ecx, 40(%rsp)
 movl %edx, 44(%rsp)

 movl $s0, %edi
 movq %rsp, %rsi
 subl %eax, %eax
 call printf

 subl %eax, %eax
 movq %rbp, %rsp
 popq %rbp
 ret
```

\=== EAX=80000005h: 1차 캐시 및 TLB ID ===  === EAX=80000006h: 확장 2차 캐시 기능 === ECX의 2차 캐시의 자세한 내용을 반환한다. 캐시 크기와 코드를 표현하는 방법이 두 가지 있다.

``` asm
.section .data
s0: .string "2차 캐시: %iMB\n"
.text
 .global main

 .type main, @function
main:
 pushq %rbp
 movq %rsp, %rbp

 movl $0x80000006, %eax
 cpuid

 subl %edx, %edx
 movl %ecx, (%rsp)
 movl 2(%rsp), %eax
 movl $1024, %ecx
 divl %ecx

 movl $s0, %edi
 movl %eax, %esi
 subl %eax, %eax
 call printf

 subl %eax, %eax
 movq %rbp, %rsp
 popq %rbp
 ret
```

\=== EAX=80000007h: 고급 전원 관리 정보 ===  === EAX=80000008h: 가상 및 물리 주소 크기 ===

## 다른 언어로부터 ID 접근

이 정보는 다른 언어로부터 접근하기 쉽다. 이를테면 아래의 C++ (gcc) 코드는 cpuid가 반환하는 처음 다섯 개의 값을 인쇄한다.

``` cpp
#include <iostream>

int main(int argc, char **argv) {
  int b;
  for (int a = 0; a < 5; a++) {
    asm ( "mov %1, %%eax; " // a → eax
          "cpuid;"
          "mov %%eax, %0;" // eeax → b
          :"=r"(b) /* 출력 */
          :"r"(a) /* 입력 */
          :"%eax" /* 레지스터 표시 */
         );
    std::cout << "코드 " << a << "은(는) 다음을 제공한다: " << b << std::endl;
  }
  return 0;
}
```

마이크로소프트 비주얼 C 컴파일러는 함수 __cpuid()를 내장하고 있으므로 cpuid 명령은 인라인 어셈블리를 사용하지 않아도 추가할 수 있다. x64 버전의 MSVC가 인라인 어셈블리를 아예 허용하지 않으므로 다루기 쉽다. MSVC의 경우 다음과 같이 하면 된다:

``` cpp
#include <iostream>
#include <intrin.h>

int main(int argc, char **argv) {
  int b[4];
  for (int a = 0; a < 5; a++) {
    __cpuid(b,a);
    std::cout << "코드 " << a << "은(는) 다음을 제공한다: " << b[0] << std::endl;
  }
  return 0;
}
```

## 각주

<references />

## 같이 보기

  - [펜티엄 III](../Page/펜티엄_III.md "wikilink")
  - [CPU-Z](../Page/CPU-Z.md "wikilink")

## 외부 링크

  - [IA-32 구조 CPUID](https://web.archive.org/web/20110608084618/http://www.sandpile.org/ia32/cpuid.htm)

  - CPUID 안내:

      - [인텔](http://www.intel.com/Assets/PDF/appnote/241618.pdf) (PDF)

      - [AMD](http://support.amd.com/us/Embedded_TechDocs/25481.pdf) (PDF)

[분류:X86 아키텍처](https://ko.wikipedia.org/wiki/분류:X86_아키텍처 "wikilink") [분류:기계어](https://ko.wikipedia.org/wiki/분류:기계어 "wikilink")

1.  <http://www.intel.com/design/processor/manuals/253668.pdf>
2.  [Detecting Intel Processors - Knowing the generation of a system CPU](http://www.rcollins.org/ddj/Sep96/Sep96.html)
3.