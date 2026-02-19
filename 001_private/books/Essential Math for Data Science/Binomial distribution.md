#core/artificialintelligence #core/mathematicalphysics

![binomial-distribution](../../../_inbox/attachments/binomial-distribution.jpg)

The binomial distribution is a **probability distribution with two possible outcomes** (hence the term “bi” in binomial). In statistics, it’s used to model events in a fixed number of trials of a random experiment.

## Definition

If an experiment is repeated `n` times, where each trial is independent of all others and leads to success with probability `p` and failure with probability `1-p`, then the random variable `X` that counts the number of successes has a binomial distribution. This is typically denoted as `X ~ B(n, p)`.

The probability mass function (PMF) of a binomial distribution is given by:

```
P(X = k) = C(n, k) * (p^k) * ((1 - p)^(n - k))
```

Where:

- `P(X = k)` is the probability of `k` successes in `n` trials,
- `C(n, k)` is the binomial coefficient (also known as “n choose k”, the number of ways to choose `k` successes from `n` trials),
- `p^k` is the probability of getting `k` successes,
- `(1 - p)^(n - k)` is the probability of getting `n - k` failures.

## Mean and Variance

The **mean** (expected value) and **variance** of a binomial distribution are:

- Mean: `μ = n*p`
- Variance: `σ^2 = n*p*(1 - p)`

## Assumptions

To apply the binomial distribution, the following assumptions must hold:

1. **Binary Outcome**: Each trial results in one of two possible outcomes (success or failure).
2. **Fixed Number of Trials**: The number of trials (n) is fixed.
3. **Independence**: The outcome of any trial is independent of the outcomes of all other trials.
4. **Constant [Probability](Probability%20approaches.md)**: Each trial’s probability of success (p) is the same.

## Applications

The binomial distribution is widely used in statistics and data analysis. Some applications include:

- Predicting the outcomes of elections or sports games.
- Quality control in manufacturing processes.
- Modelling conversion rates in marketing campaigns.

 > [!example]  Example: Calculating Binomial Probability
> Suppose you flip a fair coin ($p = 0.5$) 10 times ($n = 10$). What is the probability of getting exactly 6 heads (successes)?
> 
> $$
> P(X = 6) = C(10, 6) \times (0.5^6) \times (0.5^{4}) = \frac{10!}{6!4!} \times 0.5^{10}
> $$
> 
> This calculation gives the probability of observing exactly 6 heads in 10 coin tosses.