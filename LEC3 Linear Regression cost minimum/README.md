## What cost(W) looks like ?? 
In Linear Regression b = 0 이라면, H(x) = Wx 로 간단하게 봐보자

![image](https://user-images.githubusercontent.com/82213429/136304037-7bda6efe-33b8-4af5-a377-f4da418b2b07.png)

위와 같이 Linear Regression 에서 H(x) = Wx 에서 cost 함수는 2차 그래프를 그리게 된다

![image](https://user-images.githubusercontent.com/82213429/136303927-ac8aee57-9908-41f1-9f6e-0b90e857f756.png)

우리의 **목표는 minimize cost** 를 구하는거다.

### How can we do this ??
**Gradient descent algorithm( 경사 하강법 )** 으로 해결 가능하다.

경사하강법이란 무엇인가 ?? 

**미분**을 통해 그래프의 기울기가 0에 가장 가까운 곳을 찾아줌

경사하강법의 **의의**
+ Minimize cost funcstion
+ Gradient descent is used many minimization problems ( 가장 일반적임 )
+ 주어진 cost function 에서,cost(W,b)에서 가장 cost 가 작아지는 W, b  값을 찾아낸다

### How?? 어떻게 경사하강법이 minimize cost 를 구할 수 있나?
**미분** 을 이용 ( 그 점의 기울기를 이용 )
![image](https://user-images.githubusercontent.com/82213429/136305873-8fa1d241-3fb2-419c-9453-ef89a84f9b3e.png)

알파(learning rate)라는 값에 cost(W) 함수를 미분한것(그 점의 기울기)을 곱해줘서 현재있는 W 값에서 빼주는 것.

여기서 cost(W)의 미분값(기울기)은, 0에 가장 가까운 값으로 가기위해 W를 계속 조정한다.

( 이후 이것을 순전파를통해 손실함수(cost(W)) 를 계산하고 배치 내 데이터에 대한 손실함수 를 모두 더하고... 역전파를 통해서 값을갱신....)
위에건 나중에 알아보자!


위와 같이 미분을 통하여, W, b 를 업데이트 시켜주고 이후 cost= 0 에 가장 가까운 최적의 값을 찾는데 도와준다 ( b 도 비슷한 방법으로 갱신한다 )

이 W, b 를 어떻게 업데이트 계속 해주냐??
( 순전파를통해 손실함수(cost(W)) 를 계산하고 배치 내 데이터에 대한 손실함수 를 모두 더하고... 역전파를 통해서 값을갱신....)

**위에건 나중에 알아보자!**
이거는 이후, 순전파, 역전파를 공부하면서 한번 알아보도록 하자.

### 언제 gradient descent 를 쓸 수 있을까??

아래 그림처럼 loss function이 처음시작점에 따라 W, b가 달라지면 사용하기 어렵다.

![image](https://user-images.githubusercontent.com/82213429/136306967-e288dc9c-df1b-4e9b-a196-a436300e155c.png)

올바른예시 : 아래처럼 어느점에서 시작하든 일정한 값으로 떨어지면, 알고리즘(gradient descent)을 실행할 수 있다.
(Ex. Linear regression 의 convex fucntion)
그래서 항상 loss fucntion 을 설계할 떄 모양이 convex fucntion 이 되는지 확인을 해줘야한다.

![image](https://user-images.githubusercontent.com/82213429/136307144-6aad68f6-eae6-4b26-ac36-1e699b0be5a8.png)


### 세줄요약
1. loss(W) 값을 어떻게 하면 가장 작게 만들 수 있을까?? - > 경사하강법 (gradient desecent)
2. 경사하강법이란 loss(W)를 미분하여 W값을 계속 업데이트하여 미분한 값을 가장 작게 만들어 주기 위한것
3. 경사하강법을 사용하기 전에 loss fucntion 이 시작점이 어디든 도착하는 W, b 가 같은지 확인해 줘야한다( convex fucntion 인지 확인 )
