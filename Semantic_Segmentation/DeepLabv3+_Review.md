## Encoder-Decoder with Atrous Separable Convolution for Semantic Image Segmentation

# Summary

### In 3~5 sentences, describe the key ideas, experiments, and significance

The model proposed in this paper is DeepLabv3 +, which evolved from the DeepLabv3. This model proposes the combination of the Spatial pyramid pooling module and the advantages of Encode-decode structure. In addition, DeepLabv3+ used the Xception model(Inception with separable convolution) to make the model faster and stronger rather than using ResNet-101. Finally, they decrease computational complexity from 33% to 41% by using the depthwise separable convolution.



# Strengths

### What are the strengths of the paper? Clearly explain why these aspects of the paper are valuable

There are three strengths of this paper. Firstly, the Spatial pyramid pooling module and the advantages of Encode-decode structure were combined to present a better performance model. DeepLabv3 which is the previous model of DeepLabv3 +, used only the spatial pyramid pooling module. However, DeepLabv3 + uses the Encoder-decoder structure to gradually recover spatial information to more accurately capture the boundary of the object.

Secondly, the Xception model was used as the model's backbone network. The Xception model showed good performance with fast computation in image classification using ImageNet. In addition, the MRSA team improved it to suit object detection. In view of this, in this paper, the Xception model was improved to perform the semantic segmentation task. Through this, the performance could be improved by about 2% than when using ResNet-101 as a backbone network.

Lastly, the depthwise separable convolution made the encoder-decoder faster and more accurate. The model was designed to effectively reduce the parameters through depthwise separable convolution. Through this, it was possible to reduce the computational complexity from 33% to 41% while maintaining the mIOU performance at a similar level.

Through this, DeepLabv3 + showed 89.0% and 82.1% of the test data of PASCAL VOC 2012 and Cityscapes, respectively, without post-processing. In comparison, it was found that the performance of the previous model DeepLabv3 increased from 86.9% and 81.3%, respectively.



# Weaknesses

### What are the weaknesses of the paper? Clearly explain why these aspects of the paper are weak. Please make the comments very concrete based on facts (e.g. list relevant citations if you feel the ideas are not novel)

When compared to DeepLabv3, DeepLabv3 + added an Encode-decode structure to facilitate spatial information recovery and improved performance by adding an Xception model as a backbone network instead of ResNet-101. However, I think that the improvement in performance is not satisfactory because performances are increased only 2.1% and 0.8% for PASCAL VOC 2012 and Cityscapes test data compared to the increasing complexity of the model by adding methods.



# Why accepted

### If the paper has been accepted, why do you think its accepted?

The model DeepLabv3 in this paper is the latest version of the DeepLab Series which shows good performance in semantic segmentation. Xception was used as the backbone architecture to improve performance instead of ResNet, which was the backbone of the previous model DeepLabv3. Also, they use Encoder-decoder structure to supplement the weakness of DeepLabv3 which uses bilinear upsampling as a decoder to improve performance. All of these improvements are why I think this paper was accepted.
