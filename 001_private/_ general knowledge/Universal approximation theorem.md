#lead/cognitivecomputing #core/machinelearning

![[universal-approximation-theorem.png]]

The Universal approximation theorem is a key theorem in the field of neural networks, **stating that a feed-forward network with a single hidden layer containing a finite number of neurons can approximate any continuous function to a desired level of accuracy.** This holds when the activation function is non-constant, bounded, and monotonically-increasing continuous.

## Key Points

### Applicability

- The theorem is applicable to functions defined on compact subsets of $\mathbb{R}^n.$
- It implies that simple neural architectures can theoretically model complex functions.

### Importance

- Provides a theoretical foundation for using neural networks in various machine learning tasks such as [[regression]], classification, and other complex pattern recognition tasks in data.

### Limitations

- The theorem does not ensure that the neural network will learn efficiently.
- It does not address the generalisation of the learned model to new, unseen data.

### Practical Implications

- As a machine learning engineer, understanding this theorem helps in grasping why neural networks can be effective in diverse applications.
- It emphasises the importance of choosing appropriate activation functions and designing network architectures that balance complexity and performance.
