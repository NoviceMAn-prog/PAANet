# PAANet: Progressive Alternating Attention for Automatic Medical Image Segmentation
This repository provides code for our paper "PAANet: Progressive Alternating Attention for Automatic Medical Image Segmentation" accepted for IEEE BIOSMART 2021([arxiv version](https://arxiv.org/abs/2111.10618))  
## 2.) Overview
### 2.1.)Introduction

In this work, we introduce a novel progressive alternating attention dense block (PAAD). After each convolutional layer in the dense block, a mini-decoder is used to generate a guiding attention map (GAM). The successive layers utilize this segmentation map to prune features impertinent to identifying the region of interest. Additionally, we use reverse attention in every alternative PAAD block which allows layers to further mine peripheral features allowing the network to accurately capture the variation in shape and size of the region of interest. Since the GAM is created after every convolutional layer of the PAAD blocks, they are updated progressively which further refine the quality of feature maps, prune irrelevant features, and allow the later convolutional layers to produce only meaningful features. We validate our method on three different biomedical datasets: Data Science Bowl (DSB) 2018, ISIC 2018 skin lesion segmentation, and Kvasir-Instruments.


## 2.2.) The architecture of our Progressive Alternative Attention Dense (PAAD) block
![]()

## 2.3.) Overview of the complete PAANet architecture
![]()

## 3.) Training and Testing
## 3.1)Data Preparation
1.) make directory named "data/kins"

2.) make two sub-directories "train" and "test"

3.) Put images under directory named "images"

4.) Put masks under directory named "masks"

## 3.2)Training
Model architecture is defined in `model_bio.py`
Run the script as:
`python paanet_train.py`

## 3.2)Testing
For testing the trained model run:
`python paanet_test.py`
