---
title: "Surf-CDM: Score-Based Surface Cold-Diffusion Model for Medical Image Segmentation"
collection: publications
category: conferences
permalink: /publication/SurfCDM
date: 2024-05-27
venue: 'IEEE International Symposium on Biomedical Imaging (ISBI)'
excerpt: ''
paperurl: 'https://ieeexplore.ieee.org/abstract/document/10635329'
---

Diffusion models have shown impressive performance for image generation, often times outperforming other generative models. Since their introduction, researchers have extended the powerful noise-to-image denoising pipeline to discriminative tasks, including image segmentation. In this work we propose a conditional score-based generative modeling framework for medical image segmentation which relies on a parametric surface representation for the segmentation masks. Moreover, we adapted an extended variant of the diffusion technique known as the "cold-diffusion" where the diffusion model can be constructed with deterministic perturbations instead of Gaussian noise, which facilitates significantly faster convergence in the reverse diffusion. We evaluated our method on an echocardiogram video dataset (2230 echo image frames) and compared its performance to the most popular and widely used image segmentation models. Our proposed model not only outperformed the compared methods in terms of segmentation accuracy, but also showed potential in estimating segmentation uncertainties for further downstream analyses due to its inherent generative nature.
