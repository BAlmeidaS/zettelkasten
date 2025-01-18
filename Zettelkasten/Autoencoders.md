---
tags:
  - deep-learning
aliases:
  - AE
  - latent variables
---
An **autoencoder** is a type of neural network designed to learn efficient representations of data in an unsupervised manner. It consists of two main components:

1. **Encoder**: This part compresses the input data into a lower-dimensional latent space by mapping the input to a compressed representation, often referred to as the latent variables or code.
    
2. **Decoder**: This part reconstructs the original input from the compressed latent representation.
    

The goal of an autoencoder is to minimize the difference between the original input and the reconstructed output, typically using a loss function like [[Mean squared Error|MSE]]. By doing so, it learns a compact and meaningful representation of the input data, which can be useful for tasks like conditionality reduction, denoising, or anomaly detection.

In an autoencoder algorithm, the variables from the lower-dimensional space are typically referred to as **latent variables** or the **latent representation**. This lower-dimensional space is often called the **latent space**, **bottleneck layer**, or simply the **encoding**.

These latent variables capture the compressed and essential features of the input data, which the autoencoder uses for reconstruction in the decoder.