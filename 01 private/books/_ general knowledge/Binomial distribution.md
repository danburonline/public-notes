#core/mathematicalphysics #core/machinelearning

A Binomial Distribution is a probability distribution that describes the number of successes in a fixed number of independent Bernoulli trials, each with the same probability of success.

## Formula

The probability mass function of a Binomial Distribution is given by:

```
P(X=k) = C(n, k) * (p^k) * ((1−p)^(n−k))
```

Where:
- `P(X=k)` is the probability of `k` successes in `n` trials
- `C(n, k)` is the binomial coefficient, which can be calculated as `n! / [k!(n-k)!]`
- `p` is the probability of success on any given trial
- `n` is the number of trials
- `k` is the number of successes

## Example

Let’s consider a simple example: tossing a coin.

Suppose we toss a fair coin (where the probability of getting heads, `p`, is 0.5) 10 times. What’s the probability that we get exactly 6 heads?

Using the formula for the binomial distribution, we can calculate this as follows:

```
P(X=6) = C(10, 6) * (0.5^6) * ((1−0.5)^(10−6))
```

First, calculate `C(10, 6)`, the number of ways to choose 6 successes from 10 trials:

```
C(10, 6) = 10! / [6!(10-6)!] = 210
```

Now, substitute `C(10, 6)`, `p`, `n`, and `k` into the formula:

```
P(X=6) = 210 * (0.5^6) * ((1−0.5)^(10−6))
       = 210 * 0.015625 * 0.0625
       = 0.205078125
```

So, the probability of getting exactly 6 heads in 10 tosses of a fair coin is approximately 0.205.
