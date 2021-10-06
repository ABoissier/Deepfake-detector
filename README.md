# Deepfake-detector

![GitHub last commit](https://img.shields.io/github/last-commit/ABoissier/Deepfake-detector)

Building a MesoNet4 network &amp; deploying it online

## Context 

Deepfakes have become a growing issue, especially with the development of more robust **Generative Adversarial Networks (GANs)**. Altough GANs were first introduced in 2014 [[1]](#1), the recent advances in computer vision have allowed them to create synthetic images and videos of celebrities or politicians.

<p align="center">
  <img src= Readme_Data/Obama_DF.gif/>
</p>

The use of deepfakes in fake news, hoaxes and even financial fraud have garnered, much needed attention, both politically and academically, to try to limit their use and propagation. One such attempt, is the **MesoNet**, a neural network architecture, created by Darius Afchar &amp; al. in 2018 [[2]](#2) to help stem the deepfake tide.

## Paper

MesoNet-4 was developed by a team of three researchers in 2018 [[2]](#2) in an attempt to detect deepfakes, in a novel, deep-learning approach. 

### Dataset

The datasets used in the paper and in the project are the following :

- **Deepfake dataset :** composed of 175 rushes of forged videos. The videos were then compressed using the H.264 codec. Approximately 50 faces were extracted per scene

- **Face2Face dataset :** 300 videos were used for training out of more than of thousand.


### Model architecture

The paper suggests two possible architectures, which have achieved the best classification results among all tests. They are based on networks for image classification (alternating between convolutions and pooling for **feature extraction** and dense network for **classification**).

Meso-4 Architecture           |  Inception modules for MesoInception-4
:-------------------------:|:-------------------------:
![Meso4](Readme_Data/meso4.png) |  ![Mesoinc](Readme_Data/mesoinception4.png)


#### Meso-4
The first layers of the network are convolutions and pooling, which are followed by a dense network with one hidden layer. The convolutional layers use ReLU activation functions; as well as batch normalization and dropout, to regularize their output.

#### MesoInception-4
In this variant, the first two convolutional layers are replaced by an **inception module** [[3]](#3).

### Theoretical results (To be completed)
The Meso-4 architecture achieved a classification score of approx. 0.9 according to the paper.

<p align="center">
  <img src= Readme_Data/results.png/>
</p>


## Project

## How to use ?

## Advantages and shortcomings

## References
<a id="1">[1]</a> 
_Ian J. Goodfellow &amp; al. (2014). 
Generative Adversarial Networks.
Advances in Neural Information Processing Systems 27_

<a id="2">[2]</a> 
_Darius Afchar &amp; al. (2018). 
MesoNet: a Compact Facial Video Forgery Detection Network_

<a id="3">[3]</a> 
_Szegedy &amp; al. (2015). 
Going deeper with convolutions_
