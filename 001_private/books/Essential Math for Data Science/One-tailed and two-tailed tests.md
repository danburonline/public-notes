#core/artificialintelligence

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

|                   | One-Tailed Test                 | Two-Tailed Test                  |
|-------------------|---------------------------------|----------------------------------|
| **Null Hypothesis ($H_0$)**  | $\mu = \mu_0$                      | $\mu = \mu_0$                      |
| **Alternative Hypothesis ($H_1$)** | $\mu > \mu_0$ or $\mu < \mu_0$         | $\mu \ne \mu_0$                       |
| **Critical Region**              | Only one tail (left or right)     | Both tails                          |
| **Use Case**           | Direction is specified              | Direction is not specified           |
| **Statistical Power**           | Higher (all in one direction)     | Lower (split between two directions) |
| **Example**               | Test if mean is greater than a value | Test if mean is different from a value |

> [!example]
> Consider an example where a researcher wants to test if a drug has an effect on patients’ health:
> - If the researcher hypothesises that the drug will improve patients’ health, they will use a one-tailed test.
> - If the researcher hypothesises that the drug will either improve or deteriorate patients’ health, they will use a two-tailed test.
