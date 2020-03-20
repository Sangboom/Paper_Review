## Rethinking Atrous Convolution for Semantic Image Segmentation
# Summary

### In 3~5 sentences, describe the key ideas, experiments, and significance

In this paper, they proposed a method to obtain a more dense feature map with DeepLabv3 that utilizes atrous convolution in the ResNet structure to improve the performance of semantic segmentation. As an encoder, ResNet with atrous convolution is used, and it is also used as a cascade module and parallel module(Atrous Spatial Pyramid Pooling (ASPP)). As a decoder, a simple bilinear upsampling technique was used. I think this paper is meaningful because they improve the performance of encoder.


# Strengths

### What are the strengths of the paper? Clearly explain why these aspects of the paper are valuable

The Atrous convolution used in the DeepLabv3, unlike the normal convolution, works with an empty space inside the filter. When the rate r = 1, which is a parameter that determines how much space is empty, it is the same as the normal convolution and the r becomes larger empty spaces become larger.

The advantage of using atrous convolution is that it can take a large field of view while maintaining the same amount of parameters and calculations as a conventional convolution. Usually, in order to achieve high performance in semantic segmentation, the size of the receptive field, which determines the size of an area that can be covered by one pixel at the end of the convolutional neural network, is important. Since the receptive field can be greatly increased without increasing the number of parameters by using atrous convolution, the DeepLab series tried to actively utilize it.

In this paper, it was confirmed that the performance increased from 20.29% to 75.18% when atrous convolution was applied to ResNet-50 as a cascade. It was also confirmed that the performance increased further when ResNet-101 was used.

As a way to improve the performance of semantic segmentation, the spatial pyramid pooling technique is frequently used. DeepLab proposes to use an atrous spatial pyramid pooling (ASPP) technique that applies atrous convolutions with different rates in parallel from the feature map, and then rejoins them. These methods help to perform more accurate semantic segmentation by implementing a multi-scale context as a model structure. DeepLab uses ASPP as a basic module.

According to the experimental results in this paper, it was confirmed that the performance can reach 77.21% when using ASPP. Thus, It has strength in greatly improving the performance of the endcoder.


# Weaknesses

### What are the weaknesses of the paper? Clearly explain why these aspects of the paper are weak. Please make the comments very concrete based on facts (e.g. list relevant citations if you feel the ideas are not novel)

In this paper, several methods were used to improve the performance of the encoder, such as using atrous convolution and using ASPP that uses atrous convolution in parallel. However, I think that it is a weakness that does not care much about the performance of the decoder that performs deconvolution using only bilinear upsampling.


# Why accepted

### If the paper has been accepted, why do you think its accepted?

Although this paper did not care about the performance of the decoder, it improved the performance of the encoder by using atrous convolution and ASPP. Also, I think this paper is about the DeepLab Series which is showing good performance is the reason why this paper accepted.
