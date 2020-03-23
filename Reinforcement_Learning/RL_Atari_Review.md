# Summary

### In 3~5 sentences, describe the key ideas, experiments, and significance

It is the first deep learning to learn successfully control policies from high dimensional sensory input using Reinforcement Learning. This paper aims to connect RL algorithm to DNN which processes training data using SGD and get RGB image input directly. Learning is performed using experience replay, which stores the experiences of agents at each time step. As such, performance using DQN outperformed all previous approaches in six of the seven games, and outperformed human in three of them.



# Strengths

### What are the strengths of the paper? Clearly explain why these aspects of the paper are valuable

As mentioned earlier, this is the first deep learning to learn successfully control policies from high dimensional sensory input using Reinforcement Learning. Previously, RL applications were dependent on hand-crafted features with linear value functions or policy representations. In other words, the performance of the RL application depends on the quality of the feature representation. However, with the development of DL, it has become possible to extract high-level features from raw sensory data in computer vision or speech recognition.

There is a reason why DL has not been used in RL so far. The first is to use hand-labeled training data in DL, whereas most of the RL algorithm learns from sparse, noisy and delayed scalar reward signals. Second, most DL algorithms learn from independent data samples, while the RL algorithm handles correlated states. In addition, it can be problematic because DL deals with fixed distributions, while RL is an algorithm for learning new behaviors.

In this paper, we have verified successful learning of control policies from raw video data of complex RL environments using CNN. This network using CNN is a variation of the Q-learning algorithm using Stochastic Gradient Descent (SGD) to update weights. We also used the experience replay mechanism to alleviate the problems of correlated data and non-stationary distribution. This saves previously learned data and uses it as a random sample, which makes the training distribution smooth.

Through this, Atari 2600 games were learned using Deep Q-learning (DQN). As a result, the experience of each step is potentially used for more weight updates and has better data efficiency. Also, learning from successive samples is not sufficient because there are many correlations, so random sampling of samples reduces this change while eliminating these conflicts. In addition, the behavior distribution is averaged over many previous states because the experience repaly avoids the oscillation or divergence of parameters and the learning is smooth.

As a result of learning through this study, DQN showed higher performance than all existing methods in 6 games(B.Rider, Breakout, Enduro, Pong, Q * bert, and Seaquest) except S.Invaders. Among them, It showed higher performance than human with Breakout, Enduro, Pong.



# Weaknesses

### What are the weaknesses of the paper? Clearly explain why these aspects of the paper are weak. Please make the comments very concrete based on facts (e.g. list relevant citations if you feel the ideas are not novel)

When learning in this way, it stores up to the maximum amount of replay memory and draws randomly from the stored amount. In other words, the memory buffer does not distinguish between important transitions. Also, because of finite memory size N, overwriting is a disadvantage of this model.

In addition, the game S.Invaders is showing a lower performance than the HNeat method, so it needs to be analyzed.



# Why accepted

### If the paper has been accepted, why do you think its accepted?

I think that this paper is acceptable because authors have presented a methodology for using DNNs in RL and the way that CNN automatically generates features using only image sequences without any hand craft features. Also, they use only one neural network to learn the policy for seven different Atari games and the results outperform the existing ones. Thus I think this paper is meaningful.
