#core/machinelearning #core/appliedneuroscience

## Overview

The Student’s t-test is a **statistical test used to compare the means of two groups.** It helps determine if there are significant differences between the two groups.

## Types of t-Tests

1. **One-Sample t-Test**
   - Compares the mean of a single group against a known mean.
2. **Independent Two-Sample t-Test**
   - Compares the means of two independent groups.
3. **Paired Sample t-Test**
   - Compares means from the same group at different times (e.g., before and after a treatment).

## Assumptions

- **Normality**: Data should be approximately normally distributed.
- **Independence**: Observations should be independent of each other.
- **Homogeneity of variance**: The variances in the two groups should be approximately equal.

## Formula

The basic formula for a t-test is:

$$
 t = \frac{\bar{x}_1 - \bar{x}*2}{s*{\bar{x}_1 - \bar{x}_2}}
$$

## Interpretation

- **[[P-value]]:** Used to determine the significance of the results.
  - A small [[P-value]] (typically ≤ 0.05) indicates strong evidence against the null hypothesis, so you reject the null hypothesis.
  - A large [[P-value]] (> 0.05) indicates weak evidence against the null hypothesis, so you fail to reject the null hypothesis.

> [!example]
> Used in research fields to compare:
> - Test scores
> - Medical treatment effects
> - [[Cognitive-behavioural therapy|Behavioural]] changes
