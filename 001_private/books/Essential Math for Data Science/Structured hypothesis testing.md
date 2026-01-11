#core/artificialintelligence

Structured Hypothesis Testing is a **methodical approach that combines data collection and statistical analysis to test hypotheses.** It’s a robust method used in a variety of fields to make conclusions based on data.

## Steps in Structured Hypothesis Testing

1. **Develop a Hypothesis**: Formulate a clear, testable hypothesis. This usually includes a null hypothesis (no effect/difference) and an alternative hypothesis.
2. **Choose a Significance Level**: This is the probability of rejecting the null hypothesis when it is true, often denoted by α. Commonly used values include 0.05 and 0.01.
3. **Collect [[Types of Data|Data]]**: Collect relevant data through experiments, surveys, or observational studies.
4. **Perform a [[Common statistical issues|Statistical]] Test**: Conduct a statistical test to determine the [[P-value]], which is the probability of obtaining the observed data (or more extreme) if the null hypothesis is true.
5. **Make a Decision**: If the [[p-value]] is less than the significance level, reject the null hypothesis. If not, do not reject the null hypothesis.
6. **Report the Results**: Disclose the results, including the observed data, the statistical test used, the [[p-value]], and the conclusion.

> [!example]
> Let’s say you work for a pharmaceutical company that has developed a new drug. You want to test whether the drug is effective in reducing headache duration.
> 
> - **Null Hypothesis (H0)**: The drug has no effect on headache duration.
> - **Alternative Hypothesis (H1)**: The drug reduces headache duration.
> 
> You choose a significance level of 0.05 and collect data by having a sample of patients use the drug and record their headache duration. You perform a statistical test (e.g., a t-test) on the data.
> 
> If your [[p-value]] is less than 0.05, you would reject the null hypothesis and conclude that the drug is effective at reducing headache duration. If your [[p-value]] is greater than 0.05, you would not reject the null hypothesis, meaning you don’t have enough evidence to say the drug is effective.

> [!note]
> Remember, hypothesis testing doesn’t “prove” a hypothesis. It provides evidence to either support or refute it within the constraints of the chosen significance level and the quality and quantity of the data.
