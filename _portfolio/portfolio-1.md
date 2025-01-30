---
title: "LDSeg: Latent Diffusion for Medical Image Segmentation"
excerpt: "In this project we introduce a novel latent diffusion model for n-D medical image segmentation. The end-to-end training strategy ensures significantly faster sampling in the inference phase with improved segmentation accuracy and robustness to noisy acquisition. <br/><img src='/images/KneeSeg.gif'>"
collection: portfolio
---

## Model Architecture
![method](images/Method.png)

The model contains four components which are trained in an end-to-end strategy:
1. Label encoder
2. Image encoder
3. Denoiser
4. Label decoder

The label encoder produces the label embedding $z_{l(0)} = f_{label-enc}(y)$ and the image encoder produces image embedding $z_i = f_{image-enc}(X)$, given an Image $X$ and it's corresponding label image $y$.
A Gaussian block is used to get the perturbed label embedding $z_{l(t)} = \mathcal G(z_{l(0)}, t)$, given noise variance schedulers $\alpha$ and $\beta$ for timestep $t \in (1 \dotsc T)$.
The denoiser/score model learns the noise variances of label embedding for the transition states and predicts noise $z_{n(t)}$ for timestep $t \in (1 \dotsc T)$.
The denoised latent space $z_{dn}$ is mapped to segmentation $\hat{y}$ using the label decoder. Our training objective is to learn, ![q(\hat{y}|X)=\mathbb{E}_{q_{i}(z_{i}|X)}\left[q_{s}(\hat{y}|z)\right]](https://latex.codecogs.com/png.latex?q%28%5Chat%7By%7D%7CX%29%3D%5Cmathbb%7BE%7D_%7Bq_%7Bi%7D%28z_%7Bi%7D%7CX%29%7D%5Cleft%5Bq_%7Bs%7D%28%5Chat%7By%7D%7Cz%29%5Cright%5D) where $q_{l}(z \mid y, X) \sim \mathcal{N}(z_{dn}, \sigma^2 \mathrm{I})$.

![Latentdiffusion](images/Latentdiffusion.png)

In the inference phase, image embedding is obtained first using the image encoder, and then the Denoiser is iterated for $t = T \cdots 1$ to obtain ![Math](https://latex.codecogs.com/png.latex?\tilde{z}_{l(0)}), staring with ![Math](https://latex.codecogs.com/png.latex?\tilde{z}_{l(T)}) as a Gaussian random noise $(\mathcal{N}(\mathrm{0, I}))$. Finally, the trained label decoder is used to get the final segmentation $\hat{y}$.

## Results
A few examples of segmentation are given below for the Echo, GlaS and Knee datasets. Top row shows the source images/mmageslices, 2nd and 3rd row shows the reverse diffusion for the latent space and the segmentation outputs. The bottom layer shows the segmentations overlay on the source images.

--------------------

### <ins> <p align='center'> Echo </ins>
![Echo](images/EchoSeg.gif)

<br/>

### <ins> <p align='center'> GlaS </ins>
![GlaS](images/GlaSSeg.gif)

<br/>

### <ins> <p align='center'> Knee </ins>
![Knee](images/KneeSeg.gif)


--------------------

## Robustness to noises
An example from each dataset is shown to demonstrate the model robustness to noise. Here, $\sigma$ is the variance of the added noise to the source image. DSC is the Dice Similarity Co-efficient score for the image (2D/3D). For the Knee dataset, a randomly selected slice is shown for convenience.

--------------------

### <ins> <p align='center'> Echo </ins>
![RobustnessEcho](images/RobustnessEcho.gif)

<br/>

### <ins> <p align='center'> GlaS </ins>
![RobustnessGlaS](images/RobustnessGlaS.gif)

<br/>

### <ins> <p align='center'> Knee </ins>
![RobustnessKnee](images/RobustnessKnee.gif)

--------------------
