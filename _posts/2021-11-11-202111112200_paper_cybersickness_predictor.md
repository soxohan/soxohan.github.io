---
layout: post
title: "A Deep Cybersickness Predictor Based on Brain Signal Analysis for Virtual Reality Contents"
category: paper
changefreq : daily
priority : 1.0
comments : true
permalink : /:categories/:year/:month/:day/:title/
math_use : true
sitemap : false
---

J. Kim, W. Kim, H. Oh, S. Lee, and S. Lee, “A Deep Cybersickness Predictor based on Brain Signal Analysis for Virtual Reality Contents,” *Proceedings of the IEEE/CVF International Conference on Computer Vision (ICCV)*, 2019, pp. 10580-10589.

*랩미팅 발표용*

<br>

## Goal

- Encoding of EEG signals to the cognitive representation relative to VR cybersickness and estimating the cognitive state from visual stimulus

<br>

<br>

## Motivation

- There is no solid publication to predict the cybersickness using a model while reflection the individual difference

<br>

<br>

## Materials and methods

![image](https://user-images.githubusercontent.com/85778937/142750767-30a8eb0e-a559-4fbe-ae88-1812b343be49.png)

<br>

- ETRI-VR dataset
  - 8-channel EEG data from 202 subjects
  - 44 VR contents were divided into 3 sessions
  - The rest time between sessions was given 3 minutes
  - Subjects were asked to perform the subjective evaluation at the end of each content according to the Likert-like scale (5 cybersickness level)
- Preprocessing 
  - Sampling rate of 250 Hz
  - Filtering with bandpass filter (0.3 ~ 100 Hz) and notch filter (at 60 Hz)
- Cognitive representation learning
  - Encoding cybersickness into the low-dimensional representation of the EEG
  - Use of the inter-correlation of the EEG channels and the intra-correlation over spectral and temporal domains
  - Transformed into a spectrogram
  - Designing an architecture to reflect temporal and spectral dependency 
    - Temporal network
      - Training of temporal dependency by taking various sizes of the horizontal kernel
    - Spectral network
      - Learning of spectral dependency through various sizes of the vertical kernel
    - Combining temporal and spectral networks
      - Concatenating the temporal and spectral networks to encode the temporal and spectral features jointly

![image](https://user-images.githubusercontent.com/85778937/142750809-fb9dd4d6-145a-48a9-82f7-387dc34ce59d.png)

- Cybersickness learning
  - Predicting the cybersickness while mimicking the cognitive representation encoded in cognitive representation learning
  - Video encoder: combined ResNet18 and stacked LSTM

![image](https://user-images.githubusercontent.com/85778937/142750848-159368bb-ec44-4bd1-84ac-61b031333434.png)

<br>

<br>

## Results

- Both the cognitive and visual features are meaningful information relative to cybersickness and lead to more powerful performance when they are integrated
- Taking the cognitive features helps the model generalize individual differences to achieve higher accuracy

