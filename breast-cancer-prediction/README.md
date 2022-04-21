# 유방암 예측 예제

이 예제 노트북은 Sagemaker 의 유방암 예측을 위해 linear-learner 를 사용하는 방법을 보여줍니다.

* Sagemaker 사용을 위한 환경 구성
* Sagemeker 의 linear-learner 를 사용하기 위해 dataset 을 recordIO 포맷으로 변환 및 사용자가 제공한 S3 버킷에 업로드 
* 데이터에 대해 linear-learner 를 훈련
* 훈련된 모델 호스팅 
* 호스팅 된 모델을 이용한 추론 

## linear-learner
- linear-learner 알고리즘은 분류와 회귀 문제를 해결하기 위해 만들어진 supervised learning 의 한종류입니다.
- 이진 분류 (예를 들어 암인가 암이 아닌가) 와 같은 문제에 있어 0과 1 이 label 이 될 수 있습니다.
- linear-learner 알고리즘은 기존의 알고리즘에 비해 명확한 hyperparmeter 튜닝의 속도에 있어 이득을 제공합니다.
- SageMaker linear-learner 는 입력 및 출력 데이터 위치와 목표 유형(분류 또는 회귀)을 인수로 지정해야 합니다.
