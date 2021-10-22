---
layout: post
title: "Improved Neural Signal Classification in a Rapid Serial Visual Presentation Task Using Active Learning"
category: paper
changefreq : daily
priority : 1.0
comments : true
permalink : /:categories/:year/:month/:day/:title/
math_use : true
sitemap : false
---

A. R. Marathe, V. J. Lawhern, D. Wu, D. Slayback, and B. J. Lance, “Improved Neural Signal Classification in a Rapid Serial Visual Presentation Task Using Active Learning,” IEEE Transactions on Neural Systems and Rehabilitation Engineering, Vol. 24, No. 3, 2015, pp. 333-343..

~~active learning을 거의 초반에 활용한 논문이라고 해야 하나..~~

<br>

## Abstract

- Use of active learning for offline EEG calibration in a simulated BCI paradigm
- Combination of QBC* and uncertainty sampling 
  - By using HDCA*, CSP*, and XDBLDA* as committee of classifiers and an unweighted linear summation of each classifier’s confidence score as the uncertainty metric
- Results show that active learning can be used to more efficiently and more accurately, calibrate a simulated BCI

<br>

## Methods

![image](https://user-images.githubusercontent.com/85778937/138505337-cf87de7e-5585-470f-b89b-3ea0726a1489.png)

<br>

QBC를 활용했다.

combination of QBC and uncertainty sampling

- Hierarchical Discriminant Component Analysis (HDCA)]
  - logistic regression classifiers의 앙상블을 기반으로 한 binary classification
  - **interest score** (2 step)
    - a set of 20 logistic discriminators are applied (each → independently)
    - a separate logistic regression discriminator is applied to the output of the 20 stage 1 discriminators → to create a single interest score
- Common Spatial Patterns (CSP) : 두 가지 조건 하에서 신호 variance의 차이를 극대화하는 신호의 선형 조합을 만든다
  - combined CSP spatial filtering with a Bayesian linear discriminant analysis (BLDA) classifier
  - 8 spatial filters 사용
- XDawn+Bayesian Linear Discriminant Analysis (XDBLDA)
  - a combination of the XDawn spatial filtering technique coupled with a BLDA classifier
  - highest rank filters가 single-to-single-plus-noise ratio를 극대화할 수 있도록 순위가 정렬된 spatial filters의 세트
  - top 8 spatial filters (input)
  - concat해서 input vector
-  Confidence
  - 차별적인 경계로부터 주어진 classifier score의 거리로 정의
- Merging Classifier Output
  - prediction of target/non-target + confidence score
    → 2개의 출력 병합 
    → 각 분류자에 대한 covariate variables 만듦 
    → by multiplying the binary prediction variable with the confidence score for each trial
  - continuous measure
    - 큰 양의 값 : higher confidence in target (1)
    - 큰 음의 값 : higher confidence in non-target (-1)
    - 0에 가까운 값은 더 낮은 신뢰도 (lower degree of confidence)
  - 3개의 classifier의 출력을 covariates로 사용해서 individual trials를 target/non-target에서 온 것으로 예측한 logistic regression을 이용해서 ensemble classifier를 fit해
  - step-wise regression 이용
- Cross-Validation (CV)
  - 10-fold cross validation
