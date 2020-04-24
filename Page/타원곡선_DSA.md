> This article is converted from Wikipedia: [타원곡선 DSA](https://ko.wikipedia.org/wiki/타원곡선_DSA).


**타원곡선 DSA**(Elliptic Curve Digital Signature Algorithm, ECDSA)는 타원곡선을 이용한 전자서명 알고리즘이다.

## 정의역 매개변수

  - 모두 정의역 매개변수(domain parameter)로 (CURVE, g, n) 을 사용하기로 합의한다.
      - CURVE : 타원곡선 체(field)와 여기에 사용된 수식이다.
      - g : 타원곡선의 기준점(base point)이다. 해당 타원곡선의 생성원(generator)이다.
      - n : g의 차수이다. n X g = 0 이며, 반드시 소수이어야 한다. 보통 충분히 큰 소수를 사용한다.

## 절차

앨리스는 키쌍\((d_A,Q_A)\)를 만든다.

  - d는 무작위로 선택된 1부터 n-1사이의 정수로서, 개인키이다.
  - Q는 Q=dg를 만족하는 정수로서, 공개키이다.

### 서명

  - 앨리스가 메시지m을 다음 절차를 따라 서명한다.
    1.  e=H(m)이고, H는 암호학적 해쉬함수이다.
    2.  z는 e의 이진 값에서 왼쪽으로부터 \(L_n\)번째 까지를 잘라낸 값(\(L_n\)leftmost bits of e)이다.  \(L_n\)는 n의 비트 길이(bit length)이다.
    3.  암호학적으로 안전한 난수 k를 \[1, n-1\] 사이에서 무작위로 선택한다.
    4.  곡선 위의 점 \((x_1,y_1)=k*g\)를 계산한다.
    5.  \(r=x_1 \pmod{n}\)을 계산한다. 만약 r=0이면 3으로 되돌아가 다른 k를 다시 선택하여 순서대로 진행한다.
    6.  \(s=k^{-1}(z+rd_A) \pmod{n}\)을 계산한다. 만약 s=0이면 3으로 되돌아가 다른 k를 다시 선택하여 순서대로 진행한다.
  - 완성된 서명은 (r, s)이다.

### 검증

밥이 앨리스의 서명을 인증하려면, 앨리스의 공개키를 미리 알아야 한다.

#### 곡선 위의 점 인증

  - \(Q_A \neq O(identity \ element)\)인지 확인한다.
  - \(Q_A\)가 곡선 위의 점(curve point)인지 확인한다.
  - \(n \times Q_A=O\)인지 확인한다.

#### 서명 유효성 인증

  - r,s가 1부터 n-1사이의 정수인지 확인한다. 아니면 서명은 무효이다.
  - e=H(m)을 계산한다. H는 앨리스가 서명 생성에 썼던 해쉬함수이다.
  - z는 e의 이진 값에서 왼쪽으로부터 \(L_n\)번째 까지를 잘라낸 값이다.
  - \(w=s^{-1} \pmod{n}\)을 계산한 다음, \(u_1=zw,\ u_2=rw \pmod{n}\)를 계산한다.
  - Shamir’s trick을 사용해서\((x_1,y_1)=u_1 \times g +u_2 \times Q_A\)을 계산한다. 만약 \((x_1,y_1)= O\)이면 서명은 무효이다.
  - \(r \equiv x_1 \pmod{n}\)일때만 유효하다. 아니면 모두 무효이다.

[분류:암호학](https://ko.wikipedia.org/wiki/분류:암호학 "wikilink")