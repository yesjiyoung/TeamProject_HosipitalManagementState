# Project 
### 병원 개/폐업 데이터 분석 : 병원의 회계데이터를 기반으로 지속 경영 여부를 분류예측하기


# Intro 
### 🗓️ Date 
Project term : 2020.11.03 ~ 2020.12.14 </br>
Presentation Date : 2020.12.15 </br>
### :man: Professor 
  한양대학교 ERICA, 산업경영공학과 허선 교수님 
### 👥 Team member 
  * 산업경영공학과 노지영
  * 산업경영공학과 구건호
  * 산업경영공학과 정우석
  * 산업경영공학과 김용빈
  * 소프트웨어학과 윤병서
  
# Data Set 
### ✅ Source 
https://dacon.io/competitions/official/9565/overview/ <br/>
csv file : raw_data.csv : ( train + test )


### ✅ Characteristics of the dataset 
  * 타입 : Multivariate
  * 레코드 : 428개 
  * 피쳐 : 58개 (Target var : ‘OC’ , predictors : 57개)
  * 타겟 변수의 클래스 불균형 : 개업 데이터와 폐업 데이터의 비율 -> 92:8
  * 2016, 2017 데이터의 변동성 반영 : 연도 별 데이터가 혼재되어있음 -> 2017-2016 파생데이터 생성

# Contents 

- **1.문제정의**
- **2.데이터탐색(EDA)**
  - 2.1 데이터셋 구조 파악
  - 2.2 기술통계량
  - 2.3 단변량
    - Target variable
    - Categorical variables
    - Numerical Variables
  - 2.4 다변량
    - Categorical - target
    - Numerical - target
  - 2.5 가설설정
- **3.데이터전처리[1차+모델링]**
  - 3.1 파생변수 생성
 - 3.2 Null처리
    - Null값이 대부분인 레코드 제거
    - 수치형 피쳐 내부의 null값을 평균으로 대체
    - 범주형 피쳐 내부의 null값은 최빈값으로 대체
  - 3.3 피쳐 타입 변경
  - 3.4 이상치 제거
  - 3.5 스케일링
    - dummy 변수 생성
    - Minmax
  - 3.6 모델링
    - 오버샘플링
    - 하이퍼파라미터 튜닝
    - 모델 적용
- **데이터전처리[2차+모델링]**
  - 3.7 이상치 대치
  - 3.8 스케일링
    - dummy 변수 생성
    - Minmax
  - 3.9 모델링
    - 오버샘플링
    - 하이퍼파라미터 튜닝
    - 모델 적용
- **데이터전처리[3차+모델링]**
  - 3.10 상관관계 분석 후 변수 제거
  - 3.11 이상치 대치
  - 3.12 스케일링
    - dummy 변수 생성
    - Minmax
  - 3.13 모델링
    - 오버샘플링
    - 하이퍼파라미터 튜닝
    - 모델 적용
- **4.결과 해석**
  - 4.1 confusion matrix
  - 4.2 roc_curve 그래프
  - 4.3 가설 검정( Decision Tree로 살펴본 feature 중요도)

# Result
### ✅ Source Code 
Colab -> https://colab.research.google.com/drive/1a6Cmqp0Tj6WulPBSYFsHtXpNO3EffyjQ?usp=sharing
### ✅ Best Model & Score
RandomForest </br>
  * recall : 0.8750
  * F1socre : 0.9333
  * AUCscore : 0.9375
