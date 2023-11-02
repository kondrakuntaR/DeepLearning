# Optimization
Three things to keep in mind while optimizing
1. Optimizer should not get stuck
2. Learn good and meaning rules, features
3. Generalize well and avoid overfitting

#### Contents
1. Exponential Moving Averages
2. Stocastic Gradient Descent
3. Momentum
4. SGD + Momentum
5. ADAM Optimizer

## Exponential Moving Averages
MA is a technical indicator to observe change in values $v$ over a period $n$ of time. 
Simple Moving Average $$SMA=\frac{v_1+v_2+v_3+...+v_n}{n}$$
Weighted Moving Average $$WMA=\frac{v_1*n+v_2*(n-1)+v_3*(n-2)+...+v_n*1}{\frac{n*(n+1)}{2}}$$
Exponential Moving Average $$EMA=v_{n+1}*w+SMA_{n}*(1-w)$$
EMA adds high weight to recent data and lower weight to past data points incorporating more importance to recent values.

SMA allocates equal weights to all values, WMA weights decrease linearly and EMA weights decrease exponentially

This is a smoothing technique.

## Stocastic Gradient Descent
This is an optimization algorithm that updates the weights/parameters of the model to minimize loss.

Update Rule:$$\theta_i=\theta_{i-1}-\gamma*g_i$$
where,

$\theta$ denotes the parameters to the cost function

$g_{i}$ is the gradient indicating which direction to decrease the cost function by

$\gamma$ is the hyperparameter representing the learning rate

## Momentum
This is a technique used to accelerate convergence of optimizers. This also smoothens the path of gradient and reduces bumps.

Overcomes local minimas and oscillation of noisy gradients.

Momentum can be introduced while optimization by introducing a momentum term to the update rule.

## SGD + Momentum
SGD converges slowly. With the help of momentum, convergence is accelerated.

Momentum Term:$$b_i=\mu*b_{i-1}+g_i$$
Update Rule:$$\theta_i=\theta_{i-1}-\gamma*b_i$$
where,

$b_{i}$ is the modified step direction term (as opposed to just using $g_{i}$) that incorporates momentum

$\mu$ is a new hyperparameter that denotes the momentum constant. Usually closer to 1, eg: 0.9, 0.99

#### SGD + Nesterov Accelerated Gradient (Nesterov Momentum)
In NAG, we use look-ahead parameters i.e. the future paramater $\theta$ to calculate the gradient used in the current momentum term. Using this momentum term, update rule is performed.

## ADAM Optimizer
Adaptive Moment Estimation or ADAM was introduced by Diedrik Kingma.
ADAM stores exponentially decaying averages of past squared gradients i.e. $v_t$ (estimate of second moment - variance) as well as exponentially decaying averages of past gradients i.e. $m_t$ (estimate of first moment - mean). Here,
$$m_t=\beta_{1}*m_{t-1}+(1-\beta_{1})*g_t$$
$$v_t=\beta_{2}*v_{t-1}+(1-\beta_{2})*{g_t}^2$$
ADAM tried to measure the size of the gradient. If mean gradient is high, ADAM decreases the learning rate. It the RMS gradient is high ADAM 

## References
1. [Momentum](https://optimization.cbe.cornell.edu/index.php?title=Momentum)
2. [Moving Averages](https://www.investopedia.com/ask/answers/071414/whats-difference-between-moving-average-and-weighted-moving-average.asp)
3. [Exponential MA in Deep Learning](https://medium.com/analytics-vidhya/understanding-exponential-moving-averages-e3f020d9d13b)