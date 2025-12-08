#core/machinelearning

[[Types of Data|Data]] skew refers to the uneven distribution of data points within a dataset. It occurs when some values occur more frequently than others, leading to an imbalance in the data distribution. Skewed data can significantly impact statistical analysis and modelling in data science.

## There Are Two [[Types of Data]] Skew

![[data-skew.png]]

1. **Positive Skew (Right Skew):** The tail of the distribution is elongated towards the right, indicating a few extremely high values. The majority of the data is concentrated towards the lower values.
2. **Negative Skew (Left Skew):** The tail of the distribution is elongated towards the left, indicating a few extremely low values. The majority of the data is concentrated towards the higher values.

Dealing with data skew is important because it can affect the performance and accuracy of many statistical and machine learning algorithms. Skewed data can violate certain assumptions of these methods and lead to biased results.

## When to Use [[Measures of centre#Median|Median]] and When to Use [[Measures of centre#Mean|Mean]]

The choice between using median or mean depends on the nature of the data and the analysis objective:

1. **[[Measures of centre#Median|Median]]:** The median is a measure of central tendency representing a dataset’s middle value. It is suitable for skewed data or when extreme values (outliers) are present. The median is robust to outliers since it only considers the middle value and is less affected by extreme values.
2. **[[Measures of centre#Mean|Mean]]:** The mean is another measure of central tendency representing a dataset’s average value. It is appropriate for data that follows a symmetric distribution without significant skewness. However, the mean is sensitive to outliers since it takes into account all the values in the dataset.
