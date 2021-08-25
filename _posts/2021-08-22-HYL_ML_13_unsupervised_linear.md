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

When initializing the centers of the clusters, we randomly choose from the data set to avoid the segmentation fault that some clusters have no data points.

#### My discussion

Q: How about that some of the randomly chosen data points in initialization should actually belong to the same cluster?

A: It's possible, intuitively. However, since we just don't really know how many clusters should the data set be separated into, so possibly the better approach is to set the number $K$ slightly higher in the beginning and then we can manually merge the clusters later if we see some clusters are close to each other.

### Hierarchical Agglomerative Clustering

**Step 1: build a tree**

Find the closest 2 examples in the data set, make them a cluster, and then use their mean to represent this culser as a new data point. Repeat such process until getting the root, i.e. make the whole data set as a tree.

**Step 2: pick a threshold**

Choosw a level in the tree and separate the tree into clusters by that level.

<p align="center">
    <img src="https://baliuzeger.github.io/sjl/assets/images/HYL_ML_13/HAC.png" alt="HAC" style="width:500px;"/>
</p>

### More of My Discussions to Clustering

Aren't there any clustering methods based on low density separation assumption or smoothness assumption? Unsupervised SVM for the former? DBSCAN for the later?

## Distributed Representaion / Dimension Reduction

Transform the high-dimensional examples into low-dimensional representatils by using their attribute or characteristics.

<p align="center">
    <img src="https://baliuzeger.github.io/sjl/assets/images/HYL_ML_13/dimension-reduction.png" alt="dimension reduction" style="width:450px;"/>
</p>

### Feature Selection

Manually choose the dimensions of features that emphasizes the differences between the data points.

<p align="center">
    <img src="https://baliuzeger.github.io/sjl/assets/images/HYL_ML_13/feature-selection.png" alt="HAC" style="width:250px;"/>
</p>

### Principal Component Analysis

#### miximize variance after projection

By PCA, we project all the data points $x$ onto $W$ to get a set of $z$ of lower dimensions, while we want to find the $W$ to let the variance of $z$ be as large as possible.

![k-means steps](https://baliuzeger.github.io/sjl/assets/images/HYL_ML_13/pca-variance.png)

So we have

$$z = Wx$$

where

$$W = \begin{bmatrix}
(w^1)^T \\
(w^2)^T \\
\vdots \\
(w^n)^T \\
\end{bmatrix}$$

and

$$z_n = w^n \cdot x$$

$$w^n = arg \max \limits_{w^n} Var(z_n)$$

$$Var(z_n) = \frac{1}{N}\sum_{z^n}(z_n - \overline{z}_n)^2$$

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

More about PCA: Bishop Chap.12

[Youtube Link](https://youtube.com/playlist?list=PLJV_el3uVTsPy9oCRY30oBPNLCo89yu49)

[Course website](http://speech.ee.ntu.edu.tw/~tlkagk/courses_ML17_2.html)

