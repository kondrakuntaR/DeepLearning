# Cost Functions
Objective functions i.e Cost/Loss functions are used to assess model performance by providing a quantitaive measure. The goal is to minimize cost functions during optimization and model training.
#### Contents
1. Cross-Entropy Loss
2. KL Divergence
3. Distribution Matching
4. L2 Reconstruction Loss
5. L1 Median-finding Loss

## Cross-Entropy Loss
Also known as **Log Loss** is often associated with softmax classification. Widely used in binary and multi-class classification problems. Loss function penalizes incorrect predictions by increasing loss.

Categorical Cross-Entropy is used for multi-class problems.

## KL Divergence
Kullback-Leibler Divergence is measure of how approximation probability distribution differs from the target distribution.

## Distribution Matching
Aims to make two or more probability distributions similar to each other.

Applications include domain adaptation, transfer learning etc. 

Techniques include Maximum Mean Discrepancy (MMD), Kernel Mean Matching (KMM), Generative Adversarial Networks (GANs), Variational Autoencoders (VAEs).
## L2 Reconstruction Loss
Also known as Mean Squared Error (MSE). Sensitive to outliers as large prediction error is penalized strongly due to squaring.

## L1 Median-finding Loss
L1 Norm is the sum of magintude of vectors in space. It is also called the Manhattan Distance where distance is calculated from a data point wrt to L1 median.

## References
1. [Binary Cross-Entropy](https://www.analyticsvidhya.com/blog/2021/03/binary-cross-entropy-log-loss-for-binary-classification/)
