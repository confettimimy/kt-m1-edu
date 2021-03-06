# 오후 실습

데이터를 엄청 많이 주고 학습을 시켜야함

문제는 학습을 시키는데 시간이 엄청 오래 걸림 양이 너무 많아서

그럴려면 좋은 성능의 컴퓨터가 필요하고.. 개인이 사기엔 역부족

구글이 제공해주는 클라우드 기반의 구글 코랩이 있다 - 실습 진행

---

## **!!! 혼동금지**

- **학습용 데이터셋**

- **검사용 데이터셋**

​    

학습의 결과로 '모델'을 만든다.

​    

1000건이 있다면, 70~80퍼는 학습용. 

학습을 시키면서 패턴을 찾는다. 그 패턴이 모델이다.

​    

--> 학습용이랑 테스트용으로 나뉜다.

---

## ● KNN 알고리즘

상당히 많이 쓰이는 알고리즘

-KNN 알고리즘 소스코드로 실습 진행-

​    

*특히 파일 불러올 때, 구글 서버에 파일이 있는 것이 아니라 각 개인 로컬PC에 있기 때문에 다음과 같이 upload를 거쳐야 한다.

```python
#Step 2. 구글 코랩으로 파일 불러오기
from google.colab import files
myfile = files.upload()
```

---

# <지도학습 종류>

​    

## ● Decision Tree 의사결정트리 알고리즘

원리: 가장 쉬운 예는 20고개 퀴즈이다.

20개의 질문을 해서 답을 찾아내는 놀이

우리는 인공지능에게 어떤 문제에 대한 답을 물어볼 때 이런 원리를 이용한다. 

먼저 데이터를 주고 분석을 시키면 의사결정트리 알고리즘은 전체 데이터를 어떤 기준으로 나누어야하는지 검사를 하게 된다.

단점은 물어보는 질문이 많아질수록 - 즉 분류 기준이나 데이터가 많아질수록 복잡해지고 속도가 늦어진다는 단점이 있다.

​    

분류할 때는  의사결정트리를 굉장히 많이 쓴다.

​    

## --> 앙상블 기법 활용하기

의사결정나무 알고리즘은 사용하기가 편하고 결과를 해석하기도 좋아서 아주 많이 사용하는 방법이기도 한데 데이터가 많을 경우 속도도 느리고 복잡하고 훈련 데이터에만 과대 적합되는 문제가 있다. 이러한 문제를 해결하기 위해서 여러 개의 결정 트리를 만들어서 분석을 진행해 정확도를 높이는 앙상블 기법이 나왔다.

앙상블 기법안에 여러가지 알고리즘이 

---

## ● 부스팅 알고리즘

부스팅 방식: 그레이디언트 부스팅 알고리즘 / 히스토그램 기반

---

## ● 회귀(=예측) 알고리즘

1. 선형회귀 분석

   독립변수(X) 하나, 종속변수(Y) 하나

2. 다중회귀 분석

   독립변수(X) 여러 개, 종속변수(Y) 하나

보통은 선형회귀보다 다중회귀분석을 많이 이용한다.

​      

### 선형 회귀 분석

데이터 분석을 처음 시작할 때 거의 대부분 배우는 아주 기본적이면서도 아주 많이 사용되는 분석 기법이다.

이름에서 알 수 있듯이 현재 가지고 있는 데이터들을 분석해서 어떤 규칙이나 패턴을 찾은 후 그 규칙이나 패턴을 기반으로 앞으로 일어날 일을 예측을 할 때 사용하는 분석 기법이다.

ex: 철수가 일주일에 두 번씩 지각 -> 앞으로도 이러한 패턴으로 지각을 하겠지 하고 예측

실습을 해보면 기울기 하나 선이 나오는 모습을 확인할 수 있다.

### 다중 회귀 분석

실습 코드를 보면  선형회귀분석 소스코드랑 모두 똑같고, 칼럼수가 3개로 늘어난 것만 다르다는 점을 파악할 수 있다.

.

.

-여기까지 지도학습-

---

---

---

# <비지도학습>

앞에서 살펴본 지도 학습은 데이터를 분류하거나 예측할 때   학습용 데이터에 답(label)을 포함시켜 ...(끊김;;)

답을 모를 경우 데이터의 속성을 분석해서 패턴이나 구조를 찾아내는 방식으로 진행하는 분석 기법을 비지도 학습 이라고 한다.

간혹 지도학습의 분류와 비지도학습의 군집분석을 비슷하다고 오해하는 경우가 있는데, 지도학습의 경우에는 정답에 해당하는 라벨 정보에 따라서 분류를 수행하지만 비지도학습의 군집분석은 라벨 정보 없이 데이터의 속성으로 군집을 진행하므로 완전히 다른 개념이다.

​    

1. 클러스터링 알고리즘 = 군집분석
2. 주성분 분석
3. 특이값 분해
4. 독립 성분 분석
5. Autoencoders - 딥러닝 알고리즘

