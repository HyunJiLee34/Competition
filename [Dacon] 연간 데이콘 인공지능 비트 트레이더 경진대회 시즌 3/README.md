# bitcoin
 
1. **기간 : 2021.06.01 ~ 07.15** 

0. **팀원**
    1. 씩씩한오리너구리 (https://github.com/DongHyunByun/)
    2. 꿀지 (https://github.com/HyunJiLee34/)

2. **기술스택**
    1. 개발환경 : python.   
    2. 전처리 : pandas, numpy. 
    3. deeplearning : tensorflow.  
    4. bagging : tree, randomforest.   
    5. boosting : lgbmClassifier, xgbclassifier, gradientboosting.  
    6. regression : logisticRegression, ridgeClassifier. 
    
3. **내용 : 비트코인 가격예측**
    1. 과거 23시간의 데이터를 이용하여 미래 120분의 데이터를 예측
    2. 딥러닝, 머신러닝(배깅, 부스팅), 로지스틱 회귀분석 등의 모델을 이용하여 분석
    3. 매도 알고리즘 선택(10분내 매도 예측시 매수하지않음)

4. **파일설명**
    1. ensemble.ipynb 
        - 데이터 전처리  
        - 모델링 및 학습  
        - 예측값(매도시점, 예상가격)을 pickle 형태로 저장  
    2. algo_pickle_to_sub.ipynb
        - pickle로 저장된 예측값을 제출파일(csv) 형태로 변경
        - 매수는 항상 풀매수(1)
        - 매도는 10분이내 매도시 수수료를 고려하여 애초부터 매수하지 않는 것으로 판단
    3. bitcoin_model_sub_num.xlsx
        - 모델별 score 기재  
        
5. **결과**  
    최종 1위  
    <img width="1197" alt="스크린샷 2021-08-19 오후 3 29 27" src="https://user-images.githubusercontent.com/50386280/130019085-78cfa465-a771-4b42-8d26-61a7dd21d90a.png">

    


    
    

        
    
        
