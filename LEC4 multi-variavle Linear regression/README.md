## Multivariable linear regression

Multivariable 이란?? 말그대로 **다중** 예를들어서

<img src='https://user-images.githubusercontent.com/82213429/136365048-ca154758-fcc9-4702-a002-7d6080c1f090.png' width ='200'>  -->   <img src='https://user-images.githubusercontent.com/82213429/136364846-5f77d5be-fb47-4d75-89d3-5f4b2225a83f.png' width='400'>

**input 이 한개가 아니라 여러개**가 돼버린 것.

![image](https://user-images.githubusercontent.com/82213429/136365757-a1cc7079-f370-42a7-9628-a0c11764c9a4.png)

기존 H(x) = Wx + b 값에서 x가 여러개가 들어오며, 각 x 들의 가중치는 다르기 때문에

**H(x1, x2, x3) = W1x1 +W2x2 + W3x3 + b**  가 돼버림

이렇게 되면 input 이 엄청 많이들어오면 **수식이 이 한줄을 넘어버릴 만큼 길어져버림**

그래서 나온게 **Matrix**

###  Matrix?

말 그대로 Matrix ( 행렬 ) 이다.

<img src='https://user-images.githubusercontent.com/82213429/136366081-1008c5a6-0464-4245-b398-8046314e2656.png' width='700'>

위와 같이 행렬을 통해서 간단하게 식을 만들 수 있다.
그러면서 H(x) = XW 즉, X(input값들) 과 W(가중치) 의 행렬곱으로 정의된다.

하지만 만약에 행이 100개 많게는 1만개가 넘어버리면 총 1만번의 행렬곱이 필요하다.
하지만 걱정하지마라 행렬은 이걸 한번에 처리 가능하다

<img src='https://user-images.githubusercontent.com/82213429/136366750-85ed5e64-fa84-457f-8c2e-8ea0750c5001.png' width='700'>

위와같이 아무리 많은 열이와도 처리가 가능하다. **형태(shape)만 맞다면**

이후 행렬곱.설명

