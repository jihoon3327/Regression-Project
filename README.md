# 제주렌트카 가격예측
#
### 주제 선정 이유
- 코로나 이슈 떄문에 제주도 렌트카 가격이 급증하고있다.
- 올 여름 여행을 위해 렌트카 가격을 미리 예측하여 돈을 미리 마련하고싶다.
#
### 데이터 수집
- 데이터 수집 사이트 : 제주패스랜트카
- 수집기간 : 6월~10월
- 수집방법 : 크롤링(selenium, bs4)
#
## 최초 데이터 변수 설명
### 독립변수(17개)  / 주요 독립변수 : "차량가격"
- 모델명 | 세그먼트 | 수용인원 | 연료타입 | 제공업체 | 랜트가능 최소 연령 |
- 옵션개수 | 리뷰수 | 누적예약수 | 별점 | 일자 | 요일 | 취급렌트카수 | 연식 |
- 평일/휴일 | 비수기/성수기 | 
- 옵션종류 | 월 | 차량가격
#
### 종속변수
- 하루 렌트 가격
#  
## 모델적용
#
### 데이터 전처리 방법 1 : 범주형 데이터를 모두 one-hot incoding을 통해 수치형으로 변환
#
### OLS summary 
- R-squared : 0.933
#
### Linear Regressor 
- train RMSE : 26591.34
- test RMSE : 26736.88
#
### RandomForest Regressor
- train RMSE : 7383.02
- test RMSE : 11620.82
#
### 데이터 전처리 방법 2 : 범주형 데이터를 모두 one-hot incoding + 라벨인코딩을 통해 수치형으로 변환
#
### OLS summary 
- R-squared : 0.788
#
### Linear Regressor 
- train RMSE : 47168.96
- test RMSE : 45884.44
#
### RandomForest Regressor
- train RMSE : 7385.26
- test RMSE : 11562.87
#
### 데이터 전처리 방법 2 : 범주형 데이터를 모두 one-hot incoding + 카테고리 임베딩을 통해 수치형으로 변환
#
### OLS summary 
- R-squared : 0.784
#
### Linear Regressor 
- train RMSE : 47617.61
- test RMSE : 46335.77
#
### RandomForest Regressor
- train RMSE : 7377.90
- test RMSE : 11651.45
