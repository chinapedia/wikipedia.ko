> This article is converted from Wikipedia: [OpenCL](https://ko.wikipedia.org/wiki/OpenCL).


**OpenCL**()은 개방형 범용 병렬 컴퓨팅 프레임워크이다. [CPU](../Page/중앙_처리_장치.md "wikilink"), [GPU](../Page/그래픽_처리_장치.md "wikilink"), [DSP](../Page/디지털_신호_처리_장치.md "wikilink") 등의 프로세서로 이루어진 이종 플랫폼에서 실행되는 프로그램을 작성할 수 있게 해 준다. OpenCL은 커널 코드를 작성하기 위한 [C99](../Page/C99.md "wikilink") 기반의 언어인 OpenCL C와 플랫폼을 정의하고 제어하기 위한 [API](../Page/API.md "wikilink")를 포함하고 있다. OpenCL은 작업 기반(task-based) 및 데이터 기반(data-based) 병렬 컴퓨팅을 제공한다.

OpenCL이 만들어진 이유는 [OpenGL](../Page/OpenGL.md "wikilink")이나 [OpenAL](../Page/OpenAL.md "wikilink")이 만들어진 이유와 비슷하다. OpenGL과 OpenAL은 각각 [3차원 컴퓨터 그래픽스](../Page/3차원_컴퓨터_그래픽스.md "wikilink") 및 컴퓨터 오디오에 대한 산업계의 [개방형 표준이다](../Page/개방형_표준.md "wikilink"). OpenCL은 비영리 기술 컨소시엄인 [크로노스 그룹](../Page/크로노스_그룹.md "wikilink")(Khronos Group)에서 관리하고 있다.

## 역사

OpenCL은 [애플이](https://ko.wikipedia.org/wiki/애플_\(기업\) "wikilink") 최초로 개발했으며 OpenCL의 상표권도 애플이 가지고 있다. 그 후 [AMD](https://ko.wikipedia.org/wiki/AMD "wikilink"), [인텔](../Page/인텔.md "wikilink"), [엔비디아](../Page/엔비디아.md "wikilink") 등과 함께 애플은 문서를 다듬어 최초의 제안서(proposal)를 [크로노스 그룹에](../Page/크로노스_그룹.md "wikilink") 제출하였다. 2008년 6월 16일 크로노스 컴퓨트 워킹 그룹(Khronos Compute Working Group)이 결성되었다.\[1\] 크로노스 컴퓨트 워킹 그룹에는 CPU, GPU, 임베디드 프로세서, 소프트웨어 업체들이 참여하였다. 2008년 6월부터 5개월 동안 이 그룹은 OpenCL 1.0을 만들기 위해 작업하였다. 2008년 11월 18일 마침내 기술 규격 정보를 담은 OpenCL 1.0 명세서(specification)가 완성되었다.\[2\] 이 기술 명세서는 크로노스 그룹 그룹원들이 검토(review)하였다. 그 후, 2008년 12월 8일 공식적으로 발표되었다.\[3\]

OpenCL은 [맥 OS X 10.6](https://ko.wikipedia.org/wiki/맥_OS_X_10.6 "wikilink") 스노 레퍼드에서부터 지원된다.\[4\]  최초의 OpenCL 구현은 [LLVM](../Page/LLVM.md "wikilink") 및 [Clang](https://ko.wikipedia.org/wiki/Clang "wikilink") 컴파일러를 기반으로 한 것으로 알려졌다.

AMD는 OpenCL 및 [다이렉트엑스](https://ko.wikipedia.org/wiki/다이렉트엑스 "wikilink") 11을 지원하는 대신 AMD 고유의 스트림 프레임워크 내 "Close to Metal"을 포기하기로 결정했다.\[5\]\[6\] [RapidMind](https://ko.wikipedia.org/wiki/RapidMind "wikilink")는 OpenCL 채택을 공식 선언하여 자신들의 개발 플랫폼의 밑단에 쓰기로 하였는데, 여러 제조업체의 GPU를 단일 인터페이스를 통해 지원하기 위해서였다.\[7\] [엔비디아](../Page/엔비디아.md "wikilink")는 2008년 12월 9일 자사의 GPU 컴퓨팅 툴킷에서 OpenCL 1.0을 완벽히 지원한다고 발표하였다.\[8\] OpenCL과 [쿠다](https://ko.wikipedia.org/wiki/쿠다 "wikilink")를 비교한다면 두개의 컴퓨터 언어를 비교하는 것과 비슷하다는 입장이다.

OpenCL 명세서는 크로노스에서 개발 중이며, 관심 있는 어떤 회사에라도 개방되어 있다.

## 구현

2008/12/10 AMD와 엔비디아는 OpenCL 최초의 대중 시연을 실시하여 75분짜리 발표를 Siggraph Asia 2008에서 선보였다. AMD는 CPU 가속 OpenCL 시연으로 OpenCL의 코어 개수에 대한 규모가변성을 보였고, 엔비디아는 GPU-가속 시범을 보였다.\[9\]\[10\]

2009/03/26 GDC 2009에서는 AMD와 [하복](https://ko.wikipedia.org/wiki/하복 "wikilink")이 최초로 AMD [라데온 HD 4000 시리즈](https://ko.wikipedia.org/wiki/라데온_HD_4000_시리즈 "wikilink") GPU 상에서 OpenCL을 이용하여 [하복 클로스](https://ko.wikipedia.org/wiki/하복_클로스 "wikilink")(Havok Cloth)를 가속시키는 시연을 실시하였다.\[11\]

2009/04/20, 엔비디아가 OpenCL 조기 접근 프로그램 참가 개발자 대상으로 자신의 OpenCL 드라이버와 SDK를 배포한다고 발표하였다.\[12\]

2009년 9월 애플에서 [맥 OS X 10.6](https://ko.wikipedia.org/wiki/맥_OS_X_10.6 "wikilink") 스노 레퍼드 버전에 OpenCL이 구현되었다.\[13\] 스노 레퍼드에 포함되는 OpenCL은 초기에는 다음 GPU를 지원한다:\[14\]

  - NVIDIA Geforce 8600M GT, GeForce 8800 GT, GeForce 8800 GTS, Geforce 9400M, GeForce 9600M GT, GeForce GT 120, GeForce GT 130,
  - ATI Radeon 4850, Radeon 4870.

## 예제

다음은 [고속 푸리에 변환을](../Page/고속_푸리에_변환.md "wikilink") 하는 예제이다. 호스트 프로그램은 다음과 같다. \[15\] <code>

``` c
// GPU 장치와 계산 context를 생성한다
context = clCreateContextFromType(NULL, CL_DEVICE_TYPE_GPU, NULL, NULL, NULL);

// 작업 대기열을 생성한다
clGetDeviceIDs(NULL, CL_DEVICE_TYPE_GPU, 1, &device_id, NULL);
queue = clCreateCommandQueue(context, device_id, 0, NULL);

// 버퍼 메모리 객체를 생성한다
memobjs[0] = clCreateBuffer(context, CL_MEM_READ_ONLY | CL_MEM_COPY_HOST_PTR, sizeof(float)*2*num_entries, srcA, NULL);
memobjs[1] = clCreateBuffer(context, CL_MEM_READ_WRITE, sizeof(float)*2*num_entries, NULL, NULL);

// 계산 프로그램을 생성한다
program = clCreateProgramFromSource(context, 1, &fft1D_1024_kernel_src, NULL, NULL);

// 계산 프로그램 실행 코드를 생성한다
clBuildProgram(program, 0, NULL, NULL, NULL, NULL);

// 계산 커널을 생성한다
kernel = clCreateKernel(program, "fft1D_1024", NULL);

// args 값을 설정한다
clSetKernelArg(kernel, 0, sizeof(cl_mem), (void *)&memobjs[0]);
clSetKernelArg(kernel, 1, sizeof(cl_mem), (void *)&memobjs[1]);
clSetKernelArg(kernel, 2, sizeof(float)*(local_work_size[0]+1)*16, NULL);
clSetKernelArg(kernel, 3, sizeof(float)*(local_work_size[0]+1)*16, NULL);

// 커널을 실행시킨다
global_work_size[0] = num_entries;
local_work_size[0] = 64;
clEnqueueNDRangeKernel(queue, kernel, 1, NULL, global_work_size, local_work_size, 0, NULL, NULL);
```

</code>

실제 계산이 이루어지는 커널 함수는 다음과 같다.\[16\]\[17\] <code>

``` c
// This kernel computes FFT of length 1024. The 1024 length FFT is decomposed into
// calls to a radix 16 function, another radix 16 function and then a radix 4 function

__kernel void fft1D_1024 (__global float2 *in, __global float2 *out,
                          __local float *sMemx, __local float *sMemy) {
  int tid = get_local_id(0);
  int blockIdx = get_group_id(0) * 1024 + tid;
  float2 data[16];

  // 전역 메모리 입출력 영역 시작 주소
  in = in + blockIdx;  out = out + blockIdx;

  globalLoads(data, in, 64); // 한 덩어리로 전역 메모리 읽기
  fftRadix16Pass(data);       // 자리 변경 없이 radix-16 처리
  twiddleFactorMul(data, tid, 1024, 0);

  // 지역 메모리를 이용한 지역 shuffle
  localShuffle(data, sMemx, sMemy, tid, (((tid & 15) * 65) + (tid >> 4)));
  fftRadix16Pass(data);               // 자리 변경 없이 radix-16 처리
  twiddleFactorMul(data, tid, 64, 4); // 회전 인수 곱셈

  localShuffle(data, sMemx, sMemy, tid, (((tid >> 4) * 64) + (tid & 15)));

  // radix-4 함수 호출 4회
  fftRadix4Pass(data);
  fftRadix4Pass(data + 4);
  fftRadix4Pass(data + 8);
  fftRadix4Pass(data + 12);

  //한덩어리로 전역 메모리에 기록
  globalStores(data, out, 64);
}
```

</code>

## 같이 보기

  - [GPU](../Page/그래픽_처리_장치.md "wikilink")
  - [GPGPU](https://ko.wikipedia.org/wiki/GPGPU "wikilink")
  - [CUDA](../Page/CUDA.md "wikilink")
  - [Close to Metal](https://ko.wikipedia.org/wiki/Close_to_Metal "wikilink")
  - [BrookGPU](https://ko.wikipedia.org/wiki/BrookGPU "wikilink")
  - [Lib Sh](https://ko.wikipedia.org/wiki/Lib_Sh "wikilink")
  - [인텔 라라비](https://ko.wikipedia.org/wiki/라라비_\(마이크로아키텍처\) "wikilink")

## 참고 문헌

## 외부 링크

  - [OpenCL 홈페이지](http://www.khronos.org/opencl/)

  - [OpenCL 1.2 기술 명세서](http://www.khronos.org/registry/cl/specs/opencl-1.2.pdf)

  - [OpenCL: What you need to know](http://www.macworld.com/article/134858/2008/08/snowleopard_opencl.html) - article published in Macworld, August 2008

  - [HPCWire: OpenCL on the Fast Track](https://web.archive.org/web/20081218113641/http://www.hpcwire.com/blogs/OpenCL_On_the_Fast_Track_33608199.html)

  - [The Khronos Group Releases OpenCL 1.0 Specification](https://web.archive.org/web/20100713014204/http://www.khronos.org/news/press/releases/the_khronos_group_releases_opencl_1.0_specification/)

[분류:GPGPU](https://ko.wikipedia.org/wiki/분류:GPGPU "wikilink") [분류:API](https://ko.wikipedia.org/wiki/분류:API "wikilink") [분류:2009년 소프트웨어](https://ko.wikipedia.org/wiki/분류:2009년_소프트웨어 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.
9.
10.
11.
12.
13.
14. {{ 웹 인용 |url=<https://www.apple.com/macosx/specs.html> |제목=Mac OS X Snow Leopard – *Technical specifications and system requirements* |출판사=Apple Inc |날짜=2009-06-08 |확인날짜=2009-06-12 }}
15.
16. [Fitting FFT onto the G80 Architecture](http://www.cs.berkeley.edu/~kubitron/courses/cs258-S08/projects/reports/project6_report.pdf) 를 바탕으로 구현함
17.