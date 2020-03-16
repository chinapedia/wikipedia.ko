> This article is converted from Wikipedia: [C  ](https://ko.wikipedia.org/wiki/C__).


C 프로그래밍 언어에서 **변수**는 숫자의 표현에 관련해서 정수형과 실수형이 있다. 이것의 처리는 [마이크로프로세서](../Page/마이크로프로세서.md "wikilink")의 [ALU](https://ko.wikipedia.org/wiki/ALU "wikilink")와 연관되어 처리 한다. 그리고 자료가 있는 위치값인 [메모리](https://ko.wikipedia.org/wiki/메모리 "wikilink") 주소값으로 처리하는 [포인터](https://ko.wikipedia.org/wiki/C_언어_포인터 "wikilink") 변수가 있다. 이것은 CPU의 메모리 체계와 관련되어 있어 CPU 의존적이다. 그리고 관련된 정보 끼리 묶어 처리하는 [struct](https://ko.wikipedia.org/wiki/struct "wikilink") 구조체 변수가 있다.

정수형의 표현은 [char](https://ko.wikipedia.org/wiki/char "wikilink"), [int로](https://ko.wikipedia.org/wiki/int_\(C_프로그래밍_언어\) "wikilink") 선언을 한다. char는 8비트로 규정되어 있어 변수의 범위가 결정되지만 int는 CPU와 [OS](https://ko.wikipedia.org/wiki/OS "wikilink")에 의존적이라 변수의 크기를 조정하는 [short](https://ko.wikipedia.org/wiki/short "wikilink")와 [long](https://ko.wikipedia.org/wiki/long "wikilink")을 사용한다. 그리고 음수와 양수를 규정하기 위해 [signed](https://ko.wikipedia.org/wiki/signed "wikilink")와 [unsigned](https://ko.wikipedia.org/wiki/unsigned "wikilink")가 있다. unsigned을 이용하여 양수 정수 만을 취급할 수 있다.

## 정수형 변수

### char

### int

## 실수형 변수

실수를 처리하기 위해 float와 double을 사용한다. 실수를 2진수를 표현할 때는 [부동소수점](../Page/부동소수점.md "wikilink")(Float-Point) 방식을 사용한다. 이것은 국제표준 [IEEE 754](../Page/IEEE_754.md "wikilink") 규격에 따른다.

## struct

## 포인터

포인터 변수 모두는 메모리의 주소를 지정하는 값을 가지고 있으면 값을 변화시킬 수 있기 때문에 CPU을 설계한 설계 기준에 따라 주소값의 길이와 방식이 결정된다. 일반적인 용도의 대부분의 CPU는 메모리를 지정하는 길이(비트수)는 동일하다. RAM이든 ROM/FLASH 이든 모든 주소는 같다. MCU(8051,...)은 오히려 많은 경우 메모리 영역을 나누어 다른 주소체계를 사용한다. 8051은 내부의 256바이트 내에 변수를 할당 한다. 256바이트는 매우 적기 때문에 많은 데이터 저장용으로 16비트의 저장 공간을 갖는 주소체계를 사용하고 기계어 코드를 분리 했다. 이럴 경우는 주소값이 8비트 또는 16비트가 필요하다.

C언어가 UNIX 계열의 [OS](https://ko.wikipedia.org/wiki/OS "wikilink") 작성 할 때 사용하였으므로 커널의 프로그램 소스를 보면 상당히 많은 부분 포인터 변수를 볼 수 있다.

### 포인터 변수의 선언

포인터 변수는 \*을 이용하여 선언 한다. 포인터는 메모리의 주소값을 가지고 데이터의 위치를 지정하기 때문에 다른 변수의 저장 공간의 주소를 알아야 한다. 따라서 정적 변수의 주소는 & 연산자를 사용한다.

``` cpp
  int ival;
  int *pval;

  // ...

  pval = &ival; // ival의 &연산자는 ival가 존재하는 위치 주소값이다.
  *pval = 30;   // pval가 ival의 주소값을 가지고 있으므로,
                // 이 주소값을 먼저 읽어 30을 쓸 위치를 결정하고
                // 그 위치에 정수 값을 쓴다.
  printf("변수 pval가 존재하는 위치 주소값은 0x%08X, 정수형 데이터 저장공간 지정은 0x%08X\n", &pval, pval );
```

ival는 정수형 데이터가 들어가는 변수이다. 즉, 정수 숫자를 저장 한다. 그러나 변수 pval은 데이터 공간의 위치를 지정하는 것이지 정수형 데이터를 저장하는 것은 아니다. CPU의 주소체계에서 메모리의 주소값을 저장 함으로써 데이터가 저장 될 주소값을 가지고 액세스 하는 것이다. 그러나 메모리 주소값도 하나의 이진수의 정수형의 일종이라고 생각 할 수 있다.

#### NULL 사용

포인터 변수는 다른 정적 변수나 동적함수(malloc(), new)에 의해 생성된 저장 공간을 지정하는 변수이다. 그러나 경우에 따라 데이터 저장공간을 지정하지 못한 상태에서 액세스 할 수 있다. 보통 저장공간 지정에 성공했는지를 판단하는 방법으로 NULL을 이용할 수 있다.

NULL 사용 예:

``` cpp
  char data8;
  char *pval = NULL;  // 포인터가 데이터 저장공간을 지정하지 않았다.

   if (pval == NULL)
       pval = data8; // 변수 pval가 데이터 저장 공간을 변수 data8로 지정 한다.
   *pval = 10; // 위에서 지정한 data8에 10을 쓴다.
```

C/C++에서 NULL은 숫자 0으로 정의 되어 있다. 자료구조 등에서도 '없다'는 의미로 null을 사용하는데, 경우에 따라 정해진 비트수 만큼 이진수로 모두 1인 경우가 있다. 그러나 C/C++에서는 0으로 정의 되어 있으므로 메모리의 0번지에는 특수하게 사용하지 않는다.

만약 포인터 변수가 데이터 저장공간을 지정하지 않았다면 NULL을 사용하여 초기화 시키는 방식이 일반적이다.

### 포인터 변수형과 액세스

포인터 변수의 길이(변수의 비트수)는 [마이크로프로세서](../Page/마이크로프로세서.md "wikilink")에 의존 한다. 즉, 마이크로프로세서가 주소 공간과 액세스 체계를 이미 가지고 있기 때문에 C/C++언어의 컴파일러는 이를 따를 뿐이다. 즉, 포인터 변수의 길이는 CPU 의존적으로 결정 되어 있으므로 모든 포인터의 길이는 같다. 그렇다면 왜 포인터 변수 선언 시, 앞에 변수형이 필요한가는 액세스 할 때 데이터 액세스 길이(비트수)를 결정하기 위해서 이다.

32비트 CPU의 대부분은 32비트 주소공간과 32비트 데이터 액세스 단위를 가지므로 다음 예는 32비트라고 가정 하면:

``` cpp
  // 다음 설명에서 나오는 비트 단위는 32비트 CPU의 경우

  char buff[1024];

  int *pdata = (int*) buff; // 형이 다르나 값을 액세스 할 때, 32비트 정수형으로 액세스 하기 위해 지정
  *pdata = 23;          // 32비트 정수형 쓰기, 따라서 23은 32비트 정수형 이다.
  *((char*)pdata) = -1; // 그러나 char 8비트 정수형으로 변환 하였으므로 -1은 8비트 정수형이다.
                        // 8비트 정수 -1 : 11111111b
  void *pval;      // 데이터 액세스 타입(액세스 비트 단위)가 없는 변수가능 하다.
                   // 모든 주소값은 32비트 이기 때문이다.
  pval= (void *) buff;  // 형이 맞지 않으므로 형 변경
  *pval = 10;       // '''error : 액세스 단위를 결정할 수 없다. 따라서 기계어 코드를 확정할 수 없다.
  *(char*)pval = 10; // 액세스 단위가 8비트 이므로, 10은 8비트 정수형이며 이 값이 써진다.
```

코드 중 **\*pval = 10;**은 pval가 void형이므로 액세스 시, 10을 어떻게 규정할지 결정할 수가 없다. 보통 10은 정수형으로 취급 되지만 같은 정수형도 8,16,32비트로 다르다. 따라서 pval의 변수형에 따라서 비트수가 결정되는데 여기서는 void이므로 결정 불가능 하다.

### 예

``` cpp
#include <stdio.h>
#include <string.h>

/// Global Variables

char name[124];
char tel[] = "010-2345-6789";

// func.
char *read_name(char *pstr, int szmax);

int main(int argc, char**argv)
{
   char *pstr;

    pstr = read_name(name, 120);
    printf("이 름 = %s\n", pstr );
    printf("전화 번호 = %s\n", tel);

    return 0;
}

char *read_name(char *pstr, int szmax)
{
   size_t leng;
   static char bstr[256];

    gets(bstr);
    leng = strlen(bstr);
    if (leng >= (size_t)szmax)
        leng = szmax -1;
    strncpy (pstr,bstr,leng);
    *(pstr+leng) = 0;

    return pstr;
}
```

이 프로그램 예에서 실제 [스트링](https://ko.wikipedia.org/wiki/스트링 "wikilink") 메모리 공간을 갖는 것은 name, tel, bstr 변수 들이다. 그러나 pstr변수는 스트링 데이터가 들어갈 변수가 아니고 데이터가 들어가야할 위치를 지정하는 변수이다. CPU의 주소체계에 의한 주소값으로 데이터의 위치를 지정하는 것이다. 이 포인터 변수는 메모리 주소값만 가지면 되므로 정해진 길이의 비트수를 가지고 동작 한다.

### 포인터 변수 자료형

포인터 변수는 데이터 저장 위치 주소값을 사용하는 변수이다. 보통 정적 변수의 경우 직접 [액세스 모드](https://ko.wikipedia.org/wiki/액세스_모드 "wikilink")(direct access mode)의 기계어 코드로 컴파일 된다.

포인터 변수의 예 :

``` cpp
  char   *p8bitvar;       // 8비트 액세스
  short int  *p16bitvar;  // 16비트 액세스
  int    *pintvar;  // int형 액세스
  float  *pfvar;    // 32비트 [[부동소수점|부동소수점]] 데이터 액세스
  double *pdvar;    // 64비트 부동소수점 데이터 액세스
  void   *pvdata;   // 몇 비트 액세스 인지 규정 할 수 없다.

  struct SObject {
    int data;
    struct SObject *link;
  } *pstdata;         // 구조체의 위치를 지정 한다.
```

변수 자체의 길이는 CPU의 메모리 체계에 의해 결정된다. 32비트 CPU는 거의 다 32비트의 메모리 주소값을 갖는다. 따라서 위의 모든 변수의 크기는 4바이트이다.

앞에 변수형이 필요한 이유는 액세스 할 때, 몇 비트의 단위로 액세스 하는냐를 결정한다. void의 경우는 데이터가 몇 비트인지 결정할 수 없으므로 결국 액세스형 변환을 통해 몇비트 액세스 인지 결정 해야한다.

void 포인터 변수의 예 :

``` cpp
 char num;
 void *pvdata = (void *) &num;
 *(char*) pvdata = 10;
 int ival;
 pvdata = (int *) &ival;
 *(int*) pvdata = 10;

 *pvdata = 10; // 오류 : 액세스 단위가 정의 되지 않음.
   //error C2100: illegal indirection
   //error C2440: '=' : cannot convert from 'int' to 'void *'
```

위 **\*pvdata = 10;**에서 10이라는 숫자는 기본적으로 정수형인데, pvdata의 액세스 단위가 결정되지 않았다. 즉, 이런경우 액세스 단위는 변수가 결정 한다. 따라서 이런 경우는 오류로 나타난다.

### 포인터 변수에서 주소값의 연산

포인터 변수가 갖는 메모리의 주소값은 결국 정수형의 2진수 숫자 일 뿐이다. 따라서 CPU내의 ALU을 통해 연산 된다.

일반적인 32비트 CPU의 주소체계는 주로 32비트 메모리 주소값을 사용한다. 따라서 CPU의 주소값을 정수형으로 보고 값의 치환, 비교, 연산 등이 가능하다.

``` cpp
#define SZ_DATA 100

int main()
{
  int ival[SZ_DATA];
  int *pval = NULL;

  pval = &ival; // ival의 &연산자는 ival가 존재하는 위치 주소값이다.
  for (int cnt = 0;cnt <  SZ_DATA;cnt++) {
      *pval = 0;
      pval++;
  }
  // ...
}
```

pval++에서 연산자 ++는 포인터의 주소값을 다음 위치로 하나 더 옮기라는 뜻이다. 보통의 정수형 변수라면 1을 더하는 것이겠지만 이런경우 주소값을 한 칸 더 옮기는 경우이다. 따라서 단순히 1을 더하는 것이 아니고 포인터 변수가 갖는 int형의 크기만큼 더해진다.

pval++에서 ++ 연산자 :

  - \++ : 현재의 주소값 + sizeof(int) =\> 주소값 변경

예를 들어 현재 \&ival\[0\] == pval == 0x00301200 이라면 :

`  0x00301200 + sizeof(int) :  0x00301200 + 4 => 0x00301204 ==> pval == &ival[1]`

즉, ival의 인덱스가 0에서 1로 옮겨 간다.

``` cpp
#include <stdio.h>

#define SZ_DATA 100

char gname[SZ_DATA];
char gbuff[SZ_DATA];

int main()
{
  char *psstr = gname;
  char *pdstr = gbuff;
  gets(gname);
  while (*psstr && *psstr != ' ')
      *pdstr++ = *psstr++;
  *pdstr = 0;
  printf("%s\n", gbuff);
  return 0;
}
```

psstr++ 경우, 예를 들어 현재 psstr == 0x00301200 이라면 :

`  0x00301200 + sizeof(char) :  0x00301200 + 1 => 0x00301201 ==> psstr`

이 때는 char 변수가 한 바이트 단위로 배열 되기 때문에 주소값이 1씩 ALU에 의해 더해 진다.

``` cpp
typedef struct {
   char *name;
   int  age;
} Man, *PMan;

Man man[] = {
  { "홍길동", 23 },
  { "Kim",    20 },
  { "Song",   19 },
};

#define SZ_MAN sizeof(man)/sizeof(man[0])

int main()
{
   PMan pman = man;
   printf("sizeof(Man) = %d, man=0x%08X\n", sizeof(Man), man );
   for (int cnt = 0;cnt < SZ_MAN;cnt++) {
      printf("0x%08X : %s, %d\n", pman+cnt, (pman+cnt)->name, (pman+cnt)->age);
   }
   return 0;
}
```

실행결과 :

`sizeof(Man) = 8, man=0x00E070A8`
`0x00E070A8 : 홍길동, 23`
`0x00E070B0 : Kim, 20`
`0x00E070B8 : Song, 19`

이 경우의 pman+cnt에서

cnt = 1일 때, 포인터의 값을 다음과 같이 계산할 수 있다:

`   0x00E070A8 + `**`sizeof(Man)`**`*cnt :  0x00E070A8 + 8*1 => `**`0x00E070B0`**` ==> &man[1]`

### 포인터 변수의 길이

포인터 변수는 결국 메모리의 변수 위치의 주소값을 다루는 변수이다.따라서 CPU에 따라 길이가 결정된다. CPU에 메모리 주소체계가 컴파일러 보다 우선 설계되기 때문에 해당 CPU에 맞추어 포인터 컴파일러 설계를 한다. 주로 8비트 CPU의 16비트의 주소값을 갖는다. 그러나 8비트 중에 [MCU](https://ko.wikipedia.org/wiki/MCU "wikilink") 계열은 주소를 지정하기 위한 비트가 다양하다. 8비트와 16비트가 혼재하기도 한다. 같은 CPU라도 8비트와 16비트를 같이 사용한다는 이야기 이다.

|                                                       |              |
| ----------------------------------------------------- | ------------ |
| [Z-80](https://ko.wikipedia.org/wiki/Z-80 "wikilink") | 16비트 주소체계    |
| [8051](https://ko.wikipedia.org/wiki/8051 "wikilink") | 8비트와 16비트 혼용 |

  - 8051의 Keil Complier 예\[1\]

<!-- end list -->

``` c

#define LEDPORT0  *(unsigned char xdata*) 0xc000  // 외부 메모리 주소 0xc000번지

xdata char gGrapLedData[1024]; // 외부 메모리 설정 - 16비트 주소 공간,
                               // 8051의 내부 RAM이 256바이트 이므로 큰 데이터 처리 불가
xdata char *pxled;   // sizeof(pxled) = 2 : 외부 메모리 설정 - 16비트 주소 공간

char g_ledData[4];   // 내부 메모리 설정 - 8비트 주소 공간
char *pledfont;      // sizeof(pledfont)=1 : 내부 메모리 사용 - 8비트 주소 공간

void main()
{
    // CPU 초기화

    while (1) {
       // ...
       LEDPORT0 = *pledfont++;
    }
}
```

CPU의 프로그램에서 CPU의 메모리 체계를 이해해야만 포인터 변수의 길이를 알 수 있다.

이에 비해 32비트는 주로 32비트의 주소 비트 수를 갖는다. 거의 모든 CPU가 32비트이므로 오히려 8비트 CPU 보다 길이가 통일되어 있다. 64비트로 가면 또 다른 비트 수를 가질 것이다.

|                                                                                           |           |
| ----------------------------------------------------------------------------------------- | --------- |
| [x86](https://ko.wikipedia.org/wiki/x86 "wikilink")([IA-32](../Page/IA-32.md "wikilink")) | 32비트 주소체계 |
| [68000](https://ko.wikipedia.org/wiki/68000 "wikilink")계열                                 | 32비트 주소체계 |
| [ARM](https://ko.wikipedia.org/wiki/ARM "wikilink")                                       | 32비트 주소체계 |

각각의 변수가 들어갈 메모리의 위치와 성격에 따라 메모리를 지정하는 주소값의 비트수는 CPU에 의해 결정 되어 있으므로 어떤 컴파일이든 정해져 있다.

변수의 길이를 알아보는 방법의 예 :

``` c
#include <stdio.h>

 struct Man {
    char name[40];
    int age;
 } ;

 struct Man man;

int main(int argc, char**argv)
{
     int leng;

     printf("sizeof(int)=%d\n", sizeof(int) );
     printf("sizeof(int*)=%d\n", sizeof(int*) );
     printf("sizeof(struct Man)=%d\n", sizeof(struct Man) );
     printf("sizeof(struct Man *)=%d\n", sizeof(struct Man *) );

     // ...
     return 0;
}
```

일반적인 포인터 변수의 길이는

| CPU      | 예                                                                                                                                                                                                       | 주소체계      | 포인트 | 포인터 길이                                                 |
| -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- | --- | ------------------------------------------------------ |
| 8비트 CPU  | [8080](https://ko.wikipedia.org/wiki/8080 "wikilink"), [Z-80](https://ko.wikipedia.org/wiki/Z-80 "wikilink")                                                                                            | 16비트      | 2   | sizeof(int\*) = sizeof(char\*) = sizeof(void\*)=...= 2 |
| 8비트 MCU  | [8051](https://ko.wikipedia.org/wiki/8051 "wikilink"), SAM8                                                                                                                                             | 8/16비트 혼용 | 혼용  | 메모리 공간에 따라 1 또는 2바이트 - 컴파일러에 공간 할당 옵션 검토.              |
| 32비트 CPU | [x86](https://ko.wikipedia.org/wiki/x86 "wikilink")([IA-32](../Page/IA-32.md "wikilink")), [68000](https://ko.wikipedia.org/wiki/68000 "wikilink"), [ARM](https://ko.wikipedia.org/wiki/ARM "wikilink") | 32비트      | 4   | sizeof(int\*) = sizeof(char\*) = sizeof(void\*)=...= 4 |

  - 32비트이 CPU에서 배열의 포인트를 예\[2\]

[섬네일](https://ko.wikipedia.org/wiki/파일:Exam_int_point.png "wikilink")

``` cpp
#include <stdlib.h>
#include <stdio.h>
#include <time.h>

int a[10];
#define SZ_DATA  sizeof(a)/sizeof(a[0])
int *pa;

void fun(int *pa, int cnt);

void printvar(int length)
{
   int cnt;

   pa = a;
   printf("&a[0] = 0x%08X\n", &a[0]);
   printf("&pa = 0x%08X\n", &pa);
   printf("pa = 0x%08X\n", pa);
   printf("fun = 0x%08X\n", (int) fun);
   printf("Random Data\n");
   for(cnt = 0;cnt < length;cnt++)
       printf("%d ", a[cnt]);
   printf("\n");
}

void fun(int *pa, int cnt)
{
   while (cnt) {
      *pa = rand() % 1000 + 1;
       pa++;
       cnt--;
   }
}

int main(int argc, char *argv[], char**env)
{
   srand( (unsigned int) time(NULL));
   fun(a, SZ_DATA);
   printvar(SZ_DATA);
   return 0;
}
```

x86의 실행결과 값 예 :

`&a[0] = 0x0040DF04`
`&pa = 0x0040DF00`
`pa = 0x0040DF04`
`fun= 0x00401060`
`Random Data`
`493 539 45 17 247 113 68 941 857 744`

### 함수 포인터

함수 역시 기계어 코드가 특정 메모리를 점유하고 이것을 읽어 실행 하는 것이다. 따라서 코드의 위치를 주소값으로 표현할 수 있다.

함수의 위치 정보를 가지고 호출하는 방식으로 실행 시킬 수 있다. 이 변수의 선언은 괄호를 이용한다.

함수의 예 :

``` cpp
  int add(int a, int b) { return a +b; }

  int main()
  {
    int (*fun)(int, int);  // 함수 포인터 변수를 선언 한다.
    fun = add;    // fun의 모양이 맞는 함수의 위치 값을 넣을 수 있다.
    printf("0x%08X : %d\n", (int) fun,  fun(10,20) );

    return 0;
  }
```

[함수 포인터를](../Page/함수_포인터.md "wikilink") 사용할 때는 위와 같이 인수까지 정의를 해야 한다. 초기와는 달리 현재의 표준화 된 C/C++언어에서는 인수가 달라지면 다른 함수가 되기 때문이다.

그러나 다음과 같이 함수 포인터 변수와 인수가 맞지 않으면 문제가 발생 한다. fun과 cadd함수는 인수가 다르다. 컴파일 오류가 발생 한다.

인수가 달라서 오류가 발생하는 예 :

``` cpp
  int cadd(int a) { return a+10; }

    int (*fun)(int, int);
    fun = cadd; // error C2198: 'int (__cdecl *)(int,int)' : too few arguments for call
```

결국 함수 포인터 변수는 인수까지 정의가 되어야 한다.

배열 역시 가능하다.

배열 함수 포인터 사용 예:

``` cpp
#include <math.h>
#include <stdio.h>

#define PI 3.141592653589793

double mySin(double r);

double (*pMath[])(double) = {
    sin, cos, tan,
    mySin,
    NULL
};

double mySin(double r)
{
    double rad = r * PI / 180.;

    return sin(rad);
}

int main(int argc, char* argv[], char**env)
{
    int cnt;
    double r;

    printf("각도 입력 : "); scanf("%lf", &r);
    for (cnt = 0;pMath[cnt];cnt++)
        printf("0x%08X : %lf\n", pMath[cnt], pMath[cnt](r) );

    return 0;
}
```

실행결과 값 예 :

`각도 입력 : 45`
`0x00D510E6 : 0.850904`
`0x00D51118 : 0.525322`
`0x00D510E1 : 1.619775`
`0x00D51159 : 0.707107`

## 각주

[분류:C 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:C_프로그래밍_언어 "wikilink")

1.  [C언어 포인터 개념 I - 포인터 이해, 포인터 기초 & CPU 구조](http://blog.naver.com/dolicom/7866212)
2.