---
layout: post
title: "Notes for Prof. Hung-Yi Lee's ML Lecture 13: Unsupervised Learning- Linear Methods"
---

# Unsupervised Learning

Unsupervised learning are the scenarios that we only have either input or output for the function. Examples for the former （化繁為簡） are dimension reduction and clustering, while an example for the later （無中生有） is generation.

## Clustering

"How many cluster" is still an open question; we have to decide it.

### K-Means

To cluster $X = \{ x^1, \dots, x^N \}$ into $K$ clusters.

Steps:

![k-means steps](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_13/k-means.png)

### Hierarchical Agglomerative Clustering

## Distributed Representaion / Dimension Reduction


### Feature Selection

### Principal Component Analysis

#### miximize variance after projection

#### minimize reproduction error (looks like neural network with 1 hidden layer)

gradient gets different w's due to not orthogonal

#### Discussion

keep the distanvces from high to low dimensional space

weakness: unsupervised

Linear Discriminant Analysis: 考慮 label 的降維

why PCA w's 不像圖案的組成要素 / non-negative matrix factorization

### Matrix Factorization

#### SVD to minimize recostruction error

#### gradient descent

(can handle missing value)

加上 bias

#### More

[Netflix](https://dl.acm.org/doi/10.1145/2843948)

### More Approaches





## References
[Youtube Link](https://youtube.com/playlist?list=PLJV_el3uVTsPy9oCRY30oBPNLCo89yu49)

[Course website](http://speech.ee.ntu.edu.tw/~tlkagk/courses_ML17_2.html)

