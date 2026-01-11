#core/artificialintelligence

Softmax is a **mathematical function used in the output layer of neural network models that handle multi-class classification problems.** It converts the raw output scores (also known as logits) into probabilities that sum up to one.

## Formula

The softmax function is expressed as:

$$
\sigma(\mathbf{z})*i = \frac{e^{z_i}}{\sum*{j=1}^{K} e^{z_j}}
$$

Where:
- $\sigma(\mathbf{z})*i$ is the output of the softmax function for the $i$-th class.
- $z_i$ is the $i$-th element from the input vector $\mathbf{z}$, representing the raw score for the class $i$.
- $K$ is the total number of classes.

## Characteristics

- **Probabilistic Interpretation**: The output can be interpreted as a probability distribution over the classes.
- **Differentiable**: It allows the use of gradient-based optimisation methods.
- **Exp Function**: Using the exponential function ensures that the output is non-negative and enhances the differences between the input values.

## Applications

- **Classification Tasks**: Primarily used in multi-class classification problems in various domains like image recognition, language modelling, etc.
- **[[Reinforcement schedules|Reinforcement]] Learning**: Used in policy gradient methods where the actions are discrete.

## Example

Consider the problem of classifying an image into one of three classes (Cat, Dog, Rabbit). The raw outputs from the neural network might be [2.0, 1.0, 0.1]. Applying softmax will convert these logits into probabilities like [0.7, 0.2, 0.1], indicating the network’s prediction.

## Cautions

- **Numerical Stability**: Direct softmax computation might involve large or small exponentials. To avoid this, a normalisation trick is often used.
- **Not Suitable for Binary Classification**: For binary classification problems, the sigmoid function is typically used.
