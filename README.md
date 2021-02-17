# Kaggle, Dacon projects



## What is kaggle/Dacon Competition?

- 주어진 데이터를 이용해 예측알고리즘을 만들어 성능(prediction)을 검증하는 대회
- 이미지, 텍스트 등 비정형 데이터와 관련된 주제가 많음



## 참가 목적

- Competitive **Data Scientist**가 되기 위해서는 모델링과 같이 데이터를 이용한 예측을 하는 능력이 요구된다. 그래서 이러한 대회 참여를 통해 경험을 쌓으며 공부를 하고자 한다.
- 또한 맹목적으로 모델링을 copy & paste해서 사용하는 것으로는 최상위권에 들 수 없기 때문에 최대한 해당 모델을 이해한 후 사용하고자 한다.



## 현황

#### Kaggle

- **Riid** 

  - [URL](https://www.kaggle.com/c/riiid-test-answer-prediction)

  - **Result : Top 78% (2622/3395)**

  - 대회 개요 : 학생들의 온라인 강의 수강 데이터를 이용해 과목별 어떤 강의를 얼마만큼의 시간동안 들은 학생이 해당 과목 시험에서 정답을 맞출 수 있을 것인지를 예측

  - 사용 모델 : Logistic Regression

  - 후기 : 데이터의 Volume이 매우 크다보니 data를 import하는데도 각각의 column에 format을 지정해줘야했다. 각각의 문제의 수준과 각각 학생들의 수준을 나타내기위해 정답률을 바탕으로 데이터를 전처리 한 후 총 2개의 설명변수(문제의 난이도, 학생들의 실력)를 예측에 활용했다.

    결과가 좋지않았던 이유는 모델선정에 있기보다는, 데이터에 대한 이해가 충분히 이루어지지않아 feature engineering을 제대로 하지 못했기 때문이라고 생각한다.

  



#### Dacon

- 랜드마크 분류 : 컴퓨팅 파워의 한계로 제출못함
- 소설작가 분류 : 상위 54%