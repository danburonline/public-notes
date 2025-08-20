#core/mathematicalphysics

The Law of Large Numbers is a theorem in probability and statistics that suggests that **as the size of a sample increases, the sample mean will get closer and closer to the population mean.** This concept is foundational to the fields of statistics and probability.

The LLN has two versions:

1. **Strong Law of Large Numbers**: The sample average converges almost surely to the expected value. This means that the probability that the sample average differs from the expected value by more than a certain positive amount, however small, tends to zero as the sample size tends to infinity.

2. **Weak Law of Large Numbers**: The sample average converges in probability towards the expected value. This means that for every positive number, the probability that the absolute difference between the sample average and the expected value is greater than the number becomes closer and closer to zero as the sample size tends to infinity.

> [!example] Coin flips and the Law of Large Numbers
> Imagine flipping a fair coin with $P(\text{Heads})=0.5$.  
> - After $n=10$ flips, e.g. 6 Heads / 4 Tails → proportion $=0.6$ (deviates from 0.5).  
> - After $n=1000$ flips, e.g. 510 Heads / 490 Tails → proportion $=0.51$ (closer to 0.5).  
> As $n$ grows, the empirical mean converges to the theoretical mean $0.5$:  
> $$
> \hat p_n=\frac{1}{n}\sum_{i=1}^n \mathbf{1}\{\text{Heads}_i\} \to 0.5
> $$
