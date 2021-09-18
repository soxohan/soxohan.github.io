---
layout: post
title: "Heterogeneous Domain Adaptation via Soft Transfer Network"
category: paper
changefreq : daily
priority : 1.0
comments : true
permalink : /:categories/:year/:month/:day/:title/
math_use : true
sitemap : false
---

Y. Yao, Y. Yu, Y. Xutao, and Y. Ye, “Heterogeneous Domain Adaptation Via Soft Transfer Network,” *Proceedings of the 27**th* *ACM international conference on multimedia*, 2019, pp. 1578-1586.

<br>

## Abstract

- Propose a **Soft Transfer Network (STN)**
  - Jointly learns a domain-invariant subspace in an end-to-end manner, for addressing the HDA problem
  - The discriminative directions of domains
  - Matches both the marginal and conditional distributions across domains

![image](https://user-images.githubusercontent.com/85778937/133891306-ae25949c-5f14-4055-8368-5ff0c13db1bb.png)

<br>

<br>

## Methods

![image](https://user-images.githubusercontent.com/85778937/133891332-32e98a13-a607-4297-a6fc-052dc6add392.png)

<br>

- Source domain (in green)

- Target domain (in orange)

- The common subspace (in purple)

- r/R : the coefficient of the soft-label strategy to adaptively increase its importance

<br>

- Optimizing an objective function
  - A classification loss
    - Can be used to align the discriminative directions of domains

<br>

![image](https://user-images.githubusercontent.com/85778937/133891430-66bd32d6-4c25-4e4c-95a4-5e17883f249c.png)

<br>

- Soft-MMD loss
  - Can be applied to match both the marginal and conditional distributions between domains
  - Soft-label strategy of unlabeled target data
    - Avoids the hard assignment of each unlabeled target data to only one class that may be incorrect

<br>

![image](https://user-images.githubusercontent.com/85778937/133891435-e6877dfb-159b-4c56-b23f-100cc891ee15.png)

<br>

![image](https://user-images.githubusercontent.com/85778937/133891455-7e79e966-75b0-4256-b2d7-0c7775be956d.png)

![image](https://user-images.githubusercontent.com/85778937/133891465-6c7b398f-82f7-45c2-88a9-3c2bd848dca0.png)

<br>

![image](https://user-images.githubusercontent.com/85778937/133891477-fabe51fd-c0d2-4b01-b55c-1f7ab0b58052.png)

<br>

<br>

#### Overall objective of STN

![image](https://user-images.githubusercontent.com/85778937/133891496-f29e01bf-6020-4d34-8cb0-d7118ea5676e.png)

<br>

<br>

## Results

- Experiment
  - Image-to-image transfer task
    - Office + Caltech-256 dataset
  - Text-to-image transfer task
    - NISWIDE + ImageNet dataset
  - Text-to-text transfer task
    - Multilingual Reuters Collection dataset

![image](https://user-images.githubusercontent.com/85778937/133891517-cf49be57-110d-4207-8962-b086202b13bf.png)

<br>

![image](https://user-images.githubusercontent.com/85778937/133891530-6496b900-31c8-446c-9f9c-e56ead2971ce.png)

<br>

![image](https://user-images.githubusercontent.com/85778937/133891537-d726f272-0be0-4972-989e-05cc4dacd370.png)
