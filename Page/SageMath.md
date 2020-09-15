> This article is converted from Wikipedia: [SageMath](https://ko.wikipedia.org/wiki/SageMath).


|최근 버전 출시일={{\#invoke:wd|qualifier|P348|P577}} |저장소={{\#invoke:wd|property|P1324|best}} |프로그래밍 언어={{\#invoke:Wd|properties||linked|P277}} |운영체제={{\#invoke:Wd|properties|linked|P306}} |라이선스=[GPL](https://ko.wikipedia.org/wiki/GPL "wikilink")v3 |웹사이트=[www.sagemath.org](https://www.sagemath.org)}} **SageMath**(과거 명칭: Sage 또는 SAGE, "System for Algebra and Geometry Experimentation"\[1\])는 대수학, 조합론, 그래프 이론, 수치해석, 수론, 미적분학, 통계학 등 수학의 다양한 분야의 기능을 갖춘 [컴퓨터 대수학 시스템이다](https://ko.wikipedia.org/wiki/컴퓨터_대수학_시스템 "wikilink").

SageMath의 첫 버전은 2005년 2월 24일 [GNU 일반 공중 사용 허가서를](../Page/GNU_일반_공중_사용_허가서.md "wikilink") 따르는 [오픈 소스 자유 소프트웨어로](../Page/자유-오픈_소스_소프트웨어.md "wikilink") 배포되었다. SageMath는 [마그마](https://ko.wikipedia.org/wiki/마그마_\(컴퓨터_대수학_시스템\) "wikilink"), [메이플](../Page/메이플_\(소프트웨어\).md "wikilink"), [매스매티카](../Page/매스매티카.md "wikilink"), [MATLAB](../Page/MATLAB.md "wikilink")을 대체하는 오픈 소스 소프트웨어를 개발하는 것을 목적으로 개발되었다.

## 사용 예제

### 대수 및 미적분

``` sage
x, a, b, c = var('x, a, b, c')
# Note that IPython also supports a faster way to do this, by calling
# this equivalent expression starting with a comma:
# ,var x a b c

log(sqrt(a)).simplify_log() # returns 1/2*log(a)
log(a / b).expand_log() # returns log(a) - log(b)
sin(a + b).simplify_trig() # returns sin(a)*cos(b) + sin(b)*cos(a)
cos(a + b).simplify_trig() # returns -sin(a)*sin(b) + cos(a)*cos(b)
(a + b)^5 # returns (a + b)^5
expand((a + b) ^ 5) # a^5 + 5*a^4*b + 10*a^3*b^2 + 10*a^2*b^3 + 5*a*b^4 + b^5

limit((x ^ 2 + 1) / (2 + x + 3 * x ^ 2), x=Infinity) # returns 1/3
limit(sin(x) / x, x=0) # returns 1

diff(acos(x), x) # returns -1/sqrt(-x^2 + 1)
f = exp(x) * log(x)
f.diff(x, 3) # returns e^x*log(x) + 3*e^x/x - 3*e^x/x^2 + 2*e^x/x^3

solve(a * x ^ 2 + b * x + c, x) # returns [x == -1/2*(b + sqrt(-4*a*c + b^2))/a,
                                # x == -1/2*(b - sqrt(-4*a*c + b^2))/a]

f = x ^ 2 + 432 / x
solve(f.diff(x) == 0, x) # returns [x == 3*I*sqrt(3) - 3,
                         # x == -3*I*sqrt(3) - 3, x == 6]
```

### 미분 방정식

``` sage
t = var('t') # define a variable t
x = function('x')(t) # define x to be a function of that variable
de = (diff(x, t) + x == 1)
desolve(de, [x, t]) # returns (c + e^t)*e^(-t)
```

### 선형 대수

``` numpy
A = matrix([[1,_2,_3],_[3,_2,_1],_[1,_1,_1|1, 2, 3], [3, 2, 1], [1, 1, 1]])
y = vector([0, -4, -1])
A.solve_right(y) # returns (-2, 1, 0)
A.eigenvalues() # returns [5, 0, -1]

B = matrix([[1,_2,_3],_[3,_2,_1],_[1,_2,_1|1, 2, 3], [3, 2, 1], [1, 2, 1]])
B.inverse() # returns
   [   0  1/2 -1/2]
   [-1/4 -1/4    1]
   [ 1/2    0 -1/2]

# same matrix, but over the ring of doubles (not rationals, as above)
sage: B = matrix(RDF, [[1,_2,_3],_[3,_2,_1],_[1,_2,_1|1, 2, 3], [3, 2, 1], [1, 2, 1]])
sage: B.inverse()

[-5.55111512313e-17                0.5               -0.5]
[             -0.25              -0.25                1.0]
[               0.5                0.0               -0.5]

# The Moore-Penrose pseudo-inverse
sage: C = matrix([[1_,_1],_[2_,_2|1 , 1], [2 , 2]])
sage: C.pseudoinverse()
[1/10  1/5]
[1/10  1/5]

# Alternatively, call NumPy for the pseudo-inverse
# (only numerical)
import numpy
C = matrix([[1_,_1],_[2_,_2|1 , 1], [2 , 2]])
matrix(numpy.linalg.pinv(C)) # returns
   [0.1 0.2]
   [0.1 0.2]
```

### 정수론

``` sage
prime_pi(1000000) # returns 78498, the number of primes less than one million

E = EllipticCurve('389a') # construct an elliptic curve from its Cremona label
P, Q = E.gens()
7 * P + Q # returns (24187731458439253/244328192262001 :
          # 3778434777075334029261244/3819094217575529893001 : 1)
```

``` text
sage: E2 = EllipticCurve(CC, [0,0,-2,1,1])
sage: E2
Elliptic Curve defined by y^2 + (-2.00000000000000)*y =
         x^3 + 1.00000000000000*x + 1.00000000000000 over
         Complex Field with 53 bits of precision
sage: E2.j_invariant()
61.7142857142857
```

### 가환대수

``` sage
sage: P.<x, y, z> = PolynomialRing(QQ) # polynomial ring in x, y, z over the rationals
sage: (x**3 + y**3 + z**3 - 3*x*y*z).factor()
(x + y + z) * (x^2 - x*y + y^2 - x*z - y*z + z^2)

sage: I = P.ideal(x**2, x*y - y**2) # ideals defined by generators
sage: I.groebner_basis()
[y^3, x^2, x*y - y^2]
```

## 각주

## 외부 링크

  - [SageMath 공식 홈페이지](https://www.sagemath.org/)
  - [SageMath 웹 인터페이스](https://sagecell.sagemath.org/)

[분류:컴퓨터 대수학 시스템](https://ko.wikipedia.org/wiki/분류:컴퓨터_대수학_시스템 "wikilink")

1.