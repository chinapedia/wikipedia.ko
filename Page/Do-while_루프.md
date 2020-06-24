> This article is converted from Wikipedia: [Do-while 루프](https://ko.wikipedia.org/wiki/Do-while_루프).


[섬네일](https://ko.wikipedia.org/wiki/파일:Do-while-loop-diagram.svg "wikilink") **do-while 루프**는 대부분의 [컴퓨터 프로그래밍](../Page/컴퓨터_프로그래밍.md "wikilink") 언어에서 주어진 [불린 자료형](https://ko.wikipedia.org/wiki/불린_자료형 "wikilink") 조건을 기반으로 코드가 한 번 실행할 수 있게 하는 [제어 흐름](../Page/제어_흐름.md "wikilink")[문이다](https://ko.wikipedia.org/wiki/문_\(프로그래밍\) "wikilink"). 대부분의 언어와 달리 [포트란](../Page/포트란.md "wikilink")의 do 루프는 실제로는 [for 루프와](https://ko.wikipedia.org/wiki/for_루프 "wikilink") 같다.

## 구조체

아래의 소스는

``` C
do {
   do_work();
} while (condition);
```

"[continue](https://ko.wikipedia.org/wiki/continue "wikilink")" 문이 사용되지 않는 한 다음과 같으며

``` C
do_work();
while (condition) {
   do_work();
}
```

기술적으로는 다음과 동등하다:

``` C
while (true) {
   do_work();
   if (!condition) break;
}
```

또는

``` C
LOOPSTART:
   do_work();
   if (condition) goto LOOPSTART;
```

## 예제

### C

``` C
int counter = 5;
int factorial = 1;
do {
  factorial *= counter--; /* Multiply, then decrement. */
} while (counter > 0);
printf("factorial of 5 is %d\n", factorial);
```

### C\#

``` CSharp
int counter = 5;
int factorial = 1;
do {
  factorial *= counter--; /* Multiply, then decrement. */
} while (counter > 0);
System.Console.WriteLine(factorial);
```

### 자바

``` Java
int counter = 5;
int factorial = 1;
do {
  factorial *= counter--; /* Multiply, then decrement. */
} while (counter > 0);
System.out.println(factorial);
```

### 자바스크립트

``` JavaScript
var counter = 5;
var factorial = 1;
do {
    factorial *= counter--;
} while (counter > 0);
console.log(factorial);
```

\[1\]

### 액션스크립트 3

``` ActionScript3
var counter:int = 5;
var factorial:int = 1;
do {
  factorial *= counter--; /* Multiply, then decrement. */
} while (counter > 0);
trace(factorial);
```

### 에이다

``` ADA
with Ada.Integer_Text_IO;

procedure Factorial is
  Counter   : Integer := 5;
  Factorial : Integer := 1;
begin
  loop
    Factorial := Factorial * Counter;
    Counter   := Counter - 1;
    exit when Counter = 0;
  end loop;

  Ada.Integer_Text_IO.Put (Factorial);
end Factorial;
```

### 포트란

``` Fortran
program FactorialProg
  integer :: counter = 5
  integer :: factorial = 1
  do
    factorial = factorial * counter
    counter = counter - 1
    if (counter == 0) exit
  end do
  print *, factorial
end program FactorialProg
```

포트란 90 이후 위의 iteration count가 없는 형태의 do 문과 아래의 do while 문이 추가되었다.

``` Fortran
program FactorialProg
  integer :: counter = 5
  integer :: factorial = 1
  factorial = factorial * counter
  counter = counter - 1
  do while (counter > 0)
    factorial = factorial * counter
    counter = counter - 1
  end do
  print *, factorial
end program FactorialProg
```

### 펄

``` Perl
$counter = 5;
$factorial = 1;
do {
     $factorial *= $counter--;
} while ($counter > 0);
print $factorial;
```

### PHP

``` PHP
<?php
$counter = 5;
$factorial = 1;
do {
     $factorial *= $counter--;
} while ($counter > 0);
echo $factorial;
?>
```

\[2\]

### PL/I

아래는 do until 문법만을 보여준다.

    declare counter   fixed initial(5);
    declare factorial fixed initial(1);
    do until(counter<=0);
      factorial = factorial * counter;
      counter = counter - 1;
      end;
    put(factorial);

### 래킷

``` scheme
#lang racket
(define counter 5)
(define factorial 1)
(let loop ()
  (set! factorial (* factorial counter))
  (set! counter (sub1 counter))
  (when (> counter 0) (loop)))
(displayln factorial)
```

### 루비

``` Ruby
counter = 5
factorial = 1
begin
  factorial *= counter
  counter -= 1
end while counter > 0
puts factorial
```

### 스몰토크

``` Smalltalk
| counter factorial |
counter := 5.
factorial := 1.
[counter > 0] whileTrue:
  [factorial := factorial * counter.
  counter := counter - 1].
Transcript show: factorial printString
```

### 비주얼 베이직 닷넷

``` VBNET
Dim counter As Integer = 5
Dim factorial As Integer = 1
Do
   factorial *= counter
   counter -= 1
Loop While counter > 0
Console.WriteLine(factorial)
```

## 같이 보기

  - [for 루프](https://ko.wikipedia.org/wiki/for_루프 "wikilink")
  - [foreach](https://ko.wikipedia.org/wiki/foreach "wikilink")
  - [while 루프](https://ko.wikipedia.org/wiki/while_루프 "wikilink")
  - [제어 흐름](../Page/제어_흐름.md "wikilink")

## 참조

<references />

[분류:제어 흐름](https://ko.wikipedia.org/wiki/분류:제어_흐름 "wikilink")

1.
2.