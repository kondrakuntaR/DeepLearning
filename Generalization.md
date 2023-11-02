# Improve Generalization in Deep Neural Networks
#### Contents
1. Holdout tests
2. Weight sharing
3. Invariants and Equivariances
4. L1 regularization
5. L2 weight decay
6. Dropout
7. Early stopping
8. Data augmentation

## Holdout tests
Method to evaluate performance of a predictive model. Divide the dataset into portions as train, test and validation sets. By doing so, model's performance on unseen data can be assessed.

## Weight Sharing
Same set of filters are used across entire input allowing the network to be translation-invariant.
## Invariance
When there is no effect of transformation on the output of a function. A function $f(x)$ is said to be invariant to translation $a$ if $f(x)=f(x+a)$.

Example, recognizing objects irrespective of their position, scale, orientation in a given image.
## Equivariances
A system is equivariant if it transforms in a consistent manner. If a function is equivariant to transformation then $f(T(x))=T(f(x))$.

Example, CNNs are equivariant, if the input is shifted by x, the feature maps are shifted by x as well. This helps the network to learn local features insensitive to position.
# Regularization Techniques
These techniques help prevent overfitting and improve generalization
### L1 regularization
L1 regularization also called LASSO (Least Absolute Shrinkage and Selection Operator) encourages model sparsity. It does so by updating weights of least important features to be zero.

L1 regularization term $\lambda*\sum{|w_i|}$ is sum of absolute values of weights scaled by regularization strength $\lambda$.
### L2 regularization - Weight decay
L2 regularization also known as weight decay prevents overfitting. A penalty term is added to the loss function to keep the weights small during training.

The L2 regularization term $\lambda*\sum{w_i^2}$ is the sum of squared weights $w_i$ and it is scaled by regularization strength $\lambda$.
### Dropout
Makes a set of neurons inactive in the hidden layers and trains. This helps avoid overfitting and generalizes better.
### Early stopping
Monitors the loss on validation set and stops training when the model starts to overfit.
### Data Augumentation
Introduces data that is transformed such as rotated, flipped, scaled etc. This helps the model in generalizing.

Other techniques include denoising, weight clipping, gradient clipping, weight tying (typically in CNN), pruning.