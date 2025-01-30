---
title: "LDSeg: Latent Diffusion for Medical Image Segmentation"
excerpt: "In this project we introduce a novel latent diffusion model for n-D medical image segmentation. The end-to-end training strategy ensures significantly faster sampling in the inference phase with improved segmentation accuracy and robustness to noisy acquisition. <br/> ![demo](/images/KneeSeg.gif)"
collection: portfolio
---

## Model Architecture
![method](/images/Method.png)

The model contains four components which are trained in an end-to-end strategy:
1. Label encoder
2. Image encoder
3. Score Model
4. Label decoder

The label encoder produces the label embedding and the image encoder produces image embedding , given an Image and it's corresponding label image. A Gaussian block is used to get the perturbed label embedding, given noise variance schedulers for all the timesteps. The score model learns the noise variances of label embedding for the transition states and predicts noise. The denoised latent space is then mapped to segmentation using the label decoder.

![Latentdiffusion](/images/Latentdiffusion.png)

In the inference phase, image embedding is obtained first using the image encoder, and then the score model is iterated for the sampling steps, staring with a Gaussian random noise. Finally, the trained label decoder is used to get the final segmentation.

--------------------

## Results
A few examples of segmentation are given below for the Echo, GlaS and Knee datasets. Top row shows the source images/imageslices, 2nd and 3rd row shows the reverse diffusion for the latent space and the segmentation outputs. The bottom layer shows the segmentations overlay on the source images.

![LDSegResults](/images/LDSegResults.gif)

--------------------

## Robustness to noises
An example from each dataset is shown to demonstrate the model robustness to noise.

![LDSegRobustness](/images/LDSegRobustness.gif)
