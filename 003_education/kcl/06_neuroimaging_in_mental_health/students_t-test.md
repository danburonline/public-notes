#core/appliedneuroscience #core/artificialintelligence

## Overview

The Student’s t-test is a **statistical test for assessing a mean or mean difference relative to a null value.**

## Types of t-Tests

1. **One-Sample t-Test**: Compares a sample mean with a hypothesised mean.
2. **Paired Sample t-Test**: Tests the mean of within-pair differences, such as before–after differences.
3. **Pooled Independent Two-Sample t-Test**: Compares means from two independent groups while assuming equal population variances.
4. **Welch Independent Two-Sample t-Test**: Compares means from two independent groups without assuming equal population variances.

## Assumptions

- **Normality**: The relevant scores or differences should be approximately normally distributed, particularly for small samples.
- **Independence**: One-sample observations and independent-group observations should be independent; in a paired test, pairs should be independent, but observations within a pair are expected to be dependent.
- **Equal variances**: Required for the pooled independent test, but not for Welch’s test.

## Formulas

The general form is:

$$
t = \frac{\text{estimated effect} - \text{null effect}}{\text{standard error}}
$$

- **One-sample**: $t = \frac{\bar{x} - \mu_0}{s/\sqrt{n}}$, with $df = n - 1$.
- **Paired**: Let $d_i = x_i - y_i$. Then $t = \frac{\bar{d} - d_0}{s_d/\sqrt{n}}$, with $df = n - 1$.
- **Pooled independent two-sample**: $t = \frac{(\bar{x}_1 - \bar{x}_2) - \Delta_0}{s_p\sqrt{1/n_1 + 1/n_2}}$, where $s_p^2 = \frac{(n_1-1)s_1^2 + (n_2-1)s_2^2}{n_1+n_2-2}$ and $df = n_1+n_2-2$.
- **Welch**: $t = \frac{(\bar{x}_1 - \bar{x}_2) - \Delta_0}{\sqrt{s_1^2/n_1 + s_2^2/n_2}}$, with Welch–Satterthwaite degrees of freedom:

  $$
  df \approx \frac{(s_1^2/n_1 + s_2^2/n_2)^2}{(s_1^2/n_1)^2/(n_1-1) + (s_2^2/n_2)^2/(n_2-1)}.
  $$

## Interpretation

- **[P-value](../../../001_private/books/essential_math_for_data_science/p-value.md):** Used to determine the significance of the results.
  - A small [P-value](../../../001_private/books/essential_math_for_data_science/p-value.md) (typically ≤ 0.05) indicates strong evidence against the null hypothesis, so you reject the null hypothesis.
  - A large [P-value](../../../001_private/books/essential_math_for_data_science/p-value.md) (> 0.05) indicates weak evidence against the null hypothesis, so you fail to reject the null hypothesis.

> [!example]
> Used in research fields to compare:
>
> - Test scores
> - Medical treatment effects
> - [Behavioural](../03_mental_health_in_the_community/cognitive-behavioural_therapy.md) changes
