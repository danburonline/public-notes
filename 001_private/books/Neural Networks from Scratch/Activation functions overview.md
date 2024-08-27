#core/machinelearning

![[activation-functions.png]]

Activation functions in neural networks are **mathematical equations that determine the output of a neural network.** The function is **attached to each neuron in the network and determines whether it should be activated (“fired”) or not** based on whether each neuron’s input is relevant to the model’s prediction.

## Common Activation Functions

### Sigmoid

- **Formula**: $\sigma(x) = \frac{1}{1 + e^{-x}}$
- **Output range**: (0, 1)
- **Characteristics**: Smooth gradient, saturates and kills gradients during backpropagation, not zero-centered.

### Tanh

- **Formula**: $\tanh(x) = \frac{2}{1 + e^{-2x}} - 1$
- **Output range**: (-1, 1)
- **Characteristics**: Zero-centered, which makes optimisation easier.

### ReLU (Rectified [[Regression#2. Linear Regression|Linear]] Unit)

- **Formula**: $f(x) = \max(0, x)$
- **Output range**: [0, ∞)
- **Characteristics**: Prevents vanishing gradient problem and speeds up training.

### Leaky ReLU

- **Formula**: $f(x) = \max(0.01x, x)$
- **Output range**: (-∞, ∞)
- **Characteristics**: Attempts to fix the “dying ReLU” problem.

### Parametric ReLU

- **Formula**: $f(x) = \max(\alpha x, x)$
- **Output range**: (-∞, ∞)
- **Characteristics**: Allows the negative slope to be learned.

### ReLU6

- **Formula**: $f(x) = \min(\max(0, x), 6)$
- **Output range**: [0, 6]
- **Characteristics**: Similar to ReLU but with a capped maximum value.

### [[Softmax]]

- **Formula**: $\sigma(\mathbf{z})*i = \frac{e^{z_i}}{\sum*{j=1}^{K} e^{z_j}}$
- **Characteristics**: Converts logits to probabilities (for multi-class classification).

### Binary Step

- **Formula**: $f(x) = \begin{cases} 1 & \text{if } x > 0 \\ 0 & \text{otherwise} \end{cases}$
- **Characteristics**: Outputs a binary result, used for binary classifiers.

### Identity

- **Formula**: $f(x) = x$
- **Characteristics**: Output is the same as the input, used in regression problems.

### Swish

- **Formula**: $f(x) = \frac{x}{1 + e^{-x}}$
- **Characteristics**: Non-monotonic, smooth, and non-saturating.

### Hard Swish

- **Formula**: $f(x) = x \cdot \text{ReLU6}(x + 3) / 6$
- **Characteristics**: Piecewise linear approximation of Swish, more computationally efficient.
