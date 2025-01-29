---
title: "Patch-wise 3D segmentation quality assessment combining reconstruction and regression networks"
collection: publications
category: manuscripts
permalink: /publication/SQA2
date: 2025-09-15
venue: 'Journal of Medical Imaging'
excerpt: ''
paperurl: 'https://www.spiedigitallibrary.org/journals/journal-of-medical-imaging/volume-10/issue-5/054002/Patch-wise-3D-segmentation-quality-assessment-combining-reconstruction-and-regression/10.1117/1.JMI.10.5.054002.full'
---

Purpose
General deep-learning (DL)-based semantic segmentation methods with expert level accuracy may fail in 3D medical image segmentation due to complex tissue structures, lack of large datasets with ground truth, etc. For expeditious diagnosis, there is a compelling need to predict segmentation quality without ground truth. In some medical imaging applications, maintaining the quality of segmentation is crucial to the localized regions where disease is prevalent rather than just globally maintaining high-average segmentation quality. We propose a DL framework to identify regions of segmentation inaccuracies by combining a 3D generative adversarial network (GAN) and a convolutional regression network.

Approach
Our approach is methodologically based on the learned ability to reconstruct the original images identifying the regions of location-specific segmentation failures, in which the reconstruction does not match the underlying original image. We use conditional GAN to reconstruct input images masked by the segmentation results. The regression network is trained to predict the patch-wise Dice similarity coefficient (DSC), conditioned on the segmentation results. The method relies directly on the extracted segmentation related features and does not need to use ground truth during the inference phase to identify erroneous regions in the computed segmentation.

Results
We evaluated the proposed method on two public datasets: osteoarthritis initiative 4D (3D + time) knee MRI (knee-MR) and 3D non-small cell lung cancer CT (lung-CT). For the patch-wise DSC prediction, we observed the mean absolute errors of 0.01 and 0.04 with the independent standard for the knee-MR and lung-CT data, respectively.

Conclusions
This method shows promising results in localizing the erroneous segmentation regions that may aid the downstream analysis of disease diagnosis and prognosis prediction.
