> This article is converted from Wikipedia: [PyTorch](https://ko.wikipedia.org/wiki/PyTorch).


**PyTorch**는 Python을 위한 오픈소스 머신 러닝 라이브러리이다. Torch를 기반으로 하며\[1\]\[2\]\[3\], 자연어 처리와 같은 애플리케이션을 위해 사용된다.\[4\] GPU사용이 가능하기 때문에 속도가 상당히 빠르다. 아직까지는 Tensorflow의 사용자가 많지만, 비직관적인 구조와 난이도 때문에, Pytorch의 사용자가 늘어나고 있는 추세이다. 이는 Facebook의 인공지능 연구팀이 개발했으며, Uber의 “Pyro”(확률론적 프로그래밍 언어)소프트웨어가 Pytorch를 기반으로 한다

Pytorch는 두 개의 높은 수준의 파이선 패키지 형태로 제공한다.\[5\]

1.  강력한 GPU가속화를 통한 Tensor계산 ex) NumPy
2.  테이프 기반 자동 삭제 시스템을 기반으로 구축된 심층 신경망

Facebook은 PyTorch와 Convolutional Architecture for Fast Feature Embedding (Caffe2)을 모두 운영하고 있지만 비호환성으로 인해 PyTorch 정의 모델을 Caffe2로 변환하거나 그 반대로 변환하는 것이 어렵다. 개신경망 교환([ONNX, Open Neural Network Exchange](https://github.com/onnx/onnx)) 프로젝트는 Facebook과 Microsoft가 프레임워크 간 모델 전환을 위해 2017년 9월 만든 프로젝트다. Caffe2는 2018년 3월 말에 PyTorch으로 합병되었다.

## PyTorch Tensors

프로그래밍의 영역에서 Tensors는 단순히 다차원 배열로써 간주될 수 있다. Pytorch에서의 Tensors는 [NumPy](../Page/NumPy.md "wikilink")의 배열과 비슷한데, 추가로 Tensors도 CUDA를 지원하는 GPU에 사용할 수 있다. 또한, Pytorch는 다양한 타입의 Tensors를 지원한다.

## 모듈

### 자동 미분 모듈

PyTorch는 자동 미분이라는 기법을 사용한다. 레코더는 수행한 작업을 기록한 다음 거꾸로 재생하여 경사를 계산한다. 이 기술은 전방 패스에서 매개 변수의 미분을 계산하여 한 시대에서 시간을 절약하기 위해 신경 네트워크를 구축할 때 특히 강력하다.

### 최적화 모듈

torch.optim은 신경 네트워크를 구축하는 데 사용되는 다양한 최적화 알고리즘을 구현하는 모듈이다. 일반적으로 사용되는 대부분의 방법은 이미 지원되므로 처음부터 새로 만들 필요가 없다.

### nn 모듈

autograd 모듈을 사용하면 계산 그래프를 쉽게 정의하고 구배를 얻을 수 있지만, 원시 자동 그립은 복잡한 신경 네트워크를 정의하기에는 autograd 모듈을 직접 쓰기에는 너무 저수준의 작업이 될 것이다. 여기서 nn모듈이 도움이 된다.

## Tensorflow와의 비교\[6\]

| 구분        | Tensorflow              | PyTorch                   |
| --------- | ----------------------- | ------------------------- |
| 패러다임      | Define and Run          | Define by Run             |
| 그래프 형태    | Static graph(정적)        | Dynamic graph(동적)         |
| 현재 사용자    | 많음                      | 적음                        |
| 자체 운영 포럼  | 없음                      | 있음                        |
| 한국 사용자 모임 | Tensorflow Korea(TF-KR) | Pytorch Korea(Pytorch-KR) |

### 딥러닝 구현 라이브러리, 파이토치

파이토치는 파이썬 기반의 오픈 소스 머신러닝 라이브러리로, 페이스북 인공지능 연구집단에 의해 개발되었다. 간결하고 구현이 빨리되며, 텐서플로우보다 사용자가 익히기 훨씬 쉽다는 특징이 있다. 또한 코드를 직접 다룬다 사람들에게 설명해 주기에도 효과적이다.

텐서플로우와 Pytorch의 가장 큰 차이점은 딥러닝을 구현하는 패러다임이 다르다는 것이다. 텐서플로우는 Define-and-Run 프레임워크인 반면에, Pytorch는 Define-by-Run이다.

Define and Run는코드를 직접 돌리는 환경인 세션을 만들고, placeholder를 선언하고 이것으로 계산 그래프를 만들고(Define), 코드를 실행하는 시점에 데이터를 넣어 실행하는(Run) 방식. 이는 계산 그래프를 명확히 보여주면서 실행시점에 데이터만 바꿔줘도 되는 유연함을 장점으로 갖지만, 그 자체로 비직관적이다. 그래서 딥러닝 프레임워크 중 난이도가 가장 높은 편이다.

Pytorch는 언어 자체에 대한 어려움은 없다. 일반적인 파이썬 코딩과 비슷하기 때문이다. 선언과 동시에 데이터를 집어넣고 세션도 필요없이 돌리면 끝이다. 덕분에 코드가 간결하고 난이도가 낮은 편이다.사용자가 아직 적어 구글링으로 공부하기 힘든 환경에 있지만 이는 시간이 해결해 줄 문제이다.

이 패러다임의 차이로 텐서플로우의 경우 먼저 모델을 만들고 값을 다 따로 넣어주어야 해서 직관적이지 않지만, Pytorch의 경우 간단하고 직관적이다.

두 프레임워크 모두 계산 그래프를 정의하고 자동으로 그래디언트를 계산하는 기능이 있다. 하지만 Tensorflow의 계산 그래프는 정적이고 Pytorch는 동적이다. 즉 tensorflow에서는 계산 그래프를 한 번 정의하고 나면 그래프에 들어가는 입력 데이터만 다르게 할 수 있을 뿐 같은 그래프만을 실행할 수 있다. 하지만 PyTorch는 각 순전파마다 새로운 계산 그래프를 정의하여 이용한다.

## PyTorch의 장점

1.  설치가 간편하다.
2.  이해와 디버깅이 쉬운 직관적이고 간결한 코드로 구성되었다.
3.  Define by Run 방식을 기반으로 한 실시간 결과값을 시각화 한다.
4.  파이썬 라이브러리(Numpy, Scipy, Cython)와 높은 호환성을 가진다.
5.  Winograd Convolution Alogithm 기본 적용을 통한 빠른 모델 훈련이 가능하다.
6.  모델 그래프를 만들 때 고정상태가 아니기 때문에 언제든지 데이터에 따라 조절이 가능하다(유연성).
7.  Numpy스러운 Tensor연산이 GPU로도 가능하다.
8.  자동 미분 시스템을 이용해 쉽게 DDN(DataDirect Networks을 짤 수 있다.
9.  학습 및 추론 속도가 빠르고 다루기 쉽다.

## PyTorch 패키지\[7\]

<table>
<thead>
<tr class="header">
<th><p>패키지</p></th>
<th><p>기술</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>torch</p></td>
<td><p>강력한 GPU 지원 기능을 갖춘 Numpy와 같은 라이브러리</p></td>
</tr>
<tr class="even">
<td><p>torch.autograd</p></td>
<td><p>Torch에서 모든 차별화된 Tensor 작업을 지원하는 테이프 기반 자동 미분화 라이브러리</p></td>
</tr>
<tr class="odd">
<td><p>torch.optim</p></td>
<td><p>SGD, RMSProp, LBFGS, Adam 등과 같은 표준 최적화 방법으로 torch.nn과 함께 사용되는 최적화 패키지</p></td>
</tr>
<tr class="even">
<td><p>torch.nn</p></td>
<td><p>최고의 유연성을 위해 설계된 자동 그래프와 깊이 통합된 신경 네트워크 라이브러리</p></td>
</tr>
<tr class="odd">
<td><p>torch.legacy(.nn/optim)</p></td>
<td><p>이전 버전과의 호환성을 위해 Torch에서 이식된 레거시 코드</p></td>
</tr>
<tr class="even">
<td><p>torch.utils</p></td>
<td><p>편의를 위해 DataLoader, Trainer 및 기타 유틸리티 기능</p></td>
</tr>
<tr class="odd">
<td><p>torch.multiprocessing</p></td>
<td><p>파이썬 멀티 프로세싱을 지원하지만, 프로세스 전반에 걸쳐 Torch Tensors의 마법같은 메모리 공유 기능을 제공.</p>
<p>데이터 로딩 및 호그 워트 훈련에 유용</p></td>
</tr>
</tbody>
</table>

## 각주

## 외부 링크

  -
  - [PyTorch 튜토리얼 (한국어)](https://tutorials.pytorch.kr) - (비공식) 한국어 튜토리얼 번역 사이트

[분류:딥 러닝](https://ko.wikipedia.org/wiki/분류:딥_러닝 "wikilink") [분류:C로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:C로_작성된_자유_소프트웨어 "wikilink") [분류:파이썬으로 작성된 자유 소프트웨어](https://ko.wikipedia.org/wiki/분류:파이썬으로_작성된_자유_소프트웨어 "wikilink") [분류:BSD 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:BSD_라이선스_소프트웨어 "wikilink") [분류:자유 과학 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_과학_소프트웨어 "wikilink")

1.
2.
3.
4.
5.
6.
7.