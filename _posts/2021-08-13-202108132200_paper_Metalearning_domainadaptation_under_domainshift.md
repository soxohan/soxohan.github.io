---
layout: post
title: "Meta-Learning with Domain Adaptation for Few-Shot Learning Under Domain Shift"
category: paper
changefreq : daily
priority : 1.0
comments : true
permalink : /:categories/:year/:month/:day/:title/
math_use : true
sitemap : false
---

Anonymous authors, “Meta-Learning with Domain Adaptation for Few-Shot Learning Under Domain Shift," *ICLR*, 2019



~~anonymous authors라니.. 끌려서 읽어보았다. 굉장히 글이 잘 읽히는 편이었다. 코드는 없었던듯~~

<br>

## Abstract

- Propose a novel meta-learning paradigm: Meta-Learning with Domain Adaptation (MLDA)
  - Consider the scenario where the training tasks and test tasks are drawn from different distributions
  - Have very limited data for test tasks (tasks in the target domain)

![image](https://user-images.githubusercontent.com/85778937/130032602-42a26b58-fef3-422f-afea-23fc739f499f.png)

<br>

<br>

## Methods

![image](https://user-images.githubusercontent.com/85778937/130032780-43fe9fd3-27f5-422a-988f-0de00aa37b70.png)

굉장히 간단

base objective equation은 few-shot의 loss와 domain adaptation loss를 합치는 방향으로 설정

여기서 domain adaptation loss는 GAN loss와 cycle loss를 이용한다.

여기서 cycle consistency란 X가 G를 통과하고 다시 F를 통과했을 때 X가 나오는 것이다.

즉, 한 바퀴를 돌아도 다시 내 자신이 되어야 한다! (아래 그림 참고)

![image](https://user-images.githubusercontent.com/85778937/130034074-c18ed20d-94a5-4de2-8e9b-b86daa8b2102.png)

<br>

<br>

## Results

- Dataset
  - Omniglot dataset / Omniglot-M dataset
  - Office-Home datset

![image](https://user-images.githubusercontent.com/85778937/130034855-5a82948a-375e-4345-923b-85dc6eb63009.png)

<br>

![image](https://user-images.githubusercontent.com/85778937/130034953-3557d1db-f592-4db5-baa1-a479c94e3e41.png)

