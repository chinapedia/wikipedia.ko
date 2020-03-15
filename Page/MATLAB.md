> This article is converted from Wikipedia: [MATLAB](https://ko.wikipedia.org/wiki/MATLAB).


**MATLAB**(매트랩)은 MathWorks 사에서 개발한 [수치 해석](https://ko.wikipedia.org/wiki/수치_해석 "wikilink") 및 [프로그래밍](https://ko.wikipedia.org/wiki/프로그래밍 "wikilink") 환경을 제공하는 공학용 [소프트웨어](https://ko.wikipedia.org/wiki/소프트웨어 "wikilink")이다. [행렬](https://ko.wikipedia.org/wiki/행렬 "wikilink")을 기반으로 한 계산 기능을 지원하며, 함수나 데이터를 그림으로 그리는 기능 및 프로그래밍을 통한 알고리즘 구현 등을 제공한다. MATLAB은 수치 계산이 필요한 과학 및 공학 분야에서 다양하게 사용된다. 30일간의 무료 체험판을 사용해 볼 수도 있다. [섬네일의](https://ko.wikipedia.org/wiki/파일:MATLAB_surf_sinc3D.svg "wikilink") 3차원 표면 플롯.

|                                                                                                                                       |
| ------------------------------------------------------------------------------------------------------------------------------------- |
| \(\begin{align}
  & -10\le x\le 10 \\
 & -10\le y\le 10 \\
 & z=\operatorname{sinc}\left( \sqrt{x^{2}+y^{2}} \right) \\
\end{align}\) |
|                                                                                                                                       |

**MATLAB** 소스 코드는 다음과 같다. <code>

``` matlab
[X,Y] = meshgrid(-10:0.25:10,-10:0.25:10);
f = sinc(sqrt((X/pi).^2+(Y/pi).^2));
h = figure(1);
surf(X,Y,f);
axis([-10 10 -10 10 -0.3 1])
xlabel('{\bfx}')
ylabel('{\bfy}')
zlabel('{\bfsinc} ({\bfR})')
hidden off
plot2svg('sinc3D.svg',h)    % utilizes the SVG exporting script (by Juerg Schwizer)
                            % available from MATLAB Central File Exchange
```

</code> \]\]

## 내장 프로그램

### 툴박스

  - Control System Toolbox : 제어시스템의 설계 및 해석을 위한 툴박스
  - System Identification Toolbox : 시스템의 전달 함수를 구하기 위한 툴박스
  - Robust Control Toolbox : 강인성 제어를 위한 툴박스
  - Optimization Toolbox : 최적화를 위한 툴박스
  - Signal Processing Toolbox : 신호처리에 관련한 툴박스
  - Image Processing Toolbox : 영상처리에 관련된 툴박스
  - Wavelet Toolbox : 웨이블릿 변환에 관한 툴박스
  - Symbolic Toolbox : 심볼로 이루어진 수식을 연산하기 위한 툴박스
  - SIMULINK :그래픽하게 제어 시스템을 모델링하고 simulation하기 위한 툴박스
  - Runtime Server Toolbox : 작성된 M-file을 MATLAB없이 사용하기 위한 툴박스

### 개발도구

  - M-Lint Code Checker : 코드를 분석하고 변경을 권장하여 성능과 유지 능력을 향상시킨다.모든 파일을 스캔하여 코드 효율성, 파일의 차이점, 파일 의존성 및 코드 커버리지에 대해 보고한다.

## 같이 보기

  - [COMSOL Script](https://ko.wikipedia.org/wiki/COMSOL_Script "wikilink")
  - [GNU 옥타브](https://ko.wikipedia.org/wiki/GNU_옥타브 "wikilink")

## 외부 링크

  - [MathWorks 사이트의 MATLAB 소개](http://www.mathworks.com/products/matlab/)
  - [대구경북과학기술원 Matlab 위키](https://klein.dgist.ac.kr/matlab/index.php/DGIST_Matlab)

[분류:C 소프트웨어](https://ko.wikipedia.org/wiki/분류:C_소프트웨어 "wikilink") [분류:컴퓨터 대수학 시스템](https://ko.wikipedia.org/wiki/분류:컴퓨터_대수학_시스템 "wikilink") [분류:크로스 플랫폼 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_소프트웨어 "wikilink") [분류:선형대수학](https://ko.wikipedia.org/wiki/분류:선형대수학 "wikilink") [분류:수치선형대수학](https://ko.wikipedia.org/wiki/분류:수치선형대수학 "wikilink") [분류:수치 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:수치_프로그래밍_언어 "wikilink") [분류:수치 해석 소프트웨어](https://ko.wikipedia.org/wiki/분류:수치_해석_소프트웨어 "wikilink") [분류:병렬 컴퓨팅](https://ko.wikipedia.org/wiki/분류:병렬_컴퓨팅 "wikilink")