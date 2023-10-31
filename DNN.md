# Deep Neural Networks
Can machines thinks?
Can they perform task the way humans do? Classify images, understand natural language, can they be creative?

DNNs have been implement to solve various tasks such as image classification, segmentation, text summarization, classification, natural language translation etc.

#### Concepts Covered
1. Feedforward Neural Networks
2. Backpropogation

## Feedforward Neural Networks
Also called as deep feedforward networks or multilayer perceptrons (MLPs) aim to approximate a function $f^*$ with input $x$ and output $y$.

They define mapping $y=f^*(x,\theta)$, where the network learns values of the parameters $\theta$ to arrive at the best function approximation.

Consider three functions $f^{(1)}, f^{(2)}, f^{(3)}$ connected in chain, then $f(x)=f^{(3)}(f^{(2)}(f^{(1)}(x)))$ where $f^{(1)}$ is first layer, $f^{(2)}$ is second layer and so on.

The length of the chain is the depth of the network, the last layer is called the output layer, intermediate layers are called hidden layers and the dimensionality of the hidden layers is the width of the network.

Extend the idea of linear models to non-linear functions of $x$. Non-linear transformation is represented by $\phi(x)$. Thus, $y=f(x;\theta,w)=\phi(x;\theta)^{\top} w$

If feedback connections are included where the output of the feedforward neural network is fed back into the network, then they are called recurrent neural networks.

## Backpropogation


### References
[1] Goodfellow's Deep Learning Textbook



