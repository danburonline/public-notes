#core/machinelearning

[[Common statistical issues|Statistical]] hypothesis testing is a key aspect of both statistics and data science that allows us to make inferences about populations based on samples. One important concept within this area is the distinction between one-tailed and two-tailed tests.

![[one-tailed-two-tailed.jpg]]

## One-Tailed Test

A one-tailed test is a statistical test in which the critical area of a distribution is one-sided so that it is either greater than or less than a certain value, but not both.

If the sample being tested falls into the one-sided critical area, the alternative hypothesis will be accepted instead of the null hypothesis.

**Key Points:**
- Used when the direction of the test statistic is known (e.g., you expect one group to have higher scores than another group).
- More powerful than a two-tailed test, as all the statistical power is in one direction.
- The critical region is only in one tail of the distribution.

## Two-Tailed Test

A two-tailed test is a statistical test in which the critical area of a distribution is two-sided and tests whether a sample is greater than or less than a certain range of values.

If the sample being tested falls into either of the critical areas, the alternative hypothesis is accepted instead of the null hypothesis.

**Key Points:**
- Used when the direction of the test statistic is not known (e.g., you only expect there to be a difference).
- Less powerful than a one-tailed test, as the statistical power is split between two directions.
- The critical region is in both tails of the distribution.

## Comparison

**One-Tailed Test:**

```
|-----------------------|-----------------------|
| Null Hypothesis (H0) | X ≤ μ                 |
| Alt. Hypothesis (H1) | X > μ or X < μ        |
|-----------------------|-----------------------|
```

**Two-Tailed Test:**

```
|-----------------------|-----------------------|
| Null Hypothesis (H0) | X = μ                 |
| Alt. Hypothesis (H1) | X ≠ μ                 |
|-----------------------|-----------------------|
```

> [!example]
> Consider an example where a researcher wants to test if a drug has an effect on patients’ health:
> - If the researcher hypothesises that the drug will improve patients’ health, they will use a one-tailed test.
> - If the researcher hypothesises that the drug will either improve or deteriorate patients’ health, they will use a two-tailed test.
