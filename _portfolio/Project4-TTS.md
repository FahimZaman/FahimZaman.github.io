---
title: "Robust pathophysiological feature detection with explainable AI (XAI)"
excerpt: "Takotsubo Syndrome (TTS) is a rare cardiovascular disease that mimics the clinical characteristics of acute myocardial infarction (AMI). The gold standard of TTS diagnosis is the use of coronary angiography, which is not only invasive but also slow in process and may endanger patients in an emergency setting. In this project, we develop DL-based spatiotemporal model for improved differential diagnosis of TTS, using only echocardiogram (a non-invasive process). The DL-model significantly outperform human physicians in terms of diagnosis accuracy. Furthermore, using XAI, we visualize the DL-model learned features for identifying underlying robust pathophysiological features that can be easily applied in clinical settings and help the physicians make the 'judgement call' for accurate diagnosis. <br/> ![demo](/images/tts1demo.gif)"
collection: portfolio
---

![method](/images/ttspaper12.PNG)

We developed a DL-based classifier with VGG as a backbone. The model achieved 80% accuracy in differential diagnosis of TTS and AMI using echocardiogram videos (echo), outperforming the human physicians (65% accuracy). The GradCAM saliency map of the model shows consistent high activation in basal septal and basal lateral wall of the left ventricles. The optical flow, longitudinal strain and tissue doppler study validates significant difference in the Atrioventricular (AV) plane displacements between the two disease. This indicates, temporal features obtained from the motion differences in the echo may have played a vital role in model's differential diagnosis.

--------------------

![opticalflow](/images/opticalflow.gif)

The sparse optical flow measures the ventricular wall motion and shows significant motion difference in AV plane displacements. Furthermore, the motion pattern observed in optical flow measurement shows potential diastolic dysfunction in TTS patients. 

--------------------

![ttspaper3](/images/ttspaper3.gif)

We developed a novel two-branched spatiotemporal model for differential diagnosis of TTS, that takes echo frames as the first input to learn the spatial and textural features, dense optical flow measurment conditioned on the left-ventricle and left-atrium segmentation as the second input to learn temporal dynamics of the cardiac cycle. The model shows an improved diagnosis accuracy of 84%. The saliency map visualization shows high activation in diastolic phase for the temporal branch which farther validates diastolic dysfunction/disynchrony for TTS patients. We are currently working on validating our findings with thorough analysis on different pathophysiological features relating AV plane displacements.

![paper3demo](/images/paper3demo.gif)
