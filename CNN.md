# PaperReading


## 计算机视觉 - CNN

### AlexNet
 **Why AlexNet Matters**
AlexNet marked a turning point for the field of computer vision and ignited a renewed interest in deep learning. The following are some of the key contributions that made AlexNet groundbreaking:

1. **Groundbreaking Performance (ImageNet 2012)**  
   AlexNet achieved a significant leap in performance during the 2012 ImageNet competition, reducing the error rate by a large margin compared to previous methods.

2. **CNN Popularization**  
   AlexNet helped popularize Convolutional Neural Networks (CNNs) by demonstrating their power in large-scale image classification tasks.

3. **GPU Utilization**  
   AlexNet was one of the first deep neural networks to efficiently use GPUs for training, significantly speeding up the training process and enabling the use of much deeper networks.

---
 **Architecture Innovations**

 **1. ReLU (Rectified Linear Unit)**

- **Simpler Computation**:  
  ReLU is computationally simpler than traditional activation functions like sigmoid or tanh. It simply returns the input if it's positive, or zero otherwise, making it faster to compute.

- **Mitigating Vanishing Gradients**:  
  ReLU helps alleviate the vanishing gradient problem, which is common in deep networks using activation functions like sigmoid and tanh. In these functions, the gradient can become very small as it propagates backward through the network, causing weights in early layers to update very slowly, which hampers learning. ReLU avoids this issue because its gradient for positive values is constant (i.e., it’s always 1 for positive inputs), which makes it much more effective for backpropagation.

- **Sparsity**:  
  ReLU introduces sparsity in the network, meaning that a significant portion of neurons will be inactive (outputting zero) at any given time. This not only makes the network computationally more efficient but also may help improve generalization by forcing the network to learn more robust features.

**2. Multiple Convolutional Layers**  
AlexNet utilizes multiple convolutional layers stacked together, enabling it to learn complex hierarchies of features from raw image data. This depth is one of the reasons it outperformed traditional methods based on handcrafted features.

 **3. Max Pooling**  
While Max Pooling wasn’t a new concept introduced by AlexNet, the network helped popularize its use. Max Pooling helps reduce the spatial dimensions of the feature maps, while retaining important information. The key advantage is **translation invariance**—the network becomes less sensitive to the exact position of a feature within the image, making it more robust to variations in the input.

 **4. Dropout Regularization**  
Dropout is a regularization technique where, during training, a random subset of neurons is "dropped out" (i.e., temporarily set to zero) in each iteration. This forces the network to rely on different combinations of neurons and helps prevent overfitting, improving generalization to new data.

### VGG
VERY DEEP CONVOLUTIONAL NETWORKS FOR LARGE-SCALE IMAGE RECOGNITION

VGG's arrival in 2014 built upon the success of AlexNet, which won the 2012 ImageNet competition and popularized deep learning for image recognition. 

VGG demonstrated that increasing the depth of a network while keeping the architecture simple could lead to substantial performance gains. It challenged the prevailing notion that very deep networks would be difficult to train effectively.(只需要加多几层，但每一层的filter 3*3 就行）

VGG's consistent use of 3x3 convolutional filters and the stacking of convolutional layers became a standard practice in subsequent CNN architectures. 


  
### GoogLeNet
Detailed Explain：https://viso.ai/deep-learning/googlenet-explained-the-inception-model-that-won-imagenet/


GoogLeNet had 22 layers deeper than all the previous models released， and VGGNet had 16 layers compared to AlexNet which had only 8 layers in total.

One of the key innovations of GoogLeNet is its use of inception modules. These modules allow the network to perform multiple convolutions at different scales in parallel，inspired by the idea of 'network in network,' resulted in a deeper network while keeping the computational cost manageable.
![image](https://github.com/user-attachments/assets/285aaaa1-76aa-46e4-b47e-378aaf3b4785)
Each inception module comprises several convolutional layers with varying kernel sizes (1x1, 3x3, 5x5) and a pooling operation. The outputs of these parallel operations are then concatenated, allowing the network to learn a richer representation of the input image.


the key features of GoogLeNet:

- Inception Module
- The 1×1 Convolution
- Global Average Pooling
- Auxiliary Classifiers for Training



