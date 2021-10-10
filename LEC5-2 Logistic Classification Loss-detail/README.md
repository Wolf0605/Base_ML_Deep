# Logistic Regression 의 loss function

<img src='https://user-images.githubusercontent.com/82213429/136689972-f983da3b-5a2a-424c-a0c4-ce3305ebb0cc.png' width='700'>

위와 같이 **Linear regression의 H(x) (예측값) 는 왼쪽처럼 H(x)= Wx + b 의 형태로 직선**을 가지고 있어서 그 loss fucntion 은 직선을 제곱한 곡선이 돼서** 밥그릇 모양** 처럼 나오게된다.

하지만 **Logistic classification 에서 H(x)는 시그모이드(sigmoid)의 형태** 를 취하고 있어서 Loss function은 그래프처럼 **꾸불꾸불한 밥그릇(?)** 모양이 나오게 된다.

그렇기 때문에 **loss='mse'** 를 쓴다고 했을 떄, H(x) = Wx + b 와 달리 **시작점에 따라 다르게 minimum 측정하여 global minimum 을 찾기 어렵다.**

## 그래서 cost function 을 바꿔야한다.

**How??**

<img src='https://user-images.githubusercontent.com/82213429/136690706-ca49268e-2e3b-4d87-84ea-635a9dae83c2.png' width='700'>

**아이디어는 1 / (1+e^-z)** 에서 가져왔다. 저거 때문에 그래프가 꾸불꾸불 밥그릇 모양이 나왔는데, **저걸 어떻게하면 좀 이쁘게 만들까??**

y = e^x 는 **log 로 풀었따** 우리가 푸는거는 **Binary Classification** 이다. 그래서 **y = 0 or 1** 이면 된다는 말이다. 이제 그래프를 한번 봐보자

위의 로그식(Loss fucntion)을 그래프로 그려보면은 왼쪽( **실제값(y) = 1 일때** )은 H(x) = 1 일때 Loss(H(x) = 1) = 0 이 되고 H(x) = 0 일때, Loss(0) 은 한없이 무한대로 가까워진다.

반대로 오른쪽( **실제값(y) = 0** ) 로그식은 H(x) = 0 일때 Loss(0) = 0 이 되고, H(x) = 1 일때 Loss(1) 은 무한대로 가까워진다.

즉, 기계가 학습할 때  만약 예측을 잘못해서 y = 1 인데 H(x) = 0으로 예측한다고 하면은 Loss function 은 엄청 큰 loss 값을 얻고 이를 잘못됐다고 인식한다.

그리고 위의 **두 그래프를 합치면** 원래 H(x) = W + b 일떄의 **밥그릇 형태가 되어** Loss fucntion 으로  **loss='mse'** 를 **다시 쓸 수 있게 된다.** 


<img src='https://user-images.githubusercontent.com/82213429/136690653-6d9438bd-218f-43e1-ae12-844ad2563a20.png' width='700'>

위의 식은 앞에서 봤던 **-log(H(x)) 와 -log(1-H(x)) 를 합쳐 놓은 것** 이다.

<img src='https://user-images.githubusercontent.com/82213429/136691224-7f720e3f-0e55-448f-a240-f9ea1e349d86.png' width='400'>

우리가 Linear Regression 에서 Loss(W)을 미분하여 그 기울기( Loss(W)미분한 것 )를 갱신하면서 **기울기가 Minimum 까지 간 것과 똑같다**. 여기서 a(알파) 는 learning_rate 로 몇칸씩
얼마나 내려갈 것인가를 말하는 것. learning_rate 에 따라 학습이 효율적일 수도 아닐 수도 그리고 아예 학습을 제대로 못할 수도 있다.

<img src='https://user-images.githubusercontent.com/82213429/136691474-5196e44f-e8f2-48fe-a2b2-9e550f048264.png' width='300'>  <img src='https://user-images.githubusercontent.com/82213429/136691415-5c49ea8c-d3d3-40ca-a42e-58a027f140d0.png' width='500'>





