# Kaggle, Dacon projects



## What is kaggle/Dacon Competition?

- 주어진 데이터를 이용해 예측알고리즘을 만들어 성능(prediction)을 검증하는 대회
- 이미지, 텍스트 등 비정형 데이터와 관련된 주제가 많음



## 참가 목적

- Competitive **Data Scientist**가 되기 위해서는 모델링과 같이 데이터를 이용한 예측을 하는 능력이 요구된다. 그래서 이러한 대회 참여를 통해 경험을 쌓으며 공부를 하고자 한다.
- 또한 맹목적으로 모델링을 copy & paste해서 사용하는 것으로는 최상위권에 들 수 없기 때문에 최대한 해당 모델을 이해한 후 사용하고자 한다.



## 현황

#### Kaggle

- <font color="blue">Riid</font>

  - [대회 링크](https://www.kaggle.com/c/riiid-test-answer-prediction)

  - **Result : Top 78% (2622/3395)**

  - 개요 : 학생들의 온라인 강의 수강 데이터를 이용해 과목별 어떤 강의를 얼마만큼의 시간동안 들은 학생이 해당 과목 시험에서 정답을 맞출 수 있을 것인지를 예측

  - 사용 모델 : Logistic Regression

  - 후기 : 데이터의 Volume이 매우 크다보니 data를 import하는데도 각각의 column에 format을 지정해줘야했다. 각각의 문제의 수준과 각각 학생들의 수준을 나타내기위해 정답률을 바탕으로 데이터를 전처리 한 후 총 2개의 설명변수(문제의 난이도, 학생들의 실력)를 예측에 활용했다.

    결과가 좋지않았던 이유는 모델선정에 있기보다는, 데이터에 대한 이해가 충분히 이루어지지않아 feature engineering을 제대로 하지 못했기 때문이라고 생각한다.


- <font color="blue">PetFinder</font>
  - 기간 : 2021.12.21 ~ 진행중
  - [대회 링크](https://www.kaggle.com/c/petfinder-pawpularity-score/overview)
  - **Result : None**
  - 개요 : 유기동물들의 이미지의 특징에 따라 pawpularity를 예측하는것
  - 평가지표 : RMSE



#### Dacon

- 

- <font color="red">랜드마크 분류(landmark)</font>

  - 컴퓨팅 파워의 한계로 제출못함

- <font color="blue">소설작가 분류(fiction)</font>

  - 기간 : 2020.11 ~ 2020.12

  - [대회 링크](https://dacon.io/competitions/open/235670/overview/description/)

  - **Result : Top 54% (154/287)**

  - 개요 : 문장을 보고 어떤 작가의 문장인지를 판별하는 문제(총 5명의 작가)

  - 사용 모델 : LSTM(불용어를 제거하고 토큰화)

  - 후기 : 모델을 노트북에서 돌리다보니 학습하는데 시간이 너무오래걸려 다양한 모델, 전처리를 해보지 못했다. GPU환경을 제공하는 colab이나 데스크탑에서 작업을 할 필요성을 느꼈다.

    또 LSTM의 동작원리를 구체적으로 모르다보니 세부 parameter값들도 제대로 세팅하지못했다. 모델링을 할 때 해당 모델을 이해하고 사용하는게 필수적임을 깨달았다.
    
    

- <font color="blue">금융문자분석(smishing)</font>

  - 기간 : 2019.12 ~ 2020.01

  - [대회 링크](https://dacon.io/competitions/official/235401/overview/description/)
  
  - **Result : Top 78% (292/375)**
  
  - 개요 : 약 30만 개의 실제 문자메시지 데이터가 주어지고 그중에서 스미싱 문자를 분류하는 문제.
  
  - 평가 지표 : AUC score
  
  - 팀원 : 4명
  
  - 분석 과정 : Python의 KoNLPy 라이브러리의 형태소 분석기 중 하나인 Okt를 이용해 메시지에서 명사, 동사, 형용사 등 의미 있는 형태소를 추출. 이후 LSTM모델을 이용해 적합
  
    
  
- <font color="blue">비트 트레이더 경진대회(coin)</font>

  - 기간 : 2021.04 ~ 2021.05

  - [대회 링크](https://dacon.io/competitions/official/235712/overview/description)

  - **Result : Public(TOP 3%, 3/92), Private(TOP 85%, 78/92)**

  - 개요 : 비트코인이 포함된 10가지 종류의 암호화폐 가격데이터(1380분)를 이용해 다음 120분의 가격을 예측하고, 최적의 매매를 해서 가장 높은 수익률을 목표로 하는 대회

  - 평가 지표 : 10,000달러의 자본금을 시작으로 각자의 매매전략을 통해 최종 자본금을 평가지표로 한다.

  - 팀원 : 4명

  - 분석 과정 : 처음에는 ARIMA, Prophet등 시계열 예측기법을 사용해 Open(시초가) 데이터를 예측했는데, 거래량 등 다른 데이터를 분석에 사용할 수 없다보니 별로 좋은 결과를 얻지는 못했다. 그래서 다음 120분에서 가격이 최대로 되는 시점(argmax)와 그때의 가격(max)을 예측하는 2개의 모델을 만들어 사용했다. 모델링은 Light GBM을 이용했다. 

    public데이터에서는 꽤나 좋은 결과를 얻었지만(+280%의 수익률) private 데이터에서는 처참한 결과를 얻었다(-33%의 수익률). 이유는 **public**데이터에서는 전체적으로 **코인들이 상승하는 경향**이 강해서 최대한 많은 코인을 매매하는게 좋은 수익을 거뒀지만, **private** 데이터에서는 반대로 코인들이 **하락하는 경향**이 강해서 최대한 많은 코인을 매매하는 전략이 안좋은 결과를 야기했기 때문이라고 생각된다.

    



