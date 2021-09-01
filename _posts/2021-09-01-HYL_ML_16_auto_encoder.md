---
layout: post
title: "Notes for Prof. Hung-Yi Lee's ML Lecture 16: Auto-Encoder"
---

By the concept of auro-encoder, we train an NN encoder and an NN decoder simultzneously. The encoder is a function that generate a code by the input, and the decoder is a function that generate an output by a code. To train them, we cascade the decoder after the decoder, and train the cascaded neural network to reproduce outputs that are as close as the inputs.

![auto-encoder](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_16/auto-encoder.png)

Comparing to principal component analysis, the auto-encoder's training is like minimizing the reconstruction error in PCA. Combining the encoding and decoding parts of PCA as an auto-encoder, we can see the code as the output of the hidden layer. For dimension reduction, normally the code has the lowerest dimensionality in the whole auto-encoder, so it's also the **bottleneck** layer.

![PCA as auto-encoder](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_16/PCA-auto-encoder.png)

## Deep Auto-Encoder

Of course, the auto-encoder can be deep, so it's deep auto-encoder.

![deep auto-encoder](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_16/deep-auto-encoder.png)

It's not necessary to make the weights in the encoder and the decoder be symmetric. By applying the constrain of symmetry, we can reduce the number of parameters.

(My question: **is the initialization by RBM still necessary for training auto-encoders today? No?**)

By making the auto-encoder deep, the generated code can seperate the different classes of the examples, although without supervised learning.

![deep auto-encoder separate classes](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_16/deep-auto-encoder-separate.png)



## References

[Youtube ML Lecture 16: Unsupervised Learning - Auto-encoder](https://www.youtube.com/watch?v=Tk5B4seA-AU&list=PLJV_el3uVTsPy9oCRY30oBPNLCo89yu49&index=25)

[Course website](http://speech.ee.ntu.edu.tw/~tlkagk/courses_ML17_2.html)
