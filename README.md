# VAE-Recommendation-System
> VAE 모델을 활용한 상품 추천 시스템

#### 소비자의 구매내역을 바탕으로 각 사용자에 맞는 상품을 추천합니다. 
- 협업 필터링 기반 추천 시스템 구현
- 기존의 워드 임베딩 방식의 한계를 극복
- Kaggle의 소비자 구매내역 데이터 활용
</br>

## VAE (Variational Autoencoder)
> VAE 모델이란?

Variational Autoencoder (VAE)는 데이터의 잠재 공간을 학습하고, 고차원 데이터를 저차원으로 압축하여 새로운 데이터를 생성하는 딥러닝 모델입니다. VAE는 주로 생성 모델로 사용되며, 이미지 생성, 텍스트 생성 등 다양한 응용 분야에 활용됩니다.
</br>

## 구조
> VAE는 두 개의 주요 구성 요소로 이루어져 있습니다:

1. **인코더 (Encoder)**
    - 입력 데이터를 잠재 공간(latent space)으로 매핑
    - 인코더는 입력 데이터의 확률 분포를 학습

2. **디코더 (Decoder)**
   - 잠재 공간의 표현을 원래 데이터로 재구성
   - 디코더는 인코더가 생성한 잠재 변수를 기반으로 데이터를 생성


## 작동 원리
> VAE는 다음과 같은 과정을 통해 작동합니다:

<img src="https://github.com/user-attachments/assets/6e69ac45-a82b-4956-af1b-1fc80340698c" width="600px"/>


1. **입력 데이터 인코딩**
   -  인코더는 입력 데이터를 잠재 공간의 확률 분포로 변환
   -  이 과정에서 평균과 분산을 추정
  
2. **샘플링**
   - 추정된 평균과 분산을 사용하여 잠재 변수를 샘플링
   -  Nosie를 부여
   -  Reparemeterization Trick

3. **디코딩**
   - 샘플링된 잠재 변수를 디코더에 입력하여 새로운 데이터를 생성

4. **손실 함수**
   - 재구성 손실(Reconstruction Loss)
   - KL 발산(Kullback-Leibler Divergence)

## 응용 분야
- **이미지 생성**: VAE는 이미지 생성 및 변환에 널리 사용
- **추천 시스템**: 사용자 특성에 맞춘 개인화된 추천을 생성하는 데 활용
- **비지도 학습**: VAE는 비지도 학습에서 데이터의 패턴을 발견하는 데 활용

