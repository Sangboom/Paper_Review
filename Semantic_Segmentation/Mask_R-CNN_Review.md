# Summary

### In 3~5 sentences, describe the key ideas, experiments, and significance

Mask R-CNN 은 Faster R-CNN을 확장시킨 모델로 Faster R-CNN을 통해 Object Detection을 한 후에 Segmentation을 진행하여 Instance Segmentation이 가능하도록 하였다. 기존 Faster R-CNN에서 사용하던 RoI Pooling이 위치정보를 잘 보존하지 못한다는 점을 개량하여 RoI Align을 사용하였다. 또한 small Fully Convolutional Network를 추가하여 RoI(region of interest)내에서 segmentation을 시행한다. 이를 통해 R-CNN이 더 다양한 computer vision task에 활용할 수 있게 되었다는 점에서 의미가 있다.

---

# Strengths

### What are the strengths of the paper? Clearly explain why these aspects of the paper are valuable

Faster F-CNN은 pixel-to-pixel alignment를 위해 설계되지 않았다. 따라서 이를 Instance Segmentation과 같은 task에 활용하기 위해 Faster R-CNN을 개량한 모델이 Mask R-CNN이다. 

---

# Weaknesses

### What are the weaknesses of the paper? Clearly explain why these aspects of the paper are weak. Please make the comments very concrete based on facts (e.g. list relevant citations if you feel the ideas are not novel)

write contents

---

# Why accepted

### If the paper has been accepted, why do you think its accepted?
