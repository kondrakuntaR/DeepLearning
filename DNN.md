# Deep Neural Networks
Can machines thinks?
Can they perform task the way humans do? Classify images, understand natural language, can they be creative?

DNNs have been implement to solve various tasks such as image classification, segmentation, text summarization, classification, natural language translation etc.

#### Contents
1. Feedforward Neural Networks
2. Backpropogation
3. Vanishing and Exploding Gradients
4. Initializations
5. Residual Connections
6. Batch Normalization

## Feedforward Neural Networks
Also called as deep feedforward networks or multilayer perceptrons (MLPs) aim to approximate a function $f^*$ with input $x$ and output $y$.

They define mapping $y=f^*(x,\theta)$, where the network learns values of the parameters $\theta$ to arrive at the best function approximation.

Consider three functions $f^{(1)}, f^{(2)}, f^{(3)}$ connected in chain, then $f(x)=f^{(3)}(f^{(2)}(f^{(1)}(x)))$ where $f^{(1)}$ is first layer, $f^{(2)}$ is second layer and so on.

The length of the chain is the depth of the network, the last layer is called the output layer, intermediate layers are called hidden layers and the dimensionality of the hidden layers is the width of the network.

Extend the idea of linear models to non-linear functions of $x$. Non-linear transformation is represented by $\phi(x)$. Thus, $y=f(x;\theta,w)=\phi(x;\theta)^{\top} w$

If feedback connections are included where the output of the feedforward neural network is fed back into the network, then they are called recurrent neural networks.

## Backpropogation
- model with list of parameters $\theta$
- loss function to minimize $L$
- derivative of loss function w.r.t. parameters $\frac{\partial L}{\partial \theta}$
- optimizer to update parameters

#### Steps
1. Given inputs, perform forward pass through the feedforward neural network using the activation functions, initial weights and bias.
2. At the output layer, compute the loss between the predicted output and target output.
3. Perform the backprop algorithm by computing the gradient of loss wrt the weights between the output layer $l$ and pervious hidden layer $(l-1)$.
4. Update the weight by subtracting the product between learning rate (optional) and gradient value from the weight.
$\theta_{new}=\theta_{old}-lr*\frac{\partial L}{\partial \theta}$

#### Perceptron Learning Algorithm
#### Backprop Vs Perceptron

## Vanishing and Exploding Gradients
During backpropagation, when the values of the gradients become extremely *small*, then it is refered to as **vanishing gradients** and when the values of the gradients become extremely *large*, then it is refered to as **exploding gradients**.

#### Vanishing Gradients
- Difficult to converge
- Initial gradient value updates are extremely small; close to zero
- Extremely slow learning
#### Exploding Gradients
- Diverges easily
- Drastic change in weight updates

These are caused due to activation functions such as Sigmoid and TanH which limit the output to a small range, say [0,1].

This can be solved by incorporating weight initialization techniques rather than random initializations.

## Initializations
#### Xavier (Glorot) Initialization
Aim is to set the initial values of the network weights such that activations roughly have the same variance across the network. Intended for TanH and Sigmoid activations.

Initalization method samples values from a uniform/normal distribution with mean at 0.
$$fan_{avg}=\frac{fan_{in}+fan_{out}}{2}$$
Variance of normal distribution
$$\sigma^2=\frac{1}{fan_{avg}}$$
For uniform distribution $[-r,+r]$
$$r=\sqrt{\frac{3}{fan_{avg}}}$$

#### Kaiming (He) Initialization
Mainly for ReLU and its variants. Assumes the variance of the weights must be dependent on the number of input units to a neuron.

Variance of normal distribution
$$\sigma^2=\frac{2}{fan_{in}}$$
For uniform distribution $[-r,+r]$
$$r=\sqrt{\frac{6}{fan_{in}}}$$
## Residual Connections
## Batch Normalization
Normalizes the activations during training to avoid vanishing and exploding gradients.

## References
1. Goodfellow's Deep Learning Textbook
2. [Backpropagation Implementation - example](https://mattmazur.com/2015/03/17/a-step-by-step-backpropagation-example/)