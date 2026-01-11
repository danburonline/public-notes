#core/artificialintelligence

![[variance-and-standard-deviation.png]]

[[Binomial distribution#Mean and Variance|Variance]] and standard deviation are widely **used measures of dispersion in statistics, meaning they describe how a set of data is spread out.** They give you a sense of how much the values in a dataset differ from the mean (average).

## Variance

Variance is the average of the squared differences from the mean. In other words, it’s a numerical value that describes how much the numbers in the dataset vary from the average value.

### Calculation

1. Find the mean of the dataset.
2. Subtract the mean from each number in the dataset and then square the result (the squared difference).
3. Average the squared differences.

---

## Standard Deviation

The standard deviation is a measure of the amount of variation or dispersion of a set of values. It’s the square root of the variance, and it’s useful because it’s in the same units as the original data.

### Calculation

1. Calculate the variance.
2. Take the square root of the variance.

---

## Key Concepts

- **Population vs. Sample:** When calculating variance and standard deviation, the formula you use will depend on whether you are considering a population (all members of a defined group) or a sample (a subset of the population). The formulas slightly differ in the denominator, where population variance uses `N` (the number of scores) and sample variance uses `N-1` to compensate for sample bias.
- **Units:** Variance has squared units (e.g., square meters), which can make it hard to interpret in the context of the original data. On the other hand, standard deviation has the same units as the original data, making it easier to interpret.
