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


*******************************
# Vision Transformer (ViT) vs Convolution Networks (ResNet, AlexNet, ConvNet)

ViTs are designed in different architectural way than previously designed Convolution Nets.

ViTs are inherently robust to many kinds of adversarial perturbations and corruptions.

After understanding the neurons activation for given tasks of classifications.

1. ViTs are similar to CNNs in that they show a feature progression from textures to parts to objects as we progress from shallow to deep features.

  ![](https://github.com/joshir199/Integrated-Gradient-Attribution-for-features-of-DeepLearning-Models/blob/main/images/feature%20learning.png)
  
2. ViTs preserve spatial information of the patches even for individual channels across all layers with the exception of the last layer, indicating that the networks learn spatial relationships from scratch.
   Furthermore, the final layer in ViTs appears to behave as a learned global pooling operation that aggregates information from all patches, which is similar to its explicit averagepooling counterpart in CNNs.
   token). It is possible that the network globalizes information in the last layer to ensure that the CLS token has access to the entire image.

  ![](https://github.com/joshir199/Integrated-Gradient-Attribution-for-features-of-DeepLearning-Models/blob/main/images/feature_across_layers.png)
  
3. ViTs are significantly better than CNNs at using the background information in an image to identify the correct class. While the predictions of ResNets suffer greatly when high-frequency texture information is removed (using low-pass filtering) from their inputs, ViTs are seemingly resilient. CNNs are more dependent on high frequency textural image information than ViTs.

 ![](https://github.com/joshir199/Integrated-Gradient-Attribution-for-features-of-DeepLearning-Models/blob/main/images/low-pass%20filtering%20comparision.png)
 
4. ViTs trained with language model supervision learn more semantic and conceptual features like also modifying phrases like prepositions and epithets, rather than (noun based) object-specific visual features as is typical of classifiers.


For Reference: https://colah.github.io/
******************************
# Use Cases : 

1. Debugging Model Performance (only for model which are differentiable)
2. Debugging Data Skewness
3. Pixel distribution understanding in case of Image model

# Tools:
Captum is the python library that can be used for calculating Integrated Gradients and understanding models using visualization techniques.

It supports other attribution techniques like SHAP, DeepLift etc.
For more detailed info, refer here : https://captum.ai/
