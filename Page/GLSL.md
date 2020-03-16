> This article is converted from Wikipedia: [GLSL](https://ko.wikipedia.org/wiki/GLSL).


**GLSL**(OpenGL Shading Language, OpenGL 셰이딩 언어)는 [C 언어를](https://ko.wikipedia.org/wiki/C_언어 "wikilink") 기초로 한, 상위 레벨 셰이딩 언어이다. **GLslang**로도 알려져 있다. [HLSL과](../Page/고급_셰이더_언어.md "wikilink") 유사한 이 언어는 [어셈블리 언어나](https://ko.wikipedia.org/wiki/어셈블리_언어 "wikilink") [하드웨어](https://ko.wikipedia.org/wiki/하드웨어 "wikilink")에 의존한 언어를 사용하지 않고, 개발자가 [그래픽스 파이프라인을](https://ko.wikipedia.org/wiki/그래픽스_파이프라인 "wikilink") 직접 제어할 수 있도록 [OpenGL](../Page/OpenGL.md "wikilink") ARB()가 책정하였다.

**GLSL**은 프로파일이 있어서 개발자는 [Cg로](https://ko.wikipedia.org/wiki/Cg_\(프로그래밍_언어\) "wikilink") 개발한 코드를 바로 변환할 수도 있다.

## 특징

  - 매킨토시나 [윈도](https://ko.wikipedia.org/wiki/마이크로소프트_윈도 "wikilink"), [리눅스](../Page/리눅스.md "wikilink") 등의 여러 [운영 체제](../Page/운영_체제.md "wikilink") 간의 호환성을 지원한다.
  - GLSL을 지원하는 어떠한 제조사의 [그래픽 카드에서도](../Page/그래픽_카드.md "wikilink") 동작하는 [셰이더](../Page/셰이더.md "wikilink")를 쓸 수 있다.
  - [하드웨어](https://ko.wikipedia.org/wiki/하드웨어 "wikilink") 제조사는 [그래픽 카드](../Page/그래픽_카드.md "wikilink") [장치 드라이버](../Page/장치_드라이버.md "wikilink") 내에 GLSL [컴파일러](../Page/컴파일러.md "wikilink")를 포함할 수 있도록 지원한다. 이 덕분에, 그 그래픽 카드의 [마이크로아키텍처](../Page/마이크로아키텍처.md "wikilink")에 최적화된 코드를 만들 수 있다.

## 버전

GLSL 버전은 OpenGL API의 특정 버전과 함께 진화해왔다. GLSL과 OpenGL 메이저, 마이너 버전이 매칭되는 OpenGL 버전 3.3 이상에서만 지원된다. GLSL과 OpenGL의 이 버전들은 다음의 표와 관련된다:

| GLSL 버전      | OpenGL 버전 | 날짜            | 셰이더 전처리기      |
| ------------ | --------- | ------------- | ------------- |
| 1.10.59\[1\] | 2.0       | 2004년 4월 30일  | \#version 110 |
| 1.20.8\[2\]  | 2.1       | 2006년 9월 07일  | \#version 120 |
| 1.30.10\[3\] | 3.0       | 2009년 11월 22일 | \#version 130 |
| 1.40.08\[4\] | 3.1       | 2009년 11월 22일 | \#version 140 |
| 1.50.11\[5\] | 3.2       | 2009년 12월 04일 | \#version 150 |
| 3.30.6\[6\]  | 3.3       | 2010년 3월 11일  | \#version 330 |
| 4.00.9\[7\]  | 4.0       | 2010년 7월 24일  | \#version 400 |
| 4.10.6\[8\]  | 4.1       | 2010년 7월 24일  | \#version 410 |
| 4.20.11\[9\] | 4.2       | 2011년 12월 12일 | \#version 420 |
| 4.30.8\[10\] | 4.3       | 2013년 2월 7일   | \#version 430 |
| 4.40.9\[11\] | 4.4       | 2014년 6월 16일  | \#version 440 |
| 4.50.7\[12\] | 4.5       | 2017년 5월 09일  | \#version 450 |
| 4.60.5\[13\] | 4.6       | 2018년 6월 14일  | \#version 460 |

[OpenGL ES과](../Page/OpenGL_ES.md "wikilink") [WebGL](../Page/WebGL.md "wikilink")은 **OpenGL ES Shading Language**, 간단히 줄여 **GLSL ES**를 사용한다.

| GLSL ES 버전    | OpenGL ES 버전 | WebGL 버전 | GLSL 버전 기반 | 날짜           | 셰이더 전처리기         |
| ------------- | ------------ | -------- | ---------- | ------------ | ---------------- |
| 1.00.17\[14\] | 2.0          | 1.0      | 1.20       | 2009년 5월 12일 | \#version 100 es |
| 3.00.6\[15\]  | 3.0          | 2.0      | 3.30       | 2016년 1월 29일 | \#version 300 es |

## 예제

### 간단한 GLSL 버텍스 셰이더

다음은 고정 기능 파이프 라인과 마찬가지로 입력 정점을 변환한다.

``` glsl
 void main (void)
 {
     gl_Position = ftransform ();
 }
```

ftransform() 는 GLSL 1.40과 GLSL ES 1.0에서 지원되지 않는다. 대신, 프로그래머는 새로운 OpenGL 3.1 표준에 따라 모델 뷰 행렬과 투영 행렬을 명시적으로 지정할 필요가 있다.

``` glsl
 # version 140
 uniform mat4 projectionMatrix;
 uniform mat4 modelviewMatrix;
 in vec3 position;

 void main (void)
 {
     gl_Position = projectionMatrix * modelviewMatrix * vec4 (position, 1.0);
 }
```

### 간단한 GLSL 지오메트리 셰이더

``` glsl
 layout (triangles) in;
 layout (triangle_strip, max_vertices = 3) out;

 in Input
 {
     vec4 Position;
 } VSout [3];

 void main (void)
 {
     for (int i = 0; i <3; i + +)
     {
         gl_Position = VSout [i]. Position;
         EmitVertex ();
     }
     EndPrimitive ();
 }
```

### 간단한 GLSL 프레그먼트 셰이더

``` glsl
 void main (void)
 {
     gl_FragColor = vec4 (1.0, 0.0, 0.0, 1.0);
 }
```

## 각주

## 외부 링크

  - [GLSL 언어 명세, 버전 1.30](http://www.opengl.org/registry/doc/GLSLangSpec.Full.1.30.08.pdf)

[분류:셰이더 언어](https://ko.wikipedia.org/wiki/분류:셰이더_언어 "wikilink") [분류:그래픽 라이브러리](https://ko.wikipedia.org/wiki/분류:그래픽_라이브러리 "wikilink") [분류:3차원 컴퓨터 그래픽스](https://ko.wikipedia.org/wiki/분류:3차원_컴퓨터_그래픽스 "wikilink") [분류:C 프로그래밍 언어 계열](https://ko.wikipedia.org/wiki/분류:C_프로그래밍_언어_계열 "wikilink")

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
14.
15.