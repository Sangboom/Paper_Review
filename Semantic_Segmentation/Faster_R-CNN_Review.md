## Faster R-CNN: Toward Real-Time Object Detection with Region Proposal Network

# Summary

### In 3~5 sentences, describe the key ideas, experiments, and significance

The model of this paper, Faster R-CNN, is meaningful in that it reduced the amount of computation and make it faster by improving the previous versions of R-CNN and Fast R-CNN. Fast R-CNN uses one ConvNet and reduces the computational amount compared to R-CNN, but it is still slow and requires a lot of computation because of selective searching. Therefore, in order to solve this, Faster R-CNN used Region Proposal Networks (RPN) rather than selective searching, and through this, it could be closer to Real-Time Object Detection.

---

# Strengths

### What are the strengths of the paper? Clearly explain why these aspects of the paper are valuable

The strength of this paper is to shorten the time for object detection by reducing the amount of computation. Region Proposal Networks (RPN) was the most contributing factor. By using RPN, selective searching can be disabled and this can save time.

The principle that Faster R-CNN works starts with using a pretrained Convolutional Network with ImageNet. Secondly, by using feature map information of ConvNet, we learn RPN, which is a network that has the location of the object as an output, and extract the region proposal. Thirdly, learning Fast R-CNN based on ConvNet by using extracted region proposal. Fourthly, the RPN model is obtained by learning the RPN with all the conv features of the Fast R-CNN models fixed. Fifthly, the region proposal is extracted again using the RPN model. Lastly, Fast R-CNN model is trained while the conv feature of the RPN model is fixed. In this way, RPN and Fast R-CNN are alternately learned.

R-CNN family isn't the only object detector based on CNN. However, among them, R-CNN has attracted the most attention from researchers and is widely used. In fact, Faster R-CNN is superior in performance and speed to other types of object detectors.

---

# Weaknesses

### What are the weaknesses of the paper? Clearly explain why these aspects of the paper are weak. Please make the comments very concrete based on facts (e.g. list relevant citations if you feel the ideas are not novel)

According to the principle mentioned in the strengths, the structure of R-CNN is a form in which RPN and Fast R-CNN alternately learn. However, this process is so complex that it actually seems inefficient in learning. Therefore, I think this complex structure is the Weakness of Faster R-CNN.

---

# Why accepted

### If the paper has been accepted, why do you think its accepted?

As mentioned in Strength, the influence of the R-CNN family in object detection field is significant. In particular, the Faster R-CNN introduced in this paper complements the shortcomings of the existing R-CNN and shows better performance than other object detectors. Besides, it is being used in various fields. Thus, I think this paper has been accepted.
