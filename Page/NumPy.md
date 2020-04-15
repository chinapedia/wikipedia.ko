> This article is converted from Wikipedia: [NumPy](https://ko.wikipedia.org/wiki/NumPy).


**NumPy**("넘파이"라 읽는다)는 [행렬](../Page/행렬.md "wikilink")이나 일반적으로 대규모 다차원 [배열](../Page/배열.md "wikilink")을 쉽게 처리 할 수 있도록 지원하는 [파이썬](../Page/파이썬.md "wikilink")의 [라이브러리](https://ko.wikipedia.org/wiki/라이브러리 "wikilink")이다. NumPy는 데이터 구조 외에도 수치 계산을 위해 효율적으로 구현된 기능을 제공한다.

## 예제

  - [배열](../Page/배열.md "wikilink") 생성

<!-- end list -->

``` numpy
>>> import numpy as np
>>> x = np.array([1, 2, 3])
>>> x
array([1, 2, 3])
>>> y = np.arange(10) # like Python's range, but returns an array
>>> y
array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])
```

  - 기본 작업

<!-- end list -->

``` numpy
>>> a = np.array([1, 2, 3, 6])
>>> b = np.linspace(0, 2, 4) # create an array with four equally spaced points starting with 0 and ending with 2.
>>> c = a - b
>>> c
array([ 1. , 1.33333333, 1.66666667, 4. ])
>>> a**2
array([ 1, 4, 9, 36])
```

  - [유니버셜 함수](https://ko.wikipedia.org/wiki/유니버셜_함수 "wikilink")

<!-- end list -->

``` numpy
>>> a = np.linspace(-np.pi, np.pi, 100)
>>> b = np.sin(a)
>>> c = np.cos(a)
```

  - [선형 대수학](https://ko.wikipedia.org/wiki/선형_대수학 "wikilink")

<!-- end list -->

``` numpy
>>> from numpy.random import rand
>>> from numpy.linalg import solve, inv
>>> a = np.array([[1,_2,_3],_[3,_4,_6.7],_[5,_9.0,_5|1, 2, 3], [3, 4, 6.7], [5, 9.0, 5]])
>>> a.transpose()
array([[ 1. , 3. , 5. ],
       [ 2. ,  4. ,  9. ],
       [ 3. ,  6.7,  5. ]])
>>> inv(a)
array([[-2.27683616, 0.96045198, 0.07909605],
       [ 1.04519774, -0.56497175,  0.1299435 ],
       [ 0.39548023,  0.05649718, -0.11299435]])
>>> b = np.array([3, 2, 1])
>>> solve(a, b) # solve the equation ax = b
array([-4.83050847, 2.13559322, 1.18644068])
>>> c = rand(3, 3) * 20 # create a 3x3 random matrix of values within [0,1] scaled by 20
>>> c
array([[ 3.98732789, 2.47702609, 4.71167924],
       [  9.24410671,   5.5240412 ,  10.6468792 ],
       [ 10.38136661,   8.44968437,  15.17639591]])
>>> np.dot(a, c) # matrix multiplication
array([[ 53.61964114, 38.8741616 , 71.53462537],
       [ 118.4935668 ,   86.14012835,  158.40440712],
       [ 155.04043289,  104.3499231 ,  195.26228855]])
>>> a @ c # Starting with Python 3.5 and NumPy 1.10
array([[ 53.61964114, 38.8741616 , 71.53462537],
       [ 118.4935668 ,   86.14012835,  158.40440712],
       [ 155.04043289,  104.3499231 ,  195.26228855]])
```

  - [OpenCV](../Page/OpenCV.md "wikilink")와의 통합

<!-- end list -->

``` numpy
>>> import numpy as np
>>> import cv2
>>> r = np.reshape(np.arange(256*256)%256,(256,256)) # 256x256 pixel array with a horizontal gradient from 0 to 255 for the red color channel
>>> g = np.zeros_like(r) # array of same size and type as r but filled with 0s for the green color channel
>>> b = r.T # transposed r will give a vertical gradient for the blue color channel
>>> cv2.imwrite('gradients.png', np.dstack([b,g,r])) # OpenCV images are interpreted as BGR, the depth-stacked array will be written to an 8bit RGB PNG-file called 'gradients.png'
True
```

  - [최근접 이웃 탐색](https://ko.wikipedia.org/wiki/최근접_이웃_탐색 "wikilink")

<!-- end list -->

``` numpy
>>> # # # Pure iterative Python # # #
>>> points = [[9,2,8],[4,7,2],[3,4,4],[5,6,9],[5,0,7],[8,2,7],[0,3,2],[7,3,0],[6,1,1],[2,9,6|9,2,8],[4,7,2],[3,4,4],[5,6,9],[5,0,7],[8,2,7],[0,3,2],[7,3,0],[6,1,1],[2,9,6]]
>>> qPoint = [4,5,3]
>>> minIdx = -1
>>> minDist = -1
>>> for idx, point in enumerate(points): # iterate over all points
        dist = sum([(dp-dq)**2 for dp,dq in zip(point,qPoint)])**0.5  # compute the euclidean distance for each point to q
        if dist < minDist or minDist < 0:  # if necessary, update minimum distance and index of the corresponding point
            minDist = dist
            minIdx = idx

>>> print 'Nearest point to q: ', points[minIdx]
Nearest point to q: [3, 4, 4]

>>> # # # Equivalent NumPy vectorization # # #
>>> import numpy as np
>>> points = np.array([[9,2,8],[4,7,2],[3,4,4],[5,6,9],[5,0,7],[8,2,7],[0,3,2],[7,3,0],[6,1,1],[2,9,6|9,2,8],[4,7,2],[3,4,4],[5,6,9],[5,0,7],[8,2,7],[0,3,2],[7,3,0],[6,1,1],[2,9,6]])
>>> qPoint = np.array([4,5,3])
>>> minIdx = np.argmin(np.linalg.norm(points-qPoint,axis=1)) # compute all euclidean distances at once and return the index of the smallest one
>>> print 'Nearest point to q: ', points[minIdx]
Nearest point to q: [3 4 4]
```

## 같이 보기

  - [SciPy](../Page/SciPy.md "wikilink")
  - [SymPy](https://ko.wikipedia.org/wiki/SymPy "wikilink")
  - [Matplotlib](../Page/Matplotlib.md "wikilink")

## 외부 링크

  -
  - [History of NumPy](https://scipy.github.io/old-wiki/pages/History_of_SciPy)

[분류:배열 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:배열_프로그래밍_언어 "wikilink") [분류:자유 수학 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_수학_소프트웨어 "wikilink") [분류:자유 과학 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_과학_소프트웨어 "wikilink") [분류:수치 해석 소프트웨어](https://ko.wikipedia.org/wiki/분류:수치_해석_소프트웨어 "wikilink") [분류:수치 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:수치_프로그래밍_언어 "wikilink") [분류:파이썬 라이브러리](https://ko.wikipedia.org/wiki/분류:파이썬_라이브러리 "wikilink") [분류:BSD 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:BSD_라이선스_소프트웨어 "wikilink")