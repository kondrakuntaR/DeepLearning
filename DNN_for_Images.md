# Deep Neural Networks for Images
#### Contents
1. Convolutional Layers
2. AlexNet
3. ResNet
4. U-Nets
5. VGG
## Convolutional Neural Networks
CNNs are mainly used for image analysis. They are widely used for image related tasks such as classification, segemntation, object detection etc.

Convolution is the process of sliding a small filter or kernel usually 3x3 size (or 5x5 or 7x7 etc) over the input image. These capture various features. Multiple filters at a layer capture various features of the input. By stacking these convolution layers, spatial features of the input image are learnt in detail.

One or more fully connected neural networks are implemented towards the end to learn high dimentional features from the CNN.

ReLU activation function is commonly used after every convolutional layer and fully connected layer to introduce non-linearity.
#### Feature Maps
Output of convolutional layers. They capture portion of features of the input image using the kernel.
#### Receptive Fields
The area of the input that influences the activation of a neuron in a convolutional layer. Influenced by kernel size and number of convolution layers.

## AlexNet
It is a deep CNN. Containf 5 convolution layers and 3 fully connected layers.
Implemented Local Response Normalization (LRN)
## Residual Networks
They implement residual connections. They aim to learn and predict the difference or residual between the desired output and current input, rather than learning to predict desired output.

## U-Nets
Designed for semantic segmentation task in computer vision.

Contracting path captures context and high-level features. Comprises of conv and max-pooling layers thus reducing spatial features and increasing feature channels.

Bottleneck contains the most critical features.

Expansive path captures pixel wise segmentation. Series of up-conv layers.