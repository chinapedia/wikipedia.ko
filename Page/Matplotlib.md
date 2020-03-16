> This article is converted from Wikipedia: [Matplotlib](https://ko.wikipedia.org/wiki/Matplotlib).


**Matplotlib**은 파이썬에서 [매트랩](https://ko.wikipedia.org/wiki/매트랩 "wikilink")과 유사한 그래프 표시를 가능케 하는 라이브러리다.

## 예시

**라인 플롯** [섬네일](https://ko.wikipedia.org/wiki/파일:Matplotlib_basic_v.svg "wikilink")

``` numpy
>>> import matplotlib.pyplot as plt
>>> import numpy as np
>>> a = np.linspace(0, 10, 100)
>>> b = np.exp(-a)
>>> plt.plot(a, b)
>>> plt.show()
```

**[히스토그램](../Page/히스토그램.md "wikilink")** [섬네일](https://ko.wikipedia.org/wiki/파일:Matplotlib_histogram_v.svg "wikilink")

``` numpy
>>> import matplotlib.pyplot as plt
>>> from numpy.random import normal,rand
>>> x = normal(size=200)
>>> plt.hist(x, bins=30)
>>> plt.show()
```

**[산점도](https://ko.wikipedia.org/wiki/산점도 "wikilink")** [섬네일](https://ko.wikipedia.org/wiki/파일:Matplotlib_scatter_v.svg "wikilink")

``` numpy
>>> import matplotlib.pyplot as plt
>>> from numpy.random import rand
>>> a = rand(100)
>>> b = rand(100)
>>> plt.scatter(a, b)
>>> plt.show()
```

**3D 플롯** [섬네일](https://ko.wikipedia.org/wiki/파일:Matplotlib_3d_v.svg "wikilink")

``` numpy
>>> from matplotlib import cm
>>> from mpl_toolkits.mplot3d import Axes3D
>>> import matplotlib.pyplot as plt
>>> import numpy as np
>>> fig = plt.figure()
>>> ax = fig.gca(projection='3d')
>>> X = np.arange(-5, 5, 0.25)
>>> Y = np.arange(-5, 5, 0.25)
>>> X, Y = np.meshgrid(X, Y)
>>> R = np.sqrt(X**2 + Y**2)
>>> Z = np.sin(R)
>>> surf = ax.plot_surface(X, Y, Z, rstride=1, cstride=1, cmap=cm.coolwarm)
>>> plt.show()
```

**더 많은 예제**

파일:Mpl example qbo.svg|Image plot 파일:Mpl example Helmoltz coils.svg|Contour plot 파일:Weight Growth of RN First Rate Line-of-Battle Ships 1630-1875.svg|Scatter plot 파일:Logarithmic Spiral Pylab.svg|Polar plot 파일:Temp-sunspot-co2.svg|Line plot 파일:Mpl example Rosenbrock function.svg|3-D plot 파일:Mandelbrot set, plotted with Matplotlib.svg|Image plot

## 같이 보기

  - [NumPy](../Page/NumPy.md "wikilink")
  - [SciPy](../Page/SciPy.md "wikilink")
  - [SymPy](https://ko.wikipedia.org/wiki/SymPy "wikilink")
  - [매트랩](https://ko.wikipedia.org/wiki/매트랩 "wikilink")

## 각주

## 외부 링크

  -
[분류:파이썬 라이브러리](https://ko.wikipedia.org/wiki/분류:파이썬_라이브러리 "wikilink") [분류:파이썬으로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:파이썬으로_작성된_자유_소프트웨어 "wikilink")