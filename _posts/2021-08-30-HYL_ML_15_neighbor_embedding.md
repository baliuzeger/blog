---
layout: post
title: "Notes for Prof. Hung-Yi Lee's ML Lecture 15: Neighbor Embedding"
---
# Manifold Learning

In some data set, it may be meaningless to compute the Euclidean distance directly, especially when the distance between examples are not small. Therefore, in such cases, if we want to perform dimension reduction, it has to be **non-linear**. Such dimension reduction may benefits for further clustering or supervised learning.


### Locally LInear Embedding


### T-distribution Stochastic Neighboring Embedding

By T-SNE, we have to calculate the KL-divergence for the whole data set, so we have to re-compute the whole transformation once we want to include more data. Therefore, T-SNE is not suitable for the scenarios of training and testing. (My question: why not compute only the newly generated probabilities? It seems that we can do it, so it should be not so problematic for computing cost when adding new data. By doing so, the transofrmation of the old examples effect those of the new examples significantly, so we should still re-compute the transformation for the whole old and new data if the amount of the new data is not relatively small to the old.)


## References

[Youtube ML Lecture 15: Unsupervised Learning - Neighbor Embedding](https://www.youtube.com/watch?v=GBUEjkpoxXc&list=PLJV_el3uVTsPy9oCRY30oBPNLCo89yu49&index=24)

[Course website](http://speech.ee.ntu.edu.tw/~tlkagk/courses_ML17_2.html)
