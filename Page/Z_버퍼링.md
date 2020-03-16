> This article is converted from Wikipedia: [Z ](https://ko.wikipedia.org/wiki/Z_).


[섬네일](https://ko.wikipedia.org/wiki/파일:Z_buffer.svg "wikilink") [컴퓨터 그래픽스에서](../Page/컴퓨터_그래픽스.md "wikilink") **Z 버퍼링**(z-buffering)은 3차원 그래픽스의 이미지 심도 좌표 관리 방식이며, 일반적으로는 [하드웨어적으로](../Page/컴퓨터_하드웨어.md "wikilink") 처리되나 이따금은 [소프트웨어로](https://ko.wikipedia.org/wiki/컴퓨터_소프트웨어 "wikilink") 처리되기도 한다. 어느 물체를 보이게 할지 말아야 할지에 대한 가시도 문제의 한 해결책으로 쓰이기도 한다. [화가 알고리즘은](../Page/화가_알고리즘.md "wikilink") 덜 효율적이긴 하나 또다른 보편적 해결책으로 쓰이고 불투명 화면 요소를 관리할 수도 있다.

어떤 물체가 그려질 때 만들어진 픽셀의 깊이 정보(z 좌표)는 버퍼(**Z 버퍼** 혹은 **깊이 버퍼**)에 저장된다. 이 버퍼는 (x-y)의 2차원 좌표를 기준으로 해당하는 각각의 스크린 픽셀 요소들로 정렬되어 있다. 만약 다른 물체가 같은 픽셀에 그려져야 할 때, Z 버퍼링은 현재 픽셀과 새로 그려질 픽셀 중 어떤 것이 관찰자에게 더 가까운지 깊이를 비교한다. Z 버퍼에 기록되도록 새로 선택된 깊이는 이전의 깊이를 덮어쓴다. 즉, Z 버퍼는 더 '가까운 물체가 더 먼 물체를 가린다' 라는 직관적 깊이 관념을 정확하게 따를 수 있게 돕는다. 이 방식을 **Z 컬링**이라고 부른다.

Z 버퍼의 정밀도는 씬의 품질에 큰 영향을 미친다. [16비트](../Page/16비트.md "wikilink")의 Z 버퍼는 두 물체가 매우 가까울 때 "[Z 파이팅](https://ko.wikipedia.org/wiki/Z_파이팅 "wikilink")" 혹은 **스티칭**이라고 하는 현상을 일으킬 수 있다. [24비트](https://ko.wikipedia.org/wiki/24비트 "wikilink") 혹은 [32비트](../Page/32비트.md "wikilink")의 Z 버퍼는 더 나은 결과를 보여주지만 추가적인 알고리즘 없이는 이 문제를 완전히 해결할 수 없다. [8비트](../Page/8비트.md "wikilink")의 Z 버퍼 알고리즘은 매우 낮은 정밀도로 거의 사용되지 않는다.

## 용도

Z 버퍼는 컴퓨터 게임과 같은 3D 그래픽스가 구동되는 현대 거의 모든 컴퓨터, 노트북, 모바일 기기에 사용된다. Z 버퍼는 규소 칩(집적 회로)에 하드웨어로서 구현되어 있다. 하드웨어가 아닌 소프트웨어적으로 구현된 Z 버퍼는 영화에 컴퓨터로 만들어진 특수 효과를 만들어내는 데에도 사용된다.

또한 Z 버퍼의 정보는 빛을 기준으로 렌더링된 정보로부터 [섀도 매핑](https://ko.wikipedia.org/wiki/섀도_매핑 "wikilink")(shadow mapping)을 이용한 그림자 생성을 가능하게 한다.

## 발전

정밀도가 조금만 줄어들더라도 Z 버퍼의 거리 정보가 균일하게 퍼져있지 않고 조밀한 경우에 씬의 품질에 문제가 발생할 수 있다. 거리가 가까울수록 거리가 먼 값보다 더 정밀하고, 따라서 가까이에 존재하는 물체가 더 잘 그려진다. 일반적으로 이 현상은 바람직하지만 가끔 물체가 더 멀리 있는 것처럼 보이게 한다. 더 균일한 정밀도를 위해 고안된 Z 버퍼링의 응용은 W 버퍼링이라고 불린다.

씬을 그리기 전에 먼저 Z 버퍼는 보통 1.0으로 초기화될 필요가 있다. 왜냐하면 이 수치가 0.0부터 최대 1.0까지의 깊이 값으로 정의되기 때문이다. 즉, [뷰 프러스텀](https://ko.wikipedia.org/wiki/뷰_프러스텀 "wikilink") 내에 이 수치를 벗어나는 물체는 존재할 수 없다.

Z 버퍼의 개발에는 [에드윈 캣멀이](https://ko.wikipedia.org/wiki/에드윈_캣멀 "wikilink") 가장 많은 기여를 했지만, Wolfgang Straßer가 1974년에 이미 이 기법을 고안해냈다.

최신(1995-2005) 그래픽 카드에서, Z 버퍼는 메모리 대역폭을 상당히 많이 사용한다. Z 버퍼링의 동작 비용을 줄이기 위해 다양한 기법들이 개발되어 왔다. 예를 들면 [무손실 압축](https://ko.wikipedia.org/wiki/무손실_압축 "wikilink")(메모리 대역폭을 더 사용하는 것보다 리소스를 압축, 압축 해제하는 편이 비용이 덜 든다)과 간단하게 한 프레임은 양수, 다음 프레임은 음수로 사용하는 트릭(부호를 가진 숫자로 깊이값을 교묘하게 체크해서 프레임 사이의 Z 값 초기화를 건너 뛸 수 있다)으로 굉장히 빠르게 하드웨어의 Z값을 초기화할 수 있는 방법이 그것이다.

## Z 컬링

Z 컬링은 깊이 정보에 기반하여 픽셀을 일찍 제거해, 가려진 면을 렌더링 할 때 드는 비용을 줄여 성능 향상을 가져올 수 있는 기법이다. 픽셀에 기록된 깊이가 물체의 깊이와 비교되어 물체가 가려지는지 아닌지 자연스럽게 알 수 있기 때문에 Z 버퍼링을 수행할 때에 당연하게 따라오는 결과이다.

Z 버퍼를 사용하면, 픽셀의 깊이를 통해서 그려져야 할지 아닐지를 알 수 있으므로 조명 계산이나 텍스쳐링과 같은 모든 과정을 건너 뛸 수 있을지 판단 할 수 있다. 또한, 컬링된 픽셀에 대해서는 오래걸리는 픽셀 셰이더 계산 또한 건너 뛸 수 있다. 따라서 Z 컬링은 [fillrate](https://ko.wikipedia.org/wiki/fillrate "wikilink")(필 레이트), 조명 연산, 텍스쳐링 혹은 픽셀 셰이더가 주된 [병목](../Page/병목.md "wikilink")일 경우에 성능을 향상시킬 수 있는 좋은 해결책이 될 수 있다.

Z 버퍼링이 정렬되지 않은 모델들을 그릴 때, [화가 알고리즘을](../Page/화가_알고리즘.md "wikilink") 거꾸로 사용하여 뎁스의 오름차순으로 폴리곤들을 정렬하는 것은 각 스크린 픽셀이 더 적은 횟수로 그려지도록 유도할 수 있다. 이것은 필 레이트가 제한적인 씬을 많은 overdraw를 통해 그려야 할 때 성능 향상을 가져온다.하지만 Z 버퍼링과 함께 사용하지 않을 때 다음과 같은 많은 문제를 겪을 수 있다:

  - 폴리곤의 가려짐이 서로 순환하는 현상이 발생할 수 있다 (예를 들어 A가 B를 가리고 B가 C를 가리는데 C가 A를 가린다)
  - 삼각형 간에 언제나 "가장 가까운" 지점이란 존재하지 않는다 (예를 들어 누군가가 삼각형의 중심이나 가장 가까운 지점, 혹은 가장 먼 지점을 기준으로 삼각형을 정렬하더라도, 다른 이는 그 두 개의 삼각형 중 A가 더 가깝더라도 실제로 B가 먼저 그려진다는 것을 알게 될 것이다.)

따라서, 화가 알고리즘을 거꾸로 사용하는 방법은 많은 리엔지니어링 없이는 Z 컬링 대신 사용될 수 없으며 Z 컬링의 최적화하는 데만 사용될 수 있다. 예를 들어 x/y 위치와 z 깊이를 통해 폴리곤이 나뉘어져 경계선이 생기고, 이로써 두 개의 폴리곤이 서로 겹칠지 아닐지에 대해서 빠르게 결정하도록 도울 수 있다.

## 수학

렌더링될 카메라 공간에서 깊이값의 범위는 보통 \(\mathit{near}\) 와 \(\mathit{far}\) 사이의 \(z\) 값으로 정의된다. perspective(원근) 투영을 거친 후 \(z\), 혹은 \(z'\)값은 다음과 같이 정의된다:

\(z'=
\frac{\mathit{far}+\mathit{near}}{\mathit{far}-\mathit{near}} +
\frac{1}{z} \left(\frac{-2 \cdot \mathit{far} \cdot \mathit{near}}{\mathit{far}-\mathit{near}}\right)\)

orthographic(직교) 투영을 거친후 \(z\), 혹은 \(z'\)값은 다음과 같이 정의된다:

\(z'=
2 \cdot \frac{{z} - \mathit{near}}{\mathit{far}-\mathit{near}} - 1\)

Z값이 카메라 공간에서 새로운 Z값보다 더 과거의 값일 경우 가끔씩 \(w\) 혹은 \(w'\)로 쓰인다.

\(z'\)값은 보통 -1의 \(\mathit{near}\) [plane과](https://ko.wikipedia.org/wiki/plane_\(mathematics\) "wikilink") 1의 \(\mathit{far}\) plane 사이의 -1에서 1 사이의 값으로 정규화된다. 이 범위 밖의 값은 [뷰 프러스텀](https://ko.wikipedia.org/wiki/뷰_프러스텀 "wikilink") 내에 존재하지 않고, 그려지지 않는다

### 고정소수점(fixed point) 표현

이러한 값들은 일반적으로 [고정소수점](https://ko.wikipedia.org/wiki/고정소수점 "wikilink") 형태로 하드웨어 그래픽 가속기의 Z 버퍼에 저장된다. 먼저 다음과 같은 식 :

\(z'=
\frac{\mathit{far}+\mathit{near}}{2 \cdot \left( \mathit{far}-\mathit{near} \right) } +
\frac{1}{z} \left(\frac{-\mathit{far} \cdot \mathit{near}}{\mathit{far}-\mathit{near}}\right) +
\frac{1}{2}\)

을 통해서 \(z'_2 = \frac{\left(z'_1+1\right)}{2}\)와 같은 형태로 \[0,1\]의 범위 내의 적절한 값으로 정규화된다.

그 다음, 상단의 공식은 \(S=2^d-1\) 와 같이 곱해진 후 반올림되어 정수로 표현된다. d는 Z 버퍼의 깊이로, 일반적으로 16, 24, 32 비트로 표현된다 :\[1\]

\(z'=f\left(z\right)=\left\lfloor  \left(2^d-1\right) \cdot \left(
\frac{\mathit{far}+\mathit{near}}{2 \cdot \left( \mathit{far}-\mathit{near} \right) } +
\frac{1}{z} \left(\frac{-\mathit{far} \cdot \mathit{near}}{\mathit{far}-\mathit{near}}\right) +
\frac{1}{2} \right) \right\rfloor\)

이 공식은 Z 버퍼 해상도를 계산하기 위해 다음과 같이 파생되어 변환될 수 있다. (앞서 말한 정밀도가 이것이다) 상단 \(f\left(z\right)\)의 역함수로:

\(z=
\frac{- \mathit{far} \cdot \mathit{near}}{\frac{z'}{S}\left(\mathit{far} - \mathit{near}\right) - {far}}
=
\frac{- \mathit S  \cdot {far} \cdot \mathit{near}}{z'\left(\mathit{far} - \mathit{near}\right) - {far} \cdot S }\)

where \(S=2^d-1\)

카메라 스페이스의 관점에서 Z 버퍼의 해상도는 정수가 저장되는 Z 버퍼 상에서 작은 값이 점진적으로 변하는(1 혹은 -1) 증분의(incremental) 양상을 가진다. 따라서 해상도 값은 \(z'\)의 식에서 \(z\)로 유도될 수 있다:

\(\frac{dz}{dz'}=
\frac{-1 \cdot -1 \cdot \mathit S  \cdot {far} \cdot \mathit{near}}
     {\left( z'\left(\mathit{far} - \mathit{near}\right) - {far} \cdot S \right)^2}
\cdot \left(\mathit{far} - \mathit{near}\right)\)

카메라 스페이스 관점에서 상단의 \(f\left(z\right)\)를 \(z'\)로 대체해 표현하면:

\(\frac{dz}{dz'}=
\frac{-1 \cdot -1 \cdot \mathit S  \cdot {far} \cdot \mathit{near} \cdot \left(\mathit{far} - \mathit{near}\right)}
     {\left( \mathit S  \cdot \left(\frac{-\mathit{far} \cdot \mathit{near}}{z} + \mathit{far}\right) - {far} \cdot S \right)^2} =\)

\(\frac{ \left(\mathit{far} - \mathit{near}\right) \cdot z^2 }{ S \cdot \mathit{far} \cdot \mathit{near} }=\)

\(\frac{z^2}{S \cdot \mathit{near}}-\frac{z^2}{S \cdot \mathit{far} }=\)

\~ \(\frac{z^2}{S \cdot \mathit{near}}\)

이 식은 \(z'\)값이 \(\mathit{near}\) 플레인 근처에서 더 조밀하게 모여있는 값을 가진다는 것을 보여준다. 그래서 카메라에 더 가까운 값일수록 더 정밀한 결과를 보여준다. \(\mathit{near}/\mathit{far}\) 비율이 작을수록, 멀어짐에 따른 정확도는 더 낮아진다. 그래서 \(near\) 플레인을 너무 가깝게 설정하는 것은 가까운 물체들에 대해서도 바람직하지 못한 렌더링 결과를 보여준다. 따라서 \(near\) 플레인은 카메라에 가깝게 설정하는 것 보다, 목표 물체의 Z 값의 적절한 정밀도를 위하여 물체에 가깝도록 설정하는 편이 좋다.\[2\]

## 같이 보기

  - [에드윈 캣멀](https://ko.wikipedia.org/wiki/에드윈_캣멀 "wikilink") - Z 버퍼링의 창시자
  - [3D 컴퓨터 그래픽스](https://ko.wikipedia.org/wiki/3D_컴퓨터_그래픽스 "wikilink")
  - [깊이 지도](https://ko.wikipedia.org/wiki/깊이_지도 "wikilink")

## 각주

## 외부 링크

  - [Learning to Love your Z-buffer](http://www.sjbaker.org/steve/omniv/love_your_z_buffer.html)

  - [Alpha-blending and the Z-buffer](http://www.sjbaker.org/steve/omniv/alpha_sorting.html)

[분류:3차원 렌더링](https://ko.wikipedia.org/wiki/분류:3차원_렌더링 "wikilink")

1.
2.