#core/mathematicalphysics

The Law of Large Numbers is a theorem in probability and statistics that suggests that **as the size of a sample increases, the sample mean will get closer and closer to the population mean.** This concept is foundational to the fields of statistics and probability.

The LLN has two versions:

1. **Strong Law of Large Numbers**: The sample average converges almost surely to the expected value. This means that the probability that the sample average differs from the expected value by more than a certain positive amount, however small, tends to zero as the sample size tends to infinity.

2. **Weak Law of Large Numbers**: The sample average converges in probability towards the expected value. This means that for every positive number, the probability that the absolute difference between the sample average and the expected value is greater than the number becomes closer and closer to zero as the sample size tends to infinity.

## Example

Imagine flipping a fair coin. The probability of heads is 0.5, and the probability of tails is also 0.5. Suppose we flip the coin 10 times and get 6 heads and 4 tails. The proportion of heads is 0.6, which deviates from our expected proportion of 0.5.

However, if we continue to flip the coin and get to 1000 flips, we might see 510 heads and 490 tails. The proportion of heads is now 0.51, which is closer to our expected 0.5.

If we continue this process towards an infinite number of flips, according to the Law of Large Numbers, our proportion of heads (an empirical average) will converge to the theoretical average of 0.5.
