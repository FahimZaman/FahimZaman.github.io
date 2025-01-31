---
title: "Windows tool for Echocardiogram video segmentation"
excerpt: "In this project, we developed a windows tool for echocardiogram video segmentation using optical flow algorithm. <br/> ![demo](/images/Echosegdemo.gif)"
collection: portfolio
---

## Method
![method](/images/Echosegdemo.gif)

Manual segmentation of echocardiogram videos for ground truth generation is always challenging due to speckle noises present in the video, as well as extremely time consuming and laborious process of annotating each frame of a video. In this project, we developed an easy to use windows tool for the physicians for echocardiogram video segmentation that uses optical flow algorithm. The user only needs to select necessary surface points to create closed surface for multiple objects in only the first frame. The selected points will be used to measure the optical flow propagation throughout the whole video, thus generating full video segmentation.

![Echosegment](/images/Echosegment.PNG)

The tool also allow manual surface correction for one or multiple frames if error occurs.

![Echocorrector](/images/Echocorrector.PNG)
