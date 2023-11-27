# Integrated-Gradient-Attribution-for-features-of-DeepLearning-Models
Understanding and Implementation of Integrated Gradients attribution for feature analysis and debugging model performance.

# Attribution Methods
Attribution methods are techniques used to understand the contribution of each input feature to the model's output.
It is a part of Explainable AI where we tend to make the model understanding more better.


# Integrated Gradients
Specifically, Integrated gradients are defined as the path intergral of the gradients along the straightline path from the baseline x0 to the input x.

*******************************************
# How to know if it is better attribution method or not ?

This attribution method satisfy the axiomatic properties like:
1. Sensitivity
2. Implementation Invariance

Integrated Gradients also preserves linearity within the network.

Without these axiomatic approach, It is difficult to know whether the attribution method is affected by data artifacts, netowrk artifacts or method artifacts

*******************************************
![](https://github.com/joshir199/Integrated-Gradient-Attribution-for-features-of-DeepLearning-Models/blob/main/images/real%20ballon%20images.png)


![](https://github.com/joshir199/Integrated-Gradient-Attribution-for-features-of-DeepLearning-Models/blob/main/outputs/baseline%20images.png)


![](https://github.com/joshir199/Integrated-Gradient-Attribution-for-features-of-DeepLearning-Models/blob/main/outputs/Integrated%20gradients%20for%20ballon%20image.png)


******************************************

Research Paper reference : Axiomatic Attribution for Deep Networks,  https://arxiv.org/abs/1703.01365

For better readability and understanding, refer to the paper with highlighted points: [here](https://github.com/joshir199/Integrated-Gradient-Attribution-for-features-of-DeepLearning-Models/blob/main/Paper_with_highlighted_points.pdf)

# Use Cases : 

1. Debugging Model Performance (only for model which are differentiable)
2. Debugging Data Skewness
3. Pixel distribution understanding in case of Image model

# Tools:
Captum is the python library that can be used for calculating Integrated Gradients and understanding models using visualization techniques.

It supports other attribution techniques like SHAP, DeepLift etc.
For more detailed info, refer here : https://captum.ai/
