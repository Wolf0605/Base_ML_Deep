# Logistic Classification

**어디에 쓰이는지?**
Binary Classification ( 이진 분류 )
1. Spam Dectection : Spam(0), Ham(1) ( 일반메일과 스펨 분류 )
2. Facebook feed : Show(0) or hide(1) ( 좋아요 많이 선택한 것들 위주로 보여줌 )
3. Credit Card Fraudueltn transcation detection ( 신용카드 도난 ) : legitimate(0) / fraud(1) 돈을 다르게 쓰는걸 예측
4. Test : Fail(0), Pass(1)

## Binary Classification 할때, Linear Regression 의 문제점

<img src='https://user-images.githubusercontent.com/82213429/136650541-3ef9fae8-9888-438b-b910-763fda0a41ba.png' width='600'>

만약 위와 같이 공부 1,2,3 시간 한얘들은 탈락, 그리고 공부 5시간 한 애가 합격일때 공부 50 시간 한 애가 들어왔을때, 직선이
오른쪽으로 기울어, 공부 5시간 한 애도 합격에 못든다고 판단할 수 있다.

그래서 사람들이 생각한게 ,1과 0으로만 나눠주는 함수가 없나?? --> 있따. **Sigmoid**

<img src='https://user-images.githubusercontent.com/82213429/136650792-bd439ce4-326d-41ce-82b0-204f4a6b6efc.png' width='400'>  <img src='https://user-images.githubusercontent.com/82213429/136650747-8b487a00-96df-43d6-8c7c-847a5be9ac7f.png' width='150'>

위처럼 z 가 무한대로 커져야 1과 가깝고, 무한대로 작아지면 0과 가까워지는 합수가 **sigmoid** 함수 이다

사람들이 생각한게 기존 H(x) = WX + b 에서 WX = z 로, H(x) = g(x) 로 바꿔 본것

![image](https://user-images.githubusercontent.com/82213429/136651001-767ce2c8-d583-472f-99c3-3ca8ba5ada9f.png)

그래서 이런 함수가 나왔다.

?? 왜 W 에 transform 이 붙었을까??
