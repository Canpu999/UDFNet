# UDFNet: Unsupervised Disparity Fusion with Adversarial Networks

This repository contains the experiment results for (UDFNet: Unsupervised Disparity Fusion with Adversarial Networks) by [Can Pu](https://github.com/Canpu999) and [Robert B Fisher](http://homepages.inf.ed.ac.uk/rbf/).

We will release our code and pretrained model here in the futrue after our paper is accepted.

## Introduction

We used 100 samples from ‘000000 10.png’ to ‘000099 10.png’ in the initial training dataset as our test dataset. 

Visualization images (1.png - 100.png) corresponde to the images (‘000000 10.png’ - ‘000099 10.png’) in the folder "Visualization_stereo_stereo_fusion" and "Visualization_stereo_lidar_fusion". 

Our refined disparity maps (1.png - 100.png) corresponde to the images (‘000000 10.png’ - ‘000099 10.png’) in the folder "Our_result_in_stereo_stereo_fusion" and "Our_result_in_stereo_lidar_fusion". 

## Data format:

Disparity values range (0..256). Disparity maps are saved as uint16 PNG images. A 0 value indicates an invalid pixel (ie, no
ground truth exists, or the estimation algorithm didn't produce an estimate for that pixel). Otherwise, the disparity for a pixel can be computed by converting the uint16 value to float and dividing it by 256.0:

disp(u,v)  = ((float)I(u,v))/256.0;

## Error

### The error in Stereo-stereo fusion:
SGM [1]    (input1): 22.38 pixels;

PSMNet [2] (input2): 1.22 pixels;

Ours:                0.87 pixels;


### The error in Stereo-lidar fusion:
PSMNet [2] (input1): 1.22 pixels;

Ours:                0.86 pixels;


## Reference
[1] H. Hirschmuller, “Accurate and efficient stereo processing by semi-global matching and mutual information,” in Computer Vision and Pattern Recognition, 2005. CVPR 2005. IEEE Computer Society Conference on, vol. 2. IEEE, 2005, pp. 807–814.

[2] J.-R. Chang and Y.-S. Chen, “Pyramid stereo matching network,” in Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition, 2018, pp. 5410–5418.






