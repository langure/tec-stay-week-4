# Week 4: Maximum Likelihood Estimation (MLE)

Maximum Likelihood Estimation (MLE) is a statistical method used for estimating the parameters of a statistical model. The key idea behind MLE is to find the set of parameters that makes the observed data most probable under the assumed statistical model.

For any given model, there can be multiple sets of parameters that can describe the data. MLE provides a principled method to find the "best" set of parameters that maximizes the likelihood of the data.

Let's illustrate this concept with a simple example: flipping a coin.

Example: Coin Flipping
Suppose we have a coin and we want to find out if it's fair (i.e., P(heads) = 0.5) or if it's biased. We flip the coin 100 times and observe 60 heads and 40 tails.

Our statistical model in this case is the Binomial distribution, which describes the number of successes (heads, in our case) in a fixed number of independent Bernoulli trials (coin flips) with the same probability of success. The parameter we want to estimate is the probability of heads, which we'll denote by p.

The likelihood function for this model and data is the probability of observing 60 heads and 40 tails given p, which according to the binomial distribution, is given by:

L(p; data) = C(100, 60) * p^60 * (1-p)^40

Where C(100, 60) is the number of combinations of 100 items taken 60 at a time.

The MLE of p is the value that maximizes this likelihood function. In this case, you can show (using calculus or a computational optimizer) that the MLE for p is 0.6, which is exactly the proportion of heads that we observed. This makes intuitive sense: the most probable value for the probability of heads, given our data, is the observed proportion of heads.

This is a very basic example, but the principle of MLE is used in much more complex situations, from estimating parameters for complex statistical models in economics, to training parameters in machine learning models like logistic regression and neural networks.

# Readings

[Tutorial on maximum likelihood estimation](https://citeseerx.ist.psu.edu/document?repid=rep1&type=pdf&doi=4ab2cfe6766a5007b2fcf8cfffbf7fb566c077f4)


[Bias reduction of maximum likelihood estimates](https://www2.stat.duke.edu/~scs/Courses/Stat376/Papers/GibbsFieldEst/BiasReductionMLE.pdf)

[Maximum likelihood estimation of logistic regression models: theory and implementation](https://saedsayad.com/docs/mlelr.pdf)

