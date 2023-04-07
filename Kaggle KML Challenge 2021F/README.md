# KML_MachineLearning_2021F

대회 링크 : https://www.kaggle.com/c/kml2021f/leaderboard

2021-2 진행한 국민대학교 Machine Learning Challenge 입니다. 
## 프로젝트 소개

- 주어진 **온라인 설문조사에 응답할 가능성이 가장 높은 패널을 예측**하는 모델을 개발하는 프로젝트입니다.
- 데이터셋은 **한국의 연구 및 컨설팅 회사인 PMI에서 제공되었습니다.**

## 결과물

[분석발표자료.pdf](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1b6f4f3c-4ab9-41df-af34-211fac8bf645/%E1%84%87%E1%85%AE%E1%86%AB%E1%84%89%E1%85%A5%E1%86%A8%E1%84%87%E1%85%A1%E1%86%AF%E1%84%91%E1%85%AD%E1%84%8C%E1%85%A1%E1%84%85%E1%85%AD.pdf)

## 주요 역할

- 지표 생성 및 모델링
- 데이터 전처리 , 데이터 시각화


## Project Report

> **이런 순서로 진행했어요**
> 
> 1. 결측치 처리
> 2. 데이터 형 변환
> 3. 파생변수 생성
> 4. Feature Engineering

feature datasets는 **LGBM** 과 **DNN**에 대한 두 개의 데이터 세트로 나뉩니다.
두 데이터 세트는 동일한 베이스로 생성되었지만, 독립적으로 제출하기 위해 feature 구성이 약간 달랐으며, 각각 다른 파일에 존재합니다.

- Same Base
    
    • features = GENDER, BIRTH, REGION
    
    • response features = SQ1, SQ2, SQ3

개인 정보 Feature는 response features(SQ1, SQ2, SQ3)과 동일하지만 데이터가 다릅니다. response features이 보다 정확한 데이터라고 판단하여 개인정보 특성의 누락된 값을 response features으로 채우고, 이를 response features로 대체하였습니다.

• BIRTH는 연령(2022 - BIRTH)으로 변경되며 LOI의 경우 CPI와의 상관관계가 높아 실험결과에 따라 LOI를 drop했습니다.

• GENDER 의 경우 수치적 특성이 없는 것으로 판단되어 자료형을 문자열로 변경한 뒤 원핫인코딩하였습니다. 또한, 수치형 변수는 standard scaling 하였습니다. 


2. 코드 순서


- ipynb 및 DNN_features.ipynb를 별도로 실행하여 각 모델에 대한 데이터 집합 csv 파일을 생성합니다(**input** 폴더에 저장)
- .ipynb 파일에서 모델별 데이터 세트를 가져와 LGBM과 DNN을 통해 모델링하여 두 가지 유형의 예측 데이터를 생성하고, 이 두 가지의 산술 평균으로 얻은 데이터를 최종 예측 값으로 저장합니다.

**상세코드는 github에 정리되어 있습니다.**



## **회고**


> 1. EDA시 기록한 가설을 검증하는 과정의 중요성
> 2. 앙상블의 효과
>     - 딥러닝 모델의 앙상블은 비약적인 성능 향상을 이루었음
> 3. 제한된 제출 기간 내의 계획된 실험
> 4. Data Leakage의 위험성
>     - **Data leakage를 해결하는 것이 자료의 결측치 처리보다 중요하였음**
>     2021-02-20 을 기준으로 train set을 나눔
 
