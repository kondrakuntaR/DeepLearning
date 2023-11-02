# Activation Functions
They help a network model complex relationships within the data. Activation functions introduce non linearities while training and influence the activation of the neuron's output.

#### Common activation functions
1. Sigmoid
2. TanH
3. ReLU

## Sigmoid Activation
Also called Logistic activation is common used for binary classification problems. It outputs probabilities in the range (0,1).
$$f(x)=\frac{1}{1+e^{-x}}$$
It is prone to vanishing gradients
## TanH Activation
Often used in Recurrent Neural Networks (RNNs). It outputs probabilities in the range of (-1,1).
$$f(x)=\frac{e^x-e^{-x}}{e^x+e^{-x}}$$

## ReLU Activation
ReLU introduces non-linearity that helps learn complex relationships within the data.
$\sigma{(x)}=ReLU(x):= max\{0,x\}$

Exponential Linear Unit handle dying ReLU limitation (outputs input x if positive and 0 if input is negative). Unlike ReLU, ELU has non-zero gradients for negative values.