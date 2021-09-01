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

## Text-Retrieval and Image Search

For text-retrieval, by the vector space model, we transform documents and also the query into vectors, and then we retrieve the documents by their similarities to the vector of the query.

<p align="center">
    <img src="https://baliuzeger.github.io/sjl/assets/images/HYL_ML_16/document-vector-space.png" alt="document vector space" style="width:350px;"/>
</p>

However, by only the bag-of-word model, the semantics are not considered.

<p align="center">
    <img src="https://baliuzeger.github.io/sjl/assets/images/HYL_ML_16/bag-of-words.png" alt="bag-of-word" style="width:350px;"/>
</p>

If we further train an auto-encoder by the bag-of-word vectors of the documents, we can get good reslults for text-retrieval.

![auto-encoder text-retrieval](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_16/auto-encoder-text-retrieval.png)



## Auto-Encoder for CNN

## Use Auto-Encoder to Pre-Train DNN

## References

[Youtube ML Lecture 16: Unsupervised Learning - Auto-encoder](https://www.youtube.com/watch?v=Tk5B4seA-AU&list=PLJV_el3uVTsPy9oCRY30oBPNLCo89yu49&index=25)

[Course website](http://speech.ee.ntu.edu.tw/~tlkagk/courses_ML17_2.html)
