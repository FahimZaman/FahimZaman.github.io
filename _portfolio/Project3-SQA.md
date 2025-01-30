---
title: "Segmentation Quality Assessment (SQA)"
excerpt: "Assessng the quality of the segmentaion is extremely crucial for medical images as wrong segmentation can lead to wrong diagnosis/prognosis in the downstream analysis. In this project we introduce three deep learning-based SQA approaches. The first approach uses surface optimization technique for erroneous surface prediction on the segmented surface. The second approach uses GAN based reconstruction and patch-wise regression model to predict erroneous volumetric patches with error magnitude. The third approach deals with adversarial attacks on the segmentation network to prevent wrong prediction from SQA. <br/> ![demo](/images/SQAdemo.png)"
collection: portfolio
---

## Surface-based SQA
A unet-based model predicts the volumetric erroneous regions around target objects. The volumetric regions are mapped to the segmented surface of the target objects and optimized using patch-area for robust error prediction.

![SQA1](/images/SQA1.gif)

--------------------

## Patch-wise SQA
A GAN-based reconstruction network is trained to reconstruct the masked segmented regions only when the segmentation is accurate. Then based on the reconstruction error and the obtained segmentation, a regression model predicts patch-wise error magnitude. By design, the reconstruction network fails when the obtained segmentation is not accurate, hence produces segmentation related error features which is later used for error location and magnitude prediction.

![SQA2](/images/SQA2.png)

--------------------

## SQA with adversarial attacks
The regresion model is extremely vulnerable to a well desinged adversarial attack. Hence, any SQA model equipped with regression model can produce false negatives in such attacks which is seriously detrimental for downstream disease analysis. We introduce a GAN-based validation model that compares the structural similarity between the reconstructed and given input image to validate if the SQA model is under adversarial attack, thus preventing any false negatives in the results.

![SQA3](/images/SQA3.png)
