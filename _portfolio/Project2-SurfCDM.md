---
title: "SurfCDM: Cold diffusion for surface segmentation in medical image"
excerpt: "In this project we introduce a novel cold diffusion model for surface segmentation in medical image. The cold diffusion allows fast sampling, robust segmentation with uncertainty estimation. The method can be applied for both surface correction and multi-surface segmentation. <br/> ![demo](/images/SurfCDM.gif)"
collection: portfolio
---

## Method
![method](/images/SurfCDMmethod.png)

The label image with object is first unfolded to a surface using graph re-parameterization. The model is trained with column-wise purterbation for various noise scales.

![forwardDiffusion](/images/colddiffusion.gif)

In the inference phase, first a trained object detector is used to identify the centroid of the target object and then unfolded using graph re-parameterization. The reverse process is performed starting from the centroid and gradually correcting the surface positions in the column.

--------------------

## Results
SurfCDM can be used for both segmentation correction and multi-surface segmentation.

![segcorrector](/images/segcorrector.gif)

--------------------

![multisurface](/images/multisurface.gif)
