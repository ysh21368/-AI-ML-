# 프로그래머스 주최 AI Task: 채용 공고 추천
## 데이터셋 및 테이블 구조
### 데이터셋: 6000개의 학습용 데이터 및 2435개의 테스트용 데이터

<img width="711" alt="image" src="https://github.com/ysh21368/Job-Announcement-Recommendation-AI/assets/118493648/5bca9889-07fa-4cf0-ad4d-620b3ac4bfae">


### 테이블 구조:
- 테이블 1: job_tags
- 테이블 2: user_tags
- 테이블 3: tags
- 테이블 4: job_companies
### 전처리 및 데이터 결합
- 중복값 제거 후 4개의 테이블을 효과적으로 병합하여 사용
## 데이터 인코딩
- object 타입의 컬럼에 대해 라벨 인코딩 수행
- 다중 라벨을 가지는 컬럼에 대해서는 MultiLabelBinarizer를 활용한 인코딩 수행
## 모델 선택 및 성능 평가
- Logistic Regression
- 정확도: 0.8633
- Random Forest
- 정확도: 0.8008
- CatBoost
- 정확도: 0.8650

### 모델 선택 이유
- Logistic Regression: 우수한 성능과 빠른 속도로 학습 가능
- Random Forest: 복잡한 패턴을 학습 가능하며 과적합에 강함
- CatBoost: 범주형 데이터 다루기에 용이하며 뛰어난 성능

### 성능 평가
**정확도(accuracy)**를 평가 지표로 선택
모델 간 정확도 비교 결과, CatBoost가 가장 우수함

### 참고 사항
데이터셋 및 전처리 코드는 GitHub에서 확인 가능.
