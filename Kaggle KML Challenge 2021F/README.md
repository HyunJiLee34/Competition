# KML_MachineLearning_2021F

대회 링크 : https://www.kaggle.com/c/kml2021f/leaderboard

2021-2 진행한 국민대학교 Machine Learning Challenge 입니다. 

"Which panel is most likely to respond to the given online survey?". 
The purpose of this ML competition is to develop a predictive model that can best solve this problem. A donated dataset was provided by PMI, a research and consulting company in Korea.

1. Feature Engineering

feature datasets는 **LGBM** 과 **DNN**에 대한 두 개의 데이터 세트로 나뉩니다.
두 데이터 세트는 동일한 베이스로 생성되었지만, 독립적으로 제출하기 위해 feature 구성이 약간 달랐으며, 각각 다른 파일에 존재합니다.

- Same Base
    
    • features = GENDER, BIRTH, REGION
    
    • response features = SQ1, SQ2, SQ3

개인 정보 Feature는 response features(SQ1, SQ2, SQ3)과 동일하지만 데이터가 다릅니다. response features이 보다 정확한 데이터라고 판단하여 개인정보 특성의 누락된 값을 response features으로 채우고, 이를 response features로 대체하였습니다.

• BIRTH는 연령(2022 - BIRTH)으로 변경되며 LOI의 경우 CPI와의 상관관계가 높아 실험결과에 따라 LOI를 drop했습니다.

• GENDER 의 경우 수치적 특성이 없는 것으로 판단되어 자료형을 문자열로 변경한 뒤 원핫인코딩하였습니다. 또한, 수치형 변수는 standard scaling 하였습니다. 


2. 코드 순ㅅ

- ipynb 및 DNN_features.ipynb를 별도로 실행하여 각 모델에 대한 데이터 집합 csv 파일을 생성합니다(**input** 폴더에 저장)
- .ipynb 파일에서 모델별 데이터 세트를 가져와 LGBM과 DNN을 통해 모델링하여 두 가지 유형의 예측 데이터를 생성하고, 이 두 가지의 산술 평균으로 얻은 데이터를 최종 예측 값으로 저장합니다.

**상세코드는 github에 정리되어 있습니다.**



### Project Report

-----------------------

1. Feature Engineering

The features dataset is divided into two datasets for **LGBM** and **DNN**.
The two datasets were created based on the same base, but the feature configuration was slightly different to make an independent submission, and each exists in a different file.

- Same Base
    
    • features = GENDER, BIRTH, REGION
    
    • response features = SQ1, SQ2, SQ3
    
    Personal information features are the same as response features, but with different data. We decided that the response features were more accurate data, so we filled in the missing values of the personal information features with the response, and replaced them with the response features.
    
    •  BIRTH is changed to age (2022 - BIRTH), and in the case of LOI, the correlation with CPI is high, so LOI was dropped based on the experimental results.
    
    •  In the case of GENDER, it was determined that there was no numerical characteristic, so the data type was changed to a string and included in one-hot-encoding. Also, numerical variables were collectively standard-scaled.
    

2. The Order of Code files

- Execute ipynb and DNN_features.ipynb separately to create a dataset csv file for each model (saved in **input** folder)
- By importing the dataset for each model from the .ipynb file, two types of prediction data are created by modeling through LGBM and DNN, and the data obtained by arithmetic average of these two is saved as the final prediction value.
 
