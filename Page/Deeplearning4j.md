> This article is converted from Wikipedia: [Deeplearning4j](https://ko.wikipedia.org/wiki/Deeplearning4j).


**Eclipse Deeplearning4j**는 [자바와](../Page/자바_\(프로그래밍_언어\).md "wikilink") [자바 가상머신](../Page/자바_가상_머신.md "wikilink") 용으로 작성된 [딥 러닝](https://ko.wikipedia.org/wiki/딥_러닝 "wikilink") 라이브러리이며\[1\]\[2\] [딥 러닝](https://ko.wikipedia.org/wiki/딥_러닝 "wikilink") 알고리즘을 광범위하게 지원하는 [컴퓨팅](../Page/라이브러리_\(컴퓨팅\).md "wikilink") 프레임워크이다.\[3\] Deeplearning4j에는 [Restricted Boltzmann machine](https://ko.wikipedia.org/wiki/:en:Restricted_Boltzmann_machine "wikilink"), [deep belief net](https://ko.wikipedia.org/wiki/:en:Deep_belief_network "wikilink"), deep autoencoder, stacked denoising autoencoder, [recursive neural tensor network](https://ko.wikipedia.org/wiki/:en:Recursive_neural_network "wikilink"), [word2vec](https://ko.wikipedia.org/wiki/:en:Word2vec "wikilink"), doc2vec, [Glove](https://ko.wikipedia.org/wiki/:en:GloVe_\(machine_learning\) "wikilink") 등의 알고리듬들이 구현 되어 있다. 이 알고리듬은 모두 아파치 [하둡과](../Page/아파치_하둡.md "wikilink") [스파크를](../Page/아파치_스파크.md "wikilink") 이용해 분산 병렬 처리가 가능하다.\[4\]

Deeplearning4j는 [아파치 라이선스](../Page/아파치_라이선스.md "wikilink") 2.0을 따르는 [오픈 소스 소프트웨어이며](../Page/오픈_소스_소프트웨어.md "wikilink")\[5\] [샌프란시스코](../Page/샌프란시스코.md "wikilink")와 [도쿄에](../Page/도쿄도.md "wikilink") 근거를 두며 Adam Gibson이 이끄는 [기계 학습](../Page/기계_학습.md "wikilink") 그룹이 주로 개발하고 있다.\[6\]\[7\] Skymind Intelligence Layer라고 불리는 엔터프라이즈 배포판에 DL4J, [Tensorflow](../Page/텐서플로.md "wikilink"), [Keras](https://ko.wikipedia.org/wiki/:en:Keras "wikilink") 및 기타 딥 러닝 라이브러리를 번들로 제공하는 스타트업 회사인 [Skymind를](https://ko.wikipedia.org/wiki/:en:Skymind "wikilink") 통해 상업적 지원을 받을 수 있다.\[8\] Deeplearning4j는 2017년 10월에 [Eclipse Foundation에](../Page/이클립스_재단.md "wikilink") 합류 하였다.\[9\]

## 개요

Deeplearning4j는 널리 사용되는 프로그래밍 언어 인 [자바를](../Page/자바_\(프로그래밍_언어\).md "wikilink") 사용하지만 [클로저와도](../Page/클로저_\(프로그래밍_언어\).md "wikilink") 호환 되며 [스칼라](../Page/스칼라_\(프로그래밍_언어\).md "wikilink") API를 포함하고 있다. 자체 오픈 소스 수치 계산 라이브러리인 [ND4J를](https://ko.wikipedia.org/wiki/:en:ND4J_\(software\) "wikilink") 사용하여 [CPU와](../Page/중앙_처리_장치.md "wikilink") [GPU](../Page/그래픽_처리_장치.md "wikilink") 모두에서 작동한다.\[10\]\[11\]

Deeplearning4j는 다수의 상용 및 학술 응용 분야에서 사용되고 있다. 코드는 [깃허브](../Page/깃허브.md "wikilink")에 공개되어 있으며\[12\] 개발자 지원 포럼은 [기터를](https://ko.wikipedia.org/wiki/:en:Gitter "wikilink") 통해 서비스 되고 있다.\[13\] 한국 개발자를 위한 [기터](https://ko.wikipedia.org/wiki/:en:Gitter "wikilink") 채널도 서비스 되고 있다.\[14\]

Deeplearning4j 프레임워크를 이용하여 Restricted Boltzmann machines, convolutional nets, autoencoders, and recurrent nets과 같은 얕은 신경망들을 조합 하여 다양한 형태의 깊은 신경망을 만들 수 있다. 또한 강력한 시각화 도구\[15\]와 Computation graph\[16\]를 포함 하고 있다.

## 분산 처리

Deeplearning4j의 학습 과정은 클러스터에서 분산 컴퓨팅을 이용할 수 있도록 구현되어 있다. 아파치 [하둡](../Page/아파치_하둡.md "wikilink") 주요 배포판과 [스파크를](../Page/아파치_스파크.md "wikilink") 통한 반복적 리듀스 작업을 통해 분산 학습이 가능하다.\[17\]\[18\] 또한 Deeplearning4j는 GPU 연산을 위한 CUDA 커널 구현체를 포함하고 있으며 분산된 GPU환경에서도 작동한다.

## 활용

Deeplearning4j의 학습 과정은 분산 컴퓨팅을 이용할 수 있도록 짜여져있다. 즉, [하둡과](../Page/아파치_하둡.md "wikilink") 스파크를 기반으로 한 반복적 맵리듀스로 학습이 가능하다. 또, 쿠다 커널도 지원하고 있어서 GPU를 이용한 연산이 가능하며 여러 대의 GPU를 이용한 분산 학습도 가능하다.

Deeplearning4j는 ND4J를 이용해 다차원 어레이 클래스 연산이 가능하다. ND4J는 [파이썬](../Page/파이썬.md "wikilink")의 Numpy와 같은 역할을 한다. 이를 이용해 선형 대수과 행렬 연산을 효과적으로 처리할 수 있다.

카노바를 이용하면 CSV파일, 이미지, 소리, 텍스트, 비디오 파일을 벡터 형태의 데이터로 쉽게 만들 수 있다.

Deeplearning4j는 벡터 공간 모델링과 주제 모델링(topic modelling) 도구를 포함하고 있어 규모가 큰 텍스트 데이터를 분산 시스템에서 빠르게 처리할 수 있다. 한편 Deeplearning4j는 tf-idf, word2vec, doc2vec, GloVe 알고리즘의 구현을 포함하고 있다. 또, t-SNE를 이용해 단어 구름(word cloud)을 시각화할 수 있다.

Deeplearning4j는 금융 업계의 사기 탐지\[19\], 비정상 행위 탐지\[20\], 이미지 인식 등에 사용되고 있다. 또 RapidMiner와 Prediction.io 등 다른 기계학습 플랫폼을 포함하고 있다\[21\].

## 관련 라이브러리

  - OpenNN [c++](https://ko.wikipedia.org/wiki/c++ "wikilink")기반의 오픈소스 [딥 러닝](https://ko.wikipedia.org/wiki/딥_러닝 "wikilink") 라이브러리
  - [토치](http://torch.ch/) [루아](../Page/루아_\(프로그래밍_언어\).md "wikilink") 기반의 오픈소스 [딥 러닝](https://ko.wikipedia.org/wiki/딥_러닝 "wikilink") 라이브러리
  - [띠아노](http://www.deeplearning.net/software/theano/) [파이썬](../Page/파이썬.md "wikilink") 기반의 오픈소스 [딥 러닝](https://ko.wikipedia.org/wiki/딥_러닝 "wikilink") 라이브러리
  - [Tensorflow](http://www.tensorflow.org/) 구글에서 발표한 기계학습 오픈소스 library

## 더 보기

  - [딥 러닝](https://ko.wikipedia.org/wiki/딥_러닝 "wikilink")
  - [인공지능](../Page/인공지능.md "wikilink")
  - [머신 러닝](https://ko.wikipedia.org/wiki/머신_러닝 "wikilink")

## 각주

## 외부 링크

  -
  -
  -
  -
  -
  -
  -
  -
[분류:딥 러닝](https://ko.wikipedia.org/wiki/분류:딥_러닝 "wikilink") [분류:기계 학습](https://ko.wikipedia.org/wiki/분류:기계_학습 "wikilink") [분류:스칼라로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:스칼라로_작성된_자유_소프트웨어 "wikilink") [분류:자바 프로그래밍 언어 계열](https://ko.wikipedia.org/wiki/분류:자바_프로그래밍_언어_계열 "wikilink") [분류:수치 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:수치_프로그래밍_언어 "wikilink") [분류:자바로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:자바로_작성된_자유_소프트웨어 "wikilink") [분류:아파치 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:아파치_라이선스_소프트웨어 "wikilink") [분류:인공신경망](https://ko.wikipedia.org/wiki/분류:인공신경망 "wikilink") [분류:자바 소프트웨어](https://ko.wikipedia.org/wiki/분류:자바_소프트웨어 "wikilink") [분류:JVM 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:JVM_프로그래밍_언어 "wikilink") [분류:자연어 처리](https://ko.wikipedia.org/wiki/분류:자연어_처리 "wikilink") [분류:자유 과학 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_과학_소프트웨어 "wikilink")

1.
2.
3.   VentureBeat|언어=en-US|확인날짜=2017-11-11}}
4.
5.
6.
7.
8.
9.
10.
11.  VentureBeat|언어=en-US|확인날짜=2017-11-12}}
12.
13.
14.
15.
16.
17.
18.
19.
20.
21. <https://www.rapidminerchina.com/en/products/shop/product/deeplearning4j/>