# stock_price_prediction

1. **기간 : 2021.11.10 ~ 11.29** 

1. **팀원**
    1. 씩씩한오리너구리 (https://github.com/DongHyunByun/)
    2. 꿀지 (https://github.com/HyunJiLee34/)

1. **기술스택**
    1. 개발환경 : python. 
    2. 전처리 : pandas, numpy, pickle, tqdm
    3. boosting : XGBRegressor, LGBMRegressor, DecisionTreeRegressor, RandomForestRegressor, Ridge, LinearRegression.   
    4. stock price api : FinanceDataReader, 
    
1. **내용 : 370개의 주식종목의 종가예측**
    1. fdr을 이용하여 주식 가격 데이터 load
    2. 종목별로 과거 20201101 이후 데이터 사용
    ![image](https://user-images.githubusercontent.com/50386280/152737528-0a7f7712-cc58-434a-bb51-7ba618aeed35.png)
    3. 데이터셋은 다음과 같이 나눔
    ![image](https://user-images.githubusercontent.com/50386280/152737668-86282855-7b47-4773-92c6-1970ba62864b.png)
    3. 직전 7일의 데이터를 이용하여 다음 종가를 예측
    ![image](https://user-images.githubusercontent.com/50386280/152737789-e80a7d1e-14ee-4b8e-8566-657f29879c9c.png)
    4. 사용 모델
    ![image](https://user-images.githubusercontent.com/50386280/152737844-65a471e0-b803-4897-b130-4164fa219eed.png)

1. **파일설명**
    1. train.ipynb, train2.ipynb
        - 데이터 전처리  
        - 모델링 및 학습  
        - 예측 및 제출 파일 생성
    2. sub
        - 제출 파일
    3. 주식 종료 가격 예측 경진대회_발표자료.pptx
        - 발표자료
    4. stock_list.csv
        - 예측 대상 종목
    5. sample_submission.csv
        - 제출 샘플

1. **결과**  
    28위/205명
    <img width="1199" alt="스크린샷 2022-02-07 오후 3 45 31" src="https://user-images.githubusercontent.com/50386280/152738230-eaf09708-fece-4bbc-b144-ed438b9ab1fd.png">
    
