#core/machinelearning

![[dense-layers.png]]

Dense layers, or fully connected layers, are the **most straightforward and fundamental layers in neural networks.** They are core components of many deep learning models.

## Definition

A dense layer is a neural network layer where **each input node is connected to each output node.**

## Mathematical Representation

The output of a dense layer is calculated using matrix multiplication of the inputs and the layer’s weights, followed by adding a bias term and applying an activation function.

$$
\mathbf{y} = f(\mathbf{Wx} + \mathbf{b})
$$

Where:
- $\mathbf{x}$ is the input vector.
- $\mathbf{W}$ is the weight matrix.
- $\mathbf{b}$ is the bias vector.
- $\mathbf{y}$ is the output vector.
- $f$ is the activation function.

## Functionality

- **Feature Transformation**: Dense layers transform input features into a space where features are more separable.
- **Learning Non-linear Combinations**: With activation functions, dense layers can learn complex non-linear mappings from inputs to outputs.

## Usage

- **Output Layer**: Often used as the last layer in a network to produce output predictions.
- **Hidden Layers**: Can be stacked to form a deep network capable of learning sophisticated patterns.

## Parameters

- **Weights**: Learnable parameters adjusted during training to minimise the loss function.
- **Biases**: Additional learnable parameters allow the layer to adapt its output independently of the weighted sum of its inputs.

## Training

- **Backpropagation**: Dense layers are trained using backpropagation and an optimisation algorithm like SGD, Adam, etc.
- **Regularisation**: Techniques like L1, L2 regularisation, or dropout may be applied to prevent overfitting.
