> This article is converted from Wikipedia: [Struct](https://ko.wikipedia.org/wiki/Struct).


C/C++ 프로그래밍 언어에서 구조화 된 데이터를 처리할 때 **struct**를 사용하는데 이를 **구조체**라고 한다. 구조화되었다는 말은 의미가 연결되어 한 덩어리로 처리하는 방식을 말한다. 관련된 컴퓨터 용어로 보면 [record](https://ko.wikipedia.org/wiki/record "wikilink") 그리고 [Object](https://ko.wikipedia.org/wiki/Object "wikilink")와 비슷한 개념이다. 그리고 자료처리와 연관하여 데이터 구조와 연관이 되어 있다.

## 구조화 필요

예를 들어 인간의 정보 처리를 한다면, 사람들의 공통된 정보를 추출한 다음 이것들을 묶어 처리한다.

``` c
struct Man {
  char name[50];
  int  age;
  char gender;
  char tel[50];
};
```

만약 정보 처리 시, 변수 들이 다음과 같이 분리되어 있다면

``` c
// file : mInfo.c

char name[100][50];
int countuse;
int age[100];
char gender[100];

int getUseCount()
{
   return countuse;
}
```

``` c
// file : mngTel.c

char tel[200][50];

char *getUseCount(int nId)
{
   return tel[nId];
}
```

``` c
// file : main.c
#include <stdio.h>

extern int countuse;

int main(int argc, char**argv)
{
   countuse = 10;
   // ...
   int num = getUseCount();
   printf("NO Member+%d\n", num);

   // ...
   return 0;
}
```

3개의 프로그램 코딩 파일을 하나의 프로젝트로 묶어 개발할 때 사람의 정보를 처리하는 경우 변수들이 상당히 복잡하게 나뉘고 관리된다. 연관된 사람이라는 정보가 나뉘어 있어 동시에 여러가지 파일을 검토하고 나누어 프로그램해야 한다. 이렇게 되면 복잡한 시스템에서 오류가 증가되고 유연성이 떨어진다.

변수 선언 시, 의미적으로 연결된 변수끼리 묶어서 선언한다.

``` c
struct Man {
  char name[50];
  int  age;
  char gender;
  char tel[50];
};

struct Man man;
```

예에서 인간의 정보 처리 시, 한 사람의 정보를 구조체로 묶어 정보 처리한다. 각각의 변수가 나뉘면 서로 연관관계의 일관성 유지에 불리하다.

## struct 초기화

``` c

/* Define a type point to be a struct with integer members x, y */
typedef struct {
   int    x;
   int    y;
} point;

/* Define a variable p of type point, and initialize all its members inline! */
point p = {1,2};
```

## struct 선언 및 변수

struct는 선언부와 변수부로 나누어 선언할 수 있다. 선언부는 컴파일러에게 구조체의 구조를 알려주는 기능을 한다. 따라서 \#include 시 중복 선언이 가능하다. 선언부 만으로는 변수의 저장공간을 확보하지 않기 때문이다.

  - 선언부 예

<!-- end list -->

``` c
// 코드 파일 명 : man.h
#ifndef _MAN_H
#define _MAN_H

struct Man {
  char name[50];
  int  age;
  char gender;
  char tel[50];
};

struct Man *getMan();
#endif
```

  - 구조체 변수부 예

<!-- end list -->

``` c
// 코드 파일 명 : man.c

#include "man.h"

struct Man man;

struct Man *getMan() { return &man; }

char *getName() { return man.Name; }

int getAge() { return man.age; }

char getGender() { return man.sex; }

char *getTel() { return man.tel; }
```

``` c
// 코드 파일 명 : main.c

#include <stdio.h>

#include "man.h"

int main(int argc, char**argv)
{
   struct Man *pman;

   pman = getMan();
   printf("Name=%s\n", pman->name);

   return 0;
}
```

  - 선언부와 변수부가 결합된 예

<!-- end list -->

``` c
struct Man {
  char name[50];
  int  age;
  char gender;
  char tel[50];
} man;
```

이렇게 프로그램 구성을 하면 man이라는 변수의 메모리 공간이 만들어진다. 그러나 문제는 Man의 구조체가 여러 파일에서 사용한다면 구조체의 구조부를 include 하여야 하는데 그렇게 되면 man 변수가 중복된다. 따라서 include을 한번 밖에는 할 수가 없다. 보통 습관적으로 선언부만 분리해서 코드하는 습관이 좋다.

##### typedef과 연결

위의 예 처럼 코드를 작성할 때, 매번 struct라는 키워드를 쓰는 것은 불편할 때가 있다. 따라서 struct을 사용하지 않도록 선언할 수 있다.

``` c
// 코드 파일 명 : man.h

#ifndef _MAN_H
#define _MAN_H

typedef struct Man {
  char name[50];
  int  age;
  char gender;
  char tel[50];
} Man;

Man *getMan();
#endif
```

처럼 변경할 수가 있다. struct만을 사용한 경우와 다른 것은 선언부만을 사용한다는 것이다.

``` c
typedef struct Man {
  char name[50];
  int  age;
  char gender;
  char tel[50];
} Man, *PMan;
```

이렇게 다중 변수 구조체 타입을 선언할 수가 있다. 이것은 실제로 변수가 메모리에 확보되지 않는 것으로 단지 구조만을 지정하는 것이다. 따라서 다중 include가 가능 하다.

여기서 Man이라는 구조체 명은 다를 수도 있고 같을 수도 있다.

  - 구조체 명이 다른 경우

<!-- end list -->

``` c
typedef struct _Man {
  struct _Man *next;
  struct _Man *prev;

  char name[50];
  int  age;
  char gender;
  char tel[50];
} Man, *PMan;
```

  - 구조체 명이 같은 경우

<!-- end list -->

``` c
typedef struct Man {
  struct Man *next;
  struct Man *prev;

  char name[50];
  int  age;
  char gender;
  char tel[50];
} Man;
```

  - 구조체 명이 앞에 없는 경우

<!-- end list -->

``` c
typedef struct {

  char name[50];
  int  age;
  char gender;
  char tel[50];

} Man;
```

구조체명이 앞에 없으면 자기 자신의 포인터를 선언할 수 없는 문제가 있다. 따라서 자기 자신의 포인터를 선언할 경우는 구조체명을 앞에 넣어야 한다.

## struct의 포인터

``` c
struct point {
   int x;
   int y;
} my_point;

struct point *p = &my_point; /* To declare p as a pointer of type struct point */

my_point.y = 3; /* struct의 두 번째 변수의 값 변경 */
(*p).x = 8; /* To access the first member of the struct */
p->x = 8; /* Another way to access the first member of the struct */
```

포인터의 표현 방법은 -\>와 .이 있다.

  - \-\> : 화살표 앞의 변수가 포인터 변수이면 화살표를 사용한다. 위의 예에서 처럼 ()을 사용하면 .을 사용한다.
  - . : 점 앞의 변수가 포인터가 아닌 저장하려는 데이터가 존재할 때 사용한다.

### struct의 내부 변수 주소값 지정

포인터 변수를 사용하여 엑세스 한다면, 내부의 변수의 위치를 알 필요가 있다.

위의 예에서 변수 x와 y의 변수의 메모리 위치값은 다음과 같이 표현 한다.

``` c
   struct point *ppoint = &my_point;  // 변수 my_point의 시작 주소이다.
   int *px = &my_point.x;   // 내부 변수 x의 메모리 주소값을 px에 치환 한다. &my_point == &my_point.x
   int *py = &ppoint->y;    // ppoint 변수를 사용하여 y의 위치값을 얻는다.
   *px = 10; *py = 20;

   ppoint = (struct point *) malloc( sizeof(struct point) );  // 동적 할당에 의해 포인터 치환
   px = &ppoint->x; *px = 20;
```

함수 malloc()는 리턴값이 변수의 위치를 지정하는 메모리 주소값으로 void\*이다. 따라서 이것을 정적 형변환을 하면 된다.

## struct 내부 변수의 메모리 배치

struct의 내부 변수 배치는 선언 된 순서대로 앞에서 부터 차례로 배치 된다. 8비트 CPU의 경우 기본적인 액세스가 8비트 이므로 어떤 변수 든 한 바이트 단위로 액세스 된다. 그러나 보통의 32비트 CPU는 액세스 단위가 기계어에 따라 8,16,32비트 액세스 된다. 8비트 CPU라면 모든 변수 처리 시 8비트 단위로 액세스 하므로 빈공간 없이 변수들을 배치하면 된다. 그러나 32비트 CPU에서는 다른 문제가 있다.

예를 들어 정수형 변수 int을 선언하면 CPU는 한번에 액세스 되도록 기계어로 컴파일 한다. 따라서 32비트 변수의 경우 메모리 배치에서 주소값이 4의 배수로 할당 되어야 32비트 변수의 액세스를 한번에 할 수 있다. 즉, 주소값이 4로 나누면 나머지가 0이 되도록 배치 한다. 이것은 CPU의 주소버스의 A1:A0=00b이라는 의미를 갖는다.

### 일반적인 32비트 CPU에서의 struct 메모리 배치 예

[섬네일](https://ko.wikipedia.org/wiki/파일:Struct_map_exam1.png "wikilink")

다음과 같은 예의 경우, 컴파일러는 모든 struct의 시작 주소를 4의 배수가 되도록 메모리의 위치를 잡는다.

``` c
struct Man {
   int  age;
   char gender;
   int  id;
   char name[11];
   short int score;
};

struct Man man = { 19, 'M', 0x12345678, "Hong길동" , 100};
```

일반적으로 32비트의 little-endian CPU로 컴파일 하면, struct의 멤버의 메모리 배치는 그림과 같이 배치 된다. 정수형 int 사이에 char 변수는 4바이트 중에 한 바이트만을 사용하고 나머지 3바이트를 사용하지 않는다. 이것은 변수 id가 32비트 단위로 액세스 되어야 하므로 어쩔 수 없이 빈 공간을 넣는 방법으로 배치한 것이다. 이 struct의 크기는 빈공간(padding bit) 까지를 포함한 크기로 취급한다. `sizeof(struct Man) == 28`바이트가 된다.

## 같이 읽기

  - [C++](https://ko.wikipedia.org/wiki/C++ "wikilink")
  - [object](https://ko.wikipedia.org/wiki/object "wikilink")

[분류:C 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:C_프로그래밍_언어 "wikilink") [분류:자료형](https://ko.wikipedia.org/wiki/분류:자료형 "wikilink")