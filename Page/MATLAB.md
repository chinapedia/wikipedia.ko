> This article is converted from Wikipedia: [MATLAB](https://ko.wikipedia.org/wiki/MATLAB).


[섬네일의](https://ko.wikipedia.org/wiki/파일:MATLAB_surf_sinc3D.svg "wikilink") 3차원 표면 플롯.

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

</code> \]\] **MATLAB**(매트랩)은 MathWorks 사에서 개발한 [수치 해석](https://ko.wikipedia.org/wiki/수치_해석 "wikilink") 및 [프로그래밍](https://ko.wikipedia.org/wiki/프로그래밍 "wikilink") 환경을 제공하는 공학용 [소프트웨어](../Page/소프트웨어.md "wikilink")이다. [행렬](../Page/행렬.md "wikilink")을 기반으로 한 계산 기능을 지원하며, 함수나 데이터를 그림으로 그리는 기능 및 프로그래밍을 통한 알고리즘 구현 등을 제공한다. MATLAB은 수치 계산이 필요한 과학 및 공학 분야에서 다양하게 사용된다. 30일간의 무료 체험판을 사용해 볼 수도 있다.

## 라이선스(License)

라이선스는 목적에 따라서 구분하며, 같은 기능을 사용하더라도 라이선스 비용이 구분된다.

또한 결제 방식을 영구버전(업데이트 불가능)과 연간 구독형(업데이트 가능)으로 구분한다.

  - 산업용
  - 학생용
  - 개인용
  - 캠퍼스 라이선스(Campus-whide License)

**산업용** 라이선스는 Mathworks에서 '상용, 정부 또는 기타 조직 단일 사용자용'이라고 소개하고 있다.

기업 등 조직에서 산업에 사용하기 위하여 매트랩(Matlab)을 구매하고자 할 때, **인원 수에 따라** 산업용 라이선스를 구매하면 된다.

**학생용** 라이선스는 Mathworks에서 '학위 수여 기관에서 제공하는 코스에서도 사용'이라고 소개하고 있다.

국내의 경우 많은 사립대학이 매트랩(Matlab) 캠퍼스 라이선스(Campus-wide License)를 보유하고 있으며, 국립대학의 경우 보유하지 않은 경우도 많다. 과거에는 교육용 라이선스와 학생용 라이선스를 구분하였으며 교육용은 등록된 교육기관에서만, 학생용은 학생 개인이 집이나 어디에서든 사용할 수있는 라이선스였다.

현재는 교육기관에 캠퍼스 라이선스가 있는 경우 재학생이 자유롭게 사용하는 것도 엄격하게 제한하지 않는 분위기로 가고 있다.

**개인용**은 Mathworks에서 '개인 용도 전용. 정부, 교육기관, 상용 또는 기타 조직 사용 불가'라고 소개하고 있다.

**스타트업 프로그램**에 대하여 Mathworks에서 "스타트업을 만들고 계신가요? 스타트업 프로그램에 등록하고 스타트업을 위한 가격에 이용하세요."라고 소개하고 있다.

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

  - [GNU 옥타브](../Page/GNU_옥타브.md "wikilink")

<!-- end list -->

  - [COMSOL Script](https://ko.wikipedia.org/wiki/COMSOL_Script "wikilink")

## 외부 링크

  - [MathWorks 사이트의 MATLAB 소개](http://www.mathworks.com/products/matlab/)
  - [대구경북과학기술원 Matlab 위키](https://klein.dgist.ac.kr/matlab/index.php/DGIST_Matlab)

[분류:C 소프트웨어](https://ko.wikipedia.org/wiki/분류:C_소프트웨어 "wikilink") [분류:컴퓨터 대수학 시스템](https://ko.wikipedia.org/wiki/분류:컴퓨터_대수학_시스템 "wikilink") [분류:크로스 플랫폼 소프트웨어](https://ko.wikipedia.org/wiki/분류:크로스_플랫폼_소프트웨어 "wikilink") [분류:선형대수학](https://ko.wikipedia.org/wiki/분류:선형대수학 "wikilink") [분류:수치선형대수학](https://ko.wikipedia.org/wiki/분류:수치선형대수학 "wikilink") [분류:수치 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:수치_프로그래밍_언어 "wikilink") [분류:수치 해석 소프트웨어](https://ko.wikipedia.org/wiki/분류:수치_해석_소프트웨어 "wikilink") [분류:병렬 컴퓨팅](https://ko.wikipedia.org/wiki/분류:병렬_컴퓨팅 "wikilink")