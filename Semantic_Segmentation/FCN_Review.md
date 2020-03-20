## Fully Convolutional Networks for Semantic Segmentation

# Summary

### In 3~5 sentences, describe the key ideas, experiments, and significance

This paper is important because it is the first use of deep learning for segmentation problems. They transformed the convolutional network that is frequently used in computer vision fields and used it for semantic segmentation. They construct a network by replacing the fully-connected layer existing in the rear part of the CNN with a 1x1 convolution layer to preserve the location information of the feature map. It also improves the segmentation result image using a skip connection.


# Strengths

### What are the strengths of the paper? Clearly explain why these aspects of the paper are valuable

Firstly, when using the standard CNN, the location information of the feature map disappears due to the FC layer located rear of the CNN. Therefore, in this paper, they solved by changing the FC layer to a 1x1 convolutional layer. The result of this 1x1 convolutional layer is classified on the feature map of each class, and segmentation can be possible.

Secondly, this paper solved the problem that output is smaller than the input. They solved this problem using a method called deconvolution or upsampling. By multiplying the inverse kernel of the input image to the output, they increased the output size.

Input image comes in and Convolution operation continues. When upsampling in 5th pooling (1/32) upsampling is done 32 times, so the detail must be lost. To solve this problem, they use the skip connection technique using the feature map of the previous layer. In the deep layer of the convolutional network, we can obtain a global feature, which is a certain feature of the object. However, the shallow layer shows local features such as curves and straight lines, the performance of segmentation can be improved by using this.


# Weaknesses

### What are the weaknesses of the paper? Clearly explain why these aspects of the paper are weak. Please make the comments very concrete based on facts (e.g. list relevant citations if you feel the ideas are not novel)

In the FCN model, the amount of information is reduced because subsampling occurs. For this reason, restoration cannot be done well. In addition, the task of picking up the outline does not work well because the information has been reduced.


# Why accepted

### If the paper has been accepted, why do you think its accepted?

I think the reason why this paper was accepted is that it was the first attempt to solve the segmentation problem through DNN, especially by tuning the standard CNN models. It is good that the performance improvement through the configuration of the fully convolutional network and skip connection.
