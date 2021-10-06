## Linear Regression ( 선형 회귀 )

### What's Linear Regression

ex ) 공부 1시간에 10점, 공부 2시간에 20점, 공부 3시간에 30점이라면, 공부 6시간에 60점이라면
공부 9시간이면 몇점일까??

이와 같이, 일정하게 **직선으로 그래프**로 나타낼 수 있는 값을 **선형회귀** 라고 한다

![image](https://user-images.githubusercontent.com/82213429/136147442-6783bbd4-b7bc-4d8e-aa2f-833209145928.png)


## Loss

![image](https://user-images.githubusercontent.com/82213429/136147996-67fa9abb-11b1-440b-b479-47d81d3e0e48.png)
loss( cost ) function 이라고 부른다

보통 (H(x) - y)**2 을 이용한다. Why? : 차이가 많이 나는것은 더 차이가 분명하게 보이도록 , 음수와 양수를 구분없이
양수로 정의 가능
H(x) -> 그래프가 정의해준 예측값, y - > 실제값

![image](https://user-images.githubusercontent.com/82213429/136148366-e2786ffe-c0cb-4a37-aa27-66b9a176c2fc.png)

{(x1 의 편차 제곱) + (x2 의 편차 제곱) + (x3 의 편차 제곱)} / 데이터의갯수m  = loss

### Linear Regression 의 최종 목표

**loss값을 최소로 만드는 것**!!

![image](https://user-images.githubusercontent.com/82213429/136149116-010dc492-f6d1-48fd-9792-2027612b715f.png)

Wx + b 에서 **(W, b) 를 조절**하여 가장 작은 y 값( 실제값 ) 에 근접한 직선을 만드는것!

**HOW?** 이미 만들어져 있는 알고리즘을 이용하여 만들어보자

=====================================
### 두줄 요약

1. Linear Regression 은 점(실제값y) 에 최대한 근접한 직선을 긋는게 목표
2. 그러기 위해선 W(Weight), b(bias) 의 조절이 필요함 
