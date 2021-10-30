---
layout: post
title: "Quantifying VR cybersickness using EEG"
category: paper
changefreq : daily
priority : 1.0
comments : true
permalink : /:categories/:year/:month/:day/:title/
math_use : true
sitemap : false
---

E. Krokos, and A. Varshney, “Quantifying VR cybersickness using EEG,” *Virtual Reality*, 2021, pp. 1-13.

*랩미팅 발표용. 굉장히 쉬운 논문.*

<br>

## Goal

- Continuously measuring and quantifying cybersickness

<br>

<br>

## Motivation

- The survey-based qualitative approach is unable to provide real-time quantitative measurements

<br>

<br>

## Methods and materials

- Experimental protocol
  - The duration of the fly-through condition for 61 seconds
- Data acquisition and preprocessing
  - 43 participants
  - Brain-wave activity
    - 14-channels sampling at 128 Hz
    - Mean power for each channel is subtracted from that channel’s data
    - Filtering with a high-pass and low-pass filters
  - Joystick
    - No tilt indicated that they felt no sickness and full tilt indicated extreme sickness
    - Sampling at 90 Hz
    - Quantifying the cybersickness level between 0 and 1
- Independent Component Analysis (ICA)
  - Decomposing EEG signals, for each subject, into independent components using ICAs
    - 14 independent components per participant
  - Clustering similar components
    - Cluster A: most representative of cybersickness cluster
- Time-frequency analysis
  - Correlating the participants’ self-reported cybersickness levels with the ICA cluster power spectra

![image](https://user-images.githubusercontent.com/85778937/139538126-ec306a14-adf0-4f90-91ad-984d64cd9555.png)

<br>

<br>

## Results

- The SSQ score and the self-reported cybersickness using the joystick have a statistically significant Pearson Correlation r=0.49 and p=0.0009<0.05 
- There is a power increase across many frequencies for participants experiencing the virtual fly-through of the spaceport
- Statistically significant and high correlation exists for delta, theta, and alpha bands for cluster A with the self-reported cybersickness information from the participants
- External factors
  - Joystick movements and head movement would not have influenced the overall spectral frequency 
  - The cybersickness provocation could be construed to be too short
  - The effects being measured may be influenced by emotional arousal of being in a virtual reality environment

