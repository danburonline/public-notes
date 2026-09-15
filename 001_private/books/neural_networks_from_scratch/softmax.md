#core/artificialintelligence

Softmax is a **mathematical function used in the output layer of neural network models that handle multi-class classification problems.** It converts the raw output scores (also known as logits) into probabilities that sum up to one.

## Formula

The softmax function is expressed as:

$$
\operatorname{softmax}(\mathbf{z})_i = \frac{\exp(z_i)}{\sum_{j=1}^{K} \exp(z_j)}
$$

Where:

- $\operatorname{softmax}(\mathbf{z})_i$ is the output of the softmax function for the $i$-th class.
- $z_i$ is the $i$-th element from the input vector $\mathbf{z}$, representing the raw score for the class $i$.
- $K$ is the total number of classes.

## Characteristics

- **Probabilistic Interpretation**: The output can be interpreted as a probability distribution over the classes.
- **Differentiable**: It allows the use of gradient-based optimisation methods.
- **Exp Function**: Using the exponential function ensures that the output is non-negative and enhances the differences between the input values.

## Applications

- **Classification Tasks**: Primarily used in multi-class classification problems in various domains like image recognition, language modelling, etc.
- **[Reinforcement](../../../003_education/kcl/02_psychological_foundations/reinforcement_schedules.md) Learning**: Used in policy gradient methods where the actions are discrete.

## Example

Consider the problem of classifying an image into one of three classes (Cat, Dog, Rabbit). The raw outputs from the neural network might be [2.0, 1.0, 0.1]. Applying softmax will convert these logits into probabilities like [0.7, 0.2, 0.1], indicating the network’s prediction.

## Cautions

- **Numerical Stability**: Subtracting the largest logit before exponentiating gives the equivalent stable calculation $\operatorname{softmax}(\mathbf{z})_i = \frac{\exp(z_i-m)}{\sum_j \exp(z_j-m)}$, where $m = \max_k z_k$.
- **Binary Classification**: A two-logit softmax is valid. A sigmoid is a common equivalent parameterisation: with logits $z_0$ and $z_1$, $\operatorname{softmax}(\mathbf{z})_1 = \operatorname{sigmoid}(z_1-z_0)$.
