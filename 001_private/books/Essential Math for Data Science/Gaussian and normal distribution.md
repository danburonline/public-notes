#core/machinelearning #core/mathematicalphysics 

![[normal-distribution.png]]

Gaussian Distribution, also known as **Normal Distribution**, is a type of **continuous probability distribution for a real-valued random variable.** It forms a bell-shaped curve when plotted on a graph.

## Key Points

- Normal Distribution is symmetric about the mean. A Normal Distribution's mean, median, and mode are all equal.

![[normal-dist-formula.jpg]]

- The probability density function of a Normal Distribution is:
    - `x` is a real-valued random variable
    - `µ` is the mean
    - `σ` is the standard deviation
    - `σ²` is the variance
    - `e` is the base of the natural logarithm, approximately equal to 2.71828
    - `π` is a constant approximately equal to 3.14159
- The mean (µ) and the standard deviation (σ) define the curve. The mean defines the location of the peak, and the standard deviation spreads the curve.

- About 68% of the data falls within one standard deviation, 95% within two standard deviations, and 99.7% within three standard deviations. This is known as the Empirical Rule or the 68-95-99.7 rule.

## Applications of Normal Distribution

- Normal distribution is widely used in natural and social sciences to represent real-valued random variables whose distributions are unknown.
- It’s used in statistics for hypothesis testing, confidence intervals, and is key to the concept of statistical significance.
- Many measurement-based data follow a normal distribution, including heights, weights, and intelligence scores.

## Limitations of Normal Distribution

- Not all data sets are normally distributed. Therefore, using normal distribution methods for non-normally distributed data sets can lead to inaccurate results.
- It assumes that the mean, median and mode are equal, which is not the case in every real-world scenario.
- [[Data skew|Data]] can have significant skew and kurtosis, which are not adequately represented by the normal distribution.

> [!tip]
> Remember, the normal distribution is a model; like all models, it’s a simplification of reality. Always check if your data follows a normal distribution before applying normal distribution-based methods.

> [!example]
> Let’s assume that the weight of a particular breed of dog is normally distributed with a mean weight of 30 kg and a standard deviation of 2 kg.
> - If you randomly pick a dog of this breed, there’s a 68% chance its weight will be between 28 and 32 kg (mean ± 1 standard deviation).
> - There’s a 95% chance its weight will be between 26 and 34 kg (mean ± 2 standard deviations).
> - There’s a 99.7% chance its weight will be between 24 and 36 kg (mean ± 3 standard deviations).