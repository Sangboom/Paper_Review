## CBAM: Convolutional Block Attention Module

# Summary

### In 3~5 sentences, describe the key ideas, experiments, and significance

In this paper, we propose a new network module, named “Convolutional Block Attention Module”. Since convolution operations extract informative features by blending cross-channel and spatial information together, we adopt our module to emphasize meaningful features along those two principal dimensions: channel and spatial axes.

---

# Strengths

### What are the strengths of the paper? Clearly explain why these aspects of the paper are valuable

- CBAM은 Attention을 cross-channel, spatial 두 가지에 적용하여 중요한 feature에 집중하고 중요하지 않은 feature는 압축한다.
- Bottoleneck 직전 배치하여, 정보량을 줄이기 전에 중요한 정보, 중요하지 않은 정보 표시
- CBAM은 간단한 구조를 가지고 있어 다양한 CNN에 활용하기 좋을 것

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/af44d8c1-2be0-45f2-a227-8132992120b4/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/af44d8c1-2be0-45f2-a227-8132992120b4/Untitled.png)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/3c571120-7c24-4c2f-928b-a0a0a9637dce/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/3c571120-7c24-4c2f-928b-a0a0a9637dce/Untitled.png)

- Channel Attention 시 SEnet과 다르게 MaxPool과 AvgPool을 조합하여 사용했다.

---

# Weaknesses

### What are the weaknesses of the paper? Clearly explain why these aspects of the paper are weak. Please make the comments very concrete based on facts (e.g. list relevant citations if you feel the ideas are not novel)

---
