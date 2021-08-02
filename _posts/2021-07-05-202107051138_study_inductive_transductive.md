---
layout: post
title: "Inductive learning vs. Transductive learning"
category: study
changefreq : daily
priority : 1.0
comments : true
permalink : /study/:categories/:year/:month/:day/:title/
math_use : true
sitemap : false
show_date: true
---

## Inductive learning vs. Transductive learning

### Inductive learning

- supervised learning의 상황
- Test X에 대한 정보가 주어지지 않은 상황에서 test Y 맞추기
- transductive learning보다 test Y 맞추기 어렵다
- 즉, training에서 본 적 없는 새로운 graph에 대해서 예측해야하는 문제.
- 결과를 결정하기 위해서 증거를 사용하는 것
- 모델 or 가설이라는 개념은 훈련용 데이터셋을 통해 만들어지고, 이것은 new unseen data에 대해서도 잘 작동할 것이라는 사실은, 기본적인 ML의 가정.



### Transductive learning

- domain adaptation
- test X에 대한 정보가 주어진 상황에서 test Y를 맞추는 문제
- test 데이터의 레이블은 없지만 그 안에서 유의미한 패턴 추출이 가능
- 모델을 구축하지 않아서 새로운 데이터가 입력으로 들어왔을 때 알고리즘을 처음부터 재시작할 필요성이 존재해서 계산 효율이 낮음
- 특정 예제에 대한 예측을 시행할 때, 특정 예제를 활용하는 것을 의미한다.
- 클래식한 예제 : KNN

