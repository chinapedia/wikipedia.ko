> This article is converted from Wikipedia: [OpenMP](https://ko.wikipedia.org/wiki/OpenMP).


**OpenMP**(Open Multi-Processing, 오픈MP)는 [공유 메모리](https://ko.wikipedia.org/wiki/공유_메모리 "wikilink") [다중 처리](https://ko.wikipedia.org/wiki/멀티프로세서 "wikilink") 프로그래밍 [API](../Page/API.md "wikilink")로, [C](https://ko.wikipedia.org/wiki/C_\(프로그래밍_언어\) "wikilink"), [C++](https://ko.wikipedia.org/wiki/C++ "wikilink"), [포트란](https://ko.wikipedia.org/wiki/포트란 "wikilink") 언어와, [유닉스](../Page/유닉스_계열.md "wikilink") 및 [마이크로소프트 윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink") 플랫폼을 비롯한 여러 플랫폼을 지원한다.

[병렬 프로그래밍의](https://ko.wikipedia.org/wiki/병렬_프로그래밍 "wikilink") 하이브리드 모델로 작성된 응용 프로그램은 OpenMP와 [메시지 전달 인터페이스](https://ko.wikipedia.org/wiki/메시지_전달_인터페이스 "wikilink") (MPI)를 둘 다 사용하거나, 더 투명성 있는 방식으로 비공유 메모리 시스템을 위한 OpenMP 확장을 사용하여 [컴퓨터 클러스터](https://ko.wikipedia.org/wiki/컴퓨터_클러스터 "wikilink") 상에서 구동할 수 있다.

## 역사

OpenMP 아키텍처 리뷰 보드(ARB)는 최초의 API 규격인 포트란 1.0용 OpenMP를 1997년 10월에 출판하였다. C/C++용 OpenMP는 1998년 10월에 공개하였는데, 2000년 11월에 포트란 버전으로 2.0이 나온 다음 2002년 3월에 C/C++ 규격으로 2.0 버전이 출시되었다. 2005년 5월에 발표된 버전 2.5부터는 C/C++/포트란 규격이 통합되었다. 2008년 5월에 버전 3.0, 2013년 7월에 버전 4.0, 2015년 11월에 버전 4.5, 2018년 11월에 버전 5.0이 발표되었다.\[1\]

2019년 현재, 버전 2.5 이하를 레거시 사양으로 취급하고 있다.

## 주요 요소

[가운데](https://ko.wikipedia.org/wiki/파일:OpenMP_language_extensions.svg "wikilink")

## 예제 프로그램

### [Hello World](https://ko.wikipedia.org/wiki/Hello_World "wikilink")

#### [C](https://ko.wikipedia.org/wiki/C_\(프로그래밍_언어\) "wikilink")

``` c
 #include <omp.h>
 #include <stdio.h>
 #include <stdlib.h>

 int main (int argc, char *argv[]) {
   int th_id, nthreads;
   #pragma omp parallel private(th_id)
   {
     th_id = omp_get_thread_num();
     printf("Hello World : 스레드 %d\n", th_id);
     #pragma omp barrier
     if ( th_id == 0 ) {
       nthreads = omp_get_num_threads();
       printf("모두 %d 개의 스레드가 있습니다\n",nthreads);
     }
   }
   return EXIT_SUCCESS;
 }
```

#### [C++](https://ko.wikipedia.org/wiki/C++ "wikilink")

``` c
#include <omp.h>
#include <iostream>
#include <sstream>
int main (int argc, char *argv[]) {
 int th_id, nthreads;
#pragma omp parallel private(th_id)
 {
  th_id = omp_get_thread_num();
  std::ostringstream ss;
  ss << "Hello World : 스레드 " << th_id << std::endl;
  std::cout << ss.str();
#pragma omp barrier
#pragma omp master
  {
   nthreads = omp_get_num_threads();
   std::cout << "모두 " << nthreads << "개의 스레드가 있습니다" << std::endl;
  }
 }
 return 0;
}
```

#### [포트란 77](https://ko.wikipedia.org/wiki/포트란_77 "wikilink")

``` fortran
      PROGRAM HELLO
      INTEGER ID, NTHRDS
      INTEGER OMP_GET_THREAD_NUM, OMP_GET_NUM_THREADS
C$OMP PARALLEL PRIVATE(ID)
      ID = OMP_GET_THREAD_NUM()
      PRINT *, 'HELLO WORLD : 스레드', ID
C$OMP BARRIER
      IF ( ID .EQ. 0 ) THEN
        NTHRDS = OMP_GET_NUM_THREADS()
        PRINT *, '모두', NTHRDS, '개의 스레드가 있습니다'
      END IF
C$OMP END PARALLEL
      END
```

#### [자유형](https://ko.wikipedia.org/wiki/자유형_언어 "wikilink") [포트란 90](https://ko.wikipedia.org/wiki/포트란_90 "wikilink")

``` fortran
 program hello90
 use omp_lib
 integer:: id, nthreads
   !$omp parallel private(id)
   id = omp_get_thread_num()
   write (*,*) 'Hello World : 스레드', id
   !$omp barrier
   if ( id == 0 ) then
     nthreads = omp_get_num_threads()
     write (*,*) '모두', nthreads, '개의 스레드가 있습니다'
   end if
   !$omp end parallel
 end program
```

## 같이 보기

  - [병렬 컴퓨팅](https://ko.wikipedia.org/wiki/병렬_컴퓨팅 "wikilink")
  - [CUDA](../Page/CUDA.md "wikilink")
  - [OpenCL](https://ko.wikipedia.org/wiki/OpenCL "wikilink")

## 각주

## 외부 링크

  - [OpenMP 공식 웹사이트](http://www.openmp.org/)

[분류:병렬 컴퓨팅](https://ko.wikipedia.org/wiki/분류:병렬_컴퓨팅 "wikilink") [분류:API](https://ko.wikipedia.org/wiki/분류:API "wikilink") [분류:C 프로그래밍 언어 계열](https://ko.wikipedia.org/wiki/분류:C_프로그래밍_언어_계열 "wikilink") [분류:포트란](https://ko.wikipedia.org/wiki/분류:포트란 "wikilink")

1.  [OpenMP 버전별 사양](https://www.openmp.org/specifications/)