#core/artificialintelligence

![[autoencoder.png]]

An autoencoder is a type of artificial neural network used for unsupervised learning. It is primarily **employed in data compression, dimensionality reduction, and feature extraction tasks.** The network consists of an encoder that **transforms the input data into a compressed representation (encoding) and a decoder that reconstructs the original data from the encoded representation.** The objective of an autoencoder is to minimise the reconstruction error, which encourages the network to learn useful features in the encoded representation.

## Architecture

The basic autoencoder consists of:

- **Encoder**: Maps input $x$ to [[Latent space]] representation $z$ via $z = f(x)$
- **Bottleneck**: The compressed representation with fewer dimensions than the input
- **Decoder**: Reconstructs input from latent representation via $\hat{x} = g(z)$

The network is trained to minimise reconstruction loss $L(x, \hat{x})$, typically mean squared error or cross-entropy.

## Variants

| Type | Modification | Use Case |
|------|--------------|----------|
| **Variational (VAE)** | Learns probability distribution in latent space | Generative modelling |
| **Denoising** | Trained to reconstruct from corrupted inputs | Robust feature learning |
| **Sparse** | Regularisation enforces sparsity in encoding | Feature selection |
| **Contractive** | Penalises sensitivity to input variations | Stable representations |

## Applications

- **Dimensionality reduction**: Alternative to PCA for nonlinear relationships
- **Anomaly detection**: High reconstruction error signals out-of-distribution samples
- **Generative models**: VAEs sample from latent space to generate new data
- **Pretraining**: Learn representations before supervised fine-tuning

See [[Dense layers]] for the building blocks and [[Universal approximation theorem]] for theoretical foundations.