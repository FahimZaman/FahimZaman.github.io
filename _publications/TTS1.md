---
title: "Spatio-temporal hybrid neural networks reduce erroneous human 'judgement calls' in the diagnosis of Takotsubo syndrome"
collection: publications
category: manuscripts
permalink: /publication/TTS1
date: 2021-10-01
venue: 'eClinicalMedicine'
excerpt: ''
paperurl: 'https://www.thelancet.com/journals/eclinm/article/PIIS2589-5370(21)00395-3/fulltext'
---

Background
We investigate whether deep learning (DL) neural networks can reduce erroneous human “judgment calls” on bedside echocardiograms and help distinguish Takotsubo syndrome (TTS) from anterior wall ST segment elevation myocardial infarction (STEMI).

Methods
We developed a single-channel (DCNN[2D SCI]), a multi-channel (DCNN[2D MCI]), and a 3-dimensional (DCNN[2D+t]) deep convolution neural network, and a recurrent neural network (RNN) based on 17,280 still-frame images and 540 videos from 2-dimensional echocardiograms in 10 years (1 January 2008 to 1 January 2018) retrospective cohort in University of Iowa (UI) and eight other medical centers. Echocardiograms from 450 UI patients were randomly divided into training and testing sets for internal training, testing, and model construction. Echocardiograms of 90 patients from the other medical centers were used for external validation to evaluate the model generalizability. A total of 49 board-certified human readers performed human-side classification on the same echocardiography dataset to compare the diagnostic performance and help data visualization.

Findings
The DCNN (2D SCI), DCNN (2D MCI), DCNN(2D+t), and RNN models established based on UI dataset for TTS versus STEMI prediction showed mean diagnostic accuracy 73%, 75%, 80%, and 75% respectively, and mean diagnostic accuracy of 74%, 74%, 77%, and 73%, respectively, on the external validation. DCNN(2D+t) (area under the curve [AUC] 0·787 vs. 0·699, P = 0·015) and RNN models (AUC 0·774 vs. 0·699, P = 0·033) outperformed human readers in differentiating TTS and STEMI by reducing human erroneous judgement calls on TTS.

Interpretation
Spatio-temporal hybrid DL neural networks reduce erroneous human “judgement calls” in distinguishing TTS from anterior wall STEMI based on bedside echocardiographic videos.

Funding
University of Iowa Obermann Center for Advanced Studies Interdisciplinary Research Grant, and Institute for Clinical and Translational Science Grant. National Institutes of Health Award (1R01EB025018–01).
