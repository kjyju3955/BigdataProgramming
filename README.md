Causes of Happy 💞
===
---

### 1. Subject

<img width="548" alt="image" src="https://user-images.githubusercontent.com/55525705/147640797-107ac9af-954e-46ba-9ade-87b90c18c45a.png">

경제적 수준이 높다고 행복한 것은 아님 <br>

사람들의 행복도에 영향을 주는 요인을 파악해보고자 함. 
다양한 feature들을 이용해서 분석을 진행하고 이를 해석해 보는 과정을 통하여 결과를 이끌어 냄. <br>
또한, 우울증에 영향을 주는 요인을 파악해보고 더 나아가 자살율까지 분석을 진행해보며 행복도와의 관계를 파악해보는 과정을 통해서 이 둘을 극복할 수 있는 요소를 파악하고자 함 <br>
(자살율의 추가 이유 : 아시아 지역이 우울증으로 병원에 찾아가는 경우가 다른 지역에 비해서 적어 제대로된 데이터가 아닐 가능성이 존재)

---
### 2. Data
다양한 성향을 가진 주들이 존재하고 원하는 모든 데이터를 얻을 수 있는 **OECD국가** 별 데이터 사용. 

feature name|contents|reference
:---:|:---:|:---:
Happiness_score|각 국가의 행복도 점수|
Pertentage_change_PIR|PIR(사람들이 집을 사는데 평균적으로 필요한 년수/소득 대비 주택 가격의 비율)의 변화 %|
Real_house_price|집 값|
Safety|해당 국가의 안전도|
Elderly_popul|65세 이상의 노인 인구 비중|
Working_age_popul|사회적으로 노인 부양이 가능한 노동 인구 비중|
Working_hours|평균 근로 시간|
Employ_rate|취업률|
Gini_coff|해당 국가의 사회적 불평등 지수|
depression_percent|해당 국가의 우울증 환자 %|
suicide|해당 국가의 10,000명당 자살 한 사람 수|


---
### 3. File
파일 별 의미 대략 정리

+ **happiness.ipynb** : happiness.csv파일을 사용, 모든 OECD 국가, gdp순위에 비해서 행복도 순위가 높은 국가를 happy, 반대의 경우를 unhappy로 두고 총 3가지의 갈래로 나누어서 각 feature를 LinearRegression을 이용하여 분석
+ + **GLM.ipynb** : happiness.csv파일을 사용, 모든 OECD 국가, gdp순위에 비해서 행복도 순위가 높은 국가를 happy, 반대의 경우를 unhappy로 두고 총 3가지의 갈래로 나누어서 각 feature를 GLM을 이용하여 분석
+ **depression.ipynb** : depression_suicide.csv파일을 사용, 모든 OECD 국가를 LinearRegression, LogitResgression, OLS을 이용하여 분석
+ **suicide.ipynb** : depression_suicide.csv파일을 사용, 모든 OECD 국가를 LinearRegression, LogitResgression, OLS을 이용하여 분석

---
### 4. Model
##### 1) Regression
######  i. Linear : 종속 변수 y와 한 개 이상의 독립 변수 (또는 설명 변수) X와의 선형 상관 관계를 모델링하는 회귀분석 기법. 
![image](https://user-images.githubusercontent.com/55525705/136329638-f3a2cac1-875d-4cf6-aafa-d579b0d44d84.png)

<br>

######  ii. Logistic : 로지스틱 회귀의 목적은 일반적인 회귀 분석의 목표와 동일하게 종속 변수와 독립 변수간의 관계를 구체적인 함수로 나타내어 향후 예측 모델에 사용하는 것. 흔히 로지스틱 회귀는 종속변수가 이항형 문제(즉, 유효한 범주의 개수가 두개인 경우)를 지칭할 때 사용됨.
![image](https://user-images.githubusercontent.com/55525705/136330951-1e809cfa-b971-448d-81ff-25fe493b9803.png)

---

### 5. Result
#### 1) happy vs unhappy

![1](https://user-images.githubusercontent.com/55525705/147642546-5e3e682a-935f-4206-92bc-85f75c4d7267.JPG)


#### 2) depression vs happiness

![1](https://user-images.githubusercontent.com/55525705/147642426-6550e33a-141a-4097-b8ea-22c59d39d150.JPG)
 
 
#### 3) happiness vs suicide

![1](https://user-images.githubusercontent.com/55525705/147642789-7fa80133-e232-4c93-ba12-17d1ea9388a8.JPG)

#### 4) 결론

![2](https://user-images.githubusercontent.com/55525705/147642820-711e06db-d671-4aa3-a3f3-2894b1403433.JPG)

 - depression, suicide 모두 공통적으로 happiness와 차이를 보이는 요소 => elder/working
 - 생산 인구 대비 노인 인구의 증가로 정신적으로 힘들어 하는 사람들이 늘고 있다
 - 경제적인 성장 대비 행복도를 늘리기 위해서는 이를 해결하기 위한 노력이 필요
 
 
 
