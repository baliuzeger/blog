---
layout: post
title: "Notes for Prof. Hung-Yi Lee's ML Lecture: Deep Generative Model"
---

## Component by Component

Let the model to generate the product component by component.

### Pixel RNN

Train an RNN to take all the preceding pixels as input and then generate the next pixel. It can be trained just with a large collection of images without any annotation.

![pixel RNN](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_17/pixel-RNN.png)

## Auto-Encoder

Usually, we don't get good results by simply using a decoder trained by an auto-encoder and then using randomly generated code to generate products. We need some tricks.

### Variational Auto-Encoder

![VAE](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_17/VAE.png)

We can tune 2 dimensions of the code and fix all the other dimensions to see the function of each dimension, and then control the generation of images fo the known functions of the simensions of the codes. Take the pokemon generation as example,

![pokemon generation](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_17/pokemon_gen.png)

## Discussion

How to evaluate the performance is a difficult problem for using the generative models.

## References

[Youtube ML Lecture 17: Unsupervised Learning - Deep Generative Model (Part I)](https://www.youtube.com/watch?v=YNUek8ioAJk&list=PLJV_el3uVTsPy9oCRY30oBPNLCo89yu49&index=29)

[Course website](https://speech.ee.ntu.edu.tw/~hylee/ml/2020-spring.html)
