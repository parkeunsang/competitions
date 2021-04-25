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

  - [대회 링크](https://www.kaggle.com/c/riiid-test-answer-prediction)

  - **Result : Top 78% (2622/3395)**

  - 개요 : 학생들의 온라인 강의 수강 데이터를 이용해 과목별 어떤 강의를 얼마만큼의 시간동안 들은 학생이 해당 과목 시험에서 정답을 맞출 수 있을 것인지를 예측

  - 사용 모델 : Logistic Regression

  - 후기 : 데이터의 Volume이 매우 크다보니 data를 import하는데도 각각의 column에 format을 지정해줘야했다. 각각의 문제의 수준과 각각 학생들의 수준을 나타내기위해 정답률을 바탕으로 데이터를 전처리 한 후 총 2개의 설명변수(문제의 난이도, 학생들의 실력)를 예측에 활용했다.

    결과가 좋지않았던 이유는 모델선정에 있기보다는, 데이터에 대한 이해가 충분히 이루어지지않아 feature engineering을 제대로 하지 못했기 때문이라고 생각한다.

  

#### Dacon

- 랜드마크 분류(landmark) : 컴퓨팅 파워의 한계로 제출못함

- 소설작가 분류(fiction)

  - 기간 : 2020.11 ~ 2020.

  - [대회 링크](https://dacon.io/competitions/open/235670/overview/description/)

  - **Result : Top 54% (154/287)**

  - 개요 : 문장을 보고 어떤 작가의 문장인지를 판별하는 문제(총 5명의 작가)

  - 사용 모델 : LSTM(불용어를 제거하고 토큰화)

  - 후기 : 모델을 노트북에서 돌리다보니 학습하는데 시간이 너무오래걸려 다양한 모델, 전처리를 해보지 못했다. GPU환경을 제공하는 colab이나 데스크탑에서 작업을 할 필요성을 느꼈다.

    또 LSTM의 동작원리를 구체적으로 모르다보니 세부 parameter값들도 제대로 세팅하지못했다. 모델링을 할 때 해당 모델을 이해하고 사용하는게 필수적임을 깨달았다.

- 금융문자분석(smishing) : 상위 78%

  - 기간 : 2019.12 ~ 2020.01

  - [대회 링크](https://dacon.io/competitions/official/235401/overview/description/)
  - **Reesult : Top 78% (292/375)**

  - 개요 : 약 30만 개의 실제 문자메시지 데이터가 주어지고 그중에서 스미싱 문자를 분류하는 문제.
  - 평가 지표 : AUC score
  - 팀원 : 4명
  - 분석 과정 : Python의 KoNLPy 라이브러리의 형태소 분석기 중 하나인 Okt를 이용해 메시지에서 명사, 동사, 형용사 등 의미 있는 형태소를 추출. 이후 LSTM모델을 이용해 적합


  

  

