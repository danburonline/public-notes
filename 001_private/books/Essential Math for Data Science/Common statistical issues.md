#core/machinelearning

Statistical analyses are **prone to a variety of common pitfalls.** Being aware of these can help in designing better studies and interpreting results more reliably.

## 1. Bias and Sampling Issues

**Sources of Bias:**  
Have potential sources of bias in data collection, sampling, or analysis been considered? Failure to do so can invalidate results.

**Non-independence of Samples:**  
Treating non-independent samples with methods designed for independent samples can distort findings. Consider whether samples are clustered, paired, or otherwise related.

## 2. Assumptions of Statistical Tests

**Parametric Test Assumptions:**  
Using parametric tests (e.g., t-tests, ANOVA) when data or residuals are not normally distributed can lead to misleading conclusions. Always check assumptions before applying these tests.

## 3. Multiple Comparisons

**Multiple Testing Problem:**  
Not making corrections for multiple comparisons (such as the Bonferroni correction) increases the risk of Type I errors — falsely identifying significance.

## 4. Structural Issues in Data

**Ignoring Data Structure:**  
Overlooking clustering, grouping, or hierarchical ordering in data can underestimate variance and inflate Type I error rates. In such cases, hierarchical or multilevel analyses may be necessary.

## 5. Analysis of Effect Sizes

**Effect Size Differences Between Groups:**  
Failing to correctly analyse or report differences in effect sizes between groups can obscure meaningful results and lead to inaccurate inferences.
