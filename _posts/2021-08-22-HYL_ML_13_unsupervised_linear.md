---
layout: post
title: "Notes for Prof. Hung-Yi Lee's ML Lecture 13: Supervised Learning- Linear Methods"
---

## Unsupervised Learning

only 1 end of function (input or output)

Clustering: only input 化繁為簡

Generation: Only ouput 無中生有

## Clustering

"How many cluster" is still an open question.

### K-Means

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

