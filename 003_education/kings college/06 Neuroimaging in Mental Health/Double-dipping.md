#core/appliedneuroscience

Double dipping in exploratory analysis refers to **the practice of using the same dataset for both selecting variables and performing subsequent analyses.** It can lead to biased results and invalid statistical inferences. Double dipping, also known as circular analysis, can occur when researchers explore the same data multiple times, potentially inflating the likelihood of finding false associations or patterns. It is recommended to avoid double dipping by using independent datasets for variable selection and analysis.

## Common Examples in Neuroimaging

Double dipping frequently occurs in [[fMRI image quality|fMRI]] studies when researchers:

- Select regions of interest (ROIs) based on voxels showing peak activation, then report statistics from those same voxels
- Use the same data to identify brain-behaviour correlations and then test their significance
- Apply feature selection and classification on identical datasets without cross-validation

These practices inflate effect sizes and produce non-replicable findings (see [[Neuroimaging analysis techniques]]).

## Statistical Consequences

Circular analysis produces:

1. **Inflated correlations**: Reported effect sizes appear larger than true population values
2. **Invalid p-values**: Statistical tests become non-independent, violating assumptions
3. **Poor generalisability**: Results fail to replicate in independent samples

## Prevention Strategies

To avoid double dipping:

- **Cross-validation**: Use separate training and test sets for model selection and evaluation
- **Independent localiser scans**: Define ROIs from separate scanning sessions
- **Pre-registration**: Specify analysis plans before data collection
- **Leave-one-subject-out**: Ensure independence between selection and testing across participants

See [[Comparison of neuroimaging methods]] for methodological considerations across imaging modalities.
