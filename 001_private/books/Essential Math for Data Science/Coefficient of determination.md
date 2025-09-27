#core/mathematicalphysics #core/machinelearning

![[coefficient-of-determination.jpeg]]

- The Coefficient of Determination, denoted as R², is a statistical measure that represents the **proportion of the variance in the dependent variable that is predictable from the independent variable(s).**
- It is a key output of [[regression]] analysis and ranges from 0 to 1.

## Interpretation

- **0 R² Value:** Indicates that the model explains none of the variability of the response data around its mean.
- **1 R² Value:** Indicates that the model explains all the variability of the response data around its mean.

## Importance

- **Model Fit:** It helps in understanding how well our model fits the data.
- **Comparison:** Used to compare the explanatory power of [[regression]] models with different numbers of predictors.

## Limitations

- **Overfitting:** A high R² value does not necessarily imply that the model is good. It might overfit the data.
- **Not a Measure of Correctness:** It doesn’t indicate whether the [[regression]] model is the correct model.
- **Sensitive to Outliers:** R² can be significantly affected by outliers in the data.

## Usage

- Commonly used in linear [[regression]] but is also applicable to other types of [[regression]] models.
- It’s a quick tool to assess the strength of the relationship between variables.
