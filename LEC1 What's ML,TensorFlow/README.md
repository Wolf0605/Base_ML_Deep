## What's Machine learning??

기존의 프로그래밍 - > 정확한 명령을 받으면 그것대로만 출력이 나옴

```python
input = input()
if input == '안녕'
  print(f'{input}하세요')
```
와 같이 정해진 입력을 입력했을 떄 출력이 되는 형식 - >  Explicic programming

**문제점 예시**
1. Spam filter : Many rules ( 번호가 너무 많음 )
2. Automatic driving : Too many rules ( 처리해야할 정보가 너무 많음 )

이와 같은 문제점을 해결하고자 나온게 **머신러닝** ( 학습을 하자 !! )

### Supervised / Unsupervised learning ( 지도 / 비지도 학습 )

**Supervised learning** :  기존으로 가졌던 데이터를 바탕으로 하는 학습. 레이블이 담겨있는 ( 정답이 있는 ) 자료를 바탕으로 학습

![image](https://user-images.githubusercontent.com/82213429/136028234-ccbfca2c-34ea-4aa8-8eaf-97fb931e10c7.png)

위와 같이 고양이 사진1 = 고양이, 고양이 사진 2 = 고양이, 강아지 사진 1 = 강아지 .... 이렇게 답을 미리 알려준다.

**Unsupervise learning** : un-labeled data ( 비지도 학습 - 언라벨 데이터 )
ex ) Google news grouping ( 비슷한것들을 묶어주는 것 )

### Most common problem type in ML(Supervised learning)
= Image labeling : learning from tagged images
= Email spam filter : learning from labeled ( spam or not ) email
= Predicting exam score : learning from previous exam score and time spent


### Types of supervised learning
EX 
+ regression ( 선형 )
 >  Predicting final exam score based on time spent
+ binary calssfiaction ( 이진 분류 )
 >  Pass/ non-pass based on time spent
+ multi-label calssification ( 다중 분류 )
 >  Letter grade ( A,B,C,E and F ) based on time spent

### TensorFlow

데이터들( Array 들 ) - tensor
날아다니다 - flow
**기본구조**
![image](https://user-images.githubusercontent.com/82213429/136031607-29936741-acc7-424c-ab99-c53a97f9dc7b.png)

1. 그래프를 Build ( 그래프를 정의 ) - Placeholder 로 만들 수 있음.
+ Place 홀드란 ?
+ 미리 입력된 값이 아닌, 이후에 입력 가능한 값 ex) a=3, b=3 에서 a+b 를 실행하는게 아니라 a,b 값을 그떄 집어넣어서 실행 
3. 그래프를 실행
4. 그로인해 값이 업데이트되거나 return 됨

**Tensor Rank, Shapes, Type**
![image](https://user-images.githubusercontent.com/82213429/136032362-45157d3a-665a-4f14-9612-9721f89a81a2.png)

### 세줄요약
1. 미리 받은 데이터를 바탕으로 값을 출력해 내는걸 머신러닝이라고 함
2. 종류는 지도, 비지도 학습이 있고 지도학습 종류엔 선형,이진,다중 분류 3개가 있음
3. 텐서플로우는 수많은 데이터가 날아다니는 다는 의미

