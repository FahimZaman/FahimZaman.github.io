---
title: "Latent Diffusion for Medical Image Segmentation: End to end learning for fast sampling and accuracy"
collection: publications
category: manuscripts
permalink: /publication/Latent_Diffusion_for_Medical_Image_Segmentation
date: 2025-01-20
venue: 'ArXiv'
excerpt: ''
paperurl: 'https://arxiv.org/abs/2407.12952'
---

Diffusion Probabilistic Models (DPMs) suffer from inefficient inference due to their slow sampling and high memory consumption, which limits their applicability to various medical imaging applications. In this work, we propose a novel conditional diffusion modeling framework (LDSeg) for medical image segmentation, utilizing the learned inherent low-dimensional latent shape manifolds of the target objects and the embeddings of the source image with an end-to-end framework. Conditional diffusion in latent space not only ensures accurate image segmentation for multiple interacting objects, but also tackles the fundamental issues of traditional DPM-based segmentation methods: (1) high memory consumption, (2) time-consuming sampling process, and (3) unnatural noise injection in the forward and reverse processes. The end-to-end training strategy enables robust representation learning in the latent space related to segmentation features, ensuring significantly faster sampling from the posterior distribution for segmentation generation in the inference phase. Our experiments demonstrate that LDSeg achieved state-of-the-art segmentation accuracy on three medical image datasets with different imaging modalities. In addition, we showed that our proposed model was significantly more robust to noise compared to traditional deterministic segmentation models. The code is available at https://github.com/FahimZaman/LDSeg.git.
