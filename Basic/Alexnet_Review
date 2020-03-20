# Summary

### In 3~5 sentences, describe the key ideas, experiments, and significance

Alexnet is a basic CNN architecture that won the ILSVRC competition in 2012. Basically, it is similar in structure to LeNet-5, the ancestor of CNN, but it has been improved by using two GPUs in parallel and using ReLU activation function instead of sigmoid activation function. This paper is a meaningful because using of GPU in CNN has become popular after Alexnet.


# Strengths

### What are the strengths of the paper? Clearly explain why these aspects of the paper are valuable

I think the reason why AlexNet is important is it uses the GPU and the ReLU function. First of all, two GPUs were used as parallel architectures to solve the problem of requirement of many computational resources. The GPU used in AlexNet is the NVIDIA GTX580, which has 3GB of memory but it is insufficient to handle 1.2 million data, so they used two GPUs.

Another difference from LeNet-5 is that Alexnet uses the ReLU function instead of the Tanh function used in LeNet-5. ReLU stands for rectified linear unit, and has the strength of being six times faster while maintaining the same accuracy as the Tanh function. This ReLU function has also been preferred since AlexNet.

Other methods such as dropout, data augmentation, and overlapping pooling are used to minimize overfitting. This shows that when using ImageNet, the top-1 error rates are 37.5% and the top-5 error rates are 17.0%. In the ILSVRC-2010 competition, the top-1 error rates are 47.1% and the top-5 error rates are 28.2% It can be seen that improvements have been made.


# Weaknesses

### What are the weaknesses of the paper? Clearly explain why these aspects of the paper are weak. Please make the comments very concrete based on facts (e.g. list relevant citations if you feel the ideas are not novel)

This paper has been influential because of using GPU for CNN or using ReLU activation function after AlexNet. However, some of the methods used in this paper are not currently used. One of them is grouped convolution. This method was used because two GPUs were used in parallel in AlexNet. However, it is simpler and more effective to use convolution in general form. Moreover the performance of GPU has been improved. Therefore, the grouped convolution approach is no longer used.

Also, local response normalization, which is used to adjust the output value in this paper, is not used at present. Improvements in activation functions and the appearance of batch normalization make LRN an inefficient method. Thus LRN is rarely used in modern architectures.


# Why accepted

### If the paper has been accepted, why do you think its accepted?

It is a paper that laid the foundation of Deep Learning. Additionally, it is influential in that it uses GPU and ReLU activation function to improve performance. So I think this paper would have been accepted.
