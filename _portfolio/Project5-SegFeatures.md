---
title: "Robust feature selection from complex latent space for disease diagnosis"
excerpt: "In this project, we introduce a novel feature selection technique from the latent space of a DL-based segmentation model for disease diagnosis. <br/> ![demo](/images/tts2demo.gif)"
collection: portfolio
---

## Method
![method](/images/tts2demo.gif)

A simple CNN-based image/video disease classifier may be vulnerable to noisy acquisition and artifacts. To ensure robust feature learning, we propose to train a segmentation model that segments the target object/organ/tumor. The segmentation model's latent feature space is enriched with robust geometric and structural features that may be extremely important in a lot of disease diagnosis and prognosis. Hence, instead of using a classifier directly, we propose to use the complex latent space of a segmentation model for disease diagnosis and prognosis. We further implemented LASSO algorithm for irrelevant feature reduction, and used random forest classifier for disease diagnosis, that not only increased computational efficiency, but also achieved robust diagnosis accuracy.
